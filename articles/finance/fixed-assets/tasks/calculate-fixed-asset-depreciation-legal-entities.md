---
title: Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām
description: Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a1e71967fb126be29a76a8a29ea5e4ae2b2199
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818468"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="e9067-103">Pamatlīdzekļu nolietojuma aprēķināšana juridiskajām personām</span><span class="sxs-lookup"><span data-stu-id="e9067-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9067-104">Pamatlīdzekļa nolietojuma aprēķināšanas procesu var vienlaikus izpildīt vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="e9067-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="e9067-105">Šajā procedūras aprakstā ir paskaidrots, kā iestatīt un izpildīt šo procesu vairākām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="e9067-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="e9067-106">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="e9067-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="e9067-107">Starpuzņēmumu nolietojuma žurnālu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e9067-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="e9067-108">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="e9067-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="e9067-109">Izvērsiet sadaļu Pamatlīdzekļu priekšlikumi.</span><span class="sxs-lookup"><span data-stu-id="e9067-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="e9067-110">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="e9067-110">Click Add.</span></span>
4. <span data-ttu-id="e9067-111">Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9067-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="e9067-112">Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9067-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="e9067-113">Atkārtojiet žurnāla iestatīšanas darbības katras juridiskās personas lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="e9067-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="e9067-114">Nolietojuma izpilde</span><span class="sxs-lookup"><span data-stu-id="e9067-114">Depreciation run</span></span>
1. <span data-ttu-id="e9067-115">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Izveidot nolietojuma piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="e9067-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="e9067-116">Laukā Grāmatošanas līmenis ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e9067-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="e9067-117">Pēc noklusējuma tiek izmantots lapā Pamatlīdzekļu parametri norādītais žurnāla nosaukums.</span><span class="sxs-lookup"><span data-stu-id="e9067-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="e9067-118">Šeit to var mainīt pašreizējai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="e9067-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="e9067-119">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="e9067-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e9067-120">Atlasiet nolietojuma aprēķināšanas izpildē ietveramās juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="e9067-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="e9067-121">Sarakstā tiek rādītas tikai tās juridiskās personas, kam ir žurnāli, kuri ir iestatīti pamatlīdzekļu ieteikumiem lapā Pamatlīdzekļu parametri.</span><span class="sxs-lookup"><span data-stu-id="e9067-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="e9067-122">Atlasiet lauka Grāmatot žurnālus vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="e9067-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="e9067-123">Filtrēšanas laukos ir ietverti visi to juridisko personu pamatlīdzekļi, grupas un grāmatas, kas ir atlasītas šai nolietojuma aprēķināšanas izpildei.</span><span class="sxs-lookup"><span data-stu-id="e9067-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="e9067-124">Pēc noklusējuma ir iespējota opcija Pakešapstrāde.</span><span class="sxs-lookup"><span data-stu-id="e9067-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="e9067-125">Ja ir iespējota šī opcija, nolietojuma žurnāla izveide un grāmatošana notiek fonā.</span><span class="sxs-lookup"><span data-stu-id="e9067-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="e9067-126">Noklikšķiniet uz Izveidot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e9067-126">Click Create journal.</span></span>
6. <span data-ttu-id="e9067-127">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="e9067-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]