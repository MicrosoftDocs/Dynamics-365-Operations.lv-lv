---
title: Nolietojuma metodes un konvencijas
description: "Šajā rakstā ir sniegts pārskats par nolietojuma aprēķināšanas nosacījumiem un metodēm, ko atbalsta programma Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6ddd496aecf850a4c98043780f98e9fba8e62b49
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="depreciation-methods-and-conventions"></a>Nolietojuma metodes un konvencijas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par nolietojuma aprēķināšanas nosacījumiem un metodēm, ko atbalsta programma Microsoft Dynamics 365 for Operations.

Var atlasīt dažādas nolietojuma metodes un konvencijas. Šo metožu nolūks ir sadalīt pamatlīdzekļa nolietojuma vērtību pa finanšu periodiem. Pamatlīdzekļa nolietojuma vērtība ir iegādes cenas un lūžņu vērtības (ja tāda ir) starpība. 

Ja izmantojat nolietojuma konvencijas un modificējat pamatlīdzekļa pēdējo nolietojuma aprēķināšanas datumu, tādējādi izraisot dažu nolietojuma aprēķinu izlaišanu, nolietojums pēdējā gadā var būt lielāks vai mazāks par paredzēto. Nolietojums tiek koriģēts ar nolietojuma periodu skaitu, ko ietekmē pēdējā nolietojuma aprēķināšanas datuma modifikācija.

Piemēram, ja trīs gadus lietojat pusgada nolietojuma konvenciju, nolietošanās parasti notiek 3 1/2 gados. Ja trīsarpus gadu laikā maināt pēdējo nolietojuma aprēķināšanas datumu, pēdējais nolietojums iziet ārpus ietekmēto periodu skaita. Ja maināt datumu par trīs mēnešiem, pēdējam gadam tiek aprēķināts deviņu mēnešu nolietojums, lai gan parasti tam vajadzētu būt sešu mēnešu nolietojumam.

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
-   Manuālā
-   Koeficients
-   Patēriņš
-   Lineārais atlikušais mūžs
-   200% atlikumu bilance
-   175% atlikumu bilance
-   150% atlikumu bilance
-   125% atlikumu bilance

 



<a name="see-also"></a>Skatiet arī
--------

[Pamatlīdzekļu nolietojums](fixed-asset-depreciation.md)

[Lineārā lietošanas ilguma nolietojums](Straight-line-service-life-depreciation.md)

[Degresīvā nolietojuma aprēķināšanas metode](reduce-balance-depreciation.md)

[Manuāls nolietojuma aprēķins](manual-depreciation.md)

[Reizinātāja nolietojums](factor-depreciation.md)

[Patēriņa nolietojuma aprēķins](consumption-depreciation.md)

[Atlikušā lietošanas ilguma lineārā aprēķināšanas metode](straight-line-life-remaining-depreciation.md)

[125 procentu degresīvā nolietojuma aprēķināšanas metode](125-percent-reducing-balance-depreciation.md)

[150 procentu degresīvā nolietojuma aprēķināšanas metode](150-percent-reducing-balance-depreciation.md)

[175 procentu degresīvā nolietojuma aprēķināšanas metode](175-percent-reducing-balance-depreciation.md)

[200 procentu degresīvā nolietojuma aprēķināšanas metode](200-percent-reducing-balance-depreciation.md)




