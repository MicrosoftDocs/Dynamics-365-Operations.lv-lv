---
title: Projekta budžeta iesniegšana un apstiprināšana
description: Šajā procedūrā ir parādīts, kā projektam izveidot un iesniegt budžetu.
author: mkirknel
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14683554c45db72061ecbbf4a528656df3132692
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207455"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="b5932-103">Projekta budžeta iesniegšana un apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="b5932-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5932-104">Šajā procedūrā ir parādīts, kā projektam izveidot un iesniegt budžetu.</span><span class="sxs-lookup"><span data-stu-id="b5932-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="b5932-105">Kad veidojat projekta budžetu, varat ievadīt projektam prognozētos ieņēmumus un izmaksas un pēc tam tos izmantot, lai kontrolētu projekta faktiskās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="b5932-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="b5932-106">Projekta budžeta veidošanā visi sākotnējie budžeti un pārskatījumi ir jānosūta uz projekta darbplūsmu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="b5932-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="b5932-107">Darbplūsma jums sniedz lielāku kontroli pār procesu un izveido izmaiņu vēstures ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5932-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="b5932-108">Šis uzdevums tika izveidots, izmantojot uzņēmuma USSI datu kopu.</span><span class="sxs-lookup"><span data-stu-id="b5932-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="b5932-109">**Navigācijas rūtī** atveriet **Moduļi > Projektu pārvaldība un uzskaite > Projekti > Visiem projekti**.</span><span class="sxs-lookup"><span data-stu-id="b5932-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="b5932-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5932-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b5932-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5932-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b5932-112">**Darbību rūtī** noklikšķiniet uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="b5932-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="b5932-113">Noklikšķiniet uz **Projekta budžets**.</span><span class="sxs-lookup"><span data-stu-id="b5932-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="b5932-114">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b5932-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="b5932-115">Izvērsiet kopsavilkuma cilni **Izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="b5932-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="b5932-116">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b5932-116">Click **New**.</span></span>
9. <span data-ttu-id="b5932-117">Laukā **Transakcijas veids** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="b5932-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="b5932-118">Laukā **Kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b5932-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="b5932-119">Laukā **Sākotnējais budžets** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="b5932-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="b5932-120">Izvērsiet kopsavilkuma cilni **Ieņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="b5932-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="b5932-121">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b5932-121">Click **New**.</span></span>
14. <span data-ttu-id="b5932-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b5932-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="b5932-123">Laukā **Transakcijas veids** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="b5932-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="b5932-124">Laukā **Kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b5932-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="b5932-125">Laukā **Sākotnējais budžets** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="b5932-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="b5932-126">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b5932-126">Click **Save**.</span></span>
19. <span data-ttu-id="b5932-127">Noklikšķiniet uz **Darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="b5932-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="b5932-128">Noklikšķiniet uz **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="b5932-128">Click **Submit**.</span></span>
21. <span data-ttu-id="b5932-129">Laukā **Komentārs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b5932-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="b5932-130">Noklikšķiniet uz **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="b5932-130">Click **Submit**.</span></span>

