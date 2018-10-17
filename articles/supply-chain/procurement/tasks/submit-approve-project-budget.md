--- 
title: "Projekta budžeta iesniegšana un apstiprināšana"
description: "Šajā procedūrā ir parādīts, kā projektam izveidot un iesniegt budžetu."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="e0b91-103">Projekta budžeta iesniegšana un apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="e0b91-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0b91-104">Šajā procedūrā ir parādīts, kā projektam izveidot un iesniegt budžetu.</span><span class="sxs-lookup"><span data-stu-id="e0b91-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="e0b91-105">Kad veidojat projekta budžetu, varat ievadīt projektam prognozētos ieņēmumus un izmaksas un pēc tam tos izmantot, lai kontrolētu projekta faktiskās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="e0b91-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="e0b91-106">Projekta budžeta veidošanā visi sākotnējie budžeti un pārskatījumi ir jānosūta uz projekta darbplūsmu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="e0b91-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="e0b91-107">Darbplūsma jums sniedz lielāku kontroli pār procesu un izveido izmaiņu vēstures ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0b91-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="e0b91-108">Šis uzdevums tika izveidots, izmantojot uzņēmuma USSI datu kopu.</span><span class="sxs-lookup"><span data-stu-id="e0b91-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="e0b91-109">Dodieties uz Projektu vadība un uzskaite > Projekti > Visi projekti.</span><span class="sxs-lookup"><span data-stu-id="e0b91-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="e0b91-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0b91-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e0b91-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e0b91-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e0b91-112">Darbību rūtī noklikšķiniet uz Plāns.</span><span class="sxs-lookup"><span data-stu-id="e0b91-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="e0b91-113">Noklikšķiniet uz Projekta budžets.</span><span class="sxs-lookup"><span data-stu-id="e0b91-113">Click Project budget.</span></span>
6. <span data-ttu-id="e0b91-114">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e0b91-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="e0b91-115">Izvērsiet sadaļu Izmaksas</span><span class="sxs-lookup"><span data-stu-id="e0b91-115">Expand the Cost section</span></span>
8. <span data-ttu-id="e0b91-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e0b91-116">Click New.</span></span>
9. <span data-ttu-id="e0b91-117">Laukā Transakcijas tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="e0b91-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="e0b91-118">Laukā Kategorija ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e0b91-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="e0b91-119">Laukā Sākotnējais budžets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e0b91-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="e0b91-120">Izvērsiet sadaļu Ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="e0b91-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="e0b91-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e0b91-121">Click New.</span></span>
14. <span data-ttu-id="e0b91-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e0b91-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e0b91-123">Laukā Transakcijas tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="e0b91-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="e0b91-124">Laukā Kategorija ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e0b91-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="e0b91-125">Laukā Sākotnējais budžets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e0b91-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="e0b91-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e0b91-126">Click Save.</span></span>
19. <span data-ttu-id="e0b91-127">Noklikšķiniet uz Darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="e0b91-127">Click Workflow.</span></span>
20. <span data-ttu-id="e0b91-128">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="e0b91-128">Click Submit.</span></span>
21. <span data-ttu-id="e0b91-129">Laukā Komentārs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e0b91-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="e0b91-130">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="e0b91-130">Click Submit.</span></span>


