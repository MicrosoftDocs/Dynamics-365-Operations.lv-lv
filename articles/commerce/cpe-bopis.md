---
title: BOPIS konfigurācija Dynamics 365 Commerce novērtējuma vidē
description: Šajā tēmā skaidrots, kā konfigurēt iespēju Pirkt tiešsaistē, saņemt veikalā (BOPIS) Microsoft Dynamics 365 Commerce novērtējuma vidē pēc tās nodrošināšanas.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599800"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="71732-103">BOPIS konfigurācija Dynamics 365 Commerce novērtējuma vidē</span><span class="sxs-lookup"><span data-stu-id="71732-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71732-104">Šajā tēmā skaidrots, kā konfigurēt iespēju Pirkt tiešsaistē, saņemt veikalā (BOPIS) Microsoft Dynamics 365 Commerce novērtējuma vidē pēc vides nodrošināšanas.</span><span class="sxs-lookup"><span data-stu-id="71732-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="71732-105">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="71732-105">Prerequisite</span></span>

<span data-ttu-id="71732-106">Šajā tēmā minētās procedūras veiciet tikai pēc tam, kad ir nodrošināta un konfigurēta Commerce novērtējuma vide.</span><span class="sxs-lookup"><span data-stu-id="71732-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="71732-107">Informāciju par to, kā nodrošināt un konfigurēt jūsu vidi, skatiet [Nodrošināt Dynamics 365 Commerce novērtējuma vidi](provisioning-guide.md) un [Konfigurēt Dynamics 365 Commerce novērtējuma vidi](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="71732-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="71732-108">Pēc tam, kad jūsu Komercijas vide ir nodrošināta un konfigurēta, varat izmantot šo tēmu, lai iespējotu BOPIS scenārijus.</span><span class="sxs-lookup"><span data-stu-id="71732-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="71732-109">POS konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="71732-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="71732-110">Modern POS konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="71732-110">Configure Modern POS</span></span>

<span data-ttu-id="71732-111">BOPIS scenārijiem, kas ietver kredītkartes maksājumu, ir nepieciešama aparatūras stacija.</span><span class="sxs-lookup"><span data-stu-id="71732-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="71732-112">Aparatūras stacija ir iebūvēta Modern POS operētājsistēmas Windows un Android klientiem.</span><span class="sxs-lookup"><span data-stu-id="71732-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="71732-113">Ja izmantojat mākoni POS vai Modern POS sistēmai iOS, pārdošanas punkts (POS) klientam ir jāsavieno pārī ar koplietojamo aparatūras staciju.</span><span class="sxs-lookup"><span data-stu-id="71732-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="71732-114">Šajā tēmā skaidrots, kā konfigurēt BOPIS sistēmas Windows un Android klientiem.</span><span class="sxs-lookup"><span data-stu-id="71732-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="71732-115">Papildinformāciju par to, kā uzstādīt koplietojamo aparatūras staciju, skatiet [Retail aparatūras stacijas konfigurēšana un instalēšana](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="71732-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="71732-116">Dodieties uz **Mazumtirdzniecība un Komercija \> Kanāla iestatīšana \> POS iestatīšana \> Reģistri**.</span><span class="sxs-lookup"><span data-stu-id="71732-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="71732-117">Atlasiet reģistru **SANFRAN-5** un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="71732-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="71732-118">Mainiet **Aparatūras profila** lauka vērtību no **HW002** uz **HW001** un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="71732-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="71732-119">Lai sinhronizētu izmaiņās, dodieties uz **Mazumtirdzniecība un Komercija \> Mazumtirdzniecības un Komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="71732-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="71732-120">Atlasiet sadales grafiku **1090** un pēc tam Darbību rūtī atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="71732-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="71732-121">Atlasiet **Jā** un pēc tam **Labi**, lai uzsāktu datu sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="71732-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="71732-122">Instalēt Modern POS</span><span class="sxs-lookup"><span data-stu-id="71732-122">Install Modern POS</span></span>

1. <span data-ttu-id="71732-123">Dodieties uz **Mazumtirdzniecība un Komercija \> Kanāla iestatīšana \> POS iestatīšana \> Ierīces**.</span><span class="sxs-lookup"><span data-stu-id="71732-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="71732-124">Atlasiet ierīci **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="71732-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="71732-125">Darbību rūtī atlasiet **Lejupielādēt** un pēc tam atlasiet **Konfigurācijas fails**.</span><span class="sxs-lookup"><span data-stu-id="71732-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="71732-126">Atlasiet **Lejupielādēt** un pēc tam atlasiet **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="71732-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="71732-127">Kad **ModernPOSSetup.exe** faila lejupielāde ir pabeigta, atlasiet **Atvērt failu**.</span><span class="sxs-lookup"><span data-stu-id="71732-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Atvērt failu](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="71732-129">Atlasiet **Tālāk**, lai varētu iziet caur instalēšanas procesam.</span><span class="sxs-lookup"><span data-stu-id="71732-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="71732-130">Kad instalēšana ir pabeigta, atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="71732-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="71732-131">Aktivizēt Modern POS</span><span class="sxs-lookup"><span data-stu-id="71732-131">Activate Modern POS</span></span>

1. <span data-ttu-id="71732-132">Windows darbvirsmā atlasiet pogu **Sākums** un ievadiet **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="71732-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="71732-133">Atlasiet **Retail Modern POS**programmu, lai iniciētu aktivizāciju.</span><span class="sxs-lookup"><span data-stu-id="71732-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="71732-134">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="71732-134">Select **Next**.</span></span> <span data-ttu-id="71732-135">**Servera URL**, **Ierīces ID** un **Reģistra numuru** lauki ir jāiestata, izmantojot informāciju no konfigurācijas faila, ko lejupielādējāt iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="71732-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="71732-136">Atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="71732-136">Select **Activate**.</span></span>
5. <span data-ttu-id="71732-137">Tiek parādīts autentifikācijas dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="71732-137">An authentication dialog box appears.</span></span> <span data-ttu-id="71732-138">Atlasiet kontu, kas izmanto e-pasta adresi, kas iepriekš bija saistīta ar darbinieku **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="71732-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="71732-139">Ja vēl neesat saistījis darbinieku ar savu identitāti, aktivizēšana nebūs veiksmīga.</span><span class="sxs-lookup"><span data-stu-id="71732-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="71732-140">Šādā gadījumā izpildiet darbības sadaļā “Saistīt darbinieku ar savu identitāti”, kas aprakstītas tēmā [Dynamics 365 Commerce novērtējuma vides konfigurācija](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="71732-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="71732-141">Kad tiek parādīta uzvedne ar aicinājumu ļaut organizācijai pārvaldīt ierīci, atlasiet **Tikai šo programmu**.</span><span class="sxs-lookup"><span data-stu-id="71732-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="71732-142">Kad aktivizēšana ir pabeigta, atlasiet **Sākt darbu**.</span><span class="sxs-lookup"><span data-stu-id="71732-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="71732-143">Iespējot BOPIS Modern POS</span><span class="sxs-lookup"><span data-stu-id="71732-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="71732-144">Piesakieties Modern POS, izmantojot **000713** kā operatora ID un **123** kā paroli.</span><span class="sxs-lookup"><span data-stu-id="71732-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="71732-145">Kamēr tiek demonstrēts ievada video, atzīmējiet abas izvēles rūtiņas dialoglodziņa apakšējā kreisajā stūrī un pēc tam aizveriet dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="71732-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="71732-146">Ja netiek parādīta uzvedne, lai aizvērtu maiņu, ritiniet pa labi **Sveiciena** lapā, atlasiet **Aizvērt maiņu** un pēc tam piesakieties POS.</span><span class="sxs-lookup"><span data-stu-id="71732-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="71732-147">Pēc tam, kad esat pieteicies, saņemot aicinājumu, atlasiet **Veikt neapstrādātu operāciju**.</span><span class="sxs-lookup"><span data-stu-id="71732-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="71732-148">**Sveiciena** lapā ritiniet pa labi un atlasiet darbību **Atlasīt aparatūras staciju**.</span><span class="sxs-lookup"><span data-stu-id="71732-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="71732-149">Atlasiet **Pārvaldīt**, iestatiet opciju **Izmantot aparatūras staciju** uz **Ieslēgts** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="71732-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="71732-150">Izrakstieties no POS un pēc tam pierakstieties tajā atkal.</span><span class="sxs-lookup"><span data-stu-id="71732-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="71732-151">Kad esat pieteicies, atlasiet **Atvērt jaunu maiņu** un pēc tam atlasiet **Atvilktne**.</span><span class="sxs-lookup"><span data-stu-id="71732-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="71732-152">Pabeigt BOPIS scenāriju</span><span class="sxs-lookup"><span data-stu-id="71732-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="71732-153">Izveidot veikala pasūtījumu savākšanai veikalā</span><span class="sxs-lookup"><span data-stu-id="71732-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="71732-154">Dodieties uz vietrādi URL, kas norādīts, [Inicializēt e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) darbībā vides konfigurācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="71732-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="71732-155">Atlasiet krājumu un izvēlieties **Pievienot grozam**.</span><span class="sxs-lookup"><span data-stu-id="71732-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="71732-156">Iepirkumu groza lapā atlasiet opciju **Paņemt šo** pasūtījuma rindai, kuru tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="71732-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="71732-157">Dialoglodziņā **Atlasīt veikalu** ievadiet **Sanfrancisko** un pēc tam atlasiet pogu **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="71732-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="71732-158">Rezultātu sarakstā atrodiet Sanfrancisko veikalu un atlasiet **Saņemt šeit**.</span><span class="sxs-lookup"><span data-stu-id="71732-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="71732-159">Iepirkumu groza lapā atlasiet **Norēķināties kā viesim**.</span><span class="sxs-lookup"><span data-stu-id="71732-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="71732-160">Lai turpinātu norēķināšanos, ir jāpiekrīt sīkfailu paziņojumam.</span><span class="sxs-lookup"><span data-stu-id="71732-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="71732-161">Šis paziņojums tiek parādīts kā reklāmkarogs norēķinu lapas augšpusē.</span><span class="sxs-lookup"><span data-stu-id="71732-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="71732-162">Kredītkartes maksājuma metodei ievadiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="71732-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="71732-163">**Kartes īpašnieka vārds:** ievadiet jebkādu vārdu.</span><span class="sxs-lookup"><span data-stu-id="71732-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="71732-164">**Kartes numurs:** ievadiet **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="71732-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="71732-165">**Derīguma termiņa datums:** ievadiet**10/20**.</span><span class="sxs-lookup"><span data-stu-id="71732-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="71732-166">**Kartes verificēšanas vērtības (CVV) kods:** ievadiet **737**.</span><span class="sxs-lookup"><span data-stu-id="71732-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="71732-167">Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju.</span><span class="sxs-lookup"><span data-stu-id="71732-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="71732-168">Turpiniet norēķināšanos, ievadot detalizētu informāciju par rēķina adresi, un pēc tam atlasiet **Saglabāt un turpināt**.</span><span class="sxs-lookup"><span data-stu-id="71732-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="71732-169">Kad pasūtījums ir gatavs, atlasiet **Norēķināties**.</span><span class="sxs-lookup"><span data-stu-id="71732-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="71732-170">Sinhronizēt tiešsaistes pasūtījumus uz atbalsta biroju</span><span class="sxs-lookup"><span data-stu-id="71732-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="71732-171">Lai iegūtu informāciju par to, kā sinhronizēt tiešsaistes pasūtījumus, skatiet [Tiešsaistes pārdošanas un maksājumu grāmatošana](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="71732-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="71732-172">Pasūtīšana tiešsaistē un saņemšana veikalā</span><span class="sxs-lookup"><span data-stu-id="71732-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="71732-173">Pierakstieties pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="71732-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="71732-174">**Sveiciena** ekrānā atlasiet **Pasūtījuma izpilde**</span><span class="sxs-lookup"><span data-stu-id="71732-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="71732-175">Saņemšanai paredzēto krājumu sarakstā atlasiet rindu no pasūtījuma, kas tika ievietots tiešsaistē.</span><span class="sxs-lookup"><span data-stu-id="71732-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="71732-176">Kad ir atlasīta pasūtījuma rinda, atlasiet **Saņemt**.</span><span class="sxs-lookup"><span data-stu-id="71732-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="71732-177">Rindas vienums tiek pievienots darbības ekrānam, un **$0,00** tiek rādīta kā maksājamā bilance.</span><span class="sxs-lookup"><span data-stu-id="71732-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="71732-178">Izvēlieties atlikumu **$0,00**, vai atlasiet jebkuru maksāšanas metodi, lai noslēgtu transakciju.</span><span class="sxs-lookup"><span data-stu-id="71732-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="71732-179">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="71732-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="71732-180">POS izveidotajiem tiešsaistes pasūtījumiem nav nulles bilances</span><span class="sxs-lookup"><span data-stu-id="71732-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="71732-181">Kad pasūtījums ir iegūts saņemšanai veikalā, ja atlikums nav 0 (nulle), pārliecinieties, ka Modern POS tiek izmantots un ka aparatūras stacija ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="71732-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="71732-182">Ja tiek izmantota sistēma Mākonis POS vai Modern POS operētājsistēmai iOS, pārliecinieties, ka koplietojamā aparatūras stacija ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="71732-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="71732-183">Lai izgūtu maksājumus, kas veikti tiešsaistē, ir nepieciešama kāda aktīva aparatūras stacijas forma.</span><span class="sxs-lookup"><span data-stu-id="71732-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="71732-184">Galvenās problēmas ar maksājuma tveršanu</span><span class="sxs-lookup"><span data-stu-id="71732-184">General issues with payment capture</span></span>

<span data-ttu-id="71732-185">Par visiem vispārējiem jautājumiem kā pirmo darbību vienmēr ir jākonsultējas ar Modern POS vai interneta informācijas pakalpojumu (IIS) aparatūras stacijas notikumu žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="71732-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="71732-186">Šos žurnālus var atrast šādos mezglos Windows notikumu žurnālā:</span><span class="sxs-lookup"><span data-stu-id="71732-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="71732-187">Programmu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="71732-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="71732-188">Programmu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="71732-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71732-189">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="71732-189">Additional resources</span></span>

[<span data-ttu-id="71732-190">Dynamics 365 Commerce novērtējuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="71732-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="71732-191">Dynamics 365 Commerce novērtējuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="71732-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="71732-192">Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="71732-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="71732-193">Bieži uzdotie jautājumi par Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="71732-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="71732-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="71732-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="71732-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="71732-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="71732-196">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="71732-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="71732-197">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="71732-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="71732-198">Adyen maksājumu savienotājs</span><span class="sxs-lookup"><span data-stu-id="71732-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="71732-199">Tiešsaistes maksājumu instrumentu saglabāšana, izmantojot savienotāju Adyen</span><span class="sxs-lookup"><span data-stu-id="71732-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="71732-200">Pārskats par Omni kanāla maksājumiem</span><span class="sxs-lookup"><span data-stu-id="71732-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
