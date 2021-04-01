---
title: Lojalitātes programmas atlīdzības punktu definēšana
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bb190e720e5040d446d75a2e8c39cb360019d42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256881"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="ffba2-103">Lojalitātes programmas atlīdzības punktu definēšana</span><span class="sxs-lookup"><span data-stu-id="ffba2-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffba2-104">Šajā procedūrā parādīts, kā definēt lojalitātes programmas atlīdzības punktus.</span><span class="sxs-lookup"><span data-stu-id="ffba2-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="ffba2-105">Pirms iestatāt lojalitātes programmu, jāiestata lojalitātes programmas atlīdzības punkti.</span><span class="sxs-lookup"><span data-stu-id="ffba2-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="ffba2-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="ffba2-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="ffba2-107">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Debitori > Lojalitātes programma > Lojalitātes programmas atlīdzības punkti.</span><span class="sxs-lookup"><span data-stu-id="ffba2-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="ffba2-108">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="ffba2-108">Click New.</span></span>
3. <span data-ttu-id="ffba2-109">Laukā Atlīdzības punkta ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ffba2-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="ffba2-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ffba2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ffba2-111">Laukā Atlīdzības punkta veids atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ffba2-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="ffba2-112">Atlasiet Daudzums, ja vēlaties, lai atlīdzības punkti tiktu noapaļoti līdz tuvākajam veselam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="ffba2-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="ffba2-113">Atlasiet Summa, ja vēlaties, lai atlīdzības punkti tiktu noapaļoti atbilstoši valūtas noapaļošanas kārtulām.</span><span class="sxs-lookup"><span data-stu-id="ffba2-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="ffba2-114">Ja atlasīsiet Daudzums, izlaidiet nākamo šīs procedūras darbību.</span><span class="sxs-lookup"><span data-stu-id="ffba2-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="ffba2-115">Laukā Valūta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ffba2-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="ffba2-116">Summas veida atlīdzības punktu gadījumā visi izsniegtie punkti būs atlasītajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="ffba2-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="ffba2-117">Daudzuma veida atlīdzības punktu šis lauks netiks lietots — izlaidiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="ffba2-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="ffba2-118">Atzīmējiet izvēles rūtiņu Izpērkams vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="ffba2-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="ffba2-119">Laukā Izpirkšanas rangi ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ffba2-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="ffba2-120">Izpirkšanas rangi tiek izmantoti, ja divus vai vairāk izpērkamus atlīdzības punktus var izmantot, lai maksātu par precēm.</span><span class="sxs-lookup"><span data-stu-id="ffba2-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="ffba2-121">Ja diviem atlīdzības punktiem ir vienāds izpirkšanas rangs, tad tiks izmantots tas, kuram nepieciešams mazāks punktu skaits.</span><span class="sxs-lookup"><span data-stu-id="ffba2-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="ffba2-122">Laukā Termiņa beigu laika vērtība ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="ffba2-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="ffba2-123">Piešķirtajiem atlīdzības punktiem ir konkrēts derīguma termiņš dienās, mēnešos vai gados.</span><span class="sxs-lookup"><span data-stu-id="ffba2-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="ffba2-124">Vērtība '0' nozīmē to, ka lojalitātes programmas atlīdzības punktiem nav derīguma termiņa.</span><span class="sxs-lookup"><span data-stu-id="ffba2-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="ffba2-125">Laukā Termiņa beigu laika vienība atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ffba2-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="ffba2-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ffba2-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]