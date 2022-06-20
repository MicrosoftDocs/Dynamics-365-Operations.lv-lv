---
title: Inventory Visibility krājumu sadalījums
description: Šajā rakstā skaidrots, kā iestatīt un izmantot krājumu sadalījuma funkciju, kas ļauj jums rezervēt atvēlēto krājumu, lai nodrošinātu, ka varat izpildīt jūsu ienesīgākos kanālus un debitorus.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ccc3a8c4b3d0649397b1d1f9139f7feebf39b02f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852510"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility krājumu sadalījums

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Biznesa fons un mērķis

Daudzos gadījumos ražotājiem, mazumtirgotājiem un citiem piegādes ķēdes biznesa turētājiem ir iepriekš jāpiešķir krājumi svarīgiem pārdošanas kanāliem, vietām vai debitoriem vai noteiktiem pārdošanas notikumiem. Krājumu sadalījums ir tipiskā pārdošanas darbību plānošanas procesa prakse un tiek veikta pirms notiek faktiskās pārdošanas darbības un pārdošanas pasūtījums tiek izveidots.

Piemēram, velosipēda uzņēmumam ir ierobežots krājums ļoti populāram velosipēdam. Šis uzņēmums dara gan pārdošanu tiešsaistē, gan veikalā. Katrā pārdošanas kanālā uzņēmumam ir daži svarīgi korporatīvais partneri (tirgus un lielie mazumtirgotāji), kas pieprasa, lai tiktu saglabāta noteikta uzņēmuma pieejamo krājumu daļa. Tāpēc velosipēda uzņēmumam jāvar līdzsvarot krājumu sadali pa kanāliem, kā arī pārvaldīt tā VIP partneru izredzes. Labākais veids, kā sasniegt abus mērķus, ir izmantot krājumu sadalījumu, lai katrs kanāls un mazumtirgotājs varētu saņemt noteiktus piešķirtos daudzumus, ko vēlāk var pārdot patērētājiem.

Krājumu sadalījumam ir divi pamata biznesa nolūki:

- **Krājumu aizsardzība (ringfencing)** – organizācijas vēlas veikt ierobežotu vai ierobežotu krājumu iepriekšēju sadali, lai noteiktu prioritātes kanālus, reģionus, VIP klientus un filiāles. Krājumu redzamības sadalījuma funkcija palīdz aizsargāt piešķirtos krājumus, tādējādi citi sadalīumi, rezervācijas vai citas pārdošanas prasības neietekmēs iepriekš piešķirtos krājumus.
- **Cenas pārsaukšanas** kontrole — krājumu redzamības sadalījuma funkcija ierobežo iepriekš piešķirto daudzumu, lai saņēmēja puse (piemēram, kanāls vai debitoru grupa) tos pārpildīs, ja stājas spēkā faktiskā pārdošanas darbība, kas ir balstīta uz vieglās rezervēšanas darbību.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Sadalījuma definīcija krājumu redzamības pakalpojumā

Lai arī sadalījuma funkcija krājumu redzamības pakalpojumā neatcēlo fizisko krājumu daudzumu, tā atsaucas uz pieejamo fizisko krājumu daudzumu, *lai* definētu tā sākotnējo pieejamo virtuālās kopas daudzumu. Krājumu sadalījums krājumu redzamība ir mīksts sadalījums. Tas tiek veikts pirms faktiskās pārdošanas darbību realizācijas un nav atkarīgs no pārdošanas pasūtījumiem. Piemēram, varat piešķirt krājumus saviem vissvarīgākajiem pārdošanas kanāliem vai lieliem korporatīvajiem mazumtirgotājiem, pirms jebkurš gala debitors apmeklē pārdošanas kanālu vai mazumtirdzniecības veikalu tā pirkšanai.

Krājumu sadalījuma un krājuma vieglās rezervēšanas [starpība ir tā](inventory-visibility-reservations.md), ka vieglā rezervēšana parasti ir saistīta ar faktiskajām pārdošanas darbībām (pārdošanas pasūtījuma rindas). Tāpēc, ja vēlaties kopā izmantot sadalījuma un vieglās rezervēšanas funkcijas, ieteicams vispirms veikt krājumu sadalījumu un pēc tam viegli rezervēt piešķirtos daudzumus. Papildinformāciju skatiet sadaļā " [Patērēt kā vieglās rezervēšanas"](#consume-to-soft-reserved).

Krājumu sadalījuma funkcija ļauj pārdošanas plānotājiem vai galveno kontu vadītājiem pārvaldīt un iepriekš piešķirt svarīgu krājumu sadalījuma grupās (piemēram, kanālus, reģionus un debitoru grupas). Tas atbalsta arī reāllaika izsekošanu, korekciju un patēriņa analīzi attiecībā pret sadalītajiem daudzumiem, tādējādi papildināšanu un atkārtotas rezervēšanas var veikt laicību. Šī spēja ir reāllaika redzamība sadalījumā, patēriņā un sadalījuma bilancē ir īpaši svarīga ātras pārdošanas vai veicināšanas notikumu laikā.

## <a name="terminology"></a>Terminoloģija

Šie termini un koncepcijas ir noderīgi inventarizācijas sadalījuma diskusijas:

- **Sadalījuma grupa** – grupa, kam pieder sadalījums, piemēram, pārdošanas kanāls, debitoru grupa vai pasūtījuma tips.
- **Sadalījuma grupas** vērtība – katras sadalījuma grupas vērtība. Piemēram, tīmeklis *vai* *veikals* varētu būt pārdošanas kanāla sadalījuma grupas vērtība, bet *VIP* *vai parasts* varētu būt debitoru sadalījuma grupas vērtība.
- **Sadalījuma hierarhija** – veids, kā hierarhijas veidā kombinēt sadalījuma grupas. Piemēram, kanālu var definēt kā *1*. hierarhijas līmeni, *reģionu kā* 2. līmeni *un debitoru grupu kā* 3. līmeni. Krājumu sadalījuma laikā, norādot sadalījuma grupas vērtību, jums ir jāievēro sadalījuma hierarhijas secība. Piemēram, varat piešķirt 200 sarkanās *krāsas Web kanālam,* Londona *reģionam* un *VIP* klientu grupai.
- **Pieejama sadalīšanai** – virtuālā *kopējā kopa,* kas norāda daudzumu, kas ir pieejams tālākai piešķiršanai. Aprēķinātais līdzeklis var brīvi definēt, izmantojot savu formulu. Ja izmantojat arī vieglās rezervēšanas līdzekli, ieteicams izmantot to pašu formulu, lai aprēķinātu pieejamos un pieejamos rezervēšanai.
- **Piešķirts** – fizisks mērs, kas parāda iedalīto piešķiršanai, ko var patērēt sadalījuma grupas.
- **Patērēts** - fizisks mērs, kas norāda, ka daudzums, kas ir patērēts attiecībā pret oriģinālo iedalīto daudzumu. Kad šim fiziskajam mērvienībam tiek pievienoti cipari, sadalītais fiziskais līdzeklis tiek automātiski samazināts.

Šajā ilustrācijā parādīta biznesa darbplūsma krājumu sadalījumam.

![Krājumu redzamības sadalījuma biznesa darbplūsma.](media/inventory-visibility-allocation-flow.png "Krājumu redzamības sadalījuma biznesa darbplūsma.")

## <a name="set-up-inventory-allocation"></a>Iestatīt krājumu sadalījumu

Krājumu sadalījuma funkcija sastāv no šādiem komponentiem:

- Iepriekš definēts, ar sadalījumu saistīts datu avots, fiziskie pasākumi un aprēķinātie pasākumi.
- Pielāgojamas sadalījuma grupas, kurās ir maksimālais astoņu līmeņu skaits.
- Sadalījuma programmas programmēšanas interfeisu (API) kopa:

    - sadalīt
    - Pārcelt no vairāk
    - Atcelt nesadalīto daudzumu
    - Patērēt
    - Vaicājumu

Sadalījuma funkcijas konfigurēšanas procesam ir divi soļi:

- Iestatiet datu avotu [un](inventory-visibility-configuration.md#data-source-configuration) tā [pasākumus](inventory-visibility-configuration.md#data-source-configuration-physical-measures).
- Iestatiet sadalījuma grupas nosaukumu un hierarhiju.

### <a name="predefined-data-source"></a>Iepriekš definēts datu avots

Iespējojot sadalījuma funkciju un izsaucot konfigurācijas atjaunināšanas API, krājumu redzamība izveido vienu iepriekš definētu datu avotu un vairākus sākotnējos pasākumus.

Datu avotam ir nosaukums `@iv`.

Šie ir sākotnējie fiziskie pasākumi:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Šie ir sākotnējie aprēķinātie pasākumi:

- `@iv`

    - `@iv.@available_to_allocate` = `??`– – <a1/ `??` &amp `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Pievienot citus fiziskos mērus pieejamajam aprēķinātā mēram

Lai izmantotu sadalījumu, jāiestata pieejamais aprēķinātais līdzeklis (`@iv.@available_to_allocate`). Piemēram, jums ir `fno` datu avots un mērs, `onordered``pos` datu avots un mērs, `inbound``fno.onordered` un jūs vēlaties rīcībā veikt sadalījumu uz rīcībā esošo summu `pos.inbound` un. Šajā gadījumā tam `@iv.@available_to_allocate` ir jāietver `pos.inbound` formulā `fno.onordered` un šajā formulā. Šeit parādīts piemērs:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

### <a name="change-the-allocation-group-name"></a>Mainīt sadalījuma grupas nosaukumu

Var iestatīt maksimāli astoņus sadalījuma grupu nosaukumus. Grupām ir hierarhija.

Grupas nosaukumi tiek iestatīti lapā **Krājumu redzamības Power App** konfigurācija. Lai atvērtu šo lapu jūsu vidē Microsoft Dataverse, atveriet programmu Krājumu redzamība un atlasiet Konfigurācijas **\> sadalījums**.

Piemēram, ja izmantosiet četrus grupu nosaukumus un iestatāt tos \[`channel``customerGroup` uz, `region`, `orderType`\] šie nosaukumi būs derīgi ar sadalījumu saistītiem pieprasījumiem, kad izsaucat konfigurācijas atjauninājuma API.

### <a name="allocation-using-tips"></a>Sadalījums, izmantojot padomus

- Katrai precei sadalījuma funkcijai ir *jāizmanto* tas pats dimensijas līmenis atbilstoši preču indeksa hierarhijai, ko [iestatījāt preču indeksa hierarhijas konfigurācijā](inventory-visibility-configuration.md#index-configuration). Piemēram, pieņemsim, ka indeksa hierarhija ir \[`Site``Location`, `Color`,`Size`\]. Ja dimensijas līmenī piešķirsiet \[`Site``Location` noteiktu daudzumu vienai precei, `Color`\] nākamais reizi, kad vēlaties piešķirt šo preci, \[`Site` vajadzētu piešķirt arī vienādu līmeni, `Location`. `Color`\] Lietojot līmeni \[`Site`, vai `Location` arī `Color`, `Size`\]\[`Site` dati `Location`\] būs neatbilstīgi.
- Ja tiek mainīti sadales grupas nosaukums, pakalpojumā saglabātie dati netiks ietekmēti.
- Sadalījumam ir jānotiek pēc tam, kad produktam ir pozitīvs rīcībā esošo daudzumu.
- Lai iedalītu preces no augsta *sadalījuma līmeņa* grupas apakšgrupai, izmantojiet `Reallocate` API. Piemēram, \[`channel` jums ir sadalījuma grupu hierarhija, `customerGroup``region``orderType`\]\[un jūs vēlaties piešķirt preci no sadalījuma grupas tiešsaistē, VIP \]\[apakšsadalīšanas grupai Online, VIP, EU\], izmantojiet API, `Reallocate` lai pārvietotu daudzumu. Ja izmantojat `Allocate` API, tas piešķirs daudzumu no virtuālās parastās kopas.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a> Sadalījuma API izmantošana

Pašlaik ir atvērti pieci sadalījuma API:

- GRĀMATOT/api/vidi/sadalījumu{environmentId}/sadalīt
- GRĀMATOT/api/vidi/{environmentId} sadalījumu/nesadalīt
- GRĀMATOT/api/vidi/{environmentId} sadalījumu/no vietas piešķirt
- Grāmatot/api/vidi/sadalījumu{environmentId}/patērēt
- GRĀMATOT/api/vidi/sadalījumu{environmentId}/vaicājumu

#### <a name="allocate"></a>Iedalīt

Sazinieties ar `Allocate` API, lai piešķirtu preci ar specifiskām dimensijām. Šeit ir pieprasījuma pamatteksta shēma.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
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

Piemēram, jūs vēlaties piešķirt daudzumu 10 produktam Vip, vietai 1 *,* *atrašanās vietai 11,* *krāsai sarkani*, *kanālam Online*, klientu *grupai VIP* un reģionam *ASV*.*·* Lai veiktu šo sadalījumu, varat veikt zvanu, kam ir šāds pamatteksta saturs.

```json
{
    "id": "???",
    "productId": "Bike",
    "targetGroups": {
        "channel": "Online",
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

#### <a name="unallocate"></a>Atcelt nesadalīto

`Unallocate` Izmantojiet API, lai atsauktu operāciju `Allocate`. Operācijā nav atļauts negatīvs `Allocate` daudzums. Pamatteksts `Unallocate` ir identisks pamattekstam `Allocate`.

#### <a name="reallocate"></a>Pārvietot no vairāk

`Reallocate` Izmantojiet API, lai pārvietotu daļu sadalītā daudzuma uz citu grupas kombināciju. Šeit ir pieprasījuma pamatteksta shēma.

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
    "targetGroups": {
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

Piemēram, varat pārvietot divas palešu vietas=1, atrašanās vieta=11, krāsa=\[\] sarkana no sadalījuma grupas Tiešsaistē, VIP, ASV\[\] uz sadalījumu grupu Tiešsaistē, VIP, EU\[\], izsaukot `Reallocate` API un norādot sekojošo pamattekstu.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "targetGroups": {
        "channel": "Online",
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

#### <a name="consume"></a>Patērēt

`Consume` Izmantojiet API, lai grāmatotu patēriņa daudzumu attiecībā pret sadalījumu. Piemēram, varat izmantot šo API, lai pārvietotu sadalīto daudzumu uz dažiem reāliem daudzumiem. Šeit ir pieprasījuma pamatteksta shēma.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
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

Piemēram, ir astoņi sadalīti pakalpojumi, kuriem ir dimensiju vietne =1, atrašanās \[vieta=11, krāsa=\] sarkana sadalījuma grupai \[Tiešsaistē, VIP, ASV \]. Tiek lietota šāda pieejamā formula:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound`– `@iv.@allocated`

No mērvienības ir piešķirti astoņi `pos.inbound` rakstzīmes.

Tagad tiek pārdoti trīs velosipēdi, un tie tiek ņemti no sadalījuma kopas. Lai reģistrētu šo kustību, varat veikt izsaukumu, kam ir šāds pieprasījuma pamatteksts.

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
    "targetGroups": {
        "channel": "Online",
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

Pēc šī zvana precei piešķirtais daudzums tiks samazināts par 3. Turklāt krājumu redzamība ģenerēs rīcībā esošo izmaiņu notikumu, kur `pos.inbound` = *-3*. Alternatīvi vērtību var saglabāt tā `pos.inbound`, kā tā ir, un tikai patērēt iedalīto daudzumu. Tomēr šajā gadījumā jāizveido cits fizisks mērs, lai saglabātu patērētos daudzumus vai izmantotu iepriekš definēto mērījumu `@iv.@consumed`.

Šajā pieprasījumā ievērojiet, ka fiziskajam mērvienībai, ko izmantojat patērētā pieprasījuma pamattekstā, ir jāizmanto pretējs modifikatora tips (papildinājums vai atņemšanas), salīdzinot ar aprēķinātajā mērvienībā izmantoto modifikatora tipu. Tātad šajā patērētā pamattekstā `iv.inbound` ir vērtība `Subtraction` nevis `Addition`.

Datu `fno` avotu nevar izmantot patērētājam pamattekstā, jo mēs vienmēr pieprasām, ka krājumu redzamība datu avotam nevar mainīt `fno` nekādus datus. Datu plūsma ir vienvirziena, kas nozīmē, ka `fno` visām daudzuma izmaiņām datu avotam ir jābūt no jūsu Piegādes ķēžu pārvaldības vides.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a> Patērēt kā vieglās rezervācijas

API `Consume` var arī patērēt piešķirto daudzumu kā vieglās rezervēšanas krājumus. Šajā gadījumā operācija samazinās `Consume` piešķirto daudzumu un pēc tam šim daudzumam veiks vieglās rezervēšanas darbības. Lai izmantotu šo pieeju, jāizmanto arī krājumu [redzamības vieglās](inventory-visibility-reservations.md) rezervēšanas funkcija.

Piemēram, jūs esat iestatījis vieglās rezervēšanas modifikatoru (mērvienību).`iv.softreserved` Aprēķinātā mērvienībai, kas pieejama rezervēm, tiek izmantota šāda formula:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– `iv.softreserved`

Lai izmantotu šo iestatījumu ar sadalījuma līdzekli, pievienojiet `@iv.@allocated` šādas `iv.available_to_reserve` formulas ražošanai:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound`– – <a1/ `iv.softreserved` &amp `@iv.@allocated`

Pēc tam atjauniniet `@iv.@available_to_allocate` uz to pašu vērtību.

Kad vēlaties patērēt daudzumu 3 un tieši rezervēt šo daudzumu, varat veikt zvanu, kam ir šāds pieprasījuma pamatteksts.

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
    "targetGroups": {
        "channel": "Online",
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

Šajā pieprasījumā ievērojiet, `iv.softreserved` ka vērtība `Addition` nav.`Subtraction`

#### <a name="query"></a>Vaicājums

`Query` Izmantojiet API, lai izgūtu ar sadalījumu saistītu informāciju par dažām precēm. Varat izmantot dimensiju filtrus un sadalījuma grupu filtrus, lai sašaurinātu rezultātus. Dimensijām jāatbilst precīzi tam, ko vēlaties izgūt, piemēram, \[atrašanās vieta=1, atrašanās vieta=11\]\[būs ar vietu=1, novietojums=11, krāsa=\] sarkana.

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

Piemēram, izmantojiet lauku site \[=1, location=11, color=red\] un empty groups field, lai iegūtu visus sadalījuma ierakstus:

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
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Lai \[iegūtu šīs grupas sadalījuma ierakstus, izmantojiet vietni=1, novietojumu=11, krāsa=\]\[sarkanā un grupu kanāls=Tiešsaistē, customerGroup=VIP, reģions=\] ASV:

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
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
