---
title: Eksperimenta pievienošana un variantu rediģēšana
description: Šajā rakstā ir aprakstīts, kā savienot eksperimentu trešās puses pakalpojumā Dynamics 365 Commerce un kā rediģēt eksperimenta variācijas.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942826"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Eksperimenta pievienošana un variantu rediģēšana

Šajā rakstā ir aprakstīts, kā savienot jūsu eksperimentu Commerce un izdarīt izmaiņas jūsu variācijās, lai tās saskaņotu ar jūsu anulēšanas metodi. 

Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu soļi ir ietverti atsevišķos rakstos.

[ ![Eksperimenta lietotāja maršruts – pievienošana un rediģēšana.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Pēc [eksperimenta iestatīšanas](experimentation-setup.md) trešās puses pakalpojumā, jūs pievienosit eksperimentu Dynamics 365 Commerce un rediģēsit eksperimenta variantus.

## <a name="connect-your-experiment"></a>Eksperimenta pievienošana
Lai pievienotu eksperimentu, palaidiet vedni **Pievienot eksperimentu**. Vednis palīdz veikt nepieciešamās darbības, lai pievienotu eksperimentu. Pabeidzot vedni, jūsu eksperiments ir pievienots, un varianti ir izveidoti un gatavi rediģēšanai.

Lai sāktu eksperimenta savienošanu Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Lai palaistu vedni **Savienot eksperimentu**, kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet **Savienot**. Vai arī varam vednim piekļūt no lapas vai fragmentu redaktora, rediģējot to un komandjoslā atlasot **Savienot eksperimentu**.

    > [!NOTE]
    > - Lapu var vienlaicīgi pievienot tikai vienam eksperimentam. Lai pievienotu lapu citam eksperimentam, vispirms dzēsiet eksperimentu, ar kuru lapa ir savienota pašlaik.
    > - Eksperimentu var veikt tikai lapās ar pielāgotu izkārtojumu. Ja jūsu lapai ir iepriekš iestatīts izkārtojums, vispirms pārveidojiet to par pielāgotu izkārtojumu. To var darīt, došanās uz lapu un atlasot **Pārvērst uz pielāgotu** izkārtojumu komandjoslā. Papildinformāciju par izkārtojumiem skatiet sadaļā [Izveidotie un pielāgotie izkārtojumi](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Ja savienosieties ar eksperimentu **no** cilnes Eksperimenti navigācijas rūtī kreisajā pusē, no parādītā saraksta atlasiet eksperimenta nosaukumu.
1. Atlasiet lapu vai fragmentu, uz kā vēlaties veikt eksperimentu.
1. Vedņa pēdējā darbībā atlasiet **Ģenerēt variantus un iziet no vedņa**. Eksperimentam tiek izveidoti varianti. 

> [!NOTE]
> Ja vēlaties ieplānot eksperimenta publicēšanu tiešsaistes vietnē, pārliecinieties, ka saturs, kuru vēlaties saistīt ar eksperimentu, ir pieejams publicēšanas grupā *pirms* eksperimenta pievienošanas. Papildinformāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).

## <a name="edit-your-variations"></a>Variantu rediģēšana

Kad izejat no ceļveža **Savienot** eksperimentu, variācijas tiek izveidotas jums. Izpildiet tālāk aprakstītās darbības, lai labotu variācijas un parādītu izvēles, kas nepieciešamas pārbaudei eksperimentā.

1. Redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi. Varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.
1. Atlasiet moduli ar ko eksperimentēt, atlasot daudzpunktes (...) un pēc tam atlasot **Pievienot eksperimentam**.

> [!NOTE]
> Apsveriet iespēju izveidot kontroles vai pamata variācijas, nemainot vienu no variācijām.

## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta iestatīšana](experimentation-setup.md) 


## <a name="next-step"></a>Nākamā darbība
[Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
