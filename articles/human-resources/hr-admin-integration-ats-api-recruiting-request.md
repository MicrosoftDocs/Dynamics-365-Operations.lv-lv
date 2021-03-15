---
title: Pieņemšanas darbā pieprasījums
description: Šajā tēmā aprakstīts pieņemšanas darbā pieprasījuma elements, kas iestatīts programmā Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 572ee0755e331d19b41442e3614effb92db95a92
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125429"
---
# <a name="recruiting-request"></a>Pieņemšanas darbā pieprasījums

Šajā tēmā aprakstīts pieņemšanas darbā pieprasījuma elements, kas iestatīts programmā Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequestentity

### <a name="description"></a>Apraksts

Apraksta pieprasījumu pieņemt darbā.

### <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Pieņemšanas darbā pieprasījuma ID**<br>mshr_recruitingrequestid<br>*Virkne* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Lietotājam lasāms unikālais identifikators pieprasījumam, kas parādīts HR programmā. Numuru sērija. |
| **Personāla atlases pieprasījuma elementa ID**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbā pieņemšanas pieprasījumu. |
| **Datu apgabala ID**<br>mshr_dataareaid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti<br> | Norāda juridisko personu (uzņēmumu) personāla atlases pieprasījumam. |
| **Datu apgabala ID vērtība**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: cdm_companyid cdm_company elements | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu) personāla atlases pieprasījumam. |
| **Darbā pieņemšanas vadītāja personāla numurs**<br>mshr_hiringmanagerpersonnelnumber<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Ar šo personāla atlases pieprasījumu saistītā nolīgšanas vadītāja personāla numurs. |
| **Nolīgšanas vadītāja ID vērtība**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmworkerbaseentity elementa mshr_hcmworkerbaseentityid | Sistēmas ģenerēta GUID vērtība, lai identificētu vadītāju, kas saistīts ar personāla atlases pieprasījumu. |
| **Personāla atlases darbinieka puses numurs**<br>mshr_recruiterpartynumber<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Pieprasījumam atlasītā darbā pieņēmēja personas (puses) numurs. |
| **Darbā pieņēmēja ID vērtība**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_dirpersonentity elementa mshr_dirpersonentityid | Sistēmas ģenerēta GUID vērtība, lai identificētu darbā pieņēmēju, kas saistīts ar personāla atlases pieprasījumu. |
| **Statuss**<br>mshr_status<br>*RecruitingRequestStatus* opciju kopa | Lasīt/rakstīt<br>Obligāts<br> | Norāda darbā pieņemšanas pieprasījuma statusu. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Apraksta pieprasījumu. |
| **Darbā pieņemšanas pieprasījuma atrašanās vietas ID**<br>mshr_recruitingrequestlocationid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Lietotājam lasāms ar šo pieprasījumu saistītais darba atrašanās vietas unikālais identifikators. |
| **Darbā pieņemšanas atrašanās vietas ID vērtība**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmrecruitingrequestlocationentity elementa mshr_hcmrecruitingrequestlocationentityid | Sistēmas ģenerēta GUID vērtība, lai identificētu darbā pieņemšanas pieprasījuma atrašanās vietu, kas atlasīta pieprasījumam. |
| **Komentāri**<br>mshr_comments<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Komentāri par izmantošanas pieprasījumu, ko iesnieguši darbinieku nolīgšanas vadītāji un personāla atlases veicēji. |
| **Darba ID**<br>mshr_jobid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts |   Lietotājam lasāms ar šo pieprasījumu saistītais visu amatu kopīgotais unikālais identifikators. |
| **Darba ID vērtība**<br>_mshr_fk_job_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmjobentity elementa mshr_hcmjobentityid | Sistēmas ģenerēts ar šo darbā pieņemšanas pieprasījumu saistītais visu amatu kopīgotais unikālais identifikators. |
| **Nosaukuma ID**<br>mshr_titleid<br>*Virkne* | Tikai lasāms<br>Obligāts | Lietotājam lasāms ar šo pieprasījumu saistītais darba nosaukuma unikālais identifikators. |
| **Nosaukuma ID vērtība**<br>_mshr_fk_title_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmtitleentity elementa mshr_hcmtitleid | Sistēmas ģenerēts unikāls identifikators tā darba nosaukumam, kas atlasīts darbā pieņemšanas pieprasījumam. |
| **Darba funkcijas ID**<br>mshr_jobfunctionid<br>*Virkne* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_hcmjobfunctionentity elementa mshr_jobfunctionid | Lietotājam lasāms ar šo pieprasījumu saistītais darba funkcijas unikālais identifikators. |
| **Noklusējuma pilnas slodzes ekvivalents**<br>mshr_defaultfulltimeequivalency<br>*Dubults* | Tikai lasāms<br>Obligāts | Pilna laika ekvivalenta vērtība darbam, kur 1,0 attēlo pilna laika darbinieku. |
| **Normatīvā darba kategorija**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory* opciju kopa | Tikai lasāms<br>Neobligāti | Darbam atlasītās darba funkcijas EEO darba kategorija. Opciju kopā HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) iekļautās derīgās vērtības. |
| **Darba veida ID**<br>mshr_jobtypeid<br>*Virkne* | Tikai lasāms<br>Neobligāti | Darba veids, kas saistīts ar amatu. Darbu veidi ir lietotāja definētas vērtības, kas pieejamas elementā mshr_hcmjobtypeentity. |
| **Darba veida ID vērtība**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmjobtypenentity elementa mshr_hcmjobtypeentityid | Sistēmas ģenerēts ar darba veida identifikators, kas saistīts ar darbu darbā pieņemšanas pieprasījumam. |
| **Nodokļu atvieglojumu statuss**<br>mshr_exemptstatus<br>*JobExemptStatus* opciju kopa | Tikai lasāms<br>Neobligāti | FLSA neapliekamā statusa pamatā ir darba veids. |
| **Plānotais sākuma datums**<br>mshr_estimatedstartdate<br>*Datums* | Lasīt/rakstīt<br>Obligāts | Plānotais datums, kad kandidāts sāktu darbu. |
| **Ārējais apraksts**<br>mshr_externaldescription<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Uz kandidātu orientēts darba/amata apraksts. | Atlīdzības zemais slieksnis<br>mshr_compensationlowthreshold<br>*Dubults* | Lasīt/rakstīt<br>Neobligāti | Atlīdzības līmeņa apakšējā robeža. |
| **Atlīdzības kontrolpunkts**<br>mshr_compensationcontrolpoint<br>*Dubults* | Lasīt/rakstīt<br>Neobligāti | Atlīdzības līmeņa kontrolpunkts. |
| **Atlīdzības augstais slieksnis**<br>mshr_compensationhighthreshold<br>*Dubults* | Lasīt/rakstīt<br>Neobligāti | Atlīdzības līmeņa augšējā robeža. |
| **Atlīdzības līmenis**<br>mshr_compensationlevelid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Darba atlīdzības līmenis. Darbu var iestatīt ar vairākiem atlīdzības līmeņiem. Šis atribūts norāda šim pieprasījumam atlasīto darba atlīdzības līmeni. |
| **Darba atlīdzības ID**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_hcmjobcompensationentity elementa mshr_hcmjobcompensationentityid | Sistēmas ģenerēts ar atlīdzības līmeņa identifikators, kas saistīts ar darbā pieņemšanas pieprasījuma darbu. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]