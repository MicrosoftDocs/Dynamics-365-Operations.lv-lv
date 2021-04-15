---
title: Noteikšana, kā atbrīvoties no atgrieztiem krājumiem
description: Nosakiet, kā atbrīvoties no atgrieztiem krājumiem.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3eaeb2589329809e57ac01aba85067e94c15477c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817489"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="fc922-103">Noteikšana, kā atbrīvoties no atgrieztiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="fc922-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fc922-104">Kad apstrādājat atgriešanas pasūtījumu, jānorāda iemesla atgriešanas kods, lai noteiktu, kāpēc produkts tiek atgriezts.</span><span class="sxs-lookup"><span data-stu-id="fc922-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="fc922-105">Ir jānorāda arī atgriešanas metodes kods un atgriešanas metodes transakcija, lai noteiktu, kas jādara ar pašu atgriezto produktu.</span><span class="sxs-lookup"><span data-stu-id="fc922-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="fc922-106">Izvietojuma kodu var pielietot, ja izveidojat atgriešanas pasūtījumu, reģistrējat vienības pienākšanu vai pavadzīmes atjauninājumu vienības pienākšanai un beidzat karantīnas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="fc922-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="fc922-107">Varat definēt jebkādus atgriešanas metodes kodus, kas nepieciešami biznesa procesu atbalstam.</span><span class="sxs-lookup"><span data-stu-id="fc922-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="fc922-108">Šajā tabulā sniegta parasti izmantoto kodu kopa, kas piešķirama atgriezta krājuma atgriešanas metodei.</span><span class="sxs-lookup"><span data-stu-id="fc922-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc922-109">Atgriešanas metodes veids</span><span class="sxs-lookup"><span data-stu-id="fc922-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="fc922-110">Kopējais kods</span><span class="sxs-lookup"><span data-stu-id="fc922-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="fc922-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fc922-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc922-112">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fc922-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="fc922-113">SC</span><span class="sxs-lookup"><span data-stu-id="fc922-113">SC</span></span></p></td>
<td><p><span data-ttu-id="fc922-114">Utilizācija/Iznīcināšana</span><span class="sxs-lookup"><span data-stu-id="fc922-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-115">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fc922-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="fc922-116">DC</span><span class="sxs-lookup"><span data-stu-id="fc922-116">DC</span></span></p></td>
<td><p><span data-ttu-id="fc922-117">Ziedojuma labdarībai</span><span class="sxs-lookup"><span data-stu-id="fc922-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-118">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fc922-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="fc922-119">TD</span><span class="sxs-lookup"><span data-stu-id="fc922-119">TD</span></span></p></td>
<td><p><span data-ttu-id="fc922-120">Trešās personas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fc922-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-121">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fc922-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="fc922-122">SL</span><span class="sxs-lookup"><span data-stu-id="fc922-122">SL</span></span></p></td>
<td><p><span data-ttu-id="fc922-123">Utilizācija izejvielām</span><span class="sxs-lookup"><span data-stu-id="fc922-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-124">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fc922-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="fc922-125">TS</span><span class="sxs-lookup"><span data-stu-id="fc922-125">TS</span></span></p></td>
<td><p><span data-ttu-id="fc922-126">Pārdošana trešajai personai (sekundārie tirgi)</span><span class="sxs-lookup"><span data-stu-id="fc922-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-127">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="fc922-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="fc922-128">RW</span><span class="sxs-lookup"><span data-stu-id="fc922-128">RW</span></span></p></td>
<td><p><span data-ttu-id="fc922-129">Pārstrāde</span><span class="sxs-lookup"><span data-stu-id="fc922-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-130">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="fc922-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="fc922-131">RF</span><span class="sxs-lookup"><span data-stu-id="fc922-131">RF</span></span></p></td>
<td><p><span data-ttu-id="fc922-132">Pilnīga pārstrāde/Uzlabošana</span><span class="sxs-lookup"><span data-stu-id="fc922-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-133">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="fc922-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="fc922-134">MD</span><span class="sxs-lookup"><span data-stu-id="fc922-134">MD</span></span></p></td>
<td><p><span data-ttu-id="fc922-135">Pārveidot</span><span class="sxs-lookup"><span data-stu-id="fc922-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-136">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="fc922-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="fc922-137">RP</span><span class="sxs-lookup"><span data-stu-id="fc922-137">RP</span></span></p></td>
<td><p><span data-ttu-id="fc922-138">Remonts</span><span class="sxs-lookup"><span data-stu-id="fc922-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-139">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="fc922-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="fc922-140">RV</span><span class="sxs-lookup"><span data-stu-id="fc922-140">RV</span></span></p></td>
<td><p><span data-ttu-id="fc922-141">Atgriešana kreditoram</span><span class="sxs-lookup"><span data-stu-id="fc922-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-142">Citi</span><span class="sxs-lookup"><span data-stu-id="fc922-142">Other</span></span></p></td>
<td><p><span data-ttu-id="fc922-143">AI</span><span class="sxs-lookup"><span data-stu-id="fc922-143">AI</span></span></p></td>
<td><p><span data-ttu-id="fc922-144">Izmantot kā</span><span class="sxs-lookup"><span data-stu-id="fc922-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-145">Cita</span><span class="sxs-lookup"><span data-stu-id="fc922-145">Other</span></span></p></td>
<td><p><span data-ttu-id="fc922-146">RS</span><span class="sxs-lookup"><span data-stu-id="fc922-146">RS</span></span></p></td>
<td><p><span data-ttu-id="fc922-147">Pārdot atkāroti</span><span class="sxs-lookup"><span data-stu-id="fc922-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-148">Cita</span><span class="sxs-lookup"><span data-stu-id="fc922-148">Other</span></span></p></td>
<td><p><span data-ttu-id="fc922-149">EX</span><span class="sxs-lookup"><span data-stu-id="fc922-149">EX</span></span></p></td>
<td><p><span data-ttu-id="fc922-150">Maiņa</span><span class="sxs-lookup"><span data-stu-id="fc922-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-151">Cita</span><span class="sxs-lookup"><span data-stu-id="fc922-151">Other</span></span></p></td>
<td><p><span data-ttu-id="fc922-152">MS</span><span class="sxs-lookup"><span data-stu-id="fc922-152">MS</span></span></p></td>
<td><p><span data-ttu-id="fc922-153">Dažādi</span><span class="sxs-lookup"><span data-stu-id="fc922-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc922-154">Katram atgriešanas metodes kodam, ko definējat, ir jāatlasa atgriešanas metodes transakcija.</span><span class="sxs-lookup"><span data-stu-id="fc922-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="fc922-155">Atgriešanas metodes transakcija nosaka atgriešanas metodes kodu fiziskās un finansiālās sekas.</span><span class="sxs-lookup"><span data-stu-id="fc922-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="fc922-156">Piemēram, atgriešanas metodes transakcija nosaka atgrieztā krājuma fizisko apstrādi, atgrieztā krājuma finansiālo ietekmi un vai debitoram ir jānosūta aizvietošanas krājums.</span><span class="sxs-lookup"><span data-stu-id="fc922-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="fc922-157">Varat definēt neierobežotu skaitu atgriešanas metožu kodu saskaņā ar jūsu uzņēmējtransakcijas vajadzībām, bet ir tikai sešas iepriekš definētas atgriešanas metožu transakcijas, kuras jūs varat izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="fc922-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="fc922-158">Tabulā ir sniegtas atgriešanas metožu transakcijas un to definīcijas.</span><span class="sxs-lookup"><span data-stu-id="fc922-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc922-159">Atgriešanas metodes transakcija</span><span class="sxs-lookup"><span data-stu-id="fc922-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="fc922-160">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fc922-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc922-161"><strong>Kredītkarte</strong></span><span class="sxs-lookup"><span data-stu-id="fc922-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="fc922-162">Atgriezt krājumu inventārā un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="fc922-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-163"><strong>Tikai kredītā</strong></span><span class="sxs-lookup"><span data-stu-id="fc922-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="fc922-164">Kreditēt debitoru, nepieprasot un negaidot krājuma atgriešanu.</span><span class="sxs-lookup"><span data-stu-id="fc922-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-165"><strong>Norakstīt</strong></span><span class="sxs-lookup"><span data-stu-id="fc922-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="fc922-166">Norakstīt krājumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="fc922-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-167"><strong>Aizstāt un kreditēt</strong></span><span class="sxs-lookup"><span data-stu-id="fc922-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="fc922-168">Atgriezt krājumu inventārā, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="fc922-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc922-169"><strong>Aizstāt un izbrāķēt</strong></span><span class="sxs-lookup"><span data-stu-id="fc922-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="fc922-170">Norakstīt krājumu, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="fc922-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc922-171"><strong>Atgriezt debitoram</strong></span><span class="sxs-lookup"><span data-stu-id="fc922-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="fc922-172">Noraidīt atgriezto krājumu un atgriezt to debitoram.</span><span class="sxs-lookup"><span data-stu-id="fc922-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="fc922-173">Izvēlieties izvietojuma kodu karantīnas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="fc922-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="fc922-174">Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Kvalitātes pārvaldība** \> **Karantīnas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="fc922-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="fc922-175">Esošam karantīnas pasūtījumam atlasiet kādu darbību cilnes **Apskats** laukā **Atgriešanas metodes kods**.</span><span class="sxs-lookup"><span data-stu-id="fc922-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="fc922-176">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="fc922-176">See also</span></span>

<span data-ttu-id="fc922-177">[Karantīnas pasūtījums (forma)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="fc922-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="fc922-178">[Atgriešanas metožu kodi (forma)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="fc922-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]