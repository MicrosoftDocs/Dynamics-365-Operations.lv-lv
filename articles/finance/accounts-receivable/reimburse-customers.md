---
title: Kompensācijas debitoriem
description: Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas. Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca087b5a39432eec6b2711cc4c4decf23932b611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251125"
---
# <a name="reimburse-customers"></a><span data-ttu-id="ef347-104">Kompensācijas debitoriem</span><span class="sxs-lookup"><span data-stu-id="ef347-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef347-105">Šajā rakstā ir skaidrots, kā debitoru grupai izveidot atlīdzināšanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="ef347-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="ef347-106">Ja debitoram ir kredīta bilance, varat atlīdzināt debitoram bilances summu.</span><span class="sxs-lookup"><span data-stu-id="ef347-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="ef347-107">Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.</span><span class="sxs-lookup"><span data-stu-id="ef347-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="ef347-108">Priekšnosacījums</span><span class="sxs-lookup"><span data-stu-id="ef347-108">Prerequisite</span></span>                                                            | <span data-ttu-id="ef347-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ef347-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="ef347-110">Norādiet juridiskās personas minimālo kompensācijas summu.</span><span class="sxs-lookup"><span data-stu-id="ef347-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="ef347-111">Lapas **Debitoru parādu parametri** apgabala **Vispārīgi** laukā **Minimālā kompensācija** ievadiet minimālo summu, ko var kompensēt saistībā ar debitora pārmaksām.</span><span class="sxs-lookup"><span data-stu-id="ef347-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="ef347-112">Neobligāti: pievienojiet kreditora kontu katram debitoram, kam var tikt izmaksāta kompensācija.</span><span class="sxs-lookup"><span data-stu-id="ef347-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="ef347-113">Lapas **Debitori** kopsavilkuma cilnes **Detalizēta papildinformācija** laukā **Kreditora konts** debitoram atlasiet kreditora kontu.</span><span class="sxs-lookup"><span data-stu-id="ef347-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="ef347-114">Veidojot atlīdzināšanas darbības, tiek izveidots kreditora rēķins par kredīta bilances summu.</span><span class="sxs-lookup"><span data-stu-id="ef347-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="ef347-115">Izpildot kompensēšanas procesu, no debitora konta tiek atskaitīta kredīta bilance, savukārt debitoram atbilstošajam kreditora kontam tiek izveidota apmaksājama bilance.</span><span class="sxs-lookup"><span data-stu-id="ef347-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="ef347-116">Debitoros izpildiet procesu **Atmaksa** (**Debitori \> Periodiski uzdevumi \> Atmaksa**).</span><span class="sxs-lookup"><span data-stu-id="ef347-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="ef347-117">Lai grupētu visus darījumus neatkarīgi no Virsgrāmatas dimensijām, iestatiet opciju **Apkopot debitoru** kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ef347-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="ef347-118">Lai grupētu tikai tos darījumus,, kuriem ir līdzīgas Virsgrāmatas dimensijas, iestatiet opciju kā **Nē**.</span><span class="sxs-lookup"><span data-stu-id="ef347-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="ef347-119">Atlasiet **Iekļaut debitorus ar nenokārtotiem debeta darījumiem**, lai atlasītu debitorus, kuriem ir nenosegtas debeta summas.</span><span class="sxs-lookup"><span data-stu-id="ef347-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="ef347-120">Lai atlīdzinātu noteiktus debitora kontus, kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrēt** un pēc tam norādiet debitora kontus vaicājumā.</span><span class="sxs-lookup"><span data-stu-id="ef347-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="ef347-121">Kredīta summas tiek pārskaitītas uz debitoriem atbilstošajiem kreditoru kontiem un apstrādātas kā parasti maksājumi.</span><span class="sxs-lookup"><span data-stu-id="ef347-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="ef347-122">Ja debitoram nav kreditora konta, debitoram automātiski tiek izveidots vienreizējs kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="ef347-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="ef347-123">Lai skatītu izveidotos atlīdzības darījumus, izmantojiet pārskatu **Atmaksa** (**Debitori \> Pieprasījumi un pārskati \> Atmaksas pārskats**).</span><span class="sxs-lookup"><span data-stu-id="ef347-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="ef347-124">Sadaļā Kreditori izveidojiet maksājumu kreditora rēķiniem, kas tika izveidoti, veicot kompensācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="ef347-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="ef347-125">Informāciju par to, kā apmaksāt kreditorus, skatiet sadaļā [Kreditoru maksājumu pārskats](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="ef347-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]