---
title: Sākotnēja budžeta izveide un pēc tam publiskā sektora provizoriskā budžeta ierakstu apgriešana
description: Šajā tēmā sniegta informācija par to, kā izveidot un atsaukt sākotnējo budžeta ierakstu, izmantojot budžeta modeli un dimensijas vērtības, kam ir iepriekšējas budžeta summas.
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
ms.openlocfilehash: 134e2ca851d72965198026107817c66a808ac705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987958"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="5b333-103">Sākotnēja budžeta izveide un pēc tam publiskā sektora provizoriskā budžeta ierakstu apgriešana</span><span class="sxs-lookup"><span data-stu-id="5b333-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b333-104">Izveidojot sākotnējo budžeta ierakstu un izmantojot budžeta modeli un dimensiju vērtības, kas satur sākotnējā budžeta summas, var atcelt sākotnējās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="5b333-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="5b333-105">Šīs procedūras izveidē tika izmantoti demonstrācijas uzņēmuma “PSUS” dati un publiskā sektora nodalījums.</span><span class="sxs-lookup"><span data-stu-id="5b333-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="5b333-106">Pārejiet uz sadaļu Budžets > Budžeta reģistra ieraksti.</span><span class="sxs-lookup"><span data-stu-id="5b333-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="5b333-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5b333-107">Click New.</span></span>
3. <span data-ttu-id="5b333-108">Laukā Budžeta modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="5b333-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5b333-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5b333-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5b333-110">Laukā Budžeta kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="5b333-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5b333-111">Sarakstā noklikšķiniet uz Sākotnējais budžets.</span><span class="sxs-lookup"><span data-stu-id="5b333-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="5b333-112">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5b333-112">Click Save.</span></span>
8. <span data-ttu-id="5b333-113">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="5b333-113">Click Add line.</span></span>
9. <span data-ttu-id="5b333-114">Neobligāti: ja vēlaties mainīt datumu galvenē, ievadiet jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="5b333-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="5b333-115">Šis datums nosaka finanšu periodu, kurā tiks reģistrēts budžets.</span><span class="sxs-lookup"><span data-stu-id="5b333-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="5b333-116">Laukā Konta struktūra noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="5b333-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5b333-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5b333-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5b333-118">Laukā Dimensiju vērtības norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="5b333-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="5b333-119">Laukā Summa ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="5b333-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="5b333-120">Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="5b333-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5b333-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5b333-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="5b333-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5b333-122">Click Save.</span></span>
17. <span data-ttu-id="5b333-123">Noklikšķiniet uz Atjaunināt budžeta bilances.</span><span class="sxs-lookup"><span data-stu-id="5b333-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="5b333-124">Neobligāti: var atlasīt opciju Atcelt sākotnējo budžetu.</span><span class="sxs-lookup"><span data-stu-id="5b333-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="5b333-125">Ievērojiet, ka var atcelt visus sākotnējā budžeta ierakstus vai tikai tos sākotnējā budžeta ierakstus, kam ir jūsu noradītais budžeta kods.</span><span class="sxs-lookup"><span data-stu-id="5b333-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="5b333-126">Lai veiktu papildu atlasi, lapas augšdaļā noklikšķiniet uz atbloķēšanas ikonas.</span><span class="sxs-lookup"><span data-stu-id="5b333-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="5b333-127">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="5b333-127">Click Update.</span></span>

