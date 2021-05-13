---
title: Nodokļu aprēķina veiktspēja ietekmē transakcijas
description: Šajā tēmā sniegta traucējummeklēšanas informācija, kas saistīta ar nodokļu aprēķina veiktspēju un tās ietekmi uz transakcijām.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947677"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="62a42-103">Nodokļu aprēķina veiktspēja ietekmē transakcijas</span><span class="sxs-lookup"><span data-stu-id="62a42-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62a42-104">Dažreiz transakciju ietekmē veiktspējas problēmas, kas saistītas ar nodokļu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="62a42-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="62a42-105">Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="62a42-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="62a42-106">Pārskatītiet transakcijas rindu skaitu</span><span class="sxs-lookup"><span data-stu-id="62a42-106">Review the transaction line count</span></span>

<span data-ttu-id="62a42-107">Nosakiet, vai transakcijai ir liels rindu skaits (piemēram, vairāk nekā vairāki simti).</span><span class="sxs-lookup"><span data-stu-id="62a42-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="62a42-108">Ja tā nav, pārejiet uz nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="62a42-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="62a42-109">Ja transakcijai ir vairāki simti rindu, aizturiet nodokļu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="62a42-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="62a42-110">Papildinformācijai skatiet [Iespējot kavētu nodokļu aprēķinu žurnāliem](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="62a42-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="62a42-111">Pēc tam varat noteikt, vai ir spēkā kāds no šiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="62a42-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="62a42-112">Pastāv importa transakcijas no lieliem failiem.</span><span class="sxs-lookup"><span data-stu-id="62a42-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="62a42-113">Vairākas sesijas vienlaicīgi apstrādā vienu un to pašu transakciju nodokļu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="62a42-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="62a42-114">Transakcijai ir vairākas rindas, un skati tiek atjaunināti reāllaikā.</span><span class="sxs-lookup"><span data-stu-id="62a42-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="62a42-115">Piemēram, lauks **Aprēķinātā PVN summa** lapā **Virsgrāmatas žurnāls** tiek atjaunināts reāllaikā, mainot rindas laukus.</span><span class="sxs-lookup"><span data-stu-id="62a42-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="62a42-116">[![Aprēķinātās PVN summas lauks Žurnāla dokumenta lapā](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="62a42-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="62a42-117">Ja ir izpildīts kāds no šiem nosacījumiem, nodokļu aprēķins tiek atlikts.</span><span class="sxs-lookup"><span data-stu-id="62a42-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="62a42-118">Pārskatīt izsaukumu steku</span><span class="sxs-lookup"><span data-stu-id="62a42-118">Review the call stack</span></span>

<span data-ttu-id="62a42-119">Pārskatīt izsaukumu steku, lai noteiktu, vai nodokļu aprēķins tiek izsaukts vairākas reizes.</span><span class="sxs-lookup"><span data-stu-id="62a42-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="62a42-120">Ja tas nav, pārejiet uz nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="62a42-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="62a42-121">Ja izsaukuma steks tiek izsaukts vairākas reizes, rīkojieties šādi, lai palīdzētu samazināt nodokļu aprēķināšanas laikus.</span><span class="sxs-lookup"><span data-stu-id="62a42-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="62a42-122">Ja žurnāls ir apsvēris transakciju, atlieciet nodokļu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="62a42-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="62a42-123">Papildinformācijai skatiet [Iespējot kavētu nodokļu aprēķinu žurnāliem](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="62a42-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="62a42-124">Ja transakcija ir pirkšanas pasūtījums un pieteikuma versija ir vēlāka par 10.0.15, nodokļu aprēķinu var atlikt līdz beigu aprēķinam, iespējojot **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** testējamā varianta sniegšanu.</span><span class="sxs-lookup"><span data-stu-id="62a42-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="62a42-125">Pārskatīt izsaukumu steku laika skalu</span><span class="sxs-lookup"><span data-stu-id="62a42-125">Review the call stack timeline</span></span>

<span data-ttu-id="62a42-126">Pārskatiet izsaukumu steka laika skalu, lai noteiktu, vai pastāv šādas problēmas.</span><span class="sxs-lookup"><span data-stu-id="62a42-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="62a42-127">Ja tā ir, iespējojiet **TaxUncommittedDoIsolateScopeFlighting** testējamā varianta sniegšanu, lai novērstu šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="62a42-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="62a42-128">Transakcijas dēļ sistēma pārstāj reaģēt līdz sesijas beigām.</span><span class="sxs-lookup"><span data-stu-id="62a42-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="62a42-129">Tādējādi transakcija nevar aprēķināt nodokļu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="62a42-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="62a42-130">Šajā attēlā parādīts saņemtā ziņojuma lodziņš "Sesija pabeigta".</span><span class="sxs-lookup"><span data-stu-id="62a42-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="62a42-131">[![Ziņojums Sesija pabeigta](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="62a42-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="62a42-132">Metodes **TaxUncommitted** aizņem vairāk laika nekā citas metodes.</span><span class="sxs-lookup"><span data-stu-id="62a42-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="62a42-133">Piemēram, šajā ilustrācijā **TaxUncommitted::updateTaxUncommitted()** metode aizņem 43 347,42 sekundes, bet citas metodes aizņem 0,09 sekundes.</span><span class="sxs-lookup"><span data-stu-id="62a42-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="62a42-134">[![Metodes ilgums](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="62a42-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="62a42-135">Nodokļu aprēķina pielāgošana un izsaukšana</span><span class="sxs-lookup"><span data-stu-id="62a42-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="62a42-136">Pielāgojot netiek izsaukts nodokļu aprēķins katras rindas metodē **ievietot()** vai **atjaunināt()**.</span><span class="sxs-lookup"><span data-stu-id="62a42-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="62a42-137">Nodokļu aprēķins jāizsauc transakciju līmenī.</span><span class="sxs-lookup"><span data-stu-id="62a42-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="62a42-138">Noteikt, vai pielāgojums pastāv</span><span class="sxs-lookup"><span data-stu-id="62a42-138">Determine whether customization exists</span></span>

<span data-ttu-id="62a42-139">Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē.</span><span class="sxs-lookup"><span data-stu-id="62a42-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="62a42-140">Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.</span><span class="sxs-lookup"><span data-stu-id="62a42-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
