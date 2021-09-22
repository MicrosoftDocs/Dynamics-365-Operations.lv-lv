---
title: Nevar izveidot noslodzes rindu, jo nav derīgas krājumu dimensijas
description: Mēģinot izlaist atgriešanas pārdošanas pasūtījumu nosūtīšanai uz noliktavu, iespējams, tiks parādīts kļūdas ziņojums par nederīgām krājumu dimensijām. Noņemt šos no pasūtījuma rindas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477000"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Nevar izveidot noslodzes rindu atgriešanas pārdošanas pasūtījumam, jo nav derīgas krājumu dimensijas

## <a name="symptoms"></a>Simptomi

Mēģinot nodot atpakaļ atgriešanas pārdošanas pasūtījumu noliktavā, iespējams, saņemsit šādu kļūdas ziņojumu:

> Nevar izveidot noslodzes rindu šai pasūtījuma rindai, jo tā ietver nederīgas krājumu dimensijas. Nevar atsaukties uz krājumu dimensijām, kas atrodas zem novietojuma dimensijas rezervāciju hierarhijā. Noņemiet nederīgās dimensijas no pasūtījuma rindas.

## <a name="resolution"></a>Novēršana

Diemžēl prece pārdošanas atgriešanas procesam neatbalsta noslodzes apstrādi. Tāpēc nevar nodot atgriešanas pārdošanas pasūtījumu noliktavai.

Pārdošanas pasūtījumu transakcijās nevar atsaukties uz krājumu dimensijām, kas atrodas zem **Novietojuma** dimensijas rezervāciju hierarhijā. Risinājums ir noņemt nederīgās dimensijas no pasūtījuma rindas.
