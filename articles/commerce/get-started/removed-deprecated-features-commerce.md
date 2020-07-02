---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
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
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443922"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="06a67-103">Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="06a67-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06a67-104">Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="06a67-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="06a67-105">*Noņemts* līdzeklis produktā vairs nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="06a67-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="06a67-106">*Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.</span><span class="sxs-lookup"><span data-stu-id="06a67-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="06a67-107">Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši.</span><span class="sxs-lookup"><span data-stu-id="06a67-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="06a67-108">Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="06a67-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="06a67-109">Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.</span><span class="sxs-lookup"><span data-stu-id="06a67-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="06a67-110">Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.11 laidienā</span><span class="sxs-lookup"><span data-stu-id="06a67-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="06a67-111">Datu darbību āķi</span><span class="sxs-lookup"><span data-stu-id="06a67-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="06a67-112">**Novecošanas/noņemšanas pamatojums**</span><span class="sxs-lookup"><span data-stu-id="06a67-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a67-113">Datu darbības āķu līdzeklis ir novecojis veiktspējas problēmu dēļ.</span><span class="sxs-lookup"><span data-stu-id="06a67-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="06a67-114">**Vai ir aizstāts ar citu līdzekli?**</span><span class="sxs-lookup"><span data-stu-id="06a67-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a67-115">Ieteicams tā vietā izmantot [datu darbību ignorēšanu](../e-commerce-extensibility/data-action-overrides.md), lai mainītu biznesa loģiku datu darbības līmenī.</span><span class="sxs-lookup"><span data-stu-id="06a67-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="06a67-116">**Ietekmētie produkta apgabali**</span><span class="sxs-lookup"><span data-stu-id="06a67-116">**Product areas affected**</span></span>         | <span data-ttu-id="06a67-117">E-komercijas paplašināmības datu darbības</span><span class="sxs-lookup"><span data-stu-id="06a67-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="06a67-118">**Izvietošanas iespēja**</span><span class="sxs-lookup"><span data-stu-id="06a67-118">**Deployment option**</span></span>              | <span data-ttu-id="06a67-119">Visu</span><span class="sxs-lookup"><span data-stu-id="06a67-119">All</span></span> |
| <span data-ttu-id="06a67-120">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="06a67-120">**Status**</span></span>                         | <span data-ttu-id="06a67-121">Novecojis: sākot ar 10.0.11. laidienu</span><span class="sxs-lookup"><span data-stu-id="06a67-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="06a67-122">Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.10 laidienā</span><span class="sxs-lookup"><span data-stu-id="06a67-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="06a67-123">POS operācija 803 - izdošana un saņemšana</span><span class="sxs-lookup"><span data-stu-id="06a67-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="06a67-124">**Novecošanas/noņemšanas pamatojums**</span><span class="sxs-lookup"><span data-stu-id="06a67-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a67-125">Izdošanas un saņemšanas darbības ir novecojušas jaunas operācijas pārprojektēšanas dēļ.</span><span class="sxs-lookup"><span data-stu-id="06a67-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="06a67-126">**Vai ir aizstāts ar citu līdzekli?**</span><span class="sxs-lookup"><span data-stu-id="06a67-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a67-127">Jā.</span><span class="sxs-lookup"><span data-stu-id="06a67-127">Yes.</span></span> <span data-ttu-id="06a67-128">To aizvieto ar divām jaunām POS operācijām: saņemšanas operācija (804) un izejošā operācija (805).</span><span class="sxs-lookup"><span data-stu-id="06a67-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="06a67-129">**Ietekmētie produkta apgabali**</span><span class="sxs-lookup"><span data-stu-id="06a67-129">**Product areas affected**</span></span>         | <span data-ttu-id="06a67-130">Pārdošanas punktu (POS) lietojumprogramma</span><span class="sxs-lookup"><span data-stu-id="06a67-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="06a67-131">**Izvietošanas iespēja**</span><span class="sxs-lookup"><span data-stu-id="06a67-131">**Deployment option**</span></span>              | <span data-ttu-id="06a67-132">Visu</span><span class="sxs-lookup"><span data-stu-id="06a67-132">All</span></span> |
| <span data-ttu-id="06a67-133">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="06a67-133">**Status**</span></span>                         | <span data-ttu-id="06a67-134">Novecojis: ar 10.0.10 versijas izlaišanu izdošanas un saņemšanas operācija vairs nesaņems jaunus līdzekļu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="06a67-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="06a67-135">Turpmākajos laidienos tiks veikti tikai kritiski kļūdu labojumi šai operācijai.</span><span class="sxs-lookup"><span data-stu-id="06a67-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="06a67-136">Visi klienti tiek mudināti pāriet uz jaunajām [ienākošajām operācijām](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) un [izejošajām operācijām](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kas joprojām būs daļa no mūsu ilgtermiņa preču ceļveža.</span><span class="sxs-lookup"><span data-stu-id="06a67-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="06a67-137">Noņemtie vai novecojuši līdzekļi programmas Commerce 10.0.7 laidienā</span><span class="sxs-lookup"><span data-stu-id="06a67-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="06a67-138">Commerce GetProductAvailabilities un GetAvailableInventoryNearby API</span><span class="sxs-lookup"><span data-stu-id="06a67-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="06a67-139">**Novecošanas/noņemšanas pamatojums**</span><span class="sxs-lookup"><span data-stu-id="06a67-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="06a67-140">Jaunie, optimizētie API ir izveidoti, lai aizstātu GetProductAvailabilities un GetAvailableInventoryNearby API.</span><span class="sxs-lookup"><span data-stu-id="06a67-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="06a67-141">**Vai ir aizstāts ar citu līdzekli?**</span><span class="sxs-lookup"><span data-stu-id="06a67-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="06a67-142">Jā: tas ir aizstāts ar GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API.</span><span class="sxs-lookup"><span data-stu-id="06a67-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="06a67-143">**Ietekmētie produkta apgabali**</span><span class="sxs-lookup"><span data-stu-id="06a67-143">**Product areas affected**</span></span>         | <span data-ttu-id="06a67-144">e-komercijas programmas SDK</span><span class="sxs-lookup"><span data-stu-id="06a67-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="06a67-145">**Izvietošanas iespēja**</span><span class="sxs-lookup"><span data-stu-id="06a67-145">**Deployment option**</span></span>              | <span data-ttu-id="06a67-146">Visu</span><span class="sxs-lookup"><span data-stu-id="06a67-146">All</span></span> |
| <span data-ttu-id="06a67-147">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="06a67-147">**Status**</span></span>                         | <span data-ttu-id="06a67-148">Novecojis: ar 10.0.7 versijas izlaišanu vairs netiks izveidotas inženierijas investīcijas, kas paredzētas GetProductAvailabilities un GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="06a67-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="06a67-149">Organizācijas, kas izmanto šos API savās e-komercijas izvietošanās, ir jāpāriet uz jaunajiem GetEstimatedAvailability un GetEstimatedProductWarehouseAvailability API un jāaktivizē [Optimizētā preču pieejamības aprēķināšanas funkcija](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="06a67-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="06a67-150">Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="06a67-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="06a67-151">Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="06a67-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
