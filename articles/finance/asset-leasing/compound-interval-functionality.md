---
title: Pievienošanas intervālu funkcionalitāte
description: Šis raksts sniedz informāciju, kas palīdzēs izvēlēties starp mēneša, ceturkšņa, pusgada un gada pievienošanas intervāliem.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2de5f1e9d52de41388298031a03fbc487a1b1cde
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886427"
---
# <a name="compounding-interval-functionality"></a>Pievienošanas intervālu funkcionalitāte

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šis raksts sniedz informāciju, kas palīdzēs izvēlēties starp mēneša, ceturkšņa, pusgada un gada pievienošanas intervāliem. Pievienošanas intervāla funkcionalitāti izmanto, lai nomas maksājumu grafikā noteiktu pievienošanas periodu skaitu gadā. Katrs no četriem piemēriem šajā rakstā parāda, kā izskatīsies nomas maksājumu grafiks ar citu intervālu.

Nav iespējams atlasīt pievienošanas intervālu, kas ir retāks nekā nomas maksājuma biežums. Piemēram, ceturkšņa pievienošanas intervālu nevar izmantot ar ikmēneša maksājuma biežumu, un gada pievienošanas intervālu nevar izmantot ar pusgada maksājuma biežumu. Ja mēģināsiet atlasīt pievienošanas intervālu, kas ir retāks nekā nomas maksājuma biežums, saņemsiet kļūdas ziņojumu.

> [!NOTE]
> Visos četros piemēros šim rakstam saliktais intervāls atbilst maksājuma biežumam.

## <a name="examples"></a>Piemēri

### <a name="setup-for-all-four-leases"></a>Visu četru nomu iestatīšana

Tabulās ir parādītas vērtības, kas ir iestatītas cilnēs **Vispārīgi** un **Maksājumu grafika rindas** šīm četrām nomām, kas tiek izmantotas piemēros.

**Cilne Vispārīgi**

| Lauks                      | Vērtība                        |
|----------------------------|------------------------------|
| Salīdzināmā aizņēmuma procentu likme | **5 %**                       |
| Gada maksājuma veids               | **Parastais gada maksājums**         |
| Pievienošanas intervāls       | Aplūkojiet atsevišķus piemērus. |
| Maksājumu biežums          | **Mēnesis**                  |
| Sākuma datums          | **01.01.2020.**                 |

**Cilne Maksājumu grafika rindas**

| Lauks             | Vērtība                        |
|-------------------|------------------------------|
| Sākuma datums        | **01.01.2020.**                 |
| Periodi           | **120**                      |
| Perioda intervāls   | **Mēneši**                   |
| Beigu datums          | **31.12.2029.**               |
| Maksājumu biežums | Aplūkojiet atsevišķus piemērus. |
| Maksājuma summa    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>1. noma: ikmēneša pievienošanas intervāls un ikmēneša maksājuma biežums

Tālāk redzamajā tabulā ir uzskaitīti maksājumu grafika pirmie 12 mēneši. Ņemiet vērā tālāk norādīto informāciju.

- Vērtība kolonnā "Periods" katru mēnesi palielinās par 1, jo katrs mēnesis ir jauns pievienošanas intervāls.
- Kolonnas "Pašreizējā vērtība" formulā likme tiek dalīta ar 12, jo ir 12 pievienošanas periodi gadā. Kāpinātājs (tas ir, augšraksta cipars) ir vienāds ar vērtību kolonnā "Periods".

| Periods | mēnesis; | Datums       | Maksājuma summa | Pašreizējā vērtība                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31.01.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>1</sup> = 49 792,53  |
| 2      | 2     | 29.02.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>2</sup> = 49 585,92  |
| 3      | 3     | 31.03.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>3</sup> = 49 380,17  |
| 4      | 4     | 30.04.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>4</sup> = 49 175,28  |
| 5      | 5     | 31.05.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>5</sup> = 48 971,23  |
| 6      | 6     | 30.06.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>6</sup> = 48 768,03  |
| 7      | 7     | 31.07.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>7</sup> = 48 565,67  |
| 8      | 8     | 31.08.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>8</sup> = 48 364,15  |
| 9      | 9     | 30.09.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>9</sup> = 48 163,47  |
| 10.     | 10.    | 31.10.2020. | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>10</sup> = 47 963,62 |
| 11.     | 11.    | 30.11.2020. | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>11</sup> = 47 764,61 |
| 12.     | 12.    | 31.12.2020. | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>12</sup> = 47 566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>2. noma: ceturkšņa pievienošanas intervāls un ceturkšņa maksājuma biežums

Tālāk redzamajā tabulā ir uzskaitīti maksājumu grafika pirmie 12 mēneši. Ņemiet vērā tālāk norādīto informāciju.

- Vērtība kolonnā "Periods" katrus trīs mēnešus palielinās par 1 (t.i., katru ceturksni), jo katrs ceturksnis ir jauns pievienošanas intervāls.
- Kolonnas "Pašreizējā vērtība" formulā likme tiek dalīta ar 4, jo ir četri pievienošanas periodi gadā. Kāpinātājs ir vienāds ar vērtību kolonnā "Periods".

| Periods | mēnesis; | Datums       | Maksājuma summa | Pašreizējā vērtība                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 49 382,72 |
| 2      | 4     | 30.04.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31.05.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30.06.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 48 773,05 |
| 3      | 7     | 31.07.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31.08.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30.09.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 48 170,92 |
| 4      | 10.    | 31.10.2020. | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11.    | 30.11.2020. | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12.    | 31.12.2020. | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 47 576,21 |

> [!NOTE]
> Ja gada maksājuma veids tiek mainīts uz **Gada maksājuma termiņš**, maksājums būs ceturkšņa sākumā, nevis ceturkšņa beigās.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>3. noma: pusgada pievienošanas intervāls un pusgada maksājuma biežums

Tālāk redzamajā tabulā ir uzskaitīti maksājumu grafika pirmie 12 mēneši. Ņemiet vērā tālāk norādīto informāciju.

- Vērtība kolonnā "Periods" katrus sešus mēnešus palielinās par 1 (t.i., reizi pusgadā), jo katrs pusgads ir jauns pievienošanas intervāls.
- Kolonnas "Pašreizējā vērtība" formulā likme tiek dalīta ar 2, jo ir divi pievienošanas periodi gadā. Kāpinātājs ir vienāds ar vērtību kolonnā "Periods".

| Periods | mēnesis; | Datums       | Maksājuma summa | Pašreizējā vērtība                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020.  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 48 780,49 |
| 2      | 7     | 31.07.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31.08.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30.09.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10.    | 31.10.2020. | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11.    | 30.11.2020. | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12.    | 31.12.2020. | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 47 590,72 |

> [!NOTE]
> Ja gada maksājuma veids tiek mainīts uz **Gada maksājuma termiņš**, maksājums būs janvārī un jūlijā, nevis jūnijā un decembrī.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>4. noma: gada pievienošanas intervāls un gada maksājuma biežums

Tālāk redzamajā tabulā ir uzskaitīti maksājumu grafika pirmie 12 mēneši. Ņemiet vērā tālāk norādīto informāciju.

- Vērtība kolonnā "Periods" katrus 12 mēnešus palielinās par 1 (t.i., reizi gadā), jo katrs gads ir jauns pievienošanas intervāls.
- Kolonnas "Pašreizējā vērtība" formulā likme tiek dalīta ar 1, jo ir viens pievienošanas periods gadā. Kāpinātājs ir vienāds ar vērtību kolonnā "Periods".

| Periods | mēnesis; | Datums       | Maksājuma summa | Pašreizējā vērtība                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31.07.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31.08.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30.09.2020.  | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10.    | 31.10.2020. | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11.    | 30.11.2020. | 0.00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12.    | 31.12.2020. | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 47 619,05 |

> [!NOTE]
> Ja gada maksājuma veids tiek mainīts uz **Gada maksājuma termiņš**, maksājums būs janvārī, nevis decembrī.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
