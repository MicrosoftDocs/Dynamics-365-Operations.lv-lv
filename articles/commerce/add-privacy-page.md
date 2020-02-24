---
title: Konfidencialitātes politikas lapas pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot konfidencialitātes politikas lapu savai vietnei programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
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
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001327"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="187cc-103">Konfidencialitātes politikas lapas pievienošana</span><span class="sxs-lookup"><span data-stu-id="187cc-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="187cc-104">Šajā tēmā ir aprakstīts, kā pievienot konfidencialitātes politikas lapu savai vietnei programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="187cc-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="187cc-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="187cc-105">Overview</span></span>

<span data-ttu-id="187cc-106">Konfidencialitātes ievērošana ietver organizatoriskus pasākumus, kas informē vietnes lietotājus par to, kā tiek apkopoti un apstrādāti viņu dati.</span><span class="sxs-lookup"><span data-stu-id="187cc-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="187cc-107">Pēc tam lietotāji var izlemt, kā viņi vēlas, lai viņu personas dati tiktu apstrādāti, un var veikt atbilstošas darbības.</span><span class="sxs-lookup"><span data-stu-id="187cc-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="187cc-108">Pārskatiet Microsoft paziņojumu par konfidencialitāti pakalpojumā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="187cc-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="187cc-109">Lai pārskatītu Microsoft paziņojumu par konfidencialitāti, kamēr esat pieteicies Dynamics 365 Commerce autorēšanas rīkos, augšējā labajā stūrī atlasiet pogu **Palīdzība** (**?**) un pēc tam atlasiet **Konfidencialitāte un sīkfaili**.</span><span class="sxs-lookup"><span data-stu-id="187cc-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="187cc-110">Tiek atvērta jauna cilne, kurā ir saite uz [Microsoft paziņojumu par konfidencialitāti](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="187cc-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="187cc-111">Konfidencialitātes politikas lapas izveide jūsu vietnei</span><span class="sxs-lookup"><span data-stu-id="187cc-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="187cc-112">Pakalpojumā Dynamics 365 Commerce ir iespējami vairāki veidi, kā vietnes lietotājiem sniegt piekļuvi jūsu konfidencialitātes politikai.</span><span class="sxs-lookup"><span data-stu-id="187cc-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="187cc-113">Šajā sadaļā ir parādīts, kā izveidot konfidencialitātes politikas lapu un pēc tam atsaukties uz lapu, izmantojot kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="187cc-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="187cc-114">Vadlīnijas, kas redzamas tālāk piemērā, parāda, kā veidot vispārēju konfidencialitātes lapu Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="187cc-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="187cc-115">Jūs esat atbildīgs par to, lai izstrādātu un ieviestu tādu konfidencialitātes politikas lapas risinājumu, kas vislabāk atbilst jūsu uzņēmuma juridiskajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="187cc-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="187cc-116">Lai sāktu, autorēšanas rīkos dodieties uz vietni, kurai vēlaties izveidot konfidencialitātes politikas lapu.</span><span class="sxs-lookup"><span data-stu-id="187cc-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="187cc-117">Izveidot veidni</span><span class="sxs-lookup"><span data-stu-id="187cc-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="187cc-118">Ja veidne, ko var izmantot konfidencialitātes politikas lapā, jau ir izveidota, pārejiet uz priekšu uz sadaļu [Konfidencialitātes politikas izveide](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="187cc-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="187cc-119">Lai izveidotu veidni, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="187cc-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="187cc-120">Dodieties uz sadaļu **Veidnes \> Jauna veidne**.</span><span class="sxs-lookup"><span data-stu-id="187cc-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="187cc-121">Ievadiet veidnes nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="187cc-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="187cc-122">Veidnē pievienojiet nepieciešamos moduļus nepieciešamajiem lapas slotiem.</span><span class="sxs-lookup"><span data-stu-id="187cc-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="187cc-123">Lai iegūtu norādījumus, virziet kursoru virs sarkanajām izsaukuma zīmēm.</span><span class="sxs-lookup"><span data-stu-id="187cc-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="187cc-124">Piemēram, **HTML galvenais** slotam var būt nepieciešams **noklusējuma ārējā skripta** modulis.</span><span class="sxs-lookup"><span data-stu-id="187cc-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="187cc-125">Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.</span><span class="sxs-lookup"><span data-stu-id="187cc-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="187cc-126">Moduļa **Noklusējuma lapa** slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="187cc-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="187cc-127">Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.</span><span class="sxs-lookup"><span data-stu-id="187cc-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="187cc-128">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="187cc-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="187cc-129">Konfidencialitātes politikas lapas izveide</span><span class="sxs-lookup"><span data-stu-id="187cc-129">Build a privacy policy page</span></span>

<span data-ttu-id="187cc-130">Lai izveidotu konfidencialitātes politikas lapu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="187cc-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="187cc-131">Dodieties uz **Lapas \>Jauna lapa**.</span><span class="sxs-lookup"><span data-stu-id="187cc-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="187cc-132">Atlasiet konfidencialitātes politikas lapas veidni.</span><span class="sxs-lookup"><span data-stu-id="187cc-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="187cc-133">Ievadiet lapas nosaukumu un vietrādi URL pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="187cc-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="187cc-134">Jaunās lapas slotā **Galvenais** pievienojiet moduli **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="187cc-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="187cc-135">Modulī **Bagātinātā satura bloks** pievienojiet moduli **Bagātinātā satura bloka vienums**.</span><span class="sxs-lookup"><span data-stu-id="187cc-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="187cc-136">Moduļa **Bagātinātā satura bloks** rekvizītu rūtī atlasiet **Pievienot datu avotu** un tad atlasiet **Bagātinātā satura bloks**.</span><span class="sxs-lookup"><span data-stu-id="187cc-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="187cc-137">Bagātinātā teksta redaktorā ievadiet konfidencialitātes politikas lapas saturu.</span><span class="sxs-lookup"><span data-stu-id="187cc-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="187cc-138">Izvērsiet bagātinātā teksta redaktoru uz pilnekrāna režīmu, kā jums nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="187cc-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="187cc-139">Kad esat pabeidzis satura ievadīšanu, atlasiet **Priekšskatījums**, lai priekšskatītu lapu tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="187cc-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="187cc-140">Aizpildiet visus atlikušos lapas un moduļa rekvizītu papildinājumus.</span><span class="sxs-lookup"><span data-stu-id="187cc-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="187cc-141">Pārbaudiet konfidencialitātes politikas lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="187cc-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="187cc-142">Lai publicētu vietrādi URL konfidencialitātes politikas lapai, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="187cc-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="187cc-143">Pārejiet uz sadaļu **URL** un atlasiet konfidencialitātes politikas lapas vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="187cc-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="187cc-144">Publicējiet atlasīto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="187cc-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="187cc-145">Saites, ka novirza uz konfidencialitātes politiku lapu, izveide kājenē</span><span class="sxs-lookup"><span data-stu-id="187cc-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="187cc-146">Varat pievienot saiti uz konfidencialitātes politikas lapu fragmentam.</span><span class="sxs-lookup"><span data-stu-id="187cc-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="187cc-147">Šādā veidā varat kopīgot saiti un atjaunināt to vairākās vietnes lapās, atsaucoties uz fragmentu.</span><span class="sxs-lookup"><span data-stu-id="187cc-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="187cc-148">Šajā piemērā parādīts, kā pievienot saiti uz konfidencialitātes politikas lapu kājenes fragmentam.</span><span class="sxs-lookup"><span data-stu-id="187cc-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="187cc-149">Lai fragmentam pievienotu saiti, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="187cc-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="187cc-150">Dodieties uz **Lapas fragmenti \> Jauns lapas fragments**.</span><span class="sxs-lookup"><span data-stu-id="187cc-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="187cc-151">Atlasiet moduli **Kājene** un pēc tam ievadiet nosaukumu laukā **Lapas fragmenta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="187cc-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="187cc-152">Slotā **Kājene kategorija** pievienojiet moduli **Kājenes vienums**.</span><span class="sxs-lookup"><span data-stu-id="187cc-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="187cc-153">Rekvizītu rūts labajā pusē atlasiet **Saites teksts**.</span><span class="sxs-lookup"><span data-stu-id="187cc-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="187cc-154">Dialoglodziņā **Saites teksts** ievadiet konfidencialitātes politikas lapas saites tekstu un saites mērķi un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="187cc-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="187cc-155">Lai iegūtu konfidencialitātes politikas lapas vietrādi URL, atveriet **Lapas**, dodieties uz konfidencialitātes politikas lapu un kopējiet vietrādi URL no rekvizītu rūts.</span><span class="sxs-lookup"><span data-stu-id="187cc-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="187cc-156">Saglabājiet fragmentu, pārbaudiet un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="187cc-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="187cc-157">Priekšskatiet fragmentu un pārbaudiet saiti uz konfidencialitātes politikas lapu.</span><span class="sxs-lookup"><span data-stu-id="187cc-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="187cc-158">Uz fragmentu tagad var atsaukties veidnē citām vietnes lapām.</span><span class="sxs-lookup"><span data-stu-id="187cc-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="187cc-159">Ja uz šo fragmentu ir atsauce veidnes modulī **Kājene**, saites atsauce tiks parādīta visās lapās, kas ir veidotas, izmantojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="187cc-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="187cc-160">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="187cc-160">Additional resources</span></span>

[<span data-ttu-id="187cc-161">Atbilstības pārskats</span><span class="sxs-lookup"><span data-stu-id="187cc-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="187cc-162">Pieejamības līdzekļi un iespējas</span><span class="sxs-lookup"><span data-stu-id="187cc-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="187cc-163">Sīkfailu atbilstība</span><span class="sxs-lookup"><span data-stu-id="187cc-163">Cookie compliance</span></span>](cookie-compliance.md)
