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
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22538d58cc3499bd030848699d6c5831dfd8888a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975164"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="ff6c2-103">Izveidot publiskā sektora provizorisko budžetu</span><span class="sxs-lookup"><span data-stu-id="ff6c2-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff6c2-104">Varat izveidot sākotnējos budžeta reģistra ierakstus noteiktam budžeta modelim un dimensiju vērtībām.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="ff6c2-105">Kam faktiskais budžets ir apstiprināts, varat izveidot sākotnējos budžeta reģistra ierakstus.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="ff6c2-106">Šīs procedūras izveidē tika izmantoti demonstrācijas uzņēmuma “PSUS” dati un publiskā sektora nodalījums.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="ff6c2-107">Pārejiet uz sadaļu Budžets > Budžeta reģistra ieraksti.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="ff6c2-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-108">Click New.</span></span>
3. <span data-ttu-id="ff6c2-109">Laukā Budžeta modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ff6c2-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ff6c2-111">Laukā Budžeta kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ff6c2-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ff6c2-113">Laukā Iemesla kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ff6c2-114">Sarakstā noklikšķiniet uz vēlamā ieraksta.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="ff6c2-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-115">Click Save.</span></span>
10. <span data-ttu-id="ff6c2-116">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-116">Click Add line.</span></span>
    * <span data-ttu-id="ff6c2-117">Neobligāti: ja vēlaties mainīt datumu galvenē, ievadiet jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="ff6c2-118">Šis datums nosaka finanšu periodu, kurā tiks reģistrēts budžets.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="ff6c2-119">Skatot uzdevumu ceļvedi, lai aizpildītu citus laukus, lapas augšdaļā noklikšķiniet uz Atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="ff6c2-120">Laukā Konta struktūra noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ff6c2-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="ff6c2-122">Laukā Dimensiju vērtības norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="ff6c2-123">Laukā Summa ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="ff6c2-124">Varat arī ievadīt summas veidu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="ff6c2-125">Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="ff6c2-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ff6c2-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-127">Click Save.</span></span>
18. <span data-ttu-id="ff6c2-128">Noklikšķiniet uz Atjaunināt budžeta bilances.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="ff6c2-129">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-129">Click Update.</span></span>
    * <span data-ttu-id="ff6c2-130">Lai apskatītu izmaiņu rezultātus, zilās krāsas joslā noklikšķiniet uz Ziņojuma detalizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-130">To see the results of the update, click Message details on the blue bar.</span></span>  

