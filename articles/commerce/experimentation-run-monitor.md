---
title: Eksperimenta izpildīšana un pārraudzīšana
description: Šajā tēmā ir aprakstīts, kā izpildīt un pārraudzīt eksperimentu trešās puses pakalpojumos. Šeit ir aprakstīts arī, kā veikt izmaiņas variantiem pēc eksperimenta sākšanas.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930243"
---
# <a name="run-and-monitor-an-experiment"></a>Eksperimenta izpildīšana un pārraudzīšana

Šajā tēmā ir aprakstīts, kā izpildīt un pārraudzīt eksperimentu trešās puses programmā, un veikt izmaiņas variantiem, ja tas nepieciešams. Pirms šajā tēmā norādīto darbību veikšanas jums vajadzēs [publicēt](experimentation-preview-publish.md) savu eksperimentu pakalpojumā Commerce. Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu darbības ir apskatītas atsevišķās tēmās.

[ ![Eksperimenta lietotāja maršruts – izpildīšana un pārraudzīšana](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Pēc variantu publicēšanas, visas darbības, kas jāveic pakalpojumā Commerce, lai izpildītu eksperimentu, ir pabeigtas. Nākamā darbība ir noteikt, kādu variantu rādīt katram lietotājam, kad tie pieprasa lapu. To nosaka trešās puses pakalpojums, bet vispirms pakalpojumā ir jāaktivizē eksperiments. Tā kā eksperimenta aktivizēšanas darbības dažādos pakalpojumos atšķiras, jums ir jārīkojas saskaņā ar pakalpojuma vai nodrošinātāja instrukcijām. Ja eksperiments nav aktivizēts, lietotāji redzēs tikai lapas noklusējuma versiju – varianti netiks rādīti.

Lai apkopotu datus statistiski derīgiem rezultātiem, eksperiments ir jāveic pietiekami ilgu laiku. Izmantojiet trešās puses pakalpojumu, lai eksperimenta izpildes laikā pārraudzītu ar eksperimentu saistītos datus un analīzi.

## <a name="adjust-your-variations"></a>Variantu pielāgošana
Ja kāda iemesla dēļ ir nepieciešams veikt izmaiņas variantos, veiciet tālāk norādītās darbības.

> [!IMPORTANT]
> Ja veicat izmaiņas tiešsaistes eksperimentā pakalpojumā Commerce vai trešās puses pakalpojumā, rezultāti var tikt būtiski ietekmēti. Apsveriet iespēju eksperimentu izpildīt un pēc tam izveidot jaunu eksperimentu, ieviešot būtiskas izmaiņas.

1. Dodieties uz **Eksperimenti** cilni vietnes veidotājā un atlasiet eksperimentu. 
1. Nolaižamajā izvēlnē atlasiet variantu, kuru vēlaties atjaunināt.
1. Veiciet nepieciešamās izmaiņas, pēc tam priekšskatiet un publicējiet variantus. Papildinformāciju skatiet sadaļā [Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md).
1. Dodieties uz trešās puses pakalpojumu, lai veiktu jebkādas ar eksperimentu saistītas izmaiņas.
    
## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md)

## <a name="next-step"></a>Nākošā darbība
[Varianta publicēšana un eksperimenta pabeigšana](experimentation-review-complete.md)
