---
title: Debitoru maksājuma metodes izveide
description: Šajā tēmā ir paskaidrots, kā izveidot maksāšanas veidu klientu maksājumiem.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b9960c3fdf0d65be19e28dbb41913a310ae7530
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140218"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="a4185-103">Debitoru maksājuma metodes izveide</span><span class="sxs-lookup"><span data-stu-id="a4185-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4185-104">Šajā tēmā ir paskaidrots, kā izveidot maksāšanas veidu klientu maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="a4185-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="a4185-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="a4185-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a4185-106">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Debitori > Maksājumu iestatīšana > Maksāšanas veidi**.</span><span class="sxs-lookup"><span data-stu-id="a4185-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="a4185-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a4185-107">Select **New**.</span></span>
3. <span data-ttu-id="a4185-108">Laukā **Maksāšanas veids** ievadiet maksāšanas veida ID.</span><span class="sxs-lookup"><span data-stu-id="a4185-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="a4185-109">Maksājuma metodes ID tiek attēlots rēķinos un maksājumos, tāpēc pārliecinieties, ka tas ir pietiekami aprakstošs, lai saprastu, kāda veida maksājums tiek ierakstīts un kurā bankas kontā.</span><span class="sxs-lookup"><span data-stu-id="a4185-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="a4185-110">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="a4185-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a4185-111">Atlasiet, kāds maksājuma statuss ir nepieciešams, lai iegrāmatotu maksājumus.</span><span class="sxs-lookup"><span data-stu-id="a4185-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="a4185-112">Veidojot debitora maksājumu, to var iegrāmatot tikai tad, ja maksājuma statuss atbilst šeit definētajam maksājuma statusam.</span><span class="sxs-lookup"><span data-stu-id="a4185-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="a4185-113">Atlasiet, kā veidot debitoru maksājumus rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="a4185-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="a4185-114">Šī opcija tiek izmantota tikai izpildot maksājuma priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="a4185-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="a4185-115">Maksājuma priekšlikumu var izmantot debitoru maksājumiem, veicot tiešo debetu un velkot līdzekļus no klientu bankas kontiem.</span><span class="sxs-lookup"><span data-stu-id="a4185-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="a4185-116">Atlasiet maksājuma tipu.</span><span class="sxs-lookup"><span data-stu-id="a4185-116">Select the type of payment.</span></span> <span data-ttu-id="a4185-117">Pēc maksājuma tipa var noteikt, vai maksājumam tiks vai netiks veiktas dažādas pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="a4185-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="a4185-118">Atlasiet, uz kādu konta tipu maksājumi tiks grāmatoti.</span><span class="sxs-lookup"><span data-stu-id="a4185-118">Select what account type payments will post to.</span></span> <span data-ttu-id="a4185-119">Parasti šai opcijai jāatlasa Banka.</span><span class="sxs-lookup"><span data-stu-id="a4185-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="a4185-120">Atlasiet bankas kontu, kurā šis maksājums tiks ierakstīts.</span><span class="sxs-lookup"><span data-stu-id="a4185-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="a4185-121">Ievadiet Bankas transakcijas tipu, lai identificētu jūsu bankas izmantoto maksājuma tipu.</span><span class="sxs-lookup"><span data-stu-id="a4185-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="a4185-122">Bankas saskaņošanas procesā tiek izmantots bankas transakcijas tips, kas var atvieglot saskaņošanu.</span><span class="sxs-lookup"><span data-stu-id="a4185-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="a4185-123">Atlasiet, vai šis maksājums īslaicīgi tiks grāmatots pagaidu kontā.</span><span class="sxs-lookup"><span data-stu-id="a4185-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="a4185-124">Vai vēlaties pārbaudīt laiku, kurā maksājums tiek apstrādāts bankā, izmantojiet pagaidu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="a4185-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="a4185-125">Maksājums tiks īslaicīgi iegrāmatots Virsgrāmatas kontā, līdz to apstrādās banka un maksājums tiks pārvietots uz šeit definēto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="a4185-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="a4185-126">Ievadiet galveno kontu, kas tiks izmantots pagaidu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="a4185-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="a4185-127">Šis ir galvenais konts, kurā maksājumu uz laiku iegrāmato, ja izmantojat pagaidu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="a4185-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="a4185-128">Izmantojiet cilni **Faila formāts**, lai noteiktu iestatījumu elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="a4185-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="a4185-129">Izmantojiet cilni **Maksājumu kontroles**, lai noteiktu obligātos laukus.</span><span class="sxs-lookup"><span data-stu-id="a4185-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="a4185-130">Piemēram, ja vēlaties, lai visi šīs maksāšanas metodes maksājumi tiktu deponēti, varat izvēlēties šo opciju šajā cilnē.</span><span class="sxs-lookup"><span data-stu-id="a4185-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="a4185-131">Izmantojiet cilni **Maksājuma atribūti**, lai definētu maksājuma atribūtus, kurus vēlaties izmantot šai maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="a4185-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="a4185-132">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a4185-132">Select **Save**.</span></span>

