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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "308418"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="bf64b-103">Noapaļotas nolietojuma aprēķinu summas</span><span class="sxs-lookup"><span data-stu-id="bf64b-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf64b-104">Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="bf64b-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="bf64b-105">Katrai grāmatai tiek iestatītas noapaļotas nolietojuma summas.</span><span class="sxs-lookup"><span data-stu-id="bf64b-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="bf64b-106">Noapaļotās nolietojuma summas tiek izmantotas pamatlīdzekļa nolietojuma profilā, kurā ir norādīts turpmākais pamatlīdzekļa nolietojums un vērtība, kā arī nolietojuma aprēķināšanas piedāvājumos.</span><span class="sxs-lookup"><span data-stu-id="bf64b-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="bf64b-107">Ievadiet mazāko nolietojuma summu, kura ir atļauta šai grāmatai.</span><span class="sxs-lookup"><span data-stu-id="bf64b-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="bf64b-108">Neatkarīgi no iestatītajiem noapaļošanas kritērijiem, nolietojuma summa pēdējā nolietojuma periodā netiek noapaļota.</span><span class="sxs-lookup"><span data-stu-id="bf64b-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="bf64b-109">Pēdējā nolietojuma perioda beigās pamatlīdzekļa vērtībai jābūt 0 (nulle) vai jāsasniedz lūžņu vērtība, ja tā tiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="bf64b-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="bf64b-110">Piemērs</span><span class="sxs-lookup"><span data-stu-id="bf64b-110">Example</span></span>

<span data-ttu-id="bf64b-111">Nolietojums bez noapaļošanas ir aprēķināts par summu 2444,44.</span><span class="sxs-lookup"><span data-stu-id="bf64b-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="bf64b-112">Saskaņā ar nākamās tabulas datiem ieteiktās summas atkarībā no iestatītajiem noapaļošanas kritērijiem mainās.</span><span class="sxs-lookup"><span data-stu-id="bf64b-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="bf64b-113">Noapaļošanas metode</span><span class="sxs-lookup"><span data-stu-id="bf64b-113">Rounding method</span></span> | <span data-ttu-id="bf64b-114">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="bf64b-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="bf64b-115">Noapaļoš 0,1</span><span class="sxs-lookup"><span data-stu-id="bf64b-115">Rounding 0.1</span></span>    | <span data-ttu-id="bf64b-116">2444,40</span><span class="sxs-lookup"><span data-stu-id="bf64b-116">2,444.40</span></span>            |
| <span data-ttu-id="bf64b-117">Noapaļoš 1,00</span><span class="sxs-lookup"><span data-stu-id="bf64b-117">Rounding 1.00</span></span>   | <span data-ttu-id="bf64b-118">2444,00</span><span class="sxs-lookup"><span data-stu-id="bf64b-118">2,444.00</span></span>            |
| <span data-ttu-id="bf64b-119">Noapaļoš 10,00</span><span class="sxs-lookup"><span data-stu-id="bf64b-119">Rounding 10.00</span></span>  | <span data-ttu-id="bf64b-120">2440,00</span><span class="sxs-lookup"><span data-stu-id="bf64b-120">2,440.00</span></span>            |
| <span data-ttu-id="bf64b-121">Noapaļoš 100,00</span><span class="sxs-lookup"><span data-stu-id="bf64b-121">Rounding 100.00</span></span> | <span data-ttu-id="bf64b-122">2400,00</span><span class="sxs-lookup"><span data-stu-id="bf64b-122">2,400.00</span></span>            |





