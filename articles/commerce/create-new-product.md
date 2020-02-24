---
title: Jaunas preces izveide
description: Šajā tēmā aprakstīts, kā izveidot jaunu preci programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001971"
---
# <a name="create-a-new-product"></a><span data-ttu-id="96146-103">Jaunas preces izveide</span><span class="sxs-lookup"><span data-stu-id="96146-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="96146-104">Šajā tēmā aprakstīts, kā izveidot jaunu preci programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="96146-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="96146-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="96146-105">Overview</span></span>

<span data-ttu-id="96146-106">Preces galvenokārt nosaka pēc preces numura, nosaukuma un apraksta.</span><span class="sxs-lookup"><span data-stu-id="96146-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="96146-107">Lai aprakstītu preci vai pakalpojumu, tomēr ir nepieciešami arī citi dati.</span><span class="sxs-lookup"><span data-stu-id="96146-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="96146-108">Jaunas preces izveide</span><span class="sxs-lookup"><span data-stu-id="96146-108">Create a new product</span></span>

1. <span data-ttu-id="96146-109">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Preces pēc kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="96146-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="96146-110">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="96146-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="96146-111">Nolaižamajā saraksā **Preces veids** atlasiet vai nu **Krājums**, vai **Pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="96146-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="96146-112">Nolaižamajā sarakstā **Preces apakštips** atlasiet vai nu **Prece** (ja precei nebūs variantu), vai **Preces šablons** (ja precei būs varianti).</span><span class="sxs-lookup"><span data-stu-id="96146-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="96146-113">Ja lodziņš **Preces numurs** jau nav iepriekš aizpildīts, ievadiet tajā preces numuru.</span><span class="sxs-lookup"><span data-stu-id="96146-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="96146-114">Lodziņā **Preces nosaukums** ievadiet preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="96146-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="96146-115">Lodziņā **Saīsinātais nosaukums** ievadiet saīsināto nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="96146-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="96146-116">Nolaižamajā sarakstā **Mazumtirdzniecības kategorija** atlasiet atbilstošu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="96146-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="96146-117">Ja prece ir komplekts, izvēlieties **Jā** vaicājumam **Preču komplekts**.</span><span class="sxs-lookup"><span data-stu-id="96146-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="96146-118">Ja preces apakštips ir preces šablons, iestatiet **Preču dimensiju grupa**, lai iekļautu atbalstītos variantus.</span><span class="sxs-lookup"><span data-stu-id="96146-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="96146-119">Iespējamie varianti ir **Krāsa**, **Izmērs**, **Stils** un **Konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="96146-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="96146-120">Ja nepieciešams, jāizveido papildu preču dimensiju grupas.</span><span class="sxs-lookup"><span data-stu-id="96146-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="96146-121">Nolaižamajā sarakstā **Konfigurācijas tehnoloģija** atlasiet atbilstošu opciju.</span><span class="sxs-lookup"><span data-stu-id="96146-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="96146-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="96146-122">Select **OK**.</span></span>

<span data-ttu-id="96146-123">Tālāk redzamajā attēlā parādīts pievienojamās preces piemērs.</span><span class="sxs-lookup"><span data-stu-id="96146-123">The following image shows an example product being added.</span></span>

![Preces izveide](media/create-new-product.png)

<span data-ttu-id="96146-125">Kad prece ir pievienota, tai var iestatīt papildu datus, piemēram, **Preces apraksts**, **Variantu grupas**, **Dimensiju grupas**, **Preces īpašības** un **Saistītās preces**.</span><span class="sxs-lookup"><span data-stu-id="96146-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="96146-126">Tālāk redzamajā attēlā ir parādīta preces papildu informācija.</span><span class="sxs-lookup"><span data-stu-id="96146-126">The following image shows a product's additional details.</span></span>

![Papildinformācija par preci](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="96146-128">Izveidot preces variantus</span><span class="sxs-lookup"><span data-stu-id="96146-128">Create product variants</span></span>

<span data-ttu-id="96146-129">Ja preces apakštips ir **Preces šablons**, būs jāizveido noteikti varianti.</span><span class="sxs-lookup"><span data-stu-id="96146-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="96146-130">Lai izveidotu preču variantus, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="96146-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="96146-131">Darbību rūtī atlasiet **Preču varianti**.</span><span class="sxs-lookup"><span data-stu-id="96146-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="96146-132">Ja darbības rūtī ir atlasītas variantu grupas, atlasiet \**Variantu ieteikumi*.</span><span class="sxs-lookup"><span data-stu-id="96146-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="96146-133">Atlasiet variantus, kurus vēlaties atbalstīt šai precei.</span><span class="sxs-lookup"><span data-stu-id="96146-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="96146-134">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="96146-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="96146-135">Preces izlaišana</span><span class="sxs-lookup"><span data-stu-id="96146-135">Release a product</span></span>

<span data-ttu-id="96146-136">Lai pārdotu preci, tā vispirms jānodod juridiskai personai.</span><span class="sxs-lookup"><span data-stu-id="96146-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="96146-137">Preču lapā atlasiet **Preču izlaišana**.</span><span class="sxs-lookup"><span data-stu-id="96146-137">From the product page, select **Release products**.</span></span>

    ![Preces izlaišana](media/create-new-product-3.png)

1. <span data-ttu-id="96146-139">Atlasiet izlaižamo preci un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="96146-139">Select the product to release, and then select **Next**.</span></span>

    ![Izlaižamās preces izvēle](media/create-new-product-4.png)

1. <span data-ttu-id="96146-141">Atlasiet izlaižamo preču variantu komplektu un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="96146-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Izvēlēties izlaižamos variantus](media/create-new-product-5.png)

1. <span data-ttu-id="96146-143">Atlasiet juridisko personu un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="96146-143">Select the legal entity, and then select **Next**.</span></span>

    ![Izvēlieties juridisko personu](media/create-new-product-6.png)

1. <span data-ttu-id="96146-145">Atl. **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="96146-145">Select **Finish**.</span></span>

    ![Preces izlaišanas pabeigšana](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="96146-147">Izlaistās preces konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="96146-147">Configure a released product</span></span>

<span data-ttu-id="96146-148">Pēc preces izlaišanas tai būs nepieciešama turpmāka konfigurācija, kas ietver cenas pievienošanu precei.</span><span class="sxs-lookup"><span data-stu-id="96146-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="96146-149">Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Izlaistās preces pēc kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="96146-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="96146-150">Atlasiet preces kategorijas mezglu precei, kas tika izlaista, un pēc tam preču sarakstā atlasiet preci.</span><span class="sxs-lookup"><span data-stu-id="96146-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="96146-151">Darbību rūtī atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="96146-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="96146-152">Sadaļā **Pirkšana** konfigurējiet visus nepieciešamos rekvizītus, tostarp **Vienība**, **Cena**un **Daudzums**.</span><span class="sxs-lookup"><span data-stu-id="96146-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="96146-153">Darbības rūtī atlasiet **Pārbaudīt**, lai nodrošinātu, ka trūkstošajiem laukiem nav ziņotas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="96146-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="96146-154">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="96146-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="96146-155">Tālāk redzamajā attēlā ir parādīts izlaistās preces konfigurācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="96146-155">The following image shows an example configuration for a released product.</span></span>

![Izlaistās preces konfigurēšana](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="96146-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="96146-157">Additional resources</span></span>

[<span data-ttu-id="96146-158">Izveidot juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="96146-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="96146-159">Variantu grupas izveide</span><span class="sxs-lookup"><span data-stu-id="96146-159">Create a variant group</span></span>](create-variant-group.md) 
