---
title: Piekrišana izmantot vērtējumus un atsauksmes
description: Šajā rakstā skaidrots, kā izvēlēties izmantot novērtējumus un pārskatīšanas jūsu Microsoft Dynamics 365 Commerce vietnē.
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 00fd30ded916cc6b587ceff67728e7d964714716
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269167"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Piekrišana izmantot vērtējumus un atsauksmes

[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā izvēlēties izmantot novērtējumus un pārskatīšanas jūsu Microsoft Dynamics 365 Commerce vietnē.

Vērtējumu un apskatu risinājums ir daudzkanālu risinājums, ko var padarīt pieejamu Dynamics 365 Commerce, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir administrēšanas portāls, ko mazumtirgotāji izmanto, lai pārvaldītu savas vides no nodrošināšanas līdz ekspluatācijas pārtraukšanai.

Ja vēlaties izmantot vērtējumu un pārskatu risinājumu savā Commerce vietnē, jums ir jāpiesakās vērtējumiem un pārskatiem, kad izvietojat savu e-komercijas vietni Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Piekrišana izmantot vērtējumus un atsauksmes

Lai piekristu savā vietnē izmantot vērtējumus un apskatus, veiciet tālāk minētās darbības.

1. Veiciet darbības, kas minētas [Izvietot jaunu e-komercijas vietni](deploy-ecommerce-site.md).
1. Kamēr vēl esat LCS, dodieties uz **Mazumtirdzniecības izvietošanas iestatīšana \> Citi iestatījumi**.
1. Iestatiet opciju **Iespējot vērtējumus un apskatus** uz **Jā**.
1. **AAD drošības grupā novērtējumiem un pārskatiet regulētāja** lauku, ievadiet Microsoft Azure Active Directory (Azure AD) drošības grupas ID, kas ietver vērtējumus un pārskata starpniekus.

    ![Piekrišana izmantot vērtējumus un atsauksmes.](media/LCS_RnR_Preference_2.png)

1. Pabeidziet e-komercijas inicializēšanas procesu.

> [!NOTE] 
> Ja esat esošs Dynamics 365 Commerce klients, kas jau ir izvietojis e-komercijas vietni, neizvēloties vērtējumus un pārskatus, un tagad vēlaties izmantot vērtējumus un pārskatus Dynamics 365 Commerce pakotnē, lūdzu, iesniedziet pakalpojuma pieprasījumu. Informāciju par to, kā iesniegt pakalpojuma pieprasījumu, skatiet šeit: [Pakalpojumu pieprasījumu iesniegšanas process.](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija Dynamics 365 Commerce](sync-product-ratings.md)

[Iespējojiet moderatora manuālo vērtējumu un atsauksmju publicēšanu](manual-publish-rating-reviews.md)

[Novērtējumu un pārskatu importēšana un eksportēšana](import-export-reviews.md)

[Autentifikācijas starp pakalpojumiem konfigurēšana](service-to-service-auth.md)

[BUJ par vērtējumiem un atsauksmēm](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
