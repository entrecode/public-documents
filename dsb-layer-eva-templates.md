# DSB-Layer Templates Documentation

Markdown:

- [AGB, SEPA, PRIVACY, NEWSLETTER](#agb-sepa-privacy-newsletter)

Fabric:

- [contract-BCK\$entryid](#contract-bckentryid)

Mail:

- [MembershipActivation](#membershipactivation)
- [MemberWelcome](#memberwelcome)
- [TerminationConfirmation](#terminationconfirmation)
- [AddonBookedConfirmation](#addonbookedconfirmation)
- [Recommendation](#recommendation)


## Markdown-Templates

# AGB, SEPA, PRIVACY, NEWSLETTER

- usage: `termsForEVA` (html), AGB and PRIVACY also in `addDocumentsToEVAMembership` (pdf)
- data is full `onboarding` entry:

```js
[
  {
    identifier: 'company_name',
    value: '{{company_name}}',
    description: 'Firmenname',
    placeholder: 'Mein Club GmbH',
  },
  {
    identifier: 'company_phone',
    value: '{{company_phone}}',
    description: 'Öffentliche Telefonnummer',
    placeholder: '+49 711 12341234',
  },
  {
    identifier: 'company_mail',
    value: '{{company_mail}}',
    description: 'Öffentliche E-Mail-Adresse',
    placeholder: 'info@meinclub.de',
  },
  {
    identifier: 'company_zip',
    value: '{{company_zip}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'company_street',
    value: '{{company_street}}',
    description: 'Straße',
    placeholder: 'Straße 123',
  },
  {
    identifier: 'company_country',
    value: '{{company_country}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'company_city',
    value: '{{company_city}}',
    description: 'Stadt',
    placeholder: 'Musterstadt',
  },
  {
    identifier: 'manager_name',
    value: '{{manager_name}}',
    description: 'Name der Geschäftsführung',
    placeholder: 'Maxi Musterperson',
  },
  {
    identifier: 'manager_mail',
    value: '{{manager_mail}}',
    description: 'E-Mail der Geschäftsführung',
    placeholder: 'chef@meinclub.de',
  },
  {
    identifier: 'manager_phone',
    value: '{{manager_phone}}',
    description: 'Durchwahl-Telefonnummer der Geschäftsführung',
    placeholder: '+49 711 12341234',
  },
  {
    identifier: 'company_type',
    value: '{{company_type}}',
    description: 'Gesellschaftsform',
    placeholder: 'GmbH',
  },
  {
    identifier: 'commercial_register_number',
    value: '{{company_type}}',
    description: 'Handelsregister-Nr.',
    placeholder: 'HRB 123456',
  },
  {
    identifier: 'commercial_register_name',
    value: '{{company_type}}',
    description: 'Handelsregister (Ort)',
    placeholder: 'Amtsgericht Musterstadt',
  },
  {
    identifier: 'vat_number',
    value: '{{vat_number}}',
    description: 'USt-ID.',
    placeholder: 'DE123456789',
  },
]
```

## Fabric-Templates

# contract-BCK\$entryid

- usage: `addDocumentsToEVAMembership ` (pdf)
- data is full `eva_membership` entry (level 2) and the calculated dates:

```js
[
  {
    identifier: 'id',
    value: '{{membershipEntry.id}}',
    description: 'Membership-EntryID',
    placeholder: 'XW5jiXoPPf',
  },
  {
    identifier: 'membershipRequestID',
    value: '{{membershipEntry.membershipRequestID}}',
    description: 'Membership-Request-ID',
    placeholder: '1023',
  },
  {
    identifier: 'club.id',
    value: '{{membershipEntry.club.id}}',
    description: 'Club-ID',
    placeholder: 'YX4wsYoZZr',
  },
  {
    identifier: 'club.id',
    value: '{{membershipEntry.club.name}}',
    description: 'Club-Name',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'club.studioNumber',
    value: '{{membershipEntry.club.studioNumber}}',
    description: 'Club-Studionummer',
    placeholder: '123',
  },
  {
    identifier: 'club.owner',
    value: '{{membershipEntry.club.owner}}',
    description: 'Club-Besitzer',
    placeholder: 'Alex Besitzer',
  },
  {
    identifier: 'club.addressStreet',
    value: '{{membershipEntry.club.addressStreet}}',
    description: 'Club-Straße',
    placeholder: 'Pumperstraße 123',
  },
  {
    identifier: 'club.addressZipCode',
    value: '{{membershipEntry.club.addressZipCode}}',
    description: 'Club-PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'club.addressCity',
    value: '{{membershipEntry.club.addressZipCode}}',
    description: 'Club-Stadt',
    placeholder: 'Musterdorf',
  },
  {
    identifier: 'club.addressCountryCode',
    value: '{{membershipEntry.club.addressCountryCode}}',
    description: 'Club-Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'club.addressCo',
    value: '{{membershipEntry.club.addressCo}}',
    description: 'Club-Adresse C/O',
    placeholder: 'Businesspark 2A',
  },
  {
    identifier: 'club.bankAccountIBAN',
    value: '{{membershipEntry.club.bankAccountIBAN}}',
    description: 'Club-IBAN',
    placeholder: 'DE11500105172878648336',
  },
  {
    identifier: 'club.bankAccountBIC',
    value: '{{membershipEntry.club.bankAccountBIC}}',
    description: 'Club-BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'club.bankAccountBankName',
    value: '{{membershipEntry.club.bankAccountBankName}}',
    description: 'Club-Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'club.bankAccountOwner',
    value: '{{membershipEntry.club.bankAccountBankName}}',
    description: 'Club-Kontoinhaber',
    placeholder: 'Alex Besitzer',
  },
  {
    identifier: 'club.contactEmail',
    value: '{{membershipEntry.club.contactEmail}}',
    description: 'Club-E-Mail',
    placeholder: 'info@meinclub.de',
  },
  {
    identifier: 'club.contactMobile',
    value: '{{membershipEntry.club.contactEmail}}',
    description: 'Club-Mobilnummer',
    placeholder: '+49 1515 12341234',
  },
  {
    identifier: 'club.contactPhone',
    value: '{{membershipEntry.club.contactPhone}}',
    description: 'Club-Telefonnummer',
    placeholder: '+49 711 23456789',
  },
  {
    identifier: 'club.sepaUci',
    value: '{{membershipEntry.club.sepaUci}}',
    description: 'Club-SEPA-UCI',
    placeholder: 'XX123123',
  },
  {
    identifier: 'club.uStId',
    value: '{{membershipEntry.club.uStId}}',
    description: 'Club-USt-ID.',
    placeholder: 'DE123456789',
  },
  {
    identifier: 'membershipTemplate.id',
    value: '{{membershipEntry.membershipTemplate.id}}',
    description: 'Vertragsvorlagen-ID',
    placeholder: 'ZRXxx7Z45',
  },
  {
    identifier: 'membershipTemplate.title',
    value: '{{membershipEntry.membershipTemplate.title}}',
    description: 'Vertrags-Titel',
    placeholder: 'Flexo Abo',
  },
  {
    identifier: 'membershipTemplate.type',
    value: '{{membershipEntry.membershipTemplate.type}}',
    description: 'Vertrags-Art',
    placeholder: 'addon',
  },
  {
    identifier: 'membershipTemplate.initialPrice',
    value: '{{membershipEntry.membershipTemplate.initialPrice | currency}}',
    description: 'Einrichtungsgebühr',
    placeholder: '2900',
  },
  {
    identifier: 'membershipTemplate.mainInterval',
    value: '{{membershipEntry.membershipTemplate.mainInterval | interval}}',
    description: 'Abrchnungsintervall',
    placeholder: 'P1M',
  },
  {
    identifier: 'membershipTemplate.mainIntervalPrice',
    value: '{{membershipEntry.membershipTemplate.mainIntervalPrice | currency}}',
    description: 'Grundpreis',
    placeholder: '2999',
  },
  {
    identifier: 'membershipTemplate.initialIntervalDuration',
    value: '{{membershipEntry.membershipTemplate.initialIntervalDuration | interval}}',
    description: 'Rabattdauer',
    placeholder: 'P3M',
  },
  {
    identifier: 'membershipTemplate.initialIntervalPrice',
    value: '{{membershipEntry.membershipTemplate.initialIntervalPrice | currency}}',
    description: 'Rabattpreis',
    placeholder: '1999',
  },
  {
    identifier: 'membershipTemplate.administrationFeeInterval',
    value: '{{membershipEntry.membershipTemplate.administrationFeeInterval | interval}}',
    description: 'Verwaltungsgebühren-Intervall',
    placeholder: 'P1Y',
  },
  {
    identifier: 'membershipTemplate.administrationFee',
    value: '{{membershipEntry.membershipTemplate.administrationFee | currency}}',
    description: 'Verwaltungsgebühr',
    placeholder: '9999',
  },
  {
    identifier: 'membershipTemplate. initialAdministrationFeeDuration',
    value: '{{membershipEntry.initialAdministrationFeeDuration | interval}}',
    description: 'Rabattdauer Verwaltungsgebühr',
    placeholder: 'P1Y',
  },
  {
    identifier: 'membershipTemplate.initialAdministrationFee',
    value: '{{membershipEntry.membershipTemplate.initialAdministrationFee | currency}}',
    description: 'Anfangs-Verwaltungsgebühr',
    placeholder: '4999',
  },
  {
    identifier: 'membershipTemplate.initialDuration',
    value: '{{membershipEntry.membershipTemplate.initialDuration | interval}}',
    description: 'Grundlaufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'membershipTemplate.renewalDuration',
    value: '{{membershipEntry.membershipTemplate.renewalDuration | interval}}',
    description: 'Verlängerungs-Laufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'membershipTemplate.terminationNoticePeriod',
    value: '{{membershipEntry.membershipTemplate.terminationNoticePeriod | interval}}',
    description: 'Kündigungsfrist',
    placeholder: 'P1M',
  },
  {
    identifier: 'membershipTemplate.useFullIntervals',
    value: '{{membershipEntry.membershipTemplate.useFullIntervals}}',
    description: 'Volle Abrechnungszeiträume',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.terminationOn15thBefore',
    value: '{{membershipEntry.membershipTemplate.terminationOn15thBefore}}',
    description: 'Kündigung zum 15. des Vormonats',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.freeTrialPeriod',
    value: '{{membershipEntry.membershipTemplate.freeTrialPeriod | interval}}',
    description: 'Kostenloser Testzeitraum',
    placeholder: 'P2W',
  },
  {
    identifier: 'membershipTemplate.initialPriceIgnoresFreeTrialPeriod',
    value: '{{membershipEntry.membershipTemplate.initialPriceIgnoresFreeTrialPeriod}}',
    description: 'Einrichtungsgebühr ignoriert Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.autoAddons',
    value: '{{membershipEntry.membershipTemplate.autoAddons}}',
    description: 'Automatisch zugebuchte Addons',
    placeholder: [{_entryID: 'Kaffee'}],
  },
  {
    identifier: 'membershipTemplate.requiresAddons',
    value: '{{membershipEntry.membershipTemplate.requiresAddons}}',
    description: 'Erforderliche Abos',
    placeholder: [],
  },
  {
    identifier: 'membershipTemplate.isStandalone',
    value: '{{membershipEntry.membershipTemplate.isStandalone}}',
    description: 'Eigenständiger Vertrag',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.isBookableFrom',
    value: '{{membershipEntry.membershipTemplate.isBookableFrom | date}}',
    description: 'Buchbar ab',
    placeholder: '2021-02-12',
  },
  {
    identifier: 'membershipTemplate.isBookableTo',
    value: '{{membershipEntry.membershipTemplate.isBookableTo | date}}',
    description: 'Buchbar bis',
    placeholder: '2035-03-05',
  },
  {
    identifier: 'membershipTemplate.minimumMembershipAge',
    value: '{{membershipEntry.membershipTemplate.minimumMembershipAge}}',
    description: 'Mindestalter',
    placeholder: '16',
  },
  {
    identifier: 'accountID',
    value: '{{membershipEntry.account.accountID}}',
    description: 'Account-ID',
    placeholder: '833750b6-38c2-4304-848a-fa6d96cb1c82',
  },
  {
    identifier: 'email',
    value: '{{membershipEntry.account.email}}',
    description: 'E-Mail',
    placeholder: 'eva.adams@gmail.com',
  },
  {
    identifier: 'state',
    value: '{{membershipEntry.state}}',
    description: 'Mitgliedschafts-Status',
    placeholder: 'finished',
  },
  {
    identifier: 'aboBooking.id',
    value: '{{membershipEntry.aboBooking.id}}',
    description: 'Buchungs-ID',
    placeholder: 'XxT9kkKKOx',
  },
  {
    identifier: 'aboBooking.hasFreeTrialPeriod',
    value: '{{membershipEntry.aboBooking.hasFreeTrialPeriod}}',
    description: 'Buchung hat Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'userProfile.id',
    value: '{{membershipEntry.userProfile.id}}',
    description: 'Nutzerprofil-ID',
    placeholder: 'YyY9zzZZ3y',
  },
  {
    identifier: 'mainClub',
    value: '{{membershipEntry.userProfile.mainClub._entryTitle}}',
    description: 'Hauptclub',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'callbackUrl',
    value: '{{membershipEntry.callbackUrl}}',
    description: 'Callback-URL',
    placeholder: 'https://meinclub.de/mitglied-werden/aktivierung',
  },
  {
    identifier: 'title',
    value: '{{membershipEntry.title}}',
    description: 'Titel',
    placeholder: 'Dr.',
  },
  {
    identifier: 'first_name',
    value: '{{membershipEntry.name}}',
    description: 'Vorname',
    placeholder: 'Eva',
  },{
    identifier: 'last_name',
    value: '{{membershipEntry.surname}}',
    description: 'Nachname',
    placeholder: 'Adams',
  },
  {
    identifier: 'gender',
    value: '{{membershipEntry.gender}}',
    description: 'Geschlecht',
    placeholder: 'f',
  },
  {
    identifier: 'birthday',
    value: '{{membershipEntry.birthday | date}}',
    description: 'Geburtsdatum',
    placeholder: '2000-02-20',
  },
  {
    identifier: 'street',
    value: '{{membershipEntry.street}}',
    description: 'Straße',
    placeholder: 'Mustergasse 1',
  },
  {
    identifier: 'zipCode',
    value: '{{membershipEntry.zipCode}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'city',
    value: '{{membershipEntry.city}}',
    description: 'Stadt',
    placeholder: 'Mustermetropole',
  },
  {
    identifier: 'countryCode',
    value: '{{membershipEntry.countryCode}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'mobile',
    value: '{{membershipEntry.mobile}}',
    description: 'Telefon (Mobil)',
    placeholder: '+49 1515 67896789',
  },
  {
    identifier: 'subscribeToNewsletter',
    value: '{{membershipEntry.subscribeToNewsletter}}',
    description: 'Newsletter abonniert',
    placeholder: 'true',
  },
  {
    identifier: 'iban',
    value: '{{membershipEntry.iban}}',
    description: 'IBAN',
    placeholder: 'DE83500105177797533336',
  },
  {
    identifier: 'bic',
    value: '{{membershipEntry.bic}}',
    description: 'BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'bankName',
    value: '{{membershipEntry.bankName}}',
    description: 'Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'accountOwner',
    value: '{{membershipEntry.accountOwner}}',
    description: 'Kontoinhaber',
    placeholder: 'Eva u. Julia Adams',
  },
  {
    identifier: 'referral',
    value: '{{membershipEntry.referral}}',
    description: 'Referral-ID',
    placeholder: '0UEk8GEFPX',
  },
  {
    identifier: 'durationStart',
    value: '{{durationStart | date}}',
    description: 'Laufzeitbeginn',
    placeholder: '2021-07-07',
  },
  {
    identifier: 'endOfFreeTrial',
    value: '{{endOfFreeTrial | date}}',
    description: 'Ende der Testphase',
    placeholder: '2021-07-21',
  },
  {
    identifier: 'paymentStart',
    value: '{{paymentStart | date}}',
    description: 'Zahlungsbeginn',
    placeholder: '2021-07-22',
  },
  {
    identifier: 'aboStart',
    value: '{{aboStart | date}}',
    description: 'Zahlungsbeginn',
    placeholder: '2021-08-01',
  },
  {
    identifier: 'terminationNoticeDate',
    value: '{{terminationNoticeDate | date}}',
    description: 'Kündigungsfrist',
    placeholder: '2022-07-31',
  },
  {
    identifier: 'durationEnd',
    value: '{{durationEnd | date}}',
    description: 'Laufzeitende',
    placeholder: '2023-08-31',
  },
]
```


## Mail-Templates

# MembershipActivation

- usage: `sendActivationMail` (html)
- data is full `eva_membership` entry (level 2) and the callbackUrl:

```js
[
  {
    identifier: 'id',
    value: '{{id}}',
    description: 'Membership-EntryID',
    placeholder: 'XW5jiXoPPf',
  },
  {
    identifier: 'membershipRequestID',
    value: '{{membershipRequestID}}',
    description: 'Membership-Request-ID',
    placeholder: '1023',
  },
  {
    identifier: 'club.id',
    value: '{{club.id}}',
    description: 'Club-ID',
    placeholder: 'YX4wsYoZZr',
  },
  {
    identifier: 'club.id',
    value: '{{club.name}}',
    description: 'Club-Name',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'club.studioNumber',
    value: '{{club.studioNumber}}',
    description: 'Club-Studionummer',
    placeholder: '123',
  },
  {
    identifier: 'club.owner',
    value: '{{club.owner}}',
    description: 'Club-Besitzer',
    placeholder: 'Alex Besitzer',
  },
  {
    identifier: 'club.addressStreet',
    value: '{{club.addressStreet}}',
    description: 'Club-Straße',
    placeholder: 'Pumperstraße 123',
  },
  {
    identifier: 'club.addressZipCode',
    value: '{{club.addressZipCode}}',
    description: 'Club-PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'club.addressCity',
    value: '{{club.addressZipCode}}',
    description: 'Club-Stadt',
    placeholder: 'Musterdorf',
  },
  {
    identifier: 'club.addressCountryCode',
    value: '{{club.addressCountryCode}}',
    description: 'Club-Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'club.addressCo',
    value: '{{club.addressCo}}',
    description: 'Club-Adresse C/O',
    placeholder: 'Businesspark 2A',
  },
  {
    identifier: 'club.bankAccountIBAN',
    value: '{{club.bankAccountIBAN}}',
    description: 'Club-IBAN',
    placeholder: 'DE11500105172878648336',
  },
  {
    identifier: 'club.bankAccountBIC',
    value: '{{club.bankAccountBIC}}',
    description: 'Club-BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'club.bankAccountBankName',
    value: '{{club.bankAccountBankName}}',
    description: 'Club-Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'club.bankAccountOwner',
    value: '{{club.bankAccountBankName}}',
    description: 'Club-Kontoinhaber',
    placeholder: 'Alex Besitzer',
  },
  {
    identifier: 'club.contactEmail',
    value: '{{club.contactEmail}}',
    description: 'Club-E-Mail',
    placeholder: 'info@meinclub.de',
  },
  {
    identifier: 'club.contactMobile',
    value: '{{club.contactEmail}}',
    description: 'Club-Mobilnummer',
    placeholder: '+49 1515 12341234',
  },
  {
    identifier: 'club.contactPhone',
    value: '{{club.contactPhone}}',
    description: 'Club-Telefonnummer',
    placeholder: '+49 711 23456789',
  },
  {
    identifier: 'club.sepaUci',
    value: '{{club.sepaUci}}',
    description: 'Club-SEPA-UCI',
    placeholder: 'XX123123',
  },
  {
    identifier: 'club.uStId',
    value: '{{club.uStId}}',
    description: 'Club-USt-ID.',
    placeholder: 'DE123456789',
  },
  {
    identifier: 'membershipTemplate.id',
    value: '{{membershipTemplate.id}}',
    description: 'Vertragsvorlagen-ID',
    placeholder: 'ZRXxx7Z45',
  },
  {
    identifier: 'membershipTemplate.title',
    value: '{{membershipTemplate.title}}',
    description: 'Vertrags-Titel',
    placeholder: 'Flexo Abo',
  },
  {
    identifier: 'membershipTemplate.type',
    value: '{{membershipTemplate.type}}',
    description: 'Vertrags-Art',
    placeholder: 'addon',
  },
  {
    identifier: 'membershipTemplate.initialPrice',
    value: '{{membershipTemplate.initialPrice | currency}}',
    description: 'Einrichtungsgebühr',
    placeholder: '2900',
  },
  {
    identifier: 'membershipTemplate.mainInterval',
    value: '{{membershipTemplate.mainInterval | interval}}',
    description: 'Abrchnungsintervall',
    placeholder: 'P1M',
  },
  {
    identifier: 'membershipTemplate.mainIntervalPrice',
    value: '{{membershipTemplate.mainIntervalPrice | currency}}',
    description: 'Grundpreis',
    placeholder: '2999',
  },
  {
    identifier: 'membershipTemplate.initialIntervalDuration',
    value: '{{membershipTemplate.initialIntervalDuration | interval}}',
    description: 'Rabattdauer',
    placeholder: 'P3M',
  },
  {
    identifier: 'membershipTemplate.initialIntervalPrice',
    value: '{{membershipTemplate.initialIntervalPrice | currency}}',
    description: 'Rabattpreis',
    placeholder: '1999',
  },
  {
    identifier: 'membershipTemplate.administrationFeeInterval',
    value: '{{membershipTemplate.administrationFeeInterval | interval}}',
    description: 'Verwaltungsgebühren-Intervall',
    placeholder: 'P1Y',
  },
  {
    identifier: 'membershipTemplate.administrationFee',
    value: '{{membershipTemplate.administrationFee | currency}}',
    description: 'Verwaltungsgebühr',
    placeholder: '9999',
  },
  {
    identifier: 'membershipTemplate. initialAdministrationFeeDuration',
    value: '{{initialAdministrationFeeDuration | interval}}',
    description: 'Rabattdauer Verwaltungsgebühr',
    placeholder: 'P1Y',
  },
  {
    identifier: 'membershipTemplate.initialAdministrationFee',
    value: '{{membershipTemplate.initialAdministrationFee | currency}}',
    description: 'Anfangs-Verwaltungsgebühr',
    placeholder: '4999',
  },
  {
    identifier: 'membershipTemplate.initialDuration',
    value: '{{membershipTemplate.initialDuration | interval}}',
    description: 'Grundlaufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'membershipTemplate.renewalDuration',
    value: '{{membershipTemplate.renewalDuration | interval}}',
    description: 'Verlängerungs-Laufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'membershipTemplate.terminationNoticePeriod',
    value: '{{membershipTemplate.terminationNoticePeriod | interval}}',
    description: 'Kündigungsfrist',
    placeholder: 'P1M',
  },
  {
    identifier: 'membershipTemplate.useFullIntervals',
    value: '{{membershipTemplate.useFullIntervals}}',
    description: 'Volle Abrechnungszeiträume',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.terminationOn15thBefore',
    value: '{{membershipTemplate.terminationOn15thBefore}}',
    description: 'Kündigung zum 15. des Vormonats',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.freeTrialPeriod',
    value: '{{membershipTemplate.freeTrialPeriod | interval}}',
    description: 'Kostenloser Testzeitraum',
    placeholder: 'P2W',
  },
  {
    identifier: 'membershipTemplate.initialPriceIgnoresFreeTrialPeriod',
    value: '{{membershipTemplate.initialPriceIgnoresFreeTrialPeriod}}',
    description: 'Einrichtungsgebühr ignoriert Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.autoAddons',
    value: '{{membershipTemplate.autoAddons}}',
    description: 'Automatisch zugebuchte Addons',
    placeholder: [{_entryID: 'Kaffee'}],
  },
  {
    identifier: 'membershipTemplate.requiresAddons',
    value: '{{membershipTemplate.requiresAddons}}',
    description: 'Erforderliche Abos',
    placeholder: [],
  },
  {
    identifier: 'membershipTemplate.isStandalone',
    value: '{{membershipTemplate.isStandalone}}',
    description: 'Eigenständiger Vertrag',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.isBookableFrom',
    value: '{{membershipTemplate.isBookableFrom | date}}',
    description: 'Buchbar ab',
    placeholder: '2021-02-12',
  },
  {
    identifier: 'membershipTemplate.isBookableTo',
    value: '{{membershipTemplate.isBookableTo | date}}',
    description: 'Buchbar bis',
    placeholder: '2035-03-05',
  },
  {
    identifier: 'membershipTemplate.minimumMembershipAge',
    value: '{{membershipTemplate.minimumMembershipAge}}',
    description: 'Mindestalter',
    placeholder: '16',
  },
  {
    identifier: 'accountID',
    value: '{{account.accountID}}',
    description: 'Account-ID',
    placeholder: '833750b6-38c2-4304-848a-fa6d96cb1c82',
  },
  {
    identifier: 'email',
    value: '{{account.email}}',
    description: 'E-Mail',
    placeholder: 'eva.adams@gmail.com',
  },
  {
    identifier: 'state',
    value: '{{state}}',
    description: 'Mitgliedschafts-Status',
    placeholder: 'finished',
  },
  {
    identifier: 'aboBooking.id',
    value: '{{aboBooking.id}}',
    description: 'Buchungs-ID',
    placeholder: 'XxT9kkKKOx',
  },
  {
    identifier: 'aboBooking.hasFreeTrialPeriod',
    value: '{{aboBooking.hasFreeTrialPeriod}}',
    description: 'Buchung hat Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'userProfile.id',
    value: '{{userProfile.id}}',
    description: 'Nutzerprofil-ID',
    placeholder: 'YyY9zzZZ3y',
  },
  {
    identifier: 'mainClub',
    value: '{{userProfile.mainClub._entryTitle}}',
    description: 'Hauptclub',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'callbackUrl',
    value: '{{callbackUrl}}',
    description: 'Callback-URL',
    placeholder: 'https://meinclub.de/mitglied-werden/aktivierung',
  },
  {
    identifier: 'title',
    value: '{{title}}',
    description: 'Titel',
    placeholder: 'Dr.',
  },
  {
    identifier: 'first_name',
    value: '{{name}}',
    description: 'Vorname',
    placeholder: 'Eva',
  },{
    identifier: 'last_name',
    value: '{{surname}}',
    description: 'Nachname',
    placeholder: 'Adams',
  },
  {
    identifier: 'gender',
    value: '{{gender}}',
    description: 'Geschlecht',
    placeholder: 'f',
  },
  {
    identifier: 'birthday',
    value: '{{birthday | date}}',
    description: 'Geburtsdatum',
    placeholder: '2000-02-20',
  },
  {
    identifier: 'street',
    value: '{{street}}',
    description: 'Straße',
    placeholder: 'Mustergasse 1',
  },
  {
    identifier: 'zipCode',
    value: '{{zipCode}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'city',
    value: '{{city}}',
    description: 'Stadt',
    placeholder: 'Mustermetropole',
  },
  {
    identifier: 'countryCode',
    value: '{{countryCode}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'mobile',
    value: '{{mobile}}',
    description: 'Telefon (Mobil)',
    placeholder: '+49 1515 67896789',
  },
  {
    identifier: 'subscribeToNewsletter',
    value: '{{subscribeToNewsletter}}',
    description: 'Newsletter abonniert',
    placeholder: 'true',
  },
  {
    identifier: 'iban',
    value: '{{iban}}',
    description: 'IBAN',
    placeholder: 'DE83500105177797533336',
  },
  {
    identifier: 'bic',
    value: '{{bic}}',
    description: 'BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'bankName',
    value: '{{bankName}}',
    description: 'Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'accountOwner',
    value: '{{accountOwner}}',
    description: 'Kontoinhaber',
    placeholder: 'Eva u. Julia Adams',
  },
  {
    identifier: 'referral',
    value: '{{referral}}',
    description: 'Referral-ID',
    placeholder: '0UEk8GEFPX',
  },
]
```

(`callbackUrl` is set to override the value from the membershipEntry)

# MemberWelcome

- usage: `sendWelcomeMail` (html)
- data is full `eva_membership` entry (level 2):

```js
[
  {
    identifier: 'id',
    value: '{{id}}',
    description: 'Membership-EntryID',
    placeholder: 'XW5jiXoPPf',
  },
  {
    identifier: 'membershipRequestID',
    value: '{{membershipRequestID}}',
    description: 'Membership-Request-ID',
    placeholder: '1023',
  },
  {
    identifier: 'club.id',
    value: '{{club.id}}',
    description: 'Club-ID',
    placeholder: 'YX4wsYoZZr',
  },
  {
    identifier: 'club.id',
    value: '{{club.name}}',
    description: 'Club-Name',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'club.studioNumber',
    value: '{{club.studioNumber}}',
    description: 'Club-Studionummer',
    placeholder: '123',
  },
  {
    identifier: 'club.owner',
    value: '{{club.owner}}',
    description: 'Club-Besitzer',
    placeholder: 'Alex Besitzer',
  },
  {
    identifier: 'club.addressStreet',
    value: '{{club.addressStreet}}',
    description: 'Club-Straße',
    placeholder: 'Pumperstraße 123',
  },
  {
    identifier: 'club.addressZipCode',
    value: '{{club.addressZipCode}}',
    description: 'Club-PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'club.addressCity',
    value: '{{club.addressZipCode}}',
    description: 'Club-Stadt',
    placeholder: 'Musterdorf',
  },
  {
    identifier: 'club.addressCountryCode',
    value: '{{club.addressCountryCode}}',
    description: 'Club-Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'club.addressCo',
    value: '{{club.addressCo}}',
    description: 'Club-Adresse C/O',
    placeholder: 'Businesspark 2A',
  },
  {
    identifier: 'club.bankAccountIBAN',
    value: '{{club.bankAccountIBAN}}',
    description: 'Club-IBAN',
    placeholder: 'DE11500105172878648336',
  },
  {
    identifier: 'club.bankAccountBIC',
    value: '{{club.bankAccountBIC}}',
    description: 'Club-BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'club.bankAccountBankName',
    value: '{{club.bankAccountBankName}}',
    description: 'Club-Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'club.bankAccountOwner',
    value: '{{club.bankAccountBankName}}',
    description: 'Club-Kontoinhaber',
    placeholder: 'Alex Besitzer',
  },
  {
    identifier: 'club.contactEmail',
    value: '{{club.contactEmail}}',
    description: 'Club-E-Mail',
    placeholder: 'info@meinclub.de',
  },
  {
    identifier: 'club.contactMobile',
    value: '{{club.contactEmail}}',
    description: 'Club-Mobilnummer',
    placeholder: '+49 1515 12341234',
  },
  {
    identifier: 'club.contactPhone',
    value: '{{club.contactPhone}}',
    description: 'Club-Telefonnummer',
    placeholder: '+49 711 23456789',
  },
  {
    identifier: 'club.sepaUci',
    value: '{{club.sepaUci}}',
    description: 'Club-SEPA-UCI',
    placeholder: 'XX123123',
  },
  {
    identifier: 'club.uStId',
    value: '{{club.uStId}}',
    description: 'Club-USt-ID.',
    placeholder: 'DE123456789',
  },
  {
    identifier: 'membershipTemplate.id',
    value: '{{membershipTemplate.id}}',
    description: 'Vertragsvorlagen-ID',
    placeholder: 'ZRXxx7Z45',
  },
  {
    identifier: 'membershipTemplate.title',
    value: '{{membershipTemplate.title}}',
    description: 'Vertrags-Titel',
    placeholder: 'Flexo Abo',
  },
  {
    identifier: 'membershipTemplate.type',
    value: '{{membershipTemplate.type}}',
    description: 'Vertrags-Art',
    placeholder: 'addon',
  },
  {
    identifier: 'membershipTemplate.initialPrice',
    value: '{{membershipTemplate.initialPrice | currency}}',
    description: 'Einrichtungsgebühr',
    placeholder: '2900',
  },
  {
    identifier: 'membershipTemplate.mainInterval',
    value: '{{membershipTemplate.mainInterval | interval}}',
    description: 'Abrchnungsintervall',
    placeholder: 'P1M',
  },
  {
    identifier: 'membershipTemplate.mainIntervalPrice',
    value: '{{membershipTemplate.mainIntervalPrice | currency}}',
    description: 'Grundpreis',
    placeholder: '2999',
  },
  {
    identifier: 'membershipTemplate.initialIntervalDuration',
    value: '{{membershipTemplate.initialIntervalDuration | interval}}',
    description: 'Rabattdauer',
    placeholder: 'P3M',
  },
  {
    identifier: 'membershipTemplate.initialIntervalPrice',
    value: '{{membershipTemplate.initialIntervalPrice | currency}}',
    description: 'Rabattpreis',
    placeholder: '1999',
  },
  {
    identifier: 'membershipTemplate.administrationFeeInterval',
    value: '{{membershipTemplate.administrationFeeInterval | interval}}',
    description: 'Verwaltungsgebühren-Intervall',
    placeholder: 'P1Y',
  },
  {
    identifier: 'membershipTemplate.administrationFee',
    value: '{{membershipTemplate.administrationFee | currency}}',
    description: 'Verwaltungsgebühr',
    placeholder: '9999',
  },
  {
    identifier: 'membershipTemplate. initialAdministrationFeeDuration',
    value: '{{initialAdministrationFeeDuration | interval}}',
    description: 'Rabattdauer Verwaltungsgebühr',
    placeholder: 'P1Y',
  },
  {
    identifier: 'membershipTemplate.initialAdministrationFee',
    value: '{{membershipTemplate.initialAdministrationFee | currency}}',
    description: 'Anfangs-Verwaltungsgebühr',
    placeholder: '4999',
  },
  {
    identifier: 'membershipTemplate.initialDuration',
    value: '{{membershipTemplate.initialDuration | interval}}',
    description: 'Grundlaufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'membershipTemplate.renewalDuration',
    value: '{{membershipTemplate.renewalDuration | interval}}',
    description: 'Verlängerungs-Laufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'membershipTemplate.terminationNoticePeriod',
    value: '{{membershipTemplate.terminationNoticePeriod | interval}}',
    description: 'Kündigungsfrist',
    placeholder: 'P1M',
  },
  {
    identifier: 'membershipTemplate.useFullIntervals',
    value: '{{membershipTemplate.useFullIntervals}}',
    description: 'Volle Abrechnungszeiträume',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.terminationOn15thBefore',
    value: '{{membershipTemplate.terminationOn15thBefore}}',
    description: 'Kündigung zum 15. des Vormonats',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.freeTrialPeriod',
    value: '{{membershipTemplate.freeTrialPeriod | interval}}',
    description: 'Kostenloser Testzeitraum',
    placeholder: 'P2W',
  },
  {
    identifier: 'membershipTemplate.initialPriceIgnoresFreeTrialPeriod',
    value: '{{membershipTemplate.initialPriceIgnoresFreeTrialPeriod}}',
    description: 'Einrichtungsgebühr ignoriert Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.autoAddons',
    value: '{{membershipTemplate.autoAddons}}',
    description: 'Automatisch zugebuchte Addons',
    placeholder: [{_entryID: 'Kaffee'}],
  },
  {
    identifier: 'membershipTemplate.requiresAddons',
    value: '{{membershipTemplate.requiresAddons}}',
    description: 'Erforderliche Abos',
    placeholder: [],
  },
  {
    identifier: 'membershipTemplate.isStandalone',
    value: '{{membershipTemplate.isStandalone}}',
    description: 'Eigenständiger Vertrag',
    placeholder: 'true',
  },
  {
    identifier: 'membershipTemplate.isBookableFrom',
    value: '{{membershipTemplate.isBookableFrom | date}}',
    description: 'Buchbar ab',
    placeholder: '2021-02-12',
  },
  {
    identifier: 'membershipTemplate.isBookableTo',
    value: '{{membershipTemplate.isBookableTo | date}}',
    description: 'Buchbar bis',
    placeholder: '2035-03-05',
  },
  {
    identifier: 'membershipTemplate.minimumMembershipAge',
    value: '{{membershipTemplate.minimumMembershipAge}}',
    description: 'Mindestalter',
    placeholder: '16',
  },
  {
    identifier: 'accountID',
    value: '{{account.accountID}}',
    description: 'Account-ID',
    placeholder: '833750b6-38c2-4304-848a-fa6d96cb1c82',
  },
  {
    identifier: 'email',
    value: '{{account.email}}',
    description: 'E-Mail',
    placeholder: 'eva.adams@gmail.com',
  },
  {
    identifier: 'state',
    value: '{{state}}',
    description: 'Mitgliedschafts-Status',
    placeholder: 'finished',
  },
  {
    identifier: 'aboBooking.id',
    value: '{{aboBooking.id}}',
    description: 'Buchungs-ID',
    placeholder: 'XxT9kkKKOx',
  },
  {
    identifier: 'aboBooking.hasFreeTrialPeriod',
    value: '{{aboBooking.hasFreeTrialPeriod}}',
    description: 'Buchung hat Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'userProfile.id',
    value: '{{userProfile.id}}',
    description: 'Nutzerprofil-ID',
    placeholder: 'YyY9zzZZ3y',
  },
  {
    identifier: 'mainClub',
    value: '{{userProfile.mainClub._entryTitle}}',
    description: 'Hauptclub',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'callbackUrl',
    value: '{{callbackUrl}}',
    description: 'Callback-URL',
    placeholder: 'https://meinclub.de/mitglied-werden/aktivierung',
  },
  {
    identifier: 'title',
    value: '{{title}}',
    description: 'Titel',
    placeholder: 'Dr.',
  },
  {
    identifier: 'first_name',
    value: '{{name}}',
    description: 'Vorname',
    placeholder: 'Eva',
  },{
    identifier: 'last_name',
    value: '{{surname}}',
    description: 'Nachname',
    placeholder: 'Adams',
  },
  {
    identifier: 'gender',
    value: '{{gender}}',
    description: 'Geschlecht',
    placeholder: 'f',
  },
  {
    identifier: 'birthday',
    value: '{{birthday | date}}',
    description: 'Geburtsdatum',
    placeholder: '2000-02-20',
  },
  {
    identifier: 'street',
    value: '{{street}}',
    description: 'Straße',
    placeholder: 'Mustergasse 1',
  },
  {
    identifier: 'zipCode',
    value: '{{zipCode}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'city',
    value: '{{city}}',
    description: 'Stadt',
    placeholder: 'Mustermetropole',
  },
  {
    identifier: 'countryCode',
    value: '{{countryCode}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'mobile',
    value: '{{mobile}}',
    description: 'Telefon (Mobil)',
    placeholder: '+49 1515 67896789',
  },
  {
    identifier: 'subscribeToNewsletter',
    value: '{{subscribeToNewsletter}}',
    description: 'Newsletter abonniert',
    placeholder: 'true',
  },
  {
    identifier: 'iban',
    value: '{{iban}}',
    description: 'IBAN',
    placeholder: 'DE83500105177797533336',
  },
  {
    identifier: 'bic',
    value: '{{bic}}',
    description: 'BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'bankName',
    value: '{{bankName}}',
    description: 'Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'accountOwner',
    value: '{{accountOwner}}',
    description: 'Kontoinhaber',
    placeholder: 'Eva u. Julia Adams',
  },
  {
    identifier: 'referral',
    value: '{{referral}}',
    description: 'Referral-ID',
    placeholder: '0UEk8GEFPX',
  },
]
```

# TerminationConfirmation

- usage: `terminateBooking` (html)
- data is full `eva_user` entry, `eva_abo_booking` and `eva_abo_definition`:

```js
[
  {
    identifier: 'userProfile.id',
    value: '{{id}}',
    description: 'Nutzerprofil-ID',
    placeholder: 'YyY9zzZZ3y',
  },
  {
    identifier: 'accountID',
    value: '{{account.accountID}}',
    description: 'Account-ID',
    placeholder: '833750b6-38c2-4304-848a-fa6d96cb1c82',
  },
  {
    identifier: 'email',
    value: '{{account.email}}',
    description: 'E-Mail',
    placeholder: 'eva.adams@gmail.com',
  },
  {
    identifier: 'mainClub',
    value: '{{mainClub._entryTitle}}',
    description: 'Hauptclub',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'memberID',
    value: '{{memberID}}',
    description: 'Mitgliedsnummer',
    placeholder: '1234',
  },
  {
    identifier: 'title',
    value: '{{title}}',
    description: 'Titel',
    placeholder: 'Dr.',
  },
  {
    identifier: 'first_name',
    value: '{{name}}',
    description: 'Vorname',
    placeholder: 'Eva',
  },{
    identifier: 'last_name',
    value: '{{surname}}',
    description: 'Nachname',
    placeholder: 'Adams',
  },
  {
    identifier: 'gender',
    value: '{{gender}}',
    description: 'Geschlecht',
    placeholder: 'f',
  },
  {
    identifier: 'birthday',
    value: '{{birthday | date}}',
    description: 'Geburtsdatum',
    placeholder: '2000-02-20',
  },
  {
    identifier: 'street',
    value: '{{addressStreet}}',
    description: 'Straße',
    placeholder: 'Mustergasse 1',
  },
  {
    identifier: 'zipCode',
    value: '{{addressZipCode}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'city',
    value: '{{addressCity}}',
    description: 'Stadt',
    placeholder: 'Mustermetropole',
  },
  {
    identifier: 'countryCode',
    value: '{{addressCountryCode}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'mobile',
    value: '{{mobile}}',
    description: 'Telefon (Mobil)',
    placeholder: '+49 1515 67896789',
  },
  {
    identifier: 'iban',
    value: '{{bankAccountIBAN}}',
    description: 'IBAN',
    placeholder: 'DE83500105177797533336',
  },
  {
    identifier: 'bic',
    value: '{{bankAccountBIC}}',
    description: 'BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'bankName',
    value: '{{bankAccountBankName}}',
    description: 'Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'accountOwner',
    value: '{{bankAccountOwner}}',
    description: 'Kontoinhaber',
    placeholder: 'Eva u. Julia Adams',
  },
  {
    identifier: 'referral',
    value: '{{referral}}',
    description: 'Referral-ID',
    placeholder: '0UEk8GEFPX',
  },
  {
    identifier: 'aboDefinition.id',
    value: '{{aboDefinition.id}}',
    description: 'Vertragsvorlagen-ID',
    placeholder: 'ZRXxx7Z45',
  },
  {
    identifier: 'aboDefinition.title',
    value: '{{aboDefinition.title}}',
    description: 'Vertrags-Titel',
    placeholder: 'Flexo Abo',
  },
  {
    identifier: 'aboDefinition.type',
    value: '{{aboDefinition.type}}',
    description: 'Vertrags-Art',
    placeholder: 'addon',
  },
  {
    identifier: 'aboDefinition.initialPrice',
    value: '{{aboDefinition.initialPrice | currency}}',
    description: 'Einrichtungsgebühr',
    placeholder: '2900',
  },
  {
    identifier: 'aboDefinition.mainInterval',
    value: '{{aboDefinition.mainInterval | interval}}',
    description: 'Abrchnungsintervall',
    placeholder: 'P1M',
  },
  {
    identifier: 'aboDefinition.mainIntervalPrice',
    value: '{{aboDefinition.mainIntervalPrice | currency}}',
    description: 'Grundpreis',
    placeholder: '2999',
  },
  {
    identifier: 'aboDefinition.initialIntervalDuration',
    value: '{{aboDefinition.initialIntervalDuration | interval}}',
    description: 'Rabattdauer',
    placeholder: 'P3M',
  },
  {
    identifier: 'aboDefinition.initialIntervalPrice',
    value: '{{aboDefinition.initialIntervalPrice | currency}}',
    description: 'Rabattpreis',
    placeholder: '1999',
  },
  {
    identifier: 'aboDefinition.administrationFeeInterval',
    value: '{{aboDefinition.administrationFeeInterval | interval}}',
    description: 'Verwaltungsgebühren-Intervall',
    placeholder: 'P1Y',
  },
  {
    identifier: 'aboDefinition.administrationFee',
    value: '{{aboDefinition.administrationFee | currency}}',
    description: 'Verwaltungsgebühr',
    placeholder: '9999',
  },
  {
    identifier: 'aboDefinition. initialAdministrationFeeDuration',
    value: '{{initialAdministrationFeeDuration | interval}}',
    description: 'Rabattdauer Verwaltungsgebühr',
    placeholder: 'P1Y',
  },
  {
    identifier: 'aboDefinition.initialAdministrationFee',
    value: '{{aboDefinition.initialAdministrationFee | currency}}',
    description: 'Anfangs-Verwaltungsgebühr',
    placeholder: '4999',
  },
  {
    identifier: 'aboDefinition.initialDuration',
    value: '{{aboDefinition.initialDuration | interval}}',
    description: 'Grundlaufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'aboDefinition.renewalDuration',
    value: '{{aboDefinition.renewalDuration | interval}}',
    description: 'Verlängerungs-Laufzeit',
    placeholder: 'P12M',
  },
  {
    identifier: 'aboDefinition.terminationNoticePeriod',
    value: '{{aboDefinition.terminationNoticePeriod | interval}}',
    description: 'Kündigungsfrist',
    placeholder: 'P1M',
  },
  {
    identifier: 'aboDefinition.useFullIntervals',
    value: '{{aboDefinition.useFullIntervals}}',
    description: 'Volle Abrechnungszeiträume',
    placeholder: 'true',
  },
  {
    identifier: 'aboDefinition.terminationOn15thBefore',
    value: '{{aboDefinition.terminationOn15thBefore}}',
    description: 'Kündigung zum 15. des Vormonats',
    placeholder: 'true',
  },
  {
    identifier: 'aboDefinition.freeTrialPeriod',
    value: '{{aboDefinition.freeTrialPeriod | interval}}',
    description: 'Kostenloser Testzeitraum',
    placeholder: 'P2W',
  },
  {
    identifier: 'aboDefinition.initialPriceIgnoresFreeTrialPeriod',
    value: '{{aboDefinition.initialPriceIgnoresFreeTrialPeriod}}',
    description: 'Einrichtungsgebühr ignoriert Testphase',
    placeholder: 'true',
  },
  {
    identifier: 'aboDefinition.autoAddons',
    value: '{{aboDefinition.autoAddons}}',
    description: 'Automatisch zugebuchte Addons',
    placeholder: [{_entryID: 'Kaffee'}],
  },
  {
    identifier: 'aboDefinition.requiresAddons',
    value: '{{aboDefinition.requiresAddons}}',
    description: 'Erforderliche Abos',
    placeholder: [],
  },
  {
    identifier: 'aboDefinition.isStandalone',
    value: '{{aboDefinition.isStandalone}}',
    description: 'Eigenständiger Vertrag',
    placeholder: 'true',
  },
  {
    identifier: 'aboDefinition.isBookableFrom',
    value: '{{aboDefinition.isBookableFrom | date}}',
    description: 'Buchbar ab',
    placeholder: '2021-02-12',
  },
  {
    identifier: 'aboDefinition.isBookableTo',
    value: '{{aboDefinition.isBookableTo | date}}',
    description: 'Buchbar bis',
    placeholder: '2035-03-05',
  },
  {
    identifier: 'aboDefinition.minimumMembershipAge',
    value: '{{aboDefinition.minimumMembershipAge}}',
    description: 'Mindestalter',
    placeholder: '16',
  },
  {
    identifier: 'booking.id',
    value: '{{booking.id}}',
    description: 'Buchungs-ID',
    placeholder: 'XxT9kkKKOx',
  },
  {
    identifier: 'booking.durationStart',
    value: '{{booking.durationStart | date}}',
    description: 'Laufzeitbeginn',
    placeholder: '2021-07-07',
  },
  {
    identifier: 'booking.isTerminated',
    value: '{{booking.isTerminated | date}}',
    description: 'Kündigungsdatum',
    placeholder: '2022-07-31',
  },
  {
    identifier: 'booking.durationEnd',
    value: '{{booking.durationEnd | date}}',
    description: 'Laufzeitende',
    placeholder: '2023-08-31',
  },
  {
    identifier: 'booking.hasFreeTrialPeriod',
    value: '{{booking.hasFreeTrialPeriod}}',
    description: 'Buchung hat Testphase',
    placeholder: 'true',
  },
]
```

# AddonBookedConfirmation

- usage: `bookAddon` (html)
- data is full `eva_user` entry, `addon_config` and `addon.terms` (human readable abo definition):

```js
[
  {
    identifier: 'userProfile.id',
    value: '{{id}}',
    description: 'Nutzerprofil-ID',
    placeholder: 'YyY9zzZZ3y',
  },
  {
    identifier: 'accountID',
    value: '{{account.accountID}}',
    description: 'Account-ID',
    placeholder: '833750b6-38c2-4304-848a-fa6d96cb1c82',
  },
  {
    identifier: 'email',
    value: '{{account.email}}',
    description: 'E-Mail',
    placeholder: 'eva.adams@gmail.com',
  },
  {
    identifier: 'mainClub',
    value: '{{mainClub._entryTitle}}',
    description: 'Hauptclub',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'memberID',
    value: '{{memberID}}',
    description: 'Mitgliedsnummer',
    placeholder: '1234',
  },
  {
    identifier: 'title',
    value: '{{title}}',
    description: 'Titel',
    placeholder: 'Dr.',
  },
  {
    identifier: 'first_name',
    value: '{{name}}',
    description: 'Vorname',
    placeholder: 'Eva',
  },{
    identifier: 'last_name',
    value: '{{surname}}',
    description: 'Nachname',
    placeholder: 'Adams',
  },
  {
    identifier: 'gender',
    value: '{{gender}}',
    description: 'Geschlecht',
    placeholder: 'f',
  },
  {
    identifier: 'birthday',
    value: '{{birthday | date}}',
    description: 'Geburtsdatum',
    placeholder: '2000-02-20',
  },
  {
    identifier: 'street',
    value: '{{addressStreet}}',
    description: 'Straße',
    placeholder: 'Mustergasse 1',
  },
  {
    identifier: 'zipCode',
    value: '{{addressZipCode}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'city',
    value: '{{addressCity}}',
    description: 'Stadt',
    placeholder: 'Mustermetropole',
  },
  {
    identifier: 'countryCode',
    value: '{{addressCountryCode}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'mobile',
    value: '{{mobile}}',
    description: 'Telefon (Mobil)',
    placeholder: '+49 1515 67896789',
  },
  {
    identifier: 'iban',
    value: '{{bankAccountIBAN}}',
    description: 'IBAN',
    placeholder: 'DE83500105177797533336',
  },
  {
    identifier: 'bic',
    value: '{{bankAccountBIC}}',
    description: 'BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'bankName',
    value: '{{bankAccountBankName}}',
    description: 'Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'accountOwner',
    value: '{{bankAccountOwner}}',
    description: 'Kontoinhaber',
    placeholder: 'Eva u. Julia Adams',
  },
  {
    identifier: 'referral',
    value: '{{referral}}',
    description: 'Referral-ID',
    placeholder: '0UEk8GEFPX',
  },
  {
    identifier: 'addonconfig.title',
    value: '{{addon.title}}',
    description: 'Addon-Titel',
    placeholder: 'Kaffee-Abo',
  },
  {
    identifier: 'addonconfig.description',
    value: '{{addon.description}}',
    description: 'Addon-Beschreibung',
    placeholder: 'So viel Kaffee du willst',
  },
  {
    identifier: 'addonconfig.terms',
    value: '{{addon.terms}}',
    description: 'Addon-Bedingungen (autogeneriert)',
    placeholder: 'Jederzeit kündbar',
  },
]
```

# Recommendation

- usage: `postRecommendationsForEVA` (html)
- data is full `eva_user` entry, and referral-Object:

```js
[
  {
    identifier: 'userProfile.id',
    value: '{{id}}',
    description: 'Nutzerprofil-ID',
    placeholder: 'YyY9zzZZ3y',
  },
  {
    identifier: 'accountID',
    value: '{{account.accountID}}',
    description: 'Account-ID',
    placeholder: '833750b6-38c2-4304-848a-fa6d96cb1c82',
  },
  {
    identifier: 'email',
    value: '{{account.email}}',
    description: 'E-Mail',
    placeholder: 'eva.adams@gmail.com',
  },
  {
    identifier: 'mainClub',
    value: '{{mainClub._entryTitle}}',
    description: 'Hauptclub',
    placeholder: 'Mein Club Musterstadt',
  },
  {
    identifier: 'memberID',
    value: '{{memberID}}',
    description: 'Mitgliedsnummer',
    placeholder: '1234',
  },
  {
    identifier: 'title',
    value: '{{title}}',
    description: 'Titel',
    placeholder: 'Dr.',
  },
  {
    identifier: 'first_name',
    value: '{{name}}',
    description: 'Vorname',
    placeholder: 'Eva',
  },{
    identifier: 'last_name',
    value: '{{surname}}',
    description: 'Nachname',
    placeholder: 'Adams',
  },
  {
    identifier: 'gender',
    value: '{{gender}}',
    description: 'Geschlecht',
    placeholder: 'f',
  },
  {
    identifier: 'birthday',
    value: '{{birthday | date}}',
    description: 'Geburtsdatum',
    placeholder: '2000-02-20',
  },
  {
    identifier: 'street',
    value: '{{addressStreet}}',
    description: 'Straße',
    placeholder: 'Mustergasse 1',
  },
  {
    identifier: 'zipCode',
    value: '{{addressZipCode}}',
    description: 'PLZ',
    placeholder: '21337',
  },
  {
    identifier: 'city',
    value: '{{addressCity}}',
    description: 'Stadt',
    placeholder: 'Mustermetropole',
  },
  {
    identifier: 'countryCode',
    value: '{{addressCountryCode}}',
    description: 'Länderkürzel',
    placeholder: 'DE',
  },
  {
    identifier: 'mobile',
    value: '{{mobile}}',
    description: 'Telefon (Mobil)',
    placeholder: '+49 1515 67896789',
  },
  {
    identifier: 'iban',
    value: '{{bankAccountIBAN}}',
    description: 'IBAN',
    placeholder: 'DE83500105177797533336',
  },
  {
    identifier: 'bic',
    value: '{{bankAccountBIC}}',
    description: 'BIC',
    placeholder: 'MUSTERDEXXX',
  },
  {
    identifier: 'bankName',
    value: '{{bankAccountBankName}}',
    description: 'Bankname',
    placeholder: 'Volksbank Musterdorf',
  },
  {
    identifier: 'accountOwner',
    value: '{{bankAccountOwner}}',
    description: 'Kontoinhaber',
    placeholder: 'Eva u. Julia Adams',
  },
  {
    identifier: 'referral.email',
    value: '{{referral.email}}',
    description: 'Referral-E-Mail',
    placeholder: 'julia.adams@gmail.com',
  },
  {
    identifier: 'referral.name',
    value: '{{referral.name}}',
    description: 'Referral-Name',
    placeholder: 'Julia',
  },
  {
    identifier: 'referral.note',
    value: '{{referral.note}}',
    description: 'Referral-Nachricht',
    placeholder: 'Schau dir das an!',
  },
  {
    identifier: 'referral.callbackUrl',
    value: '{{referral.callbackUrl}}',
    description: 'Referral-Callback-URL',
    placeholder: 'https://meinclub.de/mitglied-werden',
  },
]
```
