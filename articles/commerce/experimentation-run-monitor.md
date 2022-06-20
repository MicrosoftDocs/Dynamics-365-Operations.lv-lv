---
title: Eksperimenta izpildīšana un pārraudzīšana
description: Šajā rakstā ir aprakstīts, kā palaist un uzraudzīt eksperimentu trešās puses pakalpojumā. Šeit ir aprakstīts arī, kā veikt izmaiņas variantiem pēc eksperimenta sākšanas.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909587"
---
# <a name="run-and-monitor-an-experiment"></a>Eksperimenta izpildīšana un pārraudzīšana

Šajā rakstā ir aprakstīts, kā palaist un uzraudzīt jūsu eksperimentu trešās puses programmā, kā arī, ja nepieciešams, mainīt variācijas. Pirms šī raksta darbību veikšanas vispirms ir jāpublicē savus eksperimentus [Commerce](experimentation-preview-publish.md). 

Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu soļi ir ietverti atsevišķos rakstos.

[ ![Eksperimenta lietotāja maršruts – izpildīšana un pārraudzīšana.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Pēc variantu publicēšanas, visas darbības, kas jāveic pakalpojumā Commerce, lai izpildītu eksperimentu, ir pabeigtas. Nākamā darbība ir noteikt, kādu variantu rādīt katram lietotājam, kad tie pieprasa lapu. To nosaka trešās puses pakalpojums, bet vispirms pakalpojumā ir jāaktivizē eksperiments. Tā kā eksperimenta aktivizēšanas darbības dažādos pakalpojumos atšķiras, jums ir jārīkojas saskaņā ar pakalpojuma vai nodrošinātāja instrukcijām. Ja eksperiments nav aktivizēts, lietotāji redzēs tikai lapas noklusējuma versiju (varianti netiks rādīti).

Lai apkopotu datus statistiski derīgiem rezultātiem, eksperiments ir jāveic pietiekami ilgu laiku. Izmantojiet trešās puses pakalpojumu, lai eksperimenta izpildes laikā pārraudzītu ar eksperimentu saistītos datus un analīzi.

## <a name="adjust-your-variations"></a>Variantu pielāgošana
Ja kāda iemesla dēļ ir nepieciešams veikt izmaiņas variantos, veiciet tālāk norādītās darbības.

> [!IMPORTANT]
> Ja veicat izmaiņas tiešsaistes eksperimentā pakalpojumā Commerce vai trešās puses pakalpojumā, rezultāti var tikt būtiski ietekmēti. Apsveriet iespēju eksperimentu izpildīt un pēc tam izveidot jaunu eksperimentu, ieviešot būtiskas izmaiņas.

1. Commerce vietņu veidotājā kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet eksperimentu. 
1. Nolaižamajā izvēlnē atlasiet variantu, kuru vēlaties atjaunināt.
1. Veiciet visas nepieciešamās izmaiņas un pēc tam priekšskatiet un publicējiet variantus. Papildinformāciju skatiet sadaļā [Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md).
1. Dodieties uz trešās puses pakalpojumu, lai veiktu jebkādas ar eksperimentu saistītas izmaiņas.
    
## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md)

## <a name="next-step"></a>Nākošā darbība
[Varianta publicēšana un eksperimenta pabeigšana](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]