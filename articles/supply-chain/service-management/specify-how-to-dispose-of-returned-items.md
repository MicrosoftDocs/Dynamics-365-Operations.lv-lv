---
title: Noteikšana, kā atbrīvoties no atgrieztiem krājumiem
description: Nosakiet, kā atbrīvoties no atgrieztiem krājumiem.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61bff50d55ed4c251918a327f2a033369e731bf0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242377"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="e6e26-103">Noteikšana, kā atbrīvoties no atgrieztiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="e6e26-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e6e26-104">Kad apstrādājat atgriešanas pasūtījumu, jānorāda iemesla atgriešanas kods, lai noteiktu, kāpēc produkts tiek atgriezts.</span><span class="sxs-lookup"><span data-stu-id="e6e26-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="e6e26-105">Ir jānorāda arī atgriešanas metodes kods un atgriešanas metodes transakcija, lai noteiktu, kas jādara ar pašu atgriezto produktu.</span><span class="sxs-lookup"><span data-stu-id="e6e26-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="e6e26-106">Izvietojuma kodu var pielietot, ja izveidojat atgriešanas pasūtījumu, reģistrējat vienības pienākšanu vai pavadzīmes atjauninājumu vienības pienākšanai un beidzat karantīnas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e6e26-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="e6e26-107">Varat definēt jebkādus atgriešanas metodes kodus, kas nepieciešami biznesa procesu atbalstam.</span><span class="sxs-lookup"><span data-stu-id="e6e26-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="e6e26-108">Šajā tabulā sniegta parasti izmantoto kodu kopa, kas piešķirama atgriezta krājuma atgriešanas metodei.</span><span class="sxs-lookup"><span data-stu-id="e6e26-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6e26-109">Atgriešanas metodes veids</span><span class="sxs-lookup"><span data-stu-id="e6e26-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="e6e26-110">Kopējais kods</span><span class="sxs-lookup"><span data-stu-id="e6e26-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="e6e26-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e6e26-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-112">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="e6e26-113">SC</span><span class="sxs-lookup"><span data-stu-id="e6e26-113">SC</span></span></p></td>
<td><p><span data-ttu-id="e6e26-114">Utilizācija/Iznīcināšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-115">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="e6e26-116">DC</span><span class="sxs-lookup"><span data-stu-id="e6e26-116">DC</span></span></p></td>
<td><p><span data-ttu-id="e6e26-117">Ziedojuma labdarībai</span><span class="sxs-lookup"><span data-stu-id="e6e26-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-118">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="e6e26-119">TD</span><span class="sxs-lookup"><span data-stu-id="e6e26-119">TD</span></span></p></td>
<td><p><span data-ttu-id="e6e26-120">Trešās personas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-121">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="e6e26-122">SL</span><span class="sxs-lookup"><span data-stu-id="e6e26-122">SL</span></span></p></td>
<td><p><span data-ttu-id="e6e26-123">Utilizācija izejvielām</span><span class="sxs-lookup"><span data-stu-id="e6e26-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-124">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="e6e26-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="e6e26-125">TS</span><span class="sxs-lookup"><span data-stu-id="e6e26-125">TS</span></span></p></td>
<td><p><span data-ttu-id="e6e26-126">Pārdošana trešajai personai (sekundārie tirgi)</span><span class="sxs-lookup"><span data-stu-id="e6e26-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-127">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="e6e26-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="e6e26-128">RW</span><span class="sxs-lookup"><span data-stu-id="e6e26-128">RW</span></span></p></td>
<td><p><span data-ttu-id="e6e26-129">Pārstrāde</span><span class="sxs-lookup"><span data-stu-id="e6e26-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-130">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="e6e26-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="e6e26-131">RF</span><span class="sxs-lookup"><span data-stu-id="e6e26-131">RF</span></span></p></td>
<td><p><span data-ttu-id="e6e26-132">Pilnīga pārstrāde/Uzlabošana</span><span class="sxs-lookup"><span data-stu-id="e6e26-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-133">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="e6e26-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="e6e26-134">MD</span><span class="sxs-lookup"><span data-stu-id="e6e26-134">MD</span></span></p></td>
<td><p><span data-ttu-id="e6e26-135">Pārveidot</span><span class="sxs-lookup"><span data-stu-id="e6e26-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-136">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="e6e26-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="e6e26-137">RP</span><span class="sxs-lookup"><span data-stu-id="e6e26-137">RP</span></span></p></td>
<td><p><span data-ttu-id="e6e26-138">Remonts</span><span class="sxs-lookup"><span data-stu-id="e6e26-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-139">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="e6e26-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="e6e26-140">RV</span><span class="sxs-lookup"><span data-stu-id="e6e26-140">RV</span></span></p></td>
<td><p><span data-ttu-id="e6e26-141">Atgriešana kreditoram</span><span class="sxs-lookup"><span data-stu-id="e6e26-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-142">Citi</span><span class="sxs-lookup"><span data-stu-id="e6e26-142">Other</span></span></p></td>
<td><p><span data-ttu-id="e6e26-143">AI</span><span class="sxs-lookup"><span data-stu-id="e6e26-143">AI</span></span></p></td>
<td><p><span data-ttu-id="e6e26-144">Izmantot kā</span><span class="sxs-lookup"><span data-stu-id="e6e26-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-145">Cita</span><span class="sxs-lookup"><span data-stu-id="e6e26-145">Other</span></span></p></td>
<td><p><span data-ttu-id="e6e26-146">RS</span><span class="sxs-lookup"><span data-stu-id="e6e26-146">RS</span></span></p></td>
<td><p><span data-ttu-id="e6e26-147">Pārdot atkāroti</span><span class="sxs-lookup"><span data-stu-id="e6e26-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-148">Cita</span><span class="sxs-lookup"><span data-stu-id="e6e26-148">Other</span></span></p></td>
<td><p><span data-ttu-id="e6e26-149">EX</span><span class="sxs-lookup"><span data-stu-id="e6e26-149">EX</span></span></p></td>
<td><p><span data-ttu-id="e6e26-150">Maiņa</span><span class="sxs-lookup"><span data-stu-id="e6e26-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-151">Cita</span><span class="sxs-lookup"><span data-stu-id="e6e26-151">Other</span></span></p></td>
<td><p><span data-ttu-id="e6e26-152">MS</span><span class="sxs-lookup"><span data-stu-id="e6e26-152">MS</span></span></p></td>
<td><p><span data-ttu-id="e6e26-153">Dažādi</span><span class="sxs-lookup"><span data-stu-id="e6e26-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e6e26-154">Katram atgriešanas metodes kodam, ko definējat, ir jāatlasa atgriešanas metodes transakcija.</span><span class="sxs-lookup"><span data-stu-id="e6e26-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="e6e26-155">Atgriešanas metodes transakcija nosaka atgriešanas metodes kodu fiziskās un finansiālās sekas.</span><span class="sxs-lookup"><span data-stu-id="e6e26-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="e6e26-156">Piemēram, atgriešanas metodes transakcija nosaka atgrieztā krājuma fizisko apstrādi, atgrieztā krājuma finansiālo ietekmi un vai debitoram ir jānosūta aizvietošanas krājums.</span><span class="sxs-lookup"><span data-stu-id="e6e26-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="e6e26-157">Varat definēt neierobežotu skaitu atgriešanas metožu kodu saskaņā ar jūsu uzņēmējtransakcijas vajadzībām, bet ir tikai sešas iepriekš definētas atgriešanas metožu transakcijas, kuras jūs varat izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="e6e26-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="e6e26-158">Tabulā ir sniegtas atgriešanas metožu transakcijas un to definīcijas.</span><span class="sxs-lookup"><span data-stu-id="e6e26-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6e26-159">Atgriešanas metodes transakcija</span><span class="sxs-lookup"><span data-stu-id="e6e26-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="e6e26-160">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e6e26-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-161"><strong>Kredītkarte</strong></span><span class="sxs-lookup"><span data-stu-id="e6e26-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e26-162">Atgriezt krājumu inventārā un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="e6e26-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-163"><strong>Tikai kredītā</strong></span><span class="sxs-lookup"><span data-stu-id="e6e26-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e26-164">Kreditēt debitoru, nepieprasot un negaidot krājuma atgriešanu.</span><span class="sxs-lookup"><span data-stu-id="e6e26-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-165"><strong>Norakstīt</strong></span><span class="sxs-lookup"><span data-stu-id="e6e26-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e26-166">Norakstīt krājumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="e6e26-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-167"><strong>Aizstāt un kreditēt</strong></span><span class="sxs-lookup"><span data-stu-id="e6e26-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e26-168">Atgriezt krājumu inventārā, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="e6e26-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6e26-169"><strong>Aizstāt un izbrāķēt</strong></span><span class="sxs-lookup"><span data-stu-id="e6e26-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e26-170">Norakstīt krājumu, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="e6e26-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6e26-171"><strong>Atgriezt debitoram</strong></span><span class="sxs-lookup"><span data-stu-id="e6e26-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="e6e26-172">Noraidīt atgriezto krājumu un atgriezt to debitoram.</span><span class="sxs-lookup"><span data-stu-id="e6e26-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="e6e26-173">Izvēlieties izvietojuma kodu karantīnas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="e6e26-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="e6e26-174">Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Kvalitātes pārvaldība** \> **Karantīnas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6e26-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="e6e26-175">Esošam karantīnas pasūtījumam atlasiet kādu darbību cilnes **Apskats** laukā **Atgriešanas metodes kods**.</span><span class="sxs-lookup"><span data-stu-id="e6e26-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="e6e26-176">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="e6e26-176">See also</span></span>

<span data-ttu-id="e6e26-177">[Karantīnas pasūtījums (forma)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="e6e26-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="e6e26-178">[Atgriešanas metožu kodi (forma)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e6e26-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]