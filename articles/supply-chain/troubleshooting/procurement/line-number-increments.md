---
title: Impertēti pirkuma pasūtījumi rāda nepareizus rindu numurus
description: Kad pirkuma pasūtījumi tiek importēti ar datu pārvaldību, pirkuma pasūtījuma rindas numuri neievēro sistēmas parametros definēto pieaugumu
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476939"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Impertēti pirkuma pasūtījumi rāda nepareizus rindu numurus

## <a name="symptoms"></a>Simptomi

Pēc noklusējuma automātiski ģenerētie rindu numuri pirkšanas pasūtījuma rindām, kas tiek importētas, izmantojot datu elementu *Pirkšanas pasūtījuma rindas V2*, neizmanto sistēmas rindu numuru palielinājumu, kas norādīts sistēmas parametros. Ja manuāli izveidojat pirkšanas pasūtījumu un pievienojat rindas, izmantojot lietotāja interfeisu (UI), rindu numuri tiek palielināti pareizi. Taču, ja lietojat datu pārvaldības satvaru (DMF), tie netiek palielināti pareizi.

Šī problēma rodas, ja importējat rindas, izmantojot DMF un importētajā elementā vēl nav piešķirti rindu numuri, tad sistēma izmanto DMF metodi to piešķiršanai. Šī metode vienmēr palielina rindu numurus par vienu.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Pārliecinieties, lai vēlamie rindu numuri jau ir norādīti datu elementa rindu numuru laukos, kad importējat pirkšanas pasūtījuma rindas. Šādā gadījumā DMF nepārrakstīs rindu numurus.
