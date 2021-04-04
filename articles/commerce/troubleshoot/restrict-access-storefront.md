---
title: Piekļuves ierobežošana vitrīnai testēšanas vai izstrādes laikā
description: Šajā tēmā paskaidrots, kā ierobežot piekļuvi Microsoft Dynamics 365 Commerce vitrīnai laikā, kad notiek iekšējā testēšana vai izstrāde.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585433"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="2424e-103">Piekļuves ierobežošana vitrīnai testēšanas vai izstrādes laikā</span><span class="sxs-lookup"><span data-stu-id="2424e-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2424e-104">Šajā tēmā paskaidrots, kā ierobežot piekļuvi Microsoft Dynamics 365 Commerce vitrīnai laikā, kad notiek iekšējā testēšana vai izstrāde.</span><span class="sxs-lookup"><span data-stu-id="2424e-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="2424e-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="2424e-105">Description</span></span>

<span data-ttu-id="2424e-106">Iekšējās testēšanas vai aktīvas izstrādes laikā, iespējams, vēlēsities ierobežot piekļuvi jūsu vietnei, lai neļautu ārējiem lietotājiem piekļūt publicētajām vitrīnas lapām.</span><span class="sxs-lookup"><span data-stu-id="2424e-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="2424e-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="2424e-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="2424e-108">Azure AD B2C iestatīšana, izmantojot standarta lietotāju plūsmas</span><span class="sxs-lookup"><span data-stu-id="2424e-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="2424e-109">Informāciju par to, kā konfigurēt Azure Active Directory B2C (Azure AD B2C) jūsu e-komercijas vietnei, skatiet sadaļu [B2C nomnieka iestatīšana programmā Commerce](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="2424e-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="2424e-110">Lietotāju piekļuves vitrīnas lapām ierobežošana un jaunu lietotāju izveides bloķēšana</span><span class="sxs-lookup"><span data-stu-id="2424e-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="2424e-111">Lai ierobežotu lietotāju piekļuvi vitrīnas lapām Commerce vietnes veidotājā, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="2424e-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2424e-112">Dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="2424e-112">Go to your site.</span></span>
1. <span data-ttu-id="2424e-113">Atlasiet **Lapas** un pēc tam atlasiet lapu, kurai ierobežot lietotāju piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="2424e-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="2424e-114">Atlasiet moduli vai fragmenta slotu un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2424e-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="2424e-115">Rekvizītu rūtī atlasiet **Nepieciešama pierakstīšanās?** un pēc tam atlasiet **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="2424e-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2424e-116">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="2424e-116">Select **Publish**.</span></span>

<span data-ttu-id="2424e-117">Lai bloķētu jaunu lietotāju izveidošanu Azure AD, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="2424e-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="2424e-118">Dodieties uz [Azure portālu](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="2424e-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="2424e-119">Atlasiet Azure AD B2C programmu, ko izveidojāt jūsu vietnes piekļuvei.</span><span class="sxs-lookup"><span data-stu-id="2424e-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="2424e-120">Kreisās puses navigācijā atlasiet **Lietotāju plūsmas**.</span><span class="sxs-lookup"><span data-stu-id="2424e-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="2424e-121">Lapas **Lietotāju plūsmas** augšpusē atlasiet **Jauna lietotāja plūsma**.</span><span class="sxs-lookup"><span data-stu-id="2424e-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="2424e-122">Lapā **Atlasīt lietotāja plūsmas veidu** atlasiet **Priekšskatījums**.</span><span class="sxs-lookup"><span data-stu-id="2424e-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="2424e-123">Lapas vidū atlasiet **Pierakstīties v2**.</span><span class="sxs-lookup"><span data-stu-id="2424e-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="2424e-124">Pēc tam izpildiet darbības sadaļā [B2C nomnieka iestatīšana programmā Commerce](../set-up-b2c-tenant.md), lai konfigurētu plūsmu kā jūsu vietnes standarta lietotāju plūsmu Azure AD B2C testēšanas vai izstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="2424e-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2424e-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2424e-125">Additional resources</span></span>

[<span data-ttu-id="2424e-126">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="2424e-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="2424e-127">Pielāgotu lapu iestatīšana lietotāja pierakstīšanās gadījumiem</span><span class="sxs-lookup"><span data-stu-id="2424e-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
