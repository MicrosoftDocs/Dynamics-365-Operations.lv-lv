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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2b1468328433a67253bafc21ac9c9b3a2398872
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981670"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="d9d4c-103">Noteikšana, kā atbrīvoties no atgrieztiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="d9d4c-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d9d4c-104">Kad apstrādājat atgriešanas pasūtījumu, jānorāda iemesla atgriešanas kods, lai noteiktu, kāpēc produkts tiek atgriezts.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="d9d4c-105">Ir jānorāda arī atgriešanas metodes kods un atgriešanas metodes transakcija, lai noteiktu, kas jādara ar pašu atgriezto produktu.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="d9d4c-106">Izvietojuma kodu var pielietot, ja izveidojat atgriešanas pasūtījumu, reģistrējat vienības pienākšanu vai pavadzīmes atjauninājumu vienības pienākšanai un beidzat karantīnas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="d9d4c-107">Varat definēt jebkādus atgriešanas metodes kodus, kas nepieciešami biznesa procesu atbalstam.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="d9d4c-108">Šajā tabulā sniegta parasti izmantoto kodu kopa, kas piešķirama atgriezta krājuma atgriešanas metodei.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9d4c-109">Atgriešanas metodes veids</span><span class="sxs-lookup"><span data-stu-id="d9d4c-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="d9d4c-110">Kopējais kods</span><span class="sxs-lookup"><span data-stu-id="d9d4c-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="d9d4c-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d9d4c-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-112">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-113">SC</span><span class="sxs-lookup"><span data-stu-id="d9d4c-113">SC</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-114">Utilizācija/Iznīcināšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-115">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-116">DC</span><span class="sxs-lookup"><span data-stu-id="d9d4c-116">DC</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-117">Ziedojuma labdarībai</span><span class="sxs-lookup"><span data-stu-id="d9d4c-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-118">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-119">TD</span><span class="sxs-lookup"><span data-stu-id="d9d4c-119">TD</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-120">Trešās personas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-121">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-122">SL</span><span class="sxs-lookup"><span data-stu-id="d9d4c-122">SL</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-123">Utilizācija izejvielām</span><span class="sxs-lookup"><span data-stu-id="d9d4c-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-124">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-125">TS</span><span class="sxs-lookup"><span data-stu-id="d9d4c-125">TS</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-126">Pārdošana trešajai personai (sekundārie tirgi)</span><span class="sxs-lookup"><span data-stu-id="d9d4c-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-127">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-128">RW</span><span class="sxs-lookup"><span data-stu-id="d9d4c-128">RW</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-129">Pārstrāde</span><span class="sxs-lookup"><span data-stu-id="d9d4c-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-130">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-131">RF</span><span class="sxs-lookup"><span data-stu-id="d9d4c-131">RF</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-132">Pilnīga pārstrāde/Uzlabošana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-133">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-134">MD</span><span class="sxs-lookup"><span data-stu-id="d9d4c-134">MD</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-135">Pārveidot</span><span class="sxs-lookup"><span data-stu-id="d9d4c-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-136">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-137">RP</span><span class="sxs-lookup"><span data-stu-id="d9d4c-137">RP</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-138">Remonts</span><span class="sxs-lookup"><span data-stu-id="d9d4c-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-139">Remonts/Pārveidošana</span><span class="sxs-lookup"><span data-stu-id="d9d4c-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-140">RV</span><span class="sxs-lookup"><span data-stu-id="d9d4c-140">RV</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-141">Atgriešana kreditoram</span><span class="sxs-lookup"><span data-stu-id="d9d4c-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-142">Citi</span><span class="sxs-lookup"><span data-stu-id="d9d4c-142">Other</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-143">AI</span><span class="sxs-lookup"><span data-stu-id="d9d4c-143">AI</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-144">Izmantot kā</span><span class="sxs-lookup"><span data-stu-id="d9d4c-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-145">Cita</span><span class="sxs-lookup"><span data-stu-id="d9d4c-145">Other</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-146">RS</span><span class="sxs-lookup"><span data-stu-id="d9d4c-146">RS</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-147">Pārdot atkāroti</span><span class="sxs-lookup"><span data-stu-id="d9d4c-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-148">Cita</span><span class="sxs-lookup"><span data-stu-id="d9d4c-148">Other</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-149">EX</span><span class="sxs-lookup"><span data-stu-id="d9d4c-149">EX</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-150">Maiņa</span><span class="sxs-lookup"><span data-stu-id="d9d4c-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-151">Cita</span><span class="sxs-lookup"><span data-stu-id="d9d4c-151">Other</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-152">MS</span><span class="sxs-lookup"><span data-stu-id="d9d4c-152">MS</span></span></p></td>
<td><p><span data-ttu-id="d9d4c-153">Dažādi</span><span class="sxs-lookup"><span data-stu-id="d9d4c-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d9d4c-154">Katram atgriešanas metodes kodam, ko definējat, ir jāatlasa atgriešanas metodes transakcija.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="d9d4c-155">Atgriešanas metodes transakcija nosaka atgriešanas metodes kodu fiziskās un finansiālās sekas.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="d9d4c-156">Piemēram, atgriešanas metodes transakcija nosaka atgrieztā krājuma fizisko apstrādi, atgrieztā krājuma finansiālo ietekmi un vai debitoram ir jānosūta aizvietošanas krājums.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="d9d4c-157">Varat definēt neierobežotu skaitu atgriešanas metožu kodu saskaņā ar jūsu uzņēmējtransakcijas vajadzībām, bet ir tikai sešas iepriekš definētas atgriešanas metožu transakcijas, kuras jūs varat izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="d9d4c-158">Tabulā ir sniegtas atgriešanas metožu transakcijas un to definīcijas.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9d4c-159">Atgriešanas metodes transakcija</span><span class="sxs-lookup"><span data-stu-id="d9d4c-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="d9d4c-160">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d9d4c-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-161"><strong>Kredītkarte</strong></span><span class="sxs-lookup"><span data-stu-id="d9d4c-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="d9d4c-162">Atgriezt krājumu inventārā un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-163"><strong>Tikai kredītā</strong></span><span class="sxs-lookup"><span data-stu-id="d9d4c-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="d9d4c-164">Kreditēt debitoru, nepieprasot un negaidot krājuma atgriešanu.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-165"><strong>Norakstīt</strong></span><span class="sxs-lookup"><span data-stu-id="d9d4c-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="d9d4c-166">Norakstīt krājumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-167"><strong>Aizstāt un kreditēt</strong></span><span class="sxs-lookup"><span data-stu-id="d9d4c-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="d9d4c-168">Atgriezt krājumu inventārā, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9d4c-169"><strong>Aizstāt un izbrāķēt</strong></span><span class="sxs-lookup"><span data-stu-id="d9d4c-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="d9d4c-170">Norakstīt krājumu, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9d4c-171"><strong>Atgriezt debitoram</strong></span><span class="sxs-lookup"><span data-stu-id="d9d4c-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="d9d4c-172">Noraidīt atgriezto krājumu un atgriezt to debitoram.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="d9d4c-173">Izvēlieties izvietojuma kodu karantīnas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="d9d4c-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="d9d4c-174">Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Kvalitātes pārvaldība** \> **Karantīnas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="d9d4c-175">Esošam karantīnas pasūtījumam atlasiet kādu darbību cilnes **Apskats** laukā **Atgriešanas metodes kods**.</span><span class="sxs-lookup"><span data-stu-id="d9d4c-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="d9d4c-176">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d9d4c-176">See also</span></span>

<span data-ttu-id="d9d4c-177">[Karantīnas pasūtījums (forma)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="d9d4c-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="d9d4c-178">[Atgriešanas metožu kodi (forma)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d9d4c-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  


