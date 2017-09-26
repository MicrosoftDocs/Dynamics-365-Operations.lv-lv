--- 
title: "Aizstāšanas Kanban kārtulas izveide"
description: "Šī procedūra aizstāj esošo kanban nosacījumu ar jaunu kanban nosacījumu noteiktā datumā."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 58b12edbbdcf77429c32193dfd850bc53f4c26a8
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-replacement-kanban-rule"></a>Aizstāšanas Kanban kārtulas izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra aizstāj esošo kanban nosacījumu ar jaunu kanban nosacījumu noteiktā datumā. Tas ir noderīgi, kad ir nepieciešams saskaņot un plānot izmaiņas ražošanas plūsmā vai papildināšanas kārtulās. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie sagatavo ražošanas procesu izmanītai ražošanas plūsmai vai jauniem papildināšanas noteikumiem. Šis uzdevums aizstāj kanban nosacījumu 000022 ar jaunu nosacījumu, un palielina maksimālo daudzumu jaunajam nosacījumam no 48 līdz 100.


## <a name="select-a-kanban-rule-to-replace"></a>Atlasiet aizstājamo kanban nosacījumu
1. Dodieties uz Kanban nosacījumi.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet kanban nosacījumu 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Aizstāšanas Kanban kārtulas izveide
1. Noklikšķiniet uz Aizstāt kanban nosacījumu.
2. Laukā Spēkā stāšanās datums ievadiet datumu un laiku.
    * Izvēlieties datumu nākotnē, piemēram, vienu nedēļu uz priekšu. Šis ir datums un laiks, kad jaunais kanban nosacījums kļūst aktīvs un aizstāj veco kanban nosacījumu.  
    * Ja kanban nosacījums maina ražošanas plūsmas ceļu, var atlasīt citu darbību.  Šajā procedūrā mēs atstāsim aktivitāti neskartu.  
3. Noklikšķiniet uz OK.
    * Ņemiet vērā, ka tiek izveidots jauns kanban nosacījums, lai aizstātu kanban nosacījumu 000022.  
    * Spēkā stāšanās datums tiek iestatīts saskaņā ar izvēlēto datumu, aizstājot kanban nosacījumu.  
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet aizstāto kanban nosacījumu 000022.  
    * Ņemiet vērā, ka aizstājamajam kanban nosacījumam ir tāds pats datums kā beigu datums, jo tas ir nosacījuma derīguma termiņš.  
5. Sarakstā atlasiet 1. rindu.
    * Atlasiet jaunu kanban nosacījumu saraksta augšgalā. Šis ir kanban nosacījums ar lielāko kanban nosacījuma numuru.  
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Noklikšķiniet uz kanban nosacījuma numura, lai atvērtu kanban nosacījumu.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Modificējiet maksimālo daudzumu kanban nosacījuma nomaiņai
1. Iestatiet maksimālo daudzumu uz "100".
    * Izvērsiet daudzumu kopsavilkuma cilni, lai redzētu lauku Maksimālais daudzums. Nomainot maksimālo daudzumu uz 100, ļaus apstrādāt līdz pat 100 kanban.    Šā ir pēdējā darbība šajā uzdevumā.  


