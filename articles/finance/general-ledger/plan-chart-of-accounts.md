---
title: Plānot kontu plānu
description: Šajā tēmā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29e5328043a4259b464b272983e11061ade1724c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230374"
---
# <a name="plan-your-chart-of-accounts"></a>Plānot kontu plānu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu.

Lai organizācijā izsekotu un uzturētu finanšu informāciju, varat iestatīt kontu plānu. Kontu plāns ir kontu kopa, kas definē finanšu shēmu. Lai turpmāk izsekotu šo kontu transakcijas, varat pievienot segmentus. Šos segmentus sauc par finanšu dimensijām. Piemēram, izdevumu kontā var iekļaut šādas finanšu dimensijas: Nodaļa, Izmaksu centrs un Nolūks. Lietotāja definētās kārtulas nosaka to, kā finanšu dimensijas tiek pievienotas galvenajiem kontiem un citām finanšu dimensijām, kā arī to, kā var ievadīt transakcijas. Šīs lietotāja definētās kārtulas sauc par konta struktūrām un papildu kārtulām.

Kontu plāns ir juridiskas personas virsgrāmatas kontu strukturētais saraksts. Saraksts tiek lietots, lai sagatavotu finanšu pārskatus iestādēm un īpašniekiem. Konti vispirms tiek grupēti kontu veidos un pēc tam apkopoti lielākās kategorijās. Vispārīgā līmenī konti tiek grupēti kā ieņēmumi un izmaksas (operāciju konti) un kā aktīvi un pasīvi (bilances konti).

Kontu plānu var kopīgot un jebkura juridiskā persona organizācijā to var izmantot. Kontu plāns, ko izmanto juridiskā persona, tiek definēts lapā **Virsgrāmata**.

Tālāk ir minēti daži faktori, kas jāņem vērā, plānojot savas organizācijas kontu plāna strukturu.

- Valsts vai reģiona, kurā ir bāzēta jūsu organizācija, atskaišu prasības
- Juridiskās personas prasības atskaišu veidošanai
- Nepieciešamā specifikācijas pakāpe ārējās organizācijās un savā organizācijā.

Veidojiet kontu plānu lapā **Kontu plāns**. Galvenos kontus varat izveidot lapā **Kontu plāns** vai **Galvenie konti**. Galvenajos kontos nevajadzētu izmantot speciālās rakstzīmes, ko izmanto kā kontu plāna norobežotājus. Pretējā gadījumā var veidoties nestabilitāte vai arī būs nepieciešams vienmēr izmantot uzmeklēšanas rezultātus vai dialoglodziņu, ievadot kontu un dimensiju kombinācijas. Papildinformāciju skatiet šeit: [Izveidot galveno kontu](tasks/create-main-account.md).

> [!NOTE]
> Dynamics 365 for Finance and Operations versijā 8.0 (2018. gada aprīlis) varat izmainīt kontu plāna norobežotāju lapā **Virsgrāmatas parametri**.

Ir ieteicams saistīt galvenos kontus ar galvenā konta kategorijām, lai varētu izmantot noklusējuma finanšu pārskatus, neveicot jebkādas izmaiņas. Tādējādi varat ātrāk un vieglāk izstrādāt un uzturēt pārskatus.

Kontu struktūras varat izveidot lapā **Konfigurēt kontu struktūras**. Kontu struktūras nosaka derīgās kombinācijas. Šīs kombinācijas kopā ar galvenajiem kontiem izveido kontu plānu. Papildinformāciju skatiet šeit: [Izveidot kontu struktūras](tasks/create-account-structures.md).

**Juridiskas personas prioritātes**

Daži galvenie konti nav derīgi visām juridiskajām personām un var attiekties tikai uz noteiktu laika periodu. Šādā gadījumā varat izmantot sadaļu **Juridiskas personas prioritātes**, lai identificētu uzņēmumus, attiecībā uz kuriem šis galvenais konts ir jāaiztur, kā arī īpašnieku un periodu, kad šī dimensija ir aktīva. Koplietošanas līmenī prioritātes nevar būt vairāk ierobežojošas nekā prioritātes, kas ir juridiskās personas līmenī.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Finanšu dimensijas](financial-dimensions.md)
- [Papildu kārtulu struktūru izveide un piešķiršana](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]