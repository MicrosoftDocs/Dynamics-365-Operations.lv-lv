---
title: Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6b2bdf1ca6f6ae43cd85c8a1353ee8305052761d
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/14/2019
ms.locfileid: "842560"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e7e8b-103">Programmā Finance and Operations ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service</span><span class="sxs-lookup"><span data-stu-id="e7e8b-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e7e8b-104">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e7e8b-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e7e8b-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="e7e8b-106">Templates and tasks</span></span>
<span data-ttu-id="e7e8b-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu programmā Microsoft Dynamics 365 for Finance and Operations ietverto rīcībā esošo krājumu līmeņu sinhronizēšanu ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e7e8b-108">**Veidne līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-108">**Template in Data integration**</span></span>
- <span data-ttu-id="e7e8b-109">Preču krājumi (no Fin and Ops uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="e7e8b-110">**Uzdevums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="e7e8b-111">Preču krājumi</span><span class="sxs-lookup"><span data-stu-id="e7e8b-111">Product inventory</span></span>

<span data-ttu-id="e7e8b-112">Lai varētu veikt krājumu līmeņu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e7e8b-113">Noliktavas (no Fin and Ops uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="e7e8b-114">Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e7e8b-115">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="e7e8b-115">Entity set</span></span>

| <span data-ttu-id="e7e8b-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e7e8b-116">Field Service</span></span>                      | <span data-ttu-id="e7e8b-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e7e8b-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e7e8b-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e7e8b-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e7e8b-119">Rīcībā esošie CDS krājumi pēc noliktavas</span><span class="sxs-lookup"><span data-stu-id="e7e8b-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e7e8b-120">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="e7e8b-120">Entity flow</span></span>
<span data-ttu-id="e7e8b-121">Programmā Finance and Operations ietvertā krājumu līmeņu informācija tiek nosūtīta uz programmu Field Service atlasītām precēm.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="e7e8b-122">Krājumu līmeņa informācija ietver tālāk minētos datus.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="e7e8b-123">Rīcībā esošais daudzums (pašreiz reģistrētais fiziskais daudzums, kas atrodas noliktavā)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="e7e8b-124">Pasūtījumā iekļautais daudzums (kopējais pasūtījumā iekļautais daudzums, piemēram, pārdošanas pasūtījumi)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="e7e8b-125">Pasūtītais daudzums (kopējais reģistrētais pasūtītais daudzums, piemēram, pirkšanas pasūtījumi)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="e7e8b-126">Šī informācija ir iegūta par katru izlaisto preci katrai noliktavai un sinhronizēta, pamatojoties uz izmaiņu izsekošanu, mainoties krājumu līmenim.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e7e8b-127">Programmā Field Service integrācijas risinājums izveido krājumu žurnālus starpībai, lai līmeņi programmā Field Service atbilstu līmeņiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="e7e8b-128">Programma Finance and Operations darbosies kā šablons krājumu līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="e7e8b-129">Tādēļ ir svarīgi iestatīt integrāciju darba pasūtījumiem, pārsūtīšanām un korekcijām no programmas Field Service programmā Finance and Operations, ja šī funkcionalitāte tiek izmantota programmā Field Service, kopā ar krājumu līmeņu sinhronizāciju no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="e7e8b-130">Preces un noliktavas, kurās krājumu līmeņi tiek pārvaldīti no programmas Finance and Operations, var kontrolēt, izmantojot vienumu Izvērsts vaicājums un filtrēšana (Power Query).</span><span class="sxs-lookup"><span data-stu-id="e7e8b-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="e7e8b-131">Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts** = Nē) un pēc tam kartēt tās uz vienu noliktavu programmā Finance and Operations, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e7e8b-132">Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un tikai nosūta atjauninājumus uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="e7e8b-133">Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="e7e8b-134">Papildinformāciju skatiet sadaļā [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="e7e8b-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e7e8b-135">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="e7e8b-135">Field Service CRM solution</span></span>
<span data-ttu-id="e7e8b-136">Elements **Ārējie preču krājumi** tiek izmantots tikai integrācijas iekšējos procesos.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="e7e8b-137">Šis elements saņem krājumu līmeņu vērtības no programmas Finance and Operations integrācijā un pārveido šīs vērtības manuālos krājumu žurnālos, kuri pēc tam maina krājumu preces noliktavā.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e7e8b-138">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="e7e8b-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="e7e8b-139">Datu integrācijas projekts</span><span class="sxs-lookup"><span data-stu-id="e7e8b-139">Data integration project</span></span>
<span data-ttu-id="e7e8b-140">Varat lietot filtrus ar funkcionalitāti Izvērsts vaicājums un filtrēšana, lai tikai noteiktas preces un noliktavas sūta krājumu līmeņu informāciju no programmas Finance and Operations uz programmu Field Service.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e7e8b-141">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="e7e8b-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="e7e8b-142">Preču krājumi (no Fin and Ops uz Field Service): Preču krājumi</span><span class="sxs-lookup"><span data-stu-id="e7e8b-142">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="e7e8b-143">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e7e8b-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
