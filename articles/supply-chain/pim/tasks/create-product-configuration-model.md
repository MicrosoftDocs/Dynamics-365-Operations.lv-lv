--- 
title: "Preces konfigurācijas modeļa izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e521cb9d19f2af8f931795b64ab338a3c6692399
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="9f455-103">Preces konfigurācijas modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="9f455-103">Create a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f455-104">Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus.</span><span class="sxs-lookup"><span data-stu-id="9f455-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="9f455-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="9f455-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="9f455-106">Preču modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="9f455-106">Create a product model</span></span>
1. <span data-ttu-id="9f455-107">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="9f455-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9f455-108">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="9f455-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="9f455-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f455-109">Click New.</span></span>
4. <span data-ttu-id="9f455-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9f455-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9f455-112">Laukā Risinātāja stratēģija atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9f455-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="9f455-113">Risinātāja stratēģija nosaka, kā ierobežojumi tiek apstrādāti ierobežojumam atbilstošā preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="9f455-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="9f455-114">Šī atlase var ietekmēt preces konfigurācijas modeļa veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="9f455-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="9f455-115">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9f455-116">Saknes komponents norāda preces konfigurācijas modeli, bet to var izmantot arī citos preču modeļos.</span><span class="sxs-lookup"><span data-stu-id="9f455-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="9f455-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9f455-117">Click OK.</span></span>
9. <span data-ttu-id="9f455-118">Laukā Atkārtoti izmantot konfigurācijas atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="9f455-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="9f455-119">Ja parametram Atkārtoti izmantot konfigurācijas ir iestatīta opcija Jā, sistēma meklēs identiskas konfigurācijas pēc katras konfigurācijas sesijas un atkārtoti tās izmantos, ja tiks atrasta precīza atbilstība.</span><span class="sxs-lookup"><span data-stu-id="9f455-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="9f455-120">Pievienot atribūtus</span><span class="sxs-lookup"><span data-stu-id="9f455-120">Add attributes</span></span>
1. <span data-ttu-id="9f455-121">Izvērsiet sadaļu Atribūti.</span><span class="sxs-lookup"><span data-stu-id="9f455-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="9f455-122">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9f455-122">Click Add.</span></span>
3. <span data-ttu-id="9f455-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9f455-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9f455-124">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9f455-125">Laukā Risinātāja nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="9f455-126">Risinātāja nosaukumu izmanto preču konfiguratora ierobežojumu risinātājs.</span><span class="sxs-lookup"><span data-stu-id="9f455-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="9f455-127">Tajā nedrīkst būt atstarpes vai īpašas rakstzīmes, izņemot _ (pasvītrojums).</span><span class="sxs-lookup"><span data-stu-id="9f455-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="9f455-128">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9f455-129">Apraksta teksts tiek rādīts konfigurācijas lietotājam un tādējādi var palīdzēt, izvēloties atbilstošo atribūta vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="9f455-130">Laukā Atribūta tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="9f455-131">Atribūta tips nosaka, kādas vērtības ir pieejamas atribūtam.</span><span class="sxs-lookup"><span data-stu-id="9f455-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="9f455-132">Atzīmējiet izvēles rūtiņu Iekļaut atkārtotā izmantošanā.</span><span class="sxs-lookup"><span data-stu-id="9f455-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="9f455-133">Šī iespēja pieejama tikai tad, ja ir atlasīta opcija Atkārtoti izmantot konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="9f455-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="9f455-134">Atribūta iekļaušana atkārtotas izmantošanas izvēles rūtiņā nozīmē, ka šis atribūts tiks ņemts vērā, kad sistēma meklē precīzu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="9f455-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="9f455-135">Apakškomponentu pievienošna</span><span class="sxs-lookup"><span data-stu-id="9f455-135">Add subcomponents</span></span>
1. <span data-ttu-id="9f455-136">Izvērsiet sadaļu Apakškomponenti.</span><span class="sxs-lookup"><span data-stu-id="9f455-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="9f455-137">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="9f455-137">Click Add.</span></span>
3. <span data-ttu-id="9f455-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="9f455-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9f455-139">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9f455-140">Laukā Risinātāja nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="9f455-141">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="9f455-142">Laukā Komponents ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="9f455-143">Katram apakškomponentam jābūt atsaucei uz komponenta definīciju.</span><span class="sxs-lookup"><span data-stu-id="9f455-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="9f455-144">Šāds noformējums atbalsta atkārtoti izmantojamus komponentus un nodrošina, ka pēc komponenta definēšanas to var izmantot daudzos preču modeļos.</span><span class="sxs-lookup"><span data-stu-id="9f455-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="9f455-145">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f455-145">Click Save.</span></span>
9. <span data-ttu-id="9f455-146">Noklikšķiniet uz Detalizēta informācija par MK rindu.</span><span class="sxs-lookup"><span data-stu-id="9f455-146">Click BOM line details.</span></span>
    * <span data-ttu-id="9f455-147">Veidlapa Detalizēta informācija par MK rindu ļauj lietotājam izvēlēties obligātos rekvizītus apakškomponentam.</span><span class="sxs-lookup"><span data-stu-id="9f455-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="9f455-148">Katram rekvizītam var piešķirt fiksētu vērtību, vai to var kartēt uz atribūtu.</span><span class="sxs-lookup"><span data-stu-id="9f455-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="9f455-149">Kartēšanas uz atribūtu rezultātā MK rindas rekvizītam būs atšķirīgas vērtības atkarībā no konfigurācijas atlases.</span><span class="sxs-lookup"><span data-stu-id="9f455-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="9f455-150">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f455-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9f455-151">Katrs apakškomponents pārstāv konfigurējamu preces šablonu ar konfigurācijas atbilstoši ierobežojumam tehnoloģiju.</span><span class="sxs-lookup"><span data-stu-id="9f455-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="9f455-152">Atsaucei tiek izmantots krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="9f455-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="9f455-153">Atzīmējiet izvēles rūtiņu Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="9f455-153">Select the Set check box.</span></span>
12. <span data-ttu-id="9f455-154">Laukā Aprēķins atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="9f455-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="9f455-155">Aprēķina opcijas iestatīšana nodrošina, ka prece tiks iekļauta, veicot preces izmaksu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="9f455-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="9f455-156">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="9f455-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="9f455-157">Atzīmējiet izvēles rūtiņu Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="9f455-157">Select the Set check box.</span></span>
15. <span data-ttu-id="9f455-158">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="9f455-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9f455-159">Daudzuma lauks nosaka, kāds šīs preces dadzums tiks patērēts konfigurētajai precei.</span><span class="sxs-lookup"><span data-stu-id="9f455-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="9f455-160">Atzīmējiet izvēles rūtiņu Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="9f455-160">Select the Set check box.</span></span>
17. <span data-ttu-id="9f455-161">Ievadiet skaitli laukā Pa sērijām.</span><span class="sxs-lookup"><span data-stu-id="9f455-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="9f455-162">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9f455-162">Click OK.</span></span>


