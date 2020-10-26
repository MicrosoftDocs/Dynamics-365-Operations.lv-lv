---
title: Eksperimenta priekšskatīšana un publicēšana
description: Šajā tēmā ir aprakstīts, kā priekšskatīt un publicēt eksperimentu no Dynamics 365 Commerce.
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930245"
---
# <a name="preview-and-publish-an-experiment"></a>Eksperimenta priekšskatīšana un publicēšana

Šajā tēmā ir aprakstīts, kā priekšskatīt un publicēt eksperimentu pakalpojumā Dynamics 365 Commerce pēc tam, kad esat [pievienojis eksperimentu un rediģējis variantus](experimentation-connect-edit.md). Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu darbības ir apskatītas atsevišķās tēmās.

[ ![Eksperimenta lietotāja maršruts – priekšskatīšana un publicēšana](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Eksperimenta variantu priekšskatīšana
Varat priekšskatīt variantus un turpināt to rediģēšanu, līdz tie izskatās tā, kā vēlaties.

1. Vietnes veidotājā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai atlasītu priekšskatāmo saturu. 
1. Augšējā joslā atlasiet **Priekšskatīt**. Tiek parādīts publicējamā satura priekšskatījums.
1. Lai priekšskatītu citu variantu, atlasiet to variantu nolaižamajā izvēlnē un vēlreiz atlasiet **Priekšskatīt**.

## <a name="publish-your-experiment"></a>Eksperimenta publicēšana
Ja neizmantojat publicēšanas grupu, lai ieplānotu eksperimenta sākumu, un vēlaties to publicēt nekavējoties, komandjoslā atlasiet **Publicēt**. Tiks publicēti visi eksperimentam piederošie varianti.
    
> [!IMPORTANT]
> Ja lapai ir nepublicēts URL, vispirms URL jāpublicē, pretējā gadījumā tas nebūs redzams tīmekļa vietnes lietotājiem. Papildinformāciju skatiet sadaļā [Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Publicēšanas grupu izmantošana, lai ieplānotu eksperimenta sākumu
Vietnes veidotājā izveidoto variantu publicēšana var tikt ieplānota, izmantojot publicēšanas grupu. Publicēšanas grupā, varat pievienot lapu vai fragmentu eksperimentam, dodoties uz cilni **Eksperimenti** vai uz cilnēm **Lapas** vai **Fragmenti**. Papildinformāciju skatiet tēmā [Eksperimenta pievienošana un variantu rediģēšana](experimentation-connect-edit.md). Informāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).

Izmantojot publicēšanas grupas ar eksperimentiem, ir jāņem vērā daži svarīgi apsvērumi.
- Kad publicēšanas grupai pievienojat lapu vai fragmentu, kurā tiek izpildīts eksperiments, publicēšanas grupā eksperiments tiks noņemts no lapas vai fragmenta.
- Eksperimenti, kas ir pievienoti lapām tiešsaistes vietnē, nav pieejami publicēšanas grupu lapām un otrādi. Līdzīgi lapas, kurās tiek izpildīti eksperimenti tiešsaistes vietnē, nav pieejamas citiem eksperimentiem publicēšanas grupās un otrādi.
- Kad publicējat vai ieplānojat publicēšanas grupu, tiek publicēts viss publicēšanas grupas saturs neatkarīgi no tā, vai ar publicēšanas grupu ir saistīts eksperiments.
- Tā kā publicēšanas grupa turpina pastāvēt pēc publicēšanas tiešsaistes vietnē, arī eksperimenti publicēšanas grupā saglabājas. Tāpēc nevarēsit saistīt citus eksperimentus ar to pašu lapu vai fragmentu. Lai izvairītos no šī ierobežojuma, dzēsiet visas publicēšanas grupas ar esošajiem eksperimentiem. Tāpat, ja vēlaties dzēst eksperimentu tiešsaistes vietnē, kas pastāv arī publicēšanas grupā, vispirms dzēsiet to no publicēšanas grupas.

## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta pievienošana un rediģēšana](experimentation-connect-edit.md)

## <a name="next-step"></a>Nākamā darbība
[Eksperimenta izpildīšana un pārraudzīšana](experimentation-run-monitor.md)
