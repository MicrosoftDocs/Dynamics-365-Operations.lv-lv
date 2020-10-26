---
title: Kanban darbu plānošana metodei lean manufacturing
description: Šajā rakstā ir sniegta informācija par vizuālo kontroli pār kanban darbu plānošanu un dažādajiem veidiem, kā plānot kanban darbus.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77ba67de5585022ab7d506c8cd2acb380a4e3a54
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979455"
---
# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban darbu plānošana metodei lean manufacturing

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par vizuālo kontroli pār kanban darbu plānošanu un dažādajiem veidiem, kā plānot kanban darbus.  

Lapa **Kanban darbu plānošana** nodrošina lean manufacturing darba šūnu vizuālu kontroli. Tā sniedz visu Kanban darbu pārskatu un nodrošina vairākas filtrēšanas iespējas. No šīs lapas var pārvietoties uz visām citām lapām, kas ir saistītas ar Kanban konfigurāciju un izpildi.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automātiska Kanban darbu plānošana
Plānošanu var aktivizēt automātiski, ja iestatāt Kanban nosacījuma parametru **Automātiskais plānošanas daudzums**. Ja iestatāt parametra **Automātiskais plānošanas daudzums** vērtību **1**, katrs Kanban darbs tiek automātiski plānots uzreiz pēc tā izveidošanas. Rezultāts ir pirmās pieprasījumpiegādes, pirmās apkalpošanas operāciju sērija. Ja iestatāt **Automātiskais plānošanas daudzums** uz vērtību, kas ir lielāka nekā 1, Kanban darbi tiek grupēti, pirms tie tiek plānoti. 

Šī koncepcija ļauj padarīt Kanban lielumu mazāku par faktiskās ekonomiskās partijas lielumu. Piemēram, konkrēta krājuma (vai krājumu saimes) ekonomiskās partijas lielums ir 30. Tā vietā, lai izveidotu Kanban, kas izmantot preču daudzumu 30, varat konfigurēt Kanban nosacījumu tā, lai preču daudzums būtu 10 un parametra **Automātiskais plānošanas daudzums** vērtība būtu **3**. Lai gan automātiskā plānošana plāno Kanban darbus darba šūnai tikai tad, ja pastāv trīs neplānotie darbi, plānotājs un ražotnes vadītājs var skaidri redzēt, ka divi neplānotie darbi gaida izpildi. Plānotājs vai ražotnes pārvaldnieks var iekļaut šos divus darbus ražošanā, ieplānojot tos manuāli vai izveidojot papildu Kanban.

## <a name="manual-scheduling"></a>Manuālā plānošana
Manuālai plānošanai programmā Microsoft Dynamics AX 2012 ir ieviests Kanban plānošanas panelis. Manuālo plānošanu var kombinēt ar automātisko plānošanu. Kanban plānošanas panelis ļauj jums plānot darbus un izņemt darbus no plāna, mainīt tos secību vai pārvietot to no perioda uz periodu. Darbus, kas ir balstīti uz Kanban nosacījumiem, kur vērtība **Automātistā plānošana** ir lielāka par **0**, var manuāli izslēgt no plāna. Tomēr, šie darbi tiks pārplānoti, kad notiks nākamais automātiskās plānošanas notikums (t.i., kad tiek izveidots jauns Kanban). Manuālai plānošanai ir pieejamas šādas opcijas:

-   **Plānot** plāno atlasītos darbus atbilstoši to izpildes datumam. (Šī opcija līdzinās automātiskai plānošanai.)
-   **Plānot uz priekšu no datuma** mēģina plānot atlasītos darbus atbilstoši to izpildes datumam, bet ierobežo rezultātu, izmantojot norādīto agrāko sākuma datumu.
-   **Atpakaļ** pārvieto atlasītos ieplānotos darbus atpakaļ secībā perioda ietvaros.
-   **Uz priekšu** pārvieto atlasītos ieplānotos darbus uz priekšu secībā perioda ietvaros.
-   **Iepriekšējais periods** pārvieto atlasītos ieplānotos darbus uz iepriekšējā perioda sākumu vai beigām.
-   **Nākamais periods** pārvieto atlasītos ieplānotos darbus uz nākamā perioda sākumu vai beigām.
-   Opcija **Plānot** &gt; **Atgriezt darba statusu**sniedz iespēju atcelt ieplānota darba plānošanu.

## <a name="lean-scheduling-groups"></a>Racionālās plānošanas grupas
Katra krāsa apzīmē racionālās plānošanas grupu. Racionālās plānošanas grupas var brīvi definēt kā vispārējas grupas vai grupas, kas pieder vienai darba šūnai. Krājumus un dimensijas var brīvi piešķirt plānošanas grupām. Piemēram, šūnā Krāsošana plānošanas grupa var atspoguļot preces krāsu. Darbā, kas tiek pildīts ar noteiktām rīku prasībām, krājumus iespējams grupēt pēc rīka vajadzības un iepakojuma darba šūnā tos var grupēt pēc iepakojuma veidnes. Krāsas izmantošana racionālās plānošanas grupām nav obligāta, bet ieteicama. Tādējādi tiek uzlabota plāna statusa redzamība. Piemēram, var ļoti viegli redzēt, kuras krāsas tiek ražotas konkrētās dienās, tāpēc varat uzreiz noteikt, kā optimizēt šo darbu.

## <a name="work-cell-capacity-and-period-capacity"></a>Darba šūnas noslodze un perioda noslodze
Racionālās darba šūnas noslodze vienmēr ir vienlaicīga noslodze. Citiem vārdiem sakot, darba šūnā var būt aktīvi vairāki darbi vienlaikus. Noslodzi var izsekot divos režīmos: caurlaide un stundas.

### <a name="throughput"></a>Caurlaide

Darba šūnas noslodze ir noteikta pēc atsauces perioda (standarta darbdienas, nedēļas vai mēneša) vidējā caurlaides daudzuma. Faktiskā noslodze dienā vai nedēļā pēc tam tiek aprēķināta, pamatojoties uz kalendārā norādītajiem darba laikiem, kas piešķirti darba šūnai. Noslodze, kas tiek ielādēta ar darbu, ir darba daudzums, ko koriģē ar krājuma caurlaides koeficientu darba šūnā.

### <a name="hours"></a>Stundas

Pieejamā noslodze dienā vai nedēļā tiek noteikta pēc kalendāra, kas piešķirts darba šūnai. Noslodze, kas tiek ielādēta ar darbu, ir aktivitātes cikla laiks, ko koriģē ar krājuma daudzumu (noklusētais aktivitātes daudzums, salīdzinot ar faktisko darba daudzumu) un caurlaides koeficientu darba šūnā.

#### <a name="period-capacity-factbox"></a>Papildinformācija par perioda noslodzi

Saraksta lapa **Kanban darbu plānošana** satur papildinformāciju, kur redzama pieejamā un rezervēta perioda noslodze atlasītajai darba šūnai. Atkarībā no atlasītajiem plānošanas periodiem ražošanas plūsmas modelī, periodi tiek rādīti dienās vai nedēļās.

<a name="additional-resources"></a>Papildu resursi
--------



