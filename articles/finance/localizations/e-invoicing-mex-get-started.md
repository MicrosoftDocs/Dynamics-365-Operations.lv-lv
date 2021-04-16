---
title: Darba sākšana ar elektronisko rēķinu izveidi lietošanai Meksikā
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izveidi lietošanai Meksikā.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 2f5dd1d6bc520c9f5349c77dfcabdf2d538881ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840056"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="21184-103">Darba sākšana ar elektronisko rēķinu izveidi lietošanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="21184-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="21184-104">Elektronisko rēķinu izrakstīšana Meksikai pašlaik var nenodrošināt visas funkcijas, kas ir pieejamas Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management iebūvētajā Comprobante Fiscal Digital por Internet (CFDI) dokumentu integrācijā un saistītajā integrācijā.</span><span class="sxs-lookup"><span data-stu-id="21184-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="21184-105">Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izveidi lietošanai Meksikā.</span><span class="sxs-lookup"><span data-stu-id="21184-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="21184-106">Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts risinājumos Regulatory Configuration Services (RCS) un Finance.</span><span class="sxs-lookup"><span data-stu-id="21184-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="21184-107">Tas arī palīdz veikt darbības, kas jāveic programmā Finance, lai iesniegtu CFDI rēķinus, izmantojot pakalpojumu, un tas izskaidro, kā pārskatīt apstrādes rezultātus un CFDI rēķinu statusu.</span><span class="sxs-lookup"><span data-stu-id="21184-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21184-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="21184-108">Prerequisites</span></span>

<span data-ttu-id="21184-109">Pirms šajā tēmā aprakstīto darbību veikšanas ir jāpabeidz darbības sadaļā [Sākt darbu ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="21184-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="21184-110">RCS iestatījumi</span><span class="sxs-lookup"><span data-stu-id="21184-110">RCS setup</span></span>

<span data-ttu-id="21184-111">RCS iestatīšanas laikā jūs veiksiet šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="21184-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="21184-112">Importējiet e-rēķinu izrakstīšanas līdzekli CFDI rēķinu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="21184-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="21184-113">Pārskatiet formāta konfigurācijas, kas nepieciešamas, lai ģenerētu, iesniegtu un saņemtu atbildes par CFDI rēķiniem, un lai iesniegtu un saņemtu atbildes par atcelšanu.</span><span class="sxs-lookup"><span data-stu-id="21184-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="21184-114">Konfigurējiet notikumus, kas atbalsta CFDI rēķinu iesniegšanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="21184-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="21184-115">Publicējiet e-rēķinu izrakstīšanas līdzekli CFDI rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="21184-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="21184-116">"E-rēķina izrakstīšanas līdzeklis" ir vispārējs nosaukums resursam, kas ir konfigurēts un publicēts, lai varētu patērēt elektronisko rēķinu izrakstīšanas serveri.</span><span class="sxs-lookup"><span data-stu-id="21184-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="21184-117">Šajā gadījumā CFDI rēķini (MX) ir e-rēķinu izrakstīšanas līdzeklis, ko iestatīsit.</span><span class="sxs-lookup"><span data-stu-id="21184-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="21184-118">Importējiet e-rēķinu izrakstīšanas līdzekli</span><span class="sxs-lookup"><span data-stu-id="21184-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="21184-119">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="21184-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="21184-120">Darbvietā **Globalizācijas līdzekļi** sadaļā **Līdzekli** atlasiet elementu **e-rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="21184-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="21184-121">Lapā **E-rēķina līdzekļi** atlasiet **Importēt**, lai importētu līdzekli **CFDI rēķini (MX)** no Globālās krātuves.</span><span class="sxs-lookup"><span data-stu-id="21184-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21184-122">Ja sarakstā neredzat līdzekli, atlasiet **Sinhronizēt** un pēc tam atkārtojiet 3. darbību.</span><span class="sxs-lookup"><span data-stu-id="21184-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![CFDI rēķinu (MX) līdzekļa importēšana](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="21184-124">Importējot līdzekli **CFDI rēķins (MX)** no globālās krātuves, tiek importēti arī visi līdzekļa iestatījumi, tostarp konfigurācijas un darbības.</span><span class="sxs-lookup"><span data-stu-id="21184-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="21184-125">Izveidot jaunu CFDI rēķinu (MX) līdzekļa versiju</span><span class="sxs-lookup"><span data-stu-id="21184-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="21184-126">Varat izveidot jaunu versiju, ja, piemēram, ir jāatjaunina URL.</span><span class="sxs-lookup"><span data-stu-id="21184-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="21184-127">Plašāku informāciju skatiet [E-rēķinu izrakstīšanaa CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="21184-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="21184-128">Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="21184-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Jaunas e-rēķinu izrakstīšanas līdzekļa versijas pievienošana](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="21184-130">Atjaunināt konfigurācijas versiju</span><span class="sxs-lookup"><span data-stu-id="21184-130">Update the configuration version</span></span>

1. <span data-ttu-id="21184-131">Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Konfigurācijas** vai **Dzēst**, lai pārvaldītu konfigurāciju versijas (ER failu formātu konfigurācijas).</span><span class="sxs-lookup"><span data-stu-id="21184-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![E-rēķinu izrakstīšanas līdzekļa konfigurāciju pārvaldība](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="21184-133">Kad izveidojat jaunu versiju, visas konfigurācijas tiek pārmantotas no pēdējās publicētās versijas.</span><span class="sxs-lookup"><span data-stu-id="21184-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="21184-134">Lai apstrādātu CFDI rēķinus, ir nepieciešamas šādas konfigurācijas:</span><span class="sxs-lookup"><span data-stu-id="21184-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="21184-135">CFDI rēķins (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="21184-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="21184-136">CFDI atbilžu ziņojuma importēšana</span><span class="sxs-lookup"><span data-stu-id="21184-136">CFDI response message import</span></span>
    - <span data-ttu-id="21184-137">CFDI kļūdu žurnāla importēšana</span><span class="sxs-lookup"><span data-stu-id="21184-137">CFDI error log import</span></span>
    - <span data-ttu-id="21184-138">CFDI atcelšanas pieprasījums (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="21184-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="21184-139">CFDI rēķins (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="21184-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="21184-140">Sarakstā atlasiet konfigurācijas versiju un pēc tam atlasiet **Rediģēt** vai **Skatīt**, lai atvērtu lapu **Formāta veidotājs**, kurā var rediģēt vai skatīt konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="21184-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Formāta veidotāja lapas atvēršana](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="21184-142">Lai rediģētu un skatītu ER formāta failu konfigurācijas, izmantojiet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="21184-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="21184-143">Papildinformāciju skatiet tēmā [Elektronisko dokumentu konfigurāciju izveide](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="21184-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Formāta veidotāja lapa](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="21184-145">Pārvaldīt e-rēķinu izrakstīšanas līdzekļa iestatījumus</span><span class="sxs-lookup"><span data-stu-id="21184-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="21184-146">Lapas **E-rēķina līdzekļi** cilnē **Iestatījumi** atlasiet **Pievienot**, **Dzēst** vai **Rediģēt**, lai pārvaldītu e-rēķinu izrakstīšanas līdzekļa iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="21184-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![E-rēķinu izrakstīšanas līdzekļa iestatījumu pārvaldība](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="21184-148">Lai iesniegtu CFDI rēķinus autorizācijai (ģenerēt XML failu, iesniegt XML failu un apstrādāt atbildi), ir jānorāda līdzekļa **Pārdošanas rēķins** iestatījums.</span><span class="sxs-lookup"><span data-stu-id="21184-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="21184-149">Lai iesniegtu CFDI rēķina atcelšanu, ir jānorāda līdzekļu **Atcelšana** un **Atcelt** iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="21184-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="21184-150">Konfigurēt pārdošanas rēķina līdzekļu iestatījumu</span><span class="sxs-lookup"><span data-stu-id="21184-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="21184-151">Lapā **E-rēķina līdzekļi** cilnē **Iestatījumi** kolonnā **Līdzekļu iestatīšana** atlasiet **Pārdošanas rēķins**.</span><span class="sxs-lookup"><span data-stu-id="21184-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="21184-152">Atlasiet **Rediģēt**, lai konfigurētu darbības, piemērojamības nosacījumus un mainīgos.</span><span class="sxs-lookup"><span data-stu-id="21184-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![E-rēķinu izrakstīšanas līdzekļa iestatījumu rediģēšana](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="21184-154">Lapā **Līdzekļu versijas iestatīšana** atlasiet cilni **Darbības**, lai pārvaldītu darbību sarakstu.</span><span class="sxs-lookup"><span data-stu-id="21184-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="21184-155">Darbības definē oprerāciju sarakstu, kas ir jāpalaiž secīgi, lai veiktu notikuma pilnīgu izpildi.</span><span class="sxs-lookup"><span data-stu-id="21184-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Cilne Darbības](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="21184-157">Darbības ID</span><span class="sxs-lookup"><span data-stu-id="21184-157">Action ID</span></span> | <span data-ttu-id="21184-158">Darbība</span><span class="sxs-lookup"><span data-stu-id="21184-158">Action</span></span>                   | <span data-ttu-id="21184-159">Darbības nosaukums</span><span class="sxs-lookup"><span data-stu-id="21184-159">Action name</span></span>                                  | <span data-ttu-id="21184-160">Darbības apraksts</span><span class="sxs-lookup"><span data-stu-id="21184-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="21184-161">1</span><span class="sxs-lookup"><span data-stu-id="21184-161">1</span></span>         | <span data-ttu-id="21184-162">Transformējiet dokumentu</span><span class="sxs-lookup"><span data-stu-id="21184-162">Transform document</span></span>       | <span data-ttu-id="21184-163">Ģenerēt CFDI e-rēķinu bez ciparzīmes</span><span class="sxs-lookup"><span data-stu-id="21184-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="21184-164">Ģenerēt CFDI e-rēķinu.</span><span class="sxs-lookup"><span data-stu-id="21184-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="21184-165">2</span><span class="sxs-lookup"><span data-stu-id="21184-165">2</span></span>         | <span data-ttu-id="21184-166">Parakstīt dokumentu</span><span class="sxs-lookup"><span data-stu-id="21184-166">Sign document</span></span>            | <span data-ttu-id="21184-167">Ciparzīme</span><span class="sxs-lookup"><span data-stu-id="21184-167">Digital sign</span></span>                                 | <span data-ttu-id="21184-168">Elektroniski parakstīt e-rēķinu iesniegšanai.</span><span class="sxs-lookup"><span data-stu-id="21184-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="21184-169">3</span><span class="sxs-lookup"><span data-stu-id="21184-169">3</span></span>         | <span data-ttu-id="21184-170">Izsaukt Meksikas PAC pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="21184-170">Call Mexican PAC service</span></span> | <span data-ttu-id="21184-171">Iesniegt CFDI e-rēķinu</span><span class="sxs-lookup"><span data-stu-id="21184-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="21184-172">Windows Communication Foundation (WCF) klients iesniedz CFDI e-rēķinu.</span><span class="sxs-lookup"><span data-stu-id="21184-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="21184-173">4</span><span class="sxs-lookup"><span data-stu-id="21184-173">4</span></span>         | <span data-ttu-id="21184-174">Apstrādāt atbildi</span><span class="sxs-lookup"><span data-stu-id="21184-174">Process response</span></span>         | <span data-ttu-id="21184-175">Analizēt tīmekļa pakalpojuma atbildi</span><span class="sxs-lookup"><span data-stu-id="21184-175">Analyze web service response</span></span>                 | <span data-ttu-id="21184-176">Analizēt tīmekļa pakalpojuma atbildi un atgriezt kļūdu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="21184-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="21184-177">Iestatiet vietrādi URL Meksikas PAC tīmekļa pakalpojumiem</span><span class="sxs-lookup"><span data-stu-id="21184-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="21184-178">Lapā **Līdzekļu versijas iestatīšana** cilnē **Darbības** kopsavilkuma cilnē **Darbības** atlasiet **Izsaukt Meksikas PAC pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="21184-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="21184-179">Kopsavilkuma cilnē **Parametri** laukā **URL adrese** ievadiet vietrādi URL tīmekļa pakalpojuma CFDI rēķina iesniegšanai.</span><span class="sxs-lookup"><span data-stu-id="21184-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="21184-180">Izmantojiet tās pašas darbības, lai atjauninātu vietrādi URL darbībai **Izsaukt Meksikas PAC pakalpojumu** līdzekļu **Atcelt** un **Atcelšanas pieprasījums** iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="21184-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="21184-181">Piešķirt melnraksta versiju elektroniskajai rēķinu izrakstīšanas videi</span><span class="sxs-lookup"><span data-stu-id="21184-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="21184-182">Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Vides** atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="21184-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="21184-183">Laukā **Vide** atlasiet vidi.</span><span class="sxs-lookup"><span data-stu-id="21184-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="21184-184">Laukā **Spēkā no** atlasiet datumu, kad videi jāstājas spēkā.</span><span class="sxs-lookup"><span data-stu-id="21184-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="21184-185">Atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="21184-185">Select **Enable**.</span></span>

![E-rēķina vides iespējošana](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="21184-187">Mainiet versijas statusu uz Pabeigts</span><span class="sxs-lookup"><span data-stu-id="21184-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="21184-188">Lapas **E-rēķina līdzekļi** cilnē **Versijas** atlasiet e-rēķinu izrakstīšanas līdzekļa versiju ar statusu **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="21184-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="21184-189">Atlasiet **Mainīt statusu \> Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="21184-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="21184-190">Mainiet versijas statusu uz Publicēts</span><span class="sxs-lookup"><span data-stu-id="21184-190">Change the version status to Published</span></span>

- <span data-ttu-id="21184-191">Lapā **E-rēķina izrakstīšanas līdzekļi** cilnē **Versijas** atlasiet **Mainīt statusu \> Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="21184-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="21184-192">Publicējiet e-rēķinu izrakstīšanas līdzekli</span><span class="sxs-lookup"><span data-stu-id="21184-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="21184-193">Lapā **E-rēķina līdzekļi** atlasiet cilni **Versijas**, lai pārvaldītu līdzekļa **CFDI rēķini (MX)** statusu.</span><span class="sxs-lookup"><span data-stu-id="21184-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="21184-194">Atlasiet **Mainīt statusu**, lai mainītu līdzekļa statusu.</span><span class="sxs-lookup"><span data-stu-id="21184-194">Select **Change status** to change the status of the feature.</span></span>

![E-rēķinu izrakstīšanas līdzekļa statusa maiņa](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="21184-196">Iestatiet elektronisko rēķinu izrakstīšanas integrāciju programmā Finance</span><span class="sxs-lookup"><span data-stu-id="21184-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="21184-197">Lai iestatītu elektronisko rēķinu izrakstīšanas programmā Finance, tiks pabeigti šādi uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="21184-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="21184-198">Importējiet ER datu modeli, ER datu modeļa kartēšanu un formatus, kas ir nepieciešami CFDI rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="21184-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="21184-199">Konfigurējiet atbilžu veidus CFDI rēķinu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="21184-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="21184-200">Šie atbilžu veidi tiek izmantoti atbildei no autorizētā sertifikācijas sniedzēja (PAC) servera.</span><span class="sxs-lookup"><span data-stu-id="21184-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="21184-201">Importējiet ER datu modeli, ER datu modeļa kartēšanu un konteksta konfigurācijas CFDI rēķiniem</span><span class="sxs-lookup"><span data-stu-id="21184-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="21184-202">Pieteikšanās programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="21184-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="21184-203">Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet nosaukumu **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="21184-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="21184-204">Pārliecinieties, vai šis konfigurācijas nodrošinātājs ir iestatīts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="21184-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="21184-205">Papildinformāciju par to, ka iestatīt nodrošinātāju kā **Aktīvs** skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="21184-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="21184-206">Atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="21184-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="21184-207">Atlasiet **Globālais resurss \> Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="21184-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="21184-208">Importējiet **Rēķina modelis**, **Rēķina modeļa kartēšana**, **CFDI rēķina formāts (MX)**, **CFDI rēķina atcelšanas pieprasījuma formāts (MX)** un **CFDI rēķina atcelšanas formāts (MX)**.</span><span class="sxs-lookup"><span data-stu-id="21184-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="21184-209">Ieslēdziet līdzekli CFDI rēķinu apstrādei</span><span class="sxs-lookup"><span data-stu-id="21184-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="21184-210">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="21184-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="21184-211">Cilnē **Līdzekļi** atzīmējiet izvēles rūtiņu **Iespējot**, kas atrodas līdzekļu reksturojumu rindās **MX-00010** un **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="21184-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![CFDI rēķinu apstrādes līdzekļu ieslēgšana](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="21184-213">Importējiet ER konfigurācijas un iestatiet atbilžu veidus CFDI rēķinu grāmatošanai</span><span class="sxs-lookup"><span data-stu-id="21184-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="21184-214">ER konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="21184-214">Import ER configurations</span></span>

1. <span data-ttu-id="21184-215">Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Konfigurācijas nodrošinātāji** atlasiet nosaukumu **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="21184-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="21184-216">Atlasiet **Repozitoriji**.</span><span class="sxs-lookup"><span data-stu-id="21184-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="21184-217">Atlasiet **Globālais resurss \> Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="21184-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="21184-218">Importējiet **Atbildes ziņojuma modelis**, **CFDI kļūdu žurnāla importēšana (MX)** un **CFDI atbildes ziņojuma importēšana (MX)**.</span><span class="sxs-lookup"><span data-stu-id="21184-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="21184-219">Atbildes veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="21184-219">Set up the response types</span></span>

1. <span data-ttu-id="21184-220">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="21184-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="21184-221">Cilnē **Elektronisks dokuments** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="21184-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="21184-222">Ievadiet debitora rēķinu žurnālu un pēc tam laukā **Tabulas nosaukums** atlasiet projekta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="21184-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="21184-223">Katrai tabulai definējiet saistīto dokumentu kontekstu:</span><span class="sxs-lookup"><span data-stu-id="21184-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="21184-224">Tabulai **Debitoru rēķinu žurnāls** ievadiet **Debitora rēķina konteksts**.</span><span class="sxs-lookup"><span data-stu-id="21184-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="21184-225">Tabulai **Projekta rēķins** ievadiet **Projekta rēķina konteksts**.</span><span class="sxs-lookup"><span data-stu-id="21184-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="21184-226">Atlasiet **Atbilžu veidi**, lai konfigurētu atbilžu veidus, kas var tikt atgriezti no elektronisko rēķinu izrakstīšanas un iekļauta debitoru rēķinu žurnālā vai projekta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="21184-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="21184-227">Atlasiet **Jauns** un pēc tam laukā **Atbilžu veids** atlasiet **Atbilde**.</span><span class="sxs-lookup"><span data-stu-id="21184-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="21184-228">Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.</span><span class="sxs-lookup"><span data-stu-id="21184-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="21184-229">Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojuma importēšanas formāts — Modeļa kartēšana no atbildes ziņojuma**.</span><span class="sxs-lookup"><span data-stu-id="21184-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="21184-230">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="21184-230">Select **Save**.</span></span>
9. <span data-ttu-id="21184-231">Atlasiet **Jauns** un pēc tam laukā **Atbilžu veids** atlasiet **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="21184-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="21184-232">Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.</span><span class="sxs-lookup"><span data-stu-id="21184-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="21184-233">Laukā **Modeļa kartēšana** atlasiet **CFDI atbildes datu importēšanas formāts (detaļas) — Atbildes datu importēšana**.</span><span class="sxs-lookup"><span data-stu-id="21184-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="21184-234">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="21184-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="21184-235">Apstrādāt elektroniskos rēķinus programmā Finance</span><span class="sxs-lookup"><span data-stu-id="21184-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="21184-236">CFDI rēķinu apstrādes laikā programmā Finance, izmantojot elektronisko rēķinu izrakstīšanu, varat veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="21184-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="21184-237">Iesniegt CFDI rēķinus.</span><span class="sxs-lookup"><span data-stu-id="21184-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="21184-238">Skatiet iesniegšanas izpildes žurnālus.</span><span class="sxs-lookup"><span data-stu-id="21184-238">View the submission execution logs.</span></span>
- <span data-ttu-id="21184-239">Iesniedziet CFDI rēķina atcelšanu.</span><span class="sxs-lookup"><span data-stu-id="21184-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="21184-240">Iesniegt CFDI rēķinus</span><span class="sxs-lookup"><span data-stu-id="21184-240">Submit CFDI invoices</span></span>

<span data-ttu-id="21184-241">Pēc tam, kad ieslēdzat līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana**, vairs nevarēsiet izmantot procesu **Elektronisko rēķinu eksportēšana/importēšana** (**Realizācija \> Rēķini \> E-rēķini**), lai iesniegtu CFDI rēķinus.</span><span class="sxs-lookup"><span data-stu-id="21184-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="21184-242">Tas ir aizstāts ar jaunu procesu, kura nosaukums ir **Iesniegt elektroniskus dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="21184-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="21184-243">Pirms izmantojat jauno procesu **Iesniegt elektroniskos dokumentus**, pārbaudiet, vai Meksikas e-rēķiniem nepieciešamais iestatījums ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="21184-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="21184-244">Plašāku informāciju skatiet [CFDI izkārtojuma versija 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="21184-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="21184-245">Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Iesniegt elektroniskus dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="21184-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="21184-246">Pirmā dokumenta iesniegšanai vienmēr iestatiet opciju **Atkārtoti iesniegt dokumentus** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="21184-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="21184-247">Ja ir atkārtoti jāiesniedz dokuments, izmantojot pakalpojumu, iestatiet šo opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="21184-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="21184-248">Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrs**, lai atvērtu dialoglodziņu **Pieprasījums**, kur var izveidot vaicājumu, lai atlasītu dokumentus iesniegšanai.</span><span class="sxs-lookup"><span data-stu-id="21184-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![CFDI dokumenta iesniegšana](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="21184-250">Pirmajā mēģinājumā iesniegt dokumentu, izmantojot pakalpojumu, jums tiks piedāvāts apstiprināt savienojumu ar elektronisko rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="21184-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="21184-251">Atlasiet **Noklikšķiniet šeit, lai izveidotu savienojumu ar elektronisko dokumentu iesniegšanas pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="21184-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="21184-252">Skatīt iesniegšanas žurnālus</span><span class="sxs-lookup"><span data-stu-id="21184-252">View submission logs</span></span>

<span data-ttu-id="21184-253">Var apskatīt visu iesniegto dokumentu vai tikai viena iesniegtā dokumenta iesniegšanas žurnālus.</span><span class="sxs-lookup"><span data-stu-id="21184-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="21184-254">Skatīt visus iesniegšanas žurnālus</span><span class="sxs-lookup"><span data-stu-id="21184-254">View all submission logs</span></span>

<span data-ttu-id="21184-255">Pēc tam, kad esat ieslēdzis līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana**, ir pieejama jauna lapa, kas ļauj sekot līdzi dokumentu iesniegšanas procesam.</span><span class="sxs-lookup"><span data-stu-id="21184-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="21184-256">Varat izmantot šo lapu, lai skatītu visu iesniegto dokumentu iesniegšanas žurnālus.</span><span class="sxs-lookup"><span data-stu-id="21184-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="21184-257">Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="21184-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="21184-258">Laukā **Dokumenta veids** atlasiet **Debitora rēķina žurnāls**, lai filtrētu pieprasītos elektroniskos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="21184-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Dokumenta veida atlasīšana, lai apskatītu iesniegšanas žurnālus](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="21184-260">Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="21184-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="21184-262">Informācija iesniegšanas žurnālos tiek sadalīta starp trim kopsavilkuma cilnēm:</span><span class="sxs-lookup"><span data-stu-id="21184-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="21184-263">**Apstrādes darbības** – Šī kopsavilkuma cilne rāda izpildes žurnālu darbības, kas konfigurētas līdzekļa versijā, kas tika iestatīta RCS.</span><span class="sxs-lookup"><span data-stu-id="21184-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="21184-264">Kolonna **Statuss** rāda, vai darbība ir veiksmīgi izpildīta.</span><span class="sxs-lookup"><span data-stu-id="21184-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="21184-265">**Darbības faili** – Šī kopsavilkuma cilne rāda starpposma failus, kas tika ģenerēti darbību izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="21184-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="21184-266">Varat atlasīt **Skatīt** lai lejupielādētu un skatītu failu.</span><span class="sxs-lookup"><span data-stu-id="21184-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="21184-267">**Apstrādes darbību žurnāls** – Šajā kopsavilkuma cilnē tiek rādīti saziņas rezultāti starp elektronisko rēķinu izrakstīšanu un mērķa tīmekļa pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="21184-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="21184-268">Tas arī parāda, ko atgrieza apstrāde no tīmekļa pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="21184-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="21184-269">Kolonnā **Kļūdas kods** ir parādīts atgrieztais kods, ko atgrieza autorizācijas tīmekļa pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="21184-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="21184-270">Kad iesniegtais CFDI rēķins ir autorizēts, tā statuss tiek atjaunināts uz **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="21184-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="21184-271">Skatīt iesniegumu žurnālus no CFDI rēķiniem</span><span class="sxs-lookup"><span data-stu-id="21184-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="21184-272">Pēc tam, kad esat ieslēdzis līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana**, varat arī skatīt iesniegumu žurnālus no CFDI rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="21184-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="21184-273">Dodieties uz **Debitoru parādi \> Uzziņas un atskaites \> CFDI (elektroniskie rēķini)**.</span><span class="sxs-lookup"><span data-stu-id="21184-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="21184-274">Atlasiet CFDI rēķinu, kas tika iesniegts pēc tam, kad līdzeklis **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana** tika ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="21184-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="21184-275">Darbības rūtī, kas atrodas cilnē **Vēsture**, atlasiet **Elektronisko dokumentu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="21184-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Iesniegšanas žurnālu apskate no CFDI rēķiniem](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="21184-277">CFDI rēķiniem, kas tika iesniegti pirms līdzekļa **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana** ieslēgšanas, ir pieejama poga **Vēsture**.</span><span class="sxs-lookup"><span data-stu-id="21184-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="21184-278">Poga **Vēsture** nav pieejama CFDI rēķiniem, kas tika iesniegti pēc līdzekļa **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana** ieslēgšanas.</span><span class="sxs-lookup"><span data-stu-id="21184-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="21184-279">Iesniedziet CFDI rēķinu atcelšanu</span><span class="sxs-lookup"><span data-stu-id="21184-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="21184-280">Pēc tam, kad ieslēdzat līdzekli **Konfigurējamās Elektronisko rēķinu izrakstīšanas integrēšana**, vairs nevarēsiet izmantot veco procesu, lai atceltu CFDI rēķinus.</span><span class="sxs-lookup"><span data-stu-id="21184-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="21184-281">Tas ir aizstāts ar jaunu atcelšanas procesu, kas ir iegults lapā **Elektronisko dokumentu iesniegšanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="21184-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="21184-282">Dodieties uz **Debitoru parādi \> Uzziņas un atskaites \> CFDI (elektroniskie rēķini)**.</span><span class="sxs-lookup"><span data-stu-id="21184-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="21184-283">Ja CFDI rēķina statuss ir **Apstiprināts**, atlasiet **Funkcijas \> Atcelt CFDI**.</span><span class="sxs-lookup"><span data-stu-id="21184-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="21184-284">Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="21184-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="21184-285">Atlasiet CFDI rēķinu un pēc tam atlasiet **Funkcijas \> Sūtīt saistītos iesniegumus**.</span><span class="sxs-lookup"><span data-stu-id="21184-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="21184-286">Ievadiet saistītā iesnieguma aprakstu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="21184-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="21184-287">Skatīt atcelšanas iesniegšanas žurnālus</span><span class="sxs-lookup"><span data-stu-id="21184-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="21184-288">Dodieties uz **Organizācijas administrēšana \> Periodiskais \> Elektroniskie dokumenti \> Elektronisko dokumentu iesniegšanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="21184-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="21184-289">Laukā **Dokumenta veids** atlasiet **Debitora rēķina žurnāls**, lai filtrētu tikai debitoru rēķinu žurnāla dokumentus.</span><span class="sxs-lookup"><span data-stu-id="21184-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="21184-290">Atlasiet CFDI rīķinu un pēc tam Darbību rūtī atlasiet **Vaicājumi \> Saistītie iesniegumi**.</span><span class="sxs-lookup"><span data-stu-id="21184-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="21184-291">Lapa **Saistītais iesniegums** parāda visus saistītos iesniegumus un to iesniegšanas statusu dotajam CFDI rīķinam.</span><span class="sxs-lookup"><span data-stu-id="21184-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="21184-292">Sekojošajā ilustrācijā pirmā rinda ataino iesniegumu, kas pieprasīja CFDI rīķina apstiprināšanu.</span><span class="sxs-lookup"><span data-stu-id="21184-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="21184-293">Otrā rinda ataino iesniegumu, kas atcēla šo CFDI rīķinu.</span><span class="sxs-lookup"><span data-stu-id="21184-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Atcelšanas iesniegšanas žurnālu apskate](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="21184-295">Darbības rūtī atlasiet **Vaicājumi \> Iesniegšanas detaļas**, lai skatītu detalizētu informāciju par iesniegšanas izpildes žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="21184-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Atcelšanas iesniegšanas žurnāla informācijas skatīšana](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="21184-297">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="21184-297">Privacy notice</span></span>
<span data-ttu-id="21184-298">Iespējojot līdzekli **CFDI Meksikas elektroniskais rēķins (MX)**, var būt nepieciešams nosūtīt ierobežotus datus, kas ietver organizācijas nodokļa reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="21184-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="21184-299">Tas tiks nosūtīts trešo personu aģentūrām, ko pilnvarojusi nodokļu iestāde, lai nosūtītu elektroniskos rēķinus šai nodokļu iestādei iepriekš noteiktā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="21184-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="21184-300">Administrators var iespējot un atspējot līdzekli **CFDI Meksikas elektroniskais rēķins (MX)**, pārvietojoties uz **Organizācijas administrēšana \> Iestatījumi \> Elektroniskā dokumenta parametri**.</span><span class="sxs-lookup"><span data-stu-id="21184-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="21184-301">Cilnē **Līdzekļi** atlasiet rindas, kas ietver **CFDI Meksikas elektroniskā rēķina (MX)** līdzekli, un pēc tam veiciet attiecīgo atlasi.</span><span class="sxs-lookup"><span data-stu-id="21184-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="21184-302">No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="21184-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="21184-303">Lai iegūtu plašāku informāciju, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.</span><span class="sxs-lookup"><span data-stu-id="21184-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21184-304">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="21184-304">Additional resources</span></span>

- [<span data-ttu-id="21184-305">Elektroniskās rēķinu izveides pārskats</span><span class="sxs-lookup"><span data-stu-id="21184-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="21184-306">Darba sākšana ar elektroniskās rēķinu izveidi</span><span class="sxs-lookup"><span data-stu-id="21184-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="21184-307">Elektronisko rēķinu izrakstīšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="21184-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
