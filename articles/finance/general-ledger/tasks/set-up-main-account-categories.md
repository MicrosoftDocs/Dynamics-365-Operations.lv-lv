---
title: Galvenā konta kategoriju iestatīšana
description: Šajā tēmā ir izskaidrots, kā iestatīt galvenā uzņēmuma kategorijas programmā Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144793"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="aa115-103">Galvenā konta kategoriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="aa115-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa115-104">Šajā tēmā ir izskaidrots, kā iestatīt galvenā uzņēmuma kategorijas.</span><span class="sxs-lookup"><span data-stu-id="aa115-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="aa115-105">Galveno kontu kategorijas tiek izmantotas noklusējuma pārskatiem modulī Finanšu pārskatu izveidei un pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="aa115-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="aa115-106">Galveno kontu kategorijas, kas tiek izveidotas pēc noklusējuma, var pārdēvēt, bet nevar dzēst.</span><span class="sxs-lookup"><span data-stu-id="aa115-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="aa115-107">Papildu kontu kategorijas var izveidot un izmantot pārskata un analīzes nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="aa115-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="aa115-108">Šajā tēmā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="aa115-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="aa115-109">Galvenā konta kategorijas izveide</span><span class="sxs-lookup"><span data-stu-id="aa115-109">Create a main account category</span></span>
1. <span data-ttu-id="aa115-110">Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Uzņēmumu diagramma > Uzņēmumi >Galvenā uzņēmuma kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="aa115-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="aa115-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="aa115-111">Select **New**.</span></span>
3. <span data-ttu-id="aa115-112">Lodziņā **Galvenā uzņēmuma kategorijas** ievadiet unikālu lauka nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="aa115-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="aa115-113">Laukā **Apraksta lauks** ievadiet galvenā uzņēmuma kategorijas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="aa115-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="aa115-114">Laukā **Galvenā uzņēmuma veids** atlasiet galvenā uzņēmuma veidu, kas tiks sasaistīts ar kategoriju.</span><span class="sxs-lookup"><span data-stu-id="aa115-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="aa115-115">Galveno kontu saistīšana ar kontu kategoriju</span><span class="sxs-lookup"><span data-stu-id="aa115-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="aa115-116">Noklikšķiniet uz **Sasaistīt galvenos kontus**.</span><span class="sxs-lookup"><span data-stu-id="aa115-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="aa115-117">Sarakstā atlasiet galvenos uzņēmumus, lai piešķirtu galvenā uzņēmuma kategoriju, atzīmējot rūtiņas kolonnā **Saistīts**.</span><span class="sxs-lookup"><span data-stu-id="aa115-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="aa115-118">Ja galvenos kontus piešķirt galveno kontu kategorijai, kontu bilances tiks apkopotas, kad šī kategorija tiks izmantota finanšu pārskatiem un analīzei.</span><span class="sxs-lookup"><span data-stu-id="aa115-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="aa115-119">Atlasiet vai notīriet opciju **Saistīts**, lai izvēlētos galvenos kontus.</span><span class="sxs-lookup"><span data-stu-id="aa115-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="aa115-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="aa115-120">Select **OK**.</span></span>
5. <span data-ttu-id="aa115-121">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="aa115-121">Select **Yes**.</span></span>
