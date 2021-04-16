---
title: Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi
description: Šajā tēmā paskaidrots, kā konfigurēt neobligātos līdzekļus Microsoft Dynamics 365 Commerce novērtējuma videi.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795911"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="cfdac-103">Izvēles līdzekļu konfigurēšana Dynamics 365 Commerce novērtēšanas videi</span><span class="sxs-lookup"><span data-stu-id="cfdac-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cfdac-104">Šajā tēmā paskaidrots, kā konfigurēt neobligātos līdzekļus Microsoft Dynamics 365 Commerce novērtējuma videi.</span><span class="sxs-lookup"><span data-stu-id="cfdac-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cfdac-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="cfdac-105">Prerequisites</span></span>

<span data-ttu-id="cfdac-106">Ja vēlaties novērtēt transakciju e-pasta līdzekļus, ir jāizpilda tālāk minētie priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="cfdac-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="cfdac-107">Jums ir pieejams e-pasta serveris (vienkāršā pasta pārsūtīšanas protokola \[SMTP\] serveris), kuru var izmantot no Microsoft Azure abonementa, kurā tika nodrošināta novērtējuma vide.</span><span class="sxs-lookup"><span data-stu-id="cfdac-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="cfdac-108">Jums ir pieejams pilnībā kvalificēts servera domēna nosaukums (FQDN)/IP adrese, SMTP porta numurs un autentifikācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="cfdac-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="cfdac-109">Attēla aizmugures konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cfdac-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="cfdac-110">Savas multivides bāzes URL atrašana</span><span class="sxs-lookup"><span data-stu-id="cfdac-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="cfdac-111">Lai varētu pabeigt šo procedūru, jums ir jāizpilda darbības, kas norādītas sadaļā [Savas vietnes iestatīšana pakalpojumā Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="cfdac-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="cfdac-112">Piesakieties Commerce vietņu veidotājā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-komerciju (skatiet [e-komercijas inicializēšana](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="cfdac-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="cfdac-113">Atveriet vietni **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="cfdac-114">Kreisās puses izvēlnē atlasiet **Multivides bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="cfdac-115">Atlasiet jebkuru atsevišķu attēla līdzekli.</span><span class="sxs-lookup"><span data-stu-id="cfdac-115">Select any single image asset.</span></span>
1. <span data-ttu-id="cfdac-116">Rekvizītu inspektors labajā pusē atrodiet rekvizītu **Publiskais URL**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="cfdac-117">Vērtība ir vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="cfdac-117">The value is a URL.</span></span> <span data-ttu-id="cfdac-118">Tas ir piemērs:</span><span class="sxs-lookup"><span data-stu-id="cfdac-118">Here is an example:</span></span>

    <span data-ttu-id="cfdac-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="cfdac-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="cfdac-120">Aizstājiet URL pēdējo identifikatoru (augstākminētajā URL piemērā —**MA1nQC** ) ar virkni **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="cfdac-121">Tālāk parādīts, kā izskatās URL piemērs, kad šīs izmaiņas ir veiktas.</span><span class="sxs-lookup"><span data-stu-id="cfdac-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="cfdac-122">Šis vietrādis URL ir jūsu multivides bāzes vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="cfdac-122">This URL is your media base URL.</span></span> <span data-ttu-id="cfdac-123">Pierakstiet to.</span><span class="sxs-lookup"><span data-stu-id="cfdac-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="cfdac-124">Multivides bāzes URL atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="cfdac-124">Update the media base URL</span></span>

1. <span data-ttu-id="cfdac-125">Pieteikšanās Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cfdac-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="cfdac-126">Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Kanālu iestatīšana \> Kanālu profili**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="cfdac-127">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-127">Select **Edit**.</span></span>
1. <span data-ttu-id="cfdac-128">Sadaļā **Profila rekvizīti** aizstājiet rekvizīta **Multivides servera bāzes URL** vērtību ar iepriekš izveidoto multivides bāzes URL.</span><span class="sxs-lookup"><span data-stu-id="cfdac-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="cfdac-129">Atlasiet kanālu ar nosaukumu **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="cfdac-130">Sadaļā **Profila rekvizīti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="cfdac-131">Rekvizītam, kas tika pievienots, atlasiet **Multivides servera bāzes URL** kā rekvizīta atslēgu.</span><span class="sxs-lookup"><span data-stu-id="cfdac-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="cfdac-132">Kā rekvizīta vērtību ievadiet iepriekš izveidoto multivides bāzes vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="cfdac-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="cfdac-133">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="cfdac-134">E-pasta servera konfigurācija un testēšana</span><span class="sxs-lookup"><span data-stu-id="cfdac-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="cfdac-135">Šeit ievadītajam SMTP serverim vai e-pasta pakalpojumam jābūt pieejamam no Azure abonementa, kuru izmantojat videi.</span><span class="sxs-lookup"><span data-stu-id="cfdac-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="cfdac-136">Pieteikšanās Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cfdac-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="cfdac-137">Izmantojiet izvēlni kreisajā pusē, lai dotos uz **Moduļi \> Retail un Commerce \> Headquarters iestatīšana \> Parametri \> E-pasta parametri**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="cfdac-138">Cilnes **SMTP iestatījumi** laukā **Izejošā pasta serveris** ievadiet SMTP servera vai e-pasta pakalpojuma FQDN vai IP adresi.</span><span class="sxs-lookup"><span data-stu-id="cfdac-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="cfdac-139">Laukā **SMTP porta numurs** ievadiet porta numuru.</span><span class="sxs-lookup"><span data-stu-id="cfdac-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="cfdac-140">(Ja neizmantojat drošligzdu slāņa \[SSL\], noklusējuma porta numurs ir **25**.)</span><span class="sxs-lookup"><span data-stu-id="cfdac-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="cfdac-141">Ja autentifikācija ir nepieciešama, ievadiet vērtības laukos **Lietotājvārds** un **Parole**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="cfdac-142">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-142">Select **Save**.</span></span>
1. <span data-ttu-id="cfdac-143">Atlasiet **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="cfdac-144">Cilnes **Testa e-pasts** laukā **E-pasta pakalpojumu sniedzējs** atlasiet **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="cfdac-145">Laukā **Nosūtīt uz** ievadiet e-pasta adresi, uz kuru jāpiegādā testa e-pasts.</span><span class="sxs-lookup"><span data-stu-id="cfdac-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="cfdac-146">Atlasiet **Sūtīt e-pasta ziņojumu.**</span><span class="sxs-lookup"><span data-stu-id="cfdac-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="cfdac-147">E-pasta veidņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cfdac-147">Configure email templates</span></span>

<span data-ttu-id="cfdac-148">Katram darījuma notikumam, kuram vēlaties sūtīt e-pasta ziņojumus, jums ir jāatjaunina e-pasta veidne ar derīgu sūtītāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="cfdac-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="cfdac-149">Pieteikšanās Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cfdac-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="cfdac-150">Izmantojiet izvēlni kreisajā pusē, lai dotos uz **Moduļi \> Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="cfdac-151">Atlasiet **Rādīt sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-151">Select **Show list**.</span></span>
1. <span data-ttu-id="cfdac-152">Katrai veidnei sarakstā izpildiet tālākās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="cfdac-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="cfdac-153">Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="cfdac-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="cfdac-154">Neobligāti: laukā **Sūtītāja vārds** ievadiet nosaukumu, kas jāizmanto kā sūtītāja vārds.</span><span class="sxs-lookup"><span data-stu-id="cfdac-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="cfdac-155">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="cfdac-156">E-pasta veidņu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="cfdac-156">Customize email templates</span></span>

<span data-ttu-id="cfdac-157">Iespējams, vēlēsieties pielāgot e-pasta veidnes, lai tās izmantotu dažādus attēlus.</span><span class="sxs-lookup"><span data-stu-id="cfdac-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="cfdac-158">Varat arī atjaunināt veidņu saites, lai tās pārvietotu uz novērtējuma vidi.</span><span class="sxs-lookup"><span data-stu-id="cfdac-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="cfdac-159">Šī procedūra izskaidro, kā lejupielādēt noklusējuma veidnes, pielāgot tās un atjaunināt veidnes sistēmā.</span><span class="sxs-lookup"><span data-stu-id="cfdac-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="cfdac-160">Tīmekļa pārlūkā lejupielādējiet [Microsoft Dynamics 365 Commerce novērtējuma noklusējuma e-pasta veidņu ZIP failu](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) savā lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="cfdac-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="cfdac-161">Šajā failā ir ietverti tālāk norādītie HTML dokumenti.</span><span class="sxs-lookup"><span data-stu-id="cfdac-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="cfdac-162">Pasūtījuma apstiprinājuma veidne</span><span class="sxs-lookup"><span data-stu-id="cfdac-162">Order confirmation template</span></span>
    - <span data-ttu-id="cfdac-163">Dāvanu kartes izsniegšanas veidne</span><span class="sxs-lookup"><span data-stu-id="cfdac-163">Issue gift card template</span></span>
    - <span data-ttu-id="cfdac-164">Jauna pasūtījuma veidne</span><span class="sxs-lookup"><span data-stu-id="cfdac-164">New order template</span></span>
    - <span data-ttu-id="cfdac-165">Pasūtījuma iesaiņošanas veidne</span><span class="sxs-lookup"><span data-stu-id="cfdac-165">Pack order template</span></span>
    - <span data-ttu-id="cfdac-166">Pasūtījuma saņemšanas veidne</span><span class="sxs-lookup"><span data-stu-id="cfdac-166">Pick order template</span></span>

1. <span data-ttu-id="cfdac-167">Pielāgojiet veidnes, izmantojot teksta vai HTML redaktoru.</span><span class="sxs-lookup"><span data-stu-id="cfdac-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="cfdac-168">Skatiet tālāk šajā tēmā [atbalstīto marķieru](#supported-tokens-in-the-email-template) sarakstu.</span><span class="sxs-lookup"><span data-stu-id="cfdac-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="cfdac-169">Pieteikšanās Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfdac-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="cfdac-170">Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Organizācijas administrācija \> Iestatījumi \> Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="cfdac-171">Paplašiniet sarakstu kreisajā pusē, lai redzētu visas veidnes.</span><span class="sxs-lookup"><span data-stu-id="cfdac-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="cfdac-172">Attiecībā uz katru veidni, kuru vēlaties pielāgot, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="cfdac-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="cfdac-173">Atlasiet sarakstā veidni.</span><span class="sxs-lookup"><span data-stu-id="cfdac-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="cfdac-174">Sadaļā **E-pasta ziņojuma saturs** no saraksta atlasiet atbilstošo valodas versiju.</span><span class="sxs-lookup"><span data-stu-id="cfdac-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="cfdac-175">(Noklusējuma valoda ir **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="cfdac-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="cfdac-176">Sadaļā **E-pasta** ziņojuma saturs atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="cfdac-177">Tiek parādīta rūts **Augšupielādēt e-pasta veidni**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="cfdac-178">Atlasiet **Pārlūkot** un atrodiet HTML failu, kurā ir pielāgots saturs.</span><span class="sxs-lookup"><span data-stu-id="cfdac-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="cfdac-179">Atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-179">Select **Upload**.</span></span> <span data-ttu-id="cfdac-180">Veidne tiek augšupielādēta sistēmā, un tiek parādīts priekšskatījums.</span><span class="sxs-lookup"><span data-stu-id="cfdac-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="cfdac-181">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-181">Select **OK**.</span></span>
    1. <span data-ttu-id="cfdac-182">Pēc izvēles: pielāgojiet veidnes rekvizītu **Temats**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="cfdac-183">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cfdac-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="cfdac-184">E-pasta veidnē atbalstītie marķieri</span><span class="sxs-lookup"><span data-stu-id="cfdac-184">Supported tokens in the email template</span></span>

<span data-ttu-id="cfdac-185">Kad e-pasts tiek atveidots, šie marķieri tiek aizstāti ar faktiskajām vērtībām, kas attiecas uz klientu un klienta pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cfdac-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="cfdac-186">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="cfdac-186">Sales order</span></span>

<span data-ttu-id="cfdac-187">Tālāk minētie marķieri attiecas uz vispārēju pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cfdac-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="cfdac-188">Marķējuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="cfdac-188">Name of the token</span></span> | <span data-ttu-id="cfdac-189">Marķieris</span><span class="sxs-lookup"><span data-stu-id="cfdac-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="cfdac-190">Pasūtījuma numurs</span><span class="sxs-lookup"><span data-stu-id="cfdac-190">Order number</span></span>      | <span data-ttu-id="cfdac-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="cfdac-191">%salesid%</span></span> |
| <span data-ttu-id="cfdac-192">Klienta vārds/nosaukums</span><span class="sxs-lookup"><span data-stu-id="cfdac-192">Customer's name</span></span>   | <span data-ttu-id="cfdac-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="cfdac-193">%customername%</span></span> |
| <span data-ttu-id="cfdac-194">Piegādes adrese</span><span class="sxs-lookup"><span data-stu-id="cfdac-194">Delivery address</span></span>  | <span data-ttu-id="cfdac-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="cfdac-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="cfdac-196">Norēķinu adrese</span><span class="sxs-lookup"><span data-stu-id="cfdac-196">Billing address</span></span>   | <span data-ttu-id="cfdac-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="cfdac-197">%customeraddress%</span></span> |
| <span data-ttu-id="cfdac-198">Ordera datums</span><span class="sxs-lookup"><span data-stu-id="cfdac-198">Order date</span></span>        | <span data-ttu-id="cfdac-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="cfdac-199">%shipdate%</span></span> |
| <span data-ttu-id="cfdac-200">Piegādes veids</span><span class="sxs-lookup"><span data-stu-id="cfdac-200">Delivery mode</span></span>     | <span data-ttu-id="cfdac-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="cfdac-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="cfdac-202">Atlaide</span><span class="sxs-lookup"><span data-stu-id="cfdac-202">Discount</span></span>          | <span data-ttu-id="cfdac-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="cfdac-203">%discount%</span></span> |
| <span data-ttu-id="cfdac-204">PVN</span><span class="sxs-lookup"><span data-stu-id="cfdac-204">Sales tax</span></span>         | <span data-ttu-id="cfdac-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="cfdac-205">%tax%</span></span> |
| <span data-ttu-id="cfdac-206">Pasūtījuma kopsumma</span><span class="sxs-lookup"><span data-stu-id="cfdac-206">Order total</span></span>       | <span data-ttu-id="cfdac-207">%total%</span><span class="sxs-lookup"><span data-stu-id="cfdac-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="cfdac-208">Pārdošanas rinda</span><span class="sxs-lookup"><span data-stu-id="cfdac-208">Sales line</span></span>

<span data-ttu-id="cfdac-209">Tālāk esošie marķieri tiek aizstāti ar vērtībām katram produktam pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="cfdac-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="cfdac-210">Ievietojiet marķieri **Preču saraksts — sākums** HTML bloka sākumā, kas atkārtojas katram produktam, un marķieri **Preču saraksts — beigas** bloka beigās.</span><span class="sxs-lookup"><span data-stu-id="cfdac-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="cfdac-211">Marķējuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="cfdac-211">Name of the token</span></span>      | <span data-ttu-id="cfdac-212">Marķieris</span><span class="sxs-lookup"><span data-stu-id="cfdac-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="cfdac-213">Preču saraksts — sākums</span><span class="sxs-lookup"><span data-stu-id="cfdac-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="cfdac-214">Preču saraksts — beigas</span><span class="sxs-lookup"><span data-stu-id="cfdac-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="cfdac-215">Preces nosaukums</span><span class="sxs-lookup"><span data-stu-id="cfdac-215">Product name</span></span>           | <span data-ttu-id="cfdac-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="cfdac-216">%lineproductname%</span></span> |
| <span data-ttu-id="cfdac-217">Apraksts</span><span class="sxs-lookup"><span data-stu-id="cfdac-217">Description</span></span>            | <span data-ttu-id="cfdac-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="cfdac-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="cfdac-219">Daudzums</span><span class="sxs-lookup"><span data-stu-id="cfdac-219">Quantity</span></span>               | <span data-ttu-id="cfdac-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="cfdac-220">%linequantity%</span></span> |
| <span data-ttu-id="cfdac-221">Rindas vienības cena</span><span class="sxs-lookup"><span data-stu-id="cfdac-221">Line unit price</span></span>        | <span data-ttu-id="cfdac-222">%lineprice% (pārbaudīt)</span><span class="sxs-lookup"><span data-stu-id="cfdac-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="cfdac-223">rindas preču kopsumma</span><span class="sxs-lookup"><span data-stu-id="cfdac-223">line item total</span></span>        | <span data-ttu-id="cfdac-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="cfdac-224">%linenetamount%</span></span> |
| <span data-ttu-id="cfdac-225">rindas atlaide</span><span class="sxs-lookup"><span data-stu-id="cfdac-225">line discount</span></span>          | <span data-ttu-id="cfdac-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="cfdac-226">%linediscount%</span></span> |
| <span data-ttu-id="cfdac-227">Nosūtīšanas datums</span><span class="sxs-lookup"><span data-stu-id="cfdac-227">Ship date</span></span>              | <span data-ttu-id="cfdac-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="cfdac-228">%lineshipdate%</span></span> |
| <span data-ttu-id="cfdac-229">Iepirkuma metode</span><span class="sxs-lookup"><span data-stu-id="cfdac-229">Procurement method</span></span>     | <span data-ttu-id="cfdac-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="cfdac-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="cfdac-231">piegādes adrese</span><span class="sxs-lookup"><span data-stu-id="cfdac-231">delivery address</span></span>       | <span data-ttu-id="cfdac-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="cfdac-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="cfdac-233">Rindas pārdošanas vienība</span><span class="sxs-lookup"><span data-stu-id="cfdac-233">Sales unit of the line</span></span> | <span data-ttu-id="cfdac-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="cfdac-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="cfdac-235">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cfdac-235">Additional resources</span></span>

[<span data-ttu-id="cfdac-236">Dynamics 365 Commerce novērtējuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="cfdac-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="cfdac-237">Nodrošināt Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="cfdac-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="cfdac-238">Konfigurēt Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="cfdac-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="cfdac-239">BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="cfdac-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="cfdac-240">Dynamics 365 Commerce novērtējuma vide - bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="cfdac-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="cfdac-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="cfdac-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="cfdac-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="cfdac-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="cfdac-243">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="cfdac-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="cfdac-244">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="cfdac-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]