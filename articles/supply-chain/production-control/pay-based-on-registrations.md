---
title: "Apmaksa atbilstoši reģistrācijām"
description: "Šajā tēmā ir paskaidrots, kā tiek aprēķināta apmaksa, pamatojoties uz nodarbinātaisu reģistrācijām."
author: johanhoffmann
manager: AnnBe
ms.date: 03/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgCalcApproveWeekView
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1ae0f142ebd2252b1df414998c153d32127bc1b7
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="pay-based-on-registrations"></a>Apmaksa atbilstoši reģistrācijām

[!include [banner](../includes/banner.md)]

Šajā tēmā ir plaši paskaidrots, kā tiek aprēķināta apmaksa, pamatojoties uz nodarbinātaisu reģistrācijām. Tēmā ir iekļauti piemēri, kas parāda, kā dažādas iestatījumu opciju kombinācijas, kas ir pieejamas aprēķināšanai, ietekmē rezultātu. Dažas no šajā tēmā aplūkotajām jomām:

- Brīvais režīms
- Virsstundas
- Pārtraukumi
- Pārslēgšanās kodi
- Apmaksas krājumi
- Apmaksas līgumi
- Laika un apmeklētības aprēķināšanas parametri
- Kavējumi

## <a name="the-use-of-flex-time"></a>Brīvā režīma izmantošana

Brīvā režīma periodi tiek iestatīti laika profilos, kuri tiek izmantoti laika un apmeklētības aprēķināšanai. Pastāv divi brīvā režīma profila tipi: **Brīvais režīms +** un **Brīvais režīms -**. Kad nodarbinātais reģistrē laiku brīvā režīma + periodā, nodarbinātā brīvā režīma bilance tiek palielināta, pievienojot nostrādāto stundu skaitu. Nodarbinātais nesaņem nekādu kompensāciju par stundām, kas nostrādātas brīvā režīma + periodā. Tomēr nodarbinātais var paņemt brīvu laiku brīvā režīma - periodos, kompensējot to ar stundām no sava brīvā režīma bilances. Tāpēc brīvā režīma periodos reģistrētais brīvais laiks sistēmā tiek uzskatīts par kavējumu.

## <a name="scenarios-based-on-flex-periods"></a>Scenāriji, kuru pamatā ir brīvā režīma periodi

Tālāk ir aprakstīti divi scenāriji, kuru pamatā ir brīvā režīma profils, kas atbilst darbdienai. Abos scenārijos apmaksa tiek aprēķināta saskaņā ar brīvā režīma periodu, kurā nodarbinātais ir reģistrējis ierašanās un aiziešanas laikus.

### <a name="flex-profile-for-one-workday"></a>Brīvā režīma profils vienai darbdienai

| Profila tips  | Sākšana    | Beigt      | diena;     |
|---------------|----------|----------|---------|
| Virsstundas     | 00:00 | 06:00 | Pirmdienās  |
| Brīvais režīms +         | 06:00 | 07:00 | Pirmdienās  |
| Ierašanās laiks      | 07:00 | 07:00 | Pirmdienās  |
| Standarta laiks | 07:00 | 14:30 | Pirmdienās  |
| Brīvais režīms-         | 14:30 | 15:30 | Pirmdienās  |
| Aiziešanas laiks     | 15:30 | 15:30 | Pirmdienās  |
| Virsstundas     | 15:30 | 06:00 | Otrdienās |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>1. scenārijs: nodarbinātais reģistrē ierašanās laiku brīvā režīma + periodā un aiziešanas laiku brīvā režīma - periodā

Tālāk ir attēlotas nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      |
|---------------------------|----------|----------|
| Ierašanās laiks                  | 06:30 | 06:30 |
| Ražošanas darbs            | 06:30 | 14:45 |
| Aiziešanas laiks                 | 14:45 | 14:45 |

Nodarbinātā dienas laikā veiktās reģistrācijas tiek aprēķinātas un pārsūtītas apmaksāšanai lapā **Apstiprināt** (**Laiks un apmeklētība** &gt; **Pārskatīt un apstiprināt** &gt; **Apstiprināt**). Pēc reģistrāciju aprēķināšanas rezultātus var skatīt cilnē **Laiki**. 

Lai izprastu šo scenāriju, skatiet tālāk norādītos laukus.

| Brīvais režīms + | Brīvais režīms - | Laiks | Apmaksājamais laiks |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8.25 | 8.50     |

#### <a name="calculation-of-flex"></a>Brīvā režīma + aprēķins

Saskaņā ar brīvā režīma profilu laiks starp plkst. 06:00 un plkst. 07:00 ir brīvā režīma + periods. Tādēļ, ja nodarbinātais ierodas plkst. 06:30, viņš nopelna 0,5 stundas. Šis laika apjoms tiek pievienots nodarbinātā brīvā režīma bilancei.

#### <a name="calculation-of-flex-"></a>Brīvā režīma - aprēķins

Saskaņā ar brīvā režīma profilu brīvā režīma - periods sākas plkst. 14:30 un beidzas plkst. 15:30. Tādēļ, ja nodarbinātais reģistrē aiziešanas laiku plkst. 14:45 PM, brīvā režīma - periodā atlikušās 45 minūtes (0,75 stundas) tiek reģistrētas kā apmaksājamais laiks, un šis laika apjoms tiek atskaitīts no nodarbinātā brīvā režīma bilances. Šīs 45 minūtes tiek pieskaitītas pie apmaksājamā laika, jo nodarbinātajam tiks piešķirta apmaksa par atlikušajām 45 minūtēm brīvā režīma - periodā. Ja nodarbinātais brīvā režīma - perioda laikā nav darbā, šīs 45 minūtes tiks atskaitītas no viņa brīvā režīma bilances.

#### <a name="calculation-of-time"></a>Laika aprēķins

Laiks tiek aprēķināts kā laiks starp reģistrēto ierašanās un aiziešanas laiku, t. i., laiks no plkst. 06:30 līdz plkst. 14:45 ir vienāds ar 8,25 stundām.

#### <a name="calculation-of-pay-time"></a>Apmaksājamā laika aprēķins

Apmaksājamais laiks ir laiks, par ko nodarbinātajam tiek piešķirta apmaksa. Šajā scenārijā nodarbinātais ir darbā 8,25 stundas (**Laiks**). Tomēr kā **Apmaksājamais laiks** ir aprēķinātas 8,50 stundas, jo nodarbinātajam ir piešķirta apmaksa brīvā režīma - periodā pēc tam, kad viņš ir reģistrējis aiziešanas laiku. Apmaksājamais laiks ir vienāds ar plānoto darba stundu skaitu, jo brīvā režīma + laiks tiek pievienots nodarbinātā brīvā režīma bilancei, nevis apmaksājamajam laikam. Kavējuma laiks brīvā režīma - periodā tiek kompensēts ar apmaksājamo laiku un tiek atskaitīts no nodarbinātā brīvā režīma bilances.

| Laiks              | Reģistrācijas tips | Apmaksājamais laiks (stundas)      |
|-------------------|-------------------|-----------------------|
| 6:30–7:00 | Brīvais režīms +             | 0                     |
| 7:00–14:45 | Standarta laiks     | 7,75                  |
| 14:45–15:30 | Brīvais režīms-             | 0,75 (kavējuma periods) |
|                   | Summa             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>2. scenārijs: nodarbinātais pavada darbā visu brīvā režīma - periodu un strādā arī virsstundas

Tālāk ir attēlotas nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      |
|---------------------------|----------|----------|
| Ierašanās laiks                  | 06:30 | 06:30 |
| Ražošanas darbs            | 06:30 | 17:00 |
| Aiziešanas laiks                 | 17:00 | 17:00 |

Pēc žurnāla reģistrāciju aprēķināšanas lapā **Apstiprināt** varat apskatīt aprēķina rezultātu cilnē **Laiki**. Lai izprastu šo scenāriju, skatiet tālāk norādītos laukus.

| Brīvais režīms + | Brīvais režīms - | Laiks  | Apmaksājamais laiks | Apmaksājamās virsstundas |
|--------|--------|-------|----------|--------------|
| 0,50   | 0.00   | 10,50 | 10,00    | 1.50         |

#### <a name="calculation-of-flex"></a>Brīvā režīma + aprēķins

Saskaņā ar brīvā režīma profilu laiks starp plkst. 06:00 un plkst. 07:00 ir brīvā režīma + periods. Tādēļ, ja nodarbinātais reģistrē ierašanās laiku plkst. 06:30, viņš nopelna 0,5 stundas brīvā režīma + laika, kas tiek pievienots brīvā režīma bilancei.

#### <a name="calculation-of-flex-"></a>Brīvā režīma - aprēķins

Tā kā nodarbinātais strādā brīvā režīma - periodā, brīvais režīms - netiek aprēķināts. Brīvais režīms - tiek aprēķināts tikai, ja nodarbinātais brīvā režīma - periodā nav darbā. No maksājuma viedokļa raugoties, ja nodarbinātais strādā brīvā režīma - periodā, viņam tiek piešķirta standarta laikam noteiktā apmaksas likme. Ja nodarbinātais brīvā režīma - perioda laikā nav darbā, šīs 45 minūtes tiek atskaitītas no viņa brīvā režīma bilances.

#### <a name="calculation-of-time"></a>Laika aprēķins

Laiks tiek aprēķināts kā laiks starp reģistrēto ierašanās laiku plkst. 06:30 un aiziešanas laiku plkst. 17:00, un tas ir vienāds ar 10,50 stundām.

#### <a name="calculation-of-pay-time"></a>Apmaksājamā laika aprēķins

Šajā scenārijā nodarbinātais ir darbā 10,50 stundas (**Laiks**). Tomēr **Apmaksājamais laiks** tiek aprēķināts kā 10,00 stundas, jo nodarbinātajam netiek piešķirta apmaksa par brīvā režīma + periodu.

#### <a name="calculation-of-pay-overtime"></a>Apmaksājamo virsstundu aprēķins

| Laiks               | Reģistrācijas tips | Apmaksājamais laiks (stundas) |
|--------------------|-------------------|------------------|
| 6:30–7:00  | Brīvais režīms +             | 0                |
| 7:00–14:30  | Standarta laiks     | 7,50             |
| 14:30–15:30  | Brīvais režīms-             | 1,00             |
| 15:30–17:00 | Virsstundas          | 1.50             |
|                    | Summa             | 10,00            |

### <a name="generation-of-pay-items"></a>Apmaksas elementu ģenerēšana

Nodarbināto vienas dienas reģistrācijas var pārsūtīt no lapas **Apstiprināt**. Pārsūtīšanas procesa laikā tiek izveidoti apmaksas elementi un pārsūtītās reģistrācijas. Apmaksas elementi atbilst apmaksājamā laika sadalījumam — tie ir standarta laiks, virsstundas, apmaksātais pārtraukuma laiks un citi elementi.

Lai atvērtu apmaksas elementu sarakstu, atlasiet **Laiks un apmeklētība** &gt; **Pārskatīt un apstiprināt** &gt; **Apstiprināt**. Pēc tam atlasiet **Pieprasījumi** &gt; **Pārsūtītās reģistrācijas**.

Apmaksas elementi veido nodarbinātā atmaksas pamatu. Varat ģenerēt failu, kas satur apmaksas elementu informāciju, un pārsūtīt šo failu uz algu sistēmu.

Pārsūtīšanas procesa ietvaros informācija par ražošanas un projektu aktivitāšu laiku un izmaksām tiek pārsūtīta uz ražošanas un projektu žurnāliem, lai reģistrētu laika un izmaksu tēriņus. Pārsūtītās reģistrācijas nodrošina pamatinformāciju, kas nepieciešama, lai ražošanas pasūtījumiem un projektiem noteiktu laika un izmaksu cenu stundā. Pārsūtītās reģistrācijas var atvērt, izmantojot izvēlni **Pieprasījumi**, kas atrodas lapā **Apstiprināt**.

Piemēram, 2. scenārijā tiek ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma  | Kopējās izmaksas |
|---------------|----------|-----------|-------|------------|
| Standarta laiks | 1201     | 10,0      | 10    | 100        |
| Virsstundas      | 1301     | 1.50      | 5.     | 7,50       |
|               |          |           | Summa | 107,50     |

Standarta laika apmaksas elementam ir 10 stundu apmaksas vienība, kurā ietverts standarta laiks, brīvā režīma -laiks un virsstundas. Standarta laiks, brīvā režīma -laiks un virsstundas ir konsolidēti vienā apmaksas elementā, jo visi šie elementi tiek aprēķināti kā standarta laiks atbilstoši lapā **Aprēķina parametri** atlasītā parametra noklusējuma iestatījumam (**Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Aprēķina parametri**). Virsstundas tiek aprēķinātas papildus standarta laikam, izmantojot papildu likmi “5”.

Ja vēlaties skaidri nošķirt standarta laiku un virsstundas, lai apmaksas tipu apmaksas vienības segtu tikai faktisko nostrādāto standarta laiku un virsstundu laiku, apmaksas vienības par standarta laiku ir jāaprēķina kā 8,50 un apmaksas vienības par virsstundām ir jāaprēķina kā 1,50.

Lai konfigurētu sistēmu skaidri nošķirt standarta laiku un virsstundas, virsstundas ir jāizslēdz no standarta laika. Jums jānomaina arī virsstundu apmaksas tipa iestatījumi, lai virsstundu apmaksas likme segtu visus maksājumus par stundām, kas ir pavadītas, strādājot virsstundas.

### <a name="exclude-overtime-from-the-standard-time"></a>Virsstundu izslēgšana no standarta laika

Lapā **Aprēķina parametri** atlasiet **Virsstundas** kā profila specifikācijas veidu un iestatiet opciju **Apmaksājamais laiks** uz **Nē**, kā parādīts šeit.

| Reģ. specifikācija | Profila specifikācijas tips | Aprēķins   |     | Apmaksāts         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Darba laiks       | Virsstundas                   | Standarta laiks | Jā | Apmaksājamais laiks     | Nav  |
|                    |                            | Apmaksājamais laiks      | Jā | Apmaksājamās virsstundas | Jā |

Pēc aprēķina parametru pielāgošanas tiks ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma  | Kopējās izmaksas |
|---------------|----------|-----------|-------|------------|
| Standarta laiks | 1201     | 8,50      | 10    | 85,0       |
| Virsstundas      | 1301     | 1.50      | 15.    | 22,50      |
|               |          |           | Summa | 107,50     |

> [!NOTE]
> Aprēķina parametriem ir atlasīts ieteicamais standarta iestatījums. Esiet uzmanīgi, mainot šos parametrus. Lai atjaunotu ieteicamos standarta iestatījumus, lapā **Aprēķina parametri** atlasiet **Atjaunot vērtības**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Noviržu atļaušana standarta apmaksas profiliem

Lapā **Profili** (**Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Laika profili** &gt; **Profili**) var iestatīt profila tipus, kas ietver pārslēgšanās kodus un pārtraukumus.

### <a name="switch-codes"></a>Pārslēgšanās kodi

Pārslēgšanās kodus var izmantot, lai ļautu nodarbinātajiem novirzīties no sava profila tipa, mainot uz citu profila tipu. Piemēram, varat atļaut nodarbinātajam pārslēgties no brīvā režīma + laika uz virsstundām. Nodarbinātais var pievienot pārslēgšanās kodu reģistrācijas laikā, vai arī jūs varat reģistrāciju apstiprinātājam piešķirt pārslēgšanās koda pievienošanas uzdevumu.

Lai pārslēgšanās kodu varētu izmantot, jums tas vispirms ir jādefinē kā netiešās aktivitātes tipu. Pēc tam pārslēgšanās kods ir jāpievieno laika profilam, kas atbilst periodam, kurā vēlaties atļaut profila tipa maiņu. Piemēram, izpildiet tālāk norādītās darbības, lai izveidotu pārslēgšanās kodu, kas ļauj brīvā režīma + periodu no plkst. 06:00 līdz plkst. 07:00 mainīt uz virsstundām.

1. Izveidojiet pārslēgšanās kodu ar nosaukumu **OTBCI (Pārvērst brīvā režīma laiku par virsstundām pirms ierašanās laika)**. Atlasiet **Laiks un apmeklētība** &gt; **Pārvaldīt netiešās aktivitātes** &gt; **Netiešās aktivitātes**.
2. Kolonnā **Pārslēgšanās kods** pievienojiet laika profila brīvā režīma + rindai kodu OTBCI.
3. Kolonnā **Papildu** pievienojiet profila tipu **Virsstundas**.

Kā piemēru aplūkojiet tālāk norādīto brīvā režīma profilu, kas atbilst darbdienai.

| Profila tips  | Sākšana    | Beigt      | diena;     |
|---------------|----------|----------|---------|
| Virsstundas     | 00:00 | 06:00 | Pirmdienās  |
| Brīvais režīms +         | 06:00 | 07:00 | Pirmdienās  |
| Ierašanās laiks      | 07:00 | 07:00 | Pirmdienās  |
| Standarta laiks | 07:00 | 14:30 | Pirmdienās  |
| Brīvais režīms-         | 14:30 | 15:30 | Pirmdienās  |
| Aiziešanas laiks     | 15:30 | 15:30 | Pirmdienās  |
| Virsstundas     | 15:30 | 06:00 | Otrdienās |

Tālāk ir attēlotas nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      |
|---------------------------|----------|----------|
| Ierašanās laiks                  | 06:30 | 06:30 |
| Ražošanas darbs            | 06:30 | 14:45 |
| Aiziešanas laiks                 | 17:00 | 17:00 |

Pēc pārsūtīšanas tiek ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma  | Kopējās izmaksas |
|---------------|----------|-----------|-------|------------|
| Standarta laiks | 1201     | 8,50      | 10    | 85,0       |
| Virsstundas      | 1305     | 1.50      | 15.    | 22,50      |
|               |          |           | Summa | 107,50     |

Lapā **Apstiprināt** atsauciet pārsūtīšanu un pēc tam izmantojiet izvēlni **Pārslēgšanās kods**, lai lietošanai atlasītu pārslēgšanās kodu **OTBCI**. Kad pārsūtāt reģistrācijas otro reizi, tiek ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma  | Kopējās izmaksas |
|---------------|----------|-----------|-------|------------|
| Standarta laiks | 1201     | 8,50      | 10    | 80,0       |
| Virsstundas      | 1305     | 2,00      | 15.    | 30,0       |
|               |          |           | Summa | 107,50     |

> [!NOTE]
> Kad lietojat pārslēgšanās kodu, virsstundas tiek palielinātas par 0,5 stundām — no 1,50 uz 2,00. 0,5 stundas ir no plkst. 6:30 līdz plkst. 07:00 reģistrētā brīvā režīma + laika konversija uz virsstundām.

### <a name="breaks"></a>Pārtraukumi

Darba pārtraukumi ietekmē nodarbinātā apmaksas aprēķinu. Pārtraukumi tiek definēti kā netiešās aktivitātes tips. Tie var tikt definēti vai nu kā **Apmaksāts**, lai ļautu pievienot pārtraukuma laiku nodarbinātā apmaksājamajam laikam, vai kā **Neapmaksāts**, lai neļautu pievienot pārtraukuma laiku nodarbinātā apmaksājamajam laikam. Pārtraukumu var definēt arī kā **Plānots** vai **Reģistrēts**.

#### <a name="planned-breaks"></a>Plānotie pārtraukumi

Ja uzņēmumā ir fiksēts pārtraukuma laiks, piemēram, fiksēts pusdienu pārtraukuma laiks, pārtraukumu var definēt iepriekš laika profilā. Šajā gadījumā nodarbinātajam nav jāreģistrē pārtraukuma laiks darbu kartes lapās. Tā vietā pārtraukums tiek uzskaitīts automātiski, aprēķinot nodarbinātā reģistrācijas lapā **Apstiprināt**.

#### <a name="registered-breaks"></a>Reģistrētie pārtraukumi

Ja uzņēmums neizmanto plānotos pārtraukumus, nodarbinātie var reģistrēt pārtraukumus darbdienas laikā. Reģistrētos pārtraukumus var izmantot, piemēram, ja nodarbinātais strādā atbilstoši brīvā režīma profilam, kuram nav definētu ierašanās un aiziešanas laiku. Reģistrētie pārtraukumi ir netiešās aktivitātes tips. Nodarbinātais reģistrē pārtraukumu lapā **Darbu karšu terminālis** vai lapā **Darbu kartes ierīce**. Abās šajās lapās lietotājs var atlasīt pārtraukuma tipu iepriekš definētu pārtraukuma darbību sarakstā.

#### <a name="paid-and-unpaid-breaks"></a>Apmaksātie un neapmaksātie pārtraukumi

Pārtraukuma darbības var iestatīt kā **Apmaksāts** vai **Neapmaksāts**. Apmaksāts pārtraukums tiek iekļauts apmaksājamā laika aprēķinā, un sistēma izmanto apmaksas tipu, kas apmaksas līgumā ir definēts kā reģistrācijas tips **Pārtraukums**.

### <a name="example-of-a-planned-break"></a>Plānota pārtraukuma piemērs

Kā piemēru aplūkojiet tālāk norādīto laika profilu, kurā ir iekļauts neapmaksāts pusdienu pārtraukums.

| Profila tips  | Sākšana    | Beigt      | diena;     |
|---------------|----------|----------|---------|
| Virsstundas     | 00:00 | 06:00 | Pirmdienās  |
| Brīvais režīms +         | 06:00 | 07:00 | Pirmdienās  |
| Ierašanās laiks      | 07:00 | 07:00 | Pirmdienās  |
| Standarta laiks | 07:00 | 12:00 | Pirmdienās  |
| Pārtraukums         | 12:00 | 12:30 | Pirmdienās  |
| Standarta laiks | 12:30 | 14:30 | Pirmdienās  |
| Brīvais režīms-         | 14:30 | 15:30 | Pirmdienās  |
| Aiziešanas laiks     | 15:30 | 15:30 | Pirmdienās  |
| Virsstundas     | 15:30 | 06:00 | Otrdienās |

Tālāk ir attēlotas nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      |
|---------------------------|----------|----------|
| Ierašanās laiks                  | 06:30 | 06:30 |
| Ražošanas darbs            | 06:30 | 14:45 |
| Aiziešanas laiks                 | 17:00 | 17:00 |

Pēc žurnāla reģistrāciju aprēķināšanas lapā **Apstiprināt** varat apskatīt aprēķina rezultātu cilnē **Laiki**. Lai izprastu šo scenāriju, skatiet tālāk norādītos laukus.

| Brīvais režīms + | Brīvais režīms - | Laiks  | Apmaksājamais laiks | Neapmaksātais pārtraukuma laiks | Apmaksājamās virsstundas |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0.00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Sistēma aprēķināja 0,5 stundas neapmaksātā pārtraukuma laika, un šis laiks netiek iekļauts apmaksājamajā laikā.

### <a name="example-of-a-registered-break"></a>Reģistrēta pārtraukuma piemērs

Kā piemēru aplūkojiet tālāk norādīto laika profilu, kurā nav iekļauti plānotie pārtraukumi.

| Profila tips  | Sākšana    | Beigt      | diena;     |
|---------------|----------|----------|---------|
| Virsstundas     | 00:00 | 06:00 | Pirmdienās  |
| Brīvais režīms +         | 06:00 | 07:00 | Pirmdienās  |
| Ierašanās laiks      | 07:00 | 07:00 | Pirmdienās  |
| Standarta laiks | 07:00 | 14:30 | Pirmdienās  |
| Brīvais režīms-         | 14:30 | 15:30 | Pirmdienās  |
| Aiziešanas laiks     | 15:30 | 15:30 | Pirmdienās  |
| Virsstundas     | 15:30 | 06:00 | Otrdienās |

Tālāk ir attēlotas nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      |
|---------------------------|----------|----------|
| Ierašanās laiks                  | 06:30 | 06:30 |
| Ražošanas darbs            | 06:30 | 17:00 |
| Pārtraukums                     | 12:03 | 12:32 |
| Aiziešanas laiks                 | 17:00 | 17:00 |

Aprēķinot reģistrācijas, tiek aprēķināts aktivitāšu laiks.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      | Laiks  |
|---------------------------|----------|----------|-------|
| Ierašanās laiks                  | 06:30 | 06:30 |       |
| Ražošanas darbs            | 06:30 | 17:00 | 10,00 |
| Pārtraukums                     | 12:03 | 12:32 | 0,50  |
| Aiziešanas laiks                 | 17:00 | 17:00 |       |

> [!NOTE]
> Pārtraukuma laiks darbojas paralēli aktivitātes laikam (šajā piemērā — ražošanas darbam). Šī funkcionalitāte vienmēr tiek izmantota pārtraukuma aktivitātēm. Aprēķinot reģistrācijas, pārtraukuma laiks tiek atņemts no aktivitātes laika. Šajā gadījumā ražošanas darba ilgums ir 10,50 stundas, bet aprēķinātais laiks ir 10, jo no aktivitātes laika ir atņemts 0,5 stundu pārtraukuma laiks.

Pēc žurnāla reģistrāciju aprēķināšanas lapā **Apstiprināt** varat apskatīt aprēķina rezultātu cilnē **Laiki**. Lai izprastu šo scenāriju, skatiet tālāk norādītos laukus.

| Brīvais režīms + | Brīvais režīms - | Laiks  | Apmaksājamais laiks | Neapmaksātais pārtraukuma laiks | Apmaksājamās virsstundas |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0.00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Ja plānotais pārtraukums tiktu apmaksāts, aprēķina rezultāts būtu šāds.

| Brīvais režīms + | Brīvais režīms - | Laiks  | Apmaksājamais laiks | Apmaksātais pārtraukuma laiks | Apmaksājamās virsstundas |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0.00   | 10,50 | 10,00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Apmaksas elementi un apmaksātie pārtraukumi

Pārsūtot reģistrācijas lapā **Apstiprināt**, tiek ģenerēti apmaksas elementi. Apmaksātajiem pārtraukumiem tiek ģenerēts atsevišķs apmaksas elements.

Apmaksātā pārtraukuma apmaksas likmi nosaka apmaksas līgumos noteiktais pārtraukuma apmaksas tips. Apmaksas tipa izmantošanas vietā varat iestatīt izmaksu cenu stundā pārtraukumam noteiktā datumu intervālā.

Kā piemēru aplūkojiet tālāk norādīto laika profilu.

| Profila tips  | Sākšana    | Beigt      | diena;     |
|---------------|----------|----------|---------|
| Virsstundas     | 00:00 | 06:00 | Pirmdienās  |
| Brīvais režīms +         | 06:00 | 07:00 | Pirmdienās  |
| Ierašanās laiks      | 07:00 | 07:00 | Pirmdienās  |
| Standarta laiks | 07:00 | 14:30 | Pirmdienās  |
| Brīvais režīms-         | 14:30 | 15:30 | Pirmdienās  |
| Aiziešanas laiks     | 15:30 | 15:30 | Pirmdienās  |
| Virsstundas     | 15:30 | 06:00 | Otrdienās |

Tālāk ir attēlotas nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      | Laiks |
|---------------------------|----------|----------|------|
| Ierašanās laiks                  | 07:00 | 07:00 |      |
| Ražošanas darbs            | 07:00 | 15:00 | 7,5  |
| Pārtraukums (apmaksāts)              | 12:00 | 12:30 | 0,5  |
| Aiziešanas laiks                 | 15:00 | 15:00 |      |

Šajā piemērā standarta laikam ir iestatīts apmaksas tips **1201**, un apmaksas līgumā noteiktā apmaksas likme ir **10**. Apmaksātā pārtraukuma apmaksas tips ir **1301** un apmaksas likme ir **8**. Pārsūtot reģistrācijas, tiek ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 7,50      | 10   |
| Brīvais režīms-         | 1201     | 0,50      | 10   |
| Pārtraukums (apmaksāts)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Apmaksāto pārtraukumu izmaksu piešķiršana projektiem un ražošanas pasūtījumiem

Projektu aktivitātēm un ražošanas darbiem var iestatīt stundas izmaksu noteikšanu vai nu atbilstoši lapā Laiks un apmeklētība aprēķinātajām apmaksas likmēm, vai atbilstoši aktivitātēm definētajām izmaksu kategorijām.

Lai iestatītu izmaksu kategoriju, atlasiet **Ražošanas kontrole** &gt; **Iestatījumi** &gt; **Ražošanas izpilde** &gt; **Ražošanas pasūtījuma noklusējuma vērtības** un laukā **Izmaksu kategorijas** iestatiet **Jā** vai **Nē**.

- **Nē** — izmaksas tiek aprēķinātas atbilstoši lapā Laiks un apmeklētība definētajiem reģistrācijas tipiem.
- **Jā** — izmaksas tiek aprēķinātas atbilstoši ražošanas un projektu aktivitātēm definētajām izmaksu kategorijām.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Izmaksu aprēķināšana atbilstoši lapā Laiks un apmeklētība aprēķinātajām apmaksas likmēm

Tālāk norādītajā piemērā ir parādīta stundas izmaksu aprēķināšana, ja ir iestatīta izmaksu aprēķināšana atbilstoši apmaksas likmēm.

Ražošanas pasūtījumiem un projektiem izmantotā stundas izmaksu likme tiek aprēķināta pārsūtīšanas procesa laikā. Lai skatītu katras aktivitātes stundas likmi, atveriet kategorijas Laiks un apmeklētība lapu **Apstiprināt** un pēc tam atlasiet **Pieprasījumi** &gt; **Pārsūtītās reģistrācijas**. Katras reģistrācijas stundas izmaksu likmi jūs varat atrast cilnē **Izmaksu cenas**.

Kā piemēru aplūkojiet tālāk norādītās reģistrācijas, kurās ir izmantots tāds pats profils, kā iepriekšējā piemērā.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      | Laiks |
|---------------------------|----------|----------|------|
| Ierašanās laiks                  | 07:00 | 07:00 |      |
| Apstrāde (pasūtījums: 4711)     | 07:00 | 11:00 | 4.    |
| Apstrāde (pasūtījums: 4712)     | 11:00 | 15:00 | 3,50 |
| Pārtraukums (apmaksāts)              | 12:00 | 12:30 | 0,50 |
| Aiziešanas laiks                 | 15:00 | 15:00 |      |

Kad reģistrāciju pārsūtīšana ir pabeigta, tiek ģenerētas tālāk norādītās pārsūtītās reģistrācijas.

| Reģistrācijas tips     | Laiks | Izmaksu cena stundā |
|-----------------------|------|---------------------|
| Ierašanās              | 0.00 | 0.00                |
| Apstrāde (pasūtījums: 4711) | 4,00 | 10,00               |
| Apstrāde (pasūtījums: 4712) | 3,50 | 11,14               |
| Pārtraukums (apmaksāts)          | 0,50 | 0.00                |
| Aiziešanas laiks             | 0.00 | 0.00                |

Apmaksātā pārtraukuma izmaksu cenu stundā aprēķina atkarībā no tiešo algu izmaksu iestatījuma. Atlasiet **Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Laika un apmeklētības parametri**. Sadaļas **Tiešās algu izmaksas** cilnes **Izmaksu cena** laukā **Standarta laiks** varat atlasīt **Jā**, **Nē** vai **Sadalījums**.

- **Jā** — šī vērtība tiek izmantota iepriekšējā piemērā. Izmaksas tiek piešķirtas tai ražošanas vai projektu aktivitātei, kura darbojas vienlaicīgi ar apmaksātā pārtraukuma aktivitāti. Norādītajā piemērā šī aktivitāte ir pasūtījuma 4712 ražošanas darbs. Kā varat redzēt, apmaksātā pārtraukuma izmaksu cena stundā ir 0 (nulle), un tā ir piešķirta darbam, kas norisinās vienlaicīgi ar pārtraukumu.

    Apmaksātā pārtraukuma ilgums ir 0,5 stundas, un apmaksas likme ir 8. Tādējādi apmaksātā pārtraukuma kopējās izmaksas ir 4. Kopējās izmaksas pēc tam tiek piešķirtas 3,5 stundu ilgajam apstrādes darbam. Tādā veidā apmaksātā pārtraukuma veidotās izmaksas stundā ir 1,14 (4 ÷ 3,5 = 1,14).

- **Sadalījums** — apmaksātā pārtraukuma laiks tiek sadalīts vienādi pa dienā reģistrētajiem darbiem. Ja šī vērtība tiek izmantota iepriekšējā piemērā, tiek ģenerētas tālāk norādītās pārsūtītās reģistrācijas.

    | Reģistrācijas tips     | Laiks | Izmaksu cena stundā |
    |-----------------------|------|---------------------|
    | Ierašanās              | 0.00 | 0.00                |
    | Apstrāde (pasūtījums: 4711) | 4,00 | 10,53               |
    | Apstrāde (pasūtījums: 4712) | 3,50 | 10,53               |
    | Pārtraukums (apmaksāts)          | 0,50 | 0.00                |
    | Aiziešanas laiks             | 0.00 | 0.00                |

    Abu ražošanas darbu kopējais apstrādes laiks ir 7,5 stundas, un apmaksātā pārtraukuma kopējās izmaksas ir 4. Tāpēc pārtraukuma izmaksu aprēķināšanas rezultāts ir 0,53 (= 4 ÷ 7,5).

- **Nē** — apmaksātā pārtraukuma izmaksas nepalielina apstrādes aktivitāšu stundas izmaksas.

    | Reģistrācijas tips     | Laiks | Izmaksu cena stundā |
    |-----------------------|------|---------------------|
    | Ierašanās              | 0.00 | 0.00                |
    | Apstrāde (pasūtījums: 4711) | 4,00 | 10,00               |
    | Apstrāde (pasūtījums: 4712) | 3,50 | 10,00               |
    | Pārtraukums (apmaksāts)          | 0,50 | 0.00                |
    | Aiziešanas laiks             | 0.00 | 0.00                |

## <a name="absence"></a>Kavējumi

Kavējuma kodu izmanto, lai reģistrētu nodarbinātā kavējuma periodu. Kavējuma kods tāpat kā pārtraukumi un pārslēgšanās kodi ir netiešās aktivitātes tips. Kavējuma laiks var būt plānots vai reģistrēts, un kavējums var būt atļauts vai neatļauts. Atļauta kavējuma piemēri ir ārsta apmeklējums, seminārs vai piedalīšanās zvērināto tiesā. Neatļauts kavējums ir kavējums bez pamatota iemesla, piemēram, ierašanās darbā vēlu. Parasti par atļautajiem kavējumiem netiek samazināta nodarbinātā apmaksa, taču par neatļautajiem kavējumiem nodarbinātā apmaksa tiek samazināta.

### <a name="planned-absence"></a>Plānotā prombūtne

Plānoto kavējumu nodarbinātajiem varat izveidot lapā **Izveidot plānoto kavējumu** (**Laiks un apmeklētība** &gt; **Izveidot plānoto kavējumu**). Šajā lapā plānotais kavējums tiek reģistrēts kā kavējuma darbs norādītā datuma un laika intervālā.

Darba pamatā ir vaicājums. Tāpēc plānoto kavējumu varat izveidot vairākiem nodarbinātajiem, piemēram, nodarbinātajiem, kuri pieder vienai aprēķinu grupai. Ja plānotais kavējums ir paredzēts vienam nodarbinātajam, reģistrācijas var ievadīt vai nu lapā **Apmeklētība** vai lapā **Laika reģistrācijas nodarbinātie**.

- Lai ievadītu kavējuma reģistrāciju lapā **Apmeklētība**, atlasiet **Laiks un apmeklētība** &gt; **Pieprasījumi un pārskati** &gt; **Apmeklētība** &gt; **Apmeklētība** un pēc tam atlasiet **Kavējuma reģistrācija**.
- Lai ievadītu kavējuma reģistrāciju lapā *<strong><em>Laika reģistrācijas nodarbinātie</em></strong>*, atlasiet <strong>Laiks un apmeklētība</strong> &gt; <strong>Iestatījumi</strong> &gt; <strong>Laika reģistrācijas nodarbinātie</strong> un pēc tam sadaļas <strong>Laika piešķire</strong> cilnē <strong>Laiks</strong> atlasiet <strong>Kavējumu reģistrācijas</strong>.

Varat izmantot pārskatu **Plānotie kavējumi**, lai skatītu apskatu par nodarbināto plānotajiem kavējumiem. Lai atvērtu šo pārskatu, atlasiet **Laiks un apmeklētība** &gt; **Pieprasījumi un pārskati** &gt; **Kavējumu pārskati** &gt; **Plānotie kavējumi**.

### <a name="registered-absence"></a>Reģistrētie kavējumi

Parasti nodarbinātie tiek uzskatīti par darbā neesošiem, ja viņi nav darbā jebkurā periodā starp plānoto ierašanās laiku un plānoto aiziešanas laiku. Ja nodarbinātie reģistrē ierašanās laiku vēlāk, nekā plānots, vai reģistrē aiziešanas laiku agrāk, nekā plānots, viņiem tiek piedāvāts atlasīt kavējuma kodu, kas norāda kavējuma iemeslu. Var iestatīt, lai kavējuma kods būtu izmantojams reģistrēšanai. Tikai atbilstošie kodi būs pieejami atlasei sarakstā.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Scenāriji, kuru pamatā ir dažādas darba stundu reģistrāciju kombinācijas

Tālāk aprakstītajos scenārijos ir parādīti apmaksas elementi un apstiprināmie ieraksti, kas tiek ģenerēti nodarbinātajiem atbilstoši viņu veiktajām reģistrācijām. Visi scenāriji ir veidoti atbilstoši tālāk norādītajam laika profilam.

| Profila tips  | Sākšana    | Beigt      | diena;     |
|---------------|----------|----------|---------|
| Virsstundas     | 00:00 | 06:00 | Pirmdienās  |
| Brīvais režīms +         | 06:00 | 07:00 | Pirmdienās  |
| Ierašanās laiks      | 07:00 | 07:00 | Pirmdienās  |
| Standarta laiks | 07:00 | 14:30 | Pirmdienās  |
| Brīvais režīms-         | 14:30 | 15:30 | Pirmdienās  |
| Aiziešanas laiks     | 15:30 | 15:30 | Pirmdienās  |
| Virsstundas     | 15:30 | 06:00 | Otrdienās |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>1. scenārijs: nodarbinātais reģistrē ierašanās laiku vēlāk, nekā plānots

Nodarbinātais reģistrē ierašanās laiku plkst. 08:30. Tā kā viņa plānotais ierašanās laiks ir plkst. 07:00, viņš kavē darbu 1,50 stundas. Tā kā 1,50 stundas tiek uzskatītas par kavējuma laiku, nodarbinātajam tiek piedāvāts atlasīt kavējuma kodu. Nodarbinātais aiziet no darba plkst. 15:30, kas ir plānotais aiziešanas laiks. Kad nodarbinātā reģistrācijas tiek aprēķinātas un apstiprinātas, kavējuma reģistrācija, kā arī nodarbinātā kopā ar ierašanās laika reģistrāciju atlasītais kavējuma kods parādās laika periodam no plkst. 07:00 līdz plkst. 08:30.

Laika profilā var konfigurēt reģistrācijas tipu **Ierašanās**, lai ļautu nodarbinātajiem reģistrēt ierašanās laiku nedaudz vēlāk. Piemēram, ja iestatāt 5 minūšu kavējuma toleranci, nodarbinātais tiks aicināts atlasīt kavējuma kodu tikai tad, ja viņš ieradīsies vēlāk par 07:05.

Tā kā šajā gadījumā nodarbinātā kavējumam nav pamatota iemesla, viņš atlasa kavējuma kodu, kas atbilst neatļautam kavējumam. Kavējuma kods tiek uzskatīts par atbilstošu neatļautam kavējumam, ja kavējuma kodam atbilstošajai kavējumu grupai ir iespējots virsstundu skaita samazinājuma iestatījums. Lai iestatītu šo iestatījumu, atlasiet **Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Grupas** &gt; **Kavējumu grupas** un pēc tam atzīmējiet izvēles rūtiņu **Samazināt virsstundu skaitu**.

Tālāk ir aprakstīts, kā pēc aprēķināšanas lapā **Apstiprināt** parādās nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips         | Sākšana    | Beigt      | Laiks |
|-----------------------------------|----------|----------|------|
| Kavējums (neatļauts — ierašanās darbā vēlu) | 07:00 | 08:30 | 1.5  |
| Ierašanās laiks                          | 08:30 | 08:30 |      |
| Ražošanas darbs                    | 07:30 | 15:30 | 7.0  |
| Aiziešanas laiks                         | 15:30 | 15:30 |      |

Tālāk ir norādīts pēc reģistrāciju pārsūtīšanas iegūtais apmaksas elements.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 7,00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>2. scenārijs: nodarbinātais aiziet no darba pirms plānotā aiziešanas laika standarta laika periodā

Nodarbinātais reģistrē ierašanās laiku plkst. 7:00 un aiziešanas laiku reģistrē agri, plkst. 13:00. Tā kā plkst. 13:00 ir pirms plānotā aiziešanas laika plkst. 15:30, un plkst. 13:00 ir standarta laika periodā, nodarbinātais tiek aicināts atlasīt kavējuma kodu. Nodarbinieks atlasa kavējuma kodu, kas atbilst ārsta apmeklējumam un ir definēts kā atļauts kavējums. Atļautā kavējuma apmaksas likme ir definēta apmaksas līgumos — reģistrācijas tipam **Kavējumi** (**Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Alga** &gt; **Apmaksas līgumi**).

Tālāk ir aprakstīts, kā pēc aprēķināšanas lapā **Apstiprināt** parādās nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips              | Sākšana    | Beigt      | Laiks |
|----------------------------------------|----------|----------|------|
| Ierašanās laiks                               | 07:00 | 07:00 |      |
| Ražošanas darbs                         | 07:00 | 13:00 | 4,0  |
| Aiziešanas laiks                              | 13:00 | 13:00 |      |
| Kavējums (atļauts — ārsta apmeklējums) | 13:00 | 15:30 | 3.5  |

Tālāk ir norādīts pēc reģistrāciju pārsūtīšanas iegūtais apmaksas elements.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>3. scenārijs: nodarbinātais aiziet no darba pirms plānotā aiziešanas laika brīvā režīma - periodā

Nodarbinātais reģistrē ierašanās laiku plkst. 07:00 un aiziešanas laiku plkst. 14:15, kas ir plānotajā brīvā režīma - periodā. Laiks starp faktisko aiziešanas laiku un plānoto aiziešanas laiku netiek uzskatīts par kavējumu, un nodarbinātais netiek aicināts atlasīt kavējuma kodu. Summa tiek atskaitīta no nodarbinātā brīvā režīma bilances, un nodarbinātajam tiek piešķirta apmaksa par atlikušo brīvā režīma - periodu — no plkst. 14:15 līdz plkst. 15:30.

Tālāk ir aprakstīts, kā pēc aprēķināšanas lapā **Apstiprināt** parādās nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      | Laiks |
|---------------------------|----------|----------|------|
| Ierašanās laiks                  | 07:00 | 07:00 |      |
| Ražošanas darbs            | 07:00 | 14:15 | 7,25 |
| Aiziešanas laiks                 | 14:15 | 14:15 |      |

Tālāk ir norādīts pēc reģistrāciju pārsūtīšanas iegūtais apmaksas elements.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>4. scenārijs: nodarbinātais ierodas darbā vēlu un aiziet no darba pēc plānotā aiziešanas laika virsstundu periodā

Nodarbinātais reģistrē ierašanās laiku vēlu, plkst. 09:30, un, lai kompensētu vēlo ierašanos, viņš turpina strādāt virsstundu periodā un reģistrē aiziešanas laiku plkst. 17:00. Tā kā nodarbinātais ieradās darbā vēlu un savu vēlo ierašanos kompensēja, strādājot ilgāk, uzņēmums nevēlas nodarbinātajam piešķirt apmaksu par virsstundām, kuras nodarbinātais ir pavadījis darbā starp plānoto aiziešanas laiku plkst. 15:30 un faktisko aiziešanas laiku plkst. 17:00, pat ja šis periods laika profilā ir definēts kā virsstundas.

Šajā scenārijā var iestatīt kavējuma kodu virsstundu samazināšanai atbilstoši jebkura neatļauta kavējuma laikam, kas darbiniekam ir reģistrēts tajā pašā dienā. Lai samazinātu virsstundu skaitu atbilstoši neatļauta kavējuma laikam, atlasiet **Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Grupas** &gt; **Kavējumu grupas** un atzīmējiet izvēles rūtiņu **Samazināt virsstundu skaitu**.

Tālāk ir aprakstīts, kā pēc aprēķināšanas lapā **Apstiprināt** parādās nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips         | Sākšana    | Beigt      | Laiks |
|-----------------------------------|----------|----------|------|
| Kavējums (neatļauts — ierašanās darbā vēlu) | 07:00 | 09:30 | 1.5  |
| Ierašanās laiks                          | 09:30 | 09:30 |      |
| Ražošanas darbs                    | 09:30 | 17:00 | 7,5  |
| Aiziešanas laiks                         | 17:30 | 17:30 |      |

Ja atlasītajam kavējuma kodam ir atzīmēta izvēles rūtiņa **Samazināt virsstundu skaitu**, apmaksa par virsstundām tiek samazināta atbilstoši nodarbinātā reģistrētajam neatļautā kavējuma laikam. Šajā gadījumā pēc reģistrāciju pārsūtīšanas tiek ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 9,00      | 10   |
| Virsstundas      | 1301     | 0,5       | 15.   |

Šajā piemērā 1,5 stundu neatļautais kavējums, no plkst. 07:00 līdz plkst. 09:30, tiek atņemts no 2,0 stundu virsstundu skaita, no plkst. 15:30 līdz plkst. 17:30. Reģistrācijas aprēķināšanas rezultāts ir 1,5 stundu standarta laiks un 0,5 stundu virsstundas.

Turpretim, ja izvēles rūtiņa **Samazināt virsstundu skaitu** atlasītajam kavējuma kodam nav atzīmēta, nodarbinātajam tiek piešķirta apmaksa par virsstundām, pat ja nodarbinātais ir ieradies darbā vēlu un šis kavējums ir reģistrēts kā neatļauts kavējums. Šajā gadījumā pēc reģistrāciju pārsūtīšanas tiek ģenerēti tālāk norādītie apmaksas elementi.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 7,50      | 10   |
| Virsstundas      | 1301     | 2,0       | 15.   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>5. scenārijs: nodarbinātais aiziet no darba pirms plānotā aiziešanas laika un var pārveidot kavējuma periodu par brīvā režīma - periodu.

Tālāk norādītajā piemērā ir parādīts, kā var samazināt nodarbinātā brīvā režīma bilanci, pārveidojot kavējuma periodu par brīvā režīma - periodu.

Nodarbinātais reģistrē ierašanās laiku plkst. 07:00 un reģistrē aiziešanas laiku plkst. 13:00 Nodarbinātais ir noslēdzis vienošanos ar vadītāju, ka piektdienās drīkst doties mājās agrāk, ja šīs stundas tiek atņemtas no nodarbinātā brīvā režīma bilances. Kad nodarbinātais reģistrē aiziešanas laiku plkst. 13:00, nodarbinātais tiek aicināts atlasīt kavējuma kodu, jo atlikušās darbdienas daļas kavējuma periods nav plānotajā brīvā režīma - periodā. Lai pārveidotu atlikušo darbdienas daļu par brīvā režīma - periodu, nodarbinātais var atlasīt kavējuma kodu, kas ir iestatīts nodarbinātā brīvā režīma bilances samazināšanai.

Lai samazinātu brīvā režīma stundu bilanci nodarbinātajiem, kuri reģistrē kavējumu darbdienā, atlasiet **Laiks un apmeklētība** &gt; **Iestatījumi** &gt; **Grupas** &gt; **Kavējumu grupas** un atzīmējiet izvēles rūtiņu **Samazināt brīvo režīmu**.

Tālāk ir aprakstīts, kā pirms aprēķināšanas lapā **Apstiprināt** parādās nodarbinātā dienas laikā veiktās reģistrācijas.

| Žurnāla reģistrācijas tips | Sākšana    | Beigt      | Laiks |
|---------------------------|----------|----------|------|
| Ierašanās laiks                  | 07:00 | 07:00 |      |
| Ražošanas darbs            | 07:00 | 13:00 | 6,0  |
| Aiziešanas laiks                 | 13:00 | 13:00 |      |

Ja nodarbinātais atzīmē neatļautam kavējumam atbilstošu kavējuma kodu, pēc reģistrācijas pārsūtīšanas iegūtais apmaksas elements izskatīsies, kā norādīts tālāk.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 6,00      | 10   |

Ja nodarbinātais atzīmē atļautam kavējumam atbilstošu kavējuma kodu un šis kavējuma kods ir iestatīts brīvā režīma bilances samazināšanai, pēc reģistrāciju pārsūtīšanas iegūtaie apmaksas elementi izskatīsies, kā norādīts tālāk.

| Algas tips     | Apmaksas tips | Apmaksas vienības | Norma |
|---------------|----------|-----------|------|
| Standarta laiks | 1201     | 8,50      | 10   |

Šajā gadījumā nodarbinātā brīvā režīma bilance tiek samazināta atbilstoši laikam starp faktisko aiziešanas laiku un plānoto aiziešanas laiku (t. i., 2,5 stundas, no plkst. 13:00 līdz plkst. 15:30).

> [!NOTE]
> Nav ieteicams kavējuma kodam atlasīt abas izvēles rūtiņas **Samazināt brīvo režīmu** un **Samazināt virsstundu skaitu**, jo šie iestatījumi atņems neatļautā kavējuma stundu skaitu no nodarbinātā virsstundu skaita un vienlaikus samazinās nodarbinātā brīvā režīma bilanci.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>6. scenārijs: nodarbinātajam darbdienā nav reģistrēts neviens plānotais kavējums un nav reģistrēta apmeklētība

Ja nodarbinātais darbdienā neierodas darbā un šim nodarbinātajam nav neviena plānotā kavējuma šajā dienā, nodarbinātā reģistrāciju aprēķināšanai tiek izmantots noklusējuma kavējuma kods. Lai definētu noklusējuma kavējuma kodus, atlasiet **Laiks un apmeklētība** &gt; **Laika un apmeklētības parametri**. Pēc tam varat atlasīt kavējuma kodu šādos laukos:

- Automātiski ievietot brīvo režīmu -
- Automātiski ievietot kavējumu

Aprēķinot ikdienas reģistrācijas nodarbinātajam, kuram ir iespējots brīvā režīma laiks, kā noklusējuma kavējuma kods tiek izmantots laukā **Automātiski ievietot brīvo režīmu -** norādītais kavējuma kods. Ja nodarbinātajam nav iespējots brīvā režīma laiks, tiek izmantots laukā **Automātiski ievietot kavējumu** norādītais kavējuma kods. Ja uzņēmumā ir gan tādi nodarbinātie, kuriem ir iespējots brīvā režīma laiks, gan tādi nodarbinātie, kuriem nav iespējots brīvā režīma laiks, ir jāiestata abi parametri.

