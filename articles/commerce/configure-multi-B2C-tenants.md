---
title: Konfigurēt vairākus B2C nomniekus Commerce vidē
description: Šajā tēmā aprakstīts, kad un kā iestatīt vairākus katra kanāla Microsoft Azure Active Directory (Azure AD) biznesa-patērētāja (B2C) nomniekus lietotāja autentifikācijai īpašā Dynamics 365 Commerce vidē.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
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
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: da27e3ed0a0e50126590609d09575befe17a7aa2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517131"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="f0a6b-103">Konfigurēt vairākus B2C nomniekus Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="f0a6b-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f0a6b-104">Šajā tēmā aprakstīts, kad un kā iestatīt vairākus katra kanāla Microsoft Azure Active Directory (Azure AD) biznesa-patērētāja (B2C) nomniekus lietotāja autentifikācijai īpašā Dynamics 365 Commerce vidē.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="f0a6b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f0a6b-105">Overview</span></span>

<span data-ttu-id="f0a6b-106">Dynamics 365 Commerce izmanto Azure AD B2C mākoņa identitātes pakalpojumu, lai atbalstītu lietotāja akreditācijas datus un autentifikācijas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="f0a6b-107">Lietotāji var izmantot autentifikācijas plūsmas, lai pieteiktos, pierakstītos un atjaunotu savu paroli.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="f0a6b-108">Azure AD B2C saglabā lietotāja sensitīvo autentifikācijas informāciju, piemēram, lietotāja vārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="f0a6b-109">Lietotāja ieraksts ir unikāls katram B2C nomniekam, un tas izmanto vai nu lietotājvārda (e-pasta adreses) akreditācijas datus vai sociālās identitātes nodrošinātāja akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="f0a6b-110">Vairākumā gadījumu Commerce vidē tiek izmantots viens Azure AD B2C nomnieks.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="f0a6b-111">Commerce klienti pēc tam var izveidot un publicēt vairākas vietas vienā un tajā pašā Commerce vidē, un šajos portālos tiks izmantoti vieni un tie paši klienta akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="f0a6b-112">Tomēr, ja vides vietas ir jāuzskata par dažādiem zīmoliem un lietotājiem tās tiek rādītas kā atsevišķi uzņēmumi, var konfigurēt B2C nomnieku šim kanālam, kas tiek izmantots vietas/zīmola nodalīšanai.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="f0a6b-113">Apsvērumi, kad katram kanālam tiek iestatīti vairāki B2C nomnieki</span><span class="sxs-lookup"><span data-stu-id="f0a6b-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="f0a6b-114">Bieži vien, kad katrs kanāls vai vieta tiek uzskatīts par atsevišķu biznesu, vislabākā opcija attiecībā uz lietotāja autentifikācijas plūsmām programmā Commerce ir izmantot atsevišķas juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="f0a6b-115">Tomēr, ja vēlaties saglabāt katru kanālu/vietu tajā pašā vidē un juridiskajā personā, bet vēlaties katrai vietai izveidot atsevišķu lietotāja autentifikāciju, pirms turpināt, ir svarīgi ņemt vērā šādus punktus:</span><span class="sxs-lookup"><span data-stu-id="f0a6b-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="f0a6b-116">Lietotājiem būs savi atsevišķi akreditācijas dati katram kanālam/vietai.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="f0a6b-117">Vienai personai var būt divi atsevišķi konti katram kanālam/vietai, jo katrs konts būs unikāls ieraksts atsevišķā B2C nomniekā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="f0a6b-118">Microsoft Dynamics vidē atsevišķi debitoru ieraksti tiks atgriezti globālajā ierakstu meklēšanā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="f0a6b-119">Ja lietotājs izmanto vienu un to pašu e-pasta adresi kanālos/vietās, globālās klientu meklēšanas rezultāts atgriezīs katra kanāla/vietas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="f0a6b-120">(Tiks parādīts kanāla indikators.)</span><span class="sxs-lookup"><span data-stu-id="f0a6b-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="f0a6b-121">Var izmantot adrešu grāmatu, lai palīdzētu grupas lietotājiem būs izsekojamiem katrā kanālā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="f0a6b-122">Var palielināties katra kanāla klientu ierakstu skaits, un šis pieaugums var ietekmēt globālo klientu meklējumu veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="f0a6b-123">B2C nomniekiem ir jābūt rūpīgi kartētiem kanālā, lai palīdzētu novērst situācijas, kad klienti pierakstās nepareizam nomniekam.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="f0a6b-124">Pretējā gadījumā var rasties apjukums vai izsekošanas problēmas.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="f0a6b-125">Šajā attēlā redzami vairāki B2C nomnieki Commerce vidē.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Vairāki B2C nomnieki Commerce vidē](media/MultiB2C_In_Environment.png)

<span data-ttu-id="f0a6b-127">Ja izlemjat, ka jūsu uzņēmumam ir nepieciešams atsevišķs B2C nomnieks vienam kanālam vienā un tajā pašā Commerce vidē, izpildiet tālāk norādītās darbības, lai pieprasītu šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="f0a6b-128">Pieprasīt, lai jūsu vidē tiktu iespējots B2C vienam kanālam</span><span class="sxs-lookup"><span data-stu-id="f0a6b-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="f0a6b-129">Ja vēlaties, lai katram kanālam būtu pieejams atšķirīgs B2C nomnieks, ir jāiesniedz pieprasījums Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="f0a6b-130">Papildinformāciju skatiet šeit [Saņemiet atbalstu Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) vai apspriediet šo problēmu ar savu Commerce risinājumu kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="f0a6b-131">Konfigurēt B2C nomniekus jūsu vidē</span><span class="sxs-lookup"><span data-stu-id="f0a6b-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="f0a6b-132">Lai konfigurētu B2C nomniekus savā vidē, veiciet atbilstošās procedūras, kas aprakstītas šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="f0a6b-133">Pievienot Azure AD B2C nomnieku</span><span class="sxs-lookup"><span data-stu-id="f0a6b-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="f0a6b-134">Lai savai videi pievienotu Azure AD B2C nomnieku, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="f0a6b-135">Piesakieties Commerce vietas veidotājam savai videi kā sistēmas administrators. Lai konfigurētu Azure AD B2C nomniekus, jums ir jābūt Commerce vides sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="f0a6b-136">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="f0a6b-137">Atlasiet **B2C iestatījumi** un pēc tam atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="f0a6b-138">Atlasiet **Pievienot B2C programmu**, un pēc tam ievadiet šādu informāciju.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="f0a6b-139">**Programmas nosaukums**: ievadiet nosaukumu, kas jālieto programmai saistībā ar tās pārvaldīšanu pakalpojumā Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="f0a6b-140">Ieteicams izmantot programmas nosaukumu, ko izvēlējāties, iestatot Azure AD B2C lietojumprogrammu Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="f0a6b-141">Šādā veidā jūs varat palīdzēt mazināt apjukumu, kad pakalpojumā Commerce tiek pārvaldīti B2C nomnieki.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="f0a6b-142">**Nomnieka nosaukums**: ievadiet B2C nomnieka nosaukumu, kāds tas parādās Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="f0a6b-143">**Aizmirstas paroles politikas ID**: ievadiet politikas ID (politikas nosaukumu Azure portālā).</span><span class="sxs-lookup"><span data-stu-id="f0a6b-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="f0a6b-144">**Pieteikšanās Pierakstīšanās politikas ID**: ievadiet politikas ID (politikas nosaukumu Azure portālā).</span><span class="sxs-lookup"><span data-stu-id="f0a6b-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="f0a6b-145">**Klienta GUID**: ievadiet Azure AD B2C nomnieka ID, kāds tas parādās Azure portālā (nevis programmas ID B2C nomniekam).</span><span class="sxs-lookup"><span data-stu-id="f0a6b-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="f0a6b-146">**Rediģēt profila politikas ID**: ievadiet politikas ID (politikas nosaukumu Azure portālā).</span><span class="sxs-lookup"><span data-stu-id="f0a6b-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="f0a6b-147">Kad esat pabeidzis šīs informācijas ievadīšanu, atlasiet **Labi**, lai saglabātu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="f0a6b-148">Jums ir jāatstāj tādi lauki kā, piemēram, **Tvērums**, **Neinteraktīvas politikas ID**, **Neinteraktīva klienta ID**, **Pieteikšanās pielāgots domēns** un **Pieteikšanās politikas ID** tukši, ja vien Dynamics 365 Commerce grupa jums nesniedz norādījumus to iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="f0a6b-149">Jūsu jaunajam Azure AD B2C nomniekam tagad ir jāparādās sarakstā sadaļā **Pārvaldīt B2C programmas**.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="f0a6b-150">Azure AD B2C nomnieka pārvaldīšana vai dzēšana</span><span class="sxs-lookup"><span data-stu-id="f0a6b-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="f0a6b-151">Piesakieties Commerce vietas veidotājam savai videi kā sistēmas administrators. Lai konfigurētu Azure AD B2C nomniekus, jums ir jābūt Commerce vides sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="f0a6b-152">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="f0a6b-153">Atlasiet **B2C iestatījumi** un pēc tam atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="f0a6b-154">Lai labotu B2C nomnieku, blakus tam atlasiet zīmuļa simbolu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="f0a6b-155">Lai dzēstu B2C nomnieku, atlasiet atkritnes simbolu tam blakus.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="f0a6b-156">Atlasiet **Saglabāt** un pēc tam atlasiet **Publicēt**, lai aktivizētu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="f0a6b-157">Kad B2C nomnieks ir konfigurēts dzīvai/publicētai vietai, lietotāji, iespējams, ir reģistrējušies, izmantojot kontu, kas ir nomniekā.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="f0a6b-158">Ja izdzēšat konfigurētu nomnieku izvēlnē **Nomnieka iestatījumi \> B2C nomnieks**, jūs noņemat šī B2C nomnieka saistību no vietām, kas ir saistītas ar jebkuru nomnieka kanālu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="f0a6b-159">Šādā gadījumā lietotāji, iespējams, vairs nevarēs pieteikties savos kontos.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="f0a6b-160">Tāpēc, dzēšot konfigurēto nomnieku, esiet ļoti piesardzīgi.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="f0a6b-161">Kad konfigurētais nomnieks tiek dzēsts, B2C nomnieks un ieraksti joprojām tiks uzturēti, bet šī nomnieka Commerce sistēmas konfigurācija tiks mainīta vai noņemta.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="f0a6b-162">Lietotāji, kuri mēģina pierakstīties vai pieteikties vietā, izveidos jaunu konta ierakstu noklusējuma vai nesen saistītajā B2C nomniekā, kas ir konfigurēts vietas kanālam.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="f0a6b-163">Konfigurējiet savu kanālu ar B2C nomnieku</span><span class="sxs-lookup"><span data-stu-id="f0a6b-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="f0a6b-164">Piesakieties Commerce vietas veidotājam savai videi kā sistēmas administrators. Lai konfigurētu Azure AD B2C nomniekus, jums ir jābūt Commerce vides sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="f0a6b-165">Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="f0a6b-166">Atlasiet **Kanāli** un pēc tam atlasiet kanālu, ko konfigurēt.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="f0a6b-167">Rekvizītu rūts labajā pusē, laukā **Atlasiet B2C pieteikumu** atlasiet konfigurēto Azure AD B2C nomnieku, ko izmantot šim kanālam.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="f0a6b-168">Komandjoslā atlasiet **Saglabāt un publicēt**, lai iesniegtu jauno vai atjaunināto konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="f0a6b-169">Ja mainīsit šai stacijai piešķirto B2C programmu, noņemiet pašreizējās atsauces, kas izveidotas visiem lietotājiem, kuri jau ir pieteikušies vidē.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="f0a6b-170">Šādā gadījumā visi akreditācijas dati, kas ir saistīti ar pašlaik piešķirto B2C programmu, lietotājiem nebūs pieejami.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="f0a6b-171">Tāpēc mainiet kanāla Azure AD B2C konfigurāciju tikai tad, ja pirmo reizi iestatāt kanālu, un neviens lietotājs nevarēja pieteikties.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="f0a6b-172">Pretējā gadījumā lietotājiem, iespējams, būs vēlreiz jāpierakstās, lai izveidotu jaunu Azure AD B2C nomnieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f0a6b-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="f0a6b-173">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f0a6b-173">Additional resources</span></span>

[<span data-ttu-id="f0a6b-174">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f0a6b-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f0a6b-175">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="f0a6b-175">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f0a6b-176">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="f0a6b-176">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f0a6b-177">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="f0a6b-177">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f0a6b-178">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="f0a6b-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f0a6b-179">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="f0a6b-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f0a6b-180">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="f0a6b-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f0a6b-181">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="f0a6b-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f0a6b-182">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="f0a6b-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f0a6b-183">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="f0a6b-183">Enable location-based store detection</span></span>](enable-store-detection.md)
