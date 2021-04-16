---
title: Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumiem
description: Šajā tēmā skaidrots jaunās nodokļu funkcionalitātes atbalsts pārsūtīšanas pasūtījumiem, izmantojot nodokļu aprēķināšanas pakalpojumu.
author: kailiang
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 55597e4f0f40677e793b4c182e4b0ced01057751
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832565"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="b3780-103">Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="b3780-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b3780-104">Šajā tēmā sniegta informācija par nodokļu aprēķināšanu un integrācijas grāmatošanu pārsūtīšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b3780-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="b3780-105">Šī funkcionalitāte ļauj jums iestatīt nodokļu aprēķinu un grāmatošanu pārsūtīšanas pasūtījumos krājumu pārsūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="b3780-106">Saskaņā ar Eiropas Savienības (ES) pievienotās vērtības nodokļa (PVN) noteikumiem krājumu pārsūtīšana tiek uzskatīta par piegādi Kopienas iekšienē un iegādi Kopienas iekšienē.</span><span class="sxs-lookup"><span data-stu-id="b3780-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="b3780-107">Lai konfigurētu un lietotu šo funkcionalitāti, ir jāveic trīs galvenās darbības:</span><span class="sxs-lookup"><span data-stu-id="b3780-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="b3780-108">**RCS iestatījumi**: regulēšanas konfigurācijas pakalpojumā iestatiet nodokļu līdzekli, nodokļu kodus un nodokļu kodu piemērojamību nodokļa koda noteikšanai pārsūtīšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b3780-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="b3780-109">**Finanšu iestatīšana**: programmā Microsoft Dynamics 365 Finance līdzekļa **Nodoklis** pārsūtīšanas pasūtījumā iestatiet krājumu nodokļu pakalpojumu parametrus un iestatiet galvenos nodokļu parametrus.</span><span class="sxs-lookup"><span data-stu-id="b3780-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="b3780-110">**Krājumu iestatīšana**: iestatiet krājumu konfigurāciju pārsūtīšanas pasūtījumu darījumiem.</span><span class="sxs-lookup"><span data-stu-id="b3780-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="b3780-111">Nodokļu un pārsūtīšanas pasūtījumu darījumu RCS iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b3780-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="b3780-112">Veiciet šīs darbības, lai iestatītu nodokli, kas ir iesaistīts pārsūtīšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="b3780-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="b3780-113">Šeit parādītajā piemērā pārsūtīšanas pasūtījums ir no Nīderlandes uz Beļģiju.</span><span class="sxs-lookup"><span data-stu-id="b3780-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="b3780-114">Lapā **Nodokļu līdzekļi**, cilnē **Versijas** atlasiet melnraksta līdzekļa versiju un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="b3780-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Atlasot Rediģēt](../media/image1.png)

2. <span data-ttu-id="b3780-116">Lapā **Nodokļu līdzekļu iestatījums** cilnē **Nodokļu kodi** atlasiet **Pievienot**, lai izveidotu jaunus nodokļu kodus.</span><span class="sxs-lookup"><span data-stu-id="b3780-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="b3780-117">Šajā piemērā ir izveidoti trīs nodokļu kodi: **NL-Neapliekamais**, **BE-RC-21** un **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="b3780-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="b3780-118">Kad pārsūtīšanas pasūtījums tiek nosūtīts no noliktavas Nīderlandē, tiek piemērots Nīderlandes PVN atbrīvotā nodokļa kods (**NL-Neapliekamais**).</span><span class="sxs-lookup"><span data-stu-id="b3780-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="b3780-119">Izveidojiet nodokļu kodu **NL-Neapliekamais**.</span><span class="sxs-lookup"><span data-stu-id="b3780-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="b3780-120">Atlasiet **Pievienot** ievadiet **NL-Neapliekamais** laukā **Nodokļa kods**.</span><span class="sxs-lookup"><span data-stu-id="b3780-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="b3780-121">Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.</span><span class="sxs-lookup"><span data-stu-id="b3780-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="b3780-122">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b3780-122">Select **Save**.</span></span>
        4. <span data-ttu-id="b3780-123">Atlasiet **Pievienot** tabulā **Likme**.</span><span class="sxs-lookup"><span data-stu-id="b3780-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="b3780-124">Pārsledziet **Ir neapliekams** uz **Jā** sadaļā **Vispārējais**.</span><span class="sxs-lookup"><span data-stu-id="b3780-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Neapliekamā nodokļa kods](../media/image2.png)

    - <span data-ttu-id="b3780-126">Kad pārsūtīšanas pasūtījums tiek saņemts Beļģijas noliktavā, atgriezeniskās maksas mehānisms tiek piemērots, izmantojot **BE-RC-21** un **BE-RC+21** nodokļu kodus.</span><span class="sxs-lookup"><span data-stu-id="b3780-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="b3780-127">Izveidojiet nodokļa kodu **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="b3780-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="b3780-128">Atlasiet **Pievienot** ievadiet **BE-RC-21** laukā **Nodokļa kods**.</span><span class="sxs-lookup"><span data-stu-id="b3780-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="b3780-129">Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.</span><span class="sxs-lookup"><span data-stu-id="b3780-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="b3780-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b3780-130">Select **Save**.</span></span>
        4. <span data-ttu-id="b3780-131">Atlasiet **Pievienot** tabulā **Likme**.</span><span class="sxs-lookup"><span data-stu-id="b3780-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="b3780-132">Ievadiet **-21** laukā **Nodokļa likme**.</span><span class="sxs-lookup"><span data-stu-id="b3780-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="b3780-133">Pārsledziet **Ir apgrieztā maksa** uz **Jā** sadaļā **Vispārējais**.</span><span class="sxs-lookup"><span data-stu-id="b3780-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="b3780-134">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b3780-134">Select **Save**.</span></span>

        ![BE-RC-21 nodokļa kods apgrieztām maksām](../media/image3.png)
        
        <span data-ttu-id="b3780-136">Izveidojiet nodokļa kodu **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="b3780-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="b3780-137">Atlasiet **Pievienot** ievadiet **BE-RC-21** laukā **Nodokļa kods**.</span><span class="sxs-lookup"><span data-stu-id="b3780-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="b3780-138">Atlasiet **Pēc neto summas** laukā **Nodokļu komponents**.</span><span class="sxs-lookup"><span data-stu-id="b3780-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="b3780-139">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b3780-139">Select **Save**.</span></span>
        4. <span data-ttu-id="b3780-140">Atlasiet **Pievienot** tabulā **Likme**.</span><span class="sxs-lookup"><span data-stu-id="b3780-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="b3780-141">Ievadiet **21** laukā **Nodokļa likme**.</span><span class="sxs-lookup"><span data-stu-id="b3780-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="b3780-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b3780-142">Select **Save**.</span></span>

        ![BE-RC+21 nodokļa kods apgrieztām maksām](../media/image4.png)

3. <span data-ttu-id="b3780-144">Nosakiet nodokļa kodu piemērojamību.</span><span class="sxs-lookup"><span data-stu-id="b3780-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="b3780-145">Atlasiet **Pārvaldīt kolonnas** un pēc tam atlasiet kolonnas, kas ir jāizmanto, lai izveidotu piemērojamības tabulu.</span><span class="sxs-lookup"><span data-stu-id="b3780-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b3780-146">Noteikti pievienojiet tabulai kolonnas **Biznesa process** un **Nodokļu virziens**.</span><span class="sxs-lookup"><span data-stu-id="b3780-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="b3780-147">Abas kolonnas ir būtiskas nodokļu funkcionalitātei pārsūtīšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b3780-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="b3780-148">Pievienot piemērojamības noteikumus.</span><span class="sxs-lookup"><span data-stu-id="b3780-148">Add applicability rules.</span></span> <span data-ttu-id="b3780-149">Laukus **Nodokļu kodi**, **Nodokļu grupa** un **Krājumu nodokļu grupa** nedrīkst atstāt tukšus.</span><span class="sxs-lookup"><span data-stu-id="b3780-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="b3780-150">Pievienojiet jaunu kārtulu pārsūtīšanas pasūtījuma kravai.</span><span class="sxs-lookup"><span data-stu-id="b3780-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="b3780-151">Atlasiet **Pievienot** tabulā **Piemērošanas noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="b3780-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="b3780-152">Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="b3780-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="b3780-153">Laukā **Nosūtīt no valsts/reģiona** ievadiet **NLD**.</span><span class="sxs-lookup"><span data-stu-id="b3780-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="b3780-154">Laukā **Nosūtīt uz valsti/reģionu** ievadiet **BEL**.</span><span class="sxs-lookup"><span data-stu-id="b3780-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="b3780-155">Laukā **Nodokļu virziens** atlasiet **Izvade**, lai kārtulu padarītu piemērojamu pārsūtīšanas pasūtījuma nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="b3780-156">Laukā **Nodokļa kodi** atlasiet **NL-Neapliekamais**.</span><span class="sxs-lookup"><span data-stu-id="b3780-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="b3780-157">Laukā **Nodokļu grupa** un **Krājuma nodokļu grupa** ievadiet saistīto nodokļa grupu un krājumu nodokļa grupu, kas ir definēta jūsu Finanšu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="b3780-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="b3780-158">Pievienojiet citu kārtulu pārsūtīšanas pasūtījuma saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="b3780-159">Atlasiet **Pievienot** tabulā **Piemērošanas noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="b3780-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="b3780-160">Laukā **Biznesa process** atlasiet **Krājumi**, lai noteikums būtu piemērojams pārsūtīšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="b3780-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="b3780-161">Laukā **Nosūtīt no valsts/reģiona** ievadiet **NLD**.</span><span class="sxs-lookup"><span data-stu-id="b3780-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="b3780-162">Laukā **Nosūtīt uz valsti/reģionu** ievadiet **BEL**.</span><span class="sxs-lookup"><span data-stu-id="b3780-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="b3780-163">Laukā **Nodokļu virziens** atlasiet **Ievade**, lai kārtulu padarītu piemērojamu pārsūtīšanas pasūtījuma saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="b3780-164">Laukā **Nodokļu kodi** atlasiet **BE-RC+21** un **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="b3780-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="b3780-165">Laukā **Nodokļu grupa** un **Krājuma nodokļu grupa** ievadiet saistīto nodokļa grupu un krājumu nodokļa grupu, kas ir definēta jūsu Finanšu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="b3780-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Piemērojamības kārtulas](../media/image5.png)

4. <span data-ttu-id="b3780-167">Pabeidziet un publicējiet jauno nodokļu līdzekļu versiju.</span><span class="sxs-lookup"><span data-stu-id="b3780-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="b3780-168">[![Jaunas versijas statusa maiņa](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="b3780-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="b3780-169">Pārsūtīšanas pasūtījumu darījumu Finance iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b3780-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="b3780-170">Veiciet šīs darbības, lai iespējotu un iestatītu nodokļus pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="b3780-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="b3780-171">Francija dodieties uz **Darbvietas** \> **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b3780-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="b3780-172">Sarakstā atrodiet un atlasiet līdzekli **Nodoklis pārsūtīšanas pasūtījumā** un pēc tam atlasiet **Aktivizēt tūlīt**, lai to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="b3780-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b3780-173">Līdzeklis **Nodoklis pārsūtīšanas pasūtījumā** ir pilnībā atkarīgs no nodokļu pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="b3780-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="b3780-174">Tādēļ to var ieslēgt tikai pēc nodokļu pakalpojumu instalēšanas.</span><span class="sxs-lookup"><span data-stu-id="b3780-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Līdzeklis Nodoklis pārsūtīšanas pasūtījumā](../media/image7.png)

3. <span data-ttu-id="b3780-176">Iespējojiet nodokļu pakalpojumu un atlasiet biznesa procesu **Krājums**.</span><span class="sxs-lookup"><span data-stu-id="b3780-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b3780-177">Šī darbība ir jāveic katrai Finance juridiskajai personai, kur vēlaties, lai pārsūtīšanas pasūtījumos būtu pieejams nodokļu pakalpojums un funkcionalitāte nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="b3780-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="b3780-178">Doties uz **Nodoklis** \> **Iestatījums** \> **Nodokļa konfigurācija** \> **Nodokļu pakalpojuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b3780-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="b3780-179">Laukā **Biznesa process** atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="b3780-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Biznesa procesa lauka iestatīšana](../media/image8.png)

4. <span data-ttu-id="b3780-181">Pārbaudiet, vai ir iestatīts apgrieztās maksas mehānisms.</span><span class="sxs-lookup"><span data-stu-id="b3780-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="b3780-182">Dodieties uz **Virsgrāmata** \> **Iestatījums** \> **Parametri** un pēc tam cilnē **Apgrieztā maksa** pārbaudiet, vai opcija **Iespējot apgriezto maksu** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b3780-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Aktivizēt apgrieztās maksas opciju](../media/image9.png)

5. <span data-ttu-id="b3780-184">Pārbaudiet, vai saistītie nodokļu kodi, nodokļu grupas, krājumu nodokļu grupas un PVN reģistrācijas numuri ir iestatīti Finance atbilstoši nodokļu pakalpojuma vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="b3780-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="b3780-185">Iestatiet pagaidu tranzīta kontu.</span><span class="sxs-lookup"><span data-stu-id="b3780-185">Set up an interim transit account.</span></span> <span data-ttu-id="b3780-186">Šī darbība ir nepieciešama tikai tad, ja nodoklis, kas tiek lietots pārsūtīšanas pasūtījumam, nav piemērojams ar nodokli neapliekamam vai atgriezenisko maksājumu mehānismam.</span><span class="sxs-lookup"><span data-stu-id="b3780-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="b3780-187">Pārejiet uz sadaļu **Nodokļi** \> **Iestatījumi** \> **PVN** \> **Virsgrāmatas grāmatošanas grupas**.</span><span class="sxs-lookup"><span data-stu-id="b3780-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="b3780-188">Laukā **Pagaidu tranzīts** atlasiet Virsgrāmatas kontu.</span><span class="sxs-lookup"><span data-stu-id="b3780-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Atlasot pagaidu tranzīta kontu](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="b3780-190">Iestatīt pamata krājumus pārsūtīšanas pasūtījuma darījumiem</span><span class="sxs-lookup"><span data-stu-id="b3780-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="b3780-191">Veiciet šīs darbības, lai iestatītu pamata krājumus pārsūtīšanas pasūtījumu darījumu iespējošanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="b3780-192">Izveidojiet piegādes un nosūtīšanas vietas noliktavām dažādās valstīs vai reģionos un pievienojiet katras vietas primāro adresi.</span><span class="sxs-lookup"><span data-stu-id="b3780-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="b3780-193">Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Noliktava** \> **Vietas**.</span><span class="sxs-lookup"><span data-stu-id="b3780-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="b3780-194">Atlasiet **Jauns**, lai izveidotu vietu, kuru vēlāk piešķirsit noliktavai.</span><span class="sxs-lookup"><span data-stu-id="b3780-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="b3780-195">Atkārtojiet 2. darbību visām pārējām vietām, kas ir jāizveido.</span><span class="sxs-lookup"><span data-stu-id="b3780-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3780-196">Vienai no izveidotajām vietnēm ir jābūt nosauktai **Tranzīts**.</span><span class="sxs-lookup"><span data-stu-id="b3780-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="b3780-197">Vēlākās šīs procedūras darbībās šī vieta ir jāpiešķir tranzīta noliktavai, lai ar nodokļiem saistītos krājumu dokumentus varētu grāmatot “nosūtīšanas” un “saņemšanas” transakcijās pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="b3780-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="b3780-198">Tranzīta vietas adrese nav atbilstoša nodokļu aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="b3780-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="b3780-199">Tādēļ to var atstāt tukšu.</span><span class="sxs-lookup"><span data-stu-id="b3780-199">Therefore, you can leave it blank.</span></span>

    ![Vietu iestatīšana](../media/image11.png)

2. <span data-ttu-id="b3780-201">Izveidot piegādes, tranzīta un nosūtīšanas noliktavas.</span><span class="sxs-lookup"><span data-stu-id="b3780-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="b3780-202">Jebkura adreses informācija, kas tiek uzturēta noliktavā, nodokļu aprēķināšanas laikā ignorēs vietas adresi.</span><span class="sxs-lookup"><span data-stu-id="b3780-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="b3780-203">Dodieties uz **Noliktavas vadība** \> **Iestatīšana** \> **Noliktava** \> **Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="b3780-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="b3780-204">Atlasiet **Jauns**, lai izveidotu vietu un piešķir to atbilstošajai vietai.</span><span class="sxs-lookup"><span data-stu-id="b3780-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="b3780-205">Atkārtojiet 2. darbību, lai izveidotu noliktavu katrai vietai pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="b3780-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Noliktavu iestatīšana](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="b3780-207">Piegāde no noliktavas pārsūtīšanas pasūtījuma darījumiem laukā **Tranzīta noliktava** ir jāatlasa tranzīta noliktava.</span><span class="sxs-lookup"><span data-stu-id="b3780-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Tranzīta noliktavas atlasīšana](../media/image13.png)

3. <span data-ttu-id="b3780-209">Pārbaudiet, vai krājumu grāmatošanas konfigurācija ir iestatīta pārsūtīšanas pasūtījumu darījumiem.</span><span class="sxs-lookup"><span data-stu-id="b3780-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="b3780-210">Doties uz **Krājumu vadība** \> **Iestatīšana** \> **Grāmatojums** \> **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="b3780-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="b3780-211">Cilnē **Krājumi** pārbaudiet, vai Virsgrāmatas konts ir iestatīts gan **Krājumu izejas plūsmas**, gan **Krājumu ieejas plūsmas** grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Krājumu izejas un krājumu ieejas plūsmas grāmatošanas iestatīšana](../media/image14.png)

    3. <span data-ttu-id="b3780-213">Pārbaudiet, vai Virsgrāmatas konts ir iestatīts **Starpvienību maksājumu** grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Starpvienību maksājumu grāmatošanas iestatīšana](../media/image15.png)

    4. <span data-ttu-id="b3780-215">Pārbaudiet, vai Virsgrāmatas konts ir iestatīts **Starpvienību ieņēmumi** grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="b3780-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Starpvienību ieņēmumu grāmatošanas iestatīšana](../media/image16.png)
