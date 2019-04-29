---
title: Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmu Finance and Operations
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/14/2019
ms.locfileid: "842419"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="f64a0-103">Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f64a0-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f64a0-104">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f64a0-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f64a0-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="f64a0-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f64a0-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="f64a0-106">Templates and tasks</span></span>
<span data-ttu-id="f64a0-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu programmā Microsoft Dynamics 365 for Field Service ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanu ar programmu Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f64a0-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f64a0-108">**Veidnes līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="f64a0-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="f64a0-109">Krājumu korekcija (no Field Service uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f64a0-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="f64a0-110">Krājumu pārsūtīšana (no Field Service uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f64a0-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="f64a0-111">**Uzdevumi datu integrācijas projektos**</span><span class="sxs-lookup"><span data-stu-id="f64a0-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="f64a0-112">Krājumu korekcijas</span><span class="sxs-lookup"><span data-stu-id="f64a0-112">Inventory Adjustments</span></span>
- <span data-ttu-id="f64a0-113">Krājumu pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="f64a0-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="f64a0-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="f64a0-114">Entity set</span></span>
| <span data-ttu-id="f64a0-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="f64a0-115">Field Service</span></span>                     | <span data-ttu-id="f64a0-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f64a0-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="f64a0-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="f64a0-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="f64a0-118">CDS krājumu korekciju žurnālu virsraksti un rindas</span><span class="sxs-lookup"><span data-stu-id="f64a0-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="f64a0-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="f64a0-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="f64a0-120">CDS krājumu pārsūtīšanas žurnālu virsraksti un rindas</span><span class="sxs-lookup"><span data-stu-id="f64a0-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="f64a0-121">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="f64a0-121">Entity flow</span></span>
<span data-ttu-id="f64a0-122">Programmā Field Service veiktās krājumu korekcijas un pārsūtīšanas darbības tiks sinhronizētas ar programmu Finance and Operations pēc tam, kad vienumam **Grāmatošanas statuss** iestatījums tiek mainīts no **Izveidots** uz **Grāmatots**.</span><span class="sxs-lookup"><span data-stu-id="f64a0-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="f64a0-123">Kad tas notiek, korekcijas vai pārsūtīšanas pasūtījums tiks slēgts un kļūs tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="f64a0-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="f64a0-124">Tas nozīmē, ka korekcijas un pārsūtīšanas darbības var tikt grāmatotas programmā Finance and Operations, bet tās nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="f64a0-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="f64a0-125">Programmā Finance and Operations var iestatīt pakešuzdevumu, lai automātiski grāmatotu korekcijas un pārsūtītu krājumu žurnālus, kuri ģenerēti integrācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="f64a0-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="f64a0-126">Skatiet tālāk norādītos priekšnosacījumus, lai iegūtu informāciju par to, kā iespējot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="f64a0-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f64a0-127">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="f64a0-127">Field Service CRM solution</span></span> 
<span data-ttu-id="f64a0-128">Entītijai **Prece** ir pievienots lauks **Krājumu uzskaites vienība**.</span><span class="sxs-lookup"><span data-stu-id="f64a0-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="f64a0-129">Šis lauks ir nepieciešams, jo pārdošanas un krājumu uzskaites vienības ne vienmēr sakrīt programmā Finance and Operations, un noliktavas krājumiem programmā Finance and Operations ir nepieciešama krājumu uzskaites vienība.</span><span class="sxs-lookup"><span data-stu-id="f64a0-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="f64a0-130">Atlasot preci vienumam Krājumu korekcijas prece gan krājumu korekcijām, gan krājumu pārsūtīšanai, vienība tiks iegūta no krājumu preces vērtības.</span><span class="sxs-lookup"><span data-stu-id="f64a0-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="f64a0-131">Ja vērtība tiek atrasta, laukā **Vienība** tiek fiksēts iestatījums Krājumu korekcijas prece.</span><span class="sxs-lookup"><span data-stu-id="f64a0-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="f64a0-132">Lauks **Grāmatošanas statuss** ir pievienots gan entītijai **Krājumu korekcija**, gan entītijai **Krājumu pārvietošana**.</span><span class="sxs-lookup"><span data-stu-id="f64a0-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="f64a0-133">Šo lauku izmanto kā filtru, ja korekcija vai pārsūtīšana tiek nosūtīta uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f64a0-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="f64a0-134">Šī lauka noklusējuma iestatījums ir Izveidots (1), taču tas netiek nosūtīts uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f64a0-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="f64a0-135">Atjauninot vērtību uz Grāmatots (2), tas tiek sūtīts uz programmu Finance and Operations, bet pēc tam vairs nevarēsit mainīt korekciju un pārsūtīšanas darbību vai pievienot jaunas rindas.</span><span class="sxs-lookup"><span data-stu-id="f64a0-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="f64a0-136">Entītijai **Krājumu korekcijas prece** ir pievienots lauks **Numuru sērija**.</span><span class="sxs-lookup"><span data-stu-id="f64a0-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="f64a0-137">Šis lauks nodrošina to, ka integrācijai ir unikāls numurs, tādējādi integrācija var izveidot un atjaunināt korekciju.</span><span class="sxs-lookup"><span data-stu-id="f64a0-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="f64a0-138">Veidojot pirmo krājumu korekcijas preci, tiks izveidots jauns ieraksts entītijā **P2C automātiska numerācija**, lai uzturētu izmantoto numuru sēriju un prefiksu.</span><span class="sxs-lookup"><span data-stu-id="f64a0-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f64a0-139">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="f64a0-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="f64a0-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f64a0-140">Finance and Operations</span></span>
<span data-ttu-id="f64a0-141">Integrācijas krājumu žurnālus, kas ģenerēti integrācijas ietvaros, var automātiski grāmatot, izmantojot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="f64a0-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="f64a0-142">To iespējo šādi: **Krājumu vadība > Periodiskie uzdevumi > CDS integrācija > Grāmatot integrācijas krājumu žurnālus**.</span><span class="sxs-lookup"><span data-stu-id="f64a0-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f64a0-143">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="f64a0-143">Template mapping in Data integration</span></span>

<span data-ttu-id="f64a0-144">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="f64a0-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="f64a0-145">Krājumu korekcija (no Field Service uz Fin and Ops): Krājumu korekcija</span><span class="sxs-lookup"><span data-stu-id="f64a0-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="f64a0-146">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="f64a0-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="f64a0-147">Krājumu pārsūtīšana (no Field Service uz Fin and Ops): Krājumu pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="f64a0-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="f64a0-148">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="f64a0-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
