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
ms.openlocfilehash: 5e0e1989bcc4ca02d097f9ebff40f21158f26546
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981360"
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