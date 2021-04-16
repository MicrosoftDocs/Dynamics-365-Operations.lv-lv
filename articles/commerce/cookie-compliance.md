---
title: Sīkfailu atbilstība
description: Šajā tēmā aprakstīti apsvērumi sīkdatņu atbilstībai un noklusējuma politikas, kas ir iekļautas Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796031"
---
# <a name="cookie-compliance"></a><span data-ttu-id="759b4-103">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="759b4-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="759b4-104">Šajā tēmā aprakstīti apsvērumi sīkdatņu atbilstībai un noklusējuma politikas, kas ir iekļautas Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="759b4-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="759b4-105">Privātums ir svarīgs faktors, kad tiek izmantotas izsekošanas tehnoloģijas, kas ietekmē e-komercijas klientus.</span><span class="sxs-lookup"><span data-stu-id="759b4-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="759b4-106">Sakarā ar privātuma atbilstības standartiem, piemēram, Vispārīgo datu aizsardzības regulu (VDAR) Eiropas Savienībā (ES), elektroniskas privātuma vadlīnijas ir jānorāda jebkurai vietnei, kas šobrīd darbojas.</span><span class="sxs-lookup"><span data-stu-id="759b4-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="759b4-107">Tā kā daudzas e-komercijas vietnes pēc noklusējuma ir pieejamas globāli, ir svarīgi pārskatīt e-komercijas vietnes atbilstības standartus.</span><span class="sxs-lookup"><span data-stu-id="759b4-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="759b4-108">Lai iegūtu papildinformāciju par pamatprincipiem, kurus Microsoft izmanto sīkfailu atbilstībai, apmeklējiet [Microsoft uzticības centru](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="759b4-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="759b4-109">Šajā vietnē varat arī iegūt plašāku informāciju par atbilstības un konfidencialitātes jomām.</span><span class="sxs-lookup"><span data-stu-id="759b4-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="759b4-110">Šajā tabulā parādīts pašreizējais sīkfailu atsauču saraksts, ko ievieto Dynamics 365 Commerce vietnes.</span><span class="sxs-lookup"><span data-stu-id="759b4-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="759b4-111">Sīkfaila nosaukums</span><span class="sxs-lookup"><span data-stu-id="759b4-111">Cookie name</span></span>                               | <span data-ttu-id="759b4-112">Lietojums</span><span class="sxs-lookup"><span data-stu-id="759b4-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="759b4-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="759b4-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="759b4-114">Saglabāt Microsoft Azure Active Directory (Azure AD) autentifikācijas sīkfailus vienotā pierakstīšanās (SSO).</span><span class="sxs-lookup"><span data-stu-id="759b4-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="759b4-115">Saglabā šifrētu lietotāja pamatinformāciju (vārds, uzvārds, e-pasts).</span><span class="sxs-lookup"><span data-stu-id="759b4-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="759b4-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="759b4-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="759b4-117">Veikalu groza ID, kas tiek izmantots, lai iegūtu preču sarakstu, kas pievienots groza instancei.</span><span class="sxs-lookup"><span data-stu-id="759b4-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="759b4-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="759b4-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="759b4-119">Sīkdatņu atbilstības piekrišanas izsekošana.</span><span class="sxs-lookup"><span data-stu-id="759b4-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="759b4-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="759b4-120">ai_session</span></span>                                  | <span data-ttu-id="759b4-121">Nosaka to, cik lietotāju aktivitāšu sesijas ir iekļāvušas noteiktas programmas lapas un līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="759b4-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="759b4-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="759b4-122">ai_user</span></span>                                     | <span data-ttu-id="759b4-123">Nosaka, cik cilvēku lieto programmu un tās līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="759b4-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="759b4-124">Lietotāji tiek skaitīti, izmantojot anonīmus ID.</span><span class="sxs-lookup"><span data-stu-id="759b4-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="759b4-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="759b4-125">b2cru</span></span>                                       | <span data-ttu-id="759b4-126">Dinamiski saglabā pārvirzīšanas URL.</span><span class="sxs-lookup"><span data-stu-id="759b4-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="759b4-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="759b4-127">JSESSIONID</span></span>                                  | <span data-ttu-id="759b4-128">Izmanto maksājuma savienotāja Adyen, lai saglabātu lietotāja sesiju.</span><span class="sxs-lookup"><span data-stu-id="759b4-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="759b4-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="759b4-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="759b4-130">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="759b4-130">Authentication</span></span>                                               |
| <span data-ttu-id="759b4-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="759b4-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="759b4-132">Izmanto pieprasījuma stāvokļa uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="759b4-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="759b4-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="759b4-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="759b4-134">Vairākvietu pieprasījuma viltošanas (CRSF) marķieris, ko izmanto aizsardzībai no CRSF.</span><span class="sxs-lookup"><span data-stu-id="759b4-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="759b4-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="759b4-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="759b4-136">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="759b4-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="759b4-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="759b4-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="759b4-138">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="759b4-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="759b4-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="759b4-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="759b4-140">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="759b4-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="759b4-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="759b4-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="759b4-142">Izmanto SSO sesijas uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="759b4-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="759b4-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="759b4-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="759b4-144">Tiek izmantots, lai izsekotu transakcijas (atvērto ciļņu skaits, kas tiek autentificētas attiecībā uz bizness patērētājam (B2C) vietni), ieskaitot pašreizējo transakciju.</span><span class="sxs-lookup"><span data-stu-id="759b4-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="759b4-145">Vietnes lietotāja sīkfailu piekrišana e-komercijas vietnē</span><span class="sxs-lookup"><span data-stu-id="759b4-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="759b4-146">Ja e-komercijas vietnes līdzeklis vai modulis izmanto nebūtisku sīkfailu, vietnes lietotāja atļauja ir jāsaņem pirms sīkfaila izsekošanas.</span><span class="sxs-lookup"><span data-stu-id="759b4-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="759b4-147">Lai ļautu vietnes lietotājiem sniegt sīkfailu piekrišanu e-komercijas vietnē, vietnes autoram ir jāpievieno un jākonfigurē sīkfailu piekrišanas modulis lapas virsraksta modulī, lai nodrošinātu, ka piekrišana tiek pieprasīta un saņemta.</span><span class="sxs-lookup"><span data-stu-id="759b4-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="759b4-148">Lai vietnes lapā varētu atveidot līdzekli vai moduli, kas izmanto nebūtisku sīkfailu, ir jāsaņem vietnes lietotāja piekrišana.</span><span class="sxs-lookup"><span data-stu-id="759b4-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="759b4-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="759b4-149">Additional resources</span></span>

[<span data-ttu-id="759b4-150">Pieejamības līdzekļi un iespējas</span><span class="sxs-lookup"><span data-stu-id="759b4-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="759b4-151">Atbilstības pārskats</span><span class="sxs-lookup"><span data-stu-id="759b4-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="759b4-152">Konfidencialitātes politikas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="759b4-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="759b4-153">Ar izsekotajām satura izmaiņām saistīto lietotāju ID aizstāšana</span><span class="sxs-lookup"><span data-stu-id="759b4-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="759b4-154">Sīkfailu piekrišanas modulis</span><span class="sxs-lookup"><span data-stu-id="759b4-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="759b4-155">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="759b4-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
