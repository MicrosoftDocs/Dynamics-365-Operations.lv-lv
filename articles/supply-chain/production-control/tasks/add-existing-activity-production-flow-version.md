---
title: Esošas aktivitātes pievienošana ražošanas plūsmas versijai
description: Izveidojot jaunu ražošanas plūsmu versijas, varat izvēlēties, vai jaunajai versijai pievienot aktivitātes, kas izveidots vecākām versijām.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c01d988469ead4ab09d69b1cb6e2f9b417080c69
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149416"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Esošas aktivitātes pievienošana ražošanas plūsmas versijai

[!include [banner](../../includes/banner.md)]

Izveidojot jaunu ražošanas plūsmu versijas, varat izvēlēties, vai jaunajai versijai pievienot aktivitātes, kas izveidots vecākām versijām. Šajā procedūrā ir aprakstīts, kā izveidot esošās ražošanas plūsmas jaunu versiju, nekopējot aktivitātes. Nākamajā darbībā esoša aktivitāte tiek pievienota jaunajai versijai. 

Lai varētu izpildīt šo uzdevumu, ir nepieciešama ražošanas plūsma ar jau izveidotu versiju un aktivitātēm.


## <a name="create-a-new-production-flow-version"></a>Izveidojiet jaunu ražošanas plūsmas versiju
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz Rediģēt.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā Beigu datums ievadiet datumu un laiku.
    * Ņemiet vērā, ka pirms jaunas ražošanas plūsmas versijas izveidošanas ir jāpārbauda aktīvās versijas derīguma termiņa beigu datums un laiks. Jaunā versija tiks izveidota ar spēkā stāšanās datumu, kas ir saistīts ar atlasītas versijas derīguma termiņa beigu datumu.  
7. Noklikšķiniet uz Pievienot.
8. Laukā Kopēt no versijas atlasiet Nē.
    * Ja lielākā daļa kopētās versijas aktivitāšu tiks aizstātas ar jaunām aktivitātēm, atlasiet Nē, lai sāktu darbu, izmantojot tukšu versiju. Aktivitāšu veidlapā manuāli pievienojiet neizmainītās aktivitātes funkcijai Pievienot esošo.  
9. Laukā Dublēt Kanban nosacījumus atlasiet Nē.
    * Ja aktivitātes jaunajā versijā netiek kopētas, Kanban nosacījumus nevar kopēt jebkurā jaunās versijas izveides brīdī.   Tā vietā Kanban nosacījumu formā vēlāk var izmantot aizstāšanas Kanban funkcijas izveidi, lai aizstātu iepriekšējās ražošanas plūsmas versijas Kanban nosacījumus ar Kanban nosacījumiem, izmantojot jaunās versijas aktivitātes.  
10. Noklikšķiniet uz OK.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

## <a name="add-an-existing-activity"></a>Pievienot esošu aktivitāti
1. Noklikšķiniet uz Aktivitātes.
2. Noklikšķiniet uz Pievienot esošu, lai atvērtu nolaižamo dialoglodziņu.
    * Atrodiet un atlasiet esošu aktivitāti, kas jāpievieno jaunajai ražošanas plūsmas versijai.  Ņemiet vērā, ka sarakstā ir redzamas visas aktivitātes, kas ir izveidotas plūsmas visu iepriekšējo versiju konkrētajai ražošanas plūsmai.  
3. Ievadiet vai atlasiet vērtību laukā Aktivitāte.
4. Noklikšķiniet uz OK.

