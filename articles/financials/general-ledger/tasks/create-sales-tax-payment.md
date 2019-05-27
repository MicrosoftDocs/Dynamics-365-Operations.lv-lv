---
title: PVN maksājuma izveide
description: PVN segšanas un iegrāmatošanas darbs sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d72c88d6ba851e96ca07b896630549690e9396
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563697"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="6b51d-103">PVN maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="6b51d-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b51d-104">PVN segšanas un iegrāmatošanas darbs sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.</span><span class="sxs-lookup"><span data-stu-id="6b51d-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="6b51d-105">Dodieties uz Nodokļi > Deklarācijas > PVN > Nosegt un grāmatot PVN.</span><span class="sxs-lookup"><span data-stu-id="6b51d-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="6b51d-106">Laukā Nomaksas periods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6b51d-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6b51d-107">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6b51d-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6b51d-108">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="6b51d-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="6b51d-109">Ja Virsgrāmatas parametru lapā nav atlasīta opcija Iekļaut labojumus, segšanu var apstrādāt dažādām versijām.</span><span class="sxs-lookup"><span data-stu-id="6b51d-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="6b51d-110">Oriģināls ir pirmais maksājums perioda intervālā, un to perioda intervālam var apstrādāt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="6b51d-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="6b51d-111">Jaunākie labojumi nosegs PVN transakcijas, kas ir iegrāmatotas pēc oriģinālās versijas izveides.</span><span class="sxs-lookup"><span data-stu-id="6b51d-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="6b51d-112">Ievadiet datumu laukā Transakcijas datums.</span><span class="sxs-lookup"><span data-stu-id="6b51d-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="6b51d-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6b51d-113">Click OK.</span></span>

