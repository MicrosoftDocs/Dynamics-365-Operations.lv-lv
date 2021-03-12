---
title: Zvanu centra kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: b25626dafc07d576699ceba3cc9ca691db45cb9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997754"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="54de5-103">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="54de5-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="54de5-104">Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="54de5-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="54de5-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="54de5-105">Overview</span></span>


<span data-ttu-id="54de5-106">Programmā Dynamics 365 Commerce zvanu centrs ir Commerce kanāls, ko var definēt programmā.</span><span class="sxs-lookup"><span data-stu-id="54de5-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="54de5-107">Lai noteiktu kanālu jūsu zvanu centra entītijām, sistēma ļauj saistīt specifiskus datus un pasūtījumu apstrādes noklusējumus pārdošanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="54de5-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="54de5-108">Lai gan uzņēmums var pakalpojumā Commerce noteikt vairākus zvanu centra kanālus, ir svarīgi atzīmēt, ka atsevišķu lietotāju var saistīt tikai ar vienu zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="54de5-109">Pirms jauna zvanu centra kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="54de5-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="54de5-110">Jauna zvanu centra kanāla izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="54de5-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="54de5-111">Lai izveidotu un konfigurētu jaunu zvanu centra kanālu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="54de5-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="54de5-112">Navigācijas panelī dodieties uz **Retail un Commerce \> Kanāli \> Zvanu centri \> Visi zvanu centri**.</span><span class="sxs-lookup"><span data-stu-id="54de5-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="54de5-113">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54de5-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="54de5-114">Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="54de5-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="54de5-115">Atlasiet atbilstošo **Juridisko personu** no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="54de5-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="54de5-116">Atlasiet atbilstošo atrašanās vietu **Noliktava** no nolaižamā saraksta.</span><span class="sxs-lookup"><span data-stu-id="54de5-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="54de5-117">Šī atrašanās vieta tiks izmantota kā noklusējuma vērtība pārdošanas pasūtījumiem, kas izveidoti šim zvanu centra kanālam, ja vien klienta vai krājuma līmenī nav definēti citi noklusējumi.</span><span class="sxs-lookup"><span data-stu-id="54de5-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="54de5-118">Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="54de5-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="54de5-119">Šie dati tiek izmantoti, lai palīdzētu automātiskās aizpildīšanas noklusējumos, kad tiek veidoti jauni klientu ieraksti.</span><span class="sxs-lookup"><span data-stu-id="54de5-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="54de5-120">Veidojot zvanu centra pasūtījumus, nav ieteicams izveidot pasūtījumus noklusējuma klientam.</span><span class="sxs-lookup"><span data-stu-id="54de5-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="54de5-121">Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.</span><span class="sxs-lookup"><span data-stu-id="54de5-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="54de5-122">Kad zvanu centra pasūtījumi ir izveidoti un apstrādāti, tiek izmantots e-pasta paziņojumu profils, lai aktivizētu automatizētos e-pasta brīdinājumus klientiem ar informāciju par viņu pasūtījuma statusu.</span><span class="sxs-lookup"><span data-stu-id="54de5-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="54de5-123">Nodrošiniet informācijas kodu **Cenas ignorēšana**.</span><span class="sxs-lookup"><span data-stu-id="54de5-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="54de5-124">Jums, iespējams, vispirms būs jāizveido informācijas kods.</span><span class="sxs-lookup"><span data-stu-id="54de5-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="54de5-125">Šis informācijas kods sniedz pamatojuma kodu kopu, no kuras lietotājam piedāvās izvēlēties, izmantojot cenu ignorēšanas funkcionalitāti zvanu centra pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="54de5-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="54de5-126">Norādiet informācijas kodu **Aizturēšanas kods**.</span><span class="sxs-lookup"><span data-stu-id="54de5-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="54de5-127">Jums, iespējams, vispirms būs jāizveido informācijas kods.</span><span class="sxs-lookup"><span data-stu-id="54de5-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="54de5-128">Šis informācijas kods sniedz neobligātu pamatojuma kodu kopu, no kuras lietotājam piedāvās izvēlēties, veicot aizturētu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54de5-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="54de5-129">Norādiet informācijas kodu **Kredīts**.</span><span class="sxs-lookup"><span data-stu-id="54de5-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="54de5-130">Jums, iespējams, vispirms būs jāizveido informācijas kods.</span><span class="sxs-lookup"><span data-stu-id="54de5-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="54de5-131">Šis informācijas kods sniedz pamatojuma kodu kopu, ko lietotājs var izvēlēties, izmantojot pasūtījuma kredīta funkcionalitāti zvanu centrā, lai sniegtu klientam dažās veida atmaksas klientu apkalpošanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="54de5-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="54de5-132">Neobligāti: Kopsavilkuma cilnē **Finanšu dimensijas** iestatiet finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="54de5-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="54de5-133">Šeit ievadītās dimensijas pēc noklusējuma tiek rādītas šajā zvanu centra kanālā izveidotajā pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="54de5-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="54de5-134">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54de5-134">Click **Save**.</span></span>

<span data-ttu-id="54de5-135">Tālāk redzamajā attēlā parādīta jauna zvanu centra kanāla izveide.</span><span class="sxs-lookup"><span data-stu-id="54de5-135">The following image shows the creation of a new call center channel.</span></span>

![Jauns zvanu centra kanāls](media/channel-setup-callcenter-1.png)

<span data-ttu-id="54de5-137">Tālāk redzamajā attēlā ir parādīts zvanu centra kanāla piemērs.</span><span class="sxs-lookup"><span data-stu-id="54de5-137">The following image shows an example call center channel.</span></span>

![Zvanu centra kanāla piemērs](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="54de5-139">Papildu kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="54de5-139">Additional channel setup</span></span>

<span data-ttu-id="54de5-140">Papildu uzdevumi, kas nepieciešami zvanu centra kanāla iestatīšanai, ietver maksājuma metožu un piegādes režīmu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="54de5-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="54de5-141">Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi** un **Maksāšanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="54de5-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Papildu zvanu centra kanāla iestatīšanas darbības](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="54de5-143">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="54de5-143">Set up payment methods</span></span>

<span data-ttu-id="54de5-144">Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="54de5-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="54de5-145">Lietotājiem būs jāizvēlas no iepriekš definētajām maksājumu metodēm, lai piesaistītu tās zvanu centra kanālam.</span><span class="sxs-lookup"><span data-stu-id="54de5-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="54de5-146">Pirms izveidojat zvanu centra maksājuma metodes, vispirms iestatiet savas galvenās maksājuma metodes sadaļā **Retail un Commerce \> Kanāla iestatīšana \> Maksājuma metodes \> Maksājuma metodēs**.</span><span class="sxs-lookup"><span data-stu-id="54de5-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="54de5-147">Darbības rūtī atlasiet cilni **Iestatīšana** un pēc tam atlasiet **Maksājumu metodes**.</span><span class="sxs-lookup"><span data-stu-id="54de5-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="54de5-148">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54de5-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="54de5-149">Navigācijas rūtī atlasiet maksājuma metodi no pieejamajiem iepriekš definētajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="54de5-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="54de5-150">Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="54de5-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="54de5-151">Kredītkartēm, dāvanu kartēm vai lojalitātes programmas kartēm ir nepieciešams papildu iestatījums, atlasot funkciju **Kartes iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="54de5-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="54de5-152">Konfigurējiet pareizus maksājuma tipa grāmatošanas kontus sadaļā **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="54de5-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="54de5-153">Darbību rūtī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54de5-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="54de5-154">Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="54de5-154">The following image shows an example of a cash payment method.</span></span>

![Maksājumu metožu piemērs](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="54de5-156">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="54de5-156">Set up modes of delivery</span></span>

<span data-ttu-id="54de5-157">Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.</span><span class="sxs-lookup"><span data-stu-id="54de5-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="54de5-158">Lai mainītu vai pievienotu piegādes veidu, kas ir jāsaista ar zvanu centra kanālu, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="54de5-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="54de5-159">Veidlapā Zvanu centra piegādes veidi atlasiet **Pārvaldīt piegādes veidus**</span><span class="sxs-lookup"><span data-stu-id="54de5-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="54de5-160">Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.</span><span class="sxs-lookup"><span data-stu-id="54de5-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="54de5-161">Sadaļā **Mazumtirdzniecības kanāli** noklikšķiniet uz **Pievienot rindu**, lai pievienotu zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="54de5-162">Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="54de5-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="54de5-163">Pārliecinieties, ka piegādes veids ir konfigurēts ar datiem kopsavilkuma cilnē **Preces** un kopsavilkuma cilnē **Adreses**.</span><span class="sxs-lookup"><span data-stu-id="54de5-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="54de5-164">Ja preces vai piegādes adreses nav derīgas piegādes veidam, izvēloties tās pasūtījuma izveides laikā, radīsies kļūdas.</span><span class="sxs-lookup"><span data-stu-id="54de5-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="54de5-165">Pēc tam, kad ir veiktas visas izmaiņas zvanu centra piegādes veida konfigurācijās, ir jāpalaiž darbs **Piegādes veidu apstrāde**, lai izvērstu izmaiņu matricu.</span><span class="sxs-lookup"><span data-stu-id="54de5-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="54de5-166">Šo darbu var atrast, pārvietojoties uz sadaļu **Retail un Commerce \> Retail un Commerce IT \> Apstrādāt piegādes veidus**.</span><span class="sxs-lookup"><span data-stu-id="54de5-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="54de5-167">Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.</span><span class="sxs-lookup"><span data-stu-id="54de5-167">The following image shows an example of a mode of delivery.</span></span>

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="54de5-169">Kanāla lietotāju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="54de5-169">Set up channel users</span></span>

<span data-ttu-id="54de5-170">Lai izveidotu pārdošanas pasūtījumu, kas ir saistīts ar zvanu centra kanālu no Commerce Headquarters, lietotājam, kas veido pārdošanas pasūtījumu, ir jābūt saistītam ar zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="54de5-171">Lietotājs nevar manuāli saistīt pārdošanas pasūtījumu, kas izveidots Commerce Headquarters, ar zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="54de5-172">Saite ir sistemātiska, un tā ir balstīta uz lietotāju un lietotāja attiecībām ar zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="54de5-173">Lietotājs var būt saistīts tikai ar vienu zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="54de5-174">Darbības rūtī atlasiet cilni **Kanāls**, pēc tam atlasiet **Kanāla lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="54de5-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="54de5-175">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54de5-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="54de5-176">Nolaižamajā atlases sarakstā izvēlieties esošu **Lietotāja ID**, lai saistītu šo lietotāju ar zvanu centra kanālu</span><span class="sxs-lookup"><span data-stu-id="54de5-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="54de5-177">Pēc kanāla lietotāja iestatīšanas un jauna pārdošanas pasūtījuma izveides programmā Commerce Headquarters, pārdošanas pasūtījumu saistīs ar saistīto zvanu centra kanālu.</span><span class="sxs-lookup"><span data-stu-id="54de5-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="54de5-178">Visas konfigurācijas šim kanālam tiks sistemātiski piemērotas pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="54de5-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="54de5-179">Lietotājs var apstiprināt, kurš zvanu centra kanāls ir saistīts ar pārdošanas pasūtījumu, skatot kanāla nosaukuma atsauci pārdošanas pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="54de5-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="54de5-180">Cenu grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="54de5-180">Set up price groups</span></span>

<span data-ttu-id="54de5-181">Cenu grupas ir obligātas, bet, ja tās tiek izmantotas, tās var kontrolēt, kuras pārdošanas cenas tiks piedāvātas klientiem, kuri veic pasūtījumus zvanu centra kanālā.</span><span class="sxs-lookup"><span data-stu-id="54de5-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="54de5-182">Ja klientam nav konfigurēta cenu grupa vai ja kataloga cenu grupas netiek piemērotas pārdošanas pasūtījumam (izmantojot lauku **Avota koda ID** zvanu centra pasūtījuma galvenē), tad krājuma cenu atrašanai tiek izmantot kanāla cenu grupa.</span><span class="sxs-lookup"><span data-stu-id="54de5-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="54de5-183">Ja zvanu centra kanālā nav atrasta cenu grupa, tiek izmantotas noklusētās krājuma pamata cenas.</span><span class="sxs-lookup"><span data-stu-id="54de5-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="54de5-184">Lai iestatītu cenu grupu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="54de5-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="54de5-185">Darbības rūtī noklikšķiniet uz cilnes **Kanāls**, pēc tam atlasiet **Cenu grupas**.</span><span class="sxs-lookup"><span data-stu-id="54de5-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="54de5-186">Darbību rūtī noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54de5-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="54de5-187">Nolaižamajā atlases sarakstā atlasiet **Mazumtirdzniecības cenu grupa**.</span><span class="sxs-lookup"><span data-stu-id="54de5-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54de5-188">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="54de5-188">Additional resources</span></span>

[<span data-ttu-id="54de5-189">Kanāla iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="54de5-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="54de5-190">Zvanu centra pārdošanas funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="54de5-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="54de5-191">Iestatīt zvanu centra pasūtījumu apstrādes opcijas</span><span class="sxs-lookup"><span data-stu-id="54de5-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="54de5-192">Zvanu centra katalogi</span><span class="sxs-lookup"><span data-stu-id="54de5-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="54de5-193">Pārkāpumu brīdinājumu iestatīšana un darbs ar tiem</span><span class="sxs-lookup"><span data-stu-id="54de5-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="54de5-194">Nepārtrauktības programmu iestatīšana zvanu centriem</span><span class="sxs-lookup"><span data-stu-id="54de5-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
