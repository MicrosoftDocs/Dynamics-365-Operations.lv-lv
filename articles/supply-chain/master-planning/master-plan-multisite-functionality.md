---
title: Vispārējas plānošanas un vairākvietu funkcionalitātes pārskats
description: Vispārējā plānošanā tiek ņemti vērā vietas iestatījumi un noliktavas krājumu dimensijas.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865412"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="f78dd-103">Vispārējas plānošanas un vairākvietu funkcionalitātes pārskats</span><span class="sxs-lookup"><span data-stu-id="f78dd-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f78dd-104">Vispārējā plānošanā tiek ņemti vērā vietas iestatījumi un noliktavas krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="f78dd-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="f78dd-105">Vietas dimensija ir obligāta, un varat iestatīt, lai noliktavas dimensija būtu obligāta.</span><span class="sxs-lookup"><span data-stu-id="f78dd-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="f78dd-106">Kad dimensija ir obligāta, dimensijas lielumu jāievada visās krājuma darbībās.</span><span class="sxs-lookup"><span data-stu-id="f78dd-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="f78dd-107">Tādējādi vispārējās plānošanas laikā sākotnējam pieprasījumam ir zināma vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="f78dd-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="f78dd-108">Vietas dimensija ir savienojama tā, ka arī zemākā līmeņa pieprasījuma izvēršanas laikā vietas lielums nemainās.</span><span class="sxs-lookup"><span data-stu-id="f78dd-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="f78dd-109">Kad noliktava nav iestatīta kā obligāta, tā var nebūt zināma sākotnējā pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="f78dd-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="f78dd-110">Plānošanas dzinim jānosaka, kādu noliktava izmantot, pamatojoties uz iestatījumiem, kas definēti vienībai, atsevišķām noliktavām un pasūtījuma rindas detaļām.</span><span class="sxs-lookup"><span data-stu-id="f78dd-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="f78dd-111">Tālāk sniegtajās tēmās ir aprakstīts, kā plānot dziņa darbus, ja izmantojamās noliktavas noteikšanai definēti dažādi iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="f78dd-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="f78dd-112">Vispārējā plānošana — vietas un noliktavas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="f78dd-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f78dd-113">Vispārējā plānošana — vietas segums, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="f78dd-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f78dd-114">Vispārējā plānošana — vietas un noliktavas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="f78dd-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f78dd-115">Vispārējā plānošana — vietas segums, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="f78dd-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f78dd-116">Vispārējā plānošana — kā tiek noteikta MK versija</span><span class="sxs-lookup"><span data-stu-id="f78dd-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



