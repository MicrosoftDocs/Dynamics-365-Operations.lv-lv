---
title: Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu
description: Šajā tēmā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2181a84aea08aac0ddb202f7211dbda6330a3d49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148841"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu

[!include [banner](../../includes/banner.md)]

Šajā tēmā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu. Ar operāciju plānošanu netiek izveidots neviens darbs, bet darbi tiek izveidoti ar darbu plānošanu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šī procedūra ir paredzēta ražošanas vadītājam, ražošanas plānotājam vai ražotnes vadītājam, kas strādā diskrētās ražošanas vidē.


## <a name="create-a-production-order"></a>Ražošanas pasūtījuma izveide
1. Navigācijas rūtī atveriet **Moduļi > Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi**.
2. Atlasiet **Jauns ražošanas pasūtījums**.
3. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību. Atlasiet krājuma numuru **D0001**.  
4. Atlasiet **Izveidot**.

## <a name="schedule-operations-for-the-production-order"></a>Ieplānot operācijas ražošanas pasūtījumam
1. Atzīmējiet jaunizveidoto rindu.      
2. Darbības rūtī atlasiet **Ieplānot**.
3. Atlasiet **Ieplānot operācijas**.
4. Laukā **Plānošanas virziens** atlasiet **No plānošanas datuma uz priekšu**.
5. Laukā **Plānošanas datums** ievadiet datumu. Atlasiet kādu nākotnes datumu, piemēram, vienu nedēļu pēc šodienas. Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.  
6. Atlasiet **Labi**.
7. Sarakstā atzīmējiet atlasīto rindu. Ņemiet vērā, ka statuss tiek mainīts uz **Ieplānots**. 
8. Atlasiet **Visi darbi**. Ņemiet vērā, ka darbi tiek izveidoti ar operāciju plānošanu.  
9. Aizvērt lapu.

## <a name="schedule-jobs-for-the-production-order"></a>Ieplānot darbus ražošanas pasūtījumam
1. Darbības rūtī atlasiet **Ieplānot**.
2. Atlasiet **Ieplānot darbus**.
3. Laukā **Plānošanas virziens** atlasiet **No plānošanas datuma uz priekšu**.
4. Laukā **Plānošanas datums** ievadiet datumu. Atlasiet kādu datumu nākotnē, piemēram, vienu nedēļu pēc šodienas. Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.  
5. Atlasiet **Labi**.
6. Darbību rūtī atlasiet **Ražošanas pasūtījums**.
7. Atlasiet **Visi darbi**. Ņemiet vērā, ka, pamatojoties uz aktīvo maršrutu, ar darbu plānošanu tiek izveidoti 5 darbi.  

