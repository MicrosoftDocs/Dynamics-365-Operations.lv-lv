---
title: Krājumu vecumstruktūru pārskatu piemēri un loģika
description: Šajā tēmā sniegti daži piemēri, kas parāda, kā interpretēt Krājumu vecumstruktūru pārskata rezultātus.
author: JennySong-SH
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4cfffa49f802c601da391617b123134c435fba92
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672351"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Krājumu vecumstruktūru pārskatu piemēri un loģika

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegti daži piemēri, kas parāda, kā interpretēt **Krājumu vecumstruktūru** pārskata rezultātus. Šajā pārskatā ir iedalīti rīcībā esošie daudzumi un krājumu vērtības atlasītajam krājumam vai krājumu grupai vairākos perioda intervālos. Šī tēma rāda arī pārskata iekšējo loģiku.

Šīs tēmas piemēri rāda rezultātus, kas ir sniegti standarta **Krājumu novecošanas** pārskatā. Tomēr parasti ir ieteicams izmantot šī pārskata [Krājumu novecošanas pārskata krātuve](inventory-aging-report-storage.md) versiju, īpaši, ja ir daudz krājumu un noliktavu, kas jāapstrādā. Krājumu novecošanas pārskata krātuve saglabā katru izveidoto pārskatu, parāda rezultātus kā interaktīvu lapu un diagrammu un ļauj eksportēt visu saglabāto pārskatu.

## <a name="sample-data-that-is-used-in-these-examples"></a>Šajos piemēros izmantotie parauga dati

Šīs tēmas piemēri ir balstīti uz parauga krājumu darbību datiem, kas aprakstīti šajā sadaļā.

### <a name="storage-dimension-setup"></a>Noliktavas dimensiju iestatīšana

Piemēra sistēmā ir ietverti šādi glabāšanas dimensiju iestatījumi.

| Vārds/nosaukums      | Aktīva | Fizisks krājums | Finanšu krājumi |
|-----------|--------|--------------------|---------------------|
| Vietne      | Jā    | Jā                | Jā                 |
| Noliktava | Jā    | Jā                | Nē                  |

### <a name="inventory-model"></a>Krājumu modelis

Piemēra sistēmai izlaisto preču krājumu modelis ir *FIFO*, un **Izmaksu cenas** iestatījums krājumu modelim ir *Ietver fizisko vērtību*.

### <a name="inventory-transactions"></a>Krājumu transakcijas

Piemēra sistēmā ir iekļautas šādas krājumu darbības izlaistam produktam ar krājuma numuru *1000*.

| Atsauce      | Vietne | Noliktava | Pirkš.pas. ieejas plūsma   | Izsniegt | Fiziskais datums | Finansiālais datums | Daudzums | Izmaksu summa | Fiziskā izmaksu summa |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Pirkšanas pasūtījums | 1    | 11.        | Nopirkts |       | 15. marts      | 15. marts       | 10.       | 1000       | 1000                |
| Pirkšanas pasūtījums | 2    | 21        | Nopirkts |       | 15. marts      | 15. marts       | 10.       | 2,000       | 2,000                |
| Pirkšanas pasūtījums | 1    | 11.        | Saņemts  |       | 15. aprīlis      |                | 5        |             | 375                  |
| Pārsūtīšanas pasūtījums | 1    | 11.        |           | Pārdots  | 2. maijs         | 2. maijs          | -5       | -458,33     | -458,33              |
| Pārsūtīšanas pasūtījums | 1    | 12.        | Nopirkts |       | 2. maijs         | 2. maijs          | 5        | 458.33      | 458.33               |
| Pārdošanas pasūtījums    | 1    | 12.        |           | Pārdots  | 3. maijs         | 3. maijs          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Kā tiek aprēķināti katra perioda intervāla daudzumi un summas

Izmantojot datu paraugus, kas aprakstīti iepriekšējās sadaļās, varat palaist **Krājumu vecumstruktūras** pārskatu, kam ir šādi iestatījumi:

- **Datums:** *2020. gada 9. maijs*
- **Vietne:** *Skatīt*
- **Noliktava:** *Nē*
- **Krājuma numurs:** *Kopā*
- **vecumstruktūras periods:** Iestatiet šo lauku, lai ģenerētu mēneša intervālus.

Šādā gadījumā ģenerētā pārskata saturs būs līdzīgs šim piemēram.

<table>
<thead>
<tr>
    <th rowspan="2">Krājums</th>
    <th rowspan="2">Vietne</th>
    <th rowspan="2">Rīcībā esošais daudzums</th>
    <th rowspan="2">Rīcībā esošā vērtība</th>
    <th rowspan="2">Krājumu vērtības daudzums</th>
    <th rowspan="2">Krājumu vērtība</th>
    <th rowspan="2">Vidējās vienības izmaksas</th>
    <th colspan="2">8/5/2020 - 1/5/2020</th>
    <th colspan="2">30/04/2020 - 1/04/2020</th>
    <th colspan="2">31/03/2020 - 1/03/2020</th>
</tr>
<tr>
    <th>P1: Daudzums</th>
    <th>P1: Summa</th>
    <th>P2: Daudzums</th>
    <th>P2: Summa</th>
    <th>P3: Daudzums</th>
    <th>P3: Summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14.</td>
    <td>1,283.33</td>
    <td>14.</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10.</td>
    <td>2,000.00</td>
    <td>10.</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Kopsummas</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Ievērojiet šajā piemēra pārskatā norādīto informāciju:

- **Krājumu vērtības daudzums**, **Krājumu vērtība** un **Vidējās vienības izmaksu** vērtības, kas tiek rādītas pārskatā, ir finanšu krājumu dimensijas (šajā gadījumā **Vietnes**) vērtības.

    Piemēram, 1. vietnei pārskats rāda sekojošo informāciju:

    - **Krājumu vērtības daudzuma** vērtība ir *14* (= 10 + 5 – 5 + 5 – 1).
    - **Krājumu vērtības** vērtība ir *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).
    - **Vidējā vienības izmaksu** vērtība ir *91,67*.
    - **Rīcībā esošā vērtības** vērtība un **Summas** vērtība katrā perioda intervālā tiek aprēķināta, izmantojot **Vidējo vienības izmaksu** vērtību.

- Pārskats nosaka rīcībā esošo daudzumu katram perioda intervālam, apkopojot visu saņemto krājumu daudzumu katram periodam. Pēc tam tas piemēro principu “pirmais iekšā, pirmais ārā” (FIFO), lai atskaitītu kopējo izdoto daudzumu neatkarīgi no krājuma modeļa, kuru izmanto preces.

Palaižot vienu un to pašu pārskatu, bet šoreiz iestatot gan **Vietnes**, gan **Noliktavas** laukus uz *Skatīt*, jaunais pārskats būs līdzīgs šim piemēram.

<table>
<thead>
<tr>
    <th rowspan="2">Krājums</th>
    <th rowspan="2">Vietne</th>
    <th rowspan="2">Noliktava</th>
    <th rowspan="2">Rīcībā esošais daudzums</th>
    <th rowspan="2">Rīcībā esošā vērtība</th>
    <th rowspan="2">Krājumu vērtības daudzums</th>
    <th rowspan="2">Krājumu vērtība</th>
    <th rowspan="2">Vidējās vienības izmaksas</th>
    <th colspan="2">8/5/2020 - 1/5/2020</th>
    <th colspan="2">30/04/2020 - 1/04/2020</th>
    <th colspan="2">31/03/2020 - 1/03/2020</th>
</tr>
<tr>
    <th>P1: Daudzums</th>
    <th>P1: Summa</th>
    <th>P2: Daudzums</th>
    <th>P2: Summa</th>
    <th>P3: Daudzums</th>
    <th>P3: Summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11.</td>
    <td>10.</td>
    <td>916.67</td>
    <td>14.</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12.</td>
    <td>4.</td>
    <td>366.67</td>
    <td>14.</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10.</td>
    <td>2,000.00</td>
    <td>10.</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Kopsummas</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Šoreiz 1. vietne ir sadalīta divās rindās — viena 11. noliktavai un otra 12. noliktavai. Tomēr **Krājumu vērtības daudzums**, **Krājumu vērtība** un **Vidējās vienības izmaksu** vērtības ir vienādas, jo **Noliktava** nav finanšu krājumu dimensija.

Turklāt ņemiet vērā, ka 1. vietnes daudzuma sadale atšķiras. Pirmajā jūsu veiktajā pārskatā sistēma ignorēja pārsūtīšanas pasūtījumu, kas notika vienā un tajā pašā vietā, un atskaitīja pārdošanas rēķina daudzumu no **31/03/2020-1/03/2020** perioda kopuma 1. vietnē. Tomēr jaunajā pārskatā sistēma atņem pārdošanas rēķina daudzumu no **8/05/2020-1/05/2020** perioda intervāla 12. noliktavā.

## <a name="effects-of-inventory-closing"></a>Krājumu slēgšanas sekas

Ja palaižat krājumu slēgšanu maijam un pēc tam vēlreiz palaižat iepriekšējo pārskatu, bet, iestatāt **Datuma** lauku uz *2020. gada 31. maiju*, jūs ievērosit šādus rezultātus:

- **Krājumu vērtības** un **Vidējās vienības izmaksu** vērtības tiek atjauninātas.
- **Rīcībā esošā vērtības** vērtība un visas **Summas** vērtības katrā perioda intervālā tiek attiecīgi atjauninātas.

Jaunais pārskats izskatīsies līdzīgi kā tālāk sniegtais piemērs.

<table>
<thead>
<tr>
    <th rowspan="2">Krājums</th>
    <th rowspan="2">Vietne</th>
    <th rowspan="2">Noliktava</th>
    <th rowspan="2">Rīcībā esošais daudzums</th>
    <th rowspan="2">Rīcībā esošā vērtība</th>
    <th rowspan="2">Krājumu vērtības daudzums</th>
    <th rowspan="2">Krājumu vērtība</th>
    <th rowspan="2">Vidējās vienības izmaksas</th>
    <th colspan="2">31/05/2020 - 1/05/2020</th>
    <th colspan="2">30/04/2020 - 1/04/2020</th>
    <th colspan="2">31/03/2020 - 1/03/2020</th>
</tr>
<tr>
    <th>P1: Daudzums</th>
    <th>P1: Summa</th>
    <th>P2: Daudzums</th>
    <th>P2: Summa</th>
    <th>P3: Daudzums</th>
    <th>P3: Summa</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11.</td>
    <td>10.</td>
    <td>910.70</td>
    <td>14.</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0.00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12.</td>
    <td>4.</td>
    <td>364.29</td>
    <td>14.</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10.</td>
    <td>2,000.00</td>
    <td>10.</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Kopsummas</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]