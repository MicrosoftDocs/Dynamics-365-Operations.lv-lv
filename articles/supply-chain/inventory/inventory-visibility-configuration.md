---
title: Krājumu redzamības konfigurācija
description: Šajā tēmā ir aprakstīts, kā izmantot Krājumu redzamības programmu.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345037"
---
# <a name="inventory-visibility-configuration"></a>Krājumu redzamības konfigurācija

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot Krājumu redzamības programmu.

## <a name="introduction"></a><a name="introduction"></a>Ievads

Pirms sākat strādāt ar Krājumu redzamību, ir jāveic šāda konfigurācija, kā aprakstīts šajā tēmā:

- [Datu avotu konfigurācija](#data-source-configuration)
- [Nodalījuma konfigurācija](#partition-configuration)
- [Preču indeksa hierarhijas konfigurācija](#index-configuration)
- [Rezervācijas konfigurācija (nav obligāti)](#reservation-configuration)
- [Noklusējuma konfigurācijas piemērs](#default-configuration-sample)

> [!NOTE]
> Varat skatīt un rediģēt Krājumu redzamības konfigurācijas programmā [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). Kad konfigurācija ir pabeigta, programmā atlasiet **Atjaunināt konfigurāciju**.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Datu avota konfigurācija

Datu avots parāda sistēmu, no kuras ir dati. Piemēri ietver `fno` (kas nozīmē " Dynamics 365 Finance and Operations programmas") un `pos` (kas nozīmē "pārdošanas punkts").

Datu avota konfigurācija ietver šādas daļas:

- Dimensija (dimensiju kartēšana)
- Fiziskais mērs
- Aprēķinātais līdzeklis

> [!NOTE]
> Datu avots `fno` ir rezervēts Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensija (dimensiju kartēšana)

Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām.

Krājumu redzamība atbalsta šādas vispārīgās pamatdimensijas.

| Dimensiju veids | Pamata dimensija |
|---|---|
| Produkts | `ColorId` |
| Produkts | `SizeId` |
| Produkts | `StyleId` |
| Produkts | `ConfigId` |
| Izsekošana | `BatchId` |
| Izsekošana | `SerialId` |
| Novietojums | `LocationId` |
| Novietojums | `SiteId` |
| Krājumu statuss | `StatusId` |
| Specifiski noliktavai | `WMSLocationId` |
| Specifiski noliktavai | `WMSPalletId` |
| Specifiski noliktavai | `LicensePlateId` |
| Citi | `VersionId` |
| Krājumi (pielāgoti) | `InventDimension1` ar `InventDimension12` |
| Paplašinājums | `ExtendedDimension1` ar `ExtendedDimension8` |

> [!NOTE]
> Dimensijas veidi, kas norādīti iepriekšējā tabulā, ir tikai atsaucei. Tie nav jādefinē Krājumu redzamībā.
>
> Krājumu (pielāgotas) dimensijas var būt rezervētas Supply Chain Management. Šādā gadījumā tā vietā varat lietot paplašinātās dimensijas.

Ārējās sistēmas var piekļūt krājumu redzamībai, izmantojot tā RESTful API. Integrācijai krājumu redzamība ļauj konfigurēt _ārējo datu avotu_ un _ārējo dimensiju_ kartēšanu uz _pamatdimensijām_. Tālāk ir sniegts dimensiju kartēšanas tabulas piemērs.

| Ārējā dimensija | Pamata dimensija |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Konfigurējot dimensiju kartējumu, ārējās dimensijas var nosūtīt tieši uz Krājumu redzamību. Krājumu redzamība pēc tam automātiski konvertēs ārējās dimensijas uz pamatdimensijām.

### <a name="physical-measures"></a>Fiziskie mēri

Fiziskie pasākumi modificē daudzumu un atspoguļo krājumu statusu. Varat definēt savus fiziskos līdzekļus, balstoties uz jūsu prasībām.

Krājumu redzamība sniedz ar Supply Chain Management (`fno` datu avotu) saistīto noklusējuma fizisko līdzekļu sarakstu. Tabulā sniegts fizisko līdzekļu piemērs.

| Fiziskā līdzekļa nosaukums | Apraksts |
|---|---|
| `NotSpecified` | Nav norādīta |
| `Arrived` | Pienācis |
| `AvailOrdered` | Pieejamais pasūtītais |
| `AvailPhysical` | Fiziski pieejams |
| `Deducted` | Atskaitīts |
| `OnOrder` | Pasūtīts |
| `Ordered` | Pasūtīts |
| `PhysicalInvent` | Fiziskie krājumi |
| `Picked` | Izdots |
| `PostedQty` | Grāmatotais daudzums |
| `QuotationIssue` | Piedāvājuma izejas plūsma |
| `QuotationReceipt` | Piedāvājuma ieejas plūsma |
| `Received` | Saņemts |
| `Registered` | Reģistrēts |
| `ReservOrdered` | Rezervēts pasūtījumos |
| `ReservPhysical` | Fiziski rezervēts |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Aprēķinātie līdzekļi

Aprēķinātie pasākumi nodrošina pielāgotu aprēķināšanas formulu, kas sastāv no fizisko līdzekļu kombinācijas. Funkcionalitāte vienkārši ļauj definēt fizisko mērvienību kopu, kas tiks pievienota, un/vai fizisko mēru kopu, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.

Piemēram, ir šāds vaicājuma rezultāts.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Pēc tam konfigurējiet aprēķināto mērījumu ar nosaukumu `MyCustomAvailableforReservation`, kā parādīts šajā tabulā. Šo aprēķināto mērījumu patērēs patēriņa sistēma.

| Patēriņa sistēma | Aprēķinātais līdzeklis | Datu avots | Fiziskais mērs | Aprēķina tips |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Izmantojot šo aprēķināšanas formulu, jaunais vaicājuma rezultāts ietvers pielāgoto mērījumu.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` izvade tiek balstīta uz aprēķina iestatījumu pielāgotos mērījumos kā: 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Nodalījuma konfigurācija

Nodalījuma konfigurācija sastāv no pamatdimensiju kombinācijas. Tas nosaka datu sadales modeli. Datu operācijas vienā nodalījumā atbalsta augstu veiktspēju un ne pārāk daudz izmaksu. Tāpēc labie nodalījuma raksti var sniegt nozīmīgus atvieglojumus.

Krājumu redzamība nodrošina šādu noklusējuma nodalījuma konfigurāciju.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Noklusējuma nodalījuma konfigurācija ir tikai atsaucei. Tie nav jādefinē Krājumu redzamībā. Pašlaik nodalījuma konfigurācijas jauninājums netiek atbalstīts.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Preču indeksa hierarhijas konfigurācija

Lielākā daļa laika rīcībā esošo krājumu vaicājums nebūs tikai augstākajā "kopsummas" līmenī. Tā vietā, iespējams, vēlēsieties skatīt arī rezultātus, kas uzkrāti, pamatojoties uz krājumu dimensijām.

Krājumu redzamība nodrošina elastību, neļaujot iestatīt _indeksus_. Šie indeksi ir balstīti uz dimensiju vai dimensiju kombināciju. Indeksu veido *kopas numurs*, *dimensija* un *hierarhija*, kā norādīts šajā tabulā.

| Nosaukums/vārds, uzvārds | Apraksts |
|---|---|
| Kopas skaitlis | Kopas numurs – dimensijas, kas pieder vienai kopai (indeksam), tiks grupētas kopā, un tām tiks piešķirts vienāds kopas numurs. |
| Dimensija | Pamatdimensijas, uz kurām vaicājuma rezultāts tiek apkopots. |
| Hierarhija | Hierarhija – hierarhija tiek izmantota, lai definētu atbalstītās dimensiju kombinācijas, kurām var izveidot vaicājumu. Piemēram, jūs iestatāt dimensiju kopu, kam ir hierarhijas `(ColorId, SizeId, StyleId)` secība. Šajā gadījumā sistēma atbalsta vaicājumus par četrām dimensiju kombinācijām. Pirmā kombinācija ir tukša, otrā ir `(ColorId)`, trešā ir `(ColorId, SizeId)` un ceturtā ir `(ColorId, SizeId, StyleId)`. Citas kombinācijas netiek atbalstītas. Papildinformāciju skatiet tālāk norādītajās tēmās. |

### <a name="example"></a>Paraugs

Šajā sadaļā sniegts piemērs, kā hierarhija darbojas.

Jūsu krājumos ir šādi elementi.

| Objekts | ColorId | SizeId | StyleId | Daudzums |
|---|---|---|---|---|
| T-krekls | Melna | Mazs | Plats | 1 |
| T-krekls | Melna | Mazs | Regulārs | 2 |
| T-krekls | Melna | Liels | Plats | 3 |
| T-krekls | Melna | Liels | Regulārs | 4 |
| T-krekls | Sarkanā | Mazs | Plats | 5 |
| T-krekls | Sarkanā | Mazs | Regulārs | 6 |
| T-krekls | Sarkanā | Liels | Regulārs | 7 |

Šeit ir indekss.

| Kopas skaitlis | Dimensija | Hierarhija |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indekss ļauj veikt rīcībā esošo krājumu vaicājumu šādos veidos:

- `()`– grupēt pēc visiem

    - T-krekls, 28

- `(ColorId)` – grupēts pēc `ColorId`

    - T-krekls, melns, 10
    - T-krekls, sarkans, 18

- `(ColorId, SizeId)` – grupēts pēc `ColorId` un `SizeId` kombinācijas

    - T-krekls, melns, mazs, 3
    - T-krekls, melns, liels, 7
    - T-krekls, sarkans, mazs, 11
    - T-krekls, sarkans, liels, 7

- `(ColorId, SizeId, StyleId)` – grupēts pēc `ColorId`, `SizeId` un `StyleId` kombinācijas

    - T-krekls, melns, mazs, plats, 1
    - T-krekls, melns, mazs, standarta, 2
    - T-krekls, melns, liels, plats, 3
    - T-krekls, melns, liels, standarta, 4
    - T-krekls, sarkans, mazs, plats, 5
    - T-krekls, sarkans, mazs, standarta, 6
    - T-krekls, sarkans, liels, standarta, 7

> [!NOTE]
> Pamatdimensijas, kas ir definētas nodalījuma konfigurācijās, nav jādefinē indeksa konfigurācijās.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervācijas konfigurācija (nav obligāti)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Rezervācijas konfigurācija ir nepieciešama, ja vēlaties izmantot vieglās rezervēšanas funkciju. Konfigurācija sastāv no divām fundamentālajām daļām:

- Vieglās rezervācijas kartēšana
- Vieglās rezervācijas hierarhija

### <a name="soft-reservation-mapping"></a>Vieglās rezervācijas kartēšana

Veicot rezervāciju, iespējams, vēlēsieties zināt, vai rīcībā esošie krājumi pašlaik ir pieejami rezervēšanai. Apstiprināšana ir saistīta ar aprēķinātu mērījumu, kas attēlo fizisko mērījumu kombinācijas skaitļošanas formulu.

Piemēram, rezervēšanas mērs ir balstīts uz `SoftReservOrdered` fizisko mērījumu no datu avota `iv` (Krājumu redzamība). Šajā gadījumā varat iestatīt aprēķināto `AvailableToReserve` datu avota `iv`mērījumu, kā parādīts šeit.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `AvailPhysical` |
| Papildinājums | `pos` | `Inbound` |
| Atņemšana | `pos` | `Outbound` |
| Atņemšana | `iv` | `SoftReservOrdered` |

Iestatiet vieglās rezervācijas kartēšanu, lai nodrošinātu kartēšanu no `SoftReservOrdered` rezervācijas līdzekļa uz `AvailableToReserve` aprēķināto līdzekli.

| Fiziskais mēra datu avots | Fiziskais mērs | Pieejams rezervēšanas datu avotam | Pieejams rezervēšanai aprēķinātam mēram |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Tagad, kad veiksiet rezervāciju `SoftReservOrdered`, Krājumu redzamība automātiski atradīs un rezervēšanas validācijai tiks atrasta `AvailableToReserve` saistītā aprēķināšanas formula.

Piemēram, Krājumu redzamībai ir šādi rīcībā esošie krājumi.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

Šajā gadījumā tiek lietots šāds aprēķins:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Tāpēc, mēģinot veikt rezervācijas `iv.SoftReservOrdered` un daudzums ir mazāks vai vienāds ar `AvailableToReserve` (10), varat veikt rezervēšanu.

### <a name="soft-reservation-hierarchy"></a>Vieglās rezervācijas hierarhija

Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tādā pašā veidā, kā preču indeksu hierarhija darbojas rīcībā esošos vaicājumos.

Rezervāciju hierarhija nav atkarīga no preču indeksu hierarhijas. Šī neatkarību ļauj ieviest kategoriju pārvaldību, kur lietotāji var sadalīt dimensijas detalizētāk, lai noteiktu prasības precīzākai rezervāciju veikšanai.

Tālāk ir sniegts dimensiju hierarhijas piemērs.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Šajā piemērā varat veikt rezervāciju šādām dimensiju secībām:

- `()`– dimensija nav dota.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Dimensiju secībai ir stingri jāievēro rezervāciju hierarhijas secība, dimensija pēc dimensijas. Piemēram, hierarhijas secība `(SiteId, LocationId, SizeId)` nav derīga, jo trūkst `ColorId`.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Noklusējuma konfigurācijas piemērs

Tās inicializācijas posmā Krājumu redzamība iestata noklusējuma konfigurāciju. Pēc nepieciešamības konfigurāciju var modificēt.

### <a name="data-source-configuration"></a>Datu avota konfigurācija

#### <a name="configuration-of-the-iv-data-source"></a>Datu avota konfigurācija

Šajā sadaļā ir aprakstīts, kā `iv` datu avots tiek konfigurēts.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Iv datu avotam konfigurētie fiziskie pasākumi

Datu avotam ir konfigurēti šādi `iv` fiziskie pasākumi:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal aprēķinātais līdzeklis

Pēc tam konfigurējiet `OrderedTotal` aprēķināto mērījumu ar `iv` datu avota nosaukumu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `Ordered` |
| Papildinājums | `fno` | `Arrived` |
| Papildinājums | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Rīcībā esošais aprēķinātais līdzeklis

Pēc tam konfigurējiet `OnHand` aprēķināto mērījumu ar `iv` datu avota nosaukumu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `PhysicalInvent` |
| Papildinājums | `iom` | `OnHand` |
| Papildinājums | `erp` | `Unrestricted` |
| Papildinājums | `erp` | `QualityInspection` |
| Papildinājums | `pos` | `PosInbound` |
| Atņemšana | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReservedTotal aprēķinātais līdzeklis

Pēc tam konfigurējiet `ReservedTotal` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `ReservPhysical` |
| Papildinājums | `fno` | `ReservOrdered` |
| Papildinājums | `iv` | `SoftReservPhysical` |
| Papildinājums | `iv` | `SoftReservOrdered` |
| Papildinājums | `iv` | `ReservPhysical` |
| Papildinājums | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved aprēķinātais līdzeklis

Pēc tam konfigurējiet `SoftReserved` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `iv` | `SoftReservPhysical` |
| Papildinājums | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved aprēķinātais līdzeklis

Pēc tam konfigurējiet `HardReserved` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `ReservPhysical` |
| Papildinājums | `fno` | `ReservOrdered` |
| Papildinājums | `iv` | `ReservPhysical` |
| Papildinājums | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder aprēķinātais līdzeklis

Pēc tam konfigurējiet `OpenOrder` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `OnOrder` |
| Papildinājums | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable aprēķinātais līdzeklis

Pēc tam konfigurējiet `OnHandAvailable` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `PhysicalInvent` |
| Papildinājums | `iom` | `OnHand` |
| Papildinājums | `erp` | `Unrestricted` |
| Papildinājums | `erp` | `QualityInspection` |
| Papildinājums | `pos` | `PosInbound` |
| Atņemšana | `fno` | `ReservPhysical` |
| Atņemšana | `iv` | `SoftReservPhysical` |
| Atņemšana | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve aprēķinātais līdzeklis

Pēc tam konfigurējiet `AvailableToReserve` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `PhysicalInvent` |
| Papildinājums | `iom` | `OnHand` |
| Papildinājums | `erp` | `Unrestricted` |
| Papildinājums | `erp` | `QualityInspection` |
| Papildinājums | `pos` | `PosInbound` |
| Papildinājums | `fno` | `Ordered` |
| Papildinājums | `fno` | `Arrived` |
| Papildinājums | `iv` | `Ordered` |
| Atņemšana | `fno` | `ReservPhysical` |
| Atņemšana | `fno` | `ReservOrdered` |
| Atņemšana | `iv` | `SoftReservPhysical` |
| Atņemšana | `iv` | `SoftReservOrdered` |
| Atņemšana | `iv` | `ReservPhysical` |
| Atņemšana | `iv` | `ReservOrdered` |
| Atņemšana | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply aprēķinātais līdzeklis

Pēc tam konfigurējiet `InventorySupply` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `Ordered` |
| Papildinājums | `fno` | `Arrived` |
| Papildinājums | `iv` | `Ordered` |
| Papildinājums | `fno` | `PhysicalInvent` |
| Papildinājums | `iom` | `OnHand` |
| Papildinājums | `erp` | `Unrestricted` |
| Papildinājums | `erp` | `QualityInspection` |
| Papildinājums | `pos` | `PosInbound` |
| Atņemšana | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand aprēķinātais līdzeklis

Pēc tam konfigurējiet `InventoryDemand` aprēķināto mērījumu ar `iv` datu avotu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `OnOrder` |
| Papildinājums | `iom` | `OnOrder` |
| Papildinājums | `iv` | `SoftReservPhysical` |
| Papildinājums | `iv` | `SoftReservOrdered` |
| Papildinājums | `fno` | `ReservPhysical` |
| Papildinājums | `fno` | `ReservOrdered` |
| Papildinājums | `iv` | `ReservPhysical` |
| Papildinājums | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Datu avota fno konfigurācija

Šajā sadaļā ir aprakstīts, kā `fno` datu avots tiek konfigurēts.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Fno datu avota dimensiju kartēšana

Šajā tabulā uzskaitītie dimensiju kartējumi ir konfigurēti datu `fno` avotam.

| Ārējā dimensija | Pamata dimensija |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>fno datu avotam konfigurētie fiziskie pasākumi

Datu avotam ir konfigurēti šādi `fno` fiziskie pasākumi:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Datu avota fno konfigurācija

Šajā sadaļā ir aprakstīts, kā `pos` datu avots tiek konfigurēts.

##### <a name="physical-measures-for-the-pos-data-source"></a>pos datu avotam konfigurētie fiziskie pasākumi

Datu avotam ir konfigurēti šādi `pos` fiziskie pasākumi:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity aprēķinātais līdzeklis

Pēc tam konfigurējiet `AvailQuantity` aprēķināto mērījumu ar `pos` datu avota nosaukumu , kā parādīts šajā tabulā.

| Aprēķina tips | Datu avots | Fiziskais mērs |
|---|---|---|
| Papildinājums | `fno` | `AvailPhysical` |
| Papildinājums | `pos` | `PosInbound` |
| Atņemšana | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Datu avota konfigurācija

Datu avotam ir konfigurēti šādi `iom` fiziskie pasākumi:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Datu avota erp konfigurācija

Datu avotam ir konfigurēti šādi `erp` fiziskie pasākumi:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Nodalījuma konfigurācija

Tabulā ir parādīta noklusējuma nodalījuma konfigurācija.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Izmaksu konfigurācija

Tabulā ir parādīta noklusējuma nodalījuma konfigurācija.

| Kopas skaitlis | Dimensija | Hierarhija |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Rezervācijas konfigurācija

Šajā sadaļā aprakstīta noklusējuma rezervācijas konfigurācija.

#### <a name="reservation-mapping"></a>Vieglās rezervācijas kartēšana

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tabulā ir parādīta noklusējuma rezervāciju kartēšana.

| Fiziskais mēra datu avots | Fiziskais mērs | Pieejams rezervēšanas datu avotam | Pieejams rezervēšanai aprēķinātam mēram |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Rezervāciju hierarhija

Tabulā ir parādīta noklusējuma rezervāciju kartēšana.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10. |
| `WMSPalletId` | 11. |
| `ConfigId` | 12. |
| `VersionId` | 13 |
| `CustomDimension1` | 14. |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
