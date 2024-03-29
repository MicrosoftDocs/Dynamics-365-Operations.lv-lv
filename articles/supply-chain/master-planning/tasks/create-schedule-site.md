---
title: Grafika izveide vietai
description: Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0db5095020bc14d56ae3680e7d0caa68789180e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469287"
---
# <a name="create-a-schedule-for-a-site"></a>Grafika izveide vietai

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā plānot ražošanas pasūtījumus, kas vēl nav sākti kādai vietai.  Lai izpildītu šo procedūru, tiek izmantots paraugdatu uzņēmums USMF.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]