---
title: Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843413"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="b672b-103">Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b672b-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b672b-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b672b-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b672b-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="b672b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="b672b-106">Izmantotā veidne **Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops)** ir izveidota, pamatojoties uz veidni **Darba pasūtījumu (no Field Service uz Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="b672b-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="b672b-107">Papildinformāciju skatiet rakstā [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="b672b-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="b672b-108">Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības.</span><span class="sxs-lookup"><span data-stu-id="b672b-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="b672b-109">**Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="b672b-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="b672b-110">**Darba pasūtījumi (no Field Service uz Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="b672b-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="b672b-111">Galvenā atšķirība ir tā, ka šajā veidnē ir ietverta programmā Field Service darba pasūtījumam piešķirtā projekta numura kartēšana, nodrošinot, ka pārdošanas pasūtījums, kas izveidots programmā Finance and Operations, ietver projekta numuru un ka saistītajam projektam var veikt rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="b672b-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="b672b-112">Papildus tam veidne izmanto funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="b672b-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b672b-113">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="b672b-113">Templates and tasks</span></span>

<span data-ttu-id="b672b-114">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="b672b-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="b672b-115">Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b672b-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="b672b-116">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="b672b-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="b672b-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="b672b-117">WorkOrderHeader</span></span>
- <span data-ttu-id="b672b-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="b672b-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="b672b-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="b672b-119">WorkOrderProduct</span></span>
- <span data-ttu-id="b672b-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="b672b-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b672b-121">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="b672b-121">Field Service CRM solution</span></span>
<span data-ttu-id="b672b-122">Entītijai Darba pasūtījums ir pievienots lauks **Ārējais projekts**.</span><span class="sxs-lookup"><span data-stu-id="b672b-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="b672b-123">Šis lauks ir uzmeklēšanas lauks, un, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b672b-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="b672b-124">Kad vienumam **Sistēmas statuss** iestatījums Atvērts - Notiek izpilde(690,970,000) tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="b672b-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b672b-125">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="b672b-125">Template mapping in Data integration</span></span>

<span data-ttu-id="b672b-126">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="b672b-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="b672b-127">Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="b672b-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="b672b-128">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="b672b-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="b672b-129">Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="b672b-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="b672b-130">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="b672b-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="b672b-131">Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="b672b-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="b672b-132">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="b672b-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="b672b-133">Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="b672b-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="b672b-134">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="b672b-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
