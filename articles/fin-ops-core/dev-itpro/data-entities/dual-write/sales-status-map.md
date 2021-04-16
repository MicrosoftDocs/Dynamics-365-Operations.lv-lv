---
title: Kartējuma iestatīšana pārdošanas pasūtījuma statusa kolonnām
description: Šajā tēmā ir paskaidrots, kā iestatīt pārdošanas pasūtījuma statusa kolonnas duālajam ierakstam.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750718"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="e4e2f-103">Kartējuma iestatīšana pārdošanas pasūtījuma statusa kolonnām</span><span class="sxs-lookup"><span data-stu-id="e4e2f-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4e2f-104">Kolonnām, kas norāda pārdošanas pasūtījuma statusu, ir dažādas numerācijas vērtības programmā Microsoft Dynamics 365 Supply Chain Management un Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="e4e2f-105">Lai kartētu šīs kolonnas duālajam ierakstam, ir nepieciešams papildu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="e4e2f-106">kolonnas programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e4e2f-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="e4e2f-107">Programmā Supply Chain Management pārdošanas pasūtījuma statusu ataino divas kolonnas.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="e4e2f-108">Kartējamas kolonnas ir **Statuss** un **Dokumentu statuss**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="e4e2f-109">**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="e4e2f-110">Šis statuss tiek norādīts pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-110">This status is shown on the order header.</span></span>

<span data-ttu-id="e4e2f-111">**Statusa** uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e4e2f-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="e4e2f-112">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-112">Open Order</span></span>
- <span data-ttu-id="e4e2f-113">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-113">Delivered</span></span>
- <span data-ttu-id="e4e2f-114">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-114">Invoiced</span></span>
- <span data-ttu-id="e4e2f-115">Atcelta</span><span class="sxs-lookup"><span data-stu-id="e4e2f-115">Cancelled</span></span>

<span data-ttu-id="e4e2f-116">**Dokumentu statusa** uzskaitījums norāda visjaunāko dokumentu, kas ģenerēts pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="e4e2f-117">Piemēram, ja pasūtījums ir apstiprināts, šis dokuments ir pārdošanas pasūtījuma apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="e4e2f-118">Ja pārdošanas pasūtījums ir daļēji iekļauts rēķinā un pēc tam tiek apstiprināta atlikusī rinda, dokumenta statuss paliek **Rēķins**, jo rēķins tiek ģenerēts vēlāk procesā.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="e4e2f-119">**Dokumentu statusa** uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="e4e2f-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="e4e2f-120">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="e4e2f-120">Confirmation</span></span>
- <span data-ttu-id="e4e2f-121">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-121">Picking List</span></span>
- <span data-ttu-id="e4e2f-122">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="e4e2f-122">Packing Slip</span></span>
- <span data-ttu-id="e4e2f-123">Rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="e4e2f-124">Pārdošanas kolonnas</span><span class="sxs-lookup"><span data-stu-id="e4e2f-124">columns in Sales</span></span>

<span data-ttu-id="e4e2f-125">Programmā Sales pasūtījuma statusu norāda divas kolonnas.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="e4e2f-126">Kartējamās kolonnas ir **Statuss** un **Apstrādes statuss**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="e4e2f-127">**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="e4e2f-128">Tam ir tālāk minētās vērtības:</span><span class="sxs-lookup"><span data-stu-id="e4e2f-128">It has the following values:</span></span>

- <span data-ttu-id="e4e2f-129">Aktīvs</span><span class="sxs-lookup"><span data-stu-id="e4e2f-129">Active</span></span>
- <span data-ttu-id="e4e2f-130">Iesniegts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-130">Submitted</span></span>
- <span data-ttu-id="e4e2f-131">Izpildīts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-131">Fulfilled</span></span>
- <span data-ttu-id="e4e2f-132">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-132">Invoiced</span></span>
- <span data-ttu-id="e4e2f-133">Atcelts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-133">Cancelled</span></span>

<span data-ttu-id="e4e2f-134">Tika ieviests **Apstrādes statusa** uzskaitījums, lai statusu varētu precīzāk kartēt ar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="e4e2f-135">Tabulā ir parādīta **Apstrādes statusa** kartēšana programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="e4e2f-136">Apstrādes statuss</span><span class="sxs-lookup"><span data-stu-id="e4e2f-136">Processing Status</span></span>   | <span data-ttu-id="e4e2f-137">Supply Chain Management statuss</span><span class="sxs-lookup"><span data-stu-id="e4e2f-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="e4e2f-138">Supply Chain Management dokumentu statuss</span><span class="sxs-lookup"><span data-stu-id="e4e2f-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="e4e2f-139">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="e4e2f-139">Active</span></span>              | <span data-ttu-id="e4e2f-140">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-140">Open Order</span></span>                        | <span data-ttu-id="e4e2f-141">None</span><span class="sxs-lookup"><span data-stu-id="e4e2f-141">None</span></span>                                       |
| <span data-ttu-id="e4e2f-142">Apstiprināts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-142">Confirmed</span></span>           | <span data-ttu-id="e4e2f-143">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-143">Open Order</span></span>                        | <span data-ttu-id="e4e2f-144">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="e4e2f-144">Confirmation</span></span>                               |
| <span data-ttu-id="e4e2f-145">Izdots</span><span class="sxs-lookup"><span data-stu-id="e4e2f-145">Picked</span></span>              | <span data-ttu-id="e4e2f-146">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-146">Open Order</span></span>                        | <span data-ttu-id="e4e2f-147">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-147">Picking List</span></span>                               |
| <span data-ttu-id="e4e2f-148">Daļēji piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-148">Partially Delivered</span></span> | <span data-ttu-id="e4e2f-149">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-149">Open Order</span></span>                        | <span data-ttu-id="e4e2f-150">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="e4e2f-150">Packing Slip</span></span>                               |
| <span data-ttu-id="e4e2f-151">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-151">Delivered</span></span>           | <span data-ttu-id="e4e2f-152">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-152">Delivered</span></span>                         | <span data-ttu-id="e4e2f-153">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="e4e2f-153">Packing Slip</span></span>                               |
| <span data-ttu-id="e4e2f-154">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="e4e2f-154">Partially Invoiced</span></span>  | <span data-ttu-id="e4e2f-155">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-155">Delivered</span></span>                         | <span data-ttu-id="e4e2f-156">Rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-156">Invoice</span></span>                                    |
| <span data-ttu-id="e4e2f-157">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-157">Invoiced</span></span>            | <span data-ttu-id="e4e2f-158">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-158">Invoiced</span></span>                          | <span data-ttu-id="e4e2f-159">Rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-159">Invoice</span></span>                                    |
| <span data-ttu-id="e4e2f-160">Atcelta</span><span class="sxs-lookup"><span data-stu-id="e4e2f-160">Cancelled</span></span>           | <span data-ttu-id="e4e2f-161">Atcelta</span><span class="sxs-lookup"><span data-stu-id="e4e2f-161">Cancelled</span></span>                         | <span data-ttu-id="e4e2f-162">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="e4e2f-162">Not applicable</span></span>                             |

<span data-ttu-id="e4e2f-163">Tabulā ir parādīta **Apstrādes statusa** kartēšana starp programmām Sales un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="e4e2f-164">Apstrādes statuss</span><span class="sxs-lookup"><span data-stu-id="e4e2f-164">Processing Status</span></span>   | <span data-ttu-id="e4e2f-165">Sales statuss</span><span class="sxs-lookup"><span data-stu-id="e4e2f-165">Status in Sales</span></span> | <span data-ttu-id="e4e2f-166">Supply Chain Management statuss</span><span class="sxs-lookup"><span data-stu-id="e4e2f-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="e4e2f-167">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="e4e2f-167">Active</span></span>              | <span data-ttu-id="e4e2f-168">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="e4e2f-168">Active</span></span>          | <span data-ttu-id="e4e2f-169">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-169">Open Order</span></span>                        |
| <span data-ttu-id="e4e2f-170">Apstiprināts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-170">Confirmed</span></span>           | <span data-ttu-id="e4e2f-171">Iesniegti</span><span class="sxs-lookup"><span data-stu-id="e4e2f-171">Submitted</span></span>       | <span data-ttu-id="e4e2f-172">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-172">Open Order</span></span>                        |
| <span data-ttu-id="e4e2f-173">Izdots</span><span class="sxs-lookup"><span data-stu-id="e4e2f-173">Picked</span></span>              | <span data-ttu-id="e4e2f-174">Iesniegti</span><span class="sxs-lookup"><span data-stu-id="e4e2f-174">Submitted</span></span>       | <span data-ttu-id="e4e2f-175">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-175">Open Order</span></span>                        |
| <span data-ttu-id="e4e2f-176">Daļēji piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-176">Partially Delivered</span></span> | <span data-ttu-id="e4e2f-177">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="e4e2f-177">Active</span></span>          | <span data-ttu-id="e4e2f-178">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-178">Open Order</span></span>                        |
| <span data-ttu-id="e4e2f-179">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="e4e2f-179">Partially Invoiced</span></span>  | <span data-ttu-id="e4e2f-180">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="e4e2f-180">Active</span></span>          | <span data-ttu-id="e4e2f-181">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="e4e2f-181">Open Order</span></span>                        |
| <span data-ttu-id="e4e2f-182">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="e4e2f-182">Partially Invoiced</span></span>  | <span data-ttu-id="e4e2f-183">Izpildīts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-183">Fulfilled</span></span>       | <span data-ttu-id="e4e2f-184">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="e4e2f-184">Delivered</span></span>                         |
| <span data-ttu-id="e4e2f-185">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-185">Invoiced</span></span>            | <span data-ttu-id="e4e2f-186">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-186">Invoiced</span></span>        | <span data-ttu-id="e4e2f-187">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="e4e2f-187">Invoiced</span></span>                          |
| <span data-ttu-id="e4e2f-188">Atcelta</span><span class="sxs-lookup"><span data-stu-id="e4e2f-188">Cancelled</span></span>           | <span data-ttu-id="e4e2f-189">Atcelta</span><span class="sxs-lookup"><span data-stu-id="e4e2f-189">Cancelled</span></span>       | <span data-ttu-id="e4e2f-190">Atcelta</span><span class="sxs-lookup"><span data-stu-id="e4e2f-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="e4e2f-191">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="e4e2f-191">Setup</span></span>

<span data-ttu-id="e4e2f-192">Lai iestatītu pārdošanas pasūtījuma statusa lauku kartēšanu, ir jāiespējo **IsSOPIntegrationEnabled** un **isIntegrationUser** atribūti.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="e4e2f-193">Lai iespējotu **IsSOPIntegrationEnabled** atribūtu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="e4e2f-194">Pārlūkā dodieties uz vietni `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="e4e2f-195">Aizstājiet **\<test-name\>** ar uzņēmuma saiti uz Sales.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="e4e2f-196">Atvērtajā lapā meklējiet **organizationid** un pierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizationid meklēšana](media/sales-map-orgid.png)

3. <span data-ttu-id="e4e2f-198">Sadaļā Sales atveriet pārlūka konsoli un izpildiet šādu skriptu.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="e4e2f-199">Izmantojiet **organizationid** vērtību no 2. darbības.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript kods pārlūka konsolē](media/sales-map-script.png)

4. <span data-ttu-id="e4e2f-201">Pārbaudiet, vai **IsSOPIntegrationEnabled** ir iestatīts uz **true**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="e4e2f-202">Izmantojiet URL no 1. darbības, lai pārbaudītu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled ir iestatīts uz true](media/sales-map-integration-enabled.png)

<span data-ttu-id="e4e2f-204">Lai iespējotu **isIntegrationUser** atribūtu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="e4e2f-205">Sadaļā Sales, dodieties uz **Iestatījumi \> Pielāgošana \> Pielāgot sistēmu**, atlasiet **Lietotāja tabulu** un pēc tam atveriet **Veidlapa \> Lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Lietotāja veidlapas atvēršana](media/sales-map-user.png)

2. <span data-ttu-id="e4e2f-207">Lauku pārlūkā meklējiet **Integrēšanas lietotāja režīms** un veiciet dubultklikšķi uz tā, lai to pievienotu veidlapai.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="e4e2f-208">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-208">Save your change.</span></span>

    ![Integrēšanas lietotāja režīma kolonnas pievienošana veidlapai](media/sales-map-field-explorer.png)

3. <span data-ttu-id="e4e2f-210">Sadaļā Sales dodieties uz **Iestatījums \> Drošība \> Lietotāji** un mainiet skatu no **Iespējotie lietotāji** uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Skata mainīšana no Iespējotajiem lietotājiem uz Programmas lietotājiem](media/sales-map-enabled-users.png)

4. <span data-ttu-id="e4e2f-212">Atlasiet divus ierakstu atribūtus **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Programmas lietotāju saraksts](media/sales-map-user-mode.png)

5. <span data-ttu-id="e4e2f-214">Mainiet kolonnas **Integrēšanas lietotāja režīms** vērtību uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Kolonna Integrēšanas lietotāja režīms vērtības maiņa](media/sales-map-user-mode-yes.png)

<span data-ttu-id="e4e2f-216">Jūsu pārdošanas pasūtījumi tagad ir kartēti.</span><span class="sxs-lookup"><span data-stu-id="e4e2f-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]