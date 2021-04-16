---
title: Noapaļotas nolietojuma aprēķinu summas
description: Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf7cf68c98b14fb6c206c99673168153b32a449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830427"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="28481-103">Noapaļotas nolietojuma aprēķinu summas</span><span class="sxs-lookup"><span data-stu-id="28481-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28481-104">Šajā rakstā ir izskaidrots lauks Nolietojuma noapaļošana, kas redzams lapā Grāmatas iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="28481-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="28481-105">Katrai grāmatai tiek iestatītas noapaļotas nolietojuma summas.</span><span class="sxs-lookup"><span data-stu-id="28481-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="28481-106">Noapaļotās nolietojuma summas tiek izmantotas pamatlīdzekļa nolietojuma profilā, kurā ir norādīts turpmākais pamatlīdzekļa nolietojums un vērtība, kā arī nolietojuma aprēķināšanas piedāvājumos.</span><span class="sxs-lookup"><span data-stu-id="28481-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="28481-107">Ievadiet mazāko nolietojuma summu, kura ir atļauta šai grāmatai.</span><span class="sxs-lookup"><span data-stu-id="28481-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="28481-108">Neatkarīgi no iestatītajiem noapaļošanas kritērijiem, nolietojuma summa pēdējā nolietojuma periodā netiek noapaļota.</span><span class="sxs-lookup"><span data-stu-id="28481-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="28481-109">Pēdējā nolietojuma perioda beigās pamatlīdzekļa vērtībai jābūt 0 (nulle) vai jāsasniedz lūžņu vērtība, ja tā tiek izmantota.</span><span class="sxs-lookup"><span data-stu-id="28481-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="28481-110">Piemērs</span><span class="sxs-lookup"><span data-stu-id="28481-110">Example</span></span>

<span data-ttu-id="28481-111">Nolietojums bez noapaļošanas ir aprēķināts par summu 2444,44.</span><span class="sxs-lookup"><span data-stu-id="28481-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="28481-112">Saskaņā ar nākamās tabulas datiem ieteiktās summas atkarībā no iestatītajiem noapaļošanas kritērijiem mainās.</span><span class="sxs-lookup"><span data-stu-id="28481-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="28481-113">Noapaļošanas metode</span><span class="sxs-lookup"><span data-stu-id="28481-113">Rounding method</span></span> | <span data-ttu-id="28481-114">Nolietojuma summa</span><span class="sxs-lookup"><span data-stu-id="28481-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="28481-115">Noapaļoš 0,1</span><span class="sxs-lookup"><span data-stu-id="28481-115">Rounding 0.1</span></span>    | <span data-ttu-id="28481-116">2444,40</span><span class="sxs-lookup"><span data-stu-id="28481-116">2,444.40</span></span>            |
| <span data-ttu-id="28481-117">Noapaļoš 1,00</span><span class="sxs-lookup"><span data-stu-id="28481-117">Rounding 1.00</span></span>   | <span data-ttu-id="28481-118">2444,00</span><span class="sxs-lookup"><span data-stu-id="28481-118">2,444.00</span></span>            |
| <span data-ttu-id="28481-119">Noapaļoš 10,00</span><span class="sxs-lookup"><span data-stu-id="28481-119">Rounding 10.00</span></span>  | <span data-ttu-id="28481-120">2440,00</span><span class="sxs-lookup"><span data-stu-id="28481-120">2,440.00</span></span>            |
| <span data-ttu-id="28481-121">Noapaļoš 100,00</span><span class="sxs-lookup"><span data-stu-id="28481-121">Rounding 100.00</span></span> | <span data-ttu-id="28481-122">2400,00</span><span class="sxs-lookup"><span data-stu-id="28481-122">2,400.00</span></span>            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]