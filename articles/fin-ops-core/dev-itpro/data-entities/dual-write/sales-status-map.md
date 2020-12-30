---
title: Kartēšanas iestatīšana pārdošanas pasūtījuma statusa laukiem
description: Šajā tēmā ir paskaidrots, kā iestatīt pārdošanas pasūtījuma statusa laukus duālajam ierakstam.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4454981"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="49c31-103">Kartēšanas iestatīšana pārdošanas pasūtījuma statusa laukiem</span><span class="sxs-lookup"><span data-stu-id="49c31-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49c31-104">Laukiem, kas norāda pārdošanas pasūtījuma statusu, ir dažādas numerācijas vērtības programmā Microsoft Dynamics 365 Supply Chain Management un Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="49c31-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="49c31-105">Lai kartētu šos laukus duālajam ierakstam, ir nepieciešams papildu iestatījums.</span><span class="sxs-lookup"><span data-stu-id="49c31-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="49c31-106">Supply Chain Management lauki</span><span class="sxs-lookup"><span data-stu-id="49c31-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="49c31-107">Programmā Supply Chain Management pārdošanas pasūtījuma statusu ataino divi lauki.</span><span class="sxs-lookup"><span data-stu-id="49c31-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="49c31-108">Kartējamie lauki ir **Statuss** un **Dokumentu statuss**.</span><span class="sxs-lookup"><span data-stu-id="49c31-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="49c31-109">**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu.</span><span class="sxs-lookup"><span data-stu-id="49c31-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="49c31-110">Šis statuss tiek norādīts pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="49c31-110">This status is shown on the order header.</span></span>

<span data-ttu-id="49c31-111">**Statusa** uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="49c31-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="49c31-112">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-112">Open Order</span></span>
- <span data-ttu-id="49c31-113">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-113">Delivered</span></span>
- <span data-ttu-id="49c31-114">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-114">Invoiced</span></span>
- <span data-ttu-id="49c31-115">Atcelta</span><span class="sxs-lookup"><span data-stu-id="49c31-115">Cancelled</span></span>

<span data-ttu-id="49c31-116">**Dokumentu statusa** uzskaitījums norāda visjaunāko dokumentu, kas ģenerēts pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="49c31-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="49c31-117">Piemēram, ja pasūtījums ir apstiprināts, šis dokuments ir pārdošanas pasūtījuma apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="49c31-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="49c31-118">Ja pārdošanas pasūtījums ir daļēji iekļauts rēķinā un pēc tam tiek apstiprināta atlikusī rinda, dokumenta statuss paliek **Rēķins**, jo rēķins tiek ģenerēts vēlāk procesā.</span><span class="sxs-lookup"><span data-stu-id="49c31-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="49c31-119">**Dokumentu statusa** uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="49c31-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="49c31-120">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="49c31-120">Confirmation</span></span>
- <span data-ttu-id="49c31-121">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="49c31-121">Picking List</span></span>
- <span data-ttu-id="49c31-122">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="49c31-122">Packing Slip</span></span>
- <span data-ttu-id="49c31-123">Rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="49c31-124">Pārdošanas lauki</span><span class="sxs-lookup"><span data-stu-id="49c31-124">Fields in Sales</span></span>

<span data-ttu-id="49c31-125">Programmā Sales pasūtījuma statusu norāda divi lauki.</span><span class="sxs-lookup"><span data-stu-id="49c31-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="49c31-126">Kartējamie lauki ir **Statuss** un **Apstrādes statuss**.</span><span class="sxs-lookup"><span data-stu-id="49c31-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="49c31-127">**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu.</span><span class="sxs-lookup"><span data-stu-id="49c31-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="49c31-128">Tam ir tālāk minētās vērtības:</span><span class="sxs-lookup"><span data-stu-id="49c31-128">It has the following values:</span></span>

- <span data-ttu-id="49c31-129">Aktīvs</span><span class="sxs-lookup"><span data-stu-id="49c31-129">Active</span></span>
- <span data-ttu-id="49c31-130">Iesniegts</span><span class="sxs-lookup"><span data-stu-id="49c31-130">Submitted</span></span>
- <span data-ttu-id="49c31-131">Izpildīts</span><span class="sxs-lookup"><span data-stu-id="49c31-131">Fulfilled</span></span>
- <span data-ttu-id="49c31-132">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-132">Invoiced</span></span>
- <span data-ttu-id="49c31-133">Atcelts</span><span class="sxs-lookup"><span data-stu-id="49c31-133">Cancelled</span></span>

<span data-ttu-id="49c31-134">Tika ieviests **Apstrādes statusa** uzskaitījums, lai statusu varētu precīzāk kartēt ar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49c31-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="49c31-135">Tabulā ir parādīta **Apstrādes statusa** kartēšana programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49c31-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="49c31-136">Apstrādes statuss</span><span class="sxs-lookup"><span data-stu-id="49c31-136">Processing Status</span></span>   | <span data-ttu-id="49c31-137">Supply Chain Management statuss</span><span class="sxs-lookup"><span data-stu-id="49c31-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="49c31-138">Supply Chain Management dokumentu statuss</span><span class="sxs-lookup"><span data-stu-id="49c31-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="49c31-139">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="49c31-139">Active</span></span>              | <span data-ttu-id="49c31-140">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-140">Open Order</span></span>                        | <span data-ttu-id="49c31-141">None</span><span class="sxs-lookup"><span data-stu-id="49c31-141">None</span></span>                                       |
| <span data-ttu-id="49c31-142">Apstiprināts</span><span class="sxs-lookup"><span data-stu-id="49c31-142">Confirmed</span></span>           | <span data-ttu-id="49c31-143">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-143">Open Order</span></span>                        | <span data-ttu-id="49c31-144">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="49c31-144">Confirmation</span></span>                               |
| <span data-ttu-id="49c31-145">Izdots</span><span class="sxs-lookup"><span data-stu-id="49c31-145">Picked</span></span>              | <span data-ttu-id="49c31-146">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-146">Open Order</span></span>                        | <span data-ttu-id="49c31-147">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="49c31-147">Picking List</span></span>                               |
| <span data-ttu-id="49c31-148">Daļēji piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-148">Partially Delivered</span></span> | <span data-ttu-id="49c31-149">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-149">Open Order</span></span>                        | <span data-ttu-id="49c31-150">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="49c31-150">Packing Slip</span></span>                               |
| <span data-ttu-id="49c31-151">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-151">Delivered</span></span>           | <span data-ttu-id="49c31-152">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-152">Delivered</span></span>                         | <span data-ttu-id="49c31-153">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="49c31-153">Packing Slip</span></span>                               |
| <span data-ttu-id="49c31-154">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="49c31-154">Partially Invoiced</span></span>  | <span data-ttu-id="49c31-155">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-155">Delivered</span></span>                         | <span data-ttu-id="49c31-156">Rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-156">Invoice</span></span>                                    |
| <span data-ttu-id="49c31-157">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-157">Invoiced</span></span>            | <span data-ttu-id="49c31-158">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-158">Invoiced</span></span>                          | <span data-ttu-id="49c31-159">Rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-159">Invoice</span></span>                                    |
| <span data-ttu-id="49c31-160">Atcelta</span><span class="sxs-lookup"><span data-stu-id="49c31-160">Cancelled</span></span>           | <span data-ttu-id="49c31-161">Atcelta</span><span class="sxs-lookup"><span data-stu-id="49c31-161">Cancelled</span></span>                         | <span data-ttu-id="49c31-162">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="49c31-162">Not applicable</span></span>                             |

<span data-ttu-id="49c31-163">Tabulā ir parādīta **Apstrādes statusa** kartēšana starp programmām Sales un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49c31-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="49c31-164">Apstrādes statuss</span><span class="sxs-lookup"><span data-stu-id="49c31-164">Processing Status</span></span>   | <span data-ttu-id="49c31-165">Sales statuss</span><span class="sxs-lookup"><span data-stu-id="49c31-165">Status in Sales</span></span> | <span data-ttu-id="49c31-166">Supply Chain Management statuss</span><span class="sxs-lookup"><span data-stu-id="49c31-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="49c31-167">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="49c31-167">Active</span></span>              | <span data-ttu-id="49c31-168">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="49c31-168">Active</span></span>          | <span data-ttu-id="49c31-169">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-169">Open Order</span></span>                        |
| <span data-ttu-id="49c31-170">Apstiprināts</span><span class="sxs-lookup"><span data-stu-id="49c31-170">Confirmed</span></span>           | <span data-ttu-id="49c31-171">Iesniegti</span><span class="sxs-lookup"><span data-stu-id="49c31-171">Submitted</span></span>       | <span data-ttu-id="49c31-172">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-172">Open Order</span></span>                        |
| <span data-ttu-id="49c31-173">Izdots</span><span class="sxs-lookup"><span data-stu-id="49c31-173">Picked</span></span>              | <span data-ttu-id="49c31-174">Iesniegti</span><span class="sxs-lookup"><span data-stu-id="49c31-174">Submitted</span></span>       | <span data-ttu-id="49c31-175">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-175">Open Order</span></span>                        |
| <span data-ttu-id="49c31-176">Daļēji piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-176">Partially Delivered</span></span> | <span data-ttu-id="49c31-177">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="49c31-177">Active</span></span>          | <span data-ttu-id="49c31-178">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-178">Open Order</span></span>                        |
| <span data-ttu-id="49c31-179">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="49c31-179">Partially Invoiced</span></span>  | <span data-ttu-id="49c31-180">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="49c31-180">Active</span></span>          | <span data-ttu-id="49c31-181">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="49c31-181">Open Order</span></span>                        |
| <span data-ttu-id="49c31-182">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="49c31-182">Partially Invoiced</span></span>  | <span data-ttu-id="49c31-183">Izpildīts</span><span class="sxs-lookup"><span data-stu-id="49c31-183">Fulfilled</span></span>       | <span data-ttu-id="49c31-184">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="49c31-184">Delivered</span></span>                         |
| <span data-ttu-id="49c31-185">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-185">Invoiced</span></span>            | <span data-ttu-id="49c31-186">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-186">Invoiced</span></span>        | <span data-ttu-id="49c31-187">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="49c31-187">Invoiced</span></span>                          |
| <span data-ttu-id="49c31-188">Atcelta</span><span class="sxs-lookup"><span data-stu-id="49c31-188">Cancelled</span></span>           | <span data-ttu-id="49c31-189">Atcelta</span><span class="sxs-lookup"><span data-stu-id="49c31-189">Cancelled</span></span>       | <span data-ttu-id="49c31-190">Atcelta</span><span class="sxs-lookup"><span data-stu-id="49c31-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="49c31-191">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="49c31-191">Setup</span></span>

<span data-ttu-id="49c31-192">Lai iestatītu pārdošanas pasūtījuma statusa lauku kartēšanu, ir jāiespējo **IsSOPIntegrationEnabled** un **isIntegrationUser** atribūti.</span><span class="sxs-lookup"><span data-stu-id="49c31-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="49c31-193">Lai iespējotu **IsSOPIntegrationEnabled** atribūtu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="49c31-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="49c31-194">Pārlūkā dodieties uz vietni `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="49c31-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="49c31-195">Aizstājiet **\<test-name\>** ar uzņēmuma saiti uz Sales.</span><span class="sxs-lookup"><span data-stu-id="49c31-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="49c31-196">Atvērtajā lapā meklējiet **organizationid** un pierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="49c31-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizationid meklēšana](media/sales-map-orgid.png)

3. <span data-ttu-id="49c31-198">Sadaļā Sales atveriet pārlūka konsoli un izpildiet šādu skriptu.</span><span class="sxs-lookup"><span data-stu-id="49c31-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="49c31-199">Izmantojiet **organizationid** vērtību no 2. darbības.</span><span class="sxs-lookup"><span data-stu-id="49c31-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript kods pārlūka konsolē](media/sales-map-script.png)

4. <span data-ttu-id="49c31-201">Pārbaudiet, vai **IsSOPIntegrationEnabled** ir iestatīts uz **true**.</span><span class="sxs-lookup"><span data-stu-id="49c31-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="49c31-202">Izmantojiet URL no 1. darbības, lai pārbaudītu vērtību.</span><span class="sxs-lookup"><span data-stu-id="49c31-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled ir iestatīts uz true](media/sales-map-integration-enabled.png)

<span data-ttu-id="49c31-204">Lai iespējotu **isIntegrationUser** atribūtu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="49c31-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="49c31-205">Sadaļā Sales, dodieties uz **Iestatījumi \> Pielāgošana \> Pielāgot sistēmu**, atlasiet **Lietotāja elementu** un pēc tam atveriet **Veidlapa \> Lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="49c31-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Lietotāja veidlapas atvēršana](media/sales-map-user.png)

2. <span data-ttu-id="49c31-207">Lauku pārlūkā meklējiet **Integrēšanas lietotāja režīms** un veiciet dubultklikšķi uz tā, lai to pievienotu veidlapai.</span><span class="sxs-lookup"><span data-stu-id="49c31-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="49c31-208">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="49c31-208">Save your change.</span></span>

    ![Integrēšanas lietotāja režīma lauka pievienošana veidlapai](media/sales-map-field-explorer.png)

3. <span data-ttu-id="49c31-210">Sadaļā Sales dodieties uz **Iestatījums \> Drošība \> Lietotāji** un mainiet skatu no **Iespējotie lietotāji** uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="49c31-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Skata mainīšana no Iespējotajiem lietotājiem uz Programmas lietotājiem](media/sales-map-enabled-users.png)

4. <span data-ttu-id="49c31-212">Atlasiet divus ierakstu atribūtus **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="49c31-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Programmas lietotāju saraksts](media/sales-map-user-mode.png)

5. <span data-ttu-id="49c31-214">Mainiet lauka **Integrēšanas lietotāja režīms** vērtību uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="49c31-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Lauka Integrēšanas lietotāja režīms vērtības maiņa](media/sales-map-user-mode-yes.png)

<span data-ttu-id="49c31-216">Jūsu pārdošanas pasūtījumi tagad ir kartēti.</span><span class="sxs-lookup"><span data-stu-id="49c31-216">Your sales orders are now mapped.</span></span>
