--- 
title: " Mazumtirdzniecības veikala izraksta izveide, aprēķins un grāmatošana"
description: "Šajā procedūrā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="45b27-103"> Mazumtirdzniecības veikala izraksta izveide, aprēķins un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="45b27-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="45b27-104">Šajā procedūrā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības.</span><span class="sxs-lookup"><span data-stu-id="45b27-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="45b27-105">Ir aprakstīti arī pakešuzdevumi, ko var konfigurēt vieniem tiem pašiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="45b27-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="45b27-106">Pakešuzdevumu konfigurēšanas un izpildes darbības ir aprakstītas citās tēmās.</span><span class="sxs-lookup"><span data-stu-id="45b27-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="45b27-107">Lai izpildītu šo procedūru, jābūt transakcijām, kas tika izveidotas POS un pēc tam atgādātas sistēmā Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="45b27-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="45b27-108">Šajā ierakstā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="45b27-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="45b27-109">Šo procedūru var skatīt Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="45b27-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="45b27-110">Lūdzu, ņemiet vērā, ka Dynamics AX tagad tiek dēvēts par Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="45b27-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="45b27-111">Dodieties uz Visas darbvietas > ..</span><span class="sxs-lookup"><span data-stu-id="45b27-111">Go to All workspaces > ..</span></span> <span data-ttu-id="45b27-112">> Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="45b27-112">> Retail store financials.</span></span>
2. <span data-ttu-id="45b27-113">Noklikšķiniet uz Jauns izraksts.</span><span class="sxs-lookup"><span data-stu-id="45b27-113">Click New statement.</span></span>
3. <span data-ttu-id="45b27-114">Laukā Veikala numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="45b27-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="45b27-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="45b27-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="45b27-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="45b27-116">Click OK.</span></span>
    * <span data-ttu-id="45b27-117">Laukā Iestatījumu grupā ir pieejami iestatījumi, kas nosaka, kādas transakcijas ir ietvertas pārskatā un kā tās tiek grupētas izraksta rindās.</span><span class="sxs-lookup"><span data-stu-id="45b27-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="45b27-118">Lauku Iestatīšanas grupa var atvērt un mainīt šos iestatījumus vai var izmantot noklusējuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="45b27-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="45b27-119">Lauku Izraksta metode tiek noteikts, kā tiks grupētas izraksta rindas.</span><span class="sxs-lookup"><span data-stu-id="45b27-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="45b27-120">Atlasiet darbinieku vai reģistru, ja vēlaties aprēķināt izrakstu tikai noteiktam darbiniekam vai reģistram.</span><span class="sxs-lookup"><span data-stu-id="45b27-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="45b27-121">Laukā Slēguma metode atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="45b27-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="45b27-122">Noklikšķiniet uz Aprēķināt izrakstu.</span><span class="sxs-lookup"><span data-stu-id="45b27-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="45b27-123">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="45b27-123">Click Yes.</span></span>
    * <span data-ttu-id="45b27-124">Pēc izraksta aprēķināšanas jātiek izveidotām rindām ar kopsummu katrai izmantotajai maksāšanas un izraksta izveides metodei.</span><span class="sxs-lookup"><span data-stu-id="45b27-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="45b27-125">Aprēķināto summu ievadiet katrā rindā, ja tā ir jāievada un atjaunina.</span><span class="sxs-lookup"><span data-stu-id="45b27-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="45b27-126">Aprēķinātais lauks tiek aizpildīts ar norēķinu uzskaites summām, kas aprēķinātas, izmantojot POS.</span><span class="sxs-lookup"><span data-stu-id="45b27-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="45b27-127">Noklikšķiniet uz Grāmatot izrakstu.</span><span class="sxs-lookup"><span data-stu-id="45b27-127">Click Post statement.</span></span>
10. <span data-ttu-id="45b27-128">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="45b27-128">Click Close.</span></span>
11. <span data-ttu-id="45b27-129">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="45b27-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="45b27-130">Noklikšķiniet uz cilnes Iegrāmatotie izraksti.</span><span class="sxs-lookup"><span data-stu-id="45b27-130">Click the Posted statements tab.</span></span>


