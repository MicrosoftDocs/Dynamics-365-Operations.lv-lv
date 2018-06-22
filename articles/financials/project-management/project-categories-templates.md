---
title: "Projekta izdevumu kategoriju sinhronizēšana no programmas Project Service Automation"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp programmām Microsoft Dynamics 365 for Finance and Operations un Dynamics 365 for Project Service Automation."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="ac4be-103">Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ac4be-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="ac4be-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp programmām Microsoft Dynamics 365 for Finance and Operations un Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ac4be-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="ac4be-105">Projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.0.</span><span class="sxs-lookup"><span data-stu-id="ac4be-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="ac4be-106">Datu plūsma programmai Project Service Automation un programmai Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac4be-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="ac4be-107">Risinājums, lai veiktu integrēšanu starp programmām Project Service Automation un Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs.</span><span class="sxs-lookup"><span data-stu-id="ac4be-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="ac4be-108">Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta izdevumu transakciju kategorijām starp programmu Finance and Operations un programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ac4be-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="ac4be-109">Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, integrācijas plūsma vispirms tiek nosūtīta no programmas Finance and Operations uz programmu Project Service Automation, un pēc tam tiek veikta projekta izdevumu kategoriju integrācijas ID atjaunināšana, sinhronizējot no programmas Project Service Automation uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac4be-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ac4be-110">Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Project Service Automation, integrācijas plūsma vispirms tiek nosūtīta no programmas Project Service Automation uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac4be-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="ac4be-111">Projekta kategorijām jau ir jābūt konfigurētām programmā Finance and Operations pirms sinhronizācijas no programmas Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ac4be-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="ac4be-112">Pēc tam sinhronizējiet no programmas Finance and Operations atpakaļ uz programmu Project Service Automation un pēc tam vēlreiz no programmas Project Service Automation uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac4be-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="ac4be-113">Tas nodrošina, ka kategorijas ir saistītas un ka nav izveidoti dublikāti.</span><span class="sxs-lookup"><span data-stu-id="ac4be-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="ac4be-114">Parasti projekta izdevumu kategoriju pārvaldība tiek veikta programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac4be-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="ac4be-115">Ja jūsu situācija ir atšķirīga vai jums jau ir izveidotas projekta izdevumu kategorijas programmā Project Service Automation, vispirms jāveic sinhronizēšana, izmantojot Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops) un pēc jāveic sinhronizēšana, izmantojot Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA).</span><span class="sxs-lookup"><span data-stu-id="ac4be-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="ac4be-116">Pēc tam vēlreiz jāpalaiž sinhronizēšana no PSA uz Fin and Ops.</span><span class="sxs-lookup"><span data-stu-id="ac4be-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="ac4be-117">Ja vispirms tiek veikta sinhronizēšana no programmas Project Service Automation, projektu kategorijām jau ir jābūt izveidotām programmā Finance and Operations un visām projektu kategorijām, kuras nepieciešams sinhronizēt ar programmas Project Service Automation transakciju kategorijām, jābūt iestatītam vienumam **Aktīvs žurnālos**.</span><span class="sxs-lookup"><span data-stu-id="ac4be-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="ac4be-118">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac4be-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="ac4be-119">[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ac4be-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="ac4be-120">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="ac4be-120">Templates and tasks</span></span>

<span data-ttu-id="ac4be-121">Lai piekļūtu pieejamajām veidnēm, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="ac4be-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ac4be-122">Programmā Finance and Operations ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevums.</span><span class="sxs-lookup"><span data-stu-id="ac4be-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="ac4be-123">**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA)</span><span class="sxs-lookup"><span data-stu-id="ac4be-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="ac4be-124">**Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz PSA</span><span class="sxs-lookup"><span data-stu-id="ac4be-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="ac4be-125">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="ac4be-125">Entity set</span></span>

| <span data-ttu-id="ac4be-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac4be-126">Finance and Operations</span></span>               | <span data-ttu-id="ac4be-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ac4be-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="ac4be-128">Integrācijas elements kategorijām</span><span class="sxs-lookup"><span data-stu-id="ac4be-128">Integration entity for categories</span></span>    | <span data-ttu-id="ac4be-129">Transakciju kategorijas</span><span class="sxs-lookup"><span data-stu-id="ac4be-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="ac4be-130">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="ac4be-130">Entity flow</span></span>

<span data-ttu-id="ac4be-131">Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="ac4be-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="ac4be-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="ac4be-132">Power Query</span></span>

<span data-ttu-id="ac4be-133">Ir jāizmanto Microsoft Power Query, lai iestatītu transakciju kategorijas norēķinu veidu, veicot sinhronizēšanu uz programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ac4be-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="ac4be-134">Veidnei Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) jau ir nodrošināta noklusējuma kolonna un kartēšana.</span><span class="sxs-lookup"><span data-stu-id="ac4be-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="ac4be-135">Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna risinājumā Power Query.</span><span class="sxs-lookup"><span data-stu-id="ac4be-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="ac4be-136">Atveriet veidlapu Izvērsts vaicājums un filtrēšana no projekta izdevumu kategoriju uzdevuma kartējuma.</span><span class="sxs-lookup"><span data-stu-id="ac4be-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="ac4be-137">Atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="ac4be-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="ac4be-138">Piešķiriet jaunajai kolonnai nosaukumu, piemēram “BillingType”.</span><span class="sxs-lookup"><span data-stu-id="ac4be-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="ac4be-139">Ievadiet šādu nosacījumu: “If **CATEGORYID not equal to null then 19235001, Otherwise null**”.</span><span class="sxs-lookup"><span data-stu-id="ac4be-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="ac4be-140">Noklikšķiniet **Labi** uz kolonnas.</span><span class="sxs-lookup"><span data-stu-id="ac4be-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="ac4be-141">Noteikti kartējiet šo jauno kolonnu kartēšanas lapā.</span><span class="sxs-lookup"><span data-stu-id="ac4be-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="ac4be-142">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="ac4be-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ac4be-143">Kartējums norāda programmā Finance and Operations ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ac4be-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="ac4be-144">[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ac4be-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="ac4be-145">Programmā Project Service Automation ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevums.</span><span class="sxs-lookup"><span data-stu-id="ac4be-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="ac4be-146">-**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops) -**Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="ac4be-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="ac4be-147">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="ac4be-147">Entity set</span></span>

| <span data-ttu-id="ac4be-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ac4be-148">Project Service Automation</span></span>      | <span data-ttu-id="ac4be-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac4be-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="ac4be-150">Transakciju kategorijas</span><span class="sxs-lookup"><span data-stu-id="ac4be-150">Transaction categories</span></span>          | <span data-ttu-id="ac4be-151">Integrācijas elements kategorijām</span><span class="sxs-lookup"><span data-stu-id="ac4be-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="ac4be-152">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="ac4be-152">Entity flow</span></span>

<span data-ttu-id="ac4be-153">Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="ac4be-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="ac4be-154">Sinhronizēšana atpakaļ uz programmu Finance and Operations atjaunina programmā Project Service Automation ietverto integrācijas ID programmas Finance and Operations projekta kategorijā.</span><span class="sxs-lookup"><span data-stu-id="ac4be-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="ac4be-155">Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="ac4be-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ac4be-156">Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac4be-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="ac4be-157">[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ac4be-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

