---
title: Procesa darba Kanban kārtulu maiņa
description: Šajā procedūrā aprakstīta konkrētajam Kanban nosacījumam izmantoto Kanban kārtulu maiņa.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bdbbbf8a8b3d1596c251224cba996c0631050c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829310"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Procesa darba Kanban kārtulu maiņa

[!include [banner](../../includes/banner.md)]

Šajā procedūrā aprakstīts konkrētajam Kanban izmantoto Kanban nosacījum maiņa. Tas ir noderīgi noslodzes resursu līmeņu piešķiršanā vai sadalījumā. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta plānotājam, kas strādā lean manufacturing uzņēmumā un ir atbildīgs par vērtību plūsmu.


## <a name="copy-kanban-rule"></a>Kanban nosacījumu kopēšana
1. Dodieties uz Kanban nosacījumi.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Vienumam L0001 atlasiet Notikumu Kanban nosacījumi 000022.  
3. Noklikšķiniet uz Dublējiet Kanban nosacījumus.
4. Noklikšķiniet uz OK.

## <a name="change-kanban-rule"></a>Kanban nosacījumu mainīšana
1. Aizvērt lapu.
2. Dodieties uz cilni Kanban darbu plānošana.
3. Sarakstā atzīmējiet atlasīto rindu.
    * Izvēlieties rindu ar Kanban 000177.  
4. Noklikšķiniet uz Izmantot alternatīvus Kanban nosacījumus.
5. Noklikšķiniet uz Tālāk.
6. Laukā Kanban nosacījumi ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Kanban nosacījumus, kas tika izveidoti iepriekš. Šie ir kanban nosacījumi ar lielāko numuru.  
7. Noklikšķiniet uz Pabeigt.
    * Tagad Kanban darbs izmanto citus Kanban nosacījumus. Tas var noderēt darba šūnu noslodzes līmeņu piešķiršanā.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]