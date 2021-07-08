---
title: Importēt ienākošos IPPN, izmantojot V2 datu elementu
description: Šajā tēmā skaidrots, kā pārvaldīt ienākošo papildu paziņojumu par nosūtīšanu(IPPN) importu, izmantojot ienākošo IPPN V2 datu elementu.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249135"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="85e86-103">Importēt ienākošos IPPN, izmantojot V2 datu elementu</span><span class="sxs-lookup"><span data-stu-id="85e86-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85e86-104">Papildu paziņojums par nosūtīšanu (IPPN) jūs informē par kreditora piegādēm.</span><span class="sxs-lookup"><span data-stu-id="85e86-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="85e86-105">Tie palīdz sūtītājam aprakstīt sūtījuma saturu un papildu informāciju par to, piemēram, krājumiem un iepakojumu.</span><span class="sxs-lookup"><span data-stu-id="85e86-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="85e86-106">IPPN var palīdzēt noliktavas darbiniekiem uzzināt, kas notiek.</span><span class="sxs-lookup"><span data-stu-id="85e86-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="85e86-107">Tādēļ viņi var sagatavoties.</span><span class="sxs-lookup"><span data-stu-id="85e86-107">Therefore, they can prepare.</span></span> <span data-ttu-id="85e86-108">Turklāt noliktavas darbinieki var izmantot IPPN, lai saskaņotu nosūtīšanas informāciju ar iepriekš izveidoto saistīto pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="85e86-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="85e86-109">Šajā tēmā ir apkopoti scenāriji, kas, izmantojot piemērus, parāda, kā strādāt ar IPPN failiem.</span><span class="sxs-lookup"><span data-stu-id="85e86-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85e86-110">*Ienākošais IPPN* imports attiecas tikai uz krājumiem, kas ir iespējoti papildu noliktavu pārvaldību (WMS).</span><span class="sxs-lookup"><span data-stu-id="85e86-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="85e86-111">Pirms saņemat IPPN, pirkšanas pasūtījums sistēmā jāreģistrē kreditoram, kas sūta šo IPPN.</span><span class="sxs-lookup"><span data-stu-id="85e86-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="85e86-112">Ienākošais IPPN V2 elements</span><span class="sxs-lookup"><span data-stu-id="85e86-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="85e86-113">Jūs importējat ienākošos IPPN, izmantojot *Ienākošo IPPN V2* salikto datu elementu.</span><span class="sxs-lookup"><span data-stu-id="85e86-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="85e86-114">*Ienākošais IPPN V2* izmanto šādu entītiju priekšrocības:</span><span class="sxs-lookup"><span data-stu-id="85e86-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="85e86-115">Ienākošās kravas virsraksts</span><span class="sxs-lookup"><span data-stu-id="85e86-115">Inbound load header</span></span>
- <span data-ttu-id="85e86-116">Ienākošā sūtījuma virsraksts</span><span class="sxs-lookup"><span data-stu-id="85e86-116">Inbound shipment header</span></span>
- <span data-ttu-id="85e86-117">Ienākošo kravu iepakošanas struktūras</span><span class="sxs-lookup"><span data-stu-id="85e86-117">Inbound load packing structures</span></span>
- <span data-ttu-id="85e86-118">Ienākošo kravu iepakošanas struktūras gadījumi</span><span class="sxs-lookup"><span data-stu-id="85e86-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="85e86-119">Ienākošo kravu iepakošanas struktūras gadījumu rindas</span><span class="sxs-lookup"><span data-stu-id="85e86-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="85e86-120">Ienākošo kravu iepakošanas struktūras rindas</span><span class="sxs-lookup"><span data-stu-id="85e86-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="85e86-121">Saliktais datu elements *Ienākošais IPPN V2* ir paredzēts asinhroniem integrācijas scenārijiem, kuros tiek izmantoti XML faila pamatā esoši importi.</span><span class="sxs-lookup"><span data-stu-id="85e86-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="85e86-122">XML formāts IPPN importēšanai</span><span class="sxs-lookup"><span data-stu-id="85e86-122">XML format for importing ASNs</span></span>

<span data-ttu-id="85e86-123">Microsoft Dynamics 365 Supply Chain Management atbalsta šādu XML formātu IPPN importēšanai.</span><span class="sxs-lookup"><span data-stu-id="85e86-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="85e86-124">Katrs XML faila zars pārstāv atsevišķa elementa atribūtu.</span><span class="sxs-lookup"><span data-stu-id="85e86-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="85e86-125">Piemēri</span><span class="sxs-lookup"><span data-stu-id="85e86-125">Examples</span></span>

<span data-ttu-id="85e86-126">Tālāk dotās apakšsadaļas sniedz IPPN XML importa failu piemērus kreditora kravām.</span><span class="sxs-lookup"><span data-stu-id="85e86-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="85e86-127">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="85e86-127">Example 1</span></span>

<span data-ttu-id="85e86-128">Šajā piemērā parādīts XML fails kreditora sūtījumu importēšanai vienam pirkšanas pasūtījumam, kad nav iekļauta detalizēta informācija par gadījumu.</span><span class="sxs-lookup"><span data-stu-id="85e86-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="85e86-129">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="85e86-129">Example 2</span></span>

<span data-ttu-id="85e86-130">Šajā piemērā parādīts XML fails kreditora sūtījumu importēšanai vienam pirkšanas pasūtījumam, kad ir iekļauta detalizēta informācija par gadījumu.</span><span class="sxs-lookup"><span data-stu-id="85e86-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="85e86-131">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="85e86-131">Example 3</span></span>

<span data-ttu-id="85e86-132">Šajā piemērā parādīts XML fails kreditora sūtījumu importēšanai vairākiem pirkšanas pasūtījumiem, kad ir iekļauta detalizēta informācija par gadījumu.</span><span class="sxs-lookup"><span data-stu-id="85e86-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="85e86-133">Tiek pārbaudīti IPPN faila importēšanas rezultāti</span><span class="sxs-lookup"><span data-stu-id="85e86-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="85e86-134">Veiciet šīs darbības, lai pārbaudītu IPPN faila importēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="85e86-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="85e86-135">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="85e86-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="85e86-136">Atrodiet un atveriet kravu, kas izveidota kā daļa no IPPN importa.</span><span class="sxs-lookup"><span data-stu-id="85e86-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="85e86-137">Kopsavilkuma cilnē **Krava** jums ir jāredz vērtības, kas balstītas uz XML failu.</span><span class="sxs-lookup"><span data-stu-id="85e86-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="85e86-138">Kopsavilkuma cilnē **Kravas rindas** jums ir jāredz pirkšanas pasūtījumu numuri un krājumu informācija, kas ir balstīta uz XML failu.</span><span class="sxs-lookup"><span data-stu-id="85e86-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="85e86-139">Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Saņemt** atlasiet **Iepakojuma struktūra**, lai pārskatītu kravas iepakojuma struktūru.</span><span class="sxs-lookup"><span data-stu-id="85e86-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="85e86-140">Kopsavilkuma cilnē **Paletes** jums ir jāredz numura zīmes, kas balstītas uz XML failu.</span><span class="sxs-lookup"><span data-stu-id="85e86-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="85e86-141">Kopsavilkuma cilnē **Gadījumi** jums ir jāredz gadījumus, kas balstīti uz XML failu.</span><span class="sxs-lookup"><span data-stu-id="85e86-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="85e86-142">Kopsavilkuma cilnē **Krājumi** jums ir jāredz krājumus un daudzumus, kas balstīti uz XML failu.</span><span class="sxs-lookup"><span data-stu-id="85e86-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
