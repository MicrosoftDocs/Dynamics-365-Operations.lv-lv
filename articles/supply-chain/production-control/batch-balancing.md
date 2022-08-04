---
title: Partijas līdzsvarošana
description: Šajā rakstā ir aprakstīts partijas līdzsvarošanas process.
author: johanhoffmann
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 939066fbf4ab7b316283d406c321f1a7936c187f
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066552"
---
# <a name="batch-balancing"></a>Partijas līdzsvarošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā tiek atbalstīts partijas līdzsvarošanas process.

Lai iegūtu papildu informāciju, noskatieties [videoklipu par partijas līdzsvarošanu](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

Partijas līdzsvarošanas procesā tiek aprēķināts ražošanas partijā izmantojamais sastāvdaļu daudzums, izmantojot atlasītajā preču partijā aktīvo sastāvdaļu koncentrāciju.

## <a name="products-that-have-an-active-ingredient"></a>Preces, kam ir aktīvā sastāvdaļa

Preces var definēt pēc to aktīvās sastāvdaļas koncentrācijas. Produkta aktīvā sastāvdaļa tiek veidota, izmantojot precei raksturīgu partijas atribūtu, kam ir minimālā vērtība, maksimālā vērtība un mērķa līmenis.

Partijas atribūta mērķa līmenis atspoguļo aktīvās sastāvdaļas procentuālo daudzumu precē. Minimālās un maksimālās vērtības atspoguļo pieņemto novirzi no mērķa līmeņa. To var izmantot, piemēram, kā apstiprināto toleranci pakešuzdevumos ieejas plūsmā.

Precei var būt tikai viena aktīvā sastāvdaļa. Lai norādītu preces aktīvo sastāvdaļu, vispirms ir jādefinē preces partijas atribūts. Pēc tam saistiet atribūtu kā preces pamata atribūtu.

Preču līmenī jānorāda arī tas, kā partijas preces aktīvā sastāvdaļa ir jāreģistrē: kā daļa no pirkšanas ieejas plūsmas procesa vai kā daļa no kvalitātes pārbaudes pasūtījuma procesa.

Lai pamata atribūtu saistītu ar preci, jāveic tālāk norādītā iestatīšana.

- Precei jābūt partijas kontrolētai. Lai preci izveidotu kā partijas kontrolētu, ir precei jāpiešķir izsekošanas dimensiju grupa, kam ir aktīva partijas dimensija.

- Atribūts, kas norāda sastāvdaļas līmeņus, precei ir jādefinē kā preces partijas atribūts.

Lai iegūtu un rediģētu partijas aktīvo sastāvdaļu faktisko vērtību:
1. Pārejiet uz sadaļu **Krājumu pārvaldība \> Pieprasījumi un pārskati \> Izsekošanas dimensijas \> Krājuma izsekošana**.
1. Atlasiet partijas numuru no režģa.
1. Darbību rūtī atveriet cilni **Skats** un pēc tam atlasiet **Krājumu partijas atribūti**.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Sastāvdaļas veidi un tas, kā tās mijiedarbojas partijas līdzsvarošanas procesā

Izveidotajā formulas rindā var būt viena no šādām sastāvdaļām:

- Neviena
- Aktīva
- Kompensēšana
- Aizpildīja

Šīs sadaļas turpinājumā ir sniegti piemēri par to, kā darbojas katras sastāvdaļas veids. Piemēros ir izmantota formula, kur kopējais partijas lielums ir 100 litri.

| Sastāvdaļas tips | Krājuma numurs | Formulas rindas daudzums | Vienība |
|---|---|---|---|
| Neviena | A | 20. | Litri |
| Aktīvie | B | 30 | Litri |
| Kompensēšana | C | 10. | Litri |
| Aizpildīja | D | 40 | Litri |

Tabulā ir sniegts katra piemēra rezultātu pārskats.

| Krājuma numurs | Sastāvdaļas tips | Prognozētais daudzums | Līdzsvarotais daudzums | Aktīvais daudzums | Vienība | Bāzes vērtība |
|---|---|---|---|---|---|---|
| A | Neviena | 20. | 20. | | Litri | |
| B | Aktīva | 30 | 25,71 | 9,00 | Litri | 30.00 |
| C | Kompensēšana | 10. | 14.72 | | Litri | |
| D | Aizpildīja | 40 | 39.57 | | Litri | |

### <a name="active-ingredients"></a>Aktīvās sastāvdaļas

Kad formulas rindai tiek pievienota prece, kurai ir pamata atribūts, tā tiek nosaukta par formulas *aktīvo sastāvdaļu*. Partijas pasūtījumus, kuriem ir formulas, kas ietver aktīvās sastāvdaļas, var izmantot partijas līdzsvarošanas procesā. Katrai formulas sastāvdaļai partijas līdzsvarošanas procesā tiek aprēķināts daudzums, kas ir nepieciešams, lai saražotu preci. Aprēķinātais daudzums ir balstīts uz aktīvo sastāvdaļu koncentrāciju atlasītajās partijās.

#### <a name="active-ingredient-example"></a>Aktīvās sastāvdaļas piemērs

Sastāvdaļai B ir pamata atribūts X un mērķa līmenis 30, un tā ir iekļauta formulā, kas pieprasa 30 litrus sastāvdaļas B uz katriem 100 preces litriem. Tiek izveidots partijas pasūtījums, kam partijas lielums ir 100 litri. Partijas pasūtījums tiek sākts, un partijas līdzsvarošanas procesa laikā lietotājs atlasa sastāvdaļas B partiju ar satura līmeni 35. Satura līmeņa vērtība 35 ir augstāka par mērķa līmeņa vērtību 30, tādēļ sastāvdaļas B līdzsvarotais daudzums tiek samazināts, izmantojot satura vērtību attiecību pret partijas mērķa līmeni, kas tiek reizināts ar aprēķināto daudzumu. Līdzsvarotā daudzuma aprēķins izskatās šādi:

(30 ÷ 35) x 30 litri = 25,71 litrs

### <a name="none-ingredients"></a>Neviena sastāvdaļa

Izmantojot partijas līdzsvarošanas procesu, ja **Sastāvdaļas veids** ir *Nav*, partijas pasūtījuma formulas rindā aprēķinātais un līdzsvarotais daudzums ir vienādi.

#### <a name="none-ingredient-example"></a>Nevienas sastāvdaļas piemērs

Sastāvdaļa A tiek piešķirta sastāvdaļai ar veidu *Nav* un pievienota pabeigtās preces formulai. Formula pieprasa 10 litrus sastāvdaļas A uz katriem 100 pabeigtās preces litriem. Ja partijas pasūtījumam nepieciešami 200 litri, sastāvdaļas aprēķinātais un līdzsvarotais daudzums tiek aprēķināts kā 20 litri.

### <a name="compensating-ingredients"></a>Kompensējošās sastāvdaļas

Kompensējošā sastāvdaļa var nobīdīt vai papildināt preci aktīvās sastāvdaļas efektu. Tāpēc patērētais kompensējošās sastāvdaļas daudzums ir atkarīgs no produkta satura.

- **Pretējs efekts** — ja aktīvā sastāvdaļas daudzums ir lielāks nekā gaidīts, ir jāpievieno mazāk kompensējošās sastāvdaļas.

- **Papildinošs efekts** — ja aktīvā sastāvdaļas daudzums ir mazāks nekā gaidīts, ir jāpievieno vairāk kompensējošās sastāvdaļas.

Aktīvās sastāvdaļas un papildu sastāvdaļas relācija tiek iestatīta lapā **Kompensācijas princips**.

Lai iestatītu sastāvdaļu relācijas, izpildiet tālāk minētās darbības.

1. Atlasiet **Ražošanas informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.
1. Atveriet formulas rindu un pēc tam atlasiet **Sastāvdaļas**, lai atvērtu lapu **Kompensēšanas princips**.
1. Atlasiet rindas, kas atspoguļo kompensācijas principu un pēc tam atlasiet kompensējamo aktīvo sastāvdaļu.

Kompensācijas principā jāievada arī pozitīvs vai negatīvs kompensācijas koeficients, kas norāda to, cik daudz jākompensē un vai principam jābūt pretējam vai papildu. Pozitīvs koeficients norāda papildu efektu un negatīvs koeficients norāda pretēju efektu.

#### <a name="compensating-ingredient-example"></a>Kompensējošās sastāvdaļas piemērs

Sastāvdaļa B ir aktīvā sastāvdaļa ar pamata atribūtu X un mērķa līmeni 30. Tā ir iekļauta formulā, kas pieprasa 30 litrus sastāvdaļas B uz katriem 100 preces litriem. Sastāvdaļa C ir kompensējošā sastāvdaļa, un daudzums 10 ir iekļauts tajā pašā formulā. Kompensācijas faktors 1,10 ir iestatīts kompensācijas principam. Tāpēc kompensējošās sastāvdaļas līdzsvarotais daudzums tiks samazināts par starpību starp aktīvās sastāvdaļas līdzsvaroto daudzumu un aprēķināto nepieciešamo daudzumu, kas reizināts ar 1,10.

Piemērā ar sastāvdaļas veidu *Aktīva* nepieciešamās aktīvās sastāvdaļas līdzsvarotais daudzums tika aprēķināts kā 25,71, un nepieciešamais daudzums tika aprēķināts kā 30. Šajā gadījumā kompensējošās sastāvdaļas līdzsvarotais daudzums tiks aprēķināts šādi:

1. Starpība starp aprēķināto un līdzsvaroto daudzumu tiek noteikta šādi:  
    25,71 – 30 = 4,29

1. Rezultāts tiek reizināts ar kompensācijas faktoru:  
    4,29 × 1,10 = –4,72

1. No aprēķinātā kompensējošā daudzuma tiek atņemta vērtība –4,72, lai noteiktu līdzsvaroto kompensējošo daudzumu:  
    10 –(– 4,72) = 14,72

Tā kā 1,10 ir pozitīvs kompensācijas faktors, šim kompensācijas principam ir papildinošs efekts. Šajā gadījumā aktīvā sastāvdaļa ir vairāk līdzsvarojoša, nekā gaidīts. Tādēļ ir vajadzīgs vairāk kompensējošās sastāvdaļas.

### <a name="filler-ingredients"></a>Palīgviela

*Palīgviela* ir neitrāla sastāvdaļa, kas tiek izmantota, lai sasniegtu vēlamo pabeigtās preces izejas daudzumu. Palīgvielas daudzumu korekcijas tiek aprēķinātas, pamatojoties uz aktīvās sastāvdaļas un kompensējošās sastāvdaļas variācijām, salīdzinot ar standarta daudzumu.

#### <a name="filler-ingredient-example"></a>Palīgvielas piemērs

Tika aprēķināta prece, kas ietver sastāvdaļas A, B, C un D formulas lielumam 100 litri. Tika aprēķināts visu sastāvdaļu veidu līdzsvarotais daudzums, izņemot sastāvdaļas veidam *Palīgviela*, kas tiek izmantota vienā rindā.
Palīgvielas līdzsvarotais daudzums tiek aprēķināts kā starpība starp partijas lieluma 100 litriem un sastāvdaļas A, B un C summa:

100 – (20 + 25,71 + 14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Partijas līdzsvarošanas process

Partijas līdzsvarošanas process tiek veikts no lapas **Partijas līdzsvarošana**.
Atlasiet **Izmaksu pārvaldība \> Partijas pasūtījumi**, un pēc tam cilnē **Process** atlasiet **Partijas līdzsvarošana**. Funkcija Partijas līdzsvarošana ir pieejama partijas pasūtījumiem ar statusu **Sākts**.

Kopumā partijas līdzsvarošanu var lietot partijas pasūtījumiem, ja formulā ir vismaz viena formulas rinda, kur **Sastāvdaļas veids** ir *Aktīva*. (Šīs kārtulas izņēmumu skatiet tālāk šajā rakstā sadaļā "Partijas pasūtījumi, kas nav piemērojami partijas līdzsvarošanai".)

Partijas līdzsvarošanas procesu var sadalīt divos apakšprocesos:

1. Bilances partijas sastāvdaļas
1. Formulas apstiprināšana un izdošana

### <a name="balance-batch-ingredients"></a>Bilances partijas sastāvdaļas

Apakšprocesā Bilances partijas sastāvdaļas tiek aprēķināts ražošanas partijā izmantojamais sastāvdaļu daudzums, ņemot vērā atlasītās preču partijas ar aktīvo sastāvdaļu. Aprēķinu var veikt tikai tad, ja ir pilns visu sastāvdaļu segums. Nevar līdzsvarot tikai partijas daļu, kam partijas pasūtījums ir iestatīts ražošanai.

> [!NOTE]
> Nevar saglabāt aprēķinu un pēc tam veikt partijas līdzsvarošanas procesu vēlāk. Ja aizverat lapu **Partijas līdzsvarošana**, lai pabeigtu procesu, aprēķins ir jāatkārto.

### <a name="confirm-and-release-the-formula"></a>Formulas apstiprināšana un izdošana

Kad sastāvdaļas daudzumi ir aprēķināti, varat apstiprināt un izdot formulu. Izlaišanas process atšķiras atkarībā no tā, vai preces ir iespējotas noliktavas vadības procesiem (WMS):

- Ja WMS aktivizēta prece, formulas rinda tiek nodota izpildei noliktavā saskaņā ar WMS principiem. Formulas rinda tiek izdota ar daudzumiem, kas atbilst līdzsvarotajiem daudzumiem, un tiek izdota konkrētām partijām, kas ir atlasītas aktīvajām sastāvdaļām.

    > [!NOTE]
    > Formulas rindas var izdot noliktavai tikai kā daļu no līdzsvarošanas procesa partijas. Lai gan materiālu izdošanai ražošanai uz noliktavu ir pieejamas citas opcijas, šīs opcijas nevar izmantot formulas rindām.

- Ja prece nav iespējota WMS, apstiprinot un izdodot formulu, precei tiek izveidots ražošanas izdošanas saraksts.

Vienā formulā varat kombinēt preces, kas ir iespējotas noliktavas pārvaldības procesiem, un preces, kas nav iespējotas noliktavas pārvaldības procesiem. Kad divi preču tipi ir ietverti vienā formulā, preces, kas ir iespējotas WMS, tiek izlaistas noliktavā. Precēm, kas nav iespējotas WMS, izdošanas saraksts tiek izveidots, apstiprinot un izdodot formulu.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Partijas pasūtījumi, kas nav lietojami partijas līdzsvarošanā

Ir divi kārtulas izņēmumi, kad partijas līdzsvarošanai var lietot partijas pasūtījumus, ja formulā ir vismaz viena formulas rinda, kur **Sastāvdaļas veids** ir *Aktīva*.

1. Ja formulā ir ietverta aktīva sastāvdaļa precei, kas ir iespējota WMS, bet partijas numurs atrodas zem novietojuma rezervāciju hierarhijā, partijas pasūtījums nav piemērojams partijas līdzsvarošanai.
1. Ja formulas mērvienība atšķiras no aktīvās sastāvdaļas krājumu mērvienības, partijas pasūtījums nav piemērojams partijas līdzsvarošanai.

Partijas pasūtījums, kas nav lietojams par partijas līdzsvarošanā, tiek pakļauts parastajam partijas pasūtījumu procesa ciklam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]