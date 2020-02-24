---
title: Zvanu centra kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002454"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="758c9-103">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="758c9-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="758c9-104">Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="758c9-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="758c9-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="758c9-105">Overview</span></span>

<span data-ttu-id="758c9-106">Programmā Dynamics 365 Commerce zvanu centrs ir mazumtirdzniecības kanāla veids, ko var definēt lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="758c9-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="758c9-107">Lai noteiktu kanālu jūsu zvanu centra entītijām, sistēma ļauj saistīt specifiskus datus un pasūtījumu apstrādes noklusējumus pārdošanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="758c9-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="758c9-108">Uzņēmums var definēt vairākus zvanu centra kanālus programmā Commerce.</span><span class="sxs-lookup"><span data-stu-id="758c9-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="758c9-109">Pirms jauna zvanu centra kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="758c9-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="758c9-110">Jauna zvanu centra kanāla izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="758c9-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="758c9-111">Lai izveidotu un konfigurētu jaunu zvanu centra kanālu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="758c9-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="758c9-112">Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Zvanu centri \> Visi zvanu centri**.</span><span class="sxs-lookup"><span data-stu-id="758c9-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="758c9-113">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="758c9-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="758c9-114">Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="758c9-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="758c9-115">Atlasiet atbilstošo **Juridisko personu** no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="758c9-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="758c9-116">Atlasiet atbilstošo atrašanās vietu **Noliktava** no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="758c9-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="758c9-117">Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="758c9-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="758c9-118">Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.</span><span class="sxs-lookup"><span data-stu-id="758c9-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="758c9-119">Nodrošiniet informācijas kodu **Cenas ignorēšana**.</span><span class="sxs-lookup"><span data-stu-id="758c9-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="758c9-120">Ņemiet vērā, ka jums, iespējams, vispirms būs jāizveido informācijas kods.</span><span class="sxs-lookup"><span data-stu-id="758c9-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="758c9-121">Norādiet informācijas kodu **Aizturēšanas kods**.</span><span class="sxs-lookup"><span data-stu-id="758c9-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="758c9-122">Ņemiet vērā, ka jums, iespējams, vispirms būs jāizveido informācijas kods.</span><span class="sxs-lookup"><span data-stu-id="758c9-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="758c9-123">Norādiet informācijas kodu **Kredīts**.</span><span class="sxs-lookup"><span data-stu-id="758c9-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="758c9-124">Ņemiet vērā, ka jums, iespējams, vispirms būs jāizveido informācijas kods.</span><span class="sxs-lookup"><span data-stu-id="758c9-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="758c9-125">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="758c9-125">Select **Save**.</span></span>

<span data-ttu-id="758c9-126">Tālāk redzamajā attēlā parādīta jauna zvanu centra kanāla izveide.</span><span class="sxs-lookup"><span data-stu-id="758c9-126">The following image shows the creation of a new call center channel.</span></span>

![Jauns zvanu centra kanāls](media/channel-setup-callcenter-1.png)

<span data-ttu-id="758c9-128">Tālāk redzamajā attēlā ir parādīts zvanu centra kanāla piemērs.</span><span class="sxs-lookup"><span data-stu-id="758c9-128">The following image shows an example call center channel.</span></span>

![Zvanu centra kanāla piemērs](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="758c9-130">Papildu kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="758c9-130">Additional channel setup</span></span>

<span data-ttu-id="758c9-131">Papildu uzdevumi, kas nepieciešami zvanu centra kanāla iestatīšanai, ietver maksājuma metožu un piegādes režīmu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="758c9-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="758c9-132">Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi** un **Maksāšanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="758c9-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Papildu zvanu centra kanāla iestatīšanas darbības](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="758c9-134">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="758c9-134">Set up payment methods</span></span>

<span data-ttu-id="758c9-135">Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="758c9-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="758c9-136">Darbības rūtī atlasiet cilni **Iestatīšana** un pēc tam atlasiet **Maksājumu metodes**.</span><span class="sxs-lookup"><span data-stu-id="758c9-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="758c9-137">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="758c9-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="758c9-138">Navigācijas rūtī atlasiet vēlamo maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="758c9-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="758c9-139">Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="758c9-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="758c9-140">Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="758c9-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="758c9-141">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="758c9-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="758c9-142">Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="758c9-142">The following image shows an example of a cash payment method.</span></span>

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="758c9-144">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="758c9-144">Set up modes of delivery</span></span>

<span data-ttu-id="758c9-145">Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.</span><span class="sxs-lookup"><span data-stu-id="758c9-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="758c9-146">Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="758c9-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="758c9-147">Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.</span><span class="sxs-lookup"><span data-stu-id="758c9-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="758c9-148">Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.</span><span class="sxs-lookup"><span data-stu-id="758c9-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="758c9-149">Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu.</span><span class="sxs-lookup"><span data-stu-id="758c9-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="758c9-150">Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="758c9-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="758c9-151">Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.</span><span class="sxs-lookup"><span data-stu-id="758c9-151">The following image shows an example of a mode of delivery.</span></span>

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="758c9-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="758c9-153">Additional resources</span></span>

[<span data-ttu-id="758c9-154">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="758c9-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="758c9-155">Zvanu centra pārdošanas funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="758c9-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="758c9-156">Iestatīt zvanu centra pasūtījumu apstrādes opcijas</span><span class="sxs-lookup"><span data-stu-id="758c9-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="758c9-157">Zvanu centra katalogi</span><span class="sxs-lookup"><span data-stu-id="758c9-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="758c9-158">Pārkāpumu brīdinājumu iestatīšana un darbs ar tiem</span><span class="sxs-lookup"><span data-stu-id="758c9-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="758c9-159">Nepārtrauktības programmu iestatīšana zvanu centriem</span><span class="sxs-lookup"><span data-stu-id="758c9-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
