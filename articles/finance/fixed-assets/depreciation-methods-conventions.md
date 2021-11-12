---
title: Nolietojuma metodes un konvencijas
description: Šajā rakstā ir sniegts apskats par nolietojuma aprēķināšanas metodēm un nolietojuma metodēm, kas tiek atbalstītas programmā Microsoft Dynamics 365 Finance.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6abf98b4c1eee3657960a1912445171acc0686a
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674530"
---
# <a name="depreciation-methods-and-conventions"></a>Nolietojuma metodes un konvencijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts apskats par atbalstītajām nolietojuma aprēķināšanas metodēm un nolietojuma metodēm.

Var atlasīt dažādas nolietojuma metodes un konvencijas. Šo metožu nolūks ir sadalīt pamatlīdzekļa nolietojuma vērtību pa finanšu periodiem. Pamatlīdzekļa nolietojuma vērtība ir iegādes cenas un lūžņu vērtības (ja tāda ir) starpība. 

Ja izmantojat nolietojuma konvencijas un modificējat pamatlīdzekļa pēdējo nolietojuma aprēķināšanas datumu, tādējādi izraisot dažu nolietojuma aprēķinu izlaišanu, nolietojums pēdējā gadā var būt lielāks vai mazāks par paredzēto. Nolietojums tiek koriģēts ar nolietojuma periodu skaitu, ko ietekmē pēdējā nolietojuma aprēķināšanas datuma modifikācija.

Piemēram, ja vairāk kā trīs gadus lietojat pusgada nolietojuma konvenciju, nolietošanās parasti notiek trīs ar pusi gados. Ja trīsarpus gadu laikā maināt pēdējo nolietojuma aprēķināšanas datumu, pēdējais nolietojums iziet ārpus ietekmēto periodu skaita. Ja maināt datumu par trīs mēnešiem, pēdējam gadam tiek aprēķināts deviņu mēnešu nolietojums, lai gan parasti tam vajadzētu būt sešu mēnešu nolietojumam.

Varat atlasīt kādu no tālāk norādītajām nolietojuma konvencijām.


-   Pusgads
-   Pilns mēnesis
-   Puse ceturkšņa
-   Puse mēneša (mēneša 1. datums)
-   Puse mēneša (mēneša 15. datums)
-   Pusgads (gada sākums)
-   Puse gada (nākamais gads)

Varat atlasīt kādu no tālāk norādītajām nolietojuma metodēm.
-   Lineārais lietošanas ilgums
-   Atlik. samazinošā
-   Manuāli
-   Koeficients
-   Patēriņš
-   Lineārais atlikušais mūžs
-   200% atlikumu bilance
-   175% atlikumu bilance
-   150% atlikumu bilance
-   125% atlikumu bilance





## <a name="additional-resources"></a>Papildu resursi

[Pamatlīdzekļu nolietojums](fixed-asset-depreciation.md)

[Lineārais pakalpojuma novecojums](Straight-line-service-life-depreciation.md)

[Degresīvā nolietojuma aprēķināšanas metode](reduce-balance-depreciation.md)

[Pamatlīdzekļu manuālais nolietojums](manual-depreciation.md)

[Koeficienta nolietojums](factor-depreciation.md)

[Patēriņa nolietojuma aprēķins](consumption-depreciation.md)

[Atlikušā lietošanas ilguma lineārā aprēķināšanas metode](straight-line-life-remaining-depreciation.md)

[125 procentu degresīvā nolietojuma aprēķināšanas metode](125-percent-reducing-balance-depreciation.md)

[150 procentu degresīvā nolietojuma aprēķināšanas metode](150-percent-reducing-balance-depreciation.md)

[175 procentu degresīvā nolietojuma aprēķināšanas metode](175-percent-reducing-balance-depreciation.md)

[200 procentu degresīvā nolietojuma aprēķināšanas metode](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
