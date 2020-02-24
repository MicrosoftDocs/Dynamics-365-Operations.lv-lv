---
title: Tiešsaistes veikala iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu tiešsaistes kanālu programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002431"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="d4baa-103">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d4baa-104">Šajā tēmā aprakstīts, kā izveidot jaunu tiešsaistes kanālu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4baa-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d4baa-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d4baa-105">Overview</span></span>

<span data-ttu-id="d4baa-106">Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus.</span><span class="sxs-lookup"><span data-stu-id="d4baa-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="d4baa-107">Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali).</span><span class="sxs-lookup"><span data-stu-id="d4baa-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="d4baa-108">Tiešsaistes veikali dod klientiem iespēju papildus mazumtirdzniecības veikaliem iegādāties produktus arī no mazumtirgotāja tiešsaistes veikala.</span><span class="sxs-lookup"><span data-stu-id="d4baa-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="d4baa-109">Lai izveidotu tiešsaistes veikalu pakalpojumā Commerce, vispirms ir jāizveido tiešsaistes kanāls.</span><span class="sxs-lookup"><span data-stu-id="d4baa-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="d4baa-110">Pirms jauna tiešsaistes kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d4baa-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="d4baa-111">Jauna tiešsaistes kanāla izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d4baa-111">Create and configure a new online channel</span></span>

<span data-ttu-id="d4baa-112">Lai izveidotu un konfigurētu jaunu tiešsaistes kanālu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4baa-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="d4baa-113">Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Tiešsaistes veikali**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="d4baa-114">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d4baa-115">Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d4baa-116">Nolaižamajā sarakstā **Juridiskā persona** ievadiet atbilstošo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="d4baa-117">Nolaižamajā sarakstā **Noliktava** ievadiet atbilstošo noliktavu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="d4baa-118">Laukā **Veikala laika josla** atlasiet atbilstošo laika joslu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="d4baa-119">Laukā **Valūta** atlasiet atbilstošo valūtu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="d4baa-120">Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="d4baa-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="d4baa-121">Laukā **Debitora adrešu grāmata** norādiet derīgu adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="d4baa-122">Laukā **Funkcionalitātes profils** atlasiet funkcionalitātes profilu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="d4baa-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="d4baa-123">Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="d4baa-124">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d4baa-125">Tālāk redzamajā attēlā parādīta jauna tiešsaistes kanāla izveide.</span><span class="sxs-lookup"><span data-stu-id="d4baa-125">The following image shows the creation of a new online channel.</span></span>

![Jauns tiešsaistes kanāls](media/channel-setup-online-1.png)

<span data-ttu-id="d4baa-127">Tālāk redzamajā attēlā ir parādīts tiešsaistes kanāla piemērs.</span><span class="sxs-lookup"><span data-stu-id="d4baa-127">The following image shows an example online channel.</span></span>

![Tiešsaistes kanāla piemērs](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="d4baa-129">Valodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-129">Set up languages</span></span>

<span data-ttu-id="d4baa-130">Ja e-Commerce vietne atbalstīs vairākas valodas, izvērsiet sadaļu **Valodas** un pievienojiet papildu valodas pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="d4baa-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="d4baa-131">Maksājuma konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-131">Set up payment account</span></span>

<span data-ttu-id="d4baa-132">Sadaļā **Maksājumu konts** varat pievienot trešās puses maksājuma nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="d4baa-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="d4baa-133">Lai iegūtu informāciju par Adyen maksājumu savienotāja iestatīšanu, skatiet sadaļu [Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="d4baa-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="d4baa-134">Papildu kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-134">Additional channel set up</span></span>

<span data-ttu-id="d4baa-135">Papildu uzdevumi, kas nepieciešami tiešsaistes kanāla iestatīšanai, ietver maksājuma metožu iestatīšanu un izpildes grupas piešķiršanu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="d4baa-136">Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi**, **Maksāšanas metodes** un **Izpildes grupas piešķires**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Papildu tiešsaistes kanāla iestatīšanas darbības](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d4baa-138">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="d4baa-138">Set up payment methods</span></span>

<span data-ttu-id="d4baa-139">Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4baa-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="d4baa-140">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Maksājumu metodes**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="d4baa-141">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d4baa-142">Navigācijas rūtī atlasiet vēlamo maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="d4baa-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="d4baa-143">Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="d4baa-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="d4baa-144">Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="d4baa-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="d4baa-145">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d4baa-146">Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="d4baa-146">The following image shows an example of a cash payment method.</span></span>

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d4baa-148">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="d4baa-148">Set up modes of delivery</span></span>

<span data-ttu-id="d4baa-149">Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d4baa-150">Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="d4baa-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="d4baa-151">Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="d4baa-152">Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d4baa-153">Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="d4baa-154">Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="d4baa-155">Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.</span><span class="sxs-lookup"><span data-stu-id="d4baa-155">The following image shows an example of a mode of delivery.</span></span>

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="d4baa-157">Izpildes grupas piešķires iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="d4baa-158">Lai iestatītu izpildes grupas piešķiri, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4baa-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="d4baa-159">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Izpilde/grupas piešķire**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="d4baa-160">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d4baa-161">Nolaižamajā sarakstā **Izpildes grupa** atlasiet izpildes grupu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="d4baa-162">Nolaižamajā sarakstā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="d4baa-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="d4baa-163">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4baa-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d4baa-164">Tālāk redzamajā attēlā parādīts izpildes grupas piešķires piemērs.</span><span class="sxs-lookup"><span data-stu-id="d4baa-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Izpildes grupas piešķires iestatīšana](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="d4baa-166">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d4baa-166">Additional resources</span></span>

[<span data-ttu-id="d4baa-167">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="d4baa-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d4baa-168">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="d4baa-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d4baa-169">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="d4baa-170">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d4baa-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="d4baa-171">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="d4baa-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
