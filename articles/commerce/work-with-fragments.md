---
title: Darbs ar fragmentiem
description: Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793949"
---
# <a name="work-with-fragments"></a><span data-ttu-id="ae673-103">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="ae673-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae673-104">Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ae673-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ae673-105">Fragmenti ļauj izveidot centralizētu autorēšanas pieredzi moduļa konfigurācijām, kas atkārtoti jāizmanto visā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="ae673-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="ae673-106">Piemēram, galvenes, kājenes un reklāmkarogi bieži tiek konfigurēti kā fragmenti, jo tie tiek koplietoti vairākās lapās.</span><span class="sxs-lookup"><span data-stu-id="ae673-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="ae673-107">Fragmentus varat iedomāties kā miniatūras tīmekļa lapas, kuras var ievietot citās vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="ae673-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="ae673-108">Fragmentiem ir savs dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="ae673-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="ae673-109">Citiem vārdiem, tie tiek izveidoti, pieminēti, atjaunināti un dzēsti kā neatkarīgi elementi autorēšanas rīkos.</span><span class="sxs-lookup"><span data-stu-id="ae673-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="ae673-110">Pēc tam, kad fragmenti ir konfigurēti, tos var izmantot visur, kur var izmantot moduļus vietnes struktūrā.</span><span class="sxs-lookup"><span data-stu-id="ae673-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="ae673-111">Uz fragmentiem var atsaukties lapās, izkārtojumos, veidnēs un citos fragmentos.</span><span class="sxs-lookup"><span data-stu-id="ae673-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="ae673-112">Fragmentus var ligzdot līdz septiņu līmeņu dziļumam citu fragmentu iekšpusē.</span><span class="sxs-lookup"><span data-stu-id="ae673-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="ae673-113">Piemēram, ja jūs vēlaties veicināt sezonas notikumu vairākās lapās mūsu vietnē, varat izmantot fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="ae673-114">Pirmais solis jauna fragmenta radīšanas procesā ir atlasīt moduļa tipu, no kura vēlaties sākt.</span><span class="sxs-lookup"><span data-stu-id="ae673-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="ae673-115">Šim piemēram jūs varat izveidot fragmentu no centrālā moduļa.</span><span class="sxs-lookup"><span data-stu-id="ae673-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="ae673-116">Fragmentus var izveidot no jebkura moduļa tipa.</span><span class="sxs-lookup"><span data-stu-id="ae673-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="ae673-117">Pēc tam varat konfigurēt centrālo fragmentu ar savu īpašo veicināšanas saturu.</span><span class="sxs-lookup"><span data-stu-id="ae673-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="ae673-118">Varat arī lokalizēt to, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ae673-118">You can also localize it as you require.</span></span> <span data-ttu-id="ae673-119">Pēc tam jaunais atsevišķais centrālais fragments var tikt patērēts kā iepriekš konfigurēts modulis visā jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="ae673-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="ae673-120">Varat viegli pievienot to veidnēm, noteiktām lapām vai citiem fragmentiem, kas var saturēt centrālos moduļus.</span><span class="sxs-lookup"><span data-stu-id="ae673-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="ae673-121">Visas vietas, kur šis fragments tiek pievienots, ir atsauces uz jūsu izveidoto centrālo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="ae673-122">Publicējot izmaiņas fragmentā, šīs izmaiņas nekavējoties tiek atspoguļotas visās vietās, kur vietnē ir atsauce uz fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="ae673-123">Tāpēc fragmenti nodrošina spēcīgu un efektīvu veidu, kā atkārtoti izmantot un centralizēti pārvaldīt moduļu konfigurācijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="ae673-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="ae673-124">Efektīvi izmantojot tos, varat būtiski paaugstināt dinamiskumu un samazināt izmaksas, kas saistītas ar vietnes satura pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="ae673-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="ae673-125">Tālāk esošajā attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="ae673-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="ae673-127">Fragmenta izveidošana</span><span class="sxs-lookup"><span data-stu-id="ae673-127">Create a fragment</span></span>

<span data-ttu-id="ae673-128">Varat izveidot jaunu fragmentu vai saglabāt esošu moduļa konfigurāciju kā fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="ae673-129">Esošas moduļa konfigurācijas kā fragmenta saglabāšana</span><span class="sxs-lookup"><span data-stu-id="ae673-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="ae673-130">Lai konvertētu iepriekš konfigurētu moduli par atkārtoti izmantojamu fragmentu Commerce vietņu veidotājā, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="ae673-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae673-131">Atveriet lapu vai veidni, kas satur moduli, ko vēlaties pārveidot par fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="ae673-132">Strukturējuma rūtī pa kreisi vai tieši vizuālo lapu veidotājā atlasiet iepriekš konfigurēto moduli.</span><span class="sxs-lookup"><span data-stu-id="ae673-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="ae673-133">Atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam vai nu strukturējuma rūtī, vai atlasītā moduļa rīkjoslā vizuālo lapu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="ae673-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="ae673-134">Atlasiet **Koplietot kā fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="ae673-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="ae673-135">Dialoglodziņā **Saglabāt kā fragmentu** ievadiet fragmenta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ae673-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="ae673-136">Atlasiet **Labi**, lai saglabātu moduļa konfigurāciju kā fragmentu, ko var pievienot citām lapām.</span><span class="sxs-lookup"><span data-stu-id="ae673-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="ae673-137">Izveidot jaunu fragmentu</span><span class="sxs-lookup"><span data-stu-id="ae673-137">Create a new fragment</span></span>

<span data-ttu-id="ae673-138">Lai izveidotu jaunu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae673-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae673-139">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="ae673-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="ae673-140">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ae673-140">Select **New**.</span></span> <span data-ttu-id="ae673-141">Tiek parādīts dialoglodziņš **Jauns fragments**, kurā redzami visi pieejamie moduļa veidi.</span><span class="sxs-lookup"><span data-stu-id="ae673-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="ae673-142">Kā jau tika minēts iepriekš, fragmentus var izveidot no jebkura moduļa tipa.</span><span class="sxs-lookup"><span data-stu-id="ae673-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="ae673-143">Atlasiet sava fragmenta moduļa veidu.</span><span class="sxs-lookup"><span data-stu-id="ae673-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="ae673-144">Atlasot vispārīgā konteinera moduļa tipu, jūs iegūstat augstāko elastību, kad vēlāk ir jāatjaunina un jākonfigurē jūsu fragments.</span><span class="sxs-lookup"><span data-stu-id="ae673-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="ae673-145">Fragmentu pievienošana, noņemšana vai rediģēšana lapā</span><span class="sxs-lookup"><span data-stu-id="ae673-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="ae673-146">Šīs procedūras apraksta, kā pievienot, noņemt vai rediģēt fragmentus.</span><span class="sxs-lookup"><span data-stu-id="ae673-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="ae673-147">Fragmenta pievienošana</span><span class="sxs-lookup"><span data-stu-id="ae673-147">Add a fragment</span></span>

<span data-ttu-id="ae673-148">Lai pievienotu fragmentu lapai Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae673-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae673-149">Strukturējuma rūtī pa kreisi vai tieši vizuālo lapu veidotājā atlasiet konteineru vai slotu, kuram var pievienot atvašu moduļus.</span><span class="sxs-lookup"><span data-stu-id="ae673-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="ae673-150">Atlasiet daudzpunkti (**...**) blakus konteinera nosaukumam vai slotam.</span><span class="sxs-lookup"><span data-stu-id="ae673-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="ae673-151">Vai arī, ja izmantojat vizuālo lapu veidotāju, atlasiet plus zīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="ae673-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="ae673-152">Atlasiet **Pievienot fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="ae673-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="ae673-153">Ja konteiners vai slots neatbalsta jaunus atvašu moduļus, opcija **Pievienot fragmentu** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="ae673-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="ae673-154">Dialoglodziņā **Atlasīt fragmentu** meklējiet un atlasiet pievienojamo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="ae673-155">Ja pieejamo fragmentu sarakstā nav neviena fragmenta, iespējams, vispirms ir jāizveido fragments no moduļa tipa, ko atbalsta atlasītais konteiners vai slots.</span><span class="sxs-lookup"><span data-stu-id="ae673-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="ae673-156">Atlasiet vēlamo fragmentu, kuru pievienot konteineram vai slotam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="ae673-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="ae673-157">Moduļi, kas ir atļauti konteinerā vai slotā, tiek definēti ar lapas veidni vai pašu moduļu definīcijām.</span><span class="sxs-lookup"><span data-stu-id="ae673-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="ae673-158">Fragmenta noņemšana</span><span class="sxs-lookup"><span data-stu-id="ae673-158">Remove a fragment</span></span>

<span data-ttu-id="ae673-159">Lai izņemtu fragmentu no slota vai konteinera lapā Commerce vietņu veidotājs, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae673-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae673-160">Struktūras rūtī pa kreisi izvēlieties daudzpunktes (**...**) pogu, kas atrodas blakus fragmenta nosaukumam, lai noņemtu, un pēc tam atlasiet Miskastes simbolu.</span><span class="sxs-lookup"><span data-stu-id="ae673-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="ae673-161">Vai arī varat atlasīt fragmentu vizuālo lapu veidotājā un atlasīt atkritnes simbolu fragmentu rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="ae673-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="ae673-162">Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt fragmentu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ae673-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="ae673-163">Noņemot fragmentu no lapas, jūs vienkārši noņemat atsauci no tā šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="ae673-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="ae673-164">**Netiek** dzēsts fragments no jūsu vietnes.</span><span class="sxs-lookup"><span data-stu-id="ae673-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="ae673-165">Lai dzēstu fragmentus no jūsu vietnes, jāizmanto fragmenta kontroliera lietotāja interfeiss (UI).</span><span class="sxs-lookup"><span data-stu-id="ae673-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="ae673-166">Fragmentus no vietnes vara izdzēst tikai tad, ja neviena lapā, veidnēs vai citos fragmentos uz tiem nav atsauču.</span><span class="sxs-lookup"><span data-stu-id="ae673-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="ae673-167">Fragmenta rediģēšana</span><span class="sxs-lookup"><span data-stu-id="ae673-167">Edit a fragment</span></span>

<span data-ttu-id="ae673-168">Lai rediģētu fragmentus, jāizmanto fragmentu redaktora lietotāja interfeiss.</span><span class="sxs-lookup"><span data-stu-id="ae673-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="ae673-169">Šis ierobežojums ir izstrādāts.</span><span class="sxs-lookup"><span data-stu-id="ae673-169">This restriction is by design.</span></span> <span data-ttu-id="ae673-170">Tas palīdz nodrošināt, ka autori nejauc moduļu rediģēšanas procesu konkrētai lappusei ar to fragmentu rediģēšanas procesu, kurus var koplietot daudzās lapās.</span><span class="sxs-lookup"><span data-stu-id="ae673-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="ae673-171">Lai rediģētu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae673-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ae673-172">Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.</span><span class="sxs-lookup"><span data-stu-id="ae673-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="ae673-173">Sadaļā **Fragmenti** atlasiet rediģējamo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="ae673-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="ae673-174">Rediģējiet fragmenta moduļa rekvizītus un struktūru, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ae673-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="ae673-175">Šis process līdzinās moduļu rediģēšanas procesam, kas tiek veikts lapas redaktora skatā.</span><span class="sxs-lookup"><span data-stu-id="ae673-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="ae673-176">Fragmentu var arī rediģēt, atlasot to lapā, veidnē vai pamata fragmentā un pēc tam labajā pusē rekvizītu rūtī atlasot opciju **Rediģēt fragmentu**.</span><span class="sxs-lookup"><span data-stu-id="ae673-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae673-177">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ae673-177">Additional resources</span></span>

[<span data-ttu-id="ae673-178">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="ae673-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="ae673-179">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="ae673-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="ae673-180">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="ae673-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="ae673-181">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="ae673-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
