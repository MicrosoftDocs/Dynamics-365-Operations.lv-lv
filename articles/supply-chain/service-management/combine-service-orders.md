---
title: Kombinēt pakalpojumu pasūtījumus
description: Varat kombinēt pakalpojuma pasūtījumus.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571965"
---
# <a name="combine-service-orders"></a><span data-ttu-id="a561e-103">Kombinēt pakalpojumu pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="a561e-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a561e-104">Kad veidojat pakalpojuma pasūtījuma rindas automātiski veidlapā **Pakalpojumu līgumi**, var izvēlēties vienu no šīm opcijām, lai norādītu, kā grupēt tās.</span><span class="sxs-lookup"><span data-stu-id="a561e-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="a561e-105">**Pa pakalpojumu līgumiem**</span><span class="sxs-lookup"><span data-stu-id="a561e-105">**By service agreement**</span></span>

  - <span data-ttu-id="a561e-106">**Pa pakalpojumu uzdevumiem**</span><span class="sxs-lookup"><span data-stu-id="a561e-106">**By service task**</span></span>

  - <span data-ttu-id="a561e-107">**Pa darbiniekiem**</span><span class="sxs-lookup"><span data-stu-id="a561e-107">**By employee**</span></span>

  - <span data-ttu-id="a561e-108">**Pa pakalpojumu objektiem**</span><span class="sxs-lookup"><span data-stu-id="a561e-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="a561e-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a561e-109">Example</span></span>

<span data-ttu-id="a561e-110">Jūs izveidojat pakalpojuma līgumu, kam ir sākuma datums 03.31.2007.</span><span class="sxs-lookup"><span data-stu-id="a561e-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="a561e-111">Laukā **Kombinēt pakalpojumu pasūtījumus** atlasiet **Pēc pakalpojuma objekta**.</span><span class="sxs-lookup"><span data-stu-id="a561e-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="a561e-112">Pēc tam izveidojat šādas pakalpojumu līguma rindas:</span><span class="sxs-lookup"><span data-stu-id="a561e-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a561e-113">Līguma rindas numurs</span><span class="sxs-lookup"><span data-stu-id="a561e-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="a561e-114">Darbības veids</span><span class="sxs-lookup"><span data-stu-id="a561e-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="a561e-115">apraksts</span><span class="sxs-lookup"><span data-stu-id="a561e-115">Description</span></span></p></th>
<th><p><span data-ttu-id="a561e-116">Intervāls</span><span class="sxs-lookup"><span data-stu-id="a561e-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="a561e-117">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="a561e-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="a561e-118">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="a561e-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a561e-119">1</span><span class="sxs-lookup"><span data-stu-id="a561e-119">1</span></span></p></td>
<td><p><span data-ttu-id="a561e-120"><strong>Stundas</strong></span><span class="sxs-lookup"><span data-stu-id="a561e-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="a561e-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="a561e-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="a561e-122">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="a561e-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="a561e-123">X-1</span><span class="sxs-lookup"><span data-stu-id="a561e-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="a561e-124">04.01.2007.</span><span class="sxs-lookup"><span data-stu-id="a561e-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a561e-125">2</span><span class="sxs-lookup"><span data-stu-id="a561e-125">2</span></span></p></td>
<td><p><span data-ttu-id="a561e-126"><strong>Stundas</strong></span><span class="sxs-lookup"><span data-stu-id="a561e-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="a561e-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="a561e-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="a561e-128">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="a561e-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="a561e-129">X-2</span><span class="sxs-lookup"><span data-stu-id="a561e-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="a561e-130">04.01.2007.</span><span class="sxs-lookup"><span data-stu-id="a561e-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a561e-131">3</span><span class="sxs-lookup"><span data-stu-id="a561e-131">3</span></span></p></td>
<td><p><span data-ttu-id="a561e-132"><strong>Stundas</strong></span><span class="sxs-lookup"><span data-stu-id="a561e-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="a561e-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="a561e-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="a561e-134">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="a561e-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="a561e-135">X-2</span><span class="sxs-lookup"><span data-stu-id="a561e-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="a561e-136">04.01.2007.</span><span class="sxs-lookup"><span data-stu-id="a561e-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a561e-137">Laika logu nenorāda nevienai pakalpojumu līguma rindai.</span><span class="sxs-lookup"><span data-stu-id="a561e-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="a561e-138">Tādēļ pakalpojuma pasūtījuma rindas netiks pārvietotas no aprēķinātā datuma, kurā tās ievietotas.</span><span class="sxs-lookup"><span data-stu-id="a561e-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="a561e-139">Pēc tam izveidojiet pakalpojuma pasūtījumu rindas no veidlapas **Pakalpojuma pasūtījumu izveide** no 01.04.2007. līdz 30.04.2007.</span><span class="sxs-lookup"><span data-stu-id="a561e-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="a561e-140">Kopā tiek izveidoti 10 pakalpojuma pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="a561e-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="a561e-141">Tā kā atlasījāt kombinēto iestatījumu **Pēc pakalpojuma objekta**, visiem izveidotajiem pakalpojuma pasūtījumiem ir tikai pakalpojuma pasūtījuma rindas ar vienu noteiktu pakalpojuma objektu.</span><span class="sxs-lookup"><span data-stu-id="a561e-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="a561e-142">Pakalpojuma pasūtījuma rindas, kas izveidotas no viena pakalpojumu līguma un kurām ir viens pakalpojuma datums un objekts, tiek kombinētas vienā pakalpojuma pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="a561e-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a561e-143">Šajā piemērā veidlapā <STRONG>Pakalpojumu līgumu parametri</STRONG> norādītajā kalendārā nav slēgtu dienu.</span><span class="sxs-lookup"><span data-stu-id="a561e-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="a561e-144">Papildu pakalpojumu pasūtījumu rindu grupēšana pakalpojumu pasūtījumos notiek saskaņā ar jebkuru laika logu, ko nosakāt pakalpojuma līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="a561e-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="a561e-145">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="a561e-145">See also</span></span>

[<span data-ttu-id="a561e-146">Automātiska pakalpojuma pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="a561e-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


