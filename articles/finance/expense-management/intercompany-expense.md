---
title: Starpuzņēmumu izdevumi
description: Nodarbinātais, kura darba devējs ir viena organizācijas juridiskā persona, varētu veikt darbu citā juridiskajā personā, kas ietilpst tajā pašā organizācijā. Šādā gadījumā varat izmantot starpuzņēmumu izdevumu līdzekli, lai šī nodarbinātā izdevumus piešķirtu tai juridiskajai personai, kurai darbs tika veikts.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390888"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="9ec7c-104">Starpuzņēmumu izdevumi</span><span class="sxs-lookup"><span data-stu-id="9ec7c-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ec7c-105">Nodarbinātais, kura darba devējs ir viena organizācijas juridiskā persona, varētu veikt darbu citā juridiskajā personā, kas ietilpst tajā pašā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="9ec7c-106">Šādā gadījumā varat izmantot starpuzņēmumu izdevumu līdzekli, lai šī nodarbinātā izdevumus piešķirtu tai juridiskajai personai, kurai darbs tika veikts.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="9ec7c-107">Juridiskā persona, kura ir nodarbinātā darba devējs, tiek dēvēta par patapināšanas juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="9ec7c-108">Juridiskā persona, kurai nodarbinātais izraisa izdevumus, tiek dēvēta par piesaistīšanas juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="9ec7c-109">Lai nodarbinātais varētu izveidot un iesniegt izdevumus par darbu, kurš tiek veikts citai juridiskajai personai, patapināšanas juridiskās personas lapā **Izdevumu pārvaldības parametri** atlasiet opciju **Atļaut starpuzņēmumu izdevumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="9ec7c-110">Starpuzņēmumu izdevumu nodokļu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="9ec7c-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ec7c-111">Ja izdevumu pārskatā vēlaties importa nodokļu grupas, kas saistītas ar patapināšanas (avota) juridisko personu, nevis piesaistīšanas (mērķa) juridisko personu, tas ir jākonfigurē Virsgrāmatas PVN iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="9ec7c-112">Kad Virsgrāmatas parametrs **Juridiskas personas starpuzņēmumu nodokļu grāmatošana** ir iestatīts uz **Avots** un **Piemērot PVN nodokļu sistēmas nosacījumus** ir iestatīts uz **Nē**, tiks izmantota patapināšanas juridiskās personas nodokļu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="9ec7c-113">Ja tas pats parametrs ir iestatīts uz **Mērķis**, tiks izmantota piesaistīšanas juridiskās personas nodokļu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="9ec7c-114">Juridiskajām personām Amerikas Savienotajās valstīs, parametram esot iestatītam uz **Avots**, lauks **Saņemtais PVN** ir jākonfigurē arī jaunā **Virsgrāmatas grāmatošanas grupas** lapā.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="9ec7c-115">Uzskaites programma izmantos informāciju no šī lauka ar nodokļiem saistītajos uzskaites ierakstos.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="9ec7c-116">Darbība ir saskaņota izdevumu rindām, kas grāmatotas ar vai bez projekta.</span><span class="sxs-lookup"><span data-stu-id="9ec7c-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
