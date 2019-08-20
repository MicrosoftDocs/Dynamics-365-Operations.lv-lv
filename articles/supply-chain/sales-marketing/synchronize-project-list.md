---
title: Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843557"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c56a0-103">Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service</span><span class="sxs-lookup"><span data-stu-id="c56a0-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c56a0-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c56a0-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c56a0-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="c56a0-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c56a0-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="c56a0-106">Templates and tasks</span></span>
<span data-ttu-id="c56a0-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanu ar Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c56a0-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c56a0-108">**Veidne līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="c56a0-108">**Template in Data integration**</span></span>
- <span data-ttu-id="c56a0-109">Projekti (no Fin and Ops uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="c56a0-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="c56a0-110">**Uzdevums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="c56a0-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="c56a0-111">Projekti</span><span class="sxs-lookup"><span data-stu-id="c56a0-111">Projects</span></span>

<span data-ttu-id="c56a0-112">Lai varētu veikt projektu saraksta sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="c56a0-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="c56a0-113">Konti (no Sales uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c56a0-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c56a0-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="c56a0-114">Entity set</span></span>
| <span data-ttu-id="c56a0-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c56a0-115">Field Service</span></span>           | <span data-ttu-id="c56a0-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c56a0-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="c56a0-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="c56a0-117">msdynce_externalprojects</span></span> | <span data-ttu-id="c56a0-118">Projekti</span><span class="sxs-lookup"><span data-stu-id="c56a0-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="c56a0-119">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="c56a0-119">Entity flow</span></span>
<span data-ttu-id="c56a0-120">Projekti tiek izveidoti programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c56a0-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="c56a0-121">Projekti, kuriem vienumam **Projekta tips** atlasīts iestatījums **Laiks un materiāli** un vienumam **Projekta posms** atlasīts iestatījums **Apstrāde**, tiks sinhronizēti uz entītiju **Ārējais projekts** programmā Field Service, ieskaitot šādu informāciju: Projekta numurs, Projekta nosaukums, Projekta posms un Debitora konts.</span><span class="sxs-lookup"><span data-stu-id="c56a0-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="c56a0-122">Entītijas **Ārējais projekts** saraksts tiek izmantots, lai savienotu pārī Field Service darba pasūtījumus ar Finance and Operations projektiem.</span><span class="sxs-lookup"><span data-stu-id="c56a0-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c56a0-123">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="c56a0-123">Field Service CRM solution</span></span>
<span data-ttu-id="c56a0-124">Entītija **Ārējais projekts** iegūst visus projektus no Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c56a0-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="c56a0-125">Entītijai **Darba pasūtījums** ir pievienots lauks **Ārējais projekts**.</span><span class="sxs-lookup"><span data-stu-id="c56a0-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="c56a0-126">Tas ir uzmeklēšanas lauks, tādēļ, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c56a0-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="c56a0-127">Pēc tam, kad vienumam **Sistēmas statuss** iestatījums **Atvērts - Notiek izpilde(690,970,000)** tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un vairs nebūs iespējams pievienot, noņemt vai mainīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="c56a0-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c56a0-128">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="c56a0-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="c56a0-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c56a0-129">Finance and Operations</span></span>
<span data-ttu-id="c56a0-130">Iespējojiet izmaiņu izsekošanu datu elementu projektiem.</span><span class="sxs-lookup"><span data-stu-id="c56a0-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c56a0-131">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="c56a0-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="c56a0-132">Projekti (no Fin and Ops uz Field Service): Projekti</span><span class="sxs-lookup"><span data-stu-id="c56a0-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="c56a0-133">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="c56a0-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
