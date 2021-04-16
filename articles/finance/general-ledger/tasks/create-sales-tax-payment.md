---
title: PVN maksājuma izveide
description: PVN segšanas un iegrāmatošanas darba procedūra sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5066689fb85dd176da1ca1561614e443cb87d816
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832758"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="d2378-103">PVN maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="d2378-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2378-104">PVN segšanas un iegrāmatošanas darba procedūra sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.</span><span class="sxs-lookup"><span data-stu-id="d2378-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="d2378-105">Dodieties uz **Nodokļi > Deklarācijas > PVN > Nosegt un grāmatot PVN**.</span><span class="sxs-lookup"><span data-stu-id="d2378-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="d2378-106">Laukā **Nomaksas periods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d2378-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d2378-107">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d2378-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d2378-108">Ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="d2378-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="d2378-109">Ja lapā **Virsgrāmatas parametri** neatlasīsiet opciju **Iekļaut labojumus**, segšanu var apstrādāt dažādām versijām.</span><span class="sxs-lookup"><span data-stu-id="d2378-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="d2378-110">Oriģināls ir pirmais maksājums perioda intervālā, un to perioda intervālam var apstrādāt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="d2378-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="d2378-111">Jaunākie labojumi nosegs PVN transakcijas, kas ir iegrāmatotas pēc oriģinālās versijas izveides.</span><span class="sxs-lookup"><span data-stu-id="d2378-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="d2378-112">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="d2378-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="d2378-113">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d2378-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]