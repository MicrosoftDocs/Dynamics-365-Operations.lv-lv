---
title: URL atvērš. POS
description: Šajā tēmā ir sniegts apskats par preču un debitoru meklēšanas funkcionalitātes uzlabojumiem programmā Dynamics 365 Commerce.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 137b699d5f60b9b62a5ce9501e3b2a262e60a88f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023235"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="70480-103">URL atvēršana POS</span><span class="sxs-lookup"><span data-stu-id="70480-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70480-104">Šajā tēmā aprakstīts, kā konfig. pogu sistēmā Retail POS (pārdošanas punkts), lai atvērtu URL.</span><span class="sxs-lookup"><span data-stu-id="70480-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="70480-105">Šim līdzeklim nav nepieciešama koda pielāgošana, un to var konfigurēt persona, kurai nav izstrādātāja lomas.</span><span class="sxs-lookup"><span data-stu-id="70480-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="70480-106">Šis līdzeklis ļauj konfigurēt pogu sistēmā POS, izmantojot pogu režģa veidotāju, lai atvērtu URL.</span><span class="sxs-lookup"><span data-stu-id="70480-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="70480-107">Pašlaik tas tiek atbalstīts šādās konfigurācijās:</span><span class="sxs-lookup"><span data-stu-id="70480-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="70480-108">Atvērt jaunā logā.</span><span class="sxs-lookup"><span data-stu-id="70480-108">Open in new window.</span></span>
- <span data-ttu-id="70480-109">Atvērt ar POS.</span><span class="sxs-lookup"><span data-stu-id="70480-109">Open within POS.</span></span>
- <span data-ttu-id="70480-110">Atv. iekš. progr.</span><span class="sxs-lookup"><span data-stu-id="70480-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="70480-111">Atvērt jaunā logā</span><span class="sxs-lookup"><span data-stu-id="70480-111">Open in new window</span></span>

<span data-ttu-id="70480-112">Šī konfigurācija nosaka, vai atvērt URL jaunā logā vai programmā.</span><span class="sxs-lookup"><span data-stu-id="70480-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="70480-113">Ja ir konfigurēts, lai tīmekļa URL tiktu atvērts programmā, POS sānu navigācijas panelis un augšējā josla ir redzami un pieejami lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="70480-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="70480-114">Ja konfigurēta atvērš. jaunā logā, URL tiks atvērts jaunā logā programmā Modern POS operētājsist. Windows un jaunā pārlūkprogr. cilnē pārējos POS klientos.</span><span class="sxs-lookup"><span data-stu-id="70480-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="70480-115">Lai to iespējotu, ir jākonfigurē URL, atlasot opciju **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="70480-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="70480-116">Atvērt ar POS</span><span class="sxs-lookup"><span data-stu-id="70480-116">Open within POS</span></span>

<span data-ttu-id="70480-117">Tīm. URL atvērš. ar POS tiek atbalst. tikai progr. Modern POS operētājs. Windows.</span><span class="sxs-lookup"><span data-stu-id="70480-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="70480-118">Citos klientos šī iespēja ir izstrādes stadijā, un to plānots izlaist turpmākajos atjauninājumos.</span><span class="sxs-lookup"><span data-stu-id="70480-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="70480-119">Lai to iespējotu, ir jākonfigurē URL, neatlasot opciju **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="70480-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="70480-120">Atv. iekš. progr.</span><span class="sxs-lookup"><span data-stu-id="70480-120">Open a native app</span></span>

<span data-ttu-id="70480-121">Šis līdzeklis arī ļauj norādīt ne tīmekļa URL, lai atv. iekš. programmu.</span><span class="sxs-lookup"><span data-stu-id="70480-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="70480-122">Piemēram, varat norādīt tādus URL protokolus kā MailTo, SIP, IM vai MSTEAMS, kurus pēc tam var apstrādāt attiecīgās iekšējās programmas resursierīcē.</span><span class="sxs-lookup"><span data-stu-id="70480-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="70480-123">Lai to iespējotu, ir jākonfigurē URL, atlasot opciju **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="70480-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="70480-124">Windows datoru gadījumā sk. sadaļu [Eksportēt vai importēt noklus. progr. asociācijas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), lai iestatītu noklus. protokola asociācijas, ja iestatāt datoru, lietojot Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="70480-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="70480-125">Ja lietojat MDM, piem., Intune, lai pārvaldītu Windows datorus, sk. sad. [Polit. CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="70480-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="70480-126">Ja esat izstrādātājs, kas veido pielāg. tīm. vietni, sk. sad. [Palaist nokl. progr. URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="70480-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="70480-127">Integrēti atv. iekš. progr.</span><span class="sxs-lookup"><span data-stu-id="70480-127">Open a native app seamlessly</span></span>

<span data-ttu-id="70480-128">Turklāt operētājsistēmas Windows, iOS un Android nodrošina nemanāmāku programmu atvēršanu, pamatojoties uz programmu protokola saistību.</span><span class="sxs-lookup"><span data-stu-id="70480-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="70480-129">Ja progr. vēl nav konfig., lai veiktu atvēršanu no tīm. pārlūkprogr., var būt vajadzīgs izstrād., lai to konfigurētu.</span><span class="sxs-lookup"><span data-stu-id="70480-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="70480-130">Windows — sk. [Iesp. progr. vietnēm, lietojot progr. URI apstrād.](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="70480-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="70480-131">iOS — sk. [Universālās saites izstrādātājiem](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="70480-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="70480-132">Informāciju par operētājsistēmu Android skatiet rakstā [Android programmu saišu apstrāde](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="70480-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="70480-133">Debitors</span><span class="sxs-lookup"><span data-stu-id="70480-133">Client</span></span>                | <span data-ttu-id="70480-134">Atvērt jaunā logā</span><span class="sxs-lookup"><span data-stu-id="70480-134">Open in new window</span></span> | <span data-ttu-id="70480-135">Atv. iekš. pr.</span><span class="sxs-lookup"><span data-stu-id="70480-135">Open native app</span></span> | <span data-ttu-id="70480-136">Atvērt ar POS</span><span class="sxs-lookup"><span data-stu-id="70480-136">Open within POS</span></span> | <span data-ttu-id="70480-137">Detalizēta</span><span class="sxs-lookup"><span data-stu-id="70480-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="70480-138">Modern POS Windows</span><span class="sxs-lookup"><span data-stu-id="70480-138">Modern POS on Windows</span></span> | <span data-ttu-id="70480-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="70480-139">✓\*</span></span>                | <span data-ttu-id="70480-140">✓</span><span class="sxs-lookup"><span data-stu-id="70480-140">✓</span></span>               | <span data-ttu-id="70480-141">✓</span><span class="sxs-lookup"><span data-stu-id="70480-141">✓</span></span>              | <span data-ttu-id="70480-142">\* Atveras jaunā Modern POS logā</span><span class="sxs-lookup"><span data-stu-id="70480-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="70480-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="70480-143">Cloud POS</span></span>             | <span data-ttu-id="70480-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="70480-144">✓\*</span></span>                | <span data-ttu-id="70480-145">✓</span><span class="sxs-lookup"><span data-stu-id="70480-145">✓</span></span>               | <span data-ttu-id="70480-146">X</span><span class="sxs-lookup"><span data-stu-id="70480-146">X</span></span>              | <span data-ttu-id="70480-147">\* Atveras jaunā pārlūkprogrammas cilnē</span><span class="sxs-lookup"><span data-stu-id="70480-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="70480-148">Modern POS iOS</span><span class="sxs-lookup"><span data-stu-id="70480-148">Modern POS on iOS</span></span>     | <span data-ttu-id="70480-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="70480-149">✓\*</span></span>                | <span data-ttu-id="70480-150">✓</span><span class="sxs-lookup"><span data-stu-id="70480-150">✓</span></span>               | <span data-ttu-id="70480-151">X</span><span class="sxs-lookup"><span data-stu-id="70480-151">X</span></span>              | <span data-ttu-id="70480-152">\* Atveras jaunā pārlūkprogrammas cilnē</span><span class="sxs-lookup"><span data-stu-id="70480-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="70480-153">Modern POS operētājsistēmā Android</span><span class="sxs-lookup"><span data-stu-id="70480-153">Modern POS on Android</span></span> | <span data-ttu-id="70480-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="70480-154">✓\*</span></span>                | <span data-ttu-id="70480-155">✓</span><span class="sxs-lookup"><span data-stu-id="70480-155">✓</span></span>               | <span data-ttu-id="70480-156">X</span><span class="sxs-lookup"><span data-stu-id="70480-156">X</span></span>              | <span data-ttu-id="70480-157">\* Atveras jaunā pārlūkprogrammas cilnē</span><span class="sxs-lookup"><span data-stu-id="70480-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="70480-158">Pirms sākšanas</span><span class="sxs-lookup"><span data-stu-id="70480-158">Before you begin</span></span>

<span data-ttu-id="70480-159">Pirms sākat, pārskatiet, kā konfigurēt, — [Pārdošanas punkta (POS) ekrāna izkārtojumi](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="70480-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="70480-160">URL atvērš. POS</span><span class="sxs-lookup"><span data-stu-id="70480-160">Open URL in POS</span></span>

<span data-ttu-id="70480-161">Lai konfigurētu URL, kas tiks atvērts POS, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="70480-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="70480-162">Galvenajā birojā atveriet **Retail and Commerce\>Kanāla iestatījumi \> POS iestatījumi \> POS \> Ekrāna izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="70480-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="70480-163">Atlasiet **Pogu režģi \> Veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="70480-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="70480-164">Izveid. jaunu pogu.</span><span class="sxs-lookup"><span data-stu-id="70480-164">Create a new button.</span></span>
4. <span data-ttu-id="70480-165">Atl. vienuma **Poga** rekviz.</span><span class="sxs-lookup"><span data-stu-id="70480-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="70480-166">Atl. **Atvērt URL** kā darbību.</span><span class="sxs-lookup"><span data-stu-id="70480-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="70480-167">Ievadiet URL, kuru gribat izmantot.</span><span class="sxs-lookup"><span data-stu-id="70480-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="70480-168">Konfigurējiet, vai atvērt URL jaunā logā.</span><span class="sxs-lookup"><span data-stu-id="70480-168">Configure whether to open the URL in a new window.</span></span>
