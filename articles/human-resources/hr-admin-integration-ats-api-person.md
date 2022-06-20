---
title: Persona
description: Šajā rakstā ir aprakstīts elementa Persona elements Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49d9b5e1a1297c9528bfa82d0e8307bad3b2d1cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864117"
---
# <a name="person"></a>Persona


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīts elementa Persona elements Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_dirpersonentity

### <a name="description"></a>Apraksts

Šis elements sniedz personīgo informāciju par personai, kas ir kandidāts.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Personas elementa ID**<br>mshr_dirpersonentityid<br>*GUID* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēts unikāls identifikators elementa ierakstam. |
| **Puses numurs**<br>mshr_partynumber<br>*Virkne* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Lietotājam lasāms, sistēmas ģenerēts unikāls personas identifikators.  |
| **Vārds, uzvārds**<br>mshr_name<br>*Virkne* | Tikai lasāms<br>Obligāts | Lauka vērtība ir vārda, otrā vārda, uzvārda prefiksa un uzvārda konkatenācija laukā **Vārdu secību parādīt kā**. |
| **Aizstājvārds**<br>mshr_namealias<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Aizstājvārds, ko var sniegt personai. |
| **Zināms kā**<br>mshr_knownas<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Vārds, ko var lietot personai, ja parasti tas ir zināms kā cits vārds. |
| **Valodas ID**<br>mshr_languageid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās valodas ID, kā definēts ISO 639-1 formātā. |
| **Adrešu grāmatas**<br>mshr_addressbooks<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Adrešu grāmata, kurai var piešķirt šo personu. Adrešu grāmatas, kas ir iestatītas organizācijai, ir uzskaitītas mshr_diraddressbooksentity elementā. |
| **Gadadienas diena**<br>mshr_anniversaryday<br>*Int* | Lasīt/rakstīt<br>Neobligāti | Personas gadadienas datuma diena. |
| **Gadadienas mēnesis**<br>mshr_anniversarymonth<br>*mshr_monthsofyear opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Personas gadadienas datuma mēnesis. |
| **Gadadienas gads**<br>mshr_anniversaryyear<br>*Int* | Lasīt/rakstīt<br>Neobligāti | Personas gadadienas datuma gads. |
| **Dzimšanas diena**<br>mshr_birthday<br>*Int* | Lasīt/rakstīt<br>Neobligāti | Personas dzimšanas dienas datums. |
| **Dzimšanas mēnesis**<br>mshr_birthmonth<br>*mshr_monthsofyear opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Personas dzimšanas dienas mēnesis. |
| **Dzimšanas gads**<br>mshr_birthyear<br>*Int* | Lasīt/rakstīt<br>Neobligāti | Personas dzimšanas dienas gads. |
| **Bērnu vārdi**<br>mshr_childrennames<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Virkne personas bērnu vārdiem. Nav nepieciešama norobežojuma. |
| **Dzimums**<br>mshr_gender<br>*mshr_hcmpersongender opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Personas dzimums. |
| **Hobiji**<br>mshr_hobbies<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas hobiji. |
| **Iniciāļi**<br>mshr_initials<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas vārda iniciāļi. |
| **Ģimenes stāvoklis**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Personas ģimenes stāvoklis. |
| **Fonētiskais vārds**<br>mshr_phoneticfirstname<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas vārda fonētiskā fonētiskā izruna. |
| **Fonētiskais uzvārds**<br>mshr_phoneticlastname<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas uzvārda fonētiskā fonētiskā izruna. |
| **Fonētiskais otrais vārds**<br>mshr_phoneticmiddlename<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas uzvārda fonētiskā fonētiskā izruna. |
| **Personas sufikss**<br>mshr_personalsuffix<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas personiskais sufikss. Derīgas vērtības mshr_dirnameaffixentity, kur mshr_type ir sufikss (200000001). |
| **Personas uzruna**<br>mshr_personaltitle<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas personīgā uzruna. Derīgas vērtības mshr_dirnameaffixentity, kur mshr_type ir uzruna (200000000).
| **Aroda sufikss**<br>mshr_professionalsuffix<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Aroda sufikss. |
| **Ieņemamais amats**<br>mshr_professionaltitle<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Ieņemamais amats. |
| **Pilna primārā adrese**<br>mshr_fullprimaryaddress<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā adrese, primārās adreses lauku konkatenācija. |
| **Adreses pilsēta**<br>mshr_addresscity<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses pilsēta. Iestatīt mshr_logisticsaddresscityentity elementā. |
| **Adrese Valsts Reǵions**<br>mshr_addresscountryregionid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses valsts/reǵions. Derīgas vērtības mshr_logisticsaddresscountryregionentity elements. |
| **Adrese Valsts Reǵions ISO kods**<br>mshr_addresscountryregionisocode<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses valsts ISO kods. |
| **Adrese Apgabals**<br>mshr_addresscounty<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses apgabals. Iestatīt mshr_logisticsaddresscountyentity elementā. |
| **Adreses pagasta nosaukums**<br>mshr_addressdistrictname<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses pagasts. Iestatīt mshr_logisticsaddressdistrictentity elementā. |
| **Adreses ģeogrāfiskais platums**<br>mshr_addresslatitude<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses ģeogrāfiskais platums. |
| **Adreses atrašanās vietas ID**<br>mshr_addresslocationid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Unikālais identifikators personas primārās adreses atrašanās vietai. Derīgas vērtības mshr_logisticspostaladdresslocationcdsentity elementā. |
| **Adreses atrašanās vietas lomas**<br>mshr_addresslocationroles<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses atrašanās vietas loma. Iestatīt mshr_logisticslocationrolecdsentity elementā. |
| **Adreses ǵeogrāfiskais garums**<br>mshr_addresslongitude<br>*Virkne* |  Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses ģeogrāfiskais garums. |
| **Adreses province**<br>mshr_addressstate<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses province. Iestatīt mshr_logisticsaddressstateentity elementā. |
| **Adreses iela**<br>mshr_addressstreet<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses ielas adrese. |
| **Adrese derīga no**<br>mshr_addressvalidfrom<br>*Datums* | Lasīt/rakstīt<br>Neobligāti | Datums, no kura personas primārā adrese ir derīga. |
| **Adrese derīga līdz**<br>mshr_addressvalidto<br>*Datums* | Lasīt/rakstīt<br>Neobligāti | Datums, līdz kuram personas primārā adrese ir derīga. |
| **Adreses pasta indekss**<br>mshr_addresszipcode<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses pasta indekss. Iestatīt mshr_logisticsaddresspostalcodeentity elementā. |
| **Adrese ir privāta**<br>mshr_addressisprivate<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Nosaka, vai personas primārā adrese ir koplietota ar citiem organizācijā. |
| **Adreses apraksts**<br>mshr_addressdescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses apraksts. |
| **Primārās kontaktpersonas e-pasts**<br>mshr_primarycontactemail<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā e-pasta adrese. |
| **Primārās kontaktpersonas e-pasta apraksts**<br>mshr_primarycontactemaildescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārās e-pasta adreses apraksts. |
| **Primārās kontaktpersonas e-pasts ir IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Nosaka, vai primārā e-pasta adrese ir pieejama tūlītējai ziņojumiem. |
| **Primārās kontaktpersonas e-pasts nolūks**<br>mshr_primarycontactemailpurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārās e-pasta adreses nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Primārās kontaktpersonas fakss**<br>mshr_primarycontactfax<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārais faksa numurs. |
| **Primārās kontaktpersonas faksa apraksts**<br>mshr_primarycontactfaxdescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārā faksa numura apraksts. |
| **Primārās kontaktpersonas faksa paplašinājums**<br>mshr_primarycontactfaxextension<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārā faksa numura paplašinājums. |
| **Primārās kontaktpersonas faksa nolūks**<br>mshr_primarycontactfaxpurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārā faksa numura nolūks. Iestatīt mshr_logisticslocationroleentity elementā.
| **Primārās kontaktpersonas tālrunis**<br>mshr_primarycontactphone<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārais tālruņa numurs. |
| **Primārās kontaktpersonas tālruņa apraksts**<br>mshr_primarycontactphonedescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārā tālruņa numura apraksts. |
| **Primārās kontaktpersonas tālruņa paplašinājums**<br>mshr_primarycontactphoneextension<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārā tālruņa numura paplašinājums. |
| **Primārās kontaktpersonas tālrunis ir mobilais tālrunis**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Norāda, vai primārais tālruņa numurs ir mobilais tālrunis. |
| **Primārās kontaktpersonas tālruņa nolūks**<br>mshr_primarycontactphonepurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārā tālruņa numura nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Primārās kontaktpersonas telekss**<br>mshr_primarycontacttelex<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārais teleksa numurs. |
| **Primārās kontaktpersonas teleksa apraksts**<br>mshr_primarycontacttelexdescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā teleksa numura apraksts. |
| **Primārās kontaktpersonas teleksa nolūks**<br>mshr_primarycontacttelexpurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā teleksa numura nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Primārās kontaktpersonas URL**<br>mshr_primarycontacturl<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārais URL. |
| **Primārās kontaktpersonas URL apraksts**<br>mshr_primarycontacturldescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā URL apraksts. |
| **Primārās kontaktpersonas URL nolūks**<br>mshr_primarycontacturldescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā URL nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Primārās kontaktpersonas Facebook**<br>mshr_primarycontactfacebook<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārais Facebook konts. Identificēts ar lietotāja ID. |
| **Primārās kontaktpersonas Facebook apraksts**<br>mshr_primarycontactfacebookdescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā Facebook konta apraksts. |
| **Primārās kontaktpersonas Facebook ir privāts**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Nosaka, vai primārais Facebook konts ir redzams citiem lietotājiem. |
| **Primārās kontaktpersonas Facebook nolūks**<br>mshr_primarycontactfacebookpurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā Facebook konta nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Primārās kontaktpersonas LinkedIn**<br>mshr_primarycontactlinkedin<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Primārais LinkedIn konts. Identificēts ar lietotājvārdu. |
| **Primārās kontaktpersonas LinkedIn apraksts**<br>mshr_primarycontactlinkedindescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā LinkedIn konta apraksts. |
| **Primārās kontaktpersonas LinkedIn ir privāts**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Nosaka, vai personas primārā LinkedIn konta informācija ir koplietota ar citiem lietotājiem. |
| **Primārās kontaktpersonas LinkedIn nolūks**<br>mshr_primarycontactlinkedinpurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā LinkedIn konta nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Primārās kontaktpersonas Twitter**<br>mshr_primarycontacttwitter<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārais Twitter konts. Identificēts ar @username. |
| **Primārās kontaktpersonas Twitter apraksts**<br>mshr_primarycontacttwitterdescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā Twitter konta apraksts. |
| **Primārās kontaktpersonas Twitter ir privāts**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes opciju kopa* | Lasīt/rakstīt<br>Neobligāti | Nosaka, vai personas primārā Twitter konta informācija ir koplietota ar citiem lietotājiem. |
| **Primārās kontaktpersonas Twitter nolūks**<br>mshr_primarycontacttwitterpurpose<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas primārā Twitter konta nolūks. Iestatīt mshr_logisticslocationroleentity elementā. |
| **Puses veids**<br>mshr_partytype<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas puses veids. Kandidātiem tas vienmēr būs **Persona**. |
| **Nosaukuma parādīšanas secība**<br>mshr_namesequencedisplayas<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Secība, kādā personas vārda īpašības tiek apvienotas ar veidlapas Nosaukums (mshr_name) rekvizīta vērtību. |
| **Vārds**<br>mshr_firstname<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Personas vārds. |
| **Otrais vārds**<br>mshr_middlename<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas otrais vārds. |
| **Uzvārda prefikss**<br>mshr_lastnameprefix<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas uzvārda prefikss. |
| **Uzvārds**<br>mshr_lastname<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas uzvārds. |
| **Elektroniskā novietojuma ID**<br>mshr_electroniclocationid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Personas elektroniskā novietojuma ID. |
| **Adreses laika josla**<br>mshr_addresstimezone<br>*Int* | Lasīt/rakstīt<br>Neobligāti | Personas primārās adreses laika josla. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
