---
title: Mazumtirdzniecības veikala pārskatu izveidošana, aprēķināšana un grāmatošana
description: Šajā tēmā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 693d1821779d5f7af95b900daa3bb7a2c38a6354
ms.sourcegitcommit: cb63259ad8fa5649ff12bc4a7f195bd1e40bd968
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755527"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="e0603-103">Mazumtirdzniecības veikala pārskatu izveidošana, aprēķināšana un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="e0603-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e0603-104">Šajā tēmā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības.</span><span class="sxs-lookup"><span data-stu-id="e0603-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="e0603-105">Ir aprakstīti arī pakešuzdevumi, ko var konfigurēt vieniem tiem pašiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="e0603-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="e0603-106">Pakešuzdevumu konfigurēšanas un izpildes darbības ir aprakstītas citās tēmās.</span><span class="sxs-lookup"><span data-stu-id="e0603-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="e0603-107">Lai izpildītu šo procedūru, ir nepieciešamas transakcijas, kas ir pabeigtas POS un pēc tam importētas programmā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0603-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e0603-108">Šajā ierakstā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="e0603-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e0603-109">Sākuma lapā atlasiet **Mazumtirdzniecības veikala finanses**.</span><span class="sxs-lookup"><span data-stu-id="e0603-109">Select **Retail store financials** from the home page.</span></span>
2. <span data-ttu-id="e0603-110">Atlasiet **Jauns izraksts**.</span><span class="sxs-lookup"><span data-stu-id="e0603-110">Select **New statement**.</span></span>
3. <span data-ttu-id="e0603-111">Laukā **Veikala numurs** atlasiet opciju no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="e0603-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="e0603-112">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e0603-112">Select **OK**.</span></span>
5. <span data-ttu-id="e0603-113">**Iestatīšanas** grupā ir pieejami iestatījumi, kas nosaka, kādas transakcijas ir ietvertas pārskatā un kā tās tiek grupētas izraksta rindās.</span><span class="sxs-lookup"><span data-stu-id="e0603-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="e0603-114">**Iestatīšanas** grupu var atvērt un mainīt šos iestatījumus vai var izmantot noklusējuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="e0603-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="e0603-115">Laukā **Izraksta metode** tiek noteikts, kā tiks grupētas izraksta rindas.</span><span class="sxs-lookup"><span data-stu-id="e0603-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="e0603-116">Atlasiet darbinieku vai reģistru laukā **darbinieki/reģistrs**, ja vēlaties aprēķināt izrakstu tikai noteiktam darbiniekam vai reģistram.</span><span class="sxs-lookup"><span data-stu-id="e0603-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="e0603-117">Laukā **Slēgšanas metode** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="e0603-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="e0603-118">Darbību rūtī atlasiet **Aprēķināt izrakstu**.</span><span class="sxs-lookup"><span data-stu-id="e0603-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="e0603-119">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e0603-119">Select **Yes**.</span></span>
    - <span data-ttu-id="e0603-120">Pēc izraksta aprēķināšanas jātiek izveidotām rindām ar kopsummu katrai izmantotajai maksāšanas un izraksta izveides metodei.</span><span class="sxs-lookup"><span data-stu-id="e0603-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="e0603-121">Aprēķināto summu ievadiet katrā rindā, ja tā ir jāievada un atjaunina.</span><span class="sxs-lookup"><span data-stu-id="e0603-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="e0603-122">Aprēķinātais lauks tiek aizpildīts ar norēķinu uzskaites summām, kas aprēķinātas, izmantojot POS.</span><span class="sxs-lookup"><span data-stu-id="e0603-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="e0603-123">Darbību rūtī atlasiet **Grāmatot izrakstu**.</span><span class="sxs-lookup"><span data-stu-id="e0603-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="e0603-124">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="e0603-124">Select **Close**.</span></span>
11. <span data-ttu-id="e0603-125">Aizveriet rūti.</span><span class="sxs-lookup"><span data-stu-id="e0603-125">Close the pane.</span></span>
12. <span data-ttu-id="e0603-126">Sākuma lapā atlasiet **Mazumtirdzniecības veikala finanses**.</span><span class="sxs-lookup"><span data-stu-id="e0603-126">At the home page, select **Retail store financials**.</span></span>
13. <span data-ttu-id="e0603-127">Atlasiet cilni **Iegrāmatotie izraksti**.</span><span class="sxs-lookup"><span data-stu-id="e0603-127">Select the **Posted statements** tab.</span></span>

