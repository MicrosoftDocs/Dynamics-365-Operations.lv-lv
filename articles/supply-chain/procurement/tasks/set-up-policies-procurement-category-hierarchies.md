--- 
title: "Ierobežojumu iestatīšana sagādes kategoriju hierarhijai"
description: "Izmantojiet šo procedūru, lai iestatītu nosacījumus preču pasūtīšanai kategorijā."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Ierobežojumu iestatīšana sagādes kategoriju hierarhijai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai iestatītu nosacījumus preču pasūtīšanai kategorijā. Kārtulas ir definētas noteiktai pirkšanas politikai. Kategorijas piekļuves kārtulas kontrolē to, kurām sagādes kategorijām darbinieki var piekļūt, kad viņi veido pieprasījumu. Kad tiek veidots pieprasījums, piemērojamo pirkšanas politiku un kategoriju piekļuves kārtulu nosaka juridiskā persona un darbības struktūrvienība, kurai šis darbinieks pieder. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Šo uzdevumu parasti veic pirkšanas vadītājs.


## <a name="find-the-procurement-policy"></a>Atrast sagādes politiku
1. Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas.
2. Noklikšķiniet uz saites uz Sagādes politika USMF politikas.
    * Šis ir politika, kurai pievienojat kārtulu. Tai ir jābūt aktīvai politikai.  

## <a name="create-a-category-access-rule"></a>Kategorijas piekļuves kārtulas izveidošana
1. Atlasiet vienumu Kategorijas piekļuves politikas kārtula.
    * Ja poga Izveidot politikas kārtulu ir pelēkota, tas nozīmē, ka kategorijas piekļuvei jau ir aktīva politikas kārtula. Pārbaudiet laukus Spēkā stāšanās datums un Beigu datums, lai noteiktu, kura tā ir, un pēc tam atlasiet to un noklikšķiniet uz Noņemt politikas kārtulu. Ja poga Izveidot politikas kārtulu ir pieejama, jums nav jādara nekas.  
2. Noklikšķiniet uz Izveidot politikas kārtulu.
3. Laukā Spēkā stāšanās datums ievadiet datumu un laiku.
    * Šis laiks nedrīkst pārklāties ar citu kārtulu, kas jau ir aktīva.  
    * Atlasiet kategoriju, uz kuru šī kārtula attieksies. Ievērojiet, kāda tai ir kategorija — tā jums vēlāk būs nepieciešama. Kad atlasāt kategoriju, atlasīto kategoriju sarakstam tiek pievienota arī tās pamatkategorija vai pamatkategorijas.  
    * Ja vēlaties, lai kārtula attiecas arī uz visām atlasītās kategorijas apakškategorijām, atzīmējiet izvēles rūtiņu Iekļaut apakškategorijas.  
4. Noklikšķiniet uz Pievienot.
    * Ja opciju Iekļaut vecākelementa kārtulu ir iestatāt uz Jā, tad politikas kārtula, ko definējat vecākelementa kategorijai, tiek piešķirta arī tās bērnelementa kategorijām, ja šīm bērnelementa kategorijām nav definēta neviena politikas kārtula.  
5. Noklikšķiniet uz OK.

## <a name="create-a-category-policy-rule"></a>Kategorijas politikas kārtulas izveidošana
1. Atlasīt kategorijas politikas kārtulu
    * Ja poga Izveidot politikas kārtulu ir pelēkota, atlasiet aktīvo politikas kārtulu un pēc tam noklikšķiniet uz Noņemt politikas kārtulu.  
2. Noklikšķiniet uz Izveidot politikas kārtulu.
3. Laukā Spēkā stāšanās datums ievadiet datumu un laiku.
4. Noklikšķiniet uz Pievienot.
5. Atlasiet to pašu kategoriju, ko lietojāt iestatījumam Kategorijas piekļuves kārtula.
6. Laukā Kreditora atlase atlasiet kādu opciju.
    * Atlasiet kārtulu, lai kontrolētu, kāda veida kreditorus var atlasīt kategorijai, kad tiek veidoti pieprasījumi.  
7. Noklikšķiniet uz Aizvērt.
    * Jūsu definētās politikas kārtulas bija paredzētas pieprasījumiem ar tipu Patēriņš. Ja vēlaties definēt politikas pieprasījumiem ar tipu Papildināšana, jums būtu jāizveido kārtula politikas kārtulas tipam ar nosaukumu “Papildināšanas kategorijas piekļuves politikas kārtula”.  


