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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057514"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="3fabe-103">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="3fabe-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3fabe-104">Šajā tēmā ir paskaidrots, kā piekrist izmantot vērtējumus un apskatus savā Microsoft Dynamics 365 Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="3fabe-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="3fabe-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="3fabe-105">Overview</span></span>

<span data-ttu-id="3fabe-106">Vērtējumu un apskatu risinājums ir daudzkanālu risinājums, ko var padarīt pieejamu Dynamics 365 Commerce, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3fabe-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3fabe-107">LCS ir administrēšanas portāls, ko mazumtirgotāji izmanto, lai pārvaldītu savas vides no nodrošināšanas līdz ekspluatācijas pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="3fabe-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="3fabe-108">Ja vēlaties izmantot vērtējumu un pārskatu risinājumu savā Commerce vietnē, jums ir jāpiesakās vērtējumiem un pārskatiem, kad izvietojat savu e-komercijas vietni Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3fabe-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="3fabe-109">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="3fabe-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="3fabe-110">Lai piekristu savā vietnē izmantot vērtējumus un apskatus, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="3fabe-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="3fabe-111">Veiciet darbības, kas minētas [Izvietot jaunu e-komercijas vietni](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="3fabe-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="3fabe-112">Kamēr vēl esat LCS, dodieties uz **Mazumtirdzniecības izvietošanas iestatīšana \> Citi iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="3fabe-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="3fabe-113">Iestatiet opciju **Iespējot vērtējumus un apskatus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3fabe-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="3fabe-114">Laukā **AAD drošības grupas moderators vērtējumiem un apskatiem (drošības grupas objekta ID)** ievadiet Microsoft Azure Active Directory (Azure AD) drošības grupas ID, kas ietver vērtējumu un apskatu moderatorus.</span><span class="sxs-lookup"><span data-stu-id="3fabe-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Piekrišana izmantot vērtējumus un atsauksmes](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="3fabe-116">Pabeidziet e-komercijas inicializēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="3fabe-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="3fabe-117">Ja esat esošs Dynamics 365 Commerce klients, kas jau ir izvietojis e-komercijas vietni, neizvēloties vērtējumus un pārskatus, un tagad vēlaties izmantot vērtējumus un pārskatus Dynamics 365 Commerce pakotnē, lūdzu, iesniedziet pakalpojuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="3fabe-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="3fabe-118">Informāciju par to, kā iesniegt pakalpojuma pieprasījumu, skatiet šeit: [Pakalpojumu pieprasījumu iesniegšanas process.](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="3fabe-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3fabe-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3fabe-119">Additional resources</span></span>

[<span data-ttu-id="3fabe-120">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="3fabe-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="3fabe-121">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="3fabe-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="3fabe-122">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3fabe-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="3fabe-123">Preču vērtējumu sinhronizācija Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3fabe-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


