---
title: Pirkšanas ierobežojumu izveide
description: Šajā tēmā ir parādīts, kā izveidot pirkšanas politikas, lai tās atbilstu jūsu biznesa pirkšanas procesiem.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4ba2a23f84972391283eaf01cef70a161c75226
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383177"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="f8a20-103">Pirkšanas ierobežojumu izveide</span><span class="sxs-lookup"><span data-stu-id="f8a20-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8a20-104">Šajā tēmā ir parādīts, kā izveidot pirkšanas politikas, lai tās atbilstu jūsu biznesa pirkšanas procesiem.</span><span class="sxs-lookup"><span data-stu-id="f8a20-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="f8a20-105">Lai varētu izveidot pirkšanas politikas, ir jāiestata pirkšanas politikas parametri.</span><span class="sxs-lookup"><span data-stu-id="f8a20-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="f8a20-106">Pirkšanas politiku var izveidot, modificēt un noņemt, bet pirkšanas politiku nevar dzēst.</span><span class="sxs-lookup"><span data-stu-id="f8a20-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="f8a20-107">Šo procedūru parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="f8a20-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="f8a20-108">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="f8a20-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="f8a20-109">Iestatīt politikas parametrus</span><span class="sxs-lookup"><span data-stu-id="f8a20-109">Set up policy parameters</span></span>
1. <span data-ttu-id="f8a20-110">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="f8a20-111">Darbību rūtī atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-111">On the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="f8a20-112">Politikas prioritātes kārtulas attiecas uz dažādiem līmeņiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="f8a20-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="f8a20-113">Rādītās organizācijas vienības ir atkarīgas no jūsu organizācijas hierarhijas, kā arī no tā, kuros hierarhijas līmeņos ir piešķirts sagādes iekšējās kontroles mērķis.</span><span class="sxs-lookup"><span data-stu-id="f8a20-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="f8a20-114">Piemēram, jūsu organizācijā var būt juridiskās personas, izmaksu centri, reģioni un departamenti, bet ir iespējams, ka tikai dažiem no tiem ir sagādes iekšējās kontroles hierarhijas mērķis.</span><span class="sxs-lookup"><span data-stu-id="f8a20-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="f8a20-115">Pēc noklusējuma ir pieejama organizācija ar tipu Uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="f8a20-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="f8a20-116">Atlasiet cilni **Politikas kārtulas tipu parametri**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="f8a20-117">Koka struktūrā dodieties uz **Pirkšanas politika > Pirkšanas pieprasījuma kontroles kārtula**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="f8a20-118">Jūs definējat ierobežojumu piemērošanas prioritāšu secību ierobežojumu līmenī.</span><span class="sxs-lookup"><span data-stu-id="f8a20-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="f8a20-119">Tomēr dažiem ierobežojumu veidiem var ignorēt atsevišķu ierobežojumu kārtulu tipu prioritāšu secību.</span><span class="sxs-lookup"><span data-stu-id="f8a20-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="f8a20-120">Piemēram, pirkšanas politikām varat definēt šādu prioritāšu secību: izmaksu centrs, departaments, uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="f8a20-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="f8a20-121">Kataloga politikas kārtulai, iespējams, vēlaties šādu prioritāšu secību: departaments, izmaksu centrs, uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="f8a20-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="f8a20-122">Kataloga politikas kārtulai varat mainīt prioritāšu secību.</span><span class="sxs-lookup"><span data-stu-id="f8a20-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="f8a20-123">Kad kāds nodarbinātais izveido pieprasījumu, tad rādītais katalogs ir atkarīgs no politikām, kas ir saistītas ar šī nodarbinātā departamentu, pēc tam — viņa izmaksu centru, un pēc tam — viņa uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="f8a20-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="f8a20-124">Ja ir uzskaitīti vairāki organizācijas līmeņi, varat lietot augšupvērsto/lejupvērsto bultiņu, lai iestatītu pirkšanas pieprasījuma kontroles kārtulas prioritāšu secību.</span><span class="sxs-lookup"><span data-stu-id="f8a20-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="f8a20-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f8a20-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="f8a20-126">Izveidot jaunu politiku</span><span class="sxs-lookup"><span data-stu-id="f8a20-126">Create a new policy</span></span>
1. <span data-ttu-id="f8a20-127">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-127">Select **New**.</span></span>
2. <span data-ttu-id="f8a20-128">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f8a20-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="f8a20-129">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f8a20-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="f8a20-130">Viena pirkšanas politika var attiekties tikai uz vienu organizācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="f8a20-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="f8a20-131">Piemēram, jums varētu būt viena hierarhija ar nosaukumu “Ģeogrāfisks” un viena ar nosaukumu “Departaments”, un katrai no tām var būt citāda pirkšanas politika.</span><span class="sxs-lookup"><span data-stu-id="f8a20-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="f8a20-132">Atlasiet organizāciju, kam ir jālieto šī politika.</span><span class="sxs-lookup"><span data-stu-id="f8a20-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="f8a20-133">Atlasiet bultiņu, lai pievienotu atlasīto organizāciju.</span><span class="sxs-lookup"><span data-stu-id="f8a20-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="f8a20-134">Varat atkārtot šo procesu, lai pievienotu vairāk organizāciju.</span><span class="sxs-lookup"><span data-stu-id="f8a20-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="f8a20-135">Pievienot politikas kārtulu</span><span class="sxs-lookup"><span data-stu-id="f8a20-135">Add a policy rule</span></span>
1. <span data-ttu-id="f8a20-136">Sarakstā **Politikas kārtulu tips** atlasiet **Pieprasījuma mērķa kārtula**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="f8a20-137">Jūs izveidosiet kārtulu, kas noklusējuma pieprasījuma mērķi iestata uz tipu Patēriņš, bet ļauj tā vietā atlasīt tipu Papildināšana.</span><span class="sxs-lookup"><span data-stu-id="f8a20-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="f8a20-138">Atlasiet **Izveidot ierobežojuma nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="f8a20-139">Atlasiet **Jā** laukā **Atļaut manuālo ignorēšanu**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="f8a20-140">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="f8a20-140">Select **Close**.</span></span>
- <span data-ttu-id="f8a20-141">Tagad pirkšanas politikai varat iestatīt citas politikas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="f8a20-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="f8a20-142">Ņemiet vērā, ka tipā Politikas kārtula nevar būt kārtulu, kuras pārklājas un kuras vienlaicīgi ir aktīvas vienā un tajā pašā sagādes politikā.</span><span class="sxs-lookup"><span data-stu-id="f8a20-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  

