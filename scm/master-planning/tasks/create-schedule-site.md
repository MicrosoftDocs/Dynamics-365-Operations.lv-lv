--- 
title: Grafika izveide vietai
description: "Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a611cb773919284b2bbe55395a7ec2b947d5c0b4
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-schedule-for-a-site"></a>Grafika izveide vietai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai.  Lai izpildītu šo procedūru, tiek izmantots demonstrācijas datu uzņēmums USMF.


## <a name="identify-production-orders-that-are-not-started"></a>Identificēt ražošanas pasūtījumus, kas vēl nav sākti
1. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Vieta, izmantojot vērtību “1”.
    * 1 apzīmē vietu uzņēmumā USMF. Ja neizmantojat uzņēmumu USMF, atlasiet vietu no sava uzņēmuma.  
3. Atveriet statusa kolonnas filtru.
4. Lietojiet filtru laukam “Statuss” ar vērtību “Ieplānots”, izmantojot filtra operatoru “ir precīzi”.

## <a name="create-a-schedule"></a>Izveidot grafiku
1. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
2. Darbību rūtī noklikšķiniet uz Grafiks.
3. Noklikšķiniet uz Plānot darbus.
4. Laukā Plānošanas virziens atlasiet “Atpakaļ no piegādes datuma”.
5. Laukā Ierobežota noslodze atlasiet Nē.
6. Laukā Ierobežots materiāls atlasiet Nē.
7. Noklikšķiniet uz OK.
    * Tas var aizņemt kādu laiku.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Skatīt plānoto ražošanas pasūtījumu rezultātu
1. Sarakstā atzīmējiet atlasīto rindu.
    * Varat atzīmēt jebkuru rindu.  
2. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
3. Noklikšķiniet uz Visi darbi.
    * Šajā lapā varat redzēt darbu sarakstu. Cilnē Plānošana varat redzēt darba vērtības Sākuma datums un Beigu datums.  
4. Noklikšķiniet uz Materiāli.
    * Šajā lapā varat redzēt prognozēto materiālu patēriņu ražošanas pasūtījumā iekļautajām operācijām un pašreiz pieejamos krājumus.  


