---
title: Veidot ražošanas pasūtījumus
description: Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "324633"
---
# <a name="create-production-orders"></a>Veidot ražošanas pasūtījumus

[!include [banner](../includes/banner.md)]

Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.

Ražošanas pasūtījums tiek izvadīts caur ražošanas cikla stadijām. Kad pasūtījums ir izveidots, tam tiek piešķirts statuss **Izveidots**. Kad pasūtījums ir pabeigts, tam tiek piešķirts statuss **Pabeigts**. Katras stadijas parametru iestatījumi lietotājam ļauj konfigurēt katru darbību. Šos iestatījumus var iestatīt atsevišķam lietotājam vai visiem lietotājiem.

Ražošanas materiālu komplekts un ražošanas maršruts ir galvenie ražošanas pasūtījuma elementi. Šie elementi tiek kopēti uz ražošanas pasūtījumu, pamatojoties uz atlasīto krājumu un daudzumu, ko ir paredzēts ražot. Pirms tiek sākts ražošanas pasūtījums, ražošanas materiālu komplektu un maršrutu ir iespējams rediģēt.

Ražošanas pasūtījumu var izveidot šādos scenārijos:

-   Izveidots, izpildot vispārējo plānošanu, pamatojoties uz materiālu pieprasījumu.
-   Izveidots tieši no pārdošanas pasūtījuma rindas vai laikā, kad tiek izveidots un novērtēts augstāka līmeņa ražošanas pasūtījums (piesaistītā piegāde).
-   Izveidots manuāli.




