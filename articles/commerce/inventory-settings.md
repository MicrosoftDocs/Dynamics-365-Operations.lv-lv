---
title: Krājumu iestatījumu lietošana
description: Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7d25fd62efca52dd2d60ed3435104c3507a1d19
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817613"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="8420e-103">Krājumu iestatījumu lietošana</span><span class="sxs-lookup"><span data-stu-id="8420e-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8420e-104">Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8420e-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8420e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8420e-105">Overview</span></span>

<span data-ttu-id="8420e-106">Krājumu iestatījumi nosaka, vai krājumi ir jāpārbauda pirms preču pievienošanas grozam.</span><span class="sxs-lookup"><span data-stu-id="8420e-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="8420e-107">Tie arī definē ar krājumiem saistītus preču pārdošanas ziņojumus, piemēram, "Noliktavā" un "Tikai daži atlikuši."</span><span class="sxs-lookup"><span data-stu-id="8420e-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="8420e-108">Šie iestatījumi nodrošina, ka preci nevar iegādāties, ja tā nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8420e-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="8420e-109">Dynamics 365 Commerce nodrošina rīcībā esošo preču pieejamības aplēses.</span><span class="sxs-lookup"><span data-stu-id="8420e-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="8420e-110">Informāciju par to, kā tiek aprēķināta aplēstā rīcībā esošo preču pieejamība, skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="8420e-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="8420e-111">Commerce vietņu veidotājā var definēt krājumu robežvērtības un diapazonus precei vai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="8420e-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="8420e-112">Tās nosaka, vai krājumus var klasificēt kā Noliktavā, Mazi krājumi vai Nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8420e-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="8420e-113">Plašāku informāciju skatiet [Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="8420e-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8420e-114">Krājumu robežvērtību un diapazonu atbalsts ir pieejams Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="8420e-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="8420e-115">Krājumu iestatījumi</span><span class="sxs-lookup"><span data-stu-id="8420e-115">Inventory settings</span></span>

<span data-ttu-id="8420e-116">Commerce krājumu iestatījumi tiek definēti vietņu veidotājā **Vietas iestatījumi \> Paplašinājumi \> Krājumu vadība**.</span><span class="sxs-lookup"><span data-stu-id="8420e-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="8420e-117">Ir četri krājumu iestatījumi, no kuriem viens ir novecojis.</span><span class="sxs-lookup"><span data-stu-id="8420e-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="8420e-118">**Iespējot krājumu pārbaudi programmā** — šis iestatījums ieslēdz preču krājumu pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="8420e-118">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="8420e-119">Pēc tam pirkšanas lodziņš, grozs un saņemšanas moduļi pārbauda preču krājumus un ļaus preci pievienot grozam tikai tad, ja krājumi ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="8420e-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="8420e-120">**Krājumu līmenis, pamatojoties uz** — šis iestatījums nosaka, kā tiek aprēķināti krājumu līmeņi.</span><span class="sxs-lookup"><span data-stu-id="8420e-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="8420e-121">Pieejamās vērtības ir **Kopējais pieejamais daudzums**, **Fiziski pieejamais daudzums** un **Robežvērtība Nav noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="8420e-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="8420e-122">Commerce krājumu robežvērtības un diapazonus var definēt katrai precei un kategorijai.</span><span class="sxs-lookup"><span data-stu-id="8420e-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="8420e-123">Krājumu API atgriež preču krājuma informācija par rekvizītu **Kopējais pieejamais daudzums** un rekvizītu **Fiziski pieejamais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="8420e-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="8420e-124">Mazumtirgotājs lemj, vai vērtība **Kopējais pieejamais daudzums** vai **Fiziski pieejamais daudzums** būtu jāizmanto, lai noteiktu krājumus skaitu un atbilstīgos diapazonus statusam Noliktavā un Nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8420e-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="8420e-125">Iestatījuma **Robežvērtība Nav noliktavā** vērtība **Krājumu līmenis, pamatojoties uz** ir veca (mantota), novecojusi vērtība.</span><span class="sxs-lookup"><span data-stu-id="8420e-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="8420e-126">To atlasot, krājumu skaits tiek noteikts no vērtības **Kopējais pieejamais daudzums** rezultātiem, bet robežvērtību nosaka skaitliskais iestatījums **Robežvērtība Nav noliktavā**, kas aprakstīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="8420e-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="8420e-127">Šis robežvērtības iestatījums attiecas uz visām e-Komercijas vietnē esošajām precēm.</span><span class="sxs-lookup"><span data-stu-id="8420e-127">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="8420e-128">Ja krājumi ir mazāki par robežvērtības skaitli, tiek uzskatīts, ka preces nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8420e-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="8420e-129">Pretējā gadījumā tiek uzskatīts, ka tā ir noliktavā.</span><span class="sxs-lookup"><span data-stu-id="8420e-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="8420e-130">Vērtības **Robežvērtība Nav noliktavā** iespējas ir ierobežotas, un nav ieteicams to lietot versijā 10.0.12 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="8420e-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="8420e-131">**Krājumu diapazoni** — šis iestatījums nosaka krājumu diapazonus, kas tiek parādīti uz vietas moduļiem.</span><span class="sxs-lookup"><span data-stu-id="8420e-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="8420e-132">To var lietot tikai tad, ja ir atlasīta vērtība **Kopējais pieejamais daudzums** vai vērtība **Fiziski pieejamais daudzums** iestatījumam **Krājumu līmenis, pamatojoties uz**.</span><span class="sxs-lookup"><span data-stu-id="8420e-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="8420e-133">Pieejamās vērtības ir **Viss** **Mazi krājumi un nav noliktavā** un **Nav noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="8420e-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="8420e-134">Atlasot **Viss**, tiks parādīti ziņojumi par visiem krājumu diapazoniem — no Noliktavā (ziņojums "Pieejams") līdz Nav noliktavā (ziņojums "Nav noliktavā").</span><span class="sxs-lookup"><span data-stu-id="8420e-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="8420e-135">Atlasot **Mazi krājumi un nav noliktavā**, tiks parādīti ziņojumi par visiem krājumu diapazoniem, izņemot Noliktavā (ziņojums "Pieejams").</span><span class="sxs-lookup"><span data-stu-id="8420e-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="8420e-136">Atlasot **Nav noliktavā**, tiks parādīts tikai paziņojums "Nav noliktavā".</span><span class="sxs-lookup"><span data-stu-id="8420e-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="8420e-137">**Robežvērtība Nav noliktavā** — šis vecais skaitliskais iestatījums stāsies spēkā tikai tad, ja iestatījumam **Krājumu līmenis, pamatojoties uz** ir atlasīta vērtība **Robežvērtība Nav noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="8420e-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8420e-138">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="8420e-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="8420e-139">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="8420e-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="8420e-140">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="8420e-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="8420e-141">Moduļi, kas izmanto krājumu iestatījumus</span><span class="sxs-lookup"><span data-stu-id="8420e-141">Modules that use inventory settings</span></span>

<span data-ttu-id="8420e-142">Pirkšanas lodziņš, vēlmju saraksts, veikala selektors, grozs un groza ikonu moduļi izmanto krājumu iestatījumus, lai parādītu krājumu diapazonus un ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="8420e-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="8420e-143">Attēlā zemāk ir parādīts preces informācijas lapas (PDP) piemērs, kas parāda krājumu Noliktavā ("pieejams") ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8420e-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![PDP moduļa piemērs ar ziņojumu Noliktavā](./media/pdp-InStock.png)

<span data-ttu-id="8420e-145">Attēlā zemāk ir parādīts preces informācijas lapas (PDP) piemērs, kas parāda krājumu Nav noliktavā ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8420e-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![PDP moduļa piemērs ar ziņojumu Nav noliktavā](./media/pdp-outofstock.png)

<span data-ttu-id="8420e-147">Attēlā zemāk ir parādīts groza piemērs, kas parāda krājumu Noliktavā ("Pieejams") ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8420e-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Groza moduļa piemērs ar ziņojumu Noliktavā](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="8420e-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8420e-149">Additional resources</span></span>

[<span data-ttu-id="8420e-150">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="8420e-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8420e-151">Krājumu buferu un krājumu līmeņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8420e-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="8420e-152">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="8420e-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8420e-153">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="8420e-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8420e-154">Konta pārvaldības lapas un moduļi</span><span class="sxs-lookup"><span data-stu-id="8420e-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="8420e-155">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="8420e-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8420e-156">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="8420e-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
