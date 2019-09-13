---
title: Uzturēšanas kontrolsaraksti
description: Šajā tēmā aprakstīti uzturēšanas kontrolsaraksti Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875783"
---
# <a name="maintenance-checklists"></a>Uzturēšanas kontrolsaraksti


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Uzturēšanas kontrolsaraksti tiek iestatīti uzturēšanas darbu tipiem un tiek izmantoti, kad strādājat pie darba pasūtījuma. Uzturēšanas kontrolsarakstu aizpildīšana ir daļa no darba pasūtījuma pabeigšanas. Skatiet sadaļu [Uzturēšanas darbu tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu amati un uzturēšanas kontrolsaraksti](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md), lai iegūtu vairāk informācijas par to, kā uzstādīt uzturēšanas kontrolsarakstus uzturēšanas darbu tipiem veidlapā **Uzturēšanas darbu tipu noklusējumi**.

Strādājot ar uzturēšanas kontrolsarakstiem pie darba pasūtījuma, jūs varat aizpildīt iepriekš definētus uzturēšanas kontrolsarakstus, kuri ir saistīti ar uzturēšanas darbu tipiem. Var pievienot papildu uzturēšanas sarakstus.

## <a name="fill-out-a-maintenance-checklist"></a>Uzturēšanas kontrolsaraksta aizpildīšana

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu un noklikšķiniet uz **Uzturēšanas kontrolsaraksts**.

3. Sadaļā **Darba pasūtījuma uzturēšanas darba kontrolsaraksts** ir redzami uzturēšanas kontrolsaraksti visiem darba pasūtījuma darbiem. Ja darba pasūtījuma darbiem ir atšķirīgi uzturēšanas darba tipi, uzturēšanas kontrolsaraksti var atšķirties katram darba pasūtījuma darbam. Atlasiet darba pasūtījuma darbu, lai strādātu ar saistīto uzturēšanas kontrolsarakstu. Atlasītās uzturēšanas kontrolsaraksta rindas detalizēta informācija ir uzrādīta kopsavilkuma cilnē **Detalizēta rindas informācija**.

4. Vienu pa vienai aizpildiet uzturēšanas kontrolsaraksta rindas tādā kārtībā, kādā tās ir uzrādītas. Tipa "Galvene" uzturēšanas kontrolsaraksta rinda tiek izmantota kā virsraksts, lai zemāk grupētu uzturēšanas kontrolsaraksta rindas. Jums nav jāaizpilda galvene, taču, tāpat kā visiem uzturēšanas kontrolsaraksta rindu tipiem, galvenei ir iespējams pievienot **Piezīmi**.

5. Ja instrukcijas ir saistītas ar uzturēšanas kontrolsaraksta rindu, tiek atlasīta izvēles rūtiņa **Instrukcijas**. Atlasītās uzturēšanas kontrolsaraksta rindas instrukcijas var lasīt ātrās cilnes **Rindas detalizēta informācija** > sadaļā **Instrukcijas**.

6. Informācija, kas ir nepieciešama, lai aizpildītu uzturēšanas kontrolsarakstu, var atšķirties atkarībā no saistībā uzturēšanas kontrolsaraksta tipa. Jūs aizpildāt uzturēšanas kontrolsaraksta rindu, aizpildot laukus kopsavilkuma cilnē **Detalizēta rindas informācija**. Piemēram, tipa "Teksts" rindā jūs pievienojat **Piezīmi**, kurā paskaidrots, kāds bija šīs kontrolsaraksta rindas rezultāts. Tipa "Mērījums" rindā jūs pievienojat **Skaitītāja vērtību**, kuru jūs nolasāt no aprīkojuma, un, ja nepieciešams, jūs varat pievienot arī **Piezīmi**.

- Kad esat aizpildījuši uzturēšanas kontrolsaraksta rindu, rindā atlasiet izvēles rūtiņu **Atzīmēts**, lai atzīmētu to kā pabeigtu. Ja vēlaties atsaukt uzturēšanas kontrolsaraksta rindu, jo tā neattiecas uz darba pasūtījuma darbu, rindā atlasiet izvēles rūtiņu **N/A**. Ja uzturēšanas kontrolsaraksta rinda ir atzīmēta kā **Obligāta**, jums tā jāatzīmē kā "Atzīmēts" vai "N/A".  
- Jūs varat atjaunināt uzturēšanas kontrolsaraksta reģistrācijas vienīgi tad, ja darba pasūtījums ir dzīves cikla stāvoklī [Aktīvs](../setup-for-work-orders/work-order-lifecycle-states.md).  


## <a name="add-a-maintenance-checklist-line"></a>Pievienot uzturēšanas kontrolsaraksta rindu

Uzturēšanas kontrolsaraksti tiek izveidoti no definīcijas uzturēšanas darba tipa noklusējumā un pārvirzīti uz darba pasūtījuma darbu. Nepieciešamības gadījumā jūs varat pievienot uzturēšanas kontrolsaraksta rindas darba pasūtījuma darbam. Manuāli pievienotām uzturēšanas kontrolsaraksta rindām ir atsauce "Manuāli".

1. Sadaļā **Darba pasūtījuma uzturēšanas darba kontrolsaraksts** atlasiet darba pasūtījuma darbu, kuram vēlaties pievienot uzturēšanas kontrolsarakstu.

2. Kopsavilkuma cilnē **Uzturēšanas kontrolsaraksta rindas** atlasiet uzturēšanas kontrolsaraksta rindu un nospiediet lejupvērstās bultas taustiņu, ja vēlaties ievadīt jaunu rindu pēc atlasītās uzturēšanas kontrolsaraksta rindas. Nākamais numurs secībā tiek automātiski ievadīts laukā **Rindas numurs**. Jūs varat arī atlasīt uzturēšanas kontrolsaraksta rindu un noklikšķināt uz taustiņa **Pievienot rindu**, ja vēlaties ievadīt jaunu rindu virs atlasītās uzturēšanas kontrolsaraksta rindas.

3. Laukā **Nosaukums** ievadiet uzturēšanas kontrolsaraksta rindas nosaukumu.

4. Laukā **Tips** atlasiet uzturēšanas kontrolsaraksta rindas tipu. Katram uzturēšanas kontrolsaraksta tipam kopsavilkuma cilne **Detalizēta rindas informācija** uzrāda saistītus laukus.  
  a. "Teksts" tiek izmantots, lai pievienotu uzturēšanas kontrolsaraksta rindu ar teksta aprakstu par to, ko darīt. Šo uzturēšanas kontrolsaraksta tipu var izmantot, ja vēlaties, lai speciālists kaut ko pārbauda vai izmeklē, negaidot konkrētu (mērāmu) rezultātu. Ievadiet darāmo darbību aprakstu kopsavilkuma cilnes**Rindas detalizēta informācija** sadaļā **Instrukcijas**. b. "Galvene" tiek izmantota, lai grupētu tās uzturēšanas kontrolsaraksta rindas, kuras parādās zem tās. Tas ir noderīgi, ja jums ir vairākas uzturēšanas kontrolsaraksta rindas, kuras var iedalīt konkrētās jomās. Laukā **Nosaukums** ievadiet aprakstošu nosaukumu.  
  c. "Veidne" nav piemērojama, ja manuāli darba pasūtījuma darbam pievienojat uzturēšanas kontrolsarakstu.  
  d. "Mainīgais" tiek izmantots, lai uzturēšanas kontrolsaraksta rindā definētu iespējamo rezultātu diapazonā.  Uzturēšanas kontrolsarakstu mainīgo uzstādīšana ir aprakstīta sadaļā [Darba tipu kategorijas un uzturēšanas darbu tipi, uzturēšanas darbu tipu varianti, uzturēšanas darbu amati un uzturēšanas kontrolsaraksti](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Laukā **Nosaukums** ievadiet nosaukumu, lai aprakstītu mainīgo. Laukā **Mainīgais** atlasiet mainīgo. Ievadiet darāmo darbību aprakstu kopsavilkuma cilnes**Rindas detalizēta informācija** sadaļā **Instrukcijas**.  
  e. "Mērījums" tiek izmantots, lai fiksētu konkrētu mērījumu.  Laukā **Nosaukums** ievadiet mērījuma nosaukumu. Kopsavilkuma cilnē **Rindas detalizēta informācija** atlasiet **Skaitītājs** un **Vienums**. Sadaļā **Instrukcijas** ievadiet veicamo darbību aprakstu.  

5. Kad esat beidzis manuāli pievienot uzturēšanas kontrolsaraksta rindas, aizpildiet rindas, kā aprakstīts augstāk minētajā sadaļā.

>[!NOTE]
>Sadaļā **Darba pasūtījuma uzturēšanas darba kontrolsaraksts** jūs nevarat dzēst uzturēšanas kontrolsaraksta rindas ar atsauci "Darba tips". Jūs varat dzēst vienīgi uzturēšanas kontrolsaraksta rindas ar atsauci "Manuāli", kuras jūs vai citi uzturēšanas speciālisti ir izveidojuši manuāli.


![1. attēls](media/14-work-orders.png)

