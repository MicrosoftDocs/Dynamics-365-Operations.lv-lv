---
title: Izveidot publiskā sektora provizorisko budžetu
description: Varat izveidot sākotnējos budžeta reģistra ierakstus noteiktam budžeta modelim un dimensiju vērtībām.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98968b0025ff5c3b9723dc6cc8a8eae799a4eb43
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "317135"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="3651c-103">Izveidot publiskā sektora provizorisko budžetu</span><span class="sxs-lookup"><span data-stu-id="3651c-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3651c-104">Varat izveidot sākotnējos budžeta reģistra ierakstus noteiktam budžeta modelim un dimensiju vērtībām.</span><span class="sxs-lookup"><span data-stu-id="3651c-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="3651c-105">Kam faktiskais budžets ir apstiprināts, varat izveidot sākotnējos budžeta reģistra ierakstus.</span><span class="sxs-lookup"><span data-stu-id="3651c-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="3651c-106">Šīs procedūras izveidē tika izmantoti demonstrācijas uzņēmuma “PSUS” dati un publiskā sektora nodalījums.</span><span class="sxs-lookup"><span data-stu-id="3651c-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="3651c-107">Pārejiet uz sadaļu Budžets > Budžeta reģistra ieraksti.</span><span class="sxs-lookup"><span data-stu-id="3651c-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="3651c-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3651c-108">Click New.</span></span>
3. <span data-ttu-id="3651c-109">Laukā Budžeta modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="3651c-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3651c-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3651c-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3651c-111">Laukā Budžeta kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="3651c-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3651c-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3651c-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3651c-113">Laukā Iemesla kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="3651c-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3651c-114">Sarakstā noklikšķiniet uz vēlamā ieraksta.</span><span class="sxs-lookup"><span data-stu-id="3651c-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="3651c-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3651c-115">Click Save.</span></span>
10. <span data-ttu-id="3651c-116">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="3651c-116">Click Add line.</span></span>
    * <span data-ttu-id="3651c-117">Neobligāti: ja vēlaties mainīt datumu galvenē, ievadiet jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="3651c-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="3651c-118">Šis datums nosaka finanšu periodu, kurā tiks reģistrēts budžets.</span><span class="sxs-lookup"><span data-stu-id="3651c-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="3651c-119">Skatot uzdevumu ceļvedi, lai aizpildītu citus laukus, lapas augšdaļā noklikšķiniet uz Atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="3651c-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="3651c-120">Laukā Konta struktūra noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3651c-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="3651c-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3651c-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="3651c-122">Laukā Dimensiju vērtības norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="3651c-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="3651c-123">Laukā Summa ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="3651c-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="3651c-124">Varat arī ievadīt summas veidu.</span><span class="sxs-lookup"><span data-stu-id="3651c-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="3651c-125">Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3651c-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="3651c-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3651c-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="3651c-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3651c-127">Click Save.</span></span>
18. <span data-ttu-id="3651c-128">Noklikšķiniet uz Atjaunināt budžeta bilances.</span><span class="sxs-lookup"><span data-stu-id="3651c-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="3651c-129">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="3651c-129">Click Update.</span></span>
    * <span data-ttu-id="3651c-130">Lai apskatītu izmaiņu rezultātus, zilās krāsas joslā noklikšķiniet uz Ziņojuma detalizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="3651c-130">To see the results of the update, click Message details on the blue bar.</span></span>  

