---
title: Pamatlīdzekļa iegādes priekšlikums
description: Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817173"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="0b026-103">Pamatlīdzekļa iegādes priekšlikums</span><span class="sxs-lookup"><span data-stu-id="0b026-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b026-104">Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="0b026-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="0b026-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="0b026-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="0b026-106">Lai iegūtu pamatlīdzekli, izmantojot pamatlīdzekļu priekšlikumu žurnālu, vispirms ir jāizveido pamatlīdzekļa ieraksts un pēc tam jādefinē iegādes cena pamatlīdzekļu grāmatā.</span><span class="sxs-lookup"><span data-stu-id="0b026-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="0b026-107">Līdzekļa iegādes priekšlikuma izveide</span><span class="sxs-lookup"><span data-stu-id="0b026-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="0b026-108">Lai izveidotu līdzekļa iegādes priekšlikumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0b026-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="0b026-109">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0b026-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="0b026-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0b026-110">Select **New**.</span></span>
3. <span data-ttu-id="0b026-111">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="0b026-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="0b026-112">Darbību rūtī atlasiet **Rindiņas**.</span><span class="sxs-lookup"><span data-stu-id="0b026-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="0b026-113">Atlasiet **Priekšlikumi**.</span><span class="sxs-lookup"><span data-stu-id="0b026-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="0b026-114">Atlasiet **Iegādes priekšlikums**.</span><span class="sxs-lookup"><span data-stu-id="0b026-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="0b026-115">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="0b026-115">Select **Filter**.</span></span> <span data-ttu-id="0b026-116">Atlasiet **Atiestatīt**, lai notīrītu iepriekšējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="0b026-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="0b026-117">Atlasiet rindu **Pamatlīdzekļa numurs**.</span><span class="sxs-lookup"><span data-stu-id="0b026-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="0b026-118">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="0b026-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="0b026-119">Iestatiet atlikušos kritērijus pamatlīdzekļiem, kurus vēlaties iegūt, izmantojot šo priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="0b026-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="0b026-120">Atlasiet **Labi** divas reizes, lai izietu no rūts.</span><span class="sxs-lookup"><span data-stu-id="0b026-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="0b026-121">Pārbaudiet vai ir izveidotās transakcijas rindas.</span><span class="sxs-lookup"><span data-stu-id="0b026-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="0b026-122">Tikai pamatlīdzekļi ar iegādes datumu un iegādes cenu, kas ir iestatīta grāmatā, tiks iekļauti iegādes priekšlikumā.</span><span class="sxs-lookup"><span data-stu-id="0b026-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="0b026-123">Lapā atlasiet cilni **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="0b026-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="0b026-124">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="0b026-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="0b026-125">Pirkšanas priekšlikumā iekļaut noklusējuma finanšu dimensijas</span><span class="sxs-lookup"><span data-stu-id="0b026-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="0b026-126">Iegādes darījumu var izveidot, izmantojot Excel pievienojumprogrammas, noklikšķinot uz **Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="0b026-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="0b026-127">Izveidojiet jaunu žurnālu un pārvietojieties uz lapas sadaļu **Rindas** un atlasiet Excel ikonu un pēc tam atlasiet pamatlīdzekļu žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="0b026-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="0b026-128">Sistēma izveidos un atvērs Excel veidni, kas atspoguļo žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="0b026-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="0b026-129">Varat pievienot datus žurnāla rindām, ko pievienojat veidnei, un pēc tam publicēt šo informāciju atpakaļ sistēmā.</span><span class="sxs-lookup"><span data-stu-id="0b026-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="0b026-130">Ja atlasītajai līdzekļu grāmatai un atbilstošajiem pamatlīdzekļiem, kas tika ievadīti Excel veidnē, noklusējuma dimensijas tiks izsauktas no līdzekļu grāmatas pamatdatiem, kad žurnāls ir publicēts sistēmā Excel.</span><span class="sxs-lookup"><span data-stu-id="0b026-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="0b026-131">Lai līdzekļu grāmatā automātiski iekļautu finanšu dimensijas, publicējot pamatlīdzekļu žurnālu no Excel pievienojumprogrammas, iepriekš jāiestata noklusējuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0b026-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
