---
title: Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu
description: Šajā tēmā ir paskaidrots, kā saistīt savu Microsoft Dynamics 365 Commerce vietni ar vienu vai vairākiem tiešsaistes veikaliem.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6ae02d34499275fa303358f7dae4d3835d438e1
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517334"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="017ce-103">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="017ce-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="017ce-104">Šajā tēmā ir paskaidrots, kā saistīt savu Microsoft Dynamics 365 Commerce vietni ar vienu vai vairākiem tiešsaistes veikaliem.</span><span class="sxs-lookup"><span data-stu-id="017ce-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="017ce-105">Pēc tam, kad esat nodrošinājis Dynamics 365 Commerce e-komercijas vidi, izmantojot Microsoft Dynamics Lifecycle Services (LCS) portālu, varat izveidot savu pirmo e-komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="017ce-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="017ce-106">Sākotnēji veidojot vietni, jūs saistiet vietni ar iepriekš izveidoto tiešsaistes veikalu.</span><span class="sxs-lookup"><span data-stu-id="017ce-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="017ce-107">Šī darbība piesaista vietni tiešsaistes kanālam un ļauj vietnei rādīt navigācijas hierarhiju, preces, kategorijas, cenas, piegādes opcijas un visu pārējo, kas definēts tiešsaistes veikalā.</span><span class="sxs-lookup"><span data-stu-id="017ce-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="017ce-108">Lai izveidotu jaunu vietni un saistītu ar to tiešsaistes veikalu, pakalpojumā LCS atlasiet saiti uz vietnes autorēšanas vidi.</span><span class="sxs-lookup"><span data-stu-id="017ce-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="017ce-109">Pēc tam vietnes autorēšanas vides lapā atlasiet **Jauna vietne**.</span><span class="sxs-lookup"><span data-stu-id="017ce-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="017ce-110">Dialoglodziņā **Jauna vietne** ir jānorāda pamatinformācija par savu vietni.</span><span class="sxs-lookup"><span data-stu-id="017ce-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="017ce-111">Lai iegūtu pilnīgu skaidrojumu par sniedzamo informāciju, skatiet tēmu [Jaunas e-komercijas vietnes izveide](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="017ce-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="017ce-112">Pēc vietnes izveides varat pārbaudīt, vai tā ir saistīta ar jūsu tiešsaistes veikalu, atlasot cilni **Preces**. Jābūt redzamam preču klāstam, kas tika piešķirts tiešsaistes veikalam.</span><span class="sxs-lookup"><span data-stu-id="017ce-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="017ce-113">Lai piekļūtu precēm pēc kategorijas, varat arī izmantot nolaižamo lauku lapas augšējā kreisajā malā.</span><span class="sxs-lookup"><span data-stu-id="017ce-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="017ce-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="017ce-114">Additional resources</span></span>

[<span data-ttu-id="017ce-115">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="017ce-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="017ce-116">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="017ce-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="017ce-117">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="017ce-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="017ce-118">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="017ce-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="017ce-119">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="017ce-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="017ce-120">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="017ce-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="017ce-121">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="017ce-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="017ce-122">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="017ce-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="017ce-123">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="017ce-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="017ce-124">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="017ce-124">Enable location-based store detection</span></span>](enable-store-detection.md)
