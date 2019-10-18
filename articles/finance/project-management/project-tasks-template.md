---
title: Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir apskatīta veidne un pamata uzdevums, kas tiek izmantoti programmā Microsoft  Dynamics 365 Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 977037f0e2b313ebf05a3e1616d34567f82e82d7
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250396"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="902ac-103">Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="902ac-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="902ac-104">Šajā tēmā ir apskatīta veidne un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="902ac-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="902ac-105">Versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.</span><span class="sxs-lookup"><span data-stu-id="902ac-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="902ac-106">Ja lietojat Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="902ac-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="902ac-107">Ja ir nepieciešams atiestatīt uzskaites sadali, mēs ieteicām instalēt arī KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="902ac-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="902ac-108">Faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="902ac-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="902ac-109">Project Service Automation datu plūsma uz programmu Finance</span><span class="sxs-lookup"><span data-stu-id="902ac-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="902ac-110">Risinājums, lai veiktu integrēšanu no programmas Project Service Automation uz programmu Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs.</span><span class="sxs-lookup"><span data-stu-id="902ac-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="902ac-111">Integrācijas veidne, kas ir pieejama līdzeklī Datu integrācija, iespējo datu plūsmu par projekta uzdevumiem no programmas Project Service Automation uz programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="902ac-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="902ac-112">Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="902ac-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="902ac-113">[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="902ac-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="902ac-114">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="902ac-114">Template and task</span></span>

<span data-ttu-id="902ac-115">Lai piekļūtu veidnei, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="902ac-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="902ac-116">Programmā Project Service Automation ietverto uzdevumu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevums.</span><span class="sxs-lookup"><span data-stu-id="902ac-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="902ac-117">**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta uzdevumi (no PSA uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="902ac-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="902ac-118">**Uzdevuma nosaukums projektā:** Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="902ac-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="902ac-119">Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.</span><span class="sxs-lookup"><span data-stu-id="902ac-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="902ac-120">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="902ac-120">Entity set</span></span>

| <span data-ttu-id="902ac-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="902ac-121">Project Service Automation</span></span> | <span data-ttu-id="902ac-122">Finansēt</span><span class="sxs-lookup"><span data-stu-id="902ac-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="902ac-123">Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="902ac-123">Project Tasks</span></span>              | <span data-ttu-id="902ac-124">Integrācijas elements projekta uzdevumam</span><span class="sxs-lookup"><span data-stu-id="902ac-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="902ac-125">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="902ac-125">Entity flow</span></span>

<span data-ttu-id="902ac-126">Projekta uzdevumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="902ac-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="902ac-127">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="902ac-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="902ac-128">Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.</span><span class="sxs-lookup"><span data-stu-id="902ac-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="902ac-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="902ac-129">Power Query</span></span>

<span data-ttu-id="902ac-130">Ja ir izpildīts tālāk norādītais nosacījums, datu filtrēšanai ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel.</span><span class="sxs-lookup"><span data-stu-id="902ac-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="902ac-131">Projekta uzdevumā jums ir resursam raksturīgi ieraksti.</span><span class="sxs-lookup"><span data-stu-id="902ac-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="902ac-132">Ja ir jāizmanto Power Query, ievērojiet tālāk minēto norādījumu.</span><span class="sxs-lookup"><span data-stu-id="902ac-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="902ac-133">Veidnē “Projekta uzdevumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas no projekta uzdevuma izslēdz resursam raksturīgus ierakstus, vienumam **IsLineTask** filtru iestatot uz **False** (Aplams).</span><span class="sxs-lookup"><span data-stu-id="902ac-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="902ac-134">Ja izveidojat savu veidni, ir jāpievieno šis filtrs.</span><span class="sxs-lookup"><span data-stu-id="902ac-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="902ac-135">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="902ac-135">Template mapping in Data integration</span></span>

<span data-ttu-id="902ac-136">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartējumiem līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="902ac-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="902ac-137">Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="902ac-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="902ac-138">[![Veidnes kartēšana](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="902ac-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
