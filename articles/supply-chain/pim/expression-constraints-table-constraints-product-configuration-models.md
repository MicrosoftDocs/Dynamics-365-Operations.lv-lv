---
title: Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos
description: Šajā tēmā aprakstīta izteiksmes ierobežojumu un tabulas ierobežojumu lietošana. Ierobežojumi, lai kontrolē atribūta vērtības, ko varat atlasīt, kad konfigurējat preces pārdošanas piedāvājumam, pirkšanas pasūtījumam vai ražošanas pasūtījumam. Var izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus, atkarībā no tā, kā vēlaties veidot ierobežojumus.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 989981e6ca8c1075367776ceafe5b88429e004d2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243229"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="965fe-105">Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos</span><span class="sxs-lookup"><span data-stu-id="965fe-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="965fe-106">Šajā tēmā aprakstīta izteiksmes ierobežojumu un tabulas ierobežojumu lietošana.</span><span class="sxs-lookup"><span data-stu-id="965fe-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="965fe-107">Ierobežojumi, lai kontrolē atribūta vērtības, ko varat atlasīt, kad konfigurējat preces pārdošanas piedāvājumam, pirkšanas pasūtījumam vai ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="965fe-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="965fe-108">Var izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus, atkarībā no tā, kā vēlaties veidot ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="965fe-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="965fe-109">Ierobežojumus izmanto, lai kontrolētu atribūta vērtības, ko var atlasīt, konfigurējot preces pārdošanas pasūtījumam, pārdošanas piedāvājumam, pirkšanas pasūtījumam vai ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="965fe-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="965fe-110">Var izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus, atkarībā no tā, kā vēlaties veidot ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="965fe-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="965fe-111">Kas ir izteiksmes ierobežojumi?</span><span class="sxs-lookup"><span data-stu-id="965fe-111">What are expression constraints?</span></span>
<span data-ttu-id="965fe-112">Izteiksmes ierobežojumus raksturo izteiksme, kas izmanto aritmētiskos un Būla operatorus un funkcijas.</span><span class="sxs-lookup"><span data-stu-id="965fe-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="965fe-113">Izteiksmes ierobežojums ir rakstīts noteiktai sastāvdaļai preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="965fe-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="965fe-114">To nevar izmantot atkārtoti vai koplietot ar citu sastāvdaļu.</span><span class="sxs-lookup"><span data-stu-id="965fe-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="965fe-115">Tomēr sastāvdaļās izteiksmes ierobežojumi var izveidot atsauci uz sastāvdaļās apakšsastāvdaļas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="965fe-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="965fe-116">Kas ir tabulas ierobežojumi?</span><span class="sxs-lookup"><span data-stu-id="965fe-116">What are table constraints?</span></span>
<span data-ttu-id="965fe-117">Tabulas ierobežojumi uzskaita vērtību kombinācijas, kas ir atļautas atribūtiem, konfigurējot preci.</span><span class="sxs-lookup"><span data-stu-id="965fe-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="965fe-118">Tabulas ierobežojuma definīcijas var izmantot apkopojoši.</span><span class="sxs-lookup"><span data-stu-id="965fe-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="965fe-119">Veidojot tabulas ierobežojumu sastāvdaļai preču konfigurācijas modelī, jūs izvēlaties tabulas ierobežojuma definīciju.</span><span class="sxs-lookup"><span data-stu-id="965fe-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="965fe-120">Lai izveidotu kombinācijas, kas ir pieļaujamas, jūs pievienojat specifisku sastāvdaļu atribūtus.</span><span class="sxs-lookup"><span data-stu-id="965fe-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="965fe-121">Katram atribūta veidam ir specifiska vērtība.</span><span class="sxs-lookup"><span data-stu-id="965fe-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="965fe-122">Tabulas ierobežojuma piemērs</span><span class="sxs-lookup"><span data-stu-id="965fe-122">Example of a table constraint</span></span>

<span data-ttu-id="965fe-123">Šajā piemērā parādīts, kā ierobežot skaļruņa konfigurāciju atbilstoši konkrētai korpusa apdarei un priekšdaļai.</span><span class="sxs-lookup"><span data-stu-id="965fe-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="965fe-124">Pirmā tabula parāda korpusa apdares un priekšdaļas veidus, kas parasti pieejami konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="965fe-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="965fe-125">Vērtības ir definētas atribūtu tipam **Korpusa apdare** un **Priekšējais režģis**.</span><span class="sxs-lookup"><span data-stu-id="965fe-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="965fe-126">Atribūta tips</span><span class="sxs-lookup"><span data-stu-id="965fe-126">Attribute type</span></span> | <span data-ttu-id="965fe-127">Vērtības</span><span class="sxs-lookup"><span data-stu-id="965fe-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="965fe-128">Korpusa apdare</span><span class="sxs-lookup"><span data-stu-id="965fe-128">Cabinet finish</span></span> | <span data-ttu-id="965fe-129">Melna, ozolkoka, rožkoka, balta</span><span class="sxs-lookup"><span data-stu-id="965fe-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="965fe-130">Priekšējais režģis</span><span class="sxs-lookup"><span data-stu-id="965fe-130">Front grill</span></span>    | <span data-ttu-id="965fe-131">Melns, metāla, balts</span><span class="sxs-lookup"><span data-stu-id="965fe-131">Black, Metal, White</span></span>         |

<span data-ttu-id="965fe-132">Nākamajā tabulā redzamas kombinācijas, ko definē tabulas ierobežojums **Krāsa un apdare**.</span><span class="sxs-lookup"><span data-stu-id="965fe-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="965fe-133">Izmantojot šo tabulas ierobežojumu, var konfigurēt skaļruni, kam ir ozolkoka apdare un melns režģis, rožkoka apdare un balts režģis utt.</span><span class="sxs-lookup"><span data-stu-id="965fe-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="965fe-134">Apdare</span><span class="sxs-lookup"><span data-stu-id="965fe-134">Finish</span></span>         | <span data-ttu-id="965fe-135">Režģis</span><span class="sxs-lookup"><span data-stu-id="965fe-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="965fe-136">Ozola</span><span class="sxs-lookup"><span data-stu-id="965fe-136">Oak</span></span>            | <span data-ttu-id="965fe-137">Melna</span><span class="sxs-lookup"><span data-stu-id="965fe-137">Black</span></span>                       |
| <span data-ttu-id="965fe-138">Rožkoka</span><span class="sxs-lookup"><span data-stu-id="965fe-138">Rosewood</span></span>       | <span data-ttu-id="965fe-139">Balta</span><span class="sxs-lookup"><span data-stu-id="965fe-139">White</span></span>                       |
| <span data-ttu-id="965fe-140">Balta</span><span class="sxs-lookup"><span data-stu-id="965fe-140">White</span></span>          | <span data-ttu-id="965fe-141">Melna</span><span class="sxs-lookup"><span data-stu-id="965fe-141">Black</span></span>                       |
| <span data-ttu-id="965fe-142">Balta</span><span class="sxs-lookup"><span data-stu-id="965fe-142">White</span></span>          | <span data-ttu-id="965fe-143">Balta</span><span class="sxs-lookup"><span data-stu-id="965fe-143">White</span></span>                       |
| <span data-ttu-id="965fe-144">Melna</span><span class="sxs-lookup"><span data-stu-id="965fe-144">Black</span></span>          | <span data-ttu-id="965fe-145">Melna</span><span class="sxs-lookup"><span data-stu-id="965fe-145">Black</span></span>                       |
| <span data-ttu-id="965fe-146">melna</span><span class="sxs-lookup"><span data-stu-id="965fe-146">Black</span></span>          | <span data-ttu-id="965fe-147">Metāla</span><span class="sxs-lookup"><span data-stu-id="965fe-147">Metal</span></span>                       | 

<span data-ttu-id="965fe-148">Jūs varat izveidot sistēmas definētus un lietotāja definētus tabulas ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="965fe-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="965fe-149">Plašāku informāciju skatiet sadaļā [Sistēmas definēti un lietotāja definēti tabulas ierobežojumi](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="965fe-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="965fe-150">Kāda sintakse ir jāizmanto, lai rakstītu ierobežojumus?</span><span class="sxs-lookup"><span data-stu-id="965fe-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="965fe-151">Rakstot ierobežojumus, jāizmanto optimizācijas modelēšanas valodas (OML) sintakse.</span><span class="sxs-lookup"><span data-stu-id="965fe-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="965fe-152">Ierobežojumu risināšanai sistēma izmanto Microsoft Solver Foundation ierobežojumu risinātāju.</span><span class="sxs-lookup"><span data-stu-id="965fe-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="965fe-153">Vai man izmantot izteiksmes ierobežojumus vai tabulas ierobežojumus?</span><span class="sxs-lookup"><span data-stu-id="965fe-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="965fe-154">Varat izmantot vai nu izteiksmes ierobežojumus vai tabulas ierobežojumus atkarībā no tā, kā vēlaties veidot ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="965fe-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="965fe-155">Tabulas ierobežojumu varat veidot kā matricu, savukārt izteiksmes ierobežojums ir individuāls paziņojums.</span><span class="sxs-lookup"><span data-stu-id="965fe-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="965fe-156">Konfigurējot preci, nav svarīgi, kāda veida ierobežojums tiek izmantots.</span><span class="sxs-lookup"><span data-stu-id="965fe-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="965fe-157">Šajā piemērā parādīta divu metožu atšķirība.</span><span class="sxs-lookup"><span data-stu-id="965fe-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="965fe-158">Ja konfigurējat preces, izmantojot turpmākos ierobežojumu iestatījumus, ir atļautas šādas kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="965fe-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="965fe-159">Produkts melnā krāsā, 30. vai 50. izmēra</span><span class="sxs-lookup"><span data-stu-id="965fe-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="965fe-160">Produkts sarkanā krāsā, 20. izmēra</span><span class="sxs-lookup"><span data-stu-id="965fe-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="965fe-161">Tabulas ierobežojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="965fe-161">Table constraint setup</span></span>

| <span data-ttu-id="965fe-162">Krāsa</span><span class="sxs-lookup"><span data-stu-id="965fe-162">Color</span></span> | <span data-ttu-id="965fe-163">Izmēri</span><span class="sxs-lookup"><span data-stu-id="965fe-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="965fe-164">Melna</span><span class="sxs-lookup"><span data-stu-id="965fe-164">Black</span></span> | <span data-ttu-id="965fe-165">30</span><span class="sxs-lookup"><span data-stu-id="965fe-165">30</span></span>   |
| <span data-ttu-id="965fe-166">Melna</span><span class="sxs-lookup"><span data-stu-id="965fe-166">Black</span></span> | <span data-ttu-id="965fe-167">50</span><span class="sxs-lookup"><span data-stu-id="965fe-167">50</span></span>   |
| <span data-ttu-id="965fe-168">Sarkana</span><span class="sxs-lookup"><span data-stu-id="965fe-168">Red</span></span>   | <span data-ttu-id="965fe-169">20.</span><span class="sxs-lookup"><span data-stu-id="965fe-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="965fe-170">Izteiksmes ierobežojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="965fe-170">Expression constraint setup</span></span>

<span data-ttu-id="965fe-171">(Krāsa == "Melna" un (izmērs == "30" | izmērs == "50")) | (krāsa == "Sarkana" un izmērs = "20")</span><span class="sxs-lookup"><span data-stu-id="965fe-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="965fe-172">Vai, rakstot izteiksmes ierobežojumus, lietot operatorus vai infiksālo pieraksti?</span><span class="sxs-lookup"><span data-stu-id="965fe-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="965fe-173">Izteiksmes ierobežojums var rakstīt, izmantojot vai nu pieejamos prefiksa operatorus, vai infiksālo pieraksti.</span><span class="sxs-lookup"><span data-stu-id="965fe-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="965fe-174">Operatoriem **Min**, **Max** un **Abs** nevar lietot infiksālo pieraksti.</span><span class="sxs-lookup"><span data-stu-id="965fe-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="965fe-175">Šie operatori iekļauti kā standarta operatori lielākajā daļā programmēšanas valodu.</span><span class="sxs-lookup"><span data-stu-id="965fe-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="965fe-176">Kādus operatorus un infiksālo pierakstus var lietot, rakstot izteiksmes ierobežojumus?</span><span class="sxs-lookup"><span data-stu-id="965fe-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="965fe-177">Tālāk esošajās tabulās uzskaitīti operatori un infiksālā pierakste, ko var lietot, rakstot izteiksmes ierobežojumu sastāvdaļai preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="965fe-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="965fe-178">Piemēri pirmajā tabulā parāda, kā rakstīt izteiksmi, izmantojot vai nu infiksālo pieraksti vai operatorus.</span><span class="sxs-lookup"><span data-stu-id="965fe-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="965fe-179">Operators</span><span class="sxs-lookup"><span data-stu-id="965fe-179">Operator</span></span></th>
<th><span data-ttu-id="965fe-180">Apraksts</span><span class="sxs-lookup"><span data-stu-id="965fe-180">Description</span></span></th>
<th><span data-ttu-id="965fe-181">Sintakse</span><span class="sxs-lookup"><span data-stu-id="965fe-181">Syntax</span></span></th>
<th><span data-ttu-id="965fe-182">Piemēri</span><span class="sxs-lookup"><span data-stu-id="965fe-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="965fe-183">Implies</span><span class="sxs-lookup"><span data-stu-id="965fe-183">Implies</span></span></td>
<td><span data-ttu-id="965fe-184">Tas ir patiess, ja pirmais nosacījums ir nepatiess, otrais nosacījums ir patiess vai abi.</span><span class="sxs-lookup"><span data-stu-id="965fe-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="965fe-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="965fe-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-186"><strong>Operators:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="965fe-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="965fe-187"><strong>Infiksālā pierakste:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="965fe-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="965fe-188">And</span><span class="sxs-lookup"><span data-stu-id="965fe-188">And</span></span></td>
<td><span data-ttu-id="965fe-189">Tas ir spēkā tikai tad, ja ir spēkā visi nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="965fe-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="965fe-190">Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Patiess</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="965fe-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="965fe-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-192"><strong>Operators:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="965fe-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="965fe-193"><strong>Infiksālā pierakste:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="965fe-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="965fe-194">Or</span><span class="sxs-lookup"><span data-stu-id="965fe-194">Or</span></span></td>
<td><span data-ttu-id="965fe-195">Tas ir patiess, ja jebkurš nosacījums ir patiess.</span><span class="sxs-lookup"><span data-stu-id="965fe-195">This is true if any condition is true.</span></span> <span data-ttu-id="965fe-196">Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Nepatiess</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="965fe-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="965fe-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-198"><strong>Operators:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="965fe-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="965fe-199"><strong>Infiksālā pierakste:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="965fe-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="965fe-200">Plus</span><span class="sxs-lookup"><span data-stu-id="965fe-200">Plus</span></span></td>
<td><span data-ttu-id="965fe-201">Tas summē nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="965fe-201">This sums its conditions.</span></span> <span data-ttu-id="965fe-202">Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="965fe-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="965fe-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-204"><strong>Operators:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="965fe-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="965fe-205"><strong>Infiksālā pierakste:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="965fe-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="965fe-206">Minus</span><span class="sxs-lookup"><span data-stu-id="965fe-206">Minus</span></span></td>
<td><span data-ttu-id="965fe-207">Tas noliedz savu argumentu.</span><span class="sxs-lookup"><span data-stu-id="965fe-207">This negates its argument.</span></span> <span data-ttu-id="965fe-208">Tam ir jābūt precīzi vienam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="965fe-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="965fe-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="965fe-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-210"><strong>Operators:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="965fe-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="965fe-211"><strong>Infiksālā pierakste:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="965fe-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="965fe-212">Abs</span><span class="sxs-lookup"><span data-stu-id="965fe-212">Abs</span></span></td>
<td><span data-ttu-id="965fe-213">Tas paņem absolūto nosacījuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="965fe-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="965fe-214">Tam ir jābūt precīzi vienam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="965fe-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="965fe-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="965fe-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="965fe-216"><strong>Operators:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="965fe-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="965fe-217">Times</span><span class="sxs-lookup"><span data-stu-id="965fe-217">Times</span></span></td>
<td><span data-ttu-id="965fe-218">Tas paņem preci no tā nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="965fe-218">This takes the product of its conditions.</span></span> <span data-ttu-id="965fe-219">Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="965fe-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="965fe-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-221"><strong>Operators:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="965fe-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="965fe-222"><strong>Infiksālā pierakste:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="965fe-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="965fe-223">Power</span><span class="sxs-lookup"><span data-stu-id="965fe-223">Power</span></span></td>
<td><span data-ttu-id="965fe-224">Tas paņem eksponenciāli.</span><span class="sxs-lookup"><span data-stu-id="965fe-224">This takes an exponential.</span></span> <span data-ttu-id="965fe-225">Tas piemēro kāpinājumu no labās uz kreiso pusi.</span><span class="sxs-lookup"><span data-stu-id="965fe-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="965fe-226">(Citiem vārdiem sakot, tas ir labēji asociatīvs.) Tāpēc izteiksme <strong>Power[a, b, c]</strong> ir vienāda ar izteiksmi <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="965fe-227"><strong>Power</strong> var lietot tikai tad, ja kāpinātājs ir pozitīva konstante.</span><span class="sxs-lookup"><span data-stu-id="965fe-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="965fe-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="965fe-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-229"><strong>Operators:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="965fe-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="965fe-230"><strong>Infiksālā pierakste:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="965fe-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="965fe-231">Max</span><span class="sxs-lookup"><span data-stu-id="965fe-231">Max</span></span></td>
<td><span data-ttu-id="965fe-232">Tas dod lielāko nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="965fe-232">This produces the largest condition.</span></span> <span data-ttu-id="965fe-233">Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Bezgalība</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="965fe-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="965fe-234">Max[args]</span></span></td>
<td><span data-ttu-id="965fe-235"><strong>Operators:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="965fe-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="965fe-236">Min</span><span class="sxs-lookup"><span data-stu-id="965fe-236">Min</span></span></td>
<td><span data-ttu-id="965fe-237">Tas dod mazāko nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="965fe-237">This produces the smallest condition.</span></span> <span data-ttu-id="965fe-238">Ja nosacījumu skaits ir 0 (nulle), tas veido <strong>Bezgalība</strong>.</span><span class="sxs-lookup"><span data-stu-id="965fe-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="965fe-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="965fe-239">Min[args]</span></span></td>
<td><span data-ttu-id="965fe-240"><strong>Operators:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="965fe-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="965fe-241">Not</span><span class="sxs-lookup"><span data-stu-id="965fe-241">Not</span></span></td>
<td><span data-ttu-id="965fe-242">Tas dod sava nosacījuma apgriezto loģiku.</span><span class="sxs-lookup"><span data-stu-id="965fe-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="965fe-243">Tam ir jābūt precīzi vienam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="965fe-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="965fe-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="965fe-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="965fe-245"><strong>Operators:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="965fe-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="965fe-246"><strong>Infiksālā pierakste:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="965fe-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="965fe-247">Piemēri nākamajā tabulā parada, kā rakstīt infiksālo pieraksti.</span><span class="sxs-lookup"><span data-stu-id="965fe-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="965fe-248">Infiksālā pierakste</span><span class="sxs-lookup"><span data-stu-id="965fe-248">Infix notation</span></span>   |                                          <span data-ttu-id="965fe-249">Apraksts</span><span class="sxs-lookup"><span data-stu-id="965fe-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="965fe-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="965fe-250">x + y + z</span></span>     |                                           <span data-ttu-id="965fe-251">Saskaitīšana</span><span class="sxs-lookup"><span data-stu-id="965fe-251">Addition</span></span>                                            |
|    <span data-ttu-id="965fe-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="965fe-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="965fe-253">Reizināšana</span><span class="sxs-lookup"><span data-stu-id="965fe-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="965fe-254">x - y</span><span class="sxs-lookup"><span data-stu-id="965fe-254">x - y</span></span>       | <span data-ttu-id="965fe-255">Binārā atņemšana tiek transformēta tāpat kā binārā saskaitīšana, ja ir negatīvā otrā vērtība.</span><span class="sxs-lookup"><span data-stu-id="965fe-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="965fe-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="965fe-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="965fe-257">Kāpinājums, kam ir labās puses asociācija</span><span class="sxs-lookup"><span data-stu-id="965fe-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="965fe-258">!x</span><span class="sxs-lookup"><span data-stu-id="965fe-258">!x</span></span>         |                                          <span data-ttu-id="965fe-259">Nav Būla</span><span class="sxs-lookup"><span data-stu-id="965fe-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="965fe-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="965fe-260">x -: y</span></span>       |                                      <span data-ttu-id="965fe-261">Būla saistība</span><span class="sxs-lookup"><span data-stu-id="965fe-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="965fe-262">k</span><span class="sxs-lookup"><span data-stu-id="965fe-262">x</span></span>         |                                               <span data-ttu-id="965fe-263">y</span><span class="sxs-lookup"><span data-stu-id="965fe-263">y</span></span>                                               |
|     <span data-ttu-id="965fe-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="965fe-264">x & y & z</span></span>     |                                          <span data-ttu-id="965fe-265">Būla un</span><span class="sxs-lookup"><span data-stu-id="965fe-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="965fe-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="965fe-266">x == y == z</span></span>    |                                           <span data-ttu-id="965fe-267">Vienādība</span><span class="sxs-lookup"><span data-stu-id="965fe-267">Equality</span></span>                                            |
|    <span data-ttu-id="965fe-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="965fe-268">x != y != z</span></span>    |                                           <span data-ttu-id="965fe-269">Noteikts</span><span class="sxs-lookup"><span data-stu-id="965fe-269">Distinct</span></span>                                            |
|  <span data-ttu-id="965fe-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="965fe-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="965fe-271">Mazāks nekā</span><span class="sxs-lookup"><span data-stu-id="965fe-271">Less than</span></span>                                           |
|  <span data-ttu-id="965fe-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="965fe-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="965fe-273">Lielāks nekā</span><span class="sxs-lookup"><span data-stu-id="965fe-273">Greater than</span></span>                                          |
| <span data-ttu-id="965fe-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="965fe-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="965fe-275">Mazāks vai vienāds ar</span><span class="sxs-lookup"><span data-stu-id="965fe-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="965fe-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="965fe-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="965fe-277">Lielāks vai vienāds ar</span><span class="sxs-lookup"><span data-stu-id="965fe-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="965fe-278">(x)</span><span class="sxs-lookup"><span data-stu-id="965fe-278">(x)</span></span>        |                           <span data-ttu-id="965fe-279">Iekavas ignorē noklusējuma prioritāti.</span><span class="sxs-lookup"><span data-stu-id="965fe-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="965fe-280">Kāpēc mani izteiksmes ierobežojumi nevalidējas pareizi?</span><span class="sxs-lookup"><span data-stu-id="965fe-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="965fe-281">Nevar izmantot rezervētus atslēgas vārdus kā risinātāja nosaukumus atribūtiem, sastāvdaļām vai apakšsastāvdaļām preces konfigurācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="965fe-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="965fe-282">Tālāk ir sniegts to rezervēto atslēgvārdu saraksts, kurus nevarat izmantot:</span><span class="sxs-lookup"><span data-stu-id="965fe-282">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="965fe-283">Ceiling</span><span class="sxs-lookup"><span data-stu-id="965fe-283">Ceiling</span></span>
-   <span data-ttu-id="965fe-284">Element</span><span class="sxs-lookup"><span data-stu-id="965fe-284">Element</span></span>
-   <span data-ttu-id="965fe-285">Equal</span><span class="sxs-lookup"><span data-stu-id="965fe-285">Equal</span></span>
-   <span data-ttu-id="965fe-286">Floor</span><span class="sxs-lookup"><span data-stu-id="965fe-286">Floor</span></span>
-   <span data-ttu-id="965fe-287">If</span><span class="sxs-lookup"><span data-stu-id="965fe-287">If</span></span>
-   <span data-ttu-id="965fe-288">Less</span><span class="sxs-lookup"><span data-stu-id="965fe-288">Less</span></span>
-   <span data-ttu-id="965fe-289">Greater</span><span class="sxs-lookup"><span data-stu-id="965fe-289">Greater</span></span>
-   <span data-ttu-id="965fe-290">Implies</span><span class="sxs-lookup"><span data-stu-id="965fe-290">Implies</span></span>
-   <span data-ttu-id="965fe-291">Darbu izpildes žurnāls</span><span class="sxs-lookup"><span data-stu-id="965fe-291">Log</span></span>
-   <span data-ttu-id="965fe-292">Maks.</span><span class="sxs-lookup"><span data-stu-id="965fe-292">Max</span></span>
-   <span data-ttu-id="965fe-293">Min</span><span class="sxs-lookup"><span data-stu-id="965fe-293">Min</span></span>
-   <span data-ttu-id="965fe-294">Mīnus</span><span class="sxs-lookup"><span data-stu-id="965fe-294">Minus</span></span>
-   <span data-ttu-id="965fe-295">Plus</span><span class="sxs-lookup"><span data-stu-id="965fe-295">Plus</span></span>
-   <span data-ttu-id="965fe-296">Jauda</span><span class="sxs-lookup"><span data-stu-id="965fe-296">Power</span></span>
-   <span data-ttu-id="965fe-297">Laiki</span><span class="sxs-lookup"><span data-stu-id="965fe-297">Times</span></span>
-   <span data-ttu-id="965fe-298">Slots</span><span class="sxs-lookup"><span data-stu-id="965fe-298">Slot</span></span>
-   <span data-ttu-id="965fe-299">Modelis</span><span class="sxs-lookup"><span data-stu-id="965fe-299">Model</span></span>
-   <span data-ttu-id="965fe-300">Lēmums</span><span class="sxs-lookup"><span data-stu-id="965fe-300">Decision</span></span>
-   <span data-ttu-id="965fe-301">Mērķis</span><span class="sxs-lookup"><span data-stu-id="965fe-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="965fe-302">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="965fe-302">Additional resources</span></span>
--------

[<span data-ttu-id="965fe-303">Izteiksmes ierobežojuma izveide</span><span class="sxs-lookup"><span data-stu-id="965fe-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="965fe-304">Aprēķina pievienošana preces konfigurācijas modelim</span><span class="sxs-lookup"><span data-stu-id="965fe-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]