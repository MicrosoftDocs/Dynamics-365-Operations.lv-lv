---
title: "Pamatlīdzekļu nolietojums"
description: "Šajā tēmā ir sniegts pārskats par pamatlīdzekļu nolietojumu."
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a82e14e12cbde29e5619518481d0c22f6fa1a37a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="fixed-asset-depreciation"></a><span data-ttu-id="12d65-103">Pamatlīdzekļu nolietojums</span><span class="sxs-lookup"><span data-stu-id="12d65-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12d65-104">Šajā tēmā ir sniegts pārskats par pamatlīdzekļu nolietojumu.</span><span class="sxs-lookup"><span data-stu-id="12d65-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="12d65-105">Nolietojums ir periodiska darbība, kas parasti samazina pamatlīdzekļa vērtību bilancē un tiek maksāta kā izdevumi peļņas un zaudējumu kontā.</span><span class="sxs-lookup"><span data-stu-id="12d65-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="12d65-106">Tāpēc galvenais konts parasti tiek izmantots, lai kreditētu periodisko nolietojumu bilancē.</span><span class="sxs-lookup"><span data-stu-id="12d65-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="12d65-107">Korespondējošais konts ir konts kontu plāna peļņas un zaudējumu daļā.</span><span class="sxs-lookup"><span data-stu-id="12d65-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="12d65-108">Nolietojuma korekcijas</span><span class="sxs-lookup"><span data-stu-id="12d65-108">Depreciation adjustment</span></span>
<span data-ttu-id="12d65-109">Parasti tikai jau grāmatotas nolietojuma darbības korekcija tiek grāmatota kā nolietojuma korekcija.</span><span class="sxs-lookup"><span data-stu-id="12d65-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="12d65-110">Tāpēc gan galvenais konts, gan korespondējošais konts tiek iestatīts tāpat kā nolietojuma konts.</span><span class="sxs-lookup"><span data-stu-id="12d65-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="12d65-111">Nolietojuma korekcija var būt gan pozitīva summa, gan negatīva summa, taču galvenā konta (kā bilances konta) funkcionalitāte un korespondējošā konta (parasti kā peļņas un zaudējumu konta) funkcionalitāte paliek tā pati.</span><span class="sxs-lookup"><span data-stu-id="12d65-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="12d65-112">Ārkārtas nolietojums</span><span class="sxs-lookup"><span data-stu-id="12d65-112">Extraordinary depreciation</span></span>
<span data-ttu-id="12d65-113">Ārkārtas nolietojums darbojas tāpat kā pamata nolietojums.</span><span class="sxs-lookup"><span data-stu-id="12d65-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="12d65-114">Līdz ar to galvenais konts tiek izmantots, lai kreditētu nolietojuma summu bilancē un samazinot pamatlīdzekļa vērtību.</span><span class="sxs-lookup"><span data-stu-id="12d65-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="12d65-115">Korespondējošais konts ir peļņas un zaudējumu konts, kur nolietojums, kas tiek aprēķināts finanšu periodam, tiek apmaksāts kā izdevumi.</span><span class="sxs-lookup"><span data-stu-id="12d65-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="12d65-116">Ārkārtas nolietojums darbojas neatkarīgi no pamata nolietojuma.</span><span class="sxs-lookup"><span data-stu-id="12d65-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="12d65-117">Izmantojot ārkārtas nolietojumu kā atsevišķu darbības tipu, varat grāmatot un sniegt pārskatu par ārkārtas nolietojumu atsevišķi no pamata nolietojuma.</span><span class="sxs-lookup"><span data-stu-id="12d65-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="12d65-118">Speciālā nolietojuma atļautais daudzums</span><span class="sxs-lookup"><span data-stu-id="12d65-118">Special depreciation allowance</span></span>
<span data-ttu-id="12d65-119">Speciālā nolietojuma atļauto daudzumu var lietot, lai iegūtu papildnolietojuma summas pirmā gada laikā, kurā pamatlīdzeklis tiek nodots ekspluatācijā un nolietots.</span><span class="sxs-lookup"><span data-stu-id="12d65-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="12d65-120">Speciālā nolietojuma atļautais daudzums ir jāizmanto pirms pārējiem nolietojuma aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="12d65-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="12d65-121">Tā kā speciālā nolietojuma atļautais daudzums bieži vien kļūst zināms tikai pēc tam, kad pagājis noteikts pamatlīdzekļa lietošanas laiks, šo nolietojuma veidu ieteicams lietot ar grāmatu, kuras ieraksti netiek grāmatoti virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="12d65-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="12d65-122">Varat izmantot periodisko funkciju Dzēst virsgrāmatā negrāmatotās transakcijas, lai dzēstu šīm grāmatām darbību vēsturi.</span><span class="sxs-lookup"><span data-stu-id="12d65-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="12d65-123">Pēc tam varat dzēst nolietojuma vēsturi pamatlīdzekļu grāmatai, grāmatot speciālā nolietojuma atļauto daudzumu, kad tas ir zināms, un pēc tam grāmatot atlikušās nolietojuma darbības par attiecīgo gadu.</span><span class="sxs-lookup"><span data-stu-id="12d65-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="12d65-124">Var izveidot neierobežotu speciālā nolietojuma atļautā daudzuma ierakstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="12d65-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="12d65-125">Pēc šo ierakstu piešķiršanas līdzekļu grupas grāmatai tie tiek lietoti attiecīgajai līdzekļu grāmatai.</span><span class="sxs-lookup"><span data-stu-id="12d65-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="12d65-126">Speciālā nolietojuma atļautais daudzums tiek ievadīts kā procenti vai fiksēta summa.</span><span class="sxs-lookup"><span data-stu-id="12d65-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="12d65-127">Grāmatojot nolietojuma priekšlikumus, speciālā nolietojuma atļautā daudzuma darbības tiek grāmatotas grāmatā kā darbības, kas ir atsevišķi no nolietojuma darbībām.</span><span class="sxs-lookup"><span data-stu-id="12d65-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="12d65-128"> Nolietojuma kalendāri</span><span class="sxs-lookup"><span data-stu-id="12d65-128">Depreciation calendars</span></span>
<span data-ttu-id="12d65-129">Katrai grāmatai ir kalendārs, ko izmanto, aprēķinot pamatlīdzekļu nolietojumu.</span><span class="sxs-lookup"><span data-stu-id="12d65-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="12d65-130">Pēc noklusējuma, ja nenorādīsiet kalendāru grāmatai, grāmata izmantos virsgrāmatas finanšu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="12d65-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="12d65-131">Nepieciešams atlasīt finanšu kalendāru grāmatai, ja ar grāmatu saistītais nolietojuma profils izmanto finanšu nolietojuma gadu.</span><span class="sxs-lookup"><span data-stu-id="12d65-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="12d65-132">Varat izveidot koplietojamu kalendāru, izmantojot sadaļas Virsgrāmata lapu **Finanšu kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="12d65-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="12d65-133">Papildinformāciju skatiet rakstā [Nolietojuma metodes un konvencijas](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="12d65-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>




