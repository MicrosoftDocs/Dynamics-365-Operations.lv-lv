---
title: Nevar grāmatot pavadzīmi apturētai pārdošanas pasūtījuma rindai
description: Nevar grāmatot pavadzīmi, lai apturētu pārdošanas pasūtījuma rindu
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462921"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Nevar grāmatot pavadzīmi apturētai pārdošanas pasūtījuma rindai

Kļūdas kods: SYS13203

## <a name="symptoms"></a>Simptomi

Kad jūs mēģināt grāmatot kravas pavadzīmi, sistēma parāda šādu kļūdas ziņojumu:

> Nevar grāmatot pavadzīmi, ja pārdošanas pasūtījuma rinda tiek apturēta pēc izejošā sūtījuma apstiprināšanas. Nevar izdot daudzumu.

## <a name="cause"></a>Iemesls

Viena vai vairākas saistītās pārdošanas pasūtījuma rindas var tikt apturētas, kas nozīmē, ka sistēma neļaus tālāk apstrādāt šo pārdošanas pasūtījumu. Tas nozīmē arī to, ka sistēma negrāmatos pasūtījuma pavadzīmi.

Piemēram, lietotājs var būt nolēmis apturēt vienu vai vairākas pasūtījuma rindas, jo debitors ir atzvanījis un atcēlījis pasūtījumu. Tomēr, ja izejošais sūtījums jau ir ticis apstiprināts, tad sūtījums, kas ietver pārdošanas pasūtījumu, jau būtu fiziski atstāts noliktavā, kas nozīmē, ka pārdošanas pasūtījuma rindu apturēšanai nebūs nekādas ietekmes. Tā kā sūtījumu vairs nav iespējams fiziski apturēt, variet arī noņemt nostāt rindas, lai varētu iegrāmatot pavadzīmi. Tad atceltais pasūtījums būs jārīkojas kā atgriešana.

## <a name="resolution"></a>Novēršana

Lai varētu iegrāmatot pavadzīmi, pārliecinieties, ka neviena no atbilstošām pārdošanas pasūtījuma rindām nav apturēta, rīkojoties tālāk.

1. Doties uz **Visiem pārdošanas pasūtījumiem Pārdošana \> un mārketings \> Visi pārdošanas pasūtījumi**.
1. Atrodiet un atveriet pārdošanas pasūtījumu, ar ko ir problēmas.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet pārdošanas pasūtījuma rindu.
1. Kopsavilkuma cilnē **Detalizēta informācija par** rindu atveriet cilni Vispārīgi un **pārliecinieties**, ka lauks Apturēts **ir** iestatīts uz *Nē*.
1. Turpiniet darbu, līdz visas atbilstošās pārdošanas rindas vairs netiek apturētas.
1. Mēģiniet vēlreiz grāmatot kravas vai pārdošanas pasūtījuma pavadzīmi.
