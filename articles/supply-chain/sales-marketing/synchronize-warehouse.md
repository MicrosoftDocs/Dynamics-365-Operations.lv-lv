---
title: "Programmā Finance and Operations ietverto noliktavu sinhronizēšana ar programmu Field Service"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto noliktavu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="deb43-103">Programmā Finance and Operations ietverto noliktavu sinhronizēšana ar programmu Field Service</span><span class="sxs-lookup"><span data-stu-id="deb43-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="deb43-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto noliktavu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="deb43-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="deb43-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="deb43-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="deb43-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="deb43-106">Templates and tasks</span></span>
<span data-ttu-id="deb43-107">Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu noliktavu sinhronizēšanu programmā Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="deb43-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="deb43-108">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="deb43-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="deb43-109">Noliktavas (no programmas Finance and Operations programmā Field Service)</span><span class="sxs-lookup"><span data-stu-id="deb43-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="deb43-110">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="deb43-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="deb43-111">Noliktava</span><span class="sxs-lookup"><span data-stu-id="deb43-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="deb43-112">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="deb43-112">Entity set</span></span>
| <span data-ttu-id="deb43-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="deb43-113">Field Service</span></span>    | <span data-ttu-id="deb43-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="deb43-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="deb43-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="deb43-115">msdyn_warehouses</span></span> | <span data-ttu-id="deb43-116">Noliktavas</span><span class="sxs-lookup"><span data-stu-id="deb43-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="deb43-117">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="deb43-117">Entity flow</span></span>
<span data-ttu-id="deb43-118">Noliktavas, kas ir izveidotas un uzturētas programmā Finance and Operations, var sinhronizēt ar risinājumu Field Service, izmantojot Common Data Service (CDS) datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="deb43-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="deb43-119">Nepieciešamās noliktavas, kuras tiek sinhronizētas ar programmu Field Service, var kontrolēt ar funkcionalitāti Izvērsts vaicājums un filtrēšana projektā.</span><span class="sxs-lookup"><span data-stu-id="deb43-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="deb43-120">Noliktavas, kuras tiek sinhronizētas no programmas Finance and Operations, tiek izveidotas programmā Field Service ar iestatījumu Jā laukā Tiek uzturēts ārēji, un ieraksts ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="deb43-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="deb43-121">Risinājums Field Service CRM Lai atbalstītu integrāciju starp risinājumiem Field Service un Finance and Operations, ir nepieciešama papildu funkcionalitāte no pakalpojuma Field Service CRM.</span><span class="sxs-lookup"><span data-stu-id="deb43-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="deb43-122">Risinājumā ir ietvertas šādas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="deb43-122">The solution includes the following changes.</span></span>
<span data-ttu-id="deb43-123">Entītijai **Noliktava (msdyn_warehouses)** ir pievienots lauks **Tiek uzturēti ārēji**.</span><span class="sxs-lookup"><span data-stu-id="deb43-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="deb43-124">Šis lauks palīdz noteikt, vai noliktavas pārvaldība tiek veikta no programmas Operations vai arī tā pastāv tikai programmā Field Service.</span><span class="sxs-lookup"><span data-stu-id="deb43-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="deb43-125">Jā — noliktava ir iegūta no programmas Finance and Operations, un to nevar rediģēt programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="deb43-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="deb43-126">Nē — noliktava tika ievadīta tieši programmā Field Service un tiek uzturēta šeit.</span><span class="sxs-lookup"><span data-stu-id="deb43-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="deb43-127">Lauks **Tiek ārēji uzturēts** palīdz kontrolēt krājumu līmeņu, korekciju, pārsūtīšanu un lietojuma sinhronizēšanu darba pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="deb43-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="deb43-128">Lai veiktu sinhronizēšanu tieši uz to pašu noliktavu citā sistēmā, var izmantot tikai noliktavas, kurām vienumam **Tiek ārēji uzturēts** atlasīts iestatījums Jā.</span><span class="sxs-lookup"><span data-stu-id="deb43-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="deb43-129">Piezīme. Ir iespējams izveidot vairākas noliktavas programmā Field Services (ja atlasīts iestatījums **Tiek ārēji uzturēts** = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="deb43-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="deb43-130">Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un vienkārši nosūta atjauninājumus uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="deb43-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="deb43-131">Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="deb43-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="deb43-132">Papildinformāciju skatiet sadaļā Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations un Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="deb43-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="deb43-133">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="deb43-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="deb43-134">Datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="deb43-134">In the Data Integration project</span></span>
<span data-ttu-id="deb43-135">Pirms noliktavu sinhronizācijas pārliecinieties, vai ir atjaunināta funkcionalitāte Izvērsts vaicājums un filtrēšana projektā, lai tiktu iekļautas tikai noliktavas, kuras vēlaties pārnest no programmas Finance and Operations uz programmu Field Service.</span><span class="sxs-lookup"><span data-stu-id="deb43-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="deb43-136">Ņemiet vērā, ka noliktava programmā Field Service būs nepieciešama, lai to lietotu darba pasūtījumos, korekcijās un pārsūtīšanās.</span><span class="sxs-lookup"><span data-stu-id="deb43-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="deb43-137">Pārliecinieties, ka pastāv **Integrācijas atslēga** entītijai **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="deb43-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="deb43-138">Atveriet sadaļu Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="deb43-138">Go to Data Integration</span></span>
2. <span data-ttu-id="deb43-139">Atlasiet cilni **Savienojumu kopa**</span><span class="sxs-lookup"><span data-stu-id="deb43-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="deb43-140">Atlasiet savienojumu kopu, kas tiek izmantota darba pasūtījumu sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="deb43-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="deb43-141">Atlasiet cilni **Integrācijas atslēga**</span><span class="sxs-lookup"><span data-stu-id="deb43-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="deb43-142">Atrodiet msdyn_warehouses un pārbaudiet, vai atslēga **msdyn_name (nosaukums)** ir pievienota.</span><span class="sxs-lookup"><span data-stu-id="deb43-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="deb43-143">Ja tā nav redzama, pievienojiet to, noklikšķinot uz **Pievienot atslēgu**, un noklikšķiniet uz **Saglabāt** lapas augšpusē</span><span class="sxs-lookup"><span data-stu-id="deb43-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="deb43-144">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="deb43-144">Template mapping in Data integration</span></span>

<span data-ttu-id="deb43-145">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="deb43-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="deb43-146">Noliktavas (no programmas Finance and Operations programmā Field Service): Noliktava</span><span class="sxs-lookup"><span data-stu-id="deb43-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="deb43-147">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="deb43-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

