--- 
title: " Ārpus zonu pārskatu ģenerēšana un palaišana"
description: "Izmantojiet šo uzdevumu ceļvedi, lai palaistu ārpus zonu pārskatus galvenajā pārvaldē no dažādām darbvietām un vaicājumiem, un pārdošanas pārskatiem, kas atrodas sadaļā Mazumtirdzniecība un komercija."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: f77b4289613adce27bda43d326d969c984ef01b6
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="fd2b8-103"> Ārpus zonu pārskatu ģenerēšana un palaišana</span><span class="sxs-lookup"><span data-stu-id="fd2b8-103">Generate and run out-of-box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fd2b8-104">Izmantojiet šo uzdevumu ceļvedi, lai palaistu ārpus zonu pārskatus galvenajā pārvaldē no dažādām darbvietām un vaicājumiem, un pārdošanas pārskatiem, kas atrodas sadaļā Mazumtirdzniecība un komercija.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="fd2b8-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo ierakstu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="fd2b8-106">Šis ieraksts ir paredzēts lietotajiem ar sistēmas administratora lomu.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="fd2b8-107">Pārskaitu palaišana no darbvietām</span><span class="sxs-lookup"><span data-stu-id="fd2b8-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="fd2b8-108">Dodieties uz Mazumtirdzniecība un komercija > Preces un kategorijas > Kategorijas un preču pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="fd2b8-109">Noklikšķiniet uz šīs bultiņas, lai izvērstu vai sakļautu sadaļu Pārskati.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="fd2b8-110">Noklikšķiniet uz Labāko preču pārskats.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-110">Click Top products report.</span></span>
4. <span data-ttu-id="fd2b8-111">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="fd2b8-112">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="fd2b8-113">Laukā Kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fd2b8-114">Koka struktūrā atlasiet Contoso mazumtirdzniecība\Contoso mazumtirdzniecība ASV\Centrāli\Houston.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="fd2b8-115">Tiek parādīta noklusējuma mazumtirdzniecības organizācijas hierarhija, kas tiks lietota mazumtirdzniecības pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="fd2b8-116">Dodieties uz Organizācijas administrēšana >Organizācijas > Organizācijas hierarhijas nolūki un izvēlēties Mazumtirdzniecības pārskati, savukārt sadaļā Piešķirtās hierarhijas pārbaudiet hierarhijas nosaukumu, kurai ir atzīmēta noklusējuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="fd2b8-117">Kā daļu no demonstrācijas datiem (izmantoti šī uzdevuma ierakstā) jūs ievērojāt, ka noklusējuma organizācijas hierarhija mazumtirdzniecības pārskatiem ir Mazumtirdzniecības veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="fd2b8-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-118">Click OK.</span></span>
9. <span data-ttu-id="fd2b8-119">Laukā Skats atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="fd2b8-120">Laukā Pēc atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="fd2b8-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="fd2b8-122">Palaidiet pārskatus no vaicājumiem un pārdošanas pārskatiem, kas atrodas sadaļā Mazumtirdzniecība & Komercijas lietojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="fd2b8-123">Dodieties uz Mazumtirdzniecība un komercija > Pieprasījumi un pārskati > Pārdošanas pārskati > Kategorijas pārdošanas pārskats.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="fd2b8-124">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="fd2b8-125">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="fd2b8-126">Laukā Kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fd2b8-127">Koka struktūrā atlasiet Contoso mazumtirdzniecība\Contoso mazumtirdzniecība ASV\Rietumi\Sietla.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="fd2b8-128">Tiek parādīta noklusējuma mazumtirdzniecības organizācijas hierarhija, kas tiks lietota mazumtirdzniecības pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="fd2b8-129">Dodieties uz Organizācijas administrēšana >Organizācijas > Organizācijas hierarhijas nolūki un izvēlēties Mazumtirdzniecības pārskati, savukārt sadaļā Piešķirtās hierarhijas pārbaudiet hierarhijas nosaukumu, kurai ir atzīmēta noklusējuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="fd2b8-130">Kā daļu no demonstrācijas datiem (izmantoti šī uzdevuma ierakstā) jūs ievērojāt, ka noklusējuma organizācijas hierarhija mazumtirdzniecības pārskatiem ir Mazumtirdzniecības veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="fd2b8-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-131">Click OK.</span></span>
7. <span data-ttu-id="fd2b8-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="fd2b8-133">HQ pārskatu eksportēšana</span><span class="sxs-lookup"><span data-stu-id="fd2b8-133">Export an HQ reports</span></span>
1. <span data-ttu-id="fd2b8-134">Dodieties uz Mazumtirdzniecība un komercija > Pieprasījumi un pārskati > Pārdošanas pārskati > Organizācijas pārdošanas pārskats.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="fd2b8-135">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="fd2b8-136">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="fd2b8-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-137">Click OK.</span></span>
5. <span data-ttu-id="fd2b8-138">Noklikšķiniet uz Eksportēt.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-138">Click Export.</span></span>
6. <span data-ttu-id="fd2b8-139">Noklikšķiniet uz PDF.</span><span class="sxs-lookup"><span data-stu-id="fd2b8-139">Click PDF.</span></span>


