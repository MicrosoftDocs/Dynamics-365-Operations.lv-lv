---
title: "Kompensācijas debitoriem"
description: "Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas. Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3bee87b1d82dbe3d1c6de78a26633f2e1f5e92f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="reimburse-customers"></a><span data-ttu-id="40026-104">Kompensācijas debitoriem</span><span class="sxs-lookup"><span data-stu-id="40026-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40026-105">Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="40026-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="40026-106">Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu.</span><span class="sxs-lookup"><span data-stu-id="40026-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="40026-107">Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.</span><span class="sxs-lookup"><span data-stu-id="40026-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="40026-108">Priekšnosacījums</span><span class="sxs-lookup"><span data-stu-id="40026-108">Prerequisite</span></span>                                                            | <span data-ttu-id="40026-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="40026-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40026-110">Norādiet juridiskās personas minimālo kompensācijas summu.</span><span class="sxs-lookup"><span data-stu-id="40026-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="40026-111">Lapas **Debitoru parādu parametri** apgabala **Vispārīgi** laukā **Minimālā kompensācija** ievadiet minimālo summu, ko var kompensēt saistībā ar debitora pārmaksām.</span><span class="sxs-lookup"><span data-stu-id="40026-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="40026-112">Neobligāti: pievienojiet kreditora kontu katram debitoram, kam var tikt izmaksāta kompensācija.</span><span class="sxs-lookup"><span data-stu-id="40026-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="40026-113">Lapas **Debitori** kopsavilkuma cilnes **Detalizēta papildinformācija** laukā **Kreditora konts** debitoram atlasiet kreditora kontu.</span><span class="sxs-lookup"><span data-stu-id="40026-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="40026-114">Veidojot atlīdzināšanas darbības, tiek izveidots kreditora rēķins par kredīta bilances summu.</span><span class="sxs-lookup"><span data-stu-id="40026-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="40026-115">Izpildot kompensēšanas procesu, no debitora konta tiek atskaitīta kredīta bilance, savukārt debitoram atbilstošajam kreditora kontam tiek izveidota apmaksājama bilance.</span><span class="sxs-lookup"><span data-stu-id="40026-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="40026-116">Lapā Debitori palaidiet procesu **Kompensācija**.</span><span class="sxs-lookup"><span data-stu-id="40026-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="40026-117">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="40026-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="40026-118">Lai kompensāciju atskaitītu no noteiktiem debitora kontiem, noklikšķiniet uz **Atlasīt** un vaicājumā norādiet debitora kontus.</span><span class="sxs-lookup"><span data-stu-id="40026-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="40026-119">Lai atlīdzinātu visu klientu kontus, klikšķiniet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="40026-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="40026-120">Kredīta summas tiek pārskaitītas uz debitoriem atbilstošajiem kreditoru kontiem un apstrādātas kā parasti maksājumi.</span><span class="sxs-lookup"><span data-stu-id="40026-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="40026-121">Ja debitoram nav kreditora konta, debitoram automātiski tiek izveidots vienreizējs kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="40026-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="40026-122">Lai skatītu izveidotās kompensācijas transakcijas, izmantojiet lapu **Kompensācija**.</span><span class="sxs-lookup"><span data-stu-id="40026-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="40026-123">Sadaļā Kreditori izveidojiet maksājumu kreditora rēķiniem, kas tika izveidoti, veicot kompensācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="40026-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





