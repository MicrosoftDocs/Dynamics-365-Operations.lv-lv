---
title: Importēt ienākošos NNS, izmantojot V3 datu elementu
description: Šajā tēmā skaidrots, kā pārvaldīt ienākošo papildu nosūtīšanas paziņojumu (ASN) importu, izmantojot ienākošo ASN datu elementu.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 44ec0230236451a413d483b3e9f3ddc58b49a0b0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740057"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>Importēt ienākošos NNS, izmantojot V3 datu elementu

[!include [banner](../../includes/banner.md)]

Papildu paziņojums par nosūtīšanu (IPPN) jūs informē par kreditora piegādēm. Tie palīdz sūtītājam aprakstīt sūtījuma saturu un papildu informāciju par to, piemēram, krājumiem un iepakojumu.

IPPN var palīdzēt noliktavas darbiniekiem uzzināt, kas notiek. Tādēļ viņi var sagatavoties. Turklāt noliktavas darbinieki var izmantot IPPN, lai saskaņotu nosūtīšanas informāciju ar iepriekš izveidoto saistīto pirkšanas pasūtījumu.

Šajā tēmā ir apkopoti scenāriji, kas, izmantojot piemērus, parāda, kā strādāt ar IPPN failiem.

> [!IMPORTANT]
> *Ienākošais IPPN* imports attiecas tikai uz krājumiem, kas ir iespējoti papildu noliktavu pārvaldību (WMS). Pirms saņemat IPPN, pirkšanas pasūtījums sistēmā jāreģistrē kreditoram, kas sūta šo IPPN.

## <a name="inbound-asn-v3-entity"></a>Ienākošais ASN V3 elements

Jūs importējat ienākošos NN, izmantojot Ienākošo *ASN V3 salikto* datu elementu. *Ienākošais ASN V3* izmanto šādu entītiju priekšrocības:

- Ienākošās kravas virsraksts
- Ienākošā sūtījuma virsraksts
- Ienākošo kravu iepakošanas struktūras
- Ienākošo kravu iepakošanas struktūras gadījumi
- Ienākošo kravu iepakošanas struktūras gadījumu rindas
- Ienākošo kravu iepakošanas struktūras rindas

Ienākošais *ASN V3 saliktais* datu elements ir paredzēts asinhroniem integrācijas scenārijiem, kuros tiek izmantoti XML faila pamatā esoši importi.

## <a name="xml-format-for-importing-asns"></a>XML formāts IPPN importēšanai

Microsoft Dynamics 365 Supply Chain Management atbalsta šādu XML formātu IPPN importēšanai. Katrs XML faila zars pārstāv atsevišķa elementa atribūtu.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Piemēri

Tālāk dotās apakšsadaļas sniedz IPPN XML importa failu piemērus kreditora kravām.

### <a name="example-1"></a>1. piemērs

Šajā piemērā parādīts XML fails kreditora sūtījumu importēšanai vienam pirkšanas pasūtījumam, kad nav iekļauta detalizēta informācija par gadījumu.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>2. piemērs

Šajā piemērā parādīts XML fails kreditora sūtījumu importēšanai vienam pirkšanas pasūtījumam, kad ir iekļauta detalizēta informācija par gadījumu.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>3. piemērs

Šajā piemērā parādīts XML fails kreditora sūtījumu importēšanai vairākiem pirkšanas pasūtījumiem, kad ir iekļauta detalizēta informācija par gadījumu.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Tiek pārbaudīti IPPN faila importēšanas rezultāti

Veiciet šīs darbības, lai pārbaudītu IPPN faila importēšanas rezultātus.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Atrodiet un atveriet kravu, kas izveidota kā daļa no IPPN importa.
1. Kopsavilkuma cilnē **Krava** jums ir jāredz vērtības, kas balstītas uz XML failu.
1. Kopsavilkuma cilnē **Kravas rindas** jums ir jāredz pirkšanas pasūtījumu numuri un krājumu informācija, kas ir balstīta uz XML failu.
1. Darbību rūts cilnē **Nosūtīt un saņemt** grupā **Saņemt** atlasiet **Iepakojuma struktūra**, lai pārskatītu kravas iepakojuma struktūru.
1. Kopsavilkuma cilnē **Paletes** jums ir jāredz numura zīmes, kas balstītas uz XML failu.
1. Kopsavilkuma cilnē **Gadījumi** jums ir jāredz gadījumus, kas balstīti uz XML failu.
1. Kopsavilkuma cilnē **Krājumi** jums ir jāredz krājumus un daudzumus, kas balstīti uz XML failu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
