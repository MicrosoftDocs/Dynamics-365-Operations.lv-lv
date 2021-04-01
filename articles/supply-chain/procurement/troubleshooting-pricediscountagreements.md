---
title: Cenu, atlaižu un līgumu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar cenām, atlaidēm un līgumiem.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5d17f2ec594901404fcd251e463f293258af051c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237159"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="31e5b-103">Cenu, atlaižu un līgumu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="31e5b-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="31e5b-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar cenām, atlaidēm un līgumiem.</span><span class="sxs-lookup"><span data-stu-id="31e5b-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="31e5b-105">Nevar sasaistīt pirkšanas līgumu ar pirkšanas pasūtījuma rindu pēc pirkšanas pasūtījuma izveides.</span><span class="sxs-lookup"><span data-stu-id="31e5b-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="31e5b-106">Pirkšanas līgums ar pirkšanas pasūtījumu ir jāsaista pirkšanas pasūtījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="31e5b-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="31e5b-107">Pretējā gadījumā pirkšanas pasūtījuma rindas nevar saistīt ar pirkšanas līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="31e5b-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="31e5b-108">Kāda pārbaude parāda ziņojumu “Atjauniniet cenas un atlaides, kas ievadītas manuāli vai ārējā dokumentā”?</span><span class="sxs-lookup"><span data-stu-id="31e5b-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="31e5b-109">Mainot nosūtīšanas datumu, var saņemt ziņojumu ar tekstu “Atjauniniet cenas un atlaides, kas ievadītas manuāli vai ārējā dokumentā.”</span><span class="sxs-lookup"><span data-stu-id="31e5b-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="31e5b-110">Šis ziņojums tiek parādīts, jo, mainot nosūtīšanas datumu, var rasties cits tirdzniecības vai pārdošanas līgums un tas var izraisīt cenu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="31e5b-111">Nosūtīšanas datuma maiņa var ietekmēt arī noliktavas grafikus un citu saistīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="31e5b-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="31e5b-112">Ziņojums tiek parādīts katru reizi, kad tiek mainīti datumi vai citi parametri.</span><span class="sxs-lookup"><span data-stu-id="31e5b-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="31e5b-113">Ziņojuma mērķis ir pārliecināties, vai esat informēts par cenu izmaiņām, kas var rasties šo izmaiņu dēļ.</span><span class="sxs-lookup"><span data-stu-id="31e5b-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="31e5b-114">Ziņojums ir tirdzniecības līguma novērtēšanas (TAE) uzvedne.</span><span class="sxs-lookup"><span data-stu-id="31e5b-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="31e5b-115">Pilnu aprakstu skatiet [Tirdzniecības līguma novērtēšanas politikas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="31e5b-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="31e5b-116">Pirkšanas pasūtījuma kvīts neietver visas maksas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="31e5b-117">Problēmas atveide</span><span class="sxs-lookup"><span data-stu-id="31e5b-117">Reproduce the issue</span></span>

<span data-ttu-id="31e5b-118">Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.</span><span class="sxs-lookup"><span data-stu-id="31e5b-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="31e5b-119">Lapā **Sagādes un avotu parametri** cilnē **Piegāde** pārliecinieties, vai opcija **Produktu ieejas plūsmas maksu ģenerēšana** ir iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="31e5b-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="31e5b-120">Izveidojiet pirkšanas pasūtījumu, kurā ietvertas maksas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="31e5b-121">Apstipriniet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="31e5b-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="31e5b-122">Saņemiet pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="31e5b-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="31e5b-123">Apskatiet kvīts kopsummu un salīdziniet to ar prognozēto kopsummu.</span><span class="sxs-lookup"><span data-stu-id="31e5b-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="31e5b-124">Ievērojiet, ka pirkšanas pasūtījuma kvītī nav ietvertas visas maksas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="31e5b-125">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="31e5b-125">Issue resolution</span></span>

<span data-ttu-id="31e5b-126">Risinājums ir atkarīgs no veida, kādā ir iestatītas papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="31e5b-127">Lai iegūtu informāciju par to, kā iestatīt papildmaksas, kas atbilst jūsu prasībām, skatiet šo emuāra ierakstu: [Papildmaksu grāmatošana produktu ieejas plūsmas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="31e5b-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="31e5b-128">Tirdzniecības līgumu cenas un atlaides netiek lietotas pārdošanas vai pirkšanas pasūtījuma rindās, kas ir importētas, izmantojot datu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="31e5b-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="31e5b-129">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="31e5b-129">Issue description</span></span>

<span data-ttu-id="31e5b-130">Pārdošanas vai pirkšanas pasūtījuma rindām piemērojamie tirdzniecības līgumi netiek lietoti rindās, kas ir importētas, izmantojot datu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="31e5b-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="31e5b-131">Tomēr tie paši tirdzniecības līgumi tiek lietoti pārdošanas vai pirkšanas pasūtījuma rindās, kas ir izveidotas manuāli.</span><span class="sxs-lookup"><span data-stu-id="31e5b-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="31e5b-132">Problēmas iemesls</span><span class="sxs-lookup"><span data-stu-id="31e5b-132">Reason for the issue</span></span>

<span data-ttu-id="31e5b-133">Ja pirkšanas pasūtījuma rindās, kas ir importētas, izmantojot datu pārvaldību, jau ir iekļauta cenas informācija, tirdzniecības līgums šīm rindām netiks pārvērtēts.</span><span class="sxs-lookup"><span data-stu-id="31e5b-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="31e5b-134">Piemēram, ja rindai ir iestatīta **Rindas atlaide procentos** vai kāda no cenu un atlaižu vērtībām, tad tirdzniecības līgumi šai rindai netiks meklēti.</span><span class="sxs-lookup"><span data-stu-id="31e5b-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="31e5b-135">Problēmas aprisinājums</span><span class="sxs-lookup"><span data-stu-id="31e5b-135">Issue workaround</span></span>

<span data-ttu-id="31e5b-136">Šāda darbība ir paredzama un ir līdzīga gan pārdošanas pasūtījumiem, gan pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="31e5b-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="31e5b-137">Kā aprisinājumu, importējiet pirkšanas pasūtījuma rindas bez cenas informācijas iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="31e5b-138">Pēc tam tiks lietoti tirdzniecības līgumi, un pirkšanas pasūtījuma rindas tiks atjauninātas, pamatojoties uz definētajiem tirdzniecības līgumiem.</span><span class="sxs-lookup"><span data-stu-id="31e5b-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="31e5b-139">Kreditora atlaide netiek uzkrāta, pamatojoties uz rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="31e5b-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="31e5b-140">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="31e5b-140">Issue description</span></span>

<span data-ttu-id="31e5b-141">Ja iegrāmatotajiem rēķiniem ir atšķirīgi izpildes datumi, šie rēķini netiek atspoguļoti no tiem ģenerētajās kreditoru atlaidēs.</span><span class="sxs-lookup"><span data-stu-id="31e5b-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="31e5b-142">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="31e5b-142">Issue resolution</span></span>

<span data-ttu-id="31e5b-143">Aprēķinot kreditora atlaidi, izpildes datums netiek ņemts vērā.</span><span class="sxs-lookup"><span data-stu-id="31e5b-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="31e5b-144">Apsveriet iespēju pielāgot sistēmu tā, lai izpildes datums un saistība ar rēķinu būtu skaidrāka attiecībā uz faktisko kreditora atlaidi.</span><span class="sxs-lookup"><span data-stu-id="31e5b-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="31e5b-145">Vienības cenas pirkšanas pasūtījumos netiek aprēķinātas, pamatojoties uz vienību pārveidošanu.</span><span class="sxs-lookup"><span data-stu-id="31e5b-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="31e5b-146">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="31e5b-146">Issue description</span></span>

<span data-ttu-id="31e5b-147">Mainot vienību pirkšanas pasūtījumā, tirdzniecības līguma cenas netiek pārrēķinātas atbilstoši vienības pārveidošanas definīcijām.</span><span class="sxs-lookup"><span data-stu-id="31e5b-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="31e5b-148">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="31e5b-148">Issue resolution</span></span>

<span data-ttu-id="31e5b-149">Cenas vienmēr tiek iegūtas no tirdzniecības līgumiem (vai citiem cenas iestatījumiem sistēmā, piemēram, pārdošanas līgumiem vai krājuma cenām), un tās tiek noteiktas vienībai.</span><span class="sxs-lookup"><span data-stu-id="31e5b-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="31e5b-150">Ja pasūtījuma rindā ir mainīta vienība, sistēma meklē jaunās vienības cenu un to piemēro.</span><span class="sxs-lookup"><span data-stu-id="31e5b-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="31e5b-151">Ja vienības cena netiek atrasta, sistēma cenu nepiemēro.</span><span class="sxs-lookup"><span data-stu-id="31e5b-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="31e5b-152">Vienības pārveidošanu nevar izmantot, lai pārrēķinātu cenu citā vienībā.</span><span class="sxs-lookup"><span data-stu-id="31e5b-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="31e5b-153">Teorētiski desmit kastes par vienas kastes cenu var nebūt vienāds ar vienas kastes desmitkārtīgu cenu.</span><span class="sxs-lookup"><span data-stu-id="31e5b-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="31e5b-154">Problēmas aprisinājums</span><span class="sxs-lookup"><span data-stu-id="31e5b-154">Issue workaround</span></span>

<span data-ttu-id="31e5b-155">Viens no veidiem, kā atrisināt šo problēmu, ir pārliecināties, vai tiks izmantoti tirdzniecības līgumi vienībām, kuras, iespējams, tiks izmantotas krājuma pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="31e5b-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="31e5b-156">Tirdzniecības līgumos rodas valūtas konvertēšanas problēmas.</span><span class="sxs-lookup"><span data-stu-id="31e5b-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="31e5b-157">Tirdzniecības līgumu cenas netiek pārrēķinātas atbilstoši valūtai, ja valūta pirkšanas pasūtījumā atšķiras.</span><span class="sxs-lookup"><span data-stu-id="31e5b-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="31e5b-158">Līdzeklis *Vispārējā valūta* ļauj noteikt cenas un atlaides tikai vienā valūtā.</span><span class="sxs-lookup"><span data-stu-id="31e5b-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="31e5b-159">Pēc tam varat konvertēt uz citām valūtām, pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="31e5b-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="31e5b-160">Turklāt, pēc konvertēšanas, līdzekli var automātiski lietot noapaļošanai uz leju.</span><span class="sxs-lookup"><span data-stu-id="31e5b-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="31e5b-161">Atverot Pirkšanas līguma lapu rindas skata režīmā, to nevar personalizēt, rindas pārskatā pievienojot lauku Cenas vienība.</span><span class="sxs-lookup"><span data-stu-id="31e5b-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="31e5b-162">Dažus līguma struktūras kopīgotos laukus nevar iekļaut personalizācijās.</span><span class="sxs-lookup"><span data-stu-id="31e5b-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="31e5b-163">Šis ierobežojums rodas ieviestā datu modeļa dēļ.</span><span class="sxs-lookup"><span data-stu-id="31e5b-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="31e5b-164">Tāpēc nav iespējams personalizēt lauku **Cenas vienība**.</span><span class="sxs-lookup"><span data-stu-id="31e5b-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="31e5b-165">Pirkšanas līguma maksimālais ierobežojums nav spēkā pirkšanas pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="31e5b-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="31e5b-166">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="31e5b-166">Issue description</span></span>

<span data-ttu-id="31e5b-167">Kad pirkšanas pieprasījums ir saistīts ar pirkšanas līgumu, pirkšanas līguma maksimālais ierobežojums nav spēkā pirkšanas pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="31e5b-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="31e5b-168">Noklusējuma cenas informācija ir ievadīta pareizi, tomēr pirkšanas pieprasījumā nevar pasūtīt vairāk par pirkšanas līguma maksimālo ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="31e5b-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="31e5b-169">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="31e5b-169">Issue resolution</span></span>

<span data-ttu-id="31e5b-170">Šāda darbība ir paredzama.</span><span class="sxs-lookup"><span data-stu-id="31e5b-170">This behavior is expected.</span></span> <span data-ttu-id="31e5b-171">Tā kā pieprasījumi ne vienmēr tiek apstiprināti, daudzums vai summa pirkšanas līgumā nav jārezervē.</span><span class="sxs-lookup"><span data-stu-id="31e5b-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="31e5b-172">Tādējādi netiks sasniegts pirkšanas līguma maksimālais ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="31e5b-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="31e5b-173">Tirdzniecības līgumus var izveidot no noraidītajiem piedāvājumu pieprasījumiem (PP).</span><span class="sxs-lookup"><span data-stu-id="31e5b-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="31e5b-174">Tādējādi sistēma neliedz tirdzniecības līgumu žurnālu izveidi, ja PP rinda nav pieņemta.</span><span class="sxs-lookup"><span data-stu-id="31e5b-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="31e5b-175">Tirdzniecības līgumus var izveidot jebkurai atbildei uz piedāvājuma pieprasījumu (PP) neatkarīgi no tā, vai tie ir pieņemti vai noraidīti.</span><span class="sxs-lookup"><span data-stu-id="31e5b-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="31e5b-176">Papildinformāciju skatiet rakstā [Piedāvājuma pieprasījumu (PP) pārskats](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="31e5b-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]