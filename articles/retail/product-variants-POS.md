---
title: "Krājumu pārlūkošana pārdošanas punktā"
description: "Šajā tēmā ir aprakstītas opcijas, kas ir pieejamas krājumu informācijas apskatīšanai pārdošanas punktā (Point of Sale — POS)."
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 933875f56b0f47990cb1cb767f84b23b9c9710d4
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="inventory-lookup-in-the-point-of-sale"></a><span data-ttu-id="fb7e5-103">Krājumu pārlūkošana pārdošanas punktā</span><span class="sxs-lookup"><span data-stu-id="fb7e5-103">Inventory lookup in the Point of Sale</span></span> 

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="fb7e5-104">Krājumu pārlūkošana pārdošanas punktā (POS) palīdz mazumtirgotājiem sasniegt reāllaika operatīvo izcilību un gūt ieskatus, savienojot veikalus, POS un dokumentu apstrādes biroju.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="fb7e5-105">Šī funkcionalitāte nodrošina precīzu reāllaika skatu uz preču krājumiem dažādos veikalos un vairumtirdzniecības bāzēs.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="fb7e5-106">Tā arī palīdz mazumtirgotājiem uzlabot efektivitāti un izmaksu ietaupījumus, uzlabojot krājumu plānošanu reālajā laikā.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="fb7e5-107">Precīzs reāllaika skats uz krājumiem visā organizācijā palīdz veikala darbiniekiem nodrošināt laicīgu un izcilu klientu apkalpošanu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="fb7e5-108">Šīm iespējām vislielākā nozīme ir brīdī, kad debitors ir gatavs pieņemt lēmumu par pirkumu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="fb7e5-109">Ir svarīgi, lai kasieriem veikalā pie rokas būtu informācija par reālā laika krājumiem un viņi varētu dot precīzus solījumus par preču piegādi un savākšanu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="fb7e5-110">Lapu **Krājumu pārlūkošana** varat atvērt no darbvietas **Retail Modern POS** vai no darbvietas **Retail Cloud POS**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Krājumu pārlūkošanas elements POS sākumlapā](media/POSHomepage.png)

<span data-ttu-id="fb7e5-112">Lapā **Krājumu pārlūkošana** varat izmantot cipartastatūru, lai ievadītu preces numuru.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="fb7e5-113">Pēc tam varat skatīt rīcībā esošo daudzumu vairākiem veikaliem un noliktavām.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standarta krājumu pārlūkošanas lapa](media/InventoryLookUp.png)

<span data-ttu-id="fb7e5-115">Katrai vietai tiek rādīts arī daudzums **Rezervēts** un **Pasūtīts**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="fb7e5-116">**Rezervēts** — šis daudzums attiecas uz vērtību **Fiziski rezervēts** no dokumentu apstrādes biroja attiecībā uz norādīto preces numuru attiecīgajā vietā.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="fb7e5-117">**Pasūtīts** — šis daudzums attiecas uz vērtību **Pasūtīts kopā** no dokumentu apstrādes biroja attiecībā uz norādīto preces numuru attiecīgajā vietā.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="fb7e5-118">Vietas, kurām tiek rādīta informācija par krājumu pieejamību</span><span class="sxs-lookup"><span data-stu-id="fb7e5-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="fb7e5-119">Šajā vietu sarakstā ir divu tālāk aprakstīto tipu elementi.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="fb7e5-120">**Mazumtirdzniecības veikali** — sarakstā tiek rādīti veikali, kas tiek konfigurēti, izmantojot veikalu vietrāžu grupu pašreizējam veikalam programmā Retail Headquarters.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span> 
- <span data-ttu-id="fb7e5-121">**Vairumtirdzniecības bāzes** — programmatūrā Microsoft Dynamics 365 for Retail var konfigurēt dažādu tipu vairumtirdzniecības bāzes (piemēram, noliktavas).</span><span class="sxs-lookup"><span data-stu-id="fb7e5-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="fb7e5-122">Taču šajā sarakstā tiek rādīta informācija par krājumu pieejamību tikai vairumtirdzniecības bāzēm ar noklusējuma tipu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fb7e5-123">Informācija par krājumu pieejamību netiek rādīta noliktavām ar POS tipu **Tranzīts**, **Karantīna** un **Preces ceļā**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="fb7e5-124">Lapā **Krājumu pārlūkošana** varat skatīt daudzumus Pieejams solīšanai (Available to Promise — ATP) katram veikalam, kā arī pašreizējos rīcībā esošos daudzumus, rezervētos daudzumus un pasūtītos daudzumus.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="fb7e5-125">Atlasiet veikalu, kam vēlaties skatīt ATP informāciju, un pēc tam atlasiet vienumu **Rādīt veikalu pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP daudzumi](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="fb7e5-127">No dimensijas atkarīgas matricas skata atvēršana, lai rādītu visus variantus</span><span class="sxs-lookup"><span data-stu-id="fb7e5-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="fb7e5-128">Preces šablona lapā **Informācija par preci** vai lapā **Krājumu pārlūkošana** no programmas joslas lapas apakšā atlasiet vienumu **Skatīt visus variantus**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="fb7e5-129">Skatā **No dimensijas atkarīga matrica** sākotnējai palaišanai no šīm lapām tiek rādīta informācija par krājumu pieejamību visiem pašreizējā veikala preces varantiem.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="fb7e5-130">Poga **Skatīt visus variantus** ir pieejama tikai tādiem krājumu preču šabloniem, kam ir preču varianti.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="fb7e5-131">Tā nav pieejama savrupām precēm vai komplektiem.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-131">It isn't available for standalone products or kits.</span></span>

![Poga “Skatīt visus variantus” krājumu meklēšanas lapā](media/StandardToMatrix.png)

<span data-ttu-id="fb7e5-133">Atlasiet vienumu **Skatīt visus variantus** preces šablona lapā **Informācija par preci** vai lapā **Krājumu pārlūkošana**, neatlasot atrašanās vietu, lai pārietu uz skatu **No dimensijas atkarīga matrica** un redzētu informāciju par krājumu pieejamību visiem preces variantiem pašreizējā veikalā.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Skats “No dimensijas atkarīga matrica” krājumu pārlūkošanas lapai](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="fb7e5-135">Iepriekšējā attēlā dimensiju rādīšanas secība ir pēc alfabēta, jo dimensiju rādīšanas secība atlasītajai precei nebija konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="fb7e5-136">Skata **No dimensijas atkarīga matrica** preču variantu šūnās labajā apakšējā stūrī ir rīcībā esošā vērtība.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="fb7e5-137">Nākamajā tabulā ir paskaidrota dažādo vērtību nozīme.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="fb7e5-138">Rīcībā esošā vērtība</span><span class="sxs-lookup"><span data-stu-id="fb7e5-138">On-hand value</span></span>                            | <span data-ttu-id="fb7e5-139">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fb7e5-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="fb7e5-140">Skaitliska vērtība, kas ir lielāka par 0 (nulle)</span><span class="sxs-lookup"><span data-stu-id="fb7e5-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="fb7e5-141">Uz atlasīto vietu ir izlaists variants, un šajā šūnā jūs varat veikt arī papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="fb7e5-142">(Šīs darbības ir detalizētāk aprakstītas tālāk šajā tēmā.)</span><span class="sxs-lookup"><span data-stu-id="fb7e5-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="fb7e5-143">**0** (nulle)</span><span class="sxs-lookup"><span data-stu-id="fb7e5-143">**0** (zero)</span></span>                             | <span data-ttu-id="fb7e5-144">Uz atlasīto vietu ir izlaists variants, bet krājums atlasītajā vietā nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="fb7e5-145">Taču šajā šūnā varat veikt papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="fb7e5-146">(Šīs darbības ir detalizētāk aprakstītas tālāk šajā tēmā.)</span><span class="sxs-lookup"><span data-stu-id="fb7e5-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="fb7e5-147">**Nav datu** vai neaktīva šūna</span><span class="sxs-lookup"><span data-stu-id="fb7e5-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="fb7e5-148">Uz atlasīto vietu nav izlaists neviens variants, un šajā šūnā jūs nevarat veikt papildu darbības.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="fb7e5-149">Varat arī mainīt dimensiju rakursu, atlasot jaunas izmantojamās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span> 

![Rakursa maiņa](media/ChangePivot.png)

![Rakurss ir mainīts](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="fb7e5-152">Iepriekšējos attēlos atlasīto preču dimensiju rādīšanas secība ir pielāgota (nav pēc alfabēta).</span><span class="sxs-lookup"><span data-stu-id="fb7e5-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="fb7e5-153">Tā ir balstīta uz dokumentu apstrādes birojā iestatīto dimensiju parādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="fb7e5-154">Turklāt skatā **No dimensijas atkarīga matrica** var veikt arī citas darbības, lai palīdzētu uzlabot veikala darbinieku produktivitāti.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="fb7e5-155">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="fb7e5-155">Here are some examples:</span></span>

- <span data-ttu-id="fb7e5-156">Mainīt veikala atrašanās vietu, lai uzmeklētu krājumu pieejamību visiem preču variantiem citās vietās.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="fb7e5-157">Šīs atrašanās vietas tostarp ir citi veikali attiecīgajā veikala vietrāžu grupā un vairumtirdzniecības bāzes ar noklusējuma tipu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="fb7e5-158">Pārdot atsevišķu preces variantu kādam debitoram, izmantojot skaidru naudu un pārnešnu, saņemšanu veikalā vai nosūtīšanu uz kādu adresi.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="fb7e5-159">Debitoram nodrošināt ATP informāciju par atsevišķu preces variantu noteiktā vietā.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Papildu darbības variantu elementi](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="fb7e5-161">Iepriekšējā attēlā dimensiju rādīšanas secība ir pēc alfabēta, jo dimensiju rādīšanas secība atlasītajai precei nebija konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="fb7e5-162">Nākamajā tabulā ir plašāka informācija par pieejamajām papildu darbībām.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-162">The following table provides more information about the additional actions that are available.</span></span>


|        <span data-ttu-id="fb7e5-163">Darbība</span><span class="sxs-lookup"><span data-stu-id="fb7e5-163">Action</span></span>        |                                                                                                                    <span data-ttu-id="fb7e5-164">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fb7e5-164">Description</span></span>                                                                                                                    |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       <span data-ttu-id="fb7e5-165">Pārdot tagad</span><span class="sxs-lookup"><span data-stu-id="fb7e5-165">Sell now</span></span>       |                               <span data-ttu-id="fb7e5-166">Atlasīto preces variantu pievienot transakcijai un lietotāju novirzīt uz transakcijas ekrānu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="fb7e5-167">(Šī darbība nav pieejama, ja atlasītā atrašanās vieta ir vairumtirdzniecības bāze.)</span><span class="sxs-lookup"><span data-stu-id="fb7e5-167">(This action isn't available when the selected location is a distribution center.)</span></span>                               |
|   <span data-ttu-id="fb7e5-168">Saņemšana veikalā</span><span class="sxs-lookup"><span data-stu-id="fb7e5-168">Pick up in store</span></span>   |      <span data-ttu-id="fb7e5-169">Izveidot debitora pasūtījumu preces variantam, kas tiks saņemts no atlasītās atrašanās vietas, un lietotāju novirzīt uz transakcijas ekrānu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="fb7e5-170">(Šī darbība nav pieejama, ja atlasītā atrašanās vieta ir vairumtirdzniecības bāze.)</span><span class="sxs-lookup"><span data-stu-id="fb7e5-170">(This action isn't available when the selected location is a distribution center.)</span></span>       |
|     <span data-ttu-id="fb7e5-171">Nosūtīt preci</span><span class="sxs-lookup"><span data-stu-id="fb7e5-171">Ship product</span></span>     |                                                 <span data-ttu-id="fb7e5-172">Izveidot debitora pasūtījumu preces variantam, kas tiks nosūtīts no atlasītās atrašanās vietas, un lietotāju novirzīt uz transakcijas ekrānu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span>                                                 |
|     <span data-ttu-id="fb7e5-173">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="fb7e5-173">Availability</span></span>     |                                                                             <span data-ttu-id="fb7e5-174">Rādīt ATP informāciju atlasītajai variantu kombinācijai attiecībā uz atlasīto atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-174">Show the ATP information for the selected variant combination for the selected location.</span></span>                                                                              |
|  <span data-ttu-id="fb7e5-175">Rādīt visas vietas</span><span class="sxs-lookup"><span data-stu-id="fb7e5-175">Show all locations</span></span>  | <span data-ttu-id="fb7e5-176">Pārslēgties uz standarta krājumu pārlūkošanas skatu un izcelt informāciju par krājumu pieejamību attiecībā uz nepieciešamo krājumu variantu visos veikalos šajā veikalu vietrāžu grupā, kā arī vairumtirdzniecības bāzēs ar tipu <strong>Standarta/noklusējuma</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the <strong>Standard/Default</strong> type.</span></span> |
| <span data-ttu-id="fb7e5-177">Skatīt detalizētu informāciju par preci</span><span class="sxs-lookup"><span data-stu-id="fb7e5-177">View product details</span></span> |                                                                         <span data-ttu-id="fb7e5-178">Novirzīt lietotāju uz saistītā preces šablona lapu <strong>Informācija par preci</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb7e5-178">Redirect the user to the <strong>Product details</strong> page of the associated product master.</span></span>                                                                          |


