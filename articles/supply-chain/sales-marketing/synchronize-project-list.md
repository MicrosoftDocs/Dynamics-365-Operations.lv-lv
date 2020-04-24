---
title: Programmatūrā Supply Chain Management ietvertā projektu saraksta sinhronizēšana ar Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto projektu sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215934"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="caccc-103">Programmatūrā Supply Chain Management ietvertā projektu saraksta sinhronizēšana ar Field Service</span><span class="sxs-lookup"><span data-stu-id="caccc-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="caccc-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto projektu sinhronizēšanai ar programmu Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="caccc-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="caccc-105">[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="caccc-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="caccc-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="caccc-106">Templates and tasks</span></span>
<span data-ttu-id="caccc-107">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai palaistu projektu sinhronizāciju no programmatūras Supply Chain Management uz Field Service.</span><span class="sxs-lookup"><span data-stu-id="caccc-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="caccc-108">**Veidne līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="caccc-108">**Template in Data integration**</span></span>
- <span data-ttu-id="caccc-109">Projekti (no Supply Chain Management uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="caccc-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="caccc-110">**Uzdevums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="caccc-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="caccc-111">Projekti</span><span class="sxs-lookup"><span data-stu-id="caccc-111">Projects</span></span>

<span data-ttu-id="caccc-112">Lai varētu veikt projektu saraksta sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="caccc-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="caccc-113">Konti (no Sales uz Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="caccc-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="caccc-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="caccc-114">Entity set</span></span>
| <span data-ttu-id="caccc-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="caccc-115">Field Service</span></span>           | <span data-ttu-id="caccc-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="caccc-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="caccc-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="caccc-117">msdynce_externalprojects</span></span> | <span data-ttu-id="caccc-118">Projekti</span><span class="sxs-lookup"><span data-stu-id="caccc-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="caccc-119">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="caccc-119">Entity flow</span></span>
<span data-ttu-id="caccc-120">Projekti tiek veidoti programmatūrā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="caccc-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="caccc-121">Projekti, kuriem vienumam **Projekta tips** atlasīts iestatījums **Laiks un materiāli** un vienumam **Projekta posms** atlasīts iestatījums **Apstrāde**, tiks sinhronizēti uz entītiju **Ārējais projekts** programmā Field Service, ieskaitot šādu informāciju: Projekta numurs, Projekta nosaukums, Projekta posms un Debitora konts.</span><span class="sxs-lookup"><span data-stu-id="caccc-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="caccc-122">Entītijas **Ārējais projekts** saraksts tiek izmantots, lai savienotu pārī Field Service darba pasūtījumus ar Supply Chain Management projektiem.</span><span class="sxs-lookup"><span data-stu-id="caccc-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="caccc-123">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="caccc-123">Field Service CRM solution</span></span>
<span data-ttu-id="caccc-124">Entītija **Ārējais projekts** iegūst visus projektus no Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="caccc-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="caccc-125">Entītijai **Darba pasūtījums** ir pievienots lauks **Ārējais projekts**.</span><span class="sxs-lookup"><span data-stu-id="caccc-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="caccc-126">Tas ir uzmeklēšanas lauks, tādēļ, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmatūrā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="caccc-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="caccc-127">Pēc tam, kad vienumam **Sistēmas statuss** iestatījums **Atvērts - Notiek izpilde(690,970,000)** tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un vairs nebūs iespējams pievienot, noņemt vai mainīt vērtību.</span><span class="sxs-lookup"><span data-stu-id="caccc-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="caccc-128">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="caccc-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="caccc-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="caccc-129">Supply Chain Management</span></span>
<span data-ttu-id="caccc-130">Iespējojiet izmaiņu izsekošanu datu elementu projektiem.</span><span class="sxs-lookup"><span data-stu-id="caccc-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="caccc-131">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="caccc-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="caccc-132">Projekti (no Supply Chain Management uz Field Service): Projekti</span><span class="sxs-lookup"><span data-stu-id="caccc-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="caccc-133">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="caccc-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
