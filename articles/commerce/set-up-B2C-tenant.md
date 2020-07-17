---
title: B2C nomnieka iestatīšana programmā Commerce
description: Šajā tēmā aprakstīts, kā iestatīt Azure Active Directory (Azure AD) biznesa-patērētāju (B2C) nomniekus lietotāja vietas autentifikācijai sistēmā Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: b017b0f91960be1504134f6d46878fce956de203
ms.sourcegitcommit: 8a1621327568edf49758b70964e0a3e637527e1b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2020
ms.locfileid: "3497172"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="ae5aa-103">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="ae5aa-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae5aa-104">Šajā tēmā aprakstīts, kā iestatīt Azure Active Directory (Azure AD) biznesa-patērētāju (B2C) nomniekus lietotāja vietas autentifikācijai sistēmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ae5aa-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ae5aa-105">Overview</span></span>

<span data-ttu-id="ae5aa-106">Dynamics 365 Commerce izmanto Azure AD B2C, lai atbalstītu lietotāja akreditācijas datus un autentifikācijas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="ae5aa-107">Lietotājs var pieteikties, pierakstīties un atiestatīt savu paroli, izmantojot šīs plūsmas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="ae5aa-108">Azure AD B2C saglabā lietotāja sensitīvo autentifikācijas informāciju, piemēram, lietotāja vārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="ae5aa-109">Lietotāja ieraksts B2C nomniekā saglabās vai nu B2C lokālā konta ierakstu, vai arī B2C sociālā identitātes nodrošinātāja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="ae5aa-110">Šie B2C ieraksti tiks saistīti ar klienta ierakstu tirdzniecības vidē.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="ae5aa-111">Izveidot vai saistīt ar esošo AAD B2C nomnieku Azure portālā</span><span class="sxs-lookup"><span data-stu-id="ae5aa-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="ae5aa-112">Pierakstieties [Azure portālā](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ae5aa-113">No Azure portāla izvēlnes atlasiet **Izveidot resursu**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="ae5aa-114">Noteikti izmantojiet abonementu un direktoriju, kas tiks savienots ar jūsu komercijas vidi.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Resursa izveide Azure portālā](./media/B2CImage_1.png)

1. <span data-ttu-id="ae5aa-116">Doties uz **Identitātes \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="ae5aa-117">Kad atrodaties lapā **Izveidot jaunu B2C nomnieku vai saistīt uz esošo nomnieku**, izmantojiet vienu no zemāk norādītajām opcijām, kas vislabāk atbilst jūsu uzņēmuma vajadzībām:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="ae5aa-118">**Izveidot jaunu Azure AD B2C nomnieku**: lietojiet šo opciju, lai izveidotu jaunu AAD B2C nomnieku.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="ae5aa-119">Atlasiet **Izveidot jaunu Azure AD B2C nomnieku**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="ae5aa-120">Sadaļā **Organizācijas nosaukums** ievadiet organizācijas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="ae5aa-121">Sadaļā **Sākotnējais domēna nosaukums** ievadiet sākotnējo domēna nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="ae5aa-122">Sadaļā **Valsts vai reģions** atlasiet valsti vai reģionu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="ae5aa-123">Atlasiet **Izveidot**, lai izveidotu nomnieku.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-123">Select **Create** to create the tenant.</span></span>

     ![Izveidot jaunu Azure AD nomnieku](./media/B2CImage_2.png)

     - <span data-ttu-id="ae5aa-125">**Saistīt esošu Azure AD B2C nomnieku uz manu Azure abonementu**: lietojiet šo opciju, ja jums jau ir Azure AD B2C nomnieks, ar kuru vēlaties veidot saiti.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="ae5aa-126">Atlasiet **Saistīt esošu Azure AD B2C nomnieku uz manu Azure abonementu**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="ae5aa-127">Sadaļā **Azure AD B2C nomnieks**atlasiet atbilstošo B2C nomnieku.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="ae5aa-128">Ja atlasīšanas lodziņā tiek parādīts ziņojums "Nevar atrast piemērotus B2C nomniekus", jums nav esoša piemērota B2C nomnieka, un jums būs jāizveido jauns.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="ae5aa-129">Sadaļā **Resursu grupa** atlasiet **Izveidot jaunu**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="ae5aa-130">Ievadiet **Nosaukumu** resursu grupai, kurā būs nomnieks, atlasiet **Resursu grupas atrašanās vietu** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Saistīt esošu Azure AD B2C nomnieku uz Azure abonementu](./media/B2CImage_3.png)

1. <span data-ttu-id="ae5aa-132">Kad tiek izveidots jauns Azure AD B2C direktorijs (tas var ilgt kādu brīdi), saite uz jauno direktoriju parādīsies informācijas panelī.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="ae5aa-133">Šī saite novirzīs jūs uz lapu "Laipni lūdzam Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="ae5aa-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Saite uz jaunu AAD direktoriju](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="ae5aa-135">Ja jūsu Azure kontā ir vairāki abonementi vai arī esat iestatījis B2C nomnieku, neveidojot saiti uz aktīvu abonementu, reklāmkarogs **Problēmu novēršana** jūs novirzīs, lai palīdzētu saistīt nomnieku ar abonementu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="ae5aa-136">Atlasiet problēmu novēršanas ziņojumu un izpildiet norādījumus, lai atrisinātu abonementa problēmu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="ae5aa-137">Šis attēls rāda Azure AD B2C **Problēmu novēršanas** reklāmkaroga piemēru.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Brīdinājumam, kas rāda direktoriju, nav aktīva abonementa](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="ae5aa-139">Izveidot B2C pieteikumu</span><span class="sxs-lookup"><span data-stu-id="ae5aa-139">Create the B2C application</span></span>

<span data-ttu-id="ae5aa-140">Kad B2C nomnieks ir izveidots, jūs izveidosiet B2C pieteikumu nomniekam, lai mijiedarbotos ar tirdzniecības darbībām.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="ae5aa-141">Lai izveidotu B2C pieteikumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-142">Azure portālā atlasiet **Pieteikumi** un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="ae5aa-143">Zem sadaļas **Nosaukums** ievadiet vēlamo AAD B2C pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="ae5aa-144">Sadaļā **Tīmekļa lietojumprogramma/Tīmekļa API** opcijai **Iekļaut tīmekļa programmu/Tīmekļa API** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="ae5aa-145">Opcijai **Atļaut netiešu plūsmu** atlasiet **Jā** (noklusējuma vērtība).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="ae5aa-146">Sadaļā **Atbildes vietrāži URL** ievadiet savus atvēlētos atbildes vietrāžus URL.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="ae5aa-147">Skatiet [Atbildes vietrāži URL](#reply-urls), lai iegūtu informāciju par atbildes vietrāžiem URL un to, kā tos šeit formatēt.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="ae5aa-148">Opcijai **Iekļaut vietējo klientu** izvēlieties **Nē** (noklusējuma vērtība).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="ae5aa-149">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="ae5aa-150">Atbilžu vietrāži URL</span><span class="sxs-lookup"><span data-stu-id="ae5aa-150">Reply URLs</span></span>

<span data-ttu-id="ae5aa-151">Atbilžu vietrāži URL ir svarīgi, jo tie nodrošina atgriešanās domēnus iekļaut sarakstā, kad jūsu vietne Azure AD B2C pieprasa autentificēt lietotāju.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="ae5aa-152">Tas ļauj atgriezt autentificētu lietotāju atpakaļ domēnā, no kura tie piesakās sistēmā (jūsu vietnes domēns).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="ae5aa-153">Lodziņā **Atbilžu vietrāži URL** ekrānā **Azure AD B2c - Applications \>Jauna programma** jums ir jāpievieno atsevišķas rindas gan jūsu vietnes domēnam, gan (tiklīdz jūsu vide ir nodrošināta) komercijas ģenerētajam vietrādim URL.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="ae5aa-154">Šiem URL vienmēr ir jāizmanto derīgs URL formāts, un tiem ir jābūt tikai pamata URL (bez slīpsvītrām vai ceļiem).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="ae5aa-155">Pēc tam ``/_msdyn365/authresp`` virkne ir jāpievieno pamata URL, kā tas ir sekojošajos piemēros.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="ae5aa-156">``https://www.fabrikam.com/_msdyn365/authresp`` (Domēnam ir pilnībā jāatbilst e-komercijas domēnam.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-156">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="ae5aa-157">Ja izmantojat vairākus domēnus, šis URL ir jāpievieno katram domēnam.)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-157">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="ae5aa-158">Lietotāja plūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="ae5aa-158">Create user flow policies</span></span>

<span data-ttu-id="ae5aa-159">Lietotājas plūsmas ir politika, ko Azure AD B2C izmanto, lai nodrošinātu drošu pieteikšanos sistēmā, pierakstītos, rediģētu profilu un aizmirstas paroles gadījumos.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-159">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="ae5aa-160">Dynamics 365 Commerce izmanto šīs plūsmas, lai veiktu politikas darbības, lai mijiedarbotos ar Azure AD B2C nomnieku.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-160">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="ae5aa-161">Kad lietotājs mijiedarbojas ar šīm politikām, tās tiek novirzītas uz Azure AD B2C nomnieku, lai veiktu darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-161">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="ae5aa-162">Azure AD B2C sniedz trīs pamata lietotāju plūsmas tipus:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-162">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="ae5aa-163">Pierakstīties un pieteikties</span><span class="sxs-lookup"><span data-stu-id="ae5aa-163">Sign up and sign in</span></span>
- <span data-ttu-id="ae5aa-164">Profila labošana</span><span class="sxs-lookup"><span data-stu-id="ae5aa-164">Profile editing</span></span>
- <span data-ttu-id="ae5aa-165">Paroles atiestatīšana</span><span class="sxs-lookup"><span data-stu-id="ae5aa-165">Password reset</span></span>

<span data-ttu-id="ae5aa-166">Varat izvēlēties izmantot Azure AD nodrošinātas noklusējuma lietotāja plūsmas, kas parādīs AAD B2C viesotu lapu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-166">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="ae5aa-167">Līdzīgi varat izveidot HTML lapu, lai kontrolētu šo lietotāju plūsmas pieredzes izskatu un iespaidu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-167">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="ae5aa-168">Lai pielāgotu lietotāja politikas lapas Dynamics 365 Commerce, skatiet sadaļu [Pielāgotu lapu iestatīšana lietotāju pieteikšanās tiesībām](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-168">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="ae5aa-169">Papildinformāciju skatiet sadaļā [Lietotāja pieredzes interfeisa pielāgošana Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-169">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="ae5aa-170">Izveidot pierakstīšanos un pieteikties lietotāja plūsmas politikā</span><span class="sxs-lookup"><span data-stu-id="ae5aa-170">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="ae5aa-171">Lai izveidotu Parakstīšanos un pierakstīšanos lietotāja plūsmā politiku, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-171">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-172">Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-172">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="ae5aa-173">Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-173">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="ae5aa-174">Cilnē **Ieteicams** izvēlieties **Pierakstīties un pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-174">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="ae5aa-175">Sadaļā **Nosaukums** ievadiet politikas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-175">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="ae5aa-176">Pēc tam šis nosaukums tiks parādīts ar prefiksu, kuru portāls piešķir (piemēram, "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="ae5aa-176">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="ae5aa-177">Sadaļā **Identitātes nodrošinātāji** atzīmējiet atbilstošo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-177">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="ae5aa-178">Saskaņā ar **Daudzfaktoru autentifikāciju** atlasiet atbilstošo jūsu uzņēmuma izvēli.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-178">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="ae5aa-179">Sadaļā **Lietotāja atribūti un prasības** atlasiet opcijas, lai apkopotu atbilstošos atribūtus vai atgriešanas prasības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-179">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="ae5aa-180">Commerce ir nepieciešamas šādas noklusējuma opcijas:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-180">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="ae5aa-181">**Savākt atribūtu**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-181">**Collect  attribute**</span></span> | <span data-ttu-id="ae5aa-182">**Atgriešanas prasība**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-182">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="ae5aa-183">E-pasta adrese</span><span class="sxs-lookup"><span data-stu-id="ae5aa-183">Email Address</span></span>          | <span data-ttu-id="ae5aa-184">E-pasta adreses</span><span class="sxs-lookup"><span data-stu-id="ae5aa-184">Email Addresses</span></span>   |
    | <span data-ttu-id="ae5aa-185">Norādītais nosaukums</span><span class="sxs-lookup"><span data-stu-id="ae5aa-185">Given Name</span></span>             | <span data-ttu-id="ae5aa-186">Norādītais nosaukums</span><span class="sxs-lookup"><span data-stu-id="ae5aa-186">Given Name</span></span>        |
    |                        | <span data-ttu-id="ae5aa-187">Identitātes nodrošinātājs</span><span class="sxs-lookup"><span data-stu-id="ae5aa-187">Identity Provider</span></span> |
    | <span data-ttu-id="ae5aa-188">Uzvārds</span><span class="sxs-lookup"><span data-stu-id="ae5aa-188">Surname</span></span>                | <span data-ttu-id="ae5aa-189">Uzvārds</span><span class="sxs-lookup"><span data-stu-id="ae5aa-189">Surname</span></span>           |
    |                        | <span data-ttu-id="ae5aa-190">Lietotāja objekta ID</span><span class="sxs-lookup"><span data-stu-id="ae5aa-190">User’s Object ID</span></span>  |

1. <span data-ttu-id="ae5aa-191">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-191">Select **Create**.</span></span>

<span data-ttu-id="ae5aa-192">Tālāk minētais attēls ir Azure AD B2C reģistrācijas un pieteikšanās piemērs lietotāja plūsmā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-192">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Parakstīšanās un pieteikšanās politikas iestatījumi](./media/B2CImage_11.png)

<span data-ttu-id="ae5aa-194">Sekojošajā attēlā ir parādīta opcija **Palaist lietotāja plūsmu** no Azure AD B2C pierakstīšanās un pieteikšanās lietotāja plūsmā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-194">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Izpildīt lietotāja plūsmas opciju politikas plūsmā](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="ae5aa-196">Izveidot profila rediģēšanas lietotāja plūsmas politiku</span><span class="sxs-lookup"><span data-stu-id="ae5aa-196">Create a profile editing user flow policy</span></span>

<span data-ttu-id="ae5aa-197">Lai izveidotu profila rediģēšanas lietotāja plūsmas politiku, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-197">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-198">Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-198">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="ae5aa-199">Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-199">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="ae5aa-200">Cilnē **Ieteicams** atlasiet **Profilu rediģēšana**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-200">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="ae5aa-201">Sadaļā **Nosaukums** ievadiet profila rediģēšanas lietotāja plūsmu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-201">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="ae5aa-202">Pēc tam šis nosaukums tiks parādīts ar prefiksu, kuru portāls piešķir (piemēram, "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="ae5aa-202">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="ae5aa-203">Sadaļā **Identitātes nodrošinātāji** atlasiet **Lokālā konta pierakstīšanās**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-203">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="ae5aa-204">Sadaļā **Lietotāja atribūti** atlasiet kādu no tālāk norādītajām izvēles rūtiņām:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-204">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="ae5aa-205">**E-pasta adreses** (tikai **Atgriešanas prasība**)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-205">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="ae5aa-206">**Norādītais nosaukums** (**Savākt atribūtu** un **Atgriešanas prasība**)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-206">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="ae5aa-207">**Identitātes nodrošinātājs** (tikai **Atgriešanas prasība**)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-207">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="ae5aa-208">**Uzvārds** (**Savākt atribūtu** un **Atgriešanas prasība**)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-208">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="ae5aa-209">**Lietotāja objekta ID** (tikai **Atgriešanas prasība**)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-209">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="ae5aa-210">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-210">Select **Create**.</span></span>

<span data-ttu-id="ae5aa-211">Sekojošajā attēlā parādīts piemērs ar Azure AD B2C profila rediģēšanas lietotāja plūsmu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-211">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Izveidot profila rediģēšanas lietotāja plūsmu](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="ae5aa-213">Izveidot paroles atiestatīšanas lietotāja plūsmas politiku</span><span class="sxs-lookup"><span data-stu-id="ae5aa-213">Create a password reset user flow policy</span></span>

<span data-ttu-id="ae5aa-214">Lai izveidotu paroles atiestatīšanas lietotāja plūsmas politiku, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-214">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-215">Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-215">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="ae5aa-216">Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-216">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="ae5aa-217">Cilnē **Ieteicams** atlasiet **Paroles atiestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-217">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="ae5aa-218">Sadaļā **Nosaukums** ievadiet paroles atiestatīšanas lietotāja plūsmas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-218">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="ae5aa-219">Sadaļā **Identitātes nodrošinātāji** atlasiet **Atiestatīt paroli, izmantojot e-pasta adresi**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-219">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="ae5aa-220">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-220">Select **Create**.</span></span>
1. <span data-ttu-id="ae5aa-221">Sadaļā **Pieteikumu prasības** atlasiet kādu no tālāk norādītajām izvēles rūtiņām:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-221">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="ae5aa-222">**E-pasta adreses**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-222">**Email addresses**</span></span>
    - <span data-ttu-id="ae5aa-223">**Norādītais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-223">**Given Name**</span></span>
    - <span data-ttu-id="ae5aa-224">**Uzvārds**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-224">**Surname**</span></span>
    - <span data-ttu-id="ae5aa-225">**Lietotāja objekta ID**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-225">**User's Object ID**</span></span>
1. <span data-ttu-id="ae5aa-226">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-226">Select **Create**.</span></span>

<span data-ttu-id="ae5aa-227">Sekojošajā attēlā parādīts, kur iestatīt **Atiestatīšanas paroli, izmantojot pasta adresi** Azure AD B2C paroles atiestatīšanas lietotāja plūsmā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-227">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Iestatiet "Atiestatīt paroli, izmantojot pasta adresi" paroles atiestatīšanas politikā](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="ae5aa-229">Pievienot sociālās identitātes sniedzējus (pēc izvēles)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-229">Add social identity providers (Optional)</span></span>

<span data-ttu-id="ae5aa-230">Sociālās identitātes nodrošinātāji ļauj lietotājiem izmantot savu sociālā konta autentifikāciju.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-230">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="ae5aa-231">Sociālās identitātes nodrošinātāja autentifikācijas pievienošana nav obligāta risinājumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-231">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="ae5aa-232">Ja nav pievienota sociālā identitātes nodrošinātāja autentifikācija, noklusējuma Azure AD B2C profili būs galvenie profili jūsu lietotāja bāzei.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-232">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="ae5aa-233">Lietotāji atlasīs savu lietotājvārdu (viņu vēlamo e-pasta adresi) un iestatīs paroli.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-233">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="ae5aa-234">Azure AD B2C lietotājiem tiks autentificēti tieši.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-234">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="ae5aa-235">Ja tiek pievienota sociālā identitātes nodrošinātāja autentifikācija un lietotājs izvēlas vienu no piedāvātajiem sociālās identitātes nodrošinātājiem, tas joprojām ir izveidots ar Azure AD B2C nomniekā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-235">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="ae5aa-236">Pēc tam Azure AD B2C autentificēs lietotāja akreditācijas datus ar sociālās identitātes nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-236">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="ae5aa-237">Identitātes nodrošinātāja žurnāls izveido ierakstu B2C nomniekā, bet citā formātā, nekā Lokālais konts, jo tas izsauc ārējās sociālās identitātes sniedzēja atsauci autentifikācijai.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-237">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="ae5aa-238">Lietotājs var izmantot vienu un to pašu e-pasta adresi sociālo identitātes nodrošinātāju starpā, kas nozīmē, ka Autentifikācijai izmantotais e-pasta lietotājvārds var nebūt unikāls nomniekam.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-238">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="ae5aa-239">Azure AD B2C tikai realizēs to, ka lietotājiem ir unikāla e-pasta adrese vietējos B2C kontos.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-239">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="ae5aa-240">Pirms jūs varat pievienot sociālās identitātes nodrošinātāju autentifikācijai, jums ir jādodas uz identitātes nodrošinātāja portālu un jāiestata identitātes nodrošinātāja programma, kā norādīts Azure AD B2C dokumentācijā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-240">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="ae5aa-241">Tālāk ir sniegts saraksts ar saitēm uz dokumentāciju.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-241">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="ae5aa-242">Amazon</span><span class="sxs-lookup"><span data-stu-id="ae5aa-242">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="ae5aa-243">Azure AD (Viens nomnieks)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-243">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="ae5aa-244">Microsoft konts</span><span class="sxs-lookup"><span data-stu-id="ae5aa-244">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="ae5aa-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="ae5aa-245">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="ae5aa-246">GitHub</span><span class="sxs-lookup"><span data-stu-id="ae5aa-246">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="ae5aa-247">Google</span><span class="sxs-lookup"><span data-stu-id="ae5aa-247">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="ae5aa-248">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="ae5aa-248">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="ae5aa-249">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="ae5aa-249">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="ae5aa-250">Twitter</span><span class="sxs-lookup"><span data-stu-id="ae5aa-250">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="ae5aa-251">Pievienot un iestatīt sociālās identitātes nodrošinātāju</span><span class="sxs-lookup"><span data-stu-id="ae5aa-251">Add and set up a social identity provider</span></span>

<span data-ttu-id="ae5aa-252">Lai pievienotu un iestatītu sociālās identitātes nodrošinātāju, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-252">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="ae5aa-253">Azure portālā dodieties uz **Identitātes nodrošinātājiem**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-253">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="ae5aa-254">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-254">Select **Add**.</span></span> <span data-ttu-id="ae5aa-255">Parādās ekrāns **Pievienot identitātes nodrošinātāju**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-255">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="ae5aa-256">Sadaļā **Nosaukums** ievadiet nosaukumu, kas jāparāda lietotājiem jūsu pieteikšanās ekrānā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-256">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="ae5aa-257">Sadaļā **Identitātes nodrošinātāja tips** no saraksta atlasiet identitātes nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-257">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="ae5aa-258">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-258">Select **OK**.</span></span>
1. <span data-ttu-id="ae5aa-259">Atlasiet **Iestatīt šo identitātes nodrošinātāju**, lai piekļūtu ekrānam **Iestatīt sociālās identitātes nodrošinātāja**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-259">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="ae5aa-260">Sadaļā **Klienta ID** ievadiet klienta ID, kas iegūts no identitātes nodrošinātāja programmas uzstādīšanas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-260">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="ae5aa-261">Sadaļā **Klienta slepenā atslēga** ievadiet klienta slepeno atslēgu, kas iegūts no identitātes nodrošinātāja programmas uzstādīšanas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-261">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="ae5aa-262">Pievienojiet lietotāja plūsmu žurnālam piesakieties politikām:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-262">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="ae5aa-263">Doties uz **Azure AD B2C — lietotāja plūsmas (politikas) \>{jūsu pierakstīšanās/pieteikšanās politika}\>identitātes nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-263">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="ae5aa-264">Lai pievienotu pieteikšanos/pierakstīšanos lietotāja plūsmas politikai, atlasiet katru identitātes nodrošinātāju, ko esat iestatījis savam kontam.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-264">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="ae5aa-265">Lai pārbaudītu tos, atlasiet **Palaist lietotāja plūsmu** katram identitātes nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-265">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="ae5aa-266">Jauna cilne parādīs pieteikšanās lapu, parādot jauno identitātes nodrošinātāju atlases lodziņu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-266">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="ae5aa-267">Sekojošajā attēlā ir redzami **Pievienot identitātes nodrošinātāju** un **Uzstādīt sociālo identitātes nodrošinātāju** ekrāna piemēri Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-267">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Sociālās identitātes nodrošinātāja pievienošana jūsu aplikācijai](./media/B2CImage_14.png)

<span data-ttu-id="ae5aa-269">Sekojošajā attēlā parādīts piemērs, kā atlasīt identitātes nodrošinātājus Azure AD B2C **Identitātes nodrošinātāju** lapā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-269">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Atlasiet katru Sociālā identitātes nodrošinātāju, lai iespējotu politiku](./media/B2CImage_16.png)

<span data-ttu-id="ae5aa-271">Sekojošajā attēlā parādīts noklusējuma pierakstīšanās ekrāna piemērs, kurā ir parādīts sociālās identitātes nodrošinātāja pierakstīšanās poga.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-271">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Tiek parādīts noklusētais pieteikšanās ekrāns ar sociālās identitātes nodrošinātāja pierakstīšanās pogu](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="ae5aa-273">Atjaunināt Commerce Headquarters ar jauno Azure AD B2C informāciju</span><span class="sxs-lookup"><span data-stu-id="ae5aa-273">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="ae5aa-274">Pēc tam, kad iepriekšminētās Azure AD B2C nodrošināšanas darbības ir pabeigtas, Azure AD B2C lietojumprogrammai ir jābūt reģistrētai jūsu Dynamics 365 Commerce vidē.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-274">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="ae5aa-275">Lai atjauninātu programmu Headquarters ar jauno Azure AD B2C informāciju, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-275">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-276">Programmā Commerce dodieties uz **Commerce koplietotie parametri** un atlasiet **Identitātes nodrošinātāji** kreisajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-276">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="ae5aa-277">Sadaļā **identitātes nodrošinātāji**veiciet sekojošās darbības:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-277">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="ae5aa-278">Lodziņā **Izdevējs** ievadiet identitātes nodrošinātāja izdevēja URL.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-278">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="ae5aa-279">Lai atrastu savu izdevēja URL, zemāk skatiet [Iegūt izdevēja URL](#obtain-issuer-url).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-279">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="ae5aa-280">Lodziņā **Nosaukums** ievadiet izdevēja ieraksta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-280">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="ae5aa-281">Lodziņā **Veids** ievadiet **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-281">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="ae5aa-282">Sadaļā **Pārbaudītāji** ar iepriekš atlasīto B2C identitātes nodrošinātāja vienumu rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="ae5aa-282">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="ae5aa-283">Lodziņā **ClientID** ievadiet savu B2C programmas ID.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-283">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="ae5aa-284">To varat atrast jūsu B2C programmas rekvizītu lapas lodziņā **Programmas ID**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-284">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="ae5aa-285">Lodziņā **Veids** ievadiet **Publisks**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-285">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="ae5aa-286">Lodziņā **Lietotāja veids** ievadiet **Pircējs**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-286">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="ae5aa-287">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-287">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="ae5aa-288">Lodziņā Commerce Search meklējiet **Sadales grafiku**</span><span class="sxs-lookup"><span data-stu-id="ae5aa-288">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="ae5aa-289">Lapas **Sadales grafiki** kreisajā navigācijas izvēlnē atlasiet darbu **1110 globālā konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-289">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="ae5aa-290">Darbību rūtī atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-290">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="ae5aa-291">Iegūt izdevēja URL</span><span class="sxs-lookup"><span data-stu-id="ae5aa-291">Obtain issuer URL</span></span>

<span data-ttu-id="ae5aa-292">Lai iegūtu identitātes nodrošinātāja izdevēja URL, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-292">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-293">Izveidot metadatu adreses URL šādā formātā, izmantojot B2C nomnieku un politiku:``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="ae5aa-293">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="ae5aa-294">Piemērs: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-294">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="ae5aa-295">Ievadiet metadatu adreses URL pārlūkprogrammas adreses joslā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-295">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="ae5aa-296">Metadatos kopējiet identitātes nodrošinātāja izdevēja URL ( **"izdevēja"** vērtība).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-296">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="ae5aa-297">Piemērs: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-297">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="ae5aa-298">Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā</span><span class="sxs-lookup"><span data-stu-id="ae5aa-298">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="ae5aa-299">Kad jūsu Azure AD B2C nomnieka iestatīšana ir pabeigta, jums ir jākonfigurē B2C nomnieks Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-299">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="ae5aa-300">Konfigurēšanas soļi ietver B2C lietojumprogrammas informācijas vākšanu no Azure portāla, ievadot šo B2C lietojumprogrammas informāciju vietņu veidotājā un pēc tam asociējot B2C programmu ar jūsu vietni un kanālu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-300">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="ae5aa-301">Apkopot nepieciešamo programmas informāciju</span><span class="sxs-lookup"><span data-stu-id="ae5aa-301">Collect the required application information</span></span>

<span data-ttu-id="ae5aa-302">Lai apkopotu nepieciešamo informāciju par programmu, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-302">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-303">Azure portālā dodieties uz **Sākumlapa\>Azure AD B2C - lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-303">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="ae5aa-304">Atlasiet programmu un pēc tam kreisās puses navigācijas rūtī atlasiet **Rekvizīti**, lai iegūtu detalizētu informāciju par programmu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-304">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="ae5aa-305">Lodziņā **Programmas ID** savāciet B2C programmas ID, kas izveidots jūsu B2C nomniekam.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-305">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="ae5aa-306">Tas vēlāk tiks ievadīts kā **Klienta GUID** vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-306">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="ae5aa-307">Sadaļā **Atbildes vietrāži URL** savāciet atbildes vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-307">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="ae5aa-308">Dodieties uz **Sākumlapa \>Azure AD B2C — lietotāju plūsmas (politikas)** un pēc tam savāciet katra lietotāja plūsmas politikas nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-308">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="ae5aa-309">Sekojošajā attēlā ir parādīts **Azure AD B2C - lietojumprogrammas** lapas piemērs.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-309">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Pāriet uz B2C programmu jūsu nomniekā](./media/B2CImage_19.png)

<span data-ttu-id="ae5aa-311">Sekojošajā attēlā ir parādīts lietojumprogrammas **Rekvizīti** lapas piemērs Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-311">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Kopējiet Lietojumprogrammas ID no B2C lietojumprogrammas rekvizītiem](./media/B2CImage_21.png)

<span data-ttu-id="ae5aa-313">Sekojošajā attēlā ir parādīts lietotāja plūsmas politikas piemērs, kas norādīts **Azure AD B2C — lietotāja plūsmas (politikas)** lapā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-313">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Apkopot katras B2C politikas plūsmas nosaukumus](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="ae5aa-315">Ievadiet savu AAD B2C nomnieka lietojumprogrammas informāciju Commerce</span><span class="sxs-lookup"><span data-stu-id="ae5aa-315">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="ae5aa-316">Jums jāievada Azure AD B2C nomnieka informācija Commerce vietņu veidotājā, pirms asociējat B2C nomnieku ar jūsu vietnēm.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-316">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="ae5aa-317">Lai pievienotu savu AAD B2C nomnieka lietojumprogrammas informāciju Commerce, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-317">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-318">Piesakieties kā administrators Commerce vietņu veidotājā jūsu videi.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-318">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="ae5aa-319">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-319">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="ae5aa-320">Sadaļā **Nomnieka iestatījumi** atlasiet **B2C iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-320">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="ae5aa-321">Galvenajā logā blakus **B2C lietojumprogrammas** atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-321">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="ae5aa-322">(Ja jūsu nomnieks parādās B2C lietojumprogrammu sarakstā, tad administrators to jau ir pievienojis.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-322">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="ae5aa-323">Pārbaudiet, vai vienumi 6. solī atbilst jūsu B2C lietojumprogrammai.)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-323">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="ae5aa-324">Atlasiet **Pievienot B2C lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-324">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="ae5aa-325">Veidlapā ievadiet tālāk norādītos pieprasītos vienumus, izmantojot vērtības no jūsu B2C nomnieka un lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-325">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="ae5aa-326">Lauki, kas nav nepieciešami (bez zvaigznītes), var tikt atstāti tukši.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-326">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="ae5aa-327">**Lietojumprogrammas nosaukums**: jūsu B2C lietojumprogrammas nosaukums, piemēram, "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="ae5aa-327">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="ae5aa-328">**Nomnieka nosaukums**: jūsu B2C nomnieka nosaukums (piemēram, izmantot "fabrikam", ja domēns parādās kā "fabrikam.onmicrosoft.com" B2C nomniekam).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-328">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="ae5aa-329">**Aizmirstas paroles politikas ID**: aizmirstas paroles lietotāja plūsmas politikas ID, piemēram, "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="ae5aa-329">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="ae5aa-330">**Pierakstīšanās pieteikšanās politikas ID**: pierakstīšanās un pieteikšanās lietotāja plūsmas politikas ID, piemēram, "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="ae5aa-330">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="ae5aa-331">**Klienta GUID**: B2C lietojumprogrammas ID, piemēram, "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="ae5aa-331">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="ae5aa-332">**Rediģēt profila politikas ID**: profila rediģēšanas lietotāja plūsmas politikas ID, piemēram, "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="ae5aa-332">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="ae5aa-333">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-333">Select **OK**.</span></span> <span data-ttu-id="ae5aa-334">Tagad jums ir jāredz jūsu B2C lietojumprogrammas nosaukums, kas parādās sarakstā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-334">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="ae5aa-335">Atlasiet **Saglabāt**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-335">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="ae5aa-336">Saistīt B2C lietojumprogrammu ar jūsu vietni un kanālu</span><span class="sxs-lookup"><span data-stu-id="ae5aa-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="ae5aa-337">Ja jūsu vietne jau ir saistīta ar B2C lietojumprogrammu, pārejot uz citu B2C programmu, tiks noņemtas pašreizējās atsauces, kas izveidotas lietotājiem, kas jau ir reģistrējušies šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="ae5aa-338">Ja tas tiks mainīts, visi akreditācijas dati, kas ir saistīti ar pašlaik piešķirto B2C lietojumprogrammu, lietotājiem nebūs pieejami.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="ae5aa-339">Atjauniniet tikai B2C lietojumprogrammu, ja kanāla B2C lietojumprogrammu iestatāt pirmo reizi vai vēlaties, lai lietotāji atkārtoti pierakstītos ar jauniem akreditācijas datiem šajā kanālā ar jauno B2C lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="ae5aa-340">Esiet piesardzīgs, saistot kanālus ar B2C lietojumprogrammām, un skaidri nosauciet lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="ae5aa-341">Ja kanāls nav saistīts ar B2C programmu tālāk norādītajās darbībās, lietotāji, kas piesakās šajā kanālā jūsu vietnei, tiks ievadīti B2C programmā, kas tiek parādīta kā **Noklusējums** **Nomnieka iestatījumi \>B2C iestatījumi** B2C lietojumprogrammu saraksts.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="ae5aa-342">Lai saistītu B2C lietojumprogrammu ar jūsu vietni un kanālu, sekojiet šīm darbībām,</span><span class="sxs-lookup"><span data-stu-id="ae5aa-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="ae5aa-343">Dodieties uz savu vietni Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="ae5aa-344">Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="ae5aa-345">Zem **Vietas iestatījumiem** atlasiet **Kanāli**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="ae5aa-346">Galvenajā logā zem **Kanāli** atlasiet kanālu.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="ae5aa-347">Cilnes kanāla rekvizītos labajā pusē atlasiet savu B2C lietojumprogrammas nosaukumu no nolaižamās izvēlnes **Atlasīt B2C lietojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="ae5aa-348">Atlasiet **Aizvērt**un pēc tam atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="ae5aa-349">B2C papildinformācija</span><span class="sxs-lookup"><span data-stu-id="ae5aa-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="ae5aa-350">Klientu migrācija</span><span class="sxs-lookup"><span data-stu-id="ae5aa-350">Customer migration</span></span>

<span data-ttu-id="ae5aa-351">Ja apsverat iespēju migrēt klientu ierakstus no iepriekšējas identitātes nodrošinātāja platformas, lūdzu, sazinieties ar Dynamics 365 Commerce grupu, lai pārskatītu jūsu klientu migrācijas vajadzības.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="ae5aa-352">Lai iegūtu papildu Azure AD B2C dokumentāciju par klientu migrāciju, skatiet sadaļu [Migrēt lietotājus uz Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="ae5aa-353">Pielāgotas politikas</span><span class="sxs-lookup"><span data-stu-id="ae5aa-353">Custom policies</span></span>

<span data-ttu-id="ae5aa-354">Lai iegūtu papildu informāciju par Azure AD B2C mijiedarbību un politikas plūsmu pielāgošanu, kas pārsniedz B2C standarta politiku piedāvāto, skatiet sadaļu [Pielāgotas Azure Active Directory B2C politikas](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="ae5aa-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="ae5aa-355">Sekundārais administrators</span><span class="sxs-lookup"><span data-stu-id="ae5aa-355">Secondary admin</span></span>

<span data-ttu-id="ae5aa-356">Papildu administratora kontu var pievienot jūsu B2C nomnieka **Lietotāji** sadaļā.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="ae5aa-357">Tas var būt tiešais konts vai vispārējais konts.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="ae5aa-358">Ja ir jākopīgo konts grupas resursos, var tikt izveidots arī kopīgs konts.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="ae5aa-359">Izmantojot Azure AD B2C uzglabāto datu sensivitāti, kopējais konts ir rūpīgi jākontrolē atbilstoši jūsu uzņēmuma drošības praksei.</span><span class="sxs-lookup"><span data-stu-id="ae5aa-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae5aa-360">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ae5aa-360">Additional resources</span></span>

[<span data-ttu-id="ae5aa-361">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="ae5aa-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ae5aa-362">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="ae5aa-362">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ae5aa-363">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="ae5aa-363">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ae5aa-364">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="ae5aa-364">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ae5aa-365">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="ae5aa-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ae5aa-366">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="ae5aa-366">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ae5aa-367">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="ae5aa-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ae5aa-368">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="ae5aa-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ae5aa-369">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="ae5aa-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ae5aa-370">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="ae5aa-370">Enable location-based store detection</span></span>](enable-store-detection.md)
