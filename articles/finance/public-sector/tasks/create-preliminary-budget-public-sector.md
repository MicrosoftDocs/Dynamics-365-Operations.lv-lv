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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05e8059f44000fd305ed2c2555511da29b130af9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144560"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="69b77-103">Izveidot publiskā sektora provizorisko budžetu</span><span class="sxs-lookup"><span data-stu-id="69b77-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69b77-104">Varat izveidot sākotnējos budžeta reģistra ierakstus noteiktam budžeta modelim un dimensiju vērtībām.</span><span class="sxs-lookup"><span data-stu-id="69b77-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="69b77-105">Kam faktiskais budžets ir apstiprināts, varat izveidot sākotnējos budžeta reģistra ierakstus.</span><span class="sxs-lookup"><span data-stu-id="69b77-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="69b77-106">Šīs procedūras izveidē tika izmantoti demonstrācijas uzņēmuma “PSUS” dati un publiskā sektora nodalījums.</span><span class="sxs-lookup"><span data-stu-id="69b77-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="69b77-107">Pārejiet uz sadaļu Budžets > Budžeta reģistra ieraksti.</span><span class="sxs-lookup"><span data-stu-id="69b77-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="69b77-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="69b77-108">Click New.</span></span>
3. <span data-ttu-id="69b77-109">Laukā Budžeta modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="69b77-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="69b77-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="69b77-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="69b77-111">Laukā Budžeta kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="69b77-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="69b77-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="69b77-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="69b77-113">Laukā Iemesla kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="69b77-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="69b77-114">Sarakstā noklikšķiniet uz vēlamā ieraksta.</span><span class="sxs-lookup"><span data-stu-id="69b77-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="69b77-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="69b77-115">Click Save.</span></span>
10. <span data-ttu-id="69b77-116">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="69b77-116">Click Add line.</span></span>
    * <span data-ttu-id="69b77-117">Neobligāti: ja vēlaties mainīt datumu galvenē, ievadiet jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="69b77-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="69b77-118">Šis datums nosaka finanšu periodu, kurā tiks reģistrēts budžets.</span><span class="sxs-lookup"><span data-stu-id="69b77-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="69b77-119">Skatot uzdevumu ceļvedi, lai aizpildītu citus laukus, lapas augšdaļā noklikšķiniet uz Atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="69b77-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="69b77-120">Laukā Konta struktūra noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="69b77-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="69b77-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="69b77-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="69b77-122">Laukā Dimensiju vērtības norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="69b77-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="69b77-123">Laukā Summa ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="69b77-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="69b77-124">Varat arī ievadīt summas veidu.</span><span class="sxs-lookup"><span data-stu-id="69b77-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="69b77-125">Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="69b77-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="69b77-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="69b77-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="69b77-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="69b77-127">Click Save.</span></span>
18. <span data-ttu-id="69b77-128">Noklikšķiniet uz Atjaunināt budžeta bilances.</span><span class="sxs-lookup"><span data-stu-id="69b77-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="69b77-129">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="69b77-129">Click Update.</span></span>
    * <span data-ttu-id="69b77-130">Lai apskatītu izmaiņu rezultātus, zilās krāsas joslā noklikšķiniet uz Ziņojuma detalizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="69b77-130">To see the results of the update, click Message details on the blue bar.</span></span>  

