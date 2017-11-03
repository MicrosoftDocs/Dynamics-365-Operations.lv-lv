---
title: "Ražošanas pasūtījumu nodošana izpildei"
description: "Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums. Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aa38c50a58bed5702332182b9e0827b863f536f7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="release-production-orders"></a>Ražošanas pasūtījumu nodošana izpildei

[!include[banner](../includes/banner.md)]


Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums. Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem. 

<a name="characteristics-of-the-released-state"></a>Stāvokļa Izlaists raksturojums
-------------------------------------

Stāvoklis **Izlaists** ir viens no ražošanas pasūtījuma dzīves cikla stāvokļiem. Ražošanas pasūtījumi, kuru stāvoklis ir **Izlaists**, ir pieejami izpildei ražotnē un noliktavas procesiem. Tālāk ir norādītas stāvokļa **Izlaists** raksturīpašības.

-   Ražošanas pasūtījuma stāvokli var mainīt uz **Izlaists**, izmantojot ražošanas pasūtījumu vai pakešveida apstrādi. Ražošanas pasūtījumu var arī automātiski atjaunināt, izmantojot plānotos ražošanas pasūtījumus, kas ir apstiprināti, izmantojot lauku **Apstiprināšanas periods** lapā **Vispārējais plāns**.
-   Stāvoklis **Izlaists** norāda ražotnes operatoriem (operatoriem), ka viņi var sākt ražošanas darbu izpildi ražotnē.
-   Ražošanas dokumenti, piemēram, maršrutu kartes, maršrutu darbi, un darbu kartes, sniedz informāciju par ražošanas darbiem, un tos var izsniegt.
-   Materiāliem, kas ir fiziski rezervēti, tiek ģenerēts noliktavas darbs, lai izdotu materiālus ražošanas pasūtījumam.

## <a name="releasing-jobs-to-the-shop-floor"></a>Darbu izlaišana izpildei ražotnē
Kad ražošanas pasūtījums ir izlaists, ar to saistītie ražošanas darbi ir redzami un pieejami reģistrācijai. Operatori var reģistrēt darbus, piemēram, Sākt, Apturēt, Pabeigšana, lapā **Darbu karšu terminālis** vai **Darbu kartes ierīce**. Reģistrētie laika un daudzuma dati tiek automātiski pārsūtīti no reģistrācijas lapas uz ražošanas žurnāliem, lai sekotu līdzi laika un resursu patēriņam.

## <a name="route-cards"></a>Maršruta kartes
Maršruta karte nodrošina pārskatu par informāciju no maršruta, operācijas iestatījumiem un operāciju un darbu plānošanas metodēm.

## <a name="route-jobs"></a>Maršruta darbi
Maršruta darbs sniedz detalizētu informāciju par katru operācijas darbu, un tajā ir ietverti iestatīšanas, procesa, gaidīšanas un transportēšanas laiki. Piemēram, tādai operācijai kā krāsošana var būt nepieciešami atsevišķi darbi, piemēram iestatīšanas laiks, izpildes laiks krāsošanas procesam un gaidīšanas laiks žāvēšanai.

## <a name="job-cards"></a>Darba kartes
Darbu kartē ir norādīti noteiktas operācijas atsevišķo darbu numuri. Katrā lapā ir redzams viens darbs. Darba kartē iekļautie darbi un to paredzami laiki tiek ņemti no maršruta un operācijas iestatīšanas informācijas. Darbu kartē varat atvērt lapu **Ražošanas žurnāla rindas**, **darbu karte**. Darbinieki, kas strādā ar operācijas resursiem, var sniegt atsauksmes par ražošanas procesu. Šeit ir lauki, kur varat ievadīt patēriņa statistiku un tādu informāciju kā kļūdu daudzums.

## <a name="warehouse-work-for-raw-material-picking"></a>Izejmateriālu izdošanas noliktavas darbs
Izlaišanas laikā tiek ģenerēts izejmateriālu izdošanas darbs. Darbs tiek ģenerēts tikai tam materiālu daudzumam, kas tika fiziski rezervēts ražošanas pasūtījumam pirms pasūtījuma nodošanas izpildei. Lai varētu ģenerēt noliktavas darbu izejmateriālu izdošanai, ir jāveic tālāk norādītie iestatījumi.

-   Izejmateriālu izdošanas novietojuma direktīva, kas nosaka, kurā noliktavas novietojumā ir jāizdod materiāli
-   Izejmateriālu laidiena veidne, kur ir konfigurēti noliktavas darba izpildes ierobežojumi
-   Ražošanas ievades novietojums, kas nosaka, kur materiāli tiek novietoti





