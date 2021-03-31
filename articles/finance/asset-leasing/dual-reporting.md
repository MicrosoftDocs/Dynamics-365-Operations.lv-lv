---
title: Duālie pārskati
description: Šajā tēmā ir sniegts piemērs, kā varat izpildīt gan starptautiskā finanšu pārskatu standarta (International Financial Reporting Standard — IFRS), gan likumā noteiktās prasības pārskatiem līdzekļu nomā.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229554"
---
# <a name="dual-reporting"></a>Duālie pārskati

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts piemērs, kā varat izpildīt gan starptautiskā finanšu pārskatu standarta (International Financial Reporting Standard — IFRS), gan likumā noteiktās prasības pārskatiem līdzekļu nomā. Ir nepieciešams labi pazīt grāmatošanas līmeņus Microsoft Dynamics 365 Finance, tas padarīs šo piemēru vieglāk saprotamu.

## <a name="example"></a>Paraugs

Tālāk minētais piemērs uzskaita nomu saskaņā ar Itālijā obligāto pārskatu sniegšanu, izmantojot gan skaudras naudas bāzes metodi, gan IFRS pārskata metodes. Uzņēmumam ir jāizveido trīs grāmatas, lai uzskaitītu gan Itālijā obligātās prasības, gan IFRS 16 prasības. Viena grāmata ir nepieciešama IFRS 16, viena ir nepieciešama obligātajām prasībām, un viena grāmata ir nepieciešama, lai automātiski anulētu obligātos grāmatojumus. Grāmatas ir iestatītas, kā parādīts tālāk redzamajās tabulās.

**IFRS 16 grāmata**

IFRS 16 grāmata ir iestatīta tā, lai tā atbilstu IFRS 16 uzskaites standartam. Visi ieraksti, kas tiek grāmatoti šajā grāmatā, tiks grāmatoti pielāgotajā slānī.

| Vārds, uzvārds                                    | Apraksts    |
|-----------------------------------------|----------------|
| Grāmatas tips                               | IFRS 16        |
| Grāmatas apraksts                        | IFRS 16        |
| Grāmatošanas līmenis                           | 1. pielāgotais līmenis |
| Nomas veids                              | Finance        |
| Uzskaites struktūra                    | IFRS 16        |
| Nomas termiņa / lietderīgās lietošanas laika iestatīšana         | 0.00           |
| Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana | 0.00           |
| Īstermiņa slieksnis                    | 12.             |
| Nelielas vērtības slieksnis                     | 5,000.00       |
| Maksāt kreditoram                           | Nr.             |

**Obligātā grāmata**

Obligātā grāmata ir skaidras naudas bāzes grāmata, kurā uzņēmums uzskaitīs nomas izdevumus kā skaidras naudas summu, kas katru mēnesi tiek maksāta par īri. Šī grāmata nerada līdzekļa lietošanas tiesības (LLT) vai nomas saistības.

| Vārds, uzvārds                                    | Apraksts |
|-----------------------------------------|-------------|
| Grāmatas tips                               | Obligāta   |
| Grāmatas apraksts                        | Vietējie vispārpieņemtie grāmatvedības principi  |
| Grāmatošanas līmenis                           | Pašreizējos     |
| Nomas veids                              | Automātiski   |
| Uzskaites struktūra                    | Skaidras naudas bāze  |
| Nomas termiņa / lietderīgās lietošanas laika iestatīšana         | 0.00        |
| Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana | 0.00        |
| Īstermiņa slieksnis                    | 0           |
| Nelielas vērtības slieksnis                     | 0           |
| Maksāt kreditoram                           | Nr.          |

**Obligātā anulēšanas grāmata**

Obligātā anulēšanas grāmata ir iestatīta tādā pašā veidā kā obligātā grāmata.

| Vārds, uzvārds                                    | Apraksts                    |
|-----------------------------------------|--------------------------------|
| Grāmatas tips                               | Obligātā — anulēšanas           |
| Grāmatas apraksts                        | Rezervēt, lai anulētu obligāto grāmatu |
| Grāmatošanas līmenis                           | 1. pielāgotais līmenis                 |
| Nomas veids                              | Automātiski                      |
| Uzskaites struktūra                    | Skaidras naudas bāze                     |
| Nomas termiņa / lietderīgās lietošanas laika iestatīšana         | 0.00                           |
| Pašreizējās vērtības / līdzekļa patiesās vērtības iestatīšana | 0.00                           |
| Īstermiņa slieksnis                    | 0                              |
| Nelielas vērtības slieksnis                     | 0                              |
| Maksāt kreditoram                           | Nr.                             |

Šim piemēram ir izveidota noma, kam ir tālāk norādītie iestatījumi cilnēs **Vispārīgi** un **Maksājuma grafika rindas**.

**Cilne Vispārīgi**

| Lauks                      | Vērtība            |
|----------------------------|------------------|
| Salīdzināmā aizņēmuma procentu likme | 5%               |
| Sākuma datums          | 01.01.2020.         |
| Nomas grupa                | Ēkas        |
| Kreditors                     | 1001             |
| Līdzekļa patiesā vērtība    | 245,000          |
| Līdzekļa lietderīgās lietošanas laiks          | 120              |
| Gada maksājuma veids               | Parastais gada maksājums |
| Pievienošanas intervāls       | Mēnesis          |

**Cilne Maksājumu grafika rindas**

| Lauks             | Vērtība      |
|-------------------|------------|
| Sākuma datums        | 01.01.2020.   |
| Perioda intervāls   | Mēneši     |
| Periodi           | 24         |
| Beigu datums          | 31.12.2020. |
| Maksājumu biežums | Mēnesis    |
| Maksājuma summa    | 1000      |

Lai šo nomu uzskaitītu divās struktūrās, jāizmanto pašreizējais grāmatošanas līmenis un pielāgotais grāmatošanas līmenis. Tālāk redzamajā tabulā ir parādīts katra žurnāla ieraksta piemērs, kas nepieciešams pilnīgi atspoguļotu finanšu datus saskaņā ar katru pārskata standartu. Pēc tam tiek sniegts detalizēts katra žurnāla ieraksta apraksts par nomas pirmo mēnesi.

<table>
<thead>
<tr>
<th rowspan='3'>Konta numurs</th>
<th rowspan='3'>Apraksts</th>
<th colspan='3'>Obligātā grāmata (pašreizējais slānis)</th>
<th rowspan='3'>Pašreizējais slānis kopā</th>
<th>Anulēšanas grāmata (pielāgotais slānis)</th>
<th colspan='4'>IFRS 16 grāmata (pielāgotais slānis)</th>
<th rowspan='3'>Pašreizējā slāņa + pielāgotā slāņa kopsumma</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Nomas izdevumi</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankas komisija</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>PVN izdevumi</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Dzēšanas konts</td>
<td>-1000,00</td>
<td>1,000.00</td>
<td></td>
<td>0.00</td>
<td>1,000.00</td>
<td></td>
<td>-1000,00</td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>5</td>
<td>Kreditoru parādi</td>
<td></td>
<td>-1008,00</td>
<td>1,008.00</td>
<td>0.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>6</td>
<td>LLT līdzeklis</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Finanšu nomas saistības</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
<td></td>
<td>-22 794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21 888,87</td>
</tr>
<tr>
<td>8</td>
<td>Maksājamie procenti</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Kase</td>
<td></td>
<td></td>
<td>-1008,00</td>
<td>-1008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1008,00</td>
</tr>
<tr>
<td>10.</td>
<td>Nolietojuma izmaksas</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11.</td>
<td>Uzkrātais nolietojums</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Kā redzams iepriekšējā tabulā, ir nepieciešamas trīs grāmatas, lai sniegtu pārskatu saskaņā obligāto un IFRS pārskatu sniegšanu.

- Obligātajā grāmatā ierakstīti nomas maksājumi saskaņā ar noteikumiem par skaidras naudas bāzes uzskaiti, pamatojoties uz pašreizējo slāni.
- Obligātā anulēšanas grāmata anulē obligātos žurnāla ierakstus.
- IFRS 16 grāmata izveido žurnāla ierakstus, kas ir nepieciešami saskaņā ar IFRS 16.

Noma ir jāievada tikai vienu reizi. Pēc tam varat atvērt lapu **Grāmatas**, lai skatītu visas ar nomu saistītās grāmatas.

> [!NOTE]
> Kad izveidojat grāmatas, visām trim no tām jābūt saistītām ar to pašu nomas ierakstu.

Pirmajā žurnāla ierakstā reģistrēti nomas izdevumi saskaņā ar obligāto grāmatu. Varat izveidot maksājumus vai nu partijā, vai atlasot maksājumu grafiku obligātajā grāmatā.

Šajā piemērā tālāk norādītais žurnāla ieraksts ir izveidots obligātajai grāmatai no maksājumu grafika.

### <a name="lease-payment--1312020--je-100"></a>Nomas maksājums — 01.31.2020. — JE 100

| Konta veids | Konta numurs | Līmenis   | Konta apraksts | Debetkarte    | Kredītkarte   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Pašreizējos | Nomas izdevumi       | 1,000.00 |          |
| Ledger       | 4              | Pašreizējos | Dzēšanas konts    |          | 1,000.00 |

Par Kreditoru rēķiniem atbildīgais darbinieks izmanto standarta Dynamics 365 funkcionalitāti, lai izveidotu rēķinu, kas jāmaksā par nomu ārpus Līdzekļu nomas. Tomēr tā vietā, lai atlasītu **Nomas izdevumi** kā debeta kontu, par Kreditoru rēķiniem atbildīgais darbinieks atlasa dzēšanas kontu, lai ģenerētu tālāk norādīto ierakstu.

### <a name="ap-process--1312020--je-110"></a>KR process — 31.012020. — JE 110

| Konta veids | Konta numurs | Līmenis   | Konta apraksts | Debetkarte    | Kredītkarte   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Pašreizējos | Dzēšanas konts    | 1,000.00 |          |
| Ledger       | 2              | Pašreizējos | Bankas komisija            | 3.00     |          |
| Ledger       | 3              | Pašreizējos | PVN izdevumi         | 5.00     |          |
| Kreditors       | 5              | Pašreizējos | Kreditoru parādi    |          | 1,008.00 |

Kad izraksts tiek izsniegts kreditoram, veiciet parastu maksāšanas procesu. Šī procesa laikā tiek ģenerēts tālāk norādītais žurnāla ieraksts.

### <a name="cash-payment--1312020--je-120"></a>Skaidras naudas maksājums – 31.01.2020. – JE 120

| Konta veids | Konta numurs | Līmenis   | Konta apraksts | Debetkarte    | Kredītkarte   |
|--------------|----------------|---------|---------------------|----------|----------|
| Kreditors       | 5              | Pašreizējos | Parādi kreditoriem    | 1,008.00 |          |
| Banka         | 9              | Pašreizējos | Kase                |          | 1,008.00 |

Šajā brīdī esat pilnībā uzskaitījis šo nomu saskaņā ar obligātajām prasībām un varat ģenerēt apgrozījuma bilanci, izmantojot pašreizējo slāni. Sistēma izveido apgrozījuma bilanci ar tālāk norādītajiem skaitļiem.

<table>
<thead>
<tr>
<th rowspan='3'>Konta numurs</th>
<th rowspan='3'>Apraksts</th>
<th colspan='3'>Obligātā grāmata (pašreizējais slānis)</th>
<th rowspan='3'>Pašreizējais slānis kopā</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
<th>Deb. (kred.)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Nomas izdevumi</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankas komisija</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>PVN izdevumi</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Dzēšanas konts</td>
<td>-1000,00</td>
<td>1,000.00</td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>5</td>
<td>Kreditoru parādi</td>
<td></td>
<td>-1008,00</td>
<td>1,008.00</td>
<td>0.00</td>
</tr>
<tr>
<td>6</td>
<td>LLT līdzeklis</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>7</td>
<td>Finanšu nomas saistības</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>8</td>
<td>Maksājamie procenti</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>9</td>
<td>Kase</td>
<td></td>
<td></td>
<td>-1008,00</td>
<td>-1008,00</td>
</tr>
<tr>
<td>10.</td>
<td>Nolietojuma izmaksas</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
<tr>
<td>11.</td>
<td>Uzkrātais nolietojums</td>
<td></td>
<td></td>
<td></td>
<td>0.00</td>
</tr>
</tbody>
</table>

Ja vēlaties izmantot IFRS 16 skaitļus, lai palaistu to pašu apgrozījuma bilanci, ir jāanulē obligātie uzskaites žurnāla ieraksti un jāgrāmato IFRS 16 žurnāla ieraksti. Lai anulētu obligātos žurnāla ierakstus, šajā piemērā ir iekļauta obligātā anulēšanas grāmata ar tādiem pašiem iestatījumiem kā obligātajai grāmatai, bet ar pretēju grāmatošanas profilu. Piemēram, obligātā grāmata *debetēja* nomas izdevumu kontu, bet anulēšanas grāmata *kreditēs* šo kontu. Šīs attiecības ir viegli definētas Līdzekļu nomas grāmatošanas kontos lapā **Līdzekļu nomas parametri** lapā (**Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**).

Kad tas pats process, kas tika izmantots obligātajai grāmatai, tiek izmantots anulēšanas grāmatai, tiek izveidots tālāk norādītais žurnāla ieraksts. Atšķirība ir tāda, ka anulēšanas grāmata anulē obligātās grāmatas ierakstus. Anulēšanas ieraksti arī tiek veikti pielāgotā slānī. Ja apgrozījuma bilance tiek palaista pašreizējā slānī, anulējošie žurnāla ieraksti nav ietverti.

### <a name="lease-payment--1312020--je-130"></a>Nomas maksājums — 01.31.2020. — JE 130

| Konta veids | Konta numurs | Līmenis  | Konta apraksts | Debetkarte    | Kredītkarte   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Pielāgot | Dzēšanas konts    | 1,000.00 |          |
| Ledger       | 1              | Pielāgot | Nomas izdevumi       |          | 1,000.00 |

Tagad, kad ir likvidēti obligātā žurnāla ieraksti, tiks grāmatoti visi žurnāla ieraksti, kas ir nepieciešami IFRS 16 grāmatai. Šie ieraksti ietver sākotnējo LLT un saistību atzīšanu, kā arī procentu un nolietojuma ierakstu.

### <a name="initial-recognition--112020--je-140"></a>Sākotnējā atzīšana — 01.01.2020. — JE 140

| Konta veids | Konta numurs | Līmenis  | Konta apraksts      | Debetkarte     | Kredītkarte    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Pielāgot | LLT līdzeklis                | 22,793.90 |           |
| Ledger       | 7              | Pielāgot | Finanšu nomas saistības |           | 22,793.90 |

Nomas maksājums tiek grāmatots līdzīgi citi nomas maksājumi. Dzēšanas konta izmantošanas iemesls ir nodrošināt, ka skaidra nauda tiek kreditēta tikai vienu reizi.

### <a name="lease-payment--1312020--je-150"></a>Nomas maksājums — 01.31.2020. — JE 150

| Konta veids | Konta numurs | Līmenis  | Konta apraksts      | Debetkarte    | Kredītkarte   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Pielāgot | Finanšu nomas saistības | 1,000.00 |          |
| Ledger       | 4              | Pielāgot | Dzēšanas konts         |          | 1,000.00 |

Procentu izdevumu žurnāla ieraksts tiek ģenerēts no saistību amortizācijas grafika.

### <a name="interest-expense--1312020--je-160"></a>Procentu izdevumi — 31.01.2020. — JE 160

| Konta veids | Konta numurs | Līmenis  | Konta apraksts      | Debetkarte | Kredītkarte |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Pielāgot | Maksājamie procenti         | 94.97 |        |
| Ledger       | 7              | Pielāgot | Finanšu nomas saistības |       | 94.97  |

Nolietojuma izdevumu žurnāla ieraksts tiek ģenerēts no līdzekļa nolietojuma grafika.

### <a name="depreciation-expense--1312020--je-170"></a>Nolietojuma izdevumi — 31.01.2020. — JE 170

| Konta veids | Konta numurs | Līmenis  | Konta apraksts      | Debetkarte  | Kredītkarte |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10.             | Pielāgot | Nolietojuma izmaksas     | 949.75 |        |
| Ledger       | 11.             | Pielāgot | Uzkrātais nolietojums |        | 949.75 |

Pēc tam, kad visi šie žurnāla ieraksti ir izveidoti un grāmatoti, redzēsiet tālāk norādītās "1. pielāgotā slāņa" vērtības. Ņemiet vērā, ka pēdējā kolonnā ir ietverta bankas komisija, pievienotās vērtības nodokļa (PVN) izdevumi un skaidras naudas samazinājums no iepriekšējā slāņa, bet tajā nav ietverti obligātie žurnāla ieraksti. Tādējādi tiek sasniegtas patiesas duālo pārskatu iespējas. Šajā brīdī uzņēmumam vienkārši ir jāpalaiž apgrozījuma bilance un jākombinē pašreizējais slānis un pielāgotais slānis, lai izveidotu IFRS apgrozījuma bilanci.

| Konta Nr. | Apraksts              | Obligātā grāmata\-Pašreizējais slānis\-JE\-100\-Deb. \(kred.\) | Obligātā grāmata\-Pašreizējais slānis\-JE\-110\-Deb. \(kred.\) | Obligātā grāmata\-Pašreizējais slānis\-JE\-120\-Deb. \(kred.\) | Pašreizējais slānis \- Kopā | - | Anulēšanas grāmata\-pielāgotais slānis\-JE\-130\-Deb. \(kred.\) | IFRS 16 grāmata\-pielāgotais slānis\-JE\-140\-Deb. \(kred.\) | IFRS 16 grāmata\-pielāgotais slānis\-JE\-150\-Deb. \(kred.\) | IFRS 16 grāmata\-pielāgotais slānis\-JE\-160\-Deb. \(kred.\) | IFRS 16 grāmata\-pielāgotais slānis\-JE\-170\-Deb. \(kred.\) | pielāgotais slānis \+ Pašreizējais slānis \- Kopā |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Nomas izdevumi            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankas komisija                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | PVN izdevumi              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Dzēšanas konts         | \-1000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1000                                           |                                                | \-1000                                        |                                                |                                                | 0\.00                                   |
| 5          | Kreditoru parādi         |                                                   | \-1008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | LLT līdzeklis                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Finanšu nomas saistības |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22 794                                       | 1000                                          | \-94\.97                                       |                                                | \-21 888\.87                            |
| 8          | Maksājamie procenti         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Kase                     |                                                   |                                                   | \-1008\.00                                       | \-1008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1008\.00                             |
| 10.         | Nolietojuma izmaksas     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11.         | Uzkrātais nolietojums |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]