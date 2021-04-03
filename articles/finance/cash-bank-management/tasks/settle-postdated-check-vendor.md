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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d66caa83df693445c1b1d40ffdc11e8d10cf7426
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239631"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="3d903-103">Ar iepriekšēju datumu datētu čeku no kreditora apmaksa</span><span class="sxs-lookup"><span data-stu-id="3d903-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d903-104">Nosedziet kreditoram izsniegto ar iepriekšējo datumu datēto čeku, ja banka ir noņēmusi čeka transakciju pēc tam, kad čeka datums tika nokavēts un banka to noņēma.</span><span class="sxs-lookup"><span data-stu-id="3d903-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="3d903-105">Pirms šīs procedūras izpildiet tālāk minētās procedūras.</span><span class="sxs-lookup"><span data-stu-id="3d903-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="3d903-106">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3d903-106">Set up postdated checks</span></span>

2) <span data-ttu-id="3d903-107">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram</span><span class="sxs-lookup"><span data-stu-id="3d903-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="3d903-108">Šīs procedūras izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="3d903-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="3d903-109">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="3d903-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="3d903-110">Pārejiet uz sadaļu Kreditori > Maksājumi > Kreditoru čeki, kas datēti ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="3d903-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="3d903-111">Noklikšķiniet uz Nosegt.</span><span class="sxs-lookup"><span data-stu-id="3d903-111">Click Settle.</span></span>
3. <span data-ttu-id="3d903-112">Noklikšķiniet uz Nosegt klīringa ierakstus.</span><span class="sxs-lookup"><span data-stu-id="3d903-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="3d903-113">Nosedziet kreditora kontu, lai veiktu čeka transakciju.</span><span class="sxs-lookup"><span data-stu-id="3d903-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="3d903-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d903-114">Close the page.</span></span>
5. <span data-ttu-id="3d903-115">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="3d903-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="3d903-116">Laukā Rādīt atlasiet opciju Visus.</span><span class="sxs-lookup"><span data-stu-id="3d903-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="3d903-117">Atzīmējiet vai notīriet izvēles rūtiņu Rādīt tikai lietotāja izveidotu.</span><span class="sxs-lookup"><span data-stu-id="3d903-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="3d903-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3d903-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3d903-119">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="3d903-119">Click Lines.</span></span>
10. <span data-ttu-id="3d903-120">Noklikšķiniet uz Dokuments.</span><span class="sxs-lookup"><span data-stu-id="3d903-120">Click Voucher.</span></span>
11. <span data-ttu-id="3d903-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d903-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]