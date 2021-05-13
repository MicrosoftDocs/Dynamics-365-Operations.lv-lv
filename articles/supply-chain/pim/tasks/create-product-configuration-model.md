---
title: Preces konfigurācijas modeļa izveide
description: Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921369"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="ea8d0-103">Preces konfigurācijas modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="ea8d0-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea8d0-104">Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="ea8d0-105">USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="ea8d0-106">Preču modeļa izveide</span><span class="sxs-lookup"><span data-stu-id="ea8d0-106">Create a product model</span></span>

1. <span data-ttu-id="ea8d0-107">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="ea8d0-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-108">Select **New**.</span></span>
1. <span data-ttu-id="ea8d0-109">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="ea8d0-110">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="ea8d0-111">Laukā **Risinātāja stratēģija** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="ea8d0-112">Risinātāja stratēģija nosaka, kā ierobežojumi tiek apstrādāti ierobežojumam atbilstošā preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="ea8d0-113">Šī atlase var ietekmēt preces konfigurācijas modeļa veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="ea8d0-114">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="ea8d0-115">Saknes komponents norāda preces konfigurācijas modeli, bet to var izmantot arī citos preču modeļos.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="ea8d0-116">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-116">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d0-117">Laukā **Atkārtoti izmantot konfigurācijas** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="ea8d0-118">Ja parametram Atkārtoti izmantot konfigurācijas ir iestatīta opcija Jā, sistēma meklēs identiskas konfigurācijas pēc katras konfigurācijas sesijas un atkārtoti tās izmantos, ja tiks atrasta precīza atbilstība.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="ea8d0-119">Pievienot atribūtus</span><span class="sxs-lookup"><span data-stu-id="ea8d0-119">Add attributes</span></span>

1. <span data-ttu-id="ea8d0-120">Izvērsiet sadaļu **Atribūti**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="ea8d0-121">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-121">Select **Add**.</span></span>
3. <span data-ttu-id="ea8d0-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ea8d0-123">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ea8d0-124">Laukā **Risinātāja nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="ea8d0-125">Risinātāja nosaukumu izmanto preču konfiguratora ierobežojumu risinātājs.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="ea8d0-126">Tajā nedrīkst būt atstarpes vai īpašas rakstzīmes, izņemot _ (pasvītrojums).</span><span class="sxs-lookup"><span data-stu-id="ea8d0-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="ea8d0-127">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="ea8d0-128">Apraksta teksts tiek rādīts konfigurācijas lietotājam un tādējādi var palīdzēt, izvēloties atbilstošo atribūta vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="ea8d0-129">Laukā **Atribūta veids** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea8d0-130">Atribūta tips nosaka, kādas vērtības ir pieejamas atribūtam.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="ea8d0-131">Atzīmējiet izvēles rūtiņu **Iekļaut atkārtotā izmantošanā**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="ea8d0-132">Šī iespēja pieejama tikai tad, ja ir atlasīta opcija Atkārtoti izmantot konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="ea8d0-133">Atribūta iekļaušana atkārtotas izmantošanas izvēles rūtiņā nozīmē, ka šis atribūts tiks ņemts vērā, kad sistēma meklē precīzu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="ea8d0-134">Apakškomponentu pievienošna</span><span class="sxs-lookup"><span data-stu-id="ea8d0-134">Add subcomponents</span></span>

1. <span data-ttu-id="ea8d0-135">Izvērsiet sadaļu **Apakškomponenti**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="ea8d0-136">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-136">Select **Add**.</span></span>
3. <span data-ttu-id="ea8d0-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ea8d0-138">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ea8d0-139">Laukā **Risinātāja nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="ea8d0-140">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="ea8d0-141">Laukā **Komponents** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea8d0-142">Katram apakškomponentam jābūt atsaucei uz komponenta definīciju.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="ea8d0-143">Šāds noformējums atbalsta atkārtoti izmantojamus komponentus un nodrošina, ka pēc komponenta definēšanas to var izmantot daudzos preču modeļos.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="ea8d0-144">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-144">Select **Save**.</span></span>
9. <span data-ttu-id="ea8d0-145">Atlasiet **Detalizēta MK rindas informācija**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="ea8d0-146">Veidlapa Detalizēta informācija par MK rindu ļauj lietotājam izvēlēties obligātos rekvizītus apakškomponentam.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="ea8d0-147">Katram rekvizītam var piešķirt fiksētu vērtību, vai to var kartēt uz atribūtu.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="ea8d0-148">Kartēšanas uz atribūtu rezultātā MK rindas rekvizītam būs atšķirīgas vērtības atkarībā no konfigurācijas atlases.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="ea8d0-149">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="ea8d0-150">Katrs apakškomponents pārstāv konfigurējamu preces šablonu ar konfigurācijas atbilstoši ierobežojumam tehnoloģiju.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="ea8d0-151">Atsaucei tiek izmantots krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="ea8d0-152">Atzīmējiet izvēles rūtiņu **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="ea8d0-153">Laukā **Aprēķins** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="ea8d0-154">Aprēķina opcijas iestatīšana nodrošina, ka prece tiks iekļauta, veicot preces izmaksu aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="ea8d0-155">Atlasiet cilni **Iestatījums**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="ea8d0-156">Atzīmējiet izvēles rūtiņu **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="ea8d0-157">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="ea8d0-158">Daudzuma lauks nosaka, kāds šīs preces dadzums tiks patērēts konfigurētajai precei.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="ea8d0-159">Atzīmējiet izvēles rūtiņu **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="ea8d0-160">Ievadiet skaitli laukā **Pa sērijām**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="ea8d0-161">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ea8d0-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]