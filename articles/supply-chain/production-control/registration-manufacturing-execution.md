---
title: "Ražošanas izpildes reģistrācija"
description: "Šajā tēmā ir aprakstītas galvenās koncepcijas un termini, kas ir jāsaprot, lai varētu konfigurēt un lietot ražošanas izpildi"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 939cb219a63a27ee9cb05036041d2722df3b0abc
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="registration-for-manufacturing-execution"></a>Ražošanas izpildes reģistrācija

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstītas galvenās koncepcijas un termini, kas ir jāsaprot, lai varētu konfigurēt un lietot ražošanas izpildi 

Ražošanas izpildi ir paredzēts izmantot galvenokārt ražošanas uzņēmumos. Darbinieki var reģistrēt ražošanas darbu laiku un krājumu patēriņu, izmantojot lapu **Darba reģistrācija**. Visas reģistrācijas tiek apstiprinātas un vēlāk pārsūtītas uz attiecīgajiem moduļiem. Nepārtraukta reģistrāciju apstiprināšana un pārsūtīšana ļauj vadītājiem viegli izsekot ražošanas pasūtījumu faktiskās izmaksas.

## <a name="manufacturing-execution-and-registration-terminology"></a>Reģistrācijas izpildes un reģistrācijas terminoloģija
Šajā tabulā ir norādīti termini, kas attiecas uz ražošanas izpildi un saistītajiem reģistrācijas uzdevumiem.

| Termins                          | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ražošanas izpilde       | Funkcija, kas tiek izmantota, lai reģistrētu ražošanas darbu, projektu un netiešo aktivitāšu laiku, materiālu patēriņu un izmaksas. Reģistrācija tiek veikta ražošanas izpildes reģistrācijas klientā.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Darbu saraksts                      | Lapā **Darba reģistrācija** darbiniekiem ir pieejams to darbu saraksts, kas viņiem jāveic, izmantojot noteikto resursu, piemēram, mašīnu. Darbinieks var reģistrēt laiku un krājuma patēriņu katram darbam vai uzdevumam darbu sarakstā.                                                                                                                                                                                                                                                                                                                                                                           |
| Darbu saistīšana                  | Ja darbinieks lapā **Darba reģistrācija** sāk vienlaicīgi vairāk nekā vienu darbu, to sauc par darbu saistīšanu. Saistītajos darbos pavadīto laiku var sadalīt atsevišķos darbos dažādos veidos, izmantojot sadalījuma atslēgas.                                                                                                                                                                                                                                                                                                                                                         |
| Atbildīgo/asistentu reģistrācijas | Darbinieks var reģistrēties kā resursa asistents un izveidot nelielu darba grupu, kuras vairāki darbinieki strādā ar vieniem un tiem pašiem ražošanas darbiem. Resursi, kuriem darbinieki ir piesaistīti kā asistenti, tiek saukti par atbildīgajiem. Reģistrācijas ieraksti jāveic tikai atbildīgajam resursam. Visiem asistentiem automātiskie tiek veikti vienādi reģistrācijas ieraksti. Ja, piemēram, atbildīgais elements ir mašīna, darbinieki, kas ir reģistrēti kā asistenti saistībā ar šo mašīnu, var veikt reģistrāciju lapā **Darba reģistrācija**, un gan par mašīnu, gan darbiniekiem, kas ir saistīti kā asistenti, tiek veikti vienādi reģistrācijas ieraksti. |
| Netiešā aktivitāte             | Aktivitāte vai uzdevums, kas nav tieši saistīts ar ražošanas darbu vai projektu, piemēram, nodaļas sapulce, tīrīšanas darbs vai apkopes darbs ražotnē. Darbinieki var veikt netiešo aktivitāšu reģistrācijas ierakstus tāpat, kā reģistrācijas ierakstus par ražošanas darbiem un projektiem.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Reģistrācijas ražošanas izpildē
Darbinieki var veikt dažāda veida reģistrācijas ierakstus ražošanas izpildes laikā par ražošanas darba ietvaros veiktajam darbam. Atkarībā no sistēmas iestatījumiem, darbinieki var veikt reģistrācijas ierakstus par projekta aktivitātēm un ar ražošanu nesaistītiem uzdevumiem, piemēram, pārtraukumiem, kavējumiem un netiešām aktivitātēm. Tālāk ir norādīti reģistrācijas ierakstu veidi.

-   **Ierašanās/došanās prom** (pieejams ar laika un apmeklētības ierakstiem) — darbinieki atzīmē laiku, kad viņi ir ieradušies darbā un kad devušies mājās no darba.
-   **Ražošanas darbu reģistrēšana** — darbinieki var veikt reģistrācijas ierakstus, piemēram, sākot darbu un sniedzot atgriezenisko saiti par darbu, par ražošanas darbiem, kas ir redzami viņu darbu sarakstā. Darbinieki varat sākt vairākus darbus vienlaikus. To sauc par darba saistīšanu.
-   **Reģistrācijas ieraksts par krājumiem** — darbinieks var veikt reģistrācijas ierakstus par materiāliem, kas tiek izmantoti uz veikala grīdas, bet nav tieši saistīti ar ražošanas darbiem. Materiāli var būt, piemēram, smērvielas, eļļošanas līdzekļi vai citi materiāli, ko izmanto mehānismu darbības nodrošināšanai. Reģistrāciju veic krājumu žurnālā.
-   **Reģistrācijas ieraksts par projektiem** (pieejams ar laika un apmeklētības ierakstiem) — darbinieki var veikt reģistrācijas ierakstus, piemēram, sākot un beidzot darbu pie projektiem vai projektu aktivitātēm, kas ir redzamas viņu darbu sarakstā.
-   **Projekta izmaksu un krājumu reģistrēšana** (pieejams ar laika un apmeklētības ierakstiem) — nodarbinātie var reģistrēt ar projektu saistītās izmaksas projekta izmaksu žurnālā, piemēram, nobraukumu un ceļa nodokļus. Nodarbinātie var reģistrēt arī krājumu patēriņu projektu ietvaros. Ierakstus veic projekta krājumu žurnālā.
-   **Reģistrēšanās cita darbinieka asistenta statusā** — ja divi vai vairāki darbinieki strādā kopā, izpildot ražošanas darbu vai projektu, darbinieks var reģistrēties kā mašīnas vai cita darbinieka asistents, kas darbosies kā atbildīgais. Ja nepieciešams, atbildīgais var atlasīt citu darbinieku par atbildīgo.
-   **Kavējumu reģistrēšana**(pieejams ar laika un apmeklētības ierakstiem) — darbinieki var veikt reģistrācijas ierakstus, izmantojot iestatītos kavējuma kodus. Kavējumu var norādīt, ja darbinieks ierodas ar kavēšanos, lūdz atbrīvot darba dienas laikā vai aiziet ātrāk nekā plānots saskaņā ar standarta darba laika profilu.
-   **Pārtraukuma reģistrēšana**(pieejams ar laika un apmeklētības ierakstiem) — darba dienas laikā darbinieki var veikt reģistrācijas ierakstu par to, ka viņi atstāj darba vietu, lai dotos pārtraukumā. Var iestatīt vairākus pārtraukumu veidus. Kad darbinieks atgriežas un piesakās vēlreiz, sistēmā tiek reģistrēts, ka darbinieks ir atgriezies, un pārtraukuma reģistrācija tiek pārtraukta.
-   **Netiešu aktivitāšu reģistrēšana** (pieejams ar laika un apmeklētības ierakstiem) — netiešās aktivitātes ir ar ražošanu nesaistītas darbības, kuras darbinieki var veikt darba dienas laikā, piemēram, nodaļas sapulce, grupas sapulce vai apkopes darbi, kas saistīti ar veikala grīdas uzkopšanu. Darbinieki var veikt reģistrācijas par iestatītajām netiešām aktivitātēm.
-   **Virsstundu reģistrēšana**(pieejams ar laika un apmeklētības ierakstiem) — darbinieki, kuriem ir lūgts strādāt ilgāk, var izvēlēties, vai papildu stundas reģistrēt kā brīva režīma laiks vai virsstundas.





