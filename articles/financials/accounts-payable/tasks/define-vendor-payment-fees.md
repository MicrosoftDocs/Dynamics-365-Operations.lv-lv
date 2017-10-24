--- 
title: "Kreditora maksājumu papildu maksu definēšana"
description: "Iestatiet kreditoru maksājumu papildmaksas."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f62d07ffa1ee4a525f0f266922bc88e5ac8d5ada
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="b771b-103">Kreditora maksājumu papildu maksu definēšana</span><span class="sxs-lookup"><span data-stu-id="b771b-103">Define vendor payment fees</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b771b-104">Iestatiet kreditoru maksājumu papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="b771b-104">Set up vendor payment fees.</span></span> <span data-ttu-id="b771b-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="b771b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b771b-106">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Komisijas maksa.</span><span class="sxs-lookup"><span data-stu-id="b771b-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="b771b-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b771b-107">Click New.</span></span>
3. <span data-ttu-id="b771b-108">Ierakstiet vērtību laukā Papildmaksas ID.</span><span class="sxs-lookup"><span data-stu-id="b771b-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="b771b-109">Papildmaksas ID ir jānorāda, kad šī papildmaksa tiks izmantota, piemēram, "EFT_Fee".</span><span class="sxs-lookup"><span data-stu-id="b771b-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="b771b-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b771b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b771b-111">Ierakstiet vērtību laukā Papildmaksas apraksts.</span><span class="sxs-lookup"><span data-stu-id="b771b-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="b771b-112">Pievienojiet aprakstu, kas sniedz vairāk informācijas par gadījumiem, kad šī papildmaksa tiek noteikta.</span><span class="sxs-lookup"><span data-stu-id="b771b-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="b771b-113">Laukā Maksa atlasiet Kreditors vai Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="b771b-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="b771b-114">Ja papildmaksu sedz jūsu organizācija, tiek izmantota Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="b771b-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="b771b-115">Ja papildmaksa tiek noteikta kreditoram, tiek izmantota vērtība Kreditors.</span><span class="sxs-lookup"><span data-stu-id="b771b-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="b771b-116">Ievadiet galveno kontu, kurā papildmaksa tiks iekļauta.</span><span class="sxs-lookup"><span data-stu-id="b771b-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="b771b-117">Šī opcija ir pieejama tikai tad, kad maksas opcijā izvēlēta Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="b771b-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="b771b-118">Atlasiet žurnālu, kurā šī papildmaksa var tikt izmantota.</span><span class="sxs-lookup"><span data-stu-id="b771b-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="b771b-119">Kreditora maksājuma papildmaksai jāatlasa žurnāls Kreditoru rēķinu apmaksa.</span><span class="sxs-lookup"><span data-stu-id="b771b-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="b771b-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b771b-120">Click Save.</span></span>
10. <span data-ttu-id="b771b-121">Noklikšķiniet uz Maksāšanas papildmaksu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="b771b-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="b771b-122">Dodieties uz papildmaksu iestatījumiem, lai definētu, kad atlasītajam žurnālam pēc noklusējuma jāizmanto papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="b771b-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="b771b-123">Atlasiet Tabula, Grupa vai Visi.</span><span class="sxs-lookup"><span data-stu-id="b771b-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="b771b-124">Tabula tiek izmantota, lai atlasītu vienu bankas kontu, Grupa tiek izmantota, lai atlasītu banku grupu, bet vērtība Visi tiek izmantota, lai šo papildmaksu iestatījumus izmantotu visiem bankas kontiem.</span><span class="sxs-lookup"><span data-stu-id="b771b-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="b771b-125">Atlasiet banku grupu vai bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="b771b-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="b771b-126">Ja atlasījāt Grupa, uzmeklēšanā tiks parādītas banku grupas, ja atlasījāt Tabula, uzmeklēšanā tiks parādīti bankas konti.</span><span class="sxs-lookup"><span data-stu-id="b771b-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="b771b-127">Atlasiet maksāšanas metodi, kurai noteikt šo papildmaksu.</span><span class="sxs-lookup"><span data-stu-id="b771b-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="b771b-128">Atlasiet maksājuma specifikāciju atlasītajai maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="b771b-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="b771b-129">Maksājuma specifikācija tiek izmantota maksāšanas metodēm, kas attiecināmas uz elektronisko līdzekļu pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="b771b-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="b771b-130">Atlasiet, vai papildmaksa ir procenti, summa vai intervāls.</span><span class="sxs-lookup"><span data-stu-id="b771b-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="b771b-131">Ievadiet papildmaksas procentuālo daļu vai summu.</span><span class="sxs-lookup"><span data-stu-id="b771b-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="b771b-132">Ja papildmaksa ir procentuāla daļa, ievadiet procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="b771b-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="b771b-133">Ja papildmaksa ir summa, ievadiet papildmaksas summu.</span><span class="sxs-lookup"><span data-stu-id="b771b-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="b771b-134">Ja papildmaksa ir intervāls, pa pakāpēm sadalītu papildmaksu definēšanai izmantojiet cilni Intervāls.</span><span class="sxs-lookup"><span data-stu-id="b771b-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="b771b-135">Laukā Papildmaksas valūta atlasiet valūtu, kurā papildmaksa tiek noteikta.</span><span class="sxs-lookup"><span data-stu-id="b771b-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="b771b-136">Šī valūta attiecas uz papildmaksu.</span><span class="sxs-lookup"><span data-stu-id="b771b-136">This currency is for the fee.</span></span> <span data-ttu-id="b771b-137">Apmaksas valūta tiek izmantota, lai definētu to, kad papildmaksas kārtula ir jānovērtē, pamatojoties uz maksājuma valūtu.</span><span class="sxs-lookup"><span data-stu-id="b771b-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="b771b-138">Piemēram, jūsu banka var iekasēt komisijas maksu, kad maksājums tiek veikts EUR, bet citiem maksājumiem komisijas maksa netiek noteikta.</span><span class="sxs-lookup"><span data-stu-id="b771b-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="b771b-139">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b771b-139">Click Save.</span></span>


