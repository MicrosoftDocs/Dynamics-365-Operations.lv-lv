---
title: Vēsturisko datu importēšana pieprasījuma apjoma prognozēm
description: Lai iegūtu precīzas pieprasījuma apjoma prognozes, ir nepieciešami vēsturiskie pieprasījuma dati pa krājumiem vai krājumu sadalījuma principiem. šajā tēmā ir izskaidrots, kā izmantot datu elementus, lai importētu vēsturiskos pieprasījuma datus no jebkuras sistēmas, tādējādi iegūstot vēsturiskos pieprasījuma datus par ilgāku periodu.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301654"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Vēsturisko datu importēšana pieprasījuma apjoma prognozēm

[!include [banner](../includes/banner.md)]

Lai palīdzētu nodrošināt pieprasījuma apjoma prognozes precizitāti, ir jāizmanto pēc iespējas vairāk vēsturisko pieprasījuma datu pa krājumiem vai krājumu sadalījuma principiem. Ja vēsturiskie pieprasījuma dati vēl nav importēti, importējiet tos, izmantojot Dynamics 365 Supply Chain Management datu elementu **Vēsturisks ārējs pieprasījums** (ReqDemPlanHistoricalExternalDemandEntity).

Darbvietā **Datu pārvaldība** ir redzams pārskats par visiem entītijas laukiem.

1. Atveriet darbvietu **Datu pārvaldība**.
2. Noklikšķiniet uz elementa **Datu elementi**.
3. Elementu sarakstā meklējiet elementu **Vēsturisks ārējs pieprasījums**.
4. Atlasiet **Mērķa laukus**. Šie elementu lauki ir obligāti: vieta (**DeliveringSiteId**), datums (**DemandDate**), daudzums (**DemandQuantity**) un krājuma numurs (**ItemNumber**) vai krājuma sadalījuma princips (**ProductAllocationKeyId**).

Lai izmantotu datu elementu, ir nepieciešams Microsoft Excel fails vai komatatdalīto vērtību (CSV) fails, kurā ir ietverti vēsturiskie pieprasījuma dati. Tālāk esošajā piemērā ir aprakstīts, kā importēt datus no CSV faila.

Papildinformāciju par to, kā importēt datus, tostarp to, kā iztīrīt datus pēc importēšanas, skatiet [Datu importēšanas un eksportēšanas darbu pārskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) un ar to saistītās tēmas.

Skatiet arī [Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]