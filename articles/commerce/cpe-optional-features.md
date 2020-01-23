---
title: Izvēles funkciju konfigurēšana Commerce priekšskatījuma videi
description: Šajā tēmā ir paskaidrots, kā konfigurēt izvēles funkcijas Microsoft Dynamics 365 Commerce priekšskatījuma videi.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906120"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a><span data-ttu-id="cc0b0-103">Izvēles funkciju konfigurēšana Commerce priekšskatījuma videi</span><span class="sxs-lookup"><span data-stu-id="cc0b0-103">Configure optional features for a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cc0b0-104">Šajā tēmā ir paskaidrots, kā konfigurēt izvēles funkcijas Microsoft Dynamics 365 Commerce priekšskatījuma videi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cc0b0-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="cc0b0-105">Prerequisites</span></span>

<span data-ttu-id="cc0b0-106">Ja vēlaties novērtēt transakciju e-pasta līdzekļus, ir jāizpilda tālāk minētie priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="cc0b0-107">Jums ir pieejams e-pasta serveris (vienkāršā pasta pārsūtīšanas protokola \[SMTP\] serveris), kuru var izmantot no Microsoft Azure abonementa, kur nodrošināt priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="cc0b0-108">Jums ir pieejams pilnībā kvalificēts servera domēna nosaukums (FQDN)/IP adrese, SMTP porta numurs un autentifikācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="cc0b0-109">Ja vēlaties novērtēt digitālās līdzekļu pārvaldības funkcijas, uzņemot jaunus visu kanālu attēlus, jums ir jābūt pieejamam satura pārvaldības sistēmas (CMS) nomnieka nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="cc0b0-110">Tālāk šajā tēmā sniegti norādījumi, kā atrast šo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="cc0b0-111">>>>(J: kur ir norādījumi?)</span><span class="sxs-lookup"><span data-stu-id="cc0b0-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="cc0b0-112">Attēla aizmugures konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="cc0b0-113">Savas multivides bāzes URL atrašana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="cc0b0-114">Lai varētu pabeigt šo procedūru, jums ir jāizpilda darbības, kas norādītas sadaļā [Savas vietnes iestatīšana pakalpojumā Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="cc0b0-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="cc0b0-115">Piesakieties Commerce vietnes pārvaldības rīkā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-Commerce (skatiet [e-Commerce inicializēšana](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="cc0b0-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="cc0b0-116">Atveriet vietni **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="cc0b0-117">Kreisās puses izvēlnē atlasiet **Līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="cc0b0-118">Atlasiet jebkuru atsevišķu attēla līdzekli.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-118">Select any single image asset.</span></span>
1. <span data-ttu-id="cc0b0-119">Rekvizītu inspektors labajā pusē atrodiet rekvizītu **Publiskais URL**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="cc0b0-120">Vērtība ir vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-120">The value is a URL.</span></span> <span data-ttu-id="cc0b0-121">Tas ir piemērs:</span><span class="sxs-lookup"><span data-stu-id="cc0b0-121">Here is an example:</span></span>

    <span data-ttu-id="cc0b0-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="cc0b0-123">Aizstājiet URL pēdējo identifikatoru (augstākminētajā URL piemērā —**MA1nQC**) ar virkni **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="cc0b0-124">Tālāk parādīts, kā izskatās URL piemērs, kad šīs izmaiņas ir veiktas.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="cc0b0-125">Šis vietrādis URL ir jūsu multivides bāzes vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-125">This URL is your media base URL.</span></span> <span data-ttu-id="cc0b0-126">Pierakstiet to.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="cc0b0-127">Multivides bāzes URL atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-127">Update the media base URL</span></span>

1. <span data-ttu-id="cc0b0-128">Pierakstieties programmā Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="cc0b0-129">Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Mazumtirdzniecība \> Kanālu iestatīšana \> Kanālu profili**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="cc0b0-130">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-130">Select **Edit**.</span></span>
1. <span data-ttu-id="cc0b0-131">Sadaļā **Profila rekvizīti** aizstājiet rekvizīta **Multivides servera bāzes URL** vērtību ar iepriekš izveidoto multivides bāzes URL.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="cc0b0-132">Kreisas puses saraksta kanālā **Noklusējums** atlasiet citu kanālu.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="cc0b0-133">Sadaļā **Profila rekvizīti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="cc0b0-134">Rekvizītam, kas tika pievienots, atlasiet **Multivides servera bāzes URL** kā rekvizīta atslēgu.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="cc0b0-135">Kā rekvizīta vērtību ievadiet iepriekš izveidoto multivides bāzes vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="cc0b0-136">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="cc0b0-137">E-pasta servera konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="cc0b0-138">Šeit ievadītajam SMTP serverim vai e-pasta pakalpojumam jābūt pieejamam no Azure abonementa, kuru izmantojat videi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="cc0b0-139">Pierakstieties pakalpojumā Mazumtirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="cc0b0-140">Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Sistēmas administrācija \> Iestatījumi \> E-pasts \> E-pasta parametri**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="cc0b0-141">Cilnes **SMTP iestatījumi** laukā **Izejošā pasta serveris** ievadiet SMTP servera vai e-pasta pakalpojuma FQDN vai IP adresi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="cc0b0-142">Laukā **SMTP porta numurs** ievadiet porta numuru.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="cc0b0-143">(Ja neizmantojat drošligzdu slāņa \[SSL\], noklusējuma porta numurs ir **25**.)</span><span class="sxs-lookup"><span data-stu-id="cc0b0-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="cc0b0-144">Ja autentifikācija ir nepieciešama, ievadiet vērtības laukos **Lietotājvārds** un **Parole**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="cc0b0-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-145">Select **Save**.</span></span>
1. <span data-ttu-id="cc0b0-146">Atlasiet **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="cc0b0-147">Cilnes **Testa e-pasts** laukā **E-pasta pakalpojumu sniedzējs** atlasiet **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="cc0b0-148">Laukā **Nosūtīt uz** ievadiet e-pasta adresi, uz kuru jāpiegādā testa e-pasts.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="cc0b0-149">Atlasiet **Sūtīt e-pasta ziņojumu.**</span><span class="sxs-lookup"><span data-stu-id="cc0b0-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="cc0b0-150">E-pasta veidņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-150">Configure email templates</span></span>

<span data-ttu-id="cc0b0-151">Katram darījuma notikumam, kuram vēlaties sūtīt e-pasta ziņojumus, jums ir jāatjaunina e-pasta veidne ar derīgu sūtītāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="cc0b0-152">Pierakstieties pakalpojumā Mazumtirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="cc0b0-153">Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Organizācijas administrācija \> Iestatījumi \> Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="cc0b0-154">Atlasiet **Rādīt sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-154">Select **Show list**.</span></span>
1. <span data-ttu-id="cc0b0-155">Katrai veidnei sarakstā izpildiet tālākās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="cc0b0-156">Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="cc0b0-157">Neobligāti: laukā **Sūtītāja vārds** ievadiet nosaukumu, kas jāizmanto kā sūtītāja vārds.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="cc0b0-158">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="cc0b0-159">E-pasta veidņu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-159">Customize email templates</span></span>

<span data-ttu-id="cc0b0-160">Iespējams, vēlēsieties pielāgot e-pasta veidnes, lai tās izmantotu dažādus attēlus.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="cc0b0-161">Vai arī, iespējams, vēlēsieties atjaunināt veidņu saites, lai tās novirzītu uz priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="cc0b0-162">Šī procedūra izskaidro, kā lejupielādēt noklusējuma veidnes, pielāgot tās un atjaunināt veidnes sistēmā.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="cc0b0-163">Sava datora tīmekļa pārlūkprogrammā lejupielādējiet [Microsoft Dynamics 365 Commerce priekšskatījuma noklusējuma e-pasta veidnes .zip failu](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip).</span><span class="sxs-lookup"><span data-stu-id="cc0b0-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="cc0b0-164">Šajā failā ir ietverti tālāk norādītie HTML dokumenti.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="cc0b0-165">Pasūtījuma apstiprinājuma veidne</span><span class="sxs-lookup"><span data-stu-id="cc0b0-165">Order confirmation template</span></span>
    - <span data-ttu-id="cc0b0-166">Dāvanu kartes izsniegšanas veidne</span><span class="sxs-lookup"><span data-stu-id="cc0b0-166">Issue gift card template</span></span>
    - <span data-ttu-id="cc0b0-167">Jauna pasūtījuma veidne</span><span class="sxs-lookup"><span data-stu-id="cc0b0-167">New order template</span></span>
    - <span data-ttu-id="cc0b0-168">Pasūtījuma iesaiņošanas veidne</span><span class="sxs-lookup"><span data-stu-id="cc0b0-168">Pack order template</span></span>
    - <span data-ttu-id="cc0b0-169">Pasūtījuma saņemšanas veidne</span><span class="sxs-lookup"><span data-stu-id="cc0b0-169">Pick order template</span></span>

1. <span data-ttu-id="cc0b0-170">Pielāgojiet veidnes, izmantojot teksta vai HTML redaktoru.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="cc0b0-171">Skatiet tālāk šajā tēmā [atbalstīto marķieru](#supported-tokens-in-the-email-template) sarakstu.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="cc0b0-172">Pierakstieties pakalpojumā Mazumtirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="cc0b0-173">Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Organizācijas administrācija \> Iestatījumi \> Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="cc0b0-174">Paplašiniet sarakstu kreisajā pusē, lai redzētu visas veidnes.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="cc0b0-175">Attiecībā uz katru veidni, kuru vēlaties pielāgot, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="cc0b0-176">Atlasiet sarakstā veidni.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="cc0b0-177">Sadaļā **E-pasta ziņojuma saturs** no saraksta atlasiet atbilstošo valodas versiju.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="cc0b0-178">(Noklusējuma valoda ir **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="cc0b0-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="cc0b0-179">Sadaļā **E-pasta**ziņojuma saturs atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="cc0b0-180">Tiek parādīta rūts **Augšupielādēt e-pasta veidni**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="cc0b0-181">Atlasiet **Pārlūkot** un atrodiet HTML failu, kurā ir pielāgots saturs.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="cc0b0-182">Atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-182">Select **Upload**.</span></span> <span data-ttu-id="cc0b0-183">Veidne tiek augšupielādēta sistēmā, un tiek parādīts priekšskatījums.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="cc0b0-184">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-184">Select **OK**.</span></span>
    1. <span data-ttu-id="cc0b0-185">Pēc izvēles: pielāgojiet veidnes rekvizītu **Temats**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="cc0b0-186">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="cc0b0-187">E-pasta veidnē atbalstītie marķieri</span><span class="sxs-lookup"><span data-stu-id="cc0b0-187">Supported tokens in the email template</span></span>

<span data-ttu-id="cc0b0-188">Kad e-pasts tiek atveidots, šie marķieri tiek aizstāti ar faktiskajām vērtībām, kas attiecas uz klientu un klienta pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="cc0b0-189">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-189">Sales order</span></span>

<span data-ttu-id="cc0b0-190">Tālāk minētie marķieri attiecas uz vispārēju pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="cc0b0-191">Marķējuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-191">Name of the token</span></span> | <span data-ttu-id="cc0b0-192">Marķieris</span><span class="sxs-lookup"><span data-stu-id="cc0b0-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="cc0b0-193">Pasūtījuma numurs</span><span class="sxs-lookup"><span data-stu-id="cc0b0-193">Order number</span></span>      | <span data-ttu-id="cc0b0-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-194">%salesid%</span></span> |
| <span data-ttu-id="cc0b0-195">Debitora nosaukums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-195">Customer's name</span></span>   | <span data-ttu-id="cc0b0-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-196">%customername%</span></span> |
| <span data-ttu-id="cc0b0-197">Piegādes adrese</span><span class="sxs-lookup"><span data-stu-id="cc0b0-197">Delivery address</span></span>  | <span data-ttu-id="cc0b0-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="cc0b0-199">Norēķinu adrese</span><span class="sxs-lookup"><span data-stu-id="cc0b0-199">Billing address</span></span>   | <span data-ttu-id="cc0b0-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-200">%customeraddress%</span></span> |
| <span data-ttu-id="cc0b0-201">Ordera datums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-201">Order date</span></span>        | <span data-ttu-id="cc0b0-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-202">%shipdate%</span></span> |
| <span data-ttu-id="cc0b0-203">Piegādes veids</span><span class="sxs-lookup"><span data-stu-id="cc0b0-203">Delivery mode</span></span>     | <span data-ttu-id="cc0b0-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="cc0b0-205">Atlaide</span><span class="sxs-lookup"><span data-stu-id="cc0b0-205">Discount</span></span>          | <span data-ttu-id="cc0b0-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-206">%discount%</span></span> |
| <span data-ttu-id="cc0b0-207">PVN</span><span class="sxs-lookup"><span data-stu-id="cc0b0-207">Sales tax</span></span>         | <span data-ttu-id="cc0b0-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-208">%tax%</span></span> |
| <span data-ttu-id="cc0b0-209">Pasūtījuma kopsumma</span><span class="sxs-lookup"><span data-stu-id="cc0b0-209">Order total</span></span>       | <span data-ttu-id="cc0b0-210">%total%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="cc0b0-211">Pārdošanas rinda</span><span class="sxs-lookup"><span data-stu-id="cc0b0-211">Sales line</span></span>

<span data-ttu-id="cc0b0-212">Tālāk esošie marķieri tiek aizstāti ar vērtībām katram produktam pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="cc0b0-213">Ievietojiet marķieri **Preču saraksts — sākums** HTML bloka sākumā, kas atkārtojas katram produktam, un marķieri **Preču saraksts — beigas** bloka beigās.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="cc0b0-214">Marķējuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-214">Name of the token</span></span>      | <span data-ttu-id="cc0b0-215">Marķieris</span><span class="sxs-lookup"><span data-stu-id="cc0b0-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="cc0b0-216">Preču saraksts — sākums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-216">Product list - start</span></span>   | <span data-ttu-id="cc0b0-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="cc0b0-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="cc0b0-218">Preču saraksts — beigas</span><span class="sxs-lookup"><span data-stu-id="cc0b0-218">Product list - end</span></span>     | <span data-ttu-id="cc0b0-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="cc0b0-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="cc0b0-220">Preces nosaukums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-220">Product name</span></span>           | <span data-ttu-id="cc0b0-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-221">%lineproductname%</span></span> |
| <span data-ttu-id="cc0b0-222">Apraksts</span><span class="sxs-lookup"><span data-stu-id="cc0b0-222">Description</span></span>            | <span data-ttu-id="cc0b0-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="cc0b0-224">Daudzums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-224">Quantity</span></span>               | <span data-ttu-id="cc0b0-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-225">%linequantity%</span></span> |
| <span data-ttu-id="cc0b0-226">Rindas vienības cena</span><span class="sxs-lookup"><span data-stu-id="cc0b0-226">Line unit price</span></span>        | <span data-ttu-id="cc0b0-227">%lineprice% (verificēt)</span><span class="sxs-lookup"><span data-stu-id="cc0b0-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="cc0b0-228">rindas preču kopsumma</span><span class="sxs-lookup"><span data-stu-id="cc0b0-228">line item total</span></span>        | <span data-ttu-id="cc0b0-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-229">%linenetamount%</span></span> |
| <span data-ttu-id="cc0b0-230">rindas atlaide</span><span class="sxs-lookup"><span data-stu-id="cc0b0-230">line discount</span></span>          | <span data-ttu-id="cc0b0-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-231">%linediscount%</span></span> |
| <span data-ttu-id="cc0b0-232">Nosūtīšanas datums</span><span class="sxs-lookup"><span data-stu-id="cc0b0-232">Ship date</span></span>              | <span data-ttu-id="cc0b0-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-233">%lineshipdate%</span></span> |
| <span data-ttu-id="cc0b0-234">Iepirkuma metode</span><span class="sxs-lookup"><span data-stu-id="cc0b0-234">Procurement method</span></span>     | <span data-ttu-id="cc0b0-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="cc0b0-236">piegādes adrese</span><span class="sxs-lookup"><span data-stu-id="cc0b0-236">delivery address</span></span>       | <span data-ttu-id="cc0b0-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="cc0b0-238">Rindas pārdošanas vienība</span><span class="sxs-lookup"><span data-stu-id="cc0b0-238">Sales unit of the line</span></span> | <span data-ttu-id="cc0b0-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="cc0b0-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="cc0b0-240">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cc0b0-240">Additional resources</span></span>

[<span data-ttu-id="cc0b0-241">Commerce priekšskatījuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="cc0b0-241">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="cc0b0-242">Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-242">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="cc0b0-243">Commerce priekšskatījuma vides konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cc0b0-243">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="cc0b0-244">Commerce priekšskatījuma vides BUJ</span><span class="sxs-lookup"><span data-stu-id="cc0b0-244">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="cc0b0-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="cc0b0-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="cc0b0-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="cc0b0-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="cc0b0-247">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="cc0b0-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="cc0b0-248">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="cc0b0-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="cc0b0-249">Palīdzības resursi Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="cc0b0-249">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
