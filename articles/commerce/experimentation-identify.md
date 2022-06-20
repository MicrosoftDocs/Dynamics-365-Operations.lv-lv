---
title: Hipotēzes identificēšana un eksperimenta rādītāju noteikšana
description: Šajā rakstā ir aprakstīts, kā identificēt parametrām un veiksmīgos rādītājus attiecībā uz eksperimentu, kurā darbināt e-Komercijas vietni Dynamics 365 Commerce.
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
ms.openlocfilehash: 0b6bdf160522fc93e841ec2f8a4542ff80d8f67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852790"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Hipotēzes identificēšana un eksperimenta panākumu rādītāju noteikšana
Pirmā eksperimenta dzīves cikla fāze ietver eksperimenta hipotēzes identificēšanu un rādītāju noteikšanu, kam sekosit, lai novērtētu panākumus. Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai [iestatītu un izpildītu eksperimentu](experimentation-overview.md) e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu soļi ir ietverti atsevišķos rakstos. 

[ ![Eksperimenta lietotāja maršruts – identificēšana.](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Hipotēze ir apgalvojums, kurā prognozēts eksperimenta rezultāts. Hipotēzes definēšanā ir iesaistīti daudzi faktori, piemēram, lietotāju uzvedības un apkopoto tīmekļa vietņu datu izpēte. Ar hipotēzi jūs definēsit pieņēmumu vai teoriju, kuru vēlaties apstiprināt ar savu eksperimentu. Eksperimenta hipotēzes piemērs varētu būt “*Vasaras mēnešos attēls ar baltas krāsas t-kreklu manā mājas lapā radīs lielāku vidējo klikšķu skaitu nekā tumši zils džemperis, jo vasarā cilvēki vēlas valkāt kaut ko plānu un gaišās krāsās.*” Šādā gadījumā jūs izveidosit variantus, kas ietver baltu t-kreklu un tumši zilu džemperi, un abus publicēsit vienlaicīgi.

Lai apstiprinātu hipotēzi, eksperimenta sekmībai vai nesekmībai jābūt tieši saistītai ar lietotāja darbībām, piemēram, vai tīmekļa vietnes lietotājs noklikšķina uz saites vai pogas. Šīm darbībām jāatbilst notikumiem, par kuriem tiks ziņots trešās puses pakalpojumam, kas seko eksperimentam. Laika gaitā to lietotāju procentuālais īpatsvars, kuri veic šo darbību, tiks aprēķināts kā rādītāji, ko varat izmantot, lai veidotu pārskatus un veiktu analīzes. Lai pārskatītu visus pieejamos notikumus un atribūtus, skatiet tēmu [Commerce komponentu notikumi diagnostikai un problēmu novēršanai](dev-itpro/retail-component-events-diagnostics-troubleshooting.md), .

## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Nākamā darbība
[Eksperimenta iestatīšana](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]