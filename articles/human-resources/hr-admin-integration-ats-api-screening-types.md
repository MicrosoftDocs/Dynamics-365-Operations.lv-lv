---
title: Izvērtēšanas tipi
description: Šajā tēmā aprakstīta Izvērtēšanas tipi entītija programmai Dynamics 365 Human Resources .
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
ms.openlocfilehash: a7e726f88eb5c00fef98256de7a8f924156ba8f52392bc4dc6ae6e7914227152
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782172"
---
# <a name="screening-types"></a>Izvērtēšanas tipi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]