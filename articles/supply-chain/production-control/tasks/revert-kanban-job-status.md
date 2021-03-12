---
title: Atjaunot Kanban darba statusu
description: Šajā procedūrā aprakstīts nepareiza Kanban darba statusa atgriešanas process.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bc147ec517b8141b4764f67d21b4c4a2e4d6e6e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981160"
---
# <a name="revert-kanban-job-status"></a>Atjaunot Kanban darba statusu

[!include [banner](../../includes/banner.md)]

Šajā procedūrā aprakstīts nepareiza Kanban darba statusa atgriešanas process. Tas ir noderīgi, ja datoru ievades operators kļūdas dēļ atjaunina nepareizu darbu vai iestata nepareizu statusu. Šajā procedūrā Kanban darbs kļūdas pēc tika reģistrēts kā sagatavots, un tā statuss tiek atgriezts. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta veikala vadītājam vai datu ievades operatoram, kurš strādā Lean manufacturing uzņēmumā.


## <a name="open-process-board-for-the-work-cell"></a>Apstrādes ziņojumu dēļa atvēršana darba šūnai
1. Dodieties uz procesa darbu Kanban paneli.
2. Laukā Darba šūna ievadiet vai atlasiet vērtību.
    * Atlasiet darba šūnu 1260.  

## <a name="prepare-kanban-job"></a>Kanban darba sagatavošana
1. Noklikšķiniet uz Sagatavot.
    * Ja vienums Sagatavot ir pelēkots un tādēļ nav aktīvs, pārliecinieties, vai atlasītā Kanban darba statuss ir Plānots, par ko norāda tukša Kanban ikona. Ja sagatavošana neizdevās, pārliecinieties, vai ir pieejami visi izdošanas saraksta materiāli.  
2. Sarakstā atlasiet sagatavoto darbu.
    * Atlasiet pirmo darbu, ko tikko sagatavojāt.  
    * Ņemiet vērā! Darba statuss ir Sagatavots, par ko norāda trīsstūris Kanban ikonas iekšpusē.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Sagatavota Kanban darba statusa atgriešana
1. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet pirmo darbu, kas tika sagatavots.  
2. Darbību rūtī noklikšķiniet uz Ražošana.
3. Noklikšķiniet uz Atgriezt statusu.
    * Var izmantot alternatīvu Kanban nosacījumu, ja ir spēkā tālāk minētie nosacījumi. - Abiem nosacījumiem ir vienāda papildināšanas stratēģija.  - Abiem nosacījumiem ir vienāda ražošanas plūsmas versija.  - Abiem nosacījumiem tiek piegādāta vienāda preces.  - Abiem nosacījumiem jābūt vienādām visām pakārtotajām darbībām, kas ir konfigurētas Kanban nosacījumu pēdējai aktivitātei.  - Abiem nosacījumiem jābūt konfigurētām vienādām piegādātā krājuma dimensijām.  - Materiālu apstrādes vienības statusam jābūt Nav piešķirts.  - Notikuma Kanban darbu konfigurācijai jābūt vienādai.  
    * Nodrošiniet, ka jaunais statuss ir Plānots.  
4. Noklikšķiniet uz OK.
5. Sarakstā noņemiet atzīmi no atlasītās rindas.
    * Atlasiet vienu darbu.  
    * Ņemiet vērā! Kanban darba statuss tiek atgriezts uz Plānots, par ko norāda tukša Kanban ikona.  

