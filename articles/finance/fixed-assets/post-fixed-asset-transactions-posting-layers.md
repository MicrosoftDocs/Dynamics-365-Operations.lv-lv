---
title: Pamatlīdzekļu transakciju grāmatošana grāmatošanas līmeņos
description: Šajā rakstā ir sniegts pārskats par pamatlīdzekļu transakciju grāmatošanas līmeņa funkcionalitāti.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770716"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="94c7c-103">Pamatlīdzekļu transakciju grāmatošana grāmatošanas līmeņos</span><span class="sxs-lookup"><span data-stu-id="94c7c-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94c7c-104">Šajā rakstā ir sniegts pārskats par pamatlīdzekļu transakciju grāmatošanas līmeņa funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="94c7c-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="94c7c-105">Pamatlīdzeklis bieži tiek nolietots dažādos veidos dažādiem nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="94c7c-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="94c7c-106">Nolietojums nodokļu nolūkiem tiek aprēķināts, izmantojot pašreizējos nodokļu nosacījumus, lai sasniegtu visaugstāko iespējamo nolietojumu pirms nodokļiem, bet nolietojums pārskata nolūkos tiek aprēķināts atbilstīgi uzskaites noteikumiem un standartiem.</span><span class="sxs-lookup"><span data-stu-id="94c7c-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="94c7c-107">Dažādi nolietojuma veidi tiek aprēķināti un ierakstīti atsevišķi grāmatošanas līmeņos.</span><span class="sxs-lookup"><span data-stu-id="94c7c-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="94c7c-108">Katra pamatlīdzeklim piesaistītā grāmata ir iestatīta noteiktam grāmatošanas līmenim, kuram ir vispārējā nolietojuma mērķis.</span><span class="sxs-lookup"><span data-stu-id="94c7c-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="94c7c-109">Ir desmit grāmatošanas līmeņi: Pašreizējais, Operācijas, Nodokļi un septiņi līmeņi, kuru tips ir Pielāgots.</span><span class="sxs-lookup"><span data-stu-id="94c7c-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="94c7c-110">Jūs varat arī atslēgt grāmatas grāmatošanu virsgrāmatā, iestatot laukam Grāmatot virsgrāmatā opciju Nē.</span><span class="sxs-lookup"><span data-stu-id="94c7c-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="94c7c-111">Pēc tam laukam Grāmatošanas līmenis tiek automātiski iestatīta opcija Nav.</span><span class="sxs-lookup"><span data-stu-id="94c7c-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="94c7c-112">Parasti grāmatas, kas netiek grāmatotas Virsgrāmatā, tiek izmantotas nodokļu pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="94c7c-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="94c7c-113">Šī pieeja sniedz papildu pielāgojamības iespējas pamatlīdzekļu grāmatas vēsturisko transakciju dzēšanai, jo tās nav iekļautas Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="94c7c-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="94c7c-114">Pamatlīdzekļu žurnāli tiek definēti, izmantojot lapu Žurnālu nosaukumi sadaļā Virsgrāmata > Žurnāla iestatījumi > Žurnālu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="94c7c-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="94c7c-115">Katrs žurnāls, kur varat grāmatot nolietojumu, tiek definēts pēc žurnāla nosaukuma tikai vienā grāmatošanas līmenī.</span><span class="sxs-lookup"><span data-stu-id="94c7c-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="94c7c-116">Grāmatošanas līmeni žurnālā nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="94c7c-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="94c7c-117">Šis ierobežojums palīdz nodrošināt, ka katra grāmatošanas līmeņa darbības atrodas atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="94c7c-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="94c7c-118">Katram grāmatošanas līmenim jāizveido vismaz viens žurnāla nosaukums.</span><span class="sxs-lookup"><span data-stu-id="94c7c-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="94c7c-119">Ja izmantojat grāmatas, kas netiek grāmatotas Virsgrāmatā, ir jāizveido arī žurnāls, kura grāmatošanas līmenim ir iestatīta opcija Nav.</span><span class="sxs-lookup"><span data-stu-id="94c7c-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="94c7c-120">Varat norādīt virsgrāmatas kontus pamatlīdzekļu darbībām lapā Pamatlīdzekļu grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="94c7c-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="94c7c-121">Katrai grāmatošanas metodei jāatlasa atbilstīgs darbības tips un grāmata un pēc tam jāpiešķir virsgrāmatas konti.</span><span class="sxs-lookup"><span data-stu-id="94c7c-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="94c7c-122">Iestatiet grāmatošanas metodes ierakstu katrai grāmatai, kas tiek grāmatota virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="94c7c-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="94c7c-123">Izmantojot atvasinātās grāmatas, varat vienlaikus grāmatot transakcijas dažādos grāmatošanas līmeņos.</span><span class="sxs-lookup"><span data-stu-id="94c7c-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="94c7c-124">Izveidojiet primārās grāmatas darbības žurnālā, kura grāmatošanas līmenis atbilst grāmatas grāmatošanas līmenim.</span><span class="sxs-lookup"><span data-stu-id="94c7c-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="94c7c-125">Grāmatošanas laikā atvasinātās grāmatas darbības tiek grāmatotas atbilstīgajos grāmatošanas līmeņos.</span><span class="sxs-lookup"><span data-stu-id="94c7c-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="94c7c-126">Papildinformāciju skatiet [Atvasinātās grāmatas](derived-books.md) un [Grāmatošana, izmantojot atvasinātās grāmatas](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="94c7c-126">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



