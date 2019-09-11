---
title: Pamatlīdzekļa sadalīšana
description: Šajā tēmā paskaidrots, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867587"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="ef488-103">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="ef488-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef488-104">Šajā tēmā paskaidrots, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="ef488-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="ef488-105">Tas izmanto grāmatveža lomu un USMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="ef488-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="ef488-106">Izveidojiet jaunu pamatlīdzekli</span><span class="sxs-lookup"><span data-stu-id="ef488-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="ef488-107">Navigācijas rūtī ejiet uz **Moduļi > Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="ef488-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="ef488-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ef488-108">Select **New**.</span></span>
3. <span data-ttu-id="ef488-109">Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="ef488-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="ef488-110">Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="ef488-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="ef488-111">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ef488-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ef488-112">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="ef488-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="ef488-113">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="ef488-113">Split a fixed asset</span></span>
1. <span data-ttu-id="ef488-114">Sarakstā atrodiet un atlasiet sadalāmā pamatlīdzekļa saiti.</span><span class="sxs-lookup"><span data-stu-id="ef488-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="ef488-115">Atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="ef488-115">Select **Books**.</span></span> <span data-ttu-id="ef488-116">Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="ef488-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="ef488-117">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="ef488-117">Select **Functions**.</span></span>
4. <span data-ttu-id="ef488-118">Atlasiet **Pamatlīdzekļa sadalīšana**.</span><span class="sxs-lookup"><span data-stu-id="ef488-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="ef488-119">Laukā **Uz pamatlīdzekli**, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ef488-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="ef488-120">Laukā **Uz grāmatu** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ef488-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ef488-121">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="ef488-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="ef488-122">Ievadiet skaitli laukā **Procenti**.</span><span class="sxs-lookup"><span data-stu-id="ef488-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="ef488-123">Laukā **Žurnāla nosaukums**, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ef488-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="ef488-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ef488-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="ef488-125">Žurnāla transakcijas grāmatošana</span><span class="sxs-lookup"><span data-stu-id="ef488-125">Post the journal transaction</span></span>
1. <span data-ttu-id="ef488-126">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="ef488-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ef488-127">Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="ef488-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="ef488-128">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="ef488-128">Select **Lines**.</span></span>

    - <span data-ttu-id="ef488-129">Pārbaudiet izveidotās žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="ef488-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="ef488-130">Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="ef488-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="ef488-131">Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.</span><span class="sxs-lookup"><span data-stu-id="ef488-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="ef488-132">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="ef488-132">Select **Post**.</span></span>

