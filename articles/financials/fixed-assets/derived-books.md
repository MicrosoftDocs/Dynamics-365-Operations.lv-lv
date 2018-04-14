---
title: "Atvasinātās grāmatas"
description: "Šajā rakstā ir sniegts pārskats par atvasināto grāmatu funkcionalitāti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 23b17c577fd2e0dfa6183929c86ed1950db8c50b
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="derived-books"></a><span data-ttu-id="812be-103">Atvasinātās grāmatas</span><span class="sxs-lookup"><span data-stu-id="812be-103">Derived books</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="812be-104">Šajā rakstā ir sniegts pārskats par atvasināto grāmatu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="812be-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="812be-105">Atvasināto grāmatu mērķis ir vienkāršot regulāriem intervāliem plānotu pamatlīdzekļu grāmatu transakciju grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="812be-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="812be-106">Izvēlieties vienu grāmatu kā primāro grāmatu.</span><span class="sxs-lookup"><span data-stu-id="812be-106">You choose one book as the primary book.</span></span> <span data-ttu-id="812be-107">Tā parasti ir grāmata, ko izmanto grāmatvedības nolietojumam.</span><span class="sxs-lookup"><span data-stu-id="812be-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="812be-108">Pēc tam šim modelim tiek pievienotas citas grāmatas, kas ir iestatītas darbību grāmatošanai tādos pašos intervālos kā noteikti primārajā grāmatā.</span><span class="sxs-lookup"><span data-stu-id="812be-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="812be-109">PVN nolietojuma grāmatas bieži tiek iestatītas kā atvasinātās grāmatas.</span><span class="sxs-lookup"><span data-stu-id="812be-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="812be-110">Izplatītākās iestatāmās darbības iegrāmatošanai uz atvasinātajām grāmatām ir iegādes, iegādes pielāgojumi un izslēgšanas.</span><span class="sxs-lookup"><span data-stu-id="812be-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="812be-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="812be-111">Example</span></span>

<span data-ttu-id="812be-112">Grāmata B un grāmata C ir iestatītas kā atvasinātās grāmatas grāmatai A darbību tipam Iegāde.</span><span class="sxs-lookup"><span data-stu-id="812be-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="812be-113">Grāmatā A ievadiet pamatlīdzekļa 123 iegādes darbību par summu 1500,00.</span><span class="sxs-lookup"><span data-stu-id="812be-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="812be-114">Kad darbība ir iegrāmatota, grāmatas B pamatlīdzeklim 123 un grāmatas C pamatlīdzeklim 123 tiek ģenerēta un iegrāmatota iegādes darbība par summu 1500,00.</span><span class="sxs-lookup"><span data-stu-id="812be-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="812be-115">Kad tiek sagatavotas primārās grāmatas darbības pamatlīdzekļu žurnālā, ir iespējams arī apskatīt un rediģēt atvasināto grāmatu darbības.</span><span class="sxs-lookup"><span data-stu-id="812be-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="812be-116">Ja primārās grāmatas darbības tiek sagatavotas citā žurnālā, atvasināto vērtību darbības netiek parādītas.</span><span class="sxs-lookup"><span data-stu-id="812be-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="812be-117">Tomēr, kad primārās grāmatas darbības ir iegrāmatotas, tās tiek iegrāmatotas atbilstošajos kontos un grāmatošanas līmeņos.</span><span class="sxs-lookup"><span data-stu-id="812be-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="812be-118">Grāmatas, kas iestatītas, lai grāmatotu darbības intervālos, kas atšķiras no primārās grāmatas intervāliem, jāpievieno pamatlīdzeklim kā atsevišķas grāmatas, nevis kā atvasinātas grāmatas.</span><span class="sxs-lookup"><span data-stu-id="812be-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="812be-119">Papildu informāciju skatiet rakstā [Grāmatošana ar atvasinātām grāmatām](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="812be-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




