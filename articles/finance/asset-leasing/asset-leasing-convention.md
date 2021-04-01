---
title: Līdzekļu nomas līgumi
description: Šajā tēmā ir aprakstīti līgumi iznomātajiem līdzekļiem.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237520"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="91460-103">Līdzekļu nomas līgumi</span><span class="sxs-lookup"><span data-stu-id="91460-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="91460-104">Šajā tēmā ir aprakstīti līgumi iznomātajiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="91460-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="91460-105">Nomas līgumi tiek izmantoti, lai noteiktu nomas grāmatas sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="91460-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="91460-106">Ja nomas līgums ir iestatīts uz **Nav**, sākuma datums ir tāds pats kā nomas sākuma datums (t.i., **Nomas sākuma datuma** lauka vērtība).</span><span class="sxs-lookup"><span data-stu-id="91460-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="91460-107">Ja nomas līgums ir iestatīts uz **Pilnu mēnesi**, sākuma datums ir mēneša pirmā diena, kurā beidzas nomas sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="91460-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="91460-108">Sākuma datums nosaka perioda sākuma datumu saistību amortizācijas un līdzekļu nolietojuma grafikiem.</span><span class="sxs-lookup"><span data-stu-id="91460-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="91460-109">Procentu izdevumi un nolietojuma izdevumi tiek grāmatoti atbilstošo grafiku perioda beigu datumā.</span><span class="sxs-lookup"><span data-stu-id="91460-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="91460-110">Sākotnējais atzīšanas un korekciju žurnāla ieraksts tiek grāmatots sākuma datumā.</span><span class="sxs-lookup"><span data-stu-id="91460-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="91460-111">Nomas līgumu līdzekli nav iespējams ieslēgt, izmantojot Līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="91460-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="91460-112">**Līdzekļu pārvaldības** darbvietā atrodiet un atlasiet līdzekli ar nosaukumu **Nomas līgums līdzekļa iznomāšanai**, un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="91460-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="91460-113">Nomas līgumi ir piešķirti nomas līdzekļu grāmatas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="91460-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="91460-114">Lai skatītu vai piešķirtu nomas līgumu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="91460-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="91460-115">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="91460-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="91460-116">Laukā **Nomas līgums** atlasiet vienu no šīm vērtībām.</span><span class="sxs-lookup"><span data-stu-id="91460-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="91460-117">Nomas līgums</span><span class="sxs-lookup"><span data-stu-id="91460-117">Leasing convention</span></span> | <span data-ttu-id="91460-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="91460-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="91460-119">None</span><span class="sxs-lookup"><span data-stu-id="91460-119">None</span></span>               | <span data-ttu-id="91460-120">Saistību norakstīšanas un līdzekļu nolietojuma grafiki sākas nomas sākuma datumā, jo sākuma datums ir vienāds ar nomas sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="91460-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="91460-121">Beigu datums ir vienu mēnesi vēlāk.</span><span class="sxs-lookup"><span data-stu-id="91460-121">The end date is one month later.</span></span> <span data-ttu-id="91460-122">Šis nomas līgums negarantē, ka procenti tiks grāmatoti katra mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="91460-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="91460-123">Pilns mēnesis</span><span class="sxs-lookup"><span data-stu-id="91460-123">Full month</span></span>         | <span data-ttu-id="91460-124">Nomām, kurām ir sākuma datums, kas ir jebkurā mēneša datumā, saistību norakstīšanas un līdzekļu nolietojuma grafiki sāk uzkrāt izdevumus šī mēneša pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="91460-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="91460-125">Šis nomas līgums nodrošina, ka procenti tiek uzkrāti katra mēneša pēdējā dienā par visu mēnesi.</span><span class="sxs-lookup"><span data-stu-id="91460-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="91460-126">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="91460-126">Select **Save**.</span></span>

<span data-ttu-id="91460-127">Izveidojot nomu, katras grāmatas sākuma datums tiek automātiski ievadīts, pamatojoties uz nomas sākuma datumu un uz nomas līgumu, kas norādīts grāmatai.</span><span class="sxs-lookup"><span data-stu-id="91460-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]