---
title: "Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service"
description: "Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu līmeņu informāciju programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="b45b5-103">Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service</span><span class="sxs-lookup"><span data-stu-id="b45b5-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b45b5-104">Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu līmeņu informāciju programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="b45b5-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b45b5-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="b45b5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b45b5-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="b45b5-106">Templates and tasks</span></span>
<span data-ttu-id="b45b5-107">Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu rīcībā esošo krājumu līmeņu sinhronizēšanu programmā Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="b45b5-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b45b5-108">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="b45b5-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="b45b5-109">Preču krājumi (no programmas Finance and Operations programmā Field Service)</span><span class="sxs-lookup"><span data-stu-id="b45b5-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="b45b5-110">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="b45b5-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="b45b5-111">Preču krājumi </span><span class="sxs-lookup"><span data-stu-id="b45b5-111">Product inventory</span></span>

<span data-ttu-id="b45b5-112">Lai varētu veikt krājumu līmeņu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="b45b5-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="b45b5-113">Noliktavas (no programmas Finance and Operations programmā Field Service)</span><span class="sxs-lookup"><span data-stu-id="b45b5-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="b45b5-114">Field Service preces ar krājumu uzskaites vienību (no programmas Finance and Operations programmā Sales)</span><span class="sxs-lookup"><span data-stu-id="b45b5-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="b45b5-115">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="b45b5-115">Entity set</span></span>

| <span data-ttu-id="b45b5-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="b45b5-116">Field Service</span></span>                      | <span data-ttu-id="b45b5-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b45b5-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="b45b5-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="b45b5-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="b45b5-119">Rīcībā esošie CDS krājumi pēc noliktavas</span><span class="sxs-lookup"><span data-stu-id="b45b5-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="b45b5-120">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="b45b5-120">Entity flow</span></span>
<span data-ttu-id="b45b5-121">Programmā Finance and Operations ietverto krājumu līmeņu informācija tiek nosūtīta uz programmu Field Service atlasītām precēm.</span><span class="sxs-lookup"><span data-stu-id="b45b5-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="b45b5-122">Krājumu līmeņa informācija ietver tālāk minētos datus.</span><span class="sxs-lookup"><span data-stu-id="b45b5-122">The inventory level information include:</span></span> 
- <span data-ttu-id="b45b5-123">Rīcībā esošais daudzums (pašreiz reģistrētais fiziskais daudzums, kas atrodas noliktavā)</span><span class="sxs-lookup"><span data-stu-id="b45b5-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="b45b5-124">Pasūtījumā iekļautais daudzums (kopējais pasūtījumā iekļautais daudzums — t. i., pārdošanas pasūtījumi)</span><span class="sxs-lookup"><span data-stu-id="b45b5-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="b45b5-125">Pasūtītais daudzums (kopējais reģistrētais pasūtītais daudzums — t. i., pirkšanas pasūtījumi)</span><span class="sxs-lookup"><span data-stu-id="b45b5-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="b45b5-126">Šī informācija ir iegūta par katru izlaisto preci katrai noliktavai un sinhronizēta, pamatojoties uz izmaiņu izsekošanu, mainoties krājumu līmenim.</span><span class="sxs-lookup"><span data-stu-id="b45b5-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="b45b5-127">Programmā Field Service integrācijas risinājums izveido krājumu žurnālus starpībai, lai līmeņi programmā Field Service atbilstu līmeņiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b45b5-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="b45b5-128">Programma Finance and Operations darbosies kā šablons krājumu līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="b45b5-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="b45b5-129">Tāpēc ir svarīgi iestatīt integrāciju darba pasūtījumiem, pārsūtīšanām un korekcijām no programmas Field Service programmā Finance and Operations, ja šī funkcionalitāte tiek izmantota programmā Field Service, kopā ar krājumu līmeņu sinhronizāciju no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b45b5-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="b45b5-130">Preces un noliktavas, kurās krājumu līmeņi tiek pārvaldīti no programmas Finance and Operations, var kontrolēt, izmantojot vienumu Izvērsts vaicājums un filtrēšana (Power Query).</span><span class="sxs-lookup"><span data-stu-id="b45b5-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="b45b5-131">Piezīme. Ir iespējams izveidot vairākas noliktavas programmā Field Services (ja atlasīts iestatījums Tiek ārēji uzturēts = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="b45b5-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="b45b5-132">Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un vienkārši nosūta atjauninājumus uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b45b5-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="b45b5-133">Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b45b5-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="b45b5-134">Papildinformāciju skatiet sadaļā Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations un Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b45b5-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b45b5-135">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="b45b5-135">Field Service CRM solution</span></span>
<span data-ttu-id="b45b5-136">Entītija Ārējie preču krājumi ir jauna entītija, kas tiek izmantota tikai integrācijas iekšējos procesos.</span><span class="sxs-lookup"><span data-stu-id="b45b5-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="b45b5-137">Tā saņem krājumu līmeņu vērtības no programmas Finance and Operations integrācijā un pārveido šīs vērtības manuālos krājumu žurnālos, kuri pēc tam maina krājumu preces noliktavā.</span><span class="sxs-lookup"><span data-stu-id="b45b5-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b45b5-138">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="b45b5-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="b45b5-139">Datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="b45b5-139">In the Data Integration project</span></span>
<span data-ttu-id="b45b5-140">Lietojiet filtrus ar funkcionalitāti Izvērsts vaicājums un filtrēšana, lai kontrolētu, ka tikai nepieciešamās preces un noliktavas sūta krājumu līmeņu informāciju no programmas Finance and Operations uz programmu Field Service.</span><span class="sxs-lookup"><span data-stu-id="b45b5-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b45b5-141">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="b45b5-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="b45b5-142">Preču krājumi (no programmas Finance and Operations programmā Field Service): Preču krājumi</span><span class="sxs-lookup"><span data-stu-id="b45b5-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="b45b5-143">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="b45b5-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

