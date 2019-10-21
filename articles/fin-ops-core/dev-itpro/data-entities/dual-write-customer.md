---
title: Integrētie debitoru pamatdati
description: Šajā tēmā ir aprakstīta debitoru datu integrācija starp Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6c8c94eb8ff04d489eb24b7e0f4642aef20a3b18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182052"
---
## <a name="integrated-customer-master"></a>Integrētie debitoru pamatdati

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Debitoru ierakstiem ir tipiski, ka to pamatdati ir iekļauti vairāk nekā vienā programmā. Piemēram, pārdošanas aktivitāte var ieviest komerciālo klientu ierakstus, izmantojot programmu Sales, un e-komercija vai mazumtirdzniecība var ieviest debitoru ierakstus, izmantojot programmu Finance and Operations. Neatkarīgi no tā, no kurienes ir ieviests debitora ieraksts, tas ir integrēts aiz ainām programmu robežās un infrastruktūras atšķirībās. Integrēta debitoru pamatdatu apguve palīdz apstrādāt vairāku pamatdatu apguves scenārijus un nodrošina visaptverošu skatījumu par debitoru Dynamics 365 programmu komplektam.

## <a name="customer-data-flow"></a>Debitora datu plūsma

*Debitors* ir pareizi definēta koncepcija programmās. Tādēļ debitoru datu integrēšana ietver tikai debitora koncepta saskaņošanu starp abām programmām. Nākamajā attēlā ir parādīta debitoru datu plūsma.

![Debitora datu plūsma](media/dual-write-customer-data-flow.png)

Debitorus kopumā var iedalīt divos tipos: komerciālie/organizāciju debitori un debitori/galalietotāji. Šie divi debitoru tipi tiek dažādi uzglabāti un apstrādāti programmās Finance and Operations un Common Data Service.

Programmā Finance and Operations gan komerciālo/organizāciju debitoru, gan debitoru/galalietotāju pamatdati tiek apkopoti vienā tabulā, kas saucas **CustTable** (CustomerCustomerV3Entity), un tie tiek klasificēti, pamatojoties uz atribūtu **Tips**. (Ja **Tips** ir iestatīts uz **Organizācija**, tad debitors ir komerciāls/organizācijas debitors, un ja **Tips** ir iestatīts uz **Persona**, tad debitors ir debitors/galalietotājs.) Primārā kontaktpersonas informācija tiek apstrādāta, izmantojot SMMContactPersonEntity elementu.

Programmā Common Data Service komerciālie/organizāciju debitoru pamatdati tiek apkopoti Konta elementā, un tiek identificēti kā debitori, kas atribūts **RelationshipType** ir iestatīts uz **Debitorsr**. Gan debitorus/galalietotājus, gan kontaktpersonu pārstāv Kontaktpersonas elements. Lai nodrošinātu skaidru dalījumu starp debitoru/galalietotāju un kontaktpersonu, elementam **Kontaktpersona** ir Būla karodziņš ar nosaukumu **Pārdodams**. Ja **Pārdodams** ir **Patiess**, kontaktpersona ir debitors/galalietotājs, un šai kontaktpersonai var izveidot piedāvājumus un pasūtījumus. Ja **Pārdodams** ir **Nepatiess**, kontaktpersona ir tikai debitora primārā kontaktpersona.

Kad nepārdodama kontaktpersona piedalās piedāvājumu vai pasūtījumu procesā **Pārdodams** ir iestatīts kā **Patiess**, lai atzīmētu kontaktpersonu kā pārdodamu kontaktpersonu. Kontaktpersona, kas ir kļuvusi par pārdodamu kontaktpersonu, joprojām paliek pārdodama kontaktpersona.

## <a name="templates"></a>Veidnes

Debitora dati ietver visu informāciju par debitoru, piemēram, debitora grupu, adreses, kontaktinformāciju, maksājuma profilu, rēķina profilu un lojalitātes programmas statusu. Elementa karšu vākšana darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas    | Citas Dynamics 365 programmas
--------------------------|---------------------------------
Debitora V3               | Konts
Debitora V3               | Kontaktpersona
CDS kontaktpersonas V2           | Kontaktpersona
Debitoru grupas           | Msdyn\_customergroups
Debitora maksāšanas metode   | Msdyn\_customerpaymentmethods
Lojalitātes programmas karte              | Msdyn\_loyaltycards
Maksājumu grafiks          | Msdyn\_paymentschedules
Maksājumu grafiks          | Msdyn\_paymentschedulelines
Maksāšanas diena CDS           | Msdyn\_paymentdays
Maksāšanas dienu rindas CDS     | Msdyn\_paymentdaylines
Maksājuma nosacījumi          | Msdyn\_paymentterms
Nosaukuma afiksi              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Debitora V3 uz kontu

Šī veidne sinhronizē debitora pamatinformāciju komerciāliem un organizācijas debitoriem starp programmām Finance and Operations un Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | apraksts
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | nav
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
nav | \>\> | address1\_addresstypecode
nav | \>\> | customertypecode
PARTYTYPE | \<\< | nav
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Debitors V3 ar kontaktpersonu

Šī veidne sinhronizē debitoru pamatdatus debitoriem un galalietotājiem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
nav | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | nav
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | nav
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | nav
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
nav | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
nav | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
nav | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | apraksts

## <a name="contacts"></a>Kontaktpersonas

Šī veidne sinhronizē visu primāro, sekundāro unterciālo kontaktinformāciju gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-contacts.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | nav
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
PIEZĪMES | = | apraksts
DZIMUMS | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
nav | \>\> | msdyn\_contactforvendor
nav | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Debitoru grupas

Šī veidne sinhronizē debitoru grupas informāciju starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-customer-groups.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
APRAKSTS | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Debitora maksāšanas metode

Šī veidne sinhronizē debitoru maksājumu metodes informāciju starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NOSAUKUMS | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
APRAKSTS | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Lojalitātes programmas kartes

Šī veidne sinhronizē debitoru lojalitātes kartes informāciju starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Maksājumu grafiki

Šī veidne sinhronizē maksājumu grafika atsauces datus gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-payment-schedules.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NOSAUKUMS | = | msdyn\_name
APRAKSTS | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
PIEZĪMES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Maksājumu grafika rindas

Sinhronizē maksājumu grafika rindu atsauces datus gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Maksāšanas dienas

Šī veidne sinhronizē maksājumu dienu atsauces datus gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-payment-days.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NOSAUKUMS | = | msdyn\_name
APRAKSTS | = | msdyn\_description

## <a name="payment-day-lines"></a>Maksāšanas dienu rindas

Šī veidne sinhronizē maksājumu dienu rindu atsauces datus gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
NOSAUKUMS | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Maksājumu nosacījumi

Šī veidne sinhronizē maksājumu nosacījumu atsauces datus gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-payment-terms.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
APRAKSTS | = | msdyn\_description
NOSAUKUMS | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Nosaukuma afiksi

Šī veidne sinhronizē nosaukumu afiksu atsauces datus gan debitoriem, gan kreditoriem starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![](media/dual-write-name-affixes.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
AFFIX | = | msdyn\_affix
TIPS | \>\< | msdyn\_affixtype
APRAKSTS | = | msdyn\_description
