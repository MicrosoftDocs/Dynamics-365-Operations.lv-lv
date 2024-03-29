---
title: Reizinātāja nolietojums
description: Šajā rakstā ir sniegts pārskats par koeficienta nolietojuma metodi.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbac1d84654673b3746887d943c0ecb530be4ae3
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713167"
---
# <a name="factor-depreciation"></a>Reizinātāja nolietojums

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par koeficienta nolietojuma metodi.

Koeficienti ir procenti, kurus lieto, lai pazeminātu pamatlīdzekļu vērtību. Ja iestatāt pamatlīdzekļa nolietojuma tabulu un lapā **Nolietojuma profili** atlasāt lauka **Metode** vērtību **Faktors**, varat iestatīt progresīvo, regresīvo vai lineāro nolietojumu.

-   Izmantojot progresīvo nolietojumu, katrā nolietojuma periodā palielinās nolietojuma summa.
-   Izmantojot regresīvo nolietojumu, katra perioda nolietojuma summa laika gaitā samazinās.
-   Izmantojot lineāro nolietojumu, visu periodu nolietojums ir vienāds.

Tālāk sniegtajos noteikumos un piemēros ir norādīts, kā varat iestatīt katra nolietojuma veida koeficientus. 

> [!NOTE] 
> Ja atlasāt lauka **Metode** vērtību **Koeficients**, tiek parādīts lauks **Koeficients** un lauks **Intervāls**.

## <a name="progressive-depreciation"></a>Progresīvais nolietojums
Lauka **Koeficients** vērtība ir lielāka nekā **50**.

### <a name="example"></a>Piemērs

Iegādes cena ir 100 000, koeficents ir 70, lietošanas ilgums ir 10 gadi, un nolietojums sākas 1. janvārī. Nolietojuma summas un atlikušās vērtības summas tiek rādītas vienīgi pirmajiem sešiem lietošanas ilguma gadiem.

| Gads | Periods      | Nolietojuma summa | Atlikušās vērtības summa |
|------|-------------|---------------------|-----------------------|
| 1    | 31. decembris | 307,69              | 99 692,31             |
| 2    | 31. decembris | 1 447,21            | 98 245,10             |
| 3    | 31. decembris | 3 104,50            | 95 140,60             |
| 4.    | 31. decembris | 5 150,21            | 89 990,39             |
| 5.    | 31. decembris | 7 522,95            | 82 467,44             |
| 6.    | 31. decembris | 10 184,06           | 72 283,38             |

## <a name="digressive-depreciation"></a>Novirzošais nolietojums
Lauka **Koeficients** vērtība ir mazāka nekā **50**.

### <a name="example"></a>Piemērs

Iegādes cena ir 100 000, koeficents ir 20, lietošanas ilgums ir 10 gadi, un nolietojums sākas 1. janvārī. Nolietojuma summas un atlikušās vērtības summas tiek rādītas vienīgi pirmajiem sešiem lietošanas ilguma gadiem.

| Gads | Periods      | Nolietojuma summa | Atlikušās vērtības summa |
|------|-------------|---------------------|-----------------------|
| 1    | 31. decembris | 56 080,43           | 43 919,57             |
| 2    | 31. decembris | 10 665,70           | 33 253,87             |
| 3    | 31. decembris | 7 156,22            | 26 097,65             |
| 4.    | 31. decembris | 5 538,06            | 20 559,59             |
| 5.    | 31. decembris | 4 579,89            | 15 979,70             |
| 6.    | 31. decembris | 3 937,36            | 12 042,34             |

## <a name="straight-line-depreciation"></a>Lineārais nolietojums
Lauka **Koeficients** vērtība ir **50**. Šādā gadījumā nolietojums visos periodos ir vienāds un ir jāņem vērā ietekme, ko izraisa citos laukos norādītas vērtības, kā tas ir aprakstīts rakstā [Lineārā lietošanas ilguma nolietojums](straight-line-service-life-depreciation.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
