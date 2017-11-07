---
title: "Veidot ražošanas pasūtījumus"
description: "Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58213d4d6e8c29ab6605eb7aa5c6cb9ca6ba4a10
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="create-production-orders"></a>Veidot ražošanas pasūtījumus

[!include[banner](../includes/banner.md)]


Kad ražošanas pasūtījums ir izveidots, tiek inicializēts pieprasījums sākt krājuma ražošanu. Ražošanas pasūtījumā ir iekļauta informācija par to, kas tiks ražots, ražojamais daudzums un plānotais pabeigšanas datums. Tajā ir iekļauta arī informācija par to, kurus materiālus patērēt un kurš process jāizpilda, lai ražotu šo krājumu.

Ražošanas pasūtījums tiek izvadīts caur ražošanas cikla stadijām. Kad pasūtījums ir izveidots, tam tiek piešķirts statuss **Izveidots**. Kad pasūtījums ir pabeigts, tam tiek piešķirts statuss **Pabeigts**. Katras stadijas parametru iestatījumi lietotājam ļauj konfigurēt katru darbību. Šos iestatījumus var iestatīt atsevišķam lietotājam vai visiem lietotājiem.

Ražošanas materiālu komplekts un ražošanas maršruts ir galvenie ražošanas pasūtījuma elementi. Šie elementi tiek kopēti uz ražošanas pasūtījumu, pamatojoties uz atlasīto krājumu un daudzumu, ko ir paredzēts ražot. Pirms tiek sākts ražošanas pasūtījums, ražošanas materiālu komplektu un maršrutu ir iespējams rediģēt.

Ražošanas pasūtījumu var izveidot šādos scenārijos:

-   Izveidots, izpildot vispārējo plānošanu, pamatojoties uz materiālu pieprasījumu.
-   Izveidots tieši no pārdošanas pasūtījuma rindas vai laikā, kad tiek izveidots un novērtēts augstāka līmeņa ražošanas pasūtījums (piesaistītā piegāde).
-   Izveidots manuāli.





