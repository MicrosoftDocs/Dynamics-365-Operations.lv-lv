--- 
title: "Materiālu pārsūtīšana, izmantojot Kanban darbus (tikai 2016. gada februāris)"
description: "Šajā procedūrā parādīts, kā izpildīt Kanban atsaukšanas darbu, lai pārsūtītu materiālus."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Materiālu pārsūtīšana, izmantojot Kanban darbus (tikai 2016. gada februāris)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izpildīt Kanban atsaukšanas darbu, lai pārsūtītu materiālus. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta noliktavas darbiniekam.


## <a name="display-transfer-jobs"></a>Pārsūtīšanas darbu attēlošana
1. Pārejiet uz sadaļu Ražošanas kontrole > Kanban >Pārsūtīšanas darbu Kanban panelis.
2. Izvērsiet vai sakļaujiet sadaļu Filtri.
    * Sadaļā Filtri varat norādīt, kurus darbus vēlaties apskatīt, filtrējot pēc parametriem Ražošanas plūsma, Aktivitātes nosaukums, No noliktavas un atrašanās vietas un Uz noliktavu un atrašanās vietu.  
3. Laukā No noliktavas ierakstiet "11".
4. Laukā Uz atrašanās vietu ierakstiet "12".

## <a name="start-a-transfer-job"></a>Sākt pārvietošanas darbu
1. Sarakstā noņemiet atlasi no atlasītās rindas, ja tāda ir.
2. Sarakstā atlasiet 4. rindu.
    * Atlasiet pirmo darbu ar statusu Nav plānots. Pārliecinieties, ka šis ir vienīgais atlasītais darbs.  
3. Noklikšķiniet uz Sākt.
    * Ņemiet vērā, ka ikona norāda, ka darbs ir sākts.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Atlasiet otro pārsūtīšanas darbu un mainiet daudzumu
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Varat atlasīt vairākus darbus, bet tagad atlasiet 5. rindu.  
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Pārliecinieties, ka iepriekšējā soļa darbs ir vienīgais atlasītais. Atceliet visu citu darbu atlasi.  
3. Ievērojiet vērtību laukā Darba apjoms vēlākai atsaucei
4. Vienumam Darba apjoms iestatiet vērtību "30".
    * Ņemiet vērā brīdinājumu. Jums nav atļauts pārsūtīt 30. Saskaņā ar Kanban nosacījuma iestatījumu varat pārsūtīt tikai sākotnējo daudzumu.  
5. Lietojiet vērtību, ko iepriekš ievērojāt laukā Darba apjoms
    * Iestatiet darba daudzuma vērtību uz iepriekšējo.  

## <a name="start-the-second-transfer-job"></a>Sāciet otro pārsūtīšanas darbu
1. Noklikšķiniet uz Sākt.
    * Šādi tiks uzsākta 5. rindas darba pārsūtīšana.  

## <a name="complete-both-transfer-jobs"></a>Pabeidziet abus pārvietošanas darbus
1. Sarakstā atlasiet 4. rindu.
    * Tagad ir atlasīti divi pārsūtīšanas darbi — 4. rindā un 5. rindā.  
2. Noklikšķiniet uz Pabeigt.
    * Šī darbība pabeigs abu darbu pārsūtīšanu.  


