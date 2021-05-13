---
title: Mērvienību pārvaldība
description: Šajā tēmā aprakstīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921345"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="5a4ff-103">Mērvienību pārvaldība</span><span class="sxs-lookup"><span data-stu-id="5a4ff-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a4ff-104">Šajā tēmā aprakstīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="5a4ff-105">Atveriet vienības lapu</span><span class="sxs-lookup"><span data-stu-id="5a4ff-105">Open the Units page</span></span>

<span data-ttu-id="5a4ff-106">Lai izveidotu mērvienības un strādātu ar tām, kas ir pieejamas jūsu sistēmā, dodieties uz **Organizācijas administrēšana \> Iestatījums \> Vienības \> Vienības**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="5a4ff-107">Pārējās šīs tēmas sadaļās aprakstīts, ko varat darīt lapā **Vienības**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="5a4ff-108">Standarta vienību un pārveidošanu izveide</span><span class="sxs-lookup"><span data-stu-id="5a4ff-108">Create standard units and conversions</span></span>

<span data-ttu-id="5a4ff-109">Ja sistēmā jau nav iekļautas visbiežāk izmantotās mērvienības metriskajai sistēmai un/vai ASV pielāgotajai sistēmai (USCS), vienību uzstādīšanas vednis var palīdzēt ātri sākt darbu ar pamatvienību definīcijām un pārveidošanām.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="5a4ff-110">Lai pabeigtu vedni, darbību rūtī atlasiet **Vienības izveides vednis** un pēc tam izpildiet ekrānā redzamos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="5a4ff-111">Mērvienības izveide vai rediģēšana</span><span class="sxs-lookup"><span data-stu-id="5a4ff-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="5a4ff-112">Lai izveidotu vai rediģētu mērvienību, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="5a4ff-113">Izpildiet kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="5a4ff-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="5a4ff-114">Lai rediģētu esošu vienību, atlasiet to saraksta rūtī.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="5a4ff-115">Lai izveidotu jaunu vienibu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="5a4ff-116">Ieraksta galvenē iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="5a4ff-117">**Vienība** - ievadiet ID vai simbolu, ko izmantot, lai atsauktos uz vienību sistēmas valodā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="5a4ff-118">Šis ID vai simbols parasti ir saīsinājums vienībai, piemēram, *kt* katram vai *cm* centimetriem.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="5a4ff-119">**Apraksts** - Ievadiet vienības aprakstošo nosaukumu sistēmas valodā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="5a4ff-120">Šis nosaukums parasti ir pilns vienības nosaukums, piemēram, *Katrs* vai *Centimetrs*.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="5a4ff-121">Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:</span><span class="sxs-lookup"><span data-stu-id="5a4ff-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="5a4ff-122">**Vienību klase** – atlasiet rekvizītu, ko vienība mēra (piemēram, garums, zona, masa vai daudzums).</span><span class="sxs-lookup"><span data-stu-id="5a4ff-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="5a4ff-123">**Mērvienību sistēma** – atlasiet mērvienību sistēmu, kurai pieder vienība (*Metriskās vienības* vai *Amerikas Savienotajās Valstīs lietotās vienības*).</span><span class="sxs-lookup"><span data-stu-id="5a4ff-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="5a4ff-124">**Pamatvienība** – iestatiet šo opciju kā *Jā*, lai izmantotu pašreizējo vienību kā pamatvienību tās vienību klasei.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="5a4ff-125">Šajā gadījumā jānorāda tikai pārvēršanas koeficients starp pamatvienību un katru papildu vienību vienību klasē.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="5a4ff-126">Pēc tam sistēma var konvertēt starp visām vienībām šajā vienību klasē.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="5a4ff-127">Tāpēc pārveidošanas ir vieglāk iestatīt.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="5a4ff-128">Piemēram, ja galons ir vienību klases *Apjoms* pamatvienība, jāiestata tikai pārveidošanas koeficienti no kvartas uz galonu un no pintas uz galonu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="5a4ff-129">Tad sistēma var konvertēt arī no kvartas uz pinti.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="5a4ff-130">Vienai mērvienību kategorijai var būt tikai viena pamatvienība.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="5a4ff-131">**Sistēmas vienība** – iestatiet šo opciju kā *Jā*, lai izmantotu pašreizējo vienību kā pieņemto vienību visiem nenorādītajiem mērījumiem tās mērvienību kategorijā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="5a4ff-132">Piemēram, ja lauks, kas tiek izmantots daudzuma ievadīšanai, neļauj norādīt vienību (piemēram, ja lietotājs neatlasa vienību), sistēma izmanto vienību, kas ir iestatīta kā sistēmas vienība mērvienību kategorijai *Daudzums*.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="5a4ff-133">Vienai mērvienību kategorijai var būt tikai viena sistēmas vienība.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="5a4ff-134">**Decimālā precizitāte** – norādiet decimāldaļu vietu skaitu, līdz kuram jānoapaļo vērtības, kas norādītas pašreizējai vienībai konvertētai uz to.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="5a4ff-135">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="5a4ff-136">Vienību tulkojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="5a4ff-136">Define unit translations</span></span>

<span data-ttu-id="5a4ff-137">Lai definētu ID vai simbola tulkojumus un mērvienības aprakstu, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="5a4ff-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="5a4ff-138">Izveidojiet vai atlasiet vienību, kurai jāizveido tulkojumi.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="5a4ff-139">Darbību rūtī atlasiet **Vienības teksti**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="5a4ff-140">Tiek parādīta lapa **Vienības teksti**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="5a4ff-141">Šī lapa tiek izmantota, lai definētu atlasītās vienības ID vai simbola tulkojumus.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="5a4ff-142">Šos tulkojumus pēc tam var izmantot ārējiem dokumentiem debitoram vai kreditoram raksturīgās valodās.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="5a4ff-143">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5a4ff-144">Laukā **Valoda** atlasiet valodu, ko izmantot, uz kuru tulkot vienības ID vai simbolu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="5a4ff-145">Laukā **Teksts** ievadiet vienības ID vai simbola tulkojumu atlasītajā valodā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="5a4ff-146">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5a4ff-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-147">Close the page.</span></span>
1. <span data-ttu-id="5a4ff-148">Tad **Darbību rūtī** atlasiet **Tulkotie vienību apraksti**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="5a4ff-149">Tiek parādīta lapa **Tulkotie vienību apraksti**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="5a4ff-150">Jūs izmantojat šo lapu, lai atlasītajai vienībai definētu valodai raksturīgus aprakstus.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="5a4ff-151">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5a4ff-152">Laukā **Valoda** atlasiet valodu, ko izmantot, uz kuru tulkot vienības aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="5a4ff-153">Laukā **Apraksts** ievadiet vienības apraksta tulkojumu atlasītajā valodā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="5a4ff-154">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5a4ff-155">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="5a4ff-156">Vienību pārveidošanas noteikumu definēšana</span><span class="sxs-lookup"><span data-stu-id="5a4ff-156">Define unit conversion rules</span></span>

<span data-ttu-id="5a4ff-157">Lai definētu konvertēšanas noteikumus starp mērvienībām, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="5a4ff-158">Izveidojiet vai atlasiet vienību, kurai jādefinē konvertēšanas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="5a4ff-159">Darbību rūtī atlasiet **Vienības konvertēšanas**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="5a4ff-160">Tiek paradīta lapa **Mērvienību konvertēšana**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="5a4ff-161">Izmantojiet šo lapu, lai definētu noteikumus atlasītas vienības konvertēšanai uz citām vienībām un no citām vienībām mērvienību kategorijā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="5a4ff-162">Atlasiet vienu no šīm cilnēm atkarībā no konvertēšanas tipa, ko vēlaties iestatīt:</span><span class="sxs-lookup"><span data-stu-id="5a4ff-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="5a4ff-163">**Standarta pārveidošana** – iestatiet standarta konvertēšanas noteikumus visām precēm.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="5a4ff-164">**Kategoriju iekšējās konvertēšanas** – iestatiet produktam specifiskus konvertēšanas noteikumus vienībām šajā mērvienību kategorijā.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="5a4ff-165">**Starpkategoriju konvertēšanas** – iestatiet produktam specifiskus konvertēšanas noteikumus vienībām vienībām pa mērvienību kategorijām.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="5a4ff-166">Izpildiet kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="5a4ff-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="5a4ff-167">Lai izveidotu jaunu konvertēšanu, rīkjoslā atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="5a4ff-168">Lai rediģētu esošo konvertēšanu, atlasiet režģī esošo konvertēšanu un pēc tam rīkjoslā atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="5a4ff-169">Parādītajā nolaižamajā dialoglodziņā iestatiet sekojošus laukus:</span><span class="sxs-lookup"><span data-stu-id="5a4ff-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="5a4ff-170">**Prece** – atlasiet noteiktu preci, uz kuru attiecas konvertēšana.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="5a4ff-171">Šis lauks ir pieejams tikai kategoriju iekšējām konvertēšanām un starpkategoriju konvertēšanām.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="5a4ff-172">**Formulas izkārtojums** – atstājiet šo lauku iestatītu uz *Vienkāršs*, lai norādītu vienkāršu konvertēšanu, kam ir viens faktors.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="5a4ff-173">Iestatiet to kā *Uzlabots*, lai iestatītu sarežģītāku vienādojumu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="5a4ff-174">Uzlaboto vienādojumu formāts atšķiras atkarībā no mērvienību kategorijas.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="5a4ff-175">**No vienības** – šis lauks rāda atlasīto vienību.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="5a4ff-176">Parasti vērtību nedrīkst mainīt.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-176">Usually, you should not change the value.</span></span> <span data-ttu-id="5a4ff-177">(Ja maināt vērtību, jāatver lapa **Vienību konvertēšana** atlasītajai vienībai, lai pēc tās saglabāšanas skatītu jauno konvertēšanu.)</span><span class="sxs-lookup"><span data-stu-id="5a4ff-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="5a4ff-178">**Uz vienību** – atlasiet vienību, uz kuru konvertēt.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="5a4ff-179">**Noapaļošana** – atlasiet, kā noapaļot daļskaitļus, pamatojoties uz atlasītās vienības vērtību **Decimāldaļas precizitāte** (*Līdz tuvākajam*, *Uz augšu* vai *Uz leju*).</span><span class="sxs-lookup"><span data-stu-id="5a4ff-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="5a4ff-180">**Konvertēšanas formula** – izmantojiet atlikušos laukus nolaižamā dialoglodziņa augšpusē, lai norādītu formulu konvertēšanai starp divām vienībām.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="5a4ff-181">Pieejamie lauki atšķiras atkarībā no atlasītās mērvienību kategorijas un formulas izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="5a4ff-182">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-182">Select **OK**.</span></span>
1. <span data-ttu-id="5a4ff-183">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="5a4ff-184">Varat arī iestatīt vienību konvertēšanu katram preces variantam.</span><span class="sxs-lookup"><span data-stu-id="5a4ff-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="5a4ff-185">Papildinformāciju skatiet [Mērvienību konvertēšana katram preces variantam](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="5a4ff-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
