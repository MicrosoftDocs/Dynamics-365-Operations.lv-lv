---
title: Uzturēšanas speciālisti un speciālistu grupas
description: Šajā tēmā ir pakaidroti uzturēšanas speciālisti un speciālistu grupas Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e976a28349a4bc7a371d23eb4df724e0ffd36a0553aec2deeb2ff07d0a63579
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750128"
---
# <a name="maintenance-workers-and-worker-groups"></a>Uzturēšanas speciālisti un speciālistu grupas

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir pakaidroti uzturēšanas speciālisti un speciālistu grupas Līdzekļu pārvaldībā. Pamatlīdzekļu pārvaldībā varat pievienot uzturēšanas speciālistus funkcionālajiem novietojumiem. (Papildinformāciju par funkcionālajiem novietojumiem skatiet nodaļā [Funkcionālo novietojumu izveide](../functional-locations/create-functional-locations.md).) Šī funkcionalitāte var būt noderīga, ja, piemēram, plānojat uzturēšanas darbu iekārtā, kas atrodas funkcionālajā novietojumā 01, un jūs vēlaties piešķirt uzturēšanas speciālistus no tās pašas atrašanās vietas darba izpildei.

Varat arī izveidot uzturēšanas speciālistu grupas un saistīt uzturēšanas speciālistus ar tām. Šī funkcionalitāte noder, ja veicat vienkāršu darba pasūtījumu plānošanu un vēlaties ieplānot uzturēšanas speciālistu grupu darba pasūtījumā. Varat izmantot uzturēšanas speciālistus un uzturēšanas speciālistu grupas, lai iestatītu vēlamos uzturēšanas speciālistus un atbildīgos uzturēšanas speciālistus. 


## <a name="create-workers"></a>Izveidot nodarbinātos

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Nodarbinātie** \> **Nodarbinātie**.
2. Atlasiet **Jauns**, lai pievienotu nodarbināto sarakstam.
3. Laukā **Nodarbinātais** atlasiet nodarbināto.
4. Iestatiet opciju **Aktīvs** uz **Jā**, lai nodarbinātajam ieplānotu darba pasūtījumus.

    Kopsavilkuma cilnē **Vispārīgi** lauki **Resursi** un **Apraksts** tiek automātiski aizpildīti, ja nodarbinātajam ir atlasīts resurss. Lauks **Kalendārs** arī tiek aizpildīts automātiski, ja esat iestatījis nodarbināto kā resursu un piešķīris kalendāru šim resursam lapā **Resursi** (**Organizācijas administrēšana** \> **Resursi** \> **Resursi**).

5. Kopsavilkuma cilnē **Grupas** atlasiet **Pievienot** un pēc tam nodarbinātajam atlasiet uzturēšanas speciālistu grupu. Nodarbinātais var būt saistīts ar vairāk nekā vienu grupu.
6. Standarta iestatījumā nodarbinātā piederība grupai ir spēkā no datuma, kad pievienojat grupu, un tā nekad nebeidzas. Šis datums tiek rādīts laukā **Ir spēkā**. Lai skatītu lauku **Ir spēkā**, atlasiet **Skatīt** \> **Visu**. Ja nodarbinātā piederība grupai jāierobežo līdz noteiktam periodam, tā definēšanai izmantojiet laukus **Ir spēkā** un **Beigu termiņš**.
7. Kopsavilkuma cilnē **Funkcionālais novietojums** atlasiet **Pievienot** un pēc tam uzturēšanas speciālistam atlasiet funkcionālo novietojumu. Norādiet arī, kura atrašanās vieta ir nodarbinātā primārais funkcionālais novietojums.

    > [!NOTE]
    > Ja nodarbinātajam pievienojat funkcionālos novietojumus, visi aktīvie līdzekļi, kas ir saistīti ar šiem funkcionālajiem novietojumiem, tiek parādīti dažādos izvēlnes vienumos, piemēram **Mani aktīvie līdzekļi** un **Mani aktīvie funkcionālie novietojumi**. Tie ir redzami arī līdzekļa uzmeklēšanas sarakstos, kas tiek parādīti, veidojot jaunu līdzekli, uzturēšanas pieprasījumu vai darba pasūtījumu.

    Kopsavilkuma cilnes **Detalizēta informācija** lauki rāda to uzturēšanas speciālistu grupu un funkcionālo novietojumu skaitu, ar kuriem ir saistīts atlasītais uzturēšanas speciālists.

## <a name="create-worker-groups"></a>Nodarbināto grupu izveide

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Nodarbinātie** \> **Uzturēšanas speciālistu grupas**.
2. Atlasiet **Jauns**, lai pievienotu nodarbināto grupu sarakstam.
3. Laukā **Uzturēšanas speciālistu grupa** ievadiet grupas ID.
4. Laukā **Nosaukums** ievadiet nosaukumu.
5. Kopsavilkuma cilnē **Nodarbinātie** atlasiet **Pievienot** un pēc tam atlasiet uzturēšanas speciālistu nodarbināto grupai. Informāciju par laukiem **Ir spēkā** un **Beigu datums** skatiet iepriekšējās procedūras 6. darbībā.
6. Ja resursu grupai ir jābūt saistītai ar atlasīto uzturēšanas speciālistu grupu, atlasiet **Kopēt no resursu grupas**. Laukā **Grupa** atlasiet resursu grupu, no kuras kopēt kalendāra iestatījumus. Pēc tam laukā **Nodarbināto grupa** atlasiet nodarbināto grupu, uz kuru kopēt resursu grupas kalendāra iestatījumus. Šī darbība ir būtiska tikai tad, ja vēlaties, lai uzturēšanas speciālisti darba pasūtījuma plānošanas laikā izmanto kalendāru, kas ir saistīts ar resursu (darba centru).

    Kopsavilkuma cilne **Detalizēta informācija** rāda to uzturēšanas speciālistu skaitu, kuri ir iestatīti atlasītajā uzturēšanas speciālistu grupā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]