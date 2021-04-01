---
title: Procesa darba Kanban kārtulu maiņa
description: Šajā procedūrā aprakstīts konkrētajam Kanban izmantoto Kanban nosacījum maiņa.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba77197f51b871f452c2aa94320aa2a68cf314df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255377"
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