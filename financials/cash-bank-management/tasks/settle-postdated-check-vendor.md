--- 
title: "Ar iepriekšēju datumu datētu čeku no kreditora apmaksa"
description: "Nosedziet kreditoram izsniegto ar iepriekšējo datumu datēto čeku, ja banka ir noņēmusi čeka transakciju pēc tam, kad čeka datums tika nokavēts un banka to noņēma."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ac3fcad40e2d71dbde5fab8d1aa77cbfa879cdb1
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="0412a-103">Ar iepriekšēju datumu datētu čeku no kreditora apmaksa</span><span class="sxs-lookup"><span data-stu-id="0412a-103">Settle a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0412a-104">Nosedziet kreditoram izsniegto ar iepriekšējo datumu datēto čeku, ja banka ir noņēmusi čeka transakciju pēc tam, kad čeka datums tika nokavēts un banka to noņēma.</span><span class="sxs-lookup"><span data-stu-id="0412a-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="0412a-105">Pirms šīs procedūras izpildiet tālāk minētās procedūras.</span><span class="sxs-lookup"><span data-stu-id="0412a-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="0412a-106">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0412a-106">Set up postdated checks</span></span>

2) <span data-ttu-id="0412a-107">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram</span><span class="sxs-lookup"><span data-stu-id="0412a-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="0412a-108">Šīs procedūras izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="0412a-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="0412a-109">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="0412a-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="0412a-110">Pārejiet uz sadaļu Kreditori > Maksājumi > Kreditoru čeki, kas datēti ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="0412a-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="0412a-111">Noklikšķiniet uz Nosegt.</span><span class="sxs-lookup"><span data-stu-id="0412a-111">Click Settle.</span></span>
3. <span data-ttu-id="0412a-112">Noklikšķiniet uz Nosegt klīringa ierakstus.</span><span class="sxs-lookup"><span data-stu-id="0412a-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="0412a-113">Nosedziet kreditora kontu, lai veiktu čeka transakciju.</span><span class="sxs-lookup"><span data-stu-id="0412a-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="0412a-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0412a-114">Close the page.</span></span>
5. <span data-ttu-id="0412a-115">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="0412a-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="0412a-116">Laukā Rādīt atlasiet opciju Visus.</span><span class="sxs-lookup"><span data-stu-id="0412a-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="0412a-117">Atzīmējiet vai notīriet izvēles rūtiņu Rādīt tikai lietotāja izveidotu.</span><span class="sxs-lookup"><span data-stu-id="0412a-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="0412a-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0412a-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0412a-119">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="0412a-119">Click Lines.</span></span>
10. <span data-ttu-id="0412a-120">Noklikšķiniet uz Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0412a-120">Click Voucher.</span></span>
11. <span data-ttu-id="0412a-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0412a-121">Close the page.</span></span>


