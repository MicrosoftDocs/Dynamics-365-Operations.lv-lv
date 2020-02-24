---
title: Stornēt žurnāla grāmatošanu
description: Šajā tēmā ir aprakstītas iespējas, kas ļauj stornēt dokumentus no dokumentu darbību saraksta vai finanšu žurnāliem.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 08aec836ce4b7b6a59c445f138365f101a78c68e
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030926"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="76c74-103">Stornēt žurnāla grāmatošanu</span><span class="sxs-lookup"><span data-stu-id="76c74-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76c74-104">Šajā tēmā ir aprakstītas iespējas Microsoft Dynamics 365 Finance, kas ļauj stornēt visu žurnālu vai stornēt vienu vai vairākus dokumentus no dokumentu darbību saraksta neatkarīgi no to izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="76c74-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="76c74-105">Stornējot žurnālus</span><span class="sxs-lookup"><span data-stu-id="76c74-105">Reversing journals</span></span>

<span data-ttu-id="76c74-106">Varat stornēt žurnāla rindas atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="76c74-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="76c74-107">Ar stornēto žurnāla grāmatošanu, var arī stornēt visu finanšu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="76c74-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="76c74-108">Stornēt žurnālu:</span><span class="sxs-lookup"><span data-stu-id="76c74-108">To reverse a journal:</span></span> 

- <span data-ttu-id="76c74-109">Atveriet finanšu žurnālu un filtrējiet grāmatotos žurnālus.</span><span class="sxs-lookup"><span data-stu-id="76c74-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="76c74-110">Atlasiet **Stornēt** izvēlnes lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="76c74-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="76c74-111">Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="76c74-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="76c74-112">Atlasiet **Jā**, lai izmantotu esošos darbību datumus, vai **Nē**, lai ievadītu jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="76c74-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="76c74-113">Dažos gadījumos sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="76c74-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="76c74-114">Ja jūs atlasījāt **Nē**, ievadiet darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="76c74-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="76c74-115">Ievadiet komentārā, ko vēlaties pievienot stornētai darbībai.</span><span class="sxs-lookup"><span data-stu-id="76c74-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="76c74-116">Atlasiet pogu **Stornēt**.</span><span class="sxs-lookup"><span data-stu-id="76c74-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="76c74-117">Darbības tiks stornētās.</span><span class="sxs-lookup"><span data-stu-id="76c74-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="76c74-118">Ja dokuments pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi.</span><span class="sxs-lookup"><span data-stu-id="76c74-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="76c74-119">Rezultātus varat pārskatīt, apskatot komentārus pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="76c74-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="76c74-120">Jebkuras darbības, kuras nevarēja atcelt, tiks uzskaitītas pakešuzdevuma vēsturē.</span><span class="sxs-lookup"><span data-stu-id="76c74-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="76c74-121">Ja dokuments sastāv no 100 rindām vai mazāk, stornēšanas process tiks izpildīts nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="76c74-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="76c74-122">Rezultāti tiks parādīti dialoga lodziņā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, kopā ar iemeslu, kāpēc to nevarēja stornēt.</span><span class="sxs-lookup"><span data-stu-id="76c74-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="76c74-123">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="76c74-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="76c74-124">Stornējot dokumentus no dokumentu darbību saraksta.</span><span class="sxs-lookup"><span data-stu-id="76c74-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="76c74-125">Jūs varat arī atsaukt dokumentus no **Dokumentu darbību saraksta** visās apakšgrāmatās.</span><span class="sxs-lookup"><span data-stu-id="76c74-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="76c74-126">Turklāt vienlaicīgi var stornēt vairāk nekā vienu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="76c74-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="76c74-127">Lai stornētu vienu vai vairākus dokumentus:</span><span class="sxs-lookup"><span data-stu-id="76c74-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="76c74-128">Atlasiet **Stornēt** izvēlnes lapas augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="76c74-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="76c74-129">Jūs redzēsiet kopējo dokumentu un dokumentu rindu skaitu, kā arī kopējo stornēto rindu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="76c74-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="76c74-130">Atlasiet **Jā**, lai izmantotu esošos darbību datumus, vai **Nē**, lai ievadītu jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="76c74-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="76c74-131">Dažos gadījumos sākotnējās darbības periods var būt slēgts, un jums vajadzēs ievadīt jaunu darbības datumu, lai to stornētu.</span><span class="sxs-lookup"><span data-stu-id="76c74-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="76c74-132">Ja jūs atlasījāt **Nē**, ievadiet darbības datumu stornēšanai.</span><span class="sxs-lookup"><span data-stu-id="76c74-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="76c74-133">Ievadiet komentāru, lai aprakstītu stornēšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="76c74-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="76c74-134">Atlasiet pogu **Stornēt**.</span><span class="sxs-lookup"><span data-stu-id="76c74-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="76c74-135">Darbības tiks stornētās.</span><span class="sxs-lookup"><span data-stu-id="76c74-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="76c74-136">Ja dokuments pārsniedz 100 rindas, stornēšanas process tiks izpildīts, izmantojot pakešveida apstrādi.</span><span class="sxs-lookup"><span data-stu-id="76c74-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="76c74-137">Rezultātus varat pārskatīt, apskatot komentārus pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="76c74-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="76c74-138">Jebkuras darbības, kuras nevarēja atcelt, tiks atzīmētas pakešuzdevuma vēsturē.</span><span class="sxs-lookup"><span data-stu-id="76c74-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="76c74-139">Ja dokumenta rindu skaits ir 100 rindas vai mazāk, stornēšanas process tiks izpildīts nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="76c74-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="76c74-140">Rezultāti tiks parādīti dialoga lodziņā, kur var ieraudzīt jebkuru dokumentu, kuru nevar stornēt, kopā ar iemeslu, kāpēc to nevarēja stornēt.</span><span class="sxs-lookup"><span data-stu-id="76c74-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="76c74-141">Atlasiet **Labi**, lai aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="76c74-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="76c74-142">Darbības var apgriezt tikai tad, ja tās atbilst biznesa noteikumiem, lai tos stornētu.</span><span class="sxs-lookup"><span data-stu-id="76c74-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="76c74-143">Kreditoru maksājumus nevar atcelt, izmantojot šajā tēmā aprakstītās iespējas.</span><span class="sxs-lookup"><span data-stu-id="76c74-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="76c74-144">Kreditoru maksājumi ir jāstornē, izpildot darbības, kas norādītas [Stornēt kreditora maksājumu](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="76c74-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

