---
title: Iepakošanas darbs izejošo konteineru iepakošanai un sūtījumu apstrādei
description: Šajā rakstā ir aprakstīts darba pasūtījuma veids "Iepakošana", kas pārvalda iepakošanas konteineru darbu un atbalsta iepakotu konteineru daļējus sūtījumus, kas ir saistīti ar kravām, kuru krājumu krājumi paliek atpakoti.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220747"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Iepakošanas darbs izejošo konteineru iepakošanai un sūtījumu apstrādei

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts *iepakojuma* darba pasūtījuma veids, kas pārvalda iepakošanas konteineru darbu un atbalsta daļējus iepakotu konteineru sūtījumus, kas ir saistīti ar kravām, kuru krājumu krājumi paliek atpakoti. Iepakošanas darbs ļauj izmantot apstiprināšanas [un pārsūtīšanas](confirm-and-transfer.md) funkcionalitāti, lai apstiprinātu izejošos sūtījumus, kas ir saistīti ar konteineriem.

Iepakošanas darbs tiek izveidots automātiski, kad krājumi, kas ir saistīti ar pirmdokumenta darbu, tiek novietoti novietojumos ar *iepakojuma novietojuma* veidu. Darbs sastāv no divām rindām: *·* *viena* izdošanas un viena izvietošanas gadījumā un automātiski tiek uzturēta kā daļa no konteinera slēgšanas/atvēršanas procesa.

Papildinformāciju par to, kā iestatīt un izmantot konteinera iepakošanas procesu, skatiet sadaļā [Iepakošanas konteineri nosūtīšanai](packing-containers.md).

## <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

Ja sistēmā vēl nav ietverti šajā rakstā aprakstītie līdzekļi, [pārejiet](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) uz sadaļu Līdzekļu pārvaldība un nākamajā secībā slēdziet tālāk norādītos līdzekļus. Abas funkcijas ir noliktavas pārvaldības **moduļa** daļa.

1. *Apstiprināt un pārsūtīt*
1. *Iepakošanas darbs pakošanas stacijām*

## <a name="set-up-a-location-for-packing-work"></a>Iestatīt iepakošanas darba novietojumu

Lai iestatītu iepakošanas vietas, izmantojiet tālāk norādītās darbības. Katrai atrašanās vietai varat atlasīt, vai sistēma automātiski izveido iepakošanas darbu.

1. Pārejiet uz **noliktavas pārvaldības iestatīšanas \> iepakošanas \>\> iepakošanas stacijas iestatīšanu**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** iepakošanas stacijas iestatīšanas ierakstu.
1. Jaunajā ierakstā iestatiet sekojošos laukus:

    - **Noliktava** – atlasiet vai ievadiet noliktavu, kur atrodas iepakojuma vieta.
    - **Atrašanās** vieta – atlasiet vai ievadiet iepakojuma atrašanās vietu. Šī atrašanās vieta ir jāpiešķir novietojuma profilam, **kas izmanto atrašanās vietas tipu, kas ir konfigurēts kā jūsu uzņēmuma iepakošanas novietojuma veids lapā Noliktavas pārvaldības parametri**. Papildinformāciju skatiet pakotņu [konteineros nosūtīšanai](packing-containers.md).
    - **Iepakošanas darba** izveide — atzīmējiet šo izvēles rūtiņu, lai izveidotu iepakošanas darbu katru reizi, kad krājumi tiek piegādāti iepakojuma vietā. Darbs ietvers saites uz saistītajām kravas rindām, lai daļējās kravas varētu iepakot un nosūtīt.

## <a name="example-scenario"></a>Piemērs

Šajā piemērā scenārijā ir parādīts, kā apstrādāt izejošo pārdošanas pasūtījumu plūsmu, iepakojot konteineru un nosūtot daļēju noslodzi.

### <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/fin-ops/get-started/demo-data.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

Šo scenāriju var izmantot arī kā ieteikumus par iespējas izmantošanu ražošanas sistēmā. Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības katram iestatījumam, kas šeit aprakstīts.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Konfigurēt iepakošanas darbu noliktavas iepakošanas novietojumam

Lai sāktu, ir jākonfigurē iepakošanas *darba* process noteiktai noliktavai un vietai.

1. Pārejiet uz **noliktavas pārvaldības iestatīšanas \> iepakošanas \>\> iepakošanas stacijas iestatīšanu**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** iestatīšanas ierakstu.
1. Jaunajā ierakstā iestatiet šādas vērtības:

    - **Noliktava:** *62*
    - **Atrašanās vieta:** *Pakotne*
    - **Izveidot iepakošanas darbu:** *Jā*

1. Aizveriet iepakošanas **stacijas iestatīšanas** lapu.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Izveidot kravas veidni, kas ļauj veikt daļēju nosūtīšanu

Lai ļautu piegādāt kravu, izmantojot vairākus sūtījumus, jums tā ir jāsaista ar kravas veidni, kas ļauj piegādāt pa daļējām kravām. Sekojiet šiem soļiem, lai izveidotu nepieciešamo veidni.

1. Doties uz **Noliktavas pārvaldība \> Iestatīšana \> Krava \> Kravas veidnes**.
1. Darbību rūtī atlasiet Jauns, lai **pievienotu** iestatīšanas ierakstu.
1. Jaunajā ierakstā iestatiet šādas vērtības:

    - **Kravas veidnes ID: daļējs** *·*
    - **Atļaut kravas sadali nosūtīšanas apstiprināšanas laikā:** *Jā*

1. Aizveriet lapu **Kravas** veidnes.

Papildinformāciju skatiet sadaļā Apstiprināt [un pārsūtīt](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Pārdošanas pasūtījuma apstrāde

Izpildiet šīs darbības, lai apstrādātu pārdošanas pasūtījumu un daļēji to sūtītu.

1. Pabeidziet [piemēra scenāriju](packing-containers.md#scenario), kas ir paredzēts [kravas pakotņu konteineros](packing-containers.md). Šī scenārija laikā jums būs jāizveido pārdošanas pasūtījums diviem viena krājuma gabaliem. Pēc tam vienu no gabaliem iepakosiet konteinerā un aizvērsiet. Jāizveido piezīme par izveidoto kravas ID, kā norādīts scenārijā.
1. Dodieties uz **Noliktavas pārvaldība \> Darbs\> Viss darbs**.
1. Filtra apgabalā atzīmējiet izvēles rūtiņu **Rādīt slēgto** darbu. Pēc tam ievadiet sūtījuma ID laukā **Filtrs** un atlasiet filtrēt pēc Sūtījuma **ID** vērtības. Tagad vajadzētu redzēt trīs darbu virsrakstus. Viens ir pārdošanas pasūtījuma izdošanas darbam un tam ir statuss *Slēgts*. Divas ir paredzēts iepakošanas procesam: *viena* ir saistīta ar slēgto konteineru un tās statuss ir Slēgts, otra ir saistīta ar atpakoto atlikušo krājumu un *tās statuss ir Atvērts*.
1. Atlasiet kravas **ID vērtību** jebkuram darba virsrakstam, lai atvērtu kravas **detalizētas informācijas** lapu par kravu.
1. Pārejiet uz skatu **Galvene**.
1. Kopsavilkuma cilnē **Vispārīgi** atlasiet pogu Rediģēt **kravas** veidnes **ID** laukam. Pēc tam atlasiet daļējas nosūtīšanas kravas veidni, kuru izveidojāt šim scenārijam (daļējs *·*).
1. Darbību rūts cilnē Nosūtīt **un saņemt**, kas atrodas grupas **Apstiprināt**, atlasiet Izejošais **sūtījums**.
1. Dialoglodziņā Nosūtīšanas **apstiprināšana** atlasiet opciju Sadalīt **daudzumu jaunai noslodzei**.
1. Atlasiet **Labi**.

Tagad jūs esat nosūtīts vienu konteineru, kas ir saistīts ar sākotnējo noslodzi, un sistēma ir izveidojusi jaunu noslodzi atlikušajiem krājumiem, kas joprojām ir jāiepako konteineros.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
