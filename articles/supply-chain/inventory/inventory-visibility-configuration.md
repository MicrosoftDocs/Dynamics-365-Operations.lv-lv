---
title: Inventory Visibility konfigurēšana
description: Šajā rakstā ir aprakstīts, kā konfigurēt krājumu redzamību.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 915382c14cc9ba89b9d543cfd668a94cecbc0a55
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9764868"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibility konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt krājumu redzamību, izmantojot programmu Krājumu redzamība sadaļā Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Ievads

Pirms sākat darbu ar krājumu redzamību, ir jāpabeidz tālāk norādītā konfigurācija, kā aprakstīts šajā rakstā.

- [Datu avotu konfigurācija](#data-source-configuration)
- [Nodalījuma konfigurācija](#partition-configuration)
- [Preču indeksa hierarhijas konfigurācija](#index-configuration)
- [Rezervācijas konfigurācija (nav obligāti)](#reservation-configuration)
- [Noklusējuma konfigurācijas piemērs](#default-configuration-sample)

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat darbu, uzinstalējiet un iestatiet Inventory Visibility pievienojumprogrammu, kā aprakstīts rakstā [Inventory Visibility instalēšana un iestatīšana](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Inventory Visibility lietojumprogrammas Konfigurāciju lapa

Pakalpojuma Power Apps lapa **Konfigurācijas** [Inventory Visibility programmā](inventory-visibility-power-platform.md) palīdz iestatīt rīcībā esošo konfigurāciju un vieglās rezervācijas konfigurāciju. Pēc pievienojumprogrammas instalēšanas noklusējuma konfigurācija ietver Microsoft Dynamics 365 Supply Chain Management (datu avotu `fno`) vērtību. Varat pārskatīt noklusējuma iestatījumus. Turklāt, pamatojoties uzņēmuma prasībās un ārējās sistēmas krājumu grāmatošanas prasībās, varat pārveidot konfigurāciju, lai standartizētu veidu, kādā var vairākās sistēmās grāmatot, organizēt un vaicātas krājumu izmaiņas. Pārējās šī raksta sadaļās ir paskaidrots, kā izmantot katru konfigurācijas **lapas** daļu.

Pēc konfigurācijas pabeigšanas pārliecinieties, ka programmā atlasiet opciju **Atjaunināt konfigurāciju**.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Iespējot Inventory Visibility līdzekļus Power Apps līdzekļu pārvaldībā

Inventory Visibility pievienojumprogramma pievieno vairākus jaunus līdzekļus jūsu Power Apps instalēšanai. Pēc noklusējuma šie līdzekļi ir izslēgti. Lai tos izmantotu, atveriet **lapu Konfigurācija** un pēc tam cilnē Līdzekļu pārvaldība **pēc** vajadzības ieslēdziet tālāk norādītos līdzekļus.

| Līdzekļu pārvaldības nosaukums | Apraksts |
|---|---|
| *OnHandReservation* | Šis līdzeklis ļauj izveidot rezervācijas, izmantot rezervācijas un/vai rezervēt norādītos krājumu daudzumus, izmantojot krājumu redzamību. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Šis līdzeklis nodrošina krājumu kopsavilkumu par precēm kopā ar visām dimensijām. Krājuma kopsavilkuma dati tiks periodiski sinhronizēti no Inventory Visibility. Noklusējuma sinhronizācijas frekvence ir reizi 15 minūtēs, un to var iestatīt pat reizi 5 minūtēs. Papildinformāciju skatiet sadaļā [Krājumu kopsavilkums](inventory-visibility-power-platform.md#inventory-summary). |
| *onHandIndexQueryPreloadBackgroundService* | Šis līdzeklis ļauj iepriekš ielādēt rīcībā esošos vaicājumus Krājumu redzamība, lai apkopotu rīcībā esošos sarakstus ar iepriekš atlasītiem izmēriem. Noklusējuma sinhronizācijas frekvence ir reizi 15 minūtēs. Papildinformāciju skatiet rakstā [Racionalizēta rīcībā esoša vaicājuma](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) iepriekšēja ielāde. |
| *OnhandChangeSchedule* | Šī neobligātā funkcija iespējo pieejamo izmaiņu grafiku un solījumu pievienošanas (ATP) funkcijas. Papildinformāciju skatiet sadaļā [Krājumu redzamības rīcībā esošo izmaiņu grafiks, kas ir pieejams solīšanai](inventory-visibility-available-to-promise.md). |
| *Sadalījums* | Šis neobligātais līdzeklis iespējo krājumu redzamību ar krājumu aizsardzības (aplokšņu nožogošanas) un pārpārdošanas kontroles iespēju. Papildinformāciju skatiet sadaļā [Krājumu redzamības krājumu sadalījums](inventory-visibility-allocation.md). |
| *Iespējot noliktavas preces krājumu redzamības pakalpojumā* | Šis neobligātais līdzeklis iespējo krājumu redzamību, lai atbalstītu krājumus, kas ir iespējoti noliktavas pārvaldības procesiem (WMS). Papildinformāciju skatiet sadaļā [Krājumu redzamības atbalsts WMS vienumiem](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Atrast pakalpojuma galapunktu

Ja nezināt pareizo pakalpojuma Krājumu redzamība galapunktu, atveriet **lapu** Konfigurācija Power Apps un pēc tam augšējā labajā stūrī atlasiet **Rādīt detalizētu informāciju par** pakalpojumu. Lapa parādīs pareizo pakalpojuma galapunktu. Galapunktu varat atrast arī sadaļā Lifecycle Services, kā aprakstīts sadaļā Microsoft Dynamics [Galapunkta atrašana atbilstoši savai dzīves cikla pakalpojumu videi](inventory-visibility-api.md#endpoint-lcs).

> [!NOTE]
> Nepareiza galapunkta izmantošana var izraisīt nesekmīgu krājumu redzamības instalāciju un kļūdas, kad Supply Chain Management tiek sinhronizēta ar krājumu redzamību. Ja neesat pārliecināts, kāds ir jūsu galapunkts, sazinieties ar sistēmas administratoru. Galapunktu vietrāžiem URL tiek izmantots šāds formāts:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Datu avota konfigurācija

Katrs datu avots atspoguļo sistēmu, no kuras nāk dati. Datu avotu nosaukumu piemēri ietver `fno` (kas atbilst Supply Chain Management) un `pos` (kas nozīmē "tirdzniecības vieta"). Pēc noklusējuma Krājumu redzamības programma Supply Chain Management ir iestatīta kā noklusējuma datu avots (`fno`).

> [!NOTE]
> Datu `fno` avots ir rezervēts programmatūrai Supply Chain Management. Ja krājumu redzamības pievienojumprogramma ir integrēta Supply Chain Management vidē, ieteicams neizdzēst konfigurācijas, kas ir saistītas ar `fno` datu avotu.

Lai izveidotu datu avotu, veiciet tālāk aprakstītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Datu avots atlasiet** Jauns datu **avots**, lai pievienotu datu avotu (piemēram`ecommerce`, vai citu jēgpilnu datu avota ID).

> [!NOTE]
> Kad pievienojat datu avotu, pirms Krājumu redzamības pakalpojuma konfigurācijas atjaunināšanas noteikti pārbaudiet datu avota nosaukumu, fiziskos izmērus un dimensiju kartējumus. Pēc **Konfigurācijas atjaunināšanas** atlases šos iestatījumus nevarēsit modificēt.

Datu avota konfigurācija ietver šādas daļas:

- Izmēri (izmēru kartēšana)
- Fiziskie mēri
- Aprēķinātie līdzekļi

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Izmēri (izmēru kartēšana)

Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām. Krājumu redzamība sniedz pamatdimensiju sarakstu, kuras var kartēt no datu avota dimensijām. Kartēšanai ir pieejamas trīsdesmit trīs dimensijas.

- Ja kā vienu no datu avotiem izmantojat Supply Chain Management, 13 kategorijas jau pēc noklusējuma tiek kartētas uz Supply Chain Management standarta dimensijām. Pārējās 12 dimensijas (`inventDimension1` caur `inventDimension12`) arī tiek kartētas uz pielāgotām dimensijām piegādes ķēdes pārvaldībā. Atlikušās astoņas dimensijas (`ExtendedDimension1` caur `ExtendedDimension8`) ir paplašinātas dimensijas, kuras var kartēt uz ārējiem datu avotiem.
- Ja neizmantojiet Supply Chain Management kā vienu no jūsu datu avotiem, varat brīvi kartēt dimensijas. Tabulā ir parādīts pilns pieejamo dimensiju saraksts.

> [!NOTE]
> Ja izmantojat programmatūru Supply Chain Management un maināt noklusējuma dimensiju kartējumus starp Supply Chain Management un Inventory Visibility, mainītā dimensija nesinhronizēs datus. Tāpēc, ja jūsu kategorija nav noklusējuma dimensiju sarakstā un izmantojat ārēju datu avotu, ieteicams to izmantot `ExtendedDimension1``ExtendedDimension8`, lai veiktu kartēšanu.

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
> Iepriekšējā tabulā norādītie dimensiju tipi ir paredzēti tikai jūsu atsaucei. Tie nav jādefinē Krājumu redzamībā.
>
> Krājumu (pielāgotās) dimensijas var būt rezervētas programmatūrai Supply Chain Management. Tādā gadījumā tā vietā izmantojiet paplašinātos izmērus.

Ārējās sistēmas var piekļūt krājumu redzamībai, izmantojot tā RESTful API. Integrācijai krājumu redzamība ļauj konfigurēt *ārējo datu avotu* un *ārējo dimensiju* kartēšanu uz *pamatdimensijām*. Tālāk ir sniegts dimensiju kartēšanas tabulas piemērs.

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
1. Cilnē **Datu avots** atlasiet datu avotu, kurā vēlaties veikt dimensiju kartēšanu. Pēc tam sadaļā Dimensiju kartējumi **atlasiet** Pievienot **,** lai pievienotu dimensiju kartējumus.

    ![Pievienot dimensiju kartējumus](media/inventory-visibility-dimension-mapping.png "Pievienot dimensiju kartējumus")

1. Laukā **Dimensijas nosaukums** norādiet avota dimensiju.
1. Laukā **Uz pamatdimensiju** atlasiet dimensiju Krājumu redzamībā, ko vēlaties kartēt.
1. Atlasiet **Saglabāt**.

Piemēram, jūs jau esat izveidojis datu avotu ar nosaukumu `ecommerce`, un tajā ir iekļauta preces krāsas dimensija. Šādā gadījumā, lai veiktu kartēšanu, vispirms varat pievienot `ProductColor` datu avota laukam **Dimension Name un pēc tam**`ecommerce` atlasīt laukā To Base Dimension`ColorId`**.**

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fiziskie mēri

Ja datu avots grāmato krājumu izmaiņas Krājumu redzamībai, tas grāmato šīs izmaiņas, izmantojot *fiziskos pasākumus*. Fiziskie pasākumi modificē daudzumu un atspoguļo krājumu statusu. Jūs varat definēt savus fiziskos mērus, pamatojoties uz jūsu prasībām. Vaicājumu pamatā var būt fiziskie pasākumi.

Krājumu redzamība nodrošina sarakstu ar noklusējuma fiziskajiem mēriem, kas ir kartēti uz Supply Chain Management (`fno` datu avots). Šie noklusējuma fiziskie pasākumi tiek ņemti no krājumu darbību statusiem Supply Chain Management lapā **Rīcībā esošie krājumi** (**Krājumu pārvaldība \> Pieprasījumi un pārskati \> Rīcībā esošo pārskatu saraksts**). Tabulā sniegts fizisko līdzekļu piemērs.

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

Ja datu avots ir Supply Chain Management, noklusējuma fiziskie mēri nav jāizveido no jauna. Tomēr ārējiem datu avotiem var izveidot jaunus fiziskos krājumus, veicot šādus soļus.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Datu avots** atlasiet datu avotu, kuram pievienot fiziskus mērus `ecommerce` (piemēram, datu avotu). Pēc tam sadaļā Fiziskie **mēri** atlasiet **Pievienot** un norādiet mēra nosaukumu (piemēram, `Returned` ja šajā datu avotā vēlaties ierakstīt atgrieztos daudzumus krājumu pārskatāmībā). Saglabājiet izmaiņas.

### <a name="calculated-measures"></a>Aprēķinātie līdzekļi

Varat izmantot Krājumu redzamību, lai pieprasītu gan krājumu fiziskos izmērus, gan *pielāgotos aprēķinātos izmērus*. Aprēķinātie pasākumi nodrošina pielāgotu aprēķināšanas formulu, kas sastāv no fizisko līdzekļu kombinācijas. Funkcionalitāte vienkārši ļauj definēt fizisko mērvienību kopu, kas tiks pievienota, un/vai fizisko mēru kopu, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.

> [!IMPORTANT]
> Aprēķināts mērs ir fizisko mēru sastāvs. Tās formula var ietvert tikai fiziskus mērus bez dublikātiem, nevis aprēķinātus mērus.

Konfigurācija ļauj definēt aprēķināto mērījumu formulu kopu, kas ietver saskaitīšanas vai atņemšanas modifikatorus, lai iegūtu kopējo apkopoto izvades daudzumu.

Lai iestatītu pielāgotos aprēķinātos mērījumus, izpildiet tālāk norādītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Aprēķinātais līdzeklis** atlasiet **Jaunu aprēķināto mērījumu**, lai pievienotu aprēķināto mērījumu.
1. Jaunajam aprēķinātajam mēram iestatiet šādus laukus:

    - **Jauns aprēķinātā mēra nosaukums** — ievadiet aprēķinātā mēra nosaukumu.
    - **Datu avots** — atlasiet datu avotu, kurā iekļaut jauno aprēķināto mēru. Vaicāšanas sistēma ir datu avots.

1. Atlasiet **Pievienot**, lai jaunajam aprēķinātajam mēram pievienotu modifikatoru.
1. Iestatiet jaunajam modifikatoram šādus laukus:

    - **Modifikators** - atlasiet modifikatora veidu (*saskaitīšana* vai *atņemšana*).
    - **Datu avots** — atlasiet datu avotu, kurā jāatrod mērs, kas nodrošina modifikatora vērtību.
    - **Mērījums** — atlasiet mēra nosaukumu (no atlasītā datu avota), kas nodrošina modifikatora vērtību.

1. Atkārtojiet 5.–6. darbību, līdz esat pievienojis visus nepieciešamos modifikatorus un pabeidzis aprēķinātā mērījuma formulu.
1. Atlasiet **Saglabāt**.

Piemēram, modes uzņēmums darbojas trīs datu avotos:

- `pos`– Atbilst veikala kanālam.
- `fno`– atbilst piegādes ķēdes vadībai.
- `ecommerce`- Atbilst jūsu tīmekļa kanālam.

Bez aprēķinātajiem mēriem, vaicājot par produktu D0002 (kabinets) 1. vietā, 11. noliktavā un dimensijas `ColorID` vērtību `Red`, jūs varat iegūt šādu vaicājuma rezultātu, kas parāda krājumu daudzumus zem katra iepriekš konfigurētā fiziskā mēra. Tomēr jūsu datu avotos nav redzamas rezervācijas daudzumam pieejamās kopsummas.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Izmantojot šo aprēķināšanas formulu, jaunais vaicājuma rezultāts ietvers pielāgoto mērījumu.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` izvade, pamatojoties pielāgoto mērījumu aprēķinu iestatījumā ir: 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Nodalījuma konfigurācija

Pašlaik nodalījuma konfigurācija sastāv no divām bāzes dimensijām (`SiteId` un `LocationId`), kas norāda, kā dati tiek sadalīti. Operācijas vienā nodalījumā var nodrošināt augstāku veiktspēju par zemākām izmaksām. Tālāk esošajā tabulā ir parādīta noklusējuma nodalījuma konfigurācija, ko nodrošina krājumu redzamības pievienojumprogramma.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Risinājums pēc noklusējuma ietver šo nodalījuma konfigurāciju. *Tāpēc jums tas nav jādefinē pats*.

> [!IMPORTANT]
> Nepielāgojiet noklusējuma nodalījuma konfigurāciju. Ja to izdzēsīsit vai mainīsit, visticamāk, radīsies neparedzēta kļūda.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Preču indeksa hierarhijas konfigurācija

Lielākā daļa laika rīcībā esošo krājumu vaicājums nebūs tikai augstākajā "kopsummas" līmenī. Tā vietā, iespējams, vēlēsities skatīt arī rezultātus, kas tiek apkopoti, pamatojoties uz krājumu dimensijām.

Krājumu redzamība nodrošina elastību, ļaujot iestatīt *indeksus*, lai uzlabotu vaicājumu veiktspēju. Šie indeksi ir balstīti uz dimensiju vai dimensiju kombināciju. Indeksu veido *kopas numurs*, *dimensija* un *hierarhija*, kā norādīts šajā tabulā.

| Nosaukums/vārds, uzvārds | Apraksts |
|---|---|
| Kopas skaitlis | Kopas numurs – dimensijas, kas pieder vienai kopai (indeksam), tiks grupētas kopā, un tām tiks piešķirts vienāds kopas numurs. |
| Dimensija | Pamatdimensijas, uz kurām vaicājuma rezultāts tiek apkopots. |
| Hierarhija | Hierarhija ļauj palielināt noteiktu dimensiju kombināciju veiktspēju, ja tās tiek izmantotas filtra un grupēšanas vaicājuma parametros. Piemēram, ja iestatāt dimensiju kopu ar hierarhijas secību `(ColorId, SizeId, StyleId)`, sistēma var ātrāk apstrādāt vaicājumus, kas saistīti ar četrām dimensiju kombinācijām. Pirmā kombinācija ir tukša, otrā ir `(ColorId)`, trešā ir `(ColorId, SizeId)` un ceturtā ir `(ColorId, SizeId, StyleId)`. Citas kombinācijas netiks paātrinātas. Filtri nav ierobežoti pēc pasūtījuma, taču tiem ir jābūt iekļautiem šajos izmēros, ja vēlaties uzlabot to veiktspēju. Papildinformāciju skatiet tālāk norādītajās tēmās. |

Lai iestatītu produktu hierarhijas indeksus, veiciet tālāk norādītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Dimensiju kartējumi** atlasiet **Pievienot**, lai pievienotu dimensiju kartējumus.
1. Pēc noklusējuma ir sniegts indeksu saraksts. Lai modificētu esošo indeksu, izvēlieties **Labot** vai **Pievienot** atbilstošā indeksa sadaļā. Lai izveidotu jaunu indeksu kopu, atlasiet **Jauna indeksu kopa**. Katrai rindai katrā indeksu kopā laukā **Dimensija** atlasiet pamatdimensiju sarakstā. Automātiski tiek ģenerētas šādu lauku vērtības:

    - **Kopas numurs** – dimensijas, kas pieder vienai grupai (indeksam), tiks grupētas kopā, un tām tiks piešķirts vienāds kopas numurs.
    - **Hierarhija** — hierarhija palielina noteiktu dimensiju kombināciju veiktspēju, ja tās tiek izmantotas filtra un grupēšanas vaicājuma parametros.

> [!TIP]
> Tālāk ir sniegti daži padomi, kas jāņem vērā, iestatot indeksu hierarhiju.
>
> - Pamata dimensijas, kas ir definētas nodalījuma konfigurācijā, nevajadzētu definēt indeksa konfigurācijās. Ja indeksa konfigurācijā bāzes dimensija tiek definēta vēlreiz, šis indekss nevarēs veikt vaicājumus.
> - Ja jums ir jāvaicā tikai par krājumiem, kas tiek apkopoti visās dimensiju kombinācijās, iestatiet vienu indeksu, kas satur pamata dimensiju `Empty`.

### <a name="example"></a>Paraugs

Šajā sadaļā sniegts piemērs, kā hierarhija darbojas.

Šajā tabulā sniegts šajā piemērā pieejamo krājumu saraksts.

| Krājums | ColorId | SizeId | StyleId | Daudzums |
|---|---|---|---|---|
| D0002 | Melna | Maza | Plats | 1 |
| D0002 | Melna | Maza | Regulārs | 2 |
| D0002 | Melna | Liela | Plats | 3 |
| D0002 | Melna | Liela | Regulārs | 4 |
| D0002 | Sarkana | Maza | Plats | 5 |
| D0002 | Sarkana | Maza | Regulārs | 6 |
| D0002 | Sarkana | Liela | Regulārs | 7 |

Nākamajā tabulā ir parādīts, kā tiek iestatīta indeksu hierarhija.

| Kopas skaitlis | Dimensija | Hierarhija |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indekss ļauj veikt rīcībā esošo krājumu vaicājumu šādos veidos:

- `()`– grupēt pēc visiem

    - D0002, 28

- `(ColorId)` – grupēts pēc `ColorId`

    - D0002, melns, 10
    - D0002, sarkans, 18

- `(ColorId, SizeId)` – grupēts pēc `ColorId` un `SizeId` kombinācijas

    - D0002, melns, mazs, 3
    - D0002, melns, liels, 7
    - D0002, sarkans, mazs, 11
    - D0002, sarkans, liels, 7

- `(ColorId, SizeId, StyleId)` – grupēts pēc `ColorId`, `SizeId` un `StyleId` kombinācijas

    - D0002, melns, mazs, plats, 1
    - D0002, melns, mazs, regulārs, 2
    - D0002, melns, liels, plats, 3
    - D0002, melns, liels, regulārs, 4
    - D0002, sarkans, mazs, plats, 5
    - D0002, sarkans, mazs, regulārs, 6
    - D0002, sarkans, liels, regulārs, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervācijas konfigurācija (nav obligāti)

Rezervācijas konfigurācija ir nepieciešama, ja vēlaties izmantot vieglās rezervēšanas funkciju. Konfigurācija sastāv no divām fundamentālajām daļām:

- Vieglās rezervācijas kartēšana
- Vieglās rezervācijas hierarhija

### <a name="soft-reservation-mapping"></a>Vieglās rezervācijas kartēšana

Veicot rezervāciju, iespējams, vēlēsieties zināt, vai rīcībā esošie krājumi pašlaik ir pieejami rezervēšanai. Apstiprināšana ir saistīta ar aprēķinātu mērījumu, kas attēlo fizisko mērījumu kombinācijas skaitļošanas formulu.

Iestatot kartējumu no fiziskā mēra uz aprēķināto mērījumu, iespējojiet Krājumu redzamības pakalpojumu, lai automātiski validētu rezervāciju pieejamību, pamatojoties uz fizisko mērījumu.

Pirms šīs kartēšanas iestatīšanas fiziskie mēri, aprēķinātie mēri un to datu avoti ir jādefinē **konfigurācijas lapas** cilnē **Datu** avots **un** Aprēķinātais mērs Power Apps (kā aprakstīts iepriekš šajā rakstā).

Lai definētu vieglās rezervācijas kartēšanu, veiciet šādas darbības.

1. Nosakiet fizisko mērījumu, kas kalpo kā vieglās rezervēšanas mērs (piemēram, `SoftReservPhysical`).
1. Lapas **Konfigurācija** cilnē **Aprēķinātais līdzeklis** definējiet *rezervēšanai pieejamo* (AFR) skaitļošanas formulu, kuru vēlaties kartēt uz fizisko mērījumu. Piemēram, varat iestatīt `AvailableToReserve` (pieejams rezervācijai), lai tas būtu kartēts uz iepriekš noteiktu `SoftReservPhysical` fizisko mērījumu. Šādā veidā var atrast daudzumus, kuru `SoftReservPhysical` krājumu statuss ir pieejams rezervēšanai. Tabulā ir parādīta AFR aprēķina formula.

    | Aprēķina tips | Datu avots | Fiziskais mērs |
    |---|---|---|
    | Papildinājums | `fno` | `AvailPhysical` |
    | Papildinājums | `pos` | `Inbound` |
    | Atņemšana | `pos` | `Outbound` |
    | Atņemšana | `iv` | `SoftReservPhysical` |

    Iesakām iestatīt aprēķināto izmēru tā, lai tas saturētu fizisko mērījumu, kurā ir balstīts rezervācijas mērījums. Tādējādi aprēķinātā mērījuma daudzumu ietekmēs rezervācijas mērījumu daudzums. Tāpēc Šajā piemērā `iv` datu avota `AvailableToReserve` aprēķinātajam mērījumam vajadzētu saturēt `SoftReservPhysical` fizisko mērījumu no `iv` kā komponentu.

1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Vieglās rezervācijas kartēšana** iestatiet kartējumu no fiziskā mēra uz aprēķināto mērījumu. Iepriekšējā piemērā varat izmantot tālāk norādītos iestatījumus, lai kartētu `AvailableToReserve` uz iepriekš definēto `SoftReservPhysical` fizisko mērījumu.

    | Fiziskais mēra datu avots | Fiziskais mērs | Pieejams rezervēšanas datu avotam | Pieejams rezervēšanai aprēķinātam mēram |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Ja nevarat rediģēt cilni **Vieglās rezervācijas kartēšana**, jums, iespējams, vajadzēs iespējot līdzekli *OnHandReservation* cilnē **Līdzekļu pārvaldība**.

Tagad, kad veiksiet rezervāciju `SoftReservPhysical`, Krājumu redzamība automātiski atradīs un rezervēšanas validācijai tiks atrasta `AvailableToReserve` saistītā aprēķināšanas formula.

Piemēram, Krājumu redzamībai ir šādi rīcībā esošie krājumi.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound`– – `pos.outbound``iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Tāpēc, ja jūs mēģināt veikt rezervācijas, `iv.SoftReservPhysical` un daudzums ir mazāks vai vienāds ar `AvailableToReserve` (10), mīkstās rezervācijas pieprasījums būs veiksmīgs.

> [!NOTE]
> Izsaucot rezervācijas API, varat kontrolēt rezervācijas derīgumu, pieprasījuma laukā konkretizējot Būla `ifCheckAvailForReserv` parametru. Vērtība `True`, kas nozīmē, ka validācija ir nepieciešama, bet vērtība `False` nozīmē, ka validācija nav nepieciešama (lai gan jūs varat nonākt pie negatīva `AvailableToReserve` daudzuma, sistēma joprojām ļaus jums mīkstināt rezerves). Noklusējuma vērtība ir `True`.

### <a name="soft-reservation-hierarchy"></a>Vieglās rezervācijas hierarhija

Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tādā pašā veidā, kā preču indeksu hierarhija darbojas rīcībā esošos vaicājumos.

Rezervāciju hierarhija nav atkarīga no preču indeksu hierarhijas. Šī neatkarību ļauj ieviest kategoriju pārvaldību, kur lietotāji var sadalīt dimensijas detalizētāk, lai noteiktu prasības precīzākai rezervāciju veikšanai. Jūsu vieglās rezervācijas hierarhijai vajadzētu saturēt komponentus `SiteId` un `LocationId`, jo tie veido dalīšanās konfigurāciju. Veicot rezervāciju, ir jākonkretizē produkta dalījums.

Tālāk ir sniegts neierobežotas rezervēšanas hierarhijas piemērs.

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

## <a name="available-to-promise-configuration-optional"></a>Pieejama solījumu konfigurācijai (neobligāti)

Varat iestatīt krājumu redzamību, lai varētu ieplānot turpmākās rīcībā esošās izmaiņas un aprēķināt solīšanai pieejamos (ATP) daudzumus. ATP ir krājuma daudzums, kas ir pieejams un ko var apsolīt klientam nākamajā periodā. Šī aprēķina izmantošana var ievērojami palielināt jūsu pasūtījuma izpildes iespējas. Lai izmantotu šo funkciju, tā **ir jāiespējo cilnē Funkciju pārvaldība** un pēc tam jāiestata **cilnē ATP iestatījumi** . Papildinformāciju skatiet sadaļā [Krājumu redzamības rīcībā esošie izmaiņu grafiki, kas ir pieejami solīšanai](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Pabeidziet un atjauniniet konfigurāciju

Pēc konfigurācijas pabeigšanas ir jāveic visas izmaiņas Krājumu redzamībai. Veiciet šīs darbības, lai veiktu izmaiņas.

1. Konfigurācijas Power Apps **lapā augšējā** labajā stūrī atlasiet **Atjaunināt konfigurāciju**. 
1. Sistēma pieprasa pierakstīšanās akreditācijas datus. Ievadiet šādas vērtības:

    - **Klienta ID** — Azure programmas ID, ko izveidojāt Krājumu redzamībai.
    - **Nomnieka ID** — jūsu Azure nomnieka ID.
    - **Klienta slepenā informācija** — Azure pieteikuma slepenā informācija, ko izveidojāt Krājumu redzamībai.

    Papildinformāciju par šiem akreditācijas datiem un to, kā tos atrast, skatiet sadaļā [Krājumu redzamības](inventory-visibility-setup.md) instalēšana un iestatīšana.

    > [!IMPORTANT]
    > Pirms konfigurācijas atjaunināšanas noteikti pārbaudiet datu avota nosaukumu, fiziskos mērus un dimensiju kartējumus. Pēc atjaunināšanas nevarēsit modificēt šos iestatījumus.

1. Pēc pierakstīšanās vēlreiz atlasiet **Atjaunināt konfigurāciju**. Sistēma lieto jūsu iestatījumus un parāda, kas ir mainījies.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Noklusējuma konfigurācijas piemērs

Inicializācijas posmā Inventory Visibility iestata noklusējuma konfigurāciju, kura sīkāk aprakstīta šeit. Šo konfigurāciju varat pēc vajadzības pārveidot.

### <a name="data-source-configuration"></a>Datu avota konfigurācija

#### <a name="configuration-of-the-iv-data-source"></a>Datu avota konfigurācija

Šajā sadaļā ir aprakstīts, kā `iv` datu avots tiek konfigurēts.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fiziskie mēri, kas konfigurēti datu avotam "iv"

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

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensiju kartējumi datu avotam "fno"

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fiziskie mēri, kas konfigurēti datu avotam "fno"

Datu avotam ir konfigurēti šādi `fno` fiziskie pasākumi:

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>"POS" datu avota konfigurācija

Šajā sadaļā ir aprakstīts, kā `pos` datu avots tiek konfigurēts.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fiziskie mērījumi "pos" datu avotam

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

#### <a name="configuration-of-the-iom-data-source"></a>"IOM" datu avota konfigurācija

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
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Rezervāciju hierarhija

Tabulā ir parādīta noklusējuma rezervāciju kartēšana.

| Pamata dimensija | Hierarhija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
