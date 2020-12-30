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
ms.openlocfilehash: da2dd4889a5f4722ff60a76a4a023c63fb59ad55
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514330"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="18219-103">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="18219-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18219-104">Šajā tēmā paskaidrots, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="18219-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="18219-105">Tas izmanto grāmatveža lomu un USMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="18219-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="18219-106">Izveidojiet jaunu pamatlīdzekli</span><span class="sxs-lookup"><span data-stu-id="18219-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="18219-107">Navigācijas rūtī dodieties uz **Moduļi \> Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="18219-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="18219-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="18219-108">Select **New**.</span></span>
3. <span data-ttu-id="18219-109">Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="18219-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="18219-110">Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="18219-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="18219-111">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="18219-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="18219-112">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="18219-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="18219-113">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="18219-113">Split a fixed asset</span></span>

<span data-ttu-id="18219-114">Pirms pilnībā nolietotā līdzekļa sadalīšanas, līdzekļa grāmatas statuss ir manuāli jāmaina no **Slēgts** uz **Atvērts**.</span><span class="sxs-lookup"><span data-stu-id="18219-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="18219-115">Šī darbība ir nepieciešama, jo grāmatas statusam jābūt **Atvērts**, ja ir jāgrāmato līdzekļu darbības (piemēram, izslēgšanas pārdošanai).</span><span class="sxs-lookup"><span data-stu-id="18219-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="18219-116">Ir jāieslēdz arī parametrs **Vairāku darījumu atļaušana vienā dokumentā** lapas **Virsgrāmatas parametri** cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="18219-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="18219-117">Pēc tam, kad līdzekļu grāmatošanas statuss ir mainīts un ir atļauti vairāki darījumi vienā dokumentā, veiciet tālāk norādītās darbības, lai sadalītu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="18219-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="18219-118">Sarakstā atrodiet un atlasiet sadalāmā pamatlīdzekļa saiti.</span><span class="sxs-lookup"><span data-stu-id="18219-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="18219-119">Atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="18219-119">Select **Books**.</span></span> <span data-ttu-id="18219-120">Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="18219-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="18219-121">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="18219-121">Select **Functions**.</span></span>
4. <span data-ttu-id="18219-122">Atlasiet **Pamatlīdzekļa sadalīšana**.</span><span class="sxs-lookup"><span data-stu-id="18219-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="18219-123">Laukā **Uz pamatlīdzekli**, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18219-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="18219-124">Laukā **Uz grāmatu** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="18219-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="18219-125">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="18219-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="18219-126">Ievadiet skaitli laukā **Procenti**.</span><span class="sxs-lookup"><span data-stu-id="18219-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="18219-127">Laukā **Žurnāla nosaukums**, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18219-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="18219-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="18219-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="18219-129">Žurnāla transakcijas grāmatošana</span><span class="sxs-lookup"><span data-stu-id="18219-129">Post the journal transaction</span></span>

1. <span data-ttu-id="18219-130">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Pamatlīdzekļi \> Žurnāla ieraksti \> Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="18219-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="18219-131">Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="18219-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="18219-132">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="18219-132">Select **Lines**.</span></span>

    - <span data-ttu-id="18219-133">Pārbaudiet izveidotās žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="18219-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="18219-134">Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="18219-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="18219-135">Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.</span><span class="sxs-lookup"><span data-stu-id="18219-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="18219-136">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="18219-136">Select **Post**.</span></span>
