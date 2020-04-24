---
title: MK uzturēšana preces konfigurācijas modelim
description: Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa2a22056ff4435d4c66f13c170aeadc02fbe03
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203576"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="6f112-103">MK uzturēšana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="6f112-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f112-104">Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis.</span><span class="sxs-lookup"><span data-stu-id="6f112-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="6f112-105">Augstas kvalitātes skaļruņu modelis demonstrācijas uzņēmumā USMF tiek izmantots, lai izveidotu šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="6f112-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="6f112-106">MK rindas pievienošana</span><span class="sxs-lookup"><span data-stu-id="6f112-106">Add a BOM line</span></span>
1. <span data-ttu-id="6f112-107">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="6f112-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="6f112-108">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="6f112-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="6f112-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6f112-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f112-110">Atlasiet augstas kvalitātes skaļruni šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="6f112-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="6f112-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6f112-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6f112-112">Izvērsiet sadaļu MK rindas.</span><span class="sxs-lookup"><span data-stu-id="6f112-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="6f112-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="6f112-113">Click Add.</span></span>
7. <span data-ttu-id="6f112-114">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6f112-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="6f112-115">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6f112-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="6f112-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6f112-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="6f112-117">MK rindas informācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="6f112-117">Add BOM line details</span></span>
1. <span data-ttu-id="6f112-118">Noklikšķiniet uz Detalizēta informācija par MK rindu.</span><span class="sxs-lookup"><span data-stu-id="6f112-118">Click BOM line details.</span></span>
2. <span data-ttu-id="6f112-119">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="6f112-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6f112-120">Piemēram, varat atlasīt krājumu M0055.</span><span class="sxs-lookup"><span data-stu-id="6f112-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="6f112-121">Katram MK rindas rekvizītam varat atlasīt, vai tam tiek piešķirta fiksēta vērtība vai arī tas tiek kartēts uz atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f112-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="6f112-122">Atzīmējiet izvēles rūtiņu Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="6f112-122">Select the Set check box.</span></span>
4. <span data-ttu-id="6f112-123">Laukā Aprēķins atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="6f112-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="6f112-124">Iestatot rekvizītam Aprēķins vienumu Jā, tiek nodrošināta MK rindas iekļaušana izmaksu aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="6f112-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="6f112-125">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="6f112-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="6f112-126">Atzīmējiet izvēles rūtiņu Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="6f112-126">Select the Set check box.</span></span>
7. <span data-ttu-id="6f112-127">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="6f112-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6f112-128">Daudzuma lauks nosaka, kāds krājumu daudzums tiks iekļauts MK.</span><span class="sxs-lookup"><span data-stu-id="6f112-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="6f112-129">Tas varētu būt piemērots atribūtu kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="6f112-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="6f112-130">Noklikšķiniet uz cilnes Dimensija.</span><span class="sxs-lookup"><span data-stu-id="6f112-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="6f112-131">Pārbaudiet, vai kāda no preču dimensijām ir aktīva un tādējādi tai jābūt piešķirtai vērtībai vai atribūtam.</span><span class="sxs-lookup"><span data-stu-id="6f112-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="6f112-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f112-132">Click OK.</span></span>

