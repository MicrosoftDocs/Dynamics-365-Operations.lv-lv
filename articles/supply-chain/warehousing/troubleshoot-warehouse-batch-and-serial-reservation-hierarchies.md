---
title: Problēmu novēršana saistībā ar noliktavu partiju un sēriju rezervācijas hierarhijām
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu rezervāciju hierarhijām, kas izmanto partijas vai sēriju dimensijas.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838182"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="5d09d-103">Problēmu novēršana saistībā ar noliktavu partiju un sēriju rezervācijas hierarhijām</span><span class="sxs-lookup"><span data-stu-id="5d09d-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d09d-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu rezervāciju hierarhijām, kas izmanto partijas vai sēriju dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5d09d-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="5d09d-105">Papildu informāciju skatiet [Elastīga noliktavas līmeņa dimensijas rezervēšanas politika](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="5d09d-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="5d09d-106">Krājuma rezervāciju hierarhija nosaka noliktavas dimensiju vajadzību, kas ir jāizpilda, lai pieprasījuma pasūtījumam piešķirtu vietu.</span><span class="sxs-lookup"><span data-stu-id="5d09d-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="5d09d-107">Šīs dimensijas var aprakstīt kā *dimensijas virs novietojuma*, visām dimensijām, kas jāizpilda pirms novietojuma piešķiršanas, un *dimensijām zem novietojuma*, dimensijām, ko var piešķirt pēc vietas piešķiršanas pieprasījuma pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="5d09d-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="5d09d-108">Šīs rezervāciju hierarhijas tiek sauktas arī par *pakešuzdevumu, kas atrodas augstāk* un *atrodas zem* rezervāciju hierarhijām, vai arī rezervāciju hierarhijas, kas atrodas *augstāk par sēriju* un pārsniedz *sērijas numuru zem* rezervāciju hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="5d09d-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="5d09d-109">Krājumus var sekmīgi sadalīt tikai tad, ja dimensijās virs novietojuma nav atstarpju.</span><span class="sxs-lookup"><span data-stu-id="5d09d-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="5d09d-110">Piemēram, *paketē virs* rezervāciju hierarhijas jūs sagaidāt, ka pieprasījuma pasūtījumā tiks norādīta **Vieta**, **Noliktava** un **Partijas numura** dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5d09d-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="5d09d-111">Ja kāda no šīm dimensijām trūkst, sadalījuma process neizdosies.</span><span class="sxs-lookup"><span data-stu-id="5d09d-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="5d09d-112">Pretēji, pakešveida rezervācijas hierarhijā, kas atrodas *zem paketes* vai *zem sērijas*, pieprasījuma pasūtījumā var norādīt paketes vai sērijas numuru, bet sadalījuma procesam tā nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="5d09d-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="5d09d-113">Tiek parādīts šāds kļūdas ziņojums: "Jāpiešķir kopumam, noslodzes rindām ir jānorāda dimensijas virs novietojuma.</span><span class="sxs-lookup"><span data-stu-id="5d09d-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="5d09d-114">Lai piešķirtu šīs dimensijas, rezervējiet un atkārtoti izveidojiet noslodzes rindu."</span><span class="sxs-lookup"><span data-stu-id="5d09d-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d09d-115">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5d09d-115">Issue description</span></span>

<span data-ttu-id="5d09d-116">Kad izmantojat krājumu, kam ir *partija virs* rezervāciju hierarhija (ar Partijas numura dimensiju, kas novietota virs Novietojuma dimensijas), **Izlaist uz noliktavu** komanda lapā **Kravas plānošanas rīks** daļējam daudzumam nestrādā.</span><span class="sxs-lookup"><span data-stu-id="5d09d-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="5d09d-117">Šis kļūdas ziņojums tiek parādīts, un nav izveidots neviens darbs daļējam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="5d09d-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="5d09d-118">Tomēr, ja izmantojat krājumu, kam ir *partija zem* rezervāciju hierarhija (ar Partijas numura dimensiju, kas novietota zem Novietojuma dimensijas), varat izlaist kravu no lapas **Kravas plānošanas rīks** daļējam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="5d09d-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="5d09d-119">Izsniegšanas iemesls</span><span class="sxs-lookup"><span data-stu-id="5d09d-119">Issue cause</span></span>

<span data-ttu-id="5d09d-120">Ja jūs ievietojat dimensiju virs **Novietojuma** dimensijas rezervāciju hierarhijā, tas ir jānorāda pirms izdošanas uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5d09d-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="5d09d-121">Daļējus daudzumus nevar izlaist, ja nav norādīta viena vai vairākas dimensijas virs **Novietojuma**.</span><span class="sxs-lookup"><span data-stu-id="5d09d-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="5d09d-122">Partijas numura automātiskās rezervēšanas uzvedne tiek izraisīta pat tad, ja ir pieejami krājumi.</span><span class="sxs-lookup"><span data-stu-id="5d09d-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d09d-123">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5d09d-123">Issue description</span></span>

<span data-ttu-id="5d09d-124">Izmantojot krājumu, kam noliktavā nav iespējoti noliktavas procesi un ir iespējota automātiska rezervācija, rezervāciju hierarhiju *virs* rezervāciju hierarhijas, un ir iespējota automātiskā rezervācija, partijas numura automātiskās rezervēšanas uzvedne tiek parādīta pat tad, ja izdošanai ir pieejama tikai viena partija.</span><span class="sxs-lookup"><span data-stu-id="5d09d-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="5d09d-125">Tomēr, ja izmantojat to pašu krājumu noliktavā, kur ir iespējoti noliktavas procesi, netiek parādīta automātiskās rezervācijas uzvedne.</span><span class="sxs-lookup"><span data-stu-id="5d09d-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="5d09d-126">Izsniegšanas iemesls</span><span class="sxs-lookup"><span data-stu-id="5d09d-126">Issue cause</span></span>

<span data-ttu-id="5d09d-127">Ja rezervāciju hierarhija ir definēta kā *virs* vai *pārsniedz sēriju*, atsauces dimensija (**Partijas numurs** vai **Sērijas numurs**) vienmēr jānorāda pieprasījuma pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="5d09d-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="5d09d-128">Noliktavas procesi, iespējams, var pabeigt informāciju, ja ir pieejams viens paketes vai sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="5d09d-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="5d09d-129">Tomēr, tā kā noliktava nav iespējota noliktavas procesiem, lietotājam vienmēr ir jānorāda visas dimensijas virs **Novietojuma**.</span><span class="sxs-lookup"><span data-stu-id="5d09d-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="5d09d-130">Nišu veidnes, kuras izmanto rīcībā esošo nišas kritēriju, neuztēr pašreizējos rīcībā esošos krājumus partijas iespējotiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="5d09d-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="5d09d-131">Plašāku informāciju skatiet [Noliktavas niša](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="5d09d-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="5d09d-132">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="5d09d-132">Issue description</span></span>

<span data-ttu-id="5d09d-133">Nišu veidnes, kurām ir *Rīcībā esošais nišas kritērijs*, neuztver pašreizējos rīcībā esošos krājumus *virs partijas* iespējotiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="5d09d-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="5d09d-134">Viņi to apsver, ja partijas numurs ir norādīts pārdošanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="5d09d-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="5d09d-135">Tomēr, ja izmantojat partijas krājumus, kas ir *zemāki par krājumiem*, pašreizējie rīcībā esošie krājumi tiek uzskatīti par paredzamiem.</span><span class="sxs-lookup"><span data-stu-id="5d09d-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="5d09d-136">Izsniegšanas iemesls</span><span class="sxs-lookup"><span data-stu-id="5d09d-136">Issue cause</span></span>

<span data-ttu-id="5d09d-137">Slotēšanas veidnes virsrakstu var definēt stratēģijai *Pasūtīts*, *Rezervēts* vai *Nodots izpildei*.</span><span class="sxs-lookup"><span data-stu-id="5d09d-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="5d09d-138">*Pasūtītā* pieprasījuma stratēģijai tiek lietotas tās pašas rezervāciju hierarhijas prasības, kas attiecas uz rezervācijas vai izlaišanas noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="5d09d-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="5d09d-139">Tāpēc krājumiem, kuru pakešuzdevums atrodas *virs* un sērijas atrodas *zem* rezervāciju hierarhijām, pieprasījuma pasūtījumā (pārdošana vai pārsūtīšana) ir jānorāda paketes vai sērijas numurs.</span><span class="sxs-lookup"><span data-stu-id="5d09d-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="5d09d-140">Alternatīvi *Rezervētā* pieprasījuma stratēģiju var izmantot, lai atlasītu partiju vai sērijas numuru pirms noliktavas pieprasījuma ģenerēšanas noliktavas slotā.</span><span class="sxs-lookup"><span data-stu-id="5d09d-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
