---
title: " Lojalitātes programmas atlīdzības punktu korekciju apstrāde"
description: Šajā procedūra parādīts, kā atrast informāciju par lojalitātes programmas karti un koriģēt lojalitātes programmas atlīdzības punktus.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eae943985cc2bd706c0c3c4ec7b0470e3a54bff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802627"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="3be35-103"> Lojalitātes programmas atlīdzības punktu korekciju apstrāde</span><span class="sxs-lookup"><span data-stu-id="3be35-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3be35-104">Šajā procedūra parādīts, kā atrast informāciju par lojalitātes programmas karti un koriģēt lojalitātes programmas atlīdzības punktus.</span><span class="sxs-lookup"><span data-stu-id="3be35-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="3be35-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="3be35-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="3be35-106">Šis uzdevums ir paredzēts lomai Commerce operāciju pārvaldnieks vai Klientu apkalpošanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="3be35-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="3be35-107">Pārejiet uz cilni Lojalitātes programmas kartes.</span><span class="sxs-lookup"><span data-stu-id="3be35-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="3be35-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3be35-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3be35-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3be35-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3be35-110">Noklikšķiniet uz Kartes transakcijas.</span><span class="sxs-lookup"><span data-stu-id="3be35-110">Click Card transactions.</span></span>
    * <span data-ttu-id="3be35-111">Šajā lapā varat skatīt visas lojalitātes programmas transakcijas atlasītajai lojalitātes programmas kartei.</span><span class="sxs-lookup"><span data-stu-id="3be35-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="3be35-112">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3be35-112">Close the page.</span></span>
6. <span data-ttu-id="3be35-113">Noklikšķiniet uz Karšu korekcijas.</span><span class="sxs-lookup"><span data-stu-id="3be35-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="3be35-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3be35-114">Click New.</span></span>
8. <span data-ttu-id="3be35-115">Laukā Atlīdzības punkts ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3be35-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="3be35-116">Laukā Summa vai daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="3be35-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="3be35-117">Varat pievienot vai noņemt punktus no lojalitātes programmas kartes, izmantojot pozitīvu vai negatīvu summu.</span><span class="sxs-lookup"><span data-stu-id="3be35-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="3be35-118">Laukā Lojalitātes programma ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3be35-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="3be35-119">Laukā Komentārs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3be35-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="3be35-120">Noklikšķiniet uz Grāmatot korekciju.</span><span class="sxs-lookup"><span data-stu-id="3be35-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="3be35-121">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="3be35-121">Click Yes.</span></span>
14. <span data-ttu-id="3be35-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3be35-122">Close the page.</span></span>
    * <span data-ttu-id="3be35-123">Parasti lapa ir jāatsvaidzina, lai atlīdzības punktu pārrēķina rezultāts būtu redzams atlīdzības punktu kopsavilkuma cilnē. Ja šai darbībai izmantojat uzdevumu ceļvedi, atsvaidzināšana nav jāveic, citādi uzdevumu ceļveža darbība tiks pārtraukta.</span><span class="sxs-lookup"><span data-stu-id="3be35-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="3be35-124">Noklikšķiniet uz Kartes transakcijas.</span><span class="sxs-lookup"><span data-stu-id="3be35-124">Click Card transactions.</span></span>
16. <span data-ttu-id="3be35-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3be35-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]