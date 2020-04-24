---
title: Līdzproduktu kopēšana no esošas formulas versijas
description: Šajā procedūrā ir parādīts, kā izlaistajai precei līdzproduktus no esošas formulas versijas kopēt uz citu formulas versiju.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 182cc79a3aaacd8a3af97310bd63a37de5338157
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212369"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="0c787-103">Līdzproduktu kopēšana no esošas formulas versijas</span><span class="sxs-lookup"><span data-stu-id="0c787-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c787-104">Šajā procedūrā ir parādīts, kā izlaistajai precei līdzproduktus no esošas formulas versijas kopēt uz citu formulas versiju.</span><span class="sxs-lookup"><span data-stu-id="0c787-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="0c787-105">Šai darbībai pastāv priekšnoteikums — ar līdzproduktiem ir jābūt saistītai vismaz vienai formulas versijai.</span><span class="sxs-lookup"><span data-stu-id="0c787-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="0c787-106">Lai izveidotu šo procedūru, tiek izmantots demonstrācijas datu uzņēmums USP2.</span><span class="sxs-lookup"><span data-stu-id="0c787-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="0c787-107">Izlaistās preces meklēšana</span><span class="sxs-lookup"><span data-stu-id="0c787-107">Find a released product</span></span>
1. <span data-ttu-id="0c787-108">Dodieties uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="0c787-108">Go to Released products.</span></span>
2. <span data-ttu-id="0c787-109">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="0c787-109">Click Show filters.</span></span>
    * <span data-ttu-id="0c787-110">Jūs grasāties filtra dialoglodziņā pievienot lauku Ražošanas tips.</span><span class="sxs-lookup"><span data-stu-id="0c787-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="0c787-111">Lai pievienotu lauku Ražošanas tips, noklikšķiniet uz Pievienot filtra lauku.</span><span class="sxs-lookup"><span data-stu-id="0c787-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="0c787-112">Nākamajā darbībā, pirms atlasāt Lietot, jums laukā Ražošanas tips ir manuāli jāievada Formula.</span><span class="sxs-lookup"><span data-stu-id="0c787-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="0c787-113">Šādi filtrs tiek iestatīts izlaisto preču sarakstam.</span><span class="sxs-lookup"><span data-stu-id="0c787-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="0c787-114">Laukā Ražošanas tips manuāli ievadiet vērtību Formula.</span><span class="sxs-lookup"><span data-stu-id="0c787-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="0c787-115">Noklikšķiniet uz Lietot.</span><span class="sxs-lookup"><span data-stu-id="0c787-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="0c787-116">Izlaistās preces atlasīšana</span><span class="sxs-lookup"><span data-stu-id="0c787-116">Select a released product</span></span>
1. <span data-ttu-id="0c787-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0c787-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="0c787-118">Noklikšķiniet uz Formulas versijas.</span><span class="sxs-lookup"><span data-stu-id="0c787-118">Click Formula versions.</span></span>
    * <span data-ttu-id="0c787-119">Tehnikas darbību rūtī noklikšķiniet uz Formulas versijas.</span><span class="sxs-lookup"><span data-stu-id="0c787-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="0c787-120">Līdzproduktu kopēšana</span><span class="sxs-lookup"><span data-stu-id="0c787-120">Copy co-products</span></span>
1. <span data-ttu-id="0c787-121">Darbību rūtī noklikšķiniet uz Formulas versija.</span><span class="sxs-lookup"><span data-stu-id="0c787-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="0c787-122">Nokliksķiniet uz Līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="0c787-122">Click Co-products.</span></span>
3. <span data-ttu-id="0c787-123">Noklikšķiniet uz Kopēt.</span><span class="sxs-lookup"><span data-stu-id="0c787-123">Click Copy.</span></span>
4. <span data-ttu-id="0c787-124">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0c787-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="0c787-125">Laukā Formulas versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0c787-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="0c787-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0c787-126">Click OK.</span></span>
7. <span data-ttu-id="0c787-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0c787-127">Close the page.</span></span>

