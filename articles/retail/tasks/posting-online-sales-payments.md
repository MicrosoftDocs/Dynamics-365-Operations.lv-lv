---
title: Tiešsaistes pārdošanas un maksājumu grāmatošana
description: Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "353498"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="fafaa-103">Tiešsaistes pārdošanas un maksājumu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="fafaa-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fafaa-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu pārdošanas pasūtījumus un maksājumus tiešsaistes veikala transakcijām.</span><span class="sxs-lookup"><span data-stu-id="fafaa-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="fafaa-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="fafaa-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="fafaa-106">Pārejiet uz sadaļu Visas darbvietas > Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="fafaa-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="fafaa-107">Noklikšķiniet uz Sinhronizēt pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="fafaa-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="fafaa-108">Laukā Organizācijas hierarhija atlasiet Mazumtirdzniecības veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="fafaa-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="fafaa-109">Atlasiet konkrētu tiešsaistes veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="fafaa-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="fafaa-110">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="fafaa-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="fafaa-111">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="fafaa-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="fafaa-112">Atzīmējiet izvēles rūtiņu Pakešapstrāde vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="fafaa-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="fafaa-113">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="fafaa-113">Click Recurrence.</span></span>
7. <span data-ttu-id="fafaa-114">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="fafaa-114">Select the No end date option.</span></span>
8. <span data-ttu-id="fafaa-115">Laukā Skaits ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="fafaa-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="fafaa-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fafaa-116">Click OK.</span></span>
10. <span data-ttu-id="fafaa-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fafaa-117">Click OK.</span></span>

