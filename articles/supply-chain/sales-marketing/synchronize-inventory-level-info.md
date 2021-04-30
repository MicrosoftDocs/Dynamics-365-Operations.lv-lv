---
title: Programmā Supply Chain Management ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910284"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="d7da4-103">Programmā Supply Chain Management ietverto krājumu līmeņu informācijas sinhronizēšana ar programmu Field Service</span><span class="sxs-lookup"><span data-stu-id="d7da4-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d7da4-104">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietvertās krājumu līmeņu informācijas sinhronizēšanai ar programmu Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="d7da4-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="d7da4-105">[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="d7da4-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d7da4-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d7da4-106">Templates and tasks</span></span>
<span data-ttu-id="d7da4-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu programmā Supply Chain Management ietverto rīcībā esošo krājumu līmeņu sinhronizēšanu ar programmu Field Service.</span><span class="sxs-lookup"><span data-stu-id="d7da4-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="d7da4-108">**Veidne līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="d7da4-108">**Template in Data integration**</span></span>
- <span data-ttu-id="d7da4-109">Preču krājumi (no Supply Chain Management uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="d7da4-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="d7da4-110">**Uzdevums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="d7da4-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="d7da4-111">Preču krājumi</span><span class="sxs-lookup"><span data-stu-id="d7da4-111">Product inventory</span></span>

<span data-ttu-id="d7da4-112">Lai varētu veikt krājumu līmeņu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="d7da4-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="d7da4-113">Noliktavas (no Supply Chain Management uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="d7da4-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="d7da4-114">Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)</span><span class="sxs-lookup"><span data-stu-id="d7da4-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="d7da4-115">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="d7da4-115">Entity set</span></span>

| <span data-ttu-id="d7da4-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="d7da4-116">Field Service</span></span>                      | <span data-ttu-id="d7da4-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d7da4-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="d7da4-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="d7da4-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="d7da4-119">Dataverse Rīcībā esošie krājumi pēc noliktavas</span><span class="sxs-lookup"><span data-stu-id="d7da4-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="d7da4-120">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="d7da4-120">Entity flow</span></span>
<span data-ttu-id="d7da4-121">Programmā Finance and Operations ietvertā krājumu līmeņu informācija tiek nosūtīta uz programmu Field Service atlasītām precēm.</span><span class="sxs-lookup"><span data-stu-id="d7da4-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="d7da4-122">Krājumu līmeņa informācija ietver tālāk minētos datus.</span><span class="sxs-lookup"><span data-stu-id="d7da4-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="d7da4-123">Rīcībā esošais daudzums (pašreiz reģistrētais fiziskais daudzums, kas atrodas noliktavā)</span><span class="sxs-lookup"><span data-stu-id="d7da4-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="d7da4-124">Pasūtījumā iekļautais daudzums (kopējais pasūtījumā iekļautais daudzums, piemēram, pārdošanas pasūtījumi)</span><span class="sxs-lookup"><span data-stu-id="d7da4-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="d7da4-125">Pasūtītais daudzums (kopējais reģistrētais pasūtītais daudzums, piemēram, pirkšanas pasūtījumi)</span><span class="sxs-lookup"><span data-stu-id="d7da4-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="d7da4-126">Šī informācija ir iegūta par katru izlaisto preci katrai noliktavai un sinhronizēta, pamatojoties uz izmaiņu izsekošanu, mainoties krājumu līmenim.</span><span class="sxs-lookup"><span data-stu-id="d7da4-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="d7da4-127">Programmā Field Service integrācijas risinājums izveido krājumu žurnālus starpībai, lai līmeņi programmā Field Service atbilstu līmeņiem programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7da4-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="d7da4-128">Programma Supply Chain Management darbosies kā šablons krājumu līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="d7da4-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="d7da4-129">Tādēļ ir svarīgi iestatīt integrāciju darba pasūtījumiem, pārsūtīšanām un korekcijām no programmas Field Service programmā Supply Chain Management, ja šī funkcionalitāte tiek izmantota programmā Field Service, kopā ar krājumu līmeņu sinhronizāciju no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7da4-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="d7da4-130">Preces un noliktavas, kurās krājumu līmeņi tiek pārvaldīti no programmas Supply Chain Management, var kontrolēt, izmantojot vienumu Izvērsts vaicājums un filtrēšana (Power Query).</span><span class="sxs-lookup"><span data-stu-id="d7da4-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="d7da4-131">Ir iespējams izveidot vairākas noliktavas programmā Field Service (ja atlasīts iestatījums **Tiek ārēji uzturēts= Nē**) un pēc tam kartēt tās uz vienu noliktavu programmā Supply Chain Management, izmantojot funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="d7da4-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="d7da4-132">Tas tiek izmantots gadījumos, ja vēlaties, lai programma Field Service pārvalda detalizētu krājumu līmeni un tikai nosūta atjauninājumus uz programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7da4-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="d7da4-133">Šajā gadījumā programma Field Service nesaņems krājumu līmeņu atjauninājumus no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7da4-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="d7da4-134">Papildinformāciju skatiet sadaļā [Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) un [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="d7da4-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d7da4-135">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="d7da4-135">Field Service CRM solution</span></span>
<span data-ttu-id="d7da4-136">Elements **Ārējie preču krājumi** tiek izmantots tikai integrācijas iekšējos procesos.</span><span class="sxs-lookup"><span data-stu-id="d7da4-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="d7da4-137">Šis elements saņem krājumu līmeņu vērtības no programmas Supply Chain Management integrācijā un pārveido šīs vērtības manuālos krājumu žurnālos, kuri pēc tam maina krājumu preces noliktavā.</span><span class="sxs-lookup"><span data-stu-id="d7da4-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d7da4-138">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="d7da4-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="d7da4-139">Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="d7da4-139">Data integration</span></span>
<span data-ttu-id="d7da4-140">Lai projekts darbotos, ir jānodrošina, ka tiek atjaunināta msdynce_externalproductinventories integrācijas atslēga.</span><span class="sxs-lookup"><span data-stu-id="d7da4-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="d7da4-141">Dodieties uz **Datu integrācija > Savienojumu kopas**.</span><span class="sxs-lookup"><span data-stu-id="d7da4-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="d7da4-142">Atlasiet lietoto savienojuma kopu.</span><span class="sxs-lookup"><span data-stu-id="d7da4-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="d7da4-143">Cilnē **Integrācijas atslēga** nodrošiniet, lai msdynce_externalproductinventories tiktu pievienotas šādas atslēgas:</span><span class="sxs-lookup"><span data-stu-id="d7da4-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="d7da4-144">msdynce_productnumber (preces numurs)</span><span class="sxs-lookup"><span data-stu-id="d7da4-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="d7da4-145">msdynce_warehouseid (noliktavas ID)</span><span class="sxs-lookup"><span data-stu-id="d7da4-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="d7da4-146">Datu integrācijas projekts</span><span class="sxs-lookup"><span data-stu-id="d7da4-146">Data integration project</span></span>
<span data-ttu-id="d7da4-147">Varat lietot filtrus ar funkcionalitāti Izvērsts vaicājums un filtrēšana, lai tikai noteiktas preces un noliktavas sūta krājumu līmeņu informāciju no programmas Supply Chain Management uz programmu Field Service.</span><span class="sxs-lookup"><span data-stu-id="d7da4-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d7da4-148">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="d7da4-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="d7da4-149">Preču krājumi (no Supply Chain Management uz Field Service): Preču krājumi</span><span class="sxs-lookup"><span data-stu-id="d7da4-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="d7da4-150">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="d7da4-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]