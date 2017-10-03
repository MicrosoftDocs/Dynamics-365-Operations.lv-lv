--- 
title: "Likmju šablonu iestatīšana"
description: "Šajā procedūrā parādīts, kā iestatīt likmes šablonu."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 263c912594dcf61985094dab30eab8f72cd731e9
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-rate-masters"></a>Likmju šablonu iestatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt likmes šablonu. Loģistikas vadītājs parasti iestata likmes šablonus, atkarībā no ar pārvadātājiem parakstītajiem līgumiem. Šajā scenārijā iestatīsit likmes šablonu gaisa pārvadātājam. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="set-up-rate-master"></a>Likmes šablona iestatīšana
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Likmes šablons.
2. Noklikšķiniet uz Jauns.
3. Laukā Likmes šablons ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Vērtējuma metadatu ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Vērtēšanas metadatu ID noteiks, kādi dati nepieciešami likmes šablonā, jo tas definē metadatus, kas nepieciešami šo likmes šablonu izmantojošajai TMS programmai.  
6. Šim piemēram atlasiet opciju P2P
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Noklikšķiniet uz Saglabāt.

## <a name="set-up-rate-base"></a>Likmes bāzes tipa iestatīšana
1. Noklikšķiniet uz Likmes bāze.
    * Likmes bāze nosaka pārvadātāja kursu, un to var izmantot, lai iestatītu tarifu struktūru un likmes strukturētu atbilstoši pārtraukumpunktiem, kas definēti pārtraukumu šablonā.  
2. Noklikšķiniet uz Jauns.
3. Laukā Likmes bāze ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Pārtraukuma šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Pārtraukuma šabloni tiek izmantoti, lai noteiktu izcenojuma struktūru un tās pārtraukumpunktus. Izcenojuma struktūra izmanto diferencētas cenas, kuru pamatā ir fiziskās dimensijas.  
6. Šim piemēram izmantojiet svaru
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Pārslēdziet sadaļas Detalizēti paplašinājumu.
9. Klikšķiniet Jauns.
10. Laukā Nodošanas pasta indekss no ierakstiet "30301".
11. Laukā Nodošanas pasta indekss uz ierakstiet "30318".
12. Laukā Nodošanas valsts reģions ierakstiet "ASV".
13. Laukā < 1,00 mārc. ierakstiet “100”.
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1 mārciņu.  
14. Laukā <5,00 mārc. ierakstiet "300".
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 5 mārciņām.  
15. Laukā <20,00 mārc. ierakstiet "500".
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 20 mārciņām.  
16. Laukā <100,00 mārc. ierakstiet "1000".
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 100 mārciņām.  
17. Laukā <1000,00 mārc. ierakstiet "3000".
    * Ievietojiet likmi par mārciņu, ja kravas kopējais svars ir mazāks par 1000 mārciņām.  
18. Noklikšķiniet uz Saglabāt.
19. Aizvērt lapu.

## <a name="assign-rate-base"></a>Likmes bāzes piešķiršana
1. Pārslēdziet sadaļas Likmes bāzes piešķires paplašinājumu.
2. Noklikšķiniet uz Jauns.
    * Katrā likmes šablonā var būt vairākas likmes bāzes piešķires. Tas dod iespēju katram pārvadātājam izveidot vairākus dažādus cenu punktus atkarībā no galamērķiem, pakalpojumiem vai atšķirīgām pamatlikmēm. Šajā procedūrā tiks izveidota tikai viena likmes bāzes piešķire.  
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Laukā Likmes bāze noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Pakalpojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā Saņemšanas pasta indekss ierakstiet "98052".
    * Norādiet, no kura pasta koda ir spēkā šī likmes bāzes piešķire.    
10. Laukā Saņemšanas valsts reģions ierakstiet "ASV".
11. Noklikšķiniet uz Saglabāt.


