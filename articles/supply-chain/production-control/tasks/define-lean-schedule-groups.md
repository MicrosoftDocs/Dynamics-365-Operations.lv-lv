---
title: Racionālās plānošanas grupu definēšana
description: Racionālās plānošanas grupas tiek definētas, lai grupētu un izšķirtu preces Kanban plānošanā.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0cb17c68abbc4979a65e33c50450be575df3d93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836268"
---
# <a name="define-lean-schedule-groups"></a>Racionālās plānošanas grupu definēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Racionālās plānošanas grupas tiek definētas, lai grupētu un izšķirtu preces Kanban plānošanā. Grupēšanu var veikt kā vispārīgu saistību pēc uzņēmuma vai noteiktai darba šūnai. Katrai grupai ir piešķirts krāsas kods vizuālai norādei Kanban plānošanas saraksta lapā. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="define-lean-scheduling-group"></a>Racionālās plānošanas grupas definēšana
1. Dodieties uz Preču informācijas pārvaldība > Lean manufacturing > Racionālās plānošanas grupas.
2. Noklikšķiniet uz Jauns.
3. Laukā Plānošanas grupa ierakstiet kādu vērtību.
    * Plānošanas grupu var definēt kā globālo grupu vai noteiktai darba šūnai. Šajā vienkāršajā piemērā tiks definēta globāla grupa un darba šūna paliks tukša. Šīs grupas iestatījumi attiecas uz visām darba šūnām, kurām nav noteiktu plānošanas grupu.  
4. Atlasiet krāsu no krāsu atlases.
    * Krāsas tiek lietotas, lai iezīmētu darbus Kanban grafiku saraksta lapā vai Kanban apstrādes ziņojumu dēlī.  
5. Sarakstā atzīmējiet atlasīto rindu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="associate-product"></a>Preces piesaistīšana
1. Noteiktas preces piesaistīšana
    * Ir divi veidi, kā saistīt preces ar racionālās plānošanas grupām kā noteiktu preci (Krājumu saistības tips = Krājums) vai kā daļu no krājumu sadalījuma principa (Krājumu saistības tips = Grupa).    
2. Laukā Krājumu saistības tips atlasiet vienumu Krājums
3. Laukā Krājuma kods ierakstiet kādu vērtību.
4. Laukā Caurlaides koeficients ievadiet skaitli.
    * Noklusējuma caurlaides koeficients ir 1, kas nozīmē to, ka saistītās preces patērē tieši tādu noslodzi, kas norādīta ražošanas plūsmu procesa aktivitātēs. Caurlaides koeficients > 1 norāda lielāku resursu patēriņu, caurlaides koeficients < 1 norāda mazāku resursu patēriņu. Koeficients tiek izmantots izmaksu aprēķinā un Kanban darba patēriņa aprēķinā.  

## <a name="associate-item-allocation-key"></a>Krājumu sadalījuma principa piesaistīšana
1. Krājumu sadalījuma principa piesaistīšana
    * Pievienojiet saistību ar krājumu sadalījuma principu, izmantojot krājumu saistības tipu Grupa.   Ņemiet vērā, ka šim procesam ir nepieciešams datos definēt prognozi krājumu sadalījuma principam.  
2. Laukā Krājumu saistības tips atlasiet vienumu Grupa
3. Laukā Krājumu sadalījuma princips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

