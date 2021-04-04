---
title: Izslēgt pamatlīdzekļus kā norakstītos
description: Tēmā ir aprakstīts process, kurā tiek likvidētas transakcijas pamatlīdzeklim, kas noņemts kā brāķis.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 20f5fe0f8f2654df5027c363ebf5922f8344d928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241126"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="f470f-103">Izslēgt pamatlīdzekļus kā norakstītos</span><span class="sxs-lookup"><span data-stu-id="f470f-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f470f-104">Tēmā ir aprakstīts process, kurā tiek likvidētas transakcijas pamatlīdzeklim, kas noņemts kā brāķis.</span><span class="sxs-lookup"><span data-stu-id="f470f-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="f470f-105">Transakciju veidi, kurus var likvidēt, ietver pamatlīdzekļa iegādi un uzkrātā nolietojuma transakcijas un citas pamatlīdzekļu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="f470f-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="f470f-106">Šo darbību likvidēšana ietekmē bilances kontus, piemēram, iegādes korekciju, nolietojuma korekciju, pārvērtēšanu, vērtības palielināšanu un vērtības samazināšanu.</span><span class="sxs-lookup"><span data-stu-id="f470f-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="f470f-107">Darījums</span><span class="sxs-lookup"><span data-stu-id="f470f-107">Transaction</span></span>                                         | <span data-ttu-id="f470f-108">Debets (Dr.)</span><span class="sxs-lookup"><span data-stu-id="f470f-108">Debit (Dr.)</span></span> | <span data-ttu-id="f470f-109">Kredīts (Kr.)</span><span class="sxs-lookup"><span data-stu-id="f470f-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="f470f-110">Dr. Uzkrātais nolietojums.</span><span class="sxs-lookup"><span data-stu-id="f470f-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="f470f-111">X</span><span class="sxs-lookup"><span data-stu-id="f470f-111">X</span></span>           |              |
| <span data-ttu-id="f470f-112">Kr. Pamatlīdzekļu peļņa/zaudējumi</span><span class="sxs-lookup"><span data-stu-id="f470f-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="f470f-113">X</span><span class="sxs-lookup"><span data-stu-id="f470f-113">X</span></span>            |
| <span data-ttu-id="f470f-114">Dr. Pamatlīdzekļu peļņa/zaudējumi</span><span class="sxs-lookup"><span data-stu-id="f470f-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="f470f-115">X</span><span class="sxs-lookup"><span data-stu-id="f470f-115">X</span></span>           |              |
| <span data-ttu-id="f470f-116">Kr. Pamatlīdzekļu ieguves konti</span><span class="sxs-lookup"><span data-stu-id="f470f-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="f470f-117">X</span><span class="sxs-lookup"><span data-stu-id="f470f-117">X</span></span>            |
| <span data-ttu-id="f470f-118">Dr. Pamatlīdzekļu peļņa/zaudējumi (atlikusī vērtība \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="f470f-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="f470f-119">X</span><span class="sxs-lookup"><span data-stu-id="f470f-119">X</span></span>           |              |
| <span data-ttu-id="f470f-120">Kr. Pamatlīdzekļu peļņa/zaudējumi (NBV)</span><span class="sxs-lookup"><span data-stu-id="f470f-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="f470f-121">X</span><span class="sxs-lookup"><span data-stu-id="f470f-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="f470f-122">Iesakām cieši sadarboties ar uzņēmuma galveno finanšu darbinieku (CFO) vai kontrolieri, lai identificētu pareizos kontus, kas jāizmanto katram transakcijas veidam, kā arī pārbaudīt, vai likvidēšanas process un transakcijas, ko tas ģenerē, atjauninā šos kontus pareizi.</span><span class="sxs-lookup"><span data-stu-id="f470f-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="f470f-123">Pirms pamatlīdzekļa likvidēsanas kā brāķa, ir jāizveido virsgrāmatas konts, kas ir saistīts ar pamatlīdzekļa iegādes vērtību, nolietojumu pašreizējam gadam, nolietojumu iepriekšējos gados un pamatlīdzekļa NBV.</span><span class="sxs-lookup"><span data-stu-id="f470f-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="f470f-124">Pamatlīdzekļu transakciju veidi ir uzskaitīti **Pamatlīdzekļu grāmatošanas profila** lapā.</span><span class="sxs-lookup"><span data-stu-id="f470f-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="f470f-125">Dodieties uz **Pamatlīdzekļi \> Iestatīšanas \> Pamatlīdzekļu grāmatošanas metodes** un pēc tam kopsavilkuma cilnē **Likvidēšana** atlasiet **Brāķis** laukā virs režģa.</span><span class="sxs-lookup"><span data-stu-id="f470f-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="f470f-126">Sekojošajā attēlā ir redzams pamatlīdzekļu transakciju veidu saraksts **Pamatlīdzekļu grāmatošanas profile** lapā.</span><span class="sxs-lookup"><span data-stu-id="f470f-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="f470f-127">[![Pamatlīdzekļa likvidēšana kā brāķa, 1. attēls](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="f470f-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="f470f-128">Šim piemēram, pamatlīdzeklis tika iegādāts 2018. gada 1. janvārī, un tas tiks likvidēts 2019. gada 31. martā.</span><span class="sxs-lookup"><span data-stu-id="f470f-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="f470f-129">**Iegādes cena:** 24 000,00 ASV dolāri (USD)</span><span class="sxs-lookup"><span data-stu-id="f470f-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="f470f-130">**Lietošanas ilgums:** Divi gadi</span><span class="sxs-lookup"><span data-stu-id="f470f-130">**Service life:** Two years</span></span>
- <span data-ttu-id="f470f-131">**Nolietojuma metode:** lineārais lietošanas ilgums</span><span class="sxs-lookup"><span data-stu-id="f470f-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="f470f-132">**Nolietojuma daudzums:** 1 000,00 USD mēnesī</span><span class="sxs-lookup"><span data-stu-id="f470f-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="f470f-133">Pamatlīdzekļa NBV tiek aprēķināts, izmantojot šādu formulu:</span><span class="sxs-lookup"><span data-stu-id="f470f-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="f470f-134">Atlikusī vērtība = Iegādes cena — Nolietojums</span><span class="sxs-lookup"><span data-stu-id="f470f-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="f470f-135">Šajā piemērā pamatlīdzeklis tika iegādāts un tika nolietots 15 mēnešu laikā no 2018. līdz 2019. gada martam.</span><span class="sxs-lookup"><span data-stu-id="f470f-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="f470f-136">Tāpēc pamatlīdzekļa NBV ir 9 000,00 USD (24 000,00 USD – 15 000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="f470f-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="f470f-137">[![Pamatlīdzekļa nolietojuma piemērs](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="f470f-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="f470f-138">Lai izveidotu likvidēšanas žurnālu, atveriet **Pamatlīdzekļi \> Žurnāla ieraksti \> Pamatlīdzekļu žurnāls** un pēc tam Darbības rūtī atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="f470f-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="f470f-139">Atlasiet **Likvidēšana— brāķis**, pēc tam atlasiet pamatlīdzekļa ID.</span><span class="sxs-lookup"><span data-stu-id="f470f-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="f470f-140">Lai pilnībā likvidētu pamatlīdzekli, neievadiet vērtību laukā **Debets** vai laukā **Kredīts**.</span><span class="sxs-lookup"><span data-stu-id="f470f-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="f470f-141">[![Pamatlīdzekļu žurnāls](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="f470f-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="f470f-142">Pamatlīdzekļa likvidēšanas transakcija brāķa dēļ maina pamatlīdzekļu grāmatas lauka vērtības šādos veidos:</span><span class="sxs-lookup"><span data-stu-id="f470f-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="f470f-143">Sadaļā **Bilance** lauks **Statuss** tiek atjaunināts uz **Brāķēts**.</span><span class="sxs-lookup"><span data-stu-id="f470f-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="f470f-144">Sadaļā **Izsniegšana** lauks **Likvidēšanas datums** tiek iestatīts uz datumu, kad pamatlīdzeklis tika norakstīts.</span><span class="sxs-lookup"><span data-stu-id="f470f-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="f470f-145">[![Detalizēta informācija par amatlīdzekļu žurnālu](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="f470f-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="f470f-146">Sekojošajā attēlā ir redzama pamatlīdzekļa bilance.</span><span class="sxs-lookup"><span data-stu-id="f470f-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="f470f-147">[![Pamatlīdzekļu bilance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="f470f-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="f470f-148">Sekojošajā attēlā ir redzams grāmatots dokuments.</span><span class="sxs-lookup"><span data-stu-id="f470f-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="f470f-149">[![Atlikusī vērtība](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="f470f-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]