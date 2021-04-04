---
title: Integrētās vietas un noliktavas
description: Šajā tēmā ir aprakstīta vietas un noliktavas datu integrācija starp programmām Finance and Operations un Dataverse
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560365"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="b50b7-103">Integrētās vietas un noliktavas</span><span class="sxs-lookup"><span data-stu-id="b50b7-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b50b7-104">Šajā tēmā ir aprakstīta vietas un noliktavas datu integrācija starp programmām Finance and Operations un Dataverse</span><span class="sxs-lookup"><span data-stu-id="b50b7-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="b50b7-105">Darbības vietas un noliktavas ir bieži lietotie jēdzieni Supply Chain Management programmā.</span><span class="sxs-lookup"><span data-stu-id="b50b7-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="b50b7-106">Tie ir izmantoti, lai izveidotu jūsu uzņēmuma piegādes ķēdes modeli.</span><span class="sxs-lookup"><span data-stu-id="b50b7-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="b50b7-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="b50b7-107">Templates</span></span>

<span data-ttu-id="b50b7-108">Pateicoties integrācijai ar programmu Dataverse šie jēdzieni un ar tiem saistītā informācija ir pieejami programmā Dataverse, izmantojot vietu un noliktavas datu tabulas tālāk redzamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="b50b7-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="b50b7-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="b50b7-109">Finance and Operations apps</span></span> | <span data-ttu-id="b50b7-110">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="b50b7-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b50b7-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b50b7-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="b50b7-112">Atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="b50b7-112">Sites</span></span> | <span data-ttu-id="b50b7-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="b50b7-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="b50b7-114">Noliktavas</span><span class="sxs-lookup"><span data-stu-id="b50b7-114">Warehouses</span></span> | <span data-ttu-id="b50b7-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="b50b7-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]