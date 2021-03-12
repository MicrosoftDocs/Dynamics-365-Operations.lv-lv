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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c200f7f6ff0aa5672e50c539bfaa5e30213185
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003607"
---
# <a name="configure-a-worker"></a><span data-ttu-id="c8ddd-103"> Nodarbinātā konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c8ddd-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8ddd-104">Šajā procedūrā ir aprakstīts, kā konfigurēt darbinieku kā pārdošanas pārstāvi, kurš ir tiesīgs saņemt komisiju par pārdošanu, izmantojot POS.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="c8ddd-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="c8ddd-106">Izveidot darbinieka komisijas pārdošanas grupu</span><span class="sxs-lookup"><span data-stu-id="c8ddd-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="c8ddd-107">Pārejiet uz sadaļu Pārdošana un mārketings > Komisijas > Pārdošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="c8ddd-108">Darbiniekus var piešķirt vienai vai vairākām pārdošanas grupām.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="c8ddd-109">Izmantojot POS, var izvēlēties jebkuru pārdošanas grupu, kas ietver darbiniekus no veikala adrešu grāmatas.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="c8ddd-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-110">Click New.</span></span>
3. <span data-ttu-id="c8ddd-111">Laukā Grupa ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="c8ddd-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c8ddd-113">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-113">Click Save.</span></span>
6. <span data-ttu-id="c8ddd-114">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="c8ddd-115">Noklikšķiniet uz Pārdošanas pārstāvis.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-115">Click Sales rep.</span></span>
    * <span data-ttu-id="c8ddd-116">Pārdošanas grupa var ietvert vairāk nekā vienu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="c8ddd-117">Komisijas starp darbiniekiem var sadalīt atbilstoši komisijas daļu definējumam.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="c8ddd-118">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="c8ddd-119">Ievadiet skaitli laukā Komisijas daļas.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="c8ddd-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-120">Click Save.</span></span>
11. <span data-ttu-id="c8ddd-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-121">Close the page.</span></span>
12. <span data-ttu-id="c8ddd-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="c8ddd-123">Piešķirt darbinieku noklusējuma pārdošanas grupu</span><span class="sxs-lookup"><span data-stu-id="c8ddd-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="c8ddd-124">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Darbinieki > Darbinieki.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="c8ddd-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c8ddd-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c8ddd-127">Noklikšķiniet uz cilnes Komercija.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="c8ddd-128">Darbinieku var piešķirt noklusējuma pārdošanas grupai.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="c8ddd-129">Noklusējuma pārdošanas grupa tiks automātiski pievienota POS pārdošanas rindai, ja šī opcija ir iespējota veikala funkcionalitātes profilā.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="c8ddd-130">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-130">Click Edit.</span></span>
6. <span data-ttu-id="c8ddd-131">Ievadiet vai atlasiet vērtību laukā Noklusējuma grupa.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="c8ddd-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c8ddd-132">Click Save.</span></span>

