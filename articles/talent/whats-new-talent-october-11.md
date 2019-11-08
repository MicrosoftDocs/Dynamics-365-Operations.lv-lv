---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 15. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a19aa20cef7d8671876a5fd5e8552ff72d6d29ac
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551345"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-15-2018"></a><span data-ttu-id="e249a-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 15. oktobris)</span><span class="sxs-lookup"><span data-stu-id="e249a-103">What's new or changed in Dynamics 365 Talent - Core HR (October 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e249a-104">**8.1.1056 būvējums**</span><span class="sxs-lookup"><span data-stu-id="e249a-104">**Build 8.1.1056**</span></span>

<span data-ttu-id="e249a-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="e249a-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="e249a-106">Izmaiņas</span><span class="sxs-lookup"><span data-stu-id="e249a-106">Changes</span></span>
<span data-ttu-id="e249a-107">Papildus dažādiem labojumiem šajā laidienā ir ieviesti tālāk aprakstītie jauninājumi.</span><span class="sxs-lookup"><span data-stu-id="e249a-107">In addition to miscellanous fixes, the following updates have been made in this release:</span></span>
- <span data-ttu-id="e249a-108">Pēdējā darbadiena tagad tiek iestatīta, pieņemot darbā vai iestatot nodarbinātības beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="e249a-108">Last Day worked now set when hiring or setting an employment end date.</span></span>
- <span data-ttu-id="e249a-109">ASV atbilstības atsauces ir noņemtas, ja tiek strādāts uzņēmumos, kas neatrodas ASV (ACA, ADA un I9).</span><span class="sxs-lookup"><span data-stu-id="e249a-109">US compliance references removed when in non US companies (ACA, ADA, and I9).</span></span>
- <span data-ttu-id="e249a-110">Nederīgi datumi (1/1/1900) analīzes lapās tagad tiek slēpti.</span><span class="sxs-lookup"><span data-stu-id="e249a-110">Invalid dates (1/1/1900) are now hidden on analytics pages.</span></span>

## <a name="known-issue"></a><span data-ttu-id="e249a-111">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="e249a-111">Known issue</span></span>

<span data-ttu-id="e249a-112">**Problēma:** pievienojot nodarbinātajam jaunu pielikumu, tiek deaktivizēta poga **Jauns** un **Rediģēt**. **Risinājums:** pirms pielikuma lapas atvēršanas pārbaudiet, vai lapā **Nodarbinātais** ir aizvērta papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="e249a-112">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="e249a-113">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="e249a-113">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="e249a-114">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="e249a-114">(This issue will be fixed in the next platform update.)</span></span>
