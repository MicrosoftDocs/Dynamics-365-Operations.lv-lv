---
title: Konfidencialitātes politikas lapas pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot konfidencialitātes politikas lapu savai vietnei programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59a2d9712a73c607cf5521f8e79e8e2558854fc4
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2020
ms.locfileid: "3274215"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="18e43-103">Konfidencialitātes politikas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="18e43-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="18e43-104">Šajā tēmā ir aprakstīts, kā pievienot konfidencialitātes politikas lapu savai vietnei programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18e43-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="18e43-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="18e43-105">Overview</span></span>

<span data-ttu-id="18e43-106">Konfidencialitātes ievērošana ietver organizatoriskus pasākumus, kas informē vietnes lietotājus par to, kā tiek apkopoti un apstrādāti viņu dati.</span><span class="sxs-lookup"><span data-stu-id="18e43-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="18e43-107">Pēc tam lietotāji var izlemt, kā viņi vēlas, lai viņu personas dati tiktu apstrādāti, un var veikt atbilstošas darbības.</span><span class="sxs-lookup"><span data-stu-id="18e43-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="18e43-108">Pārskatiet Microsoft paziņojumu par konfidencialitāti pakalpojumā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="18e43-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="18e43-109">Lai pārskatītu Microsoft paziņojumu par konfidencialitāti, kamēr esat pieteicies Dynamics 365 Commerce autorēšanas rīkos, augšējā labajā stūrī atlasiet pogu **Palīdzība** (**?**) un pēc tam atlasiet **Konfidencialitāte un sīkfaili**.</span><span class="sxs-lookup"><span data-stu-id="18e43-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="18e43-110">Tiek atvērta jauna cilne, kurā ir saite uz [Microsoft paziņojumu par konfidencialitāti](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="18e43-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="18e43-111">Konfidencialitātes politikas lapas izveide jūsu vietnei</span><span class="sxs-lookup"><span data-stu-id="18e43-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="18e43-112">Pakalpojumā Dynamics 365 Commerce ir iespējami vairāki veidi, kā vietnes lietotājiem sniegt piekļuvi jūsu konfidencialitātes politikai.</span><span class="sxs-lookup"><span data-stu-id="18e43-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="18e43-113">Šajā sadaļā ir parādīts, kā izveidot konfidencialitātes politikas lapu un pēc tam atsaukties uz lapu, izmantojot kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="18e43-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="18e43-114">Vadlīnijas, kas redzamas tālāk piemērā, parāda, kā veidot vispārēju konfidencialitātes lapu Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="18e43-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="18e43-115">Jūs esat atbildīgs par to, lai izstrādātu un ieviestu tādu konfidencialitātes politikas lapas risinājumu, kas vislabāk atbilst jūsu uzņēmuma juridiskajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="18e43-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="18e43-116">Lai sāktu, autorēšanas rīkos dodieties uz vietni, kurai vēlaties izveidot konfidencialitātes politikas lapu.</span><span class="sxs-lookup"><span data-stu-id="18e43-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="18e43-117">Izveidot veidni</span><span class="sxs-lookup"><span data-stu-id="18e43-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="18e43-118">Ja veidne, ko var izmantot konfidencialitātes politikas lapā, jau ir izveidota, pārejiet uz priekšu uz sadaļu [Konfidencialitātes politikas izveide](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="18e43-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="18e43-119">Lai izveidotu veidni, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="18e43-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="18e43-120">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="18e43-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="18e43-121">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Veicināšanas reklāmkaroga veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="18e43-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="18e43-122">Veidnē pievienojiet nepieciešamos moduļus nepieciešamajiem lapas slotiem.</span><span class="sxs-lookup"><span data-stu-id="18e43-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="18e43-123">Lai iegūtu norādījumus, virziet kursoru virs sarkanajām izsaukuma zīmēm.</span><span class="sxs-lookup"><span data-stu-id="18e43-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="18e43-124">(Piemēram, **HTML galvenais** slotam var būt nepieciešams **Noklusējuma ārējā skripta** modulis.)</span><span class="sxs-lookup"><span data-stu-id="18e43-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="18e43-125">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="18e43-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="18e43-126">Moduļa **Noklusējuma lapa** slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="18e43-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="18e43-127">Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.</span><span class="sxs-lookup"><span data-stu-id="18e43-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="18e43-128">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="18e43-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="18e43-129">Konfidencialitātes politikas lapas izveide</span><span class="sxs-lookup"><span data-stu-id="18e43-129">Build a privacy policy page</span></span>

<span data-ttu-id="18e43-130">Lai izveidotu konfidencialitātes politikas lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="18e43-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="18e43-131">Dodieties uz **Lapas** un pēc tam atlasiet **Jaunas lapas fragments**, lai izveidotu lapu.</span><span class="sxs-lookup"><span data-stu-id="18e43-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="18e43-132">Dialoglodziņā **Izvēlēties veidni** atlasiet konfidencialitātes politikas lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="18e43-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="18e43-133">Ievadiet lapas nosaukumu un lapas vietrādi URL pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="18e43-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="18e43-134">Jaunās lapas slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="18e43-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="18e43-135">Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.</span><span class="sxs-lookup"><span data-stu-id="18e43-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="18e43-136">Moduļa **Bagātinātā satura bloks** rekvizītu rūtī atlasiet **Pievienot datu avotu** un tad atlasiet **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="18e43-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="18e43-137">Bagātinātā teksta redaktorā ievadiet konfidencialitātes politikas lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="18e43-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="18e43-138">Izvērsiet bagātinātā teksta redaktoru uz pilnekrāna režīmu, kā jums nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="18e43-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="18e43-139">Kad esat pabeidzis satura ievadīšanu, atlasiet **Priekšskatījums**, lai priekšskatītu lapu tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="18e43-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="18e43-140">Aizpildiet visus atlikušos lapas un moduļa rekvizītu papildinājumus.</span><span class="sxs-lookup"><span data-stu-id="18e43-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="18e43-141">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="18e43-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="18e43-142">Lai publicētu vietrādi URL konfidencialitātes politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="18e43-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="18e43-143">Pārejiet uz sadaļu **URL** un atlasiet konfidencialitātes politikas lapas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="18e43-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="18e43-144">Atlasiet **Publicēt**, lai publicētu atlasīto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="18e43-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="18e43-145">Saites, ka novirza uz konfidencialitātes politiku lapu, izveide kājenē</span><span class="sxs-lookup"><span data-stu-id="18e43-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="18e43-146">Varat pievienot saiti uz konfidencialitātes politikas lapu fragmentam.</span><span class="sxs-lookup"><span data-stu-id="18e43-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="18e43-147">Šādā veidā varat kopīgot saiti un atjaunināt to vairākās vietnes lapās, atsaucoties uz fragmentu.</span><span class="sxs-lookup"><span data-stu-id="18e43-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="18e43-148">Šajā piemērā parādīts, kā pievienot saiti uz konfidencialitātes politikas lapu kājenes fragmentam.</span><span class="sxs-lookup"><span data-stu-id="18e43-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="18e43-149">Lai fragmentam pievienotu saiti, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="18e43-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="18e43-150">Dodieties uz **Lapas fragmenti** un pēc tam atlasiet **Jaunas lapas fragments**, lai izveidotu lapas fragmentu.</span><span class="sxs-lookup"><span data-stu-id="18e43-150">Go to **Page Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="18e43-151">Dialoglodziņā **Jaunas lapas fragments** atlasiet **Kājenes** moduli.</span><span class="sxs-lookup"><span data-stu-id="18e43-151">In the **New Page Fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="18e43-152">Sadaļā **Lapas fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="18e43-152">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="18e43-153">Slotā **Kājene kategorija** pievienojiet moduli **Kājenes vienums**.</span><span class="sxs-lookup"><span data-stu-id="18e43-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="18e43-154">Rekvizītu rūts labajā pusē atlasiet **Saites teksts**.</span><span class="sxs-lookup"><span data-stu-id="18e43-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="18e43-155">Dialoglodziņā **Saites teksts** ievadiet konfidencialitātes politikas lapas saites tekstu un saites mērķi un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="18e43-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="18e43-156">Lai iegūtu konfidencialitātes politikas lapas vietrādi URL, atveriet **Lapas**, dodieties uz konfidencialitātes politikas lapu un kopējiet vietrādi URL no rekvizītu rūts.</span><span class="sxs-lookup"><span data-stu-id="18e43-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="18e43-157">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="18e43-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="18e43-158">Priekšskatiet fragmentu un pārbaudiet saiti uz konfidencialitātes politikas lapu.</span><span class="sxs-lookup"><span data-stu-id="18e43-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="18e43-159">Uz fragmentu tagad var atsaukties veidnē citām vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="18e43-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="18e43-160">Ja uz šo fragmentu ir atsauce veidnes modulī **Kājene**, saites atsauce tiks parādīta visās lapās, kas ir veidotas, izmantojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="18e43-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18e43-161">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="18e43-161">Additional resources</span></span>

[<span data-ttu-id="18e43-162">Atbilstības pārskats</span><span class="sxs-lookup"><span data-stu-id="18e43-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="18e43-163">Pieejamības līdzekļi un iespējas</span><span class="sxs-lookup"><span data-stu-id="18e43-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="18e43-164">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="18e43-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="18e43-165">Aizstāt lietotāja ID, kas saistīti ar izsekotām satura izmaiņām</span><span class="sxs-lookup"><span data-stu-id="18e43-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
