---
title: Sīkfailu atbilstība
description: Šajā tēmā ir aprakstīti apsvērumi attiecībā uz sīkfailu atbilstību un noklusējuma politikām, kas ir ietvertas pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446917"
---
# <a name="cookie-compliance"></a><span data-ttu-id="4e85e-103">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="4e85e-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e85e-104">Šajā tēmā ir aprakstīti apsvērumi attiecībā uz sīkfailu atbilstību un noklusējuma politikām, kas ir ietvertas pakalpojumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e85e-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4e85e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4e85e-105">Overview</span></span>

<span data-ttu-id="4e85e-106">Privātums ir svarīgs faktors, kad tiek izmantotas izsekošanas tehnoloģijas, kas ietekmē e-komercijas klientus.</span><span class="sxs-lookup"><span data-stu-id="4e85e-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="4e85e-107">Sakarā ar privātuma atbilstības standartiem, piemēram, Vispārīgo datu aizsardzības regulu (VDAR) Eiropas Savienībā (ES), elektroniskas privātuma vadlīnijas ir jānorāda jebkurai vietnei, kas šobrīd darbojas.</span><span class="sxs-lookup"><span data-stu-id="4e85e-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="4e85e-108">Tā kā daudzas e-komercijas vietnes pēc noklusējuma ir pieejamas globāli, ir svarīgi pārskatīt e-komercijas vietnes atbilstības standartus.</span><span class="sxs-lookup"><span data-stu-id="4e85e-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="4e85e-109">Lai iegūtu papildinformāciju par pamatprincipiem, kurus Microsoft izmanto sīkfailu atbilstībai, apmeklējiet [Microsoft uzticības centru](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="4e85e-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="4e85e-110">Šajā vietnē varat arī iegūt plašāku informāciju par atbilstības un konfidencialitātes jomām.</span><span class="sxs-lookup"><span data-stu-id="4e85e-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="4e85e-111">Šajā tabulā parādīts pašreizējais sīkfailu atsauču saraksts, ko ievieto Dynamics 365 Commerce vietnes.</span><span class="sxs-lookup"><span data-stu-id="4e85e-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="4e85e-112">Sīkfaila nosaukums</span><span class="sxs-lookup"><span data-stu-id="4e85e-112">Cookie name</span></span>                               | <span data-ttu-id="4e85e-113">Lietojums</span><span class="sxs-lookup"><span data-stu-id="4e85e-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="4e85e-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="4e85e-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="4e85e-115">Saglabāt Microsoft Azure Active Directory (Azure AD) autentifikācijas sīkfailus vienotā pierakstīšanās (SSO).</span><span class="sxs-lookup"><span data-stu-id="4e85e-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="4e85e-116">Saglabā šifrētu lietotāja pamatinformāciju (vārds, uzvārds, e-pasts).</span><span class="sxs-lookup"><span data-stu-id="4e85e-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="4e85e-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="4e85e-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="4e85e-118">Veikalu groza ID, kas tiek izmantots, lai iegūtu preču sarakstu, kas pievienots groza instancei.</span><span class="sxs-lookup"><span data-stu-id="4e85e-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="4e85e-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="4e85e-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="4e85e-120">Sīkdatņu atbilstības piekrišanas izsekošana.</span><span class="sxs-lookup"><span data-stu-id="4e85e-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="4e85e-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="4e85e-121">ai_session</span></span>                                  | <span data-ttu-id="4e85e-122">Nosaka to, cik lietotāju aktivitāšu sesijas ir iekļāvušas noteiktas programmas lapas un līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="4e85e-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="4e85e-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="4e85e-123">ai_user</span></span>                                     | <span data-ttu-id="4e85e-124">Nosaka, cik cilvēku lieto programmu un tās līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="4e85e-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="4e85e-125">Lietotāji tiek skaitīti, izmantojot anonīmus ID.</span><span class="sxs-lookup"><span data-stu-id="4e85e-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="4e85e-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="4e85e-126">b2cru</span></span>                                       | <span data-ttu-id="4e85e-127">Dinamiski saglabā pārvirzīšanas URL.</span><span class="sxs-lookup"><span data-stu-id="4e85e-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="4e85e-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="4e85e-128">JSESSIONID</span></span>                                  | <span data-ttu-id="4e85e-129">Izmanto maksājuma savienotāja Adyen, lai saglabātu lietotāja sesiju.</span><span class="sxs-lookup"><span data-stu-id="4e85e-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="4e85e-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="4e85e-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="4e85e-131">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="4e85e-131">Authentication</span></span>                                               |
| <span data-ttu-id="4e85e-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="4e85e-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="4e85e-133">Izmanto pieprasījuma stāvokļa uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="4e85e-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="4e85e-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="4e85e-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="4e85e-135">Vairākvietu pieprasījuma viltošanas (CRSF) marķieris, ko izmanto aizsardzībai no CRSF.</span><span class="sxs-lookup"><span data-stu-id="4e85e-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="4e85e-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="4e85e-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="4e85e-137">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="4e85e-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4e85e-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="4e85e-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="4e85e-139">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="4e85e-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4e85e-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="4e85e-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="4e85e-141">Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci.</span><span class="sxs-lookup"><span data-stu-id="4e85e-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4e85e-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="4e85e-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="4e85e-143">Izmanto SSO sesijas uzturēšanai.</span><span class="sxs-lookup"><span data-stu-id="4e85e-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="4e85e-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="4e85e-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="4e85e-145">Tiek izmantots, lai izsekotu transakcijas (atvērto ciļņu skaits, kas tiek autentificētas attiecībā uz bizness patērētājam (B2C) vietni), ieskaitot pašreizējo transakciju.</span><span class="sxs-lookup"><span data-stu-id="4e85e-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4e85e-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4e85e-146">Additional resources</span></span>

[<span data-ttu-id="4e85e-147">Pieejamības līdzekļi un iespējas</span><span class="sxs-lookup"><span data-stu-id="4e85e-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="4e85e-148">Atbilstības pārskats</span><span class="sxs-lookup"><span data-stu-id="4e85e-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="4e85e-149">Konfidencialitātes politikas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="4e85e-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="4e85e-150">Aizstāt lietotāja ID, kas saistīti ar izsekotām satura izmaiņām</span><span class="sxs-lookup"><span data-stu-id="4e85e-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
