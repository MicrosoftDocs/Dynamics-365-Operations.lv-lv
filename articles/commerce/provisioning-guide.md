---
title: Dynamics 365 Commerce priekšskatījuma vides nodrošināšana
description: Šajā tēmā ir paskaidrots, kā nodrošināt Microsoft Dynamics 365 Commerce priekšskatījuma vidi.
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426469"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="9e7d0-103">Dynamics 365 Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9e7d0-104">Šajā tēmā ir paskaidrots, kā nodrošināt Dynamics 365 Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="9e7d0-105">Pirms sākat, iesakām ātri iziet caur šai tēmai, lai iegūtu priekšstatu par to, kas ir nepieciešams procesam.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="9e7d0-106">Ja jums pagaidām nav piešķirta piekļuve Dynamics 365 Commerce priekšskatījumam, varat pieprasīt priekšskatījuma piekļuvi no [Dynamics 365 Commerce vietnes](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="9e7d0-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="9e7d0-107">Overview</span></span>

<span data-ttu-id="9e7d0-108">Lai veiksmīgi nodrošinātu savu Commerce priekšskatījuma vidi, jāizveido projekts ar noteiktu preces nosaukumu un veidu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="9e7d0-109">Videi un Commerce Scale Unit (CSU) arī ir daži specifiski parametri, kas jāizmanto, vēlāk nodrošinot e-tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="9e7d0-110">Šajā tēmā sniegtās instrukcijas apraksta visas nepieciešamās darbības, kas jāizpilda, lai pabeigtu nodrošināšanu, un parametrus, kas jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="9e7d0-111">Pēc veiksmīgas savas Commerce priekšskatījuma vides nodrošināšanas ir jāpabeidz dažas pēcnodrošināšanas darbības, lai to sagatavotu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="9e7d0-112">Dažas darbības nav obligātas, atkarībā no sistēmas aspektiem, ko vēlaties novērtēt.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="9e7d0-113">Pēc izvēles veicamās darbības vienmēr varat pabeigt vēlāk.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="9e7d0-114">Informāciju par to, kā konfigurēt Commerce priekšskatījuma vidi pēc tās nodrošināšanas, skatiet [Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="9e7d0-115">Informāciju par to, kā konfigurēt neobligātos līdzekļus savai Commerce priekšskatījuma videi, skatiet [Commerce priekšskatījuma vides neobligāto līdzekļu konfigurēšana](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="9e7d0-116">Ja jums ir jautājumi par nodrošināšanas darbībām vai ja rodas kādas problēmas, lūdzu, paziņojiet Microsoft [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupā](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e7d0-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="9e7d0-117">Prerequisites</span></span>

<span data-ttu-id="9e7d0-118">Lai varētu nodrošināt savu Commerce priekšskatījuma vidi, ir jābūt nodrošinātiem tālāk norādītajiem priekšnosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="9e7d0-119">Jums ir piekļuve Microsoft Dynamics Lifecycle Services (LCS) portālam.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="9e7d0-120">Jūs esat esošs Microsoft Dynamics 365 partneris vai debitors un varat izveidot Dynamics 365 Commerce projektu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="9e7d0-121">Jūs esat akceptēts Dynamics 365 Commerce priekšskatījuma programmā.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="9e7d0-122">Jums ir nepieciešamās atļaujas, lai izveidotu projektu vienumam **Migrēt, izveidot risinājumus un mācīties**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="9e7d0-123">Jūs esat lomu **Vides vadītājs** vai **Projekta īpašnieks** dalībnieks projektā, kurā nodrošināsiet vidi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="9e7d0-124">Jums ir administratora piekļuve savam Microsoft Azure abonementam vai jūs varat sazināties ar abonementu administratoru, kurš jūsu vietā var pabeigt divas darbības, kam nepieciešamas administratora atļaujas.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="9e7d0-125">Jums ir pieejams savs Azure Active Directory (Azure AD) nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="9e7d0-126">Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā e-tirdzniecības sistēmas administratora grupu, un jums ir pieejams tās ID.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="9e7d0-127">Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā vērtējumu un pārskatu moderatora grupu, un jums ir pieejams tās ID.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="9e7d0-128">(Šī drošības grupa var būt tā pati, kas e-tirdzniecības sistēmas administratora grupa.)</span><span class="sxs-lookup"><span data-stu-id="9e7d0-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="9e7d0-129">Savas Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="9e7d0-130">Šīs procedūras izskaidro, kā nodrošināt Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="9e7d0-131">Pēc veiksmīgas to pabeigšanas Commerce priekšskatījuma vide būs gatava konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="9e7d0-132">Visas šeit aprakstītās darbības notiek LCS portālā.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e7d0-133">Priekšskatījuma piekļuve ir piesaistīta LCS kontam un organizācijai, ko norādījāt sava Commerce priekšskatījuma pieteikumā.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="9e7d0-134">Jums jāizmanto tas pats konts, lai nodrošinātu Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="9e7d0-135">Ja Commerce priekšskatījuma videi jums jāizmanto cits LCS konts vai nomnieks, jums Microsoft jānorāda šī detalizētā informācija.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="9e7d0-136">Kontaktinformāciju skatiet tālāk tēmā esošajā sadaļā [Commerce priekšskatījuma vides atbalsts](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="9e7d0-137">Apstiprināšana, ka LCS ir pieejami un ieslēgti priekšskatījuma līdzekļi</span><span class="sxs-lookup"><span data-stu-id="9e7d0-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="9e7d0-138">Lai apstiprinātu, ka LCS ir pieejami un ieslēgti priekšskatījuma līdzekļi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="9e7d0-139">Pierakstieties [LCS portālā](https://lcs.dynamics.com), izmantojot to pašu LCS kontu, ko izmantojāt, lai pieprasītu piekļuvi priekšskatījumam.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="9e7d0-140">LCS sākumlapā ritiniet līdz galam pa labi un atlasiet elementu **Priekšskatīt līdzekļa pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Priekšskatījuma pārvaldības elements](./media/preview1.png)

1. <span data-ttu-id="9e7d0-142">Ritiniet uz leju līdz **Privātie priekšskatīšanas līdzekļi** un apstipriniet, ka ir pieejami un ieslēgti tālāk norādītie līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="9e7d0-143">E-tirdzniecības novērtēšana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="9e7d0-144">Tirdzniecības priekšskatījuma programmas vides</span><span class="sxs-lookup"><span data-stu-id="9e7d0-144">Commerce Preview Program Environments</span></span>

    ![Privātā priekšskatījuma līdzekļi](./media/preview2.png)

1. <span data-ttu-id="9e7d0-146">Ja šie līdzekļi nav redzami sarakstā, sazinieties ar Microsoft un norādiet savu darba e-pasta adresi, LCS kontu un detalizētu informāciju par nomnieku.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="9e7d0-147">Kontaktinformāciju skatiet sadaļā [Commerce priekšskatījuma vides atbalsts](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="9e7d0-148">Izveidot jaunu projektu</span><span class="sxs-lookup"><span data-stu-id="9e7d0-148">Create a new project</span></span>

<span data-ttu-id="9e7d0-149">Lai LCS izveidotu jaunu projektu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="9e7d0-150">Lai izveidotu projektu, LCS sākumlapā atlasiet pluszīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="9e7d0-151">Labās puses rūtī veiciet vienu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="9e7d0-152">Ja esat partneris, atlasiet **Migrēt, izveidot risinājumus un mācīties**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="9e7d0-153">Ja esat klients, atlasiet **Nākamās iepriekšpārdošanas**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="9e7d0-154">Ievadiet nosaukumu, aprakstu un nozari.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="9e7d0-155">Laukā **Preces nosaukums** atlasiet **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="9e7d0-156">Laukā **Preces versija** atlasiet **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="9e7d0-157">Laukā **Metodoloģija** atlasiet **Dynamics Retail ieviešanas metodoloģija**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="9e7d0-158">Pēc izvēles: varat importēt lomas un lietotājus no esoša projekta.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="9e7d0-159">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-159">Select **Create**.</span></span> <span data-ttu-id="9e7d0-160">Tiks parādīts projekta skats.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="9e7d0-161">Azure Connector pievienošana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-161">Add the Azure Connector</span></span>

<span data-ttu-id="9e7d0-162">Lai savam LCS projektam pievienotu Azure Connector, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="9e7d0-163">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="9e7d0-164">Ja esat partneris, labās puses galā atlasiet elementu **Projekta iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="9e7d0-165">Ja esat klients, augšējā izvēlnē atlasiet **Projekta iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="9e7d0-166">Atlasiet **Azure savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="9e7d0-167">Lai pievienotu Azure Connector, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="9e7d0-168">Ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-168">Enter a name.</span></span>
1. <span data-ttu-id="9e7d0-169">Ievadiet savu Azure abonementa ID.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="9e7d0-170">Ieslēdziet opciju **Konfigurēt, lai izmantotu Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="9e7d0-171">Pārbaudiet, vai vērtība **Azure abonementa AAD nomnieka domēns (vai ID)** ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="9e7d0-172">Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="9e7d0-173">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-173">Select **Next**.</span></span>
1. <span data-ttu-id="9e7d0-174">Izpildiet lapā redzamos norādījumus, lai nepieciešamajiem pieteikumiem piešķirtu piekļuvi savam abonementam.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="9e7d0-175">Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="9e7d0-176">Pierakstieties [Azure portālā](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="9e7d0-177">Pārliecinieties, vai ir atlasīta pareiza direktorija, un pēc tam kreisās puses izvēlnē atlasiet **Abonementi**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="9e7d0-178">Sarakstā atrodiet vajadzīgo abonementu un atlasiet to.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="9e7d0-179">Ja nepieciešams, izmantojiet meklēšanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="9e7d0-180">Izvēlnē atlasiet **Piekļuves vadīkla (iAM)**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="9e7d0-181">Labajā pusē esošajā **Pievienot lomas piešķiri** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="9e7d0-182">Tiks parādīta rūts **Pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="9e7d0-183">Laukā **Loma** atlasiet **Atbalstītājs**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="9e7d0-184">Laukā **Piešķirt piekļuvi** atstājiet noklusējuma vērtību, **Azure AD lietotāju, grupu vai pakalpojuma vadītāju**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="9e7d0-185">**Atlasīt** ievadiet **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="9e7d0-186">Sarakstā atlasiet **Dynamics Deployment Services \[wsfed-enabled\]**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="9e7d0-187">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-187">Select **Save**.</span></span>

1. <span data-ttu-id="9e7d0-188">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-188">Select **Next**.</span></span>
1. <span data-ttu-id="9e7d0-189">Izpildiet lapā redzamos norādījumus, lai nepieciešamajiem pieteikumiem piešķirtu piekļuvi savam abonementam.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="9e7d0-190">Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="9e7d0-191">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-191">Select **Next**.</span></span>
1. <span data-ttu-id="9e7d0-192">Laukā **Azure reģions** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="9e7d0-193">Atlasiet **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-193">Select **Connect**.</span></span> <span data-ttu-id="9e7d0-194">Sarakstā ir jāparādās jūsu Azure Connector.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="9e7d0-195">Commerce priekšskatījuma demonstrācijas bāzes paplašinājuma imports</span><span class="sxs-lookup"><span data-stu-id="9e7d0-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="9e7d0-196">Lai sava projektā importētu Commerce priekšskatījuma demonstrācijas bāzes paplašinājumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="9e7d0-197">Atveriet sava projekta sākumlapu, augšdaļā atlasot projekta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="9e7d0-198">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="9e7d0-199">Ja esat partneris, labās puses galā atlasiet elementu **Līdzekļu bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="9e7d0-200">Ja esat klients, augšējā izvēlnē atlasiet **Līdzekļu bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="9e7d0-201">Sarakstā kreisajā pusē atlasiet **Pakotne, ko izvieto programmatūra**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="9e7d0-202">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-202">Select **Import**.</span></span>
1. <span data-ttu-id="9e7d0-203">**Koplietoto līdzekļu bibliotēka** līdzekļu sarakstā atlasiet **Commerce priekšskatījuma demonstrācijas bāzes paplašinājums**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="9e7d0-204">Atlasiet **Izdot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-204">Select **Pick**.</span></span> <span data-ttu-id="9e7d0-205">Jūs atgriezīsieties līdzekļu bibliotēkā, un jums vajadzētu redzēt saraksta paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="9e7d0-206">Tālāk redzamajā attēlā ir parādītas darbības, kas jāveic LCS lapā **Līdzekļu bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce priekšskatījuma demonstrācijas bāzes paplašinājuma importēšana](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="9e7d0-208">Vides izvietošana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-208">Deploy the environment</span></span>

<span data-ttu-id="9e7d0-209">Lai izvietotu vidi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="9e7d0-210">Iespējams, jums nebūs jāveic 6., 7. un / vai 8. darbību, jo tiek izlaistas lapas, kurās ir viena opcija.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="9e7d0-211">Kad atrodaties skatā **Vides parametri**, apstipriniet, ka teksts **Dynamics 365 Commerce - Demo (10.0.* x* ar Platform update *xx*)\*\* parādās tieši virs lauka **Vides nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="9e7d0-212">Detalizētu informāciju skatiet attēlā, kas tiek parādīts pēc 8. darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="9e7d0-213">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="9e7d0-214">Lai pievienotu vidi, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="9e7d0-215">Laukā **Programmas versija** atlasiet visjaunāko versiju.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="9e7d0-216">Ja jums ir īpaša nepieciešamība atlasīt programmas versiju, kas nav visjaunākā versija, neatlasiet versiju pirms **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="9e7d0-217">Laukā **Platformas versija** izmantojiet platformas versiju, kas tiek automātiski izvēlēta jūsu izvēlētajai programmas versijai.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Pieteikumu un platformu versiju atlasīšana](./media/project1.png)

1. <span data-ttu-id="9e7d0-219">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-219">Select **Next**.</span></span>
1. <span data-ttu-id="9e7d0-220">Kā vides topoloģiju atlasiet **Demonstrācija**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-220">Select **Demo** as the environment topology.</span></span>

    ![1. vides topoloģijas atlasīšana](./media/project2.png)

1. <span data-ttu-id="9e7d0-222">Atlasiet **Dynamics 365 Commerce - Demo** kā vides topoloģiju.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="9e7d0-223">Ja iepriekš konfigurējāt vienu Azure Connector, tas tiks izmantots šai videi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="9e7d0-224">Ja esat konfigurējis vairākus Azure Connector, varat izvēlēties, kuru savienotāju izmantot: **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="9e7d0-225">(Lai panāktu vislabāko veiktspēju visu laiku, iesakām atlasīt **Rietum ASV 2**).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![2. vides topoloģijas atlasīšana](./media/project3.png)

1. <span data-ttu-id="9e7d0-227">Lapā **Izvietot vidi** ievadiet vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="9e7d0-228">Atstājiet papildu iestatījumus, kādi tie ir.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-228">Leave the advanced settings as they are.</span></span>

    ![Vides lapas izvietošana](./media/project4.png)

1. <span data-ttu-id="9e7d0-230">Pielāgojiet VM lielumu pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-230">Adjust the VM size as required.</span></span> <span data-ttu-id="9e7d0-231">(Mēs iesakām VM noliktavas vienību \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="9e7d0-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="9e7d0-232">Pārskatiet cenu noteikšanas un licencēšanas nosacījumus un pēc tam atzīmējiet izvēles rūtiņu, lai norādītu, ka piekrītat tiem.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="9e7d0-233">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-233">Select **Next**.</span></span>
1. <span data-ttu-id="9e7d0-234">Izvietošanas apstiprinājuma lapā pārbaudiet, vai informācija ir pareiza, un pēc tam atlasiet **Izvietot**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="9e7d0-235">Jūs atgriezīsieties skatā **Mākoņvides**, un sarakstā ir jāparādās jūsu videi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="9e7d0-236">Jūsu pieprasītā vide parādīsies kā stāvoša rindā un tad izvietota.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="9e7d0-237">Vides darbplūsmas prasīs kādu laiku, līdz tiks pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="9e7d0-238">Tāpēc pārbaudiet vēlreiz pēc aptuveni sešām līdz deviņām stundām.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="9e7d0-239">Pirms turpināt, pārliecinieties, ka jūsu vides statuss ir **Izvietots**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="9e7d0-240">Commerce Scale Unit (mākoņa) inicializēšana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="9e7d0-241">Lai inicializētu CSU, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="9e7d0-242">Skatā **Mākoņvides** atlasiet saraksta savu vidi.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="9e7d0-243">Vides skatā labajā pusē atlasiet **Visa informācija**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="9e7d0-244">Parādīsies detalizēts vides informācijas skats.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-244">The environment details view appears.</span></span>
1. <span data-ttu-id="9e7d0-245">**Vides līdzekļi** atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="9e7d0-246">Cilnē **Komercija** atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="9e7d0-247">Parādīsies CSU inicializācijas parametru skats.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="9e7d0-248">Laukā **Reģions** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="9e7d0-249">Laukā **Versija** sarakstā atlasiet **Norādīt versiju** un pēc tam laukā, kas parādās, norādiet **9.18.20014.4**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="9e7d0-250">Pārliecinieties, ka norādāt tieši šeit norādīto versiju.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="9e7d0-251">Pretējā gadījumā jums vēlāk būs jāatjaunina RCSU uz pareizo versiju.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="9e7d0-252">Ieslēdziet opciju **Lietot paplašinājumu**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="9e7d0-253">Paplašinājumu sarakstā atlasiet **Commerce priekšskatījuma demonstrāciju bāzes paplašinājums**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="9e7d0-254">Atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="9e7d0-255">Izvietošanas apstiprinājuma lapā pārbaudiet, ka informācija ir pareiza, un pēc tam atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="9e7d0-256">**Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="9e7d0-257">Jūsu CSU tika ievietota rindā uz nodrošināšanu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="9e7d0-258">Pirms turpināt, pārliecinieties, ka jūsu CSU statuss ir **Veiksmīgs**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="9e7d0-259">Inicializācija ilgst aptuveni divas līdz piecas stundas.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="9e7d0-260">E-tirdzniecības inicializēšana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-260">Initialize e-Commerce</span></span>

<span data-ttu-id="9e7d0-261">Lai inicializētu e-tirdzniecību, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9e7d0-262">Cilnē **e-tirdzniecība** pārskatiet piekrišanu priekšskatījumam un pēc tam atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="9e7d0-263">Ievadiet nosaukumu laukā **E-tirdzniecības nomnieka nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="9e7d0-264">Tomēr ņemiet vērā, ka šis nosaukums parādīsies dažos URL, kas norāda uz jūsu e-tirdzniecības instanci.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="9e7d0-265">Laukā **Commerce Scale Unit nosaukums** atlasiet savu CSU.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="9e7d0-266">(Sarakstā jābūt tikai vienai opcijai.)</span><span class="sxs-lookup"><span data-stu-id="9e7d0-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="9e7d0-267">Lauks **E-tirdzniecības ģeogrāfija** tiek iestatīts automātiski, un vērtību nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="9e7d0-268">Lai turpinātu, atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="9e7d0-269">Laukā **Atbalstītie resursdatora nosaukumi** ievadiet jebkuru derīgu domēnu, piemēram, `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="9e7d0-270">Laukā **AAD drošības grupa sistēmas administratoram** ievadiet dažus pirmos burtu no tās drošības grupas nosaukuma, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="9e7d0-271">Atlasiet palielināmo klases ikonu, lai parādītu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="9e7d0-272">Sarakstā atlasiet pareizo drošības grupu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="9e7d0-273">Laukā **AAD drošības grupa vērtējumu un pārskatu moderatoram** ievadiet dažus pirmos burtu no tās drošības grupas nosaukuma, ko vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="9e7d0-274">Atlasiet palielināmo klases ikonu, lai parādītu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="9e7d0-275">Sarakstā atlasiet pareizo drošības grupu.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="9e7d0-276">Atstājiet ieslēgtu opciju **Iespējot vērtējumu un pārskatu pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="9e7d0-277">Atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-277">Select **Initialize**.</span></span> <span data-ttu-id="9e7d0-278">**Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **e-komercija**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="9e7d0-279">Ir uzsākta e-tirdzniecības inicializēšana.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="9e7d0-280">Pirms turpināt, uzgaidiet, līdz e-tirdzniecības inicializācijas statuss ir **Inicializācija veiksmīga**.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="9e7d0-281">Apakšā pa labi no **Saites** norakstiet URL tālāk noradītajām saitēm.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="9e7d0-282">**E-tirdzniecības vietne** — saite uz jūsu e-tirdzniecības vietnes sakni.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="9e7d0-283">**E-tirdzniecības vietnes pārvaldības rīks** — saite uz vietnes pārvaldības rīku.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="9e7d0-284">Commerce priekšskatījuma vides atbalsts</span><span class="sxs-lookup"><span data-stu-id="9e7d0-284">Commerce preview environment support</span></span>

<span data-ttu-id="9e7d0-285">Ja rodas problēmas, pabeidzot nodrošināšanas darbības, lūdzu, apmeklējiet [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupu](https://aka.ms/Dynamics365CommercePreviewYammer), lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="9e7d0-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9e7d0-286">Turpmākās darbības</span><span class="sxs-lookup"><span data-stu-id="9e7d0-286">Next steps</span></span>

<span data-ttu-id="9e7d0-287">Lai turpinātu nodrošināšanas procesu un konfigurētu Commerce priekšskatījuma vidi, skatiet [Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="9e7d0-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e7d0-288">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9e7d0-288">Additional resources</span></span>

[<span data-ttu-id="9e7d0-289">Dynamics 365 Commerce priekšskatījuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="9e7d0-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="9e7d0-290">Dynamics 365 Commerce priekšskatījuma vides konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9e7d0-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="9e7d0-291">Izvēles funkciju konfigurēšana Dynamics 365 Commerce priekšskatījuma videi</span><span class="sxs-lookup"><span data-stu-id="9e7d0-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9e7d0-292">Dynamics 365 Commerce priekšskatījuma vides BUJ</span><span class="sxs-lookup"><span data-stu-id="9e7d0-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="9e7d0-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9e7d0-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="9e7d0-294">Commerce Scale Unit (mākonis)</span><span class="sxs-lookup"><span data-stu-id="9e7d0-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="9e7d0-295">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="9e7d0-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="9e7d0-296">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="9e7d0-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

