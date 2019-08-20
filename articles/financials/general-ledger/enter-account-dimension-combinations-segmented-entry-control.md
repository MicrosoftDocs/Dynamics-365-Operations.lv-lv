---
title: Konta un dimensiju kombināciju ievade (segmentētu ierakstu kontrole)
description: Šajā rakstā ir aprakstīts, kā ievadīt kontu un dimensiju kombinācijas vai virsgrāmatas kontus. Ierakstīšanas darbība bieži tiek saukta par segmentētu ierakstu kontroli.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 872ee7812d98e6102798c3a10773176541c02c90
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839381"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="bc79d-104">Konta un dimensiju kombināciju ievade (segmentētu ierakstu kontrole)</span><span class="sxs-lookup"><span data-stu-id="bc79d-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc79d-105">Šajā rakstā ir aprakstīts, kā ievadīt kontu un dimensiju kombinācijas vai virsgrāmatas kontus.</span><span class="sxs-lookup"><span data-stu-id="bc79d-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="bc79d-106">Ierakstīšanas darbība bieži tiek saukta par segmentētu ierakstu kontroli.</span><span class="sxs-lookup"><span data-stu-id="bc79d-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="bc79d-107">Lietotāji kontu un dimensiju kombinācijas ievada dažādās lapās, piemēram, lapās, kas paredzētas virsgrāmatas žurnāliem, budžeta plānošanai un grāmatošanas definīcijām.</span><span class="sxs-lookup"><span data-stu-id="bc79d-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="bc79d-108">Derīgas kontu un dimensiju kombinācijas ir atkarīgas no konta struktūras, kas tiek piešķirta Virsgrāmatai un papildu kārtulām, kas piešķirtas kontu struktūram.</span><span class="sxs-lookup"><span data-stu-id="bc79d-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="bc79d-109">Kad lietotāji ir ievadījuši kombināciju, viņi var manuāli ierakstīt vērtības vai izmantot bagātīgo uzmeklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="bc79d-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="bc79d-110">Kad notiek ievadīšana laukā, varat sākt rakstīt, un tas meklēs vērtību un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="bc79d-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="bc79d-111">Piemēram, ja ierakstāt 180, tiks meklēta jebkāda vērtība, kas sākas ar šo numuru kombināciju.</span><span class="sxs-lookup"><span data-stu-id="bc79d-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="bc79d-112">Varat arī ierakstīt Skaidra nauda, un tiks meklēta jebkāda vērtība, kuras apraksts sākas ar Skaidra nauda.</span><span class="sxs-lookup"><span data-stu-id="bc79d-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="bc79d-113">Varat arī izmantot aizstājējzīmi, piemēram, \*Skaidra nauda vai \*180, lai meklētu, vai vērtībā vai aprakstā ir ietverti šie meklēšanas kritēriji.</span><span class="sxs-lookup"><span data-stu-id="bc79d-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="bc79d-114">Tabulā ir aprakstīti īsinājumtaustiņi, ko var izmantot, ja pārlūkošanas logs nav atvērts.</span><span class="sxs-lookup"><span data-stu-id="bc79d-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc79d-115">Īsinājumtaustiņš</span><span class="sxs-lookup"><span data-stu-id="bc79d-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="bc79d-116">Darbība</span><span class="sxs-lookup"><span data-stu-id="bc79d-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc79d-117">Alt+lejupvērstā bultiņa</span><span class="sxs-lookup"><span data-stu-id="bc79d-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="bc79d-118">Atver pārlūkošanas logu.</span><span class="sxs-lookup"><span data-stu-id="bc79d-118">Open the lookup.</span></span> <span data-ttu-id="bc79d-119">Ja nospiežat Alt+lejupvērstā bultiņa otro reizi, fokuss tiek pārvietots uz izlidošanas segmentiem.</span><span class="sxs-lookup"><span data-stu-id="bc79d-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="bc79d-120">Enter un Shift + Enter</span><span class="sxs-lookup"><span data-stu-id="bc79d-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="bc79d-121">Kontu plāna norobežotājs</span><span class="sxs-lookup"><span data-stu-id="bc79d-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="bc79d-122">Kreisā un labā bultiņa</span><span class="sxs-lookup"><span data-stu-id="bc79d-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="bc79d-123">Pārejiet uz nākamo vai iepriekšējo segmentu.</span><span class="sxs-lookup"><span data-stu-id="bc79d-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc79d-124">Tabulēšanas taustiņš</span><span class="sxs-lookup"><span data-stu-id="bc79d-124">Tab</span></span></td>
<td><span data-ttu-id="bc79d-125">Režģī pārejiet uz nākamo lauku.</span><span class="sxs-lookup"><span data-stu-id="bc79d-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bc79d-126">Tabulā ir aprakstīti īsinājumtaustiņi, ko var izmantot, ja pārlūkošanas logs ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="bc79d-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc79d-127">Īsinājumtaustiņš</span><span class="sxs-lookup"><span data-stu-id="bc79d-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="bc79d-128">Darbība</span><span class="sxs-lookup"><span data-stu-id="bc79d-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc79d-129">Esc</span><span class="sxs-lookup"><span data-stu-id="bc79d-129">Esc</span></span></td>
<td><span data-ttu-id="bc79d-130">Aizveriet pārlūkošanas logu.</span><span class="sxs-lookup"><span data-stu-id="bc79d-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="bc79d-131">Augšupvērstā bultiņa un lejupvērstā bultiņa</span><span class="sxs-lookup"><span data-stu-id="bc79d-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="bc79d-132">Iepriekšējā lapa un nākamā lapa</span><span class="sxs-lookup"><span data-stu-id="bc79d-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="bc79d-133">Home un End</span><span class="sxs-lookup"><span data-stu-id="bc79d-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="bc79d-134">Sarakstos pārejiet uz nākamo vai iepriekšējo vērtību, nākamo vai iepriekšējo vērtību grupu vai pirmo vai pēdējo pārlūkojamo elementu.</span><span class="sxs-lookup"><span data-stu-id="bc79d-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="bc79d-135">Kontu plāna norobežotājs</span><span class="sxs-lookup"><span data-stu-id="bc79d-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="bc79d-136">Kreisā un labā bultiņa</span><span class="sxs-lookup"><span data-stu-id="bc79d-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="bc79d-137">Pārejiet uz nākamo vai iepriekšējo segmentu.</span><span class="sxs-lookup"><span data-stu-id="bc79d-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc79d-138">Tabulēšanas taustiņš</span><span class="sxs-lookup"><span data-stu-id="bc79d-138">Tab</span></span></td>
<td><span data-ttu-id="bc79d-139">Režģī pārejiet uz nākamo lauku.</span><span class="sxs-lookup"><span data-stu-id="bc79d-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc79d-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="bc79d-140">Alt+W</span></span></td>
<td><span data-ttu-id="bc79d-141">Pārslēdz starp <strong>Rādīt visu</strong> un <strong>Rādīt derīgo</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc79d-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>





