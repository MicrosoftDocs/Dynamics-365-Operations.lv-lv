---
title: Nolietojuma metodes un konvencijas
description: "Šajā rakstā ir sniegts pārskats par nolietojuma aprēķināšanas nosacījumiem un metodēm, ko atbalsta programma Microsoft Dynamics AX."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>Nolietojuma metodes un konvencijas

Šajā rakstā ir sniegts pārskats par nolietojuma aprēķināšanas nosacījumiem un metodēm, ko atbalsta programma Microsoft Dynamics AX.

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

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

[125 % atlikumu bilances nolietojums](125-percent-reducing-balance-depreciation.md)

[150 % atlikumu bilances nolietojums](150-percent-reducing-balance-depreciation.md)

[175 % atlikumu bilances nolietojums](175-percent-reducing-balance-depreciation.md)

[200 % atlikumu bilances nolietojums](200-percent-reducing-balance-depreciation.md)


