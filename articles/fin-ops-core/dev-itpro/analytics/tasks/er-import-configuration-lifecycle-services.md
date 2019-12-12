---
title: ER Importēt konfigurāciju no Lifecycle Services
description: Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184834"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>ER Importēt konfigurāciju no Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
