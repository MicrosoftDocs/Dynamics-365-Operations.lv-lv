---
title: Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs
description: Šajā tēmā ir aprakstīts, kā iestatīt preču daudzuma ierobežojumus bizness-biznesam (B2B) e-komercijas vietnēs.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211181"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="19bfa-103">Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="19bfa-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19bfa-104">Šajā tēmā ir aprakstīts, kā iestatīt preču daudzuma ierobežojumus bizness-biznesam (B2B) e-komercijas vietnēs.</span><span class="sxs-lookup"><span data-stu-id="19bfa-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="19bfa-105">Lielākajai daļai preču grupēšanu nosaka mērvienība.</span><span class="sxs-lookup"><span data-stu-id="19bfa-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="19bfa-106">Grupēšana ietekmē preču pārdošanas veidu.</span><span class="sxs-lookup"><span data-stu-id="19bfa-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="19bfa-107">Dažām precēm var būt daudzumu papildu grupēšana.</span><span class="sxs-lookup"><span data-stu-id="19bfa-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="19bfa-108">Šī grupēšana nosaka, vai preces var pārdot kā atsevišķas vai daudzkārtējas vienības, un, vai ir jāievēro minimālais vai maksimālais pasūtījuma daudzuma ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="19bfa-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="19bfa-109">Daudzuma ierobežošanas līdzeklis nodrošina, ka minimālie, maksimālie, daudzkārtējie un standarta daudzumi, kas konfigurēti programmā Microsoft Dynamics 365 Commerce (noklusējuma pasūtījuma iestatījumos vai Commerce vietnes veidotāja vietnes iestatījumos), tiek lietoti klientu pasūtījumiem, kas tiek novietoti e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="19bfa-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="19bfa-110">Preces daudzuma ierobežojumi pārdošanas punktam (POS) un zvanu centriem pašlaik netiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="19bfa-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="19bfa-111">Daudzi mazumtirgotāji nodrošina iespēju izmantot klientu pasūtījumus (sauktus arī par īpašajiem pasūtījumiem), lai izpildītu dažādas preču un izpildes prasības.</span><span class="sxs-lookup"><span data-stu-id="19bfa-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="19bfa-112">Tālāk uzskaitīti daži tipiski scenāriji.</span><span class="sxs-lookup"><span data-stu-id="19bfa-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="19bfa-113">Klients vēlas, lai noteiktu variantu preces tiktu pārdotas daudzkārtēji.</span><span class="sxs-lookup"><span data-stu-id="19bfa-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="19bfa-114">Klients preces vēlas saņemt tādā veikalā vai atrašanās vietā, kas atšķiras no veikala vai atrašanās vietas, kur klients šīs preces iegādājās.</span><span class="sxs-lookup"><span data-stu-id="19bfa-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="19bfa-115">Tomēr veikalu iepakošanas standarti atšķiras no tiešsaistes pārdošanas sadales iepakošanas standartiem.</span><span class="sxs-lookup"><span data-stu-id="19bfa-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="19bfa-116">Klients vēlas iegādāties ierobežota izdevuma preci, kam ir piemērots maksimālā daudzuma ierobežojums preces iegādei.</span><span class="sxs-lookup"><span data-stu-id="19bfa-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="19bfa-117">Pasūtījuma noklusējuma iestatījumu līdzekļa ieslēgšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="19bfa-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="19bfa-118">Pirms varat iestatīt preču daudzuma ierobežojumus, programmā Commerce Headquarters ir jābūt ieslēgtam pasūtījuma noklusējuma iestatījumu līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="19bfa-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="19bfa-119">Lai ieslēgtu pasūtījuma noklusējuma iestatījumu līdzekli, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="19bfa-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="19bfa-120">Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="19bfa-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="19bfa-121">Atrodiet un atlasiet līdzekli **Atbalsts vietnes un pasūtījuma noklusējuma iestatījumiem klienta pasūtījumā**.</span><span class="sxs-lookup"><span data-stu-id="19bfa-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="19bfa-122">Labās rūts apakšdaļā atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="19bfa-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="19bfa-123">Daudzuma iestatījumu definēšana</span><span class="sxs-lookup"><span data-stu-id="19bfa-123">Define quantity settings</span></span> 

<span data-ttu-id="19bfa-124">Daudzuma iestatījumus varat definēt lapā **Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="19bfa-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="19bfa-125">Lai definētu daudzuma iestatījumus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="19bfa-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="19bfa-126">Dodieties uz Preču **Retail un Commerce \> Preces un kategorijas \> Izpildei nodotās preces pēc kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="19bfa-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="19bfa-127">Atlasiet izlaisto preci.</span><span class="sxs-lookup"><span data-stu-id="19bfa-127">Select a released product.</span></span>
1. <span data-ttu-id="19bfa-128">Darbību rūts cilnē **Pārvaldīt krājumu** grupā **Pasūtījuma iestatījumi** atlasiet **Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="19bfa-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="19bfa-129">Lapas **Pasūtījuma noklusējuma iestatījumi** kopsavilkuma cilnē **Pārdošanas pasūtījums** sadaļā **Pārdošanas daudzums** iestatiet preces pārdošanas daudzumu:</span><span class="sxs-lookup"><span data-stu-id="19bfa-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="19bfa-130">**Daudzkārtēji** – daudzums, kādā preces var iegādāties daudzkārtīgi.</span><span class="sxs-lookup"><span data-stu-id="19bfa-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="19bfa-131">**Minimālais pasūtījuma daudzums** – minimālais iegādājamo preču skaits.</span><span class="sxs-lookup"><span data-stu-id="19bfa-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="19bfa-132">**Maksimālais pasūtījuma daudzums** – maksimālais iegādājamo preču skaits.</span><span class="sxs-lookup"><span data-stu-id="19bfa-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="19bfa-133">**Standarta pasūtījuma daudzums** – noklusējuma daudzums, kas tiek ievadīts automātiski, kad produkts ir atlasīts.</span><span class="sxs-lookup"><span data-stu-id="19bfa-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="19bfa-134">Commerce vietnes veidotājā ieslēgšana B2B pasūtījuma daudzuma ierobežošanas līdzeklim</span><span class="sxs-lookup"><span data-stu-id="19bfa-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="19bfa-135">Lai ieslēgtu Commerce vietnes veidotāju B2B pasūtījuma daudzuma ierobežošanas līdzeklim, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="19bfa-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="19bfa-136">Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**</span><span class="sxs-lookup"><span data-stu-id="19bfa-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="19bfa-137">Zem sadaļas **Pasūtījuma daudzuma ierobežošanas iespējošana** atlasiet **Iespējot B2B klientiem** nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="19bfa-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="19bfa-138">Atjauninātā vietnes veidotāja iestatījumi stājas spēkā tikai pēc app.settings.json faila atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="19bfa-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="19bfa-139">Papildinformāciju skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="19bfa-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19bfa-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="19bfa-140">Additional resources</span></span>

[<span data-ttu-id="19bfa-141">B2B e-komercijas vietnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="19bfa-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="19bfa-142">Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām</span><span class="sxs-lookup"><span data-stu-id="19bfa-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="19bfa-143">Biznesa partnera lietotāju pārvaldība B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="19bfa-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="19bfa-144">Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs</span><span class="sxs-lookup"><span data-stu-id="19bfa-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]