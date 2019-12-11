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
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="8d0e5-103">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="8d0e5-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8d0e5-104">Šajā tēmā ir paskaidrots, kā piekrist izmantot vērtējumus un apskatus savā Microsoft Dynamics 365 Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="8d0e5-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8d0e5-105">Overview</span></span>

<span data-ttu-id="8d0e5-106">Vērtējumu un apskatu risinājums ir daudzkanālu risinājums, ko var padarīt pieejamu Dynamics 365 Commerce, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8d0e5-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8d0e5-107">LCS ir administrēšanas portāls, ko mazumtirgotāji izmanto, lai pārvaldītu savas vides no nodrošināšanas līdz ekspluatācijas pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="8d0e5-108">Ja vēlaties izmantot vērtējumu un apskatu risinājumu savā Commerce tīmekļa lapā, jums vispirms jāpiekrīt.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="8d0e5-109">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="8d0e5-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="8d0e5-110">Lai piekristu savā vietnē izmantot vērtējumus un apskatus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="8d0e5-111">Veiciet darbības, kas minētas [Izvietot jaunu e-komercijas vietni](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="8d0e5-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="8d0e5-112">Kamēr vēl esat LCS, dodieties uz **Mazumtirdzniecības izvietošanas iestatīšana \> Citi iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="8d0e5-113">Iestatiet opciju **Iespējot vērtējumus un apskatus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="8d0e5-114">Laukā **AAD drošības grupas moderators vērtējumiem un apskatiem (drošības grupas objekta ID)** ievadiet Microsoft Azure Active Directory (Azure AD) drošības grupas ID, kas ietver vērtējumu un apskatu moderatorus.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Piekrišana izmantot vērtējumus un atsauksmes](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="8d0e5-116">Pabeidziet e-komercijas inicializēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="8d0e5-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d0e5-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8d0e5-117">Additional resources</span></span>

[<span data-ttu-id="8d0e5-118">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="8d0e5-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="8d0e5-119">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="8d0e5-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="8d0e5-120">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8d0e5-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="8d0e5-121">Preču vērtējumu sinhronizācija Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="8d0e5-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
