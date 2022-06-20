---
title: PVN aprēķināšana un noapaļošana
description: Šajā rakstā sniegts PĀRSKATS par PVN aprēķināšanu un noapaļošanu un skaidroti PVN aprēķināšanas un noapaļošanas iestatījumu parametri.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939238"
---
# <a name="sales-tax-calculation-and-rounding"></a>PVN aprēķināšana un noapaļošana

[!include [banner](../includes/banner.md)]

Šis raksts sniedz apskatu par PVN aprēķināšanu un noapaļošanu Microsoft Dynamics 365 Finansēs. Šeit skaidroti parametri, kas tiek izmantoti PVN aprēķināšanas un noapaļošanas iestatījumos, un to, kā šie parametri darbojas kopā.

## <a name="parameters"></a>Parametri

Vairāki parametri kontrolē PVN aprēķināšanu un noapaļošanu:

- **Aprēķina metode** - Šis parametrs ir iestatīts **Virsgrāmatas** parametru lapā un nosaka, vai nodokļu pamatsumma tiek aprēķināta dokumentam vai rindai. Ja PVN **koda aprēķina pamata** parametrs **ir** iestatīts uz rēķina bilances neto summu, nodokļu pamatsumma vienmēr tiek aprēķināta katram dokumentam, neņemot vērā šī parametra iestatījumu.
- **Noapaļošana pēc** – šis parametrs ir iestatīts PVN grupai un nosaka, vai PVN summa tiek noapaļota uz PVN kodu vai uz PVN kodu kombināciju.
- **Izcelsme** – šis parametrs ir iestatīts PVN kodam un nosaka veidu, kādā tiek aprēķināta nodokļa summa. Plašāku informāciju skatiet PVN [aprēķināšanas metodēm laukā Izcelsme](sales-tax-calculation-methods-origin-field.md).
- **Aprēķina pamatā** – šis parametrs ir iestatīts PVN kodam un nosaka, kura summa tiek izmantota, lai atlasītu atbilstošās **nodokļu likmes PVN koda vērtību** lapā. Papildinformāciju skatiet [Nodokļu likmes, kuru pamatā ir maržinālā bāze un aprēķināšanas metodes](marginal-base-field.md).
- **PVN noapaļošanas noteikums** – šis parametrs ir iestatīts PVN kodam un nosaka, kā noteiktā PVN summa tiek noapaļota, ieskaitot noapaļošanas precizitāti un noapaļošanas metodi.

Pārējie šī raksta piemēri ir daži tipiski PVN aprēķināšanas un noapaļošanas piemēri, kas izmanto iepriekšējo parametru kombināciju.

## <a name="scenario-for-the-examples"></a>Piemēro scenārijs

- Apliekamajā dokumentā ir divas rindas, un nodokļa pamatsumma katrai rindai ir 42,42.
- Katrai rindai ir definēti divi PVN kodi: 1. PVN kods un 2. PVN kods.
- Nodokļa likme 1. un 2. nodokļa kodam ir 10 procenti.
- Cena neietver nodokli.
- Noapaļošanas precizitāte ir 0,01.
- Noapaļošanas metode ir **Noapaļošana**.

## <a name="example-1"></a>1. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz    | Izcelsme                   | Aprēķina pamatā       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Rinda               | PVN kods | Procenti no neto summas | Neto summa rindai |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ------------| ---------------| --------------| -----------------|
| 1           | 1. kods         | 42.42         | 4.25             |
| 1           | 2. kods         | 42.42         | 4.25             |
| 2           | 1. kods         | 42.42         | 4.25             |
| 2           | 2. kods         | 42.42         | 4.25             |

Nodokļa pamatsumma tiek aprēķināta katrai rindai:

- **1. rinda:** 42.42
- **2. rinda:** 42.42

Nodokļa summa tiek aprēķināta uz PVN kodu:

- **1. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti = 4,242
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti = 4,242

- **2. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti = 4,242
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti = 4,242

Nodokļu summa tiek noapaļota uz VIENU PVN kodu:

- **1. rinda**

    - Noapaļotā nodokļa summa PVN kodam 1 = 4,25
    - Noapaļotā nodokļa summa PVN kodam 2 = 4,25

- **2. rinda**

    - Noapaļotā nodokļa summa PVN kodam 1 = 4,25
    - Noapaļotā nodokļa summa PVN kodam 2 = 4,25

## <a name="example-2"></a>2. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz    | Izcelsme                   | Aprēķina pamatā                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Rinda/Kopsumma         | PVN kods | Procenti no neto summas | Rēķina bilances neto summa |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.25             |
| 1           | 2. kods         | 42.42         | 4.25             |
| 2           | 1. kods         | 42.42         | 4.24             |
| 2           | 2. kods         | 42.42         | 4.24             |

Nodokļu bāzes summa tiek aprēķināta par dokumentu:

- Nodokļa pamatsumma = 42,42 + 42,42 = 84,84

Nodokļa summa tiek aprēķināta uz PVN kodu:

- Nodokļa summa PVN kodam 1 = 84,84 &times; 10 procenti = 8,484
- Nodokļa summa PVN kodam 2 = 84,84 &times; 10 procenti = 8,484

Nodokļu summa tiek noapaļota uz VIENU PVN kodu:

- Noapaļotā nodokļa summa PVN kodam 1 = 8,49
- Noapaļotā nodokļa summa PVN kodam 2 = 8,49

Noapaļotā nodokļa summa tiek sadalīta katrā rindā uz PVN kodu:

- Sadaliniet noapaļoto nodokļa summu PVN kodam 1 (8,49) uz 1. rindu (4,25) un 2. rindu (4,24).
- Sadaliniet noapaļoto nodokļa summu PVN kodam 2 (8,49) uz 1. rindu (4,25) un 2. rindu (4,24).

## <a name="example-3"></a>3. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz    | Izcelsme                              | Aprēķina pamatā       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Rinda               | PVN kods | Neto summai aprēķinātie procenti | Neto summa rindai |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.72             |
| 1           | 2. kods         | 42.42         | 4.72             |
| 2           | 1. kods         | 42.42         | 4.72             |
| 2           | 2. kods         | 42.42         | 4.72             |

Nodokļa pamatsumma tiek aprēķināta katrai rindai:

- **1. rinda:** 42.42
- **2. rinda:** 42.42

Nodokļa summa tiek aprēķināta uz PVN kodu:

- **1. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133

- **2. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133

Nodokļu summa tiek noapaļota uz VIENU PVN kodu:

- **1. rinda**

    - Noapaļotā nodokļa summa PVN kodam 1 = 4,72
    - Noapaļotā nodokļa summa PVN kodam 2 = 4,72

- **2. rinda**

    - Noapaļotā nodokļa summa PVN kodam 1 = 4,72
    - Noapaļotā nodokļa summa PVN kodam 2 = 4,72

## <a name="example-4"></a>4. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz    | Izcelsme                              | Aprēķina pamatā                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Rinda/Kopsumma         | PVN kods | Neto summai aprēķinātie procenti | Rēķina bilances neto summa |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.72             |
| 1           | 2. kods         | 42.42         | 4.72             |
| 2           | 1. kods         | 42.42         | 4.71             |
| 2           | 2. kods         | 42.42         | 4.71             |

Nodokļu bāzes summa tiek aprēķināta par dokumentu:

- Nodokļa pamatsumma = 42,42 + 42,42 = 84,84

Nodokļa summa tiek aprēķināta uz PVN kodu:

- Nodokļa summa PVN kodam 1 = 84,84 &times; 10 procenti &divide; (1 – 10 procenti) = 9,4267
- Nodokļa summa PVN kodam 2 = 84,84 &times; 10 procenti &divide; (1 – 10 procenti) = 9,4267

Nodokļu summa tiek noapaļota uz VIENU PVN kodu:

- Noapaļotā nodokļa summa PVN kodam 1 = 9,43
- Noapaļotā nodokļa summa PVN kodam 2 = 9,43

Noapaļotā nodokļa summa tiek sadalīta katrā rindā uz PVN kodu:

- Piešķiriet nodokļa summu PVN kodam 1 (9,43) 1. rindai (4,72) un 2. rindai (4,71).
- Piešķiriet nodokļa summu PVN kodam 2 (9,43) 1. rindai (4,72) un 2. rindai (4,71).

## <a name="example-5"></a>5. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz                | Izcelsme                   | Aprēķina pamatā       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Rinda               | PVN kombinācijas | Procenti no neto summas | Neto summa rindai |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.25             |
| 1           | 2. kods         | 42.42         | 4.24             |
| 2           | 1. kods         | 42.42         | 4.24             |
| 2           | 2. kods         | 42.42         | 4.24             |

Nodokļa pamatsumma tiek aprēķināta katrai rindai:

- **1. rinda:** 42.42
- **2. rinda:** 42.42

Nodokļa summa tiek aprēķināta uz PVN kodu:

- **1. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti = 4,242
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti = 4,242

- **2. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti = 4,242
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti = 4,242

Nodokļu summa tiek noapaļota uz PVN kombinācijas:

- Kopējā PVN summa = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, kas tiek noapaļota uz 16,97

Noapaļotā nodokļa summa tiek sadalīta katrā rindā uz PVN kodu:

- Piešķiriet PVN summu (16,97) 1. rindai un 2. rindai:

    - **1. rinda**

        - Nodokļa summa PVN kodam 1 = 4,25
        - Nodokļa summa PVN kodam 2 = 4,24

    - **2. rinda**

        - Nodokļa summa PVN kodam 1 = 4,24
        - Nodokļa summa PVN kodam 2 = 4,24

## <a name="example-6"></a>6. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz                | Izcelsme                   | Aprēķina pamatā                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Rinda/Kopsumma         | PVN kombinācijas | Procenti no neto summas | Rēķina bilances neto summa |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.25             |
| 1           | 2. kods         | 42.42         | 4.24             |
| 2           | 1. kods         | 42.42         | 4.24             |
| 2           | 2. kods         | 42.42         | 4.24             |

Nodokļu bāzes summa tiek aprēķināta par dokumentu:

- Nodokļa pamatsumma = 42,42 + 42,42 = 84,84

Nodokļa summa tiek aprēķināta uz PVN kodu:

- Nodokļa summa PVN kodam 1 = 84,84 &times; 10 procenti = 8,484
- Nodokļa summa PVN kodam 2 = 84,84 &times; 10 procenti = 8,484

Nodokļu summa tiek noapaļota uz PVN kombinācijas:

- Kopējā PVN summa = 8,484 + 8,484 = 16,968, kas tiek noapaļota uz 16,97

Noapaļotā nodokļa summa tiek sadalīta katrā rindā uz PVN kodu:

- Piešķiriet PVN summu (16,97) 1. rindai un 2. rindai:

    - **1. rinda**

        - Nodokļa summa PVN kodam 1 = 4,25
        - Nodokļa summa PVN kodam 2 = 4,24

    - **2. rinda**

        - Nodokļa summa PVN kodam 1 = 4,24
        - Nodokļa summa PVN kodam 2 = 4,24

## <a name="example-7"></a>7. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz                | Izcelsme                              | Aprēķina pamatā       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Rinda               | PVN kombinācijas | Neto summai aprēķinātie procenti | Neto summa rindai |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.72             |
| 1           | 2. kods         | 42.42         | 4.71             |
| 2           | 1. kods         | 42.42         | 4.71             |
| 2           | 2. kods         | 42.42         | 4.72             |

Nodokļa pamatsumma tiek aprēķināta katrai rindai:

- **1. rinda:** 42.42
- **2. rinda:** 42.42

Nodokļa summa tiek aprēķināta uz PVN kodu:

- **1. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133

- **2. rinda**

    - Nodokļa summa PVN kodam 1 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133
    - Nodokļa summa PVN kodam 2 = 42,42 &times; 10 procenti &divide; (1 – 10 procenti) = 4,7133

Nodokļu summa tiek noapaļota uz PVN kombinācijas:

- Kopējā PVN summa = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, kas tiek noapaļota uz 18,86

Noapaļotā nodokļa summa tiek sadalīta katrā rindā uz PVN kodu:

- Piešķiriet PVN summu (18,86) 1. rindai un 2. rindai:

    - **1. rinda**

        - Nodokļa summa PVN kodam 1 = 4,72
        - Nodokļa summa PVN kodam 2 = 4,71

    - **2. rinda**

        - Nodokļa summa PVN kodam 1 = 4,71
        - Nodokļa summa PVN kodam 2 = 4,72

## <a name="example-8"></a>8. piemērs

### <a name="parameter-values"></a>Parametru vērtības

| Aprēķina metode | Noapaļošana uz                | Izcelsme                              | Aprēķina pamatā                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Rinda/Kopsumma         | PVN kombinācijas | Neto summai aprēķinātie procenti | Rēķina bilances neto summa |

### <a name="calculation-and-rounding-behavior"></a>Aprēķina un noapaļošanas uzvedība

| Rindas numurs | PVN kods | Summas izcelsme | PVN summa |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | 1. kods         | 42.42         | 4.72             |
| 1           | 2. kods         | 42.42         | 4.71             |
| 2           | 1. kods         | 42.42         | 4.71             |
| 2           | 2. kods         | 42.42         | 4.72             |

Nodokļu bāzes summa tiek aprēķināta par dokumentu:

- Nodokļa pamatsumma = 42,42 + 42,42 = 84,84

Nodokļa summa tiek aprēķināta uz PVN kodu:

- Nodokļa summa PVN kodam 1 = 84,84 &times; 10 procenti &divide; (1 – 10 procenti) = 9,4267
- Nodokļa summa PVN kodam 2 = 84,84 &times; 10 procenti &divide; (1 – 10 procenti) = 9,4267

Nodokļu summa tiek noapaļota uz PVN kombinācijas:

- Kopējā PVN summa = 9,4267 + 9,4267 = 18,8534, kas tiek noapaļota uz 18,86

Noapaļotā nodokļa summa tiek sadalīta katrā rindā uz PVN kodu:

- Piešķiriet PVN summu (18,86) 1. rindai un 2. rindai:

    - **1. rinda**

        - Nodokļa summa PVN kodam 1 = 4,72
        - Nodokļa summa PVN kodam 2 = 4,71

    - **2. rinda**

        - Nodokļa summa PVN kodam 1 = 4,71
        - Nodokļa summa PVN kodam 2 = 4,72

## <a name="additional-resources"></a>Papildu resursi

- [PVN aprēķināšanas metodes laukā Izcelsme](sales-tax-calculation-methods-origin-field.md)
- [PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode](marginal-base-field.md)
- [Visas summas un intervāla aprēķināšanas opcijas PVN kodiem](whole-amount-interval-options-sales-tax-codes.md)
