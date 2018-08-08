---
title: "Veidot ražošanas pasūtījumus"
description: "Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="create-production-orders"></a><span data-ttu-id="6e85d-105">Veidot ražošanas pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="6e85d-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e85d-106">Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu.</span><span class="sxs-lookup"><span data-stu-id="6e85d-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="6e85d-107">Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums.</span><span class="sxs-lookup"><span data-stu-id="6e85d-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="6e85d-108">Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.</span><span class="sxs-lookup"><span data-stu-id="6e85d-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="6e85d-109">Ražošanas pasūtījums tiek izvadīts caur ražošanas cikla stadijām.</span><span class="sxs-lookup"><span data-stu-id="6e85d-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="6e85d-110">Kad pasūtījums ir izveidots, tam tiek piešķirts statuss **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="6e85d-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="6e85d-111">Kad pasūtījums ir pabeigts, tam tiek piešķirts statuss **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="6e85d-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="6e85d-112">Katras stadijas parametru iestatījumi lietotājam ļauj konfigurēt katru darbību.</span><span class="sxs-lookup"><span data-stu-id="6e85d-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="6e85d-113">Šos iestatījumus var iestatīt atsevišķam lietotājam vai visiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="6e85d-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="6e85d-114">Ražošanas materiālu komplekts un ražošanas maršruts ir galvenie ražošanas pasūtījuma elementi.</span><span class="sxs-lookup"><span data-stu-id="6e85d-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="6e85d-115">Šie elementi tiek kopēti uz ražošanas pasūtījumu, pamatojoties uz atlasīto krājumu un daudzumu, ko ir paredzēts ražot.</span><span class="sxs-lookup"><span data-stu-id="6e85d-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="6e85d-116">Pirms tiek sākts ražošanas pasūtījums, ražošanas materiālu komplektu un maršrutu ir iespējams rediģēt.</span><span class="sxs-lookup"><span data-stu-id="6e85d-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="6e85d-117">Ražošanas pasūtījumu var izveidot šādos scenārijos:</span><span class="sxs-lookup"><span data-stu-id="6e85d-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="6e85d-118">Izveidots, izpildot vispārējo plānošanu, pamatojoties uz materiālu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="6e85d-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="6e85d-119">Izveidots tieši no pārdošanas pasūtījuma rindas vai laikā, kad tiek izveidots un novērtēts augstāka līmeņa ražošanas pasūtījums (piesaistītā piegāde).</span><span class="sxs-lookup"><span data-stu-id="6e85d-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="6e85d-120">Izveidots manuāli.</span><span class="sxs-lookup"><span data-stu-id="6e85d-120">Created manually.</span></span>





