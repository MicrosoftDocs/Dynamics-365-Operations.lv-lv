---
title: Piekrišana izmantot vērtējumus un atsauksmes
description: Šajā tēmā ir paskaidrots, kā piekrist izmantot vērtējumus un apskatus savā Microsoft Dynamics 365 Commerce vietnē.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697984"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Piekrišana izmantot vērtējumus un atsauksmes

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā piekrist izmantot vērtējumus un apskatus savā Microsoft Dynamics 365 Commerce vietnē.

## <a name="overview"></a>Pārskats

Vērtējumu un apskatu risinājums ir daudzkanālu risinājums, ko var padarīt pieejamu Dynamics 365 Commerce, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir administrēšanas portāls, ko mazumtirgotāji izmanto, lai pārvaldītu savas vides no nodrošināšanas līdz ekspluatācijas pārtraukšanai.

Ja vēlaties izmantot vērtējumu un apskatu risinājumu savā Commerce tīmekļa lapā, jums vispirms jāpiekrīt.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Piekrišana izmantot vērtējumus un atsauksmes

Lai piekristu savā vietnē izmantot vērtējumus un apskatus, veiciet tālāk minētās darbības.

1. Veiciet darbības, kas minētas [Izvietot jaunu e-komercijas vietni](deploy-ecommerce-site.md).
1. Kamēr vēl esat LCS, dodieties uz **Mazumtirdzniecības izvietošanas iestatīšana \> Citi iestatījumi**.
1. Iestatiet opciju **Iespējot vērtējumus un apskatus** uz **Jā**.
1. Laukā **AAD drošības grupas moderators vērtējumiem un apskatiem (drošības grupas objekta ID)** ievadiet Microsoft Azure Active Directory (Azure AD) drošības grupas ID, kas ietver vērtējumu un apskatu moderatorus.

    ![Piekrišana izmantot vērtējumus un atsauksmes](media/LCS_RnR_Preference.png)

1. Pabeidziet e-komercijas inicializēšanas procesu.

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija Dynamics 365 Retail](sync-product-ratings.md)
