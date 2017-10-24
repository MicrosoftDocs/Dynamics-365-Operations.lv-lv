--- 
title: "Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu"
description: "Šajā procedūrā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Ražošanas pasūtījuma plānošana ar operāciju un darbu plānošanu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā uzmanība ir vērsta uz ražošanas pasūtījuma plānošanu ar operāciju plānošanu un darbu plānošanu. Ar operāciju plānošanu netiek izveidots neviens darbs, bet darbi tiek izveidoti ar darbu plānošanu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šī procedūra ir paredzēta ražošanas vadītājam, ražošanas plānotājam vai ražotnes vadītājam, kas strādā diskrētās ražošanas vidē.


## <a name="create-a-production-order"></a>Ražošanas pasūtījuma izveide
1. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
2. Noklikšķiniet uz Jauns ražošanas pasūtījums.
3. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Atlasiet krājuma kodu D0001.  
4. Noklikšķiniet uz Izveidot.

## <a name="schedule-operations-for-the-production-order"></a>Ieplānot operācijas ražošanas pasūtījumam
1. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet ražošanas pasūtījumu, kuru tikko izveidojāt. Tam vajadzētu atrasties saraksta augšgalā.      
2. Darbību rūtī noklikšķiniet uz Grafiks.
3. Noklikšķiniet uz Plānot operācijas.
4. Laukā Plānošanas virziens atlasiet “No plānošanas datuma uz priekšu”.
5. Laukā Plānošanas datums ievadiet datumu.
    * Atlasiet kādu nākotnes datumu, piemēram, vienu nedēļu pēc šodienas. Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.  
6. Noklikšķiniet uz OK.
7. Sarakstā atzīmējiet atlasīto rindu.
    * Ņemiet vērā, ka statuss tiek mainīts uz Plānots.  
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz Visi darbi.
    * Ņemiet vērā, ka darbi tiek izveidoti ar operāciju plānošanu.  
10. Aizvērt lapu.

## <a name="schedule-jobs-for-the-production-order"></a>Ieplānot darbus ražošanas pasūtījumam
1. Darbību rūtī noklikšķiniet uz Grafiks.
2. Noklikšķiniet uz Plānot darbus.
3. Laukā Plānošanas virziens atlasiet “No plānošanas datuma uz priekšu”.
4. Laukā Plānošanas datums ievadiet datumu.
    * Atlasiet kādu datumu nākotnē, piemēram, vienu nedēļu pēc šodienas. Kad plānošanas virziens ir atlasīts, ražošanas pasūtījums tiek plānots no šī datuma uz priekšu.  
5. Noklikšķiniet uz OK.
6. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
7. Noklikšķiniet uz Visi darbi.
    * Ņemiet vērā, ka, pamatojoties uz aktīvo maršrutu, ar darbu plānošanu tiek izveidoti 5 darbi.  


