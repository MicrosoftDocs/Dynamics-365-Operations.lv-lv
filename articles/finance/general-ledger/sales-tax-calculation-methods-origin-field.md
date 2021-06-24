---
title: PVN aprēķina metodes laukā Izcelsme
description: Šajā rakstā ir aprakstītas lauka Izcelsme opcijas PVN kodu lapā un kā PVN tiek aprēķināts atkarībā no atlasītās PVN koda opcijas.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e57e97847c6aa7a775b0f2639dff93f1e3a9e7a2
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189377"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>PVN aprēķina metodes laukā Izcelsme

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas lauka Izcelsme opcijas PVN kodu lapā un kā PVN tiek aprēķināts atkarībā no atlasītās PVN koda opcijas.

Katram lapā PVN kodi izveidotajam PVN kodam laukā Izcelsme ir jāatlasa aprēķina metode, kas tiek lietota nodokļu pamatsummai.

## <a name="percentage-of-net-amount"></a>Procenti no neto summas
Aprēķina metode Procenti no neto summas ir lauka Izcelsme noklusējuma vērtība. PVN tiek aprēķināts kā procenti no pirkšanas vai pārdošanas summas, neieskaitot nekādu citu PVN.
### <a name="example"></a>Paraugs

Nodokļa likme ir 25%. Rēķina rindā ir norādīts daudzums 10 vienības ar vienības cenu 1,00, un debitors var saņemt rindas atlaidi 10% Neto summa: (10 x 1,00) – 10% = 9,00 PVN: 9,00 x 25% = 2,25 Kopsumma: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a>Procenti no bruto summas
Ja atlasāt metodi Procenti no bruto summas, PVN tiek aprēķināts kā procenti no bruto pārdošanas summas. Bruto summa ir rindas neto summa, ieskaitot visus rindas nodokļus un nodevas, izņemot to vienu nodokli, kuram lauka Izcelsme vērtība ir Procenti no bruto summas.
### <a name="example"></a>Paraugs

Nodokļu iestāde krājumu ir aplikusi ar speciāliem nodokļiem. Šo nodokļu summa tiek pievienota neto summai pirms PVN aprēķināšanas. Tiek izmantoti tālāk norādītie PVN kodi.
-   1. NODOKLIS = 10%, izmantojot aprēķina metodi Procenti no neto summas
-   2. NODOKLIS = 20%, izmantojot aprēķina metodi Procenti no neto summas
-   PVN = 25%, izmantojot aprēķina metodi Procenti no bruto summas

Ja neto summa ir 10,00, tad 1. NODOKLIS ir 1,00 (10,00 x 10%) un 2. nodoklis ir 2,00 (10,00 x 20%). Tālāk ir norādītas summas. Bruto summa: neto summa + 1. NODOKĻA summa + 2. NODOKĻA summa (10,00 + 1,00 + 2,00) = 13,00 PVN: 13,00 x 25% = 3,25 NODOKĻI un PVN kopā: 1,00 + 2,00 + 3,25 = 6,25 Kopsumma: 10,00 + 6,25 = 16,25

| **Piezīme.**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transakcijai var izmantoti tikai vienu nodokļa kodu, kam ir iestatīta lauka Izcelsme vērtība Procenti no bruto summas. Ja transakcijai ir norādīti vairāki šādi nodokļu kodi, tiek parādīts kļūdas ziņojums par to, ka nevar aprēķināt PVN. |


## <a name="percentage-of-sales-tax"></a>PVN %

Ja atlasāt lauka Izcelsme vērtību PVN %, PVN tiek aprēķināts kā procenti no PVN, kas ir atlasīts laukā PVN uz PVN. Vispirms tiek aprēķināts PVN, kas ir atlasīts laukā PVN uz PVN. Pēc tam otrs PVN tiek aprēķināts, pamatojoties uz pirmā PVN summu.
### <a name="example"></a>Paraugs

Tiek izmantoti tālāk norādītie PVN kodi.
-   1. NODOKLIS = 10%, izmantojot metodi Procenti no neto summas
-   2. NODOKLIS = 20%, izmantojot metodi PVN %, ja lauka PVN uz PVN vērtība ir 1. nodoklis
-   PVN = 25%, izmantojot metodi Procenti no bruto summas

Neto summa: 10,00 1. NODOKLIS: 10,00 x 10% = 1,00 2. NODOKLIS: 1,00 x 20% = 0,20 Bruto summa: 10,00 + 1,00 + 0,20 = 11,20 PVN: 11,20 x 25% = 2,80 NODOKĻI un PVN kopā: 1,00+ 0,20 + 2,80 = 4,00 Kopsumma: 10,00 + 4,00 = 14,00

| **Piezīme.**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nevar veikt daudzlīmeņu nodokļa aprēķinu, pamatojoties uz nodokli. Nevar aprēķināt nodokli, pamatojoties uz nodokli, kas jau ir aprēķināts, pamatojoties uz citu nodokli. Transakcijai var veikt vairākus vienlīmeņa nodokļa koda aprēķinus, pamatojoties uz nodokli. |

## <a name="amount-per-unit"></a>Summa uz vienu vienību
Ja atlasāt lauka Izcelsme vērtību Sumam uz vienu vienību, PVN tiek aprēķināts kā fiksēta summa uz vienību, kas tiek reizināta ar dokumenta rindā ievadīto daudzumu. Laukā Vienība ir jāatlasa vienība. Summa uz vienu vienību tiek norādīta lapā PVN koda vērtības.
### <a name="example"></a>Paraugs

PVN kods ir iestatīts kā: USD 1,20 uz vienu vienību = kasti Pārdošanas rēķina rindā ir reģistrēta 25 krājuma kastu pārdošana PVN ir aprēķināts kā: 25 x1,20 =30,00

| **Piezīme.**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja transakcija ir ievadīta, izmantojot citu vienību, nevis PVN kodam norādīto vienību, tā tiek automātiski konvertēta, pamatojoties uz vienību konvertācijām, kas ir iestatītas lapā Mērvienību pārveidošana. |

###  <a name="amount-per-unit-additional-option"></a>Summa uz vienību, papildu opcija

Cilnē Aprēķins varat atlasīt, vai kā summa uz vienību aprēķinātais nodoklis tiek aprēķināts un pieskaitīts neto pirms citiem nodokļu kodiem un tiek pieskaitīts neto summai, pirms tiek aprēķināti citi nodokļu kodi, kuriem ir atlasīta lauka Izcelsme vērtība Procenti no neto summas.

### <a name="examples"></a>Piemēri

Pieņemsim, ka transakcijai tiek aprēķināti 2 nodokļu kodi.

-   NODOKLIS: lauka Izcelsme vērtība ir Summa uz vienu vienību un PVN, iestatītā vērtība ir 5,00 uz vienu vienību = gab.
-   PVN: lauka Izcelsme vērtība ir tāda, kā ir norādīts iepriekš sniegtajos piemēros, iestatītā vērtība ir 25%

Tiek pārdots 1 gab. krājuma par vienības cenu 10,00
#### <a name="example-1"></a>1. piemērs

PVN: lauka Izcelsme vērtība ir Procenti no bruto summas Opcija Aprēķināts pirms PVN aprēķināšanas neko neietekmē, jo PVN tiek aprēķināts kā procenti no bruto summas. NODOKLIS: 1 x 5,00 = 5,00 Bruto summa: 10,00 + 5,00 = 15,00 PVN: 15,00 x 25% = 3,75 PVN kopā: 5,00 + 3,75 = 8,75 Kopsumma: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>2. piemērs

PVN: lauka Izcelsme vērtība ir Procenti no neto summas NODOKĻA aprēķinam nav atlasīta opcija Aprēķināts pirms PVN aprēķināšanas. Neto summa: 10,00 NODOKLIS: 1 x 5,00 = 5,00 PVN: 10,00 x 25% = 2,50 PVN kopā: 5,00 + 2,50 = 7,50 Kopsumma: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>3. piemērs

PVN: lauka Izcelsme vērtība ir Procenti no neto summas NODOKĻA aprēķinam ir atlasīta opcija Aprēķināts pirms PVN aprēķināšanas. Neto summa: 10,00 NODOKLIS: 1 x 5,00 = 5,00 PVN: (10,00 + 5,00) x 25% = 3,75 PVN kopā: 5,00 + 3,75 = 8,75 Kopsumma: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>4. piemērs

3. un 1. piemēra rezultāti ir vienādi, jo ir tikai viens nodoklis. Pieņemsim, ka jums ir divi NODOKĻI un tikai viens no tiem ir iekļauts neto summā PVN aprēķinam. 1. NODOKLIS: 5,00, izmantojot metodi Summa uz vienu vienību un opciju Aprēķināts pirms PVN aprēķināšanas 2. NODOKLIS: 2,50, izmantojot metodi Summa uz vienu vienību un neizmantojot opciju Aprēķināts pirms PVN aprēķināšanas PVN: 25%, izmantojot metodi Procenti no neto summas Neto summa: 10,00 1. NODOKLIS: 1 x 5,00 = 5,00 2. NODOKLIS: 1 x 2,50 = 2,50 Ar PVN apliekamā neto summa: 10,00 + 5,00 = 15,00 PVN: 15,00 x 25% = 3,75 PVN kopā, ieskaitot nodokļus: 5,00 + 2,50 + 3,75 = 11,25 Kopsumma: 10,00 + 11,25 = 21,25 25% PVN tiek aprēķināts summai, ko veido neto summa (10,00) + 1. NODOKLIS (5,00) = 15,00. 2. NODOKLIS tiek pieskaitīts nodokļu summai pēc PVN aprēķināšanas.

## <a name="calculated-percentage-of-net-amount"></a>Neto summai aprēķinātie procenti
Izmantojot metodi Neto summai aprēķinātie procenti, nodokļu aprēķins tiek veikts atšķirīgi atkarībā no dokumenta vai žurnāla parametra Summas ietver PVN iestatījuma.
### <a name="example-1"></a>1. piemērs

Dokumentam/žurnālam ir iestatīta parametra Summas ietver PVN vērtība Jā Transakcijas rindas summa: 10,00 Nodokļa likme: 25% PVN: transakcijas rindas summa x nodokļa likme (10,00 x 25%) = 2,50 Nodokļa pamatsumma (sākotnējā summa): transakcijas rindas summa – PVN (10,00 – 2,50) = 7,50

### <a name="example-2"></a>2. piemērs

Dokumentam/žurnālam ir iestatīta parametra Summas ietver PVN vērtība Nē Transakcijas rindas summa: 10,00 Nodokļa likme: 25% PVN: (transakcijas rindas summa x nodokļa likme)/(100 – nodokļa likme) ((10,00 x 25%)/(100% – 25%)) = 3,33 Nodokļa pamatsumma (sākotnējā summa): transakcijas rindas summa = 10,00



## <a name="additional-resources"></a>Papildu resursi

[PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode](marginal-base-field.md)

[Visas summas un intervāla aprēķināšanas opcijas PVN kodiem](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]