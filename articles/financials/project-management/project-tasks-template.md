---
title: "Projekta uzdevumu sinhronizēšana no programmas Project Service Automation"
description: "Šajā tēmā ir aprakstīta veidne un pamata uzdevums, kas tiek izmantots programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="4c267-103">Programmā Project Service Automation ietverto projekta uzdevumu tieša sinhronizēšana ar projekta aktivitātēm programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4c267-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="4c267-104">Šajā tēmā ir aprakstīta veidne un pamata uzdevums, kas tiek izmantots programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c267-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4c267-105">Projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.0.</span><span class="sxs-lookup"><span data-stu-id="4c267-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="4c267-106">Datu plūsma programmas Project Service Automation sinhronizēšanai ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4c267-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="4c267-107">Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs.</span><span class="sxs-lookup"><span data-stu-id="4c267-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="4c267-108">Integrācijas veidne, kas ir pieejama līdzeklī Datu integrācija, iespējo datu plūsmu par projekta uzdevumiem no programmas Project Service Automation uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c267-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4c267-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c267-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="4c267-110">[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4c267-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4c267-111">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="4c267-111">Template and task</span></span>

<span data-ttu-id="4c267-112">Lai piekļūtu veidnei, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="4c267-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4c267-113">Programmā Project Service Automation ietverto projekta uzdevumu sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevums.</span><span class="sxs-lookup"><span data-stu-id="4c267-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="4c267-114">-**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta uzdevumi (no PSA uz Fin and Ops) -**Projekta uzdevuma nosaukums:** Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4c267-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="4c267-115">Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.</span><span class="sxs-lookup"><span data-stu-id="4c267-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="4c267-116">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="4c267-116">Entity set</span></span>

|<span data-ttu-id="4c267-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4c267-117">Project Service Automation</span></span>               | <span data-ttu-id="4c267-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4c267-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="4c267-119">Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4c267-119">Project Tasks</span></span>                           | <span data-ttu-id="4c267-120">Integrācijas elements projekta uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="4c267-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="4c267-121">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="4c267-121">Entity flow</span></span>

<span data-ttu-id="4c267-122">Projekta uzdevumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekta aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="4c267-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4c267-123">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="4c267-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="4c267-124">Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.</span><span class="sxs-lookup"><span data-stu-id="4c267-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="4c267-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="4c267-125">Power Query</span></span>

<span data-ttu-id="4c267-126">Ir jāizmanto Microsoft Power Query, lai filtrētu datus, ja ir izpildīti šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="4c267-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="4c267-127">Projekta uzdevumā ir resursu ieraksti.</span><span class="sxs-lookup"><span data-stu-id="4c267-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="4c267-128">Ja ir jāizmanto Power Query, ievērojiet tālāk minētos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="4c267-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="4c267-129">Veidnē Projekta uzdevumi (no PSA uz Fin and Ops) ir noklusējuma filtrs, lai izslēgtu resursu ierakstus no projekta uzdevuma, iestatot vienumam **IsLineTask** filtru **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="4c267-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="4c267-130">Ja izveidojat savu veidni, ir jāpievieno šis filtrs.</span><span class="sxs-lookup"><span data-stu-id="4c267-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4c267-131">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="4c267-131">Template mapping in Data integration</span></span>

<span data-ttu-id="4c267-132">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartējumiem līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="4c267-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="4c267-133">Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c267-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4c267-134">[![Veidnes kartēšana](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="4c267-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


