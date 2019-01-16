---
title: "Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e12c8-103">Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service</span><span class="sxs-lookup"><span data-stu-id="e12c8-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e12c8-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e12c8-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e12c8-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="e12c8-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e12c8-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="e12c8-106">Templates and tasks</span></span>
<span data-ttu-id="e12c8-107">Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu projektu sinhronizēšanu programmā Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e12c8-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e12c8-108">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="e12c8-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e12c8-109">Projekti (no programmas Finance and Operations programmā Field Service)</span><span class="sxs-lookup"><span data-stu-id="e12c8-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="e12c8-110">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="e12c8-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e12c8-111">Projekti</span><span class="sxs-lookup"><span data-stu-id="e12c8-111">Projects</span></span>

<span data-ttu-id="e12c8-112">Lai varētu veikt projektu saraksta sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="e12c8-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="e12c8-113">Konti (no programmas Sales programmā Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e12c8-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e12c8-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="e12c8-114">Entity set</span></span>
<span data-ttu-id="e12c8-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e12c8-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="e12c8-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e12c8-116">Field Service</span></span>           | <span data-ttu-id="e12c8-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e12c8-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="e12c8-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="e12c8-118">msdynce_externalprojects</span></span> | <span data-ttu-id="e12c8-119">Projekti</span><span class="sxs-lookup"><span data-stu-id="e12c8-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="e12c8-120">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="e12c8-120">Entity flow</span></span>
<span data-ttu-id="e12c8-121">Projekti tiek izveidoti programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e12c8-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="e12c8-122">Projekti, kuriem vienumam **Projekta tips** atlasīts iestatījums Laiks un materiāli un vienumam **Projekta posms** atlasīts iestatījums Apstrāde, tiks sinhronizēti uz entītiju **Ārējais projekts** programmā Field Service, ieskaitot šādu informāciju: Projekta numurs, Projekta nosaukums, Projekta posms un Debitora konts.</span><span class="sxs-lookup"><span data-stu-id="e12c8-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="e12c8-123">Entītijas **Ārējais projekts** saraksts tiek izmantots, lai savienotu pārī Field Service darba pasūtījumus ar Finance and Operations projektiem.</span><span class="sxs-lookup"><span data-stu-id="e12c8-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="e12c8-124">Risinājums Field Service CRM Entītija Ārējais projekts ir jauna entītija, kas iegūst visus projektus no programmas Operations.</span><span class="sxs-lookup"><span data-stu-id="e12c8-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="e12c8-125">Entītijai Darba pasūtījums ir pievienots lauks Ārējais projekts.</span><span class="sxs-lookup"><span data-stu-id="e12c8-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="e12c8-126">Šis lauks ir uzmeklēšanas lauks, un, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Operations.</span><span class="sxs-lookup"><span data-stu-id="e12c8-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="e12c8-127">Kad sistēmas statuss no Atvērts - Notiek izpilde(690,970,000) tiek mainīts uz augstāku statusu, lauks Ārējais projekts tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="e12c8-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e12c8-128">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="e12c8-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="e12c8-129">Programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e12c8-129">In Finance and Operations</span></span>
<span data-ttu-id="e12c8-130">Iespējot izmaiņu izsekošanu datu elementu projektiem</span><span class="sxs-lookup"><span data-stu-id="e12c8-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e12c8-131">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="e12c8-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="e12c8-132">Projekti (no programmas Finance and Operations programmā Field Service): Projekti</span><span class="sxs-lookup"><span data-stu-id="e12c8-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="e12c8-133">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="e12c8-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

