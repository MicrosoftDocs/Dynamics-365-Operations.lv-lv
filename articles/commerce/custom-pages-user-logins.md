---
title: Pielāgotu lapu iestatīšana lietotāja pierakstīšanās gadījumiem
description: Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce izveidot pielāgotas lapas, kas apstrādā Azure Active Directory (Azure AD) bizness–patērētājs (B2C) nomnieku lietotāju pielāgotas pierakstīšanās gadījumus.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 644d937ddd3c219ae869f22d977d2846dffc20e1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697570"
---
# <a name="set-up-custom-pages-for-user-logins"></a><span data-ttu-id="34cc7-103">Pielāgotu lapu iestatīšana lietotāja pieteikšanās gadījumiem</span><span class="sxs-lookup"><span data-stu-id="34cc7-103">Set up custom pages for user logins</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="34cc7-104">Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce izveidot pielāgotas lapas, kas apstrādā Azure Active Directory (Azure AD) bizness–patērētājs (B2C) nomnieku lietotāju pielāgotas pierakstīšanās gadījumus.</span><span class="sxs-lookup"><span data-stu-id="34cc7-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="34cc7-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="34cc7-105">Overview</span></span>

<span data-ttu-id="34cc7-106">Lai izmantotu pielāgotās lapas, kas ir autorizētas Dynamics 365 Commerce, lai apstrādātu lietotāja pierakstīšanās plūsmas, ir jāiestata Azure AD politikas, kas tiks raksturotas Commerce vidē.</span><span class="sxs-lookup"><span data-stu-id="34cc7-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="34cc7-107">Varat konfigurēt Azure AD B2C politikas "Parakstīšanās un pierakstīšanās", "Profila rediģēšana" un "Paroles atiestatīšana", izmantojot Azure AD B2C programmu.</span><span class="sxs-lookup"><span data-stu-id="34cc7-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="34cc7-108">Tādējādi Azure AD B2C nomnieka un politiku nosaukumi var tikt raksturoti nodrošināšanas procesa laikā, kas tiek veikts Commerce videi, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="34cc7-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="34cc7-109">Pielāgotās Commerce lapas var veidot, izmantojot pierakstīšanos, parakstīšanos, konta profila rediģēšanu vai paroles atiestatīšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="34cc7-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="34cc7-110">Šīm pielāgotajām lapām publicētie lapu URL jāraksturo Azure AD B2C politikas konfigurācijās Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="34cc7-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="34cc7-111">B2C politiku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="34cc7-111">Set up B2C policies</span></span>

<span data-ttu-id="34cc7-112">Pēc tam, kad esat iestatījis savu Azure AD B2C nomnieku un saistījis to ar savu Commerce vidi, dodieties uz **Azure AD B2C** lapu Azure portālā un izvēlnes sadaļā **Politikas** atlasiet **Lietotāja plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Lietotāja plūsmas (politikas) komanda izvēlnē](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="34cc7-114">Tagad varat konfigurēt lietotāja pierakstīšanās plūsmas "Parakstīšanās un pierakstīšanās", "Profila rediģēšana" un "Paroles atiestatīšana".</span><span class="sxs-lookup"><span data-stu-id="34cc7-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="34cc7-115">"Parakstīšanās un pierakstīšanās" politikas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="34cc7-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="34cc7-116">Lai konfigurētu "Parakstīšanās un pierakstīšanās" politiku, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-117">Atlasiet **Jauna lietotāja plūsma** un pēc tam cilnē **Ieteiktais** atlasiet politiku **Parakstīšanās un pierakstīšanās**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="34cc7-118">Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="34cc7-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="34cc7-119">Sadaļā **Identitātes nodrošinātāji** atlasiet identitātes nodrošinātājus, ko izmantot šai politikai.</span><span class="sxs-lookup"><span data-stu-id="34cc7-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="34cc7-120">Jāatlasa vismaz **Parakstīšanās e-pastā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="34cc7-121">Kolonnā **Ievākt atribūtu** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds** un **Uzvārds**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="34cc7-122">Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Identitātes nodrošinātājs**, **Uzvārds** un **Lietotāja objekta ID**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Atlasītie atribūti un prasības](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="34cc7-124">Atlasiet **Labi**, lai izveidotu politiku.</span><span class="sxs-lookup"><span data-stu-id="34cc7-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="34cc7-125">Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="34cc7-126">Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Jaunās politikas rekvizītu lapa](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="34cc7-128">Politikas nosaukums būs pilnībā raksturots Commerce vidē.</span><span class="sxs-lookup"><span data-stu-id="34cc7-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="34cc7-129">(**B2C\_1\_** prefikss tiks iekļauts raksturojumā.) Politikas nevar pārdēvēt pēc tam, kad tās izveidotas.</span><span class="sxs-lookup"><span data-stu-id="34cc7-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="34cc7-130">Ja aizstājat esošu politiku savai Commerce videi, varat izdzēst sākotnējo politiku un izveidot jaunu politiku ar tādu pašu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="34cc7-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="34cc7-131">Vai arī, ja vide jau ir nodrošināta, varat iesniegt jauno politikas nosaukumu, izmantojot pakalpojuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="34cc7-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="34cc7-132">Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="34cc7-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="34cc7-133">Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="34cc7-134">"Profila rediģēšanas" politikas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="34cc7-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="34cc7-135">Lai konfigurētu "Profila rediģēšanas" politiku, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-136">Atlasiet **Jauna lietotāja plūsma** un pēc tam cilnē **Ieteiktais** atlasiet politiku **Profila rediģēšana**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="34cc7-137">Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="34cc7-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="34cc7-138">Sadaļā **Identitātes nodrošinātāji** atlasiet identitātes nodrošinātājus, ko izmantot šai politikai.</span><span class="sxs-lookup"><span data-stu-id="34cc7-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="34cc7-139">Jāatlasa vismaz **Pierakstīšanās lokālajā kontā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="34cc7-140">Kolonnā **Ievākt atribūtu** atlasiet izvēles lodziņus **E-pasta adreses** un **Uzvārds**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="34cc7-141">Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Identitātes nodrošinātājs**, **Uzvārds** un **Lietotāja objekta ID**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="34cc7-142">Atlasiet **Labi**, lai izveidotu politiku.</span><span class="sxs-lookup"><span data-stu-id="34cc7-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="34cc7-143">Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="34cc7-144">Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="34cc7-145">Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="34cc7-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="34cc7-146">Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="34cc7-147">"Paroles atiestatīšanas" politikas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="34cc7-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="34cc7-148">Lai konfigurētu "Paroles atiestatīšanas" politiku, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-149">Atlasiet **Jauna lietotāja plūsma** un pēc tam cilnē **Priekšskatījums** atlasiet politiku **Paroles atiestatīšana v1.1**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Paroles atiestatīšana v1.1 politika atlasīta priekšskatījuma cilnē](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="34cc7-151">Ievadiet politikas nosaukumu (piemēram, **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="34cc7-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="34cc7-152">Sadaļā **identitātes nodrošinātāji** atlasiet **Atiestatīt paroli, izmantojot e-pasta adresi**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="34cc7-153">Kolonnā **Atgriešanās prasība** atlasiet izvēles lodziņus **E-pasta adrese**, **Vārds**, **Uzvārds** un **Lietotāja objekta ID**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Atlasītās prasības](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="34cc7-155">Atlasiet **Labi**, lai izveidotu politiku.</span><span class="sxs-lookup"><span data-stu-id="34cc7-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="34cc7-156">Veiciet dubultklikšķi uz jaunā politikas nosaukuma un pēc tam navigācijas rūtī atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="34cc7-157">Iestatiet opciju **Iespējot JavaScript ieviešanu lapas izkārtojumā (priekšskatījums)** uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="34cc7-158">Pēc pielāgoto lapu izveidošanas jūs atgriezīsieties pie šīs politikas, lai pabeigtu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="34cc7-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="34cc7-159">Pagaidām aizveriet politiku, lai atgrieztos Azure portāla lapā **Lietotāja plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="34cc7-160">Pielāgoto lapu izveide</span><span class="sxs-lookup"><span data-stu-id="34cc7-160">Build the custom pages</span></span>

<span data-ttu-id="34cc7-161">Lai izveidotu pielāgotās lapas lietotāja pierakstīšanās gadījumu apstrādāšanai, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-162">Commerce autorēšanas rīkos dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="34cc7-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="34cc7-163">Izveidošanai izmantojiet tālāk minētās piecas veidnes un piecas lapas.</span><span class="sxs-lookup"><span data-stu-id="34cc7-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="34cc7-164">Veidne **Pierakstīšanās** un lapa, kas izmanto pierakstīšanās moduli.</span><span class="sxs-lookup"><span data-stu-id="34cc7-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="34cc7-165">Veidne **Parakstīšanās** un lapa, kas izmanto parakstīšanās moduli.</span><span class="sxs-lookup"><span data-stu-id="34cc7-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="34cc7-166">Veidne **Paroles atiestatīšana** un lapa, kas izmanto paroles atiestatīšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="34cc7-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="34cc7-167">Veidne **Paroles atiestatīšanas verifikācija** un lapa, kas izmanto paroles atiestatīšanas verifikācijas moduli.</span><span class="sxs-lookup"><span data-stu-id="34cc7-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="34cc7-168">Veidne **Profila rediģēšana** un lapa, kas izmanto konta profila rediģēšanas moduli</span><span class="sxs-lookup"><span data-stu-id="34cc7-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="34cc7-169">Izveidojot lapas, sekojiet tālāk minētajiem norādījumiem.</span><span class="sxs-lookup"><span data-stu-id="34cc7-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="34cc7-170">Katrai lapai vai modulim izmantojiet izkārtojumu un stilu, kas vislabāk atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="34cc7-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="34cc7-171">Publicējiet visas lapas un URL, kas jāizmanto Azure AD B2C iestatījumā.</span><span class="sxs-lookup"><span data-stu-id="34cc7-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="34cc7-172">Pēc lapu un URL publicēšanas ievāciet URL, kas jāizmanto Azure AD B2C politikas konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="34cc7-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="34cc7-173">Katram URL, kad tas tiek izmantots, tiks pievienots piedēklis **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34cc7-174">Neizmantojiet atkārtoti tādas universālas galvenes un kājenes, kurām ir relatīvas saites.</span><span class="sxs-lookup"><span data-stu-id="34cc7-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="34cc7-175">Tā kā šīs lapas izmantošanas laikā tiks viesotas Azure AD B2C domēnā, visām saitēm jāizmanto tikai absolūtie URL.</span><span class="sxs-lookup"><span data-stu-id="34cc7-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="34cc7-176">Azure AD B2C politiku konfigurēšana ar pielāgotu lapas informāciju</span><span class="sxs-lookup"><span data-stu-id="34cc7-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="34cc7-177">Azure portālā atgriezieties lapā **Azure AD B2C** un pēc tam izvēlnes sadaļā **Politikas** atlasiet **Lietotāja plūsmas (politikas)**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="34cc7-178">"Pierakstīšanās un parakstīšanās" politikas atjaunināšana ar pielāgotu lapas informāciju</span><span class="sxs-lookup"><span data-stu-id="34cc7-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="34cc7-179">Lai atjauninātu "Pierakstīšanās un parakstīšanās" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-180">Iepriekš konfigurētās **Pierakstīšanās un parakstīšanās** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="34cc7-181">Atlasiet izkārtojumu **Vienotā pierakstīšanās un parakstīšanās lapa**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="34cc7-182">Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="34cc7-183">Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL.</span><span class="sxs-lookup"><span data-stu-id="34cc7-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="34cc7-184">Iekļaujiet priedēkli **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="34cc7-185">Piemēram, ievadiet **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-185">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="34cc7-186">Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="34cc7-187">Atlasiet izkārtojumu **Lokālā konta parakstīšanās lapa**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="34cc7-188">Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="34cc7-189">Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL.</span><span class="sxs-lookup"><span data-stu-id="34cc7-189">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="34cc7-190">Iekļaujiet priedēkli **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="34cc7-191">Piemēram, ievadiet **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-191">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="34cc7-192">Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="34cc7-193">Sadaļā **Lietotāja atribūti** veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="34cc7-194">Atribūtiem **E-pasta adrese**, **Vārds** un **Uzvārds** atlasiet **Nē** laukā **Nepieciešama verifikācija**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="34cc7-195">Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** laukā **Pēc izvēles**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Lokālā konta parakstīšanās lapas politikas konfigurēšana](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="34cc7-197">"Profila rediģēšanas" politikas atjaunināšana ar pielāgotu lapas informāciju</span><span class="sxs-lookup"><span data-stu-id="34cc7-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="34cc7-198">Lai atjauninātu "Profila rediģēšanas" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-199">Iepriekš konfigurētās **Profila rediģēšanas** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="34cc7-200">Atlasiet izkārtojumu **Profila rediģēšanas lapa**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="34cc7-201">Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="34cc7-202">Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL.</span><span class="sxs-lookup"><span data-stu-id="34cc7-202">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="34cc7-203">Iekļaujiet priedēkli **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="34cc7-204">Piemēram, ievadiet **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-204">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="34cc7-205">Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="34cc7-206">Sadaļā **Lietotāja atribūti** veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="34cc7-207">Atribūtiem **E-pasta adrese** un **Vārds** atlasiet **Nē** laukā **Nepieciešama verifikācija**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="34cc7-208">Atribūtiem **Vārds** un **Uzvārds** atlasiet **Nē** laukā **Pēc izvēles**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="34cc7-209">"Paroles atiestatīšanas" politikas atjaunināšana ar pielāgotu lapas informāciju</span><span class="sxs-lookup"><span data-stu-id="34cc7-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="34cc7-210">Lai atjauninātu "Paroles atiestatīšanas" politiku ar pielāgotu lapas informāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="34cc7-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="34cc7-211">Iepriekš konfigurētās **Paroles atiestatīšanas** politikas navigācijas rūtī atlasiet **Lapas izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="34cc7-212">Atlasiet izkārtojumu **Jauna paroles lapa**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="34cc7-213">Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="34cc7-214">Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL.</span><span class="sxs-lookup"><span data-stu-id="34cc7-214">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="34cc7-215">Iekļaujiet priedēkli **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="34cc7-216">Piemēram, ievadiet **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-216">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="34cc7-217">Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="34cc7-218">Atlasiet izkārtojumu **Konta verifikācijas lapa**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="34cc7-219">Iestatiet opciju **Izmantot pielāgotu lapas saturu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="34cc7-220">Laukā **Pielāgots lapas URI** ievadiet pilnu pierakstīšanās URL.</span><span class="sxs-lookup"><span data-stu-id="34cc7-220">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="34cc7-221">Iekļaujiet priedēkli **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="34cc7-222">Piemēram, ievadiet **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-222">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="34cc7-223">Laukā **Lapas izkārtojuma versija (priekšskatījums)** atlasiet **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="34cc7-224">Etiķetēm un aprakstiem paredzētu noklusējuma teksta virkņu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="34cc7-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="34cc7-225">Sākuma komplektā pierakstīšanās moduļi ir iepriekš aizpildīti ar etiķetēm un aprakstiem paredzētām noklusējuma teksta virknēm.</span><span class="sxs-lookup"><span data-stu-id="34cc7-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="34cc7-226">Programmatūras izstrādes komplektā (SDK) varat pielāgot šīs virknes, atjauninot vērtības global.json failā, kas paredzēts, lai pierakstītos modulī.</span><span class="sxs-lookup"><span data-stu-id="34cc7-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="34cc7-227">Piemēram, aizmirstās paroles saites noklusējuma teksts ir **Aizmirsta parole?**.</span><span class="sxs-lookup"><span data-stu-id="34cc7-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="34cc7-228">Tālāk parādīts šis noklusējuma teksts pierakstīšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="34cc7-228">The following shows this default text on the sign-in page.</span></span>

![Noklusējuma teksts aizmirstas paroles saitei pierakstīšanās lapā](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="34cc7-230">Tomēr sākuma komplekta pierakstīšanās moduļa global.json failā varat rediģēt tekstu, lai būtu **Aizmirsāt paroli?**, kā parādīts tālāk redzamajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="34cc7-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Atjauninātais saites teksts pierakstīšanās moduļa global.json failā](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="34cc7-232">Pēc global.json faila atjaunināšanas un savu izmaiņu publicēšanas jaunais saites teksts parādīsies pierakstīšanās modulī gan Commerce, gan arī aktuālajā pierakstīšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="34cc7-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34cc7-233">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="34cc7-233">Additional resources</span></span>

[<span data-ttu-id="34cc7-234">Tiešsaistes veikala apskats</span><span class="sxs-lookup"><span data-stu-id="34cc7-234">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="34cc7-235">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="34cc7-235">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="34cc7-236">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="34cc7-236">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="34cc7-237">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="34cc7-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="34cc7-238">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="34cc7-238">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="34cc7-239">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="34cc7-239">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="34cc7-240">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="34cc7-240">Enable location-based store detection</span></span>](enable-store-detection.md)
