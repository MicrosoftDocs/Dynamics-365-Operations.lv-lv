---
title: Kanban aizstāšanas kārtulas izveide
description: Šī procedūra aizstāj esošo kanban nosacījumu ar jaunu Kanban nosacījumu noteiktā datumā.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2db44c1b43a6dc5e0ab37a7756c4eecaab468e15
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570061"
---
# <a name="create-a-replacement-kanban-rule"></a>Kanban aizstāšanas kārtulas izveide

[!include [banner](../../includes/banner.md)]

Šī procedūra aizstāj esošo kanban nosacījumu ar jaunu Kanban nosacījumu noteiktā datumā. Tas ir noderīgi, kad ir nepieciešams saskaņot un plānot izmaiņas ražošanas plūsmā vai papildināšanas kārtulās. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei. Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie sagatavo ražošanas procesu izmanītai ražošanas plūsmai vai jauniem papildināšanas noteikumiem. Šis uzdevums aizstāj kanban nosacījumu 000022 ar jaunu nosacījumu, un palielina maksimālo daudzumu jaunajam nosacījumam no 48 līdz 100.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]