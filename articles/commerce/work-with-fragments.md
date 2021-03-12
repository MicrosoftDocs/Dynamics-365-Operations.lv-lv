---
title: Darbs ar fragmentiem
description: Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8436fd3621e94fb761c076454423fe9842306c78
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982242"
---
# <a name="work-with-fragments"></a><span data-ttu-id="f8284-103">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="f8284-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8284-104">Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8284-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8284-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f8284-105">Overview</span></span>

<span data-ttu-id="f8284-106">Fragmenti ļauj izveidot centralizētu autorēšanas pieredzi moduļa konfigurācijām, kas atkārtoti jāizmanto visā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="f8284-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="f8284-107">Piemēram, galvenes, kājenes un reklāmkarogi bieži tiek konfigurēti kā fragmenti, jo tie tiek koplietoti vairākās lapās.</span><span class="sxs-lookup"><span data-stu-id="f8284-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="f8284-108">Fragmentus varat iedomāties kā miniatūras tīmekļa lapas, kuras var ievietot citās vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="f8284-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="f8284-109">Fragmentiem ir savs dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="f8284-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="f8284-110">Citiem vārdiem, tie tiek izveidoti, pieminēti, atjaunināti un dzēsti kā neatkarīgi elementi autorēšanas rīkos.</span><span class="sxs-lookup"><span data-stu-id="f8284-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="f8284-111">Pēc tam, kad fragmenti ir konfigurēti, tos var izmantot visur, kur var izmantot moduļus vietnes struktūrā.</span><span class="sxs-lookup"><span data-stu-id="f8284-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="f8284-112">Uz fragmentiem var atsaukties lapās, izkārtojumos, veidnēs un citos fragmentos.</span><span class="sxs-lookup"><span data-stu-id="f8284-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="f8284-113">Fragmentus var ligzdot līdz septiņu līmeņu dziļumam citu fragmentu iekšpusē.</span><span class="sxs-lookup"><span data-stu-id="f8284-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="f8284-114">Piemēram, ja jūs vēlaties veicināt sezonas notikumu vairākās lapās mūsu vietnē, varat izmantot fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="f8284-115">Pirmais solis jauna fragmenta radīšanas procesā ir atlasīt moduļa tipu, no kura vēlaties sākt.</span><span class="sxs-lookup"><span data-stu-id="f8284-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="f8284-116">Šim piemēram jūs varat izveidot fragmentu no centrālā moduļa.</span><span class="sxs-lookup"><span data-stu-id="f8284-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="f8284-117">Fragmentus var izveidot no jebkura moduļa tipa.</span><span class="sxs-lookup"><span data-stu-id="f8284-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="f8284-118">Pēc tam varat konfigurēt centrālo fragmentu ar savu īpašo veicināšanas saturu.</span><span class="sxs-lookup"><span data-stu-id="f8284-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="f8284-119">Varat arī lokalizēt to, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="f8284-119">You can also localize it as you require.</span></span> <span data-ttu-id="f8284-120">Pēc tam jaunais atsevišķais centrālais fragments var tikt patērēts kā iepriekš konfigurēts modulis visā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="f8284-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="f8284-121">Varat viegli pievienot to veidnēm, noteiktām lapām vai citiem fragmentiem, kas var saturēt centrālos moduļus.</span><span class="sxs-lookup"><span data-stu-id="f8284-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="f8284-122">Visas vietas, kur šis fragments tiek pievienots, ir atsauces uz jūsu izveidoto centrālo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="f8284-123">Publicējot izmaiņas fragmentā, šīs izmaiņas nekavējoties tiek atspoguļotas visās vietās, kur vietnē ir atsauce uz fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="f8284-124">Tāpēc fragmenti nodrošina spēcīgu un efektīvu veidu, kā atkārtoti izmantot un centralizēti pārvaldīt moduļu konfigurācijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="f8284-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="f8284-125">Efektīvi izmantojot tos, varat būtiski paaugstināt dinamiskumu un samazināt izmaksas, kas saistītas ar vietnes satura pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="f8284-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="f8284-126">Tālāk esošajā attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="f8284-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="f8284-128">Fragmenta izveidošana</span><span class="sxs-lookup"><span data-stu-id="f8284-128">Create a fragment</span></span>

<span data-ttu-id="f8284-129">Varat izveidot jaunu fragmentu vai saglabāt esošu moduļa konfigurāciju kā fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="f8284-130">Esošas moduļa konfigurācijas kā fragmenta saglabāšana</span><span class="sxs-lookup"><span data-stu-id="f8284-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="f8284-131">Lai konvertētu iepriekš konfigurētu moduli par atkārtoti izmantojamu fragmentu Commerce vietņu veidotājā, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="f8284-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f8284-132">Atveriet lapu vai veidni, kas satur moduli, ko vēlaties pārveidot par fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="f8284-133">Strukturējuma rūtī pa kreisi vai tieši vizuālo lapu veidotājā atlasiet iepriekš konfigurēto moduli.</span><span class="sxs-lookup"><span data-stu-id="f8284-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="f8284-134">Atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam vai nu strukturējuma rūtī, vai atlasītā moduļa rīkjoslā vizuālo lapu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="f8284-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="f8284-135">Atlasiet **Koplietot kā fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="f8284-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="f8284-136">Dialoglodziņā **Saglabāt kā fragmentu** ievadiet fragmenta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f8284-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="f8284-137">Atlasiet **Labi**, lai saglabātu moduļa konfigurāciju kā fragmentu, ko var pievienot citām lapām.</span><span class="sxs-lookup"><span data-stu-id="f8284-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="f8284-138">Izveidot jaunu fragmentu</span><span class="sxs-lookup"><span data-stu-id="f8284-138">Create a new fragment</span></span>

<span data-ttu-id="f8284-139">Lai izveidotu jaunu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f8284-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f8284-140">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="f8284-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="f8284-141">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f8284-141">Select **New**.</span></span> <span data-ttu-id="f8284-142">Tiek parādīts dialoglodziņš **Jauns fragments**, kurā redzami visi pieejamie moduļa veidi.</span><span class="sxs-lookup"><span data-stu-id="f8284-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="f8284-143">Kā jau tika minēts iepriekš, fragmentus var izveidot no jebkura moduļa tipa.</span><span class="sxs-lookup"><span data-stu-id="f8284-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="f8284-144">Atlasiet sava fragmenta moduļa veidu.</span><span class="sxs-lookup"><span data-stu-id="f8284-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="f8284-145">Atlasot vispārīgā konteinera moduļa tipu, jūs iegūstat augstāko elastību, kad vēlāk ir jāatjaunina un jākonfigurē jūsu fragments.</span><span class="sxs-lookup"><span data-stu-id="f8284-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="f8284-146">Fragmentu pievienošana, noņemšana vai rediģēšana lapā</span><span class="sxs-lookup"><span data-stu-id="f8284-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="f8284-147">Šīs procedūras apraksta, kā pievienot, noņemt vai rediģēt fragmentus.</span><span class="sxs-lookup"><span data-stu-id="f8284-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="f8284-148">Fragmenta pievienošana</span><span class="sxs-lookup"><span data-stu-id="f8284-148">Add a fragment</span></span>

<span data-ttu-id="f8284-149">Lai pievienotu fragmentu lapai Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f8284-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f8284-150">Strukturējuma rūtī pa kreisi vai tieši vizuālo lapu veidotājā atlasiet konteineru vai slotu, kuram var pievienot atvašu moduļus.</span><span class="sxs-lookup"><span data-stu-id="f8284-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="f8284-151">Atlasiet daudzpunkti (**...**) blakus konteinera nosaukumam vai slotam.</span><span class="sxs-lookup"><span data-stu-id="f8284-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="f8284-152">Vai arī, ja izmantojat vizuālo lapu veidotāju, atlasiet plus zīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="f8284-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="f8284-153">Atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="f8284-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="f8284-154">Ja konteiners vai slots neatbalsta jaunus atvašu moduļus, opcija **Pievienot fragmentu** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="f8284-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="f8284-155">Dialoglodziņā **Atlasīt fragmentu** meklējiet un atlasiet pievienojamo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="f8284-156">Ja pieejamo fragmentu sarakstā nav neviena fragmenta, iespējams, vispirms ir jāizveido fragments no moduļa tipa, ko atbalsta atlasītais konteiners vai slots.</span><span class="sxs-lookup"><span data-stu-id="f8284-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="f8284-157">Atlasiet vēlamo fragmentu, kuru pievienot konteineram vai slotam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="f8284-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="f8284-158">Moduļi, kas ir atļauti konteinerā vai slotā, tiek definēti ar lapas veidni vai pašu moduļu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="f8284-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="f8284-159">Fragmenta noņemšana</span><span class="sxs-lookup"><span data-stu-id="f8284-159">Remove a fragment</span></span>

<span data-ttu-id="f8284-160">Lai izņemtu fragmentu no slota vai konteinera lapā Commerce vietņu veidotājs, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f8284-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f8284-161">Struktūras rūtī pa kreisi izvēlieties daudzpunktes (**...**) pogu, kas atrodas blakus fragmenta nosaukumam, lai noņemtu, un pēc tam atlasiet Miskastes simbolu.</span><span class="sxs-lookup"><span data-stu-id="f8284-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="f8284-162">Vai arī varat atlasīt fragmentu vizuālo lapu veidotājā un atlasīt atkritnes simbolu fragmentu rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="f8284-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="f8284-163">Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt fragmentu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f8284-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="f8284-164">Noņemot fragmentu no lapas, jūs vienkārši noņemat atsauci no tā šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="f8284-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="f8284-165">**Netiek** dzēsts fragments no jūsu vietnes.</span><span class="sxs-lookup"><span data-stu-id="f8284-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="f8284-166">Lai dzēstu fragmentus no jūsu vietnes, jāizmanto fragmenta kontroliera lietotāja interfeiss (UI).</span><span class="sxs-lookup"><span data-stu-id="f8284-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="f8284-167">Fragmentus no vietnes vara izdzēst tikai tad, ja neviena lapā, veidnēs vai citos fragmentos uz tiem nav atsauču.</span><span class="sxs-lookup"><span data-stu-id="f8284-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="f8284-168">Fragmenta rediģēšana</span><span class="sxs-lookup"><span data-stu-id="f8284-168">Edit a fragment</span></span>

<span data-ttu-id="f8284-169">Lai rediģētu fragmentus, jāizmanto fragmentu redaktora lietotāja interfeiss.</span><span class="sxs-lookup"><span data-stu-id="f8284-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="f8284-170">Šis ierobežojums ir izstrādāts.</span><span class="sxs-lookup"><span data-stu-id="f8284-170">This restriction is by design.</span></span> <span data-ttu-id="f8284-171">Tas palīdz nodrošināt, ka autori nejauc moduļu rediģēšanas procesu konkrētai lappusei ar to fragmentu rediģēšanas procesu, kurus var koplietot daudzās lapās.</span><span class="sxs-lookup"><span data-stu-id="f8284-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="f8284-172">Lai rediģētu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f8284-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f8284-173">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="f8284-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="f8284-174">Sadaļā **Fragmenti** atlasiet rediģējamo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="f8284-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="f8284-175">Rediģējiet fragmenta moduļa rekvizītus un struktūru, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="f8284-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="f8284-176">Šis process līdzinās moduļu rediģēšanas procesam, kas tiek veikts lapas redaktora skatā.</span><span class="sxs-lookup"><span data-stu-id="f8284-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="f8284-177">Fragmentu var arī rediģēt, atlasot to lapā, veidnē vai pamata fragmentā un pēc tam labajā pusē rekvizītu rūtī atlasot opciju **Rediģēt fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="f8284-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8284-178">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f8284-178">Additional resources</span></span>

[<span data-ttu-id="f8284-179">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="f8284-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f8284-180">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="f8284-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f8284-181">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="f8284-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="f8284-182">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="f8284-182">Work with publish groups</span></span>](publish-groups.md)
