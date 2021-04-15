---
title: Ražošanas pasūtījumu nodošana izpildei
description: Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums. Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811706"
---
# <a name="release-production-orders"></a>Ražošanas pasūtījumu nodošana izpildei

[!include [banner](../includes/banner.md)]

Izpildei nodots ražošanas pasūtījums ir ražošanas nolūkā apstiprināts pasūtījums. Termins “nodots izpildei” tiek izmantots, lai aprakstītu ražošanas pasūtījuma dzīves cikla stāvokli, kurā ražošanas pasūtījums ir pieejams izpildei ražotnē un noliktavas procesiem.

## <a name="characteristics-of-the-released-state"></a>Stāvokļa Izlaists raksturojums

Stāvoklis **Izlaists** ir viens no ražošanas pasūtījuma dzīves cikla stāvokļiem. Ražošanas pasūtījumi, kuru stāvoklis ir **Izlaists**, ir pieejami izpildei ražotnē un noliktavas procesiem. Tālāk ir norādītas stāvokļa **Izlaists** raksturīpašības.

- Ražošanas pasūtījuma stāvokli var mainīt uz **Izlaists**, izmantojot ražošanas pasūtījumu vai pakešveida apstrādi. Ražošanas pasūtījumu var arī automātiski atjaunināt, izmantojot plānotos ražošanas pasūtījumus, kas ir apstiprināti, izmantojot lauku **Apstiprināšanas periods** lapā **Vispārējais plāns**.
- Stāvoklis **Izlaists** norāda ražotnes operatoriem (operatoriem), ka viņi var sākt ražošanas darbu izpildi ražotnē.
- Ražošanas dokumenti, piemēram, maršrutu kartes, maršrutu darbi, un darbu kartes, sniedz informāciju par ražošanas darbiem, un tos var izsniegt.
- Materiāliem, kas ir fiziski rezervēti, tiek ģenerēts noliktavas darbs, lai izdotu materiālus ražošanas pasūtījumam.

## <a name="releasing-jobs-to-the-shop-floor"></a>Darbu izlaišana izpildei ražotnē

Kad ražošanas pasūtījums ir izlaists, ar to saistītie ražošanas darbi ir redzami un pieejami reģistrācijai. Operatori var reģistrēt darbus, piemēram, Sākt, Apturēt, Pabeigšana, lapā **Darbu karšu terminālis** vai **Darbu kartes ierīce**. Reģistrētie laika un daudzuma dati tiek automātiski pārsūtīti no reģistrācijas lapas uz ražošanas žurnāliem, lai sekotu līdzi laika un resursu patēriņam.

## <a name="route-cards"></a>Maršruta kartes

Maršruta karte nodrošina pārskatu par informāciju no maršruta, operācijas iestatījumiem un operāciju un darbu plānošanas metodēm.

## <a name="route-jobs"></a>Maršruta darbi

Maršruta darbs sniedz detalizētu informāciju par katru operācijas darbu, un tajā ir ietverti iestatīšanas, procesa, gaidīšanas un transportēšanas laiki. Piemēram, tādai operācijai kā krāsošana var būt nepieciešami atsevišķi darbi, piemēram iestatīšanas laiks, izpildes laiks krāsošanas procesam un gaidīšanas laiks žāvēšanai.

## <a name="job-cards"></a>Darba kartes

Darbu kartē ir norādīti noteiktas operācijas atsevišķo darbu numuri. Katrā lapā ir redzams viens darbs. Darba kartē iekļautie darbi un to paredzami laiki tiek ņemti no maršruta un operācijas iestatīšanas informācijas. Darbu kartē varat atvērt lapu **Ražošanas žurnāla rindas**, **darbu karte**. Darbinieki, kas strādā ar operācijas resursiem, var sniegt atsauksmes par ražošanas procesu. Šeit ir lauki, kur varat ievadīt patēriņa statistiku un tādu informāciju kā kļūdu daudzums.

## <a name="warehouse-work-for-raw-material-picking"></a>Noliktavas darba izejmateriālu izdošanai

Izlaišanas laikā tiek ģenerēts izejmateriālu izdošanas darbs. Darbs tiek ģenerēts tikai tam materiālu daudzumam, kas tika fiziski rezervēts ražošanas pasūtījumam pirms pasūtījuma nodošanas izpildei. Lai varētu ģenerēt noliktavas darbu izejmateriālu izdošanai, ir jāveic tālāk norādītie iestatījumi.

- Izejmateriālu izdošanas novietojuma direktīva, kas nosaka, kurā noliktavas novietojumā ir jāizdod materiāli
- Izejmateriālu laidiena veidne, kur ir konfigurēti noliktavas darba izpildes ierobežojumi
- Ražošanas ievades novietojums, kas nosaka, kur materiāli tiek novietoti

Izmantojot noliktavas vienību, kas ir kontrolēti ar numura zīmi, var izvēlēties, vai pasūtītais daudzums vai viss krājumam pieejamais daudzums ir jāizņem, apstrādājot izejmateriālu izdošanas darbu. Lai to iestatītu:

1. Dodieties uz **Preču informācijas pārvaldība \> Preces \> Tirdzniecībā izlaistās preces** un atveriet attiecīgo krājumu.
1. Izvērsiet **Noliktava** kopsavilkuma cilni.
1. Atlasiet vienu no šīm opcijām **Materiālu izdošanas noliktavas vienību novietojumu** laukā:
    - *Pasūtījuma izdošana*: Jāpaņem tikai pasūtītais daudzums.
    - *Sagatavošana*: Ja iespējams, ir jāpaņem viss noliktavas vienībā pieejamais daudzums. Lai darbinieks varētu saņemt visu noliktavas vienības daudzumu, noliktavai nav jāietver jaukti krājumi, un tai nedrīkst būt jauktas dimensijas. Ja numura zīmi ietver jauktas dimensijas vai krājumus, izdošana tiks turpināta, it kā tā būtu iestatīta uz *Pasūtījuma izdošana*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]