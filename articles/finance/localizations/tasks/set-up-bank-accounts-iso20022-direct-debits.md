---
title: Debitoru un debitoru bankas kontu iestatīšana ISO20022 tiešajiem debetiem
description: Šajā uzdevumā ir izklāstīts, kā iestatīt debitora bankas kontu un debitora tiešā debeta pilnvarojumu, kas ir nepieciešami, lai ģenerētu debitora maksājumu failu kā ISO20022 tiešo debetu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85c1faebe9a61ad2e708ba26c7a5f0cad15f5f8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988205"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="6b853-103">Debitoru un debitoru bankas kontu iestatīšana ISO20022 tiešajiem debetiem</span><span class="sxs-lookup"><span data-stu-id="6b853-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b853-104">Šajā uzdevumā ir izklāstīts, kā iestatīt debitora bankas kontu un debitora tiešā debeta pilnvarojumu, kas ir nepieciešami, lai ģenerētu debitora maksājumu failu kā ISO20022 tiešo debetu.</span><span class="sxs-lookup"><span data-stu-id="6b853-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="6b853-105">Atkarībā no debitora maksājuma formātiem, kas ir iestatīti, papildu informācija, kas nav iekļauta šajā procedūrā, var būt nepieciešama debitoram vai debitora bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="6b853-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="6b853-106">Šis uzdevums ir izveidots, izmantojot demonstrācijas uzņēmuma DEMF datus, norādot Vāciju kā juridiskās personas primārās adreses valsti.</span><span class="sxs-lookup"><span data-stu-id="6b853-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="6b853-107">Šis ir ceturtā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6b853-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="6b853-108">Debitora bankas konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6b853-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="6b853-109">Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="6b853-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="6b853-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="6b853-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6b853-111">Piemēram, filtrējiet pēc lauka Konts vērtības DE-010.</span><span class="sxs-lookup"><span data-stu-id="6b853-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="6b853-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6b853-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6b853-113">Darbību rūtī noklikšķiniet uz Debitors.</span><span class="sxs-lookup"><span data-stu-id="6b853-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="6b853-114">Noklikšķiniet uz Banku konti.</span><span class="sxs-lookup"><span data-stu-id="6b853-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="6b853-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6b853-115">Click New.</span></span>
7. <span data-ttu-id="6b853-116">Ierakstiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="6b853-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="6b853-117">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6b853-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6b853-118">Piemēram, ievadiet 'EUR banka'.</span><span class="sxs-lookup"><span data-stu-id="6b853-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="6b853-119">Ievadiet vai atlasiet vērtību laukā Banku grupas.</span><span class="sxs-lookup"><span data-stu-id="6b853-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="6b853-120">Ievadiet vērtību laukā IBAN.</span><span class="sxs-lookup"><span data-stu-id="6b853-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="6b853-121">Piemēram, ievadiet 'DE36200400000628808808'.</span><span class="sxs-lookup"><span data-stu-id="6b853-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="6b853-122">Ierakstiet vērtību laukā SWIFT kods.</span><span class="sxs-lookup"><span data-stu-id="6b853-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="6b853-123">Piemēram, ievadiet COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="6b853-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="6b853-124">Lūdzu, ņemiet vērā, ka SWIFT\BIC nav nepieciešami daudziem maksājumu formātiem, tomēr ir ieteicams reģistrēt to bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="6b853-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="6b853-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6b853-125">Click Save.</span></span>
13. <span data-ttu-id="6b853-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6b853-126">Close the page.</span></span>
14. <span data-ttu-id="6b853-127">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="6b853-127">Click Edit.</span></span>
15. <span data-ttu-id="6b853-128">Izvērsiet Maksāšanas noklusējuma sadaļu.</span><span class="sxs-lookup"><span data-stu-id="6b853-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="6b853-129">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="6b853-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="6b853-130">Tiešā debeta pilnvarojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="6b853-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="6b853-131">Izvērsiet sadaļu Tiešā debeta pilnvarojumi.</span><span class="sxs-lookup"><span data-stu-id="6b853-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="6b853-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="6b853-132">Click Add.</span></span>
3. <span data-ttu-id="6b853-133">Laukā Kreditora bankas konts, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6b853-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="6b853-134">Piemēram, atlasiet DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="6b853-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="6b853-135">Ievadiet datumu laukā Parakstīšanas datums.</span><span class="sxs-lookup"><span data-stu-id="6b853-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="6b853-136">Noklikšķiniet uz Jā, lai apstiprinātu datuma atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="6b853-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="6b853-137">Ievadiet vai atlasiet vērtību laukā Parakstīšanas vieta.</span><span class="sxs-lookup"><span data-stu-id="6b853-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="6b853-138">Ievadiet skaitli laukā Sagaidāmais maksājumu skaits.</span><span class="sxs-lookup"><span data-stu-id="6b853-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="6b853-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6b853-139">Click OK.</span></span>
9. <span data-ttu-id="6b853-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6b853-140">Click Save.</span></span>

