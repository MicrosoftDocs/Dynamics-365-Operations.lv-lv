---
title: Jauna e-tirdzniecības nomnieka izvietošana
description: Šajā rakstā ir aprakstīts, kā izvietot jaunu Dynamics 365 Commerce e-komercijas vietni, izmantojot Microsoft Dynamics Lifecycle Services (LCS).
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c2dadbebea04b59680df5a5bbbd71e83eab41175
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267560"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Jauna e-tirdzniecības nomnieka izvietošana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izvietot jaunu Dynamics 365 Commerce e-komercijas vietni, izmantojot Microsoft Dynamics Lifecycle Services (LCS).

Microsoft Dynamics Lifecycle Services (LCS) ir mākonī balstīta sadarbības darbvieta, ko partneri un klienti var izmantot, lai pārvaldītu savus projektus un vides, skatīt jaunāko informāciju par Microsoft Dynamics precēm un līdzekļiem, kā arī izveidotu, izsekotu un pārlūkotu atbalsta incidentus. E-komercijas pārvaldības līdzekļi ir integrēti LCS.

Lai uzzinātu vairāk par LCS skatiet [Lifecycle Services lietotāja rokasgrāmatā](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Darba sākšana

Pirms e-komercijas inicializēšanas ir jāinicializē projekts, vide un Retail Cloud Scale Unit (RCSU). Lai veiktu inicializēšanu LCS, jums jābūt vai nu projekta īpašnieka vai vides pārvaldnieka lomas atļaujai. Tiek atbalstītas ražošanas un smilškastes vides topoloģijas.

Lai iegūtu vairāk informācijas par vidi, skatiet [Vides plānošana](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Lai iegūtu vairāk informācijas par RCSU, skatiet [Inicializēt Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>E-komercijas inicializēšana

Izmantojiet šo procedūru, lai esošajā vidē inicializētu e-komercijas līdzekli.

Pirms sākt, pārliecinieties, ka jums ir tālāk minētā nepieciešamā informācija.

- Izmantojamais RCSU.
- Microsoft Azure Active Directory drošības grupa, kas tiks izmantota e-komercijas sistēmas administratoriem.
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

> [!NOTE]
> Šo informāciju var pievienot vēlāk, izmantojot pakalpojuma pieprasījumu.

Pēc tam, kad ievākta nepieciešamā informācija, veiciet tālāk minētās darbības, lai inicializētu e-komerciju.

1. Pierakstieties [LCS](https://lcs.dynamics.com).
1. Atveriet projektu, kas satur vidi, kurā vēlaties inicializēt e-komerciju.
1. Sadaļā **Vides** atlasiet vidi.
1. Sadaļā **Vides līdzekļi** atlasiet saiti **Mazumtirdzniecības pārvaldība**.
1. Cilnē **E-tirdzniecība** atlasiet **Iestatīt**. Parādās dialoglodziņš, kur jāievada informācija, kas nepieciešama nodrošināšanai.
1. Ievadiet nepieciešamo informāciju un pēc tam dodieties uz nākamo lapu.
1. Nākamajā lapā ievadiet nepieciešamo informāciju un pēc iesniedziet veidlapu. Notiks atgriešanās atpakaļ cilnē **E-tirdzniecība**, kur ir jābūt redzamam, ka inicializēšana ir uzsākta.
1. Lai skatītu inicializēšanas statusu, vai nu nospiediet **Atsvaidzināt**, vai arī vēlāk atgriezieties cilnē **E-tirdzniecība**.
    
Kad e-komercija tiek inicializēta no LCS, sistēma nodrošina vairākus komponentus, kas nepieciešami e-komercijai, un saista tos ar vidi. Kad nodrošināšana pabeigta, tiek atjaunināta cilne **E-komercija** lapā **Mazumtirdzniecības pārvaldība**, lai atspoguļotu nodrošināšanu. Lapa parāda jaunākās pielāgošanas izvietošanas un visu citu notiekošo izvietošanu statusu. Tajā ir arī saites uz e-komercijas vietni un e-komercijas vietnes veidotāju, kurā vietnes tiek autorētas.

## <a name="access-commerce-site-builder"></a>Piekļuve Commerce vietnes veidotājam

Lai piekļūtu Commerce vietnes veidotājam, dodieties uz cilni **Komercija** LCS lapā **Mazumtirdziecības pārvaldība** un atlasiet saiti **e-komercijas vietnes pārvaldības rīks**. Vietnes veidotāja izvietošanas lapa tiek parādīts nomnieka līmeņa skatījums. No šīs lapas iespējams veikt tālāk minētās darbības.

- Modificēt nomnieka līmeņa iestatījumus.
- Doties uz jebkuru jūsu izveidoto vietni, un jums ir atļauja to apskatīt. 
- Piekļuves apskatu funkcijas, piemēram, regulēšanu un ziņošanu.
- Izveidot jaunu vietni. Papildinformāciju par to, kā izveidot jaunu vietni, skatiet sadaļā [E-komercijas vietnes izveide](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
