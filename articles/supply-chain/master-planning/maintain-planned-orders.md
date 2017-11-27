---
title: "Uzturēt plānotos pasūtījumus"
description: "Šajā rakstā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus. Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8931908fbf643a8154da70d2ad065ea47d2aa4e6
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="bfaf9-104">Uzturēt plānotos pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="bfaf9-104">Maintain planned orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bfaf9-105">Šajā rakstā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="bfaf9-106">Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="bfaf9-107">Plānotos pasūtījumus var pārvaldīt no darbvietas **Vispārējā plānošana**, saraksta **Plānotais pasūtījums** vai saraksta **Plānotie ražošanas pasūtījumi**, **Plānotie pirkšanas pasūtījumi** un **Plānotā pārsūtīšana**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="bfaf9-108">Lai sekotu norisei, varat izmantot lauku **Statuss**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="bfaf9-109">Tiek izmantotas šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-109">The following values are used:</span></span>

-   <span data-ttu-id="bfaf9-110">Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss **Neapstrādāts**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="bfaf9-111">Ja izvēlaties neapstiprināt plānoto pasūtījumu, tam var piešķirt statusu **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="bfaf9-112">Izvēloties apstiprināt plānoto pasūtījumu, tam var piešķirt statusu **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="bfaf9-113">Šis statuss norāda, ka jūs apstiprināt plānotā pasūtījuma apstiprināšanu, taču tas vēl nav apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="bfaf9-114">**Piezīme.** Apstiprināts plānotais pasūtījums savā pašreizējā statusā tiek pārsūtīts uz nākamo vispārējās plānošanas aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="bfaf9-115">Plānotos pasūtījumus var apstiprināt, noklikšķinot uz **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="bfaf9-116">Var apstiprināt šādus plānotos pasūtījumus:</span><span class="sxs-lookup"><span data-stu-id="bfaf9-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="bfaf9-117">Atlasītais plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="bfaf9-118">vairākus plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="bfaf9-119">Plānotie pasūtījumi, ko izvērsums ir ģenerējis no lapas **Izvēršana**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="bfaf9-120">Noklikšķiniet uz **Plānotie pasūtījumi**, atlasiet plānoto pasūtījumu un tad noklikšķiniet uz **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="bfaf9-121">Kad plānotais pasūtījums apstiprināts, tas tiek pārvietots attiecīgā moduļa pasūtījumu sadaļai.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="bfaf9-122">**Piezīme.** Varat noklikšķināt ar peles labo pogu uz plānotā pasūtījuma, kam ir noteikts statuss, un filtrēt citus plānotos pasūtījumus ar to pašu statusu.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="bfaf9-123">Šī funkcionalitāte ir noderīga, ja, piemēram, vēlaties filtrēt visus plānotos pasūtījumus ar statusu **Apstiprināts** tā, lai tie pēc tam šos pasūtījumus var apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="bfaf9-124">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="bfaf9-124">See also</span></span>
--------

[<span data-ttu-id="bfaf9-125">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="bfaf9-125">Master plans</span></span>](master-plans.md)




