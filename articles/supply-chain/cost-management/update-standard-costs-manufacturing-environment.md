---
title: Atjaunināt standarta izmaksas ražošanas vidē
description: Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas ar ražošanu vidē.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8acbcb79fa45ea2f225775068e0d061a44cba1f7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675240"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Atjaunināt standarta izmaksas ražošanas vidē

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas ar ražošanu vidē. 

Atjauninājumi var attiekties uz jauniem krājumiem, izmaksu kategorijām un netiešo izmaksu aprēķinu formulām. Tie var attiekties uz labojumiem un izmaksu izmaiņām. Atjauninājuma veids ietekmē darbības, kas ir jāveic, lai atjauninātu standarta izmaksas, kā aprakstīts tālāk aprakstītajos gadījumos.

-   Ievadiet paredzamās pirkto krājumu standarta izmaksu izmaiņas, pēc tam izmainiet krājumu izmaksu ierakstu statusu **Aktīvs** attiecīgajā datumā. Tomēr nepārrēķiniet ražoto krājumu, kas izmanto pirktos krājumus, izmaksas.
-   Ievadiet jauna, pirkta krājuma standarta izmaksas, bet nepārrēķiniet ražoto krājumu izmaksas ar materiālu komplekta (MK) versiju, kurā jaunais pirktais krājums ir iekļauts kā komponents.
-   Izlabojiet vai izmainiet pirktā krājuma izmaksas, vai arī izmainiet pirktajam krājumam piešķirto izmaksu grupu un aprēķiniet visu ražoto krājumu izmaksas ar MK versiju, kas iekļauj pirkto krājumu kā komponentu.
-   Izmainiet izmaksu kategorijas izmaksas un aprēķiniet visu ražoto krājumu izmaksas ar maršrutēšanas versiju, kas iekļauj izmaksu kategoriju izmantojošās maršrutēšanas darbības.
-   Izmainiet izmaksu kategorijas, kas ir piešķirtas maršrutēšanas darbībām vai izmaksu grupai, kas ir piešķirta izmaksu kategorijām. Pēc tam aprēķiniet visu ražoto krājumu izmaksas ar maršrutēšanas versiju, kas iekļauj izmaksu kategoriju izmantojošās maršrutēšanas darbības.
-   Izmainiet netiešo izmaksu aprēķināšanas formulu un aprēķiniet visu ražoto krājumu izmaksas, kuras ietekmē šīs izmaiņas.
-   Izmainiet vai pievienojiet ražota krājuma ražošanas vietu un aprēķiniet krājuma ražošanas izmaksas vietai.
-   Aprēķiniet vai pārrēķiniet ražotā krājuma izmaksas un pārrēķiniet visu ražoto krājumu izmaksas ar MK versiju, kas iekļauj ražoto krājumu kā komponentu.
-   Aprēķiniet jauna ražotā krājuma izmaksas, ņemot vērā tam noteiktos, apstiprinātos, aktīvā MK un maršruta datus.

Katrs gadījums pieprasa nopietnus apsvērumus par to, kā atjaunināt standarta izmaiņas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]