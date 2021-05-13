---
title: Mazumtirdzniecības kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu risinājumā Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937538"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="122b1-103">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="122b1-104">Šajā tēmā aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="122b1-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="122b1-105">Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus.</span><span class="sxs-lookup"><span data-stu-id="122b1-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="122b1-106">Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali).</span><span class="sxs-lookup"><span data-stu-id="122b1-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="122b1-107">Katram mazumtirdzniecības veikala kanālam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="122b1-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="122b1-108">Pirms varat izveidot mazumtirdzniecības veikala kanālu, jums tam ir jāiestata visi šie elementi.</span><span class="sxs-lookup"><span data-stu-id="122b1-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="122b1-109">Pirms mazumtirdzniecības kanāla izveidošanas pārliecinieties, ka esat ievērojis [kanāla priekšnosacījumus](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="122b1-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="122b1-110">Jauna mazumtirdzniecības kanāla izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="122b1-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="122b1-111">Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Veikali \> Visi veikali**.</span><span class="sxs-lookup"><span data-stu-id="122b1-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="122b1-112">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="122b1-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="122b1-113">Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="122b1-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="122b1-114">Laukā **Veikala numurs** ievadiet unikālu veikala nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="122b1-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="122b1-115">Numurs var būt burtciparu ar maksimums 10 rakstzīmēm.</span><span class="sxs-lookup"><span data-stu-id="122b1-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="122b1-116">Nolaižamajā sarakstā **Juridiskā persona** ievadiet atbilstošo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="122b1-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="122b1-117">Nolaižamajā sarakstā **Noliktava** ievadiet atbilstošo noliktavu.</span><span class="sxs-lookup"><span data-stu-id="122b1-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="122b1-118">Laukā **Veikala laika josla** atlasiet atbilstošo laika joslu.</span><span class="sxs-lookup"><span data-stu-id="122b1-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="122b1-119">Nolaižamajā sarakstā **PVN grupa** atlasiet atbilstošu veikala PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="122b1-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="122b1-120">Laukā **Valūta** atlasiet atbilstošo valūtu.</span><span class="sxs-lookup"><span data-stu-id="122b1-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="122b1-121">Laukā **Debitora adrešu grāmata** norādiet derīgu adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="122b1-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="122b1-122">Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="122b1-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="122b1-123">Laukā **Funkcionalitātes profils** atlasiet funkcionalitātes profilu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="122b1-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="122b1-124">Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.</span><span class="sxs-lookup"><span data-stu-id="122b1-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="122b1-125">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="122b1-126">Tālāk redzamajā attēlā parādīta jauna mazumtirdzniecības kanāla izveide.</span><span class="sxs-lookup"><span data-stu-id="122b1-126">The following image shows the creation of a new retail channel.</span></span>

![Jauns mazumtirdzniecības kanāls](media/channel-setup-retail-1.png)

<span data-ttu-id="122b1-128">Tālāk redzamajā attēlā ir parādīts mazumtirdzniecības kanāla piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-128">The following image shows an example retail channel.</span></span>

![Mazumtirdzniecības kanāla piemērs](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="122b1-130">Citi iestatījumi</span><span class="sxs-lookup"><span data-stu-id="122b1-130">Other settings</span></span>

<span data-ttu-id="122b1-131">Pastāv vairāki citi neobligāti iestatījumi, ko var iestatīt sadaļās **Izraksts/slēgšana** un **Dažādi** , pamatojoties uz mazumtirdzniecības veikala vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="122b1-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="122b1-132">Turklāt skatiet sadaļu [Pārdošanas punkta (POS) ekrāna izkārtojumi](pos-screen-layouts.md), lai iegūtu informāciju par noklusētā ekrāna izkārtojuma iestatīšanu sadaļā **Ekrāna izkārtojums**, un sadaļu [Retail Hardware Station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md), lai iegūtu informāciju par sadaļu **Aparatūras stacijas**.</span><span class="sxs-lookup"><span data-stu-id="122b1-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="122b1-133">Tālāk redzamajā attēlā ir parādīts mazumtirdzniecības kanāla iestatījumu konfigurācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-133">The following image shows an example retail channel setup configuration.</span></span>

![Mazumtirdzniecības kanāla konfigurācijas piemērs](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="122b1-135">Papildu kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-135">Additional channel set up</span></span>

<span data-ttu-id="122b1-136">Ir papildu vienumi, kas ir jāiestata kanālam, ko var atrast darbības rūtī sadaļā **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="122b1-137">Papildu uzdevumi, kas nepieciešami tiešsaistes kanāla iestatīšanai, ietver maksājuma metožu iestatīšanu, skaidras naudas deklarēšanu, piegādes veidus, ienākumu/izdevumu kontu, sadaļas, izpildes grupas piešķiršanu un seifus.</span><span class="sxs-lookup"><span data-stu-id="122b1-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="122b1-138">Tālāk esošajā attēlā ir parādītas dažādas papildu mazumtirdzniecības kanāla iestatīšanas opcijas cilnē **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="122b1-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanāla iestatīšana](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="122b1-140">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="122b1-140">Set up payment methods</span></span>

<span data-ttu-id="122b1-141">Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="122b1-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="122b1-142">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Maksājumu metodes**.</span><span class="sxs-lookup"><span data-stu-id="122b1-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="122b1-143">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="122b1-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="122b1-144">Navigācijas rūtī atlasiet vēlamo maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="122b1-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="122b1-145">Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="122b1-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="122b1-146">Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="122b1-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="122b1-147">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="122b1-148">Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-148">The following image shows an example of a cash payment method.</span></span>

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="122b1-150">Skaidrās naudas deklarācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-150">Set up cash declaration</span></span>

1. <span data-ttu-id="122b1-151">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Skaidras naudas deklarēšana**.</span><span class="sxs-lookup"><span data-stu-id="122b1-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="122b1-152">Darbības rūtī atlasiet **Jauns** un pēc tam izveidojiet visas **Monētu** un **Banknošu** piemērojamās denominācijas.</span><span class="sxs-lookup"><span data-stu-id="122b1-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="122b1-153">Tālāk esošajā attēlā ir parādīts skaidras naudas deklarācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-153">The following image shows an example of a cash declaration.</span></span>

![Skaidrās naudas deklarācijas iestatīšana](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="122b1-155">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="122b1-155">Set up modes of delivery</span></span>

<span data-ttu-id="122b1-156">Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas darbības rūtī.</span><span class="sxs-lookup"><span data-stu-id="122b1-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="122b1-157">Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="122b1-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="122b1-158">Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.</span><span class="sxs-lookup"><span data-stu-id="122b1-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="122b1-159">Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.</span><span class="sxs-lookup"><span data-stu-id="122b1-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="122b1-160">Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu.</span><span class="sxs-lookup"><span data-stu-id="122b1-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="122b1-161">Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="122b1-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="122b1-162">Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-162">The following image shows an example of a mode of delivery.</span></span>

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="122b1-164">Ienākumu/izdevumu konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-164">Set up income/expense account</span></span>

<span data-ttu-id="122b1-165">Lai iestatītu ienākumu/izdevumu kontu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="122b1-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="122b1-166">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **ienākumu/izdevumu konts**.</span><span class="sxs-lookup"><span data-stu-id="122b1-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="122b1-167">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="122b1-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="122b1-168">Sadaļa **nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="122b1-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="122b1-169">Sadaļā **Saīsinātais nosaukums** ievadiet saīsināto nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="122b1-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="122b1-170">Sadaļā **Konta veids** ievadiet konta veidu.</span><span class="sxs-lookup"><span data-stu-id="122b1-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="122b1-171">Ievadiet tekstu sadaļās **1. ziņojuma rinda**, **2. ziņojuma rinda**, **1. kvīts teksts** un **2. kvīts teksts**, kā tas ir nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="122b1-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="122b1-172">Sadaļā **Grāmatošana** ievadiet grāmatošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="122b1-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="122b1-173">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="122b1-174">Tālāk esošajā attēlā parādīts ieņēmumu/izdevumu konta piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-174">The following image shows an example of an income/expense account.</span></span>

![Ienākumu/izdevumu kontu iestatīšana](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="122b1-176">Sadaļu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-176">Set up sections</span></span>

<span data-ttu-id="122b1-177">Lai iestatītu sadaļas, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="122b1-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="122b1-178">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam noklikšķiniet uz **Sadaļas**.</span><span class="sxs-lookup"><span data-stu-id="122b1-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="122b1-179">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="122b1-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="122b1-180">Sadaļā **Sadaļas numurs** ievadiet sadaļas numuru.</span><span class="sxs-lookup"><span data-stu-id="122b1-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="122b1-181">Sadaļā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="122b1-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="122b1-182">Sadaļā **Sadaļas izmērs** ievadiet sadaļas izmēru.</span><span class="sxs-lookup"><span data-stu-id="122b1-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="122b1-183">Konfigurējiet papildu iestatījumus sadaļām **Vispārīgi** un **Pārdošanas statistika**, kā tas ir nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="122b1-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="122b1-184">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="122b1-185">Izpildes grupas piešķires iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="122b1-186">Lai iestatītu izpildes grupas piešķiri, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="122b1-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="122b1-187">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Izpilde/grupas piešķire**.</span><span class="sxs-lookup"><span data-stu-id="122b1-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="122b1-188">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="122b1-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="122b1-189">Nolaižamajā sarakstā **Izpildes grupa** atlasiet izpildes grupu.</span><span class="sxs-lookup"><span data-stu-id="122b1-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="122b1-190">Nolaižamajā sarakstā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="122b1-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="122b1-191">Darbību rūtī atlasiet **Saglabāt**</span><span class="sxs-lookup"><span data-stu-id="122b1-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="122b1-192">Tālāk redzamajā attēlā parādīts izpildes grupas piešķires piemērs.</span><span class="sxs-lookup"><span data-stu-id="122b1-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Izpildes grupas piešķires iestatīšana](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="122b1-194">Seifu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-194">Set up safes</span></span>

<span data-ttu-id="122b1-195">Lai iestatītu seifus, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="122b1-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="122b1-196">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam noklikšķiniet uz **Seifi**.</span><span class="sxs-lookup"><span data-stu-id="122b1-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="122b1-197">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="122b1-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="122b1-198">Ievadiet seifa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="122b1-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="122b1-199">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="122b1-200">Nodrošināt unikālus transakciju ID</span><span class="sxs-lookup"><span data-stu-id="122b1-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="122b1-201">Attiecībā uz Commerce versiju 10.0.18 pārdošanas punktam (POS) ģenerētie transakciju ID ir secīgi un ietver šādas daļas:</span><span class="sxs-lookup"><span data-stu-id="122b1-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="122b1-202">Fiksēta daļa, kas ir veikala ID un termināļa ID konkatenācija.</span><span class="sxs-lookup"><span data-stu-id="122b1-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="122b1-203">Secīga daļa, kas ir numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="122b1-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="122b1-204">It īpaši formāts ir *{store}-{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="122b1-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="122b1-205">Tā kā transakciju ID var ģenerēt bezsaistes un tiešsaistes režīmā, ir gadījumi, kad tiek ģenerēti dublēti transakciju ID.</span><span class="sxs-lookup"><span data-stu-id="122b1-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="122b1-206">Lai noņemtu transakciju ID dublikātus, ir nepieciešama manuāla datu labošana.</span><span class="sxs-lookup"><span data-stu-id="122b1-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="122b1-207">Ar Commerce versiju 10.0.19 transakciju ID formāts ir atjaunināts, lai noņemtu secīgu daļu, un tā vietā tiek izmantots 13 ciparu numurs, kas ģenerēts, aprēķinot laiku milisekundēs kopš 1970. gada.</span><span class="sxs-lookup"><span data-stu-id="122b1-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="122b1-208">Ar šo izmaiņu jaunais transakciju ID formāts ir *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="122b1-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="122b1-209">Šis atjauninājums padara transakciju ID nesecīgo un nodrošina, ka transakciju ID vienmēr ir unikāli.</span><span class="sxs-lookup"><span data-stu-id="122b1-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="122b1-210">Transakciju ID ir paredzēti tikai iekšējai sistēmai, tāpēc tiem nav jābūt secīgiem.</span><span class="sxs-lookup"><span data-stu-id="122b1-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="122b1-211">Tomēr daudzas valstis pieprasa, lai saņemšanas ID būtu secīgi.</span><span class="sxs-lookup"><span data-stu-id="122b1-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="122b1-212">Jauno transakciju ID formāta līdzekli var iespējot no darbvietas **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="122b1-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="122b1-213">Lai aktivizētu jaunu transakciju ID izmantošanu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="122b1-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="122b1-214">Programmā Commerce Headquarters dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="122b1-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="122b1-215">Filtrs modulim "mazumtirdzniecība un komercija".</span><span class="sxs-lookup"><span data-stu-id="122b1-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="122b1-216">Meklējiet līdzekļa nosaukumu **Aktivizēt jaunu transakciju ID, lai izvairītos no dublētiem transakciju ID**.</span><span class="sxs-lookup"><span data-stu-id="122b1-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="122b1-217">Atlasiet līdzekli un pēc tam labajā rūtī atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="122b1-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="122b1-218">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="122b1-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="122b1-219">Palaidiet darbus **1070 kanāla konfigurācija** un **1170 POS uzdevumu ierakstītājs**, lai sinhronizētu iespējoto līdzekli ar veikaliem.</span><span class="sxs-lookup"><span data-stu-id="122b1-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="122b1-220">Lai lietotu jauno transakciju ID formātu, kad uz veikaliem ir nosūtītas izmaiņas, POS termināļi ir jāaizver un atkārtoti jāatver.</span><span class="sxs-lookup"><span data-stu-id="122b1-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="122b1-221">Kad jaunais transakciju ID formāta līdzeklis ir aktivizēts, šo līdzekli nevarēs deaktivizēt.</span><span class="sxs-lookup"><span data-stu-id="122b1-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="122b1-222">Ja tas ir jāatspējo, lūdzu, sazinieties ar Commerce Support.</span><span class="sxs-lookup"><span data-stu-id="122b1-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="122b1-223">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="122b1-223">Additional resources</span></span>

[<span data-ttu-id="122b1-224">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="122b1-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="122b1-225">Kanāla iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="122b1-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="122b1-226">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="122b1-227">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="122b1-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
