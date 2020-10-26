---
title: Eksperimenta pievienošana un variantu rediģēšana
description: Šajā tēmā ir aprakstīts, kā pievienot eksperimentu trešās puses pakalpojumam Dynamics 365 Commerce un kā rediģēt eksperimenta variantus.
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
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930246"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Eksperimenta pievienošana un variantu rediģēšana

Šajā tēmā ir aprakstīts, kā pievienot eksperimentu pakalpojumā Commerce un kā veikt izmaiņas variantiem, lai tie atbilstu hipotēzei. Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu darbības ir apskatītas atsevišķās tēmās.

[ ![Eksperimenta lietotāja maršruts – pievienošana un rediģēšana](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Pēc [eksperimenta iestatīšanas](experimentation-setup.md) trešās puses pakalpojumā, jūs pievienosit eksperimentu Dynamics 365 Commerce un rediģēsit eksperimenta variantus.

## <a name="planning-considerations"></a>Plānošanas apsvērumi

Pirms pievienojat eksperimentu pakalpojumā Commerce, jums ir jāpieņem daži lēmumi, kas ietekmē veidu, kādā Commerce pārvalda jūsu saturu.

### <a name="determine-the-scope-of-your-experiment"></a>Eksperimenta tvēruma noteikšana
Kad pievienojat eksperimentu, jums tiek piedāvāts definēt eksperimenta tvērumu. Eksperimenti ir definēti kā **daļēja** tvēruma vai **pilnīga** tvēruma.
- Izvēlieties **daļēja**, ja vēlaties veikt eksperimentu noteiktā lapas daļā. Atlasot šo opciju, ir jānosaka, kuri moduļi ir ietverti eksperimentā. Izmaiņas, kas tiek veiktas noklusējuma lapas vai fragmenta daļām, kas nav saistītas ar eksperimentu, tiek automātiski sinhronizētas starp variantiem.
- Izvēlieties **pilnīga**, ja vēlaties veikt eksperimentu visā lapā vai fragmentā. Tiek izveidotas atsevišķas noklusējuma lapas vai fragmenta kopijas. Nav nepieciešams atlasīt, kuri moduļi tiek ietverti eksperimentā, jo izmaiņām ir pieejama visa rediģēšanas virsma. Moduļus varat pievienot, dzēst un pārkārtot pēc nepieciešamības. Tomēr, ja tiek veiktas izmaiņas noklusējuma lapā vai fragmentā, ar kuru ir saistīts eksperiments, šīs izmaiņas ir manuāli jāsinhronizē visos variantos.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Saistot eksperimentu ar lapu, kurā tiek izmantots izkārtojums, eksperimenta tvērums var būt tikai **pilnīgs**.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Izlemiet, vai vēlaties ieplānot eksperimenta publicēšanu
Ja vēlaties ieplānot eksperimenta publicēšanu tiešsaistes vietnē, pārliecinieties, ka saturs, kuru vēlaties saistīt ar eksperimentu, ir pieejams publicēšanas grupā *pirms* eksperimenta pievienošanas. 

Papildinformāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).


## <a name="connect-your-experiment"></a>Eksperimenta pievienošana
Lai pievienotu eksperimentu, palaidiet vedni **Pievienot eksperimentu**. Vednis palīdz veikt nepieciešamās darbības, lai pievienotu eksperimentu. Pabeidzot vedni, jūsu eksperiments ir pievienots, un varianti ir izveidoti un gatavi rediģēšanai.

1. Lai palaistu vedni, atlasiet cilni **Eksperimenti** vietnes veidotājā un pēc tam atlasiet **Pievienot**. Vai arī vednim varat piekļūt no lapas vai fragmenta redaktora. Rediģēšanas režīmā komandjoslā atlasiet **Pievienot eksperimentu**.

> [!NOTE]
> Lapu var vienlaicīgi pievienot tikai vienam eksperimentam. Lai pievienotu lapu citam eksperimentam, vispirms dzēsiet eksperimentu, ar kuru lapa ir savienota pašlaik.

1. Izvēlieties lapu vai fragmentu, kurā vēlaties izpildīt eksperimentu.
1. Iestatiet eksperimenta tvērumu uz **daļēju** vai **pilnīgu**, pamatojoties uz izvēli, ko veicāt augstāk minētajā sadaļā [Eksperimenta tvēruma noteikšana](#determine-the-scope-of-your-experiment).
    > [!NOTE]
    > Lai eksperimentētu ar visu lapu vai fragmentu, ir jāiespējo līdzekļa karodziņš **Eksperimentēt ar lapām vai fragmentiem**. Papildinformāciju skatiet tēmā [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).
    
1. Vedņa pēdējā darbībā atlasiet **Ģenerēt variantus un iziet no vedņa**. Eksperimentam tiek izveidoti varianti. 

## <a name="edit-your-variations"></a>Variantu rediģēšana
Izejot no vedņa, tiek izveidoti varianti. 

Pēc tam jūs rediģēsiet variantus, lai tie atspoguļotu eksperimenta hipotēzes pārbaudāmās izvēles. Izvēlieties kādu no šīm procedūrām, kas atbilst eksperimenta tvērumam, ko izvēlējāties iepriekšējā sadaļā [Eksperimenta tvēruma noteikšana](#determine-the-scope-of-your-experiment).

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Variantu rediģēšana eksperimentiem ar daļēju tvērumu
Izpildiet šīs darbības, ja eksperimenta tvērumu definējāt kā **daļēju** vednī **Pievienot eksperimentu**.

1. Redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi. Varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.
1. Atlasiet moduli ar ko eksperimentēt, atlasot daudzpunktes (...) un pēc tam atlasot **Pievienot eksperimentam**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Variantu rediģēšana eksperimentiem ar pilnīgu tvērumu
Ja definējāt eksperimenta tvērumu kā **pilnīgu** vednī **Pievienot eksperimentu**, tad redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi. 

> [!NOTE]
> Jebkurā gadījumā varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.

## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta iestatīšana](experimentation-setup.md) 


## <a name="next-step"></a>Nākamā darbība
[Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md)
