---
title: Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmatūrā Supply Chain Management
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 03/12/2019
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
ms.openlocfilehash: d733bf3256fa1f6c572bd0aa35c228490d409bbc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836498"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="b11c9-103">Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmatūrā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b11c9-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b11c9-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b11c9-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b11c9-105">[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="b11c9-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="b11c9-106">Izmantotā veidne **Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management)** ir izveidota, pamatojoties uz veidni **Darba pasūtījumu (no Field Service uz Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="b11c9-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="b11c9-107">Papildinformāciju skatiet rakstā [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmatūrā Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="b11c9-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="b11c9-108">Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības.</span><span class="sxs-lookup"><span data-stu-id="b11c9-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="b11c9-109">**Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="b11c9-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="b11c9-110">**Darba pasūtījumi (no Field Service uz Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="b11c9-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="b11c9-111">Galvenā atšķirība ir tā, ka šajā veidnē ir ietverta programmā Field Service darba pasūtījumam piešķirtā projekta numura kartēšana, nodrošinot, ka pārdošanas pasūtījums, kas izveidots programmatūrā Supply Chain Management, ietver projekta numuru un ka saistītajam projektam var veikt rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="b11c9-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="b11c9-112">Papildus tam veidne izmanto funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="b11c9-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b11c9-113">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="b11c9-113">Templates and tasks</span></span>

<span data-ttu-id="b11c9-114">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="b11c9-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="b11c9-115">Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="b11c9-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="b11c9-116">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="b11c9-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="b11c9-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="b11c9-117">WorkOrderHeader</span></span>
- <span data-ttu-id="b11c9-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="b11c9-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="b11c9-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="b11c9-119">WorkOrderProduct</span></span>
- <span data-ttu-id="b11c9-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="b11c9-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b11c9-121">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="b11c9-121">Field Service CRM solution</span></span>
<span data-ttu-id="b11c9-122">Entītijai Darba pasūtījums ir pievienots lauks **Ārējais projekts**.</span><span class="sxs-lookup"><span data-stu-id="b11c9-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="b11c9-123">Šis lauks ir uzmeklēšana, un marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums pēc tam tiks savienots ar projektu programmatūrā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b11c9-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="b11c9-124">Kad vienumam **Sistēmas statuss** iestatījums Atvērts - Notiek izpilde(690 970 000) tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="b11c9-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b11c9-125">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="b11c9-125">Template mapping in Data integration</span></span>

<span data-ttu-id="b11c9-126">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="b11c9-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="b11c9-127">Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="b11c9-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="b11c9-128">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="b11c9-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="b11c9-129">Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="b11c9-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="b11c9-130">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="b11c9-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="b11c9-131">Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="b11c9-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="b11c9-132">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="b11c9-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="b11c9-133">Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="b11c9-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="b11c9-134">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="b11c9-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]