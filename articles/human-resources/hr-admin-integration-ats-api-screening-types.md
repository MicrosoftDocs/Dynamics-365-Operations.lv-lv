---
title: Izvērtēšanas tipi
description: Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126174"
---
# <a name="screening-types"></a>Izvērtēšanas tipi

Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .

Fiziskais nosaukums: mshr_hcmscreeningtypeentity

## <a name="description"></a>Apraksts

Šis elements apraksta izvērtēšanas tipus, ko uzņēmums iestatījis pirms darbā pieņemšanas un notiekošajiem darbinieku izvērtēšanas procesiem.

## <a name="json-representation"></a>JSON pārstāvība

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Izvērtēšanas veida elementa ID**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Tikai lasāms<br>Obligāts<br>Sistēmas ģenerēts | Unikāls izvērtēšanas veida ieraksta primārais identifikators. |
| **Izvērtēšanas veida ID**<br>mshr_screeningtypeid<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Lietotāja definēts unikāls izvērtēšanas veida primārais identifikators. |
| **Apraksts**<br>mshr_description<br>*Virkne* | Lasīt/rakstīt<br>Obligāts | Izvērtēšanas veida apraksts. |
| **Biežuma vienība**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit opciju kopa* | Lasīt/rakstīt<br>Obligāts | Apraksta, cik bieži izvērtēšana jāveic nozīmētai personai. |
| **Ģenerēt no**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom opciju kopa* | Lasīt-rakstīt<br>Obligāts | Ja Biežuma vērtība ir jebkura vērtība, kas nav "Tikai vienu reizi", vērtība GenerateFrom nosaka datumu, no kura aprēķināt nākamo izvērtēšanas notikumu. |
| **Biežuma intervāls**<br>mshr_frequencyinterval<br>*Vesels skaitlis* | Lasīt-rakstīt<br>Obligāts | Ja biežuma vērtība ir jebkura vērtība, kas nav "Tikai vienu reizi", jums ir jādefinē laika vienību intervāls starp katru izvērtēšanas notikumu. |

## <a name="see-also"></a>Skatiet arī

[Kandidāta izsekošanas sistēmas integrācijas API ievads](hr-admin-integration-ats-api-introduction.md)<br>
[Piemērs Kandidāta vaicājumam par nolīgšanu](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
