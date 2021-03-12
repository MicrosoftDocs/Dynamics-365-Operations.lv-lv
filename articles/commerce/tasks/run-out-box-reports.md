---
title: Ārpus zonu pārskatu ģenerēšana un palaišana
description: Izmantojiet šo uzdevumu ceļvedi, lai palaistu ārpus zonu pārskatus Headquarters no dažādām darbvietām un vaicājumiem, un pārdošanas pārskatiem, kas atrodas sadaļā Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e11bca1e6850f401f52c2ccbea1089a4e71591c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003713"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="ce17d-103">Ārpus zonu pārskatu ģenerēšana un palaišana</span><span class="sxs-lookup"><span data-stu-id="ce17d-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce17d-104">Izmantojiet šo uzdevumu ceļvedi, lai palaistu ārpus zonu pārskatus Headquarters no dažādām darbvietām un vaicājumiem, un pārdošanas pārskatiem, kas atrodas sadaļā Commerce.</span><span class="sxs-lookup"><span data-stu-id="ce17d-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="ce17d-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo ierakstu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="ce17d-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="ce17d-106">Šis ieraksts ir paredzēts lietotajiem ar sistēmas administratora lomu.</span><span class="sxs-lookup"><span data-stu-id="ce17d-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="ce17d-107">Pārskaitu palaišana no darbvietām</span><span class="sxs-lookup"><span data-stu-id="ce17d-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="ce17d-108">Dodieties uz Retail un Commerce > Preces un kategorijas > Kategorijas un preču pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="ce17d-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="ce17d-109">Noklikšķiniet uz šīs bultiņas, lai izvērstu vai sakļautu sadaļu Pārskati.</span><span class="sxs-lookup"><span data-stu-id="ce17d-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="ce17d-110">Noklikšķiniet uz Labāko preču pārskats.</span><span class="sxs-lookup"><span data-stu-id="ce17d-110">Click Top products report.</span></span>
4. <span data-ttu-id="ce17d-111">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="ce17d-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="ce17d-112">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="ce17d-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="ce17d-113">Laukā Kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="ce17d-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ce17d-114">Koka struktūrā atlasiet Contoso mazumtirdzniecība\Contoso mazumtirdzniecība ASV\Centrāli\Houston.</span><span class="sxs-lookup"><span data-stu-id="ce17d-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="ce17d-115">Tiek parādīta noklusējuma Commerce organizācijas hierarhija, kas tiks lietota mazumtirdzniecības pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="ce17d-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="ce17d-116">Dodieties uz Organizācijas administrēšana > Organizācijas > Organizācijas hierarhijas nolūki un izvēlēties Commerce pārskati, savukārt sadaļā Piešķirtās hierarhijas pārbaudiet hierarhijas nosaukumu, kurai ir atzīmēta noklusējuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="ce17d-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="ce17d-117">Kā daļu no demonstrācijas datiem (izmantoti šī uzdevuma ierakstā) jūs ievērojāt, ka noklusējuma organizācijas hierarhija pārskatiem ir Veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="ce17d-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="ce17d-118">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ce17d-118">Click OK.</span></span>
9. <span data-ttu-id="ce17d-119">Laukā Skats atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ce17d-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="ce17d-120">Laukā Pēc atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ce17d-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="ce17d-121">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ce17d-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="ce17d-122">Palaist pārskatus no vaicājumiem un pārdošanas pārskatiem</span><span class="sxs-lookup"><span data-stu-id="ce17d-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="ce17d-123">Dodieties uz Retail un Commerce > Pieprasījumi un pārskati > Pārdošanas pārskati > Kategorijas pārdošanas pārskats.</span><span class="sxs-lookup"><span data-stu-id="ce17d-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="ce17d-124">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="ce17d-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="ce17d-125">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="ce17d-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="ce17d-126">Laukā Kanāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="ce17d-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ce17d-127">Koka struktūrā atlasiet Contoso mazumtirdzniecība\Contoso mazumtirdzniecība ASV\Rietumi\Sietla.</span><span class="sxs-lookup"><span data-stu-id="ce17d-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="ce17d-128">Tiek parādīta noklusējuma Commerce organizācijas hierarhija, kas tiks lietota mazumtirdzniecības pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="ce17d-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="ce17d-129">Dodieties uz Organizācijas administrēšana > Organizācijas > Organizācijas hierarhijas nolūki un izvēlēties Commerce pārskati, savukārt sadaļā Piešķirtās hierarhijas pārbaudiet hierarhijas nosaukumu, kurai ir atzīmēta noklusējuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="ce17d-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="ce17d-130">Kā daļu no demonstrācijas datiem (izmantoti šī uzdevuma ierakstā) jūs ievērojāt, ka noklusējuma organizācijas hierarhija pārskatiem ir Veikali pēc reģiona.</span><span class="sxs-lookup"><span data-stu-id="ce17d-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="ce17d-131">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ce17d-131">Click OK.</span></span>
7. <span data-ttu-id="ce17d-132">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ce17d-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="ce17d-133">HQ pārskatu eksportēšana</span><span class="sxs-lookup"><span data-stu-id="ce17d-133">Export an HQ reports</span></span>
1. <span data-ttu-id="ce17d-134">Dodieties uz Retail un Commerce > Pieprasījumi un pārskati > Pārdošanas pārskati > Organizācijas pārdošanas pārskats.</span><span class="sxs-lookup"><span data-stu-id="ce17d-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="ce17d-135">Ievadiet datumu laukā No datuma.</span><span class="sxs-lookup"><span data-stu-id="ce17d-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="ce17d-136">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="ce17d-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="ce17d-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce17d-137">Click OK.</span></span>
5. <span data-ttu-id="ce17d-138">Noklikšķiniet uz Eksportēt.</span><span class="sxs-lookup"><span data-stu-id="ce17d-138">Click Export.</span></span>
6. <span data-ttu-id="ce17d-139">Noklikšķiniet uz PDF.</span><span class="sxs-lookup"><span data-stu-id="ce17d-139">Click PDF.</span></span>

