---
title: Galvenā konta kategoriju iestatīšana
description: Galveno kontu kategorijas tiek izmantotas noklusējuma pārskatiem modulī Finanšu pārskatu izveidei un pakalpojumā Power BI.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46c7c86b93a3471ba10ec7ae6789f227bc9779c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545443"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="1f1a4-103">Galvenā konta kategoriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1f1a4-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f1a4-104">Galveno kontu kategorijas tiek izmantotas noklusējuma pārskatiem modulī Finanšu pārskatu izveidei un pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="1f1a4-105">Galveno kontu kategorijas, kas tiek izveidotas pēc noklusējuma, var pārdēvēt, bet nevar dzēst.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="1f1a4-106">Papildu kontu kategorijas var izveidot un izmantot pārskata un analīzes nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="1f1a4-107">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="1f1a4-108">Galvenā konta kategorijas izveide</span><span class="sxs-lookup"><span data-stu-id="1f1a4-108">Create a main account category</span></span>
1. <span data-ttu-id="1f1a4-109">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Konti > Galvenā konta kategorijas.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="1f1a4-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-110">Click New.</span></span>
3. <span data-ttu-id="1f1a4-111">Laukā Galvenā konta kategorija ievadiet unikālu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="1f1a4-112">Laukā Apraksts ievadiet galvenā konta kategorijas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="1f1a4-113">Laukā Galvenā konta tips atlasiet galvenā konta tipu, kas tiks saistīts ar kategoriju.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="1f1a4-114">Galveno kontu saistīšana ar kontu kategoriju</span><span class="sxs-lookup"><span data-stu-id="1f1a4-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="1f1a4-115">Noklikšķiniet uz Saistīt galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="1f1a4-116">Sarakstā atlasiet galvenos kontus, kas jāpiešķir galvenā konta kategorijai.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="1f1a4-117">Ja galvenos kontus piešķirt galveno kontu kategorijai, kontu bilances tiks apkopotas, kad šī kategorija tiks izmantota finanšu pārskatiem un analīzei.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="1f1a4-118">Atzīmējiet vai notīriet opciju Saistīts, lai izvēlētos galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="1f1a4-119">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-119">Click OK.</span></span>
5. <span data-ttu-id="1f1a4-120">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="1f1a4-120">Click Yes.</span></span>

