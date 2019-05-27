---
title: Ar iepriekšēju datumu datētu čeku no kreditora apmaksa
description: Nosedziet kreditoram izsniegto ar iepriekšējo datumu datēto čeku, ja banka ir noņēmusi čeka transakciju pēc tam, kad čeka datums tika nokavēts un banka to noņēma.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46b419ab613425ae2d758f80105ac94f1ec5cc2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565976"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="36dee-103">Ar iepriekšēju datumu datētu čeku no kreditora apmaksa</span><span class="sxs-lookup"><span data-stu-id="36dee-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36dee-104">Nosedziet kreditoram izsniegto ar iepriekšējo datumu datēto čeku, ja banka ir noņēmusi čeka transakciju pēc tam, kad čeka datums tika nokavēts un banka to noņēma.</span><span class="sxs-lookup"><span data-stu-id="36dee-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="36dee-105">Pirms šīs procedūras izpildiet tālāk minētās procedūras.</span><span class="sxs-lookup"><span data-stu-id="36dee-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="36dee-106">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="36dee-106">Set up postdated checks</span></span>

2) <span data-ttu-id="36dee-107">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram</span><span class="sxs-lookup"><span data-stu-id="36dee-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="36dee-108">Šīs procedūras izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="36dee-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="36dee-109">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="36dee-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="36dee-110">Pārejiet uz sadaļu Kreditori > Maksājumi > Kreditoru čeki, kas datēti ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="36dee-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="36dee-111">Noklikšķiniet uz Nosegt.</span><span class="sxs-lookup"><span data-stu-id="36dee-111">Click Settle.</span></span>
3. <span data-ttu-id="36dee-112">Noklikšķiniet uz Nosegt klīringa ierakstus.</span><span class="sxs-lookup"><span data-stu-id="36dee-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="36dee-113">Nosedziet kreditora kontu, lai veiktu čeka transakciju.</span><span class="sxs-lookup"><span data-stu-id="36dee-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="36dee-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="36dee-114">Close the page.</span></span>
5. <span data-ttu-id="36dee-115">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="36dee-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="36dee-116">Laukā Rādīt atlasiet opciju Visus.</span><span class="sxs-lookup"><span data-stu-id="36dee-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="36dee-117">Atzīmējiet vai notīriet izvēles rūtiņu Rādīt tikai lietotāja izveidotu.</span><span class="sxs-lookup"><span data-stu-id="36dee-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="36dee-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="36dee-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="36dee-119">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="36dee-119">Click Lines.</span></span>
10. <span data-ttu-id="36dee-120">Noklikšķiniet uz Dokuments.</span><span class="sxs-lookup"><span data-stu-id="36dee-120">Click Voucher.</span></span>
11. <span data-ttu-id="36dee-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="36dee-121">Close the page.</span></span>

