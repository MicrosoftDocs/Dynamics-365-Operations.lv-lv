---
title: MK uzturēšana preces konfigurācijas modelim
description: Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921321"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="c6362-103">MK uzturēšana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="c6362-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6362-104">Šīs procedūras veikšanai ir nepieciešams esošs preces konfigurācijas modelis.</span><span class="sxs-lookup"><span data-stu-id="c6362-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="c6362-105">Augstas kvalitātes skaļruņu modelis demonstrācijas uzņēmumā USMF tiek izmantots, lai izveidotu šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="c6362-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="c6362-106">MK rindas pievienošana</span><span class="sxs-lookup"><span data-stu-id="c6362-106">Add a BOM line</span></span>

1. <span data-ttu-id="c6362-107">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="c6362-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="c6362-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c6362-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c6362-109">Atlasiet augstas kvalitātes skaļruni šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="c6362-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="c6362-110">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c6362-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="c6362-111">Izvērsiet sadaļu **MK rindas**.</span><span class="sxs-lookup"><span data-stu-id="c6362-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="c6362-112">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c6362-112">Select **Add**.</span></span>
1. <span data-ttu-id="c6362-113">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6362-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="c6362-114">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6362-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="c6362-115">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c6362-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="c6362-116">MK rindas informācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="c6362-116">Add BOM line details</span></span>

1. <span data-ttu-id="c6362-117">Atlasiet **Detalizēta MK rindas informācija**.</span><span class="sxs-lookup"><span data-stu-id="c6362-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="c6362-118">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c6362-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="c6362-119">Piemēram, varat atlasīt krājumu M0055.</span><span class="sxs-lookup"><span data-stu-id="c6362-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="c6362-120">Katram MK rindas rekvizītam varat atlasīt, vai tam tiek piešķirta fiksēta vērtība vai arī tas tiek kartēts uz atribūtu.</span><span class="sxs-lookup"><span data-stu-id="c6362-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="c6362-121">Atzīmējiet izvēles rūtiņu **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="c6362-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="c6362-122">Laukā **Aprēķins** atlasiet *Jā*.</span><span class="sxs-lookup"><span data-stu-id="c6362-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="c6362-123">Iestatot rekvizītam **Aprēķins** vienumu *Jā*, tiek nodrošināta MK rindas iekļaušana izmaksu aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="c6362-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="c6362-124">Atlasiet cilni **Iestatījums**.</span><span class="sxs-lookup"><span data-stu-id="c6362-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="c6362-125">Atzīmējiet izvēles rūtiņu **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="c6362-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="c6362-126">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c6362-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="c6362-127">Daudzuma lauks nosaka, kāds krājumu daudzums tiks iekļauts MK.</span><span class="sxs-lookup"><span data-stu-id="c6362-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="c6362-128">Tas varētu būt piemērots atribūtu kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="c6362-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="c6362-129">Atlasiet cilni **Dimensija**.</span><span class="sxs-lookup"><span data-stu-id="c6362-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="c6362-130">Pārbaudiet, vai kāda no preču dimensijām ir aktīva un tādējādi tai jābūt piešķirtai vērtībai vai atribūtam.</span><span class="sxs-lookup"><span data-stu-id="c6362-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="c6362-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c6362-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]