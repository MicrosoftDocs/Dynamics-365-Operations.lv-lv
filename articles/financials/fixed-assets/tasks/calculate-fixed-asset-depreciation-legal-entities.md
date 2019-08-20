---
title: Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām
description: Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840101"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="1b427-103">Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām</span><span class="sxs-lookup"><span data-stu-id="1b427-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b427-104">Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="1b427-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="1b427-105">Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt šo procesu vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="1b427-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="1b427-106">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="1b427-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="1b427-107">Starpuzņēmumu nolietojuma žurnālu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1b427-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="1b427-108">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="1b427-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="1b427-109">Izvērsiet sadaļu Pamatlīdzekļu priekšlikumi.</span><span class="sxs-lookup"><span data-stu-id="1b427-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="1b427-110">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1b427-110">Click Add.</span></span>
4. <span data-ttu-id="1b427-111">Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b427-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="1b427-112">Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b427-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="1b427-113">Atkārtojiet žurnāla iestatīšanas darbības katras juridiskās personas lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="1b427-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="1b427-114">Nolietojuma izpilde</span><span class="sxs-lookup"><span data-stu-id="1b427-114">Depreciation run</span></span>
1. <span data-ttu-id="1b427-115">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="1b427-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="1b427-116">Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1b427-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="1b427-117">Pēc noklusējuma tiek izmantots lapā Pamatlīdzekļu parametri norādītais žurnāla nosaukums.</span><span class="sxs-lookup"><span data-stu-id="1b427-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="1b427-118">Šeit to var mainīt pašreizējai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="1b427-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="1b427-119">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="1b427-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="1b427-120">Atlasiet nolietojuma aprēķināšanas izpildē ietveramās juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="1b427-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="1b427-121">Sarakstā tiek rādītas tikai tās juridiskās personas, kam ir žurnāli, kuri ir iestatīti pamatlīdzekļu ieteikumiem lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="1b427-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="1b427-122">Atlasiet lauka Grāmatot žurnālus vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="1b427-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="1b427-123">Filtrēšanas laukos ir ietverti visi to juridisko personu pamatlīdzekļi, grupas un grāmatas, kas ir atlasītas šai nolietojuma aprēķināšanas izpildei.</span><span class="sxs-lookup"><span data-stu-id="1b427-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="1b427-124">Pēc noklusējuma ir iespējota opcija Pakešapstrāde.</span><span class="sxs-lookup"><span data-stu-id="1b427-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="1b427-125">Ja ir iespējota šī opcija, nolietojuma žurnāla izveide un grāmatošana notiek fonā.</span><span class="sxs-lookup"><span data-stu-id="1b427-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="1b427-126">Noklikšķiniet uz Izveidot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="1b427-126">Click Create journal.</span></span>
6. <span data-ttu-id="1b427-127">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="1b427-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

