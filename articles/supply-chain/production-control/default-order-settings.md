---
title: Noklusējuma pasūtījuma iestatījumi dimensijām un preču variantiem
description: Pasūtījuma noklusējuma iestatījumi definē vietu un noliktavu, kur krājumi tiks iegūti vai glabāti, minimālos, maksimālos, vairākkārtējos un standarta daudzumus, kas tiks izmantoti tirdzniecībai vai krājumu pārvaldībai, izpildes laikus, apturēšanas karodziņus un pasūtījumu solīšanas metodes.
author: t-benebo
manager: tfehr
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c3aa800c1a996a062bcb737afa23f00a9e52bb48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433071"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Noklusējuma pasūtījumu iestatījumi dimensijām un preču variantiem

[!include [banner](../includes/banner.md)]

Izmantojot pasūtījuma noklusējuma iestatījumus programmā Dynamics 365 Supply Chain Management, tiek definēta vieta un noliktava krājumu ieguvei vai glabāšanai, minimālais, maksimālais, vairākkārtējais un standarta daudzums, kas tiks izmantots tirdzniecībai vai krājumu pārvaldībai, izpildes laiks, apturēšanas karodziņš un pasūtījuma solīšanas metode. Pasūtījuma noklusējuma iestatījumi tiek izmantoti, veidojot pirkšanas pasūtījumus, pārdošanas pasūtījumus, pārsūtīšanas pasūtījumus, krājumu žurnālus un veicot vispārējo plānošanu plānoto pasūtījumu ģenerēšanai. Pasūtījuma noklusējuma iestatījumi var būt atkarīgi no preces, atkarīgi no vietas, atkarīgi no preces varianta vai atkarīgi no preces dimensijas.

Lai definētu noklusējuma pasūtījuma iestatījumus precei, rīkojieties šādi.

1. DOdieties uz **Preču informācijas pārvaldība** &gt; **Preces** &gt; **Nodotās preces**.
1. Režģī atlasiet atbilstošo preci.
1. Darbības rūtī veiciet vienu no šīm darbībām, lai atvērtu atlasītajai precei **Noklusējuma pasūtījuma iestatījumu** lapu:

    - Cilnē **Plāns** grupā **Pasūtījuma iestatījumi** atlasiet **Noklusējuma pasūtījuma iestatījumi**.
    - Cilnē **Pārvaldīt krājumu** grupā **Pasūtījuma iestatījumi** atlasiet **Noklusējuma pasūtījuma iestatījumi**.

1. Konfigurējiet iestatījumus, kā aprakstīts atlikušajā šīs tēmas sadaļā.

## <a name="default-order-settings"></a>Pasūtījuma noklusējuma iestatījumi

Pastāv trīs veidu pasūtījuma noklusējuma iestatījumi pirkšanai, pārdošanai un krājumiem. Pasūtījuma noklusējuma iestatījumi pirkšanai tiek izmantoti, kad izveidojat tālāk uzskaitītos elementus.

- Pirkšanas pasūtījuma rindas
- Pirkšanas līguma rindas
- Piedāvājuma pieprasījuma rindas
- Pirkšanas pieprasījumu rindas
- Sūtījuma papildināšanas rindas (daļēji atbalstītas, skatiet piezīmi)
- Plānotie pirkšanas pasūtījumi

> [!NOTE]
> Sūtījuma papildināšanas pasūtījuma rindām ir pieejami tikai tie iestatījumi no kopsavilkuma cilnes **Pirkšanas pasūtījums** lapā **Noklusējuma pasūtījuma iestatījumi**, kas ir no lauka **Noklusējuma vieta**, no lauka **Noklusējuma noliktava** un no izvēles rūtiņas **Aptutētie**.

Pasūtījuma noklusējuma iestatījumi pārdošanai tiek izmantoti, kad izveidojat tālāk uzskaitītos elementus.

- Pārdošanas pasūtījuma rindas
- Pārdošanas līguma rindas
- Pārdošanas piedāvājuma rindas
- Atgriešanas pasūtījuma rindas un krājumu aizstāšanas rindas
- Pieprasījuma apjoma prognozes rindas

Pārdošanas pasūtījuma noklusējuma iestatījumi tiek izmantoti arī tad, kad izveidojat tālāk uzskaitītos elementus.

- Projekta krājumu prasības
- Pakalpojumu pasūtījumu krājumu vajadzības

Pasūtījuma noklusējuma iestatījumi krājumiem tiek izmantoti, kad izveidojat tālāk uzskaitītos elementus.

- Krājumu žurnāli
- Pārsūtīšanas pasūtījumi
- Plānotie pārsūtīšanas pasūtījumi

Krājumu pasūtījuma noklusējuma iestatījumi tiek izmantoti arī tad, kad izveidojat tālāk uzskaitītos elementus.

- Karantīnas pasūtījumi
- Kvalitātes pasūtījumi
- Ražošanas pasūtījumi
- MK rindas
- Plānotie ražošanas pasūtījumi

## <a name="full-definition-of-a-released-product"></a>Pilna izlaistās preces definīcija

Transakcijas izveides laikā, rindā ir jānorāda pilnā izlaistās preces definīcija, pirms programmatūrā Supply Chain Management tiek mēģināts noteikt pasūtījuma noklusējuma iestatījumus. Pilnajā izlaistās preces definīcijā transakcijā ir norādīts krājuma kods un visas aktīvās preces dimensijas, piemēram, konfigurācija, izmērs, stils, versija un krāsa. Piemēram, ja manuāli veidojat pirkšanas pasūtījuma rindu izlaistam preces variantam, ir jānorāda visas nepieciešamās preces dimensijas, pirms pasūtījuma rindā tiek parādīta noklusējuma vieta, noliktava, daudzumi un izpildes laiks. 

Ne visi pasūtījuma noklusējuma iestatījumu parametri tiek lietoti, kad veidojat pasūtījumu vai žurnāla rindas. Daudzumi un izpildes laiki pēc noklusējuma tiek rādīti tikai tad, ja piemērojams. Piemēram, veicot aprēķinus žurnāla rindā, izveidojot rindu, pēc noklusējuma tiek rādīta tikai vieta un noliktava. Šī iemesla dēļ netiek veikta nekādi noklusējuma daudzumi vai pārbaudes par vairākiem minimālajiem daudzumiem, kad veidojot rindu vai grāmatojat žurnālu. 

Kad tiek izveidota pasūtījuma vai žurnāla rinda, sistēmā vienmēr tiek mēģināts atrast noklusējuma vietu un noliktavu. Ne vienmēr vieta pēc noklusējuma tiek rādīta no pasūtījuma iestatījumiem. Piemēram, kad veidojat pārdošanas pasūtījumu vai pirkšanas pasūtījumu, pasūtījuma rindās automātiski tiek lietota vieta no pasūtījuma virsraksta. Veidojot MK rindu, tiek lietota vieta no MK virsraksta. Kad vieta ir noteikta, tā tiek izmantota, lai atrastu visus no vietas atkarīgos pasūtījuma iestatījumus, kurus pēc tam var izmantot kā noliktavas noklusējumu. 

Lapā **Krājumu segums** norādītās krājuma seguma kārtulas var izraisīt noklusējuma pasūtījuma tipa, pirkšanas un krājuma izpildes laika pārlabošanu. Lai gan pasūtījuma noklusējuma iestatījumi neļauj nodalīt ražošanas un pārsūtīšanas izpildes laiku, krājumu seguma kārtulas to atļauj. Taču krājuma seguma iestatījumus Galvenā plānošana (MRP) izmantos tikai, lai veidotu plānotu ražošanu un plānotus pārsūtīšanas pasūtījumus, un šie iestatījumi netiks lietoti, kad ražošanas un pārsūtīšanas pasūtījumus veidojat manuāli. 

## <a name="default-order-settings-rules"></a>Pasūtījuma noklusējuma iestatījumu kārtulas

Varat definēt vispārējus pasūtījuma noklusējuma iestatījumus un neierobežotu skaitu pasūtījuma noklusējuma iestatījumu kārtulu, kuras attiecas tikai uz konkrētiem nosacījumiem, piemēram, uz kādu vietu vai konkrētu preces dimensiju, vai preces dimensiju kombināciju. Nevar definēt no noliktavas atkarīgus pasūtījumu iestatījumus.

### <a name="rank-in-default-order-settings"></a>Pasūtījuma noklusējuma iestatījumu rangs

Pasūtījuma noklusējuma iestatījumu kārtulām ir rangi. Jo augstāks rangs, jo svarīgāka kārtula — tas nozīmē, ka tai būs augstāka prioritāte un tā tiks izmantota pirms kārtulām ar zemāku rangu. Vispārējiem pasūtījuma noklusējuma iestatījumiem rangs ir nulle, un to nevar modificēt. Tikai vienai kārtulai rangs var būt nulle. Kārtulām var būt vienāds rangs, bet ar nosacījumu, ka tās attiecas uz dažādām dimensijām. Tas ir noderīgi no vietas atkarīgu pasūtījuma iestatījumu modelēšanai. Kad tiek izveidota jauna noklusējuma pasūtījuma iestatījumu kārtula, pasūtījuma vērtību, apturēšanas karodziņa un citu vienumu vērtības tiek pārmantotas no kārtulas ar nulles rangu, taču šīs vērtības var pārlabot.

### <a name="default-order-settings-for-released-products"></a>Pasūtījuma noklusējuma iestatījumi izlaistām precēm

Atšķirīgām izlaistajām precēm varat definēt vispārējos pasūtījuma iestatījumus vai no vietas atkarīgus pasūtījuma iestatījumus. Vispārīgajiem pasūtījuma iestatījumiem rangs vienmēr ir nulle. Ja vienlaicīgi iestatāt jaunus pārdošanas, pirkšanas un krājumu pasūtījuma iestatījumus, ieteicams lietot skatu **Detalizētas informācijas skats** lapā **Pasūtījuma noklusējuma iestatījumi**. Lai pārslēgtu uz detalizētas informācijas skatu, dodieties uz darbību rūti **Opcijas** &gt; **Lapas opcijas** &gt; **Mainīt skatu** &gt; **Detalizētas informācijas skats**.

### <a name="site-specific-order-settings"></a>Vietai raksturīgie pasūtījuma iestatījumi

Lai izveidotu no vietas atkarīgus pasūtījuma iestatījumus, atlasiet **Jauns**. **Detalizētas informācijas skatā** ievadiet vietni laukā **Vietne** sadaļā **Iestatījumi, kas piemērojami šeit**. Skatā **Režģa skats** ievadiet vietas vērtību kolonnā **Vieta**. Jaunajai kārtulai tiek automātiski piešķirta jauna ranga vērtība, kas ir lielāka par 0 (nulli). Varat izveidoti tik daudz vietnei raksturīgo kārtulu, cik nepieciešams. Lai norādītu, ka tās ir vienlīdz svarīgas, var piešķirt vienu ranga vērtību visām vietnei raksturīgajām kārtulām.

Ja esat atvēris skatu **Detalizētas informācijas skats**, nevar iegūt pārskatu par krājumam izveidotajām kārtulām. Izmantojiet pogu **Rādīt/slēpt sarakstu**, lai redzētu pārskata informāciju. Kad tiek izveidota jebkāda veida pasūtījuma rinda, kam nav norādīta vieta, programmatūrā Supply Chain Management tiek meklēta kārtula, kurai nav norādīta vieta. Tas palīdz pasūtījuma rindai noteikt noklusējuma vietu. Pēc tam šī vieta tiek izmantota no vietas atkarīgas kārtulas meklēšanai, kur var būt iestatīta noklusējuma noliktava. Šī noliktava tiek lietota pasūtījuma rindā.

### <a name="specific-order-settings-for-product-dimension"></a>Īpaši pasūtījuma iestatījumi preces dimensijai

Pasūtījuma iestatījumu kārtulas varat definēt jebkurai aktīvai preces dimensijai vai aktīvu preces dimensiju kombinācijai. Ja preces dimensijas lauks ir tukšs, tad šī kārtula attiecas uz visām preces dimensijas vērtībām. 

Aplūkosim nākamo preces piemēru.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Preces nosaukums**                                    | Fotoelektriskais sensors                    |
| **Krājuma numurs**                                     | XW56                                    |
| **Konfigurācija** (izmantota gaismas tipa modelēšanai) | C1-redzamā sarkanā gaisma, C2-infrasarkanā gaisma |
| **Versija** | V1, V2, V3                              |

Šajā piemērā tiek pieņemts, ka prece tiek sagādāta, nevis ražota. Tiek arī pieņemts, ka konfigurācija C1 tiek lietota biežāk, tāpēc tai ir īsāki izpildes laiki. 

Lai modelētu šo scenāriju, izveidojiet tālāk norādītos pasūtījuma noklusējuma iestatījumus.

| Rangs | Vieta | Konfigurācija | Versija | Iegādāšanās — ignorēt noklusējuma iestatījumus | Pirkšanas izpildes laiks | Iegādāšanās — apturēta | Pārdošana — ignorēt noklusējuma iestatījumus | Pārdošana — apturēta |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10.   |      | C1            |       | Jā                                  | 2.                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5.                  |                    |                                   |                 |

Kad precei XW56, konfigurācijai C1 tiek izveidota pirkšanas pasūtījuma rinda vai plānotais pirkšanas pasūtījums, tad neatkarīgi no versijas vai vietas, kur šī rinda atrodas, izpildes laiks tiek uzskatīts par 2. Pieņemam, ka ir apturētas visas versijas, izņemot V3.

Varat izveidot tālāk norādītās pasūtījuma noklusējuma iestatījumu kārtulas.

| Rangs | Vieta | Konfigurācija | Versija | Iegādāšanās — ignorēt noklusējuma iestatījumus | Pirkšanas izpildes laiks | Iegādāšanās — apturēta | Pārdošana — ignorēt noklusējuma iestatījumus | Pārdošana — apturēta |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Jā                                  |                    | Jā                | Jā                               | Jā             |
| 20   |      |               | V1    | Jā                                  |                    | Jā                | Jā                               | Jā             |
| 10.   |      | C1            |       | Jā                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Diviem veco versiju apturēšanas noteikumiem ir vienāds rangs. Tāpēc tie ir vienlīdz svarīgi. Tā kā abām šīm kārtulām ir augstāks rangs nekā kārtulai, kas attiecas uz konfigurāciju C1, tām ir virsroka pār konfigurācijas C1 kārtulu. 

Šajā piemērā ir paskaidrota ranga nepieciešamība. Ja ranks netiek izmantots brīdī, kad pirkšanas pasūtījums tiek izveidots konfigurācijai C1 un versijai V2, abas V2 un C1 definētās kārtulas būs neskaidras. Lai novērstu šo neskaidrību, programmatūrā Supply Chain Management kārtulas tiek meklētas dilstošā secībā pēc ranga un tiek izmantota pirmā attiecināmā kārtula. Pašreizējā piemērā, kad pirkšanas pasūtījuma rinda tiek izveidota konfigurācijai C1 un versijai V2, lietotājs saņem brīdinājuma ziņojumu, ka krājums ir aizturēts un ka to ir izraisījusi versijas vērtība. Ja konfigurācijas kārtulas rangs būtu augstāks par versijas kārtulas rangu, tad šī pirkšanas pasūtījuma rindas izveidošana konfigurācijai C1 un versijai V2 būtu izpildīta sekmīgi, un lietotājs nesaņemtu ziņojumu “krājums ir aizturēts”. 

Apsveriet tālāk norādītās pasūtījuma noklusējuma iestatījumu kārtulas.

| Rangs | Vieta | Konfigurācija | Versija | Noklusējuma atrašanās vieta | Noklusējuma noliktava | Pirkšana — ignorēt noklusējuma noliktavas dimensijas | Pirkšanas noliktava |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Jā                                            | 22                 |
| 10.   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11.                |                                                |                    |

Lai noteiktu vietu un noliktavu, sistēma divreiz šķērso kārtulu kopu. Kad pirkšanas pasūtījuma rinda tiek izveidota konfigurācijai C1, versijai V2, tad vietne tiek noteikta, balstoties uz kārtulu ar rangu 10. Pēc tam sistēma meklē kārtulu vietai 2, lai noteiktu noliktavu. Kārtula 20 tiek atrasta, un — tā kā tās rangs ir augstāks — noliktava pirkšanas pasūtījuma rindā būs 22, nevis 21.

Parasti konkrētas kārtulas un dimensiju kārtulas, kuras ir svarīgākas par citām dimensijām, saņem augstāku rangu, bet vispārīgākām kārtulām tiek piešķirti zemāki rangi. 

Kārtula ar nulles rangu kalpo par drošības tīklu. Ja nav piemērota neviena cita kārtula, tad tiks izmantoti pasūtījuma noklusējuma iestatījumi no nulles kārtulas. 

Tā kā ranga skaitlis ir svarīgs, darbību rūtī **Pasūtījuma noklusējuma iestatījumi** pastāv funkcijas kārtulu pārbīdīšanai uz augšu vai uz leju un kārtulu pārnumurēšanai, lai tās vienmēr būtu uzskaitītas ar soļiem pa 10. 

Izlaistajām precēm var būt daudz izveidoto kārtulu. Lai gūtu labāku priekšstatu par to, ko katra kārtula pārraksta un kāpēc tā ir nepieciešama, iesakām lietot skatu **Režģa skats** lapā **Pasūtījuma noklusējuma iestatījumi**. Režģa skatu varat iespējot, dodoties uz darbību rūti **Opcijas** &gt; **Lapas opcijas** &gt; **Mainīt skatu** &gt; **Režģa skats**. Režģī rādīto kolonnu skaits varētu būt diezgan būtisks, it īpaši attiecībā uz pārdošanas un krājumu cilnēm. Lai ierobežotu režģī rādīto kolonnu skaitu, kolonnu grupas ir iespējams slēpt vai rādīt, izmantojot pogas izvēlnē **Pasūtījuma noklusējuma iestatījumi** &gt; **Kolonnas attēlojums**.

### <a name="specific-order-settings-for-released-product-variant"></a>Īpaši pasūtījuma iestatījumi izlaistās preces variantam

Ja kārtulu sistēma pasūtījuma noklusējuma iestatījumiem ir pārāk apgrūtinoša, pastāv iespēja definēt noklusējuma pasūtījuma uzstādījumus katram preces variantam. Nākamajā piemērā ir parādīts, kā tas izskatītos precei un iepriekš aprakstītajos gadījumos.

| Rangs | Vieta | Konfigurācija | Versija | Iegādāšanās — ignorēt noklusējuma iestatījumus | Pirkšanas izpildes laiks | Iegādāšanās — apturēta | Pārdošana — ignorēt noklusējuma iestatījumus | Pārdošana — apturēta |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10.   |      | C2            | V3    | Jā                                  | 5                  |                    |                                   |                 |
| 10.   |      | C2            | V2    | Jā                                  | 5                  | Jā                | Jā                               | Jā             |
| 10.   |      | C2            | V1    | Jā                                  | 5                  | Jā                | Jā                               | Jā             |
| 10.   |      | C1            | V3    | Jā                                  | 2                  |                    |                                   |                 |
| 10.   |      | C1            | V2    | Jā                                  | 2                  | Jā                | Jā                               | Jā             |
| 10.   |      | C1            | V1    | Jā                                  | 2                  | Jā                | Jā                               | Jā             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Šajā gadījumā rangs nav īsti svarīgs, tāpēc varat izvēlēties to slēpt. Šis risinājums potenciāli izraisa uzturēšanas problēmu. Taču varat apsvērt iespēju izmantot šo iestatījumu, ja plānojat integrēšanu ar Preces dzīves cikla pārvaldības (Product Lifecycle Management — PLM) sistēmām.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Izmantojiet noklusējuma pasūtījumu daudzumu stingru vai standarta apstiprināšanu

Varat izvēlēties, cik stingrai sistēmai jābūt, pārbaudot daudzumus, kas ierakstīti preces **Noklusētajos pasūtījuma iestatījumos**. Kad izmantojat jauno, stingro opciju, **Standarta pasūtījuma daudzumam** vienmēr jābūt norādītās **Vairāku** vērtību reizinājumam pirkšanas pasūtījumiem, krājumiem un pārdošanas pasūtījumiem. Ja izmantojat stingro pārbaudi, nevarēsiet saglabāt noklusējuma pasūtījuma iestatījumus, kas neatbilst šai prasībai (un ziņojumu joslā tiek rādīta kļūda). 

Stingrā pārbaude attiecas uz **Standarta pasūtījuma daudzuma** vērtībām, kas norādītas **Pirkšanas pasūtījumā**, **Krājumā** un **Pārdošanas pasūtījuma** kopsavilkuma cilnēs lapā **Noklusējuma pasūtījuma iestatījumi**. Katrai kopsavilkuma cilnei ir savi **Vairāki** iestatījumi, kas tiek izmantoti, lai apstiprinātu **Standarta pasūtījuma daudzuma** vērtību, kas norādīta šai kopsavilkuma cilnei.

### <a name="enable-the-strict-validation-option"></a>Iespējot stingrās pārbaudes opciju

Lai varētu izmantot stingrās pārbaudes opciju, tā vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības. Šeit līdzeklis tiek norādīts kā:

- **Modulis** - *Preču informācijas pārvaldība*
- **Līdzekļa nosaukums** - *Stingrā pārbaude pēc noklusējuma pasūtījumu daudzumiem*

### <a name="set-the-validation-option"></a>Iestatiet pārbaudes opciju

Lai iestatītu pārbaudes opciju:

1. Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču informācijas pārvaldības parametri**.
1. Cilnē **Vispārīgi** iestatiet **Pārbaude noklusējuma pasūtījumu daudzumiem** uz vienu no šīm vērtībām:
    - **Stingrā** — Atlasiet šo opciju, lai nodrošinātu, ka visas **Standarta pasūtījuma daudzuma** vērtības būs **Vairāku** vērtību reizinājums katrai kopsavilkuma cilnei (**Pirkšanas pasūtījums**, **Krājumi** un **Pārdošanas pasūtījums**).
    - **Standarta** — Atlasiet šo opciju, lai izmantotu standarta pārbaudi (kas darbojas tieši tāpat, kā, kad šis līdzeklis nav iespējots).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]