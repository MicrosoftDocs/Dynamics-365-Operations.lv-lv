---
title: Krājumu iestatījumu lietošana
description: Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ae0195f63b123a345b0cdcd4976bfd25b3b3d6d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019083"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="57359-103">Krājumu iestatījumu lietošana</span><span class="sxs-lookup"><span data-stu-id="57359-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="57359-104">Šajā tēmā ir ietverti krājumu iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="57359-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="57359-105">Krājumu iestatījumi nosaka, vai krājumi ir jāpārbauda pirms preču pievienošanas grozam.</span><span class="sxs-lookup"><span data-stu-id="57359-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="57359-106">Tie arī definē ar krājumiem saistītus preču pārdošanas ziņojumus, piemēram, "Noliktavā" un "Tikai daži atlikuši."</span><span class="sxs-lookup"><span data-stu-id="57359-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="57359-107">Šie iestatījumi nodrošina, ka preci nevar iegādāties, ja tā nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="57359-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="57359-108">Dynamics 365 Commerce nodrošina rīcībā esošo preču pieejamības aplēses.</span><span class="sxs-lookup"><span data-stu-id="57359-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="57359-109">Informāciju par to, kā tiek aprēķināta aplēstā rīcībā esošo preču pieejamība, skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="57359-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="57359-110">Commerce vietņu veidotājā var definēt krājumu robežvērtības un diapazonus precei vai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="57359-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="57359-111">Tās nosaka, vai krājumus var klasificēt kā Noliktavā, Mazi krājumi vai Nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="57359-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="57359-112">Plašāku informāciju skatiet [Krājumu buferu un krājumu līmeņu konfigurēšana](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="57359-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="57359-113">Krājumu robežvērtību un diapazonu atbalsts ir pieejams Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="57359-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="57359-114">Krājumu iestatījumi</span><span class="sxs-lookup"><span data-stu-id="57359-114">Inventory settings</span></span>

<span data-ttu-id="57359-115">Commerce krājumu iestatījumi tiek definēti vietņu veidotājā **Vietas iestatījumi \> Paplašinājumi \> Krājumu vadība**.</span><span class="sxs-lookup"><span data-stu-id="57359-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="57359-116">Ir pieci krājumu iestatījumi, no kuriem viens ir novecojis.</span><span class="sxs-lookup"><span data-stu-id="57359-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="57359-117">**Iespējot krājumu pārbaudi programmā** — šis iestatījums ieslēdz preču krājumu pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="57359-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="57359-118">Pēc tam pirkšanas lodziņš, grozs un saņemšanas moduļi pārbauda preču krājumus un ļaus preci pievienot grozam tikai tad, ja krājumi ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="57359-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="57359-119">**Krājumu līmenis, pamatojoties uz** — šis iestatījums nosaka, kā tiek aprēķināti krājumu līmeņi.</span><span class="sxs-lookup"><span data-stu-id="57359-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="57359-120">Pieejamās vērtības ir **Kopējais pieejamais daudzums**, **Fiziski pieejamais daudzums** un **Robežvērtība Nav noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="57359-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="57359-121">Commerce krājumu robežvērtības un diapazonus var definēt katrai precei un kategorijai.</span><span class="sxs-lookup"><span data-stu-id="57359-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="57359-122">Krājumu API atgriež preču krājuma informācija par rekvizītu **Kopējais pieejamais daudzums** un rekvizītu **Fiziski pieejamais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="57359-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="57359-123">Mazumtirgotājs lemj, vai vērtība **Kopējais pieejamais daudzums** vai **Fiziski pieejamais daudzums** būtu jāizmanto, lai noteiktu krājumus skaitu un atbilstīgos diapazonus statusam Noliktavā un Nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="57359-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="57359-124">Iestatījuma **Robežvērtība Nav noliktavā** vērtība **Krājumu līmenis, pamatojoties uz** ir veca (mantota), novecojusi vērtība.</span><span class="sxs-lookup"><span data-stu-id="57359-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="57359-125">To atlasot, krājumu skaits tiek noteikts no vērtības **Kopējais pieejamais daudzums** rezultātiem, bet robežvērtību nosaka skaitliskais iestatījums **Robežvērtība Nav noliktavā**, kas aprakstīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="57359-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="57359-126">Šis robežvērtības iestatījums attiecas uz visām e-Komercijas vietnē esošajām precēm.</span><span class="sxs-lookup"><span data-stu-id="57359-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="57359-127">Ja krājumi ir mazāki par robežvērtības skaitli, tiek uzskatīts, ka preces nav noliktavā.</span><span class="sxs-lookup"><span data-stu-id="57359-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="57359-128">Pretējā gadījumā tiek uzskatīts, ka tā ir noliktavā.</span><span class="sxs-lookup"><span data-stu-id="57359-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="57359-129">Vērtības **Robežvērtība Nav noliktavā** iespējas ir ierobežotas, un nav ieteicams to lietot versijā 10.0.12 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="57359-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="57359-130">**Krājumu līmenis vairākām noliktavām** – šis iestatījums ļauj krājuma līmeni aprēķināt attiecībā pret noklusējuma noliktavu vai vairākām noliktavām.</span><span class="sxs-lookup"><span data-stu-id="57359-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="57359-131">Opcija **Pamatojoties uz atsevišķu noliktavu** aprēķinās krājumu līmeņi, pamatojoties uz noklusējuma noliktavu.</span><span class="sxs-lookup"><span data-stu-id="57359-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="57359-132">Vai arī e-komercijas vietne var norādīt uz vairākām noliktavām, lai atvieglotu izpildi.</span><span class="sxs-lookup"><span data-stu-id="57359-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="57359-133">Šajā gadījumā, opcija **Balstoties uz apkopoto nosūtīšanas un saņemšanas noliktavām** tiek izmantota, lai norādītu krājumu pieejamību.</span><span class="sxs-lookup"><span data-stu-id="57359-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="57359-134">Piemēram, kad debitors iegādājas krājumu un kā piegādes veidu atlasa "piegāde", krājumu var nosūtīt no jebkuras noliktavas izpildes grupā, kurā ir pieejami krājumi.</span><span class="sxs-lookup"><span data-stu-id="57359-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="57359-135">Preces informācijas lapa (product details page - PDP) nosūtīšanai parādīs ziņojumu "Noliktavā", ja kādai pieejamai nosūtīšanas noliktavai izpildes grupā ir krājumi.</span><span class="sxs-lookup"><span data-stu-id="57359-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="57359-136">Iestātījums **Krājumu līmenis vairākām noliktavām** ir pieejams Commerce versijā 10.0.19. versijā.</span><span class="sxs-lookup"><span data-stu-id="57359-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="57359-137">Ja veicat atjaunināšanu no vecākas Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="57359-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="57359-138">Instrukcijas skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="57359-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="57359-139">**Krājumu diapazoni** — šis iestatījums nosaka krājumu diapazonus, kas tiek parādīti uz vietas moduļiem.</span><span class="sxs-lookup"><span data-stu-id="57359-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="57359-140">To var lietot tikai tad, ja ir atlasīta vērtība **Kopējais pieejamais daudzums** vai vērtība **Fiziski pieejamais daudzums** iestatījumam **Krājumu līmenis, pamatojoties uz**.</span><span class="sxs-lookup"><span data-stu-id="57359-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="57359-141">Pieejamās vērtības ir **Viss** **Mazi krājumi un nav noliktavā** un **Nav noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="57359-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="57359-142">Atlasot **Viss**, tiks parādīti ziņojumi par visiem krājumu diapazoniem — no Noliktavā (ziņojums "Pieejams") līdz Nav noliktavā (ziņojums "Nav noliktavā").</span><span class="sxs-lookup"><span data-stu-id="57359-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="57359-143">Atlasot **Mazi krājumi un nav noliktavā**, tiks parādīti ziņojumi par visiem krājumu diapazoniem, izņemot Noliktavā (ziņojums "Pieejams").</span><span class="sxs-lookup"><span data-stu-id="57359-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="57359-144">Atlasot **Nav noliktavā**, tiks parādīts tikai paziņojums "Nav noliktavā".</span><span class="sxs-lookup"><span data-stu-id="57359-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="57359-145">**Robežvērtība Nav noliktavā** — šis vecais skaitliskais iestatījums stāsies spēkā tikai tad, ja iestatījumam **Krājumu līmenis, pamatojoties uz** ir atlasīta vērtība **Robežvērtība Nav noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="57359-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="57359-146">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.12 laidienā.</span><span class="sxs-lookup"><span data-stu-id="57359-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="57359-147">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="57359-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="57359-148">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="57359-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="57359-149">Moduļi, kas izmanto krājumu iestatījumus</span><span class="sxs-lookup"><span data-stu-id="57359-149">Modules that use inventory settings</span></span>

<span data-ttu-id="57359-150">Pirkšanas lodziņš, vēlmju saraksts, veikala selektors, grozs un groza ikonu moduļi izmanto krājumu iestatījumus, lai parādītu krājumu diapazonus un ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="57359-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="57359-151">Piemērā, kā parādīts šajā ilustrācijā, PDP rāda noliktavas ("Pieejams") ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="57359-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![PDP moduļa piemērs ar ziņojumu Noliktavā](./media/pdp-InStock.png)

<span data-ttu-id="57359-153&quot;>Piemērā, kā parādīts šajā ilustrācijā, PDP rāda (&quot;Nav pieejams") ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="57359-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![PDP moduļa piemērs ar ziņojumu Nav noliktavā](./media/pdp-outofstock.png)

<span data-ttu-id="57359-155&quot;>Piemērā, kā parādīts šajā ilustrācijā, grozs rāda noliktavas (&quot;Pieejams") ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="57359-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Groza moduļa piemērs ar ziņojumu Noliktavā](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="57359-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="57359-157">Additional resources</span></span>

[<span data-ttu-id="57359-158">Moduļu bibliotēkas pārskats</span><span class="sxs-lookup"><span data-stu-id="57359-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="57359-159">Krājumu buferu un krājumu līmeņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="57359-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="57359-160">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="57359-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="57359-161">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="57359-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="57359-162">Konta pārvaldības lapas un moduļi</span><span class="sxs-lookup"><span data-stu-id="57359-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="57359-163">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="57359-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="57359-164">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="57359-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
