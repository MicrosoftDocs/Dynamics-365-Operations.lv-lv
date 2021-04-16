---
title: Preces konfigurācijas modeļa aprēķini
description: Šajā tēmā aprakstīts, kā izveidot preces konfigurācijas modeļa atribūtu aprēķinus
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829622"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="22d25-103">Preces konfigurācijas modeļa aprēķini</span><span class="sxs-lookup"><span data-stu-id="22d25-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22d25-104">Šajā tēmā aprakstīts, kā izveidot preces konfigurācijas modeļa atribūtu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="22d25-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="22d25-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="22d25-105">Prerequisites</span></span>

<span data-ttu-id="22d25-106">Aprēķinus preces konfigurēšanas modelī var izmantot, lai aprēķinātu preces konfigurācijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="22d25-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="22d25-107">Pirms varat sākt iestatīt aprēķinus, ir jāpastāv saistītajam preču konfigurācijas modelim.</span><span class="sxs-lookup"><span data-stu-id="22d25-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="22d25-108">Konfigurācijas modeļu iestatīšanas procesa apskatu un saistītos uzdevumus skatiet sadaļā [Preču konfigurācijas modeļa iestatīšana](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="22d25-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="22d25-109">Aprēķina izveide</span><span class="sxs-lookup"><span data-stu-id="22d25-109">Create a calculation</span></span>

<span data-ttu-id="22d25-110">Aprēķinu veido izteiksme un mērķa atribūts.</span><span class="sxs-lookup"><span data-stu-id="22d25-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="22d25-111">Papildinformāciju par preču konfigurācijas modeļiem skatiet tēmā [BUJ par preces konfigurācijas modeļu aprēķiniem](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="22d25-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="22d25-112">Lai izveidotu aprēķinu esošam preču modelim, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="22d25-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="22d25-113">Dodieties uz **Preču informācijas pārvaldība \> Vispārīgi \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="22d25-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="22d25-114">Atlasiet preces konfigurācijas modeli un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="22d25-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="22d25-115">Kopsavilkuma cilnē **Aprēķini** atlasiet **Pievienot**, lai pievienotu aprēķinu, un iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="22d25-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="22d25-116">**Nosaukums** – ievadiet aprēķina nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="22d25-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="22d25-117">**Apraksts** — ievadiet aprēķina aprakstu.</span><span class="sxs-lookup"><span data-stu-id="22d25-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="22d25-118">**Mērķa atribūts** — atlasiet atribūtu, kam tiek veidots aprēķins.</span><span class="sxs-lookup"><span data-stu-id="22d25-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="22d25-119">Atlasiet **Rediģēt izteiksmi**.</span><span class="sxs-lookup"><span data-stu-id="22d25-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="22d25-120">Dialoglodziņā **Ievadīt aprēķinu** pievienojiet izteiksmei nepieciešamos atribūtus, operatorus un vērtības.</span><span class="sxs-lookup"><span data-stu-id="22d25-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="22d25-121">Plašāku informāciju par darbībām ar šiem elementiem skatiet rakstā [Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="22d25-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="22d25-122">Kad izteiksme ir gatava, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="22d25-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="22d25-123">Aprēķina piemēri</span><span class="sxs-lookup"><span data-stu-id="22d25-123">Calculation examples</span></span>

<span data-ttu-id="22d25-124">Šajā sadaļā sniegti daži piemēri, kas parāda, kā aprēķini darbojas.</span><span class="sxs-lookup"><span data-stu-id="22d25-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="22d25-125">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="22d25-125">Example 1</span></span>

<span data-ttu-id="22d25-126">Nākamajā piemērā mērķa atribūts ir Būla tipa, un aprēķinā tiek izmantota nosacījuma izteiksme:</span><span class="sxs-lookup"><span data-stu-id="22d25-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="22d25-127">Šī izteiksme mērķa atribūtam atgriež vērtību *Patiess*, ja vērtība `decimalAttribute2` ir lielāka par vai vienāda ar vērtību `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="22d25-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="22d25-128">Pretējā gadījumā tā atgriež Būla vērtību *Aplams*.</span><span class="sxs-lookup"><span data-stu-id="22d25-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="22d25-129">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="22d25-129">Example 2</span></span>

<span data-ttu-id="22d25-130">Šajā piemērā teksta atribūts `textFixedList` tiek izmantots kā mērķa atribūts.</span><span class="sxs-lookup"><span data-stu-id="22d25-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="22d25-131">Šis atribūts ietver šādu fiksēto sarakstu.</span><span class="sxs-lookup"><span data-stu-id="22d25-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="22d25-132">Vērtība</span><span class="sxs-lookup"><span data-stu-id="22d25-132">Value</span></span> | <span data-ttu-id="22d25-133">Risinātāja vērtība</span><span class="sxs-lookup"><span data-stu-id="22d25-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="22d25-134">A</span><span class="sxs-lookup"><span data-stu-id="22d25-134">A</span></span> | <span data-ttu-id="22d25-135">1a</span><span class="sxs-lookup"><span data-stu-id="22d25-135">1a</span></span> |
| <span data-ttu-id="22d25-136">mljrd.</span><span class="sxs-lookup"><span data-stu-id="22d25-136">B</span></span> | <span data-ttu-id="22d25-137">2b</span><span class="sxs-lookup"><span data-stu-id="22d25-137">2b</span></span> |
| <span data-ttu-id="22d25-138">K</span><span class="sxs-lookup"><span data-stu-id="22d25-138">C</span></span> | <span data-ttu-id="22d25-139">2c</span><span class="sxs-lookup"><span data-stu-id="22d25-139">2c</span></span> |

<span data-ttu-id="22d25-140">Šajā ekrānuzņēmumā parādīts, kā šī atribūta iestatījumi var izskatīties jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="22d25-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="22d25-141">![Atribūta tipa iestatījumi 2. piemēram](media/model-calculations-example2.png "Atribūta tipa iestatījumi 2. piemēram")</span><span class="sxs-lookup"><span data-stu-id="22d25-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="22d25-142">Atribūts tiek lietots šādā nosacījuma priekšrakstā:</span><span class="sxs-lookup"><span data-stu-id="22d25-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="22d25-143">Ja `integerAttribute` ir mazāks par 150, šis priekšraksts atgriež pirmā ieraksta teksta vērtību fiksētā sarakstā *A*. Pretējā gadījumā tiek atgriezta trešā ieraksta teksta vērtība fiksētā sarakstā *C*.</span><span class="sxs-lookup"><span data-stu-id="22d25-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="22d25-144">Fiksētais saraksts ir nulles bāzes uzskaitījuma (uzskaitījuma) ekvivalents, un tā vērtībām piekļūst no atbilstošā vesela skaitļa vērtības.</span><span class="sxs-lookup"><span data-stu-id="22d25-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="22d25-145">Tāpēc pirmā fiksētā saraksta vērtība (*A*) tiek saskaņota ar *0*, otrā vērtība (*B*) tiek saskaņota ar *1*, un trešā vērtība (*C*) tiek saskaņota ar *2*.</span><span class="sxs-lookup"><span data-stu-id="22d25-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="22d25-146">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="22d25-146">Example 3</span></span>

<span data-ttu-id="22d25-147">Šajā piemērā teksta atribūts `textFixedList` tiek izmantots kā mērķa atribūts no iepriekšējā piemēra.</span><span class="sxs-lookup"><span data-stu-id="22d25-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="22d25-148">Tas izmanto arī citu teksta `textAttribute` atribūtu, kas satur šādu fiksēto sarakstu.</span><span class="sxs-lookup"><span data-stu-id="22d25-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="22d25-149">Vērtība</span><span class="sxs-lookup"><span data-stu-id="22d25-149">Value</span></span> | <span data-ttu-id="22d25-150">Risinātāja vērtība</span><span class="sxs-lookup"><span data-stu-id="22d25-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="22d25-151">AA</span><span class="sxs-lookup"><span data-stu-id="22d25-151">AA</span></span> | <span data-ttu-id="22d25-152">1aa</span><span class="sxs-lookup"><span data-stu-id="22d25-152">1aa</span></span> |
| <span data-ttu-id="22d25-153">BB</span><span class="sxs-lookup"><span data-stu-id="22d25-153">BB</span></span> | <span data-ttu-id="22d25-154">2bb</span><span class="sxs-lookup"><span data-stu-id="22d25-154">2bb</span></span> |

<span data-ttu-id="22d25-155">Šajā ekrānuzņēmumā parādīts, kā šī atribūta iestatījumi var izskatīties jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="22d25-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="22d25-156">![Atribūta tipa iestatījumi 3. piemēram](media/model-calculations-example3.png "Atribūta tipa iestatījumi 3. piemēram")</span><span class="sxs-lookup"><span data-stu-id="22d25-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="22d25-157">Atribūta `textFixedList` vērtība tiek aprēķināta, izmantojot šādu nosacījuma priekšrakstu:</span><span class="sxs-lookup"><span data-stu-id="22d25-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="22d25-158">Ja `textAttribute` vērtība ir vienāda ar *1aa*, šī izteiksme atgriež pirmā ieraksta teksta vērtību fiksētā sarakstā `textFixedList` *A*. Pretējā gadījumā tiek atgriezta trešā ieraksta teksta vērtība fiksētā sarakstā `textFixedList` *C*.</span><span class="sxs-lookup"><span data-stu-id="22d25-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="22d25-159">Nosacījuma priekšrakstam ir jāizmanto atribūta risinātāja vērtība.</span><span class="sxs-lookup"><span data-stu-id="22d25-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="22d25-160">Aprēķinos var lietot tikai fiksētā saraksta teksta atribūtus.</span><span class="sxs-lookup"><span data-stu-id="22d25-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="22d25-161">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="22d25-161">See also</span></span>

- [<span data-ttu-id="22d25-162">Biežāk uzdotie jautājumi par preču konfigurācijas modeļu aprēķiniem</span><span class="sxs-lookup"><span data-stu-id="22d25-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="22d25-163">Izteiksmes ierobežojuma pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="22d25-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="22d25-164">Pārskats par preču konfigurācijas modeļiem</span><span class="sxs-lookup"><span data-stu-id="22d25-164">Product configuration models overview</span></span>](product-configuration-models.md)
