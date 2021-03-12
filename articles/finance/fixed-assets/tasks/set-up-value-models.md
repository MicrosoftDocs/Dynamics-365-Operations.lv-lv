---
title: Vērtības modeļu iestatīšana
description: Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grāmatu un sasaistīt to ar pamatlīdzekļu grupu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92c965775980d15e367b8cd5742d3bc61c3f698c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994794"
---
# <a name="set-up-value-models"></a><span data-ttu-id="34cb9-103">Vērtības modeļu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="34cb9-103">Set up value models</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34cb9-104">Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grāmatu un sasaistīt to ar pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="34cb9-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="34cb9-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="34cb9-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="34cb9-106">Izveidot grāmatu</span><span class="sxs-lookup"><span data-stu-id="34cb9-106">Create a book</span></span>
1. <span data-ttu-id="34cb9-107">Dodieties uz pamatlīdzekļi > Iestatījumi > Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="34cb9-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="34cb9-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="34cb9-108">Click New.</span></span>
3. <span data-ttu-id="34cb9-109">Laukā Grāmata, ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="34cb9-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="34cb9-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="34cb9-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="34cb9-111">Ja ir atlasīta iespēja Aprēķināt nolietojumu, saistīto pamatlīdzekļu grāmata tiks iekļauta nolietojuma priekšlikumos.</span><span class="sxs-lookup"><span data-stu-id="34cb9-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="34cb9-112">Ja tā nav atlasīta, pamatlīdzekļu grāmata netiks aprēķināta automātiski.</span><span class="sxs-lookup"><span data-stu-id="34cb9-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="34cb9-113">Atlasiet Jā laukā Aprēķināt nolietojumu.</span><span class="sxs-lookup"><span data-stu-id="34cb9-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="34cb9-114">Laukā Nolietojuma profils, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="34cb9-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="34cb9-115">Alternatīva nolietojuma metode ir zināma arī kā nolietojuma pārslēgšanas metode.</span><span class="sxs-lookup"><span data-stu-id="34cb9-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="34cb9-116">Nolietojuma priekšlikums pārslēgsies uz šo metodi, kad alternatīvās metodes aprēķinātā nolietojuma summa ir vienāda ar vai lielāka par noklusējuma nolietojuma metodes summu.</span><span class="sxs-lookup"><span data-stu-id="34cb9-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="34cb9-117">Ārkārtas nolietojuma metode tiem izmantota līdzekļa papildu nolietošanai neparastos apstākļos.</span><span class="sxs-lookup"><span data-stu-id="34cb9-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="34cb9-118">Piemēram, šo opciju varat izmantot, lai reģistrētu nolietojumu, ko izraisa dabas katastrofas.</span><span class="sxs-lookup"><span data-stu-id="34cb9-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="34cb9-119">Atlasot Izveidot nolietojuma korekcijas ar pamata pielāgojumiem, nolietojuma korekcijas tiks izveidotas automātiski atjauninot līdzekļa vērtību.</span><span class="sxs-lookup"><span data-stu-id="34cb9-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="34cb9-120">Ja tā nav atlasīta, atjauninātā līdzekļa vērtība ietekmēs tikai turpmākos nolietojuma aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="34cb9-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="34cb9-121">Atlasiet Jā, laukā Izveidot nolietojuma korekcijas ar pamata pielāgojumiem.</span><span class="sxs-lookup"><span data-stu-id="34cb9-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="34cb9-122">Pēc noklusējuma pamatlīdzekļa grāmatas darbības tiks grāmatotas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="34cb9-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="34cb9-123">Jūs varat atslēgt grāmatas grāmatošanu virsgrāmatā, iestatot lauku Grāmatot virsgrāmatā uz Nē.</span><span class="sxs-lookup"><span data-stu-id="34cb9-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="34cb9-124">Grāmatas, kas netiek grāmatotas virsgrāmatā parasti tiek izmantotas nodokļu pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="34cb9-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="34cb9-125">Tas dod jums papildu elastību vēsturisko darbības pamatlīdzekļu grāmatas dzēšanai, jo tie nav iekļauti virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="34cb9-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="34cb9-126">Grāmatošanas līmenis pēc noklusējuma ir Pašreizējais līmenis, ja tiek grāmatots virsgrāmatā, un Nav, ja to nevar grāmatot virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="34cb9-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="34cb9-127">Atjauniniet grāmatošanas līmeni, ja šīs grāmatas darbības nepieciešams grāmatot citā līmenī.</span><span class="sxs-lookup"><span data-stu-id="34cb9-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="34cb9-128">Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="34cb9-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="34cb9-129">Atvasinātās grāmatas var grāmatot darbības dažādās grāmatas vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="34cb9-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="34cb9-130">Jūs varat izveidot darbības, izmantojot primāro grāmatu, un grāmatošanas laikā, precīza darbības kopija tiek grāmatota atvasinātajā grāmatā.</span><span class="sxs-lookup"><span data-stu-id="34cb9-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="34cb9-131">Atvasinātās grāmatas darbībām nav nekādu pārrēķinu, tāpēc to nevajadzētu izmantot nolietojuma darbībās.</span><span class="sxs-lookup"><span data-stu-id="34cb9-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="34cb9-132">Saistīt grāmatu ar pamatlīdzekļu grupu</span><span class="sxs-lookup"><span data-stu-id="34cb9-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="34cb9-133">Noklikšķiniet uz Pamatlīdzekļu grupas.</span><span class="sxs-lookup"><span data-stu-id="34cb9-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="34cb9-134">Ievadiet vai atlasiet vērtību laukā Pamatlīdzekļu grupa.</span><span class="sxs-lookup"><span data-stu-id="34cb9-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="34cb9-135">Ievadiet skaitli laukā Lietošanas ilgums.</span><span class="sxs-lookup"><span data-stu-id="34cb9-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="34cb9-136">Ņemiet vērā, ka Nolietojuma periodi tiek aprēķināti pēc vērtības Lietošanas ilgums iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="34cb9-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="34cb9-137">Jūs varat arī iestatīt nolietojuma aprēķināšanas metodi, ja nepieciešams nodokļu vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="34cb9-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  

