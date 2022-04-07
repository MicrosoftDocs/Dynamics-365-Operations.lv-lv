---
title: Atmaksas maksas tiek pārrēķinātas, ņemot vērā atgriezto daudzumu.
description: Šajā tēmā ir sniegtas traucējummeklēšanas norādījumi, kas var palīdzēt kasierim pārdošanas punktā (POS) skatīt nepareizas atmaksas maksas par atgriezto krājumu daudzumu.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/28/2022
ms.locfileid: "8489727"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Atmaksas maksas tiek pārrēķinātas, ņemot vērā atgriezto daudzumu.

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas traucējummeklēšanas norādījumi, kas var palīdzēt kasierim pārdošanas punktā (POS) skatīt nepareizas atmaksas maksas par atgriezto krājumu daudzumu.

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
