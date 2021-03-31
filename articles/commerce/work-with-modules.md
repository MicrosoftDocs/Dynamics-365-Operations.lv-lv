---
title: Darbs ar moduļiem
description: Šajā tēmā aprakstīts, kā un kad izmantot moduļus programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210903"
---
# <a name="work-with-modules"></a><span data-ttu-id="438d3-103">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="438d3-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="438d3-104">Šajā tēmā aprakstīts, kā un kad izmantot moduļus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="438d3-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="438d3-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="438d3-105">Overview</span></span>

<span data-ttu-id="438d3-106">Moduļi ir loģiski veidošanas bloki, kas veido lapas struktūru, un tiem ir dažādi mērķi un tvērumi.</span><span class="sxs-lookup"><span data-stu-id="438d3-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="438d3-107">Daži moduļi ir augsta līmeņa konteineri, un to vienīgais mērķis ir aizturēt un organizēt citus moduļus (pakārtotos moduļus).</span><span class="sxs-lookup"><span data-stu-id="438d3-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="438d3-108">Citiem moduļiem, piemēram, vienkāršam attēla novietojuma modulim, ir ļoti specifisks mērķis.</span><span class="sxs-lookup"><span data-stu-id="438d3-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="438d3-109">Citi moduļi, piemēram, karuseļa modulis, atrodas kaut kur starp šīm divām kategorijām.</span><span class="sxs-lookup"><span data-stu-id="438d3-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="438d3-110">Pēc noklusējuma jūsu Dynamics 365 Commerce vietnē ir ietverta moduļu bibliotēka, kas ļauj jums sasniegt pamata e-komercijas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="438d3-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="438d3-111">Jums ir jābūt iespējai izveidot vispārīgu e-komercijas vietni, vienkārši izmantojot šos moduļus.</span><span class="sxs-lookup"><span data-stu-id="438d3-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="438d3-112">Tomēr, iespējams, vēlēsities arī pielāgot šos moduļus vai izveidot jaunus, pielāgotus moduļus specifiskām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="438d3-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="438d3-113">Ja vēlaties izveidot pielāgotus moduļus, ir pieejams moduļa dizaina programmatūras izstrādes komplekts (SDK), lai palīdzētu jums izveidot pielāgotu moduļu bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="438d3-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="438d3-114">Konteineru moduļi un sloti</span><span class="sxs-lookup"><span data-stu-id="438d3-114">Container modules and slots</span></span>

<span data-ttu-id="438d3-115">Kā jau minēts iepriekš, daži moduļi ir paredzēti pakārtotu moduļu aizturēšanai.</span><span class="sxs-lookup"><span data-stu-id="438d3-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="438d3-116">Šie moduļi ir pazīstami kā *konteineri*, un tie atļauj ligzdotu moduļu hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="438d3-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="438d3-117">Konteineru moduļi ietver *slotus*.</span><span class="sxs-lookup"><span data-stu-id="438d3-117">Container modules include *slots*.</span></span> <span data-ttu-id="438d3-118">Sloti tiek izmantoti, lai apstrādātu konteinerā esošo pakārtoto moduļu izkārtojumu un nolūku.</span><span class="sxs-lookup"><span data-stu-id="438d3-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="438d3-119">Piemērs ir pamata lapas konteinera modulis (augšējā līmeņa modulis jebkurai lapai), kas nosaka vairākus nozīmīgus slotus.</span><span class="sxs-lookup"><span data-stu-id="438d3-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="438d3-120">Galvenes slots</span><span class="sxs-lookup"><span data-stu-id="438d3-120">A header slot</span></span>
- <span data-ttu-id="438d3-121">Apakšgalvenes slots</span><span class="sxs-lookup"><span data-stu-id="438d3-121">A sub-header slot</span></span>
- <span data-ttu-id="438d3-122">Galvenais slots</span><span class="sxs-lookup"><span data-stu-id="438d3-122">A main slot</span></span>
- <span data-ttu-id="438d3-123">Kājenes slots</span><span class="sxs-lookup"><span data-stu-id="438d3-123">A footer slot</span></span>
- <span data-ttu-id="438d3-124">Apakškājenes slots</span><span class="sxs-lookup"><span data-stu-id="438d3-124">A sub-footer slot</span></span>

<span data-ttu-id="438d3-125">Moduļa izstrādātājs definē šos slotus un nosaka, kurus un cik daudz pakārtotos moduļus var ievietot tieši tajā.</span><span class="sxs-lookup"><span data-stu-id="438d3-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="438d3-126">Piemēram, galvenes slots var atbalstīt tikai vienu **Virsraksta moduļa** veidu, turpretī pamatteksta slots var atbalstīt neierobežotu moduļu skaitu jebkuram veidam (izņemot citas lapas konteinera moduļus).</span><span class="sxs-lookup"><span data-stu-id="438d3-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="438d3-127">Autorēšanas rīkos lapas autoriem nav jāzina iepriekš, kuri moduļi var un kuri nevar tikti ievietoti katrā slotā.</span><span class="sxs-lookup"><span data-stu-id="438d3-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="438d3-128">Kad lapu autori atlasa slotu un pēc tam mēģina atlasīt moduli, lai to pievienotu, viņi redz filtrētu moduļu veidu skatu, kas tiek atbalstīts šim slotam.</span><span class="sxs-lookup"><span data-stu-id="438d3-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="438d3-129">Satura moduļi</span><span class="sxs-lookup"><span data-stu-id="438d3-129">Content modules</span></span>

<span data-ttu-id="438d3-130">Satura moduļos ir ietverti satura un multivides elementi, piemēram, teksts (piemēram, virsraksti, rindkopas un saites) vai līdzekļu atsauces (piemēram, attēli, video un PDF faili).</span><span class="sxs-lookup"><span data-stu-id="438d3-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="438d3-131">Tipiskiem satura moduļu tipiem ir satura bloks, teksta bloks un promo reklāmkarogu moduļi.</span><span class="sxs-lookup"><span data-stu-id="438d3-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="438d3-132">Šo trīs tipu moduļos var būt teksts vai multivide, un tiem nav nepieciešami pakārtotie moduļi, lai radītu kaut ko redzamu lapā.</span><span class="sxs-lookup"><span data-stu-id="438d3-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="438d3-133">Lielākā daļa parasto, ikdienas lapu un satura autorēšanas aktivitāšu ietver satura moduļus, galvenokārt tāpēc, ka šie moduļi definē faktisko saturu, kas tiek atveidots to pamata konteinera moduļos.</span><span class="sxs-lookup"><span data-stu-id="438d3-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="438d3-134">Ir pieejami daudzi satura moduļi, un šie moduļi parasti ir pēdējie, ko pievienosiet ligzdoto moduļu lapas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="438d3-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="438d3-135">Tālāk esošajā attēlā ir parādīts, kā moduļi tiek ligzdoti pamata konteineru moduļa slotos.</span><span class="sxs-lookup"><span data-stu-id="438d3-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Ligzdošanas moduļi](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="438d3-137">Moduļu pievienošana vai noņemšana</span><span class="sxs-lookup"><span data-stu-id="438d3-137">Add or remove modules</span></span>

<span data-ttu-id="438d3-138">Šīs procedūras apraksta, kā pievienot un noņemt moduļus.</span><span class="sxs-lookup"><span data-stu-id="438d3-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="438d3-139">Moduļa pievienošana</span><span class="sxs-lookup"><span data-stu-id="438d3-139">Add a module</span></span>

<span data-ttu-id="438d3-140">Lai lapas slotam vai konteineram pievienotu moduli, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="438d3-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="438d3-141">Kreisajā struktūras rūtī vai tieši galvenajās kanvās atlasiet konteineru vai slotu, kuram var pievienot pakārtoto moduli.</span><span class="sxs-lookup"><span data-stu-id="438d3-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="438d3-142">Moduļa veidotājs nosaka moduļu tipu sarakstu, ko var pievienot konkrētam moduļa slotam.</span><span class="sxs-lookup"><span data-stu-id="438d3-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="438d3-143">Veidnes autori tad var precizēt atļautās moduļa opcijas, lai palīdzētu nodrošināt saskanīgu meklēšanas programmas optimizāciju (SEO) un autorēšanas efektivitāti visām lapām, kas izveidotas no noteiktas veidnes.</span><span class="sxs-lookup"><span data-stu-id="438d3-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="438d3-144">Kad pievienojat moduli slotam, **Pievienot moduli** dialoglodziņš tiek automātiski filtrēts, lai tiktu rādīti tikai moduļi, kas tiek atbalstīti atlasītajā konteinerā vai slotā.</span><span class="sxs-lookup"><span data-stu-id="438d3-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="438d3-145">Šis atļauto moduļu sarakstu nosaka lapas veidne vai konteinera moduļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="438d3-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="438d3-146">Ja izmantojat struktūras rūti, atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="438d3-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="438d3-147">Ja vadīklas izmantojat tieši kanvās, atlasiet plusa zīmi (**+**) tukšā slotā vai blakus pašlaik atlasītajam modulim un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="438d3-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="438d3-148">Ja konteiners vai slots neatbalsta jaunus pakārtotos moduļus, opcija **Pievienot moduli** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="438d3-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="438d3-149">Dialoglodziņā **Pievienot moduli** meklējiet moduli, ko pievienot lapai.</span><span class="sxs-lookup"><span data-stu-id="438d3-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="438d3-150">**Satura bloks** ir labs moduļa tips iesācējiem, ar ko strādāt.</span><span class="sxs-lookup"><span data-stu-id="438d3-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="438d3-151">Atlasiet **Labi**, lai atlasīto moduli pievienotu atlasītajam konteineram vai slotam jūsu lapā.</span><span class="sxs-lookup"><span data-stu-id="438d3-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="438d3-152">Moduļa noņemšana</span><span class="sxs-lookup"><span data-stu-id="438d3-152">Remove a module</span></span>

<span data-ttu-id="438d3-153">Lai no lapas slota vai konteinera noņemtu moduli, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="438d3-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="438d3-154">Struktūras rūtī pa kreisi izvēlieties daudzpunktes (**...**) pogu, kas atrodas blakus moduļa nosaukumam, lai noņemtu, un pēc tam atlasiet Miskastes simbolu.</span><span class="sxs-lookup"><span data-stu-id="438d3-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="438d3-155">Alternatīvi galvenajā kanvā var izvēlēties miskastes simbolu, kas atrodas atlasītajā moduļa rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="438d3-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="438d3-156">Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt moduli, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="438d3-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="438d3-157">Centrālā moduļa pārvietošana jaunā pozīcijā</span><span class="sxs-lookup"><span data-stu-id="438d3-157">Move a module to a new position</span></span>

<span data-ttu-id="438d3-158">Lai pārvietotu moduli uz jaunu pozīciju jūsu lapā, izmantojiet jebkuru no šīm metodēm.</span><span class="sxs-lookup"><span data-stu-id="438d3-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="438d3-159">Moduļa pārvietošana, izmantojot struktūras rūti</span><span class="sxs-lookup"><span data-stu-id="438d3-159">Move a module using the outline pane</span></span>

<span data-ttu-id="438d3-160">Lai moduli pārvietotu, izmantojot struktūras rūti, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="438d3-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="438d3-161">Atlasiet un turiet moduli, ko vēlaties pārvietot struktūras rūtī, pēc tam velciet moduli uz jaunu pozīciju struktūrā.</span><span class="sxs-lookup"><span data-stu-id="438d3-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="438d3-162">Zilā rinda struktūrskatā un kanvās norāda, kur modulis var tikt novietots.</span><span class="sxs-lookup"><span data-stu-id="438d3-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="438d3-163">Izlaidiet moduli, lai to nomestu jaunajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="438d3-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="438d3-164">Moduļa pārvietošana tieši kanvas ietvaros</span><span class="sxs-lookup"><span data-stu-id="438d3-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="438d3-165">Lai moduli pārvietotu tieši kanvās, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="438d3-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="438d3-166">Atlasiet moduli, kuru vēlaties pārvietot uz kanvām.</span><span class="sxs-lookup"><span data-stu-id="438d3-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="438d3-167">Moduļa rīkjoslā izvēlieties augšupvērstu vai lejupvērstu bultiņas simbolu un pēc tam velciet bultiņu uz jaunu pozīciju lapā.</span><span class="sxs-lookup"><span data-stu-id="438d3-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="438d3-168">Zilā rinda kanvās un struktūrskatā norāda, kur modulis var tikt novietots.</span><span class="sxs-lookup"><span data-stu-id="438d3-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="438d3-169">Ja moduli nevar pārvietot uz augšu vai uz leju, šis bultiņas simbols tiks pelēkots.</span><span class="sxs-lookup"><span data-stu-id="438d3-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="438d3-170">Izlaidiet moduli, lai to nomestu jaunajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="438d3-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="438d3-171">Moduļa pārvietošana, izmantojot daudzpunktes izvēlni</span><span class="sxs-lookup"><span data-stu-id="438d3-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="438d3-172">Lai moduli pārvietotu, izmantojot daudzpunktes izvēlni, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="438d3-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="438d3-173">Atlasiet moduli vai nu struktūrskatā, vai kanvās.</span><span class="sxs-lookup"><span data-stu-id="438d3-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="438d3-174">Atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam vai nu struktūras rūtī, vai atlasītā moduļa rīkjoslā kanvās.</span><span class="sxs-lookup"><span data-stu-id="438d3-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="438d3-175">Ja moduli var pārvietot uz augšu vai uz leju konteinerā vai slotā, būs redzamas opcijas **Pārvietot uz augšu** vai **Pārvietot uz leju**.</span><span class="sxs-lookup"><span data-stu-id="438d3-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="438d3-176">Atlasiet vēlamo pārvietošanas opciju, lai pārvietotu moduli uz augšu vai uz leju attiecībā pret pārējiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="438d3-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="438d3-177">Moduļu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="438d3-177">Configure modules</span></span>

<span data-ttu-id="438d3-178">Šīs procedūras apraksta, kā konfigurēt un satura un konteinera moduļus.</span><span class="sxs-lookup"><span data-stu-id="438d3-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="438d3-179">Satura moduļa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="438d3-179">Configure a content module</span></span>

<span data-ttu-id="438d3-180">Lai konfigurētu satura moduli lapā, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="438d3-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="438d3-181">Struktūras rūtī pa kreisi izvērsiet koku un atlasiet jebkuru satura moduļa tipu (piemēram, **Satura bloks**).</span><span class="sxs-lookup"><span data-stu-id="438d3-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="438d3-182">Alternatīvi jūs varat atlasīt moduli galvenajās kanvās.</span><span class="sxs-lookup"><span data-stu-id="438d3-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="438d3-183">Moduļa rekvizītu rūtī, kas atrodas labajā pusē, ievadiet rekvizītus visām vēlamajām moduļa vadīklām.</span><span class="sxs-lookup"><span data-stu-id="438d3-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="438d3-184">Komandjoslā atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="438d3-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="438d3-185">Tas arī atsvaidzinās priekšskatījuma pamatni.</span><span class="sxs-lookup"><span data-stu-id="438d3-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="438d3-186">Rediģēt moduļa teksta rekvizītus</span><span class="sxs-lookup"><span data-stu-id="438d3-186">Edit module text properties</span></span>

<span data-ttu-id="438d3-187">Moduļa teksta rekvizīti, kas nav tikai lasāmi, var tikt rediģēti tieši kanvās.</span><span class="sxs-lookup"><span data-stu-id="438d3-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="438d3-188">Lai rediģētu moduļa teksta rekvizītus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="438d3-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="438d3-189">Atlasiet kanvu teksta vadīklu, pēc tam novietojiet kursoru vietā, kur vēlaties rediģēt tekstu.</span><span class="sxs-lookup"><span data-stu-id="438d3-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="438d3-190">Ievadiet satura tekstu.</span><span class="sxs-lookup"><span data-stu-id="438d3-190">Enter your text content.</span></span>
1. <span data-ttu-id="438d3-191">Atlasiet jebkur ārpus teksta satura, lai turpinātu cita satura rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="438d3-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="438d3-192">Iekļautā attēla atlase</span><span class="sxs-lookup"><span data-stu-id="438d3-192">Inline image selection</span></span>

<span data-ttu-id="438d3-193">Moduļa attēli, kas nav tikai lasāmi, var tikt mainīti tieši no kanvām.</span><span class="sxs-lookup"><span data-stu-id="438d3-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="438d3-194">Lai izvēlētos jaunu attēlu satura modulim, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="438d3-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="438d3-195">Kanvās veiciet dubultklikšķi uz attēla.</span><span class="sxs-lookup"><span data-stu-id="438d3-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="438d3-196">Tiks izsaukts multivides uztvērēja logs.</span><span class="sxs-lookup"><span data-stu-id="438d3-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="438d3-197">Meklējiet un atlasiet jaunu attēlu, kuru vēlaties izmantot, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="438d3-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="438d3-198">Jaunais attēls tagad tiek atveidots kanvā.</span><span class="sxs-lookup"><span data-stu-id="438d3-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="438d3-199">Konteinera moduļa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="438d3-199">Configure a container module</span></span>

<span data-ttu-id="438d3-200">Lai konfigurētu konteinera moduli lapā, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="438d3-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="438d3-201">Lapā atlasiet konteinera moduli (piemēram, karuselis vai plūstošā konteinera modulis).</span><span class="sxs-lookup"><span data-stu-id="438d3-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="438d3-202">Labajā pusē rekvizītu rūtī izvērsiet ligzdotās vadīklas, atlasot galvenes, un iestatiet jebkuras nepieciešamās kontroles vērtības.</span><span class="sxs-lookup"><span data-stu-id="438d3-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="438d3-203">Struktūras rūtī pa kreisi izvēlieties daudzpunktes pogu, kas atrodas blakus vai nu konteinera nosaukumam, vai kādam no tajā esošo slotu nosaukumiem, un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="438d3-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="438d3-204">Pēc tam pievienojiet pakārtotos moduļus atlasītajam konteineram.</span><span class="sxs-lookup"><span data-stu-id="438d3-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="438d3-205">Plašāku informāciju skatiet sadaļu [Darbs ar moduļiem](#add-a-module) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="438d3-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="438d3-206">Ja vairāki pakārtotie moduļi eksistē kā pamata konteinerā esoši līdzīgie moduļi, varat mainīt to parādīšanas secību pamata konteinerā.</span><span class="sxs-lookup"><span data-stu-id="438d3-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="438d3-207">Atlasiet moduļa daudzpunktes pogu un pēc tam izmantojiet pogas ar augšup un lejup vērstām bultiņām.</span><span class="sxs-lookup"><span data-stu-id="438d3-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="438d3-208">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="438d3-208">Additional resources</span></span>

[<span data-ttu-id="438d3-209">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="438d3-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="438d3-210">Darbs ar veidnēm</span><span class="sxs-lookup"><span data-stu-id="438d3-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="438d3-211">Darbs ar iepriekš iestatītiem izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="438d3-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="438d3-212">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="438d3-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="438d3-213">Konteinera moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="438d3-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="438d3-214">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="438d3-214">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]