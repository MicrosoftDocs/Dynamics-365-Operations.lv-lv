---
title: Galvenie rēķinu dati kreditoru sistēmā, izmantojot apstiprināšanas žurnālu
description: Šajā uzdevuma ceļvedī ir parādīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus, un kā pēc tam lietot apstiprināšanas žurnālu, lai atjauninātu izdevumu kontus.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "363526"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="44656-103">Galvenie rēķinu dati kreditoru sistēmā, izmantojot apstiprināšanas žurnālu</span><span class="sxs-lookup"><span data-stu-id="44656-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44656-104">Šajā uzdevuma ceļvedī ir parādīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus, un kā pēc tam lietot apstiprināšanas žurnālu, lai atjauninātu izdevumu kontus.</span><span class="sxs-lookup"><span data-stu-id="44656-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="44656-105">Izveidot un grāmatot rēķinu</span><span class="sxs-lookup"><span data-stu-id="44656-105">Create and post and invoice</span></span>
1. <span data-ttu-id="44656-106">Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu reģistrs.</span><span class="sxs-lookup"><span data-stu-id="44656-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="44656-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="44656-107">Click New.</span></span>
3. <span data-ttu-id="44656-108">Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="44656-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="44656-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="44656-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="44656-110">Noklikšķiniet uz Rindas, lai atvērtu reģistru un ievadītu izdevumu rindas.</span><span class="sxs-lookup"><span data-stu-id="44656-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="44656-111">Atlasiet kreditoru.</span><span class="sxs-lookup"><span data-stu-id="44656-111">Select a vendor.</span></span> <span data-ttu-id="44656-112">Piemēram, ievadiet vai atlasiet US-104</span><span class="sxs-lookup"><span data-stu-id="44656-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="44656-113">Laukā Rēķins ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="44656-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="44656-114">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="44656-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="44656-115">Laukā Kredīts ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="44656-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="44656-116">Laukā Apstiprināja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="44656-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="44656-117">Iezīmējiet apstiprinātāju un noklikšķiniet uz Atlasīt, lai atlasītu šo apstiprinātāju.</span><span class="sxs-lookup"><span data-stu-id="44656-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="44656-118">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="44656-118">Click Post.</span></span>
13. <span data-ttu-id="44656-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="44656-119">Close the page.</span></span>
14. <span data-ttu-id="44656-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="44656-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="44656-121">Apstiprināt rēķinu</span><span class="sxs-lookup"><span data-stu-id="44656-121">Approve an invoice</span></span>
1. <span data-ttu-id="44656-122">Pārejiet uz sadaļu Kreditori > Rēķini > Rēķina apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="44656-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="44656-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="44656-123">Click New.</span></span>
3. <span data-ttu-id="44656-124">Atlasiet nosaukumu tam rēķinu apstiprinājumu žurnālam, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="44656-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="44656-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="44656-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="44656-126">Noklikšķiniet uz rindām, lai parādītu lapu, kur varat atlasīt rēķinus, kurus vēlaties apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="44656-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="44656-127">Atlasiet Atrast dokumentus, lai parādītu visus rēķinus, kas ir gatavi apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="44656-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="44656-128">Atzīmējiet izveidoto rēķinu.</span><span class="sxs-lookup"><span data-stu-id="44656-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="44656-129">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="44656-129">Click Select.</span></span>
    * <span data-ttu-id="44656-130">Jūsu iepriekš atlasītie dokumenti pēc to atlasīšanas tiek pārvietoti uz šo sarakstu.</span><span class="sxs-lookup"><span data-stu-id="44656-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="44656-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="44656-131">Click OK.</span></span>
10. <span data-ttu-id="44656-132">Noklikšķiniet uz konta numura lauka, lai rēķinam pievienotu izdevumu kontu.</span><span class="sxs-lookup"><span data-stu-id="44656-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="44656-133">Ievadiet konta numuru un lauka cilni.</span><span class="sxs-lookup"><span data-stu-id="44656-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="44656-134">Piemēram, ievadiet 600120.</span><span class="sxs-lookup"><span data-stu-id="44656-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="44656-135">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="44656-135">Click Post.</span></span>
13. <span data-ttu-id="44656-136">Noklikšķiniet uz Dokuments, lai apskatītu grāmatotos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="44656-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="44656-137">Konts Rēķins, kas gaida apstiprinājumu, tiek anulēts un aizstāts ar faktisko izdevumu kontu.</span><span class="sxs-lookup"><span data-stu-id="44656-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

