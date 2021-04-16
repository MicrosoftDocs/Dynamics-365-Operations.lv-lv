---
title: Eksperimenta iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt eksperimentu trešās puses pakalpojumos.
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
ms.openlocfilehash: 9976ca461f7e988c32b81565fa2d084709e5ad6e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792514"
---
# <a name="set-up-an-experiment"></a>Eksperimenta iestatīšana

Kad esat [definējis hipotēzi un noteicis, kādus panākumu rādītājus vēlaties izmantot](experimentation-identify.md), jums ir jāiestata eksperiments trešās puses pakalpojumā. Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu darbības ir apskatītas atsevišķās tēmās.

[ ![Eksperimenta lietotāja maršruts – iestatīšana](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Eksperimenta iestatīšana trešās puses pakalpojumā
Jums ir jāizvēlas trešās puses pakalpojums, lai varētu izpildīt un pārraudzīt jūsu eksperimentu un iestatīt eksperimenta savienotāju. Šie priekšnosacījumi ir uzskaitīti  [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).

Izpildiet nepieciešamās darbības, lai izveidotu eksperimentu trešās puses pakalpojumā. Ja savienotājs ir konfigurēts pareizi, pilns trešās puses pakalpojumā iestatīto eksperimentu saraksts tiks parādīts Commerce vietņu veidotājā apmēram 5 minūšu laikā.

## <a name="set-up-your-success-metrics"></a>Panākumu rādītāju iestatīšana
Katram eksperimentam ir nepieciešami rādītāji, lai noteiktu variantu ietekmi un pārbaudītu hipotēzi. Veiciet tālāk norādītās darbības, lai iespējotu rādītāju aprēķināšanu trešās puses pakalpojumā, izmantojot tiešsaistes telemetrijas notikumus no Dynamics 365 Commerce.

Lai iestatītu jūsu panākumu rādītājus, rīkojieties šādi.

1. Commerce vietņu veidotājā atlasiet **Lapas** kreisajā navigācijas rūtī un pēc tam atlasiet lapu, kuras rādītājus vēlaties apkopot. 
1. Dodieties uz sadaļu **Izsekojamie notikumu ID**, kas atrodas lapas labās puses rekvizītu rūtī vai modulī, kuru vēlaties izsekot.
1. Atlasiet **Skatīt**. Tiek parādīts visu notikumu ID saraksts. Kopējiet notikumu, kuram vēlaties sekot, un ielīmējiet notikuma atslēgu norādītajā vietā trešās puses pakalpojumā. Ja ir nepieciešams vairāk nekā viens notikums, kopējiet atslēgas pa vienai. 
    - Lai uzzinātu, kā skatīt visus pieejamos notikumus un atribūtus, ieskaitot lapu skatījumus un ieņēmumu izsekošanu, skatiet sadaļu [Commerce komponentu notikumi diagnostikai un problēmu novēršanai](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Citas darbības, lai izsekotu rādītājus, veiciet pēc nepieciešamības trešās puses pakalpojumā.

## <a name="previous-step"></a>Iepriekšējā darbība
[Hipotēzes identificēšana un eksperimenta rādītāju noteikšana](experimentation-identify.md) 


## <a name="next-step"></a>Nākamā darbība
[Eksperimenta pievienošana un rediģēšana](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]