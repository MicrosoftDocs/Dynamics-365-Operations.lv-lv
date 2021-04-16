---
title: PVN specifikācija pēc virsgrāmatas darbības pārskata
description: Šajā tēmā tiek skaidrots, kā izmantot PVN specifikāciju pēc virsgrāmatas darbību pārskata, lai skatītu un drukātu informāciju par virsgrāmatas darbībām, kas tiek aprēķinātas ar PVN.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815264"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="69d56-103">PVN specifikācija pēc virsgrāmatas darbības pārskata</span><span class="sxs-lookup"><span data-stu-id="69d56-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="69d56-104">Šajā tēmā tiek skaidrots, kā izmantot **PVN specifikācija pēc virsgrāmatas darbības** pārskatu, lai skatītu un drukātu informāciju par virsgrāmatas darbībām, kas tiek aprēķinātas ar PVN.</span><span class="sxs-lookup"><span data-stu-id="69d56-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="69d56-105">Nodokļu kinti vs. ar nodokļiem neapliekamie konti</span><span class="sxs-lookup"><span data-stu-id="69d56-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="69d56-106">**PVN specifikācija pēc virsgrāmatas darbības** pārskats parāda nodokļu darbības gan nodokļu kontos, gan ar nodokļiem neapliekamajos kontos.</span><span class="sxs-lookup"><span data-stu-id="69d56-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="69d56-107">Šie konti tiek iedalīti kategorijās šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="69d56-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="69d56-108">**Nodokļu konts** — tiek uzskatīts, ka konts ir nodokļu konts, kad tiek grāmatota nodokļu darbība, un galvenais konts **PVN** žurnāla rindā ir nodokļu konts, piemēram, PVN maksājuma konts vai PVN saņemēja konts.</span><span class="sxs-lookup"><span data-stu-id="69d56-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="69d56-109">**Ar nodokļiem neapliekamais konts**— tiek uzskatīts, ka konts ir ar nodokļiem neapliekamais konts, kad tiek grāmatota nodokļu darbība, un galvenais konts sākotnējā darbībā ir ar nodokļiem neapliekamais konts, piemēram, ieņēmumu konts vai izdevumu konts.</span><span class="sxs-lookup"><span data-stu-id="69d56-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="69d56-110">Nodokļu kontiem, **Izcelsme**, **PVN ienākumi** un **PVN maksājami** pārskata kolonnas rāda **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="69d56-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="69d56-111">Ar nodokļiem neapliekamajiem kontiem, šīs kolonnas rāda summas.</span><span class="sxs-lookup"><span data-stu-id="69d56-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="69d56-112">Filtrējot pārskatā parādītos datus.</span><span class="sxs-lookup"><span data-stu-id="69d56-112">Filtering the data on the report</span></span>

<span data-ttu-id="69d56-113">Veidojot pārskatu, ie pieejami tālāk norādītie noklusējuma lauki.</span><span class="sxs-lookup"><span data-stu-id="69d56-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="69d56-114">Izmantojot šos laukus, jūs varat filtrēt pārskatā ietvertos datus.</span><span class="sxs-lookup"><span data-stu-id="69d56-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="69d56-115">Lauks</span><span class="sxs-lookup"><span data-stu-id="69d56-115">Field</span></span>                      | <span data-ttu-id="69d56-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="69d56-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="69d56-117">Datums</span><span class="sxs-lookup"><span data-stu-id="69d56-117">Date</span></span>                       | <span data-ttu-id="69d56-118">Izmantojiet laukus sadaļās **No** un **Līdz** , lai noteiktu datumu diapazonu nodokļu darbībām.</span><span class="sxs-lookup"><span data-stu-id="69d56-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="69d56-119">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="69d56-119">Main account</span></span>               | <span data-ttu-id="69d56-120">Izmantojiet laukus sadaļās **No** un **Līdz** , lai noteiktu datumu diapazonu galvēniem kontiem.</span><span class="sxs-lookup"><span data-stu-id="69d56-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="69d56-121">PVN kods</span><span class="sxs-lookup"><span data-stu-id="69d56-121">Sales tax code</span></span>             | <span data-ttu-id="69d56-122">Izmantojiet laukus sadaļās **No** un **Līdz** , lai noteiktu datumu diapazonu PVN kodiem.</span><span class="sxs-lookup"><span data-stu-id="69d56-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="69d56-123">Grupēšana</span><span class="sxs-lookup"><span data-stu-id="69d56-123">Grouping</span></span>                   | <span data-ttu-id="69d56-124">Atlasiet, vai pārskats ir jāsagrupē pēc virsgrāmatas konta vai PVN koda.</span><span class="sxs-lookup"><span data-stu-id="69d56-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="69d56-125">Apakšsumma pēc PVN koda</span><span class="sxs-lookup"><span data-stu-id="69d56-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="69d56-126">Iestatiet šo opciju uz **Jā**, lai parādītu starpsummas pēc PVN koda.</span><span class="sxs-lookup"><span data-stu-id="69d56-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="69d56-127">Tikai kopsummas</span><span class="sxs-lookup"><span data-stu-id="69d56-127">Totals only</span></span>                | <span data-ttu-id="69d56-128">Iestatiet šo opciju uz **Jā**, lai rādītu tikai kopsummas.</span><span class="sxs-lookup"><span data-stu-id="69d56-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="69d56-129">Tikai galvenie konti</span><span class="sxs-lookup"><span data-stu-id="69d56-129">Main accounts only</span></span>         | <span data-ttu-id="69d56-130">Iestatiet šo opciju uz **Jā**, lai pārskatā iekļautu tikai galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="69d56-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="69d56-131">Rādīt pārskatā tikai ar nodokļiem neapliekamos kontus</span><span class="sxs-lookup"><span data-stu-id="69d56-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="69d56-132">Lai pārskatā rādītu tikai ar nodokļiem neapliekamos kontus, iestatiet filtra nosacījumu, piemēram, zvaigznīti (\*), kā parādīts sekojošajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="69d56-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Pārskats, kas parāda ar nodokļiem neapliekamos kontus](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]