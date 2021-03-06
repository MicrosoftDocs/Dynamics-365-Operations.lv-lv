---
title: Integrēt Dynamics 365 Supply Chain Management (Līdzekļu pārvaldība) ar Dynamics 365 Guides
description: Šajā tēmā skaidrots, kā integrēt Līdzekļu pārvaldības moduli programmā Microsoft  Dynamics 365 Supply Chain Management ar Dynamics 365 Guides, lai izmantotu jauktās realitātes ceļvežiem jūsu ikdienas pakalpojumos un uzturēšanas darbplūsmās.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 50cfea6656e1f13532b018784fa64b2aac10fc7f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908571"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Integrēt Dynamics 365 Supply Chain Management (Līdzekļu pārvaldība) ar Dynamics 365 Guides

Jūs varat integrēt **Līdzekļu pārvaldības** moduli programmā Microsoft Dynamics 365 Supply Chain Management ar Dynamics 365 Guides, lai izmantotu jauktās realitātes ceļvežus jūsu ikdienas pakalpojumos un uzturēšanas darbplūsmās. Ja ceļvedis ir saistīts ar Līdzekļu pārvaldības darba pasūtījumu, darbinieks, kurš atver darba pasūtījuma uzturēšanas kontrolsarakstu Supply Chain Management (Dynamics 365) mobilajā programmā, redz, ka ceļvedis ir pieejams. Darbinieks pēc tam var atrast un atvērt ceļvedi programmā Dynamics 365 Guides HoloLens.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms varat pievienot ceļvežus Līdzekļu pārvaldības darba pasūtījumiem, ir jāveic šie priekšnosacījumi:

- [Uzstādīt Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) 10.0.9 versiju vai jaunāku versiju.
- [Ieslēgt duālo rakstīšanu Supply Chain Management programmām](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Ieslēgt lidojumu](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** līdzeklim. (Ražošanas vidēm vispirms jāiesniedz atbalsta biļete, lai jūsu nomnieks būtu pievienots lidojuma grupai.)
- [Ieslēgt šādas konfigurācijas atslēgas](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) lapā **Licences konfigurācija**:

    - Līdzekļu pārvaldība \> Līdzekļu pārvaldības jauktā realitāte
    - Jauktā realitāte \> Jauktās realitātes ceļvedis

- [Uzstādīt Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 200.0.0.96 versiju vai jaunāku versiju.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Izmantot Dynamics 365 Guides ar Līdzekļu pārvaldību

Lai piesaistītu ceļvedi, Līdzekļu pārvaldībā jāizmanto uzturēšanas kontrolsaraksta rinda. Varat izveidot saistību, izmantojot uzturēšanas kontrolsaraksta veidni, uzturēšanas darba veidu vai darba pasūtījumu, jo visi trīs ietver uzturēšanas kontrolsaraksta rindas. Varat ietaupīt laiku, izmantojot veidni, jo veidne var tikt saistīta ar visiem uzturēšanas darbu veidiem, kas to izmanto. Piemēram, ceļvedis, kas ir saistīts ar uzturēšanas darba veidu, tiek automātiski saistīts ar visiem darba pasūtījumiem, kas norāda šo darba veidu. No otras puses, ceļvedis, kas ir tieši saistīts ar darba pasūtījumu, pastāv tikai šim darba pasūtījumam.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Saistīt ceļvedi ar uzturēšanas kontrolsaraksta veidni

Lai saistītu ceļvedi ar uzturēšanas kontrolsaraksta veidni, sekojiet šiem soļiem.

1. Izveidojiet ceļvedi, izmantojot Dynamics 365 Guides datoru un HoloLens programmas. Informāciju par to, kā izveidot ceļvedi, skatiet tālāk norādītajās tēmās.

    - [Izmantot datora programmu, lai izveidotu ceļvedi](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Izmantot HoloLens programmu, lai ievietotu jūsu hologrammas](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Supply Chain Management [izveidojiet uzturēšanas kontrolsaraksta veidni](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Saistiet ceļvedi, ko izveidojāt ar uzturēšanas kontrolsaraksta rindu jaunajā uzturēšanas kontrolsaraksta veidnē:

    1. Kopsavilkuma cilnē **Uzturēšanas kontrolsaraksta rindas** atlasiet rindu, ar kuru vēlaties saistīt ceļvedi.
    1. Kopsavilkuma cilnē **Saistītie ceļveži** atlasiet **Pievienot ceļvedi**.

        ![Saistīt ceļvedi ar uzturēšanas kontrolsaraksta rindu](media/am-guides-integration-add-guide.png "Saistīt ceļvedi ar uzturēšanas kontrolsaraksta rindu")

    1. Laukā **Nosaukums** atlasiet ceļvedi un pēc tam atlasiet **Saglabāt**.

        ![Atlasīt ceļvedi Nosaukuma laukā](media/am-guides-integration-select-guide.png "Atlasīt ceļvedi Nosaukuma laukā")

1. Saistīt uzturēšanas kontrolsaraksta veidni ar darba veidu:

    1. [Izveidot uzturēšanas darba veidu](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) vai atlasīt jau esošu uzturēšanas darba veidu.
    1. Darbības rūtī atlasiet **Uzturēšanas darba veida noklusējumi**.

        ![Uzturēšanas darba veida noklusējumu poga](media/am-guides-integration-job-defaults.png "Uzturēšanas darba veida noklusējumu poga")

    1. Izveidojiet rindu un tad atlasiet **Saglabāt**.

        ![Izveidot rindu](media/am-guides-integration-add-line.png "Izveidot rindu")

    1. Darbību rūtī atlasiet **Uzturēšanas kontrolsaraksts**.

        ![Uzturēšanas kontrolsaraksta poga](media/am-guides-integration-maintenance-checklist.png "Uzturēšanas kontrolsaraksta poga")

    1. Kopsavilkuma cilnē **Uzturēšanas kontrolsaraksta rindas** pievienojiet rindu un pēc tam mainiet lauka **Veids** vērtību uz **Veidne**.

        ![Mainīt Veida vērtību](media/am-guides-integration-checklist-lines.png "Mainīt Veida vērtību")

    1. Kopsavilkuma cilnē **Rindas detaļas** laukā **Veidne** atlasiet veidni, ar kuru esat saistījis ceļvedi, un pēc tam atlasiet **Saglabāt**.

        ![Atlasīt veidni](media/am-guides-integration-checklist-line-details.png "Atlasīt veidni")

1. [Izveidot darba pasūtījumu](work-orders/manually-created-workorders.md#create-work-order) un pēc tam atlasīt uzturēšanas darba veidu, kas izmanto uzturēšanas kontrolsaraksta veidni, ar kuru ir saistīts ceļvedis. Ceļvedis ir automātiski saistīts ar darba pasūtījumu.

    ![Atlasīt uzturēšanas darba veidu](media/am-guides-integration-create-work-order.png "Atlasīt uzturēšanas darba veidu")

1. Skatiet ceļvedi, kas saistīts ar darba pasūtījumu un darbiniekiem:

    1. Atveriet [Pamatlīdzekļu pārvaldības mobilo darbvieta](asset-management-mobile-workspace.md), lai piekļūtu darba pasūtījumam.
    1. [Atveriet uzturēšanas kontrolsarakstu](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) darba pasūtījumam.
    1. Atlasiet kontrolsaraksta rindu, lai apskatītu saistīto ceļvedi.

        ![Ceļvedis, kas saistīts ar kontrolsaraksta rindu](media/am-guides-integration-show-guide.png "Ceļvedis, kas saistīts ar kontrolsaraksta rindu")

    1. Atveriet ceļvedi programmā HoloLens.

        ![Atveriet ceļvedi programmā HoloLens](media/am-guides-integration-hololens-select.png "Atveriet ceļvedi programmā HoloLens")

> [!NOTE]
> Varat arī saistīt ceļvedi tieši darba pasūtījuma vai darba veida uzturēšanas kontrolsarakstā.

> [!IMPORTANT]
> Pastāv zināma problēma, kur, saistot uzturēšanas kontrolsaraksta veidni ar noklusējuma uzturēšanas darba veidu, ceļvedis, kas ir saistīts ar veidni, netiek parādīts kopsavilkuma cilnē **Saistītie ceļveži** lapā **Uzturēšanas darba veida noklusējumi**. Tomēr ceļvedis parādīsies pēc tam, kad darbaveids tiek lietots darba pasūtījumam kopsavilkuma cilnē **Saistītie ceļveži**.

## <a name="see-also"></a>Skatiet arī

- [Duālā ieraksta pārskats](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Pārskats par līdzekļu pārvaldību](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]