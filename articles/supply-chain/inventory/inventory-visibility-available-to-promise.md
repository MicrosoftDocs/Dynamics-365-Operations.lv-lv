---
title: Krājumu redzamības rīcībā esošo izmaiņu grafiki un pieejamās solīšanai
description: Šajā tēmā ir aprakstīts, kā plānot turpmākās rīcībā veiktās izmaiņas un aprēķināt rīcībā esošos (ATP) daudzumus.
author: yufeihuang
ms.date: 03/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7ce868871f093fd734a466bb8a06c5782bf83302
ms.sourcegitcommit: a3b121a8c8daa601021fee275d41a95325d12e7a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2022
ms.locfileid: "8526334"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Krājumu redzamības rīcībā esošo izmaiņu grafiki un pieejamās solīšanai

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, *kā* iestatīt rīcībā esošo krājumu izmaiņu grafika funkciju, lai plānotu turpmākās rīcībā esošo izmaiņu izmaiņas un aprēķinātu rīcībā esošos (ATP) daudzumus. ATP ir pieejamais krājuma daudzums, un nākamajā periodā to var solīt debitoram. Šī aprēķina izmantošana var lielā palielinās pasūtījuma izpildes iespēju.

Daudzām ražošanām, mazumtirdzniecības vai pārdevējiem nepietiek tikai, lai zinātu, kas pašlaik ir pieejams. Tām ir jābūt pilnai redzamībai nākotnē. Šai nākotnes pieejamībai jāapsver nākotnes piedāvājums, turpmāks pieprasījums un ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a> Iespējot un iestatīt līdzekļus

Lai aprēķinātu ATP daudzumus, pirms ATP izmantošanas jāiestata viens vai vairāki aprēķinātie pasākumi. Jums jāieslēdz arī funkcija un jākonfigurē ATP iestatījumi sadaļā Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Iestatīt aprēķinātos apjomus ATP daudzumiem

ATP *aprēķinātais līdzeklis* ir iepriekš definēts aprēķinātais līdzeklis, kas parasti tiek izmantots, lai atrastu rīcībā esošo daudzumu, kas pašlaik ir pieejams. Tā pievienošanas modifikatora daudzumu summa ir piegādes daudzums, un tā atņemšanas modifikatora daudzumu summa ir pieprasījuma daudzums.

Varat pievienot vairākus aprēķinātus apjomus, lai aprēķinātu ATP daudzumus. Tomēr visu ATP aprēķināto pasākumu kopējais modifikatoru skaits nedrīkst būt mazāks par deviņiem.

Piemēram, jūs iestatāt šādu aprēķināto mērījumu:

**Pieejams rīcībā =** (PhysicalInventOnHandUnrestrictedQualityInspectionInbound *·* + *·* + *·* + *·* + *) — (* ReservPhysicalSoftReservePhysicalOutbound) *·* + *·* + *·*

Summa (PhysicalInventOnHandUnrestrictedQualityInspectionInbound *·* + *·* + *·* + *·* + *) norāda piedāvājumu, un summa (* *ReservPhysicalSoftReservePhysicalOutbound* + *·* + *·*) attēlo pieprasījumu. Tādējādi aprēķinātais līdzeklis var būt izprotams šādā veidā:

**Rīcībā esošie krājumiSupply** = *·* – *Pieprasījums*

Papildinformāciju par aprēķinātajiem pasākumiem skatiet sadaļā [Aprēķinātie pasākumi](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Ieslēgt rīcībā esošo izmaiņu grafika līdzekli un konfigurēt ATP iestatījumus

Izpildiet šos soļus, lai *ieslēgtu rīcībā esošo izmaiņu* grafika līdzekli Power Apps un konfigurētu ATP iestatījumus.

1. Pieteikties un Power Apps atvērt krājumu redzamību;
1. Atveriet lapu **Konfigurācija**.
1. **Cilnē Līdzekļu pārvaldība** ieslēgiet līdzekli *OnhandChangeSchedule*.
1. Atlasiet cilni **ATP** iestatījumi.
1. Vaicājot krājumu redzamību, tas dos rezultātu, kas ietvers katru atp aprēķināto mērījumu, ko šeit pievienojat. Atlasiet **Pievienot**, lai pievienotu jaunu aprēķināto mērījumu ATP.
1. Iestatiet tālāk norādītos laukus.

    - **Datu avots** - izvēlieties datu avotu, kas ir saistīts ar aprēķināto mērījumu.
    - **Aprēķinātais** līdzeklis - atlasiet aprēķināto mērījumu, kas ir saistīts ar atlasīto datu avotu un kuru vēlaties izmantot, lai atrastu pašlaik pieejamo rīcībā esošo daudzumu.
    - **Grafika periods** - ievadiet dienu skaitu, ko lietotāji var skatīt un iesniegt plānotās rīcībā veiktās izmaiņas, kad tiek izmantots atlasītais aprēķinātais līdzeklis. Lietotāji, kuri vaicās par krājumu informāciju, saņems rīcībā esošo daudzumu, plānotās rīcībā esošās izmaiņas un ATP katrai dienai šajā periodā, sākot ar pašreizējo datumu. Atlasiet veselu skaitli no 1 līdz 7.

    > [!IMPORTANT]
    > Grafika periodā ir iekļauts pašreizējais datums. Tāpēc lietotāji var plānot rīcībā esošās izmaiņas, lai tās notiktu jebkurā laikā no pašreizējā datuma (dienas, kad izmaiņas tiek iesniegtas) līdz (grafika periods – 1) dienas nākotnē.

1. Atlasiet **Saglabāt**.
1. Atkārtojiet no 5. līdz 7. solim, līdz pievienoti visi aprēķinātie pasākumi, kas nepieciešami ATP.
1. Kad visu nepieciešamo iestatījumu konfigurēšana pabeigta, atlasiet Atjaunināt **konfigurāciju**.

Papildinformāciju skatiet sadaļā [Pabeigt un atjaunināt konfigurāciju](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Kā darbojas rīcībā esošo izmaiņu grafiks un ATP aprēķini

Rīcībā *esošo izmaiņu grafiks izveido* paredzamos datumus un plānoto rīcībā esošo izmaiņu daudzumu. Rīcībā esošo izmaiņu grafiku var iesniegt krājumu redzamībai, ja vien datumi ir perioda ietvaros, **kas** tiek definēts ar iestatījuma Plānot periodu iestatījumiem ([skatiet sadaļu Iespējot un iestatīt](#setup) funkcijas). Lietotāji, kuri vaicā par krājumu informāciju, saņems rīcībā esošo daudzumu, ieplānotās rīcībā esošo izmaiņu izmaiņas un ATP katrai dienai šajā periodā.

Ieplānotās izmaiņas sākotnēji netiek veiktas, un tādēļ tās neietekmē jūsu faktiskos rīcībā esošos daudzumus sistēmā. Lai veiktu izmaiņas, jāiesniedz rīcībā esošo *izmaiņu notikums*, kas atjaunina faktisko pieejamo rīcībā esošo daudzumu. Pēc tam plānotā izmaiņa jāatvēr, iesniedzot rīcībā esošo izmaiņu grafiku atbilstošam negatīvam daudzumam.

Piemēram, jūs veiktu pasūtījumu par 10 pirkšanas pasūtījumiem un paredzat, ka tas tiks piegādāts rīt. Tāpēc jūs iesniedziet rīcībā esošo izmaiņu grafiku, kura ienākošais daudzums ir 10 un kurš ir datēts ar rītdienu. Kad pasūtījums tiek saņemts nākamajā dienā, pievienojiet krājumus fiziskajiem rīcībā ajiem krājumiem. Pēc tam jums jāveic izmaiņas savā sistēmā, lai atjauninātu faktisko rīcībā esošo daudzumu. Lai iesniegtu izmaiņas, iesniedziet rīcībā esošo izmaiņu notikumu, kura ienākošais daudzums ir 10. Pēc tam atgriežat plānotās izmaiņas, iesniedzot rīcībā esošo izmaiņu grafiku, kura ienākošais daudzums ir -10.

Vaicājumot par rīcībā esošo krājumu un ATP daudzumu krājumu redzamību, tā atgriež šādu informāciju par katru dienu grafika periodā:

- **Datums** – datums, uz kuru attiecas rezultāts.
- **Rīcībā esošo krājumu** daudzums – faktiskais rīcībā esošo krājumu daudzums norādītajā datumā. Šis aprēķins tiek veikts saskaņā ar ATP aprēķināto mērījumu, kas ir konfigurēts krājumu redzamībai.
- **Plānotā piegāde** - visu plānoto ienākošo daudzumu summa, kas nav kļuvis fiziski pieejama tiešajam patēriņam vai kravai no norādītā datuma.
- **Plānotais** pieprasījums - visu plānoto izejošo daudzumu summa, kas nav patērēti vai nosūtīti no norādītā datuma.
- **ATP daudzums** – minimālais plānotais rīcībā esošo krājumu daudzums, kas ir pieejams no norādītā datuma līdz plānošanas perioda beigām. Šis daudzums ietver visas plānotā daudzuma korekcijas. Tas ir maksimālais daudzums, ko var solīt pašreizējā piegādes vai patēriņa datumā šajā dienā.

Piemēram, ja pašreizējais datums ir 2022. gada 1. februāris un grafika periods ir 7, lietotāji var iesniegt plānotās rīcībā esošo izmaiņu, kas paredzamas no 2022. gada 1. februāra līdz 7. februārim. Šajā gadījumā, piemēram, ATP daudzums 3. februārī tiek aprēķināts, pamatojoties uz rīcībā esošo daudzumu šai dienai un plānoto daudzumu no 3. februāra līdz 7. februārim.

## <a name="example"></a>Paraugs

Šajā piemērā parādīts, kā ieplānotā daudzuma sērijas mainās, ietekmē rīcībā esošos un ATP daudzumus, kas ir krājumu redzamības pārskatos. Tajā ir arī parādīts, kā veikt plānotas izmaiņas, kā fiksētās grafika izmaiņas ietekmē rezultātus, un kas var notikt, ja netiek izdarītas ieplānotas izmaiņas.

Šajā piemērā rezultāti rāda prognozēto *rīcībā esošo* vērtību. Šī vērtība ietver visus plānotos atjauninājumus ilustrācijas nolūkiem, bet netiek faktiski iekļauts pārskatā, kad vaicāsiet par krājumu redzamību.

1. AtP **iestatījumu lapā sistēmai tiek konfigurēti** šādi iestatījumi Power Apps:

    - **ATP aprēķinātais** līdzeklis - Jums ir aprēķināts līdzeklis, ko sauc par *Rīcībā esošo*. Tas tiek aprēķināts, kā rīcībā *esošie = piedāvājums – pieprasījums*. Šo mērījumu varat atlasīt šeit.
    - **Grafika periods** – atlasiet *7*.

1. Ir spēkā arī šādi nosacījumi:

    - Pašreizējais datums ir 2022. gada 1. februāris.
    - Pašlaik rīcībā esošo krājumu daudzums ir 20.

1. Pašreizējam datumam (2022. gada 1. februāris) jūs iesniedziet plānoto pieprasījuma daudzumu 3 krājumu redzamībai. Tādējādi plānotais rīcībā esošo krājumu daudzums ir 17. Šajā tabulā parādīts rezultāts.

    | Datums | Rīcībā esošie krājumi | Plānotā piegāde | Plānotais pieprasījums | Prognozētais rīcībā esošo krājumu | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022/02/01 | 20 | | 3 | 17 | 17 |
    | 2022/02/02 | 20 | | | 17 | 17 |
    | 2022/02/03 | 20 | | | 17 | 17 |
    | 2022/02/04 | 20 | | | 17 | 17 |
    | 2022/02/05 | 20 | | | 17 | 17 |
    | 2022/02/06 | 20 | | | 17 | 17 |
    | 2022/02/07 | 20 | | | 17 | 17 |

1. Pašreizējā datumā (2022. gada 1. februārī) jūs iesniedziet plānoto piegādes daudzumu 10 2022. gada 3. februārī. Šajā tabulā parādīts rezultāts.

    | Datums | Rīcībā esošie krājumi | Plānotā piegāde | Plānotais pieprasījums | Prognozētais rīcībā esošo krājumu | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022/02/01 | 20 | | 3 | 17 | 17 |
    | 2022/02/02 | 20 | | | 17 | 17 |
    | 2022/02/03 | 20 | 10. | | 27 | 27 |
    | 2022/02/04 | 20 | | | 27 | 27 |
    | 2022/02/05 | 20 | | | 27 | 27 |
    | 2022/02/06 | 20 | | | 27 | 27 |
    | 2022/02/07 | 20 | | | 27 | 27 |

1. Pašreizējā datumā (2022. gada 1. februārī) iesniedzat šādas plānotā daudzuma izmaiņas:

    - 2022. gada 4. februārī pieprasītais daudzums 15
    - 2022. gada 5. februārī piegādājamais daudzums 1.
    - 3. pieprasījuma daudzums 2022. gada 6. februārī

    Šajā tabulā parādīts rezultāts.

    | Datums | Rīcībā esošie krājumi | Plānotā piegāde | Plānotais pieprasījums | Prognozētais rīcībā esošo krājumu | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022/02/01 | 20 | | 3 | 17 | 12. |
    | 2022/02/02 | 20 | | | 17 | 12. |
    | 2022/02/03 | 20 | 10. | | 27 | 12. |
    | 2022/02/04 | 20 | | 15 | 12. | 12. |
    | 2022/02/05 | 20 | 1 | | 13 | 13 |
    | 2022/02/06 | 20 | 3 | | 16 | 16 |
    | 2022/02/07 | 20 | | | 16 | 16 |

1. Pašreizējā datumā (2022. gada 1. februārī) jūs nosūtat plānoto pieprasījuma daudzumu 3. Tādēļ šīs izmaiņas jāveic tā, lai tās atspoguļotu faktiskajā rīcībā esošo daudzumu. Lai iesniegtu izmaiņas, iesniedziet rīcībā esošo izmaiņu notikumu, kura izejošais daudzums ir 3. Pēc tam atgriežat plānotās izmaiņas, iesniedzot rīcībā esošo izmaiņu grafiku, kura izejošais daudzums ir -3. Šajā tabulā parādīts rezultāts.

    | Datums | Rīcībā esošie krājumi | Plānotā piegāde | Plānotais pieprasījums | Prognozētais rīcībā esošo krājumu | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022/02/01 | 17 | | 0 | 17 | 12. |
    | 2022/02/02 | 17 | | | 17 | 12. |
    | 2022/02/03 | 17 | 10. | | 27 | 12. |
    | 2022/02/04 | 17 | | 15 | 12. | 12. |
    | 2022/02/05 | 17 | 1 | | 13 | 13 |
    | 2022/02/06 | 17 | 3 | | 16 | 16 |
    | 2022/02/07 | 17 | | | 16 | 16 |

1. Nākamajā dienā (2022. gada 2. februārī) grafika periods mainās uz priekšu par vienu dienu. Šajā tabulā parādīts rezultāts.

    | Datums | Rīcībā esošie krājumi | Plānotā piegāde | Plānotais pieprasījums | Prognozētais rīcībā esošo krājumu | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022/02/02 | 17 | | | 17 | 12. |
    | 2022/02/03 | 17 | 10. | | 27 | 12. |
    | 2022/02/04 | 17 | | 15 | 12. | 12. |
    | 2022/02/05 | 17 | 1 | | 13 | 13 |
    | 2022/02/06 | 17 | 3 | | 16 | 16 |
    | 2022/02/07 | 17 | | | 16 | 16 |
    | 2022/02/08 | 17 | | | 16 | 16 |

1. Tomēr divas dienas vēlāk (2022. gada 4. februāris), piegādes daudzums 10, kas tika plānots 3. februārī, vēl nav saņemts. Šajā tabulā parādīts rezultāts.

    | Datums | Rīcībā esošie krājumi | Plānotā piegāde | Plānotais pieprasījums | Prognozētais rīcībā esošo krājumu | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022/02/04 | 17 | | 15 | 2 | 2 |
    | 2022/02/05 | 17 | 1 | | 3 | 3 |
    | 2022/02/06 | 17 | 3 | | 6 | 6 |
    | 2022/02/07 | 17 | | | 6 | 6 |
    | 2022/02/08 | 17 | | | 6 | 6 |
    | 2022/02/09 | 17 | | | 6 | 6 |
    | 2022/02/10 | 17 | | | 6 | 6 |

    Kā redzams, plānotās (bet nav fiksētās) rīcībā veiktās izmaiņas neietekmē faktisko rīcībā esošo daudzumu.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a> Iesniegt izmaiņu grafikus, izmaiņu notikumus un ATP vaicājumus, izmantojot API

Lietojumprogrammas saskarnes (API) vietrāžus URL var izmantot, lai iesniegtu rīcībā esošo izmaiņu grafikus, mainītu notikumus un vaicājumus.

| Ceļš | Metode | Apraksts |
| --- | --- | --- |
| `/api/environment/{environmentId}/on-hand/changeschedule` | `POST` | Izveidot vienu plānotu rīcībā esošo izmaiņu. |
| `/api/environment/{environmentId}/on-hand/changeschedule/bulk` | `POST` | Izveidot vairākas plānotas rīcībā esošo krājumu izmaiņas. |
| `/api/environment/{environmentId}/onhand` | `POST` | Izveidot vienu rīcībā esošo izmaiņu notikumu. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Izveidot vairākus izmaiņu notikumus. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Vaicājums, izmantojot `POST` metodi. |
| `/api/environment/{environmentId}/onhand` | `GET` | Vaicājums, izmantojot `GET` metodi. |

Plašāku informāciju skatiet krājumu redzamības [publiskajiem API](inventory-visibility-api.md).

### <a name="submit-on-hand-change-schedules"></a>Iesniegt rīcībā esošo izmaiņu grafikus

Rīcībā esošie izmaiņu grafiki tiek veikti, iesniedzot pieprasījumu atbilstošam krājumu redzamības `POST` pakalpojuma URL ([skatiet iesniegt izmaiņu grafikus, izmaiņu notikumus un ATP vaicājumus, izmantojot API](#api-urls) sadaļu). Varat arī iesniegt lielapjoma pieprasījumus.

Lai iesniegtu rīcībā esošo izmaiņu grafiku, pieprasījuma pamattekstam jāsatur organizācijas ID, preces ID, plānotais datums un daudzumi pēc datuma. Plānotajam datumam jābūt starp pašreizējo datumu un pašreizējā grafika perioda beigām.

#### <a name="example-request-body-that-contains-a-single-update"></a>Pieprasījuma pamatteksta piemērs, kas ietver vienu atjauninājumu

Šajā piemērā parādīts pieprasījuma pamatteksts, kas satur vienu atjauninājumu.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/on-hand/changeschedule

# Method
Post

# Header
# Replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "Small"
    },
    "quantitiesByDate":
    {
        "2022/02/01": // today
        {
            "pos":{
                "inbound": 10,
            },
        },
    },
}
```

#### <a name="example-request-body-that-contains-multiple-bulk-updates"></a>Pieprasījuma pamatteksta piemērs, kurā ir vairāki (lielapjoma) atjauninājumi

Šajā piemērā parādīts pieprasījuma pamatteksts, kas satur vairākus (lielapjoma) atjauninājumus.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/on-hand/changeschedule/bulk

# Method
Post

# Header
# replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId": "Small"
        },
        "quantitiesByDate":
        {
            "2022/02/01": // today
            {
                "pos":{
                    "inbound": 10,
                },
            },
        },
    },
    {
        "id": "id-bike-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId": "Small"
        },
        "quantitiesByDate":
        {
            "2022/02/05":
            {
                "pos":{
                    "outbound": 10,
                },
            },
        },
    }
]
```

### <a name="submit-on-hand-change-events"></a>Iesniegt rīcībā esošo izmaiņu notikumus

Rīcībā esošie izmaiņu notikumi tiek `POST` veikti, iesniedzot pieprasījumu atbilstošam krājumu redzamības pakalpojuma URL ([skatiet iesniegt izmaiņu grafikus, izmaiņu notikumus un ATP vaicājumus, izmantojot API](#api-urls) sadaļu). Varat arī iesniegt lielapjoma pieprasījumus.

> [!NOTE]
> Rīcībā esošo izmaiņu notikumi nav unikāli ATP funkcionalitātei, bet ir daļa no standarta krājumu redzamības API. Šis piemērs ir iekļauts, jo notikumi ir svarīgi, kad strādājat ar ATP. Rīcībā esošie izmaiņu notikumi ir līdzīgi rīcībā esošo izmaiņu rezervācijām, bet notikumu ziņojumi jānosūta uz citu API URL, `quantities``quantityByDate` un notikumi ziņojuma pamatteksta vietā tiek lietoti. Papildinformāciju par rīcībā esošiem izmaiņu notikumiem un citām krājumu redzamības API funkcijām skatiet krājumu [redzamības publiskajos API](inventory-visibility-api.md).

Lai iesniegtu rīcībā esošo izmaiņu notikumu, pieprasījuma pamattekstam jāsatur organizācijas ID, preces ID, plānotais datums un daudzumi pēc datuma. Plānotajam datumam jābūt starp pašreizējo datumu un pašreizējā grafika perioda beigām.

Šajā piemērā parādīts pieprasījuma pamatteksts, kas satur vienu rīcībā esošo izmaiņu notikumu.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# Replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red",
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Vaicāt plānotās rīcībā esošo izmaiņu un ATP rezultātus

Varat vaicāt par rīcībā esošo izmaiņu plānotajām izmaiņām un ATP `POST``GET` rezultātiem, iesniedzot pieprasījumu vai pieprasījumu atbilstošam API URL ([skatiet iesniegt izmaiņu grafikus, izmaiņu notikumus un ATP vaicājumus, izmantojot API](#api-urls) sadaļu).

Pieprasījumā iestatiet kā patiesu `QueryATP`*·*, ja vēlaties vaicāt par rīcībā esošo izmaiņu ieplānotajām izmaiņām un ATP rezultātiem.

- Ja pieprasījums tiek iesniedzis, izmantojot metodi `GET`, iestatiet šo parametru vietrādī URL.
- Ja pieprasījums tiek iesniegts, izmantojot metodi `POST`, iestatiet šo parametru pieprasījuma pamattekstā.

> [!NOTE]
> Neatkarīgi no tā `returnNegative`*·* *·*, vai parametrs pieprasījuma pamattekstā ir iestatīts kā patiess vai nepatiess, rezultāts ietvers negatīvas vērtības, kad vaicājums tiks veikts par rīcībā esošo izmaiņu veikšanu un ATP rezultātiem. Šīs negatīvās vērtības tiks iekļautas, jo, ja tiek plānoti tikai pieprasījuma pasūtījumi vai ja piegādes daudzums ir mazāks par pieprasījuma daudzumu, plānotie rīcībā esošo izmaiņu daudzumi būs negatīvi. Ja negatīvas vērtības netika iekļautas, rezultāti būtu saplūdoši. Papildinformāciju par šo opciju un to, kā tā darbojas citiem vaicājumu tipiem, skatiet Krājumu [redzamības publiskais API](inventory-visibility-api.md).

### <a name="post-method-example"></a>GRĀMATOŠANAS metodes piemērs

Tālāk sniegtajā piemērā ir parādīts, kā izveidot pieprasījuma pamattekstu, kuru, izmantojot metodi, var iesniegt krājumu redzamībai`POST`.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/on-hand/indexquery

# Method
Post

# Header
# replace {access_token} with the one from your security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true,
}
```

### <a name="get-method-example"></a>GET metodes piemērs

Šajā piemērā parādīts, kā izveidot pieprasījuma URL kā `GET` pieprasījumu.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Šī pieprasījuma rezultāts `GET` ir tieši tāds pats kā pieprasījuma `POST` rezultāts iepriekšējā piemērā.

### <a name="query-result-example"></a>Vaicājuma rezultāta piemērs

Abi iepriekšējie vaicājuma piemēri var sniegt šādu atbildi. Šajā piemērā sistēma ir konfigurēta ar šādiem iestatījumiem:

- **ATP aprēķinātais līdzeklis:** *iv.onhand = poz.inbound — poz.outbound*
- **Grafika periods:** *7*

Šeit parādīts atbildes pamatteksta piemērs.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
