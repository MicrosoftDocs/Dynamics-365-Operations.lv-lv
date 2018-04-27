---
title: "Partijas līdzsvarošana"
description: "Šajā tēmā ir aprakstīts partijas līdzsvarošanas process."
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7d00df6263530ba9fff4c246cb3593cd607f6719
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="batch-balancing"></a>Partijas līdzsvarošana

[!INCLUDE [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā tiek nodrošināts partijas līdzsvarošanas process. 

Noskatieties [video par partijas līdzsvarošanu programmā Microsoft Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

Partijas līdzsvarošanas procesā tiek aprēķināts ražošanas partijā izmantojamais sastāvdaļu daudzums, izmantojot atlasītajā preču partijā aktīvo sastāvdaļu koncentrāciju.

<a name="products-that-have-an-active-ingredient"></a>Preces, kam ir aktīvā sastāvdaļa
---------------------------------------

Preces var definēt pēc to aktīvās sastāvdaļas koncentrācijas. Produkta aktīvā sastāvdaļa tiek veidota, izmantojot precei raksturīgu partijas atribūtu, kam ir minimālā vērtība, maksimālā vērtība un mērķa līmenis.

Partijas atribūta mērķa līmenis atspoguļo aktīvās sastāvdaļas procentuālo daudzumu precē. Minimālās un maksimālās vērtības atspoguļo pieņemto novirzi no mērķa līmeņa. To var izmantot, piemēram, kā apstiprināto toleranci pakešuzdevumos ieejas plūsmā.

Precei var būt tikai viena aktīvā sastāvdaļa. Lai norādītu preces aktīvo sastāvdaļu, vispirms ir jādefinē preces partijas atribūts. Pēc tam saistiet atribūtu kā preces pamata atribūtu.

Preču līmenī jānorāda arī tas, kā partijas preces aktīvā sastāvdaļa ir jāreģistrē: kā daļa no pirkšanas ieejas plūsmas procesa vai kā daļa no kvalitātes pārbaudes pasūtījuma procesa.

Lai pamata atribūtu saistītu ar preci, jāveic tālāk norādītā iestatīšana.

-   Precei jābūt partijas kontrolētai. Lai preci izveidotu kā partijas kontrolētu, ir precei jāpiešķir izsekošanas dimensiju grupa, kam ir aktīva partijas dimensija.

-   Atribūts, kas norāda sastāvdaļas līmeņus, precei ir jādefinē kā preces partijas atribūts.

Partijas aktīvās sastāvdaļas faktisko vērtību var pārlūkot un rediģēt lapā **Krājuma partijas atribūti**. 

-  Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Izsekošanas dimensijas** \> **Partijas** \> **Krājuma partijas atribūti**.

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Sastāvdaļas veidi un tas, kā tās mijiedarbojas partijas līdzsvarošanas procesā
---------------------------------------------------------------------

Izveidotajā formulas rindā var būt viena no šādām sastāvdaļām:

-   Neviens

-   Aktīva

-   Kompensēšana

-   Aizpildīja

Šīs sadaļas turpinājumā ir sniegti piemēri par to, kā darbojas katras sastāvdaļas veids. Piemēros ir izmantota formula, kur kopējais partijas lielums ir 100 litri.

| **Sastāvdaļas tips** | **Krājums** | **Formulas rindas daudzums** | **Vienība** |
|---------------------|-----------------|---------------------------|----------|
| Neviens                | A               | 20.                        | Litri    |
| Aktīva              | M               | 30                        | Litri    |
| Kompensēšana        | U               | 10                        | Litri    |
| Aizpildīja              | D               | 40                        | Litri    |

### <a name="active"></a>Aktīva

Kad formulas rindai tiek pievienota prece, kurai ir pamata atribūts, tā tiek nosaukta par formulas *aktīvo sastāvdaļu*. Partijas pasūtījumus, kuriem ir formulas, kas ietver aktīvās sastāvdaļas, var izmantot partijas līdzsvarošanas procesā. Katrai formulas sastāvdaļai partijas līdzsvarošanas procesā tiek aprēķināts daudzums, kas ir nepieciešams, lai saražotu preci. Aprēķinātais daudzums ir balstīts uz aktīvo sastāvdaļu koncentrāciju atlasītajās partijās.

**Piemērs**

Sastāvdaļai B ir pamata atribūts X un mērķa līmenis 30, un tā ir iekļauta formulā, kas pieprasa 30 litrus sastāvdaļas B uz katriem 100 preces litriem. Tiek izveidots partijas pasūtījums, kam partijas lielums ir 100 litri. Partijas pasūtījums tiek sākts, un partijas līdzsvarošanas procesa laikā lietotājs atlasa sastāvdaļas B partiju ar satura līmeni 35. Satura līmeņa vērtība 35 ir augstāka par mērķa līmeņa vērtību 30, tādēļ sastāvdaļas B līdzsvarotais daudzums tiek samazināts, izmantojot satura vērtību attiecību pret partijas mērķa līmeni, kas tiek reizināts ar aprēķināto daudzumu. Līdzsvarotā daudzuma aprēķins izskatās šādi:

(30 ÷ 35) x 30 litri = 25,71 litrs

| **Krājums** | **Sastāvdaļas tips** | **Prognozētais daudzums** | **Līdzsvarotais daudzums** | **Aktīvais daudzums** | **Vienība** | **Bāzes vērtība** |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| A               | Neviens                | 20.                     | 20.                    |                     | Litri    |                |
| M               | Aktīva              | 30                     | 25,71                 | 9,00                | Litri    | 30,00          |
| U               | Kompensēšana        | 10                     | 14,72                 |                     | Litri    |                |
| D               | Aizpildīja              | 40                     | 39,57                 |                     | Litri    |                |

### <a name="none"></a>Neviens

Izmantojot partijas līdzsvarošanas procesu, ja sastāvdaļas veids ir **Nav**, partijas pasūtījuma formulas rindā aprēķinātais un līdzsvarotais daudzums ir vienādi.

**Piemērs**

Sastāvdaļa A tiek piešķirta sastāvdaļai ar veidu **Nav** un pievienota pabeigtās preces formulai. Formula pieprasa 10 litrus sastāvdaļas A uz katriem 100 pabeigtās preces litriem. Ja partijas pasūtījumam nepieciešami 200 litri, sastāvdaļas aprēķinātais un līdzsvarotais daudzums tiek aprēķināts kā 20 litri.

### <a name="compensating"></a>Kompensēšana

Kompensējošā sastāvdaļa var nobīdīt vai papildināt preci aktīvās sastāvdaļas efektu. Tāpēc patērētais kompensējošās sastāvdaļas daudzums ir atkarīgs no produkta satura.

-   **Pretējs efekts** — ja aktīvā sastāvdaļas daudzums ir lielāks nekā gaidīts, ir jāpievieno mazāk kompensējošās sastāvdaļas.

-   **Papildinošs efekts** — ja aktīvā sastāvdaļas daudzums ir mazāks nekā gaidīts, ir jāpievieno vairāk kompensējošās sastāvdaļas.

Aktīvās sastāvdaļas un papildu sastāvdaļas relācija tiek iestatīta lapā **Kompensācijas princips**.

Lai iestatītu sastāvdaļu relācijas, izpildiet tālāk minētās darbības.

1.  Atlasiet **Preču informācijas pārvaldība** \> **Rēķini, materiāli un formulas** \> **Formulas**, atveriet formulas rindu un pēc tam atlasiet **Sastāvdaļas**, lai atvērtu lapu **Kompensācijas princips**.

2.  Atlasiet rindas, kas atspoguļo kompensācijas principu un pēc tam atlasiet kompensējamo aktīvo sastāvdaļu.

>   Kompensācijas principā jāievada arī pozitīvs vai negatīvs kompensācijas koeficients, kas norāda to, cik daudz jākompensē un vai principam jābūt pretējam vai papildu. Pozitīvs koeficients norāda papildu efektu un negatīvs koeficients norāda pretēju efektu.

**Piemērs**

Sastāvdaļa B ir aktīvā sastāvdaļa ar pamata atribūtu X un mērķa līmeni 30. Tā ir iekļauta formulā, kas pieprasa 30 litrus sastāvdaļas B uz katriem 100 preces litriem. Sastāvdaļa C ir kompensējošā sastāvdaļa, un daudzums 10 ir iekļauts tajā pašā formulā. Kompensācijas faktors 1,10 ir iestatīts kompensācijas principam. Tāpēc kompensējošās sastāvdaļas līdzsvarotais daudzums tiks samazināts par starpību starp aktīvās sastāvdaļas līdzsvaroto daudzumu un aprēķināto nepieciešamo daudzumu, kas reizināts ar 1,10.

Piemērā ar sastāvdaļas veidu **Aktīva** nepieciešamās aktīvās sastāvdaļas līdzsvarotais daudzums tika aprēķināts kā 25,71, un nepieciešamais daudzums tika aprēķināts kā 30. Šajā gadījumā kompensējošās sastāvdaļas līdzsvarotais daudzums tiks aprēķināts šādi:

1.  Starpība starp aprēķināto un līdzsvaroto daudzumu tiek noteikta šādi:

>   25,71 – 30 = 4,29

2.  Rezultāts tiek reizināts ar kompensācijas faktoru:

>   4,29 × 1,10 = –4,72

3.  No aprēķinātā kompensējošā daudzuma tiek atņemta vērtība –4,72, lai noteiktu līdzsvaroto kompensējošo daudzumu:

>   10 –(– 4,72) = 14,72

Tā kā 1,10 ir pozitīvs kompensācijas faktors, šim kompensācijas principam ir papildinošs efekts. Šajā gadījumā aktīvā sastāvdaļa ir vairāk līdzsvarojoša, nekā gaidīts. Tādēļ ir vajadzīgs vairāk kompensējošās sastāvdaļas.

### <a name="filler"></a>Aizpildīja

*Palīgviela* ir neitrāla sastāvdaļa, kas tiek izmantota, lai sasniegtu vēlamo pabeigtās preces izejas daudzumu. Palīgvielas daudzumu korekcijas tiek aprēķinātas, pamatojoties uz aktīvās sastāvdaļas un kompensējošās sastāvdaļas variācijām, salīdzinot ar standarta daudzumu.

**Piemērs**

Tika aprēķināta prece, kas ietver sastāvdaļas A, B, C un D formulas lielumam 100 litri. Tika aprēķināts visu sastāvdaļu veidu līdzsvarotais daudzums, izņemot sastāvdaļas veidam **Palīgviela**, kas tiek izmantota vienā rindā.
Palīgvielas līdzsvarotais daudzums tiek aprēķināts kā starpība starp partijas lieluma 100 litriem un sastāvdaļas A, B un C summa:

100 – (20 + 25,71 + 14,72) = 39,57

<a name="the-batch-balancing-process"></a>Partijas līdzsvarošanas process
---------------------------

Partijas līdzsvarošanas process tiek veikts no lapas **Partijas līdzsvarošana**.
Atlasiet **Izmaksu pārvaldība** \> **Partijas pasūtījumi** un pēc tam cilnē **Process** atlasiet **Partijas līdzsvarošana**. Funkcija Partijas līdzsvarošana ir pieejama partijas pasūtījumiem ar statusu **Sākts**.

Kopumā partijas līdzsvarošanu var lietot partijas pasūtījumiem, ja formulā ir vismaz viena formulas rinda, kur sastāvdaļas veids ir **Aktīva**. (Šīs kārtulas izņēmumu skatiet tālāk šīs tēmas sadaļā “Partijas pasūtījumi, kas nav piemērojami partijas līdzsvarošanai”).

Partijas līdzsvarošanas procesu var sadalīt divos apakšprocesos:

1.  Bilances partijas sastāvdaļas

2.  Formulas apstiprināšana un izdošana

### <a name="balance-batch-ingredients"></a>Bilances partijas sastāvdaļas

Apakšprocesā Bilances partijas sastāvdaļas tiek aprēķināts ražošanas partijā izmantojamais sastāvdaļu daudzums, ņemot vērā atlasītās preču partijas ar aktīvo sastāvdaļu. Aprēķinu var veikt tikai tad, ja ir pilns visu sastāvdaļu segums. Nevar līdzsvarot tikai partijas daļu, kam partijas pasūtījums ir iestatīts ražošanai.

[!NOTE]
Nevar saglabāt aprēķinu un pēc tam veikt partijas līdzsvarošanas procesu vēlāk. Ja aizverat lapu **Partijas līdzsvarošana**, lai pabeigtu procesu, aprēķins ir jāatkārto.

### <a name="confirm-and-release-the-formula"></a>Formulas apstiprināšana un izdošana

Kad sastāvdaļas daudzumi ir aprēķināti, varat apstiprināt un izdot formulu. Izdošanas process atšķiras atkarībā no tā, vai preces ir iespējotas noliktavas pārvaldības procesiem:

-   ja prece ir iespējota noliktavas pārvaldības procesiem, formulas rinda tiek izdota noliktavai saskaņā ar noliktavas pārvaldības procesu principiem. Formulas rinda tiek izdota ar daudzumiem, kas atbilst līdzsvarotajiem daudzumiem, un tiek izdota konkrētām partijām, kas ir atlasītas aktīvajām sastāvdaļām.

> [!NOTE]
>   Formulas rindas var izdot noliktavai tikai kā daļu no līdzsvarošanas procesa partijas. Lai gan materiālu izdošanai ražošanai uz noliktavu ir pieejamas citas opcijas, šīs opcijas nevar izmantot formulas rindām.

-   Ja prece nav iespējota noliktavas pārvaldības procesiem, ražošanas izdošanas saraksts tiek izveidots precei tikai tad, kad formula tiek apstiprināta un atbrīvota.

Vienā formulā varat kombinēt preces, kas ir iespējotas noliktavas pārvaldības procesiem, un preces, kas nav iespējotas noliktavas pārvaldības procesiem. Ja divu veidu preces ir iekļautas vienā formulā, uz noliktavu tiek izdotas preces, kas ir iespējotas noliktavas pārvaldības procesiem. Ja prece nav iespējota noliktavas pārvaldības procesiem, izdošanas saraksts tiek izveidots tikai tad, kad formula tiek apstiprināta un izdota.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Partijas pasūtījumi, kas nav lietojami partijas līdzsvarošanā

Ir viens kārtulas izņēmums: partijas līdzsvarošanai var lietot partijas pasūtījumus, ja formulā ir vismaz viena formulas rinda, kur sastāvdaļas veids ir **Aktīva**.

Ja formulā ir aktīvā sastāvdaļa precei, kas ir iespējota noliktavas pārvaldības procesiem, bet partijas numurs ir rezervāciju hierarhijā zemāks par vērtību Atrašanās vieta, partijas pasūtījums nav lietojams partijas līdzsvarošanā.

Partijas pasūtījums, kas nav lietojams par partijas līdzsvarošanā, tiek pakļauts parastajam partijas pasūtījumu procesa ciklam.

