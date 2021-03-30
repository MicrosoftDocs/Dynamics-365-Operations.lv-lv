---
title: Dynamics 365 Commerce vietnes saistīšana ar tiešsaistes kanālu
description: Šajā tēmā paskaidrots, kā saistīt Microsoft Dynamics 365 Commerce vietni ar vienu vai vairākiem tiešsaistes veikaliem.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb39b54e45e387067720dcbc5d9ccffbf8bf08b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211526"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="4adde-103">Dynamics 365 Commerce vietnes saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="4adde-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4adde-104">Šajā tēmā paskaidrots, kā saistīt Microsoft Dynamics 365 Commerce vietni ar vienu vai vairākiem tiešsaistes veikaliem.</span><span class="sxs-lookup"><span data-stu-id="4adde-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="4adde-105">Pēc tam, kad esat nodrošinājis Dynamics 365 Commerce e-komercijas vidi, izmantojot Microsoft Dynamics Lifecycle Services (LCS) portālu, varat izveidot savu pirmo e-komercijas vietni.</span><span class="sxs-lookup"><span data-stu-id="4adde-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="4adde-106">Sākotnēji veidojot vietni, jūs saistiet vietni ar iepriekš izveidoto tiešsaistes veikalu.</span><span class="sxs-lookup"><span data-stu-id="4adde-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="4adde-107">Šī darbība piesaista vietni tiešsaistes kanālam un ļauj vietnei rādīt navigācijas hierarhiju, preces, kategorijas, cenas, piegādes opcijas un visu pārējo, kas definēts tiešsaistes veikalā.</span><span class="sxs-lookup"><span data-stu-id="4adde-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="4adde-108">Lai izveidotu jaunu vietni un saistītu ar to tiešsaistes veikalu, pakalpojumā LCS atlasiet saiti uz vietnes autorēšanas vidi.</span><span class="sxs-lookup"><span data-stu-id="4adde-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="4adde-109">Pēc tam vietnes autorēšanas vides lapā atlasiet **Jauna vietne**.</span><span class="sxs-lookup"><span data-stu-id="4adde-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="4adde-110">Dialoglodziņā **Jauna vietne** ir jānorāda pamatinformācija par savu vietni.</span><span class="sxs-lookup"><span data-stu-id="4adde-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="4adde-111">Lai iegūtu pilnīgu skaidrojumu par sniedzamo informāciju, skatiet tēmu [Jaunas e-komercijas vietnes izveide](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="4adde-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="4adde-112">Pēc vietnes izveides varat pārbaudīt, vai tā ir saistīta ar jūsu tiešsaistes veikalu, atlasot cilni **Preces**. Jābūt redzamam preču klāstam, kas tika piešķirts tiešsaistes veikalam.</span><span class="sxs-lookup"><span data-stu-id="4adde-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="4adde-113">Lai piekļūtu precēm pēc kategorijas, varat arī izmantot nolaižamo lauku lapas augšējā kreisajā malā.</span><span class="sxs-lookup"><span data-stu-id="4adde-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4adde-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4adde-114">Additional resources</span></span>

[<span data-ttu-id="4adde-115">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="4adde-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4adde-116">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="4adde-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4adde-117">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="4adde-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4adde-118">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="4adde-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4adde-119">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="4adde-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4adde-120">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="4adde-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4adde-121">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="4adde-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4adde-122">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="4adde-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4adde-123">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="4adde-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4adde-124">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="4adde-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]