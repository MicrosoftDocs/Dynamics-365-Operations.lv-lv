---
title: "Preces dzīves cikla stāvoklis"
description: "Preces dzīves cikla stāvoklis dokumentē izlaistās preces vai preces varianta dzīves cikla stāvokli."
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8337f1dfb938f9fa69924e77a25a68ee56dbd2ac
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="8e1c6-103">Preces dzīves cikla stāvoklis</span><span class="sxs-lookup"><span data-stu-id="8e1c6-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8e1c6-104">Preces dzīves cikla stāvoklis dokumentē izlaistās preces vai preces varianta dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="8e1c6-105">Preces dzīves cikla stāvokļus definē lietotājs — parasti tas ir produktu menedžeris vai preces pamatdatu pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="8e1c6-106">Īpašus biznesa procesus, piemēram, vispārējo plānošanu, var ietekmēt noteikts dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="8e1c6-107">Izlaista prece vai preces variants var būt saistīts ar preces dzīves cikla stāvokli, kurš dokumentē, kādā dzīves cikla stāvoklī konkrētā prece vai variants atrodas pašlaik.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="8e1c6-108">Varat definēt neierobežotu skaitu preces dzīves cikla stāvokļu, piešķirot stāvokļa nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="8e1c6-109">Jaunajām izlaistajām precēm varat atlasīt vienu dzīves cikla stāvokli kā noklusējuma stāvokli.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="8e1c6-110">Izlaistie preces varianti izveidošanas laikā savu preces dzīves cikla stāvokli pārmanto no to izlaistās preces šablona.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="8e1c6-111">Mainot dzīves cikla stāvokli kādam izlaistas preces šablonam, varat izvēlēties atjaunināt visus esošos variantus, kuriem ir tāds pats sākotnējais stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="8e1c6-112">Jauna preces dzīves cikla stāvokļa izveidošana</span><span class="sxs-lookup"><span data-stu-id="8e1c6-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="8e1c6-113">Lai izveidotu jaunu preces dzīves cikla stāvokli, atskaņojiet vai izlasiet uzdevuma ceļvedi **Jauna preces dzīves cikla stāvokļa izveidošana**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="8e1c6-114">Lai izveidotu noklusējuma preces dzīves cikla stāvokli, atskaņojiet vai izlasiet uzdevuma ceļvedi **Noklusējuma preces dzīves cikla stāvokļa izveidošana**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="8e1c6-115">Preces dzīves cikla stāvokļu saistīšana ar izlaistajām precēm</span><span class="sxs-lookup"><span data-stu-id="8e1c6-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="8e1c6-116">Pastāv vairāki veidi, kā preces dzīves cikla stāvokļus saistīt ar izlaistajām precēm vai preces variantiem.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="8e1c6-117">Izveidojot jaunu izlaisto preci, automātiski tiek piešķirts noklusējuma **Preces dzīves cikla stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="8e1c6-118">Izlaižot preci kādai juridiskajai personai, automātiski tiek piešķirts noklusējuma **Preces dzīves cikla stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="8e1c6-119">Preces variantu izlaižot kādai juridiskajai personai, ar izlaistās preces šablonu saistītais **Preces dzīves cikla stāvoklis** šajā juridiskajā personā tiek automātiski piešķirts jaunajam variantam.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="8e1c6-120">Preces dzīves cikla stāvokli varat atjaunināt manuāli, izmantojot tālāk norādītos vienumus.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="8e1c6-121">Saraksta lapa **Izlaistās preces** vai **Detalizēts skats**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="8e1c6-122">Saraksta lapa **Izlaistie preces varianti** vai **Detalizēts skats**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="8e1c6-123">Atrodiet novecojušās preces vai preces variantus, pamatojoties uz pieprasījumu, un piesaistiet dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="8e1c6-124">Lai iegūtu detalizētu informāciju par to, kā piesaistīt preces dzīves cikla stāvokļus, atskaņojiet vai izlasiet divus tālāk norādītos uzdevuma ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="8e1c6-125">Lai preces dzīves cikla stāvokli piesaistītu izlaistas preces šablonam, atskaņojiet vai izlasiet uzdevuma ceļvedi **Preces dzīves cikla stāvokļa saistīšana ar izlaistas preces šablonu**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="8e1c6-126">Lai preces dzīves cikla stāvokli piesaistītu izlaistai precei, atskaņojiet vai izlasiet uzdevuma ceļvedi **Preces dzīves cikla stāvokļa saistīšana ar izlaistu preci**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="8e1c6-127">Ietekme uz vispārējo plānošanu</span><span class="sxs-lookup"><span data-stu-id="8e1c6-127">Impact on master planning</span></span> 

<span data-ttu-id="8e1c6-128">Preces dzīves cikla stāvoklim ir tikai viens kontroles karodziņš: **Ir aktīvs plānošanai**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="8e1c6-129">Pēc noklusējuma tas ir iestatīts uz **Jā** visiem izveidotajiem preces dzīves cikla stāvokļiem, bet to var mainīt uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="8e1c6-130">Ja tas ir iestatīts uz **Nē**, saistītās izlaistās preces vai izlaistie preču varianti ir:</span><span class="sxs-lookup"><span data-stu-id="8e1c6-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="8e1c6-131">Izslēgts no vispārējās plānošanas.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="8e1c6-132">Izslēgts no MK līmeņa aprēķina.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="8e1c6-133">Lai iegūtu detalizētu informāciju par to, kā lietot preces dzīves cikla stāvokli, lai preces izslēgtu no vispārējās plānošanas un MK līmeņa aprēķina, atskaņojiet vai izlasiet uzdevuma ceļvedi **Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="8e1c6-134">Veiktspējas apsvērumu dēļ ir ļoti ieteicams visas novecojušās izlaistās preces vai preces variantus — it īpaši, ja strādājat ar preces konfigurācijas variantiem, kas nav lietojami atkārtoti — saistīt ar preces dzīves cikla stāvokli, kas ir deaktivizēts vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="8e1c6-135">Noklusējuma migrēšana, importēšana un eksportēšana</span><span class="sxs-lookup"><span data-stu-id="8e1c6-135">Default migration, import, and export</span></span> 

<span data-ttu-id="8e1c6-136">Preces dzīves cikla stāvokļi netiek atbalstīti datu elementos, un dzīves cikla stāvokli nevar iestatīt uz mainīgu stāvokli, izmantojot izlaistas preces datu elementus.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="8e1c6-137">Veicot migrēšanu no iepriekšējiem laidieniem, visu preču un preču variantu dzīves cikla stāvoklis ir tukšs.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="8e1c6-138">Importējot izlaistās preces, izmantojot kādu datu elementu, izveidošanas laikā tiek lietots noklusējuma dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="8e1c6-139">Importējot izlaisto preču variantus, izmantojot kādu datu elementu, tiek importēts izlaistās preces šablona preces dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="8e1c6-140">Novecojušu preču un preces variantu atrašana</span><span class="sxs-lookup"><span data-stu-id="8e1c6-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="8e1c6-141">Varat palaist simulācijas analīzi, lai atrastu novecojušas izlaistās preces vai preču variantus, un pēc tam atjaunināt to preces dzīves cikla statusu.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="8e1c6-142">Lai atrastu novecojušas preces, atskaņojiet un uzlasiet uzdevuma ceļvedi **Novecojušu preces variantu atrašana un preces dzīves cikla stāvokļa piešķiršana**.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="8e1c6-143">Šajā uzdevuma ceļvedī ir parādīts, kā atrast novecojušas izlaistās preces vai preces variantus, un kā preces dzīves cikla stāvokli saistīt ar novecojušām precēm.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="8e1c6-144">Tajā ir arī parādīts, kā skatīt simulācijas rezultātus un novērtēt, cik preču un preces variantu tiks saistīti ar jaunu preces dzīves cikla stāvokli, izpildot atjauninājumu bez simulācijas.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="8e1c6-145">Izpildot analīzi simulācijas režīmā, preces un preču varianti, kas identificēti kā novecojuši, tiek parādīti īpašā veidlapā, kur tos var vienkārši pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="8e1c6-146">Analīze meklē transakcijas un īpašus pamatdatus, lai identificētu preces, kurām nav pieprasījuma mainīgā periodā un nav pamatdatu, kas varētu radīt pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="8e1c6-147">Jaunās izlaistās preces mainīgā periodā var izslēgt no analīzes.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="8e1c6-148">Ja analīzes simulācija atgriež prognozētos rezultātus, lietotājs var palaist analīzi un iestatīt jaunu preces dzīves cikla stāvokli visām precēm, ko analīze identificējusi kā novecojušas.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="8e1c6-149">Ņemiet vērā, ka visas analīzes un atjauninājumi ir jāizpilda tajā pašā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="8e1c6-150">Izlaisto preču vai preču variantu atlasīšanas un atjaunināšanas kritēriji</span><span class="sxs-lookup"><span data-stu-id="8e1c6-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="8e1c6-151">Lai atlasītu un atjauninātu izlaistās preces un preču variantus, izmantojiet tālāk norādītos kritērijus.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="8e1c6-152">Preces vai preces varianta preces dzīves cikla stāvoklim ir jāatšķiras no jaunā vēlamā stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="8e1c6-153">Prece vai preces variants tika izveidots pirms dažām dienām, ņemot vērā atlases dialoglodziņā ievadīto dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="8e1c6-154">Šai precei vai preces variantam nav atvērtu ražošanas pasūtījumu (= statuss < beidzies).</span><span class="sxs-lookup"><span data-stu-id="8e1c6-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="8e1c6-155">Šai precei vai preces variantam nav atvērtu krājumu transakciju (= statuss izejas plūsma no ReservPhysical uz QuotationIssue vai status ieejas plūsma no Registrered uz QuotationReceipt).</span><span class="sxs-lookup"><span data-stu-id="8e1c6-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="8e1c6-156">Šai precei vai preces variantam nav krājumu transakciju noteiktā iepriekšējo dienu skaita periodā.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="8e1c6-157">Šai precei vai preces variantam nav nākotnes pieprasījuma vai piedāvājuma apjoma prognozes.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="8e1c6-158">Šai precei vai preces variantam krājumu vajadzībā nav iestatīts minimālais krājumu līmenis.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="8e1c6-159">Šai precei vai preces variantam nav aktīvu fiksēta daudzuma Kanban nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="8e1c6-160">Šai precei vai preces variantam nav pakalpojuma pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="8e1c6-161">Šai precei vai preces variantam nav aktīvu vai nākotnes pārdošanas vai pirkšanas līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="8e1c6-162">Šī prece vai preces variants netiek lietots tādā MK, kurš ir piesaistīts plānošanai aktīvas preces vai varianta apstiprinātai MK versijai, kurai nav beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e1c6-163">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="8e1c6-163">Related topics</span></span>

-  <span data-ttu-id="8e1c6-164">Jauna preces dzīves cikla stāvokļa izveidošana</span><span class="sxs-lookup"><span data-stu-id="8e1c6-164">Create a new product lifecycle state</span></span>
-  <span data-ttu-id="8e1c6-165">Jauna noklusējuma preces dzīves cikla stāvokļa izveidošana</span><span class="sxs-lookup"><span data-stu-id="8e1c6-165">Create a default new product lifecycle state</span></span>
-  <span data-ttu-id="8e1c6-166">Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam</span><span class="sxs-lookup"><span data-stu-id="8e1c6-166">Assign a product lifecycle state to a released product master</span></span>
-  <span data-ttu-id="8e1c6-167">Preces dzīves cikla stāvokļa piešķiršana izlaistai precei</span><span class="sxs-lookup"><span data-stu-id="8e1c6-167">Assign a product lifecycle state to a released product</span></span>
-  <span data-ttu-id="8e1c6-168">Novecojušu preču variantu atrašana un preces dzīves cikla stāvokļa piešķiršana</span><span class="sxs-lookup"><span data-stu-id="8e1c6-168">Find obsolete product variants and assign a product lifecycle state</span></span>
-  <span data-ttu-id="8e1c6-169">Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas</span><span class="sxs-lookup"><span data-stu-id="8e1c6-169">Create a product lifecycle state to exclude products from Master planning</span></span>

