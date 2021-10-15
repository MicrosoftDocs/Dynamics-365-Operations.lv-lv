---
title: Pārsniegtās/nepārsniegtās transakcijas
description: Šī tēma sniedz informāciju, kas palīdzēs jums iestatīt detalizētu informāciju par pārsniegto/nepārsniegto darbību politikām, tādējādi sistēma var noteikt, kā pārvaldīt preču apstrādes pārsniegšanu/nepietiekamību saņemšanas laikā.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 60f4f31e9da762a89b034961a703e1d7b1bbd903
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580748"
---
# <a name="overunder-transactions"></a>Pārsniegtās/nepārsniegtās transakcijas

[!include [banner](../../includes/banner.md)]

Kad reisa pasūtījumi ir apstrādāti, sistēma sagaida, ka krājumu daudzums, kas gala galamērķa noliktavā saņemts patēriņam, saskanēs ar daudzumu, kas norādīts ar reisu saistītās pirkšanas pasūtījuma rindās. Tomēr, tā kā noliktavā ne vienmēr nav saņemts precīzs pirkšanas pasūtījuma rindu daudzums, **Kopējo izmaksu** modulis definē kārtulu kopu, kas tiek lietota, lai apstrādātu preču pārāk daudz saņemšanu un nepiemērošanu. Šīs kārtulas ir īpaši svarīgas, jo oriģinālais pirkšanas pasūtījums ir iekļauts rēķinā un to vairs nevar modificēt. Iestatot detalizētu informāciju par pārsniegšanas/nepārsniegšanas darbību politikām, jūs iespējojat sistēmu, lai noteiktu, kā preču pārsniegšanas un nepietiekamības apstrādi saņemšanas laikā. Jūs variet arī manuāli pārvaldīt krājumu pietiekamību vai trūkumu, izmantojot lapu **Pārsniegtās/neveiktās darbības**.

## <a name="overunder-tolerances"></a>Pārsniegšanas/nepārsniegšanas tolerances

Jūs iestatāt pasūtījuma pārsniegšanas un nepiegādāšanas tolerances, lai norādītu pārsniegtos un nesasniegtos daudzumus vai tilpumus, kurus var apstrādāt reisā, neraisot kļūdu. Ja reisa rindas saņemšana ir ārpus šīm tolerancēm, tā ir jāmodificē un jāatrisina, pirms reisa rindu var slēgt turpmākai apstrādei.

Lai konfigurētu tolerances, dodieties uz sadaļu **Kopējās izmaksas \> Pāsniegšanas/nepiegādāšanas iestatījumi \> Pārsniegšanas/nepiegādāšanas tolerances**. Tur varat skatīt, rediģēt, pievienot un noņemt tolerances ierakstus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Konta kods | <p>Nosakiet kreditoru darbības jomu, uz kuru attiecas tolerance, atlasot vienu no šīm vērtībām:</p><ul><li>**Tabula** – pārsniegšanas/nepiegādāšanas pielaides vērtības attiecas tikai uz kreditoru, kurš ir atlasīts rindai.</li><li>**Grupa** – pārsniegtās/nepiegādātās tolerances vērtības attiecas tikai uz kreditoru, kurš ir atlasīts rindai.</li><li>**Visi** – pārsniegšanas/nepiegādāšanas pielaide tiek piemērota visiem kreditoriem.</li></ul> |
| Kontu saistība | Atlasiet kreditoru vai kreditoru grupu, uz kuru attiecas virs tolerance/nevērtība, atkarībā no vērtības, ko izvēlējāties **Konta koda** laukā. |
| Krājuma kods | <p>Nosakiet krājumu darbības jomu, uz kuru attiecas tolerance, atlasot vienu no šīm vērtībām:</p><ul><li>**Tabula** – pārsniegšnas/nepiegādāšanas pielaides vērtības attiecas tikai uz krājumu, kurš ir atlasīts rindai.</li><li>**Grupa** – pārsniegšanas/nepiegādāšanas tolerances vērtības attiecas uz visiem krājumiem krājumu tolerances grupā, kas ir atlasīta rindai.</li><li>**Visi** – pārsniegšanas/nepiegādāšanas tolerance tiek piemērota visiem krājumiem.</li></ul> |
| Krājumu saistība | Atlasiet krājumu vai krājumu grupu, uz kuru attiecas pārsniegšanas/nepiegādāšanas tolerance atkarībā no vērtības, ko izvēlējāties **Krājuma koda** laukā. |
| Pieļaujamā summa | Ievadiet summas toleranci, kas jālieto visam pirkšanas pasūtījumam. |
| Procentuālā tolerance | Ievadiet procentuālo toleranci, kas jālieto atsevišķai pirkšanas pasūtījuma rindai. |

## <a name="overunder-reasons"></a>Pārsniegšanas/nepārsniegšanas iemesli

Ja daudzums, kas pārsniedz daudzumu vai ir zem tā, ir saistīts ar saņemto reisa rindu, iespējams, būs jāidentificē daudzuma pietiekamības vai trūkuma iemesli. Šajā gadījumā preču saņemšanas rindā var atlasīt pasūtījuma pārssniegšanu vai nezemās piegādes iemeslu.

Lai iestatītu pasūtījuma pārsniegšanu un nepiegādāšanas iemeslus, dodieties uz sadaļu **Kopējās izmaksas \> Pārsniegšanas/nepiegādāšanas iestatījumi \> Pārsniegšanas/nepiegādāšanas iemesli**. Tur ir iespējams apskatīt, rediģēt, pievienot un noņemt pieejamos piegādes pārsniegšanas un nepiegādāšanas iemeslus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram iemeslam.

| Lauks | Apraksts |
|---|---|
| Pārsniegšanas/nepārsniegšanas iemesls | Ievadiet unikālu nosaukumu darbību pārsniegšanas vai nepiegādāšanas iemeslam. |
| Apraksts | Ievadiet pārsniegšanas/nepiegādāšanas iemesla aprakstu. |
| Kustība | Atlasiet kustības žurnālu, kas ir saistīts ar pārsniegšanas/nepiegādāšanas iemeslu. Šis lauks uzskaita visus pieejamos žurnālus, kuru *Kustību* žurnāla tips ir saistīts ar **Krājumu žurnālu nosaukumiem** lapā (**Krājumu vadības iestatījumi \> Žurnālu nosaukumi \> Krājumi**). |

## <a name="item-overunder-tolerance-groups"></a>Krājuma pārsniegtās/nepārsniegtās tolerances grupas

Krājumus ar līdzīgām toleranci var grupēt kopā. Šādā veidā visiem šīs grupas krājumiem var iestatīt pārt/ne zemo toleranci vienlaikus.

Lai iestatītu krājuma pārsniegšanu un nepiegādāšanas grupas, dodieties uz **Kopējās izmaksas \> Pārsniegšanas/nepiegādāšanas iestatījumi \> Tolerances grupu pārsniegšanas/nepiegādāšanas krājumi**. Tur varat skatīt, rediģēt, pievienot un noņemt pārsniegšanas/nepiegādāšanas tolerances grupas ierakstus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Pārsniegšanas/nepārsniegšanas tolerances grupa | Ievadiet unikālu grupas nosaukumu. Izvēlieties nosaukumu, kas apraksta toleranci, piemēram, *1% Var*. |
| Apraksts | Ievadiet grupas aprakstu. |

## <a name="vendor-overunder-tolerance-groups"></a>Kreditora pārsniegtās/nepārsniegtās tolerances grupas

Var sagrupēt kreditorus, kas regulāri nodrošina pārsniedz pasūtījumu vai nepiegādā pilnībā. Pēc tam varat iestatīt pārsniegšanas/nepilnas piegādes tolerances vērtības katrai grupai.

Lai iestatītu kreditoru pārsniegšanas/nepiegādāšanas tolerances grupas, dodieties uz **Kopējās izmaksas \> Pārsniegšanas/nepiegādāšanas iestatījumi \> Kreditoru pārsniegšanas/nepiegādāšanas tolerances grupas**. Tur varat skatīt, rediģēt, pievienot un noņemt pārsniegšanas/nepiegādāšanas tolerances grupas ierakstus. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Pārsniegšanas/nepiegādāšanas grupas | Ievadiet unikālu grupas nosaukumu. Izvēlieties nosaukumu, kas apraksta grupai piedero kreditoru tipu. |
| Apraksts | Ievadiet grupas aprakstu. |

## <a name="view-and-process-overunder-transactions"></a>Skatīt un apstrādāt pārsniegšanas/nepiegādāšanas darbības

Pārsniegšanas un nepiegādāšanas darbības veidojas, novietoto preču daudzumam neatbilstot sākotnējam daudzumam. Saņemšanas žurnālā daudzums jāatjaunina tikai ar daudzumu, kas ir ievietots.

Kad reisa rindu ieejas plūsma ir apstrādāta, kreditoram var tikt iestatītas pārsniegšanas/nepiegādāšanas tolerances. Pēc tam krājumi tiks pārskatīti un pārbaudīti. Toleranci var iestatīt kā procentus, vietējo summu vai abus.

Ja saņemtais krājums ir tolerances robežās, sistēma izveidos kustības žurnālu. Šo žurnālu var norādīt reisu parametru lapā. Turklāt tiks izveidota pārsniegšanas/nepiegādāšanas darbība. Piemēram, pasūtījuma vērtība ir $100, ieejas plūsmas vērtība ir $99, un šīs vērtības atbilst tolerances nosacījumiem. Šajā gadījumā tiks izveidots negatīvs kustību žurnāls par daudzumu, kas nav saņemts.

Ja saņemtais krājums ir ārpus tolerances, sistēma ģenerēs daudzuma atšķirību virs/zemo darbību.

Lai skatītu un apstrādātu pārsniegšanas/nepiegādāšanas darbības, dodieties uz **Kopējās izmaksas \> Uzziņas \> Pārsniegšanas/nepiegādāšanas darbības**. Pārsniegšanas/nepiegādāšanas darbība tiks saistīta ar visiem reisa krājumiem, kuru ir pārāk vai nepietiekami daudz. Ieteicams izmantot lapu **Pārsniegtās/neveiktās darbības**, lai atrisinātu visas ar reisiem saistītās pārsniegtās/neveiktās darbības. Iesakām arī **neizmantot** kustības vai inventarizācijas žurnālus, lai manuāli atrisinātu ne ievadītās piegādes noliktavas darbības. Tā vietā ir jāizmanto lapa **Pārsniegtās/neveiktās darbības**, lai pārvaldītu nepiegādātā pasūtījuma noliktavas daudzumus.

### <a name="upper-overview-tab"></a>Augšējā cilne Pārskats

Lai skatītu pārsniegtās/neveiktās darbības, atlasiet cilni **Pārskats**, kas atrodas lapas **Pārsniegtās/neveiktās darbības** augšējā daļā. Tālāk esošajā tabula apraksta laukus, kas ir pieejami režģī.

| Lauks | Apraksts |
|---|---|
| Pārsniegtās/nepārsniegtās transakcijas numurs | Unikālais pārsniegto/neveikto darbību ieraksta nosaukums, kas tika izveidots automātiski saņemšanas žurnāla apstrādes laikā. |
| Reiss | Reiss, kam pievienota pirkšanas rinda. |
| Nosūtīšanas konteiners | Konteiners, kam pievienota pirkšanas rinda. |
| Saņemšanas žurnāls | Saņemšanas žurnāls, no kura tika ģenerēta pārsniegšanas/neveikšanas rinda. |
| Atsauce | Atsauce vai nu uz pirkšanas pasūtījumu, vai pārsūtīšanas pasūtījumu, kas ir saistīts ar pārsniegšanas/neveikšanas darbību. |
| Skaits | Pirkšanas pasūtījums, uz kuru ir atsauce pārsniegtajā/neveiktajā darbībā. |
| Kreditora konts | Kreditors, ar ko ir saistīta pārsniegšana/neveikšana. |
| Tranzītpreču numurs | Tranzīta preču numurs, ja nepieciešams. |
| Krājums | Krājuma numurs, ar ko ir saistīta pārsniegšana/neveikšana. |
| Sākotnējais daudzums | Sākotnējais pirkšanas pasūtījuma rindas daudzums, kas ir piesaistīts sūtījumam. |
| Saņemtais daudzums | Faktiski saņemtais daudzums. |
| Starpība | Paredzamās saņemšanas žurnāla summas un saņemšanas žurnālā grāmatotās summas starpība. Negatīva vērtība norāda preču piegādes pāsniegšanu. |
| Atlikušais daudzums | Daudzums, kas paliek saņemšanas žurnāla rindā. |
| Pārsniegts/nepārsniegts pasūtījums | Vērtība, kas norāda, vai saņemtais daudzums ir pārāk liels vai mazs. |
| Statuss | Skatiet pārsniegtās/neveiktās darbības statusu. Atkarībā no iestatījumiem lapā **[Kopējo izmaksu parametri](landed-cost-parameters.md)**, pārāk lielu piegādi var automātiski izveidot kustības žurnālu papildu piegādes summai un grāmatot žurnālu. Šādā gadījumā pārsniegtās/neveiktās darbības statuss būs *Pabeigts*. Ja ir jāveic darbība, lai preces pārvietotu no nepiegādātās noliktavas, ieraksta statuss būs *Procesā*. |
| Pārsniegšanas/nepārsniegšanas iemesls | Atlasiet kustības žurnālu, kas ir saistīts ar pārsniegšanas/nepiegādāšanas iemeslu. |
| Citas krājumu dimensijas | Ja nepieciešams, varat rādīt režģī papildu dimensiju kolonnas. Šīs dimensijas ietver partijas numuru, krājuma statusu un noliktavu. Darbību rūtī atlasiet **Krājumi \> Rādīt dimensijas**, lai atvērtu dialoglodziņu, kurā var atlasīt iekļaujamās dimensijas. |

### <a name="upper-general-tab"></a>Augšējā cilne Vispārīgi

Lai skatītu papildinformāciju par rindu, kas pašreiz atlasīta augšējā cilnē **Pārskats**, atlasiet cilni **Vispārīgi**, kas atrodas lapas **Pārsniegtās/neveiktās darbības** augšējā daļā. Informācija šajā cilnē ietver vērtības visām pieejamām dimensijām. Šī informācija tiek izvilkta no sākotnējā pirkšanas pasūtījuma.

### <a name="lower-overview-tab"></a>Apakšējā cilne Pārskats

Lai skatītu papildinformāciju par rindu, kas pašreiz atlasīta augšējā cilnē **Pārskats**, atlasiet cilni **Vispārīgi**, kas atrodas lapas **Pārsniegtās/neveiktās darbības** apakšējā daļā. Nākamajā tabulā ir aprakstīti pieejamie lauki.

| Lauks | Apraksts |
|---|---|
| Jauna dokumenta veids | Atkarībā no darbības, kas parādīta atlasītajā pārsniegtās//neveiktās darbības rindas, šis lauks ir iestatīts vai nu uz *Kustības žurnāls*, vai nu uz *Pirkšanas pasūtījums*. |
| Skaits | Atsauce un saite vai nu uz pirkšanas pasūtījumu, vai kustību žurnālu, kas ir saistīts ar pārsniegšanas/neveikšanas darbību rindu. |
| Pārsniegšanas/nepārsniegšanas iemesls | Atlasiet ar izvēlēto pārsniegšanas/nepiegādāšanas darbību rindu saistīto iemeslu. |
| Daudzums | Atlasītais daudzums pirkšanas pasūtījumam vai kustību žurnālam, kas ir saistīts ar pārsniegšanas/neveikšanas darbību rindu. |

### <a name="lower-general-tab"></a>Apakšējā cilne Vispārīgi

Lai skatītu pārspīlēšanas/apakšdarbības numuru, laidiena ID un dimensijas numuru, kas ir saistīti ar atlasīto pārsniegto/neveikto darbību rindu, atlasiet cilni **Vispārīgi**, kas atrodas lapas **Pārsniegtās/neveiktās darbības** apakšējā daļā. 

### <a name="process-overunder-transactions"></a>Apstrādāt pārsniegtās/neveiktās darbības

Darbību rūts darbību lapā **Pārsniegtās/neveiktās darbības** nodrošina šādas komandas, lai apstrādātu lapā atlasītās darbības. Katra komanda ļauj izvēlēties, kā apstrādāt katru darbību.

- **Izveidot \> Kustība** - izveidojiet un grāmatojiet kustības žurnālu atlasītajai darbībai. Sadaļās darbībām kustības žurnāls tiek automātiski izveidots un grāmatots, lai prognozētā un faktiskā saņemtā daudzuma starpībai. Atlasiet šo komandu pārsniegtajām darbībām, ja vēlaties, lai kreditors realizētu izmaksu atšķirību.
- **Izveidot \> Pirkšanas pasūtījums** - izveidojiet pirkšanas pasūtījumu, lai uzlabotu atlasītās darbības prognozētā un faktiskā saņemtā daudzuma starpību. Atlasiet šo komandu pārsniegtajām darbībām, ja vēlaties, lai kreditors realizētu izmaksu atšķirību.
- **Izveidot \> Pārsūtīšana uz galamērķi** - šī komanda attiecas tikai uz pārsūtīšanas pasūtījumiem. Atlasiet to, ja uz mērķa noliktavu vēlaties pārsūtīt pārsniegto vai nepietiekamo daudzumu.
- **Izveidot \> Pārsūtīšana uz izcelsmes vietu** - šī komanda attiecas tikai uz pārsūtīšanas pasūtījumiem. Atlasiet to, ja uz izcelsmes noliktavu vēlaties pārsūtīt pārsniegto vai nepietiekamo daudzumu.
