---
title: Inventory Visibility krājumu sadalījums
description: Šajā rakstā ir paskaidrots, kā iestatīt un izmantot krājumu sadalījuma līdzekli, kas ļauj rezervēt īpašus krājumus, lai nodrošinātu, ka varat izpildīt visrentablākos kanālus vai klientus.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762677"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility krājumu sadalījums

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Uzņēmējdarbības priekšvēsture un mērķis

Organizācijām bieži vien ir iepriekš jāpiešķir rīcībā esošie krājumi saviem svarīgākajiem pārdošanas kanāliem, klientu grupām, reģioniem un reklāmas pasākumiem, lai nodrošinātu, ka iepriekš piešķirtie krājumi ir aizsargāti pret jebkādu citu lietojumu un tos var patērēt tikai ar pārdošanas transakcijām, kas attiecas uz sadalījumu. Krājumu sadalījums krājumu redzamībā ir pārdošanas darbības plānošanas procesa komponents, un tas tiek darīts, pirms notiek faktiskas pārdošanas darbības vai tiek izveidots pārdošanas pasūtījums.

Piemēram, uzņēmums, kura nosaukums ir Contoso, ražo populāru velosipēdu. Diemžēl, tā kā nesenie piegādes ķēdes traucējumi ir ietekmējuši visus šī velosipēda krājumus tranzītā, Contoso rīcībā esošie krājumi ir ierobežoti un ir jāizmanto pēc iespējas labāk. Contoso veic pārdošanu gan tiešsaistē, gan veikalā. Katrā pārdošanas kanālā uzņēmumam ir daži svarīgi korporatīvie partneri (tirdzniecības vietas un lieli mazumtirgotāji), kas pieprasa, lai viņiem tiktu saglabāta noteikta daļa no velosipēda pieejamajiem krājumiem. Tāpēc velosipēdu uzņēmumam ir jāspēj līdzsvarot akciju sadalījumu pa kanāliem, kā arī pārvaldīt savu VIP partneru cerības. Labākais veids, kā sasniegt abus mērķus, ir izmantot krājumu sadalījumu, lai katrs kanāls un mazumtirgotājs varētu saņemt konkrētus piešķirtos daudzumus, kurus vēlāk var pārdot patērētājiem.

Krājumu piešķiršanai ir divi galvenie uzņēmējdarbības mērķi:

- **Krājumu aizsardzība (norobežošana)** — organizācijas vēlas iepriekš piešķirt ierobežotus vai ierobežotus krājumus prioritāriem kanāliem, reģioniem, VIP klientiem un meitasuzņēmumiem. Krājumu redzamības sadalījuma līdzekļa mērķis ir aizsargāt piešķirtos krājumus, lai citi sadalījumi, rezervācijas vai citas pārdošanas prasības neietekmētu iepriekš piešķirtos krājumus.
- **Oversell control** — krājumu redzamības sadalījuma līdzekļa mērķis ir ierobežot iepriekš piešķirtos daudzumus, lai saņēmēja puse (piemēram, kanāls vai debitoru grupa) tos pārmērīgi nepatērētu, kad stājas spēkā faktiskā pārdošanas transakcija, kuras pamatā ir nevainojamā rezervācija.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Sadalījuma definīcija krājumu redzamības pakalpojumā

### <a name="allocation-virtual-pool"></a>Piešķiršanas virtuālais baseins

Lai gan krājumu redzamības līdzekļa sadalījuma līdzeklis neatdala fiziskos krājumu daudzumus, tas atsaucas uz pieejamo fizisko krājumu daudzumu, lai definētu tā sākotnējo pieejamo daudzumu *virtuālā pūla daudzuma piešķiršanai*. Krājumu sadalījums krājumu redzamībā ir mīksts sadalījums. Tas tiek darīts pirms faktisko pārdošanas transakciju rašanās un nav atkarīgs no pārdošanas pasūtījumiem. Piemēram, varat piešķirt krājumus saviem svarīgākajiem pārdošanas kanāliem vai lieliem korporatīvajiem mazumtirgotājiem, pirms gala klienti apmeklē pārdošanas kanālu vai mazumtirdzniecības veikalu, lai tos iegādātos.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Starpība starp krājumu sadali un nesaistošo rezervēšanu

[Mīkstās rezervācijas](inventory-visibility-reservations.md) parasti ir saistītas ar faktiskajām pārdošanas transakcijām (pārdošanas pasūtījuma rindām). Gan piešķiršanu, gan nesaistošo rezervāciju var izmantot neatkarīgi, bet, ja vēlaties tos izmantot kopā, pēc piešķiršanas ir jāveic mīkstā rezervācija. Mēs iesakām vispirms veikt krājumu sadali un pēc tam veikt nelielu rezervi attiecībā pret piešķirtajiem daudzumiem, lai sasniegtu gandrīz reāllaika patēriņu pret sadalījumu. Papildinformāciju skatiet sadaļā [Patērēšana kā viegla rezervācija](#consume-to-soft-reserved).

Krājumu sadalījuma līdzeklis ļauj pārdošanas plānotājiem vai galvenajiem kontu vadītājiem pārvaldīt un iepriekš piešķirt svarīgus krājumus dažādām sadalījuma grupām (piemēram, kanāliem, reģioniem un debitoru grupām). Tas arī atbalsta reāllaika patēriņa izsekošanu, pielāgošanu un analīzi attiecībā pret piešķirtajiem daudzumiem, lai nodrošinātu, ka papildināšanu vai pārdali var veikt savlaicīgi. Šī spēja reāllaikā redzēt piešķiršanas, patēriņa un sadalījuma bilanci ir īpaši svarīga ātrās pārdošanas vai veicināšanas pasākumos.

## <a name="terminology"></a>Terminoloģija

Diskusijās par krājumu sadali noder šādi termini un jēdzieni:

- **Sadalījuma grupa — grupa, kurai pieder sadalījums, piemēram, pārdošanas kanāls, debitoru grupa** vai pasūtījuma tips.
- **Sadalījuma grupas vērtība — katras sadalījuma grupas vērtība**. Piemēram, tīmeklis vai veikals *var būt pārdošanas kanāla sadalījuma grupas vērtība,* savukārt *VIP* vai *parasts* *var būt debitoru sadalījuma grupas* vērtība.
- **Sadalījuma hierarhija** — līdzeklis sadalījuma grupu apvienošanai hierarhiskā veidā. Piemēram, varat definēt *kanālu* kā hierarhijas 1. līmeni, *reģionu* kā 2. līmeni un *klientu grupu* kā 3. līmeni. Krājumu sadalījuma laikā, norādot sadalījuma grupas vērtību, ir jāievēro sadalījuma hierarhijas secība. Piemēram, varat piešķirt 200 sarkanus velosipēdus *tīmekļa* kanālam, *Londonas* reģionam un *VIP* klientu grupai.
- **Pieejams piešķiršanai —** virtuālais kopīgais pūls *, kas norāda daudzumu, kas ir pieejams tālākai piešķiršanai*. Tas ir aprēķināts mērs, kuru varat brīvi definēt, izmantojot savu formulu. Ja izmantojat arī mīkstās rezervēšanas funkciju, ieteicams izmantot to pašu formulu, lai aprēķinātu pieejamo piešķiršanai un rezervēšanai pieejamo.
- **Piešķirts** — fizisks mērs, kas parāda piešķirto kvotu, ko var patērēt sadalījuma grupas. Tas tiek atskaitīts tajā pašā laikā, kad tiek pievienots patērētais daudzums.
- **Patērēts** — fizisks mērījums, kas norāda, ka patērētie daudzumi salīdzinājumā ar sākotnēji piešķirto daudzumu. Tā kā šim fiziskajam pasākumam tiek pievienoti skaitļi, piešķirtais fiziskais pasākums tiek automātiski samazināts.

Nākamajā attēlā ir parādīta biznesa darbplūsma krājumu sadalījumam.

![Krājumu redzamības piešķiršanas biznesa darbplūsma.](media/inventory-visibility-allocation-flow.png "Krājumu redzamības piešķiršanas biznesa darbplūsma.")

Nākamajā attēlā ir parādīta sadalījuma hierarhija un sadalījuma grupas. Virtuālais *kopīgais baseins*, kas šeit ir parādīts, ir pieejamais daudzums, kas jāpiešķir.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title=" Krājumu redzamības sadalījuma hierarhija" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>Krājumu sadalījuma iestatīšana

Krājumu sadales līdzeklis sastāv no šādiem komponentiem:

- Iepriekš definēts, ar sadalījumu saistīts datu avots, fiziskie mēri un aprēķinātie mēri.
- Pielāgojamas sadalījuma grupas, kurām ir ne vairāk kā astoņi līmeņi.
- Iedalījuma lietojumprogrammu saskarņu (API) kopa:

    - sadalīt
    - Pārdalīt
    - nepiešķirt
    - Patērēt
    - Vaicājumu

Sadalījuma līdzekļa konfigurēšanas procesam ir trīs darbības:

- Iespējojiet šo līdzekli programmā Krājumu redzamība, dodoties uz Konfigurācijas **\> līdzekļu pārvaldība un iestatījumu \> piešķiršana**.
- Iestatiet [datu avotu](inventory-visibility-configuration.md#data-source-configuration) un tā [mērus](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Iestatiet sadalījuma grupas nosaukumu un hierarhiju.

### <a name="predefined-data-source"></a>Iepriekš definēts datu avots

Kad iespējojat sadalījuma līdzekli un izsaucat konfigurācijas atjaunināšanas API, krājumu redzamība izveido vienu iepriekš definētu datu avotu un vairākus sākotnējos mērus.

Datu avota nosaukums ir `@iv`. Tas ietver noklusējuma fizisko pasākumu kopu. Tos var skatīt no programmas Krājumu redzamība, dodoties uz **Konfigurācijas \> datu avots**. Jums vajadzētu redzēt **Datasource - @IV**. Izvērsiet datu avotu, `@iv` lai skatītu sākotnējo fizisko mērījumu sarakstu:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Atlasiet cilni Aprēķinātie **mēri**, lai skatītu sākotnēji aprēķināto mēru, kura nosaukums `@iv.@available_to_allocate` ir :

- `@iv`

    - `@iv.@available_to_allocate` = `??`– – `??``@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Citu fizisku mēru pievienošana sadalāmajam aprēķinātajam pasākumam

Lai izmantotu sadalījumu, ir pareizi jāiestata piešķiramā aprēķinātā mēra`@iv.@available_to_allocate` () formula. Piemēram, jums ir `fno` datu avots un mērs, kā arī `onordered` datu avots un mērs, un jūs vēlaties veikt sadalījumu rīcībā esošajā krājumā par summu `pos` un `inbound``fno.onordered``pos.inbound`. Šajā gadījumā `@iv.@available_to_allocate` jāiekļauj `pos.inbound` un `fno.onordered` formulā. Lūk, piemērs:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

> [!NOTE]
> Datu avots ir iepriekš definēts datu avots`@iv`, un fiziskie mēri, kas definēti ar prefiksu`@iv`, ir iepriekš definēti mēri `@`. Šie mēri ir iepriekš definēta sadalījuma līdzekļa konfigurācija, tāpēc nemainiet un nedzēsiet tos, kā arī, izmantojot sadalījuma līdzekli, jūs, visticamāk, saskarsities ar neparedzētām kļūdām.
>
> Iepriekš definētajam aprēķinātajam mēram `@iv.@available_to_allocate` var pievienot jaunus fiziskos mērus, bet nedrīkst mainīt tā nosaukumu.

### <a name="manage-allocation-groups"></a>Sadalījuma grupu pārvaldība

Var iestatīt ne vairāk kā astoņus sadalījuma grupu nosaukumus. Grupām ir hierarhija. Veiciet šīs darbības, lai skatītu un atjauninātu sadalījuma grupas.

1. Piesakieties savā Power Apps vidē un atveriet **Krājumu redzamību**.
1. **Atveriet lapu Konfigurācija** un pēc tam **cilnē Sadalījums** atlasiet **Rediģēt konfigurāciju**. Pēc noklusējuma pastāv sadalījuma hierarhija, kurā ir četri slāņi: `Channel` (augšējais slānis), (otrais slānis), `customerGroup``Region` (trešais slānis) un `OrderType` (ceturtais slānis).
1. Varat noņemt esošu sadalījuma grupu, blakus tai atlasot **X**. Varat arī pievienot hierarhijai jaunas sadalījuma grupas, tieši laukā ievadot katras jaunās grupas nosaukumu.

    > [!IMPORTANT]
    > Esiet piesardzīgs, dzēšot vai mainot sadalījuma hierarhijas kartējumu. Norādījumus skatiet sadaļā [Padomi par piešķīruma](#allocation-tips) izmantošanu.

1. Kad esat konfigurējis sadalījuma grupu un hierarhijas iestatījumus, saglabājiet izmaiņas un pēc tam augšējā labajā stūrī atlasiet **Atjaunināt konfigurāciju**. Konfigurēto sadalījuma grupu vērtības tiks atjauninātas, kad izveidosit sadalījumu, izmantojot lietotāja interfeisu vai API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate). Sīkāka informācija par abām pieejām ir sniegta vēlāk šajā rakstā.

Ja izmantojat četrus grupu nosaukumus un iestatāt tos uz \[`channel`,,,,, `customerGroup``region``orderType`\] šie nosaukumi būs derīgi ar piešķiršanu saistītiem pieprasījumiem, kad izsauksit konfigurācijas atjaunināšanas API.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a> Padomi par sadalījuma izmantošanu

- Katrai precei sadalījuma funkcijai ir jāizmanto tas pats *dimensiju līmenis* atbilstoši preču indeksu hierarhijai, ko iestatāt [preču indeksu hierarhijas konfigurācijā](inventory-visibility-configuration.md#index-configuration). Piemēram, pieņemsim, ka indeksa hierarhija ir \[`Site`,, `Location``Color`,`Size`\]. Ja piešķirat kādu daudzumu vienai precei dimensiju līmenī,,, nākamreiz, kad vēlaties piešķirt šo reizi, jums arī jāpiešķir tajā pašā līmenī\[`Site`,,, `Location`,`Color`\]\[`Site``Location``Color`\]. Ja izmantojat līmeni \[`Site`,,,, vai `Location``Color`,, `Size`\]\[`Site``Location`\] dati būs nekonsekventi.
- **Sadalījuma grupu un hierarhijas modificēšana:** ja sistēmā jau ir sadalījuma dati, dzēšot esošās sadalījuma grupas vai nobīdot sadalījuma grupu hierarhijā, tiks bojāta esošā kartēšana starp sadalījuma grupām. Tāpēc pirms jaunās konfigurācijas atjaunināšanas noteikti manuāli iztīriet visus vecos datus. Tomēr, tā kā jaunu sadalījuma grupu pievienošana zemākajai hierarhijai neietekmē esošos kartējumus, dati nav jātīra.
- Sadale būs veiksmīga tikai tad, ja produktam ir pozitīvs `available_to_allocate` daudzums.
- Lai apakšgrupai piešķirtu produktus no augsta *sadalījuma līmeņa* grupas, izmantojiet `Reallocate` API. Piemēram, jums ir sadalījuma grupu hierarhija \[`channel`,,,, un jūs vēlaties piešķirt kādu produktu no sadalījuma grupas `customerGroup` Tiešsaistē, VIP apakšiedalījuma grupā `region` Tiešsaistē, VIP`orderType`\], \[ES\], izmantojiet \[API, \]`Reallocate` lai pārvietotu daudzumu. Ja izmantojat `Allocate` API, tas piešķirs daudzumu no virtuālā kopējā baseina.
- Lai skatītu vispārējo produktu pieejamību (kopējo pūlu), izmantojiet rīcībā [esošo vaicājumu API, lai pieprasītu](inventory-visibility-api.md#query-on-hand) sadalīšanai *pieejamo krājumu summu*. Pēc tam varat pieņemt lēmumus par sadali, pamatojoties uz šo informāciju.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a> Sadalījuma API izmantošana

Pašlaik ir atvērtas piecas piešķiršanas API:

- **POST / api<wbr> / vides<wbr>/\{videId\}<wbr>/piešķiršana<wbr> / piešķiršana** - Šī API tiek izmantota, lai izveidotu sākotnējo piešķīrumu.
- **POST / api<wbr> / vides<wbr>/\{videId\}<wbr> / piešķiršana<wbr> / unallocate** - Šī API tiek izmantota, lai atgrieztu vai noņemtu piešķirtos daudzumus.
- **POST / api<wbr> / vide<wbr>/\{Id\}<wbr>/piešķiršana<wbr> / pārdale** — šī API tiek izmantota, lai pārvietotu piešķirto daudzumu no esoša piešķīruma uz citām sadalījuma grupām.
- **POST / api<wbr> / vide<wbr>/\{Id\}<wbr>/piešķiršana<wbr> / patēriņš** - Šī API tiek izmantota, lai atskaitītu (izmantotu) piešķirto daudzumu.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** — šī API tiek izmantota, lai pārbaudītu esošos sadalījuma ierakstus attiecībā pret sadalījuma grupām un hierarhiju.

### <a name="allocate"></a>Iedalīt

Zvaniet API, lai piešķirtu produktu, `Allocate` kam ir noteiktas dimensijas. Šeit ir pieprasījuma pamatteksta shēma.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Piemēram, jūs vēlaties piešķirt 10 daudzumu precei Velosipēds, 1 *. vietne*, 11 *. atrašanās vieta*, sarkanā *krāsa*, tiešsaistes *kanāls*, klientu grupa *VIP* un ASV *reģions*.*·* Lai veiktu šo piešķiršanu, varat veikt zvanu, kuram ir šāds pamatteksta saturs.

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Daudzumam vienmēr jābūt lielākam par 0 (nulli).

### <a name="unallocate"></a>Nepiešķirt

Izmantojiet API, `Unallocate` lai mainītu `Allocate` darbību. Negatīvs daudzums operācijā nav atļauts `Allocate`. Ķermenis `Unallocate` ir identisks `Allocate`.

### <a name="reallocate"></a>Pārdalīt

Izmantojiet API, lai pārvietotu `Reallocate` daļu piešķirto daudzumu uz citu grupas kombināciju. Šeit ir pieprasījuma pamatteksta shēma.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Piemēram, varat pārvietot divus velosipēdus, kuru izmēri \[ir site=1, location=11, color=red\], no sadalījuma grupas \[tiešsaistē, VIP, ASV\] uz sadalījuma grupu \[Online, VIP, EU\], zvanot API `Reallocate` un nodrošinot tālāk norādīto pamattekstu.

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>Patērēt

Izmantojiet API, `Consume` lai grāmatotu patēriņa daudzumu pret piešķīrumu. Piemēram, varat izmantot šo API, lai piešķirto daudzumu pārvietotu uz dažiem reāliem mēriem. Šeit ir pieprasījuma pamatteksta shēma.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Piemēram, ir astoņi piešķirtie velosipēdi, kuru izmēri \[ir site=1, location=11, color=red\] sadalījuma grupai \[Online, VIP, US.\] Tiek izmantota šāda sadalāmā formula:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

Astoņi velosipēdi tiek piešķirti no `pos.inbound` pasākuma.

Tagad tiek pārdoti trīs velosipēdi, un tie tiek ņemti no sadales baseina. Lai reģistrētu šo gājienu, varat veikt zvanu, kuram ir šāda pieprasījuma pamatteksts.

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Pēc šī uzaicinājuma piešķirtais daudzums produktam tiks samazināts par 3. Turklāt krājumu redzamība ģenerēs rīcībā esošu izmaiņu notikumu, kur `pos.inbound` = *-3*. Alternatīvi, jūs varat saglabāt `pos.inbound` vērtību tādu, kāda tā ir, un vienkārši patērēt piešķirto daudzumu. Tomēr šajā gadījumā jums ir vai nu jāizveido cits fizisks pasākums, lai saglabātu patērētos daudzumus, vai jāizmanto iepriekš definētais pasākums `@iv.@consumed`.

Šajā pieprasījumā ņemiet vērā, ka fiziskajam mēram, ko izmantojat patēriņa pieprasījuma struktūrā, jāizmanto pretējs modifikatora tips (saskaitīšana vai atņemšana), salīdzinot ar modifikatora tipu, kas izmantots aprēķinātajā mērījumā. Tātad šajā patērētajā ķermenī, ir vērtība `iv.inbound`, `Subtraction` nevis `Addition`.

Datu `fno` avotu nevar izmantot patēriņa struktūrā, jo mēs vienmēr apgalvojām, ka krājumu redzamība nevar mainīt nekādus datu avota datus `fno`. Datu plūsma ir vienvirziena, kas nozīmē, ka visām datu avota daudzuma izmaiņām `fno` ir jānāk no jūsu Supply Chain Management vides.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Patērē kā mīkstu rezervāciju

API `Consume` var arī patērēt piešķirto daudzumu kā mīkstu rezervāciju. Šajā gadījumā `Consume` operācija samazinās piešķirto daudzumu un pēc tam veiks vieglu rezervēšanu šim daudzumam. Lai izmantotu šo pieeju, jums ir jāizmanto [arī krājumu pārskatāmības mīkstās rezervēšanas](inventory-visibility-reservations.md) funkcija.

Piemēram, jūs esat iestatījis neierobežotu rezervācijas fizisko mēru kā `iv.softreserved`. Rezervēm pieejamajam aprēķinātajam mēram izmanto šādu formulu:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– `iv.softreserved`

Lai izmantotu šo iestatījumu ar sadalījuma līdzekli, pievienojiet `@iv.@allocated``iv.available_to_reserve`, lai izveidotu šādu formulu:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– – `iv.softreserved``@iv.@allocated`

Pēc tam atjauniniet `@iv.@available_to_allocate` uz to pašu vērtību.

Ja vēlaties patērēt 3 daudzumu un tieši rezervēt šo daudzumu, varat veikt zvanu, kuram ir šāda pieprasījuma iestāde.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Šajā pieprasījumā paziņojums, kam `iv.softreserved` ir vērtība `Addition`, nevis `Subtraction`.

### <a name="query"></a>Vaicājums

Izmantojiet API, `Query` lai izgūtu ar piešķīrumiem saistītu informāciju par dažiem produktiem. Varat izmantot dimensiju filtrus un sadalījuma grupu filtrus, lai sašaurinātu rezultātus. Dimensijām ir precīzi jāatbilst tai, kuru vēlaties izgūt, piemēram, \[site=1, location=11\] būs nesaistīti rezultāti, salīdzinot ar \[site=1, location=11, color=red \].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Piemēram, izmantojiet \[laukus site=1, location=11, color=red\] un empty groups, lai iegūtu visus sadalījuma ierakstus:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Izmantojiet \[site=1, location=11, color=red\] un groups \[channel=Online, customerGroup=VIP, region=US\], lai iegūtu šīs grupas sadalījuma ierakstus:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Sadalījuma lietotāja interfeisa izmantošana

Varat manuāli pārvaldīt piešķīrumus, izmantojot lietotāja interfeisu, atverot programmu Krājumu redzamība un dodoties uz sadaļu **Darbības redzamības \> piešķiršana**. No turienes jūs varat veikt jebkuru no darbībām, kas aprakstītas nākamajās apakšsadaļās.

### <a name="create-an-allocation"></a>Sadalījuma izveide

Veiciet tālāk norādītās darbības, lai izveidotu piešķīrumu **no programmas Krājumu redzamība lapas Sadalījums**.

1. Atlasiet **Piešķirt**.
1. Iestatiet pamata lauku, dimensiju un mērķa sadalījuma grupu vērtības. (Atlasot apkopošanas datu avotu **Sadaļa Izmēri**, vispirms izmantojiet nolaižamo sarakstu, lai norādītu izmērus (piemēram, `siteId`). Pēc tam parādītajos laukos ievadiet dimensiju vērtības.)
1. Atlasiet **Iesniegt**.

### <a name="consume-an-allocation"></a>Lietojiet piešķīrumu

Atlasiet **Patērēt**, lai patērētu piešķīrumu. Lai nodrošinātu, ka patērējat pareizajā sadalījuma grupā un hierarhijā, ievadiet tās pašas organizācijas un dimensiju datu kopas, kuras ievadījāt, veidojot sadalījumu.

### <a name="reallocate-an-allocation"></a>Piešķīruma pārdale

Atlasiet **Atkārtoti piešķirt**, lai esošo piešķirto daudzumu pārvietotu no vienas sadalījuma grupu kopas uz citu.

### <a name="query-existing-allocations"></a>Vaicājums esošajiem sadalījumiem

Atlasiet **Vaicājums** un pēc tam ievadiet preču, organizāciju, dimensiju un sadalījuma grupu vērtības, lai iegūtu vaicājuma rezultātus par esošajiem sadalījumiem.
