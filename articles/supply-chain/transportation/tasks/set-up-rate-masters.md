---
title: Likmju šablonu iestatīšana
description: Šajā procedūrā parādīts, kā iestatīt likmes šablonu.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433240"
---
# <a name="set-up-rate-masters"></a>Likmju šablonu iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt likmes šablonu. Loģistikas vadītājs parasti iestata likmes šablonus, atkarībā no ar pārvadātājiem parakstītajiem līgumiem. Šajā scenārijā iestatīsit likmes šablonu gaisa pārvadātājam. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.

## <a name="set-up-break-master"></a>Pārtraukuma šablona iestatīšana

1. Dodieties uz **Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Pārtraukuma šablons**. Pārtraukuma šabloni tiek izmantoti, lai noteiktu izcenojuma struktūru un tās pārtraukumpunktus. Izcenojuma struktūra izmanto diferencētas cenas, kuru pamatā ir fiziskās dimensijas.  
1. Atlasiet **Jauns**.
1. Laukā **Pārtraukuma šablons** ievadiet kādu vērtību.
1. Laukā **Nosaukums** ievadiet vērtību.
1. Laukā **Datu tips** atlasiet datu tipu.
1. Laukā **Salīdzinājums** ievadiet nepieciešamo salīdzinājuma veidu (izmantojot operatorus).
1. Laukā **Pārtraukuma vienība** ievadiet pārtraukuma vienības vērtības.
1. Sadaļā **Detalizēti** izveidojiet tik daudz pārtraukumu, cik nepieciešams cenu struktūrai.
1. Atlasiet **Saglabāt**.

## <a name="set-up-rate-master"></a>Likmes šablona iestatīšana

1. Dodieties uz **Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Likmes šablons**.
1. Atlasiet **Jauns**.
1. Laukā **Likmes šablons** ierakstiet vērtību.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
1. Laukā **Vērtējuma metadatu ID** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu. Vērtēšanas metadatu ID noteiks, kādi dati nepieciešami likmes šablonā, jo tas definē metadatus, kas nepieciešami šo likmes šablonu izmantojošajai pārvadājošajai pārvaldības programmai.  
1. Šim piemēram atlasiet opciju P2P. Tas jau ir definēts demonstrācijas datos.
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Atlasiet **Saglabāt**.

## <a name="set-up-rate-base"></a>Likmes bāzes tipa iestatīšana

1. Atlasiet **Likmes bāze**.
    * Likmes bāze nosaka pārvadātāja kursu, un to var izmantot, lai iestatītu tarifu struktūru un likmes strukturētu atbilstoši pārtraukumpunktiem, kas definēti pārtraukumu šablonā.  
2. Atlasiet **Jauns**.
3. Laukā **Likmes bāze** ierakstiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Pārtraukuma šablons** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
    * Pārtraukuma šabloni tiek izmantoti, lai noteiktu izcenojuma struktūru un tās pārtraukumpunktus. Izcenojuma struktūra izmanto diferencētas cenas, kuru pamatā ir fiziskās dimensijas.  
6. Šim piemēram izmantojiet svaru. Tas jau ir definēts demonstrācijas datos.
7. Sarakstā atlasiet saiti iezīmētajā rindā.
8. Izvērsiet sadaļu **Detalizēti**.
9. Atlasiet **Jauns**.
10. Laukā **Nodošanas pasta indekss no ierakstiet** ievadiet "30301".
11. Laukā **Nodošanas pasta indekss uz** ierakstiet "30318".
12. Laukā **Nodošanas valsts reģions** ierakstiet "ASV".
13. Laukā **<1,00 mārc.** ierakstiet “100”.
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1 mārciņu.  
14. Laukā **<5,00 mārc.** ierakstiet “300”.
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 5 mārciņām.  
15. Laukā **<20,00 mārc.** ierakstiet “500”.
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 20 mārciņām.  
16. Laukā **<100,00 mārc.** ierakstiet “1000”.
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 100 mārciņām.  
17. Laukā **<1000,00 mārc.** ierakstiet “3000”.
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1000 mārciņām.  
18. Atlasiet **Saglabāt**.
19. Aizvērt lapu.

## <a name="assign-rate-base"></a>Likmes bāzes piešķiršana

1. Izvērsiet sadaļu **Likmes bāzes piešķires**.
2. Atlasiet **Jauns**.
    * Katrā likmes šablonā var būt vairākas likmes bāzes piešķires. Tas dod iespēju katram pārvadātājam izveidot vairākus dažādus cenu punktus atkarībā no galamērķiem, pakalpojumiem vai atšķirīgām pamatlikmēm. Šajā procedūrā tiks izveidota tikai viena likmes bāzes piešķire.  
3. Laukā **Nosaukums** ierakstiet kādu vērtību.
4. Laukā **Likmes bāze** atlasiet nolaižamo saraksta pogu, lai atvērtu uzmeklēšanu.
5. Sarakstā atlasiet saiti iezīmētajā rindā.
6. Laukā **Pakalpojums** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā atlasiet saiti iezīmētajā rindā.
9. Laukā **Saņemšanas pasta indekss** ierakstiet "98052".
    * Norādiet, no kura pasta koda ir spēkā šī likmes bāzes piešķire.
10. Laukā **Saņemšanas valsts reģions** ierakstiet "ASV".
11. Atlasiet **Saglabāt**.
