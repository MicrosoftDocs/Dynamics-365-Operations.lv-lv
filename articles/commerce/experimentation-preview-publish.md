---
title: Eksperimenta priekšskatīšana un publicēšana
description: Šajā rakstā ir aprakstīts, kā priekšskatīt un publicēt eksperimentu no Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946146"
---
# <a name="preview-and-publish-an-experiment"></a>Eksperimenta priekšskatīšana un publicēšana

Šajā rakstā aprakstīts, kā priekšskatīt un publicēt jūsu eksperimentu Dynamics 365 Commerce pēc tam, kad esat pievienojis [savu eksperimentu un rediģējis variācijas](experimentation-connect-edit.md). Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce. Papildu soļi ir ietverti atsevišķos rakstos.

[ ![Eksperimenta lietotāja maršruts – priekšskatīšana un publicēšana.](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Eksperimenta variantu priekšskatīšana
Varat priekšskatīt variantus un turpināt to rediģēšanu, līdz tie izskatās tā, kā vēlaties.

Lai priekšskatītu eksperimenta variantus Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Zem komandjoslas esošajā variantu nolaižamajā izvēlnē atlasiet priekšskatāmo saturu. 
1. Komandjoslā atlasiet **Priekšskatīt**. Tiek parādīts publicējamā satura priekšskatījums.
1. Lai priekšskatītu citu variantu, atlasiet to variantu nolaižamajā izvēlnē un vēlreiz atlasiet **Priekšskatīt**.

## <a name="publish-your-experiment"></a>Eksperimenta publicēšana
Ja neizmantojat publicēšanas grupu, lai ieplānotu eksperimenta sākumu, un vēlaties to publicēt nekavējoties, komandjoslā atlasiet **Publicēt**. Tiks publicēti visi eksperimentam piederošie varianti.
    
> [!IMPORTANT]
> Ja lapai ir nepublicēts URL, vispirms URL jāpublicē, pretējā gadījumā tas nebūs redzams tīmekļa vietnes lietotājiem. Papildinformāciju skatiet sadaļā [Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Publicēšanas grupu izmantošana, lai ieplānotu eksperimenta sākumu
Vietnes veidotājā izveidoto variantu publicēšana var tikt ieplānota, izmantojot publicēšanas grupu. Publicētajā grupā varat pievienot lapu vai fragmentu savam eksperimentam, kreisajā navigācijas rūtī atlasot **Eksperimenti**. To var arī izdarīt, atlasot **Lapas** vai **Fragmenti** un izpildot instrukcijas sadaļā [Eksperimenta pievienošana un variantu rediģēšana](experimentation-connect-edit.md). Informāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).

Izmantojot publicēšanas grupas ar eksperimentiem, ir jāņem vērā daži svarīgi apsvērumi.
- Kad publicēšanas grupai pievienojat lapu vai fragmentu, kurā tiek izpildīts eksperiments, publicēšanas grupā eksperiments tiks noņemts no lapas vai fragmenta.
- Eksperimenti, kas ir pievienoti lapām tiešsaistes vietnē, nav pieejami publicēšanas grupu lapām un otrādi. Līdzīgi lapas, kurās tiek izpildīti eksperimenti tiešsaistes vietnē, nav pieejamas citiem eksperimentiem publicēšanas grupās un otrādi.
- Kad publicējat vai ieplānojat publicēšanas grupu, tiek publicēts viss publicēšanas grupas saturs neatkarīgi no tā, vai ar publicēšanas grupu ir saistīts eksperiments.
- Tā kā publicēšanas grupa turpina pastāvēt pēc publicēšanas tiešsaistes vietnē, arī eksperimenti publicēšanas grupā saglabājas. Tāpēc nevarēsit saistīt citus eksperimentus ar to pašu lapu vai fragmentu. Lai izvairītos no šī ierobežojuma, dzēsiet visas publicēšanas grupas ar esošajiem eksperimentiem. Tāpat, ja vēlaties dzēst eksperimentu tiešsaistes vietnē, kas pastāv arī publicēšanas grupā, vispirms dzēsiet to no publicēšanas grupas.

### <a name="force-variations-for-testing"></a>Uzsvīdiet variācijas testēšanai

Kad eksperiments notiek, varat pievienot eksperimenta ID un variācijas ID noklusējuma lapas URL, lai piestātu variāciju testēšanas vai automatizācijas nolūkiem. Piemēram, ja noklusējuma lapas URL ir `https://fabrikam.com/modern/homepage`, jūs varat uzstāsiet uzstāsiet kā URL variāciju `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464`. Varat iegūt eksperimenta ID un variācijas ID jūsu eksperimenta variācijai no priekšskatījuma URL iepriekš **izskaidrotā priekšskatījuma** pieredzes.

## <a name="previous-step"></a>Iepriekšējā darbība
[Eksperimenta pievienošana un rediģēšana](experimentation-connect-edit.md)

## <a name="next-step"></a>Nākamā darbība
[Eksperimenta veikšana un uzraudzība](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
