---
title: " Lojalitātes programmas atlīdzības punktu definēšana"
description: Šajā procedūrā parādīts, kā definēt lojalitātes programmas atlīdzības punktus.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ae26123d41fa74d32b102ddb7f021e9846a676
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "354510"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="50df1-103"> Lojalitātes programmas atlīdzības punktu definēšana</span><span class="sxs-lookup"><span data-stu-id="50df1-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="50df1-104">Šajā procedūrā parādīts, kā definēt lojalitātes programmas atlīdzības punktus.</span><span class="sxs-lookup"><span data-stu-id="50df1-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="50df1-105">Pirms iestatāt lojalitātes programmu, jāiestata lojalitātes programmas atlīdzības punkti.</span><span class="sxs-lookup"><span data-stu-id="50df1-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="50df1-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="50df1-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="50df1-107">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Debitori > Lojalitātes programma > Lojalitātes programmas atlīdzības punkti.</span><span class="sxs-lookup"><span data-stu-id="50df1-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="50df1-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="50df1-108">Click New.</span></span>
3. <span data-ttu-id="50df1-109">Laukā Atlīdzības punkta ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="50df1-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="50df1-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="50df1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="50df1-111">Laukā Atlīdzības punkta veids atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="50df1-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="50df1-112">Atlasiet Daudzums, ja vēlaties, lai atlīdzības punkti tiktu noapaļoti līdz tuvākajam veselam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="50df1-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="50df1-113">Atlasiet Summa, ja vēlaties, lai atlīdzības punkti tiktu noapaļoti atbilstoši valūtas noapaļošanas kārtulām.</span><span class="sxs-lookup"><span data-stu-id="50df1-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="50df1-114">Ja atlasīsiet Daudzums, izlaidiet nākamo šīs procedūras darbību.</span><span class="sxs-lookup"><span data-stu-id="50df1-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="50df1-115">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="50df1-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="50df1-116">Summas veida atlīdzības punktu gadījumā visi izsniegtie punkti būs atlasītajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="50df1-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="50df1-117">Daudzuma veida atlīdzības punktu šis lauks netiks lietots — izlaidiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="50df1-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="50df1-118">Atzīmējiet izvēles rūtiņu Izpērkams vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="50df1-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="50df1-119">Laukā Izpirkšanas rangi ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="50df1-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="50df1-120">Izpirkšanas rangi tiek izmantoti, ja divus vai vairāk izpērkamus atlīdzības punktus var izmantot, lai maksātu par precēm.</span><span class="sxs-lookup"><span data-stu-id="50df1-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="50df1-121">Ja diviem atlīdzības punktiem ir vienāds izpirkšanas rangs, tad tiks izmantots tas, kuram nepieciešams mazāks punktu skaits.</span><span class="sxs-lookup"><span data-stu-id="50df1-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="50df1-122">Laukā Termiņa beigu laika vērtība ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="50df1-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="50df1-123">Piešķirtajiem atlīdzības punktiem ir konkrēts derīguma termiņš dienās, mēnešos vai gados.</span><span class="sxs-lookup"><span data-stu-id="50df1-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="50df1-124">Vērtība 0 nozīmē to, ka lojalitātes programmas atlīdzības punktiem nav derīguma termiņa.</span><span class="sxs-lookup"><span data-stu-id="50df1-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="50df1-125">Laukā Termiņa beigu laika vienība atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="50df1-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="50df1-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50df1-126">Click Save.</span></span>

