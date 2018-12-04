---
title: "Pašreizējās vidējās izmaksu cenas izsekošana pēc krājumu dimensijas"
description: "Katrai krājumu vienībai ir piesaistīta krājumu dimensiju grupa. Tāpēc krājuma kārtējo vidējo izmaksu cena tiek aprēķināta, pamatojoties uz atlasītajām krājumu dimensijām, kas tiek finansiāli izsekotas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 48db7ff047a50343bd473d2c71f878e4ee2201e5
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="track-running-average-cost-per-inventory-dimension"></a>Pašreizējās vidējās izmaksu cenas izsekošana pēc krājumu dimensijas

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Katrai krājumu vienībai ir piesaistīta krājumu dimensiju grupa. Tāpēc krājuma kārtējo vidējo izmaksu cena tiek aprēķināta, pamatojoties uz atlasītajām krājumu dimensijām, kas tiek finansiāli izsekotas.

Ir pieejami trīs krājumu dimensiju veidi: preces, uzglabāšanas un izsekošanas dimensijas. Krājumu dimensijas ietver konfigurāciju, izmēru un krāsu. Krājumu dimensijas vienmēr tiek izsekotas finansiāli. Uzglabāšanas un izsekošanas dimensijas ietver vietu, noliktavu, novietojumu, krājumu statusu, noliktavas vienību, partijas numur un sērijas numuru. Varat izvēlēties, kuras uzglabāšanas un izsekošanas dimensijas tiek izsekotas finansiāli. 

**1. piemērs** 

Ja krājumu dimensiju grupa, kas ir piesaistīta krājumam, tiek finansiāli izsekota pēc noliktavas, tad kārtējo vidējo izmaksu cena tiek aprēķināta katrai noliktavai. Rēķinā ir iekļauti šādi pirkšanas pasūtījumi:

-   Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 2 un izmaksu cenu USD 10,00 noliktavai GW.
-   Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 3 un izmaksu cenu USD 12,00 noliktavai GW.
-   Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 5 un izmaksu cenu USD 15,00 noliktavai MW.

Kārtējo vidējo izmaksu cena noliktavai GW ir USD 11,20, bet noliktavai MW tā ir USD 15,00. Tiek grāmatots pārdošanas pasūtījuma rēķins noliktavai GW. Krājumu vērtība un pārdoto preču pašizmaksa (pirms krājumu slēgšanas un noliktavas iezīmēšanas) ir USD 11,20. Tiek grāmatots cits pārdošanas pasūtījums noliktavai MW. Krājumu vērtība un pārdoto preču pašizmaksa (pirms krājumu slēgšanas un noliktavas iezīmēšanas) ir USD 15,00. 

**2. piemērs.** Ja noliktavas dimensiju grupa, kas ir piesaistīta krājumam, tiek finansiāli izsekota pēc noliktavas un izsekošanas dimensiju grupa tiek finansiāli izsekota pēc partijas numura, kārtējo vidējo izmaksu cena tiek aprēķināta katrai partijai. 

**Piezīme.** Ir ieteicams vienmēr skatīt izmaksu cenu visām izsekotajām finanšu dimensijām. Rēķinā ir iekļauti šādi pirkšanas pasūtījumi:

-   Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 2 un izmaksu cenu USD 10,00 noliktavai GW un partijai AAA.
-   Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 3 un izmaksu cenu USD 12,00 noliktavai GW un partijai AAA.
-   Rēķinā ir iekļauts pirkšanas pasūtījums ar daudzumu 2 un izmaksu cenu USD 15,00 noliktavai GW un partijai BBB.

Kārtējo vidējo izmaksu cena noliktavai GW un partijai AAA ir USD 11,20, bet noliktavai MW un partijai BBB tā ir USD 15,00.




