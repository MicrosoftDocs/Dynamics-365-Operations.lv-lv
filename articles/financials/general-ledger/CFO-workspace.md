---
title: "Pievienot finanšu dimensijas CFO darbvietai"
description: "Šajā tēmā izskaidrots, kā CFO darbvietai pievienot finanšu dimensijas, lai tās varētu izmantot virsgrāmatas un budžeta pārskatos."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5faefe5da8c3a64987a38ebef92eb87049ebe874
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="4317f-103">Pievienot finanšu dimensijas CFO darbvietai</span><span class="sxs-lookup"><span data-stu-id="4317f-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4317f-104">Šajā tēmā izskaidrots, kā finanšu direktora (CFO) darbvietai pievienot finanšu dimensijas, lai tās varētu izmantot virsgrāmatas un budžeta pārskatos.</span><span class="sxs-lookup"><span data-stu-id="4317f-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="4317f-105">CFO darbvietā ir cilne **Apskats** un cilne **Finanšu**. Abās šajās cilnēs pieejamos pārskatus nodrošina divi mēri: LedgerActivityMeasure un BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="4317f-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="4317f-106">Programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs) pastāv relācija starp šiem diviem mēriem un elementu DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="4317f-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="4317f-107">Tādējādi var atlasīt dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4317f-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="4317f-108">Finance and Operations lapā **Elementu krātuve** atjauniniet **LedgerActivityMeasure** un **BudgetActivityMeasure** mērus.</span><span class="sxs-lookup"><span data-stu-id="4317f-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="4317f-109">Microsoft Visual Studio atveriet programmu Lietojumprogrammas pārlūks un meklējiet **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="4317f-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="4317f-110">Sadaļā **Resursi** atveriet **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="4317f-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="4317f-111">Kad resurss tiek atvērts Microsoft Power BI darbvirsmā, atlasiet **Iegūt datus**, atlasiet **SQL Server datu bāze** un pēc tam atlasiet **Izveidot savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="4317f-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="4317f-112">Ievadiet servera nosaukumu un ievadiet **AxDW** kā datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="4317f-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="4317f-113">Atlasiet **DirectQuery** un pēc tam **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4317f-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="4317f-114">Meklējiet un atlasiet **LedgerActivityMeasure\_DimensionCombination** un pēc tam atlasiet **Ielādēt**.</span><span class="sxs-lookup"><span data-stu-id="4317f-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="4317f-115">Laukā **Lauki** pārdēvējiet tabulu **Finanšu dimensijas** tā, lai to būtu viegli identificēt.</span><span class="sxs-lookup"><span data-stu-id="4317f-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="4317f-116">Atlasiet **Pārvaldīt relācijas** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4317f-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="4317f-117">Pirmajā laukā atlasiet **Virsgrāmatas aktivitātes** un pēc tam atlasiet **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="4317f-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="4317f-118">Otrajā laukā atlasiet **LedgerActivityMeasure\_DimensionCombination** (vai **Finanšu dimensijas**, ja pārdēvējāt tabulu).</span><span class="sxs-lookup"><span data-stu-id="4317f-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="4317f-119">Atlasiet virsrakstu **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="4317f-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="4317f-120">Laukā **Kardinalitāte** atlasiet **Daudzi pret vienu**.</span><span class="sxs-lookup"><span data-stu-id="4317f-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="4317f-121">Mainiet vērtību **Krusteniskās filtrēšanas virziens** uz **Viens**.</span><span class="sxs-lookup"><span data-stu-id="4317f-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="4317f-122">Atlasiet gan **Aktivizēt šo relāciju**, gan **Pieņemt atsauces integritāti**, atlasiet **Labi** un pēc tam atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="4317f-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="4317f-123">[![Relācijas izveide](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="4317f-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="4317f-124">Laukā **Lauki** tiek rādīta tabula un pieejamās finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4317f-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="4317f-125">Velciet nepieciešamās finanšu dimensijas uz pārskata līmeņa filtriem.</span><span class="sxs-lookup"><span data-stu-id="4317f-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="4317f-126">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4317f-126">Save your changes.</span></span>
15. <span data-ttu-id="4317f-127">Lietojumprogrammas objektu kokā (AOT) ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet **Sinhronizēt**.</span><span class="sxs-lookup"><span data-stu-id="4317f-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="4317f-128">Izveidojiet projektu un pēc tam atveriet lietojumprogrammu, lai skatītu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="4317f-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="4317f-129">[![Izpildīta darbvieta](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="4317f-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

