--- 
title: " Kredītkaršu apstrādes konfigurēšana"
description: "Šajā procedūrā ir aprakstīts, kā skatīt maksājumu nodrošinātāju sarakstu un konfigurēt maksājumu kontu debitoru parādiem."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3b54cfdb22c0c9daa9564ae36ad2bb89edb81f11
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="2afe9-103"> Kredītkaršu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2afe9-103">Configure credit card processing</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2afe9-104">Šajā procedūrā ir aprakstīts, kā skatīt maksājumu nodrošinātāju sarakstu un konfigurēt maksājumu kontu debitoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="2afe9-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="2afe9-105">Šajā procedūra tiek izmantoti demonstrācijas uzņēmuma “USRT” dati un tas ir paredzēts lomai Administrators un IT profesionālis.</span><span class="sxs-lookup"><span data-stu-id="2afe9-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="2afe9-106">Maksājumu nodrošinātāju saraksta skatīšana</span><span class="sxs-lookup"><span data-stu-id="2afe9-106">View a list of payment providers</span></span>
1. <span data-ttu-id="2afe9-107">Pārejiet uz sadaļu Debitoru parādi > Maksājumu iestatīšana > Maksājumu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="2afe9-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="2afe9-108">Noklikšķiniet uz Skatīt pieejamos nodrošinātājus.</span><span class="sxs-lookup"><span data-stu-id="2afe9-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="2afe9-109">Maksājumu konta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="2afe9-109">Configure payment account</span></span>
1. <span data-ttu-id="2afe9-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2afe9-110">Click New.</span></span>
2. <span data-ttu-id="2afe9-111">Laukā Maksājumu pakalpojums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2afe9-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="2afe9-112">Laukā Maksājumu savienotājs atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="2afe9-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="2afe9-113">Pārslēdziet sadaļas Maksājumu pakalpojuma konts paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="2afe9-114">Laukā Vide ierakstiet PROD.</span><span class="sxs-lookup"><span data-stu-id="2afe9-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="2afe9-115">Noklikšķiniet uz Kredītkaršu veidi.</span><span class="sxs-lookup"><span data-stu-id="2afe9-115">Click Credit card types.</span></span>
7. <span data-ttu-id="2afe9-116">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2afe9-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2afe9-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2afe9-118">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2afe9-118">Click Add.</span></span>
10. <span data-ttu-id="2afe9-119">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2afe9-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="2afe9-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2afe9-121">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2afe9-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2afe9-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2afe9-123">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2afe9-123">Click Add.</span></span>
15. <span data-ttu-id="2afe9-124">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2afe9-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="2afe9-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2afe9-126">Varat atkārtot šīs darbības tik daudz kartes tipiem, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="2afe9-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="2afe9-127">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="2afe9-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2afe9-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="2afe9-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2afe9-129">Click Add.</span></span>
20. <span data-ttu-id="2afe9-130">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2afe9-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="2afe9-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2afe9-131">Click Save.</span></span>
22. <span data-ttu-id="2afe9-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2afe9-132">Close the page.</span></span>
23. <span data-ttu-id="2afe9-133">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="2afe9-133">Click Validate.</span></span>
24. <span data-ttu-id="2afe9-134">Noklikšķiniet uz opcijas Noklusējuma procesors, kas redzams blakus jauno kredītkaršu izvēles rūtiņai.</span><span class="sxs-lookup"><span data-stu-id="2afe9-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="2afe9-135">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2afe9-135">Click Save.</span></span>


