---
title: Ierobežojumu iestatīšana sagādes kategoriju hierarhijai
description: Izmantojiet šo procedūru, lai iestatītu nosacījumus preču pasūtīšanai kategorijā.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d113181b5c78c0f35292b5f14cedd12bacdc7364
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207535"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Ierobežojumu iestatīšana sagādes kategoriju hierarhijai

[!include [banner](../../includes/banner.md)]

Izmantojiet šo procedūru, lai iestatītu nosacījumus preču pasūtīšanai kategorijā. Kārtulas ir definētas noteiktai pirkšanas politikai. Kategorijas piekļuves kārtulas kontrolē to, kurām sagādes kategorijām darbinieki var piekļūt, kad viņi veido pieprasījumu. Kad tiek veidots pieprasījums, piemērojamo pirkšanas politiku un kategoriju piekļuves kārtulu nosaka juridiskā persona un darbības struktūrvienība, kurai šis darbinieks pieder. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Šo uzdevumu parasti veic pirkšanas vadītājs.


## <a name="find-the-procurement-policy"></a>Atrast sagādes politiku
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas**.
2. Noklikšķiniet uz Sagādes politika USMF politika. Šis ir politika, kurai pievienojat kārtulu. Tai ir jābūt aktīvai politikai.  

## <a name="create-a-category-access-rule"></a>Kategorijas piekļuves kārtulas izveidošana
1. Izvērsiet kopsavilkuma cilni **Ierobežojuma nosacījumi**.
2. Sarakstā **Politikas nosacījumu veids** atlasiet **Kategoriju piekļuves ierobežojuma nosacījumi**. Ja poga **Izveidot ierobežojuma nosacījumus** ir pelēkota, tas nozīmē, ka kategorijas piekļuvei jau ir aktīvi ierobežojuma nosacījumi. Pārbaudiet laukus **Ir spēkā** un **Beigu datums** , lai noteiktu, kura tā ir, un pēc tam atlasiet to un noklikšķiniet uz **Noņemt ierobežojuma nosacījumus**. If the **Izveidot ierobežojuma nosacījumus**, jums nav jādara nekas.  
3. Noklikšķiniet uz **Izveidot ierobežojuma nosacījumus**.
4. Laukā **Spēkā stāšanās datums** ievadiet datumu un laiku. Šis laiks nedrīkst pārklāties ar citu kārtulu, kas jau ir aktīva.  
5. Atlasiet kategoriju, uz kuru šī kārtula attieksies. Ievērojiet, kāda tai ir kategorija — tā jums vēlāk būs nepieciešama. Kad atlasāt kategoriju, atlasīto kategoriju sarakstam tiek pievienota arī tās pamatkategorija vai pamatkategorijas. Ja vēlaties, lai kārtula attiecas arī uz visām atlasītās kategorijas apakškategorijām, atzīmējiet izvēles rūtiņu **Iekļaut apakškategorijas**.
6. Noklikšķiniet bultiņu pa labi, lai pievienotu sarakstu **Atlasītās kategorijas**.  
4. Noklikšķiniet uz **Labi**. Ja opciju **Iekļaut vecākelementa kārtulu** iestatāt uz Jā, tad politikas kārtula, ko definējat vecākelementa kategorijai, tiek piešķirta arī tās bērnelementa kategorijām, ja šīm bērnelementa kategorijām nav definēti ierobežojuma nosacījumi.

## <a name="create-a-category-policy-rule"></a>Kategorijas politikas kārtulas izveidošana
1. Sarakstā **Ierobežojuma nosacījumu veids** atlasiet **Kategoriju ierobežojuma nosacījumi**. Ja poga **Izveidot Create ierobežojuma nosacījumus** ir pelēkota, atlasiet aktīvos ierobežojuma nosacījumus un pēc tam noklikšķiniet uz **Noņemt ierobežojuma nosacījumus**.  
2. Noklikšķiniet uz **Izveidot ierobežojuma nosacījumus**.
3. Laukā **Spēkā stāšanās datums** ievadiet datumu un laiku.
4. Noklikšķiniet uz **Pievienot**.
5. Laukā **Kategorija** atlasiet to pašu kategoriju, ko lietojāt iestatījumam **Kategorijas piekļuves kārtula**.
6. Laukā **Kreditora atlase** atlasiet kādu opciju. Atlasiet kārtulu, lai kontrolētu, kāda veida kreditorus var atlasīt kategorijai, kad tiek veidoti pieprasījumi.  
7. Noklikšķiniet uz **Aizvērt**. Jūsu definētās politikas kārtulas bija paredzētas pieprasījumiem ar tipu Patēriņš. Ja vēlaties definēt politikas pieprasījumiem ar tipu Papildināšana, jums būtu jāizveido kārtula politikas kārtulas tipam ar nosaukumu "Papildināšanas kategorijas piekļuves politikas kārtula".  

