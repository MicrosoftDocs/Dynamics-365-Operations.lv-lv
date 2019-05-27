---
title: Noliktavas darba politikas
description: Noliktavas darba politikas kontrolē to, vai ražošanā noliktavas procesi izveido noliktavas darbu, pamatojoties uz darba pasūtījuma tipu, krājumu novietojumu un preci.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0710eac8daba7f51f6b5d1522476b812a130960d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567036"
---
# <a name="warehouse-work-policies"></a><span data-ttu-id="a4b65-103">Noliktavas darba politikas</span><span class="sxs-lookup"><span data-stu-id="a4b65-103">Warehouse work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4b65-104">Noliktavas darba politikas programmā Microsoft Dynamics 365 for Finance and Operations kontrolē to, vai ražošanā noliktavas procesi izveido noliktavas darbu, pamatojoties uz darba pasūtījuma tipu, krājumu novietojumu un preci.</span><span class="sxs-lookup"><span data-stu-id="a4b65-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="a4b65-105">Šī darba politika kontrolē to, vai ražošanā noliktavas procesiem tiek izveidots noliktavas darbs.</span><span class="sxs-lookup"><span data-stu-id="a4b65-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="a4b65-106">Šo darba politiku varat iestatīt, izmantojot kombināciju no vienumiem **darba pasūtījuma veidi**, **krājumu novietojums** un **prece**.</span><span class="sxs-lookup"><span data-stu-id="a4b65-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="a4b65-107">Piemēram, prece L0101 tiek ziņota kā pabeigta uz izvades novietojumu 001.</span><span class="sxs-lookup"><span data-stu-id="a4b65-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="a4b65-108">Vēlāk šī pabeigtā prece tiek patērēta citā ražošanas pasūtījumā izvades novietojumā 001.</span><span class="sxs-lookup"><span data-stu-id="a4b65-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="a4b65-109">Šajā gadījumā varat iestatīt darba politiku, lai neļautu izveidot darbu gatavo preču izvietošanai, kad preci L0101 ziņojat kā pabeigtu uz izvades novietojumu 001.</span><span class="sxs-lookup"><span data-stu-id="a4b65-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="a4b65-110">Darba politika ir atsevišķs elements, ko var aprakstīt ar tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="a4b65-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="a4b65-111">**Darba politikas nosaukums** (darba politikas unikālais identifikators)</span><span class="sxs-lookup"><span data-stu-id="a4b65-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="a4b65-112">**Darba pasūtījumu veidi** un **Darba izveidošanas metode**</span><span class="sxs-lookup"><span data-stu-id="a4b65-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="a4b65-113">**Krājumu vietas**</span><span class="sxs-lookup"><span data-stu-id="a4b65-113">**Inventory locations**</span></span>
-   <span data-ttu-id="a4b65-114">**preces.**</span><span class="sxs-lookup"><span data-stu-id="a4b65-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="a4b65-115">Darba pasūtījumu veidi</span><span class="sxs-lookup"><span data-stu-id="a4b65-115">Work order types</span></span>
<span data-ttu-id="a4b65-116">Varat atlasīt no tālāk uzskaitītajiem darba pasūtījumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="a4b65-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="a4b65-117">Pabeigto preču izvietošana</span><span class="sxs-lookup"><span data-stu-id="a4b65-117">Finished goods put away</span></span>
-   <span data-ttu-id="a4b65-118">Līdzproduktu un blakusproduktu izvietošana</span><span class="sxs-lookup"><span data-stu-id="a4b65-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="a4b65-119">Izejmateriālu izdošana</span><span class="sxs-lookup"><span data-stu-id="a4b65-119">Raw material picking</span></span>

<span data-ttu-id="a4b65-120">Laukam **Darba izveidošanas metode** vērtība ir **Nekad**.</span><span class="sxs-lookup"><span data-stu-id="a4b65-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="a4b65-121">Šī vērtība norāda, ka šī darba politika atlasītajam darba pasūtījuma veidam neļaus izveidot noliktavas darbu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="a4b65-122">Krājumu vietas</span><span class="sxs-lookup"><span data-stu-id="a4b65-122">Inventory locations</span></span>
<span data-ttu-id="a4b65-123">Varat atlasīt novietojumu, uz kuru attiecas šī darba politika.</span><span class="sxs-lookup"><span data-stu-id="a4b65-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="a4b65-124">Ja darba politikai nav piesaistīts neviens novietojums, tad šī darba politika netiek lietota nevienam procesam.</span><span class="sxs-lookup"><span data-stu-id="a4b65-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="a4b65-125">Lapā **Novietojumi** varat arī atlasīt vai atcelt konkrēta novietojuma atlasi darba politikai.</span><span class="sxs-lookup"><span data-stu-id="a4b65-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="a4b65-126">Preces</span><span class="sxs-lookup"><span data-stu-id="a4b65-126">Products</span></span>
<span data-ttu-id="a4b65-127">Varat atlasīt preci, uz kuru attiecas šī darba politika.</span><span class="sxs-lookup"><span data-stu-id="a4b65-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="a4b65-128">Darba politiku varat lietot visām precēm vai atlasītām precēm.</span><span class="sxs-lookup"><span data-stu-id="a4b65-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="a4b65-129">Piemērs</span><span class="sxs-lookup"><span data-stu-id="a4b65-129">Example</span></span>
<span data-ttu-id="a4b65-130">Nākamajā piemērā ir divi ražošanas pasūtījumi, PRD-001 un PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="a4b65-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="a4b65-131">Ražošanas pasūtījumā PRD-001 ir operācija ar nosaukumu **Montāža**, kur prece SC1 tiek ziņota kā pabeigta uz novietojumu O1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="a4b65-132">Ražošanas pasūtījumā PRD-002 ir operācija ar nosaukumu **Krāsošana**, un tas patērē preci SC1 no novietojuma O1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="a4b65-133">Ražošanas pasūtījums PRD-002 patērē arī izejmateriālu RM1 no novietojuma O1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="a4b65-134">Izejmateriāls RM1 tiek glabāts noliktavas novietojumā BULK-001 un ar noliktavas darbu izejmateriālu izdošanai tiks izdots uz novietojumu O1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="a4b65-135">Izdošanas darbs tiek ģenerēts, kad tiek izlaista ražošana PRD-002.</span><span class="sxs-lookup"><span data-stu-id="a4b65-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="a4b65-136">[![Noliktavas darba politikas](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="a4b65-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="a4b65-137">Kad plānojat konfigurēt noliktavas darba politiku šim scenārijam, ir jāņem vērā tālāk norādītā informācija.</span><span class="sxs-lookup"><span data-stu-id="a4b65-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="a4b65-138">Noliktavas darbs gatavo preču izvietošanai nav nepieciešams, kad preci SC1 ziņojat kā pabeigtu no ražošanas pasūtījuma PRD-001 uz novietojumu O1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="a4b65-139">Tas ir tādēļ, ka operācija **Krāsošana** ražošanas pasūtījumam PRD-002 preci SC1 patērē tajā pašā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="a4b65-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="a4b65-140">Noliktavas darbs izejmateriālu izdošanai ir nepieciešams, lai izejmateriālu RM1 no noliktavas novietojumā BULK-001 pārvietotu uz novietojumu O1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="a4b65-141">Šeit ir sniegts darba politikas piemērs, kuru varat iestatīt, pamatojoties uz šiem apsvērumiem.</span><span class="sxs-lookup"><span data-stu-id="a4b65-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="a4b65-142"><strong>Darba politikas nosaukums</strong></span><span class="sxs-lookup"><span data-stu-id="a4b65-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="a4b65-143"><strong>Darba pasūtījumu veidi</strong></span><span class="sxs-lookup"><span data-stu-id="a4b65-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="a4b65-144">Nav izvietošanas 01     \`</span><span class="sxs-lookup"><span data-stu-id="a4b65-144">No put away 01     \`</span></span>          |     <span data-ttu-id="a4b65-145">- Pabeigtas preces izvietošana</span><span class="sxs-lookup"><span data-stu-id="a4b65-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="a4b65-146"><strong>Novietojumi</strong></span><span class="sxs-lookup"><span data-stu-id="a4b65-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="a4b65-147">- O1</span><span class="sxs-lookup"><span data-stu-id="a4b65-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="a4b65-148"><strong>Preces</strong></span><span class="sxs-lookup"><span data-stu-id="a4b65-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="a4b65-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="a4b65-149">- SC1</span></span>                 |

<span data-ttu-id="a4b65-150">Nākamajās procedūrās ir sniegtas detalizētas instrukcijas par to, kā iestatīt noliktavas darba politiku šim scenārijam.</span><span class="sxs-lookup"><span data-stu-id="a4b65-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="a4b65-151">Ir aprakstīts arī piemēra iestatījums, kurā redzams, kā ražošanas pasūtījumu ziņot kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības.</span><span class="sxs-lookup"><span data-stu-id="a4b65-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="a4b65-152">Iestatīt noliktavas darba politiku</span><span class="sxs-lookup"><span data-stu-id="a4b65-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="a4b65-153">Ne vienmēr noliktavas procesi ietver noliktavas darbu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="a4b65-154">Definējot darba politiku, jūs varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai preču kopai konkrētos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="a4b65-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="a4b65-155">Šīs procedūras izveidošanai tika izmantots demonstrācijas datu uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="a4b65-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="a4b65-156">DARBĪBAS (21)</span><span class="sxs-lookup"><span data-stu-id="a4b65-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="a4b65-157">1.</span><span class="sxs-lookup"><span data-stu-id="a4b65-157">1.</span></span>  | <span data-ttu-id="a4b65-158">Dodieties uz Noliktavas vadība &gt; Iestatīšana &gt; Darbs &gt; Darba politikas.</span><span class="sxs-lookup"><span data-stu-id="a4b65-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="a4b65-159">2.</span><span class="sxs-lookup"><span data-stu-id="a4b65-159">2.</span></span>  | <span data-ttu-id="a4b65-160">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a4b65-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="a4b65-161">3.</span><span class="sxs-lookup"><span data-stu-id="a4b65-161">3.</span></span>  | <span data-ttu-id="a4b65-162">Darba politikas nosaukumu laukā ierakstiet 'Nav izvietošanas darbu'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="a4b65-163">4.</span><span class="sxs-lookup"><span data-stu-id="a4b65-163">4.</span></span>  | <span data-ttu-id="a4b65-164">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a4b65-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="a4b65-165">5.</span><span class="sxs-lookup"><span data-stu-id="a4b65-165">5.</span></span>  | <span data-ttu-id="a4b65-166">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a4b65-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="a4b65-167">6.</span><span class="sxs-lookup"><span data-stu-id="a4b65-167">6.</span></span>  | <span data-ttu-id="a4b65-168">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="a4b65-169">7.</span><span class="sxs-lookup"><span data-stu-id="a4b65-169">7.</span></span>  | <span data-ttu-id="a4b65-170">Darba pasūtījuma veida laukā atlasiet 'Pabeigto preču izvietošana'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="a4b65-171">8.</span><span class="sxs-lookup"><span data-stu-id="a4b65-171">8.</span></span>  | <span data-ttu-id="a4b65-172">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a4b65-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="a4b65-173">9.</span><span class="sxs-lookup"><span data-stu-id="a4b65-173">9.</span></span>  | <span data-ttu-id="a4b65-174">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="a4b65-175">10.</span><span class="sxs-lookup"><span data-stu-id="a4b65-175">10.</span></span> | <span data-ttu-id="a4b65-176">Darba pasūtījuma veida laukā atlasiet 'Līdzproduktu un blakusproduktu izvietošana'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="a4b65-177">11.</span><span class="sxs-lookup"><span data-stu-id="a4b65-177">11.</span></span> | <span data-ttu-id="a4b65-178">Izvērsiet sadaļu Krājumu atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="a4b65-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="a4b65-179">12.</span><span class="sxs-lookup"><span data-stu-id="a4b65-179">12.</span></span> | <span data-ttu-id="a4b65-180">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a4b65-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="a4b65-181">13.</span><span class="sxs-lookup"><span data-stu-id="a4b65-181">13.</span></span> | <span data-ttu-id="a4b65-182">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="a4b65-183">14.</span><span class="sxs-lookup"><span data-stu-id="a4b65-183">14.</span></span> | <span data-ttu-id="a4b65-184">Sarakstā Noliktava ievadiet '51'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="a4b65-185">15.</span><span class="sxs-lookup"><span data-stu-id="a4b65-185">15.</span></span> | <span data-ttu-id="a4b65-186">Laukā Atrašanās vieta, ievadiet vai atlasiet '001'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="a4b65-187">16.</span><span class="sxs-lookup"><span data-stu-id="a4b65-187">16.</span></span> | <span data-ttu-id="a4b65-188">Izvērsiet sadaļu Preces.</span><span class="sxs-lookup"><span data-stu-id="a4b65-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="a4b65-189">17.</span><span class="sxs-lookup"><span data-stu-id="a4b65-189">17.</span></span> | <span data-ttu-id="a4b65-190">Laukā Preču atlase, atlasiet 'Atlasīts'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="a4b65-191">18.</span><span class="sxs-lookup"><span data-stu-id="a4b65-191">18.</span></span> | <span data-ttu-id="a4b65-192">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a4b65-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="a4b65-193">19.</span><span class="sxs-lookup"><span data-stu-id="a4b65-193">19.</span></span> | <span data-ttu-id="a4b65-194">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="a4b65-195">20.</span><span class="sxs-lookup"><span data-stu-id="a4b65-195">20.</span></span> | <span data-ttu-id="a4b65-196">Laukā Krājuma kods ievadiet vai atlasiet 'L0101'.</span><span class="sxs-lookup"><span data-stu-id="a4b65-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="a4b65-197">21.</span><span class="sxs-lookup"><span data-stu-id="a4b65-197">21.</span></span> | <span data-ttu-id="a4b65-198">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a4b65-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="a4b65-199">Ziņot ražošanas pasūtījumu kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības</span><span class="sxs-lookup"><span data-stu-id="a4b65-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="a4b65-200">Šajā procedūrā ir parādīts piemērs tam, kā ziņot kā pabeigtu uz novietojumu, kas nav atkarīgs no noliktavas vienības.</span><span class="sxs-lookup"><span data-stu-id="a4b65-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="a4b65-201">Šim uzdevumam ir nepieciešama piemērojama darba politika.</span><span class="sxs-lookup"><span data-stu-id="a4b65-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="a4b65-202">Iepriekšējā procedūrā ir parādīta darba politikas iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="a4b65-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="a4b65-203">DARBĪBAS (25)</span><span class="sxs-lookup"><span data-stu-id="a4b65-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="a4b65-204"><strong>Apakšuzdevums: iestatīt izvades novietojumu.</strong></span><span class="sxs-lookup"><span data-stu-id="a4b65-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="a4b65-205">Dodieties uz Organizācijas administrēšana &gt; Resursi &gt; Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="a4b65-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="a4b65-206">Sarakstā atlasiet resursu grupu &#39;5102&#39;.</span><span class="sxs-lookup"><span data-stu-id="a4b65-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="a4b65-207">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a4b65-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="a4b65-208">Laukā Izvades noliktava ievadiet &#39;51&#39;.</span><span class="sxs-lookup"><span data-stu-id="a4b65-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="a4b65-209">Laukā Izvades vieta ievadiet &#39;001&#39;.</span><span class="sxs-lookup"><span data-stu-id="a4b65-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="a4b65-210">Novietojums 001 nav no numura zīmes atkarīgs novietojums.</span><span class="sxs-lookup"><span data-stu-id="a4b65-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="a4b65-211">Novietojumu, kas nav atkarīgs no numura zīmes, var iestatīt tikai tad, ja attiecīgajam novietojumam ir piemērojama darba politika.</span><span class="sxs-lookup"><span data-stu-id="a4b65-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="a4b65-212"><strong>Apakšuzdevums: izveidot ražošanas pasūtījumu un norādīt to kā pabeigtu.</strong></span><span class="sxs-lookup"><span data-stu-id="a4b65-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="a4b65-213">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="a4b65-214">Doties uz Ražošanas kontrole &gt; Ražošanas pasūtījumi &gt; Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a4b65-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="a4b65-215">Noklikšķiniet uz Jauns ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a4b65-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="a4b65-216">Laukā Krājuma kods ievadiet &#39;L0101&#39;.</span><span class="sxs-lookup"><span data-stu-id="a4b65-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="a4b65-217">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="a4b65-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="a4b65-218">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a4b65-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="a4b65-219">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="a4b65-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="a4b65-220">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a4b65-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="a4b65-221">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="a4b65-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="a4b65-222">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="a4b65-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="a4b65-223">Laukā Automātisks MK patēriņš atlasiet &#39;Nekad&#39;.</span><span class="sxs-lookup"><span data-stu-id="a4b65-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="a4b65-224">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a4b65-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="a4b65-225">Uzklikšķiniet Reģistrēt pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="a4b65-226">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="a4b65-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="a4b65-227">Laukā Pieņemt kļūdu atlasiet vienumu Jā.</span><span class="sxs-lookup"><span data-stu-id="a4b65-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="a4b65-228">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a4b65-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="a4b65-229">Darbību rūtī noklikšķiniet uz Noliktava.</span><span class="sxs-lookup"><span data-stu-id="a4b65-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="a4b65-230">Noklikšķiniet uz Detalizēta informācija par darbu.</span><span class="sxs-lookup"><span data-stu-id="a4b65-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="a4b65-231">Kad ražošanas pasūtījums tika norādīts kā pabeigts, netika ģenerēts darbs izvietošanai.</span><span class="sxs-lookup"><span data-stu-id="a4b65-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="a4b65-232">Tas notiek tāpēc, ka ir definēta darba politika, kas neļauj ģenerēt darbu, kad produkts L0101 tiek norādīts kā pabeigts novietojumā 001.</span><span class="sxs-lookup"><span data-stu-id="a4b65-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



