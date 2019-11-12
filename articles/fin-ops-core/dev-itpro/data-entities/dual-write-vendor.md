---
title: Integrētie kreditora pamatdati
description: Šajā tēmā ir aprakstīta kreditora datu integrācija starp Finance and Operations programmām un Common Data Service.
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
ms.openlocfilehash: d33625b94e7611a256c389a6de4692ae8f4ff2a7
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572476"
---
# <a name="integrated-vendor-master"></a>Integrētie kreditora pamatdati

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Termins *Kreditors* attiecas uz piegādātāja organizāciju vai vienīgo īpašnieku, kas ir piegādes ķēdes procesa daļa un kas piegādā preces uzņēmumam. Kaut arī *kreditors* ir reģistrēts koncepts Finance and Operations programmās, kreditora koncepts nepastāv citās Dynamics 365 programmās. Tā vietā daži uzņēmumi pārslogo Konta elementu, lai uzglabātu gan debitora informāciju, gan kreditora informāciju. Citi uzņēmumi izmanto pielāgotu kreditoru konceptu. Common Data Service integrācija atbalsta abus šos modeļus. Tāpēc atkarībā no jūsu biznesa varat iespējot jebkuru no modeļiem.

Kreditoru datu integrēšana starp Finance and Operations programmām un citām Dynamics 365 programmām ļauj veikt vairāku pamatdatu apkopošanu. Neatkarīgi no tā, no kurienes ir ieviests kreditora ieraksts, tas ir integrēts aiz ainām programmu robežās un infrastruktūras atšķirībās. 

### <a name="vendor-data-flow"></a>Kreditora datu plūsma

Ja vēlaties izmantot citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties nošķirt kreditora informāciju no debitora informācijas, varat izmantot jauno kreditora modeli.

![Kreditora datu plūsma](media/dual-write-vendor-data-flow.png)

Ja vēlaties izmantot citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties arī turpmāk izmantot Konta elementu kreditora informācijas glabāšanai, varat izmantot jauno paplašināto kreditora modeli. Šajā modelī paplašinātā kreditora informācija, piemēram, kreditoru grupa un kreditora grāmatošanas metode tiek glabāta kreditora detalizētajā informācijā.

![Kreditora paplašinātā datu plūsma](media/dual-write-vendor-detail.jpg)

Kreditora kontaktpersonas informācija ir līdzīga debitora kontaktpersonas informācijai. Nemanāmi kontaktpersonas informācija tiek glabāta un izgūta no tiem pašiem elementiem.

## <a name="templates"></a>Veidnes

Kreditora dati ietver visu informāciju par kreditoru, piemēram, kreditora grupu, adreses, kontaktinformāciju, maksājuma metodi un rēķina metodi. Elementa karšu vākšana darbojas kopā kreditora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas  | Citas Dynamics 365 programmas
------------------------|---------------------------------
V2 kreditors               | Konts
V2 kreditors               | Msdyn\_vendors
CDS kontaktpersonas V2         | Kontaktpersona
Kreditoru grupas           | Msdyn\_vendorgroups
Kreditora maksāšanas metode   | Msdyn\_vendorpaymentmethods
Maksājumu grafiks        | Msdyn\_paymentschedules
Maksājumu grafiks        | Msdyn\_paymentschedulelines
Maksāšanas diena CDS         | Msdyn\_paymentdays
Maksāšanas dienu rindas CDS   | Msdyn\_paymentdaylines
Maksājuma nosacījumi        | Msdyn\_paymentterms
Nosaukuma afiksi            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>V2 kreditors un konts 

Uzņēmumi, kas izmanto Konta elementu, lai glabātu kreditora informāciju, var turpināt to lietot tādā pašā veidā. Tie var arī izmantot skaidras kreditora funkcionalitātes priekšrocības, ko rada Finance and Operations programmu integrācija.

## <a name="vendor-v2-and-msdyn_vendors"></a>Vendor V2 and Msdyn\_vendors

Uzņēmumiem, kas izmanto pielāgotu risinājumu kreditoriem, var izmantot standarta komplektācijas kreditora konceptu, kas ir ieviests pakalpojumā Common Data Service saistībā ar Finance and Operations programmu integrāciju. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber. msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Kontaktpersonas

Šī veidne sinhronizē visu primāro, sekundāro unterciālo kontaktinformāciju gan debitoriem, gan kreditoriem starp Finance and Operations programmām un citām Dynamics 365 programmām. Detalizētu informāciju par elementa karti skatiet rakstā [Integrēti debitora pamatdati](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Kreditoru grupas

Šī veidne sinhronizē kreditoru grupas informāciju starp Finance and Operations programmām un citām Dynamics 365 programmām.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
APRAKSTS | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Kreditora maksāšanas metode

Šī veidne sinhronizē kreditoru maksājumu metodes informāciju starp Finance and Operations un citām Dynamics 365 programmām.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Avota lauks | Kartes veids | Mērķa lauks
---|---|---
NOSAUKUMS | = | msdyn\_name
APRAKSTS | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

