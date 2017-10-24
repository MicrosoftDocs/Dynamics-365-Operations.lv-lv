---
title: "Sistēmas definēti un lietotāja definēti tabulas ierobežojumi"
description: "Šajā rakstā ir aprakstīti lietotāja un sistēmas definēta preces konfigurācijas modeļa komponentu tabulas divi ierobežojumu veidi. Tabulas ierobežojumi attiecas uz atļauto atribūtu kombināciju matricām, kur katra rinda nosaka vienu iespējamo atribūta vērtību kopu."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b59452496f0ad47f1fe2ff034895a082a205dda9
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="84004-104">Sistēmas definēti un lietotāja definēti tabulas ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="84004-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="84004-105">Šajā rakstā ir aprakstīti lietotāja un sistēmas definēta preces konfigurācijas modeļa komponentu tabulas divi ierobežojumu veidi.</span><span class="sxs-lookup"><span data-stu-id="84004-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="84004-106">Tabulas ierobežojumi attiecas uz atļauto atribūtu kombināciju matricām, kur katra rinda nosaka vienu iespējamo atribūta vērtību kopu.</span><span class="sxs-lookup"><span data-stu-id="84004-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="84004-107">Tabulas ierobežojumi attiecas uz to atribūtu kombināciju matricām, kas atļauti komponentiem preču konfigurēšanas modelī.</span><span class="sxs-lookup"><span data-stu-id="84004-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="84004-108">Katra tabulas rinda nosaka vienu iespējamo atribūtu vērtību kopu.</span><span class="sxs-lookup"><span data-stu-id="84004-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="84004-109">Preču konfigurēšanas modelī ir iespējams noteikt divu veidu ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="84004-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="84004-110">**Izteiksmes ierobežojums** — izveidojiet izteiksmi, kas nosaka attiecības starp atribūtiem, lai nodrošinātu, ka preces konfigurācijas laikā var atlasīt tikai saderīgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="84004-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="84004-111">**Tabulas ierobežojums** — izveidot tabulu, kas definē visas kombinācijas, kas atļautas norādītajai atribūtu kopai.</span><span class="sxs-lookup"><span data-stu-id="84004-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="84004-112">Ir pieejami divu veidu tabulas ierobežojumi: lietotāja definēti tabulas ierobežojumi un sistēmas definēti tabulas ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="84004-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="84004-113">Šajā rakstā aprakstīti lietotāja definēti un sistēmas definēti tabulas ierobežojumi komponentiem preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="84004-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="84004-114">Lietotāja definēti tabulas ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="84004-114">User-defined table constraints</span></span>
<span data-ttu-id="84004-115">Lietotāja definēts tabulas ierobežojums ir matricas veids, ko izmanto, lai aprakstītu tādu atribūtu vērtību kombināciju kopas, ko definē atribūtu veidi.</span><span class="sxs-lookup"><span data-stu-id="84004-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="84004-116">Piemēram, ja ražojat skaļruņus, lietotāja definētā tabulas ierobežojumā varat iekļaut korpusa apdares kolonnas un priekšējo režģi.</span><span class="sxs-lookup"><span data-stu-id="84004-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="84004-117">Korpusa apdares atribūta veidam ir četras vērtības, bet priekšējā režģa atribūta veidam — trīs vērtības.</span><span class="sxs-lookup"><span data-stu-id="84004-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="84004-118">Tādēļ, ja ierobežojumi netiek izmantoti, ir iespējamas 4 × 3 = 12 kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="84004-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="84004-119">Tomēr šajā piemērā ir atļautas tikai sešas kombinācijas, kā parādīts nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="84004-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="84004-120">Šī Informācija tiek parādīta lapas **Rediģēt tabulas ierobežojumu** cilnē **Atļautās kombinācijas**.</span><span class="sxs-lookup"><span data-stu-id="84004-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="84004-121">Korpusa apdare</span><span class="sxs-lookup"><span data-stu-id="84004-121">Cabinet finish</span></span> | <span data-ttu-id="84004-122">Priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="84004-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="84004-123">melna</span><span class="sxs-lookup"><span data-stu-id="84004-123">Black</span></span>          | <span data-ttu-id="84004-124">melna</span><span class="sxs-lookup"><span data-stu-id="84004-124">Black</span></span>       |
| <span data-ttu-id="84004-125">melna</span><span class="sxs-lookup"><span data-stu-id="84004-125">Black</span></span>          | <span data-ttu-id="84004-126">Metāla</span><span class="sxs-lookup"><span data-stu-id="84004-126">Metal</span></span>       |
| <span data-ttu-id="84004-127">Ozola</span><span class="sxs-lookup"><span data-stu-id="84004-127">Oak</span></span>            | <span data-ttu-id="84004-128">melna</span><span class="sxs-lookup"><span data-stu-id="84004-128">Black</span></span>       |
| <span data-ttu-id="84004-129">Rožkoka</span><span class="sxs-lookup"><span data-stu-id="84004-129">Rosewood</span></span>       | <span data-ttu-id="84004-130">Balta</span><span class="sxs-lookup"><span data-stu-id="84004-130">White</span></span>       |
| <span data-ttu-id="84004-131">Balta</span><span class="sxs-lookup"><span data-stu-id="84004-131">White</span></span>          | <span data-ttu-id="84004-132">melna</span><span class="sxs-lookup"><span data-stu-id="84004-132">Black</span></span>       |
| <span data-ttu-id="84004-133">Balta</span><span class="sxs-lookup"><span data-stu-id="84004-133">White</span></span>          | <span data-ttu-id="84004-134">Balta</span><span class="sxs-lookup"><span data-stu-id="84004-134">White</span></span>       |

<span data-ttu-id="84004-135">Lietotāja definētos tabulas ierobežojumus nosaka ar statisku tabulu ievadi, kas darbojas tādā pašā veidā, kā izteiksmes ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="84004-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="84004-136">Izmantojot lietotāja definētu tabulas ierobežojumu, tabulas parasti ir vieglāk izveidot, izprast un uzturēt, nekā garus izteiksmes ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="84004-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="84004-137">Sistēmas definēti tabulas ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="84004-137">System-defined table constraints</span></span>
<span data-ttu-id="84004-138">Sistēmas definēts tabulas ierobežojums izveido dinamisku kartēšanu starp atribūta veidu un lauku tabulā.</span><span class="sxs-lookup"><span data-stu-id="84004-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="84004-139">Ja sistēmas definētu tabulas ierobežojumu iekļauj preces konfigurācijas modelī, kartēšana nodrošina, ka tiks paradīti nevis atribūta veida vērtības, bet gan tabulas dati.</span><span class="sxs-lookup"><span data-stu-id="84004-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="84004-140">Rezultātā tiek iegūts dinamisks ierobežojums, jo tabulas saturu var modificēt (piemēram, izmantojot citus moduļus).</span><span class="sxs-lookup"><span data-stu-id="84004-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="84004-141">Izveidojot sistēmas definētu tabulas ierobežojumu, atlasiet tabulu, ja vēlaties papildus definēt izmantojamu vaicājumu, un pēc tam piesaistiet atribūtu veidus atlasītās tabulas laukiem.</span><span class="sxs-lookup"><span data-stu-id="84004-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="84004-142">Lauku veidiem jāatbilst atribūtu veidiem.</span><span class="sxs-lookup"><span data-stu-id="84004-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="84004-143">Pirms tabulas ierobežojumu var izmantot preces konfigurācijas modelī, tabulas ierobežojums jāiekļauj ierobežojumā vienā no modeļu komponentiem.</span><span class="sxs-lookup"><span data-stu-id="84004-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="84004-144">Procedūra paredzēta, lai izveidotu jaunu ierobežojumu, atlasītu tabulas ierobežojuma veidu, un pēc tam atlasītu tabulas lietojamo ierobežojuma definīciju.</span><span class="sxs-lookup"><span data-stu-id="84004-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="84004-145">Visbeidzot visi tabulas ierobežojuma lauki jākartē uz atribūtiem preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="84004-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="84004-146">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="84004-146">See also</span></span>
--------

[<span data-ttu-id="84004-147">Preču konfigurācijas modeļu galvenie jēdzieni</span><span class="sxs-lookup"><span data-stu-id="84004-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




