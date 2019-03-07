---
title: Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "329854"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="693b7-103">Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="693b7-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="693b7-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="693b7-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="693b7-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="693b7-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="693b7-106">Izmantotā veidne **Field Service preces (no Finance and Operations uz Field Service)** balstās uz veidni **Preces (no Finance and Operations uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="693b7-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="693b7-107">Papildinformāciju skatiet sadaļā [Preces (no Finance and Operations uz Sales) — tieši](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="693b7-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="693b7-108">Šajā tēmā ir aprakstītas tikai atšķirības starp veidnēm **Field Service preces (no Finance and Operations uz Field Service)** un **Field Service preces (no Finance and Operations uz Field Service) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="693b7-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="693b7-109">Galvenā atšķirība ir tā, ka šajā veidnē ir ietverta programmā Field Service darba pasūtījumam piešķirtā projekta numura kartēšana, nodrošinot, ka pārdošanas pasūtījums, kas izveidots programmā Finance and Operations, ietver projekta numuru un ka saistītajam projektam var veikt rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="693b7-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="693b7-110">Papildus tam veidne izmanto funkcionalitāti Izvērsts vaicājums un filtrēšana.</span><span class="sxs-lookup"><span data-stu-id="693b7-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="693b7-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="693b7-111">Templates and tasks</span></span>

<span data-ttu-id="693b7-112">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="693b7-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="693b7-113">Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="693b7-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="693b7-114">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="693b7-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="693b7-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="693b7-115">WorkOrderHeader</span></span>
- <span data-ttu-id="693b7-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="693b7-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="693b7-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="693b7-117">WorkOrderProduct</span></span>
- <span data-ttu-id="693b7-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="693b7-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="693b7-119">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="693b7-119">Field Service CRM solution</span></span>
<span data-ttu-id="693b7-120">Entītijai Darba pasūtījums ir pievienots lauks **Ārējais projekts**.</span><span class="sxs-lookup"><span data-stu-id="693b7-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="693b7-121">Šis lauks ir uzmeklēšanas lauks, un, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="693b7-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="693b7-122">Kad vienumam **Sistēmas statuss** iestatījums Atvērts - Notiek izpilde(690,970,000) tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="693b7-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="693b7-123">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="693b7-123">Template mapping in Data integration</span></span>

<span data-ttu-id="693b7-124">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="693b7-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="693b7-125">Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="693b7-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="693b7-126">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="693b7-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="693b7-127">Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="693b7-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="693b7-128">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="693b7-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="693b7-129">Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="693b7-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="693b7-130">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="693b7-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="693b7-131">Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="693b7-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="693b7-132">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="693b7-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
