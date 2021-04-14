---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā tēmā ir sniegta informācija par to, kā pārbaudīt krājumu pieejamību duālajā ierakstā.
author: yijialuan
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748569"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="c7fab-103">Krājumu pieejamība duālajā ierakstā</span><span class="sxs-lookup"><span data-stu-id="c7fab-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7fab-104">Izmantojot krājumu pieejamību, varat pārbaudīt krājumus pirms preču pievienošanas lapā **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** programmā Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="c7fab-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="c7fab-105">Piemēram, krājumu pārbaude un izpildes datuma noteikšana ir galvenais uzdevums procesā [no potenciālā klienta līdz skaidrai naudai](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="c7fab-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="c7fab-106">Ja nav pietiekami daudz krājumu, varat aplēst piegādes datumu, pamatojoties uz prognozēto krājumu saņemšanas un izsniegšanas plūsmām.</span><span class="sxs-lookup"><span data-stu-id="c7fab-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="c7fab-107">Varat arī pārbaudīt preces pieejams solīšanai (ATP) informāciju, kur varat atrast ATP daudzumu iepriekš definētā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="c7fab-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="c7fab-108">Rīcībā esošie krājumi</span><span class="sxs-lookup"><span data-stu-id="c7fab-108">On-hand inventory</span></span>

<span data-ttu-id="c7fab-109">Dynamics 365 Sales **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** lapu galvenē ir pievienota jauna poga **Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="c7fab-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="c7fab-110">Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu un preci, kurai vēlaties pārbaudīt rīcībā esošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="c7fab-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="c7fab-111">Šis dialoglodziņš parāda to pašu informāciju, ko [rīcībā esošie krājumi](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="c7fab-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="c7fab-112">Dialoglodziņā tiek atgriezta informācija par krājumiem no Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7fab-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c7fab-113">Šajā informācijā ir iekļauti tālāk norādītie daudzumi:</span><span class="sxs-lookup"><span data-stu-id="c7fab-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="c7fab-114">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-114">On-hand quantity</span></span>
- <span data-ttu-id="c7fab-115">Rezervētais rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="c7fab-116">Pieejamais rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-116">Available on-hand quantity</span></span>
- <span data-ttu-id="c7fab-117">Pasūtītais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-117">Ordered quantity</span></span>
- <span data-ttu-id="c7fab-118">Pasūtījumā iekļautais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-118">On-order quantity</span></span>
- <span data-ttu-id="c7fab-119">Rezervētais pasūtītais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="c7fab-120">Kopējais pieejamais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="c7fab-121">ATP informācija</span><span class="sxs-lookup"><span data-stu-id="c7fab-121">ATP information</span></span>

<span data-ttu-id="c7fab-122">Programmā Sales ir pievienota jauna **ATP informācija**, kas ir pievienota rindas precēm **Piedāvājumu**, **Pasūtījumu** un **Rēķinu** lapās.</span><span class="sxs-lookup"><span data-stu-id="c7fab-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="c7fab-123">Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu, preci, krājuma atrašanās vietu, krājuma noliktavu un krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="c7fab-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="c7fab-124">Šim dialoglodziņam ir tie paši iestatījumi, kas aprakstīti [Pasūtījumu solīšanā](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="c7fab-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="c7fab-125">Dialoglodziņā tiek atgriezta ATP informācija no Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7fab-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="c7fab-126">Šajā informācijā ir iekļauti tālāk norādītie daudzumi:</span><span class="sxs-lookup"><span data-stu-id="c7fab-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="c7fab-127">ATP daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-127">ATP quantity</span></span>
- <span data-ttu-id="c7fab-128">Ieejas plūsmas daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-128">Receipt quantity</span></span>
- <span data-ttu-id="c7fab-129">Izejas plūsmas daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-129">Issue quantity</span></span>
- <span data-ttu-id="c7fab-130">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="c7fab-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="c7fab-131">Kā tas darbojas</span><span class="sxs-lookup"><span data-stu-id="c7fab-131">How it works</span></span>

<span data-ttu-id="c7fab-132">Atlasot pogu **Rīcībā esošie krājumi** lapā **Piedāvājumi**, **Pasūtījumi** vai **Rēķini**, **Rīcībā esošo krājumu API** tiek veikts tiešais duālās rakstīšanas izsaukums.</span><span class="sxs-lookup"><span data-stu-id="c7fab-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="c7fab-133">API aprēķina dotās preces rīcībā esošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="c7fab-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="c7fab-134">Rezultāts tiek glabāts tabulās **InventCDSInventoryOnHandRequestEntity** un **InventCDSInventoryOnHandEntryEntity**, tad to ieraksta programmā Dataverse duālā ieraksta formā.</span><span class="sxs-lookup"><span data-stu-id="c7fab-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="c7fab-135">Lai lietotu šo funkcionalitāti, ir jāpalaiž šādas duālās rakstīšanas kartes.</span><span class="sxs-lookup"><span data-stu-id="c7fab-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="c7fab-136">Izlaist sākotnējo sinhronizāciju, kad palaižat kartes.</span><span class="sxs-lookup"><span data-stu-id="c7fab-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="c7fab-137">CDS rīcībā esošo krājumu ieraksti (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="c7fab-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="c7fab-138">CDS rīcībā esošo krājumu pieprasījumi (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="c7fab-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="c7fab-139">Veidnes</span><span class="sxs-lookup"><span data-stu-id="c7fab-139">Templates</span></span>
<span data-ttu-id="c7fab-140">Rīcībā esošo krājumu datu atklāšanai ir pieejamas šādas veidnes.</span><span class="sxs-lookup"><span data-stu-id="c7fab-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="c7fab-141">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="c7fab-141">Finance and Operations apps</span></span> | <span data-ttu-id="c7fab-142">Customer engagement programma</span><span class="sxs-lookup"><span data-stu-id="c7fab-142">Customer engagement app</span></span> | <span data-ttu-id="c7fab-143">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c7fab-143">Description</span></span> 
---|---|---
[<span data-ttu-id="c7fab-144">CDS krājumu rīcībā esošie ieraksti</span><span class="sxs-lookup"><span data-stu-id="c7fab-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="c7fab-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="c7fab-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="c7fab-146">CDS krājumu rīcībā esošie pieprasījumi</span><span class="sxs-lookup"><span data-stu-id="c7fab-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="c7fab-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="c7fab-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="c7fab-148">CDS rīcībā esošo krājumu ieraksti (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="c7fab-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="c7fab-149">Šī veidne sinhronizē datus starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c7fab-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="c7fab-150">Finance and Operations lauks</span><span class="sxs-lookup"><span data-stu-id="c7fab-150">Finance and Operations field</span></span> | <span data-ttu-id="c7fab-151">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="c7fab-151">Map type</span></span> | <span data-ttu-id="c7fab-152">Lauks Customer engagement</span><span class="sxs-lookup"><span data-stu-id="c7fab-152">Customer engagement field</span></span> | <span data-ttu-id="c7fab-153">Noklusētā vērtība</span><span class="sxs-lookup"><span data-stu-id="c7fab-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="c7fab-154">CDS rīcībā esošo krājumu pieprasījumi (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="c7fab-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="c7fab-155">Šī veidne sinhronizē datus starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c7fab-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="c7fab-156">Finance and Operations lauks</span><span class="sxs-lookup"><span data-stu-id="c7fab-156">Finance and Operations field</span></span> | <span data-ttu-id="c7fab-157">Kartes veids</span><span class="sxs-lookup"><span data-stu-id="c7fab-157">Map type</span></span> | <span data-ttu-id="c7fab-158">Lauks Customer engagement</span><span class="sxs-lookup"><span data-stu-id="c7fab-158">Customer engagement field</span></span> | <span data-ttu-id="c7fab-159">Noklusētā vērtība</span><span class="sxs-lookup"><span data-stu-id="c7fab-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]