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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829289"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="0b426-103">Kartēšanas iestatīšana pārdošanas pasūtījuma statusa laukiem</span><span class="sxs-lookup"><span data-stu-id="0b426-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b426-104">Laukiem, kas norāda pārdošanas pasūtījuma statusu, ir dažādas numerācijas vērtības programmā Microsoft Dynamics 365 Supply Chain Management un Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0b426-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="0b426-105">Lai kartētu šos laukus duālajam ierakstam, ir nepieciešams papildu iestatījums.</span><span class="sxs-lookup"><span data-stu-id="0b426-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="0b426-106">Supply Chain Management lauki</span><span class="sxs-lookup"><span data-stu-id="0b426-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="0b426-107">Programmā Supply Chain Management pārdošanas pasūtījuma statusu ataino divi lauki.</span><span class="sxs-lookup"><span data-stu-id="0b426-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="0b426-108">Kartējamie lauki ir **Statuss** un **Dokumentu statuss**.</span><span class="sxs-lookup"><span data-stu-id="0b426-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="0b426-109">**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu.</span><span class="sxs-lookup"><span data-stu-id="0b426-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="0b426-110">Šis statuss tiek norādīts pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="0b426-110">This status is shown on the order header.</span></span>

<span data-ttu-id="0b426-111">**Statusa** uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="0b426-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="0b426-112">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-112">Open Order</span></span>
- <span data-ttu-id="0b426-113">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-113">Delivered</span></span>
- <span data-ttu-id="0b426-114">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-114">Invoiced</span></span>
- <span data-ttu-id="0b426-115">Atcelta</span><span class="sxs-lookup"><span data-stu-id="0b426-115">Cancelled</span></span>

<span data-ttu-id="0b426-116">**Dokumentu statusa** uzskaitījums norāda visjaunāko dokumentu, kas ģenerēts pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="0b426-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="0b426-117">Piemēram, ja pasūtījums ir apstiprināts, šis dokuments ir pārdošanas pasūtījuma apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="0b426-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="0b426-118">Ja pārdošanas pasūtījums ir daļēji iekļauts rēķinā un pēc tam tiek apstiprināta atlikusī rinda, dokumenta statuss paliek **Rēķins**, jo rēķins tiek ģenerēts vēlāk procesā.</span><span class="sxs-lookup"><span data-stu-id="0b426-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="0b426-119">**Dokumentu statusa** uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="0b426-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="0b426-120">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="0b426-120">Confirmation</span></span>
- <span data-ttu-id="0b426-121">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="0b426-121">Picking List</span></span>
- <span data-ttu-id="0b426-122">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="0b426-122">Packing Slip</span></span>
- <span data-ttu-id="0b426-123">Rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="0b426-124">Pārdošanas lauki</span><span class="sxs-lookup"><span data-stu-id="0b426-124">Fields in Sales</span></span>

<span data-ttu-id="0b426-125">Programmā Sales pasūtījuma statusu norāda divi lauki.</span><span class="sxs-lookup"><span data-stu-id="0b426-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="0b426-126">Kartējamie lauki ir **Statuss** un **Apstrādes statuss**.</span><span class="sxs-lookup"><span data-stu-id="0b426-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="0b426-127">**Statusa** uzskaitījums norāda pasūtījuma vispārējo statusu.</span><span class="sxs-lookup"><span data-stu-id="0b426-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="0b426-128">Tam ir tālāk minētās vērtības:</span><span class="sxs-lookup"><span data-stu-id="0b426-128">It has the following values:</span></span>

- <span data-ttu-id="0b426-129">Aktīvs</span><span class="sxs-lookup"><span data-stu-id="0b426-129">Active</span></span>
- <span data-ttu-id="0b426-130">Iesniegts</span><span class="sxs-lookup"><span data-stu-id="0b426-130">Submitted</span></span>
- <span data-ttu-id="0b426-131">Izpildīts</span><span class="sxs-lookup"><span data-stu-id="0b426-131">Fulfilled</span></span>
- <span data-ttu-id="0b426-132">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-132">Invoiced</span></span>
- <span data-ttu-id="0b426-133">Atcelts</span><span class="sxs-lookup"><span data-stu-id="0b426-133">Cancelled</span></span>

<span data-ttu-id="0b426-134">Tika ieviests **Apstrādes statusa** uzskaitījums, lai statusu varētu precīzāk kartēt ar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b426-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="0b426-135">Tabulā ir parādīta **Apstrādes statusa** kartēšana programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b426-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="0b426-136">Apstrādes statuss</span><span class="sxs-lookup"><span data-stu-id="0b426-136">Processing Status</span></span>   | <span data-ttu-id="0b426-137">Supply Chain Management statuss</span><span class="sxs-lookup"><span data-stu-id="0b426-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="0b426-138">Supply Chain Management dokumentu statuss</span><span class="sxs-lookup"><span data-stu-id="0b426-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="0b426-139">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="0b426-139">Active</span></span>              | <span data-ttu-id="0b426-140">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-140">Open Order</span></span>                        | <span data-ttu-id="0b426-141">None</span><span class="sxs-lookup"><span data-stu-id="0b426-141">None</span></span>                                       |
| <span data-ttu-id="0b426-142">Apstiprināts</span><span class="sxs-lookup"><span data-stu-id="0b426-142">Confirmed</span></span>           | <span data-ttu-id="0b426-143">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-143">Open Order</span></span>                        | <span data-ttu-id="0b426-144">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="0b426-144">Confirmation</span></span>                               |
| <span data-ttu-id="0b426-145">Izdots</span><span class="sxs-lookup"><span data-stu-id="0b426-145">Picked</span></span>              | <span data-ttu-id="0b426-146">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-146">Open Order</span></span>                        | <span data-ttu-id="0b426-147">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="0b426-147">Picking List</span></span>                               |
| <span data-ttu-id="0b426-148">Daļēji piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-148">Partially Delivered</span></span> | <span data-ttu-id="0b426-149">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-149">Open Order</span></span>                        | <span data-ttu-id="0b426-150">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="0b426-150">Packing Slip</span></span>                               |
| <span data-ttu-id="0b426-151">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-151">Delivered</span></span>           | <span data-ttu-id="0b426-152">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-152">Delivered</span></span>                         | <span data-ttu-id="0b426-153">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="0b426-153">Packing Slip</span></span>                               |
| <span data-ttu-id="0b426-154">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="0b426-154">Partially Invoiced</span></span>  | <span data-ttu-id="0b426-155">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-155">Delivered</span></span>                         | <span data-ttu-id="0b426-156">Rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-156">Invoice</span></span>                                    |
| <span data-ttu-id="0b426-157">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-157">Invoiced</span></span>            | <span data-ttu-id="0b426-158">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-158">Invoiced</span></span>                          | <span data-ttu-id="0b426-159">Rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-159">Invoice</span></span>                                    |
| <span data-ttu-id="0b426-160">Atcelta</span><span class="sxs-lookup"><span data-stu-id="0b426-160">Cancelled</span></span>           | <span data-ttu-id="0b426-161">Atcelta</span><span class="sxs-lookup"><span data-stu-id="0b426-161">Cancelled</span></span>                         | <span data-ttu-id="0b426-162">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="0b426-162">Not applicable</span></span>                             |

<span data-ttu-id="0b426-163">Tabulā ir parādīta **Apstrādes statusa** kartēšana starp programmām Sales un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b426-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="0b426-164">Apstrādes statuss</span><span class="sxs-lookup"><span data-stu-id="0b426-164">Processing Status</span></span>   | <span data-ttu-id="0b426-165">Sales statuss</span><span class="sxs-lookup"><span data-stu-id="0b426-165">Status in Sales</span></span> | <span data-ttu-id="0b426-166">Supply Chain Management statuss</span><span class="sxs-lookup"><span data-stu-id="0b426-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="0b426-167">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="0b426-167">Active</span></span>              | <span data-ttu-id="0b426-168">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="0b426-168">Active</span></span>          | <span data-ttu-id="0b426-169">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-169">Open Order</span></span>                        |
| <span data-ttu-id="0b426-170">Apstiprināts</span><span class="sxs-lookup"><span data-stu-id="0b426-170">Confirmed</span></span>           | <span data-ttu-id="0b426-171">Iesniegti</span><span class="sxs-lookup"><span data-stu-id="0b426-171">Submitted</span></span>       | <span data-ttu-id="0b426-172">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-172">Open Order</span></span>                        |
| <span data-ttu-id="0b426-173">Izdots</span><span class="sxs-lookup"><span data-stu-id="0b426-173">Picked</span></span>              | <span data-ttu-id="0b426-174">Iesniegti</span><span class="sxs-lookup"><span data-stu-id="0b426-174">Submitted</span></span>       | <span data-ttu-id="0b426-175">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-175">Open Order</span></span>                        |
| <span data-ttu-id="0b426-176">Daļēji piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-176">Partially Delivered</span></span> | <span data-ttu-id="0b426-177">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="0b426-177">Active</span></span>          | <span data-ttu-id="0b426-178">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-178">Open Order</span></span>                        |
| <span data-ttu-id="0b426-179">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="0b426-179">Partially Invoiced</span></span>  | <span data-ttu-id="0b426-180">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="0b426-180">Active</span></span>          | <span data-ttu-id="0b426-181">Atvērts pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0b426-181">Open Order</span></span>                        |
| <span data-ttu-id="0b426-182">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="0b426-182">Partially Invoiced</span></span>  | <span data-ttu-id="0b426-183">Izpildīts</span><span class="sxs-lookup"><span data-stu-id="0b426-183">Fulfilled</span></span>       | <span data-ttu-id="0b426-184">Piegādāts</span><span class="sxs-lookup"><span data-stu-id="0b426-184">Delivered</span></span>                         |
| <span data-ttu-id="0b426-185">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-185">Invoiced</span></span>            | <span data-ttu-id="0b426-186">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-186">Invoiced</span></span>        | <span data-ttu-id="0b426-187">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="0b426-187">Invoiced</span></span>                          |
| <span data-ttu-id="0b426-188">Atcelta</span><span class="sxs-lookup"><span data-stu-id="0b426-188">Cancelled</span></span>           | <span data-ttu-id="0b426-189">Atcelta</span><span class="sxs-lookup"><span data-stu-id="0b426-189">Cancelled</span></span>       | <span data-ttu-id="0b426-190">Atcelta</span><span class="sxs-lookup"><span data-stu-id="0b426-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="0b426-191">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="0b426-191">Setup</span></span>

<span data-ttu-id="0b426-192">Lai iestatītu pārdošanas pasūtījuma statusa lauku kartēšanu, ir jāiespējo **IsSOPIntegrationEnabled** un **isIntegrationUser** atribūti.</span><span class="sxs-lookup"><span data-stu-id="0b426-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="0b426-193">Lai iespējotu **IsSOPIntegrationEnabled** atribūtu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0b426-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="0b426-194">Pārlūkā dodieties uz vietni `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="0b426-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="0b426-195">Aizstājiet **\<test-name\>** ar uzņēmuma saiti uz Sales.</span><span class="sxs-lookup"><span data-stu-id="0b426-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="0b426-196">Atvērtajā lapā meklējiet **organizationid** un pierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b426-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizationid meklēšana](media/sales-map-orgid.png)

3. <span data-ttu-id="0b426-198">Sadaļā Sales atveriet pārlūka konsoli un izpildiet šādu skriptu.</span><span class="sxs-lookup"><span data-stu-id="0b426-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="0b426-199">Izmantojiet **organizationid** vērtību no 2. darbības.</span><span class="sxs-lookup"><span data-stu-id="0b426-199">Use the **organizationid** value from step 2.</span></span>

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

4. <span data-ttu-id="0b426-201">Pārbaudiet, vai **IsSOPIntegrationEnabled** ir iestatīts uz **true**.</span><span class="sxs-lookup"><span data-stu-id="0b426-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="0b426-202">Izmantojiet URL no 1. darbības, lai pārbaudītu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0b426-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled ir iestatīts uz true](media/sales-map-integration-enabled.png)

<span data-ttu-id="0b426-204">Lai iespējotu **isIntegrationUser** atribūtu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0b426-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="0b426-205">Sadaļā Sales, dodieties uz **Iestatījumi \> Pielāgošana \> Pielāgot sistēmu**, atlasiet **Lietotāja elementu** un pēc tam atveriet **Veidlapa \> Lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="0b426-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Lietotāja veidlapas atvēršana](media/sales-map-user.png)

2. <span data-ttu-id="0b426-207">Lauku pārlūkā meklējiet **Integrēšanas lietotāja režīms** un veiciet dubultklikšķi uz tā, lai to pievienotu veidlapai.</span><span class="sxs-lookup"><span data-stu-id="0b426-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="0b426-208">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0b426-208">Save your change.</span></span>

    ![Integrēšanas lietotāja režīma lauka pievienošana veidlapai](media/sales-map-field-explorer.png)

3. <span data-ttu-id="0b426-210">Sadaļā Sales dodieties uz **Iestatījums \> Drošība \> Lietotāji** un mainiet skatu no **Iespējotie lietotāji** uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="0b426-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Skata mainīšana no Iespējotajiem lietotājiem uz Programmas lietotājiem](media/sales-map-enabled-users.png)

4. <span data-ttu-id="0b426-212">Atlasiet divus ierakstu atribūtus **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="0b426-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Programmas lietotāju saraksts](media/sales-map-user-mode.png)

5. <span data-ttu-id="0b426-214">Mainiet lauka **Integrēšanas lietotāja režīms** vērtību uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0b426-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Lauka Integrēšanas lietotāja režīms vērtības maiņa](media/sales-map-user-mode-yes.png)

<span data-ttu-id="0b426-216">Jūsu pārdošanas pasūtījumi tagad ir kartēti.</span><span class="sxs-lookup"><span data-stu-id="0b426-216">Your sales orders are now mapped.</span></span>
