---
title: Ar iepriekšēju datumu datētu čeku no debitora apmaksa
description: Ar iepriekšēju datumu datētu čeku var nosegt pēc tam, kad banka to ir dzēsusi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abcd6532c294223e768d1a01d97309e35c30edbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217414"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="ff79f-103">Ar iepriekšēju datumu datētu čeku no debitora apmaksa</span><span class="sxs-lookup"><span data-stu-id="ff79f-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff79f-104">Ar iepriekšēju datumu datētu čeku var nosegt pēc tam, kad banka to ir dzēsusi.</span><span class="sxs-lookup"><span data-stu-id="ff79f-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="ff79f-105">Šī finanšu transakcija dzēš arī pagaidu konta transakciju ar iepriekšēju datumu datētajam čekam.</span><span class="sxs-lookup"><span data-stu-id="ff79f-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="ff79f-106">Pirms šī darba sākšanas jābūt pabeigtiem tālāk minētajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="ff79f-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="ff79f-107">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ff79f-107">Set up postdated checks</span></span>

2) <span data-ttu-id="ff79f-108">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram</span><span class="sxs-lookup"><span data-stu-id="ff79f-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="ff79f-109">Šī uzdevuma izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="ff79f-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="ff79f-110">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="ff79f-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="ff79f-111">Pārejiet uz sadaļu Kredīts un iekasēšana > Pieprasījumi un pārskati > Maksājumi > Ar iepriekšēju datumu datēti debitoru čeki.</span><span class="sxs-lookup"><span data-stu-id="ff79f-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="ff79f-112">Noklikšķiniet uz Nosegt.</span><span class="sxs-lookup"><span data-stu-id="ff79f-112">Click Settle.</span></span>
3. <span data-ttu-id="ff79f-113">Noklikšķiniet uz Nosegt klīringa ierakstus.</span><span class="sxs-lookup"><span data-stu-id="ff79f-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="ff79f-114">Nosedziet debitora kontu, lai veiktu čeka transakciju.</span><span class="sxs-lookup"><span data-stu-id="ff79f-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="ff79f-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff79f-115">Close the page.</span></span>
5. <span data-ttu-id="ff79f-116">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="ff79f-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="ff79f-117">Laukā Rādīt atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="ff79f-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="ff79f-118">Atzīmējiet vai notīriet izvēles rūtiņu Rādīt tikai lietotāja izveidotu.</span><span class="sxs-lookup"><span data-stu-id="ff79f-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="ff79f-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ff79f-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ff79f-120">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="ff79f-120">Click Lines.</span></span>
10. <span data-ttu-id="ff79f-121">Noklikšķiniet uz Dokuments.</span><span class="sxs-lookup"><span data-stu-id="ff79f-121">Click Voucher.</span></span>
11. <span data-ttu-id="ff79f-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff79f-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]