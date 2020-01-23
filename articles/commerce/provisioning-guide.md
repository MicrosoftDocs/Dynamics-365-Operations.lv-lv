---
title: Commerce priekšskatījuma vides nodrošināšana
description: Šajā tēmā ir paskaidrots, kā nodrošināt Microsoft Dynamics 365 Commerce priekšskatījuma vidi.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934752"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="ac1ac-103">Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ac1ac-104">Šajā tēmā ir paskaidrots, kā nodrošināt Microsoft Dynamics 365 Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="ac1ac-105">Pirms sākt, iesakām vismaz izskatīt visu šo tēmu, lai gūtu priekšstatu par to, ko nozīmē process un ko satur šī tēma.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="ac1ac-106">Ja jums pagaidām nav piešķirta piekļuve Dynamics 365 Commerce priekšskatījumam, varat pieprasīt priekšskatījuma piekļuvi no [Commerce vietnes](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="ac1ac-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ac1ac-107">Overview</span></span>

<span data-ttu-id="ac1ac-108">Lai veiksmīgi nodrošinātu savu Commerce priekšskatījuma vidi, jāizveido projekts ar noteiktu preces nosaukumu un veidu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="ac1ac-109">Videi un Retail Cloud Scale Unit (RCSU) arī ir daži specifiski parametri, kas jāizmanto, vēlāk nodrošinot e-tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="ac1ac-110">Šajā tēmā sniegtās instrukcijas apraksta visas nepieciešamās darbības, kas jāizpilda, un parametrus, kas jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="ac1ac-111">Pēc veiksmīgas savas Commerce priekšskatījuma vides nodrošināšanas ir jāpabeidz dažas pēcnodrošināšanas darbības, lai to sagatavotu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="ac1ac-112">Dažas darbības nav obligātas, atkarībā no sistēmas aspektiem, ko vēlaties novērtēt.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="ac1ac-113">Pēc izvēles veicamās darbības vienmēr varat pabeigt vēlāk.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="ac1ac-114">Informāciju par to, kā konfigurēt Commerce priekšskatījuma vidi pēc tās nodrošināšanas, skatiet [Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="ac1ac-115">Informāciju par to, kā konfigurēt neobligātos līdzekļus savai Commerce priekšskatījuma videi, skatiet [Commerce priekšskatījuma vides neobligāto līdzekļu konfigurēšana](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="ac1ac-116">Ja jums ir jautājumi par nodrošināšanas darbībām vai ja rodas kādas problēmas, lūdzu, paziņojiet Microsoft [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupā](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac1ac-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="ac1ac-117">Prerequisites</span></span>

<span data-ttu-id="ac1ac-118">Lai varētu nodrošināt savu Commerce priekšskatījuma vidi, ir jābūt nodrošinātiem tālāk norādītajiem priekšnosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="ac1ac-119">Jums ir piekļuve Microsoft Dynamics Lifecycle Services (LCS) portālam.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="ac1ac-120">Jūs esat akceptēts Dynamics 365 Commerce priekšskatījuma programmā.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="ac1ac-121">Jums ir nepieciešamās atļaujas, lai izveidotu projektu vienumiem **Nākamās iepriekšpārdošanas** vai **Migrēt, izveidot risinājumus un mācīties**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="ac1ac-122">Jūs esat lomu **Vides vadītājs** vai **Projekta īpašnieks** dalībnieks projektā, kurā nodrošināsiet vidi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="ac1ac-123">Jums ir administratora piekļuve savam Microsoft Azure abonementam vai jūs varat sazināties ar abonementu administratoru, kurš jūsu vietā var pabeigt divas darbības, kam nepieciešamas administratora atļaujas.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="ac1ac-124">Jums ir pieejams savs Azure Active Directory (Azure AD) nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="ac1ac-125">Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā e-tirdzniecības sistēmas administratora grupu, un jums ir pieejams tās ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="ac1ac-126">Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā vērtējumu un pārskatu moderatora grupu, un jums ir pieejams tās ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="ac1ac-127">(Šī drošības grupa var būt tā pati, kas e-tirdzniecības sistēmas administratora grupa.)</span><span class="sxs-lookup"><span data-stu-id="ac1ac-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="ac1ac-128">Sava Azure AD nomnieka ID atrašana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="ac1ac-129">Jūsu Azure AD nomnieka ID ir globāli unikāls identifikators (globally unique identifier — GUID), kas līdzinās šim piemēram: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="ac1ac-130">Sava Azure AD nomnieka ID atrašana, izmantojot Azure portālu</span><span class="sxs-lookup"><span data-stu-id="ac1ac-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="ac1ac-131">Pierakstieties [Azure portālā](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ac1ac-132">Pārliecinieties, ka ir atlasīta vajadzīgā direktorija.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="ac1ac-133">Kreisās puses izvēlnē atlasiet **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="ac1ac-134">Sadaļā **Pārvaldīt** atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="ac1ac-135">Jūsu Azure AD nomnieka ID parādās sadaļā **Direktorijas ID**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="ac1ac-136">Sava Azure AD nomnieka ID atrašana, izmantojot OpenID Connect metadatus</span><span class="sxs-lookup"><span data-stu-id="ac1ac-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="ac1ac-137">Izveidojiet OpenID URL, aizvietojot **\{YOUR\_DOMAIN\}** ar savu domēnu, piemēram, `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="ac1ac-138">Piemēram, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` kļūs par `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="ac1ac-139">Atveriet OpenID URL, kas satur jūsu domēnu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="ac1ac-140">Varat atrast sava Azure AD nomnieka ID vairākās rekvizītu vērtībās.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="ac1ac-141">Atrodiet **authorization\_endpoint** un izgūstiet GUID, kas tiek parādīts tūlīt pēc `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="ac1ac-142">Sava Azure AD drošības grupas ID atrašana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="ac1ac-143">Jūsu Azure AD drošības grupas ID ir GUID, kas līdzinās šim piemēram: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="ac1ac-144">Šajā procedūrā tiek pieņemts, ka esat grupas dalībnieks, kurai mēģināt atrast ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="ac1ac-145">Atveriet [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="ac1ac-146">Atlasiet **Pierakstīties ar Microsoft** un pierakstieties, izmantojot savus akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="ac1ac-147">Kreisajā pusē atlasiet **rādīt vairāk paraugu**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="ac1ac-148">Labajās puses rūtī iespējojiet **Grupas**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="ac1ac-149">Aizveriet labo rūti.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-149">Close the right pane.</span></span>
1. <span data-ttu-id="ac1ac-150">Atlasiet **visas manas grupas**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="ac1ac-151">Laukā **Atbildes priekšskatījums** atrodiet savu grupu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="ac1ac-152">Drošības grupas ID tiek parādīts rekvizītā **id**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="ac1ac-153">Savas Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="ac1ac-154">Šīs procedūras izskaidro, kā nodrošināt Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="ac1ac-155">Pēc veiksmīgas to pabeigšanas Commerce priekšskatījuma vide būs gatava konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="ac1ac-156">Visas šeit aprakstītās darbības notiek LCS portālā.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac1ac-157">Priekšskatījuma piekļuve ir piesaistīta LCS kontam un organizācijai, ko norādījāt sava priekšskatījuma pieteikumā.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="ac1ac-158">Jums jāizmanto tas pats konts, lai nodrošinātu Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="ac1ac-159">Ja Commerce priekšskatījuma videi jums jāizmanto cits LCS konts vai nomnieks, jums Microsoft jānorāda šī detalizētā informācija.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="ac1ac-160">Kontaktinformāciju skatiet tālāk tēmā esošajā sadaļā [Commerce priekšskatījuma vides atbalsts](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="ac1ac-161">Piešķiriet piekļuvi e-tirdzniecības programmām</span><span class="sxs-lookup"><span data-stu-id="ac1ac-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac1ac-162">Personai, kas pierakstās, jābūt Azure AD nomnieka administratoram, kuram ir Azure AD nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="ac1ac-163">Ja šī darbība nav veiksmīgi pabeigta, pārējās nodrošināšanas darbības neizdosies.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="ac1ac-164">Lai autorizētu e-tirdzniecības pieteikumus piekļuvei Azure abonementam, veiciet tālāk noradītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-165">Sastādiet URL tālāk norādītajā formātā.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="ac1ac-166">Kopējiet un ielīmējiet vietrādi URL savā pārlūkprogrammā vai teksta redaktorā, un aizstājiet **\{AAD\_TENANT\_ID\}** ar sava Azure AD nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="ac1ac-167">Pēc tam atveriet URL.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-167">Then open the URL.</span></span>
1. <span data-ttu-id="ac1ac-168">Pierakstieties Azure AD pierakstīšanās dialoglodziņā un apstipriniet, ka vēlaties piešķirt **Dynamics 365 Commerce (priekšskatījums)** piekļuvi savam abonementam.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="ac1ac-169">Jūs tiekat novirzīts uz lapu, kas norādīs, vai operācija bija veiksmīga.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="ac1ac-170">Apstiprināšana, ka LCS ir pieejami un ieslēgti priekšskatījuma līdzekļi</span><span class="sxs-lookup"><span data-stu-id="ac1ac-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="ac1ac-171">Lai apstiprinātu, ka LCS ir pieejami un ieslēgti priekšskatījuma līdzekļi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-172">Pierakstieties [LCS portālā](https://lcs.dynamics.com), izmantojot to pašu LCS kontu, ko izmantojāt, lai pieprasītu piekļuvi priekšskatījumam.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="ac1ac-173">LCS sākumlapā ritiniet līdz galam pa labi un atlasiet elementu **Priekšskatīt līdzekļa pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Priekšskatījuma pārvaldības elements](./media/preview1.png)

1. <span data-ttu-id="ac1ac-175">Ritiniet uz leju līdz **Privātie priekšskatīšanas līdzekļi** un apstipriniet, ka ir pieejami un ieslēgti tālāk norādītie līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="ac1ac-176">E-tirdzniecības novērtēšana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="ac1ac-177">Tirdzniecības priekšskatījuma programmas vides</span><span class="sxs-lookup"><span data-stu-id="ac1ac-177">Commerce Preview Program Environments</span></span>

    ![Privātā priekšskatījuma līdzekļi](./media/preview2.png)

1. <span data-ttu-id="ac1ac-179">Ja šie līdzekļi nav redzami sarakstā, sazinieties ar Microsoft un norādiet savu darba e-pasta adresi, LCS kontu un detalizētu informāciju par nomnieku.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="ac1ac-180">Kontaktinformāciju skatiet sadaļā [Commerce priekšskatījuma vides atbalsts](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="ac1ac-181">Izveidot jaunu projektu</span><span class="sxs-lookup"><span data-stu-id="ac1ac-181">Create a new project</span></span>

<span data-ttu-id="ac1ac-182">Lai LCS izveidotu jaunu projektu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-183">Lai izveidotu projektu, LCS sākumlapā atlasiet pluszīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="ac1ac-184">Labās puses rūtī veiciet vienu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="ac1ac-185">Ja esat partneris, atlasiet **Migrēt, izveidot risinājumus un mācīties**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="ac1ac-186">Ja esat klients, atlasiet **Nākamās iepriekšpārdošanas**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="ac1ac-187">Ievadiet nosaukumu, aprakstu un nozari.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="ac1ac-188">Laukā **Preces nosaukums** atlasiet **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="ac1ac-189">Laukā **Preces versija** atlasiet **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="ac1ac-190">Laukā **Metodoloģija** atlasiet **Dynamics Retail ieviešanas metodoloģija**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="ac1ac-191">Pēc izvēles: varat importēt lomas un lietotājus no esoša projekta.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="ac1ac-192">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-192">Select **Create**.</span></span> <span data-ttu-id="ac1ac-193">Tiks parādīts projekta skats.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="ac1ac-194">Azure Connector pievienošana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-194">Add the Azure Connector</span></span>

<span data-ttu-id="ac1ac-195">Lai savam LCS projektam pievienotu Azure Connector, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-196">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="ac1ac-197">Ja esat partneris, labās puses galā atlasiet elementu **Projekta iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="ac1ac-198">Ja esat klients, augšējā izvēlnē atlasiet **Projekta iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="ac1ac-199">Atlasiet **Azure savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="ac1ac-200">Lai pievienotu Azure Connector, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="ac1ac-201">Ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-201">Enter a name.</span></span>
1. <span data-ttu-id="ac1ac-202">Ievadiet savu Azure abonementa ID.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="ac1ac-203">Ieslēdziet opciju **Konfigurēt, lai izmantotu Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="ac1ac-204">Pārbaudiet, vai vērtība **Azure abonementa AAD nomnieka domēns (vai ID)** ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="ac1ac-205">Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="ac1ac-206">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-206">Select **Next**.</span></span>
1. <span data-ttu-id="ac1ac-207">Izpildiet lapā redzamos norādījumus, lai nepieciešamajiem pieteikumiem piešķirtu piekļuvi savam abonementam.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="ac1ac-208">Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="ac1ac-209">Pierakstieties [Azure portālā](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="ac1ac-210">Pārliecinieties, vai ir atlasīta pareiza direktorija, un pēc tam kreisās puses izvēlnē atlasiet **Abonementi**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="ac1ac-211">Sarakstā atrodiet vajadzīgo abonementu un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="ac1ac-212">Ja nepieciešams, izmantojiet meklēšanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="ac1ac-213">Izvēlnē atlasiet **Piekļuves vadīkla (iAM)**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="ac1ac-214">Labajā pusē esošajā **Pievienot lomas piešķiri** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="ac1ac-215">Tiks parādīta rūts **Pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="ac1ac-216">Laukā **Loma** atlasiet **Atbalstītājs**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="ac1ac-217">Laukā **Piešķirt piekļuvi** atstājiet noklusējuma vērtību, **Azure AD lietotāju, grupu vai pakalpojuma vadītāju**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="ac1ac-218">**Atlasīt** ievadiet **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="ac1ac-219">Sarakstā atlasiet **Dynamics Deployment Services \[wsfed-enabled\]**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="ac1ac-220">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-220">Select **Save**.</span></span>

1. <span data-ttu-id="ac1ac-221">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-221">Select **Next**.</span></span>
1. <span data-ttu-id="ac1ac-222">Izpildiet lapā redzamos norādījumus, lai nepieciešamajiem pieteikumiem piešķirtu piekļuvi savam abonementam.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="ac1ac-223">Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="ac1ac-224">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-224">Select **Next**.</span></span>
1. <span data-ttu-id="ac1ac-225">Laukā **Azure reģions** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="ac1ac-226">Atlasiet **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-226">Select **Connect**.</span></span> <span data-ttu-id="ac1ac-227">Sarakstā ir jāparādās jūsu Azure Connector.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="ac1ac-228">Commerce priekšskatījuma demonstrācijas bāzes paplašinājuma imports</span><span class="sxs-lookup"><span data-stu-id="ac1ac-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="ac1ac-229">Lai sava projektā importētu Commerce priekšskatījuma demonstrācijas bāzes paplašinājumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-230">Atveriet sava projekta sākumlapu, augšdaļā atlasot projekta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="ac1ac-231">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="ac1ac-232">Ja esat partneris, labās puses galā atlasiet elementu **Līdzekļu bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="ac1ac-233">Ja esat klients, augšējā izvēlnē atlasiet **Līdzekļu bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="ac1ac-234">Sarakstā kreisajā pusē atlasiet **Pakotne, ko izvieto programmatūra**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="ac1ac-235">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-235">Select **Import**.</span></span>
1. <span data-ttu-id="ac1ac-236">**Koplietoto līdzekļu bibliotēka** līdzekļu sarakstā atlasiet **Commerce priekšskatījuma demonstrācijas bāzes paplašinājums**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="ac1ac-237">Atlasiet **Izdot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-237">Select **Pick**.</span></span> <span data-ttu-id="ac1ac-238">Jūs atgriezīsieties līdzekļu bibliotēkā, un jums vajadzētu redzēt saraksta paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="ac1ac-239">Tālāk redzamajā attēlā ir parādītas darbības, kas jāveic LCS lapā **Līdzekļu bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce priekšskatījuma demonstrācijas bāzes paplašinājuma importēšana](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="ac1ac-241">Vides izvietošana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-241">Deploy the environment</span></span>

<span data-ttu-id="ac1ac-242">Lai izvietotu vidi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ac1ac-243">Iespējams, jums nebūs jāveic 6., 7. un / vai 8. darbību, jo tiek izlaistas lapas, kurās ir viena opcija.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="ac1ac-244">Kad atrodaties skatā **Vides parametri**, apstipriniet, ka teksts **Dynamics 365 Commerce (priekšskatījums) — Demo (10.0.6 ar platformas atjauninājumu 30)** tiek parādīts tieši virs lauka **Vides nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="ac1ac-245">Skatiet attēlu, kas tiek parādīts pēc 8. darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="ac1ac-246">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ac1ac-247">Lai pievienotu vidi, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="ac1ac-248">Laukā **Pieteikuma versija** atlasiet **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="ac1ac-249">Laukā **Platformas versija** atlasiet **Platformas atjauninājums 30**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Pieteikumu un platformu versiju atlasīšana](./media/project1.png)

1. <span data-ttu-id="ac1ac-251">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-251">Select **Next**.</span></span>
1. <span data-ttu-id="ac1ac-252">Kā vides topoloģiju atlasiet **Demonstrācija**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-252">Select **Demo** as the environment topology.</span></span>

    ![1. vides topoloģijas atlasīšana](./media/project2.png)

1. <span data-ttu-id="ac1ac-254">Kā vides topoloģiju atlasiet **Dynamics 365 Commerce (priekšskatījums) — demonstrācija**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="ac1ac-255">Ja iepriekš konfigurējāt vienu Azure Connector, tas tiks izmantots šai videi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="ac1ac-256">Ja esat konfigurējis vairākus Azure Connector, varat izvēlēties, kuru savienotāju izmantot: **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="ac1ac-257">(Lai panāktu vislabāko veiktspēju visu laiku, iesakām atlasīt **Rietum ASV 2**).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![2. vides topoloģijas atlasīšana](./media/project3.png)

1. <span data-ttu-id="ac1ac-259">Lapā **Izvietot vidi** ievadiet vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="ac1ac-260">Atstājiet papildu iestatījumus, kādi tie ir.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-260">Leave the advanced settings as they are.</span></span>

    ![Vides lapas izvietošana](./media/project4.png)

1. <span data-ttu-id="ac1ac-262">Pielāgojiet VM lielumu pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-262">Adjust the VM size as required.</span></span> <span data-ttu-id="ac1ac-263">(Mēs iesakām VM noliktavas vienību \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="ac1ac-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="ac1ac-264">Pārskatiet cenu noteikšanas un licencēšanas nosacījumus un pēc tam atzīmējiet izvēles rūtiņu, lai norādītu, ka piekrītat tiem.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="ac1ac-265">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-265">Select **Next**.</span></span>
1. <span data-ttu-id="ac1ac-266">Izvietošanas apstiprinājuma lapā pārbaudiet, vai informācija ir pareiza, un pēc tam atlasiet **Izvietot**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="ac1ac-267">Jūs atgriezīsieties skatā **Mākoņvides**, un sarakstā ir jāparādās jūsu videi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="ac1ac-268">Jūsu pieprasītā vide parādīsies kā stāvoša rindā un tad izvietota.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="ac1ac-269">Vides darbplūsmas prasīs kādu laiku, līdz tiks pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="ac1ac-270">Tāpēc pārbaudiet vēlreiz pēc aptuveni sešām līdz deviņām stundām.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="ac1ac-271">Pirms turpināt, pārliecinieties, ka jūsu vides statuss ir **Izvietots**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="ac1ac-272">RCSU inicializēšana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-272">Initialize RCSU</span></span>

<span data-ttu-id="ac1ac-273">Lai inicializētu RCSU, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-274">Skatā **Mākoņvides** atlasiet saraksta savu vidi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="ac1ac-275">Vides skatā labajā pusē atlasiet **Visa informācija**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="ac1ac-276">Parādīsies detalizēts vides informācijas skats.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-276">The environment details view appears.</span></span>
1. <span data-ttu-id="ac1ac-277">**Vides līdzekļi** atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="ac1ac-278">Cilnē **Mazumtirdzniecība** atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="ac1ac-279">Parādīsies RCSU inicializācijas parametru skats.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="ac1ac-280">Laukā **Reģions** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="ac1ac-281">Laukā **Versija** sarakstā atlasiet **Norādīt versiju** un pēc tam laukā, kas parādās, norādiet **9.16.19262.5**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="ac1ac-282">Pārliecinieties, ka norādāt tieši šeit norādīto versiju.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="ac1ac-283">Pretējā gadījumā jums vēlāk būs jāatjaunina RCSU uz pareizo versiju.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="ac1ac-284">Ieslēdziet opciju **Lietot paplašinājumu**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="ac1ac-285">Paplašinājumu sarakstā atlasiet **Commerce priekšskatījuma demonstrāciju bāzes paplašinājums**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="ac1ac-286">Atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="ac1ac-287">Izvietošanas apstiprinājuma lapā pārbaudiet, ka informācija ir pareiza, un pēc tam atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="ac1ac-288">Jūs atgriezīsieties skatā **Mazumtirdzniecības pārvaldība**, kur atlasīta cilne **Mazumtirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="ac1ac-289">Jūsu RCSU tika ievietota rindā uz nodrošināšanu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="ac1ac-290">Pirms turpināt, pārliecinieties, ka jūsu RCSU statuss ir **Veiksmīgs**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="ac1ac-291">Inicializācija ilgst aptuveni divas līdz piecas stundas.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="ac1ac-292">E-tirdzniecības inicializēšana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-292">Initialize e-Commerce</span></span>

<span data-ttu-id="ac1ac-293">Lai inicializētu e-tirdzniecību, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ac1ac-294">Cilnē **e-tirdzniecība (priekšskatījums)** pārskatiet piekrišanu priekšskatījumam un pēc tam atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="ac1ac-295">Ievadiet nosaukumu laukā **E-tirdzniecības nomnieka nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="ac1ac-296">Tomēr ņemiet vērā, ka šis nosaukums parādīsies dažos URL, kas norāda uz jūsu e-tirdzniecības instanci.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="ac1ac-297">Laukā **Retail Cloud Scale Unit nosaukums** sarakstā atlasiet savu RCSU.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="ac1ac-298">(Sarakstā jābūt tikai vienai opcijai.)</span><span class="sxs-lookup"><span data-stu-id="ac1ac-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="ac1ac-299">Lauks **E-tirdzniecības ģeogrāfija** tiek iestatīts automātiski, un vērtību nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="ac1ac-300">Lai turpinātu, atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="ac1ac-301">Laukā **Atbalstītie resursdatora nosaukumi** ievadiet jebkuru derīgu domēnu, piemēram, `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="ac1ac-302">Laukā **AAD drošības grupa sistēmas administratoram** ievadiet dažus pirmos burtu no tās drošības grupas nosaukuma, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="ac1ac-303">Atlasiet palielināmo klases ikonu, lai parādītu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="ac1ac-304">Izvēlieties drošības grupu no saraksta.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="ac1ac-305">Laukā **AAD drošības grupa vērtējumu un pārskatu moderatoram** ievadiet dažus pirmos burtu no tās drošības grupas nosaukuma, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="ac1ac-306">Atlasiet palielināmo klases ikonu, lai parādītu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="ac1ac-307">Izvēlieties drošības grupu no saraksta.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="ac1ac-308">Atstājiet ieslēgtu opciju **Iespējot vērtējumu un pārskatu pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="ac1ac-309">Ja jau esat pabeidzis Microsoft Azure Active Directory (Azure AD) piekrišanas darbību, kā aprakstīts sadaļā "Piekļuves piešķiršana e-tirdzniecības pieteikumiem", atlasiet izvēles rūtiņu, lai apstiprinātu savu piekrišanu.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="ac1ac-310">Ja vēl neesat pabeidzis šo darbību, jums tā jāveic pirms turpināt inicializāciju.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="ac1ac-311">Tekstā atlasiet saiti, kas atrodas blakus izvēles rūtiņai, lai atvērtu piekrišanas dialoglodziņu un pabeigtu darbību.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="ac1ac-312">Atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-312">Select **Initialize**.</span></span> <span data-ttu-id="ac1ac-313">Jūs atgriezīsieties skatā **Mazumtirdzniecības pārvaldība**, kur atlasīta cilne **E-tirdzniecība (priekšskatījums)**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="ac1ac-314">Ir uzsākta e-tirdzniecības inicializēšana.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="ac1ac-315">Pirms turpināt, uzgaidiet, līdz e-tirdzniecības inicializācijas statuss ir **Inicializācija veiksmīga**.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="ac1ac-316">Apakšā pa labi no **Saites** norakstiet URL tālāk noradītajām saitēm.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="ac1ac-317">**E-tirdzniecības vietne** — saite uz jūsu e-tirdzniecības vietnes sakni.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="ac1ac-318">**E-tirdzniecības vietnes pārvaldības rīks** — saite uz vietnes pārvaldības rīku.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="ac1ac-319">Commerce priekšskatījuma vides atbalsts</span><span class="sxs-lookup"><span data-stu-id="ac1ac-319">Commerce preview environment support</span></span>

<span data-ttu-id="ac1ac-320">Ja rodas problēmas, pabeidzot nodrošināšanas darbības, lūdzu, apmeklējiet [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupu](https://aka.ms/Dynamics365CommercePreviewYammer), lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="ac1ac-321">Ja rodas problēmas, mēģinot piekļūt Yammer grupai, varat sazināties ar Microsoft, izmantojot e-pastu <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="ac1ac-322">Šī e-pasta adrese netiek aktīvi uzraudzīta.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="ac1ac-323">Tādēļ rēķinieties ar novēlotu atbildi.</span><span class="sxs-lookup"><span data-stu-id="ac1ac-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ac1ac-324">Nākamās darbības</span><span class="sxs-lookup"><span data-stu-id="ac1ac-324">Next steps</span></span>

<span data-ttu-id="ac1ac-325">Lai turpinātu nodrošināšanas procesu un konfigurētu Commerce priekšskatījuma vidi, skatiet [Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="ac1ac-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac1ac-326">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ac1ac-326">Additional resources</span></span>

[<span data-ttu-id="ac1ac-327">Commerce priekšskatījuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="ac1ac-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ac1ac-328">Commerce priekšskatījuma vides konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="ac1ac-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="ac1ac-329">Neobligāto līdzekļu konfigurēšana Commerce priekšskatījuma videi</span><span class="sxs-lookup"><span data-stu-id="ac1ac-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ac1ac-330">Commerce priekšskatījuma vides BUJ</span><span class="sxs-lookup"><span data-stu-id="ac1ac-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ac1ac-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ac1ac-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ac1ac-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ac1ac-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ac1ac-333">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="ac1ac-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ac1ac-334">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="ac1ac-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="ac1ac-335">Palīdzības resursi Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="ac1ac-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
