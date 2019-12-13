---
title: Jauna e-tirdzniecības nomnieka izvietošana
description: Šajā tēmā ir aprakstīts, kā izvietot jaunu e-tirdzniecības nomnieku, izmantojot Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697455"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Jauna e-tirdzniecības nomnieka izvietošana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izvietot jaunu e-tirdzniecības vietni, izmantojot Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>Pārskats
    
Microsoft Dynamics Lifecycle Services (LCS) ir mākonī balstīta sadarbības darbvieta, ko partneri un klienti var izmantot, lai pārvaldītu savus projektus un vides, skatīt jaunāko informāciju par Microsoft Dynamics precēm un līdzekļiem, kā arī izveidotu, izsekotu un pārlūkotu atbalsta incidentus. E-tirdzniecības pārvaldības līdzekļi ir integrēti LCS.

Lai uzzinātu vairāk par LCS skatiet [Lifecycle Services lietotāja rokasgrāmatā](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Sākt darbu

Pirms e-tirdzniecības inicializēšanas ir jāinicializē projekts, vide un Retail Cloud Scale Unit (RCSU). Lai veiktu inicializēšanu LCS, jums jābūt vai nu projekta īpašnieka vai vides pārvaldnieka lomas atļaujai. Tiek atbalstītas ražošanas un smilškastes vides topoloģijas.

Lai iegūtu vairāk informācijas par vidi, skatiet [Vides plānošana](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Lai iegūtu vairāk informācijas par RCSU, skatiet [Retail Cloud Scale Unit inicializēšana](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>E-tirdzniecības inicializēšana

Izmantojiet šo procedūru, lai esošajā vidē inicializētu e-tirdzniecības līdzekli.

Pirms sākt, pārliecinieties, ka jums ir tālāk minētā nepieciešamā informācija.

- Izmantojamais RCSU.
- Microsoft Azure Active Directory drošības grupa, kas tiks izmantota e-tirdzniecības sistēmas administratoriem.
- Microsoft Azure Active Directory drošības grupa, kas tiks izmantota vērtējumu un apskatu moderatoriem.
- Domēni, kas tiks saistīti ar vidi.

Pēc izvēles papildus varat ievākt tālāk minēto informāciju.

- Azure AD bizness–patērētājs (B2C) informācija:

    - Nomnieka nosaukums.
    - Klienta ID.
    - Pielāgotā domēna pieteikšanās.
    - Atbildes URL.
    - Parakstīšanās un pierakstīšanās politikas ID.
    - Paroles atiestatīšanas politikas ID.
    - Profila rediģēšanas politikas ID.

[!NOTE]
Šo informāciju var pievienot vēlāk, izmantojot pakalpojuma pieprasījumu.

Pēc tam, kad ievākta nepieciešamā informācija, veiciet tālāk minētās darbības, lai inicializētu e-tirdzniecību.

1. Pierakstieties [LCS](https://lcs.dynamics.com).
1. Atveriet projektu, kas satur vidi, kurā vēlaties inicializēt e-tirdzniecību.
1. Sadaļā **Vides** atlasiet vidi.
1. Sadaļā **Vides līdzekļi**atlasiet saiti **Mazumtirdzniecības pārvaldība**.
1. Cilnē **E-tirdzniecība** atlasiet **Iestatīt**. Parādās dialoglodziņš, kur jāievada informācija, kas nepieciešama nodrošināšanai.
1. Ievadiet nepieciešamo informāciju un pēc tam dodieties uz nākamo lapu.
1. Nākamajā lapā ievadiet nepieciešamo informāciju un pēc iesniedziet veidlapu. Notiks atgriešanās atpakaļ cilnē **E-tirdzniecība**, kur ir jābūt redzamam, ka inicializēšana ir uzsākta.
1. Lai skatītu inicializēšanas statusu, vai nu nospiediet **Atsvaidzināt**, vai arī vēlāk atgriezieties cilnē **E-tirdzniecība**.
    
Kad e-tirdzniecība tiek inicializēta no LCS, sistēma nodrošina vairākus komponentus, kas nepieciešami e-tirdzniecībai, un saista tos ar vidi. Kad nodrošināšana ir pabeigta, tiek atjaunināta cilne **E-tirdzniecība** lapā **Mazumtirdzniecības pārvaldība**, lai atspoguļotu nodrošināšanu. Lapa parāda jaunākās pielāgošanas izvietošanas un visu citu notiekošo izvietošanu statusu. Tajā ir arī saites uz e-tirdzniecības vietni un e-tirdzniecības vietnes pārvaldības rīku (autorēšanas rīku).

## <a name="access-the-authoring-environment"></a>Piekļuve autorēšanas videi

Lai piekļūtu autorēšanas videi, dodieties uz cilni **E-tirdzniecība**, kas atrodas lapā **Mazumtirdzniecības pārvaldība**. Tur atradīsit saites uz e-tirdzniecības vietni un vietnes pārvaldības rīku.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes veikala apskats](online-store-overview.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Tiešsaistes vietnes saistīšana ar kanālu](associate-site-online-store.md)

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)
