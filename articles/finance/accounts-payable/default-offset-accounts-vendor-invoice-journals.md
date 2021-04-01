---
title: Noklusējuma korespondējošie konti kreditoru rēķinam un rēķinu apstiprinājumu žurnāliem
description: Šajā tēmā sniegtā informācija palīdzēs jums izlemt, vai rēķinu žurnāliem ir jāpiešķir noklusējuma konti.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e67bebcfb934a3e6dae78cafd7bb2b01c05e450
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250630"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a><span data-ttu-id="605e5-103">Noklusējuma korespondējošie konti kreditoru rēķinam un rēķinu apstiprinājumu žurnāliem</span><span class="sxs-lookup"><span data-stu-id="605e5-103">Default offset accounts for vendor invoice and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="605e5-104">Noklusējuma korespondējošie konti tiek izmantoti tālāk norādītajās kreditoru rēķinu žurnālu lapās.</span><span class="sxs-lookup"><span data-stu-id="605e5-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="605e5-105">Rēķinu žurnāls</span><span class="sxs-lookup"><span data-stu-id="605e5-105">Invoice journal</span></span>
-   <span data-ttu-id="605e5-106">Rēķinu apstiprināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="605e5-106">Invoice approval journal</span></span>

<span data-ttu-id="605e5-107">Izmantojiet tālāk esošo tabulu, lai izlemtu, kur ir jāpiešķir rēķinu žurnālu noklusējuma konti.</span><span class="sxs-lookup"><span data-stu-id="605e5-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="605e5-108">Noklusējuma kontu iestatīšanas vieta</span><span class="sxs-lookup"><span data-stu-id="605e5-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="605e5-109">Noklusējuma kontu nodrošināšanas vieta</span><span class="sxs-lookup"><span data-stu-id="605e5-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="605e5-110">Šīs opcijas ietekme uz apstrādi</span><span class="sxs-lookup"><span data-stu-id="605e5-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="605e5-111">Šis opcijas izmantošanas gadījumi</span><span class="sxs-lookup"><span data-stu-id="605e5-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="605e5-112"><strong>Kreditoru grupa</strong> — iestatiet kreditoru grupu noklusējuma korespondējošos kontus lapā <strong>Noklusētie konta iestatījumi</strong>, ko varat atvērt lapā <strong>Kreditoru grupas</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="605e5-113">Kreditora konts</span><span class="sxs-lookup"><span data-stu-id="605e5-113">Vendor account</span></span></li>
<li><span data-ttu-id="605e5-114">Kreditoru kontu žurnāla ieraksti kreditoru grupā, ja kreditoru kontiem nav norādīti noklusējuma konti</span><span class="sxs-lookup"><span data-stu-id="605e5-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="605e5-115">Kreditoru grupu noklusējuma korespondējošie konti tiek rādītas kā kreditoru noklusējuma korespondējošie konti lapā <strong>Noklusētie konta iestatījumi</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="605e5-116">Šo lapu varat atvērt saraksta lapā <strong>Visi kreditori</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="605e5-117">Izmantojiet šo opciju, ja parasti maksājat par viena veida precēm, ko nodrošina vienas un tās pašas kreditoru grupas.</span><span class="sxs-lookup"><span data-stu-id="605e5-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="605e5-118"><strong>Kreditora konts</strong> — iestatiet kreditoru kontu noklusējuma kontus lapā <strong>Noklusētie konta iestatījumi</strong>, ko varat atvērt lapā <strong>Kreditori</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="605e5-119">Kreditoru konta žurnāla ieraksti</span><span class="sxs-lookup"><span data-stu-id="605e5-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="605e5-120">Kreditoru noklusējuma korespondējošie konti tiek rādīti kā kreditora konta žurnāla ierakstu noklusējuma korespondējošie konti.</span><span class="sxs-lookup"><span data-stu-id="605e5-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="605e5-121">Izmantojiet šo opciju, ja parasti maksājat par viena veida precēm, ko nodrošina vieni un tie paši kreditori.</span><span class="sxs-lookup"><span data-stu-id="605e5-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="605e5-122"><strong>Žurnālu nosaukumi</strong> — iestatiet žurnālu noklusējuma korespondējošos kontus lapā <strong>Žurnālu nosaukumi</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="605e5-123">Atlasiet opciju <strong>Fiksēts korespondējošais konts</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="605e5-124">Ņemiet vērā, ka nevara&#39;t norādīt žurnālu nosaukumu noklusējuma korespondējošos kontus, ja žurnālu nosaukumiem atbilstošais žurnāla veids ir <strong>Rēķinu reģistrs</strong> vai <strong>Apstiprinājums</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="605e5-125">Žurnāla virsraksts, kurā tiek izmantots žurnāla nosaukums</span><span class="sxs-lookup"><span data-stu-id="605e5-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="605e5-126">Žurnāla ieraksti žurnālos, kuros tiek lietots žurnāla nosaukums</span><span class="sxs-lookup"><span data-stu-id="605e5-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="605e5-127">Ja lapā <strong>Žurnālu nosaukumi</strong> ir atlasīta opcija <strong>Fiksēts korespondējošais konts</strong>, žurnāla nosaukuma noklusējuma korespondējošais konts tiek izmantots kreditora vai kreditoru grupas noklusējuma korespondējošā konta vieta.</span><span class="sxs-lookup"><span data-stu-id="605e5-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="605e5-128">Izmantojiet šo opciju, lai iestatītu žurnālus noteiktām maksām vai izdevumiem, kas tiek iekasēti no konkrētiem kontiem neatkarīgi no kreditora vai kreditoru grupas, kurā ir ietverts kreditors.</span><span class="sxs-lookup"><span data-stu-id="605e5-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="605e5-129"><strong>Žurnālu nosaukumi</strong> — iestatiet žurnālu noklusējuma korespondējošos kontus lapā <strong>Žurnālu nosaukumi</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="605e5-130">Noņemiet atzīmi no opcijas <strong>Fiksēts korespondējošais konts</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="605e5-131">Ņemiet vērā, ka nevara&#39;t norādīt žurnālu nosaukumu noklusējuma korespondējošos kontus, ja žurnālu nosaukumiem atbilstošais žurnāla veids ir <strong>Rēķinu reģistrs</strong> vai <strong>Apstiprinājums</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="605e5-132">Žurnāla virsraksts</span><span class="sxs-lookup"><span data-stu-id="605e5-132">Journal header</span></span></li>
<li><span data-ttu-id="605e5-133">Žurnāla ieraksti žurnālos, kuros tiek lietots žurnāla nosaukums</span><span class="sxs-lookup"><span data-stu-id="605e5-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="605e5-134">Šie noklusējuma ierakstu tiek izmantoti žurnālu virsrakstu lapās, un žurnāla virsraksta lapā norādītais korespondējošais konts tiek izmantots kā noklusējuma ieraksts žurnālu dokumentu lapās.</span><span class="sxs-lookup"><span data-stu-id="605e5-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="605e5-135">Lapā <strong>Žurnālu nosaukumi</strong> norādītie noklusējuma konti tiek izmantoti tikai tad, ja nav iestatīti kreditora konta noklusējuma konti.</span><span class="sxs-lookup"><span data-stu-id="605e5-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="605e5-136">Izmantojiet šo opciju, lai iestatītu noklusējuma kontus, kas tiek izmatoti tad, ja nav piešķirts kreditora noklusējuma korespondējošais konts.</span><span class="sxs-lookup"><span data-stu-id="605e5-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="605e5-137"><strong>Žurnāla virsraksts</strong> — iestatiet žurnāla noklusējuma korespondējošo kontu, kas tiks izmantots kā noklusējuma ieraksts žurnālu dokumentu lapās.</span><span class="sxs-lookup"><span data-stu-id="605e5-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="605e5-138">Ņemiet vērā, ka nevara&#39;t norādīt žurnāla virsraksta noklusējuma korespondējošos kontus, ja žurnālu nosaukumiem atbilstošais žurnāla veids ir <strong>Rēķinu reģistrs</strong> vai <strong>Apstiprinājums</strong>.</span><span class="sxs-lookup"><span data-stu-id="605e5-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="605e5-139">Žurnāla ieraksti žurnālā</span><span class="sxs-lookup"><span data-stu-id="605e5-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="605e5-140">Žurnāla noklusējuma korespondējošais konts tiek izmantots kā noklusējuma ieraksts žurnālu dokumentu lapās.</span><span class="sxs-lookup"><span data-stu-id="605e5-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="605e5-141">Izmantojiet šo opciju, lai paātrinātu datu ievadi, ja vairumā žurnāla ierakstu tiek izmantots viens un tas pats korespondējošais konts.</span><span class="sxs-lookup"><span data-stu-id="605e5-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]