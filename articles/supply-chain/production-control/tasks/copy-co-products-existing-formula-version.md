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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79d55c3dfe69e9a67c5e3d0d1cf84acbb6a51d07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255353"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="60abb-103">Līdzproduktu kopēšana no esošas formulas versijas</span><span class="sxs-lookup"><span data-stu-id="60abb-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60abb-104">Šajā procedūrā ir parādīts, kā izlaistajai precei līdzproduktus no esošas formulas versijas kopēt uz citu formulas versiju.</span><span class="sxs-lookup"><span data-stu-id="60abb-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="60abb-105">Šai darbībai pastāv priekšnoteikums — ar līdzproduktiem ir jābūt saistītai vismaz vienai formulas versijai.</span><span class="sxs-lookup"><span data-stu-id="60abb-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="60abb-106">Lai izveidotu šo procedūru, tiek izmantots demonstrācijas datu uzņēmums USP2.</span><span class="sxs-lookup"><span data-stu-id="60abb-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="60abb-107">Izlaistās preces meklēšana</span><span class="sxs-lookup"><span data-stu-id="60abb-107">Find a released product</span></span>
1. <span data-ttu-id="60abb-108">Dodieties uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="60abb-108">Go to Released products.</span></span>
2. <span data-ttu-id="60abb-109">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="60abb-109">Click Show filters.</span></span>
    * <span data-ttu-id="60abb-110">Jūs grasāties filtra dialoglodziņā pievienot lauku Ražošanas tips.</span><span class="sxs-lookup"><span data-stu-id="60abb-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="60abb-111">Lai pievienotu lauku Ražošanas tips, noklikšķiniet uz Pievienot filtra lauku.</span><span class="sxs-lookup"><span data-stu-id="60abb-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="60abb-112">Nākamajā darbībā, pirms atlasāt Lietot, jums laukā Ražošanas tips ir manuāli jāievada Formula.</span><span class="sxs-lookup"><span data-stu-id="60abb-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="60abb-113">Šādi filtrs tiek iestatīts izlaisto preču sarakstam.</span><span class="sxs-lookup"><span data-stu-id="60abb-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="60abb-114">Laukā Ražošanas tips manuāli ievadiet vērtību Formula.</span><span class="sxs-lookup"><span data-stu-id="60abb-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="60abb-115">Noklikšķiniet uz Lietot.</span><span class="sxs-lookup"><span data-stu-id="60abb-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="60abb-116">Izlaistās preces atlasīšana</span><span class="sxs-lookup"><span data-stu-id="60abb-116">Select a released product</span></span>
1. <span data-ttu-id="60abb-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="60abb-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="60abb-118">Noklikšķiniet uz Formulas versijas.</span><span class="sxs-lookup"><span data-stu-id="60abb-118">Click Formula versions.</span></span>
    * <span data-ttu-id="60abb-119">Tehnikas darbību rūtī noklikšķiniet uz Formulas versijas.</span><span class="sxs-lookup"><span data-stu-id="60abb-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="60abb-120">Līdzproduktu kopēšana</span><span class="sxs-lookup"><span data-stu-id="60abb-120">Copy co-products</span></span>
1. <span data-ttu-id="60abb-121">Darbību rūtī noklikšķiniet uz Formulas versija.</span><span class="sxs-lookup"><span data-stu-id="60abb-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="60abb-122">Nokliksķiniet uz Līdzprodukti.</span><span class="sxs-lookup"><span data-stu-id="60abb-122">Click Co-products.</span></span>
3. <span data-ttu-id="60abb-123">Noklikšķiniet uz Kopēt.</span><span class="sxs-lookup"><span data-stu-id="60abb-123">Click Copy.</span></span>
4. <span data-ttu-id="60abb-124">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="60abb-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="60abb-125">Laukā Formulas versija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="60abb-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="60abb-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="60abb-126">Click OK.</span></span>
7. <span data-ttu-id="60abb-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60abb-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]