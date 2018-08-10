---
title: "Operāciju plānošana"
description: "Šajā tēmā ir sniegta informācija par operāciju plānošanu. Operāciju plānošanu var lietot, lai sniegtu vispārēju ražošanas procesa novērtējumu laika periodam."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 660d6b2dfb5fbed58a5c28b77aac3bb4604c7d8d
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="operations-scheduling"></a>Operāciju plānošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par operāciju plānošanu. Operāciju plānošanu var lietot, lai sniegtu vispārēju ražošanas procesa novērtējumu laika periodam.

Varat plānot ražošanu operāciju līmenī un darbu līmenī. Atšķirībā no darbu plānošanas operāciju plānošana neizvērš ražošanas maršruta operācijas darbos. Ja vēlaties plānošanā iekļaut vairāk informācijas, piemēram, informāciju par pašreizējo noslodzi, varat palaist darbu plānošanu pēc operāciju plānošanas palaišanas. Varat arī palaist tikai darbu plānošanu. Darbu plānošana parasti tiek izmantota atsevišķu darbu plānošanai ražotnē nekavējoties vai īstermiņa periodā.

## <a name="components-of-operations-scheduling"></a>Operāciju plānošanas komponenti
Operāciju plānošanas galvenie komponenti ir plānošanas virziens, resursu noslodze un materiālu optimizācija. Izmantojot operāciju plānošanu, jūs varat sasniegt šādus mērķus:

-   Kontrolējiet plānošanas metodi, veicot plānošanu uz priekšu vai atpakaļ no attiecīgā datuma.
-   Optimizējiet resursu izmantošanu, plānojot ražošanu, kas balstās uz resursu noslodzi. Šī pieeja arī palīdz noteikt, kad ir jāizmanto alternatīvie resursi.
-   Optimizējiet materiālu izmantošanu, plānojot ražošanu, kas balstās uz nepieciešamo materiālu pieejamību.
-   Plānojiet un sinhronizējiet atsauces ražošanas uzdevumus. Atsauces ražošanas uzdevumu datumi tiek pielāgoti, kad tiek mainīts ražošanas pasūtījuma grafiks.

Pirms operāciju plānošanas palaišanas ir jānovērtē ražošanas pasūtījuma izmaksas. Ja neesat palaidis novērtējumu, tas tiks palaists automātiski pirms operāciju plānošanas sākšanas. Operāciju plānā ir norādīta šāda informācija:

-   Prece, kuru plānots ražot
-   Preces konfigurācija
-   Ražošanā iesaistītais daudzumus
-   Ražošanas sākuma un beigu datums
-   Noslodzes rezervācijas resursiem, kas veic ražošanas darbības

Iestatīšanas laiks, apstrādes laiks un izpildes laiks ir iestatīts ražošanas operācijām Pēc operāciju plānošanas palaišanas ražošanas pasūtījuma statuss ir **Plānots**, un visas operācijas tiek plānotas tādā secībā, kāda ir norādīta ražošanas maršrutā. Tomēr tiek ņemts vērā tikai operācijas ilgums. Sākuma laiki un beigu laiki netiek plānoti.

## <a name="scheduling-direction-and-date"></a>Plānošanas virziens un datums
Plānošanas virziens ir plānošanas procesa pamatā. Ražošanu var plānot uz priekšu un atpakaļ no jebkura datuma atkarībā no laika un plānošanas prasībām.

-   **No plānošanas datuma uz priekšu** — jūs varat plānot ražošanas sākšanu pēc iespējas agrāk. Ražošanu var sākt šodien, rīt vai jebkurā citā datumā nākotnē. Ražošana tiek plānota uz priekšu līdz agrākajam iespējamajam beigu datumam.
-   **No plānošanas datuma atpakaļ** — jūs varat plānot ražošanas sākšanu pēc iespējas vēlāk. Atpakaļejošā plānošana balstās uz datumu, kad ražošana jāpabeidz. Grafikā tiek veikta skaitīšana atpakaļ no attiecīgā datuma līdz pēdējam iespējamajam datumam, kurā var sākt ražošanu un laikus to pabeigt.

## <a name="resource-scheduling"></a>Resursu plānošana
Izpildot operāciju grafiku, katra operācija ražošanas maršrutā ir plānota resursam, kas norādīts attiecīgajai operācijai. Turklāt katras operācijas ilgums ir norādīts ražošanas maršrutā. Ja operācijai ir norādīta resursu grupa, plānošana rezervē noslodzi grupai. Tomēr atšķirībā no darba plānošanas operāciju plānošana neatlasa noteiktus resursus grupā. Ja strādājat ar ierobežotu noslodzi, grafiks būs atkarīgs no tādu resursu pieejamības, kas nepieciešami ražošanas pabeigšanai. Operāciju plānošana ievēro operāciju secību, kas norādīta ražošanas maršrutā. Plānošana rezervē noslodzi resursu grupās, pamatojoties uz darbības laikiem, kas definēti ražošanas maršrutā. Iesaistīto resursu kopējā pieejamā noslodze nosaka resursu grupas noslodzi. Noslodzes rezervācijas, kas jau pastāv resursiem, tiek uzskatītas par nepieejamu noslodzi. Ja nav pietiekami daudz pieejamās noslodzes ražošanai, ražošanas pasūtījumus var aizkavēt vai pat apturēt. Varat arī norādīt efektivitāti, kuru sagaidāt no resursiem, kas ir iesaistīti ražošanā. Efektivitāti norāda procentos attiecīgajam resursam. Efektivitātes procentuālā vērtība pielāgo resursa caurlaidspēju. Šis pielāgojums ietekmē laiku, kas ir rezervēts resursam. Tiek atbilstoši pielāgoti arī tādu darbību veikšanas izpildes laiki, kurās izmantots resurss.

## <a name="operations-scheduling-and-master-planning"></a>Operāciju plānošana un vispārējā plānošana
Operāciju plāns vada arī vispārējo plānošanu un nosaka materiālu vajadzību aprēķinus. Operāciju plānošana ņem vērā šādu informāciju:

-   **Nepabeigtā ražošana** — preces ir plānotas, izlaistas vai iesāktas ražot
-   **Materiālu pieejamība** — krājumi, apakšražošana, piegādātāji un kreditori
-   **Noslodzes pieejamība** — ražošanai nepieciešamie resursi

## <a name="cancellations"></a>Atcelšanas
Izpildot operāciju plānošanu, var atcelt noteiktas maršruta daļas. Šīs daļas ietver gaidīšanas laiku, uzstādīšanas laiku, apstrādes laiku, pārklāšanās laiku un transportēšanas laikus.

## <a name="finite-materials"></a>Ierobežoti materiāli
Ja strādājat ar ierobežotiem materiāliem, plānošana ir atkarīga arī no ražošanai nepieciešamo materiālu pieejamības. Ja nav pietiekami daudz pieejamo sastāvdaļu ražošanai, tā var aizkavēties. Varat balstīt plānošanu uz materiālu izmantošanu, norādot materiālus, kuriem ir jābūt pieejamiem ražošanai. Optimizējot pēc resursu noslodzes un materiālu pieejamības, ražošana tiek aprēķināta saskaņā ar šiem ierobežojumiem. Ražošanas pasūtījuma sākumu nevar plānot, kamēr noslodze un materiāli nav pieejami tajā pašā laikā un nepieciešamajā daudzumā.

<a name="additional-resources"></a>Papildu resursi
--------

[Operāciju plānošanas opcijas](operation-scheduling-options.md)




