---
title: "Pievienot finanšu dimensijas CFO darbvietai"
description: "Šajā tēmā izskaidrots, kā CFO darbvietai pievienot finanšu dimensijas, lai tās varētu izmantot virsgrāmatas un budžeta pārskatos."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: lv-lv
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="27ad3-103">Pievienot finanšu dimensijas CFO darbvietai</span><span class="sxs-lookup"><span data-stu-id="27ad3-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27ad3-104">Šajā tēmā izskaidrots, kā finanšu direktora (CFO) darbvietai pievienot finanšu dimensijas, lai tās varētu izmantot virsgrāmatas un budžeta pārskatos.</span><span class="sxs-lookup"><span data-stu-id="27ad3-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="27ad3-105">CFO darbvietai ir cilne **Apskats** un **Finanses**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="27ad3-106">Šajās divās cilnēs pieejamos pārskatus nodrošina divi mēri: LedgerActivityMeasure un BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="27ad3-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="27ad3-107">Microsoft Dynamics 365 for Finance and Operations Enterprise edition 2017. gada jūlija atjauninājumā ir relācija starp šiem diviem mēriem un DimensionCombinationEntity elementu.</span><span class="sxs-lookup"><span data-stu-id="27ad3-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="27ad3-108">Tādējādi var atlasīt dimensijas.</span><span class="sxs-lookup"><span data-stu-id="27ad3-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="27ad3-109">Finance and Operations lapā **Elementu krātuve** atjauniniet **LedgerActivityMeasure** un **BudgetActivityMeasure** mērus.</span><span class="sxs-lookup"><span data-stu-id="27ad3-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="27ad3-110">Microsoft Visual Studio atveriet programmu Lietojumprogrammas pārlūks un meklējiet **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="27ad3-111">Sadaļā **Resursi** atveriet **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="27ad3-112">Kad resurss tiek atvērts Microsoft Power BI darbvirsmā, atlasiet **Iegūt datus**, atlasiet **SQL Server datu bāze** un pēc tam atlasiet **Izveidot savienojumu**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="27ad3-113">Ievadiet servera nosaukumu un ievadiet **AxDW** kā datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="27ad3-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="27ad3-114">Atlasiet **DirectQuery** un pēc tam **Labi**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="27ad3-115">Meklējiet un atlasiet **LedgerActivityMeasure\_DimensionCombination** un pēc tam atlasiet **Ielādēt**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="27ad3-116">Laukā **Lauki** pārdēvējiet tabulu **Finanšu dimensijas** tā, lai to būtu viegli identificēt.</span><span class="sxs-lookup"><span data-stu-id="27ad3-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="27ad3-117">Atlasiet **Pārvaldīt relācijas** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="27ad3-118">Pirmajā laukā atlasiet **Virsgrāmatas aktivitātes** un pēc tam atlasiet **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="27ad3-119">Otrajā laukā atlasiet **LedgerActivityMeasure\_DimensionCombination** (vai **Finanšu dimensijas**, ja pārdēvējāt tabulu).</span><span class="sxs-lookup"><span data-stu-id="27ad3-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="27ad3-120">Atlasiet virsrakstu **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="27ad3-121">Laukā **Kardinalitāte** atlasiet **Daudzi pret vienu**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="27ad3-122">Mainiet vērtību **Krusteniskās filtrēšanas virziens** uz **Viens**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="27ad3-123">Atlasiet gan **Aktivizēt šo relāciju**, gan **Pieņemt atsauces integritāti**, atlasiet **Labi** un pēc tam atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="27ad3-124">[![Relācijas izveide](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="27ad3-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="27ad3-125">Laukā **Lauki** tiek rādīta tabula un pieejamās finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="27ad3-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="27ad3-126">Velciet nepieciešamās finanšu dimensijas uz pārskata līmeņa filtriem.</span><span class="sxs-lookup"><span data-stu-id="27ad3-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="27ad3-127">Saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="27ad3-127">Save your changes.</span></span>
15. <span data-ttu-id="27ad3-128">Lietojumprogrammas objektu kokā (AOT) ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet **Sinhronizēt**.</span><span class="sxs-lookup"><span data-stu-id="27ad3-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="27ad3-129">Izveidojiet projektu un pēc tam atveriet lietojumprogrammu, lai skatītu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="27ad3-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="27ad3-130">[![Izpildīta darbvieta](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="27ad3-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

