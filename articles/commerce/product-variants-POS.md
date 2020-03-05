---
title: Krājumu uzmeklēšana pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstītas opcijas, kas ir pieejamas krājumu informācijas apskatīšanai pārdošanas punktā (Point of Sale — POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 1d6133d80d7674a1d896bc19a743a6bd4d0fb40f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023331"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="29441-103">Krājumu uzmeklēšana pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="29441-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="29441-104">Krājumu pārlūkošana pārdošanas punktā (POS) palīdz mazumtirgotājiem sasniegt reāllaika operatīvo izcilību un gūt ieskatus, savienojot veikalus, POS un dokumentu apstrādes biroju.</span><span class="sxs-lookup"><span data-stu-id="29441-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="29441-105">Šī funkcionalitāte nodrošina precīzu reāllaika skatu uz preču krājumiem dažādos veikalos un vairumtirdzniecības bāzēs.</span><span class="sxs-lookup"><span data-stu-id="29441-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="29441-106">Tā arī palīdz mazumtirgotājiem uzlabot efektivitāti un izmaksu ietaupījumus, uzlabojot krājumu plānošanu reālajā laikā.</span><span class="sxs-lookup"><span data-stu-id="29441-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="29441-107">Precīzs reāllaika skats uz krājumiem visā organizācijā palīdz veikala darbiniekiem nodrošināt laicīgu un izcilu klientu apkalpošanu.</span><span class="sxs-lookup"><span data-stu-id="29441-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="29441-108">Šīm iespējām vislielākā nozīme ir brīdī, kad debitors ir gatavs pieņemt lēmumu par pirkumu.</span><span class="sxs-lookup"><span data-stu-id="29441-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="29441-109">Ir svarīgi, lai kasieriem veikalā pie rokas būtu informācija par reālā laika krājumiem un viņi varētu dot precīzus solījumus par preču piegādi un savākšanu.</span><span class="sxs-lookup"><span data-stu-id="29441-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="29441-110">Varat atvērt lapu **Krājumu pārlūkošana** darbvietā **Retail Modern POS** vai darbvietā **Retail Cloud POS**.</span><span class="sxs-lookup"><span data-stu-id="29441-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Krājumu pārlūkošanas elements POS sākumlapā](media/POSHomepage.png)

<span data-ttu-id="29441-112">Lapā **Krājumu pārlūkošana** varat izmantot cipartastatūru, lai ievadītu preces numuru.</span><span class="sxs-lookup"><span data-stu-id="29441-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="29441-113">Pēc tam varat skatīt rīcībā esošo daudzumu vairākiem veikaliem un noliktavām.</span><span class="sxs-lookup"><span data-stu-id="29441-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standarta krājumu pārlūkošanas lapa](media/InventoryLookUp.png)

<span data-ttu-id="29441-115">Katrai vietai tiek rādīts arī daudzums **Rezervēts** un **Pasūtīts**.</span><span class="sxs-lookup"><span data-stu-id="29441-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="29441-116">**Rezervēts** — šis daudzums attiecas uz vērtību **Fiziski rezervēts** no dokumentu apstrādes biroja attiecībā uz norādīto preces numuru attiecīgajā vietā.</span><span class="sxs-lookup"><span data-stu-id="29441-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="29441-117">**Pasūtīts** — šis daudzums attiecas uz vērtību **Pasūtīts kopā** no dokumentu apstrādes biroja attiecībā uz norādīto preces numuru attiecīgajā vietā.</span><span class="sxs-lookup"><span data-stu-id="29441-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="29441-118">Vietas, kurām tiek rādīta informācija par krājumu pieejamību</span><span class="sxs-lookup"><span data-stu-id="29441-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="29441-119">Šajā vietu sarakstā ir divu tālāk aprakstīto tipu elementi.</span><span class="sxs-lookup"><span data-stu-id="29441-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="29441-120">**Veikali** — sarakstā tiek rādīti veikali, kas tiek konfigurēti, izmantojot veikalu vietrāžu grupu pašreizējam veikalam programmā Headquarters.</span><span class="sxs-lookup"><span data-stu-id="29441-120">**Stores** – The list shows stores that are configured by using the store locator group for the current store in the Headquarters.</span></span>
- <span data-ttu-id="29441-121">**Sadales centri** — programmā Commerce var konfigurēt dažādus sadales centru veidus (piemēram, noliktavas).</span><span class="sxs-lookup"><span data-stu-id="29441-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Commerce.</span></span> <span data-ttu-id="29441-122">Taču šajā sarakstā tiek rādīta informācija par krājumu pieejamību tikai vairumtirdzniecības bāzēm ar noklusējuma tipu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="29441-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29441-123">Informācija par krājumu pieejamību netiek rādīta noliktavām ar POS tipu **Tranzīts**, **Karantīna** un **Preces ceļā**.</span><span class="sxs-lookup"><span data-stu-id="29441-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="29441-124">Lapā **Krājumu pārlūkošana** varat skatīt daudzumus Pieejams solīšanai (Available to Promise — ATP) katram veikalam, kā arī pašreizējos rīcībā esošos daudzumus, rezervētos daudzumus un pasūtītos daudzumus.</span><span class="sxs-lookup"><span data-stu-id="29441-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="29441-125">Atlasiet veikalu, kam vēlaties skatīt ATP informāciju, un pēc tam atlasiet vienumu **Rādīt veikalu pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="29441-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP daudzumi](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="29441-127">No dimensijas atkarīgas matricas skata atvēršana, lai rādītu visus variantus</span><span class="sxs-lookup"><span data-stu-id="29441-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="29441-128">Preces šablona lapā **Informācija par preci** vai lapā **Krājumu pārlūkošana** no programmas joslas lapas apakšā atlasiet vienumu **Skatīt visus variantus**.</span><span class="sxs-lookup"><span data-stu-id="29441-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="29441-129">Skatā **No dimensijas atkarīga matrica** sākotnējai palaišanai no šīm lapām tiek rādīta informācija par krājumu pieejamību visiem pašreizējā veikala preces varantiem.</span><span class="sxs-lookup"><span data-stu-id="29441-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="29441-130">Poga **Skatīt visus variantus** ir pieejama tikai tādiem krājumu preču šabloniem, kam ir preču varianti.</span><span class="sxs-lookup"><span data-stu-id="29441-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="29441-131">Tā nav pieejama savrupām precēm vai komplektiem.</span><span class="sxs-lookup"><span data-stu-id="29441-131">It isn't available for standalone products or kits.</span></span>

![Poga “Skatīt visus variantus” krājumu meklēšanas lapā](media/StandardToMatrix.png)

<span data-ttu-id="29441-133">Atlasiet vienumu **Skatīt visus variantus** preces šablona lapā **Informācija par preci** vai lapā **Krājumu pārlūkošana**, neatlasot atrašanās vietu, lai pārietu uz skatu **No dimensijas atkarīga matrica** un redzētu informāciju par krājumu pieejamību visiem preces variantiem pašreizējā veikalā.</span><span class="sxs-lookup"><span data-stu-id="29441-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Skats “No dimensijas atkarīga matrica” krājumu pārlūkošanas lapai](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="29441-135">Iepriekšējā attēlā dimensiju rādīšanas secība ir pēc alfabēta, jo dimensiju rādīšanas secība atlasītajai precei nebija konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="29441-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="29441-136">Skata **No dimensijas atkarīga matrica** preču variantu šūnās labajā apakšējā stūrī ir rīcībā esošā vērtība.</span><span class="sxs-lookup"><span data-stu-id="29441-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="29441-137">Nākamajā tabulā ir paskaidrota dažādo vērtību nozīme.</span><span class="sxs-lookup"><span data-stu-id="29441-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="29441-138">Rīcībā esošā vērtība</span><span class="sxs-lookup"><span data-stu-id="29441-138">On-hand value</span></span>                            | <span data-ttu-id="29441-139">Apraksts</span><span class="sxs-lookup"><span data-stu-id="29441-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="29441-140">Skaitliska vērtība, kas ir lielāka par 0 (nulle)</span><span class="sxs-lookup"><span data-stu-id="29441-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="29441-141">Uz atlasīto vietu ir izlaists variants, un šajā šūnā jūs varat veikt arī papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="29441-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="29441-142">(Šīs darbības ir detalizētāk aprakstītas tālāk šajā tēmā.)</span><span class="sxs-lookup"><span data-stu-id="29441-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="29441-143">**0** (nulle)</span><span class="sxs-lookup"><span data-stu-id="29441-143">**0** (zero)</span></span>                             | <span data-ttu-id="29441-144">Uz atlasīto vietu ir izlaists variants, bet krājums atlasītajā vietā nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="29441-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="29441-145">Taču šajā šūnā varat veikt papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="29441-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="29441-146">(Šīs darbības ir detalizētāk aprakstītas tālāk šajā tēmā.)</span><span class="sxs-lookup"><span data-stu-id="29441-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="29441-147">**Nav datu** vai neaktīva šūna</span><span class="sxs-lookup"><span data-stu-id="29441-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="29441-148">Uz atlasīto vietu nav izlaists neviens variants, un šajā šūnā jūs nevarat veikt papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="29441-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="29441-149">Varat arī mainīt dimensiju rakursu, atlasot jaunas izmantojamās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="29441-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Rakursa maiņa](media/ChangePivot.png)

![Rakurss ir mainīts](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="29441-152">Iepriekšējos attēlos atlasīto preču dimensiju rādīšanas secība ir pielāgota (nav pēc alfabēta).</span><span class="sxs-lookup"><span data-stu-id="29441-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="29441-153">Tā ir balstīta uz dokumentu apstrādes birojā iestatīto dimensiju parādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="29441-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="29441-154">Turklāt skatā **No dimensijas atkarīga matrica** var veikt arī citas darbības, lai palīdzētu uzlabot veikala darbinieku produktivitāti.</span><span class="sxs-lookup"><span data-stu-id="29441-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="29441-155">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="29441-155">Here are some examples:</span></span>

- <span data-ttu-id="29441-156">Mainīt veikala atrašanās vietu, lai uzmeklētu krājumu pieejamību visiem preču variantiem citās vietās.</span><span class="sxs-lookup"><span data-stu-id="29441-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="29441-157">Šīs atrašanās vietas tostarp ir citi veikali attiecīgajā veikala vietrāžu grupā un vairumtirdzniecības bāzes ar noklusējuma tipu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="29441-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="29441-158">Pārdot atsevišķu preces variantu kādam debitoram, izmantojot skaidru naudu un pārnešnu, saņemšanu veikalā vai nosūtīšanu uz kādu adresi.</span><span class="sxs-lookup"><span data-stu-id="29441-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="29441-159">Debitoram nodrošināt ATP informāciju par atsevišķu preces variantu noteiktā vietā.</span><span class="sxs-lookup"><span data-stu-id="29441-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Papildu darbības variantu elementi](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="29441-161">Iepriekšējā attēlā dimensiju rādīšanas secība ir pēc alfabēta, jo dimensiju rādīšanas secība atlasītajai precei nebija konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="29441-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="29441-162">Nākamajā tabulā ir plašāka informācija par pieejamajām papildu darbībām.</span><span class="sxs-lookup"><span data-stu-id="29441-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="29441-163">Darbība</span><span class="sxs-lookup"><span data-stu-id="29441-163">Action</span></span>               | <span data-ttu-id="29441-164">Apraksts</span><span class="sxs-lookup"><span data-stu-id="29441-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="29441-165">Pārdot tagad</span><span class="sxs-lookup"><span data-stu-id="29441-165">Sell now</span></span>             | <span data-ttu-id="29441-166">Atlasīto preces variantu pievienot transakcijai un lietotāju novirzīt uz transakcijas ekrānu.</span><span class="sxs-lookup"><span data-stu-id="29441-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="29441-167">(Šī darbība nav pieejama, ja atlasītā atrašanās vieta ir vairumtirdzniecības bāze.)</span><span class="sxs-lookup"><span data-stu-id="29441-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="29441-168">Saņemšana veikalā</span><span class="sxs-lookup"><span data-stu-id="29441-168">Pick up in store</span></span>     | <span data-ttu-id="29441-169">Izveidot debitora pasūtījumu preces variantam, kas tiks saņemts no atlasītās atrašanās vietas, un lietotāju novirzīt uz transakcijas ekrānu.</span><span class="sxs-lookup"><span data-stu-id="29441-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="29441-170">(Šī darbība nav pieejama, ja atlasītā atrašanās vieta ir vairumtirdzniecības bāze.)</span><span class="sxs-lookup"><span data-stu-id="29441-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="29441-171">Nosūtīt preci</span><span class="sxs-lookup"><span data-stu-id="29441-171">Ship product</span></span>         | <span data-ttu-id="29441-172">Izveidot debitora pasūtījumu preces variantam, kas tiks nosūtīts no atlasītās atrašanās vietas, un lietotāju novirzīt uz transakcijas ekrānu.</span><span class="sxs-lookup"><span data-stu-id="29441-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="29441-173">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="29441-173">Availability</span></span>         | <span data-ttu-id="29441-174">Rādīt ATP informāciju atlasītajai variantu kombinācijai attiecībā uz atlasīto atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="29441-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="29441-175">Rādīt visas vietas</span><span class="sxs-lookup"><span data-stu-id="29441-175">Show all locations</span></span>   | <span data-ttu-id="29441-176">Pārslēgties uz standarta krājumu pārlūkošanas skatu un izcelt informāciju par krājumu pieejamību attiecībā uz nepieciešamo krājumu variantu visos veikalos šajā veikalu vietrāžu grupā, kā arī vairumtirdzniecības bāzēs ar tipu **Standarta/noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="29441-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="29441-177">Skatīt detalizētu informāciju par preci</span><span class="sxs-lookup"><span data-stu-id="29441-177">View product details</span></span> | <span data-ttu-id="29441-178">Novirzīt lietotāju uz saistītā preces šablona lapu **Informācija par preci**.</span><span class="sxs-lookup"><span data-stu-id="29441-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |