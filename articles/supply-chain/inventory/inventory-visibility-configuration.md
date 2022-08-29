---
title: Inventory Visibility konfigurēšana
description: Šajā rakstā ir aprakstīts, kā konfigurēt krājumu redzamību.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 576d8d5d0cad09aed40f1ceb9ce5682816c0f666
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306324"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibility konfigurēšana

[!include [banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā konfigurēt krājumu redzamību, izmantojot krājumu redzamības programmu Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Ievads

Pirms sākat strādāt ar krājumu redzamību, ir jāveic šāda konfigurācija, kā aprakstīts šajā rakstā:

- [Datu avotu konfigurācija](#data-source-configuration)
- [Nodalījuma konfigurācija](#partition-configuration)
- [Preču indeksa hierarhijas konfigurācija](#index-configuration)
- [Rezervācijas konfigurācija (nav obligāti)](#reservation-configuration)
- [Noklusējuma konfigurācijas piemērs](#default-configuration-sample)

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat darbu, uzinstalējiet un iestatiet Inventory Visibility pievienojumprogrammu, kā aprakstīts rakstā [Inventory Visibility instalēšana un iestatīšana](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Inventory Visibility lietojumprogrammas Konfigurāciju lapa

Pakalpojuma Power Apps lapa **Konfigurācijas** [Inventory Visibility programmā](inventory-visibility-power-platform.md) palīdz iestatīt rīcībā esošo konfigurāciju un vieglās rezervācijas konfigurāciju. Pēc pievienojumprogrammas instalēšanas noklusējuma konfigurācija ietver Microsoft Dynamics 365 Supply Chain Management (datu avotu `fno`) vērtību. Varat pārskatīt noklusējuma iestatījumus. Turklāt, pamatojoties uzņēmuma prasībās un ārējās sistēmas krājumu grāmatošanas prasībās, varat pārveidot konfigurāciju, lai standartizētu veidu, kādā var vairākās sistēmās grāmatot, organizēt un vaicātas krājumu izmaiņas. Pārējās šī raksta sadaļas skaidro kā izmantot katru konfigurācijas **lapas** daļu.

Pēc konfigurācijas pabeigšanas pārliecinieties, ka programmā atlasiet opciju **Atjaunināt konfigurāciju**.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Iespējot Inventory Visibility līdzekļus Power Apps līdzekļu pārvaldībā

Inventory Visibility pievienojumprogramma pievieno vairākus jaunus līdzekļus jūsu Power Apps instalēšanai. Pēc noklusējuma šie līdzekļi ir izslēgti. Lai tos lietotu, atveriet **konfigurācijas** lapu **un pēc tam cilnē Līdzekļu** pārvaldība pēc lietotāja ieslēkojiet šādas funkcijas.

| Līdzekļu pārvaldības nosaukums | Apraksts |
|---|---|
| *OnHandReservation* | Izmantojot krājumu redzamību, varat izveidot rezervācijas, patērētās rezervācijas un/vai atcelt norādītos krājumu daudzumus. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Šī funkcija sniedz preču krājumu kopsavilkumu kopā ar visām dimensijām. Krājuma kopsavilkuma dati tiks periodiski sinhronizēti no Inventory Visibility. Noklusējuma sinhronizācijas biežums ir ik pēc 15 minūtēm un to var iestatīt kā augstu, ik pēc 5 minūtēm. Papildinformāciju skatiet krājumu [kopsavilkumā](inventory-visibility-power-platform.md#inventory-summary). |
| *OnhandChangeSchedule* | Šī izvēles funkcija aktivizē rīcībā esošo izmaiņu grafiku un pieejamās solīšanai (ATP) funkcijas. Papildinformāciju skatiet sadaļā Rīcībā [esošo krājumu redzamības izmaiņu grafiks un apsolīšanai pieejamais](inventory-visibility-available-to-promise.md). |
| *Sadalījums* | Šī izvēles funkcija iespējo krājumu redzamību, lai varētu nodrošināt krājumu aizsardzību (ringfencing) un pārsaukt kontroli. Plašāku informāciju skatiet krājumu redzamības [krājumu sadalījumā](inventory-visibility-allocation.md). |
| *Iespējot noliktavas preces krājumu redzamības pakalpojumā* | Šī izvēles funkcija iespējo krājumu redzamību, lai atbalstītu krājumus, kas ir iespējoti noliktavas pārvaldības procesiem (WMS). Papildinformāciju skatiet šeit: [Krājumu redzamības atbalsts WMS krājumiem](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Atrast pakalpojuma galapunktu

Ja nezināt pareizo Krājumu redzamības pakalpojuma galapunktu, atveriet lapu **Konfigurācija** programmā Power Apps un pēc tam augšējā labajā stūrī atlasiet **Rādīt pakalpojuma galapunktu**. Lapa parādīs pareizo pakalpojuma galapunktu.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Datu avota konfigurācija

Katrs datu avots atspoguļo sistēmu, no kuras nāk dati. Piemēram, datu avotu nosaukumi ietver `fno` (kas nozīmē "Dynamics 365 finanšu un operāciju programmas") `pos` un (kas nozīmē "pārdošanas punkts"). Pēc noklusējuma Krājumu redzamības programma Supply Chain Management ir iestatīta kā noklusējuma datu avots (`fno`).

> [!NOTE]
> Datu `fno` avots ir rezervēts Piegādes ķēžu pārvaldībai. Ja krājumu redzamības pievienojumprogramma ir integrēta Piegādes ķēdes pārvaldības vidē, mēs iesakām nedzēšam konfigurācijas, kas saistītas `fno` ar datu avotu.

Lai izveidotu datu avotu, veiciet tālāk aprakstītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Datu avots** atlasiet **Jauns datu avots**, lai pievienotu datu avotu.

> [!NOTE]
> Kad pievienojat datu avotu, pirms Krājumu redzamības pakalpojuma konfigurācijas atjaunināšanas noteikti pārbaudiet datu avota nosaukumu, fiziskos izmērus un dimensiju kartējumus. Pēc **Konfigurācijas atjaunināšanas** atlases šos iestatījumus nevarēsit modificēt.

Datu avota konfigurācija ietver šādas daļas:

- Izmēri (izmēru kartēšana)
- Fiziskie mēri
- Aprēķinātie līdzekļi

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Izmēri (izmēru kartēšana)

Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām. Krājumu redzamība sniedz pamatdimensiju sarakstu, kuras var kartēt no datu avota dimensijām. Kartēšanai ir pieejamas trīsdesmit trīs dimensijas.

- Pēc noklusējuma, ja jūs izmantojat Supply Chain Management kā vienu no jūsu datu avotiem, 13 dimensijas tiek kartētas uz Supply Chain Management standarta dimensijām. Pārējās divpadsmit dimensijas (`inventDimension1` ar `inventDimension12`) tiek kartētas uz pielāgotām dimensijām Supply Chain Management. Atlikušās astoņas dimensijas ir paplašinātās dimensijas, kuras var kartēt uz ārējiem datu avotiem.
- Ja neizmantojiet Supply Chain Management kā vienu no jūsu datu avotiem, varat brīvi kartēt dimensijas. Tabulā ir parādīts pilns pieejamo dimensiju saraksts.

> [!NOTE]
> Ja dimensijas nav noklusējuma dimensiju sarakstā un jūs izmantojat ārēju datu avotu, ieteicams izmantot to `ExtendedDimension1` ar `ExtendedDimension8` kartēšanas darbības laikā.

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
| System | `Empty` |

> [!NOTE]
> Dimensijas veidi, kas norādīti iepriekšējā tabulā, ir tikai atsaucei. Tie nav jādefinē Krājumu redzamībā.
>
> Krājumu (pielāgotas) dimensijas var būt rezervētas Supply Chain Management. Šādā gadījumā tā vietā varat lietot paplašinātās dimensijas.

Ārējās sistēmas var piekļūt krājumu redzamībai, izmantojot tā RESTful API. Integrācijai krājumu redzamība ļauj konfigurēt _ārējo datu avotu_ un _ārējo dimensiju_ kartēšanu uz _pamatdimensijām_. Šeit parādīts dimensiju kartēšanas tabulas piemērs.

| Ārējā dimensija | Pamata dimensija |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Konfigurējot dimensiju kartējumu, ārējās dimensijas var nosūtīt tieši uz Krājumu redzamību. Krājumu redzamība pēc tam automātiski konvertēs ārējās dimensijas uz pamatdimensijām.

Lai pievienotu dimensiju kartējumus, rīkojieties šādi.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Dimensiju kartējumi** atlasiet **Pievienot**, lai pievienotu dimensiju kartējumus.
    ![Pievienot dimensiju kartējumus](media/inventory-visibility-dimension-mapping.png "Pievienot dimensiju kartējumus")

1. Laukā **Dimensijas nosaukums** norādiet avota dimensiju.
1. Laukā **Uz pamatdimensiju** atlasiet dimensiju Krājumu redzamībā, ko vēlaties kartēt.
1. Atlasiet **Saglabāt**.

Piemēram, ja datu avots ietver preces krāsas dimensiju, varat to kartēt uz `ColorId` pamatdimensiju, lai pievienotu pielāgotu `ProductColor` dimensiju `exterchannel` datu avotam. Pēc tam tā ir kartēta uz `ColorId` pamatdimensiju.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fiziskie mēri

Ja datu avots grāmato krājumu izmaiņas Krājumu redzamībai, tas grāmato šīs izmaiņas, izmantojot *fiziskos pasākumus*. Fiziskie pasākumi modificē daudzumu un atspoguļo krājumu statusu. Varat definēt savus fiziskos līdzekļus, balstoties uz jūsu prasībām. Vaicājumu pamatā var būt fiziskie pasākumi.

Krājumu redzamība sniedz ar Supply Chain Management (`fno` datu avotu) saistīto noklusējuma fizisko līdzekļu sarakstu. Šie noklusējuma fiziskie pasākumi tiek ņemti no krājumu darbību statusiem Supply Chain Management lapā **Rīcībā esošie krājumi** (**Krājumu pārvaldība \> Pieprasījumi un pārskati \> Rīcībā esošo pārskatu saraksts**). Tabulā sniegts fizisko līdzekļu piemērs.

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

Ja datu avots ir Supply Chain Management, jums nav no jauna jāizveido noklusējuma fiziskie pasākumi. Tomēr ārējiem datu avotiem var izveidot jaunus fiziskos krājumus, veicot šādus soļus.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Fiziskie mēri** atlasiet **Pievienot**, norādiet avota mērvienības nosaukumu un saglabājiet izmaiņas.

### <a name="calculated-measures"></a>Aprēķinātie līdzekļi

Varat izmantot Krājumu redzamību, lai pieprasītu gan krājumu fiziskos izmērus, gan *pielāgotos aprēķinātos izmērus*. Aprēķinātie pasākumi nodrošina pielāgotu aprēķināšanas formulu, kas sastāv no fizisko līdzekļu kombinācijas. Funkcionalitāte vienkārši ļauj definēt fizisko mērvienību kopu, kas tiks pievienota, un/vai fizisko mēru kopu, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.

> [!IMPORTANT]
> Aprēķinātais līdzeklis ir fizisko mērījumu sastāvs. Tā formulā var būt iekļauti tikai fiziskie pasākumi bez dublikātiem, nevis aprēķinātajiem parādītajiem.

Konfigurācija ļauj definēt modifikatoru kopu, kas tiek pievienota vai atņemta, lai iegūtu kopējo uzkrāto izvades daudzumu.

Lai iestatītu pielāgotos aprēķinātos mērījumus, izpildiet tālāk norādītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Aprēķinātais līdzeklis** atlasiet **Jaunu aprēķināto mērījumu**, lai pievienotu aprēķināto mērījumu.
1. Iestatiet šādus laukus jaunajam aprēķinātajam mēram:

    - **Jauns aprēķinātā mēra** nosaukums - ievadiet aprēķinātā mēra nosaukumu.
    - **Datu avots** - izvēlieties datu avotu, kas ir saistīts ar jauno modifikatoru. Vaicāšanas sistēma ir datu avots.

1. Atlasiet **Pievienot**, lai jaunam aprēķinātam mēram pievienotu modifikatoru.
1. Iestatiet sekojošos laukus jaunajam modifikatoram:

    - **Modifikators** — atlasiet modifikatora veidu (pievienošana *vai* *atņemšanas).*
    - **Datu avots** – atlasiet datu avotu, kur atrast mēru, kas nodrošina modifikatora vērtību.
    - **Mērvienība** – atlasiet mērvienības nosaukumu (no atlasītā datu avota), kas nodrošina modifikatora vērtību.

1. Atkārtojiet 5. līdz 6. soli, līdz esat pievienojis visus nepieciešamos modifikatorus.
1. Atlasiet **Saglabāt**.

Piemēram, varētu iegūt šādu vaicājuma rezultātu.

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

`MyCustomAvailableforReservation` izvade, pamatojoties pielāgoto mērījumu aprēķinu iestatījumā ir: 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Nodalījuma konfigurācija

Pašlaik nodalījuma konfigurācija sastāv no divām pamatdimensijām (`SiteId` un `LocationId`), kas norāda, kā dati tiek sadalīti. Operācijas vienā un tajā pašā nodalījumā var piegādāt lielāku veiktspēju par zemākām izmaksām. Šajā tabulā ir parādīta noklusējuma nodalījuma konfigurācija, kas paredzēta krājumu redzamības pievienojumprogrammai.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Risinājums ietver šo nodalījuma konfigurāciju pēc noklusējuma. *Tādēļ jums tas nav jādefinē pats*.

> [!IMPORTANT]
> Ne pielāgojiet noklusējuma nodalījuma konfigurāciju. Ja to dzēšat vai maināt, iespējams, radusies negaidīta kļūda.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Preču indeksa hierarhijas konfigurācija

Lielākā daļa laika rīcībā esošo krājumu vaicājums nebūs tikai augstākajā "kopsummas" līmenī. Tā vietā, iespējams, vēlēsieties arī redzēt rezultātus, kas uzkrāti, pamatojoties uz krājumu dimensijām.

Krājumu redzamība nodrošina elastību, neļaujot iestatīt _indeksus_. Šie indeksi ir balstīti uz dimensiju vai dimensiju kombināciju. Indeksu veido *kopas numurs*, *dimensija* un *hierarhija*, kā norādīts šajā tabulā.

| Nosaukums/vārds, uzvārds | Apraksts |
|---|---|
| Kopas skaitlis | Kopas numurs – dimensijas, kas pieder vienai kopai (indeksam), tiks grupētas kopā, un tām tiks piešķirts vienāds kopas numurs. |
| Dimensija | Pamatdimensijas, uz kurām vaicājuma rezultāts tiek apkopots. |
| Hierarhija | Hierarhija – hierarhija tiek izmantota, lai definētu atbalstītās dimensiju kombinācijas, kurām var izveidot vaicājumu. Piemēram, jūs iestatāt dimensiju kopu, kam ir hierarhijas `(ColorId, SizeId, StyleId)` secība. Šajā gadījumā sistēma atbalsta vaicājumus par četrām dimensiju kombinācijām. Pirmā kombinācija ir tukša, otrā ir `(ColorId)`, trešā ir `(ColorId, SizeId)` un ceturtā ir `(ColorId, SizeId, StyleId)`. Citas kombinācijas netiek atbalstītas. Papildinformāciju skatiet tālāk norādītajās tēmās. |

Lai iestatītu produktu hierarhijas indeksus, veiciet tālāk norādītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Dimensiju kartējumi** atlasiet **Pievienot**, lai pievienotu dimensiju kartējumus.
1. Pēc noklusējuma ir sniegts indeksu saraksts. Lai modificētu esošo indeksu, izvēlieties **Labot** vai **Pievienot** atbilstošā indeksa sadaļā. Lai izveidotu jaunu indeksu kopu, atlasiet **Jauna indeksu kopa**. Katrai rindai katrā indeksu kopā laukā **Dimensija** atlasiet pamatdimensiju sarakstā. Automātiski tiek ģenerētas šādu lauku vērtības:

    - **Kopas numurs** – dimensijas, kas pieder vienai grupai (indeksam), tiks grupētas kopā, un tām tiks piešķirts vienāds kopas numurs.
    - **Hierarhija** – hierarhija tiek izmantota, lai definētu atbalstītās dimensiju kombinācijas, kuras var vaicāt dimensiju grupā (indekss). Piemēram, ja iestatāt *dimensiju* grupu, kam ir stila, *·* *krāsas* un izmēra hierarhijas secība, sistēma atbalsta trīs vaicājumu grupu rezultātu. Pirmā grupa ir tikai stils. Otrā grupa ir stila un krāsas kombinācija. Trešā grupa ir stila, krāsas un izmēra kombinācija. Citas kombinācijas netiek atbalstītas.

> [!TIP]
> Šeit sniegti daži padomi, kas jāpatur prātā, iestatot indeksu hierarhiju:
>
> - Pamatdimensijas, kas ir definētas nodalījuma konfigurācijās, nav jādefinē indeksa konfigurācijās. Ja pamatdimensija atkal ir definēta indeksa konfigurācijā, nevarēsiet vaicāt pēc šī indeksa.
> - Ja ir tikai jāvaicā krājumi, kas uzkrāti pēc visām dimensiju kombinācijām, pēc tam iestatiet vienu indeksu, kas satur pamatdimensiju `Empty`.
> - Ir jābūt vismaz vienai indeksu hierarhijai (piemēram, `Empty` satur pamatdimensiju), pretējā gadījumā vaicājumiem neizdosies kļūda "Nav iestatīta indeksu hierarhija."

### <a name="example"></a>Paraugs

Šajā sadaļā sniegts piemērs, kā hierarhija darbojas.

Šajā tabulā sniegts šajā piemērā pieejamo krājumu saraksts.

| Objekts | ColorId | SizeId | StyleId | Daudzums |
|---|---|---|---|---|
| T-krekls | Melna | Mazs | Plats | 1 |
| T-krekls | Melna | Mazs | Regulārs | 2 |
| T-krekls | Melna | Liels | Plats | 3 |
| T-krekls | Melna | Liels | Regulārs | 4 |
| T-krekls | Sarkanā | Mazs | Plats | 5 |
| T-krekls | Sarkanā | Mazs | Regulārs | 6 |
| T-krekls | Sarkanā | Liels | Regulārs | 7 |

Nākamajā tabulā ir parādīts, kā tiek iestatīta indeksu hierarhija.

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

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervācijas konfigurācija (nav obligāti)

Rezervācijas konfigurācija ir nepieciešama, ja vēlaties izmantot vieglās rezervēšanas funkciju. Konfigurācija sastāv no divām fundamentālajām daļām:

- Vieglās rezervācijas kartēšana
- Vieglās rezervācijas hierarhija

### <a name="soft-reservation-mapping"></a>Vieglās rezervācijas kartēšana

Veicot rezervāciju, iespējams, vēlēsieties zināt, vai rīcībā esošie krājumi pašlaik ir pieejami rezervēšanai. Apstiprināšana ir saistīta ar aprēķinātu mērījumu, kas attēlo fizisko mērījumu kombinācijas skaitļošanas formulu.

Iestatot kartējumu no fiziskā mēra uz aprēķināto mērījumu, iespējojiet Krājumu redzamības pakalpojumu, lai automātiski validētu rezervāciju pieejamību, pamatojoties uz fizisko mērījumu.

Pirms **šīs** **kartēšanas** iestatīšanas konfigurācijas lapas cilnēs Datu avots un Aprēķinātais **mērs** Power Apps jādefinē fiziskie mēri, aprēķinātie mēri un to datu avoti (aprakstīts iepriekš šajā rakstā).

Lai definētu vieglās rezervācijas kartēšanu, veiciet šādas darbības.

1. Nosakiet fizisko mērījumu, kas kalpo kā vieglās rezervēšanas mērs (piemēram, `SoftReservOrdered`).
1. Lapas **Konfigurācija** cilnē **Aprēķinātais līdzeklis** definējiet *rezervēšanai pieejamo* (AFR) skaitļošanas formulu, kuru vēlaties kartēt uz fizisko mērījumu. Piemēram, varat iestatīt `AvailableToReserve` (pieejams rezervācijai), lai tas būtu kartēts uz iepriekš noteiktu `SoftReservOrdered` fizisko mērījumu. Šādā veidā var atrast daudzumus, kuru `SoftReservOrdered` krājumu statuss ir pieejams rezervēšanai. Tabulā ir parādīta AFR aprēķina formula.

    | Aprēķina tips | Datu avots | Fiziskais mērs |
    |---|---|---|
    | Papildinājums | `fno` | `AvailPhysical` |
    | Papildinājums | `pos` | `Inbound` |
    | Atņemšana | `pos` | `Outbound` |
    | Atņemšana | `iv` | `SoftReservOrdered` |

    Iesakām iestatīt aprēķināto izmēru tā, lai tas saturētu fizisko mērījumu, kurā ir balstīts rezervācijas mērījums. Tādējādi aprēķinātā mērījuma daudzumu ietekmēs rezervācijas mērījumu daudzums. Tāpēc Šajā piemērā `iv` datu avota `AvailableToReserve` aprēķinātajam mērījumam vajadzētu saturēt `SoftReservOrdered` fizisko mērījumu no `iv` kā komponentu.

1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Vieglās rezervācijas kartēšana** iestatiet kartējumu no fiziskā mēra uz aprēķināto mērījumu. Iepriekšējā piemērā varat izmantot tālāk norādītos iestatījumus, lai kartētu `AvailableToReserve` uz iepriekš definēto `SoftReservOrdered` fizisko mērījumu.

    | Fiziskais mēra datu avots | Fiziskais mērs | Pieejams rezervēšanas datu avotam | Pieejams rezervēšanai aprēķinātam mēram |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Ja nevarat rediģēt cilni **Vieglās rezervācijas kartēšana**, jums, iespējams, vajadzēs iespējot līdzekli *OnHandReservation* cilnē **Līdzekļu pārvaldība**.

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

> [!NOTE]
> Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True` nozīmē, ka ir vajadzīga validācija, bet vērtība `False` nozīmē, ka validācija nav vajadzīga. Noklusējuma vērtība ir `True`.

### <a name="soft-reservation-hierarchy"></a>Vieglās rezervācijas hierarhija

Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tādā pašā veidā, kā preču indeksu hierarhija darbojas rīcībā esošos vaicājumos.

Rezervāciju hierarhija nav atkarīga no preču indeksu hierarhijas. Šī neatkarību ļauj ieviest kategoriju pārvaldību, kur lietotāji var sadalīt dimensijas detalizētāk, lai noteiktu prasības precīzākai rezervāciju veikšanai. Jūsu vieglās rezervācijas hierarhijai vajadzētu saturēt komponentus `SiteId` un `LocationId`, jo tie veido dalīšanās konfigurāciju. Veicot rezervāciju, ir jākonkretizē produkta dalījums.

Šajā piemērā ir vieglās rezervācijas hierarhijas piemērs.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Šajā piemērā rezervāciju var veikt šādām izmēru secībām. Veicot rezervāciju, ir jākonkretizē produkta dalījums. Tāpēc pamata hierarhija, kuru varat lietot ir `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Dimensiju secībai ir stingri jāievēro rezervāciju hierarhijas secība, dimensija pēc dimensijas. Piemēram, hierarhijas secība `(SiteId, LocationId, SizeId)` nav derīga, jo trūkst `ColorId`.

## <a name="available-to-promise-configuration-optional"></a>Konfigurācija pieejama solīšanai (neobligāti)

Var iestatīt krājumu redzamību, lai ļautu plānot rīcībā esošo krājumu turpmākās izmaiņas un aprēķināt rīcībā esošos (ATP) daudzumus. ATP ir pieejamais krājuma daudzums, un nākamajā periodā to var solīt debitoram. Šī aprēķina izmantošana var lielā palielinās pasūtījuma izpildes iespēju. Lai izmantotu šo funkciju, jums tā ir jāiespējo **cilnē** Līdzekļu pārvaldība un pēc tam tā jāiestata **cilnē ATP** iestatījumi. Papildinformāciju skatiet krājumu redzamības [rīcībā esošo izmaiņu grafiki un apsolīšanai pieejamos.](inventory-visibility-available-to-promise.md)

## <a name="complete-and-update-the-configuration"></a>Pabeidziet un atjauniniet konfigurāciju

Pēc konfigurācijas pabeigšanas ir jāveic visas izmaiņas Krājumu redzamībai. Lai veiktu izmaiņas, atlasiet **Atjaunināt konfigurāciju** lapas **Konfigurācija** augšējā labajā stūrī programmā Power Apps.

Pirmo reizi atlasot **Atjaunināt konfigurāciju**, sistēma pieprasa savus akreditācijas datus.

- **Klienta ID** — Azure programmas ID, ko izveidojāt Krājumu redzamībai.
- **Nomnieka ID** — jūsu Azure nomnieka ID.
- **Klienta slepenā informācija** — Azure pieteikuma slepenā informācija, ko izveidojāt Krājumu redzamībai.

Pēc pieteikšanās konfigurācija tiek atjaunināta Krājumu redzamības pakalpojumā.

> [!NOTE]
> Kad pievienojat datu avotu, pirms Krājumu redzamības pakalpojuma konfigurācijas atjaunināšanas noteikti pārbaudiet datu avota nosaukumu, fiziskos izmērus un dimensiju kartējumus. Pēc **Konfigurācijas atjaunināšanas** atlases šos iestatījumus nevarēsit modificēt.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Noklusējuma konfigurācijas piemērs

Inicializācijas posmā Inventory Visibility iestata noklusējuma konfigurāciju, kura sīkāk aprakstīta šeit. Šo konfigurāciju varat pēc vajadzības pārveidot.

### <a name="data-source-configuration"></a>Datu avota konfigurācija

#### <a name="configuration-of-the-iv-data-source"></a>Datu avota konfigurācija

Šajā sadaļā ir aprakstīts, kā `iv` datu avots tiek konfigurēts.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fiziskie pasākumi, kas konfigurēti datu avotam "iv"

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

#### <a name="configuration-of-the-fno-data-source"></a>"fno" datu avota konfigurācija

Šajā sadaļā ir aprakstīts, kā `fno` datu avots tiek konfigurēts.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensiju kartējumi "fno" datu avotam

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fiziskie pasākumi, kas konfigurēti "fno" datu avotam

Datu avotam ir konfigurēti šādi `fno` fiziskie pasākumi:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>"pos" datu avota konfigurācija

Šajā sadaļā ir aprakstīts, kā `pos` datu avots tiek konfigurēts.

##### <a name="physical-measures-for-the-pos-data-source"></a>"POS" datu avota fiziskie pasākumi

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

#### <a name="configuration-of-the-iom-data-source"></a>"iom" datu avota konfigurācija

Datu avotam ir konfigurēti šādi `iom` fiziskie pasākumi:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>"erp" datu avota konfigurācija

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

