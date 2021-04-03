---
title: Kopējo izmaksu modulis
description: Kopējo izmaksu modulis palīdz uzņēmumiem racionalizēt ienākošās kravas nosūtīšanas darbības, sniedzot lietotājiem pilnīgu finanšu un nepilnu kontroli pār importēto kravu no ražotāja uz noliktavu.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9d04c377080a1d301efb771b98c249f610a3289d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500336"
---
# <a name="landed-cost-module"></a><span data-ttu-id="6001a-103">Kopējo izmaksu modulis</span><span class="sxs-lookup"><span data-stu-id="6001a-103">Landed cost module</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6001a-104">**Kopējo izmaksu** modulis palīdz uzņēmumiem racionalizēt ienākošās kravas nosūtīšanas darbības, sniedzot lietotājiem pilnīgu finanšu un nepilnu kontroli pār importēto kravu no ražotāja uz noliktavu.</span><span class="sxs-lookup"><span data-stu-id="6001a-104">The **Landed cost** module helps businesses streamline inbound shipping operations by giving users complete financial and logistical control over imported freight, from the manufacturer to the warehouse.</span></span> <span data-ttu-id="6001a-105">Importētajām precēm kopējās izmaksas var būt 40 procenti vai vairāk no katras importētās preces kopējām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="6001a-105">For imported goods, landed costs can account for 40 percent or more of the total cost of each imported item.</span></span> <span data-ttu-id="6001a-106">Tāpēc ir jāsniedz precīzs kopējo izmaksu novērtējums.</span><span class="sxs-lookup"><span data-stu-id="6001a-106">Therefore, the challenge is to provide accurate estimates for landed costs.</span></span>

<span data-ttu-id="6001a-107">Uzņēmumi var izmantot kopējās izmaksas, lai veiktu sekojošos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="6001a-107">Businesses can use Landed cost to complete the following tasks:</span></span>

- <span data-ttu-id="6001a-108">Novērtētās kopējās izmaksas reisa izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="6001a-108">Estimate landed costs at the time of voyage creation.</span></span>
- <span data-ttu-id="6001a-109">Iedalītās kopējā izmaksas uz vairākiem krājumiem un pirkšanas pasūtījumiem vai pārsūtīšanas pasūtījumiem vienā reisā.</span><span class="sxs-lookup"><span data-stu-id="6001a-109">Apportion landed costs to multiple items and purchase orders or transfer orders in a single voyage.</span></span>
- <span data-ttu-id="6001a-110">Atbalstiet preču pārsūtīšanu starp fiziskām atrašanās vietām, atpazīstot kopējās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="6001a-110">Support the transfer of goods between physical locations by recognizing landed costs.</span></span>
- <span data-ttu-id="6001a-111">Atpazīt uzkrājumus tranzīta precēm.</span><span class="sxs-lookup"><span data-stu-id="6001a-111">Recognize accruals for goods in transit.</span></span>

<span data-ttu-id="6001a-112">Kopējās izmaksas nodrošina precīzas un laicīgas pieskaitāmās zemes izmaksu tāmes.</span><span class="sxs-lookup"><span data-stu-id="6001a-112">Landed cost provides accurate and timely cost estimates for overhead landed costs.</span></span> <span data-ttu-id="6001a-113">Tajā pašā laikā tā nodrošina palielinātu finanšu un elektronisku redzamību paplašinātā piegādes ķēdē.</span><span class="sxs-lookup"><span data-stu-id="6001a-113">At the same time, it provides increased financial and logistical visibility into the extended supply chain.</span></span> <span data-ttu-id="6001a-114">Tas arī palīdz samazināt izmaksu aprēķināšanas un izmaksu aprēķināšanas kļūdu administrēšanu.</span><span class="sxs-lookup"><span data-stu-id="6001a-114">It also helps reduce the administration of costing and costing errors.</span></span>

## <a name="highlights"></a><span data-ttu-id="6001a-115">Galvenie punkti</span><span class="sxs-lookup"><span data-stu-id="6001a-115">Highlights</span></span>

### <a name="voyages"></a><span data-ttu-id="6001a-116">Reisi</span><span class="sxs-lookup"><span data-stu-id="6001a-116">Voyages</span></span>

<span data-ttu-id="6001a-117">Kopējās izmaksās reiss ir atšķirīga kustība no nosūtīšanas vietas, izmantojot noteiktu adresātu kopu noteiktā laika posmā uz norādītu saņemšanas noliktavas atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="6001a-117">In Landed cost, a voyage is a distinct movement from an outbound location, through a specific set of destinations over a specified period, to a specified inbound warehouse location.</span></span> <span data-ttu-id="6001a-118">Pirkšanas pasūtījumus un pasūtījumu rindas var pievienot vienam konteineram vai vairākiem reisa konteineriem, un izmaksas tiks pareizi sadalītas atpakaļ uz krājumu rindu.</span><span class="sxs-lookup"><span data-stu-id="6001a-118">Purchase orders and order lines can be added to either a single container or multiple containers for a voyage, and the costs will be correctly allocated back to the item line.</span></span> <span data-ttu-id="6001a-119">Pasūtījumus un pasūtījumu rindas var pievienot arī visām juridiskajām personām vienam reisam.</span><span class="sxs-lookup"><span data-stu-id="6001a-119">Orders and order lines can also be added across legal entities for a single voyage.</span></span>

### <a name="item-ownership"></a><span data-ttu-id="6001a-120">Krājuma īpašumtiesības</span><span class="sxs-lookup"><span data-stu-id="6001a-120">Item ownership</span></span>

<span data-ttu-id="6001a-121">Sistēmā Microsoft Dynamics 365 Supply Chain Management preces parasti tiek saņemtas noliktavas galamērķī un pēc tam iekļautas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6001a-121">In Microsoft Dynamics 365 Supply Chain Management, goods are typically received at the warehouse destination and then invoiced.</span></span> <span data-ttu-id="6001a-122">Tomēr saskaņā ar vairumu starptautisko tirdzniecības līgumu uzņēmums uzņemsies atbildību par precēm no laika, kad tās atstāj oriģinālo ostu, pirms tās ir fiziski saņemtas.</span><span class="sxs-lookup"><span data-stu-id="6001a-122">However, under most international trade agreements, a business takes ownership of goods from the time when they leave the original port, before they have been physically received.</span></span> <span data-ttu-id="6001a-123">Kopējās izmaksas ļauj uzņēmumiem izrakstīt rēķinu par precēm pirms to fiziskās saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="6001a-123">Landed cost enables businesses to invoice goods before they have been physically received.</span></span> <span data-ttu-id="6001a-124">Šī koncepcija ir pazīstama kā preces tranzīta pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="6001a-124">This concept is known as a goods in transit order.</span></span> <span data-ttu-id="6001a-125">Tas izveido jaunu pasūtījuma tipu, lai pārvaldītu preču saņemšanu pēc sākotnējā pirkšanas pasūtījuma saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="6001a-125">It creates a new type of order to manage the receipt of goods after the original purchase order has been invoiced.</span></span>

### <a name="costs"></a><span data-ttu-id="6001a-126">Izmaksas</span><span class="sxs-lookup"><span data-stu-id="6001a-126">Costs</span></span>

<span data-ttu-id="6001a-127">Izveidojot reisu kopējās izmaksās, tam var automātiski pievienot izmaksas.</span><span class="sxs-lookup"><span data-stu-id="6001a-127">When you create a voyage in Landed cost, costs can automatically be added to it.</span></span> <span data-ttu-id="6001a-128">Šīs izmaksas ir iestatītas Kopējās izmaksās un tām ir pieejamas dažādas izmaksu opcijas un izmaksu bāzes.</span><span class="sxs-lookup"><span data-stu-id="6001a-128">These costs are set up in Landed cost, and various cost options and cost bases are available for them.</span></span> <span data-ttu-id="6001a-129">Katras izmaksas var iestatīt dažādiem reisa līmeņiem un sadalīt uz krājuma līmeni, izmantojot sadalījuma noteikumus, kas atbalsta daudzumu, tilpumu, svaru, summu un noteiktus tilpuma dalītājus.</span><span class="sxs-lookup"><span data-stu-id="6001a-129">Each cost can be set up for different levels of a voyage and apportioned to the item level through apportionment rules that support quantity, volume, weight, amount, and defined volumetric divisors.</span></span> <span data-ttu-id="6001a-130">Šīs novērtētās izmaksas sniedz precīzu visu reisa izmaksu novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="6001a-130">These estimated costs provide an accurate estimate of all costs for a voyage.</span></span>

<span data-ttu-id="6001a-131">Pēc tam Kopējās izmaksas veic prognozēto kopējo izmaksu iepriekšēju grāmatošanu/uzkrājumu, lai nodrošinātu, ka reisa izveides laikā tiek sniegtas precīzas aprēķinātās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="6001a-131">Landed cost then runs a preliminary posting/accrual of the estimated landed costs to ensure that an accurate calculation of estimated costs is provided at the time of voyage creation.</span></span> <span data-ttu-id="6001a-132">Kad šīs automātiskās izmaksas tiek iekļautas rēķinā, novērtētās izmaksas tiek apgrieztas un aizstātas ar faktiskajām izmaksām, pamatojoties uz izmaksu rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="6001a-132">As these automatic costs are invoiced, the estimated costs are reversed and replaced by the actual costs, based on cost invoices.</span></span>

<span data-ttu-id="6001a-133">Faktiskās izmaksas tiek atgrieztas prognozētās izmaksas, kas tiek grāmatotas izmaksu rēķinu izrakstīšanas laikā, izmantojot klīringa kontus, kas iestatīti katram izmaksu tipam (piemēram, nodoklis, kravas pārvadāšana un apdrošināšana).</span><span class="sxs-lookup"><span data-stu-id="6001a-133">Actual costs are reverse estimated costs that are posted at the time of cost invoicing by using clearing accounts that are set up for each type of cost (for example, duty, freight, and insurance).</span></span> <span data-ttu-id="6001a-134">Šie grāmatojumi seko grāmatošanas uzvedībai, kas saistīta ar noteiktu krājumu.</span><span class="sxs-lookup"><span data-stu-id="6001a-134">These postings follow the posting behavior that is associated with the specific item.</span></span> <span data-ttu-id="6001a-135">Tie automātiski atjaunina krājumu grāmatošanu, neņemot vērā to, vai grāmatošanas tips ir pirmais in, pirmais ārā (FIFO), pēdējais atrodas, pirmais ārā (LIFO), pārvieto svērto vidējo vai pārvieto vidējo.</span><span class="sxs-lookup"><span data-stu-id="6001a-135">They automatically update inventory posting, regardless of whether the posting type is first in, first out (FIFO), last in, first out (LIFO), moving weighted average, or moving average.</span></span> <span data-ttu-id="6001a-136">Visi krājumu modeļu grupu grāmatošanas tipi tiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="6001a-136">All inventory model group posting types are supported.</span></span> <span data-ttu-id="6001a-137">Lai pārvietotu vidējo un standarta izmaksu grāmatošanu, pirkšanas cenas novirzes konti ir pieejami, lai grāmatotu atšķirības starp prognozētajām izmaksām un faktiskajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="6001a-137">For moving average and standard cost posting, purchase price variance accounts are available to post the differences between estimated costs and actual costs.</span></span>

### <a name="item-and-order-tracking"></a><span data-ttu-id="6001a-138">Krājumu un pasūtījumu izsekošana</span><span class="sxs-lookup"><span data-stu-id="6001a-138">Item and order tracking</span></span>

<span data-ttu-id="6001a-139">Kad reiss pārvietojas no sākotnējās nosūtīšanas vietas uz beigu mērķa noliktavu, lietotāji var pēc vajadzības atjaunināt katru kravu vai *kāju*, vai ceļojumu.</span><span class="sxs-lookup"><span data-stu-id="6001a-139">As a voyage moves from the originating outbound location to the final destination warehouse, users can update each step, or *leg*, of its journey as required.</span></span> <span data-ttu-id="6001a-140">Katrai kājai tiek identificēts izpildes laiks un kravas statuss.</span><span class="sxs-lookup"><span data-stu-id="6001a-140">For each leg, a lead time and a shipment status are identified.</span></span> <span data-ttu-id="6001a-141">Tiek identificēti arī apstiprinātie piegādes datumi kustībai uz nākošo ceļojuma daļu.</span><span class="sxs-lookup"><span data-stu-id="6001a-141">Confirmed delivery dates for movement to the next leg of the journey are also identified.</span></span> <span data-ttu-id="6001a-142">Kopā šie piegādes datumi nodrošina paredzamo preču piegādes datumu saņemšanas noliktavā.</span><span class="sxs-lookup"><span data-stu-id="6001a-142">Together, these delivery dates provide an estimated delivery date of the goods to the inbound warehouse.</span></span> <span data-ttu-id="6001a-143">Lietotāji var mainīt šos piegādes datumus.</span><span class="sxs-lookup"><span data-stu-id="6001a-143">Users can change these delivery dates.</span></span> <span data-ttu-id="6001a-144">Šādā gadījumā preču plānotais piegādes datums pēc tam tiek automātiski atjaunināts, pamatojoties uz ceļojuma izpildes laikiem un sadaļām.</span><span class="sxs-lookup"><span data-stu-id="6001a-144">In this case, the estimated delivery date of the goods is then automatically updated, based on the lead times and legs of the journey.</span></span> <span data-ttu-id="6001a-145">Redzamība tranzītā, izmantojot reisu un kuģi, ir pieejama uz konteinera pamata pirms preču saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="6001a-145">Visibility into goods in transit by voyage and vessel is available on a per-container basis before receipt of the goods.</span></span> <span data-ttu-id="6001a-146">Ņemot vērā to, ka datumi tiek atjaunināti katrā pirkšanas pasūtījuma rindā, uzņēmumiem ir lielāka kontrole pār loģistiku un noliktavas plānošanu.</span><span class="sxs-lookup"><span data-stu-id="6001a-146">Because the dates are updated on each purchase order line, businesses have more control over logistics and warehouse planning.</span></span>

## <a name="landed-cost-concepts"></a><span data-ttu-id="6001a-147">Kopējo izmaksu koncepcijas</span><span class="sxs-lookup"><span data-stu-id="6001a-147">Landed cost concepts</span></span>

<span data-ttu-id="6001a-148">Tabulā ir apkopotas dažas galvenās Kopējo izmaksu koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="6001a-148">The following table summarizes some core concepts of Landed cost.</span></span>

| <span data-ttu-id="6001a-149">Koncepcija</span><span class="sxs-lookup"><span data-stu-id="6001a-149">Concept</span></span> | <span data-ttu-id="6001a-150">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6001a-150">Description</span></span> |
|---|---|
| <span data-ttu-id="6001a-151">Reiss</span><span class="sxs-lookup"><span data-stu-id="6001a-151">Voyage</span></span> | <span data-ttu-id="6001a-152">Parasti reiss ir viens kuģis.</span><span class="sxs-lookup"><span data-stu-id="6001a-152">Typically, a voyage is one vessel.</span></span> <span data-ttu-id="6001a-153">Tomēr atkarībā no jūsu prakses un procedūrām, tas var būt viens kreditors vai viens pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="6001a-153">However, depending on your practices and procedures, it can be one vendor or one purchase order.</span></span> <span data-ttu-id="6001a-154">Nav ierobežojumu šīs koncepcijas izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="6001a-154">There are no limitations on the use of this concept.</span></span> |
| <span data-ttu-id="6001a-155">Folio</span><span class="sxs-lookup"><span data-stu-id="6001a-155">Folio</span></span> | <span data-ttu-id="6001a-156">Folio bieži nosaka muitas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="6001a-156">A folio is often determined by customs regulations.</span></span> <span data-ttu-id="6001a-157">Tas var ietvert viena kreditora preces vienam elementam/uzņēmumam vienā sūtījumā.</span><span class="sxs-lookup"><span data-stu-id="6001a-157">It can consist of one vendor's goods for one entity/company per shipment.</span></span> <span data-ttu-id="6001a-158">Folio preces var būt vienā konteinerā vai izplatītas starp vairākiem konteineriem.</span><span class="sxs-lookup"><span data-stu-id="6001a-158">The goods in a folio can be in one container or spread among multiple containers.</span></span> |
| <span data-ttu-id="6001a-159">Nosūtīšanas konteiners</span><span class="sxs-lookup"><span data-stu-id="6001a-159">Shipping container</span></span> | <span data-ttu-id="6001a-160">Sūtījumu konteineru veikala pirkšanas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="6001a-160">Shipping containers store purchase order lines.</span></span> <span data-ttu-id="6001a-161">Šo līmeņu līmenis ir zem nosūtīšanas līmeņa.</span><span class="sxs-lookup"><span data-stu-id="6001a-161">They are a level below the shipment level.</span></span> <span data-ttu-id="6001a-162">Parasti tās tiek izmantotas, ja preces tiek segtas pa konteineriem vai ja saņemšana ir veikta uz konteineru.</span><span class="sxs-lookup"><span data-stu-id="6001a-162">They are typically used if costs are apportioned for goods by container, or if receiving is done per container.</span></span> |
| <span data-ttu-id="6001a-163">Nosūtīšanas konteinera veids</span><span class="sxs-lookup"><span data-stu-id="6001a-163">Shipping container type</span></span> | <span data-ttu-id="6001a-164">Pārvadāšanas konteinera veidi var noteikt izmaksu tipa cenu (piemēram, kravas pārvadāšana).</span><span class="sxs-lookup"><span data-stu-id="6001a-164">Shipping container types can determine the price for a cost type (for example, freight).</span></span> <span data-ttu-id="6001a-165">Tās sniedz arī noderīgu nosūtīšanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="6001a-165">They also provide useful shipping information.</span></span> |
| <span data-ttu-id="6001a-166">Izmaksu tips</span><span class="sxs-lookup"><span data-stu-id="6001a-166">Cost type</span></span> | <span data-ttu-id="6001a-167">Izmaksu tipi identificē izmaksas, kas saistītas ar importu, piemēram, nodeva, kravas pārvadāšana un apdrošināšana.</span><span class="sxs-lookup"><span data-stu-id="6001a-167">Cost types identify costs that are associated with imports, such as duty, freight, and insurance.</span></span> |
| <span data-ttu-id="6001a-168">Automātiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="6001a-168">Auto cost</span></span> | <span data-ttu-id="6001a-169">Automātiskās izmaksas darbojas kā tirdzniecības līgumi.</span><span class="sxs-lookup"><span data-stu-id="6001a-169">Auto costs work like trade agreements.</span></span> <span data-ttu-id="6001a-170">Automātiskās izmaksas ir saistītas ar reisa līmeni.</span><span class="sxs-lookup"><span data-stu-id="6001a-170">An auto cost is linked to a voyage level.</span></span> |
| <span data-ttu-id="6001a-171">Osta</span><span class="sxs-lookup"><span data-stu-id="6001a-171">Port</span></span> | <span data-ttu-id="6001a-172">Ostas ir apgabali, no kurienes preces tiek saņemtas un no tām pārsūtītas.</span><span class="sxs-lookup"><span data-stu-id="6001a-172">Ports are areas where goods are received and transferred from.</span></span> |
| <span data-ttu-id="6001a-173">Kuģis</span><span class="sxs-lookup"><span data-stu-id="6001a-173">Vessel</span></span> | <span data-ttu-id="6001a-174">Kuģis ir līdzeklis, ko izmanto preču transportēšanai, piemēram, kuģis vai lidmašīna.</span><span class="sxs-lookup"><span data-stu-id="6001a-174">A vessel is the medium that is used to transport goods, such as a ship or an airplane.</span></span> |
| <span data-ttu-id="6001a-175">Tranzītpreces</span><span class="sxs-lookup"><span data-stu-id="6001a-175">Goods in transit</span></span> | <span data-ttu-id="6001a-176">Atkarībā no iestatījumiem preces tiek novietotas tranzīta noliktavā pēc rēķina atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="6001a-176">Depending on settings, goods are put into an in-transit warehouse after an invoice is updated.</span></span> |
| <span data-ttu-id="6001a-177">Aktivitāte</span><span class="sxs-lookup"><span data-stu-id="6001a-177">Activity</span></span> | <span data-ttu-id="6001a-178">Aktivitātes var izmantot, lai uzglabātu katru nozīmīgu ceļojuma soli starp divām ostām.</span><span class="sxs-lookup"><span data-stu-id="6001a-178">Activities can be used to store each significant step of the journey between two ports.</span></span> <span data-ttu-id="6001a-179">Tos var izmantot datumu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="6001a-179">They can be used to update dates.</span></span> |
| <span data-ttu-id="6001a-180">Maršruta veidne</span><span class="sxs-lookup"><span data-stu-id="6001a-180">Journey template</span></span> | <span data-ttu-id="6001a-181">Ceļojuma veidnes ir maršruti, ko preces izmanto starp divām ostām.</span><span class="sxs-lookup"><span data-stu-id="6001a-181">Journey templates are routes that goods take between two ports.</span></span> |

<span data-ttu-id="6001a-182">**Kopējo izmaksu** un **Transportēšanas pārvaldības (TMS)** moduļu terminoloģijas un funkciju salīdzināšanai skatiet sadaļu [Kopējās izmaksas pret Transportēšanas pārvaldību](landed-cost-vs-tms.md).</span><span class="sxs-lookup"><span data-stu-id="6001a-182">For a comparison of the terminology and features of the **Landed cost** and **Transportation management** (TMS) modules, see [Landed cost vs. Transportation management](landed-cost-vs-tms.md).</span></span>