---
title: No dimensijām atkarīgas preču konfigurācijas pārskats
description: No dimensijām atkarīga preču konfigurācija ir vienkāršs risinājums, kā no viena preces šablona un tā materiālu komplekta izveidot daudzus preču variantus.
author: cvocph
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45688f1882d2711cd43b9b7c199f1fca7ff089ea
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985537"
---
# <a name="dimension-based-product-configuration-overview"></a><span data-ttu-id="4e95e-103">No dimensijām atkarīgas preču konfigurācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="4e95e-103">Dimension-based product configuration overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e95e-104">No dimensijām atkarīga preču konfigurācija ir vienkāršs risinājums, kā no viena preces šablona un tā materiālu komplekta izveidot daudzus preču variantus.</span><span class="sxs-lookup"><span data-stu-id="4e95e-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="4e95e-105">Preces konfigurācija atbilstoši dimensijām ir viena no trim preču konfigurācijas tehnoloģijām.</span><span class="sxs-lookup"><span data-stu-id="4e95e-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="4e95e-106">Pārējās divas tehnoloģijas ir šādas: Iepriekš definēti varianti un Konfigurācija atbilstoši ierobežojumam.</span><span class="sxs-lookup"><span data-stu-id="4e95e-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="4e95e-107">Visas trīs tehnoloģijas kā sākuma punktu izmanto preces šablonu un ļauj lietotājam izveidot daudz preču variantus vienam preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="4e95e-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="4e95e-108">Galvenie principi</span><span class="sxs-lookup"><span data-stu-id="4e95e-108">Key concepts</span></span>
<span data-ttu-id="4e95e-109">Preces konfigurācijas atbilstoši dimensijām pamatā ir tālāk minētie galvenie principi.</span><span class="sxs-lookup"><span data-stu-id="4e95e-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="4e95e-110">Preces šabloni</span><span class="sxs-lookup"><span data-stu-id="4e95e-110">Product masters</span></span>
-   <span data-ttu-id="4e95e-111">Preces dimensijas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="4e95e-111">Configuration product dimension</span></span>
-   <span data-ttu-id="4e95e-112">Konfigurācijas grupas</span><span class="sxs-lookup"><span data-stu-id="4e95e-112">Configuration groups</span></span>
-   <span data-ttu-id="4e95e-113">Materiālu komplekts (BOM)</span><span class="sxs-lookup"><span data-stu-id="4e95e-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="4e95e-114">Konfigurācijas maršruts</span><span class="sxs-lookup"><span data-stu-id="4e95e-114">Configuration route</span></span>
-   <span data-ttu-id="4e95e-115">Konfigurācijas noteikumi</span><span class="sxs-lookup"><span data-stu-id="4e95e-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="4e95e-116">Preces šabloni</span><span class="sxs-lookup"><span data-stu-id="4e95e-116">Product masters</span></span>

<span data-ttu-id="4e95e-117">Preces šablons ir sākuma punkts jebkurā preces konfigurācijas procesā.</span><span class="sxs-lookup"><span data-stu-id="4e95e-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="4e95e-118">Preces konfigurācijai atbilstoši dimensijām jāizmanto preces šablons ar konkrēto konfigurācijas tehnoloģiju un preces dimensiju grupa, kurā ietverta konfigurējamās preces dimensija.</span><span class="sxs-lookup"><span data-stu-id="4e95e-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="4e95e-119">Preces dimensijas konfigurācija</span><span class="sxs-lookup"><span data-stu-id="4e95e-119">Configuration product dimension</span></span>

<span data-ttu-id="4e95e-120">Konfigurējamās preces dimensija tiek izmantota, lai identificētu preces variantus preces šablonā, izmantojot konfigurācijas atbilstoši dimensijām tehnoloģiju.</span><span class="sxs-lookup"><span data-stu-id="4e95e-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="4e95e-121">Konfigurācijas dimensijas vērtību ievada lietotājs, un tai būtu jāpalīdz identificēt atsevišķus preces variantus.</span><span class="sxs-lookup"><span data-stu-id="4e95e-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="4e95e-122">Konfigurācijas grupas</span><span class="sxs-lookup"><span data-stu-id="4e95e-122">Configuration groups</span></span>

<span data-ttu-id="4e95e-123">Konfigurācijas grupas tiek definētas centrālajā repozitorijā un var tikt izmantotas visos no dimensijām atkarīgajos konfigurācijas modeļos.</span><span class="sxs-lookup"><span data-stu-id="4e95e-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="4e95e-124">Konfigurācijas grupas tiek saistītas ar atsevišķam MK rindām un ietver tādu rindu grupu, kuras ir savstarpēji izslēdzošas.</span><span class="sxs-lookup"><span data-stu-id="4e95e-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="4e95e-125">Tas nozīmē, ka katram preces variantam var atlasīt tikai vienu grupas rindu.</span><span class="sxs-lookup"><span data-stu-id="4e95e-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="4e95e-126">Materiālu komplekts (BOM)</span><span class="sxs-lookup"><span data-stu-id="4e95e-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="4e95e-127">MK atspoguļo no dimensijam atkarīgas preces konfigurācijas veidošanas blokus.</span><span class="sxs-lookup"><span data-stu-id="4e95e-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="4e95e-128">Tajā ir jāietver visas dažādās preces, ko var izmantot visiem preces variantiem.</span><span class="sxs-lookup"><span data-stu-id="4e95e-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="4e95e-129">Katrai MK rinda var būt atsauce uz konfigurāciju grupu.</span><span class="sxs-lookup"><span data-stu-id="4e95e-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="4e95e-130">Ja rindai nav atsauces uz konfigurāciju grupu, tā tiks iekļauta visos preces variantos.</span><span class="sxs-lookup"><span data-stu-id="4e95e-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="4e95e-131">Konfigurācijas maršruts</span><span class="sxs-lookup"><span data-stu-id="4e95e-131">Configuration route</span></span>

<span data-ttu-id="4e95e-132">Konfigurācijas maršruts nosaka konfigurāciju grupu secību, kādā tās tiks parādītas lietotājam preces konfigurēšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="4e95e-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="4e95e-133">Konfigurācijas noteikumi</span><span class="sxs-lookup"><span data-stu-id="4e95e-133">Configuration rules</span></span>

<span data-ttu-id="4e95e-134">Konfigurācijas nosacījumi ir mehānisms, kas nodrošina, ka vienā MK konfigurāciju grupā iekļautā prece īsteno preces iekļaušanu vai izslēgšanu viena MK dažādās konfigurāciju grupās.</span><span class="sxs-lookup"><span data-stu-id="4e95e-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="4e95e-135">Preces modelēšanas process</span><span class="sxs-lookup"><span data-stu-id="4e95e-135">Product modeling process</span></span>
<span data-ttu-id="4e95e-136">Veidojot no dimensijas atkarīgas preces modeli, parastā darbību secība sākas ar saistīto konfigurāciju grupu definēšanu.</span><span class="sxs-lookup"><span data-stu-id="4e95e-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="4e95e-137">Ir svarīgi pārliecināties, ka visas preces, kas tiks izmantotas MK, ir izlaistas uzņēmumam, kuram tiek veidots preces modelis.</span><span class="sxs-lookup"><span data-stu-id="4e95e-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="4e95e-138">Izmantojot šos veidošanas blokus, lietotājs var izveidot MK un piešķirt konfigurāciju grupas visiem saistītajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="4e95e-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="4e95e-139">Kad MK ir pabeigts, var definēt konfigurācijas maršrutu konfigurāciju grupu kārtošanai pareizā secībā.</span><span class="sxs-lookup"><span data-stu-id="4e95e-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="4e95e-140">[![No dimensijām atkarīgs preču modelēšanas process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Ja dažādās konfigurāciju grupās ir noteiktas preces, kas ir jālieto kopā vai kuras nedrīkst lietot kopā, tad varat izveidot konfigurācijas nosacījumus, kas liks ievērot šo preču attiecības.</span><span class="sxs-lookup"><span data-stu-id="4e95e-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="4e95e-141">Pēc tam, kad MK tiek saistīts ar no dimensijām atkarīgs preces šablonu, izmantojot MK versiju, un abi ir apstiprināti un aktivizēti, varat izveidot preces konfigurācijas un ievadīt nosaukumu katrai konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="4e95e-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="4e95e-142">Konfigurācijas var definēt pirms tiek ģenerētas jebkādas transakcijas, vai arī to var izdarīt tad, kad rodas vajadzība pēc noteiktas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="4e95e-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="4e95e-143">Ieteiktais pielietojums</span><span class="sxs-lookup"><span data-stu-id="4e95e-143">Suggested use</span></span>

<span data-ttu-id="4e95e-144">Tehnoloģiju Konfigurācija atbilstoši dimensijām ieteicams lietot precēm ar ierobežotu mainīgumu, un noteikta preces varianta identificēšanai ir piemērota standarta preces dimensijs izmēru, krāsas, stila un konfigurācijas kombinācija.</span><span class="sxs-lookup"><span data-stu-id="4e95e-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="4e95e-145">Piemēram, velosipēds ar rāmja augstumu, riteņu diametru, bremžu veidu un vairākiem pārnesumiem.</span><span class="sxs-lookup"><span data-stu-id="4e95e-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="4e95e-146">Nākošais solis</span><span class="sxs-lookup"><span data-stu-id="4e95e-146">Next step</span></span> 

<span data-ttu-id="4e95e-147">Nākamie astoņi uzdevumu ceļveži ir uzskaitīti tādā secībā, kādā jums tie ir jāizpilda.</span><span class="sxs-lookup"><span data-stu-id="4e95e-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="4e95e-148">Uz dimensijas balstītas preces šablona izveide</span><span class="sxs-lookup"><span data-stu-id="4e95e-148">Create a dimension-based product master</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="4e95e-149">Uz dimensijas balstītas preces šablona izlaišana</span><span class="sxs-lookup"><span data-stu-id="4e95e-149">Release a dimension-based product master</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="4e95e-150">Pilnīga izlaistās preces šablona pamata iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4e95e-150">Complete basic setup of a released product master</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="4e95e-151">Konfigurācijas grupu definēšana</span><span class="sxs-lookup"><span data-stu-id="4e95e-151">Define configuration groups</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="4e95e-152">Materiālu komplekta izveide uz dimensiju balstītas preces šablonam</span><span class="sxs-lookup"><span data-stu-id="4e95e-152">Create a bill of materials for a dimension-based product master</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="4e95e-153">Konfigurācijas maršrutu definēšana</span><span class="sxs-lookup"><span data-stu-id="4e95e-153">Define configuration routes</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="4e95e-154">Konfigurācijas kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="4e95e-154">Create configuration rules</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="4e95e-155">Konfigurāciju izveide atbilstoši dimensijām</span><span class="sxs-lookup"><span data-stu-id="4e95e-155">Create dimension-based configurations</span></span>](tasks/create-dimension-based-configurations.md)

