---
title: Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma
description: Šajā tēmā aprakstīta metode, kas tiek izmantota pamatlīdzekļos, lai aprēķinātu nolietojumu pēc līdzekļa sadalīšanas, izmantojot bilances samazināšanas metodi.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 615d17c71b904d426081d4c57492ba7e95c2c749
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650673"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="e3826-103">Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma</span><span class="sxs-lookup"><span data-stu-id="e3826-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3826-104">Šajā tēmā aprakstīta metode, kas tiek izmantota pamatlīdzekļos, lai aprēķinātu nolietojumu pēc līdzekļa sadalīšanas citā līdzeklī, izmantojot bilances samazināšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="e3826-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="e3826-105">Nolietojuma gads, kas ir konfigurēts līdzekļa grāmatā, ir finanšu gads.</span><span class="sxs-lookup"><span data-stu-id="e3826-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="e3826-106">Lai iegūtu papildu informāciju, skatiet sadaļas [Nolietojuma bilances samazināšana](reduce-balance-depreciation.md) un [Pamatlīdzekļa sadalīšana](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="e3826-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="e3826-107">Ja pamatlīdzeklis tiek sadalīts finanšu periodā, kas ir vēlāks par periodu, kad pamatlīdzeklis tika iegūts, samazinātais bilances nolietojums attieksies uz pamatlīdzekļa atlikušo vērtību (AV) iepriekšējā gadā.</span><span class="sxs-lookup"><span data-stu-id="e3826-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="e3826-108">Tas arī attieksies uz ieguves un nolietojuma korekcijas darījumiem, kas tika izveidoti no darījuma, kas sadalīja līdzekli.</span><span class="sxs-lookup"><span data-stu-id="e3826-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="e3826-109">Šī darbība pieņem, ka līdzeklis tika iegūts vienā finanšu gadā un sadalīts vēlākā finanšu gadā.</span><span class="sxs-lookup"><span data-stu-id="e3826-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="e3826-110">Summa, kas ir jāizlieto oriģinālajam līdzeklim pēc sadalījuma, ataino pamatlīdzekļa AV pirms līdzekļa sadalīšanas, kā arī ieguves un nolietojuma korekcijas darījumu, kas tika grāmatots sadalīšanai.</span><span class="sxs-lookup"><span data-stu-id="e3826-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="e3826-111">Piemēram, ir spēkā šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="e3826-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="e3826-112">Finanšu periods ir no 30. jūnija līdz 1. jūlijam.</span><span class="sxs-lookup"><span data-stu-id="e3826-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="e3826-113">Bilances samazinājuma procentuālā vērtība ir 18 procenti, un līdzeklis tiek iegūts 2019. jūnijā par $ 10 000 iegādes cenu.</span><span class="sxs-lookup"><span data-stu-id="e3826-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="e3826-114">Pirmā finanšu gada nolietojums ir vienāds ar $ 18 000, mēneša nolietojums ir vienāds ar $ 150, un pamatlīdzeklis tiek nolietots līdz 2019. novembrim (summa ir $ 738,75).</span><span class="sxs-lookup"><span data-stu-id="e3826-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="e3826-115">2019. novembrī 80 procenti līdzekļa tiek sadalīti uz citu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="e3826-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="e3826-116">[![Degresīvā nolietojuma aprēķināšanas metode pēc sadalījuma](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="e3826-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="e3826-117">Oriģinālā pamatlīdzekļa nolietošanas summa ir $ 1822,25.</span><span class="sxs-lookup"><span data-stu-id="e3826-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="e3826-118">Šī summa ir vienāda ar AV pirms sadalītā darījuma grāmatošanas ($ 9111,25), pieskaitot iegādes korekciju, kas tiek ģenerēta, grāmatojot sadalīto darījumu (-$ 8000), kā arī nolietojuma korekciju, kas tiek ģenerēta sadalīšanas darījumā ($ 711).</span><span class="sxs-lookup"><span data-stu-id="e3826-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="e3826-119">Tāpēc nolietojums otrajā gadā ir (1822,25 × 18 procenti) ÷ 12 = $ 27,33.</span><span class="sxs-lookup"><span data-stu-id="e3826-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="e3826-120">Jaunā pamatlīdzekļa nolietošanas summa pirmajā gadā ir (8000 × 18 procenti) ÷ 12 = $ 120.</span><span class="sxs-lookup"><span data-stu-id="e3826-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
