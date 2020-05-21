---
title: Izveidot prognozes modeļus projekta budžetiem
description: Šajā tēmā aprakstīts, kā izveidot prognozes modeli atlikušajiem budžetiem.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321783"
---
# <a name="create-forecast-models-for-project-budgets"></a>Izveidot prognozes modeļus projekta budžetiem 

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot prognozes modeli atlikušajiem budžetiem. Projekts, kas ir pakļauts budžeta kontrolei, izmanto divu veidu budžetus: sākotnējo un atlikušo. Veidojot projekta budžetu, ir jānorāda sākotnējā un atlikušā budžeta prognozes modeļi, kas izveidoti **Prognozes modeļi** lapā. Uz norādītajiem modeļiem pamatotie projekta budžeti tiek veidoti, kad apstiprināt projekta budžetu.

> [!NOTE]
> Budžeta modelim, kuru izmanto budžeta kontrolei, nevar būt apakšmodeļu vai izmantot kā apakšmodeli.

1. Atlasiet **Projektu pārvaldība un uzskaite** > **Iestatījumi** > **Prognozes**  > **Prognožu modeļi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu prognozes modeli, un pēc tam ierakstiet modeļa ID numuru un jaunā modeļa nosaukumu. 
3. Iestatiet opciju **Apturēts** uz **Jā**, lai nepieļautu izmaiņas prognožu modeļa rindās. 
4. Ja prognozes rindām, ar kurām modelis ir saistīts, ir jāģenerē naudas plūsmas prognozes virsgrāmatā, iestatiet **iekļaut skaidras naudas plūsmas prognozes** uz **Jā.** 
5. Lai lietotu projekta datumu kā rēķina datumu, iestatiet **Prognozes rēķina datumu** uz **Jā**. 
6. Laukā **Budžeta veids** atlasiet vienu no šādiem modeļa veidiem:

   - **Sākotnējais budžets**: izmantojiet sākotnējā budžeta summas, kas tiek izpildītas, kad sākotnējais budžets ir izveidots un apstiprināts.
   - **Atlikušais budžets**: izmantojiet atlikušā budžeta summas projekta dzīves cikla laikā. Šī budžeta modeļa bilances tiek samazinātas ar faktiskajiem darījumiem un palielinātas vai samazinātas ar budžeta pārskatījumiem.
   - **Pārnešana**: izmantojiet pārnestā budžeta summas šim projektam. Pārnešana ir neobligāts process, ko var palaist, lai neizmantotās budžeta summas pārsūtītu no viena finanšu gada uz citu.

7. Iestatiet sekojošās opcijas, kā nepieciešams:

   - Iespējojiet **Prognozes rēķina datumu**, lai lietotu projekta datumu kā rēķina datumu.
   - Iespējojiet **Prognoze ar NP** uz prognozi, pamatojoties uz nepabeigto darbu (NP), un pēc tam atlasiet NP veidu. 
   - Noklusējuma **Budžeta veidu** var paturēt kā **Neviens** vai ievadīt jaunu veidu. Pēc ieraksta maiņas budžeta veidu nevar mainīt.     
    > [!NOTE]
    > Mainot noklusējuma budžeta veidu, visas citas opcijas vairs nebūs pieejamas atjauninājumiem un šo budžeta modeli nevar izmantot atkārtoti. 
   


 

