---
title: Darbs ar fragmentiem
description: Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698100"
---
# <a name="work-with-fragments"></a><span data-ttu-id="a9e04-103">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="a9e04-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a9e04-104">Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9e04-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a9e04-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="a9e04-105">Overview</span></span>

<span data-ttu-id="a9e04-106">Fragmenti ļauj izveidot centralizētu autorēšanas pieredzi moduļa konfigurācijām, kas atkārtoti jāizmanto visā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="a9e04-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="a9e04-107">Piemēram, galvenes, kājenes un reklāmkarogi bieži tiek konfigurēti kā fragmenti, jo tie tiek koplietoti vairākās lapās.</span><span class="sxs-lookup"><span data-stu-id="a9e04-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="a9e04-108">Fragmentus varat iedomāties kā miniatūras tīmekļa lapas, kuras var ievietot citās vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="a9e04-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="a9e04-109">Fragmentiem ir savs dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="a9e04-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="a9e04-110">Citiem vārdiem, tie tiek izveidoti, pieminēti, atjaunināti un dzēsti kā neatkarīgi elementi autorēšanas rīkos.</span><span class="sxs-lookup"><span data-stu-id="a9e04-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="a9e04-111">Pēc tam, kad fragmenti ir konfigurēti, tos var izmantot visur, kur var izmantot moduļus vietnes struktūrā.</span><span class="sxs-lookup"><span data-stu-id="a9e04-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="a9e04-112">Uz fragmentiem var atsaukties lapās, izkārtojumos, veidnēs un citos fragmentos.</span><span class="sxs-lookup"><span data-stu-id="a9e04-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e04-113">Fragmentus var ligzdot līdz septiņu līmeņu dziļumam citu fragmentu iekšpusē.</span><span class="sxs-lookup"><span data-stu-id="a9e04-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="a9e04-114">Piemēram, ja jūs vēlaties veicināt sezonas notikumu vairākās lapās mūsu vietnē, varat izmantot fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="a9e04-115">Pirmais solis jauna fragmenta radīšanas procesā ir atlasīt moduļa tipu, no kura vēlaties sākt.</span><span class="sxs-lookup"><span data-stu-id="a9e04-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="a9e04-116">Šim piemēram jūs varat izveidot fragmentu no centrālā moduļa.</span><span class="sxs-lookup"><span data-stu-id="a9e04-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e04-117">Fragmentus var izveidot no jebkura moduļa tipa.</span><span class="sxs-lookup"><span data-stu-id="a9e04-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="a9e04-118">Pēc tam varat konfigurēt centrālo fragmentu ar savu īpašo veicināšanas saturu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="a9e04-119">Varat arī lokalizēt to, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a9e04-119">You can also localize it as you require.</span></span> <span data-ttu-id="a9e04-120">Pēc tam jaunais atsevišķais centrālais fragments var tikt patērēts kā iepriekš konfigurēts modulis visā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="a9e04-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="a9e04-121">Varat viegli pievienot to veidnēm, noteiktām lapām vai citiem fragmentiem, kas var saturēt centrālos moduļus.</span><span class="sxs-lookup"><span data-stu-id="a9e04-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="a9e04-122">Visas vietas, kur šis fragments tiek pievienots, ir atsauces uz jūsu izveidoto centrālo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="a9e04-123">Publicējot izmaiņas fragmentā, šīs izmaiņas nekavējoties tiek atspoguļotas visās vietās, kur vietnē ir atsauce uz fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="a9e04-124">Tāpēc fragmenti nodrošina spēcīgu un efektīvu veidu, kā atkārtoti izmantot un centralizēti pārvaldīt moduļu konfigurācijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="a9e04-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="a9e04-125">Efektīvi izmantojot tos, varat būtiski paaugstināt dinamiskumu un samazināt izmaksas, kas saistītas ar vietnes satura pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="a9e04-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="a9e04-126">Tālāk esošajā attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="a9e04-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="a9e04-128">Fragmenta izveidošana</span><span class="sxs-lookup"><span data-stu-id="a9e04-128">Create a fragment</span></span>

<span data-ttu-id="a9e04-129">Varat izveidot jaunu fragmentu vai saglabāt esošu moduļa konfigurāciju kā fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="a9e04-130">Jauna fragmenta izveidošana</span><span class="sxs-lookup"><span data-stu-id="a9e04-130">Create a new fragment</span></span>

<span data-ttu-id="a9e04-131">Lai izveidotu jaunu fragmentu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a9e04-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="a9e04-132">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a9e04-133">Atlasiet **Jauns fragments**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="a9e04-134">Tiek parādīts dialoglodziņš, kurā redzami visi pieejamie moduļa tipi.</span><span class="sxs-lookup"><span data-stu-id="a9e04-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="a9e04-135">Kā jau tika minēts iepriekš, fragmentus var izveidot no jebkura moduļa tipa.</span><span class="sxs-lookup"><span data-stu-id="a9e04-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="a9e04-136">Atlasiet jūsu fragmentam moduļa tipu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="a9e04-137">Atlasot vispārīgā konteinera moduļa tipu, jūs iegūstat augstāko elastību, kad vēlāk ir jāatjaunina un jākonfigurē jūsu fragments.</span><span class="sxs-lookup"><span data-stu-id="a9e04-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="a9e04-138">Esošas moduļa konfigurācijas kā fragmenta saglabāšana</span><span class="sxs-lookup"><span data-stu-id="a9e04-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="a9e04-139">Lai konvertētu iepriekš konfigurētu moduli par atkārtoti izmantojamu fragmentu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="a9e04-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="a9e04-140">Atveriet lapu vai veidni, kas satur moduli, ko vēlaties pārveidot par fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="a9e04-141">Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu (**...**), kas atrodas blakus moduļa nosaukumam, lai noņemtu, un pēc tam atlasiet pogu **Saglabāt ka fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="a9e04-142">Parādīsies dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="a9e04-142">A dialog box appears.</span></span>
1. <span data-ttu-id="a9e04-143">Ievadiet fragmenta nosaukumu un metadatus.</span><span class="sxs-lookup"><span data-stu-id="a9e04-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="a9e04-144">Atlasiet **Labi**, lai saglabātu moduļa konfigurāciju kā fragmentu, ko var pievienot citām lapām.</span><span class="sxs-lookup"><span data-stu-id="a9e04-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="a9e04-145">Fragmentu pievienošana, noņemšana vai rediģēšana lapā</span><span class="sxs-lookup"><span data-stu-id="a9e04-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="a9e04-146">Šīs procedūras apraksta, kā pievienot, noņemt vai rediģēt fragmentus.</span><span class="sxs-lookup"><span data-stu-id="a9e04-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="a9e04-147">Fragmenta pievienošana</span><span class="sxs-lookup"><span data-stu-id="a9e04-147">Add a fragment</span></span>

<span data-ttu-id="a9e04-148">Lai lapai pievienotu fragmentu, veiciet tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="a9e04-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="a9e04-149">Kreisajā struktūras rūtī atlasiet konteineru vai slotu, kuram var pievienot pakārtotos moduļus.</span><span class="sxs-lookup"><span data-stu-id="a9e04-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="a9e04-150">Atlasiet daudzpunktes pogu blakus konteinera vai slota nosaukumam un pēc tam atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="a9e04-151">Parādīsies dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="a9e04-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9e04-152">Ja konteiners vai slots neatbalsta jaunus pakārtotos moduļus, opcija **Pievienot fragmentu** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="a9e04-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="a9e04-153">Dialoglodziņā meklējiet un atlasiet fragmentu, ko pievienot lapai.</span><span class="sxs-lookup"><span data-stu-id="a9e04-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="a9e04-154">Ja pieejamo fragmentu sarakstā nav neviena fragmenta, iespējams, vispirms ir jāizveido fragments no moduļa tipa, ko atbalsta atlasītais konteiners vai slots.</span><span class="sxs-lookup"><span data-stu-id="a9e04-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="a9e04-155">Atlasiet **Labi**, lai atlasīto fragmentu pievienotu atlasītajam konteineram vai slotam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="a9e04-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e04-156">Moduļi, kas ir atļauti konteinerā vai slotā, tiek definēti ar lapas veidni vai pašu moduļu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="a9e04-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="a9e04-157">Fragmenta noņemšana</span><span class="sxs-lookup"><span data-stu-id="a9e04-157">Remove a fragment</span></span>

<span data-ttu-id="a9e04-158">Lai no lapas slota vai konteinera noņemtu fragmentu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="a9e04-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="a9e04-159">Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus fragmenta nosaukumam, lai noņemtu, un pēc tam atlasiet pogu Miskaste.</span><span class="sxs-lookup"><span data-stu-id="a9e04-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="a9e04-160">Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt fragmentu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a9e04-161">Noņemot fragmentu no lapas, jūs vienkārši noņemat atsauci no tā šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="a9e04-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="a9e04-162">**Netiek** dzēsts fragments no jūsu vietnes.</span><span class="sxs-lookup"><span data-stu-id="a9e04-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="a9e04-163">Lai dzēstu fragmentus no jūsu vietnes, jāizmanto fragmenta kontroliera lietotāja interfeiss (UI).</span><span class="sxs-lookup"><span data-stu-id="a9e04-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="a9e04-164">Fragmentus no vietnes vara izdzēst tikai tad, ja neviena lapā, veidnēs vai citos fragmentos uz tiem nav atsauču.</span><span class="sxs-lookup"><span data-stu-id="a9e04-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="a9e04-165">Fragmenta rediģēšana</span><span class="sxs-lookup"><span data-stu-id="a9e04-165">Edit a fragment</span></span>

<span data-ttu-id="a9e04-166">Lai rediģētu fragmentus, jāizmanto fragmentu redaktora lietotāja interfeiss.</span><span class="sxs-lookup"><span data-stu-id="a9e04-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="a9e04-167">Šis ierobežojums ir izstrādāts.</span><span class="sxs-lookup"><span data-stu-id="a9e04-167">This restriction is by design.</span></span> <span data-ttu-id="a9e04-168">Tas palīdz nodrošināt, ka autori nejauc moduļu rediģēšanas procesu konkrētai lappusei ar to fragmentu rediģēšanas procesu, kurus var koplietot daudzās lapās.</span><span class="sxs-lookup"><span data-stu-id="a9e04-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="a9e04-169">Lai rediģētu fragmentu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a9e04-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="a9e04-170">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="a9e04-171">Sadaļā **Fragmenti** atlasiet rediģējamo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a9e04-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="a9e04-172">Rediģējiet fragmenta moduļa rekvizītus un struktūru, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="a9e04-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="a9e04-173">Šis process līdzinās moduļu rediģēšanas procesam, kas tiek veikts lapas redaktora skatā.</span><span class="sxs-lookup"><span data-stu-id="a9e04-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="a9e04-174">Fragmentu var arī rediģēt, atlasot to lapā, veidnē vai pamata fragmentā un pēc tam labajā pusē rekvizītu rūtī atlasot opciju **Rediģēt fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="a9e04-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9e04-175">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a9e04-175">Additional resources</span></span>

[<span data-ttu-id="a9e04-176">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="a9e04-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a9e04-177">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="a9e04-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="a9e04-178">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="a9e04-178">Work with preset layouts</span></span>](work-with-layouts.md)
