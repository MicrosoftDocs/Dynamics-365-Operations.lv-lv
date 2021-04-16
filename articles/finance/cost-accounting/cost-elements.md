---
title: Izmaksu elementu dimensijas
description: Kā viens no pamatelementiem Izmaksu uzskaitē, izmaksu elementa dimensijas tiek izmantotas, lai sadalītu kategorijās un izsekotu, uz kurieni plūst izmaksas.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 067d7035cdb9c8f4bcb2bdac9cf0a33cd4e01079
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811441"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="77c93-103">Izmaksu elementu dimensijas</span><span class="sxs-lookup"><span data-stu-id="77c93-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77c93-104">Kā viens no pamatelementiem Izmaksu uzskaitē, izmaksu elementa dimensijas tiek izmantotas, lai sadalītu kategorijās un izsekotu, uz kurieni plūst izmaksas.</span><span class="sxs-lookup"><span data-stu-id="77c93-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="77c93-105">Izmaksu elements atbilst izmaksu atbilstošajam krājumam kontu plānā.</span><span class="sxs-lookup"><span data-stu-id="77c93-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="77c93-106">Būtībā tas var būt jebkura veida elements, kam ir zemākais līmenis uzņēmumā, kur var plūst izmaksas.</span><span class="sxs-lookup"><span data-stu-id="77c93-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="77c93-107">Izmaksu elementi kā koncepcijas diapazons no virsgrāmatas kontiem uz visiem izmaksu atbilstošajiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="77c93-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="77c93-108">Pašlaik Izmaksu uzskaite atbalsta virsgrāmatas kontus.</span><span class="sxs-lookup"><span data-stu-id="77c93-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="77c93-109">Divu veidu izmaksu elementi</span><span class="sxs-lookup"><span data-stu-id="77c93-109">Two types of cost elements</span></span>
<span data-ttu-id="77c93-110">Ir divu veidu izmaksu elementi: primāro izmaksu elementi un sekundāro izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="77c93-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="77c93-111">Šajā tabulā ir parādīta atšķirība starp abiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="77c93-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77c93-112"><strong>Primāro izmaksu elementi</strong></span><span class="sxs-lookup"><span data-stu-id="77c93-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="77c93-113"><strong>Sekundāro izmaksu elementi</strong></span><span class="sxs-lookup"><span data-stu-id="77c93-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77c93-114">Primāro izmaksu elementi pārstāv izmaksu plūsmu no finanšu uzskaites uz izmaksu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="77c93-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="77c93-115">Izmaksu elementu struktūra atbilst peļņas un zaudējumu konta struktūrai virsgrāmatā, kur izmaksu elements var atbilst galvenajam kontam.</span><span class="sxs-lookup"><span data-stu-id="77c93-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="77c93-116">Ne visi galvenie konti vienmēr var tikt pārstāvēti kā izmaksu elementi atkarībā no biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="77c93-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="77c93-117">Primāro izmaksu elementu piemēri:</span><span class="sxs-lookup"><span data-stu-id="77c93-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="77c93-118">Pārdoto preču pašizmaksa</span><span class="sxs-lookup"><span data-stu-id="77c93-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="77c93-119">Netiešās materiālu izmaksas</span><span class="sxs-lookup"><span data-stu-id="77c93-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="77c93-120">Personāla izmaksas</span><span class="sxs-lookup"><span data-stu-id="77c93-120">Personnel costs</span></span></li>
<li><span data-ttu-id="77c93-121">Enerģijas izmaksas</span><span class="sxs-lookup"><span data-stu-id="77c93-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="77c93-122">Sekundāro izmaksu elementi, kas pārstāv plūsmas izmaksas iekšēji, jo šīs izmaksas tiek izveidotas un izmantotas tikai Izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="77c93-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="77c93-123">Tās tiek izmantotas, lai nodrošinātu, ka izmaksu avotu var izsekot.</span><span class="sxs-lookup"><span data-stu-id="77c93-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="77c93-124">Šos izmaksu elementus izmanto izmaksu sadalījumos un pieskaitāmo izmaksu aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="77c93-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="77c93-125">Sekundāro izmaksu elementu piemēri:</span><span class="sxs-lookup"><span data-stu-id="77c93-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="77c93-126">Ražošanas izmaksas</span><span class="sxs-lookup"><span data-stu-id="77c93-126">Production costs</span></span></li>
<li><span data-ttu-id="77c93-127">Ražošanas, materiālu un mārketinga pieskaitāmās izmaksas</span><span class="sxs-lookup"><span data-stu-id="77c93-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="77c93-128">Izmaksu elementu dimensijas un izmaksu elementu dimensijas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="77c93-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="77c93-129">Izmaksu elementi, kas tiek saukti par *izmaksu elementu dimensijas*.</span><span class="sxs-lookup"><span data-stu-id="77c93-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="77c93-130">Atsevišķas dimensiju vērtības tiek sauktas par *izmaksu elementu dimensijas dalībnieki*.</span><span class="sxs-lookup"><span data-stu-id="77c93-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="77c93-131">Piemēram, jums ir ASV kontu plāna struktūra (COA), kas ir pamats ar likumu noteikto pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="77c93-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="77c93-132">Šī COA tiek izmantota kā izmaksu elementa dimensija.</span><span class="sxs-lookup"><span data-stu-id="77c93-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="77c93-133">Konti, kas ir primāro izmaksu elementi, tiek attēloti kā izmaksu elementu dimensijas dalībnieki Izmaksu uzskaitē.</span><span class="sxs-lookup"><span data-stu-id="77c93-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="77c93-134">Šajā ekrānuzņēmumā parādīts Galveno kontu kā izmaksu elementu dimensijas piemērs, ar tā faktiskajiem galvenajiem kontiem kā izmaksu elementa dimensijas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="77c93-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="77c93-135">[![Galveno kontu ekrānuzņēmums kā izmaksu elementa dimensija](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="77c93-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="77c93-136">Importējiet izmaksu elementu dimensijas dalībniekus, izmantojot datu savienotājus</span><span class="sxs-lookup"><span data-stu-id="77c93-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="77c93-137">Lai vienkāršotu izmaksu elementa dimensijas dalībnieku iestatīšanu Izmaksu uzskaitē, jūs varat izmantot datu savienotājus, kas ir vai nu iepriekš izveidoti vai jūsu izveidoti, lai izgūt primāro izmaksu elementus no vienas vai vairākām avota sistēmām.</span><span class="sxs-lookup"><span data-stu-id="77c93-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="77c93-138">Ieviešanas apsvērumi</span><span class="sxs-lookup"><span data-stu-id="77c93-138">Implementation considerations</span></span>
<span data-ttu-id="77c93-139">Tā kā izmaksu elementi pārstāv izmaksu informācijas zemāko līmeni, jums nepieciešams pārliecināties, ka visi izmaksu elementi, kas ir nepieciešami vadības pārskata izveidei, ir iekļauti, īstenojot izmaksu elementu struktūru.</span><span class="sxs-lookup"><span data-stu-id="77c93-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="77c93-140">Var būt sarežģīti atrast atbilstošu izmaksu elementu skaitu izmaksu kontrolei.</span><span class="sxs-lookup"><span data-stu-id="77c93-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="77c93-141">Tā kā pastāv tūkstošiem izmaksu elementu, var būt sarežģīti kontrolēt katru izmaksu elementu.</span><span class="sxs-lookup"><span data-stu-id="77c93-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="77c93-142">Alternatīva metode - jūs varat grupēt izmaksu elementus un pārvaldīt izmaksu kontroli uzkrātajā līmenī.</span><span class="sxs-lookup"><span data-stu-id="77c93-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]