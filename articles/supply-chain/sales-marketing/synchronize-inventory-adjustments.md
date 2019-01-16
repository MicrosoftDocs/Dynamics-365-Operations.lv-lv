---
title: "Programmā Field Service ietverto krājumu pārsūtīšanas un korekcijas darbību sinhronizēšana ar programmu Finance and Operations"
description: "Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu korekcijas un pārsūtīšanas darbības programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="75817-103">Programmā Field Service ietverto krājumu korekcijas darbību sinhronizēšana ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75817-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="75817-104">Šajā tēmā aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu krājumu korekcijas un pārsūtīšanas darbības programmā Microsoft Dynamics 365 for Finance and Operations ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="75817-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="75817-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="75817-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="75817-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="75817-106">Templates and tasks</span></span>
<span data-ttu-id="75817-107">Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu krājumu korekcijas un pārsūtīšanas darbības sinhronizēšanu programmā Microsoft Dynamics 365 for Field Service un programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75817-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="75817-108">**Veidņu nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="75817-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="75817-109">Krājumu korekcija (no programmas Field Service programmā Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="75817-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="75817-110">Krājumu pārsūtīšana (no programmas Field Service programmā Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="75817-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="75817-111">**Uzdevumu nosaukumi datu integrācijas projektos:**</span><span class="sxs-lookup"><span data-stu-id="75817-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="75817-112">Krājumu korekcijas</span><span class="sxs-lookup"><span data-stu-id="75817-112">Inventory Adjustments</span></span>
- <span data-ttu-id="75817-113">Krājumu pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="75817-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="75817-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="75817-114">Entity set</span></span>
| <span data-ttu-id="75817-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="75817-115">Field Service</span></span>                     | <span data-ttu-id="75817-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75817-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="75817-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="75817-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="75817-118">CDS krājumu korekciju žurnālu virsraksti un rindas</span><span class="sxs-lookup"><span data-stu-id="75817-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="75817-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="75817-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="75817-120">CDS krājumu pārsūtīšanas žurnālu virsraksti un rindas</span><span class="sxs-lookup"><span data-stu-id="75817-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="75817-121">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="75817-121">Entity flow</span></span>
<span data-ttu-id="75817-122">Programmā Field Service veiktās krājumu korekcijas un pārsūtīšanas darbības tiks sinhronizētas ar programmu Finance and Operations, kad vienumam **Grāmatošanas statuss** iestatījums tiek mainīts no Izveidots uz Grāmatots.</span><span class="sxs-lookup"><span data-stu-id="75817-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="75817-123">Kad tas notiek, korekcijas vai pārsūtīšanas pasūtījums tiks slēgts un kļūs tikai lasāms, jo korekcijas un pārsūtīšanas darbības var tikt grāmatotas programmā Finance and Operations un tādēļ tās nevar modificēt.</span><span class="sxs-lookup"><span data-stu-id="75817-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="75817-124">Programmā Finance and Operations var iestatīt pakešuzdevumu, lai automātiski grāmatotu korekcijas un pārsūtītu krājumu žurnālus, kas ģenerēti, veicot integrāciju.</span><span class="sxs-lookup"><span data-stu-id="75817-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="75817-125">Skatiet tālāk norādīto priekšnosacījumu, lai iegūtu informāciju par to, kā iespējot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="75817-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="75817-126">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="75817-126">Field Service CRM solution</span></span> 
<span data-ttu-id="75817-127">Entītijai Prece ir pievienots lauks Krājumu uzskaites vienība.</span><span class="sxs-lookup"><span data-stu-id="75817-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="75817-128">Šis lauks ir nepieciešams, jo pārdošanas un krājumu uzskaites vienības ne vienmēr sakrīt programmā Operations, un noliktavas krājumiem programmā Operations ir nepieciešama krājumu uzskaites vienība.</span><span class="sxs-lookup"><span data-stu-id="75817-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="75817-129">Atlasot iestatījumu Prece vienumam Krājumu korekcijas prece gan krājumu korekcijām, gan krājumu pārsūtīšanai, vienība tiks iegūta no preču krājumu preces vērtības.</span><span class="sxs-lookup"><span data-stu-id="75817-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="75817-130">Ja vērtība tiek atrasta, laukā Vienība tiek fiksēts iestatījums Krājumu korekcijas prece</span><span class="sxs-lookup"><span data-stu-id="75817-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="75817-131">Lauks Grāmatošanas statuss ir pievienots gan entītijai Krājumu korekcija, gan entītijai Krājumu pārvietošana.</span><span class="sxs-lookup"><span data-stu-id="75817-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="75817-132">Šo lauku izmanto kā filtru, ja korekcija vai pārsūtīšana tiek nosūtīta uz programmu Operations.</span><span class="sxs-lookup"><span data-stu-id="75817-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="75817-133">Laukam tiek iestatīta noklusējuma vērtība Izveidots (1), un pēc tam tas netiek nosūtīts uz programmu Operations.</span><span class="sxs-lookup"><span data-stu-id="75817-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="75817-134">Mainot vērtību uz Grāmatots (2), tas tiek sūtīts uz programmu Operations, bet pēc tam vairs nevarēsit neko mainīt sadaļā Korekcija vai Pārsūtīšana vai pievienot jaunas rindas.</span><span class="sxs-lookup"><span data-stu-id="75817-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="75817-135">Entītijai Krājumu korekcijas prece ir pievienots lauks Numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="75817-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="75817-136">Šis lauks palīdz nodrošināt integrācijai unikālu numuru, lai integrācijas process zina, kad veikt izveidošanu un kad veikt atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="75817-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="75817-137">Veidojot pirmo Krājumu korekcijas preci, tiks izveidots jauns ieraksts entītijā P2C automātiska numerācija, lai uzturētu izmantoto numuru sēriju un prefiksu.</span><span class="sxs-lookup"><span data-stu-id="75817-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="75817-138">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="75817-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="75817-139">Programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75817-139">In Finance and Operations</span></span>
<span data-ttu-id="75817-140">Integrācijas krājumu žurnālus, kas ģenerēti integrācijas ietvaros, var automātiski grāmatot, izmantojot pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="75817-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="75817-141">To iespējo šādi: Krājumu vadība > Periodiskie uzdevumi > CDS integrācija > Grāmatot integrācijas krājumu žurnālus</span><span class="sxs-lookup"><span data-stu-id="75817-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="75817-142">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="75817-142">Template mapping in Data integration</span></span>

<span data-ttu-id="75817-143">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="75817-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="75817-144">Krājumu korekcija (no programmas Field Service programmā Finance and Operations): Krājumu korekcija</span><span class="sxs-lookup"><span data-stu-id="75817-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="75817-145">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="75817-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="75817-146">Krājumu pārsūtīšana (no programmas Field Service programmā Finance and Operations): Krājumu pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="75817-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="75817-147">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="75817-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

