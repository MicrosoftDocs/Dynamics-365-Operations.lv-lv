---
title: Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu programmā Microsoft Dynamics 365 for Finance and Operations ietvertās projekta izdevumu kategorijas ar programmu Microsoft Dynamics 365 for Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838371"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="ad31f-103">Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ad31f-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ad31f-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu programmā Microsoft Dynamics 365 for Finance and Operations ietvertās projekta izdevumu kategorijas ar programmu Microsoft Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ad31f-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="ad31f-105">Microsoft Dynamics 365 for Finance and Operations versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.</span><span class="sxs-lookup"><span data-stu-id="ad31f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="ad31f-106">Faktisko vērtību integrācija ir pieejama Microsoft Dynamics 365 for Finance and Operations versijā 8.0.1 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="ad31f-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="ad31f-107">Ja lietojat Microsoft Dynamics 365 for Finance and Operations Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="ad31f-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="ad31f-108">Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="ad31f-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="ad31f-109">Datu plūsma programmai Project Service Automation un programmai Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ad31f-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="ad31f-110">Risinājums, lai veiktu integrēšanu starp programmām Project Service Automation un Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs.</span><span class="sxs-lookup"><span data-stu-id="ad31f-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="ad31f-111">Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo projekta izdevumu transakciju kategoriju datu plūsmu starp programmu Finance and Operations un programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ad31f-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="ad31f-112">Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, integrācijas plūsma vispirms tiek nosūtīta no programmas Finance and Operations uz programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ad31f-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="ad31f-113">Pēc tam projekta izdevumu kategoriju integrācijas ID tiek atjaunināti, veicot sinhronizāciju no programmas Project Service Automation uz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ad31f-114">Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Project Service Automation, integrācijas plūsma vispirms tiek nosūtīta no programmas Project Service Automation uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="ad31f-115">Projekta kategorijām jau ir jābūt konfigurētām programmā Finance and Operations pirms sinhronizācijas no programmas Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ad31f-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="ad31f-116">Pēc tam sinhronizējiet no programmas Finance and Operations atpakaļ uz programmu Project Service Automation un pēc tam vēlreiz no programmas Project Service Automation uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="ad31f-117">Šādā veidā varat nodrošināt, ka tiek saistītas kategorijas un netiek izveidoti dublikāti.</span><span class="sxs-lookup"><span data-stu-id="ad31f-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="ad31f-118">Parasti projekta izdevumu kategoriju pārvaldība tiek veikta programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="ad31f-119">Taču, ja izdevumu kategorijas netiek pārvaldītas programmā Finance and Operations vai tās jau ir izveidotas programmā Project Service Automation, vispirms veiciet sinhronizāciju, izmantojot veidni Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="ad31f-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="ad31f-120">Pēc tam veiciet sinhronizāciju, izmantojot veidni Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA).</span><span class="sxs-lookup"><span data-stu-id="ad31f-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="ad31f-121">Pēc tam vēl vienu reizi ir jāpalaiž sinhronizācija no Project Service Automation uz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="ad31f-122">Ja vispirms sinhronizējat no programmas Project Service Automation, pirms sinhronizēšanas palaišanas programmā Finance and Operations ir jābūt ievērotām tālāk norādītajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="ad31f-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="ad31f-123">Ir jābūt koplietojamai kategorijai, kas atbilst programmā Project Service Automation iestatītajai projekta kategorijai, un tai ir jābūt iespējotai gan vienumam **Projekts**, gan vienumam **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="ad31f-124">Katrai Finance and Operations juridiskajai personai, ar kuru ir jābūt veiktai integrācijai, ir jābūt tālāk norādītajām projekta kategorijām.</span><span class="sxs-lookup"><span data-stu-id="ad31f-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="ad31f-125">Pastāv **Projekta kategorija**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="ad31f-126">Ir iespējots vienums **Lietot izdevumos**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="ad31f-127">Ir iespējots vienums **Aktīvs žurnālā**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="ad31f-128">**Transakcijas veids** ir iestatīts uz **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="ad31f-129">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="ad31f-130">[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ad31f-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="ad31f-131">Projekta izdevumu kategoriju sinhronizēšana no programmas Finance and Operations uz Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ad31f-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ad31f-132">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="ad31f-132">Template and task</span></span>

<span data-ttu-id="ad31f-133">Lai piekļūtu veidnei, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="ad31f-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ad31f-134">Programmā Finance and Operations ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevums.</span><span class="sxs-lookup"><span data-stu-id="ad31f-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="ad31f-135">**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA)</span><span class="sxs-lookup"><span data-stu-id="ad31f-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="ad31f-136">**Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz PSA</span><span class="sxs-lookup"><span data-stu-id="ad31f-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="ad31f-137">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="ad31f-137">Entity set</span></span>

| <span data-ttu-id="ad31f-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ad31f-138">Finance and Operations</span></span>            | <span data-ttu-id="ad31f-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ad31f-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="ad31f-140">Integrācijas elements kategorijām</span><span class="sxs-lookup"><span data-stu-id="ad31f-140">Integration entity for categories</span></span> | <span data-ttu-id="ad31f-141">Transakciju kategorijas</span><span class="sxs-lookup"><span data-stu-id="ad31f-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="ad31f-142">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="ad31f-142">Entity flow</span></span>

<span data-ttu-id="ad31f-143">Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="ad31f-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ad31f-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="ad31f-144">Power Query</span></span>

<span data-ttu-id="ad31f-145">Kad veicat sinhronizāciju ar programmu Project Service Automation, ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel, lai iestatītu transakciju kategorijas norēķinu veidu.</span><span class="sxs-lookup"><span data-stu-id="ad31f-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="ad31f-146">Veidne Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) nodrošina noklusējuma kolonnu un kartējumu.</span><span class="sxs-lookup"><span data-stu-id="ad31f-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="ad31f-147">Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna risinājumā Power Query.</span><span class="sxs-lookup"><span data-stu-id="ad31f-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="ad31f-148">Veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ad31f-148">Follow these steps.</span></span>

1. <span data-ttu-id="ad31f-149">Noklikšķiniet uz bultiņas, lai veidnē Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) atvērtu projekta izdevumu kategoriju uzdevuma kartējumu.</span><span class="sxs-lookup"><span data-stu-id="ad31f-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="ad31f-150">Noklikšķiniet uz saites **Paplašinātais vaicājums un filtrēšana**, lai atvērtu Power Query.</span><span class="sxs-lookup"><span data-stu-id="ad31f-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="ad31f-151">Atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="ad31f-152">Ievadiet jaunās kolonnas nosaukumu, piemēram, **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="ad31f-153">Ievadiet šādu nosacījumu: **ja CATEGORYID nav vienāds ar Null, tad 19235001; pretējā gadījumā vērtība ir Null**.</span><span class="sxs-lookup"><span data-stu-id="ad31f-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="ad31f-154">Noklikšķiniet **Labi** uz kolonnas.</span><span class="sxs-lookup"><span data-stu-id="ad31f-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="ad31f-155">Noteikti kartējiet šo jauno kolonnu uz kartējuma lapu.</span><span class="sxs-lookup"><span data-stu-id="ad31f-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="ad31f-156">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="ad31f-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ad31f-157">Kartējums norāda programmā Finance and Operations ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ad31f-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="ad31f-158">[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ad31f-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ad31f-159">Projekta izdevumu kategoriju sinhronizēšana no programmas Project Service Automation uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ad31f-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ad31f-160">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="ad31f-160">Template and task</span></span>

<span data-ttu-id="ad31f-161">Programmā Project Service Automation ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevums.</span><span class="sxs-lookup"><span data-stu-id="ad31f-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="ad31f-162">**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ad31f-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ad31f-163">**Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz Fin Ops</span><span class="sxs-lookup"><span data-stu-id="ad31f-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="ad31f-164">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="ad31f-164">Entity set</span></span>

| <span data-ttu-id="ad31f-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ad31f-165">Project Service Automation</span></span> | <span data-ttu-id="ad31f-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ad31f-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="ad31f-167">Transakciju kategorijas</span><span class="sxs-lookup"><span data-stu-id="ad31f-167">Transaction categories</span></span>     | <span data-ttu-id="ad31f-168">Integrācijas elements kategorijām</span><span class="sxs-lookup"><span data-stu-id="ad31f-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ad31f-169">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="ad31f-169">Entity flow</span></span>

<span data-ttu-id="ad31f-170">Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="ad31f-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="ad31f-171">Sinhronizēšana atpakaļ uz programmu Finance and Operations atjaunina programmā Finance and Operations ietverto projekta kategoriju ar Project Service Automation integrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="ad31f-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ad31f-172">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="ad31f-172">Template mapping in Data integration</span></span>

<span data-ttu-id="ad31f-173">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="ad31f-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ad31f-174">Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ad31f-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ad31f-175">[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ad31f-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
