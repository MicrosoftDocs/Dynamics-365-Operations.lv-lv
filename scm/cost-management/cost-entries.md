---
title: Izmaksu ieraksti
description: "Šajā rakstā ir sniegta informācija par izmaksu ierakstiem un to, kad tie tiek izveidoti. Izmaksu ieraksts ir ieraksts, kas reģistrē noteikta notikuma daudzumu un izmaksas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1045ecbf7080f12bc60336609180173544e4e0eb
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="cost-entries"></a>Izmaksu ieraksti

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par izmaksu ierakstiem un to, kad tie tiek izveidoti. Izmaksu ieraksts ir ieraksts, kas reģistrē noteikta notikuma daudzumu un izmaksas.

Izmaksu ieraksti ir tādu krājumu transakciju apkopojumi, kas ir reģistrētas aktīvajās finanšu krājumu dimensijās.

## <a name="examples"></a>Piemēri
### <a name="example-1-no-cost-entries-are-created"></a>1. piemērs: netiek izveidoti izmaksu ieraksti

Tiek reģistrēts pārsūtīšanas žurnāla notikums. Notikuma ietvaros viens krājuma A gabals tiek pārsūtīts no novietojuma A uz novietojumu B. Krājumu dimensija Novietojums nav uzskatāma par daļu no izmaksu objekta. Tādējādi notikuma ietvaros tiek izveidotas divas krājumu transakcijas un netiek izveidoti izmaksu ieraksti.

### <a name="example-2-cost-entries-are-created"></a>2. piemērs: tiek izveidoti izmaksu ieraksti

Tiek reģistrēts pārsūtīšanas žurnāla notikums. Notikuma ietvaros viens krājuma A gabals tiek pārsūtīts no 1. vietas uz 2. vietu. Krājumu dimensija Vieta tiek uzskatīta par daļu no izmaksu objekta. Tādējādi notikuma ietvaros tiek izveidotas divas krājumu transakcijas un divi izmaksu ieraksti.

### <a name="example-3-one-cost-entry-is-created"></a>3. piemērs: tiek izveidots viens izmaksu ieraksts

Pirkšanas pasūtījumam tiek reģistrēts produktu ieejas plūsmas notikums. Notikuma ietvaros tiek reģistrēti 100 krājuma A gabali, kuru vienības izmaksas ir 10,00 ASV dolāri (USD). Tā kā krājumam A tiek izmantots sērijas numuru, lai izsekotu krājumu vadības mērķi, katram saņemtajam krājumam tiek izveidots unikāls sērijas numurs. Tādējādi notikuma ietvaros tiek izveidotas 100 krājumu transakcijas un viens izmaksu ieraksts.

## <a name="cost-entries-page"></a>Izmaksu ierakstu lapa
Jaunā lapa **Izmaksu ieraksti** ļauj skatīt un kontrolēt daudzuma un izmaksu reģistrācijas. Šī lapa papildina lapas **Krājumu darbība** un **Krājumu nosegšana**. Notikuma ieraksti tiek reģistrēti hronoloģiskā secībā. Tādējādi var ātri atrast un kontrolēt uzkrātās izmaksas noteiktam notikumam vai visiem notikumiem, kas ir saistīti ar dokumentu. Tālāk minēts piemērs:

-   Krājumam A tiek reģistrēts produktu ieejas plūsmas notikums. Ir saņemti 100 gabali, kuru vienības izmaksas ir 10,00 USD.
-   Dažas dienas pēc rēķina notikuma reģistrēšanas, izmaksas palielinās līdz 11,00 USD. Tādējādi kopsumma ir 1100 USD. Tiek izveidots otrais dokuments, lai uzskaitītu 100 USD starpību.
-   Dažas dienas vēlāk pirkšanas pasūtījumā tiek reģistrēta papildmaksa 15,00 USD transportēšanas izmaksu segšanai.

| Dokuments | Datums       | Atsauce      | Skaits | Laidiena ID  | Daudzums | Summa  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01.01.2015 | Pirkšanas pasūtījums | 100001 | 0000101 | 100,00   | 1000,00 |
| 00002   | 20.01.2015 | Pirkšanas pasūtījums | 100001 | 0000101 |          | 100,00  |
| 00003   | 31.01.2015 | Korekcija     | 100001 | 0000101 |          | 15,00   |

Lapa **Izmaksu ieraksti** ļauj veikt filtrēšanu pēc dokumenta ID un dokumenta datuma. 

> [!NOTE]
> Izmaksu ieraksti ir pieejami tikai [izmaksu objektiem](cost-object.md) vai izlaistajām precēm.

<a name="see-also"></a>Skatiet arī
--------

[Izmaksu objekti](cost-object.md)




