---
title: Jūs saņemsiet uzaicinājumu saglabāt krājumu vajadzības iestatījumus, pat ja izmaiņas nav veiktas
description: Jūs saņemsiet uzaicinājumu saglabāt krājumu vajadzības iestatījumus, pat ja izmaiņas nav veiktas.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049478"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="f814f-103">Jūs saņemsiet uzaicinājumu saglabāt krājumu vajadzības iestatījumus, pat ja izmaiņas nav veiktas</span><span class="sxs-lookup"><span data-stu-id="f814f-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="f814f-104">KB numurs: 4615588</span><span class="sxs-lookup"><span data-stu-id="f814f-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="f814f-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="f814f-105">Symptoms</span></span>

<span data-ttu-id="f814f-106">Dažos scenārijos, varat saņemt šādu ziņojumu, atverot **krājumu vajadzības** lapu pēc tam, kad importējat krājumus, izmantojot *Krājumu vajadzības V2* elementu:</span><span class="sxs-lookup"><span data-stu-id="f814f-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="f814f-107">Vai pirms aizvēršanas vēlaties saglabāt savas veiktās izmaiņas?</span><span class="sxs-lookup"><span data-stu-id="f814f-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="f814f-108">Jūs saņemat šo ziņojumu, kaut arī neesat veicis nekādas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="f814f-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="f814f-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="f814f-109">Resolution</span></span>

<span data-ttu-id="f814f-110">**Krājumu vajadzības** lapa ietver kompleksu noklusējumu loģiku, kas var izraisīt ziņojuma rādīšanu pēc tiešu izmaiņu veikšanas datubāzē, piemēram, izmantojot elementa importu.</span><span class="sxs-lookup"><span data-stu-id="f814f-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="f814f-111">Piemēram, `AREGENERALSETTINGSOVERRIDDEN` elementa lauks ir iestatīts uz *Nē*, bet jūs importējiet failu, kas nodrošina jaunas vai modificētas vērtības tādiem laukiem kā `PRODUCTCOVERAGEGROUPID` un/vai `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="f814f-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="f814f-112">Šajā gadījumā, tā kā lauks `AREGENERALSETTINGSOVERRIDDEN` ir iestatīts uz *Nē*, vērtības automātiski tiek notīrītas no laukiem, atverot **Krājumu vajadzības** lapu pirmo reiz pēc importēšanas.</span><span class="sxs-lookup"><span data-stu-id="f814f-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="f814f-113">Ja izmaiņas saglabājat kā uzvednes ziņojumu, tās tiek saglabātas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="f814f-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="f814f-114">Pretējā gadījumā nākamajā lapas atvēršanas reizē saņemsit to pašu ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="f814f-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="f814f-115">Lai novērstu šo darbību, bet ietvertu arī vērtības tādiem laukiem kā `PRODUCTCOVERAGEGROUPID`, izmantojot elementa importēšanu, iestatiet `AREGENERALSETTINGSOVERRIDDEN` uz *Jā*, kad veicat importēšanu.</span><span class="sxs-lookup"><span data-stu-id="f814f-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
