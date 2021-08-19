---
title: Nolietojuma priekšlikuma izveide
description: Šajā tēmā ir aprakstīts, kā darbojas nolietojuma partijas priekšlikumi, un paskaidrots, kā piedāvāt pamatlīdzekļu nolietojumu.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6cf285e8764af8c6525fb3f9cbec7306917e57e832777588e8c2c1d4aeed818
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719250"
---
# <a name="create-a-depreciation-proposal"></a>Nolietojuma priekšlikuma izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā darbojas nolietojuma partijas priekšlikumi, un paskaidrots, kā piedāvāt pamatlīdzekļu nolietojumu. Šajā uzdevumā izmantots USMF demonstrācijas uzņēmums un grāmatveža loma.


## <a name="create-a-depreciation-proposal"></a>Nolietojuma priekšlikuma izveide
1. Navigācijas rūtī ejiet uz **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma priekšlikumu**.
2. Laukā **Žurnāla nosaukums** nolaižamajā izvēlnē atlasiet opciju.
3. Ievadiet datumu laukā **Līdz datumam**.

    - Atlasiet opciju **Nolietojuma kopsavilkums**, lai apkopotu ikmēneša nolietojumus vienā žurnāla rindā.  
    - Piemēram, ja beigu datuma vērtība ir 2015. gada 31. marts, tiek ģenerēts šādam apraksts: "Nolietojums kopš 2015. gada 31. janvāra". Tad lauks **Datums** piedāvātajās žurnāla līnijās tiek iestatīts kā 2015. gada 31. marts.  
    - Nolietojuma priekšlikumu var filtrēt pēc līdzekļa, līdzekļa grupas vai cita kritērija, izmantojot opciju **Filtrēt**.  
    - Izmantojot veidlapu **Izveidot pamatlīdzekļu iegādes vai nolietojuma priekšlikumu**, varat izteikt priekšlikumu par nolietojumu partijām. Šo iespēju ieteicams izmantot lielākiem priekšlikumiem, kas aizņem vairāk sistēmas resursu. Ja atlasāt pakešu opciju, šajā laikā varat pabeigt citus uzdevumus. Kad piedāvājat nolietojumu veikt šādi, nolietojums tiek aprēķināts pamatlīdzekļu vērtības modeļiem.  

4. Atlasiet **Izveidot žurnālu**.

## <a name="review-depreciation-entries"></a>Nolietojuma ierakstu pārskatīšana
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Atlasiet **Rindas**.
4. Atlasiet **Grāmatot**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]