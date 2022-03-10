---
title: Varianta publicēšana un eksperimenta pabeigšana
description: Šajā tēmā ir aprakstīts, kā publicēt veiksmīgu variantu un pabeigt eksperimentu Dynamics 365 Commerce.
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
ms.openlocfilehash: 48d66e84ce52e77e83843853e3d528f9394a7676cadc4a4be5198065696dd10e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738750"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Varianta publicēšana un eksperimenta pabeigšana

Šajā tēmā ir aprakstīts, kā publicēt variantu, kas sniedza labākos rezultātus eksperimentā un kā pabeigt eksperimentu. Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu darbības ir apskatītas atsevišķās tēmās.

[ ![Eksperimenta lietotāja maršruts - pārskatīšana un pabeigšana.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Pēc tam, kad [eksperiments ir izpildīts](experimentation-run-monitor.md) un ir apkopoti pietiekami daudz datu, lai noteiktu, kuru variantu vēlaties izmantot savā tiešsaistes vietnē, jūs publicēsit variantu un beigsit eksperimentu.

## <a name="promote-a-variation"></a>Varianta publicēšana
Izmantojiet datus un analīzi, kas saistīta ar trešās puses pakalpojuma eksperimentu, lai izlemtu, kurš no variantiem sniedza vislabākos rezultātus. Pēc tam varat to reklamēt, aizvietokot pašreizējo saturu tiešsaistes vietnē ar labāko variantu tā, lai tas būtu pieejams visiem tīmekļa vietnes lietotājiem.

Lai reklamētu labāko variantu, veiciet tālāk norādītās darbības. 

1. Commerce vietņu veidotājā kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet eksperimentu.
1. Komandjoslā atlasiet **Pabeigt eksperimentu**.
1. Dialoglodziņā **Pabeigt eksperimentu** atlasiet **Pārskatīt eksperimenta datus**. Tiek atvērts trešās puses pakalpojums, kur varat validēt rādītājus un noteikt, kurš no variantiem ir vislabākais.
1. Dialoglodziņā **Pabeigt eksperimentu** atlasiet labāko variantu un pēc tam atlasiet **Tālāk**.
1. Atveriet trešās puses pakalpojumu un beidziet eksperimentu.
1. Vietnes veidotājā atlasiet **Pabeigt**, lai pārrakstītu sākotnējo tiešsaistes lapu, un publicētu labāko variantu, lai tas būtu pieejams visiem tīmekļa vietnes lietotājiem. 

> [!NOTE]
> Ja izvēlaties saglabāt pašreizējo tiešsaistes lapu un nepublicēt variantu, atlasiet **Pārpublicēt sākotnējo lapu**.

## <a name="delete-your-experiment"></a>Eksperimenta dzēšana
Lai gan pakalpojumā Commerce nav nepieciešams dzēst pabeigtu eksperimentu, varat izvēlēties to dzēst, lai ietaupītu vietu vai iztīrītu darbvietu. 

Lai dzēstu eksperimentu Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.

1. Kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet eksperimentu. 
    > [!NOTE]
    > Ja eksperiments joprojām ir aktīvs, pirms turpināt, beidziet eksperimentu trešās puses pakalpojumā.
1. Komandjoslā atlasiet **Nepublicēt**, lai noņemtu varianta saturu no tiešsaistes vietnes.
1. Atlasiet **Dzēst**, lai dzēstu eksperimentu.

## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta veikšana un uzraudzība](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]