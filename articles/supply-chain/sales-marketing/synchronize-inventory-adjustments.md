---
title: Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmatūru Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/30/2019
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
ms.openlocfilehash: 9f3bfe950446a6e87e34c32d2593cba0af84d8e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838985"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="7b8eb-103">Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmatūru Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7b8eb-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7b8eb-104">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto krājumu korekciju un pārsūtīšanas darbību sinhronizēšanai ar programmu Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="7b8eb-105">[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="7b8eb-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7b8eb-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="7b8eb-106">Templates and tasks</span></span>
<span data-ttu-id="7b8eb-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai sinhronizētu krājumu korekciju un pārsūtīšanu no programmas Field Service uz Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="7b8eb-108">**Veidnes līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="7b8eb-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="7b8eb-109">Krājumu korekcija (no Field Service uz Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7b8eb-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="7b8eb-110">Krājumu pārsūtījumi (no Field Service uz Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="7b8eb-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="7b8eb-111">**Uzdevumi datu integrācijas projektos**</span><span class="sxs-lookup"><span data-stu-id="7b8eb-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="7b8eb-112">Krājumu korekcijas</span><span class="sxs-lookup"><span data-stu-id="7b8eb-112">Inventory Adjustments</span></span>
- <span data-ttu-id="7b8eb-113">Krājumu pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="7b8eb-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="7b8eb-114">Tabulu kopa</span><span class="sxs-lookup"><span data-stu-id="7b8eb-114">Table set</span></span>
| <span data-ttu-id="7b8eb-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="7b8eb-115">Field Service</span></span>                     | <span data-ttu-id="7b8eb-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7b8eb-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="7b8eb-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="7b8eb-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="7b8eb-118">Dataverse Krājumu korekciju žurnālu virsraksti un rindas</span><span class="sxs-lookup"><span data-stu-id="7b8eb-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="7b8eb-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="7b8eb-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="7b8eb-120">Dataverse Krājumu pārsūtīšanas žurnālu virsraksti un rindas</span><span class="sxs-lookup"><span data-stu-id="7b8eb-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="7b8eb-121">Tabulu plūsma</span><span class="sxs-lookup"><span data-stu-id="7b8eb-121">Table flow</span></span>
<span data-ttu-id="7b8eb-122">Programmā Field Service veiktās krājumu korekcijas un pārsūtīšanas darbības tiks sinhronizētas ar programmatūru Supply Chain Management pēc tam, kad vienumam **Grāmatošanas statuss** iestatījums tiek mainīts no **Izveidots** uz **Grāmatots**.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="7b8eb-123">Kad tas notiek, korekcijas vai pārsūtīšanas pasūtījums tiks slēgts un kļūs tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="7b8eb-124">Tas nozīmē, ka korekcijas un pārsūtīšanas darbības var tikt grāmatotas programmatūrā Supply Chain Management, bet tās nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="7b8eb-125">Programmatūrā Supply Chain Management var iestatīt pakešuzdevumu, lai automātiski grāmatotu korekcijas un pārsūtītu krājumu žurnālus, kuri ģenerēti integrācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="7b8eb-126">Skatiet tālāk norādītos priekšnosacījumus, lai iegūtu informāciju par to, kā iespējot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="7b8eb-127">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="7b8eb-127">Field Service CRM solution</span></span> 
<span data-ttu-id="7b8eb-128">Tabulai **Prece** ir pievienota kolonna **Krājumu uzskaites vienība**.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="7b8eb-129">Šī kolonna ir nepieciešama, jo pārdošanas un krājumu uzskaites vienības ne vienmēr sakrīt programmatūrā Supply Chain Management, un noliktavas krājumiem programmatūrā Supply Chain Management ir nepieciešama krājumu uzskaites vienība.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="7b8eb-130">Atlasot preci vienumam Krājumu korekcijas prece gan krājumu korekcijām, gan krājumu pārsūtīšanai, vienība tiks iegūta no krājumu preces vērtības.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="7b8eb-131">Ja vērtība tiek atrasta, kolonnā **Vienība** tiek fiksēts iestatījums Krājumu korekcijas prece.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="7b8eb-132">Kolonna **Grāmatošanas statuss** ir pievienota gan tabulai **Krājumu korekcija**, gan tabulai **Krājumu pārvietošana**.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="7b8eb-133">Šo kolonnu izmanto kā filtru, ja korekcija vai pārsūtīšana tiek nosūtīta uz programmatūru Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="7b8eb-134">Šīs kolonnas noklusējuma iestatījums ir Izveidots (1), taču tas netiek nosūtīts uz programmatūru Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="7b8eb-135">Atjauninot vērtību uz Grāmatots (2), tas tiek sūtīts uz programmatūru Supply Chain Management, bet pēc tam vairs nevarēsit mainīt korekciju un pārsūtīšanas darbību vai pievienot jaunas rindas.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="7b8eb-136">Tabulai **Krājumu korekcijas prece** ir pievienota kolonna **Numuru sērija**.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="7b8eb-137">Šī kolonna nodrošina to, ka integrācijai ir unikāls numurs, tādējādi integrācija var izveidot un atjaunināt korekciju.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="7b8eb-138">Veidojot pirmo krājumu korekcijas preci, tiks izveidots jauns ieraksts tabulā **P2C AutoNumber**, lai uzturētu izmantoto numuru sēriju un prefiksu.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7b8eb-139">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="7b8eb-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="7b8eb-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7b8eb-140">Supply Chain Management</span></span>
<span data-ttu-id="7b8eb-141">Integrācijas krājumu žurnālus, kas ģenerēti integrācijas ietvaros, var automātiski grāmatot, izmantojot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="7b8eb-142">To iespējo šādi: **Krājumu vadība > Periodiskie uzdevumi > Dataverse integrācija > Grāmatot integrācijas krājumu žurnālus**.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b8eb-143">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="7b8eb-143">Template mapping in Data integration</span></span>

<span data-ttu-id="7b8eb-144">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="7b8eb-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="7b8eb-145">Krājumu korekcija (no Field Service uz Supply Chain Management): Krājumu korekcija</span><span class="sxs-lookup"><span data-stu-id="7b8eb-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="7b8eb-146">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="7b8eb-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="7b8eb-147">Krājumu pārsūtījumi (no Field Service uz Supply Chain Management): Krājumu pārsūtījumi</span><span class="sxs-lookup"><span data-stu-id="7b8eb-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="7b8eb-148">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="7b8eb-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]