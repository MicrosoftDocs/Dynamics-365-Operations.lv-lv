---
title: "Kontu plāna plānošana"
description: "Šajā rakstā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 34425ecd4b78a134c92a2282576d0d7967d870b3
ms.lasthandoff: 03/31/2017


---

# <a name="plan-your-chart-of-accounts"></a>Kontu plāna plānošana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu.

Lai organizācijā izsekotu un uzturētu finanšu informāciju, varat iestatīt kontu plānu. Kontu plāns ir kontu kopa, kas definē finanšu shēmu. Lai turpmāk izsekotu šo kontu transakcijas, varat pievienot segmentus, kurus sauc par finanšu dimensijām. Piemēram, izdevumu kontā var iekļaut šādas finanšu dimensijas: Nodaļa, Izmaksu centrs un Nolūks. Lietotāja definētajās kārtulas, ko sauc par konta struktūrām un papildu kārtulām, nosaka to, kā šīs finanšu dimensijas tiek pievienotas galvenajiem kontiem un citām finanšu dimensijām, kā arī to, kā var ievadīt transakcijas. 

Kontu plāns ir juridiskas personas Virsgrāmatas kontu strukturētais saraksts. Saraksts tiek lietots, lai sagatavotu finanšu pārskatus iestādēm un īpašniekiem. Konti tiek grupēti kontu veicos un pēc tam apkopoti lielākās kategorijās. Vispārīgā līmenī konti tiek grupēti kā ieņēmumi un izmaksas (operāciju konti) un kā aktīvi un pasīvi (bilances konti). 

Kontu plānu var kopīgot un jebkura juridiskā persona organizācijā to var izmantot. Kontu plāns, ko izmanto juridiskā persona, tiek definēts lapā **Virsgrāmata**. 

Tālāk ir minēti daži faktori, kas jāņem vērā, plānojot savas organizācijas kontu plāna strukturu.

-   Valsts/reģiona, kurā ir bāzēta jūsu organizācija, atskaišu prasības
-   Juridiskās personas prasības atskaišu veidošanai
-   Nepieciešamā specifikācijas pakāpe ārējās organizācijās un savā organizācijā.

Kontu plānu var izveidot lapā **Kontu plāns**. Galvenos kontus var izveidot lapā **Kontu plāns** vai **Galvenie konti**. Galvenajos kontos nevajadzētu izmantot speciālās rakstzīmes, ko izmanto kā kontu plāna norobežotājus. Ja pastāv speciālā rakstzīme, kas tiek izmantota arī kā kontu plāna norobežotājs, ievadot konta un dimensijas kombinācijas, var veidoties nestabilitāte, vai arī būs nepieciešams vienmēr izmantot uzmeklēšanas rezultātus vai izlidošanu. 

Ir ieteicams saistīt galvenos kontus ar galvenā konta kategorijām, lai varētu izmantot noklusējuma finanšu pārskatus, neveicot jebkādas izmaiņas. Tādējādi varat ātrāk un vieglāk izstrādāt un uzturēt pārskatus. 

Izmantojiet lapu **Konfigurēt kontu struktūras**, lai izveidotu kontu struktūras. Kontu struktūras nosaka derīgās kombinācijas. Kombinācijas kopā ar galvenajiem kontiem izveido kontu plānu. 

**Juridiskas personas prioritātes** 

Daži galvenie konti nav derīgi visām juridiskajām personām un var attiekties tikai uz noteiktu laika periodu. Šādā gadījumā varat izmantot sadaļu Juridiskas personas prioritātes, lai norādītu, kuriem uzņēmumiem galvenais konts ir jāaiztur, kas ir īpašnieks un kāds ir dimensijas aktīvais laika periods. Koplietošanas līmenī prioritātes nevar būt vairāk ierobežojošas nekā prioritātes, kas ir juridiskās personas līmenī.

Papildinformāciju skatiet tēmā [Finanšu dimensijas](financial-dimensions.md).




