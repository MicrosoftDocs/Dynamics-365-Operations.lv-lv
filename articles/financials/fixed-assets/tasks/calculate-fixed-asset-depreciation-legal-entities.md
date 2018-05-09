--- 
title: "Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām"
description: "Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt nolietojuma aprēķināšanas procesu vairākām juridiskajām personām."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77df61bd85d3c296e44d3a2cfb0fce8b16eaaf9f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="cda2d-103">Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām</span><span class="sxs-lookup"><span data-stu-id="cda2d-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cda2d-104">Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="cda2d-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="cda2d-105">Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt šo procesu vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="cda2d-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="cda2d-106">Tiek izmantota grāmatveža loma.</span><span class="sxs-lookup"><span data-stu-id="cda2d-106">It uses the accountant role.</span></span>  

<span data-ttu-id="cda2d-107">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="cda2d-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="cda2d-108">Darbības (16) — apakšuzdevums: starpuzņēmumu nolietojuma žurnālu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cda2d-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="cda2d-109">Vispirms ir jāiestata žurnāli, kas tiks izmantoti starpuzņēmumu nolietojuma aprēķināšanas procedūras izpildei katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="cda2d-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="cda2d-110">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="cda2d-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="cda2d-111">Izvērsiet sadaļu Pamatlīdzekļu priekšlikumi.</span><span class="sxs-lookup"><span data-stu-id="cda2d-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="cda2d-112">Izveidojiet ierakstu ar žurnāla nosaukumu, kas ir jāizmanto katram juridiskās personas grāmatošanas līmenim.</span><span class="sxs-lookup"><span data-stu-id="cda2d-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="cda2d-113">Ja grāmatas nenodrošina grāmatošanu Virsgrāmatā, saistītajam žurnālam ir jāatlasa grāmatošanas līmeņa vērtība Nav.</span><span class="sxs-lookup"><span data-stu-id="cda2d-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="cda2d-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="cda2d-114">Click Add.</span></span> 
4. <span data-ttu-id="cda2d-115">Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda2d-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="cda2d-116">Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda2d-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="cda2d-117">Atkārtojiet žurnāla iestatīšanas darbības katras juridiskās personas lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="cda2d-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="cda2d-118">Apakšuzdevums: nolietojuma aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="cda2d-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="cda2d-119">Lapā Izveidot nolietojuma priekšlikumu sāciet nolietojuma aprēķināšanas izpildi vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="cda2d-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="cda2d-120">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="cda2d-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="cda2d-121">Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cda2d-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="cda2d-122">Pēc noklusējuma tiek izmantots lapā Pamatlīdzekļu parametri norādītais žurnāla nosaukums.</span><span class="sxs-lookup"><span data-stu-id="cda2d-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="cda2d-123">Šeit to var mainīt pašreizējai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="cda2d-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="cda2d-124">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="cda2d-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="cda2d-125">Atlasiet nolietojuma aprēķināšanas izpildē ietveramās juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="cda2d-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="cda2d-126">Sarakstā tiek rādītas tikai tās juridiskās personas, kam ir žurnāli, kuri ir iestatīti pamatlīdzekļu ieteikumiem lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="cda2d-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="cda2d-127">Ja tā ir iespējota, opcija Grāmatot žurnālus nodrošina nolietojuma žurnālu automātisku grāmatošanu to izveides brīdī.</span><span class="sxs-lookup"><span data-stu-id="cda2d-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="cda2d-128">Ja šī opcija nav atlasīt, žurnāli tiek izveidoti, taču netiek grāmatoti, tāpēc pirms grāmatošanas varat pārskatīt informāciju.</span><span class="sxs-lookup"><span data-stu-id="cda2d-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="cda2d-129">Atlasiet lauka Grāmatot žurnālus vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="cda2d-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="cda2d-130">Filtrēšanas laukos ir ietverti visi to juridisko personu pamatlīdzekļi, grupas un grāmatas, kas ir atlasītas šai nolietojuma aprēķināšanas izpildei.</span><span class="sxs-lookup"><span data-stu-id="cda2d-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="cda2d-131">Pēc noklusējuma ir iespējota opcija Pakešapstrāde.</span><span class="sxs-lookup"><span data-stu-id="cda2d-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="cda2d-132">Ja ir iespējota šī opcija, nolietojuma žurnāla izveide un grāmatošana notiek fonā.</span><span class="sxs-lookup"><span data-stu-id="cda2d-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="cda2d-133">Noklikšķiniet uz Izveidot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="cda2d-133">Click Create journal.</span></span> 
10. <span data-ttu-id="cda2d-134">Skatiet izveidotos nolietojuma žurnālus attiecīgo juridisko personu sadaļās.</span><span class="sxs-lookup"><span data-stu-id="cda2d-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="cda2d-135">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="cda2d-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

