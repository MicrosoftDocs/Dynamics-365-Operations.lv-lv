---
title: Apakšlīgumu slēgšana
description: Šajā sadaļā ir izskaidrots, kā veidot ražošanas apakšlīgumu slēgšanas kritisku analīzi programmā Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1cc1040393d843f39ca8c741a7c51435c7169c00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432514"
---
# <a name="subcontracting"></a><span data-ttu-id="db87b-103">Apakšlīgumu slēgšana</span><span class="sxs-lookup"><span data-stu-id="db87b-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db87b-104">Šajā sadaļā ir izskaidrots, kā veidot ražošanas apakšlīgumu slēgšanas kritisku analīzi programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="db87b-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="db87b-105">Šīs sadaļas pirmajā daļa ir aprakstīta datu iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="db87b-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="db87b-106">Otrajā daļā ir sniegtas pakāpeniskas norādes par kritiskas analīzes darbībām.</span><span class="sxs-lookup"><span data-stu-id="db87b-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="db87b-107">Mērķauditorija</span><span class="sxs-lookup"><span data-stu-id="db87b-107">Target audience</span></span>

<span data-ttu-id="db87b-108">Šajā sadaļā ir izskaidrots, kā iestatīt apakšlīgumu slēgšanu ražošanā.</span><span class="sxs-lookup"><span data-stu-id="db87b-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="db87b-109">Esošie dati tiek izmantoti HQUS juridiskajai personai, lai veiktu apakšlīgumu slēgšanas darbību plūsmas pamatfunkcionalitātes iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="db87b-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="db87b-110">HQUS juridiskās personas demonstrācijas dati ietver iestatīšanas parametrus, kas ir iepriekš iestatīti, lai atbalstītu kritiskās analīzes darbības.</span><span class="sxs-lookup"><span data-stu-id="db87b-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="db87b-111">Kaut arī kritiskā analīze ietver galvenos dažādu lomu problemātiskos punktus un problēmas, to var izpildīt sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="db87b-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="db87b-112">Demonstrācijas scenārijs</span><span class="sxs-lookup"><span data-stu-id="db87b-112">Demo scenario</span></span>

<span data-ttu-id="db87b-113">HQUS juridiskā persona ražo augstas kvalitātes skaļruņus.</span><span class="sxs-lookup"><span data-stu-id="db87b-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="db87b-114">Ražošanas procesa gaitā skaļruņi ir pakļauti tālāk aprakstītajiem trīs operāciju līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="db87b-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="db87b-115">**Iepriekšēja montāža** — tiek samontēts skaļruņa korpuss.</span><span class="sxs-lookup"><span data-stu-id="db87b-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="db87b-116">Pirms operācijas sākšanas materiālu noliktavā tiek izdots korpusa materiāls.</span><span class="sxs-lookup"><span data-stu-id="db87b-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="db87b-117">**Pārklāšana** — kad skaļruņa korpuss ir samontēts, tas ir jāpārklāj.</span><span class="sxs-lookup"><span data-stu-id="db87b-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="db87b-118">Šo operācija pabeidz kreditors (apakšuzņēmējs).</span><span class="sxs-lookup"><span data-stu-id="db87b-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="db87b-119">Iepriekš samontētais skaļruņa korpuss kopā ar diviem materiāliem tiek nosūtīts apakšuzņēmējam pārklāšanai.</span><span class="sxs-lookup"><span data-stu-id="db87b-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="db87b-120">**Pabeigšana** — kad apakšuzņēmējs ir pārklājis iepriekš samontēto skaļruņa korpusu, tas tiek atgriezts HQUS juridiskajai personai, lai var pabeigt galīgo skaļruņa montāžu.</span><span class="sxs-lookup"><span data-stu-id="db87b-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="db87b-121">Nākamajā attēlā ir redzamas trīs operācijas un visi materiāli, kuri tajās tiek izmantoti.</span><span class="sxs-lookup"><span data-stu-id="db87b-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Operācija Iepriekšēja montāža, Pārklāšana un Pabeigšana un tajās izmantotie materiāli](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="db87b-123">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="db87b-123">Setup</span></span>

<span data-ttu-id="db87b-124">Pirms kritiskās analīzes uzsākšanas ir jāiestata dati.</span><span class="sxs-lookup"><span data-stu-id="db87b-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="db87b-125">Pabeigtās preces iestatīšana</span><span class="sxs-lookup"><span data-stu-id="db87b-125">Set up the finished product</span></span>

<span data-ttu-id="db87b-126">Šajā sadaļā ir izskaidrots, kā iestatīt izlaisto preci D8100 “Pārklātais korpuss”.</span><span class="sxs-lookup"><span data-stu-id="db87b-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="db87b-127">Lai atvērtu lapu **Izlaisto preču detalizēta informācija**, atlasiet **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="db87b-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="db87b-128">Lai atrastu esošo izlaisto preci, ātrās filtrēšanas laukā ievadiet **D8100**.</span><span class="sxs-lookup"><span data-stu-id="db87b-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Izlaistās preces D8100 filtrēšana izlaisto preču detalizētas informācijas lapā](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="db87b-130">Lai atvērtu lapu **Maršruts**, darbību rūts cilnē **Inženieris** atlasiet **Maršruts**.</span><span class="sxs-lookup"><span data-stu-id="db87b-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="db87b-131">Lapā **Maršruts** ir redzamas izlaistās preces D8100 astoņas maršruta versijas.</span><span class="sxs-lookup"><span data-stu-id="db87b-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="db87b-132">Astoņas maršruta versijas tiek sadalītas četras maršrutos vietā Nr. 1 un Nr. 5.</span><span class="sxs-lookup"><span data-stu-id="db87b-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="db87b-133">Maršruts 000400 tiek izmantots izmaksu aprēķināšanai, maršruts 00041 tiek izmantots, ja operācija Pārklāšana ir iekšēja operācija, un maršruts 00042 tiek izmantots, ja operācija Pārklāšana ir ārēja operācija.</span><span class="sxs-lookup"><span data-stu-id="db87b-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Astoņu maršruta versijas lapā Maršruts](./media/subcontract03_route-page.png)

4. <span data-ttu-id="db87b-135">Augšējās rūts režģī **Versijas** atlasiet maršruta versiju **00042** vietai **5**.</span><span class="sxs-lookup"><span data-stu-id="db87b-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="db87b-136">Apakšējās rūts režģa cilnē **Pārskats** atlasiet operāciju **20** (**Cbnt CtSc**).</span><span class="sxs-lookup"><span data-stu-id="db87b-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Atlasīta maršruta versijas 00042 operācija 20 vietai Nr. 5](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="db87b-138">Atlasiet cilni **Vispārēji**.</span><span class="sxs-lookup"><span data-stu-id="db87b-138">Select the **General** tab.</span></span>

    <span data-ttu-id="db87b-139">Ievērojiet, ka ir iestatīta lauka **Maršruta veids** opcija **Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="db87b-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="db87b-140">Šī vērtība norāda, ka operācija 20 (Cbnt CtSc) ir apakšlīgumā paredzēta operācija.</span><span class="sxs-lookup"><span data-stu-id="db87b-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Lauka Maršruta veids iestatījums Kreditors cilnē Vispārīgi](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="db87b-142">Atlasiet cilni **Resursu pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="db87b-143">Parametrus izmanto, lai ražošanas plānošanas laikā atrastu attiecīgo resursu.</span><span class="sxs-lookup"><span data-stu-id="db87b-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="db87b-144">Ievērojiet, ka operācijai 20 (Cbnt CtSc) ir nepieciešams resurss, kam ir divi parametri **Pārklāšana** un **Pārklāti korpusi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Parametrs Pārklāšana un Pārklāti korpusi resursu pieprasījumu cilnē](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="db87b-146">Lai atvērtu dialoglodziņu **Izmantojamie resursi**, atlasiet **Izmantojamie resursi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="db87b-147">Atrasti ir trīs resursi, kas atbilst operācijas resursu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="db87b-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="db87b-148">Ievērojiet, ka ir resursa 8851 un 8852 veids ir **Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="db87b-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Trīs attiecīgie resursi dialoglodziņā Izmantojamie resursi](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="db87b-150">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Izmantojamie resursi**, un atveriet atkal lapu **Maršruts**.</span><span class="sxs-lookup"><span data-stu-id="db87b-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="db87b-151">Aizveriet lapu **Maršruts**, lai atkal atvērtu lapu **Izlaistās preces detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="db87b-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Izlaistās preces detalizētas informācijas lapa](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="db87b-153">Lai atvērtu lapu **MK versijas**, darbību rūts cilnē **Inženieris** atlasiet **MK versijas**.</span><span class="sxs-lookup"><span data-stu-id="db87b-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="db87b-154">Lapā **MK versijas** lapa ir redzami izlaistās preces D8100 četras materiālu komplektu (MK) versijas.</span><span class="sxs-lookup"><span data-stu-id="db87b-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="db87b-155">MK 000040 izmanto izmaksu aprēķināšanai un plānošanai, MK 000041 izmanto, ja operācija Pārklāšana tiek veikta savā uzņēmumā, un MK 000042 un 000043 izmanto, ja operācija Pārklāšana ir paredzēta apakšlīgumā.</span><span class="sxs-lookup"><span data-stu-id="db87b-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="db87b-156">Ievērojiet, ka krājums S8050 ir krājuma veida **Pakalpojums** prece.</span><span class="sxs-lookup"><span data-stu-id="db87b-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="db87b-157">Šis krājums pārstāv apakšuzņēmēja darbu.</span><span class="sxs-lookup"><span data-stu-id="db87b-157">This item represents the subcontracted work.</span></span>

    ![Četras MK versijas MK versiju lapā](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="db87b-159">Lai atvērtu dialoglodziņu **MK rindas rediģēšana**, kopsavilkuma cilnē **Materiālu komplektu rindas** atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="db87b-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="db87b-160">Kad ražošanas pasūtījums ir izveidots un novērtēts saskaņā ar izlaisto preci D8100, automātiski tiek ģenerēts krājuma S8050 pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="db87b-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="db87b-161">Šis pirkšanas pasūtījums tiek saistīts ar ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="db87b-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="db87b-162">Lai pirkšanas pasūtījumi tiktu ģenerēti automātiski, jāiestata lauka **Rindas veids** opcija **Kreditors** un apakšuzņēmējam jāatlasa kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="db87b-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="db87b-163">Šajā gadījumā kreditora konts ir US-801.</span><span class="sxs-lookup"><span data-stu-id="db87b-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="db87b-164">Ievērojiet, ka MK rinda ir savienota ar darbību Pārklāšana, izmantojot operācijas numuru (šajā gadījumā 20).</span><span class="sxs-lookup"><span data-stu-id="db87b-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialoglodziņš MK rinda rediģēšana](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="db87b-166">Noliktavā nodarbināto paroļu izveide</span><span class="sxs-lookup"><span data-stu-id="db87b-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="db87b-167">Noliktavā nodarbinātajiem, kuri izmanto pārnēsājamu ierīci, ir jānosaka parole.</span><span class="sxs-lookup"><span data-stu-id="db87b-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="db87b-168">Lai atvērtu lapu **Darba lietotāji**, atlasiet **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.</span><span class="sxs-lookup"><span data-stu-id="db87b-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="db87b-169">Kopsavilkuma cilnē **Lietotāji** atlasiet lietotāja rindu **51**.</span><span class="sxs-lookup"><span data-stu-id="db87b-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Darba lietotāju lapa](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="db87b-171">Atlasiet **Atiestatīt paroli**.</span><span class="sxs-lookup"><span data-stu-id="db87b-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="db87b-172">Laukā **Parole** un **Apstiprināt paroli** ievadiet **1**.</span><span class="sxs-lookup"><span data-stu-id="db87b-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="db87b-173">Atlasiet **Iestatīt paroli**.</span><span class="sxs-lookup"><span data-stu-id="db87b-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="db87b-174">Kritiskā analīze soli pa solim</span><span class="sxs-lookup"><span data-stu-id="db87b-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="db87b-175">**Scenārijs un fons**</span><span class="sxs-lookup"><span data-stu-id="db87b-175">**Scenario and background**</span></span>

<span data-ttu-id="db87b-176">Ir izveidots preces D8100 “Pārklāts korpuss” 10 gabalu ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="db87b-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="db87b-177">Korpusa pārklāšana ir apakšlīgumā paredzēta operācija, kuru izpilda kreditors US-801 Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="db87b-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="db87b-178">Ražošanas pasūtījums ietver trīs operācijas.</span><span class="sxs-lookup"><span data-stu-id="db87b-178">The production order consists of three operations.</span></span> <span data-ttu-id="db87b-179">Pirmajā operācijā korpuss tiek iepriekš samontēts, operāciju veicot uz vietas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="db87b-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="db87b-180">Iepriekšējai montāžai nepieciešamais materiāls tiek izdots izejmateriālu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="db87b-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="db87b-181">Kad iepriekšējā montāža ir pabeigta, iepriekš samontētais korpuss tiek nosūtīts uzņēmumam Perfect Coating Solutions kopā ar diviem materiāliem, kuri ir nepieciešami operācijas Pārklāšana izpildei.</span><span class="sxs-lookup"><span data-stu-id="db87b-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="db87b-182">Kad pārklātais korpuss tiek saņemts atpakaļ no kreditora, pirms ziņojuma par tā pabeigšanu sagatavošanas tas tiek apstrādāts uz vietas uzņēmumā galīgās montāžas operācijā.</span><span class="sxs-lookup"><span data-stu-id="db87b-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="db87b-183">Lai atvērtu lapu **Visi ražošanas pasūtījumi**, atlasiet **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="db87b-184">Lai atvērtu dialoglodziņu **Ražošanas pasūtījumu izveide**, darbību rūtī atlasiet **Jauns ražošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="db87b-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialoglodziņš Ražošanas pasūtījumu izveide](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="db87b-186">Laukā **Krājuma numurs** atlasiet **D8100**.</span><span class="sxs-lookup"><span data-stu-id="db87b-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="db87b-187">Kad krājuma numurs ir atlasīts, tiek parādīti krājumu dimensiju lauki.</span><span class="sxs-lookup"><span data-stu-id="db87b-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="db87b-188">Laukā **Krāsa** atlasiet **Hroms**.</span><span class="sxs-lookup"><span data-stu-id="db87b-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="db87b-189">Tiek parādīts ziņojuma lodziņš ar jautājumu, vai ir jāievada MK aktīvās versijas un maršruts.</span><span class="sxs-lookup"><span data-stu-id="db87b-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Ziņojuma lodziņš](./media/subcontract13_message-box.png)

5. <span data-ttu-id="db87b-191">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="db87b-191">Select **Yes**.</span></span> 

    <span data-ttu-id="db87b-192">Dialoglodziņa **Ražošanas pasūtījumu izveide** laukā **MK numurs** un **Maršruta numurs** automātiski attiecīgi tiek atlasītas preces D8100 MK aktīvās versijas un maršruts.</span><span class="sxs-lookup"><span data-stu-id="db87b-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="db87b-193">Šajā gadījumā tiek atlasīts MK **000040** un maršruts **000040**.</span><span class="sxs-lookup"><span data-stu-id="db87b-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="db87b-194">Gan MK, gan maršruta izmaksu aprēķināšanai un plānošanai izmanto versiju 000040.</span><span class="sxs-lookup"><span data-stu-id="db87b-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="db87b-195">Laukā **Vieta** atlasiet **5**.</span><span class="sxs-lookup"><span data-stu-id="db87b-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="db87b-196">Laukā **Noliktava** atlasiet **51**.</span><span class="sxs-lookup"><span data-stu-id="db87b-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="db87b-197">Laukā **MK numurs** un **Maršruta numurs** automātiski atlasīto vērtību mainiet uz **000042**.</span><span class="sxs-lookup"><span data-stu-id="db87b-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db87b-198">Lai korpusa pārklāšanu ar apakšlīgumu nodotu kreditoram US-801, gan MK, gan maršrutam tiek izmantota versija 000042.</span><span class="sxs-lookup"><span data-stu-id="db87b-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Dialoglodziņā Ražošanas pasūtījumu izveide iestatītās vērtības](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="db87b-200">Lai izveidotu ražošanas pasūtījumu, atlasiet **Izveidot** un atgriezieties lapā **Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Jauns ražošanas pasūtījums lapā Visi ražošanas pasūtījumi](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="db87b-202">Lai atvērtu dialoglodziņu **Aprēķināšana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="db87b-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialoglodziņš Aprēķināšana](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="db87b-204">Lai apstiprinātu aprēķinu, atlasiet **Labi** un atgriezieties lapā **Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db87b-205">Kad ražošanas pasūtījums ir aprēķināts, kreditoram US-801 tiek ģenerēts pakalpojuma krājuma S8050 pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="db87b-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="db87b-206">Lai atvērtu lapu **MK**, kur var skatīt ražošanas pasūtījuma MK rindas, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **MK**.</span><span class="sxs-lookup"><span data-stu-id="db87b-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="db87b-207">Ievērojiet, ka pakalpojama krājumam S8050 ir pievienota atsauce uz pirkšanas pasūtījumu, kas tika ģenerēts, kad tikai aprēķināts ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="db87b-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Ražošanas pasūtījuma MK rindas MK lapā](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="db87b-209">Lai atgrieztos lapā **Visi ražošanas pasūtījumi**, aizveriet lapu **MK**.</span><span class="sxs-lookup"><span data-stu-id="db87b-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="db87b-210">Lai atvērtu dialoglodziņu **Darba grafika izveide**, darbību rūts cilnē **Grafiks** atlasiet **Izveidot darbu grafiku**.</span><span class="sxs-lookup"><span data-stu-id="db87b-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="db87b-211">Norādiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="db87b-211">Specify the following values:</span></span>

    - <span data-ttu-id="db87b-212">Laukā **Plānošanas virziens** atlasiet **Sākot no rītdienas**.</span><span class="sxs-lookup"><span data-stu-id="db87b-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="db87b-213">Iestatiet opcijas **Ierobežota noslodze** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="db87b-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialoglodziņš Darba grafika izveide](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="db87b-215">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Darba grafika izveide**, un atveriet atkal lapu **Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="db87b-216">Darbību rūts cilnē **Grafiks** atlasiet **Ganta diagramma**, lai atvērtu lapu **Ganta diagramma — resursu skats**.</span><span class="sxs-lookup"><span data-stu-id="db87b-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="db87b-217">Ganta diagramma sniedz vizuālu pārskatu par to, kā tiek izveidots grafiks par ražošanas darbiem, kas saistīti ar resursiem.</span><span class="sxs-lookup"><span data-stu-id="db87b-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="db87b-218">Ievērojiet, ka ārējā operācija Pārklāšana ietver trīs darbus: procesa darbu, transportēšanas darbu un gaidīšanas laika darbu.</span><span class="sxs-lookup"><span data-stu-id="db87b-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Ganta diagramma lapā Ganta diagramma — resursu skats](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="db87b-220">Lai atgrieztos lapā **Visi ražošanas pasūtījumi**, aizveriet lapu **Ganta diagramma — resursu skats** lapu.</span><span class="sxs-lookup"><span data-stu-id="db87b-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="db87b-221">Lai atvērtu dialoglodziņu **Izlaišana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Izlaist**.</span><span class="sxs-lookup"><span data-stu-id="db87b-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialoglodziņš Izlaišana](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="db87b-223">Lai dialoglodziņu **Izlaišana** aizvērtu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="db87b-224">Lai atvērtu dialoglodziņu **Automātiska MK un formulas rindu izlaide**, atlasiet **Ražošanas kontrole \> Regulārie uzdevumi \> Izlaišana uz noliktavu \> Automātiska MK un formulas rindu izlaide**.</span><span class="sxs-lookup"><span data-stu-id="db87b-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialoglodziņš Automātiska MK un formulas rindu izlaide](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="db87b-226">Lai palaistu automātisko MK un formulas rindu darbu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="db87b-227">Šis darbs izlaiž izejmateriālu izdošanas uz noliktavu darbu.</span><span class="sxs-lookup"><span data-stu-id="db87b-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="db87b-228">Lai atvērtu lapu **Visi ražošanas pasūtījumi**, atlasiet **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="db87b-229">Izmantojiet ātrās filtrēšanas lauku, lai atlasītu ražošanas pasūtījumu, pie kura strādājat.</span><span class="sxs-lookup"><span data-stu-id="db87b-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="db87b-230">Lai atvērtu lapu **Darbs**, darbību rūts cilnē **Noliktava** atlasiet **Darba detaļas**.</span><span class="sxs-lookup"><span data-stu-id="db87b-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="db87b-231">Ievērojiet, ka lapā ir redzami divi izejmateriālu izdošanas darbu komplekti.</span><span class="sxs-lookup"><span data-stu-id="db87b-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="db87b-232">Pirmais darbs attiecas uz materiālu M8100 un M8101.</span><span class="sxs-lookup"><span data-stu-id="db87b-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="db87b-233">Šie materiāli tiek izmantoti operācijā 10.</span><span class="sxs-lookup"><span data-stu-id="db87b-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="db87b-234">Otrais darbs attiecas uz materiālu M8202 un M8250.</span><span class="sxs-lookup"><span data-stu-id="db87b-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="db87b-235">Šie materiāli tiek izmantoti operācijā 20, kas ir apakšlīgumā paredzētā darbība.</span><span class="sxs-lookup"><span data-stu-id="db87b-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Divi izejmateriālu izdošanas darbu komplekti lapā Darbs](./media/subcontract22_work-page.png)

26. <span data-ttu-id="db87b-237">Lai apstrādātu noliktavas darba operāciju 10, palaidiet noliktavas programmu.</span><span class="sxs-lookup"><span data-stu-id="db87b-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="db87b-238">Lai atvērtu lapu **Visi ražošanas pasūtījumi**, atlasiet **Ražošanas kontrole \> Ražošanas pasūtījumi \> Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="db87b-239">Izmantojiet ātrās filtrēšanas lauku, lai atlasītu ražošanas pasūtījumu, pie kura strādājat.</span><span class="sxs-lookup"><span data-stu-id="db87b-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="db87b-240">Lai atvērtu dialoglodziņu **Sākšana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Sākt**.</span><span class="sxs-lookup"><span data-stu-id="db87b-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="db87b-241">Cilnē **Vispārīgi** norādiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="db87b-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="db87b-242">Laukā **No operācijas Nr.**</span><span class="sxs-lookup"><span data-stu-id="db87b-242">In the **From Oper. No.**</span></span> <span data-ttu-id="db87b-243">atlasiet **10**.</span><span class="sxs-lookup"><span data-stu-id="db87b-243">field, select **10**.</span></span>
    - <span data-ttu-id="db87b-244">Laukā **Uz operācijas Nr.**</span><span class="sxs-lookup"><span data-stu-id="db87b-244">In the **To Oper. No.**</span></span> <span data-ttu-id="db87b-245">atlasiet **10**.</span><span class="sxs-lookup"><span data-stu-id="db87b-245">field, select **10**.</span></span>

    ![Cilnē Vispārīgi iestatītās vērtības](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="db87b-247">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Sākšana**, un atveriet atkal lapu **Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="db87b-248">Ievērojiet, ka ražošanas pasūtījuma statuss tagad ir **Sākts**.</span><span class="sxs-lookup"><span data-stu-id="db87b-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="db87b-249">Operācijai 10 nepieciešamie materiāli tiek izmantoti pēc izdošanas saraksta žurnāla automātiskas grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="db87b-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="db87b-250">Laika patēriņš darbībai 10 tiek uzskaitīts pēc maršruta karšu žurnāla automātiskas grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="db87b-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="db87b-251">Lai apstrādātu noliktavas darba operāciju 20, palaidiet noliktavas programmu.</span><span class="sxs-lookup"><span data-stu-id="db87b-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="db87b-252">Lai atvērtu dialoglodziņu **Sākšana**, darbību rūts cilnē **Ražošanas pasūtījums** atlasiet **Sākt**.</span><span class="sxs-lookup"><span data-stu-id="db87b-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="db87b-253">Cilnē **Vispārīgi** norādiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="db87b-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="db87b-254">Laukā **No operācijas Nr.**</span><span class="sxs-lookup"><span data-stu-id="db87b-254">In the **From Oper. No.**</span></span> <span data-ttu-id="db87b-255">atlasiet **20**.</span><span class="sxs-lookup"><span data-stu-id="db87b-255">field, select **20**.</span></span>
    - <span data-ttu-id="db87b-256">Laukā **Uz operācijas Nr.**</span><span class="sxs-lookup"><span data-stu-id="db87b-256">In the **To Oper. No.**</span></span> <span data-ttu-id="db87b-257">atlasiet **20**.</span><span class="sxs-lookup"><span data-stu-id="db87b-257">field, select **20**.</span></span>
    - <span data-ttu-id="db87b-258">Laukā **Daudzums** ievadiet **10**.</span><span class="sxs-lookup"><span data-stu-id="db87b-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="db87b-259">Iestatiet opcijas **Grāmatot izdošanas sarakstu tagad** vērtību **Nē**.</span><span class="sxs-lookup"><span data-stu-id="db87b-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Cilnē Vispārīgi iestatītās vērtības](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="db87b-261">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Sākšana**, un atveriet atkal lapu **Visi ražošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="db87b-262">Tiek izveidots operācijā Pārklāšana izmantoto materiālu un pakalpojumu krājuma izdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="db87b-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="db87b-263">Pakalpojumu krājums pārstāv apakšlīgumā paredzētās operācijas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="db87b-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="db87b-264">Darbību rūts cilnē **Skats** atlasiet **Izdošanas saraksts**, lai atvērtu lapu **Izdošanas saraksts**.</span><span class="sxs-lookup"><span data-stu-id="db87b-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="db87b-265">Atlasiet izdošanas sarakstu, kas nav iegrāmatotas, un pēc tam atlasiet žurnāla numuru, lai skatītu žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="db87b-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Žurnāla rindas lapā Izdošanas saraksts](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="db87b-267">Darbību rūtī atlasiet **Drukāt** \> **Izdošanas saraksta pārskats**, lai atvērtu dialoglodziņu **Izdošanas saraksta pārskats**.</span><span class="sxs-lookup"><span data-stu-id="db87b-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="db87b-268">Iestatiet opcijas **Izmantot piegādes pavadzīmes izkārtojumu** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="db87b-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialoglodziņš Izdošanas saraksta pārskats](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="db87b-270">Lai ģenerētu pārskatu **Izdošanas saraksts**, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="db87b-271">Šajā gadījumā kreditora piegādes pavadzīme tiek drukāta no ražošanas izdošanas saraksta žurnāla.</span><span class="sxs-lookup"><span data-stu-id="db87b-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="db87b-272">Piegādes pavadzīmē ir norādīti materiāli, kas tiek nosūtīti kreditoram, kurš veic operāciju Pārklāšana.</span><span class="sxs-lookup"><span data-stu-id="db87b-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Izdošanas saraksta pārskats](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="db87b-274">Lai atgrieztos lapā **Izdošanas saraksts**, aizveriet pārskatu **Izdošanas saraksts**.</span><span class="sxs-lookup"><span data-stu-id="db87b-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="db87b-275">Darbību rūtī atlasiet **Grāmatot**, lai atvērtu dialoglodziņu **Žurnāla grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="db87b-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialoglodziņš Žurnāla grāmatošana](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="db87b-277">Lai dialoglodziņu **Žurnāla grāmatošana** aizvērtu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db87b-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="db87b-278">Atveriet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="db87b-278">Open the purchase order.</span></span>

    ![Pirkšanas pasūtījuma lapa](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="db87b-280">Darbību rūts cilnē **Pirkums** atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="db87b-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="db87b-281">Atlasiet **Grāmatot**, lai atvērtu dialoglodziņu **Žurnāla grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="db87b-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="db87b-282">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Žurnāla grāmatošana**, un atveriet atkal lapu **Pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="db87b-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="db87b-283">Mainiet vienības cenu no **33** uz **40**.</span><span class="sxs-lookup"><span data-stu-id="db87b-283">Change the unit price from **33** to **40**.</span></span>

    ![Pirkšanas pasūtījuma lapā mainīta vienības cena](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="db87b-285">Vēlreiz apstipriniet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="db87b-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="db87b-286">Preces ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="db87b-286">Product receipt.</span></span>

    ![Dialoglodziņš Preces ieejas plūsmas grāmatošana](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="db87b-288">Pirkšanas rēķins.</span><span class="sxs-lookup"><span data-stu-id="db87b-288">Purchase invoice.</span></span>
52. <span data-ttu-id="db87b-289">Atjauniniet atbilstības statusu.</span><span class="sxs-lookup"><span data-stu-id="db87b-289">Update the match status.</span></span>

    ![Kreditora rēķinu lapa](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="db87b-291">Sniedziet pārskatu, ka prece ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="db87b-291">Report as finished.</span></span>

    ![Dialoglodziņš Pārskata par preces pabeigšanu sniegšana](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="db87b-293">Nobeidziet procesu.</span><span class="sxs-lookup"><span data-stu-id="db87b-293">End.</span></span>

    ![Dialoglodziņš Beigšana](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="db87b-295">Izmaksu salīdzinājums.</span><span class="sxs-lookup"><span data-stu-id="db87b-295">Cost comparison.</span></span>

    ![Izmaksu salīdzinājuma diagrammas](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="db87b-297">Trūkstoši datu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="db87b-297">Missing setup in data.</span></span>
