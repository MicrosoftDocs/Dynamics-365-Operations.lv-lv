---
title: "Plānoto pasūtījumu uzturēšana"
description: "Šajā sadaļā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus. Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam."
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.contentlocale: lv-lv
ms.lasthandoff: 10/08/2018

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="b6a3e-104">Plānoto pasūtījumu uzturēšana</span><span class="sxs-lookup"><span data-stu-id="b6a3e-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6a3e-105">Šajā sadaļā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="b6a3e-106">Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="b6a3e-107">Plānotos pasūtījumus var pārvaldīt no darbvietas **Vispārējā plānošana**, saraksta **Plānotais pasūtījums** vai saraksta **Plānotie ražošanas pasūtījumi**, **Plānotie pirkšanas pasūtījumi** un **Plānotā pārsūtīšana**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="b6a3e-108">Lai sekotu norisei, varat izmantot lauku **Statuss**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="b6a3e-109">Tiek izmantotas šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-109">The following values are used:</span></span>

-   <span data-ttu-id="b6a3e-110">Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss **Neapstrādāts**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="b6a3e-111">Ja izvēlaties neapstiprināt plānoto pasūtījumu, tam var piešķirt statusu **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="b6a3e-112">Izvēloties apstiprināt plānoto pasūtījumu, tam var piešķirt statusu **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="b6a3e-113">Šis statuss norāda, ka jūs apstiprināt plānotā pasūtījuma apstiprināšanu, taču tas vēl nav apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="b6a3e-114">**Piezīme.** Apstiprināts plānotais pasūtījums savā pašreizējā statusā tiek pārsūtīts uz nākamo vispārējās plānošanas aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="b6a3e-115">Plānotos pasūtījumus var apstiprināt, noklikšķinot uz **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="b6a3e-116">Var apstiprināt šādus plānotos pasūtījumus:</span><span class="sxs-lookup"><span data-stu-id="b6a3e-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="b6a3e-117">Atlasītais plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="b6a3e-118">vairākus plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="b6a3e-119">Plānotie pasūtījumi, ko izvērsums ir ģenerējis no lapas **Izvēršana**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="b6a3e-120">Noklikšķiniet uz **Plānotie pasūtījumi**, atlasiet plānoto pasūtījumu un tad noklikšķiniet uz **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="b6a3e-121">Kad plānotais pasūtījums apstiprināts, tas tiek pārvietots attiecīgā moduļa pasūtījumu sadaļai.</span><span class="sxs-lookup"><span data-stu-id="b6a3e-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="b6a3e-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b6a3e-122">Additional resources</span></span>
--------

[<span data-ttu-id="b6a3e-123">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="b6a3e-123">Master plans</span></span>](master-plans.md)




