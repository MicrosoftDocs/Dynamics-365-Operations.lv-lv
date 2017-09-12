--- 
title: "PVN maksājuma izveide"
description: "PVN segšanas un iegrāmatošanas darbs sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā."
author: twheeloc
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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6ee84da7fd055c8b0b50c43f134c0fc048ecfaeb
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="4caae-103">PVN maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="4caae-103">Create a sales tax payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4caae-104">PVN segšanas un iegrāmatošanas darbs sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.</span><span class="sxs-lookup"><span data-stu-id="4caae-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="4caae-105">Dodieties uz Nodokļi > Deklarācijas > PVN > Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="4caae-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="4caae-106">Laukā Nomaksas periods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="4caae-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4caae-107">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4caae-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4caae-108">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="4caae-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4caae-109">Ja Virsgrāmatas parametru lapā nav atlasīta opcija Iekļaut labojumus, segšanu var apstrādāt dažādām versijām.</span><span class="sxs-lookup"><span data-stu-id="4caae-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="4caae-110">Oriģināls ir pirmais maksājums perioda intervālā, un to perioda intervālam var apstrādāt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="4caae-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="4caae-111">Jaunākie labojumi nosegs PVN transakcijas, kas ir iegrāmatotas pēc oriģinālās versijas izveides.</span><span class="sxs-lookup"><span data-stu-id="4caae-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="4caae-112">Ievadiet datumu laukā Transakcijas datums.</span><span class="sxs-lookup"><span data-stu-id="4caae-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="4caae-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4caae-113">Click OK.</span></span>


