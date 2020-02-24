---
title: " Lojalitātes programmas atlīdzības punktu korekciju apstrāde"
description: Šajā procedūra parādīts, kā atrast informāciju par lojalitātes programmas karti un koriģēt lojalitātes programmas atlīdzības punktus.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e767ca571255bcf583b83c6e300292552a96a38
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023269"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="faecc-103"> Lojalitātes programmas atlīdzības punktu korekciju apstrāde</span><span class="sxs-lookup"><span data-stu-id="faecc-103">Process loyalty reward point adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="faecc-104">Šajā procedūra parādīts, kā atrast informāciju par lojalitātes programmas karti un koriģēt lojalitātes programmas atlīdzības punktus.</span><span class="sxs-lookup"><span data-stu-id="faecc-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="faecc-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="faecc-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="faecc-106">Šis uzdevums ir paredzēts lomai Commerce operāciju pārvaldnieks vai Klientu apkalpošanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="faecc-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="faecc-107">Pārejiet uz cilni Lojalitātes programmas kartes.</span><span class="sxs-lookup"><span data-stu-id="faecc-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="faecc-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="faecc-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="faecc-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="faecc-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="faecc-110">Noklikšķiniet uz Kartes transakcijas.</span><span class="sxs-lookup"><span data-stu-id="faecc-110">Click Card transactions.</span></span>
    * <span data-ttu-id="faecc-111">Šajā lapā varat skatīt visas lojalitātes programmas transakcijas atlasītajai lojalitātes programmas kartei.</span><span class="sxs-lookup"><span data-stu-id="faecc-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="faecc-112">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="faecc-112">Close the page.</span></span>
6. <span data-ttu-id="faecc-113">Noklikšķiniet uz Karšu korekcijas.</span><span class="sxs-lookup"><span data-stu-id="faecc-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="faecc-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="faecc-114">Click New.</span></span>
8. <span data-ttu-id="faecc-115">Laukā Atlīdzības punkts ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="faecc-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="faecc-116">Laukā Summa vai daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="faecc-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="faecc-117">Varat pievienot vai noņemt punktus no lojalitātes programmas kartes, izmantojot pozitīvu vai negatīvu summu.</span><span class="sxs-lookup"><span data-stu-id="faecc-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="faecc-118">Laukā Lojalitātes programma ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="faecc-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="faecc-119">Laukā Komentārs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="faecc-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="faecc-120">Noklikšķiniet uz Grāmatot korekciju.</span><span class="sxs-lookup"><span data-stu-id="faecc-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="faecc-121">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="faecc-121">Click Yes.</span></span>
14. <span data-ttu-id="faecc-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="faecc-122">Close the page.</span></span>
    * <span data-ttu-id="faecc-123">Parasti lapa ir jāatsvaidzina, lai atlīdzības punktu pārrēķina rezultāts būtu redzams atlīdzības punktu kopsavilkuma cilnē. Ja šai darbībai izmantojat uzdevumu ceļvedi, atsvaidzināšana nav jāveic, citādi uzdevumu ceļveža darbība tiks pārtraukta.</span><span class="sxs-lookup"><span data-stu-id="faecc-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="faecc-124">Noklikšķiniet uz Kartes transakcijas.</span><span class="sxs-lookup"><span data-stu-id="faecc-124">Click Card transactions.</span></span>
16. <span data-ttu-id="faecc-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="faecc-125">Close the page.</span></span>

