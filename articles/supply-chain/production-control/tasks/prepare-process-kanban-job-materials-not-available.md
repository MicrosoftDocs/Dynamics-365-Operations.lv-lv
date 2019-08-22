---
title: Procesa sagatavošana Kanban darbam, kad materiāli nav pieejami darba šūnai
description: Šajā procedūrā parādīts, kā sagatavot procesa Kanban darbu, kad darba šūnai nav pieejami daži no nepieciešamajiem materiāliem un tādēļ ir nepieciešams atlasīt materiālus no noliktavas.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bba9e5cb7dfddd2a80a37e7a57fdf94a91341e8f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843629"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Procesa sagatavošana Kanban darbam, kad materiāli nav pieejami darba šūnai

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

