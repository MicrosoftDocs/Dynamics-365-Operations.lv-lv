---
title: Peļņas vai zaudējumu aprēķina finanšu pārskats
description: Šajā rakstā ir aprakstīts peļņas vai zaudējumu aprēķina noklusējuma pārskats. Tajā ir aprakstīti arī ar šo pārskatu saistītie veidošanas bloki.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146d4b9946c1b29105cff637fa9d8803db3d0c0f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988781"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="6ed91-104">Peļņas vai zaudējumu aprēķina finanšu pārskats</span><span class="sxs-lookup"><span data-stu-id="6ed91-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ed91-105">Šajā rakstā ir aprakstīts peļņas vai zaudējumu aprēķina noklusējuma pārskats.</span><span class="sxs-lookup"><span data-stu-id="6ed91-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="6ed91-106">Tajā ir aprakstīti arī ar šo pārskatu saistītie veidošanas bloki.</span><span class="sxs-lookup"><span data-stu-id="6ed91-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="6ed91-107">Noklusējuma peļņas vai zaudējumu aprēķina pārskats</span><span class="sxs-lookup"><span data-stu-id="6ed91-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="6ed91-108">Noklusējuma pārskats</span><span class="sxs-lookup"><span data-stu-id="6ed91-108">Default report</span></span>             | <span data-ttu-id="6ed91-109">Ko tā dara</span><span class="sxs-lookup"><span data-stu-id="6ed91-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed91-110">Peļņas vai zaudējumu aprēķins — noklusējums</span><span class="sxs-lookup"><span data-stu-id="6ed91-110">Income Statement – Default</span></span> | <span data-ttu-id="6ed91-111">Sniedz organizācijas ienesīguma pārskatu pašreizējam periodam un arī šim gadam.</span><span class="sxs-lookup"><span data-stu-id="6ed91-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="6ed91-112">Veidošanas bloki</span><span class="sxs-lookup"><span data-stu-id="6ed91-112">Building blocks</span></span>
<span data-ttu-id="6ed91-113">Peļņas vai zaudējumu aprēķina finanšu pārskats izmanto tālāk aprakstītos veidošanas blokus.</span><span class="sxs-lookup"><span data-stu-id="6ed91-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="6ed91-114">Noklusējuma atskaite</span><span class="sxs-lookup"><span data-stu-id="6ed91-114">Default report</span></span>             | <span data-ttu-id="6ed91-115">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="6ed91-115">Row definition</span></span>                     | <span data-ttu-id="6ed91-116">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="6ed91-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="6ed91-117">Peļņas vai zaudējumu aprēķins — noklusējums</span><span class="sxs-lookup"><span data-stu-id="6ed91-117">Income Statement - Default</span></span> | <span data-ttu-id="6ed91-118">Kopsavilkuma peļņas vai zaudējumu aprēķins — noklusējums</span><span class="sxs-lookup"><span data-stu-id="6ed91-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="6ed91-119">Periodisks un šī gada - noklusējuma</span><span class="sxs-lookup"><span data-stu-id="6ed91-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="6ed91-120">Rindas definīcija</span><span class="sxs-lookup"><span data-stu-id="6ed91-120">Row definition</span></span>

<span data-ttu-id="6ed91-121">Rindas definīcijā "kopsavilkuma peļņas vai zaudējumu aprēķins — noklusējuma" iekļauta sadaļa katrai tradicionālā aprēķina daļai.</span><span class="sxs-lookup"><span data-stu-id="6ed91-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="6ed91-122">Šīs rindas definīcijas izveidē tiek izmantota galvenā konta kategorijas dimensija.</span><span class="sxs-lookup"><span data-stu-id="6ed91-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="6ed91-123">Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas.</span><span class="sxs-lookup"><span data-stu-id="6ed91-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="6ed91-124">Kolonnas definīcija</span><span class="sxs-lookup"><span data-stu-id="6ed91-124">Column Definition</span></span>

<span data-ttu-id="6ed91-125">Kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.</span><span class="sxs-lookup"><span data-stu-id="6ed91-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="6ed91-126">**Periodisks un šī gada – noklusējuma kolonnu tipi**</span><span class="sxs-lookup"><span data-stu-id="6ed91-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="6ed91-127">**DESC** — apraksts no rindas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="6ed91-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="6ed91-128">**FD** — finanšu dati par pašreizējo periodu.</span><span class="sxs-lookup"><span data-stu-id="6ed91-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="6ed91-129">**FD** — finanšu dati par šo gadu.</span><span class="sxs-lookup"><span data-stu-id="6ed91-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="6ed91-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6ed91-130">Additional resources</span></span>
--------

[<span data-ttu-id="6ed91-131">Finanšu pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="6ed91-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="6ed91-132">Finanšu pārskatu skatīšana</span><span class="sxs-lookup"><span data-stu-id="6ed91-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="6ed91-133">Dynamics finanšu pārskatu veidošanas emuārs</span><span class="sxs-lookup"><span data-stu-id="6ed91-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



