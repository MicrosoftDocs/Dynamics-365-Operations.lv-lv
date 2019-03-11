---
title: Fiksēta daudzuma Kanban kārtulu izveide ražošanai
description: Šī procedūra fokusējas iestatījumiem, kas nepieciešami, lai izveidotu fiksētus ražošanas Kanban nosacījumus transformēšanas aktivitāšu palaišanai darba šūnā racionālā vidē.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0f58d1e265fb001474eb572b9bc325cf08790c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "338686"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Fiksēta daudzuma Kanban kārtulu izveide ražošanai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra fokusējas iestatījumiem, kas nepieciešami, lai izveidotu fiksētus ražošanas Kanban nosacījumus transformēšanas aktivitāšu palaišanai darba šūnā racionālā vidē. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.


## <a name="create-new-kanban-rule"></a>Jaunu Kanban nosacījumu izveide
1. Dodieties uz Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
    * Ievērojiet, ka noklusējuma Tips ir Ražošana un Papildināšanas stratēģija ir Fiksēts. Šie parametri nav jāmaina.  
3. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Tā ir aktivitāte, kas tiks veikta Kanban, kas izveidoti, pamatojoties uz šiem Kanban nosacījumiem.  Atlasiet "SpeakerTestAndPackaging".  
4. Izvērsiet sadaļu Detalizēti.
5. Laukā Prece ievadiet vai atlasiet kādu vērtību.
    * Atlasiet L0050.  
6. Laukā Mērvienība ievadiet vai atlasiet kādu vērtību.
    * Atlasiet minūtes.  
7. Laukā Izpildes laiks ievadiet kādu skaitli.
    * Ievadiet 5.  

## <a name="set-quantities"></a>Daudzumu iestatīšana
1. Izvērsiet sadaļu Daudzumi.
2. Vienumam Noklusējuma daudzums iestatiet vērtību "10".
    * Tas ir daudzums, kas tiks pārsūtīts katram Kanban.  
3. Atzīmējiet izvēles rūtiņu Preču daudzuma novirze.
    * Ar šo, atlasītos Kanban var papildināt ar novirzi no noklusējuma daudzuma.  Lai atļautu papildināt Kanban ar daudzumu no 8 līdz 12, iestatiet abas novirzes uz 2.  
4. Iestatiet Novirze zem uz "2".
    * Tas ļaus papildināt līdz pat 10 - 2 = 8  
5. Iestatiet Novirze virs uz "2".
    * Tas ļaus papildināt līdz pat 10 + 2 = 12  
6. Laukā Fiksēts Kanban daudzums ierakstiet kādu skaitli.
    * Tas ir Kanban daudzums, kuram jābūt aktīvam. Šajā gadījumā, katrs no 5 Kanban apstrādā 10.  
7. Laukā Minimālā brīdinājuma robeža ievadiet "2".
    * Izmantojiet, lai sekotu līdzi pilnu Kanban minimālajam skaitam, kuram jābūt galamērķī. Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.  
8. Laukā Maksimālā brīdinājuma robeža ievadiet "4".
    * Izmantojiet, lai sekotu līdzi pilnu Kanban maksimālajam skaitam, kuram jābūt galamērķī. Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.  
9. Laukā Automātiskais plānošanas daudzums ievadiet "1".
    * Iestatot šo uz 1 nozīmē, ka katrs Kanban tiks automātiski plānots.   Ievadot 3, Kanban netiks plānoti, kamēr plānošanai nebūs gatavi 3 tukši Kanban. Tas ir noderīgi darbu grupēšanai, izvairoties no pārāk daudziem iestatījumiem.  

## <a name="create-kanbans"></a>Vairāku Kanban izveide
1. Izvērsiet sadaļu Vairāki Kanban.
2. Noklikšķiniet uz Saglabāt.
    * Lai Kanban varētu izveidot, Kanban nosacījumi ir jāsaglabā.  
3. Noklikšķiniet uz Pievienot.
    * Ņemiet vērā: tā kā nav neviena aktīva Kanban, ieteiktā opcijas "Jaunu Kanban skaits" vērtība ir 5. Tas ir vienāds ar vērtību "Fiksēts Kanban daudzums".  
4. Noklikšķiniet uz Izveidot.
    * Šādi tiks izveidoti 5 Kanban.  
    * Ņemiet vērā, ka šim ražošanas Kanban nosacījumam tika izveidoti 5 Kanban pa 10 katrs. Šā ir pēdējā darbība šajā procedūrā.  

