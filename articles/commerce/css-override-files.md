---
title: Darbs ar CSS pārlabošanas failiem
description: Šajā tēmā ir aprakstīts, kāpēc, kad un kā lietot stila lapas kaskadēšanas (CSS) pārlabošanas failus Microsoft pakalpojumā Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b5a50fc0c9060117cdddc0875446afc2edc12a11
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915443"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="303e8-103">Darbs ar CSS pārlabošanas failiem</span><span class="sxs-lookup"><span data-stu-id="303e8-103">Work with CSS override files</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="303e8-104">Šajā tēmā ir aprakstīts, kāpēc, kad un kā lietot stila lapas kaskadēšanas (CSS) pārlabošanas failus Microsoft pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="303e8-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="303e8-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="303e8-105">Overview</span></span>

<span data-ttu-id="303e8-106">Pastāvīgā vietā stili parasti būtu jāapstrādā, izmantojot vietnes tēmu.</span><span class="sxs-lookup"><span data-stu-id="303e8-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="303e8-107">Tēmas nodrošina galvenos CSSun stila iestatījumus moduļiem jebkurā lapā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="303e8-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="303e8-108">Tēmas tiek izveidotas, izmantojot Dynamics 365 Commerce tiešsaistes programmatūras izstrādes komplektu (SDK), un tās tiek izvietotas jūsu tīmekļa vietnēs, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="303e8-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="303e8-109">Tēmas atkļūdošanas iespējas un moduļa saskarnes konfigurācijas SDK palīdz vietnes izstrādātājiem izveidot pielāgojamas un vienotas vietņu noformējuma pakotnes.</span><span class="sxs-lookup"><span data-stu-id="303e8-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="303e8-110">Kad šīs dizaina pakotnes ir izvietotas vietnē, vietnes autori var koncentrēties uz satura izveidi, rediģēšanu un publicēšanu, nevis vietnes izstrādi.</span><span class="sxs-lookup"><span data-stu-id="303e8-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="303e8-111">Ņemot vērā parasto tēmas dzīves ciklu, atkarība no izstrādātājiem, lai veiktu stila izmaiņas, izmantojot SDK un LCS izvietošanas konveijeru, dažos gadījumos var būt pārmērīgi augsta.</span><span class="sxs-lookup"><span data-stu-id="303e8-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="303e8-112">Vietnes prototipi vai labojumfaili var šķist apgrūtinoši, ja SDK nav konfigurēts vai jums nav laika gaidīt uz LCS izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="303e8-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="303e8-113">Minētajās situācijās var palīdzēt CSS pārlabošanas faili.</span><span class="sxs-lookup"><span data-stu-id="303e8-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="303e8-114">Commerce autorēšanas rīkos autentificēti lietotāji var augšupielādēt CSS failu, priekšskatīt to un pēc tam aktivizēt, lai pārlabotu vietnes tēmu.</span><span class="sxs-lookup"><span data-stu-id="303e8-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="303e8-115">SDK vai LCS papildu izvietošana nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="303e8-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="303e8-116">CSS pārlabošanas failā norādītie labojumi var būt tik mazi kā viena teksta stila maiņa vai tik plaši kā pilnīgas zīmola izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="303e8-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="303e8-117">Pirms izmantojat CSSpārlabošanas failus, ņemiet vērā šādus ierobežojumus:</span><span class="sxs-lookup"><span data-stu-id="303e8-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="303e8-118">Vietnē vienlaikus var būt aktīvs tikai viens CSS pārlabošanas fails.</span><span class="sxs-lookup"><span data-stu-id="303e8-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="303e8-119">Tādēļ visiem aktīvajiem labojumiem ir jābūt vienā pārlabošanas failā.</span><span class="sxs-lookup"><span data-stu-id="303e8-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="303e8-120">Lai gan jūs varat priekšskatīt labojumus Commerce autorēšanas rīkos, nav īpašu atkļūdošanas iespēju, lai palīdzētu identificēt visas kļūmes, kuras labojumi varētu ieviest.</span><span class="sxs-lookup"><span data-stu-id="303e8-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="303e8-121">Citiem vārdiem sakot, izmantojot CSS pārlabošanas failus, jūsu rīcībā nav tāda pati rīkkopa, ko SDK nodrošina moduļa un autorēšanas validācijai.</span><span class="sxs-lookup"><span data-stu-id="303e8-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="303e8-122">Tomēr CSS pārlabošanas faili nodrošina ātru veidu, kādā izveidot dizaina prototipu vai ieviest labojumfailu, pirms pilns tēma atjauninājums ir izstrādāts un izvietots.</span><span class="sxs-lookup"><span data-stu-id="303e8-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="303e8-123">CSS pārlabošanas faila izveide</span><span class="sxs-lookup"><span data-stu-id="303e8-123">Create a CSS override file</span></span>

<span data-ttu-id="303e8-124">Lai izveidotu CSS pārlabošanas failu, varat izmantot jebkuru integrēto izstrādes vidi (IDE), teksta redaktoru vai avota koda redaktoru.</span><span class="sxs-lookup"><span data-stu-id="303e8-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="303e8-125">Tipiska pieeja ir izmantot standarta tīmekļa atkļūdotājus jūsu pārlūkprogrammā, lai identificētu stilu atlasītājus, rekvizītus un vērtības jūsu esošajā vietnē.</span><span class="sxs-lookup"><span data-stu-id="303e8-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="303e8-126">Vairākums pārlūkprogrammu ļauj mainīt vērtības un priekšskatīt tās atkļūdotājā.</span><span class="sxs-lookup"><span data-stu-id="303e8-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="303e8-127">Kad esat identificējis izmaiņas, kuras vēlaties veikt, varat tās saglabāt savā CSS failā.</span><span class="sxs-lookup"><span data-stu-id="303e8-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="303e8-128">CSS pārlabošanas faila augšupielāde</span><span class="sxs-lookup"><span data-stu-id="303e8-128">Upload a CSS override file</span></span>

<span data-ttu-id="303e8-129">Lai Commerce vietnē augšupielādētu CSS failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="303e8-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="303e8-130">Autorēšanas rīkos dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="303e8-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="303e8-131">Navigācijas rūtī kreisajā pusē atlasiet **Dizains**.</span><span class="sxs-lookup"><span data-stu-id="303e8-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="303e8-132">Atkarībā no Commerce autorēšanas rīku versijas, ko lietojat, iespējams, navigācijas rūtī ir jāpaplašina **Iestatījumi**, lai varētu atlasīt **Dizainu**.</span><span class="sxs-lookup"><span data-stu-id="303e8-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="303e8-133">Galvenās noformējuma rūts augšdaļā atlasiet cilni **CSS pārlabošana**, ja tā vēl nav atlasīta.</span><span class="sxs-lookup"><span data-stu-id="303e8-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="303e8-134">Sadaļā **Pieejamie CSS labojumi**atlasiet **Augšupielādēt CSS failu**.</span><span class="sxs-lookup"><span data-stu-id="303e8-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="303e8-135">Parādās failu pārlūka logs.</span><span class="sxs-lookup"><span data-stu-id="303e8-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="303e8-136">Failu pārlūkā atrodiet un atlasiet CSS failu un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="303e8-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="303e8-137">Augšupielādētais CSS fails tagad tiek parādīts sadaļā **Pieejamie CSS labojumi**.</span><span class="sxs-lookup"><span data-stu-id="303e8-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="303e8-138">CSS pārlabošanas faila priekšskatīšana</span><span class="sxs-lookup"><span data-stu-id="303e8-138">Preview a CSS override file</span></span>

<span data-ttu-id="303e8-139">Lai priekšskatītu CSS pārlabošanas failu, pirms veicat tā aktīvu darbību savā tiešsaistes vietnē, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="303e8-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="303e8-140">Kreisajā navigācijas rūtī atlasiet  **Dizains**un pēc tam cilnē **CSS labojums** sadaļā **Pieejamie CSS labojumi** atrodiet CSS failu, kuru vēlaties priekšskatīt.</span><span class="sxs-lookup"><span data-stu-id="303e8-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="303e8-141">Blakus CSS faila nosaukumam atlasiet **Priekšskatījuma vietne**.</span><span class="sxs-lookup"><span data-stu-id="303e8-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="303e8-142">Dialoglodziņā **Atlasīt vietrādi URL** atlasiet tās vietnes vietrādi URL, kurai vēlaties skatīt ignorēšanas opciju, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="303e8-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="303e8-143">Ja atlasītajam vietrādim URL ir vairāki varianti, parādītajā dialoglodziņā **Priekšskatījuma variācijas** atlasiet vēlamo variantu.</span><span class="sxs-lookup"><span data-stu-id="303e8-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="303e8-144">Tiek atvērta jauna pārlūkprogrammas cilne vai logs, kurā varat validēt stila labojumus jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="303e8-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="303e8-145">Pēc tam varat kopīgot vietrādi URL ar citiem autentificētiem Commerce lietotājiem apskatiem un atsauksmēm.</span><span class="sxs-lookup"><span data-stu-id="303e8-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="303e8-146">CSS pārlabošanas faila aktivizēšana jūsu tiešsaistes vietnē</span><span class="sxs-lookup"><span data-stu-id="303e8-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="303e8-147">Kad esat priekšskatījis un apstiprinājis CSS pārlabošanas failu, varat to aktivizēt tiešsaistes vietnē.</span><span class="sxs-lookup"><span data-stu-id="303e8-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="303e8-148">Vietnē vienlaikus var būt aktīvs tikai viens CSS pārlabošanas fails.</span><span class="sxs-lookup"><span data-stu-id="303e8-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="303e8-149">Ja aktivizējat jaunu pārlabošanas failu, iepriekšējais pārlabošanas fails tiek deaktivizēts.</span><span class="sxs-lookup"><span data-stu-id="303e8-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="303e8-150">Tādēļ pārliecinieties, ka visi nepieciešamie labojumi atrodas vienā CSS pārlabošanas failā.</span><span class="sxs-lookup"><span data-stu-id="303e8-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="303e8-151">Lai aktivizētu CSS pārlabošanas failu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="303e8-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="303e8-152">Kreisajā navigācijas rūtī atlasiet  **Dizains**un pēc tam cilnē **CSS labojums** sadaļā **Pieejamie CSS labojumi** atrodiet CSS failu, kuru vēlaties aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="303e8-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="303e8-153">Sadaļā CSS faila nosaukums atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="303e8-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="303e8-154">Pārlabotais fails nekavējoties kļūst aktīvs jūsu tiešsaistes vietnē.</span><span class="sxs-lookup"><span data-stu-id="303e8-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="303e8-155">CSS pārlabošanas faila deaktivizēšana jūsu tiešsaistes vietnē</span><span class="sxs-lookup"><span data-stu-id="303e8-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="303e8-156">Lai deaktivizētu CSS pārlabošanas failu savā vietnē, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="303e8-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="303e8-157">Kreisajā navigācijas rūtī atlasiet  **Dizains**un pēc tam cilnē **CSS labojums** sadaļā **Pieejamie CSS labojumi** atrodiet CSS failu, kuru vēlaties deaktivizēt.</span><span class="sxs-lookup"><span data-stu-id="303e8-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="303e8-158">Sadaļā CSS faila nosaukums atlasiet **Deaktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="303e8-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="303e8-159">Pārlabotais fails nekavējoties kļūst neaktīvs jūsu tiešsaistes vietnē.</span><span class="sxs-lookup"><span data-stu-id="303e8-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="303e8-160">Lai piekļūtu papildu opcijām CSS pārlabošanas failiem, atlasiet daudzpunkti (**...**) blakus CSS faila nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="303e8-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="303e8-161">Opcijas **Lejupielādēt**, **Pārdēvēt**un **Aizstāt** ir noderīgas, lai ātri varētu veikt esošā CSS pārlabošanas faila izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="303e8-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="303e8-162">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="303e8-162">Additional resources</span></span>

[<span data-ttu-id="303e8-163">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="303e8-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="303e8-164">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="303e8-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="303e8-165">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="303e8-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="303e8-166">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="303e8-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="303e8-167">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="303e8-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="303e8-168">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="303e8-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="303e8-169">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="303e8-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)