--- 
title: "Racionālās plānošanas grupu definēšana"
description: "Racionālās plānošanas grupas tiek definētas, lai grupētu un izšķirtu preces Kanban plānošanā."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e07fa270b47be3527c572dc53ca30a7bcde5ba6
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-schedule-groups"></a>Racionālās plānošanas grupu definēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Racionālās plānošanas grupas tiek definētas, lai grupētu un izšķirtu preces Kanban plānošanā. Grupēšanu var veikt kā vispārīgu saistību pēc uzņēmuma vai noteiktai darba šūnai. Katrai grupai ir piešķirts krāsas kods, lai grupu varētu vizuāli atpazīt Kanban plānošanas saraksta lapā. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


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
    * Noklusējuma caurlaides koeficients ir 1, un tas nozīmē, ka saistītajām precēm tiek patērēta tieši tāda noslodze, kāda ir norādīta ražošanas plūsmu procesa aktivitātēs. Caurlaides koeficients > 1 norāda lielāku resursu patēriņu, caurlaides koeficients < 1 norāda mazāku resursu patēriņu. Koeficients tiek izmantots izmaksu aprēķinā un Kanban darba patēriņa aprēķinā.  

## <a name="associate-item-allocation-key"></a>Krājumu sadalījuma principa piesaistīšana
1. Krājumu sadalījuma principa piesaistīšana
    * Pievienojiet saistību ar krājumu sadalījuma principu, izmantojot krājumu saistības tipu Grupa.   Ņemiet vērā, ka, lai izpildītu šo procesu, datos ir jābūt definētai krājumu sadalījuma principa prognozei.  
2. Laukā Krājumu saistības tips atlasiet vienumu Grupa
3. Laukā Krājumu sadalījuma princips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.


