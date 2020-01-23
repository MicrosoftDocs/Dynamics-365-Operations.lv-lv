---
title: Darbs ar moduļiem
description: Šajā tēmā aprakstīts, kā un kad izmantot moduļus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914798"
---
# <a name="work-with-modules"></a><span data-ttu-id="e6d24-103">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="e6d24-103">Work with modules</span></span>

<span data-ttu-id="e6d24-104">Šajā tēmā aprakstīts, kā un kad izmantot moduļus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e6d24-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e6d24-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e6d24-105">Overview</span></span>

<span data-ttu-id="e6d24-106">Moduļi ir loģiski veidošanas bloki, kas veido lapas struktūru, un tiem ir dažādi mērķi un tvērumi.</span><span class="sxs-lookup"><span data-stu-id="e6d24-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="e6d24-107">Daži moduļi ir augsta līmeņa konteineri, un to vienīgais mērķis ir aizturēt un organizēt citus moduļus (pakārtotos moduļus).</span><span class="sxs-lookup"><span data-stu-id="e6d24-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="e6d24-108">Citiem moduļiem, piemēram, vienkāršam attēla novietojuma modulim, ir ļoti specifisks mērķis.</span><span class="sxs-lookup"><span data-stu-id="e6d24-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="e6d24-109">Citi moduļi, piemēram, karuseļa modulis, atrodas kaut kur starp šīm divām kategorijām.</span><span class="sxs-lookup"><span data-stu-id="e6d24-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="e6d24-110">Pēc noklusējuma jūsu Dynamics 365 Commerce vietnē ir ietverta sākuma komplekta moduļa bibliotēka, kas ļauj jums sasniegt pamata e-komercijas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="e6d24-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="e6d24-111">Jums ir jābūt iespējai izveidot vispārīgu e-komercijas vietni, vienkārši izmantojot šos moduļus.</span><span class="sxs-lookup"><span data-stu-id="e6d24-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="e6d24-112">Tomēr, iespējams, vēlēsities arī pielāgot šos moduļus vai izveidot jaunus, pielāgotus moduļus specifiskām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="e6d24-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="e6d24-113">Ja vēlaties izveidot pielāgotus moduļus, ir pieejams moduļa dizaina programmatūras izstrādes komplekts (SDK), lai palīdzētu jums izveidot pielāgotu moduļu bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="e6d24-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="e6d24-114">Konteineru moduļi un sloti</span><span class="sxs-lookup"><span data-stu-id="e6d24-114">Container modules and slots</span></span>

<span data-ttu-id="e6d24-115">Kā jau minēts iepriekš, daži moduļi ir paredzēti pakārtotu moduļu aizturēšanai.</span><span class="sxs-lookup"><span data-stu-id="e6d24-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="e6d24-116">Šie moduļi ir pazīstami kā *konteineri*, un tie atļauj ligzdotu moduļu hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="e6d24-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="e6d24-117">Konteineru moduļi ietver *slotus*.</span><span class="sxs-lookup"><span data-stu-id="e6d24-117">Container modules include *slots*.</span></span> <span data-ttu-id="e6d24-118">Sloti tiek izmantoti, lai apstrādātu konteinerā esošo pakārtoto moduļu izkārtojumu un nolūku.</span><span class="sxs-lookup"><span data-stu-id="e6d24-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="e6d24-119">Piemērs ir pamata lapas konteinera modulis (augšējā līmeņa modulis jebkurai lapai), kas nosaka vairākus nozīmīgus slotus.</span><span class="sxs-lookup"><span data-stu-id="e6d24-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="e6d24-120">Galvenes slots</span><span class="sxs-lookup"><span data-stu-id="e6d24-120">A header slot</span></span>
- <span data-ttu-id="e6d24-121">Pamatteksta slots</span><span class="sxs-lookup"><span data-stu-id="e6d24-121">A body slot</span></span>
- <span data-ttu-id="e6d24-122">Kājenes slots</span><span class="sxs-lookup"><span data-stu-id="e6d24-122">A footer slot</span></span>

<span data-ttu-id="e6d24-123">Moduļa izstrādātājs definē šos slotus un nosaka, kurus un cik daudz pakārtotos moduļus var ievietot tieši tajā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="e6d24-124">Piemēram, galvenes slots var atbalstīt tikai vienu **Virsraksta moduļa** veidu, turpretī pamatteksta slots var atbalstīt neierobežotu moduļu skaitu jebkuram veidam (izņemot citas lapas konteinera moduļus).</span><span class="sxs-lookup"><span data-stu-id="e6d24-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="e6d24-125">Autorēšanas rīkos lapas autoriem nav jāzina iepriekš, kuri moduļi var un kuri nevar tikti ievietoti katrā slotā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="e6d24-126">Kad lapu autori atlasa slotu un pēc tam mēģina atlasīt moduli, lai to pievienotu, viņi redz filtrētu moduļu veidu skatu, kas tiek atbalstīts šim slotam.</span><span class="sxs-lookup"><span data-stu-id="e6d24-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="e6d24-127">Satura moduļi</span><span class="sxs-lookup"><span data-stu-id="e6d24-127">Content modules</span></span>

<span data-ttu-id="e6d24-128">Satura moduļos ir ietverti satura un multivides elementi, piemēram, teksts (piemēram, virsraksti, rindkopas un saites) vai līdzekļu atsauces (piemēram, attēli, video un PDF faili).</span><span class="sxs-lookup"><span data-stu-id="e6d24-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="e6d24-129">Tipisku satura moduļu tipu piemēri ir **Centrālais** ,**Līdzekļa** un **Reklāmkarogs**.</span><span class="sxs-lookup"><span data-stu-id="e6d24-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="e6d24-130">Šo trīs tipu moduļos var būt teksts vai multivide, un tiem nav nepieciešami pakārtotie moduļi, lai radītu kaut ko redzamu lapā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="e6d24-131">Lielākā daļa parasto, ikdienas lapu un satura autorēšanas aktivitāšu ietver satura moduļus, galvenokārt tāpēc, ka šie moduļi definē faktisko saturu, kas tiek atveidots to pamata konteinera moduļos.</span><span class="sxs-lookup"><span data-stu-id="e6d24-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="e6d24-132">Ir pieejami daudzi satura moduļi, un šie moduļi parasti ir pēdējie, ko pievienosiet ligzdoto moduļu lapas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="e6d24-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="e6d24-133">Tālāk esošajā attēlā ir parādīts, kā moduļi tiek ligzdoti pamata konteineru moduļa slotos.</span><span class="sxs-lookup"><span data-stu-id="e6d24-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Ligzdošanas moduļi](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="e6d24-135">Moduļu pievienošana vai noņemšana</span><span class="sxs-lookup"><span data-stu-id="e6d24-135">Add or remove modules</span></span>

<span data-ttu-id="e6d24-136">Šīs procedūras apraksta, kā pievienot un noņemt moduļus.</span><span class="sxs-lookup"><span data-stu-id="e6d24-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="e6d24-137">Moduļa pievienošana</span><span class="sxs-lookup"><span data-stu-id="e6d24-137">Add a module</span></span>

<span data-ttu-id="e6d24-138">Lai lapas slotam vai konteineram pievienotu moduli, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6d24-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6d24-139">Kreisajā struktūras rūtī atlasiet konteineru vai slotu, kuram var pievienot pakārtoto moduli.</span><span class="sxs-lookup"><span data-stu-id="e6d24-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6d24-140">Moduļa veidotājs nosaka moduļu tipu sarakstu, ko var pievienot konkrētam moduļa slotam.</span><span class="sxs-lookup"><span data-stu-id="e6d24-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="e6d24-141">Veidnes autori tad var precizēt atļautās moduļa opcijas, lai palīdzētu nodrošināt saskanīgu meklēšanas programmas optimizāciju (SEO) un autorēšanas efektivitāti visām lapu lapām, kas izveidotas no noteiktas veidnes.</span><span class="sxs-lookup"><span data-stu-id="e6d24-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="e6d24-142">Atlasiet daudzpunktes pogu (**...**) modulim un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="e6d24-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="e6d24-143">Tiek parādīts dialoglodziņš **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="e6d24-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="e6d24-144">Šis dialoglodziņš tiek automātiski filtrēts, lai tiktu rādīti tikai moduļi, kas tiek atbalstīti atlasītajā konteinerā vai slotā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="e6d24-145">Moduļu sarakstu nosaka lapas veidne vai konteinera moduļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="e6d24-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6d24-146">Ja konteiners vai slots neatbalsta jaunus pakārtotos moduļus, opcija **Pievienot moduli** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="e6d24-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="e6d24-147">Dialoglodziņā meklējiet un atlasiet moduli, ko pievienot lapai.</span><span class="sxs-lookup"><span data-stu-id="e6d24-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="e6d24-148">**Funkcija** un **Centrālais** ir labi moduļu veidi iesācējiem.</span><span class="sxs-lookup"><span data-stu-id="e6d24-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="e6d24-149">Atlasiet **Labi**, lai atlasīto moduli pievienotu atlasītajam konteineram vai slotam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="e6d24-150">Moduļa noņemšana</span><span class="sxs-lookup"><span data-stu-id="e6d24-150">Remove a module</span></span>

<span data-ttu-id="e6d24-151">Lai no lapas slota vai konteinera noņemtu moduli, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6d24-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6d24-152">Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus moduļa nosaukumam, lai noņemtu, un pēc tam atlasiet pogu Miskaste.</span><span class="sxs-lookup"><span data-stu-id="e6d24-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="e6d24-153">Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt moduli, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e6d24-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="e6d24-154">Moduļu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6d24-154">Configure modules</span></span>

<span data-ttu-id="e6d24-155">Šīs procedūras apraksta, kā konfigurēt un satura un konteinera moduļus.</span><span class="sxs-lookup"><span data-stu-id="e6d24-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="e6d24-156">Satura moduļa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6d24-156">Configure a content module</span></span>

<span data-ttu-id="e6d24-157">Lai konfigurētu satura moduli lapā, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="e6d24-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6d24-158">Struktūras rūtī pa kreisi atlasiet satura moduļa tipu (piemēram, **Līdzekļa**, **Centrālais** vai **Reklāmkarogs**).</span><span class="sxs-lookup"><span data-stu-id="e6d24-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="e6d24-159">Labajā pusē rekvizītu rūtī izvērsiet ligzdotās vadīklas, atlasot galvenes, un iestatiet jebkuras nepieciešamās kontroles vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6d24-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="e6d24-160">Ja rekvizītu rūtij ir sadaļa **Datu konfigurācija**, atlasiet to, lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="e6d24-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="e6d24-161">Citādi pārejiet uz 5. darbību.</span><span class="sxs-lookup"><span data-stu-id="e6d24-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="e6d24-162">Ja tur ir poga **Pievienot datu avotu**, atlasiet to un pēc tam atlasiet pievienojamos satura vienumus.</span><span class="sxs-lookup"><span data-stu-id="e6d24-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="e6d24-163">Ievadiet iestatījumus visām nepieciešamajām vai vēlamajām moduļa vadīklām.</span><span class="sxs-lookup"><span data-stu-id="e6d24-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="e6d24-164">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e6d24-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="e6d24-165">Konteinera moduļa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6d24-165">Configure a container module</span></span>

<span data-ttu-id="e6d24-166">Lai konfigurētu konteinera moduli lapā, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="e6d24-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="e6d24-167">Lapā atlasiet konteinera moduli (piemēram, karuselis vai plūstošā konteinera modulis).</span><span class="sxs-lookup"><span data-stu-id="e6d24-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="e6d24-168">Labajā pusē rekvizītu rūtī izvērsiet ligzdotās vadīklas, atlasot galvenes, un iestatiet jebkuras nepieciešamās kontroles vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6d24-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="e6d24-169">Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus vai nu konteinera nosaukumam, vai kādam no tajā esošo slotu nosaukumiem, un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="e6d24-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="e6d24-170">Pēc tam pievienojiet pakārtotos moduļus atlasītajam konteineram.</span><span class="sxs-lookup"><span data-stu-id="e6d24-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="e6d24-171">Plašāku informāciju skatiet procedūru [Moduļa pievienošana](#add-a-module) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="e6d24-172">Ja vairāki pakārtotie moduļi eksistē kā pamata konteinerā esoši brāļi, varat mainīt to parādīšanas secību pamata konteinerā.</span><span class="sxs-lookup"><span data-stu-id="e6d24-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="e6d24-173">Atlasiet moduļa daudzpunktes pogu un pēc tam izmantojiet pogas ar augšup un lejup vērstām bultiņām.</span><span class="sxs-lookup"><span data-stu-id="e6d24-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6d24-174">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e6d24-174">Additional resources</span></span>

[<span data-ttu-id="e6d24-175">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="e6d24-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e6d24-176">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="e6d24-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="e6d24-177">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="e6d24-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="e6d24-178">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="e6d24-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="e6d24-179">Konteinera moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="e6d24-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="e6d24-180">Satura izvietojuma moduļu pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="e6d24-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e6d24-181">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="e6d24-181">Work with publish groups</span></span>](publish-groups.md)

