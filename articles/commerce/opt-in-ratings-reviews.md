---
title: Piekrišana izmantot vērtējumus un atsauksmes
description: Šajā tēmā ir paskaidrots, kā piekrist izmantot vērtējumus un apskatus savā Microsoft Dynamics 365 Commerce vietnē.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 481a8750b2333d5dd5de2c05e175569804a6046f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985840"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Piekrišana izmantot vērtējumus un atsauksmes

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā piekrist izmantot vērtējumus un apskatus savā Microsoft Dynamics 365 Commerce vietnē.

## <a name="overview"></a>Pārskats

Vērtējumu un apskatu risinājums ir daudzkanālu risinājums, ko var padarīt pieejamu Dynamics 365 Commerce, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir administrēšanas portāls, ko mazumtirgotāji izmanto, lai pārvaldītu savas vides no nodrošināšanas līdz ekspluatācijas pārtraukšanai.

Ja vēlaties izmantot vērtējumu un pārskatu risinājumu savā Commerce vietnē, jums ir jāpiesakās vērtējumiem un pārskatiem, kad izvietojat savu e-komercijas vietni Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Piekrišana izmantot vērtējumus un atsauksmes

Lai piekristu savā vietnē izmantot vērtējumus un apskatus, veiciet tālāk minētās darbības.

1. Veiciet darbības, kas minētas [Izvietot jaunu e-komercijas vietni](deploy-ecommerce-site.md).
1. Kamēr vēl esat LCS, dodieties uz **Mazumtirdzniecības izvietošanas iestatīšana \> Citi iestatījumi**.
1. Iestatiet opciju **Iespējot vērtējumus un apskatus** uz **Jā**.
1. Laukā **AAD drošības grupas moderators vērtējumiem un apskatiem (drošības grupas objekta ID)** ievadiet Microsoft Azure Active Directory (Azure AD) drošības grupas ID, kas ietver vērtējumu un apskatu moderatorus.

    ![Piekrišana izmantot vērtējumus un atsauksmes](media/LCS_RnR_Preference.png)

1. Pabeidziet e-komercijas inicializēšanas procesu.

> [!NOTE] 
> Ja esat esošs Dynamics 365 Commerce klients, kas jau ir izvietojis e-komercijas vietni, neizvēloties vērtējumus un pārskatus, un tagad vēlaties izmantot vērtējumus un pārskatus Dynamics 365 Commerce pakotnē, lūdzu, iesniedziet pakalpojuma pieprasījumu. Informāciju par to, kā iesniegt pakalpojuma pieprasījumu, skatiet šeit: [Pakalpojumu pieprasījumu iesniegšanas process.](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Vērtējumu un atsauksmju pārvaldība](manage-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija Dynamics 365 Commerce](sync-product-ratings.md)


