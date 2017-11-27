---
title: "Plānot kravas, izmantojot pārkraušanas punktu konsolidāciju"
description: "Šajā rakstā ir aprakstīts līdzeklis sūtījumu konsolidēšanai pārkraušanas punktā, kad preces no dažādām noliktavām piegādājat tam pašam debitoram vai kad preces no vairākiem kreditoriem saņemat tajā pašā noliktavā."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 475fa9b73deeddd0f9118b0062e834a053fcb919
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="987d5-103">Plānot kravas, izmantojot pārkraušanas punktu konsolidāciju</span><span class="sxs-lookup"><span data-stu-id="987d5-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="987d5-104">Šajā rakstā ir aprakstīts līdzeklis sūtījumu konsolidēšanai pārkraušanas punktā, kad preces no dažādām noliktavām piegādājat tam pašam debitoram vai kad preces no vairākiem kreditoriem saņemat tajā pašā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="987d5-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="987d5-105">Kad preces no dažādām noliktavām piegādājat tam pašam debitoram vai kad preces no vairākiem kreditoriem tiek piegādātas uz to pašu noliktavu, var būt noderīgi sūtījumus konsolidēt vienā pārkraušanas punktā.</span><span class="sxs-lookup"><span data-stu-id="987d5-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="987d5-106">Kravu plānošana</span><span class="sxs-lookup"><span data-stu-id="987d5-106">Building loads</span></span>
<span data-ttu-id="987d5-107">Lai varētu izmantot pārkraušanas punkta konsolidāciju, ir jāiespējo opcija **Tranzīta plānošana**lapā **Transportēšanas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="987d5-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="987d5-108">Jums ir arī jāizveido pārkraušanas punkti, kur notiks konsolidēšana.</span><span class="sxs-lookup"><span data-stu-id="987d5-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="987d5-109">Nākamajā diagrammā ir parādīts pārkraušanas punkta konsolidācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="987d5-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="987d5-110">Šajā gadījumā pārdošanas pasūtījumi no dažādām noliktavām tiek piegādāti vienam un tam pašam debitoram.</span><span class="sxs-lookup"><span data-stu-id="987d5-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="987d5-111">Pamata kravas tiek veidotas, pamatojoties uz pārdošanas pasūtījumiem parastajā veidā, izmantojot lapu **Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="987d5-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="987d5-112">Lai divas kravas konsolidētu vienā pārkraušanas punktā, pirms tās tiek piegādātas debitoram, lapas **Kravu plānošanas rīks** laukā **Transportēšana** atlasiet vienumu **Pārkraušanas punktu konsolidācija**.</span><span class="sxs-lookup"><span data-stu-id="987d5-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="987d5-113">Kad katrai kravai atlasāt pareizo pārkraušanas punktu, kravām šis pārkraušanas punkts tiek norādīts kā “nodošanas” galamērķis.</span><span class="sxs-lookup"><span data-stu-id="987d5-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="987d5-114">Jums būs arī divas “transportēšanas pieprasījuma rindas” sadaļā **Piedāvājums un pieprasījums**, lapā **Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="987d5-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="987d5-115">Pēc tam šīs abas rindas varat pievienot jaunai kravai.</span><span class="sxs-lookup"><span data-stu-id="987d5-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="987d5-116">Šai jaunajai kravai būs abas pārdošanas pasūtījuma rindas, kā arī būs pārkraušanas punkts kā “saņemšanas” adrese un debitors A kā “nodošanas” galamērķis.</span><span class="sxs-lookup"><span data-stu-id="987d5-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="987d5-117">Pēc tam šīs trīs kravas ir gatavas vērtēšanai un maršrutēšanai kā jebkura cita krava.</span><span class="sxs-lookup"><span data-stu-id="987d5-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="987d5-118">Jūs varat norādīt jebkādu sūtījumu pārvadātāju, ko sistēma ierosina katrai kravai.</span><span class="sxs-lookup"><span data-stu-id="987d5-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="987d5-119">[![Pārkraušanas punktu konsolidācija](./media/hubconsol.jpg)](./media/hubconsol.jpg) Šo pašu metodi varat arī izmantot, lai konsolidētu kravas no vairākiem pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="987d5-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="987d5-120">Šajā gadījumā debitors A iepriekšējā diagrammā ir noliktava.</span><span class="sxs-lookup"><span data-stu-id="987d5-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="987d5-121">Vai varat konsolidēt kravas no vairākiem pirkšanas pasūtījumiem, kur kravas no dažādiem kreditoriem tiek piegādātas uz to pašu noliktavu.</span><span class="sxs-lookup"><span data-stu-id="987d5-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="987d5-122">Jums var būt vairāki konsolidācijas pārkraušanas punkti, un varat konsolidēt vairākos pārkraušanas punktos vairākām kravām, kas tiek piegādātas no dažādām noliktavām.</span><span class="sxs-lookup"><span data-stu-id="987d5-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="987d5-123">Kad esat izveidojis savas pamata kravas un izmantojis pārkraušanas punktu konsolidēšanas opciju, jūs veidojat jaunu kravas, izmantojot konsolidēto transportēšanas pieprasījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="987d5-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="987d5-124">Pēc tam jūs vērtējat un maršrutējat savas kravas.</span><span class="sxs-lookup"><span data-stu-id="987d5-124">You then rate and route your loads.</span></span>




