---
title: Sava kontu plāna plānošana
description: Šajā rakstā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10906d7b30628dfe69907cfa69ae1022fde33243
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070640"
---
# <a name="plan-your-chart-of-accounts"></a>Sava kontu plāna plānošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu.

Lai organizācijā izsekotu un uzturētu finanšu informāciju, varat iestatīt kontu plānu. Kontu plāns ir kontu kopa, kas definē finanšu shēmu. Lai turpmāk izsekotu šo kontu transakcijas, varat pievienot segmentus. Šos segmentus sauc par finanšu dimensijām. Piemēram, izdevumu kontā var iekļaut šādas finanšu dimensijas: Nodaļa, Izmaksu centrs un Nolūks. Lietotāja definētās kārtulas nosaka to, kā finanšu dimensijas tiek pievienotas galvenajiem kontiem un citām finanšu dimensijām, kā arī to, kā var ievadīt transakcijas. Šīs lietotāja definētās kārtulas sauc par konta struktūrām un papildu kārtulām.

Kontu plāns ir juridiskas personas virsgrāmatas kontu strukturētais saraksts. Saraksts tiek lietots, lai sagatavotu finanšu pārskatus iestādēm un īpašniekiem. Konti vispirms tiek grupēti kontu veidos un pēc tam apkopoti lielākās kategorijās. Vispārīgā līmenī konti tiek grupēti kā ieņēmumi un izmaksas (operāciju konti) un kā aktīvi un pasīvi (bilances konti).

Kontu plānu var kopīgot un jebkura juridiskā persona organizācijā to var izmantot. Kontu plāns, ko izmanto juridiskā persona, tiek definēts lapā **Virsgrāmata**.

Tālāk ir minēti daži faktori, kas jāņem vērā, plānojot savas organizācijas kontu plāna strukturu.

- Valsts vai reģiona, kurā ir bāzēta jūsu organizācija, atskaišu prasības
- Juridiskās personas prasības atskaišu veidošanai
- Nepieciešamā specifikācijas pakāpe ārējās organizācijās un savā organizācijā.

Veidojiet kontu plānu lapā **Kontu plāns**. Galvenos kontus varat izveidot lapā **Kontu plāns** vai **Galvenie konti**. Galvenajos kontos nevajadzētu izmantot speciālās rakstzīmes, ko izmanto kā kontu plāna norobežotājus. Pretējā gadījumā var veidoties nestabilitāte vai arī būs nepieciešams vienmēr izmantot uzmeklēšanas rezultātus vai dialoglodziņu, ievadot kontu un dimensiju kombinācijas. Papildinformāciju skatiet sadaļā [Galvenā konta izveidošana](tasks/create-main-account.md).

> [!NOTE]
> Programmā Dynamics 365 Finanšu versija 8.0 (2018. gada aprīlis) **jūs varat modificēt kontu plāna norobežotāju no Virsgrāmatas parametru** lapas.

Ir ieteicams saistīt galvenos kontus ar galvenā konta kategorijām, lai varētu izmantot noklusējuma finanšu pārskatus, neveicot jebkādas izmaiņas. Tādējādi varat ātrāk un vieglāk izstrādāt un uzturēt pārskatus.

Kontu struktūras varat izveidot lapā **Konfigurēt kontu struktūras**. Kontu struktūras nosaka derīgās kombinācijas. Šīs kombinācijas kopā ar galvenajiem kontiem izveido kontu plānu. Papildinformāciju skatiet šeit: [Izveidot kontu struktūras](tasks/create-account-structures.md).

**Juridiskas personas prioritātes**

Daži galvenie konti nav derīgi visām juridiskajām personām un var attiekties tikai uz noteiktu laika periodu. Šādā gadījumā varat izmantot sadaļu **Juridiskas personas prioritātes**, lai identificētu uzņēmumus, attiecībā uz kuriem šis galvenais konts ir jāaiztur, kā arī īpašnieku un periodu, kad šī dimensija ir aktīva. Koplietošanas līmenī prioritātes nevar būt vairāk ierobežojošas nekā prioritātes, kas ir juridiskās personas līmenī.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Finanšu dimensijas](financial-dimensions.md)
- [Papildu kārtulu struktūru izveide un piešķiršana](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

