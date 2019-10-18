---
title: Stornēt žurnāla grāmatošanu
description: Šajā tēmā ir aprakstītas iespējas, kas ļauj stornēt dokumentus no dokumentu darbību saraksta vai finanšu žurnāliem.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248589"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="a7322-103">Stornēt žurnāla grāmatošanu</span><span class="sxs-lookup"><span data-stu-id="a7322-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7322-104">Šajā tēmā ir aprakstītas iespējas Microsoft Dynamics 365 Finance , kas ļauj stornēt visu žurnālu vai stornēt vienu vai vairākus dokumentus no dokumentu darbību saraksta neatkarīgi no to izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="a7322-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="a7322-105">Stornējot žurnālus</span><span class="sxs-lookup"><span data-stu-id="a7322-105">Reversing journals</span></span>

<span data-ttu-id="a7322-106">Varat stornēt žurnāla rindas atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="a7322-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="a7322-107">Ar stornēto žurnāla grāmatošanu, var arī stornēt visu finanšu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="a7322-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="a7322-108">Stornēt žurnālu:</span><span class="sxs-lookup"><span data-stu-id="a7322-108">To reverse a journal:</span></span> 
- <span data-ttu-id="a7322-109">Atvēriet finanšu žurnālu un filtrējiet grāmatotos žurnālus</span><span class="sxs-lookup"><span data-stu-id="a7322-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="a7322-110">Noklikšķiniet uz Stornēt izvēlnes lapas augšdaļā</span><span class="sxs-lookup"><span data-stu-id="a7322-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="a7322-111">Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="a7322-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="a7322-112">Atlasiet Jā, lai izmantotu esošos darbību datumus, vai Nē, lai ievadītu jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="a7322-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="a7322-113">Dažos gadījumos, sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="a7322-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="a7322-114">Ja jūs atlasījāt Nē, ievadiet darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="a7322-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="a7322-115">Ievadiet komentārā, ko vēlaties pievienot stornētai darbībai</span><span class="sxs-lookup"><span data-stu-id="a7322-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="a7322-116">Noklikšķināt uz pogas Stornēt.</span><span class="sxs-lookup"><span data-stu-id="a7322-116">Click the Reverse button</span></span>

<span data-ttu-id="a7322-117">Darbības tiks stornētās.</span><span class="sxs-lookup"><span data-stu-id="a7322-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="a7322-118">Ja dokumenta rindu skaits pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi.</span><span class="sxs-lookup"><span data-stu-id="a7322-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="a7322-119">Stornēšanas rezultātus var pārskatīt, apskatot komentārus palaistajā pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="a7322-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="a7322-120">Visas kļūmes tiks atzīmētas pakešuzdevuma vēsturē.</span><span class="sxs-lookup"><span data-stu-id="a7322-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="a7322-121">Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="a7322-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="a7322-122">Rezultāti tiks parādīti dialogā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, un iemeslu, kāpēc to nevarēja stornēt.</span><span class="sxs-lookup"><span data-stu-id="a7322-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="a7322-123">Noklikšķiniet uz Labi, lai aizvērtu dialogu.</span><span class="sxs-lookup"><span data-stu-id="a7322-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="a7322-124">Stornējot dokumentus no dokumentu darbību saraksta.</span><span class="sxs-lookup"><span data-stu-id="a7322-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="a7322-125">Jūs varat arī atsaukt dokumentus no **Dokumentu darbību saraksta** visās apakšgrāmatās.</span><span class="sxs-lookup"><span data-stu-id="a7322-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="a7322-126">Turklāt vienlaicīgi var stornēt vairāk nekā vienu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="a7322-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="a7322-127">Lai stornētu vienu vai vairākus dokumentus:</span><span class="sxs-lookup"><span data-stu-id="a7322-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="a7322-128">Noklikšķiniet uz Stornēt izvēlnes lapas augšdaļā</span><span class="sxs-lookup"><span data-stu-id="a7322-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="a7322-129">Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="a7322-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="a7322-130">Atlasiet Jā, lai izmantotu esošos darbību datumus, vai Nē, lai ievadītu jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="a7322-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="a7322-131">Dažos gadījumos, sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="a7322-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="a7322-132">Ja jūs atlasījāt Nē, ievadiet darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="a7322-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="a7322-133">Ievadiet komentārā, ko vēlaties pievienot stornētai darbībai</span><span class="sxs-lookup"><span data-stu-id="a7322-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="a7322-134">Noklikšķināt uz pogas Stornēt.</span><span class="sxs-lookup"><span data-stu-id="a7322-134">Click the Reverse button</span></span>

<span data-ttu-id="a7322-135">Darbības tiks stornētās.</span><span class="sxs-lookup"><span data-stu-id="a7322-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="a7322-136">Ja dokumenta rindu skaits pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi.</span><span class="sxs-lookup"><span data-stu-id="a7322-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="a7322-137">Stornēšanas rezultātus var pārskatīt, apskatot komentārus palaistajā pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="a7322-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="a7322-138">Visas kļūmes tiks atzīmētas pakešuzdevuma vēsturē.</span><span class="sxs-lookup"><span data-stu-id="a7322-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="a7322-139">Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="a7322-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="a7322-140">Rezultāti tiks parādīti dialogā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, un iemeslu, kāpēc to nevarēja stornēt.</span><span class="sxs-lookup"><span data-stu-id="a7322-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="a7322-141">Noklikšķiniet uz Labi, lai aizvērtu dialogu.</span><span class="sxs-lookup"><span data-stu-id="a7322-141">Click on Ok to close the dialog.</span></span>

