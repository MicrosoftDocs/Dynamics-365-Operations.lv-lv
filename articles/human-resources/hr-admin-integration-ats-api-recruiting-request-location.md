---
title: Darbā pieņemšanas pieprasījuma atrašanās vieta
description: Šajā tēmā aprakstīta personāla atlases pieprasījuma atrašanās vietas elements, kas iestatīts programmā Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9a3b47c76094adb6c601daf2f9583116255b0a99
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465946"
---
# <a name="recruiting-request-location"></a>Darbā pieņemšanas pieprasījuma atrašanās vieta

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā aprakstīta personāla atlases pieprasījuma atrašanās vietas elements, kas iestatīts programmā Dynamics 365 Human Resources.

Fiziskais nosaukums: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>Apraksts

To vietu saraksts, kas definētas kā vietas, kur darbā pieņemtie darbinieki strādās pēc nolīgšanas. Šīs ir vietas, kas izveidotas juridiskajām personām.

### <a name="json-representation"></a>JSON pārstāvība

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Atrašanās vietas ID**<br>mshr_locationid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Sistēmas ģenerēts lietotājam lasāms identifikators darbā pieņemšanas atrašanās vietai. |
| **Darbā pieņemšanas pieprasījuma atrašanās vieta**<br>mshr_recruitingrequestlocationid<br>*Virkne* | Rakstīt vienu reizi<br>Obligāts | Lietotāja definēts unikāls darbā pieņemšanas atrašanās vietas identifikators. |
| **Personāla atlases pieprasījuma atrašanās vietas elementa ID**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Tikai lasāms<br>Obligāts | Sistēmas ģenerēts unikāls identifikators Personāla atlases pieprasījuma atrašanās vietas ierakstam. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Vietas apraksts. |
| **Valsts/reģiona ID**<br>mshr_countryregionid<br>*Virkne* | Tikai lasāms<br>Neobligāti | Norāda valsti vai reģionu, kur kandidātam ir pilsonība. |
| **Valsts/reģiona ID vērtība**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: mshr_logisticsaddresscountryregionentity mshr_logisticaddresscountryregionentityid | Sistēmas ģenerēts unikālais adreses valsts/reģiona identifikators. |
| **Pasta indekss**<br>mshr_zipcode<br>*Virkne* | Tikai lasāms<br>Neobligāti | Pasta indekss. |
| **Iela**<br>mshr_street<br>*Virkne* | Tikai lasāms<br>Neobligāti | Ielas adrese. |
| **Pilsēta**<br>mshr_city<br>*Virkne* | Tikai lasāms<br>Neobligāti | Pilsēta. |
| **Novads**<br>mshr_state<br>*Virkne* | Tikai lasāms<br>Neobligāti | Novads. |
| **Pagasts**<br>mshr_county<br>*Virkne* | Tikai lasāms<br>Neobligāti | Pagasts. |
| **Tālrunis**<br>mshr_telephone<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Atrašanās vietas tālruņa numurs. |
| **E-pasts**<br>mshr_email<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | E-pasta adrese. |
| **InternetAddress**<br>mshr_internetaddress<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Atrašanās vietas vietnes vietrādis URL. |
| **Datu apgabala ID**<br>mshr_dataareaid<br>*Virkne* | Lasīt/rakstīt<br>Neobligāti | Norāda juridisko personu (uzņēmumu). |
| **Datu apgabala ID vērtība**<br>_mshr_dataareaid_id_value<br>*GUID* | Tikai lasāms<br>Neobligāti<br>Ārējā atslēga: cdm_companyid cdm_company elements | Sistēmas ģenerēta GUID vērtība, kas identificē juridisko personu (uzņēmumu). |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs personāla atlases pieprasījuma vaicājumam](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]