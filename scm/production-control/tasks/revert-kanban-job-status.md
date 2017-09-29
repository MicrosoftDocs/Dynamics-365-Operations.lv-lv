--- 
title: Atjaunot Kanban darba statusu
description: "Šajā procedūrā aprakstīts nepareiza Kanban darba statusa atgriešanas process."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 00b6ae872e60a322c994420ab69236abef7fb312
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="revert-kanban-job-status"></a>Atjaunot Kanban darba statusu

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

