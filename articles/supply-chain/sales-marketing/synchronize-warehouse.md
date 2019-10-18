---
title: Programmatūrā Supply Chain Management ietverto noliktavu sinhronizēšana ar Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto noliktavu sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 94fb6720152cbf6aec58d2b8d9d02fc5343c05e2
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251182"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="575cb-103">Programmatūrā Supply Chain Management ietverto noliktavu sinhronizēšana ar Field Service</span><span class="sxs-lookup"><span data-stu-id="575cb-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="575cb-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto noliktavu sinhronizēšanai ar programmu Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="575cb-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="575cb-105">[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="575cb-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="575cb-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="575cb-106">Templates and tasks</span></span>
<span data-ttu-id="575cb-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai palaistu noliktavu sinhronizāciju no programmatūras Supply Chain Management uz Field Service.</span><span class="sxs-lookup"><span data-stu-id="575cb-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="575cb-108">**Veidne līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="575cb-108">**Template in Data integration**</span></span>
- <span data-ttu-id="575cb-109">Noliktavas (no Supply Chain Management uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="575cb-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="575cb-110">**Uzdevums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="575cb-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="575cb-111">Noliktava</span><span class="sxs-lookup"><span data-stu-id="575cb-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="575cb-112">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="575cb-112">Entity set</span></span>
| <span data-ttu-id="575cb-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="575cb-113">Field Service</span></span>    | <span data-ttu-id="575cb-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="575cb-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="575cb-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="575cb-115">msdyn_warehouses</span></span> | <span data-ttu-id="575cb-116">Noliktavas</span><span class="sxs-lookup"><span data-stu-id="575cb-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="575cb-117">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="575cb-117">Entity flow</span></span>
<span data-ttu-id="575cb-118">Noliktavas, kas ir izveidotas un uzturētas programmatūrā Supply Chain Management, var sinhronizēt ar risinājumu Field Service, izmantojot Common Data Service (CDS) datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="575cb-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="575cb-119">Noliktavas, kuras vēlaties sinhronizēt ar programmu Field Service, var kontrolēt ar funkcionalitāti Izvērsts vaicājums un filtrēšana projektā.</span><span class="sxs-lookup"><span data-stu-id="575cb-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="575cb-120">Noliktavas, kuras tiek sinhronizētas no programmatūras Supply Chain Management, tiek izveidotas programmā Field Service ar iestatījumu **Jā** laukā **Tiek uzturēts ārēji**, un ieraksts ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="575cb-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="575cb-121">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="575cb-121">Field Service CRM solution</span></span>
<span data-ttu-id="575cb-122">Lai atbalstītu integrāciju starp risinājumiem Field Service un Finance and Operations ir nepieciešama papildu funkcionalitāte no pakalpojuma Field Service CRM.</span><span class="sxs-lookup"><span data-stu-id="575cb-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="575cb-123">Risinājumā entītijai **Noliktava (msdyn_warehouses)** ir pievienots lauks **Tiek uzturēti ārēji**.</span><span class="sxs-lookup"><span data-stu-id="575cb-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="575cb-124">Šis lauks palīdz noteikt, vai noliktavas pārvaldība tiek veikta no programmatūras Supply Chain Management vai arī tā pastāv tikai programmā Field Service.</span><span class="sxs-lookup"><span data-stu-id="575cb-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="575cb-125">Šim laukam ir pieejami šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="575cb-125">The settings for this field include:</span></span>
- <span data-ttu-id="575cb-126">**Jā**— noliktava ir iegūta no programmatūras Supply Chain Management, un to nevar rediģēt programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="575cb-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="575cb-127">**Nē** — noliktava tika ievadīta tieši programmā Field Service un tiek uzturēta šeit.</span><span class="sxs-lookup"><span data-stu-id="575cb-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="575cb-128">Lauks **Tiek ārēji uzturēts** palīdz kontrolēt krājumu līmeņu, korekciju, pārsūtīšanu un lietojuma sinhronizēšanu darba pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="575cb-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="575cb-129">Lai veiktu sinhronizēšanu tieši uz to pašu noliktavu citā sistēmā, var izmantot tikai noliktavas, kurām vienumam **Tiek ārēji uzturēts** atlasīts iestatījums **Jā**.</span><span class="sxs-lookup"><span data-stu-id="575cb-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="575cb-130">Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts** = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="575cb-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="575cb-131">Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un vienkārši nosūta atjauninājumus uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="575cb-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="575cb-132">Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="575cb-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="575cb-133">Papildinformāciju skatiet sadaļā [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="575cb-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="575cb-134">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="575cb-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="575cb-135">Datu integrācijas projekts</span><span class="sxs-lookup"><span data-stu-id="575cb-135">Data Integration project</span></span>
<span data-ttu-id="575cb-136">Pirms noliktavu sinhronizācijas pārliecinieties, vai ir atjaunināta funkcionalitāte Izvērsts vaicājums un filtrēšana projektā, lai tiktu iekļautas tikai noliktavas, kuras vēlaties pārnest no programmatūras Supply Chain Management uz programmu Field Service.</span><span class="sxs-lookup"><span data-stu-id="575cb-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="575cb-137">Ņemiet vērā, ka noliktava programmā Field Service būs nepieciešama, lai to lietotu darba pasūtījumos, korekcijās un pārsūtīšanās.</span><span class="sxs-lookup"><span data-stu-id="575cb-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="575cb-138">Lai pārliecinātos, ka pastāv **Integrācijas atslēga** entītijai **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="575cb-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="575cb-139">Atveriet sadaļu Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="575cb-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="575cb-140">Atlasiet cilni **Savienojumu kopa**.</span><span class="sxs-lookup"><span data-stu-id="575cb-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="575cb-141">Atlasiet savienojumu kopu, kas tiek izmantota darba pasūtījumu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="575cb-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="575cb-142">Atlasiet cilni **Integrācijas atslēga**.</span><span class="sxs-lookup"><span data-stu-id="575cb-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="575cb-143">Atrodiet msdyn_warehouses un pārliecinieties, vai atslēga **msdyn_name (nosaukums)** ir pievienota.</span><span class="sxs-lookup"><span data-stu-id="575cb-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="575cb-144">Ja tā nav redzama, pievienojiet to, noklikšķinot uz **Pievienot atslēgu**, un pēc tam noklikšķiniet uz **Saglabāt** lapas augšpusē.</span><span class="sxs-lookup"><span data-stu-id="575cb-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="575cb-145">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="575cb-145">Template mapping in Data integration</span></span>

<span data-ttu-id="575cb-146">Tālāk esošajā attēlā ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="575cb-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="575cb-147">Noliktavas (no Supply Chain Management uz Field Service): Noliktava</span><span class="sxs-lookup"><span data-stu-id="575cb-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="575cb-148">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="575cb-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
