---
title: PVN kodu visas summas un intervāla aprēķināšanas opcijas
description: Šajā raksta ir aprakstītas lauka Aprēķina metode opcijas, kas attiecas uz PVN kodiem, un izskaidrots kā tiek aprēķināts intervālu un visu summu PVN.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b81780e60825021ad7a700d85257ba0f5a2447a
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715282"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>PVN kodu visas summas un intervāla aprēķināšanas opcijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrotas opcijas PVN **kodu laukā** Aprēķināšanas metode un kā PVN tiek aprēķināts intervāliem un veselām summām.

Varat iestatīt PVN kodu tā, lai tas tiktu aprēķināts, pamatojoties uz visu summu vai intervāla summu. Lapā **PVN kodi** izmantojiet lauku **Aprēķina metode** kopsavilkuma cilnē **Aprēķins**, lai izvēlētos PVN koda aprēķina metodi.
- Visa summa — nodokļa likme tiek lietota visai apliekamajai summai.
- Intervāls — apliekamā summa tiek sadalīta daļās, katra no kurām atbilst diapazonam ar noteiktu PVN likmi. Summas daļa, kas atbilst noteiktam intervālam, tiek aplikta ar nodokļiem saskaņā ar šī intervāla nodokļa likmi. PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.
  > [!NOTE]                                                                                                                              
  > Opcija Intervāls ir pieejama tikai tad, ja lapas Virsgrāmatas parametri apgabalā PVN ir atlasīta lauka Aprēķina metode vērtība Rinda. 

Intervālus var iestatīt lapā PVN koda vērtības, ievadot minimālā un maksimālā ierobežojuma summu katrai nodokļa likmei. Lai nodokļi tiktu aprēķināti visai apliekamajai summai neatkarīgi no atlasītās aprēķina metodes, intervāliem ir jāatbilst tālāk norādītajiem nosacījumiem.
-   Pirmā intervāla minimālā ierobežojuma vērtībai ir jābūt nulle.
-   Pēdējā intervāla maksimālā ierobežojuma vērtībai ir jābūt nulle, kas norāda bezgalību.
-   Intervāla maksimālā ierobežojuma vērtībai ir jābūt vienādai ar nākamā intervāla minimālā ierobežojuma vērtību.

Ja summa ir vienāda ar iepriekšējā intervāla maksimālā ierobežojuma vērtību un nākamā intervāla minimālā ierobežojuma vērtību, summai tiek lietota pirmā intervāla PVN likme. Ja summa neatbilst intervāliem, kas ir definēti ar maksimālā un minimālā ierobežojuma vērtībām, tiek lietota PVN likme nulle.

## <a name="example-whole-amount-method-of-calculation"></a>Piemērs: visas summas aprēķina metode
Lapā PVN koda vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.

| Minimālā robeža     | Maksimālā robeža     | Nodokļa likme     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

PVN tiek aprēķināts visai apliekamajai summai.

| Apliekamā summa (cena) | Aprēķins    | PVN |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Piemērs: intervāla aprēķina metode
Lapā Vērtības tiek iestatītas PVN likmes tālāk norādītajos intervālos.

| Minimālā robeža     | Maksimālā robeža     | Nodokļa likme     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

PVN likme ir summa no visiem nodokļu daudzumiem, kas tiek aprēķināti katram daudzuma intervālam.

| Apliekamā summa (cena) | Aprēķins                                                               | PVN |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Papildinformāciju skatiet [Nodokļu likmes, kuru pamatā ir maržinālā bāze un aprēķināšanas metodes](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
