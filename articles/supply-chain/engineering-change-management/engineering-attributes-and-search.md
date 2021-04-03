---
title: Tehniskie atribūti un tehnisko atribūtu meklēšana
description: Šajā tēmā izskaidrots, kā varat izmantot tehniskos atribūtus, lai norādītu visas nestandarta īpašības, lai nodrošinātu, ka visi preču šablona dati var tikt reģistrēti sistēmā. Tas arī izskaidro, kā varat izmantot tehnisko atribūtu meklēšanu, lai viegli atrastu produktus, pamatojoties uz šīm reģistrētajām iezīmēm.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 3ddb271535f0f2151f46a37a3ab3f3742e67ca87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262385"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a><span data-ttu-id="de00a-104">Tehniskie atribūti un tehnisko atribūtu meklēšana</span><span class="sxs-lookup"><span data-stu-id="de00a-104">Engineering attributes and engineering attribute search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de00a-105">Lai nodrošinātu, ka visus produkta pamatdatus var reģistrēt sistēmā, izmantojiet tehniskos atribūtus, lai norādītu visus nestandarta raksturlielumus.</span><span class="sxs-lookup"><span data-stu-id="de00a-105">To ensure that all product master data can be registered in the system, you should use engineering attributes to specify all non-standard characteristics.</span></span> <span data-ttu-id="de00a-106">Pēc tam varat izmantot tehnisko atribūtu meklēšanu, lai viegli atrastu produktus, pamatojoties uz šīm reģistrētajām iezīmēm.</span><span class="sxs-lookup"><span data-stu-id="de00a-106">You can then use engineering attribute search to easily find products, based on those registered characteristics.</span></span>

## <a name="engineering-attributes"></a><span data-ttu-id="de00a-107">Tehniskie atribūti</span><span class="sxs-lookup"><span data-stu-id="de00a-107">Engineering attributes</span></span>

<span data-ttu-id="de00a-108">Parasti tehniskiem produktiem ir daudz parametru un rekvizītu, kas ir jāaptver.</span><span class="sxs-lookup"><span data-stu-id="de00a-108">Typically, engineering products have many characteristics and properties that you must capture.</span></span> <span data-ttu-id="de00a-109">Lai gan dažus rekvizītus varat reģistrēt, izmantojot standarta produktu laukus, pēc nepieciešamības varat izveidot arī jaunus tehniskos rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="de00a-109">Although you can register some of the properties by using the standard product fields, you can also create new engineering properties as required.</span></span> <span data-ttu-id="de00a-110">Varat definēt savus *tehniskos atribūtus* un padarīt tos par daļu no produkta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="de00a-110">You can define your own *engineering attributes* and make them part of the product definition.</span></span>

### <a name="create-engineering-attributes-and-attribute-types"></a><span data-ttu-id="de00a-111">Izveidot tehniskos atribūtus un atribūtu veidus</span><span class="sxs-lookup"><span data-stu-id="de00a-111">Create engineering attributes and attribute types</span></span>

<span data-ttu-id="de00a-112">Katram tehniskajam atribūtam ir jāpieder *atribūta veidam*.</span><span class="sxs-lookup"><span data-stu-id="de00a-112">Each engineering attribute must belong to an *attribute type*.</span></span> <span data-ttu-id="de00a-113">Šī prasība pastāv, jo katram tehniskajam atribūtam ir jābūt *datu veidam*, kas nosaka vērtību veidus, kurus tas var saturēt.</span><span class="sxs-lookup"><span data-stu-id="de00a-113">This requirement exists because each engineering attribute must have a *data type* that defines the types of values that it can hold.</span></span> <span data-ttu-id="de00a-114">Inženierijas atribūta veids var būt standarta veids (piemēram, brīvais teksts, vesels skaitlis vai decimāls) vai pielāgots veids (piemēram, teksts, kam ir noteikta vērtību kopa, no kuras atlasīt).</span><span class="sxs-lookup"><span data-stu-id="de00a-114">An engineering attribute type can be a standard type (such as free text, integer, or decimal) or a custom type (such as text that has a specific set of values to select from).</span></span> <span data-ttu-id="de00a-115">Varat atkārtoti izmantot katru atribūta veidu ar jebkādu skaitu tehnisko atribūtu.</span><span class="sxs-lookup"><span data-stu-id="de00a-115">You can reuse each attribute type with any number of engineering attributes.</span></span>

#### <a name="set-up-engineering-attribute-types"></a><span data-ttu-id="de00a-116">Iestatīt tehnisko atribūtu veidus</span><span class="sxs-lookup"><span data-stu-id="de00a-116">Set up engineering attribute types</span></span>

<span data-ttu-id="de00a-117">Lai skatītu, izveidotu vai rediģētu tehnisko atribūta veidu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="de00a-117">To view, create, or edit an engineering attribute type, follow these steps.</span></span>

1. <span data-ttu-id="de00a-118">Dodieties uz **Tehniskā izmaiņu pārvaldība \> Iestatīšana \> Atribūti \> Atribūtu veidi**.</span><span class="sxs-lookup"><span data-stu-id="de00a-118">Go to **Engineering change management \> Setup \> Attributes \> Attribute types**.</span></span>
1. <span data-ttu-id="de00a-119">Atlasiet esošu atribūta veidu saraksta rūtī vai atlasiet **Jauns** darbības rūtī, lai izveidotu jaunu atribūta veidu.</span><span class="sxs-lookup"><span data-stu-id="de00a-119">Select an existing attribute type in the list pane, or select **New** on the Action Pane to create a new attribute type.</span></span>
1. <span data-ttu-id="de00a-120">Iestatiet tālāk minētos laukus:</span><span class="sxs-lookup"><span data-stu-id="de00a-120">Set the following fields:</span></span>

    - <span data-ttu-id="de00a-121">**Atribūta veida nosaukums** - ievadiet atribūta veida nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="de00a-121">**Attribute type name** – Enter a name for the attribute type.</span></span>
    - <span data-ttu-id="de00a-122">**Veids** — Atlasiet standarta datu veidu (*Valūta*, *Datums un laiks*, *Decimāls*, *Vesels skaitlis*, *Teksts*, *Būla* vai *Atsauce*).</span><span class="sxs-lookup"><span data-stu-id="de00a-122">**Type** – Select a standard data type (*Currency*, *DateTime*, *Decimal*, *Integer*, *Text*, *Boolean*, or *Reference*).</span></span>
    - <span data-ttu-id="de00a-123">**Fiksēts saraksts** — Šī opcija ir pieejama tikai tad, ja lauks **Veids** ir iestatīts uz *Teksts*.</span><span class="sxs-lookup"><span data-stu-id="de00a-123">**Fixed list** – This option is available only if you set the **Type** field to *Text*.</span></span> <span data-ttu-id="de00a-124">Iestatiet to uz *Jā*, lai definētu konkrētas vērtības šī veida atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="de00a-124">Set it to *Yes* to define specific values for attributes of this type.</span></span> <span data-ttu-id="de00a-125">Šādā gadījumā tiks izveidots nolaižamais saraksts.</span><span class="sxs-lookup"><span data-stu-id="de00a-125">In this case, a drop-down list will be created.</span></span> <span data-ttu-id="de00a-126">Izmantojiet kopsavilkuma cilni **Vērtība**, lai noteiktu vērtības, kas ir pieejamas šim atribūta veidam.</span><span class="sxs-lookup"><span data-stu-id="de00a-126">You use the **Value** FastTab to establish the values that are available for this attribute type.</span></span> <span data-ttu-id="de00a-127">Iestatiet šo opciju uz *Nē*, lai ļautu lietotājiem ievadīt jebkuru vērtību.</span><span class="sxs-lookup"><span data-stu-id="de00a-127">Set this option to *No* to allow users to enter any value.</span></span> <span data-ttu-id="de00a-128">Šādā gadījumā tiks izveidots ievades lauks.</span><span class="sxs-lookup"><span data-stu-id="de00a-128">In this case, an input field will be created.</span></span>
    - <span data-ttu-id="de00a-129">**Vērtību diapazons** — Šī opcija ir pieejama tikai tad, ja lauks **Veids** ir iestatīts kā *Vesels skaitlis*, *Decimāls* vai *Valūta*.</span><span class="sxs-lookup"><span data-stu-id="de00a-129">**Value range** – This option is available only if you set the **Type** field to *Integer*, *Decimal*, or *Currency*.</span></span> <span data-ttu-id="de00a-130">Iestatiet to uz *Jā*, lai noteiktu minimālās un maksimālās vērtības, kas tiks pieņemtas šī veida atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="de00a-130">Set it to *Yes* to establish minimum and maximum values that will be accepted for attributes of this type.</span></span> <span data-ttu-id="de00a-131">Lietojiet kopsavilkuma cilni **Diapazons**, lai noteiktu minimālās un maksimālās vērtības un (valūtai) valūtu, kas tiek piemērota ievadītajiem ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="de00a-131">You use the **Range** FastTab to establish the minimum and maximum values, and (for currency) the currency that applies for the limits that you entered.</span></span> <span data-ttu-id="de00a-132">Iestatiet šo opciju uz *Nē*, lai akceptētu jebkuru vērtību.</span><span class="sxs-lookup"><span data-stu-id="de00a-132">Set this option to *No* to accept any value.</span></span> 
    - <span data-ttu-id="de00a-133">**Mērvienība** - Šis lauks ir pieejams tikai tad, ja lauks **Veids** ir iestatīts kā *Vesels skaitlis* vai *Decimāls*.</span><span class="sxs-lookup"><span data-stu-id="de00a-133">**Unit of measure** – This field is available only if you set the **Type** field to *Integer* or *Decimal*.</span></span> <span data-ttu-id="de00a-134">Atlasiet mērvienību, kas attiecas uz šo atribūta veidu.</span><span class="sxs-lookup"><span data-stu-id="de00a-134">Select the unit of measure that applies for this attribute type.</span></span> <span data-ttu-id="de00a-135">Ja nav nepieciešama vienība, atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="de00a-135">If no unit is required, leave this field blank.</span></span>

#### <a name="set-up-engineering-attributes"></a><span data-ttu-id="de00a-136">Iestatīt tehniskos atribūtus</span><span class="sxs-lookup"><span data-stu-id="de00a-136">Set up engineering attributes</span></span>

<span data-ttu-id="de00a-137">Lai skatītu, izveidotu vai rediģētu tehnisko atribūtu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="de00a-137">To view, create, or edit an engineering attribute, follow these steps.</span></span>

1. <span data-ttu-id="de00a-138">Dodieties uz **Tehniskā izmaiņu pārvaldība \> Iestatīšana \> Atribūti \> Tehniskie atribūti**.</span><span class="sxs-lookup"><span data-stu-id="de00a-138">Go to **Engineering change management \> Setup \> Attributes \> Engineering attributes**.</span></span>
1. <span data-ttu-id="de00a-139">Atlasiet esošu atribūtu saraksta rūtī vai atlasiet **Jauns** darbības rūtī, lai izveidotu jaunu atribūtu.</span><span class="sxs-lookup"><span data-stu-id="de00a-139">Select an existing attribute in the list pane, or select **New** on the Action Pane to create a new attribute.</span></span>
1. <span data-ttu-id="de00a-140">Iestatiet tālāk minētos laukus:</span><span class="sxs-lookup"><span data-stu-id="de00a-140">Set the following fields:</span></span>

    - <span data-ttu-id="de00a-141">**Nosaukums** – ievadiet atribūta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="de00a-141">**Name** – Enter a name for the attribute.</span></span> <span data-ttu-id="de00a-142">Šis nosaukums tiek rādīts tikai lapā **Tehniskie atribūti**.</span><span class="sxs-lookup"><span data-stu-id="de00a-142">This name appears only on the **Engineering attributes** page.</span></span> <span data-ttu-id="de00a-143">Visur citur sistēmā lauka **Vārds un uzvārds** vērtība parasti tiek rādīta, lai identificētu atribūtu.</span><span class="sxs-lookup"><span data-stu-id="de00a-143">Everywhere else in the system, the value of the **Friendly name** field is usually shown to identify the attribute.</span></span>
    - <span data-ttu-id="de00a-144">**Atribūta veids** — Atlasiet atribūta veidu, kas definēts iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="de00a-144">**Attribute type** – Select an attribute type that you defined in the previous section.</span></span>
    - <span data-ttu-id="de00a-145">**Vārds un uzvārds** — Ievadiet nosaukumu, kas identificēs atribūtu sistēmā (izņemot lapā **Tehniskie atribūti** ).</span><span class="sxs-lookup"><span data-stu-id="de00a-145">**Friendly name** – Enter a name that will identify the attribute in the system (except on the **Engineering attributes** page).</span></span> 
    - <span data-ttu-id="de00a-146">**Apraksts** — ievadiet atribūta aprakstu.</span><span class="sxs-lookup"><span data-stu-id="de00a-146">**Description** – Enter a description of the attribute.</span></span>
    - <span data-ttu-id="de00a-147">**Palīdzības teksts** — Ievadiet palīdzības tekstu, kas citiem lietotājiem norāda, kam šis atribūts ir paredzēts.</span><span class="sxs-lookup"><span data-stu-id="de00a-147">**Help text** – Enter Help text that tells other users what the attribute is for.</span></span>
    - <span data-ttu-id="de00a-148">**Noklusētā vērtība** — Ievadiet atribūtam noklusēto vērtību.</span><span class="sxs-lookup"><span data-stu-id="de00a-148">**Default value** – Enter a default value for the attribute.</span></span> <span data-ttu-id="de00a-149">Piedāvātās opcijas ir atkarīgas no atlasītā atribūta veida.</span><span class="sxs-lookup"><span data-stu-id="de00a-149">The options that are presented depend on the attribute type that you selected.</span></span>
    - <span data-ttu-id="de00a-150">**Valūta** – Ja izvēlētais atribūta veids ir valūta, atlasiet valūtu, ko atribūts akceptēs, un parādiet vērtības elementā.</span><span class="sxs-lookup"><span data-stu-id="de00a-150">**Currency** – If the attribute type that you selected is a currency, select the currency that the attribute will accept and show values in.</span></span>

1. <span data-ttu-id="de00a-151">Ja izvēlētais atribūta veids ir vesels skaitlis vai decimāls, tiek rādīta kopsavilkuma cilne **Diapazons**.</span><span class="sxs-lookup"><span data-stu-id="de00a-151">If the attribute type that you selected is an integer or a decimal, the **Range** FastTab is shown.</span></span> <span data-ttu-id="de00a-152">Šajā kopsavilkuma cilnē, pēc nepieciešamības iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="de00a-152">On this FastTab, set the following fields as required:</span></span>

    - <span data-ttu-id="de00a-153">**Tolerances darbība** — Atlasiet, kā sistēmai jāreaģē, ja lietotājs ievada vērtību, kas atrodas ārpus norādītā diapazona.</span><span class="sxs-lookup"><span data-stu-id="de00a-153">**Tolerance action** – Select how the system should respond if a user enters a value outside the specified range.</span></span> <span data-ttu-id="de00a-154">Ja atlasāt *Brīdinājums*, tiek parādīts brīdinājums, bet lietotājs var saglabāt vērtību.</span><span class="sxs-lookup"><span data-stu-id="de00a-154">If you select *Warning*, a warning is shown, but the user can save the value.</span></span> <span data-ttu-id="de00a-155">Ja atlasāt *Nav atļauts*, tiek parādīts brīdinājums, un vērtību nevar saglabāt, kamēr lietotājs to nelabo.</span><span class="sxs-lookup"><span data-stu-id="de00a-155">If you select *Not allowed*, a warning is shown, and the value can't be saved until the user corrects it.</span></span>
    - <span data-ttu-id="de00a-156">**Minimums** — Ievadiet minimālo ieteicamo vai akceptēto vērtību.</span><span class="sxs-lookup"><span data-stu-id="de00a-156">**Minimum** – Enter the minimum recommended or accepted value.</span></span>
    - <span data-ttu-id="de00a-157">**Maksimums** — Ievadiet maksimālo ieteicamo vai akceptēto vērtību.</span><span class="sxs-lookup"><span data-stu-id="de00a-157">**Maximum** – Enter the maximum recommended or accepted value.</span></span>

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a><span data-ttu-id="de00a-158">Piesaistiet tehniskos atribūtus tehnisko produktu kategorijai</span><span class="sxs-lookup"><span data-stu-id="de00a-158">Connect engineering attributes to an engineering product category</span></span>

<span data-ttu-id="de00a-159">Daži tehniskie atribūti attiecas uz visiem produktiem, turpretī citi ir raksturīgi atsevišķiem produktiem vai produktu kategorijām.</span><span class="sxs-lookup"><span data-stu-id="de00a-159">Some engineering attributes apply to all products, whereas others are specific to individual products or product categories.</span></span> <span data-ttu-id="de00a-160">Piemēram, elektriskie atribūti nav nepieciešami mehāniskajiem produktiem.</span><span class="sxs-lookup"><span data-stu-id="de00a-160">For example, electrical attributes aren't required for mechanical products.</span></span> <span data-ttu-id="de00a-161">Tāpēc varat iestatīt *tehnisko produktu kategorijas*.</span><span class="sxs-lookup"><span data-stu-id="de00a-161">Therefore, you can set up *engineering product categories*.</span></span> <span data-ttu-id="de00a-162">Tehnisko produktu kategorija nosaka tehnisko atribūtu kolekciju, kam jābūt daļai no definīcijas produktiem, kas pieder šai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="de00a-162">An engineering product category establishes the collection of engineering attributes that must be part of the definition for products that belong to that category.</span></span> <span data-ttu-id="de00a-163">Varat arī norādīt, kuri tehniskie atribūti ir obligāti un vai ir noklusētā vērtība.</span><span class="sxs-lookup"><span data-stu-id="de00a-163">You can also specify which engineering attributes are mandatory and whether there is a default value.</span></span>

<span data-ttu-id="de00a-164">Papildinformāciju par to, kā strādāt ar tehnisko produktu kategorijām, tostarp informāciju par to, kā pievienot atribūtus kategorijām, skatiet [Tehniskās versijas un tehnisko produktu kategorijas](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="de00a-164">For more information about how to work with engineering product categories, including information about how to connect attributes to categories, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

### <a name="set-values-for-engineering-attributes"></a><span data-ttu-id="de00a-165">Iestatīt tehnisko atribūtu vērtības</span><span class="sxs-lookup"><span data-stu-id="de00a-165">Set values for engineering attributes</span></span>

<span data-ttu-id="de00a-166">Tehniskie atribūti, kas ir pievienoti tehnisko produktu kategorijai, tiek parādīti, kad izveidojat jaunu tehnisko produktu, kas ir balstīts uz šo kategoriju.</span><span class="sxs-lookup"><span data-stu-id="de00a-166">The engineering attributes that are connected to an engineering product category are presented when you create a new engineering product that is based on that category.</span></span> <span data-ttu-id="de00a-167">Tajā laikā varat iestatīt atribūtu vērtības.</span><span class="sxs-lookup"><span data-stu-id="de00a-167">At that time, you can set values for the attributes.</span></span> <span data-ttu-id="de00a-168">Vēlāk šīs vērtības var mainīt lapā **Tehniskās versijas** vai kā daļu no tehnisko izmaiņu pārvaldības tehnisko izmaiņu pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="de00a-168">Later, those values can be changed on the **Engineering version** page or as part of engineering change management in an engineering change order.</span></span> <span data-ttu-id="de00a-169">Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="de00a-169">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>

### <a name="create-an-engineering-product"></a><span data-ttu-id="de00a-170">Izveidot tehnisko produktu</span><span class="sxs-lookup"><span data-stu-id="de00a-170">Create an engineering product</span></span>

<span data-ttu-id="de00a-171">Lai izveidotu tehnisko produktu, atveriet lapu **Izlaistie produkti**.</span><span class="sxs-lookup"><span data-stu-id="de00a-171">To create an engineering product, open the **Released products** page.</span></span> <span data-ttu-id="de00a-172">Pēc tam darbību rūts grupas **Jauns** cilnē **Produkts** atlasiet **Tehniskais produkts**.</span><span class="sxs-lookup"><span data-stu-id="de00a-172">Then, on the Action Pane, on **Product** tab, in the **New** group, select **Engineering product**.</span></span>

<span data-ttu-id="de00a-173">Jānorāda tehniskā kategorija, kurai pieder šis produkts.</span><span class="sxs-lookup"><span data-stu-id="de00a-173">You must specify the engineering category that the product belongs to.</span></span> <span data-ttu-id="de00a-174">Kategorija noteiks visas produkta noklusētās vērtības un īpašības.</span><span class="sxs-lookup"><span data-stu-id="de00a-174">The category will set all the default values and characteristics for the product.</span></span> <span data-ttu-id="de00a-175">Tas arī iestatīs atribūtus, kas attiecas uz produktu.</span><span class="sxs-lookup"><span data-stu-id="de00a-175">It will also set the attributes that are applicable to the product.</span></span> <span data-ttu-id="de00a-176">Pēc kategorijas atlasīšanas, vērtības tiks iestatītas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="de00a-176">After the category is selected, values will be set for the attributes.</span></span> <span data-ttu-id="de00a-177">Pēc tam šīs vērtības var modificēt.</span><span class="sxs-lookup"><span data-stu-id="de00a-177">You can then modify those values.</span></span>

## <a name="search-for-products-by-using-engineering-attribute-values"></a><span data-ttu-id="de00a-178">Meklēt produktus, izmantojot tehnisko atribūtu vērtības</span><span class="sxs-lookup"><span data-stu-id="de00a-178">Search for products by using engineering attribute values</span></span>

<span data-ttu-id="de00a-179">Varat izmantot tehnisko atribūtu meklēšanu, lai atrastu produktus, meklējot to tehnisko atribūtu vērtības.</span><span class="sxs-lookup"><span data-stu-id="de00a-179">You can use engineering attribute search to find products by searching for their engineering attributes values.</span></span> <span data-ttu-id="de00a-180">Tādēļ viegli varat atrast tehniskos produktus, pamatojoties uz to īpašībām.</span><span class="sxs-lookup"><span data-stu-id="de00a-180">Therefore, you can easily find engineering products, based on their characteristics.</span></span> <span data-ttu-id="de00a-181">Varat meklēt produktus, kas pieder tehnisko produktu kategorijai, vai arī varat meklēt visos tehniskos produktos.</span><span class="sxs-lookup"><span data-stu-id="de00a-181">You can search in the products that belong to an engineering product category, or you can search across all engineering products.</span></span>

<span data-ttu-id="de00a-182">Meklēšana ir pieejama preces šablona datu lapās un no transakciju krājumiem sistēmā, piemēram, pārdošanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="de00a-182">The search is available on product master data pages and from transactional items in the system, such as sales orders.</span></span> <span data-ttu-id="de00a-183">Lai meklētu produktu, varat izmantot lapu **Tehnisko atribūtu meklēšana**.</span><span class="sxs-lookup"><span data-stu-id="de00a-183">For a transactional item, you can use the **Engineering attribute search** page to search for a product.</span></span> <span data-ttu-id="de00a-184">Pēc tam varat izmantot pogu **Pievienot kā jaunu rindu**, lai pievienotu produktu pārdošanas pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="de00a-184">You can then use the **Add as new line** button to add the product to the sales order lines.</span></span> <span data-ttu-id="de00a-185">Produktus meklēšanas rezultātos var arī pievienot tieši pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="de00a-185">Products in the search results can also be added directly to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]