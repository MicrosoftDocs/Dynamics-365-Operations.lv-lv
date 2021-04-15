---
title: Autentifikācija
description: Šajā rakstā ir sniegta informācija par to, kā autentificēties Microsoft Dynamics 365 Human Resources datu programmu programmēšanas interfeisā (API).
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dffe1db98ba39fde2229e69bc70bdbf113ff6ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793685"
---
# <a name="authentication"></a><span data-ttu-id="71c01-103">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="71c01-103">Authentication</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="71c01-104">Šajā rakstā ir sniegta informācija par to, kā autentificēties Microsoft Dynamics 365 Human Resources datu programmu programmēšanas interfeisā (API).</span><span class="sxs-lookup"><span data-stu-id="71c01-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="71c01-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="71c01-105">Overview</span></span>

<span data-ttu-id="71c01-106">Personāla vadības datu API ir OData ieviešana.</span><span class="sxs-lookup"><span data-stu-id="71c01-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="71c01-107">Papildinformāciju skatiet šeit: [Atvērto datu protokols (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="71c01-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="71c01-108">Jūsu pieteikumam ir jābūt autentificētam kā autorizētam zvanītājam, pirms API apkalpos pieprasījumus no jūsu pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="71c01-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="71c01-109">Pamati</span><span class="sxs-lookup"><span data-stu-id="71c01-109">Fundamentals</span></span>

<span data-ttu-id="71c01-110">Lai izsauktu datu API, jūsu pieteikumam ir jāiegūst piekļuves marķieris no Microsoft identitātes platformas.</span><span class="sxs-lookup"><span data-stu-id="71c01-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="71c01-111">Piekļuves marķieris satur informāciju par jūsu pieteikumu un atļauju, kurai tai ir, lai zvanītu personāla vadības resursiem.</span><span class="sxs-lookup"><span data-stu-id="71c01-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="71c01-112">Piekļuves marķieris</span><span class="sxs-lookup"><span data-stu-id="71c01-112">Access token</span></span>

<span data-ttu-id="71c01-113">Microsoft identitātes platformas izsniegtie piekļuves marķieri ir base64 kodēti JavaScript objekta notācijas (JSON) tīmekļa marķieri (JWT).</span><span class="sxs-lookup"><span data-stu-id="71c01-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="71c01-114">Tajos ir ietverta informācija (apgalvojumi), kuru datu API (un citi tīmekļa API, ko aizsargā Microsoft identitātes platforma) izmanto, lai apstiprinātu zvanītāju un pārliecinātos, ka zvanītājam ir atbilstošas atļaujas, lai veiktu pieprasīto operāciju.</span><span class="sxs-lookup"><span data-stu-id="71c01-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="71c01-115">Zvanu laikā varat apstrādāt piekļuves marķierus kā necaurredzamus.</span><span class="sxs-lookup"><span data-stu-id="71c01-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="71c01-116">Vienmēr vajadzētu pārraidīt piekļuves marķierus, izmantojot drošu kanālu, piemēram, transportēšanas slāņa drošību (TLS) un hiperteksta pārsūtīšanas protokolu (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="71c01-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="71c01-117">Šajā piemērā ir parādīts piekļuves marķieris, ko izsniegusi Microsoft identitātes platforma.</span><span class="sxs-lookup"><span data-stu-id="71c01-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="71c01-118">Lai izsauktu datu API, jums ir jāpievieno piekļuves marķieris kā datu nesēja marķieris autorizācijas virsrakstam HTTP pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="71c01-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="71c01-119">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="71c01-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="71c01-120">REģistrējiet jaunu pieteikumu, izmantojot Azure portālu</span><span class="sxs-lookup"><span data-stu-id="71c01-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="71c01-121">Piesakieties [Microsoft Azure portālā](https://portal.azure.com) ar darba vai skolas kontu vai personīgu Microsoft kontu.</span><span class="sxs-lookup"><span data-stu-id="71c01-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="71c01-122">Ja jūsu konts sniedz piekļuvi vairāk nekā vienam nomniekam, izvēlieties savu kontu augšējā labajā stūrī un iestatiet savu portāla sesiju uz Azure Active Directory (Azure AD) nomnieku, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="71c01-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="71c01-123">Kreisajā rūtī atlasiet **Azure Active Directory** pakalpojumu un pēc tam atlasiet **Pieteikumu reģistrācijas \> Jauna reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="71c01-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="71c01-124">Kad parādās lapa **Reģistrēt pieteikumu**, ievadiet savu pieteikuma reģistrācijas informāciju:</span><span class="sxs-lookup"><span data-stu-id="71c01-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="71c01-125">**Nosaukums**: Ievadiet jēgpilnu pieteikuma nosaukumu, kas tiks rādīts programmas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="71c01-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="71c01-126">**Atbalstītie kontu veidi**: Atlasiet kontu tipus, kurus jūsu programmai vajadzētu atbalstīt.</span><span class="sxs-lookup"><span data-stu-id="71c01-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="71c01-127">Atbalstītie kontu veidi</span><span class="sxs-lookup"><span data-stu-id="71c01-127">Supported account types</span></span> | <span data-ttu-id="71c01-128">Apraksts</span><span class="sxs-lookup"><span data-stu-id="71c01-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="71c01-129">Tikai šajā organizatoriskajā direktorijā iekļautie konti</span><span class="sxs-lookup"><span data-stu-id="71c01-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="71c01-130">Atlasiet šo opciju, ja veidojat biznesa programmu.</span><span class="sxs-lookup"><span data-stu-id="71c01-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="71c01-131">Šī opcija nav pieejama, ja nereģistrējat programmu direktorijā.</span><span class="sxs-lookup"><span data-stu-id="71c01-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="71c01-132">Šī opcija ir kartēta **Azure AD tikai vienam nomniekam**.</span><span class="sxs-lookup"><span data-stu-id="71c01-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="71c01-133">Šī opcija ir noklusējuma opcija, izņemot tad, ja reģistrējat programmu ārpus direktorija.</span><span class="sxs-lookup"><span data-stu-id="71c01-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="71c01-134">Šādā gadījumā noklusētā opcija ir **Azure AD vairāku nomnieku un personīgais Microsoft konts**.</span><span class="sxs-lookup"><span data-stu-id="71c01-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="71c01-135">Jebkurā organizatoriskajā direktorijā iekļautie konti</span><span class="sxs-lookup"><span data-stu-id="71c01-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="71c01-136">Atlasiet šo opciju, lai adresētu visus biznesa un izglītības klientus.</span><span class="sxs-lookup"><span data-stu-id="71c01-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="71c01-137">Šī opcija ir kartēta **Azure AD tikai vairākiem nomniekiem**.</span><span class="sxs-lookup"><span data-stu-id="71c01-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="71c01-138">Ja reģistrējāt programmu kā **Azure AD tikai vienam nomniekam**, varat izmantot **Autentifikācijas** disku, lai to atjauninātu uz **Azure AD tikai vairākiem nomniekiem** un pēc tam atgrieztos **Azure AD tikai vienam nomniekam**.</span><span class="sxs-lookup"><span data-stu-id="71c01-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="71c01-139">Konti jebkurā organizācijas direktorijā un personiskajā Microsoft kontā</span><span class="sxs-lookup"><span data-stu-id="71c01-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="71c01-140">Atlasiet šo opciju, lai sasniegtu visplašāko klientu kopu.</span><span class="sxs-lookup"><span data-stu-id="71c01-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="71c01-141">Šī opcija ir kartēta uz **Azure AD vairāku nomnieku un personīgais Microsoft konts**.</span><span class="sxs-lookup"><span data-stu-id="71c01-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="71c01-142">Ja reģistrējāt programmu kā **Azure AD vairāku nomnieku un personīgie Microsoft konti**, šo iestatījumu nevar mainīt lietotāja interfeisā (UI).</span><span class="sxs-lookup"><span data-stu-id="71c01-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="71c01-143">Tā vietā ir jāizmanto pieteikuma manifesta redaktors, lai mainītu atbalstītos kontu tipus.</span><span class="sxs-lookup"><span data-stu-id="71c01-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="71c01-144">**Novirzīt URI (nav obligāti)** — atlasiet veidojamās programmas tipu: **Tīmekļa** vai **Publiskais klients (mobilā un datora)**.</span><span class="sxs-lookup"><span data-stu-id="71c01-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="71c01-145">Pēc tam ievadiet programmas novirzīšanas URI (vai atbildes vietrādi URL).</span><span class="sxs-lookup"><span data-stu-id="71c01-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="71c01-146">Tīmekļa lietotnēm norādiet programmas bāzes vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="71c01-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="71c01-147">Piemēram, `http://localhost:31544` var būt tīmekļa programmas vietrādis URL, kas tiek palaists lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="71c01-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="71c01-148">Pēc tam lietotāji izmanto šo vietrādi URL, lai pieteiktos tīmekļa klienta programmā.</span><span class="sxs-lookup"><span data-stu-id="71c01-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="71c01-149">Publiskajām klientu lietotnēm norādiet URI, kuras Azure AD izmanto, lai atgrieztu marķiera atbildes.</span><span class="sxs-lookup"><span data-stu-id="71c01-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="71c01-150">Ievadiet vērtību, kas ir konkrēta jūsu programmai, piemēram, `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="71c01-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="71c01-151">Lai skatītu konkrētus piemērus tīmekļa programmām vai vietējām programmām, iesākumam skatiet [Microsoft identitātes platforma (iepriekš Azure Active Directory izstrādātājiem)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="71c01-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="71c01-152">Sadaļā **API atļaujas** atlasiet **Pievienot atļauju**.</span><span class="sxs-lookup"><span data-stu-id="71c01-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="71c01-153">Pēc tam cilnē **API, kurus izmanto mana organizācija** meklējiet **Dynamics 365 Human Resources** un pievienojiet **user\_impersonation** atļauju savai programmai.</span><span class="sxs-lookup"><span data-stu-id="71c01-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="71c01-154">Personāla vadības pieteikuma ID ir f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="71c01-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="71c01-155">Lietojiet šo ID, lai nodrošinātu, ka esat izvēlējies pareizo pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="71c01-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="71c01-156">Atlasiet **Reģistrēt**.</span><span class="sxs-lookup"><span data-stu-id="71c01-156">Select **Register**.</span></span>

   <span data-ttu-id="71c01-157">[![Jaunas programmas reģistrēšana Azure portālā](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="71c01-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="71c01-158">Azure AD piešķir jūsu programmai unikālu pieteikuma ID (klienta ID) un aizved jūs uz jūsu programmas **Pārskata** lapu.</span><span class="sxs-lookup"><span data-stu-id="71c01-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="71c01-159">Lai savai programmai pievienotu vairāk iespēju, varat izvēlēties citas konfigurācijas opcijas, piemēram, opcijas zīmolradei un sertifikātiem un slepenajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="71c01-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="71c01-160">Piekļuves marķiera izgūšana</span><span class="sxs-lookup"><span data-stu-id="71c01-160">Retrieving an access token</span></span>

<span data-ttu-id="71c01-161">Dati par to, kā tiek izgūts piekļuves marķieris, lai izsauktu personāla vadības datu API, būs atkarīgi no tā, kādas tehnoloģijas izmantojat, lai izstrādātu savu klientu programmu.</span><span class="sxs-lookup"><span data-stu-id="71c01-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="71c01-162">Piemēram, jūs varētu [testēt ar trešās puses utilītu](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (piemēram, Postman), izstrādājot C# konsoles programmu vai tīmekļa pakalpojumu vai veidojot JavaScript/TypeScript klientu.</span><span class="sxs-lookup"><span data-stu-id="71c01-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="71c01-163">Piemērs C# klienta pieteikumam:</span><span class="sxs-lookup"><span data-stu-id="71c01-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="71c01-164">Kad esat izguvis piekļuves tiesības, marķieris tiks nodots autorizācijas galvenē kā datu nesēja marķieris ar katru pieprasījumu, ko nosūtāt datu API, kā aprakstīts iepriekš.</span><span class="sxs-lookup"><span data-stu-id="71c01-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]