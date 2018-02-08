---
title: "Transportēšanas pārvaldības pārskats"
description: "Šajā tēmā ir sniegts apskats par transportēšanas pārvaldības funkcionalitāti programmā Microsoft Dynamics 365 for Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 0ec45fcf7cebf530b3a5889a857214b97b3fffbb
ms.contentlocale: lv-lv
ms.lasthandoff: 02/08/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="cf7a1-103">Transportēšanas pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="cf7a1-103">Transportation management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cf7a1-104">Šajā tēmā ir sniegts apskats par transportēšanas pārvaldības funkcionalitāti programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="cf7a1-105">Transportēšanas pārvaldība jums ļauj lietot jūsu uzņēmuma transportēšanu, kā arī ļauj identificēt kreditoru un maršrutēšanas risinājumus ienākošiem un izejošiem pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="cf7a1-106">Piemēram, var norādīt ātrāko ceļu vai vislētāko sūtījuma likmi.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="cf7a1-107">Nākamajā tabulā ir aprakstīti galvenie scenāriji attiecībā uz moduļa Transportēšanas pārvaldība lietošanu programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf7a1-108">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="cf7a1-108">Scenario</span></span></th>
<th><span data-ttu-id="cf7a1-109">Transportēšanas pārvaldības sniegtās iespējas</span><span class="sxs-lookup"><span data-stu-id="cf7a1-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf7a1-110">Izmantojiet ārējos loģistikas pakalpojumu sniedzējus transportēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="cf7a1-111">Izmantojiet transportēšanas pārvaldību ienākošajai un izejošajai transportēšanai.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf7a1-112">Paša uzņēmuma autoparks ir pieejams piegādei/saņemšanai, un piegādes maksas tiek nodotas debitoriem.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-112">The company's own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="cf7a1-113">Izejošajiem procesiem transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas maksas un nodotu tās debitoriem.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="cf7a1-114">Tomēr nav nepieciešams pārvadātāja rēķina saskaņošanas process.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-114">However, the carrier invoice reconciliation process isn't required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf7a1-115">Paša uzņēmuma autoparks ir pieejams piegādei/saņemšanai, taču piegādes maksas netiek nodotas debitoriem, jo preču cenās ir iekļauta transportēšana.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-115">The company's own fleet is available for delivery/pickup, but delivery charges aren't passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="cf7a1-116">Liela daļa transportēšanas pārvaldības funkcionalitātes nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-116">A lot of the Transportation management functionality isn't required.</span></span> <span data-ttu-id="cf7a1-117">Tomēr transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas likmes un attiecīgi pielāgotu pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf7a1-118">Loģistikas pakalpojumus sniedz cita juridiska persona tajā pašā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="cf7a1-119">Transportēšanas pārvaldību var izmantot, veicot darbības ar citu juridisku personu tāpat kā ar jebkuru citu sūtījumu pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="cf7a1-120">Ekonomiskās darbības starp juridiskajām personām nevar automatizēt.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-120">You can't automate the economic transactions between legal entities.</span></span> <span data-ttu-id="cf7a1-121">Tādēļ jums jāapstrādā šīs darbības manuāli (piemēram, izveidojot pirkšanas pasūtījumu).</span><span class="sxs-lookup"><span data-stu-id="cf7a1-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="cf7a1-122">Juridiskajā personā, kas nodrošina loģistikas pakalpojumus, transportēšanas pārvaldību var izmantot, lai noteiktu transportēšanas likmes.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="cf7a1-123">Transporta plānošana programmatūrā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf7a1-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="cf7a1-124">Modulī Transportēšanas pārvaldība transportēšanas plānošanu var balstīt uz pasūtījumiem vai uz sūtījumiem, kuri izveidoti, pamatojoties uz šiem pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="cf7a1-125">Sūtījumi vienmēr pastāv kādā noteiktā brīdī, bet nav nepieciešami transportēšanas plānošanai.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="cf7a1-126">Pārsūtīšanas pasūtījumi ir daļa no izejošās plūsmas scenārija, un tos var plānot kopā ar pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Zīmējuma ielāde](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="cf7a1-128">Ienākošā transportēšana</span><span class="sxs-lookup"><span data-stu-id="cf7a1-128">Inbound transportation</span></span>
<span data-ttu-id="cf7a1-129">Ja pasūtat preces pie kreditora, un tās ir jāpiegādā uz jūsu noliktavu, ieteicams pašiem organizēt transportu preču pārvešanai.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="cf7a1-130">Pārvešanas plānošanai un ienākošās kravas saņemšanai varat izmantot programmatūru Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="cf7a1-131">Tālāk redzamajā attēlā ir attēlota biznesa procesa plūsma attiecībā uz ienākošas kravas transportēšanu.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Biznesa procesa plūsma ienākošo kravu transportēšanai](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="cf7a1-133">Izejošā transportēšana</span><span class="sxs-lookup"><span data-stu-id="cf7a1-133">Outbound transportation</span></span>
<span data-ttu-id="cf7a1-134">Var plānot un apstrādāt izejošo kravu, lai nosūtītu noteiktus krājumus no uzņēmuma noliktavas debitoram.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="cf7a1-135">Programmatūru Finance and Operations varat izmantot, lai plānotu izejošo kravu transportēšanu un nosūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="cf7a1-136">Tālāk ir paskaidrota nosūtīšanas izejošo noslodžu plānošanas un apstrādes biznesa procesa plūsma.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Izejošo kravu plānošana un apstrāde](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="cf7a1-138">Noslodzes plānošana</span><span class="sxs-lookup"><span data-stu-id="cf7a1-138">Load building</span></span>
<span data-ttu-id="cf7a1-139">Programmatūra Finance and Operations nodrošina noslodzes plānošanas stratēģiju, kuras nosaukums ir Uz apjomu balstīta noslodzes plānošanas stratēģija.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="cf7a1-140">Šī stratēģija ļauj izmantot maksimālās vērtības, kuras ir norādītas garumam un svaram noslodzes veidnē, vai arī iestatījumus var ignorēt, ievadot jaunas vērtības.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="cf7a1-141">Lai izmantotu šo stratēģiju, atlasiet to laukā **Noslodzes plānošanas stratēģija** kopsavilkuma cilnē **Iestatījumi** lapā **Noslodzes plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="cf7a1-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="cf7a1-142">Turklāt var pievienot savas noslodzes plānošanas stratēģijas, izveidojot jaunu klasi lietojumprogrammas objektu kokā (AOT).</span><span class="sxs-lookup"><span data-stu-id="cf7a1-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




