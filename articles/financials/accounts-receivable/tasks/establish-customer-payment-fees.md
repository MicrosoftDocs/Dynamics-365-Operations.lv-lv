--- 
title: "Debitoru maksājumu papildu maksu izveide"
description: "Izveidojiet maksāšanas papildmaksas debitoru maksājumiem."
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 02449aff2273d30e0d0d847e137e3283aef1839b
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="7abab-103">Debitoru maksājumu papildu maksu izveide</span><span class="sxs-lookup"><span data-stu-id="7abab-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7abab-104">Izveidojiet maksāšanas papildmaksas debitoru maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="7abab-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="7abab-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="7abab-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="7abab-106">Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Komisijas maksa.</span><span class="sxs-lookup"><span data-stu-id="7abab-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="7abab-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7abab-107">Click New.</span></span>
3. <span data-ttu-id="7abab-108">Ievadiet papildmaksas ID laukā Papildmaksas ID.</span><span class="sxs-lookup"><span data-stu-id="7abab-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="7abab-109">Papildmaksas ID tiek attēlots maksājumu žurnālos, tāpēc pārliecinieties, ka tas ir aprakstošs un palīdz saprast papildmaksas veidu.</span><span class="sxs-lookup"><span data-stu-id="7abab-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="7abab-110">Ievadiet papildmaksas nosaukumu laukā Nosaukums.</span><span class="sxs-lookup"><span data-stu-id="7abab-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="7abab-111">Ievadiet papildmaksas aprakstu laukā Papildmaksas apraksts.</span><span class="sxs-lookup"><span data-stu-id="7abab-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="7abab-112">Atlasiet, vai papildmaksa tiks attiecināta uz debitoru vai Virsgrāmatas kontu.</span><span class="sxs-lookup"><span data-stu-id="7abab-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="7abab-113">Ja debitors tiek aplikts ar papildmaksu, izvēlieties Debitors.</span><span class="sxs-lookup"><span data-stu-id="7abab-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="7abab-114">Ja ar papildmaksu tiks aplikta jūsu organizācija, atlasiet Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="7abab-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="7abab-115">Šajā uzdevumā atlasiet Debitors.</span><span class="sxs-lookup"><span data-stu-id="7abab-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="7abab-116">Atlasiet žurnāla tipu, kurā atļauts izmantot šo papildmaksu.</span><span class="sxs-lookup"><span data-stu-id="7abab-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="7abab-117">Ja šīs papildmaksas tiek izmantotas debitoru maksājumiem, žurnāla tips visdrīzāk būs Debitora maksājumi.</span><span class="sxs-lookup"><span data-stu-id="7abab-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="7abab-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7abab-118">Click Save.</span></span>
9. <span data-ttu-id="7abab-119">Noklikšķiniet uz Maksāšanas papildmaksu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="7abab-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="7abab-120">Maksājuma papildmaksas iestatījumi tiek izmantoti kritēriju definēšanai, lai noteiktu, kad tiks noteikta papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="7abab-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="7abab-121">Piemēram, varat definēt, ka papildmaksa tiks aprēķināta, ja bankas konts ir USMF OPER un maksāšanas metode ir čeks.</span><span class="sxs-lookup"><span data-stu-id="7abab-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="7abab-122">Lai definētu, kuriem bankas kontiem tiks noteikta šī papildmaksa, atlasiet Tabula, Grupa vai Visi.</span><span class="sxs-lookup"><span data-stu-id="7abab-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="7abab-123">Ja atlasāt Visi, šī papildmaksa var tikt piemērota visiem bankas kontiem.</span><span class="sxs-lookup"><span data-stu-id="7abab-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="7abab-124">Ja atlasāt Tabula, šī papildmaksa var tikt piemērota tikai izvēlētajam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="7abab-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="7abab-125">Ja atlasāt Grupa, šī papildmaksa var tikt piemērota tikai bankas kontiem, kas pieder atlasītajai banku grupai.</span><span class="sxs-lookup"><span data-stu-id="7abab-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="7abab-126">Atlasiet banku grupu vai bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="7abab-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="7abab-127">Atlasot Tabula, bankas konti tiks attēloti, izmantojot uzmeklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="7abab-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="7abab-128">Atlasot Grupa, banku grupas tiks attēlotas, izmantojot uzmeklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="7abab-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="7abab-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7abab-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7abab-130">Atlasiet maksāšanas metodi, kurai noteikt šo papildmaksu.</span><span class="sxs-lookup"><span data-stu-id="7abab-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="7abab-131">Piemēram, varat noteikt papildmaksu klientiem, ja tie veic maksājumus, izmantojot čekus nevis elektronisko maksājumu.</span><span class="sxs-lookup"><span data-stu-id="7abab-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="7abab-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7abab-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="7abab-133">Ja nepieciešams, ievadiet maksāšanas valūtu.</span><span class="sxs-lookup"><span data-stu-id="7abab-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="7abab-134">Apmaksas valūta tiek izmantota kā papildu kritērijs, lai definētu, vai tiks noteikta papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="7abab-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="7abab-135">Piemēram, jūsu banka var iekasēt papildu maksu par maksājumiem, kas saņemti USD valūtā, jo tā parasti veic operācijas tikai EUR valūtā.</span><span class="sxs-lookup"><span data-stu-id="7abab-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="7abab-136">Atlasiet, vai papildmaksa būs procenti, summa vai intervāls.</span><span class="sxs-lookup"><span data-stu-id="7abab-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="7abab-137">Ievadiet papildmaksas procentus vai summu.</span><span class="sxs-lookup"><span data-stu-id="7abab-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="7abab-138">Ja laukā Procenti/Summa ir atlasīta vērtība Procenti, šeit ievadītā vērtība būs procentuālā daļa.</span><span class="sxs-lookup"><span data-stu-id="7abab-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="7abab-139">Ja laukā Procenti/Summa ir atlasīta vērtība Summa, šeit ievadītā vērtība būs summa.</span><span class="sxs-lookup"><span data-stu-id="7abab-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="7abab-140">Ja laukā Procenti/Summa ir atlasīta vērtība Intervāls, pakāpju definēšanai izmantojiet cilni Intervāls.</span><span class="sxs-lookup"><span data-stu-id="7abab-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="7abab-141">Atlasiet papildmaksas valūtu laukā Papildmaksas valūta.</span><span class="sxs-lookup"><span data-stu-id="7abab-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="7abab-142">Šī ir valūta, kurā tiks izveidota papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="7abab-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="7abab-143">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7abab-143">Click Save.</span></span>


