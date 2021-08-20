---
title: Kandidāts pieņemšanai darbā
description: Šajā tēmā aprakstīts darbā pieņemamā kandidāta elements programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: aef9f4889d17811026fc36091bb98494412dacd898f847ac661333628e8e32e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742828"
---
# <a name="candidate-to-hire"></a>Kandidāts pieņemšanai darbā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīts darbā pieņemamā kandidāta elements programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmcandidatetohireentity

## <a name="description"></a>Apraksts

Šis elements nodrošina kandidāta detalizētu informāciju, ko izmanto, lai izveidotu darbinieku programmā Dynamics 365 Human Resources. Tas tiek izmantots, lai lasītu visus kandidāta ierakstus un izveidotu iekšējos un ārējos kandidāta ierakstus, kas ļauj izveidot jaunā kandidāta personisko informāciju.

Kad izveidojat ārēja kandidāta ierakstu, kas būs jaunas personas ieraksts sistēmā, jums nav jādefinē puses (personas) numurs, kurā grāmatojat jaunu kandidāta ierakstu. Jaunās personas elementa ieraksts tiek izveidots ar jaunu kandidāta ierakstu.

Kad izveidojat iekšējo kandidāta ierakstu (kandidāts amatam, kuram jau ir darbinieka ieraksts ar uzņēmumu), norādiet ieraksta, kas personai jau pastāv mshr_partynumber rekvizītam kandidāta ierakstā, numuru, nevis norādiet personisko informāciju (tādu kā vārds, dzimums vai dzimšanas datums), kas tiktu izmantots jauna personas ieraksta izveidošanai.

## <a name="json-representation"></a>JSON pārstāvība

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Kandidāta pieņemšanai darbā elementa ID**<br>mshr_hcmcandidatetohireentityid<br>GUID | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēts unikāls identifikators elementa ierakstam. |
| **Kandidāta ID**<br>mshr_candidateid<br>Virkne | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Elementa unikāls identifikators. |
| **Puses numurs**<br>mshr_partynumber<br>Virkne | Tikai lasāms<br>Obligāts | Kandidāta personas ieraksta puses (personas) numurs. |
| **Personas ID vērtība**<br>_mshr_fk_person_id_value<br>GUID | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_direpersonentity mshr_dirpersonentityid | Sistēmas ģenerēts unikāls kandidāta puses (personas) ieraksta identifikators. |
| **Puses veids**<br>mshr_partytype<br>mshr_dirpartytype opciju kopa | Tikai lasāms<br>Obligāts | Ieraksta puses veids, kā norādīts opciju kopā mshr_dirpartytype. Šī elementa veids vienmēr būs "Persona". |
| **Pieņemšanas darbā pieprasījuma ID**<br>mshr_recruitingrequestid<br>Virkne | Rakstīt vienu reizi<br>Neobligāti | Norāda, ka personāla atlases pieprasījums šim kandidātam atbilst. |
| **Pieņemšanas darbā pieprasījuma ID vērtība**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Lasīt/rakstīt<br>Neobligāti<br>Ārējā atslēga: mshr_hcmrecruitingrequestentity mshr_hcmrecruitingrequestentityid | Sistēmas ģenerēts unikāls darbā pieņemšanas pieprasījuma, kuram kandidāts atbilst, identifikators. |
| **Amata ID**<br>mshr_positionid<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Amata ID, kuram tiek apsvērts kandidāts. |
| **Amata ID vērtība**<br>_mshr_fk_position_if_value<br>GUID | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmpositionv2entity mshr_hcmpositionv2entityid | Sistēmas ģenerēts amata, kuram tiek apsvērts kandidāts, identifikators. |
| **Vārds**<br>mshr_firstname<br>Virkne | Lasīt/rakstīt<br>Obligāts | Kandidāta vārds. |
| **Otrais vārds**<br>mshr_middlename<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Kandidāta otrais vārds. |
| **Uzvārda prefikss**<br>mshr_lastnameprefix<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Kandidāta uzvārda prefikss. |
| **Uzvārds**<br>mshr_lastname<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Kandidāta uzvārds. |
| **Dzimums**<br>mshr_gender<br>mshr_hcmpersongender opciju kopa | Lasīt/rakstīt<br>Neobligāti | Kandidāta dzimums. |
| **Dzimšanas datums**<br>mshr_birthdate<br>Datetime | Lasīt/rakstīt<br>Neobligāti | Kandidāta dzimšanas datums. |
| **Pilsonības valsts kods**<br>mshr_citizenshipcountrycode<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Norāda valsti, kur kandidātam ir pilsonība. Derīgie valstu kodi ir norādīti mshr_logisticaddresscountryregionentity. |
| **Veterāna statusa ID**<br>mshr_veteranstatusid<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Norāda kandidāta veterāna statusu. |
| **Veterāna statusa ID vērtība**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmveteranstatusentity mshr_hcmveteranstatusentityid | Sistēmas ģenerēts unikāls identifikators veterāna statusa elementa ierakstam. |
| **Karadienesta sākuma datums**<br>mshr_militaryservicestartdate<br>Datetime | Lasīt/rakstīt<br>Neobligāti | Kandidāta militārā dienesta sākuma datums. |
| **Karadienesta beigu datums**<br>mshr_militaryserviceenddate<br>Datetime | Lasīt/rakstīt<br>Neobligāti | Kandidāta militārā dienesta beigu datums. |
| **Ir invalīds veterāns**<br>mshr_isdisabledveteran<br>mshr_noyes opciju kopa | Lasīt/rakstīt<br>Neobligāti | Norāda, vai kandidāts veterāna statusā tika atvaļināts. |
| **Pieejamības datums**<br>mshr_availabilitydate<br>Datetime | Lasīt/rakstīt<br>Neobligāti | Agrākais datums, kad kandidāts būs pieejams darbam. |
| **Ir gatavs mainīt dzīvesvietu**<br>mshr_iswillingtorelocate<br>mshr_noyes opciju kopa | Lasīt/rakstīt<br>Neobligāti | Norāda, vai kandidāts ir gatavs amatam pārcelties uz citu dzīves vietu. |
| **Komentāri**<br>mshr_comments<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Komentāri, ko izmantos personāla atlases vadītājs vai pieņemšanas darbā vadītājs. |
| **Programmas integrācijas rezultāts**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult opciju kopa | Lasīt/rakstīt<br>Obligāts | Ar integrāciju saistītā kandidāta statuss darbā pieņemšanas procesā. |
| **Nenolīgšanas iemesla koda ID**<br>mshr_donothirereasoncodeid<br>Virkne | Lasīt/rakstīt<br>Neobligāti | Pēc izvēles pamatojuma kods tiek nodrošināts, ja statuss (programmas integrācijas rezultāts) ir iestatīts uz "Nav nolīgts". |
| **Iemesla koda ID vērtība**<br>_mshr_fk_reasoncode_id_value<br>GUID | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmreasoncodeentity elementa mshr_hcmreasoncodeentityid | Sistēmas ģenerēts unikālais identifikators iemesla kodam **Nav nolīgts**. |
| **Datu apgabala ID**<br>mshr_dataareaid<br>Virkne | Lasīt/rakstīt<br>Neobligāti |  Norāda juridisko personu (uzņēmumu). |
| **Datu apgabala ID vērtība**<br>_mshr_dataareaid_id_value<br>GUID | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: cdm_companyid cdm_company elements | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu). |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]