---
title: Dynamics 365 Commerce novērtēšanas vides nodrošinājums
description: Šajā tēmā ir paskaidrots, kā nodrošināt programmas Microsoft Dynamics 365 Commerce novērtējuma vidi.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b675d4af6fb9a080f3f3a13e64b2c5b6ad4b783
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022426"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="57607-103">Dynamics 365 Commerce novērtēšanas vides nodrošinājums</span><span class="sxs-lookup"><span data-stu-id="57607-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57607-104">Šajā tēmā ir paskaidrots, kā nodrošināt programmas Microsoft Dynamics 365 Commerce novērtējuma vidi.</span><span class="sxs-lookup"><span data-stu-id="57607-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="57607-105">Pirms sākat, iesakām ātri iziet caur šai tēmai, lai iegūtu priekšstatu par to, kas ir nepieciešams procesam.</span><span class="sxs-lookup"><span data-stu-id="57607-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="57607-106">Commerce novērtējuma vides nav vispārpieejamas, un tās tiek piešķirtas partneriem un klientiem pēc pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="57607-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="57607-107">Lai iegūtu plašāku informāciju, sazinieties ar sava Microsoft partnera kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="57607-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="57607-108">Lai veiksmīgi nodrošinātu Commerce novērtējuma vidi, ir jāizveido projekts ar noteiktu preces nosaukumu un veidu.</span><span class="sxs-lookup"><span data-stu-id="57607-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="57607-109">Videi un Commerce Scale Unit (CSU) arī ir daži specifiski parametri, kas jāizmanto, vēloties nodrošināt e-tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="57607-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="57607-110">Šajā tēmā sniegtās instrukcijas apraksta visas nepieciešamās darbības, lai pabeigtu nodrošināšanu, un parametrus, kas jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="57607-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="57607-111">Pēc veiksmīgas Commerce novērtējuma vides nodrošināšanas ir jāpabeidz dažas pēc nodrošināšanas darbības, lai to sagatavotu izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="57607-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="57607-112">Dažas darbības nav obligātas, atkarībā no sistēmas aspektiem, ko vēlaties novērtēt.</span><span class="sxs-lookup"><span data-stu-id="57607-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="57607-113">Pēc izvēles veicamās darbības vienmēr varat pabeigt vēlāk.</span><span class="sxs-lookup"><span data-stu-id="57607-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="57607-114">Informāciju par to, kā konfigurēt Commerce novērtējuma vidi pēc tās nodrošināšanas, skatiet [Commerce novērtējuma vides konfigurācija](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="57607-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="57607-115">Informāciju par to, kā konfigurēt neobligātos līdzekļus Commerce novērtējuma videi, skatiet [Commerce novērtējuma vides neobligāto līdzekļu konfigurācija](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="57607-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="57607-116">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="57607-116">Prerequisites</span></span>

<span data-ttu-id="57607-117">Lai varētu nodrošināt Commerce novērtējuma vidi, ir jābūt ieviestiem tālāk norādītajiem priekšnoteikumiem.</span><span class="sxs-lookup"><span data-stu-id="57607-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="57607-118">Jūs esat iekāpis novērtēšanas programmā un jums piešķirta novērtēšanas vides noslodze.</span><span class="sxs-lookup"><span data-stu-id="57607-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="57607-119">Jums ir piekļuve Microsoft Dynamics Lifecycle Services (LCS) portālam.</span><span class="sxs-lookup"><span data-stu-id="57607-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="57607-120">Jūs esat esošs Microsoft Dynamics 365 partneris vai debitors un varat izveidot Dynamics 365 Commerce projektu.</span><span class="sxs-lookup"><span data-stu-id="57607-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="57607-121">Jums ir administratora piekļuve Microsoft Azure abonementam, vai arī jūs kontaktējaties ar abonementa administratoru, kurš nepieciešamības gadījumā var jums palīdzēt.</span><span class="sxs-lookup"><span data-stu-id="57607-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="57607-122">Jums ir pieejams savs Azure Active Directory (Azure AD) nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="57607-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="57607-123">Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā e-tirdzniecības sistēmas administratora grupu, un jums ir pieejams tās ID.</span><span class="sxs-lookup"><span data-stu-id="57607-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="57607-124">Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā vērtējumu un pārskatu moderatora grupu, un jums ir pieejams tās ID.</span><span class="sxs-lookup"><span data-stu-id="57607-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="57607-125">(Šī drošības grupa var būt tā pati, kas e-tirdzniecības sistēmas administratora grupa.)</span><span class="sxs-lookup"><span data-stu-id="57607-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="57607-126">Ņemiet vērā, ka šis saraksts nav pilnīgs.</span><span class="sxs-lookup"><span data-stu-id="57607-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="57607-127">Ja rodas kādas problēmas, sazinieties ar Microsoft partnera kontaktpersonu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="57607-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="57607-128">Commerce novērtējuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="57607-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="57607-129">Šīs procedūras izskaidro, kā nodrošināt Commerce novērtējuma vidi.</span><span class="sxs-lookup"><span data-stu-id="57607-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="57607-130">Pēc to veiksmīgas pabeigšanas Commerce novērtējuma vide būs gatava konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="57607-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="57607-131">Visas šeit aprakstītās darbības notiek LCS portālā.</span><span class="sxs-lookup"><span data-stu-id="57607-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="57607-132">Izveidot jaunu projektu</span><span class="sxs-lookup"><span data-stu-id="57607-132">Create a new project</span></span>

<span data-ttu-id="57607-133">Lai LCS izveidotu jaunu projektu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57607-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="57607-134">Lai izveidotu projektu, LCS sākumlapā atlasiet pluszīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="57607-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="57607-135">Labās puses rūtī veiciet vienu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="57607-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="57607-136">Ja esat partneris, atlasiet **Migrēt, izveidot risinājumus un mācīties**.</span><span class="sxs-lookup"><span data-stu-id="57607-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="57607-137">Ja esat klients, atlasiet **Nākamās iepriekšpārdošanas**.</span><span class="sxs-lookup"><span data-stu-id="57607-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="57607-138">Ievadiet nosaukumu, aprakstu un nozari.</span><span class="sxs-lookup"><span data-stu-id="57607-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="57607-139">Laukā **Preces nosaukums** atlasiet **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="57607-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="57607-140">Laukā **Preces versija** atlasiet **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="57607-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="57607-141">Laukā **Metodoloģija** atlasiet **Dynamics Retail ieviešanas metodoloģija**.</span><span class="sxs-lookup"><span data-stu-id="57607-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="57607-142">Pēc izvēles: varat importēt lomas un lietotājus no esoša projekta.</span><span class="sxs-lookup"><span data-stu-id="57607-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="57607-143">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="57607-143">Select **Create**.</span></span> <span data-ttu-id="57607-144">Tiks parādīts projekta skats.</span><span class="sxs-lookup"><span data-stu-id="57607-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="57607-145">Azure Connector pievienošana</span><span class="sxs-lookup"><span data-stu-id="57607-145">Add the Azure Connector</span></span>

<span data-ttu-id="57607-146">Lai Azure savienotāju pievienotu LCS projektam, veiciet darbības, kas norādītas sadaļā [Pabeigt Azure Resource Manager (ARM) pievienošanas procesu](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span><span class="sxs-lookup"><span data-stu-id="57607-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="57607-147">Vides izvietošana</span><span class="sxs-lookup"><span data-stu-id="57607-147">Deploy the environment</span></span>

<span data-ttu-id="57607-148">Lai izvietotu vidi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57607-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="57607-149">Iespējams, jums nebūs jāveic 6., 7. un / vai 8. darbību, jo tiek izlaistas lapas, kurās ir viena opcija.</span><span class="sxs-lookup"><span data-stu-id="57607-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="57607-150">Kad atrodaties skatā **Vides parametri**, apstipriniet, ka teksts **Dynamics 365 Commerce - Demo (10.0.* x* ar Platform update *xx*)\*\* parādās tieši virs lauka **Vides nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="57607-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="57607-151">Detalizētu informāciju skatiet attēlā, kas tiek parādīts pēc 8. darbības.</span><span class="sxs-lookup"><span data-stu-id="57607-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="57607-152">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="57607-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="57607-153">Lai pievienotu vidi, atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="57607-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="57607-154">Laukā **Programmas versija** atlasiet visjaunāko versiju.</span><span class="sxs-lookup"><span data-stu-id="57607-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="57607-155">Ja jums ir īpaša nepieciešamība atlasīt programmas versiju, kas nav visjaunākā versija, neatlasiet versiju pirms **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="57607-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="57607-156">Laukā **Platformas versija** izmantojiet platformas versiju, kas tiek automātiski izvēlēta jūsu izvēlētajai programmas versijai.</span><span class="sxs-lookup"><span data-stu-id="57607-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Pieteikumu un platformu versiju atlasīšana](./media/project1.png)

1. <span data-ttu-id="57607-158">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="57607-158">Select **Next**.</span></span>
1. <span data-ttu-id="57607-159">Kā vides topoloģiju atlasiet **Demonstrācija**.</span><span class="sxs-lookup"><span data-stu-id="57607-159">Select **Demo** as the environment topology.</span></span>

    ![1. vides topoloģijas atlasīšana](./media/project2.png)

1. <span data-ttu-id="57607-161">Lapā **Izvietot vidi** ievadiet vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="57607-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="57607-162">Atstājiet papildu iestatījumus, kādi tie ir.</span><span class="sxs-lookup"><span data-stu-id="57607-162">Leave the advanced settings as they are.</span></span>

    ![Vides lapas izvietošana](./media/project4.png)

1. <span data-ttu-id="57607-164">Pielāgojiet VM lielumu pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="57607-164">Adjust the VM size as required.</span></span> <span data-ttu-id="57607-165">(Mēs iesakām VM noliktavas vienību \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="57607-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="57607-166">Pārskatiet cenu noteikšanas un licencēšanas nosacījumus un pēc tam atzīmējiet izvēles rūtiņu, lai norādītu, ka piekrītat tiem.</span><span class="sxs-lookup"><span data-stu-id="57607-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="57607-167">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="57607-167">Select **Next**.</span></span>
1. <span data-ttu-id="57607-168">Izvietošanas apstiprinājuma lapā pārbaudiet, vai informācija ir pareiza, un pēc tam atlasiet **Izvietot**.</span><span class="sxs-lookup"><span data-stu-id="57607-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="57607-169">Jūs atgriezīsieties skatā **Mākoņvides**, un sarakstā ir jāparādās jūsu videi.</span><span class="sxs-lookup"><span data-stu-id="57607-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="57607-170">Jūsu pieprasītā vide parādīsies kā stāvoša rindā un tad izvietota.</span><span class="sxs-lookup"><span data-stu-id="57607-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="57607-171">Vides darbplūsmas prasīs kādu laiku, līdz tiks pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="57607-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="57607-172">Tāpēc pārbaudiet vēlreiz pēc aptuveni sešām līdz deviņām stundām.</span><span class="sxs-lookup"><span data-stu-id="57607-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="57607-173">Pirms turpināt, pārliecinieties, ka jūsu vides statuss ir **Izvietots**.</span><span class="sxs-lookup"><span data-stu-id="57607-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="57607-174">Commerce Scale Unit (mākoņa) inicializēšana</span><span class="sxs-lookup"><span data-stu-id="57607-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="57607-175">Lai inicializētu CSU, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57607-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="57607-176">Skatā **Mākoņvides** atlasiet saraksta savu vidi.</span><span class="sxs-lookup"><span data-stu-id="57607-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="57607-177">Vides skatā labajā pusē atlasiet **Visa informācija**.</span><span class="sxs-lookup"><span data-stu-id="57607-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="57607-178">Parādīsies detalizēts vides informācijas skats.</span><span class="sxs-lookup"><span data-stu-id="57607-178">The environment details view appears.</span></span>
1. <span data-ttu-id="57607-179">**Vides līdzekļi** atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="57607-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="57607-180">Cilnē **Komercija** atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="57607-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="57607-181">Parādīsies CSU inicializācijas parametru skats.</span><span class="sxs-lookup"><span data-stu-id="57607-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="57607-182">Laukā **Reģions** atlasiet reģionu, kas ir tāds pats vai tuvu reģionam, kurā tika izvietota vide.</span><span class="sxs-lookup"><span data-stu-id="57607-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="57607-183">Atstājiet lauku **Versija**, kā tas ir.</span><span class="sxs-lookup"><span data-stu-id="57607-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="57607-184">Atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="57607-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="57607-185">Izvietošanas apstiprinājuma lapā pārbaudiet, ka informācija ir pareiza, un pēc tam atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="57607-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="57607-186">**Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="57607-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="57607-187">Jūsu CSU tika ievietota rindā uz nodrošināšanu.</span><span class="sxs-lookup"><span data-stu-id="57607-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="57607-188">Pirms turpināt, pārliecinieties, ka jūsu CSU statuss ir **Veiksmīgs**.</span><span class="sxs-lookup"><span data-stu-id="57607-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="57607-189">Inicializācija ilgst aptuveni divas līdz piecas stundas.</span><span class="sxs-lookup"><span data-stu-id="57607-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="57607-190">Ja nevarat atrast saiti **Pārvaldība** vides informācijas skatā, sazinieties ar Microsoft kontaktpersonu, lai saņemtu palīdzību.</span><span class="sxs-lookup"><span data-stu-id="57607-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="57607-191">Izvietošanas procesa laikā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="57607-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="57607-192">Novērtējuma (demonstrācijas/testa) vidēm jāreģistrē mēroga vienību savienotāja programma \<application ID\> galvenajā birojā.</span><span class="sxs-lookup"><span data-stu-id="57607-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="57607-193">Ja CSU inicializācija neizdodas un saņemat šo kļūdas ziņojumu, pierakstiet programmas ID, kas ir vispārēji unikāls identifikators (GUID), un pēc tam izpildiet nākamajā sadaļā norādītās darbības, lai reģistrētu CSU izvietošanas programmu komponentā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="57607-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="57607-194">CSU izvietošanas programmas reģistrācija Commerce Headquarters (ja nepieciešams)</span><span class="sxs-lookup"><span data-stu-id="57607-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="57607-195">Lai reģistrētu CSU izvietošanas programmu Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57607-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="57607-196">Komponentā Commerce Headquarters dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Azure Active Directory programmas**.</span><span class="sxs-lookup"><span data-stu-id="57607-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="57607-197">Kolonnā **Klienta ID** ievadiet programmas ID no saņemtā CSU inicializēšanas kļūdas ziņojuma.</span><span class="sxs-lookup"><span data-stu-id="57607-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="57607-198">Kolonnā **Nosaukums** ievadiet jebkādu apraksta tekstu (piemēram, **CSU novērtējums**).</span><span class="sxs-lookup"><span data-stu-id="57607-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="57607-199">Kolonnā **Lietotāja ID** ievadiet **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="57607-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="57607-200">Atkārtoti mēģiniet CSU inicializāciju un izvietošanu no LCS.</span><span class="sxs-lookup"><span data-stu-id="57607-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="57607-201">E-tirdzniecības inicializēšana</span><span class="sxs-lookup"><span data-stu-id="57607-201">Initialize e-Commerce</span></span>

<span data-ttu-id="57607-202">Lai inicializētu e-tirdzniecību, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="57607-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="57607-203">Cilnē **E-tirdzniecība** pārskatiet piekrišanu novērtējumam un pēc tam atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="57607-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="57607-204">Laukā **E-tirdzniecības novērtējuma nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="57607-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="57607-205">Ņemiet vērā, ka šis nosaukums parādīsies dažos URL vietrāžos, kas norāda uz jūsu e-tirdzniecības instanci.</span><span class="sxs-lookup"><span data-stu-id="57607-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="57607-206">Laukā **Commerce Scale Unit nosaukums** atlasiet savu CSU.</span><span class="sxs-lookup"><span data-stu-id="57607-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="57607-207">(Sarakstā jābūt tikai vienai opcijai.)</span><span class="sxs-lookup"><span data-stu-id="57607-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="57607-208">Lauks **E-tirdzniecības ģeogrāfija** tiek iestatīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="57607-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="57607-209">Lai turpinātu, atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="57607-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="57607-210">Laukā **Atbalstītie resursdatora nosaukumi** ievadiet jebkuru derīgu domēnu, piemēram, `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="57607-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="57607-211">Laukā **Sistēmas administratora AAD drošības grupa** ievadiet tās drošības grupas nosaukuma pirmos dažus burtus, ko vēlaties izmantot, un pēc tam atlasiet lupas simbolu, lai skatītu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="57607-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="57607-212">Sarakstā atlasiet pareizo drošības grupu.</span><span class="sxs-lookup"><span data-stu-id="57607-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="57607-213">Laukā **Vērtējumu un pārskatu moderatora AAD drošības grupa** ievadiet tās drošības grupas nosaukuma pirmos dažus burtus, ko vēlaties izmantot, un pēc tam atlasiet lupas simbolu, lai skatītu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="57607-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="57607-214">Sarakstā atlasiet pareizo drošības grupu.</span><span class="sxs-lookup"><span data-stu-id="57607-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="57607-215">Atstājiet opciju **Iespējot vērtējumu un pārskatu pakalpojumu** iestatītu uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="57607-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="57607-216">Atlasiet **Inicializēt**.</span><span class="sxs-lookup"><span data-stu-id="57607-216">Select **Initialize**.</span></span> <span data-ttu-id="57607-217">**Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **e-komercija**.</span><span class="sxs-lookup"><span data-stu-id="57607-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="57607-218">Ir uzsākta e-tirdzniecības inicializēšana.</span><span class="sxs-lookup"><span data-stu-id="57607-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="57607-219">Pirms turpināt, uzgaidiet, līdz e-tirdzniecības inicializācijas statuss ir **Inicializācija veiksmīga**.</span><span class="sxs-lookup"><span data-stu-id="57607-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="57607-220">Apakšā pa labi no **Saites** norakstiet URL tālāk noradītajām saitēm.</span><span class="sxs-lookup"><span data-stu-id="57607-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="57607-221">**E-tirdzniecības vietne** — saite uz jūsu e-tirdzniecības vietnes sakni.</span><span class="sxs-lookup"><span data-stu-id="57607-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="57607-222">**Commerce vietņu veidotājs** – saite uz vietnes pārvaldības rīku.</span><span class="sxs-lookup"><span data-stu-id="57607-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="57607-223">Turpmākās darbības</span><span class="sxs-lookup"><span data-stu-id="57607-223">Next steps</span></span>

<span data-ttu-id="57607-224">Lai turpinātu nodrošināšanas procesu un konfigurētu Commerce novērtējuma vidi, skatiet sadaļu [Commerce novērtējuma vides konfigurācija](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="57607-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57607-225">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="57607-225">Additional resources</span></span>

[<span data-ttu-id="57607-226">Dynamics 365 Commerce novērtējuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="57607-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="57607-227">Dynamics 365 Commerce novērtējuma vides konfigurācija</span><span class="sxs-lookup"><span data-stu-id="57607-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="57607-228">BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="57607-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="57607-229">Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="57607-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="57607-230">Bieži uzdotie jautājumi par Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="57607-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="57607-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="57607-231">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="57607-232">Commerce Scale Unit (mākonis)</span><span class="sxs-lookup"><span data-stu-id="57607-232">Commerce Scale Unit (cloud)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="57607-233">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="57607-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="57607-234">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="57607-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]