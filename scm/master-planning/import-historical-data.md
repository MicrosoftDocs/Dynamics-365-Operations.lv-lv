---
title: "Vēsturisko datu importēšana pieprasījuma apjoma prognozēm"
description: "Lai iegūtu precīzas pieprasījuma apjoma prognozes, ir nepieciešami vēsturiskie pieprasījuma dati pa krājumiem vai krājumu sadalījuma principiem. šajā tēmā ir izskaidrots, kā izmantot datu elementus, lai importētu vēsturiskos pieprasījuma datus no jebkuras sistēmas, tādējādi iegūstot vēsturiskos pieprasījuma datus par ilgāku periodu."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Vēsturisko datu importēšana pieprasījuma apjoma prognozēm

[!include[banner](../includes/banner.md)]

Lai palīdzētu nodrošināt pieprasījuma apjoma prognozes precizitāti, ir jāizmanto pēc iespējas vairāk vēsturisko pieprasījuma datu pa krājumiem vai krājumu sadalījuma principiem. Ja vēsturiskie pieprasījuma dati vēl nav importēti, izmantojiet Microsoft Dynamics 365 for Operations datu entītiju **Vēsturisks ārējs pieprasījums** (ReqDemPlanHistoricalExternalDemandEntity), lai tos importētu.

Darbvietā **Datu pārvaldība** ir redzams pārskats par visiem entītijas laukiem.

1. Atveriet darbvietu **Datu pārvaldība**.
2. Noklikšķiniet uz elementa **Datu elementi**.
3. Elementu sarakstā meklējiet elementu **Vēsturisks ārējs pieprasījums**.
4. Noklikšķiniet uz **Mērķa lauki**. Šie elementu lauki ir obligāti: vieta (**DeliveringSiteId**), datums (**DemandDate**), daudzums (**DemandQuantity**) un krājuma numurs (**ItemNumber**) vai krājuma sadalījuma princips (**ProductAllocationKeyId**).

Lai izmantotu datu elementu, ir nepieciešams Microsoft Excel fails vai komatatdalīto vērtību (CSV) fails, kurā ir saglabāti vēsturiskie pieprasījuma dati. Tālāk esošajā piemērā ir aprakstīts, kā importēt datus no CSV faila.

## <a name="example"></a>Paraugs

Kā paraugu varat izmantot tālāk pieejamo failu. Lejupielādējiet failu [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Šajā failā ir ietverti vēsturiskie pieprasījuma dati par krājumu D0001. Tajā ir ietverti tikai šādi obligātie lauki: vieta, daudzums un pieprasījuma datums.

1. Atlasiet uzņēmumu, kurā ir jāimportē vēsturiskie pieprasījuma dati.
2. Atveriet darbvietu **Datu pārvaldība**.
3. Noklikšķiniet uz elementa **Importēt**.
4. Ievadiet importēšanas projekta nosaukumu, piemēram, **Importētie krājuma D0001 vēsturiskie pieprasījuma dati**.
5. Laukā **Avota datu formāts** atlasiet importētā faila formātu. Lai importētu šī piemēra ietveros lietoto failu HistoricalDemandData, atlasiet **CSV**.
6. Laukā **Elementa nosaukums** atlasiet **Vēsturisks ārējs pieprasījums**.
7. Saglabājiet failu datorā un pēc tam augšupielādējiet to.
8. Noklikšķiniet uz **Importēt**.
9. Tiek automātiski atvērta lapa **Izpildes kopsavilkums**. Pārbaudiet importētos datus šajā lapā.

Pēc vēsturisko pieprasījuma datu importēšanas varat ģenerēt pieprasījuma apjoma prognozi.

## <a name="see-also"></a>Skatiet arī

[Ģenerēt statistiskās bāzlīnijas prognozi](generate-statistical-baseline-forecast.md)
