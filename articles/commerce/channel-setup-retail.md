---
title: Mazumtirdzniecības kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113832"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="5d154-103">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5d154-104">Šajā tēmā aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5d154-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5d154-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="5d154-105">Overview</span></span>

<span data-ttu-id="5d154-106">Dynamics 365 Commerce atbalsta vairākus mazumtirdzniecības kanālus.</span><span class="sxs-lookup"><span data-stu-id="5d154-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="5d154-107">Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali).</span><span class="sxs-lookup"><span data-stu-id="5d154-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="5d154-108">Katram mazumtirdzniecības veikala kanālam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls.</span><span class="sxs-lookup"><span data-stu-id="5d154-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5d154-109">Pirms varat izveidot mazumtirdzniecības veikala kanālu, jums tam ir jāiestata visi šie elementi.</span><span class="sxs-lookup"><span data-stu-id="5d154-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="5d154-110">Pirms mazumtirdzniecības kanāla izveidošanas pārliecinieties, ka esat ievērojis [kanāla priekšnosacījumus ](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5d154-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="5d154-111">Jauna mazumtirdzniecības kanāla izveide un konfigurācija</span><span class="sxs-lookup"><span data-stu-id="5d154-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="5d154-112">Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Veikali \> Visi veikali**.</span><span class="sxs-lookup"><span data-stu-id="5d154-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5d154-113">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d154-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d154-114">Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5d154-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="5d154-115">Laukā **Veikala numurs** ievadiet unikālu veikala nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5d154-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="5d154-116">Numurs var būt burtciparu ar maksimums 10 rakstzīmēm.</span><span class="sxs-lookup"><span data-stu-id="5d154-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="5d154-117">Nolaižamajā sarakstā **Juridiskā persona** ievadiet atbilstošo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="5d154-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="5d154-118">Nolaižamajā sarakstā **Noliktava** ievadiet atbilstošo noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5d154-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="5d154-119">Laukā **Veikala laika josla** atlasiet atbilstošo laika joslu.</span><span class="sxs-lookup"><span data-stu-id="5d154-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="5d154-120">Nolaižamajā sarakstā **PVN grupa** atlasiet atbilstošu veikala PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="5d154-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="5d154-121">Laukā **Valūta** atlasiet atbilstošo valūtu.</span><span class="sxs-lookup"><span data-stu-id="5d154-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="5d154-122">Laukā **Debitora adrešu grāmata** norādiet derīgu adrešu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="5d154-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="5d154-123">Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="5d154-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="5d154-124">Laukā **Funkcionalitātes profils** atlasiet funkcionalitātes profilu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="5d154-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="5d154-125">Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.</span><span class="sxs-lookup"><span data-stu-id="5d154-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="5d154-126">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5d154-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5d154-127">Tālāk redzamajā attēlā parādīta jauna mazumtirdzniecības kanāla izveide.</span><span class="sxs-lookup"><span data-stu-id="5d154-127">The following image shows the creation of a new retail channel.</span></span>

![Jauns mazumtirdzniecības kanāls](media/channel-setup-retail-1.png)

<span data-ttu-id="5d154-129">Tālāk redzamajā attēlā ir parādīts mazumtirdzniecības kanāla piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-129">The following image shows an example retail channel.</span></span>

![Mazumtirdzniecības kanāla piemērs](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="5d154-131">Citi iestatījumi</span><span class="sxs-lookup"><span data-stu-id="5d154-131">Other settings</span></span>

<span data-ttu-id="5d154-132">Pastāv vairāki citi neobligāti iestatījumi, ko var iestatīt sadaļās **Izraksts/slēgšana** un **Dažādi** , pamatojoties uz mazumtirdzniecības veikala vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="5d154-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="5d154-133">Turklāt skatiet sadaļu [Pārdošanas punkta (POS) ekrāna izkārtojumi](pos-screen-layouts.md), lai iegūtu informāciju par noklusētā ekrāna izkārtojuma iestatīšanu sadaļā **Ekrāna izkārtojums**, un sadaļu [Retail Hardware Station konfigurēšana un instalēšana](retail-hardware-station-configuration-installation.md), lai iegūtu informāciju par sadaļu **Aparatūras stacijas**.</span><span class="sxs-lookup"><span data-stu-id="5d154-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="5d154-134">Tālāk redzamajā attēlā ir parādīts mazumtirdzniecības kanāla iestatījumu konfigurācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-134">The following image shows an example retail channel setup configuration.</span></span>

![Mazumtirdzniecības kanāla konfigurācijas piemērs](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="5d154-136">Papildu kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-136">Additional channel set up</span></span>

<span data-ttu-id="5d154-137">Ir papildu vienumi, kas ir jāiestata kanālam, ko var atrast **Darbības rūtī** sadaļā **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="5d154-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="5d154-138">Papildu uzdevumi, kas nepieciešami tiešsaistes kanāla iestatīšanai, ietver maksājuma metožu iestatīšanu, skaidras naudas deklarēšanu, piegādes veidus, ienākumu/izdevumu kontu, sadaļas, izpildes grupas piešķiršanu un seifus.</span><span class="sxs-lookup"><span data-stu-id="5d154-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="5d154-139">Tālāk esošajā attēlā ir parādītas dažādas papildu mazumtirdzniecības kanāla iestatīšanas opcijas cilnē **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="5d154-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanāla iestatīšana](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="5d154-141">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="5d154-141">Set up payment methods</span></span>

<span data-ttu-id="5d154-142">Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5d154-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="5d154-143">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Maksājumu metodes**.</span><span class="sxs-lookup"><span data-stu-id="5d154-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="5d154-144">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d154-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d154-145">Navigācijas rūtī atlasiet vēlamo maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="5d154-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="5d154-146">Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="5d154-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="5d154-147">Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.</span><span class="sxs-lookup"><span data-stu-id="5d154-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="5d154-148">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5d154-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5d154-149">Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-149">The following image shows an example of a cash payment method.</span></span>

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="5d154-151">Skaidrās naudas deklarācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-151">Set up cash declaration</span></span>

1. <span data-ttu-id="5d154-152">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Skaidras naudas deklarēšana**.</span><span class="sxs-lookup"><span data-stu-id="5d154-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="5d154-153">Darbības rūtī atlasiet **Jauns** un pēc tam izveidojiet visas **Monētu** un **Banknošu** piemērojamās denominācijas.</span><span class="sxs-lookup"><span data-stu-id="5d154-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="5d154-154">Tālāk esošajā attēlā ir parādīts skaidras naudas deklarācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-154">The following image shows an example of a cash declaration.</span></span>

![Skaidrās naudas deklarācijas iestatīšana](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="5d154-156">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="5d154-156">Set up modes of delivery</span></span>

<span data-ttu-id="5d154-157">Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.</span><span class="sxs-lookup"><span data-stu-id="5d154-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="5d154-158">Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="5d154-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="5d154-159">Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.</span><span class="sxs-lookup"><span data-stu-id="5d154-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="5d154-160">Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.</span><span class="sxs-lookup"><span data-stu-id="5d154-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="5d154-161">Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu.</span><span class="sxs-lookup"><span data-stu-id="5d154-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="5d154-162">Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.</span><span class="sxs-lookup"><span data-stu-id="5d154-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="5d154-163">Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-163">The following image shows an example of a mode of delivery.</span></span>

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="5d154-165">Ienākumu/izdevumu konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-165">Set up income/expense account</span></span>

<span data-ttu-id="5d154-166">Lai iestatītu ienākumu/izdevumu kontu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5d154-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="5d154-167">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **ienākumu/izdevumu konts**.</span><span class="sxs-lookup"><span data-stu-id="5d154-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="5d154-168">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d154-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d154-169">Sadaļa **nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5d154-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="5d154-170">Sadaļā **Saīsinātais nosaukums** ievadiet saīsināto nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5d154-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="5d154-171">Sadaļā **Konta veids** ievadiet konta veidu.</span><span class="sxs-lookup"><span data-stu-id="5d154-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="5d154-172">Ievadiet tekstu sadaļās **1. ziņojuma rinda**, **2. ziņojuma rinda**, **1. kvīts teksts** un **2. kvīts teksts**, kā tas ir nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="5d154-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="5d154-173">Sadaļā **Grāmatošana** ievadiet grāmatošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="5d154-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="5d154-174">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5d154-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5d154-175">Tālāk esošajā attēlā parādīts ieņēmumu/izdevumu konta piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-175">The following image shows an example of an income/expense account.</span></span>

![Ienākumu/izdevumu kontu iestatīšana](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="5d154-177">Sadaļu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-177">Set up sections</span></span>

<span data-ttu-id="5d154-178">Lai iestatītu sadaļas, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="5d154-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="5d154-179">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam noklikšķiniet uz **Sadaļas**.</span><span class="sxs-lookup"><span data-stu-id="5d154-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="5d154-180">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d154-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d154-181">Sadaļā **Sadaļas numurs** ievadiet sadaļas numuru.</span><span class="sxs-lookup"><span data-stu-id="5d154-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="5d154-182">Sadaļā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5d154-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="5d154-183">Sadaļā **Sadaļas izmērs** ievadiet sadaļas izmēru.</span><span class="sxs-lookup"><span data-stu-id="5d154-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="5d154-184">Konfigurējiet papildu iestatījumus sadaļām **Vispārīgi** un **Pārdošanas statistika**, kā tas ir nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="5d154-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="5d154-185">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5d154-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="5d154-186">Izpildes grupas piešķires iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="5d154-187">Lai iestatītu izpildes grupas piešķiri, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5d154-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="5d154-188">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam atlasiet **Izpilde/grupas piešķire**.</span><span class="sxs-lookup"><span data-stu-id="5d154-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="5d154-189">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d154-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d154-190">Nolaižamajā sarakstā **Izpildes grupa** atlasiet izpildes grupu.</span><span class="sxs-lookup"><span data-stu-id="5d154-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="5d154-191">Nolaižamajā sarakstā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5d154-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="5d154-192">Darbību rūtī atlasiet **Saglabāt**</span><span class="sxs-lookup"><span data-stu-id="5d154-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="5d154-193">Tālāk redzamajā attēlā parādīts izpildes grupas piešķires piemērs.</span><span class="sxs-lookup"><span data-stu-id="5d154-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Izpildes grupas piešķires iestatīšana](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="5d154-195">Seifu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-195">Set up safes</span></span>

<span data-ttu-id="5d154-196">Lai iestatītu seifus, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="5d154-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="5d154-197">Darbības rūtī atlasiet cilni **Iestatīšana**, pēc tam noklikšķiniet uz **Seifi**.</span><span class="sxs-lookup"><span data-stu-id="5d154-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="5d154-198">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d154-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5d154-199">Ievadiet seifa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5d154-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="5d154-200">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5d154-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d154-201">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5d154-201">Additional resources</span></span>

[<span data-ttu-id="5d154-202">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="5d154-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5d154-203">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5d154-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5d154-204">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="5d154-205">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d154-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

