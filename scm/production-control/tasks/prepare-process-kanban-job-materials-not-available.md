--- 
title: "Procesa sagatavošana Kanban darbam, kad materiāli nav pieejami darba šūnai"
description: "Šajā procedūrā parādīts, kā sagatavot procesa Kanban darbu, kad darba šūnai nav pieejami daži no nepieciešamajiem materiāliem un tādēļ ir nepieciešams atlasīt materiālus no noliktavas."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4899c1d0baebb451e665853767e64f660ca25ca6
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Procesa sagatavošana Kanban darbam, kad materiāli nav pieejami darba šūnai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā sagatavot procesa Kanban darbu, kad darba šūnai nav pieejami daži no nepieciešamajiem materiāliem un tādēļ ir nepieciešams atlasīt materiālus no noliktavas. Šīs procedūras izveides priekšnosacījums ir procedūra "Sagatavot procesa Kanban darbu, kad materiāli ir pieejami". Šī procedūra ir paredzēta mašīnas operatoram. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.

1. Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban panelis procesa darbiem.
2. Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet darba šūnu 1250.  
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet Kanban 000356.  
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Sarakstā noņemiet atzīmi no 4. rindas izvēles rūtiņas. vai atlasiet 4. rindu, ja neesat izpildījis uzdevumu "Procesa Kanban darba sagatavošana, kad materiāli ir pieejami."  
6. Pārslēdziet sadaļas Izdošanas saraksts paplašinājumu.
    * Piegādes statusā attēlotā ikona Nav ierakstu norāda, ka darba šūnā krājumam P0002 trūkst 48 vienumi.  

## <a name="transfer-materials-to-work-cell"></a>Materiālu pārsūtīšana uz darba šūnu
1. Pārslēdziet sadaļas Pārvietošanas darbi paplašinājumu.
2. Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P0002.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Noklikšķiniet uz Sākt.
    * Tiek veikta pārsūtīšana.  
5. Noklikšķiniet uz Pabeigt.
    * Krājums P0002 tagad ir pieejams Kanban darba izdošanas sarakstā. Tas nozīmē, ka varat sagatavot Kanban ar visiem nepieciešamajiem materiāliem.  
6. Noklikšķiniet uz Sagatavot.
    * Ņemiet vērā, ka ikona Darba statusa laukā norāda, ka darbs ir gatavs.  

