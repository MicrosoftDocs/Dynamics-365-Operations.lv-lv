---
title: "Finanšu dimensijas"
description: "Šajā rakstā ir aprakstīti dažādi finanšu dimensiju veidi un izskaidrots, kā tie tiek iestatīti."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ee2d132f0b23ceec2a79ee6b0ee33862d6a0518
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="financial-dimensions"></a>Finanšu dimensijas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīti dažādi finanšu dimensiju veidi un izskaidrots, kā tie tiek iestatīti.

Izmantojiet lapu Finanšu dimensijas, lai izveidotu finanšu dimensijas, ko varat izmantot kā kontu segmentus kontu plānos. Ir divu veidu finanšu dimensijas — pielāgotas dimensijas un uz elementu balstītas dimensijas. Pielāgotās dimensijas tiek izmantotas visām juridiskajām personām, un to vērtības ievada un uztur lietotājs. Uz elementu balstītas dimensijas ir dimensijas, kuru vērtības tiek definētas citā sistēmas sadaļā, piemēram, modulī Klienti vai Veikali. Dažas uz elementu balstītas dimensijas tiek izmantotas visām juridiskajām personām, bet dažas uz elementu balstītas dimensijas ir paredzētas noteiktam uzņēmumam. 

Kad esat izveidojis finanšu dimensijas, izmantojiet lapu Finanšu dimensijas, lai piešķirtu papildu rekvizītus katrai finanšu dimensijai. 

Lai gan programmatūrā Microsoft Dynamics 365 for Operations varat izmantot finanšu dimensijas, lai norādītu juridiskās personas, tās neizveidojot, finanšu dimensijas nav paredzētas juridisko personu operāciju vai uzņēmējdarbības vajadzību nodrošināšanai. Programmatūras Microsoft Dynamics 365 for Operations starpvienību uzskaites funkcionalitāte ir paredzēta darbam tikai ar katras transakcijas izveidotajiem uzskaites ierakstiem. 

Pirms iestatāt finanšu dimensijas kā juridiskas personas, nosakiet, vai šie iestatījumi ir piemēroti jūsu organizācijai, novērtējot savas uzņēmējdarbības procesus tālāk norādītajās jomās.

-   Krājumi
-   Pārdošanas un pirkšanas darījumi starp finanšu dimensijām un juridiskām personām
-   PVN aprēķins un pārskatu izveide
-   Operāciju pārskatu izveide

Tālāk ir sniegti daži ierobežojumu piemēri.

-   PVN funkcijas var lietot tikai juridiskām personām, nevis finanšu dimensijām.
-   Dažos pārskatos nav ietvertas finanšu dimensijas, tāpēc dažreiz pārskatus nevar veidot pēc finanšu dimensijas, ja vien šie pārskati netiek modificēti.

**Pielāgotas dimensijas** 

Lai izveidotu lietotāja definētu finanšu dimensiju, laukā Izmantot vērtības no atlasiet opciju &lt; Pielāgota dimensija &gt;. Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku. Jūs varat ievadīt rakstzīmes, kas paliek vienādas katrai dimensijas vērtībai, piemēram, burtus vai pārnesumzīmi. Numura zīmes (\#) un zīmes & varat arī ievadīt kā vietturus burtiem un cipariem, kas mainīsies ikreiz, kad tiks izveidota dimensijas vērtība. Numura zīmi (\#) izmantojiet kā vietturi cipariem un zīmi & izmantojiet kā vietturi burtiem. 

**Piemērs** 

Lai dimensijas vērtību noteiktu kā burtus CC un trīs ciparus, kā formāta maska ir jāieraksta CC-\#\#\#. Šis lauks ir pieejams tikai tad, ja laukā Izmantot vērtības no ir atlasīta vērtība &lt; Pielāgota dimensija &gt;. 

**Uz elementu balstītas dimensijas** 

Lai izveidotu uz elementu balstītu finanšu dimensiju, laukā Izmantot vērtības no atlasiet sistēmas definētu elementu, uz kuru balstīt finanšu dimensiju. Finanšu dimensijas vērtības tiek veidotas no šīs atlases. Piemēram, lai izveidotu dimensijas vērtības projektiem, atlasiet Projekti. Dimensijas vērtība tiks izveidota katram projekta nosaukumam. Dimensiju vērtību lapā tiek rādītas elementa vērtības un vērtībai atbilstošais uzņēmums, ja vērtības ir raksturīgas noteiktam uzņēmumam. 

**Dimensiju aktivizēšana** 

Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas. Varat ievadīt dimensijas vērtības pirms finanšu dimensijas aktivizēšanas, taču finanšu dimensiju nevar nekur patērēt, kamēr tā nav aktivizēta. Piemēram, nevarat pievienot finanšu dimensiju konta struktūrai, kamēr finanšu dimensija nav aktivizēta. Noklikšķinot uz Aktivizēt, tiek atjauninātas visas dimensijas, kuru statuss ir mainīts. 

**Tulkojumi** 

Lapā Teksta tulkojums varat ievadīt atlasītajai finanšu dimensijai parādāmo tekstu dažādās valodās. Lapā Galvenā konta tulkojums varat ievadīt galvenā konta parādāmo tekstu dažādās valodās. 

**Juridiskas personas prioritātes** 

Ne visas dimensijas ir derīgas visām juridiskajām personām, un noteiktas dimensijas var attiekties tikai uz noteiktu laika periodu. Šādā gadījumā varat izmantot sadaļu Juridiskas personas prioritātes, lai norādītu, kuriem uzņēmumiem dimensija ir jāaiztur, kas ir īpašnieks un kāds ir dimensijas aktīvais laika periods.






