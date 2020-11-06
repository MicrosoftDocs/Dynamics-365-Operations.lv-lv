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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000297"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="30656-103">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="30656-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30656-104">Šajā tēmā paskaidrots, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="30656-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="30656-105">Tas izmanto grāmatveža lomu un USMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="30656-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="30656-106">Izveidojiet jaunu pamatlīdzekli</span><span class="sxs-lookup"><span data-stu-id="30656-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="30656-107">Navigācijas rūtī dodieties uz **Moduļi \> Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="30656-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="30656-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="30656-108">Select **New**.</span></span>
3. <span data-ttu-id="30656-109">Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="30656-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="30656-110">Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="30656-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="30656-111">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="30656-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="30656-112">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="30656-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="30656-113">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="30656-113">Split a fixed asset</span></span>

<span data-ttu-id="30656-114">Pirms pilnībā nolietotā līdzekļa sadalīšanas, līdzekļa grāmatas statuss ir manuāli jāmaina no **Slēgts** uz **Atvērts**.</span><span class="sxs-lookup"><span data-stu-id="30656-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="30656-115">Šī darbība ir nepieciešama, jo grāmatas statusam jābūt **Atvērts** , ja ir jāgrāmato līdzekļu darbības (piemēram, izslēgšanas pārdošanai).</span><span class="sxs-lookup"><span data-stu-id="30656-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="30656-116">Kad līdzekļa grāmatas statuss ir mainīts, veiciet tālāk minētās darbības, lai sadalītu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="30656-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="30656-117">Sarakstā atrodiet un atlasiet sadalāmā pamatlīdzekļa saiti.</span><span class="sxs-lookup"><span data-stu-id="30656-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="30656-118">Atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="30656-118">Select **Books**.</span></span> <span data-ttu-id="30656-119">Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="30656-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="30656-120">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="30656-120">Select **Functions**.</span></span>
4. <span data-ttu-id="30656-121">Atlasiet **Pamatlīdzekļa sadalīšana**.</span><span class="sxs-lookup"><span data-stu-id="30656-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="30656-122">Laukā **Uz pamatlīdzekli** , ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="30656-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="30656-123">Laukā **Uz grāmatu** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="30656-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="30656-124">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="30656-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="30656-125">Ievadiet skaitli laukā **Procenti**.</span><span class="sxs-lookup"><span data-stu-id="30656-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="30656-126">Laukā **Žurnāla nosaukums** , ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="30656-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="30656-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="30656-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="30656-128">Žurnāla transakcijas grāmatošana</span><span class="sxs-lookup"><span data-stu-id="30656-128">Post the journal transaction</span></span>

1. <span data-ttu-id="30656-129">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Pamatlīdzekļi \> Žurnāla ieraksti \> Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="30656-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="30656-130">Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="30656-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="30656-131">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="30656-131">Select **Lines**.</span></span>

    - <span data-ttu-id="30656-132">Pārbaudiet izveidotās žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="30656-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="30656-133">Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="30656-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="30656-134">Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.</span><span class="sxs-lookup"><span data-stu-id="30656-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="30656-135">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="30656-135">Select **Post**.</span></span>
