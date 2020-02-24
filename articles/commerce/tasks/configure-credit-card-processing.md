---
title: " Kredītkaršu apstrādes konfigurēšana"
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
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04ce158a833d04122ee5a724165b06925cea1185
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023294"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="66b25-103"> Kredītkaršu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="66b25-103">Configure credit card processing</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="66b25-104">Šajā procedūrā ir aprakstīts, kā skatīt maksājumu nodrošinātāju sarakstu un konfigurēt maksājumu kontu debitoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="66b25-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="66b25-105">Šajā procedūra tiek izmantoti demonstrācijas uzņēmuma “USRT” dati un tas ir paredzēts lomai Administrators un IT profesionālis.</span><span class="sxs-lookup"><span data-stu-id="66b25-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="66b25-106">Maksājumu nodrošinātāju saraksta skatīšana</span><span class="sxs-lookup"><span data-stu-id="66b25-106">View a list of payment providers</span></span>
1. <span data-ttu-id="66b25-107">Pārejiet uz sadaļu Debitoru parādi > Maksājumu iestatīšana > Maksājumu pakalpojumi.</span><span class="sxs-lookup"><span data-stu-id="66b25-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="66b25-108">Noklikšķiniet uz Skatīt pieejamos nodrošinātājus.</span><span class="sxs-lookup"><span data-stu-id="66b25-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="66b25-109">Maksājumu konta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="66b25-109">Configure payment account</span></span>
1. <span data-ttu-id="66b25-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="66b25-110">Click New.</span></span>
2. <span data-ttu-id="66b25-111">Laukā Maksājumu pakalpojums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="66b25-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="66b25-112">Laukā Maksājumu savienotājs atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="66b25-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="66b25-113">Pārslēdziet sadaļas Maksājumu pakalpojuma konts paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="66b25-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="66b25-114">Laukā Vide ierakstiet PROD.</span><span class="sxs-lookup"><span data-stu-id="66b25-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="66b25-115">Noklikšķiniet uz Kredītkaršu veidi.</span><span class="sxs-lookup"><span data-stu-id="66b25-115">Click Credit card types.</span></span>
7. <span data-ttu-id="66b25-116">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="66b25-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="66b25-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="66b25-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="66b25-118">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="66b25-118">Click Add.</span></span>
10. <span data-ttu-id="66b25-119">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66b25-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="66b25-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="66b25-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="66b25-121">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="66b25-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="66b25-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="66b25-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="66b25-123">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="66b25-123">Click Add.</span></span>
15. <span data-ttu-id="66b25-124">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66b25-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="66b25-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="66b25-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66b25-126">Varat atkārtot šīs darbības tik daudz kartes tipiem, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="66b25-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="66b25-127">Laukā Maksājumu žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="66b25-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="66b25-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="66b25-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="66b25-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="66b25-129">Click Add.</span></span>
20. <span data-ttu-id="66b25-130">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="66b25-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="66b25-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="66b25-131">Click Save.</span></span>
22. <span data-ttu-id="66b25-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="66b25-132">Close the page.</span></span>
23. <span data-ttu-id="66b25-133">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="66b25-133">Click Validate.</span></span>
24. <span data-ttu-id="66b25-134">Noklikšķiniet uz opcijas Noklusējuma procesors, kas redzams blakus jauno kredītkaršu izvēles rūtiņai.</span><span class="sxs-lookup"><span data-stu-id="66b25-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="66b25-135">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="66b25-135">Click Save.</span></span>

