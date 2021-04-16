---
title: Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828110"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="691a9-103">Problēmu novēršana saistībā ar rezervācijām noliktavas pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="691a9-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="691a9-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu recervācijām programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="691a9-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="691a9-105">Tēmām, kas ir saistītas ar pakešu un sēriju numuru reģistrācijām, skatiet informāciju par [Noliktavas pakešuzdevumu un sēriju rezervāciju hierarhiju problēmu novēršanu](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="691a9-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="691a9-106">Tiek atgriezta sekojošā kļūda: “Rezervācijas nevar noņemt, jo ir izveidots darbs, kas balstās uz rezervāciju.”</span><span class="sxs-lookup"><span data-stu-id="691a9-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="691a9-107">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="691a9-107">Issue description</span></span>

<span data-ttu-id="691a9-108">Pārdošanas rindā nevar atrezervēt krājumus, jo uz šo rindu ir atvērts darbs.</span><span class="sxs-lookup"><span data-stu-id="691a9-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="691a9-109">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="691a9-109">Issue resolution</span></span>

<span data-ttu-id="691a9-110">Izpētiet, vai ir atvērts pakošanas grupas darbs, lai atgrieztu krājumu no iepakošanas stacijas uz citu vietu (piemēram, *Baydoor*).</span><span class="sxs-lookup"><span data-stu-id="691a9-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="691a9-111">Pārskatiet ierakstus lapās **Darba izveides vēstures žurnāls** un **Darba informācija**, lai noteiktu, kas fiziski rezervē krājumus, un pēc tam pabeidziet vai dzēsiet darbu, lai atbrīvotu rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="691a9-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="691a9-112">Tiek parādīts šāds kļūdas ziņojums: "Krājumu daudzums - %1 nevarēja atjaunināt, jo krājumam %2 ir nepietiekamu krājumu darbību...."</span><span class="sxs-lookup"><span data-stu-id="691a9-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="691a9-113">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="691a9-113">Issue description</span></span>

<span data-ttu-id="691a9-114">Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="691a9-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="691a9-115">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma pilns teksts:</span><span class="sxs-lookup"><span data-stu-id="691a9-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="691a9-116">Krājumu daudzums -%1 nevarēja atjaunināt %2 krājumu darbību nepietiekamā daudzuma dēļ, kas atbilst dimensijas Lielumam=%3, Krāsai=%4, Papildinājumiem=%5, Vietai=%6, Noliktavai=%7, Novietojumam=%8, Krājuma statusam=pieejams, Numura zīmei=%9, Partijas numuram=%10, Atsauces ID %11, Laidien ID %12.</span><span class="sxs-lookup"><span data-stu-id="691a9-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="691a9-117">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="691a9-117">Issue resolution</span></span>

<span data-ttu-id="691a9-118">Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu.</span><span class="sxs-lookup"><span data-stu-id="691a9-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="691a9-119">Piemēram, šīs darbības var atvērt kvalitātes pasūtījumus, krājumu bloķēšanas ierakstus vai izdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="691a9-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="691a9-120">Tiek parādīts šāds kļūdas ziņojums: "Fiziski rīcībā esošo...nevar rezervēt, jo krājumos ir pieejams tikai 0,00."</span><span class="sxs-lookup"><span data-stu-id="691a9-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="691a9-121">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="691a9-121">Issue description</span></span>

<span data-ttu-id="691a9-122">Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="691a9-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="691a9-123">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma pilns teksts:</span><span class="sxs-lookup"><span data-stu-id="691a9-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="691a9-124">Fiziskais rīcībā esošais Vietne=%1, Noliktava=%2, Krājumu statuss=pieejams, Partijas numurs=%3, Īpašnieks=%4: %5 nevar rezervēt, jo krājumos ir pieejamas tikai 0,00.</span><span class="sxs-lookup"><span data-stu-id="691a9-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="691a9-125">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="691a9-125">Issue resolution</span></span>

<span data-ttu-id="691a9-126">Šo problēmu, iespējams, izraisa atvērts darbs.</span><span class="sxs-lookup"><span data-stu-id="691a9-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="691a9-127">Vai nu pabeidziet darbu, vai saņemiet bez darba izveides.</span><span class="sxs-lookup"><span data-stu-id="691a9-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="691a9-128">Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu.</span><span class="sxs-lookup"><span data-stu-id="691a9-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="691a9-129">Piemēram, šīs darbības var būt atvērti kvalitātes pasūtījumi, krājumu bloķēšanas ieraksti vai izdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="691a9-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
