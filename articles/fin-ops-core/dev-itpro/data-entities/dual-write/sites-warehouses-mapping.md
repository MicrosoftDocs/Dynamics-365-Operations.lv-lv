---
title: Integrētās vietas un noliktavas
description: Šajā tēmā ir aprakstīta vietas un noliktavas datu integrācija starp programmām Finance and Operations un Dataverse
author: t-benebo
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750670"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="0d06f-103">Integrētās vietas un noliktavas</span><span class="sxs-lookup"><span data-stu-id="0d06f-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0d06f-104">Šajā tēmā ir aprakstīta vietas un noliktavas datu integrācija starp programmām Finance and Operations un Dataverse</span><span class="sxs-lookup"><span data-stu-id="0d06f-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="0d06f-105">Darbības vietas un noliktavas ir bieži lietotie jēdzieni Supply Chain Management programmā.</span><span class="sxs-lookup"><span data-stu-id="0d06f-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="0d06f-106">Tie ir izmantoti, lai izveidotu jūsu uzņēmuma piegādes ķēdes modeli.</span><span class="sxs-lookup"><span data-stu-id="0d06f-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="0d06f-107">Veidnes</span><span class="sxs-lookup"><span data-stu-id="0d06f-107">Templates</span></span>

<span data-ttu-id="0d06f-108">Pateicoties integrācijai ar programmu Dataverse šie jēdzieni un ar tiem saistītā informācija ir pieejami programmā Dataverse, izmantojot vietu un noliktavas datu tabulas tālāk redzamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0d06f-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="0d06f-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="0d06f-109">Finance and Operations apps</span></span> | <span data-ttu-id="0d06f-110">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="0d06f-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0d06f-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="0d06f-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="0d06f-112">Atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="0d06f-112">Sites</span></span> | <span data-ttu-id="0d06f-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="0d06f-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="0d06f-114">Noliktavas</span><span class="sxs-lookup"><span data-stu-id="0d06f-114">Warehouses</span></span> | <span data-ttu-id="0d06f-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="0d06f-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]