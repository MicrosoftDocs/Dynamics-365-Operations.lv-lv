---
title: Integrētās vietas un noliktavas
description: Šajā tēmā ir aprakstīta vietas un noliktavas datu integrācija starp programmām Finance and Operations un Common Data Service
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997628"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="2eb49-103">Integrētās vietas un noliktavas</span><span class="sxs-lookup"><span data-stu-id="2eb49-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2eb49-104">Šajā tēmā ir aprakstīta vietas un noliktavas datu integrācija starp programmām Finance and Operations un Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2eb49-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="2eb49-105">Darbības vietas un noliktavas ir bieži lietotie jēdzieni Supply Chain Management programmā.</span><span class="sxs-lookup"><span data-stu-id="2eb49-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="2eb49-106">Tie ir izmantoti, lai izveidotu jūsu uzņēmuma piegādes ķēdes modeli.</span><span class="sxs-lookup"><span data-stu-id="2eb49-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="2eb49-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="2eb49-107">Templates</span></span>

<span data-ttu-id="2eb49-108">Pateicoties integrācijai ar programmu Common Data Service šie jēdzieni un ar tiem saistītā informācija ir pieejami programmā Common Data Service, izmantojot vietu un noliktavas datu elementus tālāk redzamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="2eb49-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="2eb49-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="2eb49-109">Finance and Operations apps</span></span> | <span data-ttu-id="2eb49-110">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="2eb49-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="2eb49-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="2eb49-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="2eb49-112">Atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="2eb49-112">Sites</span></span> | <span data-ttu-id="2eb49-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="2eb49-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="2eb49-114">Noliktavas</span><span class="sxs-lookup"><span data-stu-id="2eb49-114">Warehouses</span></span> | <span data-ttu-id="2eb49-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="2eb49-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

