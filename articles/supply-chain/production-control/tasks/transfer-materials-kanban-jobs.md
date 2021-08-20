---
title: Materiālu pārsūtīšana, izmantojot Kanban darbus
description: Šajā procedūrā parādīts, kā izpildīt Kanban atsaukšanas darbu, lai pārsūtītu materiālus.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d4e6d8bbdb50394ef575e1088dd238eb39170124854edb878f6dccb6c9e07d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771351"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Materiālu pārsūtīšana, izmantojot Kanban darbus

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]