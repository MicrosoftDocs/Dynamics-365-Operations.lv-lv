---
title: Tirdzniecības līguma nosacījumi nav piemēroti importētajām pasūtījuma rindām
description: Tirdzniecības līgumu cenas un atlaides netiek lietotas pārdošanas vai pirkšanas pasūtījuma rindās, kas ir importētas, izmantojot datu pārvaldību
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477012"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Tirdzniecības līguma nosacījumi nav piemēroti importētajām pasūtījuma rindām

## <a name="symptoms"></a>Simptomi

Pārdošanas vai pirkšanas pasūtījuma rindām piemērojamie tirdzniecības līgumi netiek lietoti rindās, kas ir importētas, izmantojot datu pārvaldību. Tomēr tie paši tirdzniecības līgumi tiek lietoti pārdošanas vai pirkšanas pasūtījuma rindās, kas ir izveidotas manuāli.

## <a name="cause"></a>Iemesls

Ja pirkšanas pasūtījuma rindās, kas ir importētas, izmantojot datu pārvaldību, jau ir iekļauta cenas informācija, tirdzniecības līgums šīm rindām netiks pārvērtēts. Piemēram, ja rindai ir iestatīta **Rindas atlaide procentos** vai kāda no cenu un atlaižu vērtībām, tad tirdzniecības līgumi šai rindai netiks meklēti.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Šāda darbība ir paredzama un ir līdzīga gan pārdošanas pasūtījumiem, gan pirkšanas pasūtījumiem.

Kā aprisinājumu, importējiet pirkšanas pasūtījuma rindas bez cenas informācijas iestatīšanas. Pēc tam tiks lietoti tirdzniecības līgumi, un pirkšanas pasūtījuma rindas tiks atjauninātas, pamatojoties uz definētajiem tirdzniecības līgumiem.
