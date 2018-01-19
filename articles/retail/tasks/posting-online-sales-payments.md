--- 
title: " Tiešsaistes pārdošanas un maksājumu grāmatošana"
description: "Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3799515c538826ac2a0b37a26e83f375591f9813
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="501a7-103"> Tiešsaistes pārdošanas un maksājumu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="501a7-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="501a7-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.</span><span class="sxs-lookup"><span data-stu-id="501a7-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="501a7-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="501a7-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="501a7-106">Pārejiet uz sadaļu Visas darbvietas > Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="501a7-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="501a7-107">Noklikšķiniet uz Sinhronizēt pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="501a7-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="501a7-108">Laukā Organizācijas hierarhija atlasiet Mazumtirdzniecības veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="501a7-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="501a7-109">Atlasiet konkrētu tiešsaistes veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="501a7-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="501a7-110">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="501a7-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="501a7-111">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="501a7-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="501a7-112">Atzīmējiet izvēles rūtiņu Pakešapstrāde vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="501a7-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="501a7-113">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="501a7-113">Click Recurrence.</span></span>
7. <span data-ttu-id="501a7-114">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="501a7-114">Select the No end date option.</span></span>
8. <span data-ttu-id="501a7-115">Laukā Skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="501a7-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="501a7-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="501a7-116">Click OK.</span></span>
10. <span data-ttu-id="501a7-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="501a7-117">Click OK.</span></span>


