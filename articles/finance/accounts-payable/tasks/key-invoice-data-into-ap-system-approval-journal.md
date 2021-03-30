---
title: Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu
description: Šajā tēmā paskaidrots, kā izmantot rēķinu reģistru, lai izveidotu rēķinus, un tad izmantot apstiprināšanas žurnālu, lai atjauninātu izdevumu kontus.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227188"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="4fbd4-103">Rēķinu datu ievade kreditoru modulī, izmantojot apstiprināšanas žurnālu</span><span class="sxs-lookup"><span data-stu-id="4fbd4-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fbd4-104">Šajā tēmā paskaidrots, kā izmantot rēķinu reģistru, lai izveidotu rēķinus, un tad izmantot apstiprināšanas žurnālu, lai atjauninātu izdevumu kontus.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="4fbd4-105">Izveidot un grāmatot rēķinu</span><span class="sxs-lookup"><span data-stu-id="4fbd4-105">Create and post and invoice</span></span>
1. <span data-ttu-id="4fbd4-106">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu reģistrs**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="4fbd4-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-107">Select **New**.</span></span>
3. <span data-ttu-id="4fbd4-108">Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="4fbd4-109">Atlasiet **Rindas**, lai atvērtu reģistru un ievadītu izmaksu rindas. </span><span class="sxs-lookup"><span data-stu-id="4fbd4-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="4fbd4-110">Atlasiet kreditoru.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-110">Select a vendor.</span></span> <span data-ttu-id="4fbd4-111">Piemēram, ievadiet vai atlasiet `US-104`.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="4fbd4-112">Laukā **Rēķins** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="4fbd4-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="4fbd4-114">Laukā **Kredīts** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="4fbd4-115">Laukā **Apstiprināja** nolaižamajā izvēlnē atlasiet apstiprinātāju.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="4fbd4-116">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="4fbd4-117">Apstiprināt rēķinu</span><span class="sxs-lookup"><span data-stu-id="4fbd4-117">Approve an invoice</span></span>
1. <span data-ttu-id="4fbd4-118">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="4fbd4-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-119">Select **New**.</span></span>
3. <span data-ttu-id="4fbd4-120">Atlasiet nosaukumu tam rēķinu apstiprinājumu žurnālam, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="4fbd4-121">Atlasiet **Rindas**, lai attēlotu lapu, kurā jūs varēsit atlasīt rēķinus, kurus vēlaties apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="4fbd4-122">Atlasiet **Atrast dokumentus**, lai uzrādītu visus rēķinus, kuri ir gatavi apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="4fbd4-123">Atzīmējiet rēķinu, kuru izveidojāt, tad noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="4fbd4-124">Jūsu iepriekš atlasītie dokumenti pēc to atlasīšanas tiek pārvietoti uz šo sarakstu.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="4fbd4-125">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-125">Select **OK**.</span></span>
8. <span data-ttu-id="4fbd4-126">Atlasiet lauku **konta numurs**, lai rēķinam pievienotu izdevumu kontu.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="4fbd4-127">Ievadiet konta numuru un lauka cilni.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="4fbd4-128">Piemēram, ievadiet `600120`.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="4fbd4-129">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-129">Select **Post**.</span></span>
11. <span data-ttu-id="4fbd4-130">Atlasiet **Dokuments**, lai skatītu ievietotos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="4fbd4-131">Konts Rēķins, kas gaida apstiprinājumu, tiek anulēts un aizstāts ar faktisko izdevumu kontu.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]