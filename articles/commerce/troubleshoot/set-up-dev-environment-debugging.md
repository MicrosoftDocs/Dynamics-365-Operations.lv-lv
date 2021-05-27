---
title: E-komercijas izstrādes vides iestatīšana, lai atkļūdotu, izmantojot 1. līmeņa Retail Server virtuālo mašīnu
description: Šajā tēmā paskaidrots, kā iestatīt E-komercijas izstrādes vidi, lai atkļūdotu, izmantojot 1. līmeņa Retail Server virtuālo mašīnu (VM).
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
ms.openlocfilehash: 38a616c418c3b32490c9adaf69a69af0d47d3478
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019450"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="4e80b-103">E-komercijas izstrādes vides iestatīšana, lai atkļūdotu, izmantojot 1. līmeņa Retail Server virtuālo mašīnu</span><span class="sxs-lookup"><span data-stu-id="4e80b-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e80b-104">Šajā tēmā paskaidrots, kā iestatīt E-komercijas izstrādes vidi, lai atkļūdotu, izmantojot 1. līmeņa Retail Server virtuālo mašīnu (VM).</span><span class="sxs-lookup"><span data-stu-id="4e80b-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="4e80b-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4e80b-105">Description</span></span>

<span data-ttu-id="4e80b-106">Microsoft Dynamics 365 Commerce 1. līmeņa vides parasti tiek izvietotas Commerce Runtime (CRT) un pārdošanas punkta (POS) paplašinājuma izstrādei.</span><span class="sxs-lookup"><span data-stu-id="4e80b-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="4e80b-107">Tās ir savrupas vides.</span><span class="sxs-lookup"><span data-stu-id="4e80b-107">They are standalone environments.</span></span> <span data-ttu-id="4e80b-108">Programmatūras kā pakalpojuma (SAA) arhitektūras rakstura dēļ tās neietver e-komercijas komponentus.</span><span class="sxs-lookup"><span data-stu-id="4e80b-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="4e80b-109">Dažos scenārijos, iespējams, vēlēsities testēt izsaukumus paplašinājumiem 1. līmeņa vidē, lai varētu atkļūdot paplašinājumus no e-komercijas komponentiem.</span><span class="sxs-lookup"><span data-stu-id="4e80b-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="4e80b-110">Vispārīgiem norādījumiem skatiet sadaļu [Atkļūdošana, izmantojot 1. līmeņa Commerce izstrādes vidi](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="4e80b-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="4e80b-111">Kad atkļūdojat, izmantojot 1. līmeņa vidi, jo vietne tagad izsauc citu Retail Server, starpservera izsaukumi var izraisīt dažādas kļūdas, kas saistītas ar satura drošības politiku.</span><span class="sxs-lookup"><span data-stu-id="4e80b-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="4e80b-112">Attēlā zemāk parādīts kļūdas piemērs, kura var rasties, ja preču informācijas lapā ir atlasīts variants.</span><span class="sxs-lookup"><span data-stu-id="4e80b-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Kļūda, ja preču informācijas lapā ir atlasīts variants](media/unhandled-rejection-error.jpg)

<span data-ttu-id="4e80b-114">Attēlā zemāk ir parādīts līdzīgas kļūdas piemērs pārlūka atkļūdotāja rīkos (F12 izstrādātāja rīki).</span><span class="sxs-lookup"><span data-stu-id="4e80b-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="4e80b-115">Kļūdas ziņojumā minēts satura drošības politikas direktīvas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="4e80b-115">The error message mentions violation of the content security policy directive.</span></span>

![Atkļūdotāja rīku kļūda](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="4e80b-117">Novēršana</span><span class="sxs-lookup"><span data-stu-id="4e80b-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="4e80b-118">Vietnes satura drošības politikas atspējošana Commerce vietnes veidotājam</span><span class="sxs-lookup"><span data-stu-id="4e80b-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="4e80b-119">Atlasiet vietni, pie kuras strādājat.</span><span class="sxs-lookup"><span data-stu-id="4e80b-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="4e80b-120">Atlasiet **Iestatījumi** un pēc tam atlasiet **Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="4e80b-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="4e80b-121">Cilnē **Satura drošības politika** atlasiet **Atspējot satura drošības politiku**.</span><span class="sxs-lookup"><span data-stu-id="4e80b-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="4e80b-122">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="4e80b-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="4e80b-123">Pierakstīšanās "uzņēmums-patērētājs" (B2C) nedarbosies vietējā izstrādes vidē.</span><span class="sxs-lookup"><span data-stu-id="4e80b-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="4e80b-124">Tomēr, ja nepieciešams, varat izmantot viesa norēķinu vai veidot lapas pārbaudes objektus, lai simulētu lietotāja pierakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="4e80b-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e80b-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4e80b-125">Additional resources</span></span>

[<span data-ttu-id="4e80b-126">Darba sākšana ar e-komercijas tiešsaistes paplašināmības izstrādi</span><span class="sxs-lookup"><span data-stu-id="4e80b-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="4e80b-127">Satura drošības politikas (CSP) pārvaldība e-komercijas vietnē</span><span class="sxs-lookup"><span data-stu-id="4e80b-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
