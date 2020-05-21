---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335280"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="b4aeb-103">Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b4aeb-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4aeb-104">Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="b4aeb-105">*Noņemts* līdzeklis produktā vairs nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b4aeb-106">*Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b4aeb-107">Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="b4aeb-108">Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="b4aeb-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="b4aeb-109">Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="b4aeb-110">Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.10 laidienā</span><span class="sxs-lookup"><span data-stu-id="b4aeb-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="b4aeb-111">POS operācija 803 - izdošana un saņemšana</span><span class="sxs-lookup"><span data-stu-id="b4aeb-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b4aeb-112">**Novecošanas/noņemšanas pamatojums**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b4aeb-113">Izdošanas un saņemšanas darbības ir novecojušas jaunas operācijas pārprojektēšanas dēļ.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="b4aeb-114">**Vai ir aizstāts ar citu līdzekli?**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b4aeb-115">Jā.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-115">Yes.</span></span> <span data-ttu-id="b4aeb-116">To aizvieto ar divām jaunām POS operācijām: saņemšanas operācija (804) un izejošā operācija (805).</span><span class="sxs-lookup"><span data-stu-id="b4aeb-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="b4aeb-117">**Ietekmētie produkta apgabali**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-117">**Product areas affected**</span></span>         | <span data-ttu-id="b4aeb-118">Pārdošanas punktu (POS) lietojumprogramma</span><span class="sxs-lookup"><span data-stu-id="b4aeb-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="b4aeb-119">**Izvietošanas iespēja**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-119">**Deployment option**</span></span>              | <span data-ttu-id="b4aeb-120">Visu</span><span class="sxs-lookup"><span data-stu-id="b4aeb-120">All</span></span> |
| <span data-ttu-id="b4aeb-121">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-121">**Status**</span></span>                         | <span data-ttu-id="b4aeb-122">Novecojis: ar 10.0.10 versijas izlaišanu izdošanas un saņemšanas operācija vairs nesaņems jaunus līdzekļu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="b4aeb-123">Turpmākajos laidienos tiks veikti tikai kritiski kļūdu labojumi šai operācijai.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="b4aeb-124">Visi klienti tiek mudināti pāriet uz jaunajām [ienākošajām operācijām](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) un [izejošajām operācijām](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kas joprojām būs daļa no mūsu ilgtermiņa preču ceļveža.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="b4aeb-125">Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.7 laidienā</span><span class="sxs-lookup"><span data-stu-id="b4aeb-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="b4aeb-126">Commerce GetProductAvailabilities un GetAvailableInventoryNearby API</span><span class="sxs-lookup"><span data-stu-id="b4aeb-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b4aeb-127">**Novecošanas/noņemšanas pamatojums**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b4aeb-128">Jaunie, optimizētie API ir izveidoti, lai aizstātu GetProductAvailabilities un GetAvailableInventoryNearby API.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="b4aeb-129">**Vai ir aizstāts ar citu līdzekli?**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b4aeb-130">Jā: tas ir aizstāts ar GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="b4aeb-131">**Ietekmētie produkta apgabali**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-131">**Product areas affected**</span></span>         | <span data-ttu-id="b4aeb-132">e-komercijas programmas SDK</span><span class="sxs-lookup"><span data-stu-id="b4aeb-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="b4aeb-133">**Izvietošanas iespēja**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-133">**Deployment option**</span></span>              | <span data-ttu-id="b4aeb-134">Visu</span><span class="sxs-lookup"><span data-stu-id="b4aeb-134">All</span></span> |
| <span data-ttu-id="b4aeb-135">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="b4aeb-135">**Status**</span></span>                         | <span data-ttu-id="b4aeb-136">Novecojis: ar 10.0.7 versijas izlaišanu vairs netiks izveidotas inženierijas investīcijas, kas paredzētas GetProductAvailabilities un GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="b4aeb-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="b4aeb-137">Organizācijas, kas izmanto šos API savās e-komercijas izvietošanās, ir jāpāriet uz jaunajiem GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API un jāaktivizē [Optimizētā preču pieejamības aprēķināšanas funkcija](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="b4aeb-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="b4aeb-138">Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="b4aeb-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="b4aeb-139">Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b4aeb-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
