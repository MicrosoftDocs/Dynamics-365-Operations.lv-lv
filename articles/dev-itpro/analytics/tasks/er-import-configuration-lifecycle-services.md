--- 
title: "Importēt konfigurāciju no Lifecycle Services elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a>Importēt konfigurāciju no Lifecycle Services elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS).

Šajā piemērā jūs atlasīsiet vēlamo ER konfigurācijas versiju un importēsiet to parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas visos uzņēmumos. Lai izpildītu šīs darbības, jums vispirms ir jāizpilda procedūras “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services” darbības. Lai izpildītu šīs darbības, ir nepieciešama arī piekļuve pakalpojumiem LCS.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Konfigurācijas.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Dzēst koplietotu datu modeļa konfigurācijas versiju
1. Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.
    * Parauga datu modeļa konfigurācijas pirmā versija tiek izveidota un pakalpojumos LCS tiek publicēta, izpildot procedūru “Augšupielādēt ER konfigurāciju pakalpojumos Lifecycle Services”. Šajā procedūrā jūs dzēsīsiet šo ER konfigurācijas versiju. Šī parauga datu modeļa konfigurācijas versija vēlāk tiks importēta no LCS.  
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”. Šis statuss norāda, ka konfigurācija ir publicēta pakalpojumos LCS.  
3. Noklikšķiniet uz Mainīt statusu.
4. Noklikšķiniet uz Pārtraukt.
    * Atlasītās versijas statusu no “Koplietots” mainiet uz “Pārtraukts”, lai tā kļūtu pieejama dzēšanai.  
5. Noklikšķiniet uz OK.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Pārtraukts”.  
7. Noklikšķiniet uz Dzēst.
8. Noklikšķiniet uz Jā.
    * Ņemiet vērā, ka atlasītajai datu modeļa konfigurācijai ir pieejama tikai melnraksta 2. versija.  
9. Aizvērt lapu.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Importēt koplietotu datu modeļa konfigurācijas versiju no LCS
1. Sarakstā atzīmējiet atlasīto rindu.
    * Atveriet sarakstu ar repozitorijiem, kas paredzēti “Litware, Inc.” konfigurācijas nodrošinātājam.  
2. Noklikšķiniet uz Repozitoriji.
3. Noklikšķiniet uz Atvērt.
    * Atlasiet LCS repozitoriju un atveriet to.  
4. Sarakstā atzīmējiet atlasīto rindu.
    * Versiju sarakstā atlasiet konfigurācijas “Parauga modeļa konfigurācija” pirmo versiju.  
5. Noklikšķiniet uz Importēt.
6. Noklikšķiniet uz Jā.
    * Apstipriniet atlasītās versijas importēšanu no LCS.  
    * Ņemiet vērā, ka informatīvais ziņojums (virs formas) apstiprina, ka atlasītās versijas importēšana ir sekmīgi pabeigta.  
7. Aizvērt lapu.
8. Aizvērt lapu.
9. Noklikšķiniet uz Konfigurācijas.
10. Koka struktūrā atlasiet “Parauga modeļa konfigurācija”.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet šīs konfigurācijas versiju, kuras statuss ir “Koplietots”.  
    * Ņemiet vērā, ka tagad atlasītajai datu modeļa konfigurācijai ir pieejama arī koplietotā 1. versija.  


