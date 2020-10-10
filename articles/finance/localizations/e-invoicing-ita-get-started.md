---
title: Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai elektronisko rēķinu izrakstīšanas pievienojumprogrammai programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ea0408f4ef72bf77a0659799075338e4e6b2aa30
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835994"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="c3981-103">Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai</span><span class="sxs-lookup"><span data-stu-id="c3981-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="c3981-104">Elektronisko rēķinu izrakstīšanas pievienojumprogramma Itālija, iespējams, pašlaik neatbalsta visas funkcijas, kas ir pieejamas elektroniskajiem rēķiniem Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3981-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="c3981-105">Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumu Itālijai.</span><span class="sxs-lookup"><span data-stu-id="c3981-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="c3981-106">Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts risinājumos Regulatory Configuration Services (RCS) un Finance.</span><span class="sxs-lookup"><span data-stu-id="c3981-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="c3981-107">Tas arī palīdz veikt to elektronisko rēķinu iesniegšanas procesu, kas tiek ģenerēti Itālijai specifiskajā **FatturaPA** formātā, izmantojot šo pakalpojumu, un tas izskaidro, kā pārskatīt apstrādes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="c3981-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c3981-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="c3981-108">Prerequisites</span></span>

<span data-ttu-id="c3981-109">Pirms šajā tēmā aprakstīto darbību veikšanas ir jāpabeidz darbības sadaļā [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="c3981-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="c3981-110">RCS iestatījumi</span><span class="sxs-lookup"><span data-stu-id="c3981-110">RCS setup</span></span>

<span data-ttu-id="c3981-111">RCS iestatīšanas laikā jūs veiksiet šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="c3981-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="c3981-112">Importējiet e-rēķinu izrakstīšanas līdzekli debitoru elektronisko rēķinu eksportēšanai **FatturaPA** formātā.</span><span class="sxs-lookup"><span data-stu-id="c3981-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="c3981-113">Pārskatiet formāta konfigurācijas, kas nepieciešamas, lai ģenerētu, iesniegtu un saņemtu atbildes par elektroniskiem rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="c3981-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="c3981-114">Konfigurējiet notikumus, kas atbalsta elektronisko rēķinu iesniegšanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="c3981-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="c3981-115">Publicējiet e-rēķinu izrakstīšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c3981-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="c3981-116">"E-rēķina izrakstīšanas līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas pievienojumprogrammas serveri.</span><span class="sxs-lookup"><span data-stu-id="c3981-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="c3981-117">Šādā gadījumā debitoru elektronisko rēķinu eksportēšana ir uzstādāmais e-rēķinu līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="c3981-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="c3981-118">Importējiet e-rēķinu izrakstīšanas līdzekli</span><span class="sxs-lookup"><span data-stu-id="c3981-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="c3981-119">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="c3981-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c3981-120">Darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekli** atlasiet elementu **e-rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="c3981-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="c3981-121">Lapā **E-rēķina līdzekļi** atlasiet **Importēt**, lai importētu e-rēķinu izrakstīšanas līdzekli no Globālās krātuves.</span><span class="sxs-lookup"><span data-stu-id="c3981-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c3981-122">Ja nav redzams pieejamo līdzekļu saraksts, atlasiet **Sinhronizēt**.</span><span class="sxs-lookup"><span data-stu-id="c3981-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="c3981-123">Atlasiet līdzekli **E-rēķinu eksportēšana (IT)** un pēc tam atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="c3981-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![E-rēķinu eksportēšanas (IT) līdzekļa importēšana](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="c3981-125">Importējot līdzekli **E-rēķina eksportēšana (IT)** no globālās krātuves, tiek importēti arī visi nākamajā sadaļā aprakstītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="c3981-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="c3981-126">Izveidot jaunu e-rēķina eksportēšanas (IT) līdzekļa versiju</span><span class="sxs-lookup"><span data-stu-id="c3981-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="c3981-127">Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c3981-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Jaunas e-rēķinu izrakstīšanas līdzekļa versijas pievienošana](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="c3981-129">Pēc tam konfigurējiet elektronisko pārskatu (Electronic reporting - ER) formātus, kas ir saistīti ar e-rēķinu izrakstīšanas līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c3981-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="c3981-130">Cilnē **Konfigurācijas** atlasiet **Pievienot**, lai pārvaldītu konfigurācijas versijas.</span><span class="sxs-lookup"><span data-stu-id="c3981-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![E-rēķinu izrakstīšanas līdzekļa konfigurācijas versiju pārvaldība](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="c3981-132">Šajā darbībā jūs pievienojat un konfigurējat ER formātus dažādiem failiem, kas tiek izmantoti, lai eksportētu itāļu e-rēķinus.</span><span class="sxs-lookup"><span data-stu-id="c3981-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="c3981-133">Itāļu FatturaPA e-rēķiniem izmantojiet šādas standarta konfigurācijas vai faktiskās pielāgotās konfigurācijas, ko izmantojat e-rēķinu izrakstīšanai:</span><span class="sxs-lookup"><span data-stu-id="c3981-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="c3981-134">Pārdošanas rēķins (IT)</span><span class="sxs-lookup"><span data-stu-id="c3981-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="c3981-135">Projekta rēķins (IT)</span><span class="sxs-lookup"><span data-stu-id="c3981-135">Project invoice (IT)</span></span>

    <span data-ttu-id="c3981-136">Kad izveidojat e-rēķinu izrakstīšanas līdzekli, kas ir atvasināts no cita e-rēķinu izrakstīšanas līdzekļa, visi ER formāti tiek pārmantoti no oriģinālā līdzekļa.</span><span class="sxs-lookup"><span data-stu-id="c3981-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="c3981-137">Atlasiet noteiktu ER formāta faila konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c3981-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="c3981-138">Atlasiet **Rediģēt** vai **Skatīt**, lai atvērtu lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="c3981-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Formāta veidotāja lapas atvēršana](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="c3981-140">Lai rediģētu un skatītu ER formāta failu konfigurācijas, izmantojiet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="c3981-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Formāta veidotāja lapa](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="c3981-142">Pārvaldīt e-rēķinu izrakstīšanas līdzekļa iestatījumus</span><span class="sxs-lookup"><span data-stu-id="c3981-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="c3981-143">Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Pievienot**, **Dzēst** vai **Rediģēt**, lai pārvaldītu e-rēķinu izrakstīšanas līdzekļa iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c3981-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![E-rēķinu izrakstīšanas līdzekļa iestatījumu pārvaldība](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="c3981-145">Šajā darbībā konfigurējiet notikumus, kas attiecināmi uz elektroniskajiem rēķiniem, tostarp XML izvades failu ģenerēšanu **FatturaPA** formātā un digitālu parakstīšanu (ja nepieciešams).</span><span class="sxs-lookup"><span data-stu-id="c3981-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="c3981-146">Konfigurēt pārdošanas rēķina līdzekļu iestatījumu</span><span class="sxs-lookup"><span data-stu-id="c3981-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="c3981-147">Lapā **E-rēķina līdzekļi** cilnē **Iestatījumi** kolonnā **Līdzekļu iestatīšana** atlasiet **Pārdošanas rēķins**.</span><span class="sxs-lookup"><span data-stu-id="c3981-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="c3981-148">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c3981-148">Select **Edit**.</span></span>
3. <span data-ttu-id="c3981-149">Lapā **Līdzekļu versijas iestatīšana** atlasiet cilni **Darbības**, lai pārvaldītu darbību sarakstu.</span><span class="sxs-lookup"><span data-stu-id="c3981-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="c3981-150">Darbības definē oprerāciju sarakstu, kas ir jāpalaiž secīgi, lai veiktu notikuma pilnīgu izpildi.</span><span class="sxs-lookup"><span data-stu-id="c3981-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Cilne Darbības](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="c3981-152">Darbības ID</span><span class="sxs-lookup"><span data-stu-id="c3981-152">Action ID</span></span> | <span data-ttu-id="c3981-153">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="c3981-153">Action name</span></span>        | <span data-ttu-id="c3981-154">Darbības apraksts</span><span class="sxs-lookup"><span data-stu-id="c3981-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="c3981-155">1</span><span class="sxs-lookup"><span data-stu-id="c3981-155">1</span></span>         | <span data-ttu-id="c3981-156">Transformējiet dokumentu</span><span class="sxs-lookup"><span data-stu-id="c3981-156">Transform document</span></span> | <span data-ttu-id="c3981-157">Izveidojiet e-rēķina XML failu **FatturaPA** formātā.</span><span class="sxs-lookup"><span data-stu-id="c3981-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="c3981-158">2</span><span class="sxs-lookup"><span data-stu-id="c3981-158">2</span></span>         | <span data-ttu-id="c3981-159">Parakstīt dokumentu</span><span class="sxs-lookup"><span data-stu-id="c3981-159">Sign document</span></span>      | <span data-ttu-id="c3981-160">Lietojiet digitālo parakstu XML failam.</span><span class="sxs-lookup"><span data-stu-id="c3981-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="c3981-161">Atlasiet cilni **Piemērojamības noteikumi**, lai skatītu un uzturētu piemērojamības noteikumus.</span><span class="sxs-lookup"><span data-stu-id="c3981-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="c3981-162">Piemērojamības noteikumi nosaka kontekstu, kurā darbība tiks izpildīta.</span><span class="sxs-lookup"><span data-stu-id="c3981-162">Applicability rules define the context where the action will be run.</span></span>

    ![Piemērojamības noteikumu cilne](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="c3981-164">Atlasiet cilni **Mainīgie**, lai skatītu un uzturētu mainīgos.</span><span class="sxs-lookup"><span data-stu-id="c3981-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Cilne Mainīgie](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="c3981-166">Definējiet publiskus mainīgos, kas nepieciešami darbību izpildei.</span><span class="sxs-lookup"><span data-stu-id="c3981-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="c3981-167">Konfigurēt projektu rēķina līdzekļa iestatījumu</span><span class="sxs-lookup"><span data-stu-id="c3981-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="c3981-168">Darbības un iestatījumi, kas nepieciešami līdzekļa **Projekta rēķins** iestatījuma konfigurēšanai, ir ļoti līdzīgi līdzekļa **Pārdošanas rēķins** iestatījuma darbībām un iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="c3981-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="c3981-169">Strādājot ar projekta rēķiniem, skatiet pārdošanas rēķinu procedūras.</span><span class="sxs-lookup"><span data-stu-id="c3981-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="c3981-170">E-rēķinu izrakstīšanas līdzekļa piešķiršana videi</span><span class="sxs-lookup"><span data-stu-id="c3981-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="c3981-171">Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Vides** atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="c3981-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="c3981-172">Laukā **Vide** atlasiet vidi.</span><span class="sxs-lookup"><span data-stu-id="c3981-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="c3981-173">Laukā **Spēkā no** atlasiet datumu, kad videi jāstājas spēkā.</span><span class="sxs-lookup"><span data-stu-id="c3981-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="c3981-174">Atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="c3981-174">Select **Enable**.</span></span> 

![E-rēķina vides iespējošana](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="c3981-176">Publicējiet e-rēķinu izrakstīšanas līdzekli</span><span class="sxs-lookup"><span data-stu-id="c3981-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="c3981-177">Varat publicēt e-rēķinu izrakstīšanas līdzekli, mainot versijas statusu uz **Pabeigts** vai **Publicēts**.</span><span class="sxs-lookup"><span data-stu-id="c3981-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="c3981-178">Mainiet versijas statusu uz Pabeigts</span><span class="sxs-lookup"><span data-stu-id="c3981-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="c3981-179">Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="c3981-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="c3981-180">Atlasiet **Mainīt statusu \> Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="c3981-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="c3981-181">Mainiet versijas statusu uz Publicēts</span><span class="sxs-lookup"><span data-stu-id="c3981-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="c3981-182">Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="c3981-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="c3981-183">Atlasiet **Mainīt statusu \> Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="c3981-183">Select **Change status \> Publish**.</span></span>

![E-rēķinu izrakstīšanas līdzekļa statusa maiņa](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="c3981-185">Iestatiet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrāciju programmā Finance</span><span class="sxs-lookup"><span data-stu-id="c3981-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="c3981-186">Finance iestatīšanas laikā jūs veiksiet šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="c3981-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="c3981-187">Importējiet ER datu modeli, ER datu modeļa kartēšanu un konteksta konfigurācijas FatturaPA e-rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="c3981-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="c3981-188">Konfigurējiet sertifikātu, kas nepieciešams, lai digitāli parakstītu itāļu e-rēķinus.</span><span class="sxs-lookup"><span data-stu-id="c3981-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="c3981-189">Importējiet ER datu modeli, datu modeļa kartēšanu un formātus</span><span class="sxs-lookup"><span data-stu-id="c3981-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="c3981-190">Darbvietā **Elektroniskie pārskati** pārbaudiet, vai konfigurācijas nodrošinātājs **Biznesa dokumentu pakalpojums** ir iestatīts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="c3981-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="c3981-191">Atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="c3981-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="c3981-192">Atlasiet **Globālais resurss \> Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="c3981-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="c3981-193">Importēt **Rēķina modelis**, **Rēķina modeļa kartēšana** un **Debitora rēķina konteksta modelis**.</span><span class="sxs-lookup"><span data-stu-id="c3981-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="c3981-194">Ieslēgt līdzekli, lai eksportētu debitoru elektroniskos rēķinus Itālijai</span><span class="sxs-lookup"><span data-stu-id="c3981-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="c3981-195">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="c3981-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="c3981-196">Cilnē **Līdzekļi** atzīmējiet izvēles rūtiņu **Iespējots**, kas atrodas līdzekļu reksturojuma rindā **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="c3981-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![FatturaPA līdzekļa ieslēgšana](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="c3981-198">Konfigurēt elektroniskos dokumentus</span><span class="sxs-lookup"><span data-stu-id="c3981-198">Configure electronic documents</span></span>

1. <span data-ttu-id="c3981-199">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="c3981-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="c3981-200">Cilnē **Elektroniskais dokuments** atlasiet **Pievienot** un ievadiet tabulas, kas nepieciešamas, lai ģenerētu itāļu e-rēķinus:</span><span class="sxs-lookup"><span data-stu-id="c3981-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="c3981-201">**Tabulas nosaukums:** Debitoru rēķinu žurnāls</span><span class="sxs-lookup"><span data-stu-id="c3981-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="c3981-202">**Tabulas nosaukums:** Projekta rēķins</span><span class="sxs-lookup"><span data-stu-id="c3981-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="c3981-203">Katrai tabulai definējiet saistīto dokumentu kontekstu:</span><span class="sxs-lookup"><span data-stu-id="c3981-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="c3981-204">Tabulai **Debitoru rēķinu žurnāls** atlasiet **Debitora rēķina konteksts**.</span><span class="sxs-lookup"><span data-stu-id="c3981-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="c3981-205">Tabulai **Projekta rēķins** atlasiet **Projekta rēķina konteksts**.</span><span class="sxs-lookup"><span data-stu-id="c3981-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Atbilžu veidu iestatīšana](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="c3981-207">Elektroniska rēķina apstrāde</span><span class="sxs-lookup"><span data-stu-id="c3981-207">Electronic invoice processing</span></span>

<span data-ttu-id="c3981-208">Finance apstrādes laikā jūs veiksiet šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="c3981-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="c3981-209">Ģenerēt itāļu e-rēķinus, izmantojot elektronisko rēķinu izrakstīšanas pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="c3981-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="c3981-210">Skatiet izpildes žurnālus un pārskatiet apstrādes rezultātus</span><span class="sxs-lookup"><span data-stu-id="c3981-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="c3981-211">Ģenerēt elektroniskos rēķinus</span><span class="sxs-lookup"><span data-stu-id="c3981-211">Generate electronic invoices</span></span>

<span data-ttu-id="c3981-212">Pēc tam, kad ieslēdzat līdzekli **Konfigurējamu elektronisko rēķinu pievienošana** un aktivizējat līdzekli **IT00036**, vairs nevar izmantot veco finanšu procesu itāļu e-rēķinu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c3981-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="c3981-213">Tas ir aizstāts ar jaunu procesu, kura nosaukums ir **Iesniegt elektroniskus dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="c3981-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="c3981-214">Varat iesniegt dokumentus manuāli, pamatojoties uz pieprasījumu e-rēķinu dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="c3981-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="c3981-215">Pirms turpināt, pārbaudiet, vai ir pabeigts itāļu e-rēķiniem nepieciešamais iestatījums.</span><span class="sxs-lookup"><span data-stu-id="c3981-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="c3981-216">Plašāku informāciju skatiet šeit: [Debitoru elektroniskie rēķini](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="c3981-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="c3981-217">Ņemiet vērā, ka daži no šajā tēmā aprakstītajiem iestatīšanas darbībam var nebūt pieejamas elektronisko rēķinu izrakstīšanas pievienojumprogrammas aktivizēšanas dēļ.</span><span class="sxs-lookup"><span data-stu-id="c3981-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="c3981-218">Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Iesniegt elektroniskus dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="c3981-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="c3981-219">Pirmā dokumenta iesniegšanai iestatiet opciju **Atkārtoti iesniegt dokumentus** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="c3981-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="c3981-220">Ja ir atkārtoti jāiesniedz dokuments, izmantojot pakalpojumu, iestatiet šo opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c3981-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="c3981-221">Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu dialoglodziņu **Pieprasījums**, kur var izveidot vaicājumu, lai atlasītu dokumentus iesniegšanai.</span><span class="sxs-lookup"><span data-stu-id="c3981-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Dialoglodziņš Iesniegt elektroniskos dokumentus](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="c3981-223">Filtra vaicājums</span><span class="sxs-lookup"><span data-stu-id="c3981-223">Filter query</span></span>

1. <span data-ttu-id="c3981-224">Dialoglodziņā **Pieprasījums** konfigurējiet filtrēšanas nosacījumus gan pārdošanas rēķiniem, gan projekta rēķiniem, vai atstājiet nosacījumus tukšus, lai iekļautu visus neiesniegtos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="c3981-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Iesniegšanas filtra kritēriju iestatīšana](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="c3981-226">Lai dialoglodziņu **Pieprasījums** aizvērtu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c3981-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="c3981-227">Atlasiet **Labi**, iesniedziet atlasītos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c3981-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="c3981-228">! [PIEZĪME] Pirmajā mēģinājumā iesniegt dokumentu, izmantojot pakalpojumu, jums tiks piedāvāts apstiprināt savienojumu ar elektronisko rēķinu pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="c3981-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="c3981-229">Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar elektronisko dokumentu iesniegšanas pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="c3981-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="c3981-230">Skatīt iesniegšanas žurnālus</span><span class="sxs-lookup"><span data-stu-id="c3981-230">View submission logs</span></span>

<span data-ttu-id="c3981-231">Varat skatīt visu iesniegto dokumentu iesniegšanas žurnālus.</span><span class="sxs-lookup"><span data-stu-id="c3981-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="c3981-232">Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="c3981-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="c3981-233">Laukā **Dokumenta veids** atlasiet **Debitora rēķina žurnāls** vai **Projekta rēķins**, lai filtrētu pieprasītos elektroniskos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c3981-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Dokumenta veida atlasīšana, lai apskatītu iesniegšanas žurnālus](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="c3981-235">Vērtība, kas tiek rādīta kolonnā **Iesniegšanas statuss**, norāda iesniegšanas procesa statusu.</span><span class="sxs-lookup"><span data-stu-id="c3981-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="c3981-236">Tas norāda, vai process darbojās kā konfigurēts, un vai ir nepieciešama papildu darbība.</span><span class="sxs-lookup"><span data-stu-id="c3981-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="c3981-237">Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="c3981-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="c3981-239">Kopsavilkuma cilnē **Apstrādes darbības** var skatīt izpildes žurnālu darbībām, kas konfigurētas līdzekļa versijā, kas tika iestatīta RCS.</span><span class="sxs-lookup"><span data-stu-id="c3981-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="c3981-240">Kolonna **Statuss** rāda, vai darbība ir veiksmīgi izpildīta.</span><span class="sxs-lookup"><span data-stu-id="c3981-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="c3981-241">Kopsavilkuma cilnē **Darbības faili** var apskatīt starpposma failus, kas tika ģenerēti darbību izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="c3981-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="c3981-242">Varat atlasīt **Skats**, lai lejupielādētu izvades XML failu **FatturaPA** formātā un apskatīt tā saturu.</span><span class="sxs-lookup"><span data-stu-id="c3981-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3981-243">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="c3981-243">Related topics</span></span>

- [<span data-ttu-id="c3981-244">Pārskats par elektronisko rēķinu izrakstīšanas pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="c3981-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="c3981-245">Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="c3981-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="c3981-246">Elektronisko rēķinu izrakstīšanas pievienojumprogrammas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c3981-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
