---
title: Neatbilstības izveide un apstrāde
description: Šajā tēmā ir aprakstīts, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956210"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="12b45-103">Neatbilstības izveide un apstrāde</span><span class="sxs-lookup"><span data-stu-id="12b45-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12b45-104">Šajā tēmā ir aprakstīts, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="12b45-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="12b45-105">Parasti neatbilstības pārvaldību veic kvalitātes darbinieks.</span><span class="sxs-lookup"><span data-stu-id="12b45-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="12b45-106">Pēcnosacījumam jābūt pieejamam kvalitātes pārbaudes pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="12b45-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="12b45-107">(Informāciju par to, kā izveidot kvalitātes pārbaudes pasūtījumu, skatiet [Pārbaudīt preču kvalitāti](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="12b45-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="12b45-108">Pirms lietotājs var apstrādāt neatbilstības apstiprinājumu, darbiniekiem jābūt piešķirtiem laukā **Persona** lapā **Lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="12b45-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="12b45-109">Turklāt, pirms lietotājs var lietot dokumentu piezīmes, lietotāja opcijās **Aktivizēt dokumentu apstrādi** jābūt iestatītai uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="12b45-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="12b45-110">Neatbilstības izveide</span><span class="sxs-lookup"><span data-stu-id="12b45-110">Create a nonconformance</span></span>

<span data-ttu-id="12b45-111">Lai izveidotu neatbilstību, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="12b45-112">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-113">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="12b45-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="12b45-114">Dialoglodziņā **Izveidot neatbilstību** laukā **Problēmas veids** atlasiet problēmas veidu, kas tika atrasts pārbaudes procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="12b45-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="12b45-115">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="12b45-116">Neatbilstības apstiprināšana vai noraidīšana</span><span class="sxs-lookup"><span data-stu-id="12b45-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="12b45-117">Lai neatbilstību apstiprinātu vai noraidītu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="12b45-118">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-119">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-120">Varat pievienot labojumu tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-121">Darbību rūtī atlasiet **Funkcijas \> Apstiprināt neatbilstību**, lai apstiprinātu neatbilstību vai **Funkcijas \> Noraidīt neatbilstību**, lai to noraidītu.</span><span class="sxs-lookup"><span data-stu-id="12b45-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="12b45-122">Jūs varat saistīt apstiprinātas neatbilstības ar [saistītajām operācijām](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="12b45-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="12b45-123">Šādā veidā var ierakstīt darbu, kas tiek veikts kā neatbilstības apstrādes un labošanas apstrādes daļa.</span><span class="sxs-lookup"><span data-stu-id="12b45-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="12b45-124">Tiek piedāvāts apstiprināt savu izvēli.</span><span class="sxs-lookup"><span data-stu-id="12b45-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="12b45-125">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="12b45-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="12b45-126">Pievienot neatbilstībai operācijas un citu detalizētu informāciju</span><span class="sxs-lookup"><span data-stu-id="12b45-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="12b45-127">Pēc tam, kad esat izveidojis neatbilstību, varat sākt pievienot saistītās operācijas un norādīt papildu informāciju par šīm operācijām.</span><span class="sxs-lookup"><span data-stu-id="12b45-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="12b45-128">Varat pievienot saistītas operācijas tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="12b45-129">Papildus pamatinformācijai, operācijai varat pievienot šādas detaļas:</span><span class="sxs-lookup"><span data-stu-id="12b45-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="12b45-130">**Krājumi** – varat izveidot krājumu sarakstu, kas patērēti labošanas veikšanai.</span><span class="sxs-lookup"><span data-stu-id="12b45-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="12b45-131">Piemēram, krājumi var būt produkti, kas nepieciešami iekārtas remontam vai sastāvdaļas, kas nepieciešamas pabeigtas preces remontam.</span><span class="sxs-lookup"><span data-stu-id="12b45-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="12b45-132">**Kvalitātes izmaksas** – var izveidot to izmaksu sarakstu, kas radušās vai par kurām izrakstīts rēķins ārējiem avotiem.</span><span class="sxs-lookup"><span data-stu-id="12b45-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="12b45-133">**Darba laika uzskaites tabula** – varat izveidot darba laika žurnālu, ko katrs darbinieks tērē operācijai.</span><span class="sxs-lookup"><span data-stu-id="12b45-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="12b45-134">Atlikušie iestātījumi nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="12b45-134">The remaining settings are optional.</span></span> <span data-ttu-id="12b45-135">Katra krājuma, kvalitātes maksu un darba laika uzskaites tabulas izmaksas tiek summētas un parādītas operācijā.</span><span class="sxs-lookup"><span data-stu-id="12b45-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="12b45-136">Operācijas lauku **Izmaksas** nevar labot tieši.</span><span class="sxs-lookup"><span data-stu-id="12b45-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="12b45-137">Operācijas izveide neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="12b45-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="12b45-138">Lai izveidotu operāciju neatbilstībai, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="12b45-139">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-140">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-141">Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-142">Darbību rūtī atlasiet **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="12b45-143">Darbību rūts lapā **Saistītās operācijas** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="12b45-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12b45-144">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="12b45-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="12b45-145">**Operācija** – atlasiet neatbilstībai veicamās operācijas kodu.</span><span class="sxs-lookup"><span data-stu-id="12b45-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="12b45-146">**Pamatojums** – ievadiet detalizētu aprakstu, kas skaidro, kāpēc operācija ir vajadzīga.</span><span class="sxs-lookup"><span data-stu-id="12b45-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="12b45-147">**Pārdošanas pasūtījums** - ja atlasītais operācijas kods ir saistīts ar pārdošanas pasūtījuma veidu, atlasiet pārdošanas pasūtījumu, ar kuru saistāt operāciju.</span><span class="sxs-lookup"><span data-stu-id="12b45-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="12b45-148">**Pirkšanas pasūtījums** - ja atlasītais operācijas kods ir saistīts ar pirkšanas pasūtījuma veidu, atlasiet pirkšanas pasūtījumu, ar kuru saistāt operāciju.</span><span class="sxs-lookup"><span data-stu-id="12b45-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="12b45-149">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="12b45-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="12b45-150">Pievienot krājumus operācijai</span><span class="sxs-lookup"><span data-stu-id="12b45-150">Add items to an operation</span></span>

<span data-ttu-id="12b45-151">Lai pievienotu operācijai krājumus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="12b45-152">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-153">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-154">Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-155">Darbību rūtī atlasiet **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="12b45-156">Lapā **Saistītās operācijas** atlasiet operāciju, kurai vēlaties pievienot krājumus.</span><span class="sxs-lookup"><span data-stu-id="12b45-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="12b45-157">Darbību rūtī atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="12b45-158">Darbību rūts lapā **Saistītās operācijas** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="12b45-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12b45-159">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="12b45-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="12b45-160">**Krājuma numurs** – atlasiet preci, kas tiks patērēta kā daļa no atlasītās operācijas.</span><span class="sxs-lookup"><span data-stu-id="12b45-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="12b45-161">**Daudzums** – ievadiet krājumu skaitu, kas tiks patērēts.</span><span class="sxs-lookup"><span data-stu-id="12b45-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-162">Izmaksas par krājumu var skatīt laukā **Izmaksas**, cilnē **Vispārīgi**. Parādītās izmaksas nāk no izmaksām, kas iestatītas lapā **Izlaistā prece**.</span><span class="sxs-lookup"><span data-stu-id="12b45-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="12b45-163">Izmaksas nevar atjaunināt tieši lapā **Saistīto operāciju krājums**.</span><span class="sxs-lookup"><span data-stu-id="12b45-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="12b45-164">Visu krājumu izmaksas, kas tiek pievienotas lapā **Saistīto operāciju krājumi**, tiek automātiski pievienotas laukam **Izmaksas** lapā **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="12b45-165">Atkārtojiet iepriekšējo darbību katrai papildu precei, kas jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="12b45-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="12b45-166">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="12b45-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="12b45-167">Kvalitātes maksu pievienošana darbībai</span><span class="sxs-lookup"><span data-stu-id="12b45-167">Add quality charges to an operation</span></span>

<span data-ttu-id="12b45-168">Lai pievienotu operācijai kvalitātes maksu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="12b45-169">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-170">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-171">Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-172">Darbību rūtī atlasiet **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="12b45-173">Lapā **Saistītās operācijas** atlasiet operāciju, kurai vēlaties pievienot kvalitātes maksu.</span><span class="sxs-lookup"><span data-stu-id="12b45-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="12b45-174">Darbību rūtī atlasiet **Kvalitātes maksa**.</span><span class="sxs-lookup"><span data-stu-id="12b45-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="12b45-175">Darbību rūts lapā **Saistītās operāciju maksas** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="12b45-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12b45-176">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="12b45-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="12b45-177">**Izmaksu kods** — atlasiet kvalitātes maksu, ko vēlaties pievienot.</span><span class="sxs-lookup"><span data-stu-id="12b45-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="12b45-178">**Apraksts** — ievadiet maksas detālizēto aprakstu.</span><span class="sxs-lookup"><span data-stu-id="12b45-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="12b45-179">**Maksas vērtība** - Ievadiet maksas summu.</span><span class="sxs-lookup"><span data-stu-id="12b45-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="12b45-180">Atkārtojiet iepriekšējo darbību katrai papildu maksai, kas jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="12b45-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="12b45-181">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="12b45-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="12b45-182">Summa laukā **Izmaksu vērtība** tiek automātiski summēta visām kvalitātes maksām un pievienota visām citām summām laukā **Izmaksas**, lapā **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="12b45-183">Darba laika uzskaites tabulas izveide operācijā</span><span class="sxs-lookup"><span data-stu-id="12b45-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="12b45-184">Lai pievienotu operācijai darba laika uzskaites tabulu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="12b45-185">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-186">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-187">Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-188">Darbību rūtī atlasiet **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="12b45-189">Lapā **Saistītās operācijas** atlasiet operāciju, kurai vēlaties pievienot darba laika uzskaites tabulu.</span><span class="sxs-lookup"><span data-stu-id="12b45-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="12b45-190">Darbību rūtī atlasiet **Darba laika uzskaites tabula**.</span><span class="sxs-lookup"><span data-stu-id="12b45-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="12b45-191">Darbību rūts lapā **Saistītās operāciju darba laika uzskaites tabulas** atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="12b45-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12b45-192">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="12b45-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="12b45-193">**Datums** – norādiet datumu, kad darbs tika paveikts.</span><span class="sxs-lookup"><span data-stu-id="12b45-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="12b45-194">Pēc noklusējuma šis lauks tiek iestatīts kā pašreizējais datums.</span><span class="sxs-lookup"><span data-stu-id="12b45-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="12b45-195">**Nodarbinātais** - Izvēlieties darbinieku, kurš paveica darbu.</span><span class="sxs-lookup"><span data-stu-id="12b45-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="12b45-196">Pēc noklusējuma šis lauks ir iestatīts darbiniekam, kas piešķirts pašreizējam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="12b45-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="12b45-197">**Operācijas stundas** – ievadiet stundu skaitu, kas tika nostrādāts atlasītajai operācijai.</span><span class="sxs-lookup"><span data-stu-id="12b45-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="12b45-198">**Izveidots rēķins** – atzīmējiet šo izvēles rūtiņu, ja rēķins ir izrakstīts debitoram vai kreditoram.</span><span class="sxs-lookup"><span data-stu-id="12b45-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-199">Izmaksas var skatīt laukā **Izmaksas** cilnē **Vispārīgi**. Izmaksas tiek aprēķinātas, izmantojot likmi, ko nosakiet lapā **Krājumu vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="12b45-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="12b45-200">Atkārtojiet iepriekšējo darbību katrai papildu darba laika uzskaites tabulas rindai, kas jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="12b45-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="12b45-201">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="12b45-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="12b45-202">Summa laukā **Izmaksas** tiek summēta visām darba laika uzskaites tabulas rindām un pievienota visām citām summām laukā **Izmaksas**, lapā **Saistītās operācijas**.</span><span class="sxs-lookup"><span data-stu-id="12b45-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="12b45-203">Pievienot labojumu neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="12b45-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="12b45-204">Lai neatbilstībai pievienotu labojumu, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="12b45-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="12b45-205">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-206">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-207">Varat pievienot labojumu tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-208">Darbību rūtī atlasiet **Labojumi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="12b45-209">Lapā **Labojumi**, darbības rūtī atlasiet **Jauns**, lai režģim pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="12b45-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12b45-210">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="12b45-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="12b45-211">**Diagnostika** – atlasiet diagnostikas veidu, kas identificē jūsu veidotā labojuma veidu.</span><span class="sxs-lookup"><span data-stu-id="12b45-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="12b45-212">**Nodarbinātais** - Atlasiet par labojumu atbildīgo personu.</span><span class="sxs-lookup"><span data-stu-id="12b45-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="12b45-213">**Labošanas prioritāte** – atlasiet opciju, lai norādītu, kā labojumam vajadzētu būt prioritāram (*Zema*, *Normāla* VAI *Augsta*).</span><span class="sxs-lookup"><span data-stu-id="12b45-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="12b45-214">**Pieprasītais datums** – ievadiet datumu, kad tika pieprasīta labošanas darbība.</span><span class="sxs-lookup"><span data-stu-id="12b45-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="12b45-215">**Plānotais datums** – ievadiet datumu, kad būtu jāpabeidz labojums.</span><span class="sxs-lookup"><span data-stu-id="12b45-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="12b45-216">**Īstermiņa risinājums** - atzīmējiet šo izvēles rūtiņu, ja labojoša darbība izlabo neatbilstību tikai uz neilgu laiku.</span><span class="sxs-lookup"><span data-stu-id="12b45-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="12b45-217">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="12b45-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="12b45-218">Atzīmēt labojumu kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="12b45-218">Mark a correction as completed</span></span>

<span data-ttu-id="12b45-219">Lai atzīmētu neatbilstības labojumu kā pabeigtu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="12b45-220">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-221">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="12b45-222">Varat pievienot labojumu tikai apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="12b45-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="12b45-223">Darbību rūtī atlasiet **Labojumi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="12b45-224">Režģī lapā **Labojumi** atlasiet labojumu, kuru vēlaties atzīmēt kā pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="12b45-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="12b45-225">Darbību rūtī atlasiet **Atzīmēt kā pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="12b45-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="12b45-226">Tiek piedāvāts apstiprināt savu izvēli.</span><span class="sxs-lookup"><span data-stu-id="12b45-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="12b45-227">Lai turpinātu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-227">Select **OK** to continue.</span></span> <span data-ttu-id="12b45-228">Lauks **Pabeigšanas datums un laiks** ir iestatīts uz pašreizējo datumu un laiku, un tiek atzīmēta izvēles rūtiņa **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="12b45-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="12b45-229">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12b45-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="12b45-230">Atkārtoti atvērt pabeigto labojumu</span><span class="sxs-lookup"><span data-stu-id="12b45-230">Reopen a completed correction</span></span>

<span data-ttu-id="12b45-231">Lai atkārtoti atvērtu pabeigto labojumu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="12b45-232">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-233">Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="12b45-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="12b45-234">Darbību rūtī atlasiet **Labojumi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="12b45-235">Režģī lapā **Labojumi** atlasiet labojumu, kuru vēlaties atkārtoti atvērt.</span><span class="sxs-lookup"><span data-stu-id="12b45-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="12b45-236">Darbību rūtī atlasiet **Atkārtoti atvērt**.</span><span class="sxs-lookup"><span data-stu-id="12b45-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="12b45-237">Tiek piedāvāts apstiprināt savu izvēli.</span><span class="sxs-lookup"><span data-stu-id="12b45-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="12b45-238">Lai turpinātu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-238">Select **OK** to continue.</span></span> <span data-ttu-id="12b45-239">Vērtība tiek notīrīta no lauka **Pabeigšanas datums un laiks**, un tiek notīrīta izvēles rūtiņa **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="12b45-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="12b45-240">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12b45-240">Close the page.</span></span>

<span data-ttu-id="12b45-241">Tagad labojumam var veikt papildu labojumus vai atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="12b45-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="12b45-242">Pēc pabeigšanas labojumu var atzīmēt kā pabeigtu vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="12b45-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="12b45-243">Neatbilstības aizvēršana</span><span class="sxs-lookup"><span data-stu-id="12b45-243">Close a nonconformance</span></span>

<span data-ttu-id="12b45-244">Lai aizvērtu neatbilstību, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="12b45-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="12b45-245">Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="12b45-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="12b45-246">Atlasiet režģī kvalitātes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="12b45-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="12b45-247">Darbību rūtī atlasiet **Vaicājumi \> Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="12b45-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="12b45-248">Lapā **Neatbilstības** atlasiet mērķa neatbilstību režģī.</span><span class="sxs-lookup"><span data-stu-id="12b45-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="12b45-249">Darbību rūtī atlasiet **Funkcijas \> Aizvērt neatbilstību**.</span><span class="sxs-lookup"><span data-stu-id="12b45-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="12b45-250">Tiek piedāvāts apstiprināt savu izvēli.</span><span class="sxs-lookup"><span data-stu-id="12b45-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="12b45-251">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="12b45-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="12b45-252">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="12b45-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12b45-253">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="12b45-253">Additional resources</span></span>

- [<span data-ttu-id="12b45-254">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="12b45-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="12b45-255">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="12b45-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="12b45-256">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="12b45-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="12b45-257">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="12b45-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="12b45-258">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="12b45-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="12b45-259">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="12b45-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="12b45-260">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="12b45-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="12b45-261">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="12b45-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
