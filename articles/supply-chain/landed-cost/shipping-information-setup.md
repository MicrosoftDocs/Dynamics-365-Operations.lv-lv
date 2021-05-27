---
title: Informācijas par nosūtīšanu iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt piegādes informāciju Kopējo izmaksu modulim.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020891"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="12c47-103">Informācijas par nosūtīšanu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="12c47-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12c47-104">Šajā tēmā ir aprakstīts, kā iestatīt piegādes informāciju **Kopējo izmaksu** modulim.</span><span class="sxs-lookup"><span data-stu-id="12c47-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="12c47-105">Preču apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-105">Description of goods</span></span>

<span data-ttu-id="12c47-106">Preču apraksti palīdz identificēt reisu, nosūtīšanas konteineru vai preču folio un tajā uzglabātās preces.</span><span class="sxs-lookup"><span data-stu-id="12c47-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="12c47-107">Preču aprakstu var atlasīt nosūtīšanas konteinerā vai folio galvenē.</span><span class="sxs-lookup"><span data-stu-id="12c47-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="12c47-108">Lai strādātu ar preču aprakstiem, dodieties uz **Kopējās izmaksas \> Nosūtīšanas informācijas iestatījumi \> Preču apraksts**.</span><span class="sxs-lookup"><span data-stu-id="12c47-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="12c47-109">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst preču aprakstu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="12c47-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="12c47-110">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="12c47-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="12c47-111">Lauks</span><span class="sxs-lookup"><span data-stu-id="12c47-111">Field</span></span> | <span data-ttu-id="12c47-112">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-112">Description</span></span> |
|---|---|
| <span data-ttu-id="12c47-113">Preču apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-113">Description of goods</span></span> | <span data-ttu-id="12c47-114">Ievadiet unikālu identifikācijas nosaukumu/numuru preču tipam, kas izmantos šo aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="12c47-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-115">Description</span></span> | <span data-ttu-id="12c47-116">Ievadiet šajā kategorijā preču tipa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="12c47-117">Kuģis</span><span class="sxs-lookup"><span data-stu-id="12c47-117">Vessels</span></span>

<span data-ttu-id="12c47-118">Kuģis ir unikāls nosūtīšanas vai kuģa nosaukums, ko izmanto kravu nosūtīšanas uzņēmums vai aģentūra.</span><span class="sxs-lookup"><span data-stu-id="12c47-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="12c47-119">Kad izveidojat reisu, tam vienmēr ir jāatlasa vai jāievada kuģis.</span><span class="sxs-lookup"><span data-stu-id="12c47-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="12c47-120">Ja bieži izmantojat vienu un to pašu, tad ir iespējams ātrāk un vieglāk izveidot jaunu reisu, izveidojot kuģa ierakstu katram no tiem, tādējādi ļaujot lietotājiem izvēlēties kuģi no saraksta, nevis katru reizi ievadīt nosaukumu vai numuru manuāli.</span><span class="sxs-lookup"><span data-stu-id="12c47-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="12c47-121">Lai strādātu ar nosūtīšanas ostām, dodieties uz sadaļu **Kopējās izmaksas \> Piegādes informācijas iestatīšana \> Kuģi**.</span><span class="sxs-lookup"><span data-stu-id="12c47-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="12c47-122">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ierakstus par kuģiem.</span><span class="sxs-lookup"><span data-stu-id="12c47-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="12c47-123">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="12c47-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="12c47-124">Lauks</span><span class="sxs-lookup"><span data-stu-id="12c47-124">Field</span></span> | <span data-ttu-id="12c47-125">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-125">Description</span></span> |
|---|---|
| <span data-ttu-id="12c47-126">Kuģis</span><span class="sxs-lookup"><span data-stu-id="12c47-126">Vessel</span></span> | <span data-ttu-id="12c47-127">Ievadiet unikālu identifikācijas nosaukumu/numuru nosūtīšanai, kas tiks izmantota preču transportēšanai reisā.</span><span class="sxs-lookup"><span data-stu-id="12c47-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="12c47-128">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-128">Description</span></span> | <span data-ttu-id="12c47-129">Ievadiet kuģa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-129">Enter a description of the vessel.</span></span> <span data-ttu-id="12c47-130">Parasti šis apraksts identificē nosūtīšanas un nosūtīšanas uzņēmuma/aģenta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="12c47-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="12c47-131">Piegādes veids</span><span class="sxs-lookup"><span data-stu-id="12c47-131">Mode of delivery</span></span> | <span data-ttu-id="12c47-132">Atlasiet kuģa izmantoto piegādes veidu (piemēram, _gaiss_, _okeāns_ vai _vilciens_).</span><span class="sxs-lookup"><span data-stu-id="12c47-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="12c47-133">Eksportētāji</span><span class="sxs-lookup"><span data-stu-id="12c47-133">Exporters</span></span>

<span data-ttu-id="12c47-134">Katrs eksportētāja ieraksts norāda kreditoru vai eksportētāju, ko var definēt kā reisa kreditoru.</span><span class="sxs-lookup"><span data-stu-id="12c47-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="12c47-135">Eksportētāju var saistīt ar reisu un izmantot pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="12c47-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="12c47-136">Lai strādātu ar eksportētājiem, dodieties uz **Kopējās izmaksas \> Piegādes informācijas iestatīšana \> Eksportētāji**.</span><span class="sxs-lookup"><span data-stu-id="12c47-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="12c47-137">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ierakstus par eksportētājiem.</span><span class="sxs-lookup"><span data-stu-id="12c47-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="12c47-138">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="12c47-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="12c47-139">Lauks</span><span class="sxs-lookup"><span data-stu-id="12c47-139">Field</span></span> | <span data-ttu-id="12c47-140">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-140">Description</span></span> |
|---|---|
| <span data-ttu-id="12c47-141">Eksportētājs</span><span class="sxs-lookup"><span data-stu-id="12c47-141">Exporter</span></span> | <span data-ttu-id="12c47-142">Ievadiet unikālu identifikācijas nosaukumu/numuru, lai eksportētu reisā transportējamās preces.</span><span class="sxs-lookup"><span data-stu-id="12c47-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="12c47-143">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-143">Description</span></span> | <span data-ttu-id="12c47-144">Ievadiet eksportētāja aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-144">Enter a description of the exporter.</span></span> <span data-ttu-id="12c47-145">Parasti šis apraksts identificē pilnu nosūtīšanas uzņēmuma/aģenta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="12c47-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="12c47-146">Preču kodi</span><span class="sxs-lookup"><span data-stu-id="12c47-146">Commodity codes</span></span>

<span data-ttu-id="12c47-147">Preču kodi tiek lietoti, lai palīdzētu ar muitas identifikāciju un nodokļu likmju aprēķināšanu precēm reisā.</span><span class="sxs-lookup"><span data-stu-id="12c47-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="12c47-148">Lai atlasītu preču kodus lapā **Izlaistās preces**, varat atlasīt preču kodus.</span><span class="sxs-lookup"><span data-stu-id="12c47-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="12c47-149">Lai strādātu ar preču kodiem, dodieties uz **Kopējās izmaksas \> Piegādes informācijas iestatīšana \> Preču kodi**.</span><span class="sxs-lookup"><span data-stu-id="12c47-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="12c47-150">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst preču kodu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="12c47-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="12c47-151">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="12c47-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="12c47-152">Lauks</span><span class="sxs-lookup"><span data-stu-id="12c47-152">Field</span></span> | <span data-ttu-id="12c47-153">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-153">Description</span></span> |
|---|---|
| <span data-ttu-id="12c47-154">Preču kods</span><span class="sxs-lookup"><span data-stu-id="12c47-154">Commodity code</span></span> | <span data-ttu-id="12c47-155">Ievadiet šī veida preces unikālo kodu.</span><span class="sxs-lookup"><span data-stu-id="12c47-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="12c47-156">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-156">Description</span></span> | <span data-ttu-id="12c47-157">Ievadiet preces tipa aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="12c47-158">Muitošanas apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-158">Customs description</span></span>

<span data-ttu-id="12c47-159">Muitas apraksti palīdz identificēt preces muitas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="12c47-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="12c47-160">**Izlaisto preču** lapā vai pirkšanas pasūtījuma rindās varat atlasīt muitas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="12c47-161">Lai strādātu ar muitas aprakstiem, dodieties uz **Kopējās izmaksas \> Nosūtīšanas informācijas iestatījumi \> Muitas apraksts**.</span><span class="sxs-lookup"><span data-stu-id="12c47-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="12c47-162">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst muitas aprakstu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="12c47-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="12c47-163">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="12c47-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="12c47-164">Lauks</span><span class="sxs-lookup"><span data-stu-id="12c47-164">Field</span></span> | <span data-ttu-id="12c47-165">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-165">Description</span></span> |
|---|---|
| <span data-ttu-id="12c47-166">Muitošanas apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-166">Customs description</span></span> | <span data-ttu-id="12c47-167">Ievadiet šī veida muitas klasifikācijas unikālo kodu.</span><span class="sxs-lookup"><span data-stu-id="12c47-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="12c47-168">Bieži šis kods ir oficiāls apraksts, ko muitas iestāde sniedz preču aprakstam un kvalitatīvai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="12c47-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="12c47-169">Apraksts</span><span class="sxs-lookup"><span data-stu-id="12c47-169">Description</span></span> | <span data-ttu-id="12c47-170">Ievadiet muitas klasifikācijas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12c47-170">Enter a description of the customs classification.</span></span> |
