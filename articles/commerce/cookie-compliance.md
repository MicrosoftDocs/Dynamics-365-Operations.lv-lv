---
title: Sīkfailu atbilstība
description: Šajā tēmā aprakstīti apsvērumi sīkdatņu atbilstībai un noklusējuma politikas, kas ir iekļautas Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10a58cf7197d2a8596107a42174b35350e72ae11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215701"
---
# <a name="cookie-compliance"></a><span data-ttu-id="70775-103">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="70775-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70775-104">Šajā tēmā aprakstīti apsvērumi sīkdatņu atbilstībai un noklusējuma politikas, kas ir iekļautas Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="70775-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="70775-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="70775-105">Overview</span></span>

<span data-ttu-id="70775-106">Privātums ir svarīgs faktors, kad tiek izmantotas izsekošanas tehnoloģijas, kas ietekmē e-komercijas klientus.</span><span class="sxs-lookup"><span data-stu-id="70775-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="70775-107">Sakarā ar privātuma atbilstības standartiem, piemēram, Vispārīgo datu aizsardzības regulu (VDAR) Eiropas Savienībā (ES), elektroniskas privātuma vadlīnijas ir jānorāda jebkurai vietnei, kas šobrīd darbojas.</span><span class="sxs-lookup"><span data-stu-id="70775-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="70775-108">Tā kā daudzas e-komercijas vietnes pēc noklusējuma ir pieejamas globāli, ir svarīgi pārskatīt e-komercijas vietnes atbilstības standartus.</span><span class="sxs-lookup"><span data-stu-id="70775-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="70775-109">Lai iegūtu papildinformāciju par pamatprincipiem, kurus Microsoft izmanto sīkfailu atbilstībai, apmeklējiet [Microsoft uzticības centru](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="70775-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="70775-110">Šajā vietnē varat arī iegūt plašāku informāciju par atbilstības un konfidencialitātes jomām.</span><span class="sxs-lookup"><span data-stu-id="70775-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="70775-111">Šajā tabulā parādīts pašreizējais sīkfailu atsauču saraksts, ko ievieto Dynamics 365 Commerce vietnes.</span><span class="sxs-lookup"><span data-stu-id="70775-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="70775-112">Sīkfaila nosaukums</span><span class="sxs-lookup"><span data-stu-id="70775-112">Cookie name</span></span>                               | <span data-ttu-id="70775-113">Lietojums</span><span class="sxs-lookup"><span data-stu-id="70775-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="70775-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="70775-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="70775-115">Saglabāt Microsoft Azure Active Directory (Azure AD) autentifikācijas sīkfailus vienotā pierakstīšanās (SSO).</span><span class="sxs-lookup"><span data-stu-id="70775-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="70775-116">Saglabā šifrētu lietotāja pamatinformāciju (vārds, uzvārds, e-pasts).</span><span class="sxs-lookup"><span data-stu-id="70775-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="70775-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="70775-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="70775-118">Veikalu groza ID, kas tiek izmantots, lai iegūtu preču sarakstu, kas pievienots groza instancei.</span><span class="sxs-lookup"><span data-stu-id="70775-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="70775-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="70775-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="70775-120">Sīkdatņu atbilstības piekrišanas izsekošana.</span><span class="sxs-lookup"><span data-stu-id="70775-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="70775-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="70775-121">ai_session</span></span>                                  | <span data-ttu-id="70775-122">Nosaka to, cik lietotāju aktivitāšu sesijas ir iekļāvušas noteiktas programmas lapas un līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="70775-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="70775-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="70775-123">ai_user</span></span>                                     | <span data-ttu-id="70775-124">Nosaka, cik cilvēku lieto programmu un tās līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="70775-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="70775-125">Lietotāji tiek skaitīti, izmantojot anonīmus ID.</span><span class="sxs-lookup"><span data-stu-id="70775-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="70775-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="70775-126">b2cru</span></span>                                       | <span data-ttu-id="70775-127">Dinamiski saglabā pārvirzīšanas URL.</span><span class="sxs-lookup"><span data-stu-id="70775-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="70775-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="70775-128">JSESSIONID</span></span>                                  | <span data-ttu-id="70775-129">Izmanto maksājuma savienotāja Adyen, lai saglabātu lietotāja sesiju.</span><span class="sxs-lookup"><span data-stu-id="70775-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="70775-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="70775-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="70775-131">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="70775-131">Authentication</span></span>                                               |
| <span data-ttu-id="70775-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="70775-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="70775-133">Izmanto pieprasījuma stāvokļa uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="70775-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="70775-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="70775-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="70775-135">Vairākvietu pieprasījuma viltošanas (CRSF) marķieris, ko izmanto aizsardzībai no CRSF.</span><span class="sxs-lookup"><span data-stu-id="70775-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="70775-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="70775-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="70775-137">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="70775-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="70775-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="70775-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="70775-139">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="70775-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="70775-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="70775-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="70775-141">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="70775-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="70775-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="70775-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="70775-143">Izmanto SSO sesijas uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="70775-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="70775-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="70775-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="70775-145">Tiek izmantots, lai izsekotu transakcijas (atvērto ciļņu skaits, kas tiek autentificētas attiecībā uz bizness patērētājam (B2C) vietni), ieskaitot pašreizējo transakciju.</span><span class="sxs-lookup"><span data-stu-id="70775-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="70775-146">Vietnes lietotāja sīkfailu piekrišana e-komercijas vietnē</span><span class="sxs-lookup"><span data-stu-id="70775-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="70775-147">Ja e-komercijas vietnes līdzeklis vai modulis izmanto nebūtisku sīkfailu, vietnes lietotāja atļauja ir jāsaņem pirms sīkfaila izsekošanas.</span><span class="sxs-lookup"><span data-stu-id="70775-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="70775-148">Lai ļautu vietnes lietotājiem sniegt sīkfailu piekrišanu e-komercijas vietnē, vietnes autoram ir jāpievieno un jākonfigurē sīkfailu piekrišanas modulis lapas virsraksta modulī, lai nodrošinātu, ka piekrišana tiek pieprasīta un saņemta.</span><span class="sxs-lookup"><span data-stu-id="70775-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="70775-149">Lai vietnes lapā varētu atveidot līdzekli vai moduli, kas izmanto nebūtisku sīkfailu, ir jāsaņem vietnes lietotāja piekrišana.</span><span class="sxs-lookup"><span data-stu-id="70775-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70775-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="70775-150">Additional resources</span></span>

[<span data-ttu-id="70775-151">Pieejamības līdzekļi un iespējas</span><span class="sxs-lookup"><span data-stu-id="70775-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="70775-152">Atbilstības pārskats</span><span class="sxs-lookup"><span data-stu-id="70775-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="70775-153">Konfidencialitātes politikas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="70775-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="70775-154">Ar izsekotajām satura izmaiņām saistīto lietotāju ID aizstāšana</span><span class="sxs-lookup"><span data-stu-id="70775-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="70775-155">Sīkfailu piekrišanas modulis</span><span class="sxs-lookup"><span data-stu-id="70775-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="70775-156">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="70775-156">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]