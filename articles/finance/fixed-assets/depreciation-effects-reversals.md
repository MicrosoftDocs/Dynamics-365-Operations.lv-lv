---
title: Nolietojuma ietekmes ar apgriešanām
description: Šajā rakstā ir apspriesta pamatlīdzekļu transakcijas atcelšanas potenciālā ietekme.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f0eeaafe7538b6aeeadfc804096ecee11e714da
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714206"
---
# <a name="depreciation-effects-with-reversals"></a>Nolietojuma ietekmes ar apgriešanām

[!include [banner](../includes/banner.md)]

Šajā rakstā ir apspriesta pamatlīdzekļu transakcijas atcelšanas potenciālā ietekme. 

Varat apgriezt pamatlīdzekļu transakcijas, kā arī transakcijas, kas ir saistītas ar kādu pamatlīdzekli. Apgrieztu transakciju varat arī atcelt. 

Varat apgriezt vai atcelt transakciju, kas nav visjaunākā transakcija, kura tika grāmatota grāmatā par šo līdzekli. Jums vispirms ir jānosaka, vai pēc transakcijas, kurai veicat apgriešanu, tika grāmatotas kādas nolietojuma transakcijas. Tas nepieciešams tāpēc, ka pēc transakcijas apgriešanas nolietojums netiek pārrēķināts. Šī iemesla dēļ pēc apgriešanas nolietojums bieži tiek pārvērtēts vai novērtēts nepietiekami, kā parādīts piemēros. 

Lai nodrošinātu, ka nolietojums ir pareizs, kad veicat transakcijas apgriešanu, neturpiniet apgriešanu, ja saņemat ziņojumu, ka nolietojums netiks pārrēķināts. Tā vietā vispirms apgrieziet nolietojuma transakciju, kas tika grāmatota pēc tās transakcijas, kuru mēģinājāt apgriezt, un pēc tam turpiniet apgriešanas procesu. Jūs netiksiet brīdināts par nolietojuma pārrēķiniem un varat turpināt apgriešanu. 

Nākamajos piemēros ir parādīti aprēķini, kas rodas, ja pēc ziņojuma saņemšanas procedūru turpināt, neapgriežot nolietojuma transakcijas.

## <a name="example-1-depreciation-is-overstated"></a>1. piemērs. Nolietojums tiek pārvērtēts
Līdzeklis ir iestatīts ar 5 gadu lietošanas laiku un lineāro nolietojumu (60 nolietojuma periodi). Šajā piemērā nolietojums tiek pārvērtēts.
#### <a name="asset-transaction-history"></a>Līdzekļu darbību vēsture

| Datums       | Darbības tips                                                          | Summa                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. janvāris  | Pirkšana                                                               | 59 000,00                                 |
| 1. janvāris  | Kapitālās izmaksas                                                    | 1000,00                                  |
| 31. janvāris | Nolietojums (izveidots, izmantojot priekšlikumu vienam nolietojuma periodam) | 1000,00 Aprēķins: Atlikusī vērtība (59 000 + 1000) / Atlikušo nolietojuma periodu skaits (60) |

#### <a name="reversal-action"></a>Atgriezta darbība

| Datums      | Darījuma veids                | Summa    |
|-----------|---------------------------------|-----------|
| 1. janvāris | Kapitālo izmaksu atgriešana | -1000,00 |

#### <a name="depreciation-effect"></a>Nolietojuma ietekme

| Datums        | Darījuma veids        | Summa                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. februāris | Nolietojums (priekšlikums) | 983,05 Aprēķins: Atlikusī vērtība (59 000 - 1000 nolietojums) / Atlikušo nolietojuma periodu skaits (59) |

Nolietojums ir pārvērtēts par 16,95 (1000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a>2. piemērs. Nolietojums tiek nepietiekami novērtēts
Līdzeklis ir iestatīts ar 5 gadu lietošanas laiku un lineāro nolietojumu (60 nolietojuma periodi). Šajā piemērā nolietojums tiek nepietiekami novērtēts.
#### <a name="asset-transaction-history"></a>Līdzekļu darbību vēsture

| Datums       | Darījuma veids                                                          | Summa                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. janvāris  | Iegāde                                                               | 59 000,00                                   |
| 1. janvāris  | Vērtības samazināšana                                                     | 1000,00                                    |
| 31. janvāris | Nolietojums (izveidots, izmantojot priekšlikumu vienam nolietojuma periodam) | 966,67 Aprēķins: Atlikusī vērtība (59 000 - 1000) / Atlikušo nolietojuma periodu skaits (60) |

#### <a name="reversal-action"></a>Atgriezta darbība

| Datums      | Darījuma veids               | Summa    |
|-----------|--------------------------------|-----------|
| 1. janvāris | Vērtības samazināšanas apgriešana | -1000,00 |

#### <a name="depreciation-effect"></a>Nolietojuma ietekme

| Datums        | Darījuma veids        | Summa                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. februāris | Nolietojums (priekšlikums) | 983,62 Aprēķins: Atlikusī vērtība (59 000 - 966,67 nolietojums) / Atlikušo nolietojuma periodu skaits (59) |

Nolietojums ir nepietiekami novērtēts par 16,95 (983,62 - 966,67).



## <a name="additional-resources"></a>Papildu resursi

[Pamatlīdzekļu nolietojums](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
