---
title: Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma
description: Šajā rakstā ir aprakstīta metode, kas tiek izmantota pamatlīdzekļos nolietojuma aprēķināšanai pēc pamatlīdzekļa sadalīšanas, izmantojot bilances samazināšanas metodi.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883305"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīta metode, kas tiek izmantota pamatlīdzekļos nolietojuma aprēķināšanai pēc pamatlīdzekļa sadalīšanas citā, izmantojot bilances samazināšanas metodi. Nolietojuma gads, kas ir konfigurēts līdzekļa grāmatā, ir finanšu gads. Lai iegūtu papildu informāciju, skatiet sadaļas [Nolietojuma bilances samazināšana](reduce-balance-depreciation.md) un [Pamatlīdzekļa sadalīšana](tasks/split-fixed-asset.md).

Ja pamatlīdzeklis tiek sadalīts finanšu periodā, kas ir vēlāks par periodu, kad pamatlīdzeklis tika iegūts, samazinātais bilances nolietojums attieksies uz pamatlīdzekļa atlikušo vērtību (AV) iepriekšējā gadā. Tas arī attieksies uz ieguves un nolietojuma korekcijas darījumiem, kas tika izveidoti no darījuma, kas sadalīja līdzekli. Šī darbība pieņem, ka līdzeklis tika iegūts vienā finanšu gadā un sadalīts vēlākā finanšu gadā. Summa, kas ir jāizlieto oriģinālajam līdzeklim pēc sadalījuma, ataino pamatlīdzekļa AV pirms līdzekļa sadalīšanas, kā arī ieguves un nolietojuma korekcijas darījumu, kas tika grāmatots sadalīšanai.

Piemēram, ir spēkā šādi nosacījumi:

- Finanšu periods ir no 30. jūnija līdz 1. jūlijam.
- Bilances samazinājuma procentuālā vērtība ir 18 procenti, un līdzeklis tiek iegūts 2019. jūnijā par $ 10 000 iegādes cenu.
- Pirmā finanšu gada nolietojums ir vienāds ar $ 18 000, mēneša nolietojums ir vienāds ar $ 150, un pamatlīdzeklis tiek nolietots līdz 2019. novembrim (summa ir $ 738,75).
- 2019. novembrī 80 procenti līdzekļa tiek sadalīti uz citu līdzekli.

[![Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Oriģinālā pamatlīdzekļa nolietošanas summa ir $ 1822,25. Šī summa ir vienāda ar AV pirms sadalītā darījuma grāmatošanas ($ 9111,25), pieskaitot iegādes korekciju, kas tiek ģenerēta, grāmatojot sadalīto darījumu (-$ 8000), kā arī nolietojuma korekciju, kas tiek ģenerēta sadalīšanas darījumā ($ 711). Tāpēc nolietojums otrajā gadā ir (1822,25 × 18 procenti) ÷ 12 = $ 27,33.

Jaunā pamatlīdzekļa nolietošanas summa pirmajā gadā ir (8000 × 18 procenti) ÷ 12 = $ 120.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
