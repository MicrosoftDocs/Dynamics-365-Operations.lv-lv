---
title: Kreditora maksājumu papildu maksu definēšana
description: Iestatiet kreditoru maksājumu papildmaksas.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399291a98ddc6b01fb08f7a5c629ec7a6f8acfbf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570272"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="0f051-103">Kreditora maksājumu papildu maksu definēšana</span><span class="sxs-lookup"><span data-stu-id="0f051-103">Define vendor payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f051-104">Iestatiet kreditoru maksājumu papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="0f051-104">Set up vendor payment fees.</span></span> <span data-ttu-id="0f051-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="0f051-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0f051-106">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Komisijas maksa.</span><span class="sxs-lookup"><span data-stu-id="0f051-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="0f051-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0f051-107">Click New.</span></span>
3. <span data-ttu-id="0f051-108">Ierakstiet vērtību laukā Papildmaksas ID.</span><span class="sxs-lookup"><span data-stu-id="0f051-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="0f051-109">Papildmaksas ID ir jānorāda, kad šī papildmaksa tiks izmantota, piemēram, "EFT_Fee".</span><span class="sxs-lookup"><span data-stu-id="0f051-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="0f051-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0f051-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0f051-111">Ierakstiet vērtību laukā Papildmaksas apraksts.</span><span class="sxs-lookup"><span data-stu-id="0f051-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="0f051-112">Pievienojiet aprakstu, kas sniedz vairāk informācijas par gadījumiem, kad šī papildmaksa tiek noteikta.</span><span class="sxs-lookup"><span data-stu-id="0f051-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="0f051-113">Laukā Maksa atlasiet Kreditors vai Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="0f051-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="0f051-114">Ja papildmaksu sedz jūsu organizācija, tiek izmantota Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="0f051-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="0f051-115">Ja papildmaksa tiek noteikta kreditoram, tiek izmantota vērtība Kreditors.</span><span class="sxs-lookup"><span data-stu-id="0f051-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="0f051-116">Ievadiet galveno kontu, kurā papildmaksa tiks iekļauta.</span><span class="sxs-lookup"><span data-stu-id="0f051-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="0f051-117">Šī opcija ir pieejama tikai tad, kad maksas opcijā izvēlēta Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="0f051-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="0f051-118">Atlasiet žurnālu, kurā šī papildmaksa var tikt izmantota.</span><span class="sxs-lookup"><span data-stu-id="0f051-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="0f051-119">Kreditora maksājuma papildmaksai jāatlasa žurnāls Kreditoru rēķinu apmaksa.</span><span class="sxs-lookup"><span data-stu-id="0f051-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="0f051-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0f051-120">Click Save.</span></span>
10. <span data-ttu-id="0f051-121">Noklikšķiniet uz Maksāšanas papildmaksu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="0f051-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="0f051-122">Dodieties uz papildmaksu iestatījumiem, lai definētu, kad atlasītajam žurnālam pēc noklusējuma jāizmanto papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="0f051-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="0f051-123">Atlasiet Tabula, Grupa vai Visi.</span><span class="sxs-lookup"><span data-stu-id="0f051-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="0f051-124">Tabula tiek izmantota, lai atlasītu vienu bankas kontu, Grupa tiek izmantota, lai atlasītu banku grupu, bet vērtība Visi tiek izmantota, lai šo papildmaksu iestatījumus izmantotu visiem bankas kontiem.</span><span class="sxs-lookup"><span data-stu-id="0f051-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="0f051-125">Atlasiet banku grupu vai bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="0f051-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="0f051-126">Ja atlasījāt Grupa, uzmeklēšanā tiks parādītas banku grupas, ja atlasījāt Tabula, uzmeklēšanā tiks parādīti bankas konti.</span><span class="sxs-lookup"><span data-stu-id="0f051-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="0f051-127">Atlasiet maksāšanas metodi, kurai noteikt šo papildmaksu.</span><span class="sxs-lookup"><span data-stu-id="0f051-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="0f051-128">Atlasiet maksājuma specifikāciju atlasītajai maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="0f051-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="0f051-129">Maksājuma specifikācija tiek izmantota maksāšanas metodēm, kas attiecināmas uz elektronisko līdzekļu pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="0f051-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="0f051-130">Atlasiet, vai papildmaksa ir procenti, summa vai intervāls.</span><span class="sxs-lookup"><span data-stu-id="0f051-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="0f051-131">Ievadiet papildmaksas procentuālo daļu vai summu.</span><span class="sxs-lookup"><span data-stu-id="0f051-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="0f051-132">Ja papildmaksa ir procentuāla daļa, ievadiet procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="0f051-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="0f051-133">Ja papildmaksa ir summa, ievadiet papildmaksas summu.</span><span class="sxs-lookup"><span data-stu-id="0f051-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="0f051-134">Ja papildmaksa ir intervāls, pa pakāpēm sadalītu papildmaksu definēšanai izmantojiet cilni Intervāls.</span><span class="sxs-lookup"><span data-stu-id="0f051-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="0f051-135">Laukā Papildmaksas valūta atlasiet valūtu, kurā papildmaksa tiek noteikta.</span><span class="sxs-lookup"><span data-stu-id="0f051-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="0f051-136">Šī valūta attiecas uz papildmaksu.</span><span class="sxs-lookup"><span data-stu-id="0f051-136">This currency is for the fee.</span></span> <span data-ttu-id="0f051-137">Apmaksas valūta tiek izmantota, lai definētu to, kad papildmaksas kārtula ir jānovērtē, pamatojoties uz maksājuma valūtu.</span><span class="sxs-lookup"><span data-stu-id="0f051-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="0f051-138">Piemēram, jūsu banka var iekasēt komisijas maksu, kad maksājums tiek veikts EUR, bet citiem maksājumiem komisijas maksa netiek noteikta.</span><span class="sxs-lookup"><span data-stu-id="0f051-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="0f051-139">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0f051-139">Click Save.</span></span>

