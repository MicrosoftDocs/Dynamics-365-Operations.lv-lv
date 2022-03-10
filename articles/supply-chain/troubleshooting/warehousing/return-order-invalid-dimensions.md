---
title: Nevar izveidot noslodzes rindu, jo nav derīgas krājumu dimensijas
description: Mēģinot izlaist atgriešanas pārdošanas pasūtījumu nosūtīšanai uz noliktavu, iespējams, tiks parādīts kļūdas ziņojums par nederīgām krājumu dimensijām. Noņemt šos no pasūtījuma rindas.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119216"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Nevar izveidot noslodzes rindu atgriešanas pārdošanas pasūtījumam, jo nav derīgas krājumu dimensijas

## <a name="symptoms"></a>Simptomi

Mēģinot nodot atpakaļ atgriešanas pārdošanas pasūtījumu noliktavā, iespējams, saņemsit šādu kļūdas ziņojumu:

> Nevar izveidot noslodzes rindu šai pasūtījuma rindai, jo tā ietver nederīgas krājumu dimensijas. Nevar atsaukties uz krājumu dimensijām, kas atrodas zem novietojuma dimensijas rezervāciju hierarhijā. Noņemiet nederīgās dimensijas no pasūtījuma rindas.

## <a name="resolution"></a>Novēršana

Diemžēl prece pārdošanas atgriešanas procesam neatbalsta noslodzes apstrādi. Tāpēc nevar nodot atgriešanas pārdošanas pasūtījumu noliktavai.

Pārdošanas pasūtījumu transakcijās nevar atsaukties uz krājumu dimensijām, kas atrodas zem **Novietojuma** dimensijas rezervāciju hierarhijā. Risinājums ir noņemt nederīgās dimensijas no pasūtījuma rindas.
