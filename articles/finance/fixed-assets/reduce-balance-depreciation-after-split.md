---
title: Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma
description: Šajā tēmā aprakstīta metode, kas tiek izmantota pamatlīdzekļos, lai aprēķinātu nolietojumu pēc līdzekļa sadalīšanas, izmantojot bilances samazināšanas metodi.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 056808b7d4d490bc4d60aa058108d159c1d4867c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826255"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta metode, kas tiek izmantota pamatlīdzekļos, lai aprēķinātu nolietojumu pēc līdzekļa sadalīšanas citā līdzeklī, izmantojot bilances samazināšanas metodi. Nolietojuma gads, kas ir konfigurēts līdzekļa grāmatā, ir finanšu gads. Lai iegūtu papildu informāciju, skatiet sadaļas [Nolietojuma bilances samazināšana](reduce-balance-depreciation.md) un [Pamatlīdzekļa sadalīšana](tasks/split-fixed-asset.md).

Ja pamatlīdzeklis tiek sadalīts finanšu periodā, kas ir vēlāks par periodu, kad pamatlīdzeklis tika iegūts, samazinātais bilances nolietojums attieksies uz pamatlīdzekļa atlikušo vērtību (AV) iepriekšējā gadā. Tas arī attieksies uz ieguves un nolietojuma korekcijas darījumiem, kas tika izveidoti no darījuma, kas sadalīja līdzekli. Šī darbība pieņem, ka līdzeklis tika iegūts vienā finanšu gadā un sadalīts vēlākā finanšu gadā. Summa, kas ir jāizlieto oriģinālajam līdzeklim pēc sadalījuma, ataino pamatlīdzekļa AV pirms līdzekļa sadalīšanas, kā arī ieguves un nolietojuma korekcijas darījumu, kas tika grāmatots sadalīšanai.

Piemēram, ir spēkā šādi nosacījumi:

- Finanšu periods ir no 30. jūnija līdz 1. jūlijam.
- Bilances samazinājuma procentuālā vērtība ir 18 procenti, un līdzeklis tiek iegūts 2019. jūnijā par $ 10 000 iegādes cenu.
- Pirmā finanšu gada nolietojums ir vienāds ar $ 18 000, mēneša nolietojums ir vienāds ar $ 150, un pamatlīdzeklis tiek nolietots līdz 2019. novembrim (summa ir $ 738,75).
- 2019. novembrī 80 procenti līdzekļa tiek sadalīti uz citu līdzekli.

[![Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Oriģinālā pamatlīdzekļa nolietošanas summa ir $ 1822,25. Šī summa ir vienāda ar AV pirms sadalītā darījuma grāmatošanas ($ 9111,25), pieskaitot iegādes korekciju, kas tiek ģenerēta, grāmatojot sadalīto darījumu (-$ 8000), kā arī nolietojuma korekciju, kas tiek ģenerēta sadalīšanas darījumā ($ 711). Tāpēc nolietojums otrajā gadā ir (1822,25 × 18 procenti) ÷ 12 = $ 27,33.

Jaunā pamatlīdzekļa nolietošanas summa pirmajā gadā ir (8000 × 18 procenti) ÷ 12 = $ 120.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]