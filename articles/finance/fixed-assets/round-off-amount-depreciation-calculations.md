---
title: Noapaļotas nolietojuma aprēķinu summas
description: Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40fd019b1b5900fbd15866d9d3c32ed6d88147b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445646"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="55154-103">Noapaļotas nolietojuma aprēķinu summas</span><span class="sxs-lookup"><span data-stu-id="55154-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55154-104">Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="55154-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="55154-105">Katrai grāmatai tiek iestatītas noapaļotas nolietojuma summas.</span><span class="sxs-lookup"><span data-stu-id="55154-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="55154-106">Noapaļotās nolietojuma summas tiek izmantotas pamatlīdzekļa nolietojuma profilā, kurā ir norādīts turpmākais pamatlīdzekļa nolietojums un vērtība, kā arī nolietojuma aprēķināšanas piedāvājumos.</span><span class="sxs-lookup"><span data-stu-id="55154-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="55154-107">Ievadiet mazāko nolietojuma summu, kura ir atļauta šai grāmatai.</span><span class="sxs-lookup"><span data-stu-id="55154-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="55154-108">Neatkarīgi no iestatītajiem noapaļošanas kritērijiem, nolietojuma summa pēdējā nolietojuma periodā netiek noapaļota.</span><span class="sxs-lookup"><span data-stu-id="55154-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="55154-109">Pēdējā nolietojuma perioda beigās pamatlīdzekļa vērtībai jābūt 0 (nulle) vai jāsasniedz lūžņu vērtība, ja tā tiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="55154-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="55154-110">Piemērs</span><span class="sxs-lookup"><span data-stu-id="55154-110">Example</span></span>

<span data-ttu-id="55154-111">Nolietojums bez noapaļošanas ir aprēķināts par summu 2444,44.</span><span class="sxs-lookup"><span data-stu-id="55154-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="55154-112">Saskaņā ar nākamās tabulas datiem ieteiktās summas atkarībā no iestatītajiem noapaļošanas kritērijiem mainās.</span><span class="sxs-lookup"><span data-stu-id="55154-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="55154-113">Noapaļošanas metode</span><span class="sxs-lookup"><span data-stu-id="55154-113">Rounding method</span></span> | <span data-ttu-id="55154-114">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="55154-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="55154-115">Noapaļoš 0,1</span><span class="sxs-lookup"><span data-stu-id="55154-115">Rounding 0.1</span></span>    | <span data-ttu-id="55154-116">2444,40</span><span class="sxs-lookup"><span data-stu-id="55154-116">2,444.40</span></span>            |
| <span data-ttu-id="55154-117">Noapaļoš 1,00</span><span class="sxs-lookup"><span data-stu-id="55154-117">Rounding 1.00</span></span>   | <span data-ttu-id="55154-118">2444,00</span><span class="sxs-lookup"><span data-stu-id="55154-118">2,444.00</span></span>            |
| <span data-ttu-id="55154-119">Noapaļoš 10,00</span><span class="sxs-lookup"><span data-stu-id="55154-119">Rounding 10.00</span></span>  | <span data-ttu-id="55154-120">2440,00</span><span class="sxs-lookup"><span data-stu-id="55154-120">2,440.00</span></span>            |
| <span data-ttu-id="55154-121">Noapaļoš 100,00</span><span class="sxs-lookup"><span data-stu-id="55154-121">Rounding 100.00</span></span> | <span data-ttu-id="55154-122">2400,00</span><span class="sxs-lookup"><span data-stu-id="55154-122">2,400.00</span></span>            |





