---
title: " Nodarbinātā konfigurēšana"
description: Šajā procedūrā ir aprakstīts, kā konfigurēt darbinieku kā pārdošanas pārstāvi, kurš ir tiesīgs saņemt komisiju par pārdošanu, izmantojot POS.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aee84f2dc39d2225985992fac0f9c20985ed9804
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023261"
---
# <a name="configure-a-worker"></a><span data-ttu-id="371e0-103"> Nodarbinātā konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="371e0-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="371e0-104">Šajā procedūrā ir aprakstīts, kā konfigurēt darbinieku kā pārdošanas pārstāvi, kurš ir tiesīgs saņemt komisiju par pārdošanu, izmantojot POS.</span><span class="sxs-lookup"><span data-stu-id="371e0-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="371e0-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="371e0-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="371e0-106">Izveidot darbinieka komisijas pārdošanas grupu</span><span class="sxs-lookup"><span data-stu-id="371e0-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="371e0-107">Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Pārdošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="371e0-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="371e0-108">Darbiniekus var piešķirt vienai vai vairākām pārdošanas grupām.</span><span class="sxs-lookup"><span data-stu-id="371e0-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="371e0-109">Izmantojot POS, var izvēlēties jebkuru pārdošanas grupu, kas ietver darbiniekus no veikala adrešu grāmatas.</span><span class="sxs-lookup"><span data-stu-id="371e0-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="371e0-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="371e0-110">Click New.</span></span>
3. <span data-ttu-id="371e0-111">Laukā Grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="371e0-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="371e0-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="371e0-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="371e0-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="371e0-113">Click Save.</span></span>
6. <span data-ttu-id="371e0-114">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="371e0-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="371e0-115">Noklikšķiniet uz Pārdošanas pārstāvis.</span><span class="sxs-lookup"><span data-stu-id="371e0-115">Click Sales rep.</span></span>
    * <span data-ttu-id="371e0-116">Pārdošanas grupa var ietvert vairāk nekā vienu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="371e0-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="371e0-117">Komisijas starp darbiniekiem var sadalīt atbilstoši komisijas daļu definējumam.</span><span class="sxs-lookup"><span data-stu-id="371e0-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="371e0-118">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="371e0-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="371e0-119">Ievadiet skaitli laukā Komisijas daļas.</span><span class="sxs-lookup"><span data-stu-id="371e0-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="371e0-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="371e0-120">Click Save.</span></span>
11. <span data-ttu-id="371e0-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="371e0-121">Close the page.</span></span>
12. <span data-ttu-id="371e0-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="371e0-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="371e0-123">Piešķirt darbinieku noklusējuma pārdošanas grupu</span><span class="sxs-lookup"><span data-stu-id="371e0-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="371e0-124">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Darbinieki > Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="371e0-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="371e0-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="371e0-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="371e0-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="371e0-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="371e0-127">Noklikšķiniet uz cilnes Komercija.</span><span class="sxs-lookup"><span data-stu-id="371e0-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="371e0-128">Darbinieku var piešķirt noklusējuma pārdošanas grupai.</span><span class="sxs-lookup"><span data-stu-id="371e0-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="371e0-129">Noklusējuma pārdošanas grupa tiks automātiski pievienota POS pārdošanas rindai, ja šī opcija ir iespējota veikala funkcionalitātes profilā.</span><span class="sxs-lookup"><span data-stu-id="371e0-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="371e0-130">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="371e0-130">Click Edit.</span></span>
6. <span data-ttu-id="371e0-131">Ievadiet vai atlasiet vērtību laukā Noklusējuma grupa.</span><span class="sxs-lookup"><span data-stu-id="371e0-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="371e0-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="371e0-132">Click Save.</span></span>
