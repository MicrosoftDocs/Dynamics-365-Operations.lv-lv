---
title: "Uzkrājumu pārskats"
description: "Šajā rakstā ir aprakstīti uzkrājumi un sniegta informācija par to, kā tos iestatīt un izveidot transakcijas."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0b4d8e7eb268857ce753415a24e600b8006eb5e3
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="a3ab0-103">Uzkrājumu pārskats</span><span class="sxs-lookup"><span data-stu-id="a3ab0-103">Accruals overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a3ab0-104">Šajā rakstā ir aprakstīti uzkrājumi un sniegta informācija par to, kā tos iestatīt un izveidot transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="a3ab0-105">Uzkrājumi tiek izmantoti uzkrājumu principa uzskaitē, lai izsekotu ieņēmumus, kas tiek atzīti par iegūtiem noteiktā periodā, nevis tad, kad tiek saņemts maksājums, un izsekotu izdevumus (izmaksas), kas tiek atzītas tad, kad tie rodas, nevis tad, kad tiek veikts maksājums.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="a3ab0-106">Uzkrāšanas shēmas</span><span class="sxs-lookup"><span data-stu-id="a3ab0-106">Accrual schemes</span></span>
<span data-ttu-id="a3ab0-107">Uzkrājumu shēmas tiek izmantotas, lai iestatītu atliktos ieņēmumus un izmaksas, un to pašu uzkrājumu shēmu var izmantot gan ieņēmumiem, gan izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="a3ab0-108">Virsgrāmatas uzkrājumi pārdala žurnāla rindas izmaksas vai ieņēmumus tā, lai tos atpazītu atbilstošajos periodos.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="a3ab0-109">Lapā **Uzkrājumu shēma** norādiet debeta un kredīta kontu, kas tiks izmantots, lietojot uzkrājumu shēmu.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="a3ab0-110">**Debets** — definētais galvenais konts aizstās debeta galveno kontu žurnāla dokumenta rindā.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="a3ab0-111">Šis konts tiks izmantots arī atliktā maksājuma anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="a3ab0-112">**Kredīts** — definētais galvenais konts aizstās kredīta galveno kontu žurnāla dokumenta rindā.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="a3ab0-113">Šis konts tiks izmantots arī atliktā maksājuma anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="a3ab0-114">Pēc tam, kad definēsiet, kurus kontus izmantot, var norādīt, kā dokumenta numurs tiek izveidots uzkrājumu transakciju izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="a3ab0-115">Varat arī norādīt, cik bieži transakcijas notiek, to izveides reižu skaitu un grāmatošanas brīdi.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="a3ab0-116">Kad uzkrājumu shēma ir izveidota, to var izmantot dažos no žurnāliem, lieotojot funkciju Virsgrāmatas uzkrājumi.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="a3ab0-117">Virsgrāmatas uzkrājumi</span><span class="sxs-lookup"><span data-stu-id="a3ab0-117">Ledger accruals</span></span>
<span data-ttu-id="a3ab0-118">Atverot žurnālu, izvēlnē **Funkcijas** varat noklikšķināt uz **Virsgrāmatas uzkrājumi**.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="a3ab0-119">Atlasot uzkrājumu shēmu, redzēsit pamatsummu no žurnāla, kas tiks sadalīts laika posmā, kā noteikts uzkrājmu shēmā.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="a3ab0-120">Piemēram, ja janvārī apmaksājat darbinieka apdrošināšanu par visu gadu, un summa ir 12 000, šie izdevumi ir jāapstiprina katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="a3ab0-121">Varat atlasīt sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-121">You can select the start date.</span></span> <span data-ttu-id="a3ab0-122">Var arī norādīt, vai summa, kas tiek uzkrāta, tiek apstiprināta kontā vai korespondējošajā kontā.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="a3ab0-123">Pēc atlases veikšanas noklikšķiniet uz **Transakcijas**, lai skatītu visas transakcijas, kas tika izveidotas atbilstoši uzkrājumu shēmai.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="a3ab0-124">Piemēram, ja izdevumus par apdrošināšanu 12 000 apmērā sadalāt uz visu gadu, tad katru mēnesi redzēsiet 1000.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="a3ab0-125">Pēc žurnāla grāmatošanas transakcijas varat apskatīt, izmantojot uzziņu lapu **Dokumentu transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="a3ab0-126">Ja uzkrājumu shēmu nevar lietot (piemēram, ja ir iesaistīts pārdošanas pasūtījuma rēķins vai pirkšanas pasūtījuma rēķins), varat kreditēt priekšapmaksas summu un debitēt izdevumu summu.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="a3ab0-127">Kad tiek lietota uzkrājumu shēma, varat atlasīt **Korespondējošais**.</span><span class="sxs-lookup"><span data-stu-id="a3ab0-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="a3ab0-128">Plašāku informāciju skatiet šeit: [Uzkrāšanas shēmu izveide](tasks/create-accrual-schemes.md) un [Virsgrāmatas uzkrājumu darbību izveide](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="a3ab0-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

