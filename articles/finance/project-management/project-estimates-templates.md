---
title: Projekta novērtējumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Dynamics 365 Project Service Automation ietvertos projekta stundu novērtējumus un projekta izdevumu prognozes ar programmu Microsoft Dynamics 365 Finance.
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
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250488"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="4dcbb-103">Projekta novērtējumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4dcbb-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4dcbb-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai tiešā veidā sinhronizētu programmā Dynamics 365 Project Service Automation ietvertos projekta stundu novērtējumus un projekta izdevumu prognozes ar programmu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="4dcbb-105">Versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="4dcbb-106">Faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="4dcbb-107">Project Service Automation datu plūsma uz programmu Finance</span><span class="sxs-lookup"><span data-stu-id="4dcbb-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="4dcbb-108">Risinājums, lai veiktu integrēšanu no programmas Project Service Automation uz programmu Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="4dcbb-109">Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta stundu novērtējumiem un projekta izdevumu novērtējumiem no programmas Project Service Automation uz programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4dcbb-110">Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="4dcbb-111">[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4dcbb-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="4dcbb-112">Projekta stundu novērtējumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="4dcbb-113">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-113">Template and tasks</span></span>

<span data-ttu-id="4dcbb-114">Lai piekļūtu pieejamajām veidnēm, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-114">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4dcbb-115">Programmā Project Service Automation ietverto projekta stundu novērtējumu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="4dcbb-116">**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta stundu novērtējumi (no PSA uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4dcbb-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="4dcbb-117">**Projekta uzdevumu nosaukums:**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="4dcbb-118">Transakciju attiecības</span><span class="sxs-lookup"><span data-stu-id="4dcbb-118">Transaction relationships</span></span>
    - <span data-ttu-id="4dcbb-119">Izdevumu novērtējumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="4dcbb-120">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="4dcbb-120">Entity set</span></span>

| <span data-ttu-id="4dcbb-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4dcbb-121">Project Service Automation</span></span> | <span data-ttu-id="4dcbb-122">Finansēt</span><span class="sxs-lookup"><span data-stu-id="4dcbb-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="4dcbb-123">Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-123">Project tasks</span></span>              | <span data-ttu-id="4dcbb-124">Integrēšanas elements projekta stundu novērtējumiem</span><span class="sxs-lookup"><span data-stu-id="4dcbb-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="4dcbb-125">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="4dcbb-125">Entity flow</span></span>

<span data-ttu-id="4dcbb-126">Projekta stundu novērtējumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta stundu prognozes.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4dcbb-127">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-127">Prerequisites</span></span>

<span data-ttu-id="4dcbb-128">Pirms projekta stundu novērtējumu sinhronizēšanas ir jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="4dcbb-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="4dcbb-129">Power Query</span></span>

<span data-ttu-id="4dcbb-130">Projekta stundu novērtējumu veidnē jums ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel, lai izpildītu tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="4dcbb-131">Iestatīt noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija izveido jaunus stundu novērtējumus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="4dcbb-132">Izfiltrēt uzdevumā visus resursiem raksturīgos ierakstus, kuriem nevarēs veikt integrēšanu stundu novērtējumos.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="4dcbb-133">Filtrēt visas tukšo transakcijas kategoriju rindas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="4dcbb-134">Ja šis uzdevums netiek izpildīts, stundu prognozes var būt nepareizas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="4dcbb-135">Noklusējuma prognozes modeļa ID iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4dcbb-135">Set the default forecast model ID</span></span>

<span data-ttu-id="4dcbb-136">Lai atjauninātu noklusējuma budžeta modeļa ID veidnē, noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="4dcbb-137">Pēc tam atlasiet saiti **Paplašinātais vaicājums un filtrēšana**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="4dcbb-138">Ja izmantojat noklusējuma veidni “Projekta stundu novērtējumi” (no PSA uz Fin and Ops), atlasiet vienumu **Ievietotais nosacījums** sarakstā **Izmantotās darbības**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="4dcbb-139">Ierakstā **Funkcija** uzrakstu **O\_forecast** aizstājiet ar prognozes modeļa ID nosaukumu, kas ir jāizmanto integrācijai.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="4dcbb-140">Noklusējuma veidnei ir budžeta modeļa ID no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="4dcbb-141">Ja veidojat jaunu veidni, ir jāpievieno šī kolonna.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="4dcbb-142">Pievienojumprogrammā Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet nosaukumu jaunajai kolonnai, piemēram, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="4dcbb-143">Ievadiet nosacījumu šai kolonnai, kurš paredz, ka gadījumā, ja vērtība “Projekta uzdevums” nav Null, tad \<ievadīt prognozes modeļa ID\>; pretējā gadījumā vērtība ir Null.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="4dcbb-144">Resursam raksturīgo ierakstu izfiltrēšana</span><span class="sxs-lookup"><span data-stu-id="4dcbb-144">Filter out resource-specific records</span></span>

<span data-ttu-id="4dcbb-145">Veidnei “Projekta stundu novērtējumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas noņem visus resursam raksturīgos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="4dcbb-146">Ja izveidojat savu veidni, ir jāpievieno šis filtrs.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="4dcbb-147">Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**, lai filtrētu pēc kolonnas **msdyn\_islinetask**, tādējādi ietverot tikai ierakstus **False** (Aplams).</span><span class="sxs-lookup"><span data-stu-id="4dcbb-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="4dcbb-148">Tukšo transakcijas kategoriju rindu filtrēšana</span><span class="sxs-lookup"><span data-stu-id="4dcbb-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="4dcbb-149">Ir jāpievieno filtrs, lai noņemtu visas rindas, kurās ir tukšas transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="4dcbb-150">Šis uzdevums ir jāveic neatkarīgi no tā, vai izmantojat noklusējuma veidni, vai izveidojat pats savu veidni.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="4dcbb-151">Šis filtrs no Project Service Automation noņem visas kopsavilkuma rindas, kuras varētu izraisīt to, ka stundu prognozes programmā Finance ir nepareizas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="4dcbb-152">Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**, lai izfiltrētu Null ierakstus kolonnā **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4dcbb-153">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="4dcbb-153">Template mapping in Data integration</span></span>

<span data-ttu-id="4dcbb-154">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="4dcbb-155">Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4dcbb-156">[![Veidnes kartēšana](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4dcbb-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="4dcbb-157">Projekta izdevumu novērtējumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="4dcbb-158">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-158">Template and tasks</span></span>

<span data-ttu-id="4dcbb-159">Programmā Project Service Automation ietverto projekta izdevumu novērtējumu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="4dcbb-160">**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu novērtējumi (no PSA uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4dcbb-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="4dcbb-161">**Projekta uzdevumu nosaukums:**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="4dcbb-162">Transakciju attiecības</span><span class="sxs-lookup"><span data-stu-id="4dcbb-162">Transaction relationships</span></span> 
    - <span data-ttu-id="4dcbb-163">Izdevumu novērtējumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="4dcbb-164">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="4dcbb-164">Entity set</span></span>

| <span data-ttu-id="4dcbb-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4dcbb-165">Project Service Automation</span></span> | <span data-ttu-id="4dcbb-166">Finansēt</span><span class="sxs-lookup"><span data-stu-id="4dcbb-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="4dcbb-167">Transakciju savienojumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-167">Transaction Connections</span></span>    | <span data-ttu-id="4dcbb-168">Integrēšanas elements projekta transakciju attiecībām</span><span class="sxs-lookup"><span data-stu-id="4dcbb-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="4dcbb-169">Novērtēšanas rindas</span><span class="sxs-lookup"><span data-stu-id="4dcbb-169">Estimate Lines</span></span>             | <span data-ttu-id="4dcbb-170">Integrēšanas elements projekta izdevumu prognozēm</span><span class="sxs-lookup"><span data-stu-id="4dcbb-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="4dcbb-171">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="4dcbb-171">Entity flow</span></span>

<span data-ttu-id="4dcbb-172">Projekta izdevumu novērtējumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta izdevumu prognozes.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4dcbb-173">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4dcbb-173">Prerequisites</span></span>

<span data-ttu-id="4dcbb-174">Pirms projekta izdevumu novērtējumu sinhronizēšanas ir jāsinhronizē projektu, projekta uzdevumu un projekta izdevumu transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="4dcbb-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="4dcbb-175">Power Query</span></span>

<span data-ttu-id="4dcbb-176">Projekta izdevumu novērtējumu veidnē ir jāizmanto Power Query, lai izpildītu tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="4dcbb-177">Filtrēt, lai ietvertu tikai izdevumu novērtējumu rindu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="4dcbb-178">Iestatīt noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija izveido jaunus stundu novērtējumus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="4dcbb-179">Pārveidot norēķinu veidus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-179">Transform the billing types.</span></span>
- <span data-ttu-id="4dcbb-180">Pārveidot transakciju veidus.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="4dcbb-181">Filtrēšana, lai iekļautu tikai izdevumu novērtējumu rindas</span><span class="sxs-lookup"><span data-stu-id="4dcbb-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="4dcbb-182">Veidnē “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kurš integrācijā ietver tikai izdevumu rindas.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="4dcbb-183">Ja izveidojat savu veidni, ir jāpievieno šis filtrs.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="4dcbb-184">Atlasiet uzdevumu **Transakciju attiecības** un pēc tam noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="4dcbb-185">Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="4dcbb-186">Filtrējiet kolonnu **msdyn\_transactiontype1**, lai tajā būtu tikai **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="4dcbb-187">Noklusējuma prognozes modeļa ID iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4dcbb-187">Set the default forecast model ID</span></span>

<span data-ttu-id="4dcbb-188">Lai veidnē atjauninātu noklusējuma prognozes modeļa ID, atlasiet uzdevumu **Izdevumu novērtējumi** un pēc tam noklikšķiniet uz bultiņas **Kartēt**, lai atvērtu kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="4dcbb-189">Atlasiet saiti **Paplašinātais vaicājums un filtrēšana**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="4dcbb-190">Ja izmantojat noklusējuma veidni “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops), pievienojumprogrammā Power Query atlasiet pirmo vienumu **Ievietotais nosacījums** no sadaļas **Izmantotās darbības**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="4dcbb-191">Ierakstā **Funkcija** uzrakstu **O\_forecast** aizstājiet ar prognozes modeļa ID nosaukumu, kas ir jāizmanto integrācijai.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="4dcbb-192">Noklusējuma veidnei ir budžeta modeļa ID no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="4dcbb-193">Ja veidojat jaunu veidni, ir jāpievieno šī kolonna.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="4dcbb-194">Pievienojumprogrammā Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet nosaukumu jaunajai kolonnai, piemēram, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="4dcbb-195">Ievadiet nosacījumu šai kolonnai, kurš paredz, ka gadījumā, ja Novērtējuma rindas ID vērtība nav Null, tad \<ievadīt prognozes modeļa ID\>; pretējā gadījumā vērtība ir Null.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="4dcbb-196">Norēķinu veidu pārveidošana</span><span class="sxs-lookup"><span data-stu-id="4dcbb-196">Transform the billing types</span></span>

<span data-ttu-id="4dcbb-197">Veidnē “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops) ir nosacījuma kolonna, kas tiek izmantota, lai pārveidotu norēķinu tipus, kuri integrācijas laikā ir saņemti no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="4dcbb-198">Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="4dcbb-199">Atlasiet saiti **Paplašinātais vaicājums un filtrēšana** un pēc tam atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="4dcbb-200">Ievadiet jaunās kolonnas nosaukumu, piemēram, **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="4dcbb-201">Pēc tam ievadiet tālāk norādīto nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-201">Then enter the following condition:</span></span>

<span data-ttu-id="4dcbb-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="4dcbb-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="4dcbb-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="4dcbb-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="4dcbb-206">Transakciju veidu pārveidošana</span><span class="sxs-lookup"><span data-stu-id="4dcbb-206">Transform the transaction types</span></span>

<span data-ttu-id="4dcbb-207">Veidnē “Projekta izdevumu novērtējumi” (no PSA uz Fin and Ops) ir nosacījuma kolonna, kas tiek izmantota, lai pārveidotu transakciju tipus, kuri integrācijas laikā ir saņemti no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="4dcbb-208">Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="4dcbb-209">Atlasiet saiti **Paplašinātais vaicājums un filtrēšana** un pēc tam atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="4dcbb-210">Ievadiet nosaukumu jaunajai kolonnai, piemēram, **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="4dcbb-211">Pēc tam ievadiet tālāk norādīto nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-211">Then enter the following condition:</span></span>

<span data-ttu-id="4dcbb-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="4dcbb-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="4dcbb-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="4dcbb-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4dcbb-215">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="4dcbb-215">Template mapping in Data integration</span></span>

<span data-ttu-id="4dcbb-216">Tālāk esošajos attēlos ir redzami piemēri veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="4dcbb-217">Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.</span><span class="sxs-lookup"><span data-stu-id="4dcbb-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4dcbb-218">[![Veidnes kartēšana](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4dcbb-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="4dcbb-219">[![Veidnes kartēšana](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4dcbb-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
