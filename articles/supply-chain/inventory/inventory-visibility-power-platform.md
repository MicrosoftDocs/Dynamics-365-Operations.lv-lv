---
title: Krājumu redzamības programma
description: Šajā tēmā ir aprakstīts, kā izmantot Krājumu redzamības līdzekļus.
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
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345006"
---
# <a name="inventory-visibility-app"></a>Krājumu redzamības programma

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot Krājumu redzamības līdzekļus.

Krājumu redzamība nodrošina modeļa vadītas programmas vizualizēšanu. Programmā ir trīs lapas: **Konfigurācija**, **Operāciju redzamība** un **Krājumu kopsavilkums**. Tam ir tālāk minētās vērtības:

- Tā nodrošina lietotāja interfeisu (UI) rīcībā esošo konfigurāciju un vieglās rezervēšanas konfigurāciju.
- Tas atbalsta reāllaika rīcībā esošo krājumu vaicājumus par dažādām dimensiju kombinācijām.
- Tas sniedz UI rezervāciju pieprasījumu grāmatošanai.
- Tajā ir pielāgots rīcībā esošo krājumu skats precēm kopā ar visām dimensijām

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, instalējiet un iestatiet Krājumu redzamības pievienojumprogrammu, kā tas ir aprakstīts sadaļā [Iestatīt Krājumu redzamību](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Konfigurācija

Lapa **Konfigurācija** palīdz iestatīt rīcībā esošo konfigurāciju un vieglās rezervācijas konfigurāciju. Pēc pievienojumprogrammas instalēšanas noklusējuma konfigurācija ietver Microsoft Dynamics 365 Supply Chain Management (datu avotu `fno`) vērtību. Varat pārskatīt noklusēto iestatījumu. Turklāt, balstoties uz jūsu uzņēmējdarbības prasībām un jūsu ārējās sistēmas krājumu grāmatošanas prasībām, jūs varat modificēt konfigurāciju, lai standartizētu veidu, kādā krājumu izmaiņas var iegrāmatot, organizēt un vaicāt vairākās [Dataverse](/powerapps/maker/common-data-service/data-platform-intro)sistēmās.

### <a name="define-data-sources"></a>Datu avotu definēšana

Definējiet katru *datu avotu*, kuru vēlaties integrēt ar Krājumu redzamību. Krājumu redzamība atbalsta integrāciju ar dažādiem datu avotiem, piemēram, pārdošanas punkta (POS) sistēmu, Supply Chain Management un citām ārējām sistēmām. Pēc noklusējuma Krājumu redzamības programma Supply Chain Management ir iestatīta kā noklusējuma datu avots (`fno`).

Lai izveidotu datu avotu, veiciet tālāk aprakstītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Datu avots** atlasiet **Jauns datu avots**, lai pievienotu datu avotu.

> [!NOTE]
> Kad pievienojat datu avotu, pirms Krājumu redzamības pakalpojuma konfigurācijas atjaunināšanas noteikti pārbaudiet datu avota nosaukumu, fiziskos izmērus un dimensiju kartējumus. Pēc **Konfigurācijas atjaunināšanas** atlases šos iestatījumus nevarēsit modificēt.

### <a name="set-up-dimension-mappings"></a>Iestatīt dimensiju kartējumus

Krājumu redzamība sniedz pamatdimensiju sarakstu, kuras var kartēt no datu avota dimensijām. Kartēšanai ir pieejamas trīsdesmit trīs dimensijas.

- Pēc noklusējuma, ja jūs izmantojat Supply Chain Management kā vienu no jūsu datu avotiem, 13 dimensijas tiek kartētas uz Supply Chain Management standarta dimensijām. Pārējās divpadsmit dimensijas (`inventDimension1` ar `inventDimension12`) tiek kartētas uz pielāgotām dimensijām Supply Chain Management. Atlikušās astoņas dimensijas ir paplašinātās dimensijas, kuras var kartēt uz ārējiem datu avotiem.
- Ja neizmantojiet Supply Chain Management kā vienu no jūsu datu avotiem, varat brīvi kartēt dimensijas. Tabulā ir parādīts pilns pieejamo dimensiju saraksts.

> [!NOTE]
> Ja dimensijas nav noklusējuma dimensiju sarakstā un jūs izmantojat ārēju datu avotu, ieteicams izmantot to `ExtendedDimension1` ar `ExtendedDimension8` kartēšanas darbības laikā.

| Dimensiju veids | Dimensijas nosaukums |
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
| Specifiska noliktava | `WMSLocationId` |
| Specifiska noliktava | `WMSPalletId` |
| Specifiska noliktava | `LicensePlateId` |
| Cita | `VersionId` |
| Krājumi (pielāgoti) | `InventDimension1` ar `InventDimension12` |
| Cita | `ExtendedDimension1` ar `ExtendedDimension8` |

Lai pievienotu dimensiju kartējumus, rīkojieties šādi.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Dimensiju kartējumi** atlasiet **Pievienot**, lai pievienotu dimensiju kartējumus.
1. Laukā **Dimensijas nosaukums** norādiet avota dimensiju.
1. Laukā **Uz pamatdimensiju** atlasiet dimensiju Krājumu redzamībā, ko vēlaties kartēt.
1. Atlasiet **Saglabāt**.

![Pievienot dimensiju kartējumus](media/inventory-visibility-dimension-mapping.png "Pievienot dimensiju kartējumus")

Piemēram, ja datu avots ietver preces krāsas dimensiju, varat to kartēt uz `ColorId` pamatdimensiju, lai pievienotu pielāgotu `ProductColor` dimensiju `exterchannel` datu avotam. Pēc tam tā ir kartēta uz `ColorId` pamatdimensiju.

## <a name="create-a-physical-measure"></a>Fiziskas mērvienības izveide

Ja datu avots grāmato krājumu izmaiņas Krājumu redzamībai, tas grāmato šīs izmaiņas, izmantojot *fiziskos pasākumus*. Fiziskie pasākumi ir modifikatori, kas atspoguļo apkopoto krājumu darbību statusus. Vaicājumu pamatā var būt fiziskie pasākumi.

Krājumu redzamībai ir noklusējuma fizisko krājumu saraksts. Šie noklusējuma fiziskie pasākumi tiek ņemti no krājumu darbību statusiem Supply Chain Management lapā **Rīcībā esošie krājumi** (**Krājumu pārvaldība \> Pieprasījumi un pārskati \> Rīcībā esošo pārskatu saraksts**).

| Modifikators | Nosaukums/vārds, uzvārds |
|---|---|
| `PhysicalInvent` | Fizisks krājums |
| `ReservPhysical` | Rezervēts fiziski |
| `AvailPhysical` | Fiziski pieejams |
| `ReservOrdered` | Rezervēts pasūtījumos |
| `PostedQty` | Grāmatotais daudzums |
| `Deducted` | Atskaitīts |
| `Picked` | Izdots |
| `Received` | Saņemts |
| `Registered` | Reģistrēts |
| `Arrived` | Pienācis |
| `Ordered` | Pasūtīts |
| `OnOrder` | Pasūtīts |
| `QuotationReceipt` | PIedāvājuma kvīts |
| `QuotationIssue` | Piedāvājuma izsniegšana |

Ja datu avots ir Supply Chain Management, jums nav no jauna jāizveido noklusējuma fiziskie pasākumi. Tomēr ārējiem datu avotiem var izveidot jaunus fiziskos krājumus, veicot šādus soļus.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Fiziskie mēri** atlasiet **Pievienot**, norādiet avota mērvienības nosaukumu un saglabājiet izmaiņas.

## <a name="define-the-product-hierarchy-index"></a>Definēt preču hierarhijas indeksu

Iestatot uzkrātās dimensiju grupas, varat izmantot krājumu redzamību, lai pieprasītu rīcībā esošo krājumu statusu. Krājumu redzamības katru dimensiju grupu sauc par *indeksu*. Katrs indekss atbilst iestatītam numuram. Varat izlemt, kuras dimensijas tiks lietotas indeksēšanas iestatīšanai, pamatojoties uz veidu, kādā vaicāsiet krājumu redzamībai.

Lai iestatītu produktu hierarhijas indeksus, veiciet tālāk norādītās darbības.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnes **Datu avots** sadaļā **Dimensiju kartējumi** atlasiet **Pievienot**, lai pievienotu dimensiju kartējumus.
1. Pēc noklusējuma ir sniegts indeksu saraksts. Lai modificētu esošo indeksu, izvēlieties **Labot** vai **Pievienot** atbilstošā indeksa sadaļā. Lai izveidotu jaunu indeksu kopu, atlasiet **Jauna indeksu kopa**. Katrai rindai katrā indeksu kopā laukā **Dimensija** atlasiet pamatdimensiju sarakstā. Automātiski tiek ģenerētas šādu lauku vērtības:

    - **Kopas numurs** – dimensijas, kas pieder vienai grupai (indeksam), tiks grupētas kopā, un tām tiks piešķirts vienāds kopas numurs.
    - **Hierarhija** – hierarhija tiek izmantota, lai definētu atbalstītās dimensiju kombinācijas, kuras var vaicāt dimensiju grupā (indekss). Piemēram, ja iestatāt dimensiju grupu, kam ir hierarhijas secība *Stils*, *Krāsa* un *Lielums*, sistēma atbalsta trīs vaicājumu grupu rezultātus. Pirmā grupa ir tikai stils. Otrā grupa ir stila un krāsas kombinācija. Trešā grupa ir stila, krāsas un izmēra kombinācija. Citas kombinācijas netiek atbalstītas.

Papildinformāciju skatiet [Preču indeksa hierarhijas konfigurēšana](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Paraugs

Šajā sadaļā sniegts piemērs, kā hierarhija darbojas. Šajā tabulā sniegts šajā piemērā pieejamo krājumu saraksts.

| Objekts | Stils | krāsa | izmērs | Daudzums |
|---|---|---|---|---|
| I0001 | Plats | Melna | Mazs | 1 |
| I0001 | Plats | Melna | Liels | 2 |
| I0001 | Plats | Sarkanā | Mazs | 3 |
| I0001 | Regulārs | Melna | Mazs | 4 |
| I0001 | Regulārs | Melna | Liels | 5 |
| I0001 | Regulārs | Sarkanā | Mazs | 6 |
| I0001 | Regulārs | Sarkanā | Liels | 7 |

Nākamajā tabulā ir parādīts, kā tiek iestatīta indeksu hierarhija.

| Princips | Kopas skaitlis | Hierarhija |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Pamatojoties uz iepriekš minētajiem iestatījumiem, krājumu redzamības vaicājuma dimensiju kombinācija ir *Stils*, *Krāsa* un *Izmērs*. Hierarhijas iestatīšana ļauj ārējām sistēmām veikt rīcībā esošo krājumu vaicājumu šādos veidos:

- `()`– grupēt pēc visiem. Šeit ir iegūtā izvade:

    - I0001, 28

- `(StyleId)` – grupēt pēc stila. Šeit ir iegūtā izvade:

    - I0001, plats, 6
    - I0001, standarta, 22

- `(StyleId, ColorId)` – grupēts pēc stila un krāsas kombinācijas. Šeit ir iegūtā izvade:

    - I0001, plats, melns, 3
    - I0001, plats, sarkans, 3
    - I0001, parasts, melns, 9
    - I0001, parasts, sarkans, 13

- `(StyleId, ColorId, SizeId)` – grupēts pēc stila, krāsas un izmēra kombinācijas. Šeit ir iegūtā izvade:

    - I0001, plats, melns, mazs, 1
    - I0001, plats, melns, liels, 2
    - I0001, plats, sarkans, mazs, 3
    - I0001, parasts, melns, mazs, 4
    - I0001, parasts, melns, liels, 5
    - I0001, parasts, sarkans, mazs, 6
    - I0001, parasts, sarkans, liels, 7

## <a name="set-up-a-custom-calculated-measure"></a>Iestatīt pielāgotu aprēķināto mērījumu

Varat izmantot Krājumu redzamību, lai pieprasītu gan krājumu fiziskos izmērus, gan *pielāgotos aprēķinātos izmērus*.

Konfigurācija ļauj definēt modifikatoru kopu, kas tiek pievienota vai atņemta, lai iegūtu kopējo uzkrāto izvades daudzumu.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Aprēķinātais līdzeklis** atlasiet **Jaunu aprēķināto mērījumu**, lai pievienotu aprēķināto mērījumu. Pēc tam iestatiet laukus, kā aprakstīts nākamajā tabulā.

    | Lauks | Vērtība |
    |---|---|
    | Jauns aprēķinātā mēra nosaukums | Ievadiet aprēķinātā mēra nosaukumu. |
    | Datu avots | Vaicāšanas sistēma ir datu avots. |
    | Modifikatora datu avots | Skatiet vai ievadiet modifikatora avota tipu. |
    | Modifikators | Ievadiet modifikatora vārdu. |
    | Modifikatora veids | Atlasiet modifikatora tipu (*Saskaitīšana* vai *Atņemšana*). |

Tālāk esošajā tabulā ir norādīts `MyCustomAvailableforReservation` pielāgota aprēķinātā mēra piemērs. Plašāku informāciju par šo piemēru skatiet [Datu avota konfigurācijā](inventory-visibility-configuration.md#data-source-configuration).

| Aprēķinātais mēra datu avots | Aprēķinātais līdzeklis | Modifikatora datu avots | Modifikators | Modifikatora veids |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Vieglās rezervācijas kartēšanas iestatīšana

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Pirms varat rediģēt cilni **Vieglās rezervācijas kartēšana**, ir jāiespējo funkcija *OnHandReservation* cilnē **Līdzekļu pārvaldība**.

Iestatot kartējumu no fiziskā mēra uz aprēķināto mērījumu, iespējojiet Krājumu redzamības pakalpojumu, lai automātiski validētu rezervāciju pieejamību, pamatojoties uz fizisko mērījumu.

Pirms kartēšanas iestatīšanas, lapas **Konfigurācija** cilnēs **Datu avots** un **Aprēķinātais līdzeklis** ir jābūt definētiem fiziskajiem līdzekļiem, aprēķinātajiem līdzekļiem un to datu avotiem programmā Power Apps (kā iepriekš aprakstīts šajā tēmā).

Lai definētu vieglās rezervācijas kartēšanu, veiciet šādas darbības.

1. Nosakiet fizisko mērījumu, kas kalpo kā vieglās rezervēšanas mērs (piemēram, `softreservordered`).
1. Lapas **Konfigurācija** cilnē **Aprēķinātais līdzeklis** definējiet *rezervēšanai pieejamo* (AFR) skaitļošanas formulu, kuru vēlaties kartēt uz fizisko mērījumu. Piemēram, varat iestatīt `availforreserv` (pieejams rezervācijai), lai tas būtu kartēts uz iepriekš noteiktu `softreservordered` fizisko mērījumu. Šādā veidā var atrast daudzumus, kuru `softreservordered` krājumu statuss ir pieejams rezervēšanai. Tabulā ir parādīta AFR aprēķina formula.

    | Modifikators | Datu avots | Mērījums |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Atveriet lapu **Konfigurācija**.
1. Cilnē **Vieglās rezervācijas kartēšana** iestatiet kartējumu no fiziskā mēra uz aprēķināto mērījumu. Iepriekšējā piemērā varat izmantot tālāk norādītos iestatījumus, lai kartētu `availforreserv` uz iepriekš definēto `softreservordered` fizisko mērījumu.

    | Fiziskais mēra datu avots | Fiziskais mērs | Pieejams rezervēšanas datu avotam | Pieejams rezervēšanai aprēķinātam mēram |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Vieglās rezervācijas hierarhijas iestatīšana

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Pirms varat rediģēt cilni **Vieglās rezervācijas kartēšana**, ir jāiespējo funkcija *OnHandReservation* cilnē **Līdzekļu pārvaldība**.

Rezervāciju hierarhija apraksta dimensiju secību, kas jānorāda, veicot rezervācijas. Tas darbojas tādā pašā veidā, kā preču indeksu hierarhija darbojas rīcībā esošos vaicājumos.

Rezervāciju hierarhija var atšķirties no rīcībā esošās indeksu hierarhijas. Šī neatkarību ļauj ieviest kategoriju pārvaldību, kur lietotāji var sadalīt dimensijas detalizētāk, lai noteiktu prasības precīzākai rezervāciju veikšanai.

#### <a name="example"></a>Paraugs

Sistēmā ir iestatīta tālāk norādītā rezervāciju hierarhija.

| Dimensija | Hierarhija |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Ņemot vērā šo rezervāciju hierarhiju, varat veikt rezervāciju šādos dimensiju pasūtījumos:

- `()`– dimensija nav dota.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Dimensiju secībai ir stingri jāievēro rezervāciju hierarhijas secība, dimensija pēc dimensijas. Piemēram, rezervācijas ar `(ColorId, StyleId)` šajā piemērā netiks atļautas, jo šī secība nav definēta rezervāciju hierarhijā.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Līdzekļu pārvaldības kontrole

Krājumu redzamības pievienojumprogramma nodrošina tādus līdzekļus kā *OnHandReservation* un *OnHandMostSpecificBackgroundService*. Pēc noklusējuma šie līdzekļi ir izslēgti. Lai tos lietotu, atveriet lapu **Konfigurācija** programmā Power Apps un pēc tam cilnē **Līdzekļu pārvaldība** iespējojeit tos.

### <a name="complete-and-update-the-configuration"></a>Pabeidziet un atjauniniet konfigurāciju

Pēc konfigurācijas pabeigšanas ir jāveic visas izmaiņas Krājumu redzamībai. Lai veiktu izmaiņas, atlasiet **Atjaunināt konfigurāciju** lapas **Konfigurācija** augšējā labajā stūrī programmā Power Apps.

Pirmo reizi atlasot **Atjaunināt konfigurāciju**, sistēma pieprasa savus akreditācijas datus.

- **Klienta ID** — Azure programmas ID, ko izveidojāt Krājumu redzamībai.
- **Nomnieka ID** — jūsu Azure nomnieka ID.
- **Klienta slepenā informācija** — Azure pieteikuma slepenā informācija, ko izveidojāt Krājumu redzamībai.

Pēc pieteikšanās konfigurācija tiek atjaunināta Krājumu redzamības pakalpojumā.

> [!NOTE]
> Kad pievienojat datu avotu, pirms Krājumu redzamības pakalpojuma konfigurācijas atjaunināšanas noteikti pārbaudiet datu avota nosaukumu, fiziskos izmērus un dimensiju kartējumus. Pēc **Konfigurācijas atjaunināšanas** atlases šos iestatījumus nevarēsit modificēt.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Atrast pakalpojuma galapunktu

Ja nezināt pareizo Krājumu redzamības pakalpojuma galapunktu, atveriet lapu **Konfigurācija** programmā Power Apps un pēc tam augšējā labajā stūrī atlasiet **Rādīt pakalpojuma galapunktu**. Lapa parādīs pareizo pakalpojuma galapunktu.

## <a name="operational-visibility"></a>Darbības redzamība

Lapa **Darbības redzamība** sniedz reāllaika rīcībā esošo krājumu vaicājuma rezultātus, kas pamatoti uz dažādām dimensiju kombinācijām. Ja ir ieslēgta funkcija *OnHandReservation*, varat arī grāmatot rezervēšanas pieprasījumus no lapas **Operāciju redzamība**.

### <a name="on-hand-query"></a>Rīcībā esošie vaicājumi

Cilnē **Rīcībā esošie vaicājumi** tiek rādīti reāllaika rīcībā esošo krājumu vaicājuma rezultāti.

Atlasot cilni **Rīcībā esošie vaicājumi**, sistēma pieprasa savus akreditācijas datus, lai varētu iegūt uzrādītāja marķieri, kas ir nepieciešams, lai vaicātu par Krājumu redzamības pakalpojumu. Variet tikai ielīmēt uzrādītāja marķieri laukā **BearerToken** un aizvērt dialoglodziņu. Pēc tam varat iegrāmatot rīcībā esošo vaicājumu pieprasījumu.

Ja uzrādītāja marķieris nav derīgs vai arī tā derīgums ir beidzies, pievienojiet jaunu laukā **BearerToken**. Ievadiet pareizo **Klienta ID**, **Nomnieka ID**, **Klienta slepeno informāciju** un pēc tam atlasiet **Atsvaidzināt**. Sistēma automātiski saņems jaunu, derīgu uzrādītāja marķieri.

Lai grāmatotu rīcībā esošo vaicājumu, ievadiet pieprasījuma pamattekstā. Izmantojiet Modeli, kas aprakstīts [Vaicājumā, izmantojot grāmatošanas metodi](inventory-visibility-api.md#query-with-post-method).

![Rīcībā esošie vaicājumu iestatījumi](media/inventory-visibility-query-settings.png "Rīcībā esošie vaicājumu iestatījumi")

### <a name="reservation-posting"></a>Rezervāciju grāmatošana

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Izmantojiet cilni **Rezervācijas grāmatošana**, lai grāmatotu rezervēšanas pieprasījumu. Pirms rezervēšanas pieprasījuma grāmatošanas ir jāslēdz funkcija *OnHandReservation*. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

Lai grāmatotu rezervēšanas pieprasījumu, pieprasījuma pamattekstā ir jāievada vērtība. Izmantojiet modeli, kas ir aprakstīts sadaļā [Izveidot vienu rezervācijas notikumu](inventory-visibility-api.md#create-one-reservation-event). Pēc tam atlasiet **Grāmatot**. Lai skatītu informāciju par atbildi, atlasiet **Rādīt detalizētu informāciju**. Jūs varat arī saņemt **reservationId** vērtību no atbildes informācijas.

## <a name="inventory-summary"></a>Krājumu kopsavilkums

**Krājumu kopsavilkums** ir pielāgots skats elementam *Rīcībā esošo krājumu summas entītija*. Tajā sniegts krājumu kopsavilkums precēm kopā ar visām dimensijām. Izmantojot **Papildu filtru**, ko nodrošina Dataverse, varat izveidot personisku skatu, kurā redzamas jums svarīgās rindas. Papildu filtra opcijas ļauj izveidot plašu skatījumu klāstu no vienkāršiem uz kompleksiem. Tie arī ļauj pievienot filtriem grupētus un ligzdotus nosacījumus.

Papildinformāciju par to, kā izmantot **Papildu filtru**, skatiet sadaļā [Rediģēt vai izveidot personālos skatus, izmantojot papildu režģa filtrus](/powerapps/user/grid-filters-advanced)

Pielāgotā skata augšpusē ir trīs lauki: **Noklusējuma dimensija**, **Pielāgotā dimensija** un **Mērs**. Šos laukus varat izmantot, lai kontrolētu, kuras kolonnas ir redzamas.

Var atlasīt kolonnas virsrakstu, lai filtrētu vai kārtotu pašreizējo rezultātu.

Pielāgotā skata apakšā ir redzama informācija, piemēram, "50 ieraksti (atlasīti 29)" vai "50 ieraksti." Šī informācija attiecas uz pašlaik ielādētajiem ierakstiem no **Papildu filtra** rezultāta. Teksts "atlasīts 29" attiecas uz ierakstu skaitu, kas ir atlasīti, ielādētajiem ierakstiem izmantojot kolonnas virsraksta filtru.

Skatījuma apakšdaļā ir poga **Ielādēt vairāk**, ko varat izmantot, lai ielādētu vairāk Dataverse ierakstu. Noklusējuma ielādēto ierakstu skaits ir 50. Ja atlasāt **Ielādēt vairāk**, nākamajā skatā tiek ielādēti nākamie 1000 pieejamie ieraksti. Pogas **Ielādēt vairāk** skaitlis norāda pašlaik ielādētos ierakstus un **Papildu filtra** rezultāta ierakstu kopējo skaitu.

![Krājumu kopsavilkums](media/inventory-visibility-onhand-list.png "Krājumu kopsavilkums")
