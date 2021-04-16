---
title: Vispārējas plānošanas un vairākvietu funkcionalitātes pārskats
description: Vispārējā plānošanā tiek ņemti vērā vietas iestatījumi un noliktavas krājumu dimensijas.
author: roxanadiaconu
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30bb8dfb790958b30cb3be807847ee737fb5026
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833573"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="fba9d-103">Vispārējas plānošanas un vairākvietu funkcionalitātes pārskats</span><span class="sxs-lookup"><span data-stu-id="fba9d-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fba9d-104">Vispārējā plānošanā tiek ņemti vērā vietas iestatījumi un noliktavas krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="fba9d-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="fba9d-105">Vietas dimensija ir obligāta, un varat iestatīt, lai noliktavas dimensija būtu obligāta.</span><span class="sxs-lookup"><span data-stu-id="fba9d-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="fba9d-106">Kad dimensija ir obligāta, dimensijas lielumu jāievada visās krājuma darbībās.</span><span class="sxs-lookup"><span data-stu-id="fba9d-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="fba9d-107">Tādējādi vispārējās plānošanas laikā sākotnējam pieprasījumam ir zināma vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="fba9d-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="fba9d-108">Vietas dimensija ir savienojama tā, ka arī zemākā līmeņa pieprasījuma izvēršanas laikā vietas lielums nemainās.</span><span class="sxs-lookup"><span data-stu-id="fba9d-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="fba9d-109">Kad noliktava nav iestatīta kā obligāta, tā var nebūt zināma sākotnējā pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="fba9d-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="fba9d-110">Plānošanas programmai jānosaka, kādu noliktava izmantot, pamatojoties uz iestatījumiem, kas definēti vienībai, atsevišķām noliktavām un pasūtījuma rindas detaļām.</span><span class="sxs-lookup"><span data-stu-id="fba9d-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="fba9d-111">Tālāk sniegtajās tēmās ir aprakstīts, kā plānot dziņa darbus, ja izmantojamās noliktavas noteikšanai definēti dažādi iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="fba9d-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="fba9d-112">Galvenais plāns vietas un noliktavas segumam, noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="fba9d-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="fba9d-113">Vietas seguma vispārējā plānošana, ja noliktava ir obligāta</span><span class="sxs-lookup"><span data-stu-id="fba9d-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="fba9d-114">Galvenais plāns vietas un noliktavas segumam, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="fba9d-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="fba9d-115">Vietas seguma vispārējā plānošana, noliktava nav obligāta</span><span class="sxs-lookup"><span data-stu-id="fba9d-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="fba9d-116">MK versijas noteikšana</span><span class="sxs-lookup"><span data-stu-id="fba9d-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]