---
title: Kanban darbu grafika izveide
description: Šajā procedūrā apskatīts Kanban darbu plānošanas process noteiktai darba šūnai.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a56bca460af229b53d41959d48562ef425c0bf7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843485"
---
# <a name="schedule-kanban-jobs"></a>Kanban darbu grafika izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā apskatīts Kanban darbu plānošanas process noteiktai darba šūnai. Šīs procedūras izveides priekšnosacījums ir procedūra "Sagatavot procesa Kanban darbu, kad materiāli nav pieejami". Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šis uzdevums ir paredzēts ražotnes vadītājam un ražošanas plānotājam, kas strādā ar Kanban.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Kanban darbu atlase darba šūnai
1. Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban darbu plānošana.
2. Izvērsiet sadaļas Perioda noslodze papildinformāciju
    * Izvērsiet Kanban papildinformāciju.  
3. Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet darba šūnu 1250. Šādi atfiltrēsiet skatu, lai parādītu tikai darbus šūnai 1250.  
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz Atlasīt.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Kanban darbs ieplānošana pirmajā pieejamā periodā
1. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet pirmo rindu sarakstā, kuras statuss ir Nav plānots. Punktotā ikona laukā Darba statuss norāda, ka statuss ir Nav plānots.  
2. Noklikšķiniet uz Grafiks.
    * Šādi Kanban darbs tiks ieplānots pirmajā pieejamā periodā.  
    * Ņemiet vērā, ka Kanban darbs tiek pārvietots uz saraksta beigām, jo tas ir pievienots periodam, kas sākas šodien.  
    * Ja periods, kas sākas šodien, ir pilnībā rezervēts, darbs tiks pārvietots uz pirmo pieejamo periodu.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Divu Kanban darbu plānošana noteiktai dienai
1. Sarakstā atlasiet 1. rindu.
    * Vajadzētu būt redzamam, ka pirmās rindas vērtība laukā Darba statuss ir Nav plānots.  
2. Sarakstā atlasiet 2. rindu.
    * Vajadzētu būt redzamam, ka otrās rindas vērtība laukā Darba statuss ir Nav plānots. Tagad esat atlasījis pirmos divus darbus.  
3. Noklikšķiniet uz Grafiks no datuma, lai atvērtu nolaižamo dialoglodziņu.
4. Atzīmējiet rūtiņu Ignorēt noslodzes nepietiekamības sekas vai noņemiet atzīmi.
    * Šī opcija ļauj ignorēt noklusējuma noslodzes nepietiekamības sekas.  
5. Laukā Noslodzes nepietiekamības sekas atlasiet Pievienot pieprasītajam periodam.
    * Šī opcija nodrošina, ka darbs tiek pievienots pieprasītajā periodā neatkarīgi no tā, vai darba šūna ir pārslogota.  
6. Noklikšķiniet uz Grafiks.
    * Ņemiet vērā, ka abi darbi tiek pievienoti izvēlētajam periodam.  
    * Sadaļā Perioda noslodze varat redzēt katra perioda slodzi. Laukā Patēriņš parādīts šī perioda plānotais patēriņš. Ja plānotais patēriņš ir lielāks par šajā periodā pieejamo noslodzi, tiks atlasīts pārslodzes patēriņš.  

