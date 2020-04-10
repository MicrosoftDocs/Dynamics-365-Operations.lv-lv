---
title: Pārnest projektu budžetus fiskālā gada beigās
description: Šajā rakstā sniegta informācija par to, kā pārsūtīt atlikušās budžeta summas uz nākamajiem gadiem un izveidot budžeta reģistra informāciju.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172334"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Pārnest projektu budžetus fiskālā gada beigās

[!include [banner](../includes/banner.md)]

Strādājot pie daudzgadu projekta, iespējams, jums fiskālā gada beigās radies budžeta pārpalikums. Varat pārvirzīt atlikušās budžeta summas uz gadu nākotnē un izveidot budžeta reģistra informāciju summām virsgrāmatas kontos. Pirms atlikušo summu pārnešanas, pārskatiet un analizējiet atlikušās budžeta summas.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Atlikušo budžeta summu pārskatīšana un analizēšana

Veiciet šādas darbības, lai pārskatītu gada beigu budžeta summas projektiem, taču šīs summas nepārnestu.

1. Dodieties uz **Projektu vadība un uzskaite** > **Periodiski** > **Budžeti** > **Pārnest budžetus**. 
2. Lapā **Projekta budžeta pārnešanas process**, kas atrodas cilnē **Gada beigu opcijas**, pārbaudiet, vai nav aktivizēta opcija **Pārnest atlikušās projekta budžeta summas**.
3. Cilnes **Parametri** laukā **Projekta budžeta gads** atlasiet fiskālo gadu, kuram vēlaties skatīt atlikušo budžeta summu. 
4. Laukā **Atvēršanas fiskālais gads** atlasiet finanšu gada sākumu, kuram vēlaties skatīt atlikušās budžeta summu. 
5. Laukā **No prognozes modeļa** atlasiet **Atlikušais budžets**. 
6. Lai iekļautu projektus, kas atbilst jūsu atlasītajiem kritērijiem un kuriem nav budžeta pārpalikuma, atlasiet **Rādīt nulles atlikumu**.  
7. Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus**, lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem, un pēc atlasiet **Apstrādāt**. 
8. Lai izveidotu datu bāzes vaicājumu, kas rūtī ielādē konkrētu budžetu kopu, atlasiet **Izgūt atlasītos budžetus**.

Lai iegūtu papildu informāciju par noteiktu rindu rūtī, atlasiet rindu un pēc tam atlasiet **Skatīt budžeta informāciju** vai **Skatīt kontus**.

## <a name="carry-forward-remaining-budget-amounts"></a>Pārnest atlikušās budžeta summas 

Apstrādājot atlikušās budžeta summas, varat Virsgrāmatā izveidot transakcijas summām, kuras pārnesat. Lai izveidotu Virsgrāmatas darījumus, veiciet darbības, kas norādītas sadaļā [Pārnesiet budžeta summas un izveidojiet Virsgrāmatas transakcijas](#carry-forward). 

> [!NOTE]
> Pārnestās budžeta summas tiek pārvirzītas uz prognozes modeli, ko atlasa lapā **Prognozes modeļi** kā pārnesamo prognozes modeli.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Budžeta summu pārnešana un virsgrāmatas darījumu izveidošana

1.  Atlasiet **Projektu vadība un uzskaite** > **Periodiski** > **Budžeti** > **Pārnest budžetus**. 
2. Lapā **Projekta budžeta pārneses process** atlasiet **Gada beigas**un pēc tam iespējojiet **Pārnest atlikušās projekta budžeta summas** un **Izveidot budžeta reģistra ierakstus Virsgrāmatā**. 
3. Cilnē **Parametri**, kas atrodas lauku grupā **Projekta parametri**, atlasiet sekojošo:

   - **Projekta budžeta gads**: Atlasiet finanšu gada sākumu, kuram vēlaties skatīt atlikušās budžeta summas. 
   - **Peļņa un zaudējumi**: Izveidojiet peļņas un zaudējumu transakcijas Virsgrāmatā. 
   -  **NP**: Izveidojiet nepabeigto darbu (NP) transakcijas Virsgrāmatā.
   -  **Alga**: Izveidojiet algas sadalījuma transakcijas Virsgrāmatā. 

5. Lauka grupā **Virsgrāmata** norādiet šādu informāciju: 

   - Laukā **Atvēršanas fiskālais gads** atlasiet finanšu gada sākumu, uz kuru vēlaties pārsūtīt projektiem atlikušās budžeta summas. Noklusētā vērtība ir viens gads pēc vērtības laukā **Projekta budžeta gads**.
   -  Laukā **Pārneses periods** atlasiet periodu, kuram vēlaties izveidot budžeta reģistra informāciju virsgrāmatā. Parasti tas ir pirmais periods atvērtajā finanšu gadā.

6. Lauka grupā **Kopēt no/uz** norādiet šādu informāciju:

   - Laukā **No prognozes modeļa** atlasiet projekta budžeta modeli, kas ir saistīts ar atlikušajām budžeta summām, kuras vēlaties pārsūtīt projektiem. 
   - Laukā **Uz Virsgrāmatas budžeta modeli** atlasiet virsgrāmatas budžeta modeli, kas ir saistīts ar budžeta summām, kuras vēlaties pārsūtīt uz virsgrāmatu. 
   -  Lai izmantotu projekta pārdošanas valūtu virsgrāmatas darījumiem, kas tiek izveidoti, kad projektiem pārsūtāt budžeta summas, atlasiet **Pārvirzīt pārdošanas valūtu**. Kad opcija nav atlasīta, transakcijas izmanto uzskaites valūtu. 
   -  Atlasiet **Rādīt nulles atlikumu**, lai iekļautu projektus, kuriem nav pārpalikušu budžeta summu, taču atbilst citiem kritērijiem, kurus atlasiet projektos, kas rādīti apakšējā rūtī.

7. Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus**, lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem. ja labāk vēlaties izveidot datu bāzes vaicājumu, kas rūtī ielādē konkrētu projekta budžetu kopu, atlasiet **Izgūt atlasītos budžetus**.
8. Katram projektam, ko vēlaties apstrādāt, atzīmējiet opciju šī projekta rindas sākumā.

    > [!TIP]
    > Lai atlasītu visus vai vairumu projektu, atzīmējiet izvēles rūtiņu augšējā kreisajā stūrī. Lai neiekļautu nevienu projektu, noņemiet atzīmi šim projektam.

9. Lai atlasītajiem projektiem atlikušās budžeta summas nodotu atlasītājam finanšu gadam un izveidotu budžeta reģistra informāciju Virsgrāmatā, noklikšķiniet **Apstrādāt**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Budžeta summu pārnešana bez Virsgrāmatas darījumu izveidošanas

1. Dodieties uz **Projektu vadība un uzskaite** > **Periodiski** > **Budžeti** > **Pārnest budžetus**.
2. Lapas **Projekta budžeta pārnešanas process** laukā **Gada beigu opcijas** atlasiet opciju **Pārnest atlikušās projekta budžeta summas**.
3. Grupas **Parametri** laukā **Projekta budžeta gads** atlasiet fiskālo gadu, kuram vēlaties skatīt atlikušās budžeta summas.
4. Grupā **Kopēt no/uz** norādiet šādu informāciju:

   - Laukā **No prognozes modeļa** atlasiet projekta budžeta modeli, kas ir saistīts ar atlikušajām budžeta summām, kuras vēlaties pārsūtīt projektiem. 
   - Lai iekļautu projektus, kuriem nav budžeta pārpalikuma bet kas atbilst citiem jūsu atlasītajiem kritērijiem, atlasiet **Rādīt nulles atlikumu**.
   - Grupā **Atlasīt budžetus** atlasiet **Izgūt visus budžetus**, lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem. Lai izveidotu datu bāzes vaicājumu, kas rūtī ielādē konkrētu projekta budžetu kopu, atlasiet **Izgūt atlasītos budžetus**.

5. Katram projektam, ko vēlaties apstrādāt, atzīmējiet opciju šī projekta rindas sākumā. 
6. Atlasiet **Apstrādāt**, lai izvēlētajiem projektiem atlikušās budžeta summas nodotu atlasītājam finanšu gadam.

