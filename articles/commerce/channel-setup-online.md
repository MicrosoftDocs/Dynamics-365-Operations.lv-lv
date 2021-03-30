---
title: Tiešsaistes kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu tiešsaistes kanālu risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 44cc63560c048031c8315dc3f15ef07583bdc266
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218349"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="5b057-103">Tiešsaistes kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5b057-104">Šajā tēmā aprakstīts, kā izveidot jaunu tiešsaistes kanālu risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5b057-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5b057-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="5b057-105">Overview</span></span>

<span data-ttu-id="5b057-106">Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus.</span><span class="sxs-lookup"><span data-stu-id="5b057-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="5b057-107">Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali).</span><span class="sxs-lookup"><span data-stu-id="5b057-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="5b057-108">Tiešsaistes veikali dod klientiem iespēju papildus mazumtirdzniecības veikaliem iegādāties produktus arī no mazumtirgotāja tiešsaistes veikala.</span><span class="sxs-lookup"><span data-stu-id="5b057-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="5b057-109">Lai izveidotu tiešsaistes veikalu pakalpojumā Commerce, vispirms ir jāizveido tiešsaistes kanāls.</span><span class="sxs-lookup"><span data-stu-id="5b057-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="5b057-110">Pirms jauna tiešsaistes kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5b057-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="5b057-111">Pirms varat izveidot jaunu vietni, jāizveido vismaz viens tiešsaistes veikals programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="5b057-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="5b057-112">Papildinformāciju skatiet [E-komercijas vietnes izveide](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="5b057-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="5b057-113">Jauna tiešsaistes kanāla izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="5b057-113">Create and configure a new online channel</span></span>

<span data-ttu-id="5b057-114">Lai izveidotu un konfigurētu jaunu tiešsaistes kanālu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5b057-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="5b057-115">Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Tiešsaistes veikali**.</span><span class="sxs-lookup"><span data-stu-id="5b057-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="5b057-116">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b057-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5b057-117">Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5b057-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="5b057-118">Nolaižamajā sarakstā **Juridiskā persona** ievadiet atbilstošo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="5b057-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="5b057-119">Nolaižamajā sarakstā **Noliktava** ievadiet atbilstošo noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5b057-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="5b057-120">Laukā **Veikala laika josla** atlasiet atbilstošo laika joslu.</span><span class="sxs-lookup"><span data-stu-id="5b057-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="5b057-121">Laukā **Valūta** atlasiet atbilstošo valūtu.</span><span class="sxs-lookup"><span data-stu-id="5b057-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="5b057-122">Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="5b057-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="5b057-123">Laukā **Debitora adrešu grāmata** norādiet derīgu adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="5b057-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="5b057-124">Laukā **Funkcionalitātes profils** atlasiet funkcionalitātes profilu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="5b057-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="5b057-125">Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.</span><span class="sxs-lookup"><span data-stu-id="5b057-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="5b057-126">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b057-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5b057-127">Tālāk redzamajā attēlā parādīta jauna tiešsaistes kanāla izveide.</span><span class="sxs-lookup"><span data-stu-id="5b057-127">The following image shows the creation of a new online channel.</span></span>

![Jauns tiešsaistes kanāls](media/channel-setup-online-1.png)

<span data-ttu-id="5b057-129">Tālāk redzamajā attēlā ir parādīts tiešsaistes kanāla piemērs.</span><span class="sxs-lookup"><span data-stu-id="5b057-129">The following image shows an example online channel.</span></span>

![Tiešsaistes kanāla piemērs](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="5b057-131">Valodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-131">Set up languages</span></span>

<span data-ttu-id="5b057-132">Ja e-Commerce vietne atbalstīs vairākas valodas, izvērsiet sadaļu **Valodas** un pievienojiet papildu valodas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="5b057-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="5b057-133">Maksājuma konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-133">Set up payment account</span></span>

<span data-ttu-id="5b057-134">Sadaļā **Maksājumu konts** varat pievienot trešās puses maksājuma nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="5b057-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="5b057-135">Papildinformāciju par Adyen maksājumu savienotāja iestatīšanu skatiet sadaļā [Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="5b057-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="5b057-136">Papildu kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-136">Additional channel setup</span></span>

<span data-ttu-id="5b057-137">Papildu uzdevumi, kas nepieciešami tiešsaistes kanāla iestatīšanai, ietver maksājuma metožu iestatīšanu un izpildes grupas piešķiršanu.</span><span class="sxs-lookup"><span data-stu-id="5b057-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="5b057-138">Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi**, **Maksāšanas metodes** un **Izpildes grupas piešķires**.</span><span class="sxs-lookup"><span data-stu-id="5b057-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Papildu tiešsaistes kanāla iestatīšanas darbības](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="5b057-140">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="5b057-140">Set up payment methods</span></span>

<span data-ttu-id="5b057-141">Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5b057-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="5b057-142">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Maksājumu metodes**.</span><span class="sxs-lookup"><span data-stu-id="5b057-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="5b057-143">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b057-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5b057-144">Navigācijas rūtī atlasiet vēlamo maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="5b057-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="5b057-145">Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="5b057-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="5b057-146">Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="5b057-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="5b057-147">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b057-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5b057-148">Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="5b057-148">The following image shows an example of a cash payment method.</span></span>

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="5b057-150">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="5b057-150">Set up modes of delivery</span></span>

<span data-ttu-id="5b057-151">Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.</span><span class="sxs-lookup"><span data-stu-id="5b057-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="5b057-152">Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="5b057-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="5b057-153">Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.</span><span class="sxs-lookup"><span data-stu-id="5b057-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="5b057-154">Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.</span><span class="sxs-lookup"><span data-stu-id="5b057-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="5b057-155">Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu.</span><span class="sxs-lookup"><span data-stu-id="5b057-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="5b057-156">Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="5b057-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="5b057-157">Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.</span><span class="sxs-lookup"><span data-stu-id="5b057-157">The following image shows an example of a mode of delivery.</span></span>

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="5b057-159">Izpildes grupas piešķires iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="5b057-160">Lai iestatītu izpildes grupas piešķiri, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5b057-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="5b057-161">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Izpilde/grupas piešķire**.</span><span class="sxs-lookup"><span data-stu-id="5b057-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="5b057-162">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5b057-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5b057-163">Nolaižamajā sarakstā **Izpildes grupa** atlasiet izpildes grupu.</span><span class="sxs-lookup"><span data-stu-id="5b057-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="5b057-164">Nolaižamajā sarakstā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5b057-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="5b057-165">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5b057-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5b057-166">Tālāk redzamajā attēlā parādīts izpildes grupas piešķires piemērs.</span><span class="sxs-lookup"><span data-stu-id="5b057-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Izpildes grupas piešķires iestatīšana](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="5b057-168">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5b057-168">Additional resources</span></span>

[<span data-ttu-id="5b057-169">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="5b057-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5b057-170">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5b057-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5b057-171">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="5b057-172">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5b057-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="5b057-173">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="5b057-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]