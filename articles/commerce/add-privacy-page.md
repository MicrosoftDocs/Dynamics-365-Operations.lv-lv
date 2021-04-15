---
title: Konfidencialitātes politikas lapas pievienošana
description: Šajā tēmā aprakstīts, kā pievienot privātuma politikas lapu vietnei risinājumā Microsoft Dynamics 365 Commerce.
author: v-chgri
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
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797531"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="83f8a-103">Konfidencialitātes politikas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="83f8a-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83f8a-104">Šajā tēmā aprakstīts, kā pievienot privātuma politikas lapu vietnei risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="83f8a-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="83f8a-105">Konfidencialitātes ievērošana ietver organizatoriskus pasākumus, kas informē vietnes lietotājus par to, kā tiek apkopoti un apstrādāti viņu dati.</span><span class="sxs-lookup"><span data-stu-id="83f8a-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="83f8a-106">Pēc tam lietotāji var izlemt, kā viņi vēlas, lai viņu personas dati tiktu apstrādāti, un var veikt atbilstošas darbības.</span><span class="sxs-lookup"><span data-stu-id="83f8a-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="83f8a-107">Pārskatiet Microsoft paziņojumu par konfidencialitāti pakalpojumā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="83f8a-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="83f8a-108">Lai pārskatītu Microsoft paziņojumu par konfidencialitāti, kamēr esat pieteicies Dynamics 365 Commerce autorēšanas rīkos, augšējā labajā stūrī atlasiet pogu **Palīdzība** (**?**) un pēc tam atlasiet **Konfidencialitāte un sīkfaili**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="83f8a-109">Tiek atvērta jauna cilne, kurā ir saite uz [Microsoft paziņojumu par konfidencialitāti](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="83f8a-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="83f8a-110">Konfidencialitātes politikas lapas izveide jūsu vietnei</span><span class="sxs-lookup"><span data-stu-id="83f8a-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="83f8a-111">Pakalpojumā Dynamics 365 Commerce ir iespējami vairāki veidi, kā vietnes lietotājiem sniegt piekļuvi jūsu konfidencialitātes politikai.</span><span class="sxs-lookup"><span data-stu-id="83f8a-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="83f8a-112">Šajā sadaļā ir parādīts, kā izveidot konfidencialitātes politikas lapu un pēc tam atsaukties uz lapu, izmantojot kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="83f8a-113">Vadlīnijas, kas redzamas tālāk piemērā, parāda, kā veidot vispārēju konfidencialitātes lapu Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="83f8a-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="83f8a-114">Jūs esat atbildīgs par to, lai izstrādātu un ieviestu tādu konfidencialitātes politikas lapas risinājumu, kas vislabāk atbilst jūsu uzņēmuma juridiskajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="83f8a-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="83f8a-115">Lai sāktu, autorēšanas rīkos dodieties uz vietni, kurai vēlaties izveidot konfidencialitātes politikas lapu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="83f8a-116">Izveidot veidni</span><span class="sxs-lookup"><span data-stu-id="83f8a-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="83f8a-117">Ja veidne, ko var izmantot konfidencialitātes politikas lapā, jau ir izveidota, pārejiet uz priekšu uz sadaļu [Konfidencialitātes politikas izveide](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="83f8a-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="83f8a-118">Lai izveidotu veidni, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="83f8a-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="83f8a-119">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="83f8a-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="83f8a-120">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Veicināšanas reklāmkaroga veidni** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="83f8a-121">Veidnē pievienojiet nepieciešamos moduļus nepieciešamajiem lapas slotiem.</span><span class="sxs-lookup"><span data-stu-id="83f8a-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="83f8a-122">Lai iegūtu norādījumus, virziet kursoru virs sarkanajām izsaukuma zīmēm.</span><span class="sxs-lookup"><span data-stu-id="83f8a-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="83f8a-123">(Piemēram, **HTML galvenais** slotam var būt nepieciešams **Noklusējuma ārējā skripta** modulis.)</span><span class="sxs-lookup"><span data-stu-id="83f8a-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="83f8a-124">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="83f8a-125">Moduļa **Noklusējuma lapa** slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="83f8a-126">Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="83f8a-127">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="83f8a-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="83f8a-128">Konfidencialitātes politikas lapas izveide</span><span class="sxs-lookup"><span data-stu-id="83f8a-128">Build a privacy policy page</span></span>

<span data-ttu-id="83f8a-129">Lai izveidotu konfidencialitātes politikas lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="83f8a-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="83f8a-130">Dodieties uz **Lapas** un pēc tam atlasiet **Jaunas lapas fragments**, lai izveidotu lapu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="83f8a-131">Dialoglodziņā **Izvēlēties veidni** atlasiet konfidencialitātes politikas lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="83f8a-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="83f8a-132">Ievadiet lapas nosaukumu un lapas vietrādi URL pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="83f8a-133">Jaunās lapas slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="83f8a-134">Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="83f8a-135">Moduļa **Bagātinātā satura bloks** rekvizītu rūtī atlasiet **Pievienot datu avotu** un tad atlasiet **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="83f8a-136">Bagātinātā teksta redaktorā ievadiet konfidencialitātes politikas lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="83f8a-137">Izvērsiet bagātinātā teksta redaktoru uz pilnekrāna režīmu, kā jums nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="83f8a-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="83f8a-138">Kad esat pabeidzis satura ievadīšanu, atlasiet **Priekšskatījums**, lai priekšskatītu lapu tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="83f8a-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="83f8a-139">Aizpildiet visus atlikušos lapas un moduļa rekvizītu papildinājumus.</span><span class="sxs-lookup"><span data-stu-id="83f8a-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="83f8a-140">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="83f8a-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="83f8a-141">Lai publicētu vietrādi URL konfidencialitātes politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="83f8a-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="83f8a-142">Pārejiet uz sadaļu **URL** un atlasiet konfidencialitātes politikas lapas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="83f8a-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="83f8a-143">Atlasiet **Publicēt**, lai publicētu atlasīto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="83f8a-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="83f8a-144">Saites, ka novirza uz konfidencialitātes politiku lapu, izveide kājenē</span><span class="sxs-lookup"><span data-stu-id="83f8a-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="83f8a-145">Varat pievienot saiti uz konfidencialitātes politikas lapu fragmentam.</span><span class="sxs-lookup"><span data-stu-id="83f8a-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="83f8a-146">Šādā veidā varat kopīgot saiti un atjaunināt to vairākās vietnes lapās, atsaucoties uz fragmentu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="83f8a-147">Šajā piemērā parādīts, kā pievienot saiti uz konfidencialitātes politikas lapu kājenes fragmentam.</span><span class="sxs-lookup"><span data-stu-id="83f8a-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="83f8a-148">Lai fragmentam pievienotu saiti, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="83f8a-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="83f8a-149">Dodieties uz **Fragmenti** un pēc tam atlasiet **Jaunas lapas fragments**, lai izveidotu lapas fragmentu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="83f8a-150">Dialoglodziņā **Jauns fragments** atlasiet **Kājenes** moduli.</span><span class="sxs-lookup"><span data-stu-id="83f8a-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="83f8a-151">Sadaļā **Fragmenta nosaukums** ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="83f8a-152">Slotā **Kājene kategorija** pievienojiet moduli **Kājenes vienums**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="83f8a-153">Rekvizītu rūts labajā pusē atlasiet **Saites teksts**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="83f8a-154">Dialoglodziņā **Saites teksts** ievadiet konfidencialitātes politikas lapas saites tekstu un saites mērķi un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83f8a-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="83f8a-155">Lai iegūtu konfidencialitātes politikas lapas vietrādi URL, atveriet **Lapas**, dodieties uz konfidencialitātes politikas lapu un kopējiet vietrādi URL no rekvizītu rūts.</span><span class="sxs-lookup"><span data-stu-id="83f8a-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="83f8a-156">Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="83f8a-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="83f8a-157">Priekšskatiet fragmentu un pārbaudiet saiti uz konfidencialitātes politikas lapu.</span><span class="sxs-lookup"><span data-stu-id="83f8a-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="83f8a-158">Uz fragmentu tagad var atsaukties veidnē citām vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="83f8a-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="83f8a-159">Ja uz šo fragmentu ir atsauce veidnes modulī **Kājene**, saites atsauce tiks parādīta visās lapās, kas ir veidotas, izmantojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="83f8a-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83f8a-160">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="83f8a-160">Additional resources</span></span>

[<span data-ttu-id="83f8a-161">Atbilstības pārskats</span><span class="sxs-lookup"><span data-stu-id="83f8a-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="83f8a-162">Pieejamības līdzekļi un iespējas</span><span class="sxs-lookup"><span data-stu-id="83f8a-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="83f8a-163">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="83f8a-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="83f8a-164">Aizstāt lietotāja ID, kas saistīti ar izsekotām satura izmaiņām</span><span class="sxs-lookup"><span data-stu-id="83f8a-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
