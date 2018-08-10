---
title: "Pieskaitāmo izmaksu aprēķins"
description: "Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 549e9b4b073a4e93dd3a1dd52dd6f43e7420a31b
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="overhead-calculation"></a>Pieskaitāmo izmaksu aprēķins

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti tipiskie procesi pieskaitāmo izmaksu aprēķināšanai un piešķiršanai.

<a name="term-definition"></a>Termina definīcija
---------------

Pieskaitāmās izmaksas ir izmaksas, kas rodas uzņēmējdarbības veikšanas nolūkos, bet kuras nevar tieši piesaistīt nevienai konkrētai uzņēmējdarbības aktivitātei, precei vai pakalpojumam. Pieskaitāmās izmaksas sniedz kritisku atbalstu peļņu nesošo aktivitāšu ģenerēšanai. Šeit norādītas dažas pieskaitāmās izmaksas:

-   Īre
-   Elektrība
-   Administratīvās algas

## <a name="overhead-calculation-overview"></a>Pieskaitāmo izmaksu aprēķina apskats
Pieskaitāmo izmaksu aprēķins izpilda izmaksu uzskaites politikas pareizajā secībā. Pieskaitāmo izmaksu aprēķinu par vienu un to pašu finanšu periodu varat izpildīt vairākas reizes, ja izmaksu uzskaites politikas ir mainītas vai ja ir konstatētas noteiktas kļūdas. Katra pieskaitāmo izmaksu aprēķina izpildes reize tiek saglabāts un saņem unikālu versijas ID, kas jums ļauj salīdzināt aprēķinus dažādās versijās. Pieskaitāmo izmaksu aprēķina ģenerētie izmaksu ieraksti saņem uzskaites datumu. Šis uzskaites datums atbilst aprēķinā izmantotā finanšu perioda beigu datumam. Unikāls versijas ID sastāv no tālāk uzskaitītajiem elementiem.

-   Versijas tips
-   Datums un laiks
-   Izmaksu uzskaites virsgrāmata
-   Finanšu gads
-   Fiskālais periods

Pieskaitāmo izmaksu aprēķins tiek darbināts neatkarīgi no versijas. Tāpēc budžeta versiju varat aprēķināt pirms faktiskās versijas. Pieskaitāmo izmaksu aprēķinu veido četri soļi, kā parādīts nākamajā attēlā. Katrā solī tiek izveidots žurnāla virsraksts, kurā ir žurnāla ieraksti. Šis žurnāla virsraksts glabā ievades datus par katru aprēķina soli. Politikas un kārtulas tiek lietotas katrai žurnāla rindai, un izmaksu ieraksti tiek ģenerēti kā izvade. Tādēļ jums vienmēr ir pilnīga izsekojamība. 

[![Pieskaitāmo izmaksu aprēķins](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Aprēķināt un piešķirt elektrības pieskaitāmās izmaksas
Finanšu uzskaitē noteiktas izmaksas, piemēram, par elektrību, tiek reģistrētas kā vienreizēja izmaksa. Tāpēc izmaksu uzskaitei netiek nodrošināti detalizēti pārvaldības ieskati. Lai izmaksu uzskaitē sniegtu pareizus pārvaldības ieskatus par visām organizācijas vienībām un līmeņiem, izmaksām ir jāplūst caur organizatoriskajām vienībām. Šīs plūsmas pamatā ir jābūt vai nu precīzai patēriņa reģistrēšanai, vai objektīvam novērtējumam. Virsgrāmatā elektrības izmaksas var grāmatot nākamajā tabulā parādītajā veidā.

<table>
<thead>
<tr>
<th>Uzskaites datums</th>
<th colspan="2">Izmaksu centrs</th>
<th colspan="2">Galvenais konts</th>
<th>Summa uzskaites valūtā</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017. gada 3. janvāris</td>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>10 000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>1. solis. Apstrādāt izmaksu uzvedību aprēķinu

Pēc noklusējuma, kad izmaksu ieraksti tiek importēti no datu avota, izmaksu uzskaitē tie saņem izmaksu uzvedības klasifikāciju **Neklasificēts**. Lietojot izmaksu uzvedības politikas kārtulas, izmaksu ierakstus varat pārklasificēt kā **Fiksētas izmaksas** vai kā **Mainīgas izmaksas**.

#### <a name="define-the-cost-behavior-rule"></a>Definēt izmaksu uzvedības kārtulu

Noteiktos gadījumos daļa izmaksu ir fiksēta maksa, un atlikušās izmaksas ir balstītas uz patēriņu. Elektrības rēķini bieži atbilst šai definīcijai. Kad samaksājat noteiktu fiksēto maksu, jums ir jāmaksā atbilstoši patērētajam kilovatstundu (Kwh) skaitam. Piemēram, tālāk ir norādīts, kā definēt izmaksu uzvedību kārtulu, ja fiksēto izmaksu maksa ir 1000,00.

-   Fiksētā summa 1000,00
    -   0 &lt;= 1000,00 = Fiksēts
    -   1000,01 &lt; N = Mainīgs

##### <a name="journal"></a>Žurnāls

<table>
<thead>
<tr>
<th>Žurnāls</th>
<th>Žurnāla tips</th>
<th colspan="3">Kalendārais finanšu periods</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Izmaksu izturēšanās aprēķināšanas žurnāls</td>
<td>Finanšu</td>
<td>2017</td>
<td>Periods 1</td>
<td>Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)

<table>
<thead>
<tr>
<th>Uzskaites datums</th>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017. gada 3. janvāris</td>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Neklasificēts</td>
<td>10 000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Izmaksu ieraksti

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
<th>Uzskaites datums</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Neklasificēts</td>
<td>10 000,00</td>
<td>2017. gada 3. janvāris</td>
</tr>
<tr>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Neklasificēts</td>
<td>-10 000,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>1000,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>9,000.00</td>
<td>2017. gada 31. janvāris</td>
</tr>
</tbody>
</table>

Detalizētu informāciju par izmaksu uzvedību skatiet sadaļā Izmaksu uzvedības politika. (Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)

### <a name="step-2-process-the-cost-distribution-calculation"></a>2. solis. Apstrādāt izmaksu sadalījuma aprēķinu

Izmaksu sadalījums tiek izmantots, lai izmaksas no viena izmaksu objekta pārdalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu. Izmaksu izplatīšana no izmaksu sadalījuma atšķiras ar to, ka izmaksu izplatīšana vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī.

#### <a name="define-the-cost-distribution-rule"></a>Definēt izmaksu izplatīšanas kārtulu

Finanšu uzskaitē izmaksas par elektrību bieži tiek reģistrētas kā vienreizēja izmaksa. Izmaksu uzskaitē šī metode nav pietiekami detalizēta. Mainīgās izmaksas ir taisnīgi jāsadala uz atsevišķajiem izmaksu objektiem. Visloģiskākais sadalījuma pamats ir elektrības patēriņš (Kwh). Tiek izveidots statistiskas dimensijas elements ar nosaukumu Elektrība, un tiek reģistrēts elektrības patēriņš. Pēc noklusējuma visi statistiskas dimensijas elementi kļūst pieejami kā sadalījuma pamati.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>0</td>
</tr>
</tbody>
</table>

Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1000</td>
<td>(1000 ÷ 7000) × 9000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>6,000</td>
<td>(6000 ÷ 7000) × 9000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>0</td>
<td>(0 ÷ 7000) × 9000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Fiksētās izmaksas ir vienādi jāsadala uz atsevišķajiem izmaksu objektiem, kas ir patērējuši elektrību. Šādu rezultātu varat iegūt, izmantojot statistiskās dimensijas elementu Elektrība formulas sadalījuma pamatā: (Elektrība &gt; 0,00) Nākamajā tabulā ir parādīts rezultāts, kāds rodas, ja mainīgajām izmaksām kā sadalījuma pamats tiek lietots elektrības patēriņš.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Formula</th>
<th>Lielums</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>(1000 &gt; 0,00)</td>
<td>1.</td>
<td>(1 ÷ 2) × 1000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>(6000 &gt; 0,00)</td>
<td>1.</td>
<td>(1 ÷ 2) × 1000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Žurnāls

<table>
<thead>
<tr>
<th>Žurnāls</th>
<th>Žurnāla tips</th>
<th colspan="3">Kalendārais finanšu periods</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Izmaksu sadales aprēķina žurnāls</td>
<td>Finanšu</td>
<td>2017</td>
<td>Periods 1</td>
<td>Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)

<table>
<thead>
<tr>
<th>Uzskaites datums</th>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>1000,00</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Izmaksu ieraksti

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
<th>Uzskaites datums</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>-1000,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>500,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>500,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC099</td>
<td>Noklusējuma izmaksu centrs</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-9000,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>1,285.71</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>7,714.29</td>
<td>2017. gada 31. janvāris</td>
</tr>
</tbody>
</table>

Detalizētu informāciju par izmaksu sadali un sadalījuma pamatiem skatiet sadaļā Izmaksu sadales politika un Sadalījuma pamati. (Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)

### <a name="step-3-process-the-overhead-rate-calculation"></a>3. solis. Apstrādāt pieskaitāmo izmaksu likmes aprēķinu

Pieskaitāmo izmaksu likme tiek izmantota, lai iekasētu maksu par vienu vai vairākiem specifiskiem izmaksu objektiem. Šī iekasēšana ir balstīta uz iepriekš noteiktu izmaksu likmi un lielumu no piešķirtā sadalījuma pamata. 

#### <a name="define-the-overhead-rate"></a>Definēt pieskaitāmo izmaksu likmi

Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos iekšējos projektos. Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR projekti.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Stundas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>1. projekts</td>
<td>3.</td>
</tr>
<tr>
<td>Proj 2</td>
<td>2. projekts</td>
<td>1.</td>
</tr>
</tbody>
</table>

Ir definēta iepriekš noteikta izmaksu likme attiecībā uz izmaksu projektu ieguldījumu.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Mērvienības</th>
<th>Likme</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Mainīgas izmaksas</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Nākamajā tabulā ir parādīts rezultāts, kādu iegūst, ja kā sadalījuma pamats tiek lietoti HR projekti.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
<th>Izmaksu elements</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>1. projekts</td>
<td>3.</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>2. projekts</td>
<td>1.</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Žurnāls

<table>
<thead>
<tr>
<th>Žurnāls</th>
<th>Žurnāla tips</th>
<th colspan="3">Kalendārais finanšu periods</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Pieskaitāmo izmaksu likmes aprēķina žurnāls</td>
<td>Finanšu</td>
<td>2017</td>
<td>Periods 1</td>
<td>Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Žurnāla ieraksti (žurnāla ieraksti pieskaitāmo izmaksu likmes aprēķinam)

<table>
<thead>
<tr>
<th>Uzskaites datums</th>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017. gada 31. janvāris</td>
<td>Proj 1</td>
<td>Iekšējais 1. projekts</td>
<td>3,00</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>Proj 2</td>
<td>Iekšējais 2. projekts</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Izmaksu ieraksti

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
<th>Uzskaites datums</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-30,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Proj 1</td>
<td>Iekšējais 1. projekts</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>30,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-10,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Iekšējais 2. projekts</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>10,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
</tbody>
</table>

Detalizētu informāciju par pieskaitāmo izmaksu likmes politiku skatiet sadaļā Pieskaitāmo izmaksu likmes politika un Sadalījuma pamati. (Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)

### <a name="step-4-process-the-cost-allocation-calculation"></a>4. solis. Apstrādāt izmaksu sadalījuma aprēķinu

Sadalījums tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu. Finance and Operations atbalsta savstarpējā sadalījuma metodi. Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās. Sistēma automātiski nosaka pareizo secību, kādā veikt sadalījumus. Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata. Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos. Sadalījuma secību kontrolē izmaksu kontroles vienība. 

[![Savstarpējā metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Definēt izmaksu sadalījumu

Tālāk ir sniegts vienkāršs piemērs, kurā skaidrots, kā varat izsekot izmaksu plūsmu. Izmaksu objekts CC001 HR sniedz ieguldījumu vairākos izmaksu objektos. Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu HR pakalpojumi.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>HR pakalpojumi</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10.</td>
</tr>
</tbody>
</table>

Izmaksu objekts CC002 Finanses sniedz ieguldījumu vairākos izmaksu objektos. Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Finanses.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Finanšu pakalpojumi</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>35</td>
</tr>
</tbody>
</table>

Izmaksu objekts CC003 Montāža sniedz ieguldījumu vairākos izmaksu objektos. Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Montāža.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Montāžas pakalpojumi (stundas)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>60</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>20</td>
</tr>
</tbody>
</table>

Izmaksu objekts CC004 Iepakošana sniedz ieguldījumu vairākos izmaksu objektos. Lai izmērītu patērēto apjomu, tiek izveidots statistiskas dimensijas elements ar nosaukumu Iepakošana.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Iepakošanas pakalpojumi (stundas)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>80</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>15.</td>
</tr>
</tbody>
</table>

**Piezīme.** Sistēmā Finance and Operations statistiskos mērus, piemēram, preces patērētās ražošanas stundas, var atvasināt no avota datiem. Plašāku informāciju par statistisko mēru nodrošinātājiem skatiet sadaļā Statistisko mēru nodrošinātāja veidnes. (Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.) Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti HR pakalpojumi.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
<th>Izmaksu izturēšanās</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10.</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>35</td>
<td>(35 ÷ 100) × 1245,71</td>
<td>436.00</td>
<td>Mainīgas izmaksas</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>55</td>
<td>(55 ÷ 100) × 1245,71</td>
<td>685.14</td>
<td>Mainīgas izmaksas</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10.</td>
<td>(10 ÷ 100) × 1245,71</td>
<td>124.57</td>
<td>Mainīgas izmaksas</td>
</tr>
</tbody>
</table>

Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti finanšu pakalpojumi.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
<th>Izmaksu izturēšanās</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>65</td>
<td>(65 ÷ 100) × (7714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Mainīgas izmaksas</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>35</td>
<td>(35 ÷ 100) × (7714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Mainīgas izmaksas</td>
</tr>
</tbody>
</table>

Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti montāžas pakalpojumi.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
<th>Izmaksu izturēšanās</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>20.</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>60</td>
<td>(60 ÷ 80) × (5297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Mainīgas izmaksas</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>20.</td>
<td>(20 ÷ 80) × (5297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Mainīgas izmaksas</td>
</tr>
</tbody>
</table>

Nākamajā tabulā ir parādīts rezultāts, kāds tiek iegūts, ja kopējām izmaksām (fiksētajām izmaksām un mainīgajām izmaksām) kā sadalījumam pamats tiek lietoti iepakošanas pakalpojumi.

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th>Lielums</th>
<th>Sadalījuma koeficients</th>
<th>Summa</th>
<th>Izmaksu izturēšanās</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Fiksētas izmaksas</td>
</tr>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>80</td>
<td>(80 ÷ 95) × (2852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Mainīgas izmaksas</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>15</td>
<td>(15 ÷ 95) × (2852,60 + 124,57)</td>
<td>470.08</td>
<td>Mainīgas izmaksas</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Žurnāla ieraksti (izmaksu objekta bilances žurnāla ieraksti)

<table>
<thead>
<tr>
<th>Žurnāls</th>
<th>Žurnāla tips</th>
<th colspan="3">Kalendārais finanšu periods</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Izmaksu sadalījuma žurnāls</td>
<td>Finanšu</td>
<td>2017</td>
<td>Periods 1</td>
<td>Pieskaitāmo izmaksu aprēķins / 01-02-2017 23:51:00 / Virsgrāmata /2017 / 1. periods</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Žurnāla rindas

<table>
<thead>
<tr>
<th>Uzskaites datums</th>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>500,00</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>1,245.71</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>675.00</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>8,150.29</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>713.75</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>5,982.83</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC003</td>
<td>Iepakošana</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>286.25</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>CC003</td>
<td>Iepakošana</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>2,977.17</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>Prod 1</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>776.36</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>Prod 1</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>6,994.21</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>Prod 2</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>223.64</td>
</tr>
<tr>
<td>2017. gada 31. janvāris</td>
<td>Prod 2</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Izmaksu ieraksti

<table>
<thead>
<tr>
<th colspan="2">Izmaksu objekts</th>
<th colspan="2">Izmaksu elements</th>
<th>Izmaksu izturēšanās</th>
<th>Summa</th>
<th>Uzskaites datums</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>-500,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>175.00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>275.00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>50,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-1245,71</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>436.00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>685.14</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>124.57</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>-675,00</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>438.75</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>236.25</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC002</td>
<td>Finanses</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-8150,29</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>5,297.69</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC004</td>
<td>Iepakošana</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>2,852.60</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>-713,75</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>535.31</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>178.44</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-5982,83</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>4,487.12</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>1,495.71</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>-286,25</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>241.05</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Fiksētas izmaksas</td>
<td>45.20</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>CC003</td>
<td>Montāža</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>-2977,17</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 1</td>
<td>1. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>2,507.09</td>
<td>2017. gada 31. janvāris</td>
</tr>
<tr>
<td>Prod 2</td>
<td>2. prece</td>
<td>10001</td>
<td>Elektrība</td>
<td>Mainīgas izmaksas</td>
<td>470.08</td>
<td>2017. gada 31. janvāris</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Nobeigums
Finanšu grāmatvedībā 10 000,00 izmaksas par elektrību tiek grāmatotas uz fiktīvu izmaksu centra ID. Tāpēc izmaksu grāmatveži zina, ka šīs izmaksas ir jāsadala. Izmaksu uzskaitē izmaksas plūst uz dažādām organizatoriskajām vienībām un līmeņiem, pamatojoties uz lietotajām politikām un kārtulām. Katras izmaksas ir saistītas ar kādu sadalījuma pamatu, kurš nodrošina vislabāko novērtējumu attiecībā uz izmaksu sadalījumu.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Izmaksu elements</th>
<th colspan="9">Izmaksu objekts</th>
<th rowspan="2">Summa</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Proj 1</th>
<th>Proj 2</th>
<th>Prod 1</th>
<th>Prod 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Elektrība</td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30,00</strong></td>
<td style="text-align: right;"><strong>10,00</strong></td>
<td style="text-align: right;"><strong>7.770,57</strong></td>
<td style="text-align: right;"><strong>2.189,43</strong></td>
<td style="text-align: right;"><strong>10.000,00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Neklasificēts</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Fiksētas izmaksas</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1.000,00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Mainīgas izmaksas</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9.000,00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Šajā tēmā ir parādīts, kā primārais izmaksu elements, 10001 Elektrība, plūst caur izmaksu objektiem. Tāpēc šīs pieskaitāmās izmaksas tiek sadalītas līdz zemākajam līmenim organizācijā. Citiem vārdiem sakot — izmaksas sedz zemākajā līmenī esošie izmaksu objekti. Ja ir nepieciešama vizuāla izmaksu plūsma starp izmaksu objektiem, varat izmantot izmaksu apkopošanas politiku kārtulas, lai šo izmaksu plūsmu vizualizētu. Papildinformāciju skatiet sadaļā Izmaksu apkopošanas politika. (Ņemiet vērā, ka šī tēma vēl nav pabeigta, bet būs pieejama drīzumā.)




