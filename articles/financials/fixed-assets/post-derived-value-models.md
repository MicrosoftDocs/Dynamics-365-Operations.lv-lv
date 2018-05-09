---
title: "Grāmatošana, izmantojot atvasinātās grāmatas"
description: "Šajā rakstā ir aprakstīts, kā izmantot atvasinātās grāmatas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 463c43f9960a21ab88da92febaa9a65e370326e8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="post-with-derived-books"></a><span data-ttu-id="680e5-103">Grāmatošana, izmantojot atvasinātās grāmatas</span><span class="sxs-lookup"><span data-stu-id="680e5-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="680e5-104">Šajā rakstā ir aprakstīts, kā izmantot atvasinātās grāmatas.</span><span class="sxs-lookup"><span data-stu-id="680e5-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="680e5-105">Grāmatojot darbības grāmatai, kurā iekļautas atvasinātās grāmatas, atvasināto grāmatu darbības tiek automātiski grāmatotas žurnālos, pirkšanas pasūtījumos vai brīva teksta rēķinos.</span><span class="sxs-lookup"><span data-stu-id="680e5-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="680e5-106">Tomēr, sagatavojot primārās grāmatas darbības žurnālā Pamatlīdzekļi, atvasināto darbību summas var skatīt un modificēt pirms to grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="680e5-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="680e5-107">Noteikti konti, piemēram, PVN un debitoru vai kreditoru konti, tiek atjaunināti tikai vienreiz ar primārās grāmatas grāmatojumiem.</span><span class="sxs-lookup"><span data-stu-id="680e5-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="680e5-108">Atvasinātās grāmatas darbības tiek grāmatotas kontos, kas definēti atvasinātajai grāmatai lapā Pamatlīdzekļu grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="680e5-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="680e5-109">Iegāde bieži tiek lietota kā atvasināto grāmatu darbības tips.</span><span class="sxs-lookup"><span data-stu-id="680e5-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="680e5-110">To lieto, ja pamatlīdzeklim nepieciešams pielietot grāmatu un atvasināto grāmatu, sākot no pamatlīdzekļa iegādes datuma.</span><span class="sxs-lookup"><span data-stu-id="680e5-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="680e5-111">Uz darbības tipu var attiekties arī citas vērtības.</span><span class="sxs-lookup"><span data-stu-id="680e5-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="680e5-112">Piemēram, ja primārajai grāmatai un atvasinātajām grāmatām ir vienādi pārdošanas vai izslēgšanas intervāli, visi pamatlīdzekļu darbību tipi ir pieejami atvasinātās grāmatas iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="680e5-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="680e5-113">Atvasinātajā grāmatā iegrāmatotā nolietojuma summa ir tāda pati kā primārajā grāmatā iegrāmatotā summa.</span><span class="sxs-lookup"><span data-stu-id="680e5-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="680e5-114">Ja nolietojuma metodes atšķiras starp grāmatām, nedrīkst ģenerēt nolietojuma darbības, lietojot atvasinātu procesu.</span><span class="sxs-lookup"><span data-stu-id="680e5-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="680e5-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="680e5-115">Example</span></span> 
<span data-ttu-id="680e5-116">Tālāk sniegtajā informācijā ir aprakstīts, kā iestatīt iegādes darbības, izmantojot atvasinātās grāmatas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="680e5-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="680e5-117">Izveidojiet grāmatas lapā Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="680e5-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="680e5-118">Grāmata uzskaitei: 1. VM, pašreizējais grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="680e5-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="680e5-119">Grāmata nodokļu aprēķinam: 2. VM, nodokļu grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="680e5-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="680e5-120">1. VM noklikšķiniet uz cilnes Atvasinātās grāmatas. Laukā Grāmata atlasiet 2. VM un laukā Transakcijas tips atlasiet Iegāde.</span><span class="sxs-lookup"><span data-stu-id="680e5-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="680e5-121">Pēc tam grāmatas var pievienot specifiskiem pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="680e5-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="680e5-122">Grāmatojot pamatlīdzekļa iegādi, izmantojot grāmatu 1. VM, iegāde tiek grāmatota ne tikai grāmatā 1. VM, bet arī atvasinātajā grāmatā 2. VM.</span><span class="sxs-lookup"><span data-stu-id="680e5-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="680e5-123">Abu pamatlīdzekļu grāmatu statuss tiek mainīts uz Atvērts.</span><span class="sxs-lookup"><span data-stu-id="680e5-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="680e5-124">Ja atvasinātās grāmatas netiek lietotas, pamatlīdzekļa iegāde jāgrāmato gan grāmatai 1. VM, gan grāmatai 2. VM.</span><span class="sxs-lookup"><span data-stu-id="680e5-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="680e5-125">Papildu informāciju skatiet tēmā [Atvasinātās grāmatas](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="680e5-125">For more information, see [Derived books](derived-books.md)</span></span>




