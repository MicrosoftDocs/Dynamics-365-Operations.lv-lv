---
title: Ražošanas pasūtījuma dzīves cikla pārskats
description: Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df773cf13b8ccd9ee4f861955b1a4321af38a150
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811802"
---
# <a name="production-order-lifecycle-overview"></a>Ražošanas pasūtījuma dzīves cikla pārskats

[!include [banner](../includes/banner.md)]

Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.

Ražošanas pasūtījums tiek izvadīts caur ražošanas cikla stadijām. Kad pasūtījums ir izveidots, tam tiek piešķirts statuss **Izveidots**. Kad pasūtījums ir pabeigts, tam tiek piešķirts statuss **Pabeigts**. Katras stadijas parametru iestatījumi lietotājam ļauj konfigurēt katru darbību. Šos iestatījumus var iestatīt atsevišķam lietotājam vai visiem lietotājiem.

Ražošanas materiālu komplekts un ražošanas maršruts ir galvenie ražošanas pasūtījuma elementi. Šie elementi tiek kopēti uz ražošanas pasūtījumu, pamatojoties uz atlasīto krājumu un daudzumu, ko ir paredzēts ražot. Pirms tiek sākts ražošanas pasūtījums, ražošanas materiālu komplektu un maršrutu ir iespējams rediģēt.

Ražošanas pasūtījumu var izveidot šādos scenārijos:

-   Izveidots, izpildot vispārējo plānošanu, pamatojoties uz materiālu pieprasījumu.
-   Izveidots tieši no pārdošanas pasūtījuma rindas vai laikā, kad tiek izveidots un novērtēts augstāka līmeņa ražošanas pasūtījums (piesaistītā piegāde).
-   Izveidots manuāli.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]