# EVA Webhooks API

> ### Vorläufiger Entwurf

Über die EVA Webhook API können sich externe Systeme für Webhooks registrieren, die bei gewissen Events im EVA-System automatisiert ausgelöst werden. Die externen Systeme können dann als Reaktion vordefinierte Daten abrufen oder verändern.

Jede EVA-Clubapp hat eine eigene Webhook-API. 

## Eventtypen
Die folgenden Events sind definiert. Webhooks können auf einen oder mehrere Eventtypen registriert werden.

### event `main_contract_activated`
Wird ausgelöst, wenn ein Nutzer einen Hauptvertrag aktiviert/bestätigt hat.

### event `addon_booked`
Wird ausgelöst, wenn ein Nutzer ein Addon-Abo gebucht hat.

### event `abo_terminated`
Wird ausgelöst, wenn ein Nutzer ein Addon oder einen Hauptvertrag gekündigt hat.

### event `abo_renewed`
Wird ausgelöst, wenn ein Addon oder ein Hauptvertrag automatisiert verlängert wurde.

### event `ping`
Event ohne Bedeutung, zum Test eines Webhooks.

## Webhooks konfigurieren

Webhooks werden im Appsite-Admin konfiguriert.
Die folgenden Felder müssen ausgefüllt werden, um einen neuen Webhook für eine EVA-Clubapp zu registrieren:

- `url` - Ziel-URL des externen Systems, die über den Webhook aufgerufen werden soll
- `header` - Key/Value-Map für zusätzliche HTTP-Header. Darüber kann eine Authentifizierung abgebildet werden, z.B. `x-eva-webhook-secret: mysecret`
- `events` - Liste der Event-Typen, für die der Webhook ausgelöst werden soll
- `active` - ein Webhook kann aktiviert und deaktiviert werden.

Ein Webhook macht **immer** einen HTTP POST Request an `url`, mit optionalen `header`-Angaben im HTTP-Header. Der Content-Type ist **immer** `application/json`. Der POST Body hat immer die gleiche Struktur:

```json
{
  "data": {
    "event_type": "main_contract_activated",
    "event_id": "0bda708c-de39-466c-86fc-1ff48c36f489",
    "timestamp": "2021-07-21T09:13:08.377Z",
    "franchise": "dsbeva"
  },
  "links": {
    "related": "https://dsb-layer.entrecode.de/dsbeva/exportapi/abo_booking?id=qyAIXmsqpi&event=0bda708c-de39-466c-86fc-1ff48c36f489"
  }
}
```

- `data.event_type` entspricht einem der oben definierten Eventtypen (String)
- `data.event_id` ist eine eindeutige ID für dieses event (String)
- `data.timestamp` ist der genaue Zeitpunkt des Events als ISO 8601 Timestamp mit Zeitzonenangabe (String)
- `data.franchise` ist der Identifier der EVA-Clubapp ("seoTitle"). Dadurch ist es möglich, dass ein externes System Webhooks von verschiedenen EVA-Clubapps entgegennimmt (String)
- `links.related` ist eine URL, über die zugehörige Event-Daten abgerufen werden können, siehe unten. Ein Ping-Event enthält keine URL (String)

Es wird erwartet, dass der POST-Request mit einem HTTP-Statuscode 2xx (z.B. 200) quittiert wird. Ein Statuscode >= 300 wird nicht unterstützt bzw. als Fehler gewertet.

## Abruf von Daten
Der POST-Body eines Webhooks enthält immer eine URL, über die das externe System die genauen Daten abrufen kann. 

> Die Struktur der URL kann sich ändern. Sie ist außerdem unterschiedlich für jedes Event. Die URL kann **nicht** selbst zusammengebaut werden!

Die Daten können nur mit einem gültigen API Key im Authorization-Header abgerufen werden.

```sh
curl -XGET -H 'Authorization: Bearer YOURTOKENHERE' -H "Content-Type: application/json" 'https://dsb-layer.entrecode.de/dsbeva/exportapi/abo_booking?id=qyAIXmsqpi&event=0bda708c-de39-466c-86fc-1ff48c36f489'
```

```json
{
	"data": {
	  "abo_booking_id": "qyAIXmsqpi",
	  ...
	  "abo_definition": {
	    "abo_definition_id": "odASDms3i",
	    "title": "Flexi Abo",
	    ...
	  },
	  "user": {
	    "email": "youruser@gmail.com",
	    "memberID": null,
	    ...
	  }
	}
}
```

### memberID setzen

Sofern ein Nutzer noch keine `memberID` hat, kann diese über einen PUT-Request an die gleiche URL gesetzt werden:

```sh
curl -XPUT -H 'Authorization: Bearer YOURTOKENHERE' -H "Content-Type: application/json" -d '{"data": {"user": {"memberID": "newMemberID123"}}}' 'https://dsb-layer.entrecode.de/dsbeva/exportapi/abo_booking?id=qyAIXmsqpi&event=0bda708c-de39-466c-86fc-1ff48c36f489'
```
Die Response ist gleich wie bei GET und wird mit Statuscode 200 bestätigt. 

### Fehlerfälle

- Statuscode 400: PUT-Body fehlerhaft
- Statuscode 401: Authentifizierung fehlgeschlagen
- Statuscode 403: Authorisierung fehlgeschlagen
- Statuscode 404: Event nicht gefunden
- Statuscode 429: Zu viele Requests in zu kurzer Zeit


## Event Log
Das Eventlog kann im Appsite-Admin abgerufen werden.

- Events eines Webhooks

oder

- Events einer Buchung

Die Events enthalten einen Status, ob bereits mit einem GET oder PUT darauf reagiert wurde.

Es gibt die Möglichkeit, ein Event erneut an einen Webhook zu senden.

## API Keys
Für den Datenabruf wird ein valider API Key benötigt.
API Keys können im Appsite-Admin angelegt werden. Er kann nur beim Anlegen eingesehen werden und muss sofort gespeichert werden. API Keys können auch widerrufen werden. 

Die Berechtigungen, welche Events von welchem API Key abgerufen werden können, können individuell angepasst werden.