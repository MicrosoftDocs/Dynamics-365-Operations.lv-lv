---
title: Grafika izveide vietai
description: Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51c9ca8c402880f93a5998605d946b881d5ccdf5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835883"
---
# <a name="create-a-schedule-for-a-site"></a>Grafika izveide vietai

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

