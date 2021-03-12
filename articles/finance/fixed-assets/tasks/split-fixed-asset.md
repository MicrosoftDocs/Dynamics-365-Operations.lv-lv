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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75938e6fdf5fd8f10ac9719fc449a586c08d06b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975945"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="ed382-103">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="ed382-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed382-104">Šajā tēmā paskaidrots, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="ed382-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="ed382-105">Tas izmanto grāmatveža lomu un USMF demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="ed382-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="ed382-106">Izveidojiet jaunu pamatlīdzekli</span><span class="sxs-lookup"><span data-stu-id="ed382-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="ed382-107">Navigācijas rūtī dodieties uz **Moduļi \> Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="ed382-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="ed382-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ed382-108">Select **New**.</span></span>
3. <span data-ttu-id="ed382-109">Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="ed382-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="ed382-110">Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="ed382-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="ed382-111">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ed382-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="ed382-112">Aizveriet formu.</span><span class="sxs-lookup"><span data-stu-id="ed382-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="ed382-113">Pamatlīdzekļa sadalīšana</span><span class="sxs-lookup"><span data-stu-id="ed382-113">Split a fixed asset</span></span>

<span data-ttu-id="ed382-114">Pirms pilnībā nolietotā līdzekļa sadalīšanas, līdzekļa grāmatas statuss ir manuāli jāmaina no **Slēgts** uz **Atvērts**.</span><span class="sxs-lookup"><span data-stu-id="ed382-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="ed382-115">Šī darbība ir nepieciešama, jo grāmatas statusam jābūt **Atvērts**, ja ir jāgrāmato līdzekļu darbības (piemēram, izslēgšanas pārdošanai).</span><span class="sxs-lookup"><span data-stu-id="ed382-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="ed382-116">Ir jāieslēdz arī parametrs **Vairāku darījumu atļaušana vienā dokumentā** lapas **Virsgrāmatas parametri** cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="ed382-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="ed382-117">Pēc tam, kad līdzekļu grāmatošanas statuss ir mainīts un ir atļauti vairāki darījumi vienā dokumentā, veiciet tālāk norādītās darbības, lai sadalītu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="ed382-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="ed382-118">Sarakstā atrodiet un atlasiet sadalāmā pamatlīdzekļa saiti.</span><span class="sxs-lookup"><span data-stu-id="ed382-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="ed382-119">Atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="ed382-119">Select **Books**.</span></span> <span data-ttu-id="ed382-120">Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="ed382-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="ed382-121">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="ed382-121">Select **Functions**.</span></span>
4. <span data-ttu-id="ed382-122">Atlasiet **Pamatlīdzekļa sadalīšana**.</span><span class="sxs-lookup"><span data-stu-id="ed382-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="ed382-123">Laukā **Uz pamatlīdzekli**, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ed382-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="ed382-124">Laukā **Uz grāmatu** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ed382-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ed382-125">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="ed382-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="ed382-126">Ievadiet skaitli laukā **Procenti**.</span><span class="sxs-lookup"><span data-stu-id="ed382-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="ed382-127">Laukā **Žurnāla nosaukums**, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ed382-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="ed382-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ed382-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="ed382-129">Žurnāla transakcijas grāmatošana</span><span class="sxs-lookup"><span data-stu-id="ed382-129">Post the journal transaction</span></span>

1. <span data-ttu-id="ed382-130">Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Pamatlīdzekļi \> Žurnāla ieraksti \> Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="ed382-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="ed382-131">Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="ed382-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="ed382-132">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="ed382-132">Select **Lines**.</span></span>

    - <span data-ttu-id="ed382-133">Pārbaudiet izveidotās žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="ed382-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="ed382-134">Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="ed382-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="ed382-135">Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.</span><span class="sxs-lookup"><span data-stu-id="ed382-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="ed382-136">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="ed382-136">Select **Post**.</span></span>
