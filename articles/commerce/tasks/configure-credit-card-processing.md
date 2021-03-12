---
title: Kredītkaršu apstrādes konfigurēšana
description: Šajā procedūrā ir aprakstīts, kā skatīt maksājumu nodrošinātāju sarakstu un konfigurēt maksājumu kontu debitoru parādiem.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 611cc49d2373247da141d2fafc149d05f3bd13b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006114"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="86696-103">Kredītkaršu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="86696-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86696-104">Šajā procedūrā ir aprakstīts, kā skatīt maksājumu nodrošinātāju sarakstu un konfigurēt maksājumu kontu debitoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="86696-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="86696-105">Šajā procedūra tiek izmantoti demonstrācijas uzņēmuma “USRT” dati un tas ir paredzēts lomai Administrators un IT profesionālis.</span><span class="sxs-lookup"><span data-stu-id="86696-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="86696-106">Maksājumu nodrošinātāju saraksta skatīšana</span><span class="sxs-lookup"><span data-stu-id="86696-106">View a list of payment providers</span></span>
1. <span data-ttu-id="86696-107">Pārejiet uz sadaļu Debitoru parādi > Maksājumu iestatīšana > Maksājumu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="86696-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="86696-108">Noklikšķiniet uz Skatīt pieejamos nodrošinātājus.</span><span class="sxs-lookup"><span data-stu-id="86696-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="86696-109">Maksājumu konta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="86696-109">Configure payment account</span></span>
1. <span data-ttu-id="86696-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="86696-110">Click New.</span></span>
2. <span data-ttu-id="86696-111">Laukā Maksājumu pakalpojums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="86696-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="86696-112">Laukā Maksājumu savienotājs atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="86696-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="86696-113">Pārslēdziet sadaļas Maksājumu pakalpojuma konts paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="86696-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="86696-114">Laukā Vide ierakstiet PROD.</span><span class="sxs-lookup"><span data-stu-id="86696-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="86696-115">Noklikšķiniet uz Kredītkaršu veidi.</span><span class="sxs-lookup"><span data-stu-id="86696-115">Click Credit card types.</span></span>
7. <span data-ttu-id="86696-116">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="86696-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="86696-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="86696-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="86696-118">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="86696-118">Click Add.</span></span>
10. <span data-ttu-id="86696-119">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="86696-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="86696-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="86696-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="86696-121">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="86696-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="86696-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="86696-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="86696-123">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="86696-123">Click Add.</span></span>
15. <span data-ttu-id="86696-124">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="86696-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="86696-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="86696-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="86696-126">Varat atkārtot šīs darbības tik daudz kartes tipiem, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="86696-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="86696-127">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="86696-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="86696-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="86696-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="86696-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="86696-129">Click Add.</span></span>
20. <span data-ttu-id="86696-130">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="86696-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="86696-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="86696-131">Click Save.</span></span>
22. <span data-ttu-id="86696-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="86696-132">Close the page.</span></span>
23. <span data-ttu-id="86696-133">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="86696-133">Click Validate.</span></span>
24. <span data-ttu-id="86696-134">Noklikšķiniet uz opcijas Noklusējuma procesors, kas redzams blakus jauno kredītkaršu izvēles rūtiņai.</span><span class="sxs-lookup"><span data-stu-id="86696-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="86696-135">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="86696-135">Click Save.</span></span>

