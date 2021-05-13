---
title: Preces numuru nomenklatūras izveide konfigurētiem preces variantiem
description: Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921015"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="ba760-103">Preces numuru nomenklatūras izveide konfigurētiem preces variantiem</span><span class="sxs-lookup"><span data-stu-id="ba760-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba760-104">Šajā procedūrā parādīts, kā iestatīt preces numura nomenklatūru konfigurētiem preču variantiem, un kā to var piesaistīt konfigurējamam preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="ba760-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="ba760-105">Šajā procedūrā ir parādīts, kā jūs varat izveidot konfigurācijas nomenklatūru preces konfigurācijas modeļa komponentam.</span><span class="sxs-lookup"><span data-stu-id="ba760-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="ba760-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="ba760-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ba760-107">Jauna preces numura nomenklatūra tiek piešķirta D0004 preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="ba760-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="ba760-108">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="ba760-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ba760-109">Izveidot preces numura nomenklatūru</span><span class="sxs-lookup"><span data-stu-id="ba760-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="ba760-110">Dodieties uz **Preču informācijas pārvaldība \> Iestātījums \> Produktu nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="ba760-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="ba760-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ba760-111">Select **New**.</span></span>
1. <span data-ttu-id="ba760-112">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="ba760-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="ba760-114">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-114">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-115">Atlasiet **Galvenā produkta numurs**.</span><span class="sxs-lookup"><span data-stu-id="ba760-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="ba760-116">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-116">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-117">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="ba760-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="ba760-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-119">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ba760-120">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-120">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-121">Atlasīt **Konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="ba760-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="ba760-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba760-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="ba760-123">Piešķirt preces numura nomenklatūru preces šablonam</span><span class="sxs-lookup"><span data-stu-id="ba760-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="ba760-124">Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Produktu šabloni**.</span><span class="sxs-lookup"><span data-stu-id="ba760-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="ba760-125">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="ba760-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ba760-126">Piemēram, filtrējiet pēc lauka **Preces numurs**, izmantojot vērtību 'D'.</span><span class="sxs-lookup"><span data-stu-id="ba760-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="ba760-127">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ba760-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="ba760-128">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ba760-128">Select **Edit**.</span></span>
1. <span data-ttu-id="ba760-129">Atlasiet *Jā* laukā **Izmantot nomenklatūru**.</span><span class="sxs-lookup"><span data-stu-id="ba760-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="ba760-130">Ievadiet vai atlasiet vērtību laukā **Produkta varianta numura nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="ba760-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba760-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba760-131">Close the page.</span></span>
1. <span data-ttu-id="ba760-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba760-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="ba760-133">Izveidot nomenklatūru preces konfigurācijas modeļa komponentam</span><span class="sxs-lookup"><span data-stu-id="ba760-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="ba760-134">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="ba760-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="ba760-135">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ba760-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="ba760-136">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ba760-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="ba760-137">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ba760-137">Select **Edit**.</span></span>
1. <span data-ttu-id="ba760-138">Atlasiet *Jā* laukā **Izmantot konfigurācijas nomenklatūru**.</span><span class="sxs-lookup"><span data-stu-id="ba760-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="ba760-139">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-139">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-140">Atlasiet **Atribūta vērtība**.</span><span class="sxs-lookup"><span data-stu-id="ba760-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="ba760-141">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-142">Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba760-143">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-143">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-144">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="ba760-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="ba760-145">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-146">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ba760-147">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-147">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-148">Atlasiet **Atribūta vērtība**.</span><span class="sxs-lookup"><span data-stu-id="ba760-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="ba760-149">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-150">Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba760-151">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-151">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-152">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="ba760-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="ba760-153">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-154">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ba760-155">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-155">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-156">Atlasiet **Atribūta vērtība**.</span><span class="sxs-lookup"><span data-stu-id="ba760-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="ba760-157">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-158">Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba760-159">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-159">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-160">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="ba760-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="ba760-161">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-162">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ba760-163">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-163">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-164">Atlasiet **Atribūta vērtība**.</span><span class="sxs-lookup"><span data-stu-id="ba760-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="ba760-165">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-166">Laukā **Atribūts** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba760-167">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-167">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-168">Atlasiet **Pastāvīgais teksts**.</span><span class="sxs-lookup"><span data-stu-id="ba760-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="ba760-169">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-170">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ba760-171">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba760-171">Select **Add**.</span></span>
1. <span data-ttu-id="ba760-172">Atlasiet **Numuru sērijas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="ba760-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="ba760-173">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ba760-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="ba760-174">Laukā **Numuru sērija** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ba760-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="ba760-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba760-175">Close the page.</span></span>
1. <span data-ttu-id="ba760-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba760-176">Close the page.</span></span>
1. <span data-ttu-id="ba760-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ba760-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]