---
title: Uzturēšanas kontrolsaraksti
description: Šajā rakstā ir aprakstīti uzturēšanas kontrolsaraksti Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9139ce57283482d8da4b7f1e5d6275c74ad28
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854534"
---
# <a name="maintenance-checklists"></a>Uzturēšanas kontrolsaraksti

[!include [banner](../../includes/banner.md)]



Uzturēšanas kontrolsaraksti tiek iestatīti uzturēšanas darbu veidiem. Aizpildiet uzturēšanas kontrolsarakstus kā daļu no darba pasūtījuma pabeigšanas procesa. Lai iegūtu papildinformāciju par to, kā uzstādīt uzturēšanas kontrolsarakstus uzturēšanas darbu veidiem lapā **Uzturēšanas darbu veidu noklusējumi**, skatiet sadaļu [Uzturēšanas darbu veidu kategorijas un uzturēšanas darbu veidi, uzturēšanas darbu veidu varianti, uzturēšanas darbu amati un uzturēšanas kontrolsaraksti](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Kad jūs strādājāt ar uzturēšanas kontrolsarakstiem pie darba pasūtījuma, jūs varat aizpildīt iepriekš definētus uzturēšanas kontrolsarakstus, kuri ir saistīti ar uzturēšanas darbu veidiem. Varat arī pievienot papildu uzturēšanas kontrolsarakstus.


## <a name="fill-in-a-maintenance-checklist"></a>Aizpildiet uzturēšanas kontrolsarakstu

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu un pēc tam darbības rūtī, cilnē **Darba pasūtījums** grupā **Rindas** atlasiet **Uzturēšanas kontrolsaraksts**.

3. Sadaļā **Darba pasūtījuma uzturēšanas darba kontrolsaraksts** ir redzami kontrolsaraksti visiem darba pasūtījuma darbiem. Ja darba pasūtījuma darbiem ir atšķirīgi uzturēšanas darba veidi, uzturēšanas kontrolsaraksti var būt atšķirīgi katram darba pasūtījuma darbam. Atlasiet darba pasūtījuma darbu, lai strādātu ar saistīto uzturēšanas kontrolsarakstu. Atlasītās uzturēšanas kontrolsaraksta rindas detalizēta informācija ir uzrādīta kopsavilkuma cilnē **Detalizēta informācija par rindu**.

4. Aizpildiet uzturēšanas kontrolsaraksta rindas pa vienai tādā secībā, kādā tās parādās. Jūs aizpildāt uzturēšanas kontrolsaraksta rindu, aizpildot laukus kopsavilkuma cilnē **Detalizēta informācija par rindu**. Rindas pabeigšanai vajadzīgā informācija var atšķirties atkarībā no rindas veida. Piemēram, rindas veidā **Teksts** jūs pievienojat piezīmi, kurā paskaidrots jūsu pārbaudes rezultāts. Rindas veidā **Mērījums** jūs pievienojat skaitītāja vērtību, kuru jūs nolasāt no aprīkojuma, un, ja nepieciešams, jūs varat pievienot arī piezīmi. Uzturēšanas kontrolsaraksta rindas veids **Galvene** tiek izmantots kā virsraksts, lai grupētu uzturēšanas kontrolsaraksta rindas, kas parādās zem tās. Jums nav jāaizpilda galvene. Tāpat kā visiem citiem uzturēšanas kontrolsaraksta rindu veidiem, jūs varat pievienot piezīmi rindas veidam **Virsraksts**.

5. Ja instrukcijas ir saistītas ar uzturēšanas kontrolsaraksta rindu, tiek atlasīta izvēles rūtiņa **Instrukcijas**. Atlasītās uzturēšanas kontrolsaraksta rindas instrukcijas var lasīt laukā **Instrukcijas** kopsavilkuma cilnē **Detalizēta informācija par rindu**.

6. Kad esat aizpildījuši uzturēšanas kontrolsaraksta rindu, tajā rindā atlasiet izvēles rūtiņu **Atzīmēts**, lai atzīmētu to kā pabeigtu. Lai atsauktu uzturēšanas kontrolsaraksta rindu, jo tā neattiecas uz darba pasūtījuma darbu, rindā atlasiet izvēles rūtiņu **N/A**. Ja uzturēšanas kontrolsaraksta rindā ir atlasīta izvēles rūtiņa **Obligāts**, ir jāatlasa vai nu izvēles rūtiņa **Atzīmēts** , vai izvēles rūtiņa **N/A**.

>[!NOTE]
>Jūs varat atjaunināt uzturēšanas kontrolsaraksta reģistrācijas vienīgi tad, ja darba pasūtījums ir dzīves cikla stāvoklī [Aktīvs](../setup-for-work-orders/work-order-lifecycle-states.md).  


## <a name="add-a-maintenance-checklist-line"></a>Pievienot uzturēšanas kontrolsaraksta rindu

Uzturēšanas kontrolsaraksti tiek izveidoti no definīcijas uzturēšanas darba veida noklusējumā un ir pārvirzīti uz darba pasūtījuma darbu. Nepieciešamības gadījumā varat pievienot uzturēšanas kontrolsaraksta rindas darba pasūtījuma darbam. Uzturēšanas kontrolsaraksta rindām, kuras jūs manuāli pievienojat, ir atsauce **Manuāli**.

1. Lapā **Darba pasūtījuma uzturēšanas darba kontrolsaraksts** atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot uzturēšanas kontrolsarakstu.

2. Kopsavilkuma cilnē **Uzturēšanas kontrolsarakstu rindas** atlasiet uzturēšanas kontrolsaraksta rindu. Pēc tam, lai pēc atlasītās rindas ievietotu jaunu rindu, nospiediet taustiņu **Lejupvērstā bultiņa**. Nākamais numurs secībā tiek automātiski ievadīts **Rindas numurs** laukā. Lai ievietotu jaunu rindu pirms atlasītās rindas, atlasiet **Pievienot rindu.** 

3. Ievadiet uzturēšanas kontrolsaraksta rindas nosaukumu laukā **Nosaukums**.

4. Laukā **Tips** atlasiet uzturēšanas kontrolsaraksta rindas tipu. Kopsavilkuma cilne **Detalizēta informācija par rindu** satur saistītus laukus katram uzturēšanas kontrolsaraksta veidam.
    - **Teksts** - Izmantojiet šo veidu, lai pievienotu uzturēšanas kontrolsaraksta rindu ar tekstu, kas apraksta, kas ir jādara. Piemēram, jūs varat izmantot šo uzturēšanas kontrolsaraksta veidu, ja vēlaties, lai speciālists kaut ko pārbauda vai izmeklē, taču ja jūs nesagaidāt konkrētu (izmērāmu) rezultātu. Pēc šī veida atlasīšanas **Detalizētā informācija par rindu** kopsavilkuma cilnes laukā **Instrukcijas** ievadiet tekstu, kas apraksta, kas ir jādara.
    - **Galvene** - Šāda veida uzturēšanas kontrolsaraksta rinda tiek izmantota kā virsraksts, lai grupētu uzturēšanas kontrolsaraksta rindas, kas parādās zem tās. Šis tips ir noderīgs, ja jums ir vairākas uzturēšanas kontrolsaraksta rindas, kuras var iedalīt konkrētās jomās. Pēc šāda veida atlasīšanas ievadiet aprakstošu nosaukumu laukā **Nosaukums**.
    - **Veidne** - Šis veids nav piemērojams, ja manuāli darba pasūtījuma darbam pievienojat uzturēšanas kontrolsarakstu.  
    - **Mainīgais** - Izmantojiet šo veidu, lai uzturēšanas kontrolsaraksta rindā definētu iespējamo rezultātu diapazonā. Lai iegūtu informāciju par uzturēšanas kontrolsarakstu mainīgo uzstādīšana, skatiet [Darba veidu kategorijas un uzturēšanas darbu veidi, uzturēšanas darbu veidu varianti, uzturēšanas darbu amati un uzturēšanas kontrolsaraksti](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Pēc šī veida atlasīšanas laukā **Nosaukums** ievadiet aprakstošu mainīgā nosaukumu. Kopsavilkuma cilnē **Detalizētā informācija par rindu** laukā **Mainīgais** atlasiet mainīgo. Laukā **Norādījumi** ievadiet tekstu, kas apraksta, kas ir jādara.
    - **Mērījums** - Izmantojiet šo veidu, lai ierakstītu konkrētu mērījumu uzturēšanas kontrolsaraksta rindā. Pēc šī veida atlasīšanas laukā **Nosaukums** ievadiet veidnes nosaukumu. Kopsavilkuma cilnē **Detalizētā informācija par rindu** laukos **Skaitītājs** un **Vienība** atlasiet atbilstīgās vērtības. Laukā **Norādījumi** ievadiet tekstu, kas apraksta, kas ir jādara.

5. Kad esat beidzis manuālo uzturēšanas kontrolsaraksta rindu pievienošanu, aizpildiet rindas, kā aprakstīts iepriekšējā sadaļā **Uzturēšanas kontrolsaraksta aizpildīšana**.

>[!NOTE]
>Lapā **Darba pasūtījuma uzturēšanas darba kontrolsaraksts** jūs nevarat dzēst uzturēšanas kontrolsaraksta rindas ar atsauci **Darba veids**. Jūs varat dzēst vienīgi uzturēšanas kontrolsaraksta rindas ar atsauci **Manuāli**, kuras jūs vai citi uzturēšanas speciālisti ir izveidojuši manuāli.

Attēlā tālāk parādīts uzturēšanas kontrolsaraksta piemērs.

![1. attēls.](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]