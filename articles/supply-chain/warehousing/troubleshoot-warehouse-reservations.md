---
title: Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
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
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1ea23059d56ebf387a95a1378e2a3cd47556d5f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993875"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="c0d3e-103">Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="c0d3e-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0d3e-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="c0d3e-105">Tiek atgriezta sekojošā kļūda: “Rezervācijas nevar noņemt, jo ir izveidots darbs, kas balstās uz rezervāciju.”</span><span class="sxs-lookup"><span data-stu-id="c0d3e-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c0d3e-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="c0d3e-106">Issue description</span></span>

<span data-ttu-id="c0d3e-107">Pārdošanas rindā nevar atrezervēt krājumus, jo uz šo rindu ir atvērts darbs.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c0d3e-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="c0d3e-108">Issue resolution</span></span>

<span data-ttu-id="c0d3e-109">Izpētiet, vai ir atvērts pakošanas grupas darbs, lai atgrieztu krājumu no iepakošanas stacijas uz citu vietu (piemēram, *Baydoor*).</span><span class="sxs-lookup"><span data-stu-id="c0d3e-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="c0d3e-110">Pārskatiet ierakstus lapās **Darba izveides vēstures žurnāls** un **Darba informācija**, lai noteiktu, kas fiziski rezervē krājumus, un pēc tam pabeidziet vai dzēsiet darbu, lai atbrīvotu rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="c0d3e-111">Tiek parādīts šāds kļūdas ziņojums: "Krājumu daudzums - %1 nevarēja atjaunināt, jo krājumam %2 ir nepietiekamu krājumu darbību...."</span><span class="sxs-lookup"><span data-stu-id="c0d3e-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c0d3e-112">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="c0d3e-112">Issue description</span></span>

<span data-ttu-id="c0d3e-113">Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="c0d3e-114">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma pilns teksts:</span><span class="sxs-lookup"><span data-stu-id="c0d3e-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="c0d3e-115">Krājumu daudzums -%1 nevarēja atjaunināt %2 krājumu darbību nepietiekamā daudzuma dēļ, kas atbilst dimensijas Lielumam=%3, Krāsai=%4, Papildinājumiem=%5, Vietai=%6, Noliktavai=%7, Novietojumam=%8, Krājuma statusam=pieejams, Numura zīmei=%9, Partijas numuram=%10, Atsauces ID %11, Laidien ID %12.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c0d3e-116">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="c0d3e-116">Issue resolution</span></span>

<span data-ttu-id="c0d3e-117">Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="c0d3e-118">Piemēram, šīs darbības var atvērt kvalitātes pasūtījumus, krājumu bloķēšanas ierakstus vai izdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="c0d3e-119">Tiek parādīts šāds kļūdas ziņojums: "Fiziski rīcībā esošo...nevar rezervēt, jo krājumos ir pieejams tikai 0,00."</span><span class="sxs-lookup"><span data-stu-id="c0d3e-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c0d3e-120">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="c0d3e-120">Issue description</span></span>

<span data-ttu-id="c0d3e-121">Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="c0d3e-122">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma pilns teksts:</span><span class="sxs-lookup"><span data-stu-id="c0d3e-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="c0d3e-123">Fiziskais rīcībā esošais Vietne=%1, Noliktava=%2, Krājumu statuss=pieejams, Partijas numurs=%3, Īpašnieks=%4: %5 nevar rezervēt, jo krājumos ir pieejamas tikai 0,00.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c0d3e-124">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="c0d3e-124">Issue resolution</span></span>

<span data-ttu-id="c0d3e-125">Šo problēmu, iespējams, izraisa atvērts darbs.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="c0d3e-126">Vai nu pabeidziet darbu, vai saņemiet bez darba izveides.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="c0d3e-127">Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="c0d3e-128">Piemēram, šīs darbības var būt atvērti kvalitātes pasūtījumi, krājumu bloķēšanas ieraksti vai izdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="c0d3e-129">Tiek parādīts šāds kļūdas ziņojums: "Jāpiešķir kopumam, noslodzes rindām ir jānorāda dimensijas virs novietojuma.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="c0d3e-130">Lai piešķirtu šīs dimensijas, rezervējiet un atkārtoti izveidojiet noslodzes rindu."</span><span class="sxs-lookup"><span data-stu-id="c0d3e-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c0d3e-131">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="c0d3e-131">Issue description</span></span>

<span data-ttu-id="c0d3e-132">Kad izmantojat krājumu, kam ir "partija virs" rezervāciju hierarhija (ar **Partijas numura** dimensiju, kas novietota *virs* **Novietojuma** dimensijas), **Izlaist uz noliktavu** komanda lapā **Kravas plānošanas rīks** daļējam daudzumam nestrādā.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="c0d3e-133">Šis kļūdas ziņojums tiek parādīts, un nav izveidots neviens darbs daļējam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="c0d3e-134">Tomēr, ja izmantojat krājumu, kam ir "partija zem" rezervāciju hierarhija (ar **Partijas numura** dimensiju, kas novietota *zem* **Novietojuma** dimensijas), varat izlaist kravu no lapas **Kravas plānošanas rīks** daļējam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c0d3e-135">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="c0d3e-135">Issue resolution</span></span>

<span data-ttu-id="c0d3e-136">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-136">This behavior is by design.</span></span> <span data-ttu-id="c0d3e-137">Ja jūs ievietojat dimensiju virs **Novietojuma** dimensijas rezervāciju hierarhijā, tas ir jānorāda pirms izdošanas uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="c0d3e-138">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums laikā, kad tiek veikti izsniegumi uz noliktavu no kravas plānošanas rīka.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="c0d3e-139">Daļējus daudzumus nevar izlaist, ja nav norādīta viena vai vairākas dimensijas virs **Novietojuma**.</span><span class="sxs-lookup"><span data-stu-id="c0d3e-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="c0d3e-140">Papildu informāciju skatiet [Elastīga noliktavas līmeņa dimensijas rezervēšanas politika](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="c0d3e-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
