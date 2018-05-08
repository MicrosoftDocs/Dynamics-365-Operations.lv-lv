---
title: "Ražošanas pasūtījuma statusa atsaukšana"
description: "Šajā tēmā ir aprakstīts, kā atsaukt ražošanas pasūtījuma statusu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a>Ražošanas pasūtījuma statusa atsaukšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā atsaukt ražošanas pasūtījuma statusu. 

Ja atsaucat ražošanas pasūtījuma statusu, pasūtījums un visas ar maršrutiem saistītās operācijas tiek pārnesti atpakaļ uz iepriekšējo ražošanas dzīves cikla posmu. Pieņemsim, ka ražošanas pasūtījuma statuss ir **Ieplānots** un jūs maināt statusu atpakaļ uz **Izveidots**. Šādā gadījumā sistēmā statuss vispirms ir jāmaina uz **Novērtēts**, kas ir iepriekšējais statuss pirms statusa **Ieplānots**. Pēc tam sistēmā statuss var tikt mainīts uz vajadzīgo statusu **Izveidots**. **Piezīme.** Ja pasūtījuma statuss jau ir **Reģistrēt pabeigšanu**, joprojām varat to atsaukt un atjaunot kādu no iepriekšējiem statusiem. Taču ir vēlreiz jāveic novērtēšana un operāciju plānošana vai darbu plānošana, vai abu veidu plānošana, lai atjauninātu pasūtījumā ietverto informāciju. Šī darbība ir obligāti jāveic, jo ir jāatiestata arī visas atlikušā krājumu patēriņa un operācijas resursu patēriņa rezervācijas. Šī raksta turpinājumā ir paskaidrots, kas notiek, kad atsaucat ražošanas pasūtījuma statusu tālāk norādītajos veidos.

-   No **Novērtēts** uz **Izveidots**
-   No **Ieplānots** uz **Novērtēts**
-   No **Izlaists** uz **Ieplānots**
-   No **Sākts** uz **Izlaists**

## <a name="from-estimated-to-created"></a>No Novērtēts uz Izveidots
Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Ieplānots** uz **Izveidots**, tiek noņemts krājumu patēriņš, kas krājumiem tika aprēķināts materiālu komplektā (MK). Tiek dzēstas krājumu transakcijas ražošanas rindā, un ražošanas pasūtījuma MK rindās lauka **Nepabeigtā pasūtījuma statuss** vērtība tiek atiestatīta uz **Pabeigts**. Ja ir atlasītas opcijas **Atvasinātie pirkšanas pasūtījumi** un **Atvasinātā ražošana**, tiek dzēsti visi pamata pirkšanas pasūtījumi vai ražošanas pasūtījumi. Ja novērtējāt ražošanas pasūtījuma izmaksas vai manuāli rezervējāt krājumus, lai tos varētu izmantot ražošanā, šīs transakcijas tiek noņemtas.

## <a name="from-scheduled-to-estimated"></a>No Ieplānots uz Novērtēts
Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Ieplānots** uz **Novērtēts**, tiek noņemti ieplānotie sākuma un beigu datumi un laiks. Tiek noņemtas plānošanas laikā veiktās noslodzes rezervācijas, un tiek dzēsti darbu plānošanas laikā izveidotie darbi. Tiek atiestatīta visa lapā **Ražošanas pasūtījumu informācija** reģistrētā informācija par operāciju plānošanu un darbu plānošanu.

## <a name="from-released-to-scheduled"></a>No Izlaists uz Ieplānots
Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Izlaists** uz **ieplānots**, tiek mainīta vienīgi statusa lauka vērtība.

## <a name="from-started-to-released"></a>No Sākts uz Izlaists
Ja atsaucat ražošanas pasūtījuma statusu, mainot to no **Sākts** uz **Izlaists**, tiek atsaukts visu to krājumu statuss, kas ir reģistrēti kā pabeigti. Ja materiāls ir izdots vai ir veikta ieejošā vai izejošā piegāde ražošanai, šie iestatījumi tiek atsaukti. Ražošanas pasūtījuma MK rindu lauka**Nepabeigtā pasūtījuma statuss** tiek mainīts no **Pabeigts** uz **Materiālu patēriņš**. Ja operācijām ražošanas maršrutā ir reģistrēts laiks vai daudzumi ir reģistrēti kā pabeigti, šie iestatījumi tiek atsaukti. Ražošanas maršruta lauka**Nepabeigtā pasūtījuma statuss** tiek mainīts no **Pabeigts** uz **Maršruta patēriņš**. Tiek atsaukti visu to krājumu iestatījumi, kas ir grāmatoti kā notiekošs process vai nepabeigtā ražošana. Lapā **Ražošanas pasūtījumu informācija** tiek atiestatīti lauki, kuros ir redzams daudzums, kas ir sākts vai reģistrēts kā pabeigts. Tiek atiestatīti arī šo transakciju datumi.




