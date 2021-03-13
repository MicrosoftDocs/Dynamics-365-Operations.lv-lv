---
title: Ražošanas pasūtījuma dzīves cikla pārskats
description: Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28ef1da29b38354d7ccaad56fb036f21d8c9ff15
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011176"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="2c63c-105">Ražošanas pasūtījuma dzīves cikla pārskats</span><span class="sxs-lookup"><span data-stu-id="2c63c-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c63c-106">Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu.</span><span class="sxs-lookup"><span data-stu-id="2c63c-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="2c63c-107">Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums.</span><span class="sxs-lookup"><span data-stu-id="2c63c-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="2c63c-108">Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.</span><span class="sxs-lookup"><span data-stu-id="2c63c-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="2c63c-109">Ražošanas pasūtījums tiek izvadīts caur ražošanas cikla stadijām.</span><span class="sxs-lookup"><span data-stu-id="2c63c-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="2c63c-110">Kad pasūtījums ir izveidots, tam tiek piešķirts statuss **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="2c63c-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="2c63c-111">Kad pasūtījums ir pabeigts, tam tiek piešķirts statuss **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="2c63c-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="2c63c-112">Katras stadijas parametru iestatījumi lietotājam ļauj konfigurēt katru darbību.</span><span class="sxs-lookup"><span data-stu-id="2c63c-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="2c63c-113">Šos iestatījumus var iestatīt atsevišķam lietotājam vai visiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="2c63c-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="2c63c-114">Ražošanas materiālu komplekts un ražošanas maršruts ir galvenie ražošanas pasūtījuma elementi.</span><span class="sxs-lookup"><span data-stu-id="2c63c-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="2c63c-115">Šie elementi tiek kopēti uz ražošanas pasūtījumu, pamatojoties uz atlasīto krājumu un daudzumu, ko ir paredzēts ražot.</span><span class="sxs-lookup"><span data-stu-id="2c63c-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="2c63c-116">Pirms tiek sākts ražošanas pasūtījums, ražošanas materiālu komplektu un maršrutu ir iespējams rediģēt.</span><span class="sxs-lookup"><span data-stu-id="2c63c-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="2c63c-117">Ražošanas pasūtījumu var izveidot šādos scenārijos:</span><span class="sxs-lookup"><span data-stu-id="2c63c-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="2c63c-118">Izveidots, izpildot vispārējo plānošanu, pamatojoties uz materiālu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="2c63c-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="2c63c-119">Izveidots tieši no pārdošanas pasūtījuma rindas vai laikā, kad tiek izveidots un novērtēts augstāka līmeņa ražošanas pasūtījums (piesaistītā piegāde).</span><span class="sxs-lookup"><span data-stu-id="2c63c-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="2c63c-120">Izveidots manuāli.</span><span class="sxs-lookup"><span data-stu-id="2c63c-120">Created manually.</span></span>




