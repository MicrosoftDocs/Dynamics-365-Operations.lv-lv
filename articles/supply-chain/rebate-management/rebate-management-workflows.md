---
title: Atlaižu pārvaldības darījumu darbplūsmas
description: Šajā tēmā skaidrots, kā iestatīt atlaižu pārvaldības darījuma darbplūsmu, lai apstiprinātu un aktivizētu darījumus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020391"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="e4fa1-103">Atlaižu pārvaldības darījumu darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="e4fa1-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4fa1-104">Lai apstiprinātu atlaižu darījumus, atlaižu pārvaldība izmanto to pašu darbplūsmas platformu, ko citas Finance and Operations lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="e4fa1-105">Divi darba procesi ir saistīti ar katru darbplūsmu:</span><span class="sxs-lookup"><span data-stu-id="e4fa1-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="e4fa1-106">Viens darbplūsmas elements aktivizē darījumu, lai lietotājs vai darbplūsmas process varētu apstiprināt darbības.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="e4fa1-107">Viens darbplūsmas elements apstiprina darījumu.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="e4fa1-108">Pirms atlaides darījuma izmantošanas tam jābūt aktīvam **Atlaižu pārvaldības** modulī.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="e4fa1-109">Lai aktivizētu darījumu, vispirms ir jāizveido un jākonfigurē *Atlaižu pārvaldības darījuma darbplūsma*.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="e4fa1-110">Kad atlaižu pārvaldībai ir aktivizēta darbplūsma, lietotāji darījumus nevar apstiprināt manuāli.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="e4fa1-111">Darbplūsma vienmēr ir jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="e4fa1-112">Izveidot un pārvaldīt atlaižu pārvaldības darījumu darbplūsmas</span><span class="sxs-lookup"><span data-stu-id="e4fa1-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="e4fa1-113">Lai strādātu ar Atlaižu pārvaldības darījumu darbplūsmām, dodieties uz **Atlaižu pārvaldība \> Iestatījumi \> Atlaižu pārvaldības darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="e4fa1-114">Tur varat skatīt, izveidot un atjaunināt darbplūsmas pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="e4fa1-115">KVienlaicīgi var būt aktīvs tikai viens darbplūsmas veids.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="e4fa1-116">Papildinformāciju par darbplūsmām, kā strādāt ar **Atlaižu pārvaldības darbplūsmu** lapu un kā izveidot darbplūsmas, skatiet [Darbplūsmas sistēmas pārskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) un ar to saistītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="e4fa1-117">Izmantojiet darbplūsmu, lai aktivizētu darījumu</span><span class="sxs-lookup"><span data-stu-id="e4fa1-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="e4fa1-118">Lai aktivizētu darījumu, izmantojot darbplūsmu, atveriet darījumu (piemēram, lapā **Visi atlaižu pārvaldības darījumi**).</span><span class="sxs-lookup"><span data-stu-id="e4fa1-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="e4fa1-119">Darbību rūtī atlasiet **Darbplūsma \> Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="e4fa1-120">Kad jaunais darījums darbplūsmā ir apstrādāts un apstiprināts, tas būs aktīvs un gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="e4fa1-121">Pēc darījuma aktivizēšanas tā iestatījumu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="e4fa1-122">Ja jums ir jāmaina aktīvs darījums, deaktivizējiet to un tad izveidojiet jaunu darījumu.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="e4fa1-123">Ja jaunais darījums būs līdzīgs vecajam darījumam, to var izveidot, kopējot veco darījumu.</span><span class="sxs-lookup"><span data-stu-id="e4fa1-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
