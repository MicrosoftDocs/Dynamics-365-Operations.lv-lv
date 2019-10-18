---
title: Fantoma krājumi
description: Šajā tēmā ir detalizēti aprakstīts, kā rindas tipu Fantoms var izmantot materiālu komplekta (MK) un formulas rindām programmā Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7c39b0ac2eb8a2293c828fee23ed6a78cb5fe2c9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250017"
---
# <a name="phantom-items"></a><span data-ttu-id="ac66f-103">Fantoma krājumi</span><span class="sxs-lookup"><span data-stu-id="ac66f-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac66f-104">Šajā sadaļā ir sniegta detalizēta informācija par to, kā fantoma rindas veidu var izmantot materiālu komplektu (MK) un formulas rindām.</span><span class="sxs-lookup"><span data-stu-id="ac66f-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="ac66f-105">Nākamajā attēlā (a) ir preces H un daļu F un G MK un (b) ir preces H un daļas F maršruta lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Prece H un daļa F](media/product-H-part-F.png)


<span data-ttu-id="ac66f-107">Šajā attēlā ir redzams MK struktūras divos līmeņos piemērs.</span><span class="sxs-lookup"><span data-stu-id="ac66f-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="ac66f-108">Pabeigtā prece H pārstāv iekārtas montāžai paredzētu preci.</span><span class="sxs-lookup"><span data-stu-id="ac66f-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="ac66f-109">Iekārtas montāža ietver divas daļas, elektroiekārtu (F), kas ietver divus materiālus (A un B), un iepakojuma materiālu grupu (G), kas arī ietver divus materiālus (C un D).</span><span class="sxs-lookup"><span data-stu-id="ac66f-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="ac66f-110">Iekārtas vispārējas montāžās laikā tiek izmantots cits materiāls (E).</span><span class="sxs-lookup"><span data-stu-id="ac66f-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Prece H un daļa F](media/product-H-part-B.png)

<span data-ttu-id="ac66f-112">Iepriekšējā attēlā ir redzams preces H konstruēšanas MK. Šī struktūra sniedz labu pārskatu par vispārējās iekārtas montāžas daļām un komponentiem.</span><span class="sxs-lookup"><span data-stu-id="ac66f-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="ac66f-113">Taču, lai gan preces izstrādātāji varētu vēlēties, lai MK tiek parādīts šādā veidā, šī struktūra var pareizi neatspoguļot viedu, kādā iekārta tiek būvēta ražošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="ac66f-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="ac66f-114">Piemēram, konstruēšanas MK iepriekšējā attēlā norāda, ka elektroiekārta F tiek montēta kā atsevišķa daļa pēc atsevišķa darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="ac66f-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="ac66f-115">Tomēr ražotnē var novērtēt labāk, ka elektroiekārtas montāža tiek veikta vispārējā iekārtas montāžas ietvaros, nevis kā atsevišķa darba pasūtījuma izpilde.</span><span class="sxs-lookup"><span data-stu-id="ac66f-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="ac66f-116">Šo konstruēšanas MK arī norāda, ka daļa G ir atsevišķa daļa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="ac66f-117">Tomēr šajā struktūrā daļa G nepārstāv fizisko daļu, bet iepakojuma materiālu komplektu.</span><span class="sxs-lookup"><span data-stu-id="ac66f-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="ac66f-118">Tāpēc, lai gan konstruēšanas MK nodrošina preces konstrukcijas un šīs konstrukcijas uzturēšanas lielu vērtību, tas var nebūt loģiskākais veids, kā atbalstīt preces ražošanas izpildes procesu.</span><span class="sxs-lookup"><span data-stu-id="ac66f-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="ac66f-119">Turpretim konstruēšanas MK ir labākais veids, kā veidot preci.</span><span class="sxs-lookup"><span data-stu-id="ac66f-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="ac66f-120">Nākamajā attēlā ir parādīts, kā iepriekšējais konstruēšanas MK tiek pārvērsts par ražošanas MK.</span><span class="sxs-lookup"><span data-stu-id="ac66f-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="ac66f-121">Šajā attēlā (a) ir preces H MK un b ir preces H maršruta lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="ac66f-122">Šajā struktūrā var redzēt, ka nav nekas norādīts par daļu F un G, un materiāli, kurus ietver šīs daļas, ir pārnesti uz nākamo MK līmeni.</span><span class="sxs-lookup"><span data-stu-id="ac66f-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="ac66f-123">Atšķirībā no konstruēšanas MK, kurā bija divas operāciju lapas, ražošanas MK ir tikai viena operāciju lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="ac66f-124">Iepakojuma operācija, kas ir saistīta ar daļu G, arī ir pārnesta, un tā tagad ir preces H operācijas lapas daļa. Elektroierīces montāža ir pirmajā operācija.</span><span class="sxs-lookup"><span data-stu-id="ac66f-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="ac66f-125">Šai secībai ir jēga, jo šī ierīce tiek izmantota nākamajā darbībā, kas ir iekārtas montāža.</span><span class="sxs-lookup"><span data-stu-id="ac66f-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="ac66f-126">Pēdējā operācija ir iepakošanas darbība, kurā tiek izmantoti divi iepakojuma materiāli (C un D).</span><span class="sxs-lookup"><span data-stu-id="ac66f-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="ac66f-127">Pāreja no konstruēšanas MK uz ražošanas MK ir tiek nodrošināta, izmantojot MK rindas tipu Fantoms.</span><span class="sxs-lookup"><span data-stu-id="ac66f-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="ac66f-128">Kā jau termins “fantoms” norāda, pārejas starp abiem MK viediem laikā daļa F un G ir pazudusi.</span><span class="sxs-lookup"><span data-stu-id="ac66f-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="ac66f-129">Šajā piemērā fantoma rindas veids tiek lietots daļas F un G MK rindās konstruēšanas MK.</span><span class="sxs-lookup"><span data-stu-id="ac66f-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="ac66f-130">Izveidojot ražošanas vai partijas pasūtījumu, konstruēšanas MK tiek kopēts ražošanas vai partijas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="ac66f-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="ac66f-131">Pēc tam, novērtējot pasūtījumu, rodas pāreja no konstruēšanas MK uz ražošanas MK, kā parādīts iepriekšējos attēlos.</span><span class="sxs-lookup"><span data-stu-id="ac66f-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="ac66f-132">Saskaņā ar operācijas lapu otrajā attēlā iepakojuma materiāls C un D tiek ievadīts operācijai.</span><span class="sxs-lookup"><span data-stu-id="ac66f-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="ac66f-133">Daudzlīmeņu fantoma MK struktūras</span><span class="sxs-lookup"><span data-stu-id="ac66f-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="ac66f-134">Fantoma rindas veidu var izmantot daudzlīmeņu MK struktūrās, kā parādīts nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="ac66f-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="ac66f-135">Šajā attēlā (a) ir preces G MK un (b) ir daļas E un F un preces G maršruta lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Prece G un daļa F ar maršruta lapām](media/product-G-route-sheet-G.png)


<span data-ttu-id="ac66f-137">Nākamajā attēlā ir parādīts galīgais ražošanas MK un maršruta lapa, ja daļas E un F MK rindas ir konfigurētas tā, lai rindas veids ir fantoms.</span><span class="sxs-lookup"><span data-stu-id="ac66f-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="ac66f-138">Šajā attēlā (a) ir preces G MK un (b) ir preces G maršruta lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Prece G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="ac66f-140">Fantoms un maršruta tīkls</span><span class="sxs-lookup"><span data-stu-id="ac66f-140">Phantom and route network</span></span>
<span data-ttu-id="ac66f-141">Fantoma MK var izmantot arī MK, kam ir maršruta tīkls.</span><span class="sxs-lookup"><span data-stu-id="ac66f-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="ac66f-142">Maršruta tīklā viena vai vairākas operācijas tiek veiktas paralēli.</span><span class="sxs-lookup"><span data-stu-id="ac66f-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="ac66f-143">Nākamajā attēlā ir parādīts tāda maršruta tīkla piemērs, kas tiek izmantots daudzlīmeņu MK.</span><span class="sxs-lookup"><span data-stu-id="ac66f-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="ac66f-144">Šajā attēlā (a) ir preces G un daļas F MK un (b) ir preces G un daļas F, kam ir maršruta tīkls, maršruta lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Prece G un daļa F](media/product-G-part-F.png)


<span data-ttu-id="ac66f-146">Nākamajā attēlā (a) ir preces G un daļas F MK un (b) ir preces G un daļas F maršruta lapa.</span><span class="sxs-lookup"><span data-stu-id="ac66f-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Prece G un daļa F ar maršruta lapām](media/product-G-part-F-with-route-sheet.png)
