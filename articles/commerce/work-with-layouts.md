---
title: Darbs ar iepriekš iestatītiem izkārtojumiem
description: Šajā rakstā ir aprakstīts, kā strādāt ar izveidotiem izkārtojumiem Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: b588df5702657f07e1e790ffba39d2e459901557
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286281"
---
# <a name="work-with-preset-layouts"></a>Darbs ar iepriekš iestatītiem izkārtojumiem

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā strādāt ar izveidotiem izkārtojumiem Microsoft Dynamics 365 Commerce.

Pirms šī raksta procedūru izpildīšanas noteikti izlasiet Iepriekš [iestatītos un pielāgotos izkārtojumus](templates-layouts-overview.md#preset-and-custom-layouts). Vispārīgam pārskatam skatiet sadaļu [Veidnes un izkārtojumu pārskats](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Jauna iepriekš iestatīta izkārtojuma izveide

Iepriekš iestatīta izkārtojuma izveidošanai ir pieejamas divas metodes. Varat saglabāt esošu pielāgotu izkārtojumu kā jaunu iepriekš iestatītu izkārtojumu vai arī izveidot iepriekš iestatītu izkārtojumu no jauna.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Iepriekš iestatīta izkārtojuma izveidošana no esoša pielāgota izkārtojuma

Lai izveidotu iepriekš iestatītu izkārtojumu no esoša pielāgota izkārtojuma, veiciet tālāk norādītās darbības.

1. Atveriet esošu lapu, kas pašlaik neizmanto iepriekš iestatītu izkārtojumu un kurai ir moduļa struktūra, ko vēlaties atkārtoti izmantot citām jūsu vietnes lapām.
1. Atlasiet **Rediģēt**, lai paņemtu lapu.
1. Atlasiet **Saglabāt kā jaunu izkārtojumu**. Tiek parādīts dialoglodziņš **Saglabāt kā jaunu izkārtojumu**.
1. Ievadiet iepriekš iestatītā izkārtojuma nosaukumu un aprakstu. Vērtības, ko ievadāt, tiks rādītas citiem autoriem, kad tie izveido jaunas lapas no jūsu izkārtojuma vai pārslēdzas uz to. Tāpēc ievadiet vērtības, kas noderēs lapu autoriem.
1. Atlasiet **Labi**.

Iepriekš iestatītais izkārtojums tagad būs pieejams, veidojot jaunas lapas vai arī izvēloties citu izkārtojumu lapai tajā pašā veidnes hierarhijā.

> [!TIP]
> Lai ātri apskatītu, vai konkrēta lapa pašlaik ir saistīta ar iepriekš iestatītu izkārtojumu, atlasiet lapu no lapu saraksta skata un pārbaudiet izkārtojuma metadatus rekvizītu rūtī labajā pusē.

### <a name="create-a-new-preset-layout"></a>Jauna iepriekš iestatīta izkārtojuma izveide

Lai izveidotu iepriekš iestatītu izkārtojumu no jauna, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī kreisajā pusē atlasiet **Izkārtojumi**.
1. Atlasiet **Jauns izkārtojums**. Tiek parādīts dialoglodziņš **Jauns izkārtojums**.
1. Atlasiet veidni, ko izmantot iepriekš iestatītajam izkārtojumam.
1. Ievadiet iepriekš iestatītā izkārtojuma nosaukumu un aprakstu. Vērtības, ko ievadāt, tiks rādītas citiem autoriem, kad tie izveido jaunas lapas no jūsu izkārtojuma vai pārslēdzas uz to. Tāpēc ievadiet vērtības, kas noderēs lapu autoriem.
1. Atlasiet **Labi**, lai izveidotu jaunu iepriekš iestatīto izkārtojumu un atvērtu izkārtojuma redaktoru.
1. Izkārtojuma redaktorā pievienojiet un konfigurējiet moduļus, izmantojot struktūras koku kreisajā pusē un rekvizītu rūti labajā pusē. (Šis process ir līdzīgs moduļu pievienošanas un konfigurēšanas procesam veidnes redaktorā.) Moduļu izkārtojums un visi bloķētie noklusējuma iestatījumi kļūst par centralizētu moduļa konfigurāciju visām lapām, kurās tiek izmantots šis iepriekš iestatītais izkārtojums.

## <a name="modify-a-preset-layout"></a>Iepriekš iestatīta izkārtojuma modificēšana

Lai modificētu iepriekš iestatītu izkārtojumu, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī kreisajā pusē atlasiet **Izkārtojumi**.
1. Izkārtojuma redaktorā struktūras kokā pa kreisi atlasiet moduli, ko modificēt. Pēc tam izpildiet jebkuru no norādītajām darbībām.

    - Lai moduli pārvietotu uz augšu vai uz leju, atlasiet daudzpunktes pogu (**...**) modulim un pēc tam atlasiet **Pārvietot uz augšu** vai **Pārvietot uz leju**.
    - Lai mainītu moduļa noklusējuma iestatījumus, izmantojiet rekvizītu rūti, lai ievadītu noklusējuma vērtības un pēc izvēles bloķētu tās visām pakārtotajām lapām.
    - Lai pievienotu jaunus moduļus vai fragmentus konteineru moduļiem, atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli** vai **Pievienot fragmentu**.
    - Lai moduli noņemtu no izkārtojuma, atlasiet daudzpunktes pogu un pēc tam atlasiet **Dzēst**.

## <a name="change-a-preset-layout-theme"></a>Iepriekš iestatīta izkārtojuma dizaina maiņa

Parasta prakse ir iestatīt noklusējuma dizainu visām lappusēm, kas izmanto iepriekš iestatītu izkārtojumu.

Lai iestatītu vai mainītu dizainu visām pakārtotajām lapām, kas izmanto jūsu iepriekš iestatīto izkārtojumu, veiciet šādas darbības.

1. Izkārtojuma redaktorā struktūras kokā pa kreisi atlasiet lapas konteinera moduli. (Parasti šis modulis ir otrais mezgls un ir nosaukts **Noklusējuma lapu**.)
1. **Rekvizītu** rūts laukā Tēma labajā pusē atlasiet tēmu.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Saglabājiet, atdodiet, priekšskatiet un publicējiet iepriekš iestatīto izkārtojumu

Lai saglabātu un atdotu iepriekš iestatīto izkārtojumu, izpildiet tālāk aprakstītās darbības.

1. Izkārtojuma redaktora augšā atlasiet **Saglabāt**. Saglabātās izmaiņas neietekmē lejupstraumes lapas, kamēr tās nav atdotas.
1. Atlasiet **Beigt rediģēšanu**. Jūsu veiktās izmaiņas tagad ir redzamas lejupstraumes darbplūsmām.

Lai priekšskatītu izmaiņas, vai nu atveriet esošu lapu, kas izmanto iepriekš iestatīto izkārtojumu, vai izveidojiet jaunu lapu no šī izkārtojuma.

Pēc tam, kad iepriekš iestatītā izkārtojuma izmaiņas ir priekšskatītas, veiciet vienu no tālāk norādītajām darbībām, lai publicētu izkārtojumu jūsu tiešsaistes vietnē.

1. Dodieties uz **Izkārtojumi**, atlasiet izkārtojumu un pēc tam atlasiet **Publicēt**.
1. Atlasiet izkārtojuma nosaukumu, lai atvērtu izkārtojuma redaktoru, un tad atlasiet **Publlicēt**.
1. Publicējiet lapu, kurā ir atsauce uz nepublicēto izkārtojumu. Izkārtojums tiks automātiski publicēts.

> [!WARNING]
> Uz iepriekš iestatītajiem izkārtojumiem var atsaukties vairākas lapas. Publicējot iepriekš iestatītu izkārtojumu, ņemiet vērā, ka var tikt ietekmēts vairāku lappušu izkārtojums.

## <a name="rename-a-preset-layout"></a>Izveidot iepriekš iestatīta izkārtojuma pārdēvēšanu

Lai vietas veidotājā pārdēvētu izveidoto izkārtojumu, veiciet šādus soļus.

1. Kreisajā navigācijas rūtī atlasiet **Izkārtojumi**.
1. Atlasiet izkārtojuma nosaukumu izkārtojumam, ko vēlaties pārdēvēt.
1. Atlasiet **Labot,** lai sāktu izkārtojuma rediģēšanu.
1. Izkārtojuma rekvizītu rūtī atlasiet pildspalvas simbolu blakus izkārtojuma nosaukumam.
1. Ja nepieciešams, labojiet izkārtojuma nosaukumu.
1. Atzīmējiet izvēles rūtiņu, lai apstiprinātu nosaukuma maiņu.
1. Atlasiet **Beigt rediģēšanu**.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Darbs ar veidnēm](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
