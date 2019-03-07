---
title: URL atvērš. POS
description: Šajā tēmā ir sniegts apskats par preču un debitoru meklēšanas funkcionalitātes uzlabojumiem programmā Microsoft Dynamics 365 for Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "327094"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="f9e8a-103">URL atvēršana POS</span><span class="sxs-lookup"><span data-stu-id="f9e8a-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9e8a-104">Šajā tēmā aprakstīts, kā konfig. pogu sistēmā Retail POS (pārdošanas punkts), lai atvērtu URL.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="f9e8a-105">Šim līdzeklim nav nepieciešama koda pielāgošana, un to var konfigurēt persona, kurai nav izstrādātāja lomas.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="f9e8a-106">Šis līdzeklis ir ietverts programmas Dynamics 365 for Finance and Operations versijas 8.1.3 laidienā (būvējums 8.1.227.10014) un jaunākās tās versijās.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="f9e8a-107">Šis līdzeklis ļauj konfigurēt pogu sistēmā POS, izmantojot pogu režģa veidotāju, lai atvērtu URL.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="f9e8a-108">Pašlaik tas tiek atbalstīts šādās konfigurācijās:</span><span class="sxs-lookup"><span data-stu-id="f9e8a-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="f9e8a-109">Atvērt jaunā logā.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-109">Open in new window.</span></span>
- <span data-ttu-id="f9e8a-110">Atvērt ar POS.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-110">Open within POS.</span></span>
- <span data-ttu-id="f9e8a-111">Atv. iekš. progr.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="f9e8a-112">Atvērt jaunā logā</span><span class="sxs-lookup"><span data-stu-id="f9e8a-112">Open in new window</span></span>

<span data-ttu-id="f9e8a-113">Šī konfigurācija nosaka, vai atvērt URL jaunā logā vai programmā.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="f9e8a-114">Ja ir konfigurēts, lai tīmekļa URL tiktu atvērts programmā, POS sānu navigācijas panelis un augšējā josla ir redzami un pieejami lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="f9e8a-115">Ja konfigurēta atvērš. jaunā logā, URL tiks atvērts jaunā logā programmā Modern POS operētājsist. Windows un jaunā pārlūkprogr. cilnē pārējos POS klientos.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="f9e8a-116">Lai to iespējotu, ir jākonfigurē URL, atlasot opciju **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="f9e8a-117">Atvērt ar POS</span><span class="sxs-lookup"><span data-stu-id="f9e8a-117">Open within POS</span></span>

<span data-ttu-id="f9e8a-118">Tīm. URL atvērš. ar POS tiek atbalst. tikai progr. Modern POS operētājs. Windows.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="f9e8a-119">Citos klientos šī iespēja ir izstrādes stadijā, un to plānots izlaist turpmākajos atjauninājumos.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="f9e8a-120">Lai to iespējotu, ir jākonfigurē URL, neatlasot opciju **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="f9e8a-121">Atv. iekš. progr.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-121">Open a native app</span></span>

<span data-ttu-id="f9e8a-122">Šis līdzeklis arī ļauj norādīt ne tīmekļa URL, lai atv. iekš. programmu.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="f9e8a-123">Piemēram, varat norādīt tādus URL protokolus kā MailTo, SIP, IM vai MSTEAMS, kurus pēc tam var apstrādāt attiecīgās iekšējās programmas resursierīcē.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="f9e8a-124">Lai to iespējotu, ir jākonfigurē URL, atlasot opciju **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="f9e8a-125">Windows datoru gadījumā sk. sadaļu [Eksportēt vai importēt noklus. progr. asociācijas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), lai iestatītu noklus. protokola asociācijas, ja iestatāt datoru, lietojot Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="f9e8a-126">Ja lietojat MDM, piem., Intune, lai pārvaldītu Windows datorus, sk. sad. [Polit. CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="f9e8a-127">Ja esat izstrādātājs, kas veido pielāg. tīm. vietni, sk. sad. [Palaist nokl. progr. URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="f9e8a-128">Integrēti atv. iekš. progr.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-128">Open a native app seamlessly</span></span>

<span data-ttu-id="f9e8a-129">Turklāt operētājsistēmas Windows, iOS un Android nodrošina nemanāmāku programmu atvēršanu, pamatojoties uz programmu protokola saistību.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="f9e8a-130">Ja progr. vēl nav konfig., lai veiktu atvēršanu no tīm. pārlūkprogr., var būt vajadzīgs izstrād., lai to konfigurētu.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="f9e8a-131">Windows — sk. [Iesp. progr. vietnēm, lietojot progr. URI apstrād.](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="f9e8a-132">iOS — sk. [Universālās saites izstrādātājiem](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="f9e8a-133">Informāciju par operētājsistēmu Android skatiet rakstā [Android programmu saišu apstrāde](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="f9e8a-134">Debitors</span><span class="sxs-lookup"><span data-stu-id="f9e8a-134">Client</span></span>                | <span data-ttu-id="f9e8a-135">Atvērt jaunā logā</span><span class="sxs-lookup"><span data-stu-id="f9e8a-135">Open in new window</span></span> | <span data-ttu-id="f9e8a-136">Atv. iekš. pr.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-136">Open native app</span></span> | <span data-ttu-id="f9e8a-137">Atvērt ar POS</span><span class="sxs-lookup"><span data-stu-id="f9e8a-137">Open within POS</span></span> | <span data-ttu-id="f9e8a-138">Detalizēta</span><span class="sxs-lookup"><span data-stu-id="f9e8a-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="f9e8a-139">Modern POS Windows</span><span class="sxs-lookup"><span data-stu-id="f9e8a-139">Modern POS on Windows</span></span> | <span data-ttu-id="f9e8a-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="f9e8a-140">✓\*</span></span>                | <span data-ttu-id="f9e8a-141">✓</span><span class="sxs-lookup"><span data-stu-id="f9e8a-141">✓</span></span>               | <span data-ttu-id="f9e8a-142">✓</span><span class="sxs-lookup"><span data-stu-id="f9e8a-142">✓</span></span>              | <span data-ttu-id="f9e8a-143">\* Atveras jaunā Modern POS logā</span><span class="sxs-lookup"><span data-stu-id="f9e8a-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="f9e8a-144">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="f9e8a-144">Cloud POS</span></span>             | <span data-ttu-id="f9e8a-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="f9e8a-145">✓\*</span></span>                | <span data-ttu-id="f9e8a-146">✓</span><span class="sxs-lookup"><span data-stu-id="f9e8a-146">✓</span></span>               | <span data-ttu-id="f9e8a-147">X</span><span class="sxs-lookup"><span data-stu-id="f9e8a-147">X</span></span>              | <span data-ttu-id="f9e8a-148">\* Atveras jaunā pārlūkprogrammas cilnē</span><span class="sxs-lookup"><span data-stu-id="f9e8a-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="f9e8a-149">Modern POS iOS</span><span class="sxs-lookup"><span data-stu-id="f9e8a-149">Modern POS on iOS</span></span>     | <span data-ttu-id="f9e8a-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="f9e8a-150">✓\*</span></span>                | <span data-ttu-id="f9e8a-151">✓</span><span class="sxs-lookup"><span data-stu-id="f9e8a-151">✓</span></span>               | <span data-ttu-id="f9e8a-152">X</span><span class="sxs-lookup"><span data-stu-id="f9e8a-152">X</span></span>              | <span data-ttu-id="f9e8a-153">\* Atveras jaunā pārlūkprogrammas cilnē</span><span class="sxs-lookup"><span data-stu-id="f9e8a-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="f9e8a-154">Modern POS operētājsistēmā Android</span><span class="sxs-lookup"><span data-stu-id="f9e8a-154">Modern POS on Android</span></span> | <span data-ttu-id="f9e8a-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="f9e8a-155">✓\*</span></span>                | <span data-ttu-id="f9e8a-156">✓</span><span class="sxs-lookup"><span data-stu-id="f9e8a-156">✓</span></span>               | <span data-ttu-id="f9e8a-157">X</span><span class="sxs-lookup"><span data-stu-id="f9e8a-157">X</span></span>              | <span data-ttu-id="f9e8a-158">\* Atveras jaunā pārlūkprogrammas cilnē</span><span class="sxs-lookup"><span data-stu-id="f9e8a-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="f9e8a-159">Pirms sākšanas</span><span class="sxs-lookup"><span data-stu-id="f9e8a-159">Before you begin</span></span>

<span data-ttu-id="f9e8a-160">Pirms sākat, pārskatiet, kā konfigurēt, — [Pārdošanas punkta (POS) ekrāna izkārtojumi](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="f9e8a-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="f9e8a-161">URL atvērš. POS</span><span class="sxs-lookup"><span data-stu-id="f9e8a-161">Open URL in POS</span></span>

<span data-ttu-id="f9e8a-162">Lai konfigurētu URL, kas tiks atvērts POS, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="f9e8a-163">Galv. birojā atv. sad. **Mazumt. \>. Kan. iestat. \> POS iestat. \> POS \> Ekr. izk.**.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="f9e8a-164">Atlasiet **Pogu režģi \> Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="f9e8a-165">Izveid. jaunu pogu.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-165">Create a new button.</span></span>
4. <span data-ttu-id="f9e8a-166">Atl. vienuma **Poga** rekviz.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="f9e8a-167">Atl. **Atvērt URL** kā darbību.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="f9e8a-168">Ievadiet URL, kuru gribat izmantot.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="f9e8a-169">Konfigurējiet, vai atvērt URL jaunā logā.</span><span class="sxs-lookup"><span data-stu-id="f9e8a-169">Configure whether to open the URL in a new window.</span></span>
