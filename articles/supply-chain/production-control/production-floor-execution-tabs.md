---
title: Ražošanas izpildes interfeisa izstrādāšana
description: Šajā tēmā ir aprakstīts, kā izstrādāt lietotāja interfeisa saturu katrai konfigurācijai.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664276"
---
# <a name="design-the-production-floor-execution-interface"></a>Ražošanas izpildes interfeisa izstrādāšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jūs varat izstrādāt lietotāja interfeisa saturu katrai konfigurācijai, ko izmanto ražošanas līmeņa izpildes interfeiss. Piemēram, darbiniekiem vienā darba šūnā, iespējams, ir jāspēj atvērt darba instrukcijas ražošanas līmenī, bet citā darba šūnā instrukcijas nav nepieciešamas. Šādā gadījumā ir jāizveido divas konfigurācijas, viena ar pogu dokumenta pielikumu atvēršanai un viena bez šīs pogas.

## <a name="design-a-tab"></a>Izveidot cilni

Lapā **Ražošanas līmeņa izpildes konfigurēšana** varat izveidot un konfigurēt cilnes, darbību rūtī atlasot **Izveidot cilnes**.

Katra cilne ir sadalīta četrās sadaļās, kā parādīts sekojošajā ilustrācijā.

![Cilnes izkārtojums](media/pfe-tab-layout.png "Cilnes izkārtojums")

Attēlā redzami šādi elementi:

1. Primārā rīkjosla
1. Sekundārā rīkjosla
1. Galvenais skats
1. Detalizēts skats

Lai izveidotu un konfigurētu jaunu cilni, veiciet tālāk norādītās darbības:

1. Dodieties uz **Ražošanas kontrole &gt; Uzstādīšana &gt; Ražošanas izpilde**.

1. Darbību rūtī atlasiet **Izveidot cilnes**, lai atvērtu lapu **Izveidot cilnes**.

    ![Izveidot cilnes lapa](media/pfe-design-tabs.png "Izveidot cilnes lapa")

1. Atlasiet **Jauns** darbību rūtī.

1. Lapas virsrakstā veiciet tālāk norādītos iestatījumus:

    - **Cilnes nosaukums** - norādiet cilnes nosaukumu.
    - **Galvenais skats** – atlasiet starp diviem iepriekš definētiem darbu sarakstiem (*Aktīvie darbi* vai *Visi darbi*).
    - **Detalizētas informācijas skats** - izvēlieties starp tukšu vērtību vai **Darba detalizēta informācija**. Ja atlasīsit tukšu vērtību, nebūs detalizēta skatījuma cilnē. Ja izvēlaties **Darba detalizētu informāciju**, detalizētajā skatījumā būs detalizēts darba apraksts, kas atlasīts darbu sarakstā galvenajā skatā.

1. **Primārās rīkjoslas** sadaļā Izvēlieties, kurām pogām jābūt pieejamām primārajā rīkjoslā. Kolonnā **Pieejamās darbības** redzams saraksts ar visām pogām, kuras var pievienot. Kolonnas **Atlasītās darbības** rāda visu to pogu saraksts, kas iekļautas pašreizējā konfigurācijā. Izmantojiet pogas starp kolonnām, lai atlasītos vienumus pārvietotu starp kolonnām pēc nepieciešamības. Izmantojiet pogas augšup un lejup blakus kolonnai **Atlasītās darbībās**, lai kontrolētu secību, kādā pogas tiek rādītas lietotāja interfeisā.

1. **Sekundārās** **rīkjoslas** sadaļā izvēlieties, kurām pogām jābūt pieejamām sekundārajā rīkjoslā. Kolonnā **Pieejamās darbības** redzams saraksts ar visām pogām, kuras var pievienot. Kolonnas **Atlasītās darbības** rāda visu to pogu saraksts, kas iekļautas pašreizējā konfigurācijā. Izmantojiet pogas starp kolonnām, lai atlasītos vienumus pārvietotu starp kolonnām pēc nepieciešamības. Izmantojiet pogas augšup un lejup blakus kolonnai **Atlasītās darbībās**, lai kontrolētu secību, kādā pogas tiek rādītas lietotāja interfeisā.

## <a name="associate-a-tab-with-a-configuration"></a>Cilnes saistīšana ar konfigurāciju

Pēc tam, kad visas cilnes ir izveidotas, tās var saistīt ar konfigurāciju.

1. Dodieties uz **Ražošanas kontrole &gt; Uzstādīšana &gt; Konfigurēt ražošanas līmeņa izpildi**.

    ![Konfigurēt ražošanas līmeņa izpildi](media/pfe-config-prod-floor-execution.png "Konfigurēt ražošanas līmeņa izpildi")

1. Kopsavilkuma cilnē **Cilnes atlase** atlasiet **Pievienot**.

1. Režģim tiek pievienota jauna rinda. Šai jaunajai rindai atlasiet cilnes nosaukumu, kuru vēlaties pievienot konfigurācijai.

1. Turpiniet pievienot papildu cilnes pēc nepieciešamības.

1. Izmantojiet rīkjoslas pogu **Pārvietot uz augšu** un **Pārvietot uz leju**, lai pēc nepieciešamības kārtotu cilnes. Cilnes tiks rādītas no kreisās uz labo tādā secībā, kā norādīts iepriekš attēlā (cilne virspusē tiek rādīta kreisajā pusē).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]