---
title: Atmaksājamās maksas tiek nepareizi aprēķinātas, pamatojoties uz atgriezto daudzumu
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad kasieri pārdošanas punktā (POS) redz nepareizas atmaksas maksas par atgriezto krājumu daudzumu.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 7a84207f587a826b9acdfd818c64220c5327bde1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890247"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Atmaksājamās maksas tiek nepareizi aprēķinātas, pamatojoties uz atgriezto daudzumu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad kasieri pārdošanas punktā (POS) redz nepareizas atmaksas maksas par atgriezto krājumu daudzumu.

## <a name="description"></a>Apraksts

Debitors atgriež daļēju krājumu daudzumu, kas tika iegādāti pārdošanas pasūtījumam, kam ir rindas līmeņa atmaksas maksas. Tomēr, lai parādītu daļēju atmaksu, POS parāda visas maksas kā atmaksas.

Piemēram, debitors iepērk piecu krājumu daudzumu $5 krājumam, kopējām izmaksām $25. Debitors pēc tam atgriež trīs no pieciem krājumiem. Tomēr, kasieris pos $25 atmaksas maksu paredzētās cenas $15 par trim atgrieztajām vienībām.

## <a name="resolution"></a>Novēršana

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Ieslēgt iespēju Iespējot maksu atmaksu, ņemot vērā atmaksātā daudzuma līdzekli

Microsoft Dynamics 365 Commerce Izmantojot versiju 10.0.26, iespējot atmaksas maksas, pamatojoties uz atmaksāto daudzumu iespēju, **rindu** līmeņa atmaksas maksas tiek aprēķinātas, pamatojoties uz atgriezto krājumu daudzumu.

Lai iespējotu iespējot **maksu atmaksu, pamatojoties uz** commerce headquarters funkcijai Atmaksātais daudzums, veiciet šos soļus.

1. Atveriet līdzekļu **pārvaldības darbvietu** (Sistēmas **administratora darbalauku \> līdzekļu \> pārvaldība**).
1. Pieejamo līdzekļu sarakstā meklējiet un atlasiet iespēju Iespējot **atmaksas maksas, pamatojoties uz atmaksātā daudzuma** līdzekli.
1. Labās puses rūtī izvēlieties Aktivizēt **tagad**.
