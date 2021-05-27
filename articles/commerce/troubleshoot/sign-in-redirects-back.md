---
title: Pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni, nevis atver pierakstīšanās lapu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020607"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="bf8bd-103">Pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni</span><span class="sxs-lookup"><span data-stu-id="bf8bd-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf8bd-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni, nevis atver pierakstīšanās lapu.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="bf8bd-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="bf8bd-105">Description</span></span>

<span data-ttu-id="bf8bd-106">Pēc jauna Microsoft Azure Active Directory B2C (Azure AD B2C) nomnieka konfigurēšanas Commerce vietnes veidotājā lietotāji, kuri atlasa saiti **Pierakstīties**, tiek pārvirzēti atpakaļ uz galveno e-komercijas informācijas lapu, neatverot pierakstīšanās lapu.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="bf8bd-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="bf8bd-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="bf8bd-108">Apstipriniet, ka atbildes vietrādis URL ir pareizi konfigurēts Azure AD B2C programmā</span><span class="sxs-lookup"><span data-stu-id="bf8bd-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="bf8bd-109">Lai apstiprinātu, ka atbildes vietrādis URL ir pareizi konfigurēts Azure AD B2C programmā, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="bf8bd-110">Dodieties uz [Azure portālu](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="bf8bd-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="bf8bd-111">Atlasiet Azure AD B2C programmu, ko izveidojāt jūsu vietnes piekļuvei.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="bf8bd-112">Atlasiet programmu, ko izveidojāt Azure AD B2C iestatīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="bf8bd-113">Sadaļā **Atbildes vietrādis URL** pārliecinieties, vai sarakstā ir ietverti gan vietnes domēna vietrāža URL, gan e-komercijas ģenerētā vietrāža URL ieraksti, kā parādīts piemērā nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C atbildes vietrāža URL ieraksti](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="bf8bd-115">Gan vietnes domēna vietrādim URL, gan e-komercijas ģenerētajam vietrādim URL ir jābūt derīgā URL formātā, kas neietver sākuma un beigu slīpsvītras.</span><span class="sxs-lookup"><span data-stu-id="bf8bd-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf8bd-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bf8bd-116">Additional resources</span></span>

[<span data-ttu-id="bf8bd-117">Tīmekļa programmas reģistrēšana portālā Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="bf8bd-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="bf8bd-118">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="bf8bd-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)