---
title: Apgrieztais PVN
description: Šajā tēmā ir paskaidrots, kā iestatīt apgriezto pievienotās vērtības nodokli (PVN) Eiropas valstīs un Saūda Arābijā.
author: epodkolz
manager: AnnBe
ms.date: 04/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 627b90659ce4e285667492e37be203cd9dbb7c9c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538162"
---
# <a name="reverse-charge-vat"></a><span data-ttu-id="a240a-103">Apgrieztais PVN</span><span class="sxs-lookup"><span data-stu-id="a240a-103">Reverse charge VAT</span></span>


[!include [banner](../includes/banner.md)]


<span data-ttu-id="a240a-104">Sājā tēmā ir vispārīgi aprakstīts, kā iestatīt apgriezto pievienotās vērtības nodokli (PVN) Saūda Arābijā un Eiropas valstīs.</span><span class="sxs-lookup"><span data-stu-id="a240a-104">This topic describes a generic approach for setting up reverse charge value-added tax (VAT) for Saudi Arabia and European countries.</span></span>

<span data-ttu-id="a240a-105">Apgrieztā maksāšana ir nodokļu maksāšanas metode, kuras ietvaros atbildība par PVN uzskaiti un ziņošanu tiek pārnesta no pārdevēja uz preču un/vai pakalpojumu pircēju.</span><span class="sxs-lookup"><span data-stu-id="a240a-105">Reverse Charge is a tax schema that moves the responsibility for the accounting and reporting of VAT from the seller to the buyer of goods and/or services.</span></span> <span data-ttu-id="a240a-106">Tādējādi preču un/vai pakalpojumu saņēmēji savā PVN deklarācijā ziņo gan par pārdošanas PVN (kā pārdevējs), gan pirkšanas PVN (kā pircējs).</span><span class="sxs-lookup"><span data-stu-id="a240a-106">Therefore, recipients of goods and/or services report both the output VAT (in the role of a seller) and the input VAT (in the role of a purchaser) on their VAT statement.</span></span>

<span data-ttu-id="a240a-107">Dažās valstīs vai reģionos apgrieztās maksāšanas metode ir ieviesta tikai dažām precēm un/vai pakalpojumiem un ir noteikti papildu pārdošanas summas nosacījumi vai sliekšņi.</span><span class="sxs-lookup"><span data-stu-id="a240a-107">In some countries or regions, the Reverse Charge schema is implemented only for some goods and/or services, and there are additional conditions or thresholds on sales amounts.</span></span> <span data-ttu-id="a240a-108">Citās valstīs vai reģionos atbildība par PVN maksāšanu ir atkarīga no piegādātāja un pircēja statusa.</span><span class="sxs-lookup"><span data-stu-id="a240a-108">In other countries or regions, the responsibility for VAT payment depends on the status of the supplier and the buyer.</span></span> <span data-ttu-id="a240a-109">Ja pircējam ir jāmaksā PVN, tam ir jābūt skaidri norādītam piegādātāja izrakstītajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="a240a-109">If the buyer is liable to pay VAT, this fact must be clearly indicated on the invoice that the supplier issues.</span></span> <span data-ttu-id="a240a-110">Piemēram, rēķinā ir jābūt ietvertam tekstam “apgrieztā maksāšana” un norādītām pozīcijām, uz kurām attiecas apgrieztā maksāšana.</span><span class="sxs-lookup"><span data-stu-id="a240a-110">For example, the invoice must include the words "Reverse charge" and must indicate which positions are under the Reverse Charge schema.</span></span> 

<span data-ttu-id="a240a-111">Lai lietotu atgriezto maksāšanu, ir jāveic tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="a240a-111">To apply the reverse charge, you must complete the following setup.</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="a240a-112">Iestatīt PVN kodus</span><span class="sxs-lookup"><span data-stu-id="a240a-112">Set up sales tax codes</span></span>
<span data-ttu-id="a240a-113">Ir ieteicams pārdošanas un pirkšanas operācijām izmantot atsevišķus PVN kodus.</span><span class="sxs-lookup"><span data-stu-id="a240a-113">We recommend that you use separate sales tax codes for sales operations and purchase operations.</span></span>

<table>
<body>
<tr>
<td><span data-ttu-id="a240a-114"><strong>Pārdošanas PVN kods</strong></span><span class="sxs-lookup"><span data-stu-id="a240a-114"><strong>Sales tax code for sales</strong></span></span></td>
<td><span data-ttu-id="a240a-115">Izveidojiet PVN kodu apgrieztās maksāšanas pārdošanas operācijām (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN kodi</strong>).</span><span class="sxs-lookup"><span data-stu-id="a240a-115">Create a sales tax code for reverse charge sales operations (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="a240a-116"><strong>Pirkšanas PVN kods</strong></span><span class="sxs-lookup"><span data-stu-id="a240a-116"><strong>Sales tax code for purchases</strong></span></span></td>
<td><p><span data-ttu-id="a240a-117">Izveidojiet pozitīvā un negatīvā PVN kodus pirkšanas apgrieztajam PVN (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN kodi</strong>).</span><span class="sxs-lookup"><span data-stu-id="a240a-117">Create positive and negative sales tax codes for the reverse charge VAT for purchases (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span></p>
<ol>
<li><span data-ttu-id="a240a-118">Izveidojiet pozitīvas vērtības PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="a240a-118">Create a sales tax code that has a positive value.</span></span></li>
<li><span data-ttu-id="a240a-119">Izveidojiet negatīvas vērtības PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="a240a-119">Create a sales tax code that has a negative value.</span></span> <span data-ttu-id="a240a-120">Iestatiet opcijas <strong>Atļaut negatīvu PVN likmi</strong> vērtību <strong>Jā</strong>.</span><span class="sxs-lookup"><span data-stu-id="a240a-120">Set the <strong>Allow negative sales tax percentage</strong> option to <strong>Yes</strong>.</span></span>
<span data-ttu-id="a240a-121">Šis negatīvas vērtības PVN kods ir jāpiešķir krājumu PVN grupai, un pēc tam šī krājumu PVN grupa ir jāpiešķir krājumiem, uz kuriem attiecas apgrieztais PVN.</span><span class="sxs-lookup"><span data-stu-id="a240a-121">You must assign this negative sales tax code to an item sales tax group and then assign that item sales tax group to the items that are subject to the reverse charge VAT.</span></span></li>
</ol>
<p><span data-ttu-id="a240a-122">Papildinformāciju skatiet nākamajā sadaļā &quot;PVN grupu un krājumu PVN grupu iestatīšana&quot;.</span><span class="sxs-lookup"><span data-stu-id="a240a-122">For more information, see the next section, &quot;Set up sales tax groups and item sales tax groups.&quot;</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="a240a-123">PVN grupu un krājumu PVN grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a240a-123">Set up sales tax groups and item sales tax groups</span></span>
<span data-ttu-id="a240a-124">Ir ieteicams pārdošanas un pirkšanas operācijām izmantot atsevišķas PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="a240a-124">We recommend that you use separate sales tax groups for sales operations and purchase operations.</span></span>

<table>
<tr>
<td><span data-ttu-id="a240a-125"><strong>Pārdošanas PVN grupas</strong></span><span class="sxs-lookup"><span data-stu-id="a240a-125"><strong>Sales tax groups for sales</strong></span></span></td>
<td><span data-ttu-id="a240a-126">Izveidojiet PVN grupu apgrieztās maksāšanas pārdošanas operācijām (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN grupas</strong>).</span><span class="sxs-lookup"><span data-stu-id="a240a-126">Create a sales tax group for sales operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="a240a-127">Cilnē <strong>Iestatīšana</strong> ietveriet šajā grupā apgrieztās maksāšanas PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="a240a-127">On the <strong>Setup</strong> tab, include the sales tax code for the reverse charge in this group.</span></span> <span data-ttu-id="a240a-128">Atzīmējiet pārdošanas PVN koda izvēles rūtiņas <strong>Neapliekams</strong> un <strong>Atgriezes maksa</strong>.</span><span class="sxs-lookup"><span data-stu-id="a240a-128">Select the <strong>Exempt</strong> and <strong>Reverse charge</strong> check boxes for the sales tax code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a240a-129"><strong>Pirkšanas PVN grupas</strong></span><span class="sxs-lookup"><span data-stu-id="a240a-129"><strong>Sales tax groups for purchases</strong></span></span></td>
<td><span data-ttu-id="a240a-130">Izveidojiet PVN grupu apgrieztās maksāšanas pirkšanas operācijām (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>PVN grupas</strong>).</span><span class="sxs-lookup"><span data-stu-id="a240a-130">Create a sales tax group for purchase operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="a240a-131">Cilnē <strong>Iestatījumi</strong> ietveriet šajā grupā gan pozitīvās, gan negatīvās vērtības PVN kodus.</span><span class="sxs-lookup"><span data-stu-id="a240a-131">On the <strong>Setup</strong> tab, include both positive and negative sales tax codes in this group.</span></span> <span data-ttu-id="a240a-132">Atzīmējiet negatīvās vērtības PVN koda izvēles rūtiņu <strong>Atgriezes maksa</strong>.</span><span class="sxs-lookup"><span data-stu-id="a240a-132">Select the <strong>Reverse charge</strong> check box for the sales tax code that has a negative value.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a240a-133"><strong>Krājumu PVN grupas</strong></span><span class="sxs-lookup"><span data-stu-id="a240a-133"><strong>Item sales tax groups</strong></span></span></td>
<td><span data-ttu-id="a240a-134">Izveidojiet vai atjauniniet krājumu PVN grupu, izmantojot negatīvās vērtības PVN kodu (<strong>Nodokļi</strong> &gt; <strong>Netiešie nodokļi</strong> &gt; <strong>PVN</strong> &gt; <strong>Krājumu PVN grupas</strong>).</span><span class="sxs-lookup"><span data-stu-id="a240a-134">Create or update the item sales tax group with the sales tax code that has a negative value (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Item sales tax groups</strong>).</span></span> <span data-ttu-id="a240a-135">Produktiem un kategorijām, uz kuriem attiecas apgrieztā maksāšana, ir jāpiešķir noklusējuma krājumu PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="a240a-135">You must assign the default item sales tax group to the products and categories that are subject to the reverse charge.</span></span></td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a><span data-ttu-id="a240a-136">Apgrieztās maksāšanas grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a240a-136">Set up reverse charge groups</span></span>
<span data-ttu-id="a240a-137">Lapā **Atgriezes maksas krājumu grupas** (**Nodokļi** &gt; **Iestatīšana** &gt; **PVN** &gt; **Atgriezes maksas krājumu grupas**) varat definēt preču vai pakalpojumu grupas vai atsevišķas preces vai pakalpojumus, uz kuriem var attiecināt apgriezto maksāšanu.</span><span class="sxs-lookup"><span data-stu-id="a240a-137">On the **Reverse charge item groups** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge item groups**), you can define groups of products or services, or individual products or services, that the reverse charge can be applied to.</span></span> <span data-ttu-id="a240a-138">Katrai apgrieztās maksāšanas krājumu grupai definējiet pārdošanas un/vai pirkšanas krājumu, krājumu grupu un kategoriju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a240a-138">For each reverse charge item group, define the list of items, item groups, and categories for sales and/or purchases.</span></span>

## <a name="set-up-reverse-charge-rules"></a><span data-ttu-id="a240a-139">Apgrieztās maksāšanas kārtulu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a240a-139">Set up reverse charge rules</span></span>
<span data-ttu-id="a240a-140">Lapā **Atgriezes maksas kārtulas** (**Nodokļi** &gt; **Iestatīšana** &gt; **PVN** &gt; **Atgriezes maksas kārtulas**) varat definēt pirkšanai un pārdošanai lietojamās kārtulas.</span><span class="sxs-lookup"><span data-stu-id="a240a-140">On the **Reverse charge rules** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge rules**), you can define the applicability rules for purchase and sales purposes.</span></span> <span data-ttu-id="a240a-141">Varat konfigurēt apgrieztās maksāšanas piemērotības kārtulu kopu.</span><span class="sxs-lookup"><span data-stu-id="a240a-141">You can configure a set of reverse charge applicability rules.</span></span> <span data-ttu-id="a240a-142">Katrai kārtulai iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="a240a-142">For each rule, set the following fields:</span></span>

- <span data-ttu-id="a240a-143">**Dokumenta tips** — atlasiet **Pirkšanas pasūtījums**, **Kreditoru rēķinu žurnāls**, **Pārdošanas pasūtījums**, **Brīva teksta rēķins**, **Debitoru rēķinu žurnāls** un/vai **Kreditora rēķins**.</span><span class="sxs-lookup"><span data-stu-id="a240a-143">**Document type** – Select **Purchase order**, **Vendor invoice journal**, **Sales order**, **Free text invoice**, **Customer invoice journal**, and/or **Vendor invoice**.</span></span>
- <span data-ttu-id="a240a-144">**Partnera valsts/reģiona veids** — atlasiet **Iekšzemes**, **ES** vai **Ārvalstu**.</span><span class="sxs-lookup"><span data-stu-id="a240a-144">**Country/region type of the partner** – Select **Domestic**, **EU**, or **Foreign**.</span></span> <span data-ttu-id="a240a-145">Ja kārtulu var lietot visiem tirdzniecības partneriem neatkarīgi no partneru adreses valsts vai reģiona, atlasiet opciju **Visi**.</span><span class="sxs-lookup"><span data-stu-id="a240a-145">Alternatively, if the rule can be applied to all trade partners, regardless of the country or region of their address, select **All**.</span></span>
- <span data-ttu-id="a240a-146">**Iekšzemes piegādes adrese** — atzīmējiet šo izvēles rūtiņu, lai lietotu kārtulu piegādēm tajā pašā valstī vai reģionā.</span><span class="sxs-lookup"><span data-stu-id="a240a-146">**Domestic delivery address** – Select this check box to apply the rule to deliveries within the same country or region.</span></span> <span data-ttu-id="a240a-147">Šo izvēles rūtiņu nevar atzīmēt, ja ir iestatīts dokumenta tips **Kreditoru rēķinu žurnāls** vai **Debitoru rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="a240a-147">This check box can't be selected for the **Vendor invoice journal** and **Customer invoice journal** document types.</span></span>
- <span data-ttu-id="a240a-148">**Atgriezes maksas krājumu grupa** — atlasiet grupu, kam var lietot kārtulu.</span><span class="sxs-lookup"><span data-stu-id="a240a-148">**Reverse charge item group** – Select the group that the rule can be applied to.</span></span>
- <span data-ttu-id="a240a-149">**Sliekšņa summa** — apgrieztās maksāšanas metode tiek lietota rēķinam tikai tad, ja apgrieztās maksāšanas krājumu grupā ietverto preču un/vai pakalpojumu vērtība pārsniedz šajā laukā norādīto ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="a240a-149">**Threshold amount** – The Reverse Charge schema is applied to an invoice only if the value of items and/or services that are included in the reverse charge item group exceeds the limit that you specify here.</span></span>

<span data-ttu-id="a240a-150">Varat arī izmantot laukus **Spēkā stāšanās datums** un **Beigu datums**, lai definētu kārtulas darbības periodu.</span><span class="sxs-lookup"><span data-stu-id="a240a-150">You can also use the **Effective date** and **Expiration date** fields to define the period when the rule is effective.</span></span>

<span data-ttu-id="a240a-151">Varat arī norādīt to, vai gadījumā, ja ir izpildīts dokumenta rindas nosacījums, tiek parādīts paziņojums un šī rinda tiek atjaunināta, izmantojot noklusējuma apgrieztā PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="a240a-151">Additionally, you can specify whether a notification appears and the document line is updated with the default reverse charge sales tax group if the condition for that document line is met.</span></span> <span data-ttu-id="a240a-152">Pieejamas šādas opcijas</span><span class="sxs-lookup"><span data-stu-id="a240a-152">The following options are available:</span></span>

- <span data-ttu-id="a240a-153">**Nav** — dokumenta rinda netiek atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="a240a-153">**None** – The document line isn't updated.</span></span>
- <span data-ttu-id="a240a-154">**Uzvedne** — tiek parādīts paziņojums, lai apstiprinātu, ka var lietot apgriezto maksāšanu.</span><span class="sxs-lookup"><span data-stu-id="a240a-154">**Prompt** – A notification appears to confirm that the reverse charge can be applied.</span></span>
- <span data-ttu-id="a240a-155">**Iestatīt** — dokumenta rinda tiek atjaunināta bez papildu paziņojuma.</span><span class="sxs-lookup"><span data-stu-id="a240a-155">**Set** – The document line is updated without additional notification.</span></span>

## <a name="set-up-default-parameters"></a><span data-ttu-id="a240a-156">Noklusējuma parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a240a-156">Set up default parameters</span></span>
<span data-ttu-id="a240a-157">Lai iespējotu funkcionalitāti attiecībā uz apgriezto PVN, lapas **Virsgrāmatas parametri** cilnē **Atgriezes maksa** iestatiet opcijas **Aktivizēt apgriezto maksu** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a240a-157">To enable the functionality for reverse charge VAT, on the **General ledger parameters** page, on the **Reverse charge** tab, set the **Enable reverse charge** option to **Yes**.</span></span> <span data-ttu-id="a240a-158">Laukos **Pirkšanas pasūtījuma PVN grupa** un **Pārdošanas pasūtījuma PVN grupa** atlasiet noklusējuma PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="a240a-158">In the **Purchase order sales tax group** and **Sales order tax group** fields, select the default sales tax groups.</span></span> <span data-ttu-id="a240a-159">Ja ir izpildīts apgrieztās maksāšanas piemērotības nosacījums, pārdošanas vai pirkšanas rinda tiek atjaunināta, izmantojot šīs PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="a240a-159">When a reverse charge applicability condition is met, the sales or purchase order line is updated with these sales tax groups.</span></span>

## <a name="reverse-charge-on-a-sales-invoice"></a><span data-ttu-id="a240a-160">Apgrieztā maksāšana pārdošanas rēķinā</span><span class="sxs-lookup"><span data-stu-id="a240a-160">Reverse charge on a sales invoice</span></span>
<span data-ttu-id="a240a-161">Ja pārdošanai tiek izmantota apgrieztās maksāšanas metode, pārdevējs neiekasē PVN.</span><span class="sxs-lookup"><span data-stu-id="a240a-161">For sales under the Reverse Charge schema, the seller doesn't charge VAT.</span></span> <span data-ttu-id="a240a-162">Tā vietā rēķinā ir norādīti gan krājumi, uz kuriem attiecas apgrieztais PVN, gan apgrieztā PVN kopsumma.</span><span class="sxs-lookup"><span data-stu-id="a240a-162">Instead, the invoice indicates both the items that are subject to the reverse charge VAT and the total amount of the reverse charge VAT.</span></span>

<span data-ttu-id="a240a-163">Kad tiek grāmatots pārdošanas rēķins, kurā ir ietverta apgrieztā maksāšana, PVN transakciju nodokļa virziens ir **Maksājamais PVN**, tām ir PVN nulles likme un tiek atzīmēta izvēles rūtiņa **Atgriezes maksa**.</span><span class="sxs-lookup"><span data-stu-id="a240a-163">When a sales invoice that has the reverse charge is posted, the sales tax transactions have the **Sales tax payable** tax direction and zero sales tax, and the **Reverse charge** check box is selected.</span></span>

## <a name="reverse-charge-on-a-purchase-invoice"></a><span data-ttu-id="a240a-164">Apgrieztā maksāšana pirkšanas rēķinā</span><span class="sxs-lookup"><span data-stu-id="a240a-164">Reverse charge on a purchase invoice</span></span>
<span data-ttu-id="a240a-165">Ja pirkšanai tiek izmantota apgrieztās maksāšanas metode, pircējs, kurš saņem apgrieztajai maksāšanai paredzēto rēķinu, pilda gan pārdevēja, gan pircēja PVN uzskaites pienākumus.</span><span class="sxs-lookup"><span data-stu-id="a240a-165">For purchases under the Reverse Charge schema, the purchaser who receives the invoice that has the reverse charge acts as a buyer and a seller for VAT accounting purposes.</span></span>

<span data-ttu-id="a240a-166">Kad tiek grāmatots pirkšanas rēķins, kurā ir ietverta apgrieztā maksāšana, tiek izveidotas divas PVN transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a240a-166">When a purchase invoice that has the reverse charge is posted, two sales tax transactions are created.</span></span> <span data-ttu-id="a240a-167">Vienas transakcijas nodokļu virziens ir **Saņemtais PVN**.</span><span class="sxs-lookup"><span data-stu-id="a240a-167">One transaction has the **Sales tax receivable** tax direction.</span></span> <span data-ttu-id="a240a-168">Otras transakcijas nodokļu virziens ir **Maksājamais PVN**, un tai ir atzīmēta izvēles rūtiņa **Atgriezes maksa**.</span><span class="sxs-lookup"><span data-stu-id="a240a-168">The other transaction has the **Sales tax payable** tax direction, and the **Reverse charge** check box is selected.</span></span>

<span data-ttu-id="a240a-169">Tālāk redzamajā ekrānuzņēmumā vienai transakcijai ir virziens **Saņemtais PVN** un otrai transakcijai — virziens **Maksājamais PVN**.</span><span class="sxs-lookup"><span data-stu-id="a240a-169">In the following screenshot, one transaction has the **Sales tax receivable** direction, and the other transaction has the **Sales tax payable** direction.</span></span> 

![Grāmatotais PVN](media/apac-sau-posted-sales-tax.png)
