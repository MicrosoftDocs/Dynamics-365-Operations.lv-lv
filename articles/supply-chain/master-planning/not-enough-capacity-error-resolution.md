---
title: Labot plānošanas programmas kļūdu un ierobežoto noslodzi
description: Šajā rakstā ir sniegta informācija par iemesliem un rīkojumiem, kas paredzēti tam, ka ražošanas %1 pasūtījums nav ieplānots. Plānošanas rīka kļūda "Nav atrasts pietiekami daudz kapacitātes".
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135605"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Plānošanas rīka kļūdas "Nav atrasts pietiekami daudz kapacitātes" novēršana

[!include [banner](../includes/banner.md)]

Palaižot plānošanu, iespējams, saņemsit šādu kļūdas ziņojumu:

> Ražošanas pasūtījumu %1 nevarēja plānot. Nav atrasts pietiekami daudz kapacitātes.

Ir vairāki iemesli, kāpēc plānošanas rīkam radās problēma un tiek radīts šis ziņojums. Šajā rakstā ir sniegtas vadlīnijas, kas palīdzēs atrast kļūdas saknes iemeslu un pēc tam to samazināt.

## <a name="review-the-applicable-resources"></a>Pārskatiet piemērojamos resursus

Šī kļūda var rasties, ja nav piemērojamu resursu, kuri atbilstu darbības prasībām ražošanas pasūtījuma vietā.

Lai pārskatītu piemērojamos resursus, izpildiet šīs darbības.

1. Dodieties uz **Ražošanas kontrole\> Ražošanas pasūtījumi\> Visi ražošanas pasūtījumi** un atveriet vai atlasiet to ražošanas pasūtījumu, kuru nevar ieplānot.
1. Darbību rūts cilnē **Ražošanas pasūtījums**, grupā **Ražošanas informācija** atlasiet **Maršruts**.
1. Lapā **Ražošanas maršruts** atlasiet darbību un Darbību rūtī atlasiet **Piemērojamie resursi**.
1. Dialoglodziņā **Piemērojamie resursi** iestatiet lauku **Izmantot prasības** uz *Darbību plānošana* vai *Darba plānošana* atkarībā no grafika veida, kuru izmantojat.
1. Pārliecinieties, ka ražošanas pasūtījuma vietā ir piemērojamie resursi.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Pārskatiet kalendārus, kuri ir saistīti ar resursiem

Šī kļūda var tikt parādīta, ja ar resursu vai resursu grupu nav saistīts neviens kalendārs vai ja saistītais kalendārs nav pareizi iestatīts (piemēram, tam nav darba laika vai tā efektivitāte procentos ir 0 \[nulle\]).

Lai verificētu, vai kalendārs ir saistīts ar resursu vai resursu grupu, izpildiet šīs darbības.

1. Dodieties uz **Ražošanas kontrole\> Ražošanas pasūtījumi\> Visi ražošanas pasūtījumi** un atveriet vai atlasiet to ražošanas pasūtījumu, kuru nevar ieplānot.
1. Darbību rūts cilnē **Ražošanas pasūtījums**, grupā **Ražošanas informācija** atlasiet **Maršruts**.
1. Lapā **Ražošanas maršruts** atlasiet darbību un Darbību rūtī atlasiet **Piemērojamie resursi**.
1. Dialoglodziņā **Piemērojamie resursi** atlasiet resursu un pēc tam atlasiet **Skatīt resursu**. Jūs varat arī atlasīt un turēt (vai nospiest labo peles taustiņu) laukā **Resursu grupa** un pēc tam atlasīt **Skatīt informāciju**.
1. Lapas **Resursi** vai **Resursu grupas** kopsavilkuma cilnē **Kalendāri** pārliecinieties, ka kalendārs ir saistīts ar resursu vai resursu grupu.

> [!NOTE]
> Ja darba plānošanas laikā rodas kļūda, ir jānodrošina, ka kalendārs ir saistīts ar visām piemērojamajām resursu grupām.

Lai pārskatītu kalendāra iestatījumu, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas pārvaldība\> Iestatīšana\> Kalendāri\> Kalendāri** un atlasiet kalendāru, kas ir saistīts ar resursu vai resursu grupu.
1. Darbību rūtī atlasiet **Darba laiki**.
1. Lapā **Darba laiki** pārliecinieties, ka lapa nav atstāta tukša. Turklāt pārliecinieties, ka jums interesējošo dienu lauks **Vadība** nav iestatīts uz vērtību *Slēgta*, ka ir norādīti darba laiki un ka lauks **Efektivitāti izsaka procentos** nav iestatīts uz *0* (nulli).

Ja kalendāru saista ar bāzes kalendāru, ir jāpārskata arī bāzes kalendāra iestatījumi.

> [!NOTE]
> Darbību plānošanā resursu grupas kalendāru izmanto, lai noteiktu katras darbības sākuma un beigu laiku. Tas arī ierobežo laika daudzumu, kurā sistēma var plānot vienu konkrētu darbību vienā konkrētā dienā vienā konkrētā resursu grupā. Piemēram, ja resursu grupas darba laiki konkrētā dienā ir no plkst. 8:00 līdz plkst. 16:00, krava, kuru viena darbība uzliek resursu grupai, nedrīkst pārsniegt kravu, kura tiek piemērota astoņām stundām — neatkarīgi no pieejamās kapacitātes, kura resursu grupai tajā dienā ir. Taču pieejamā kapacitāte var papildu ierobežot kravu.

## <a name="review-the-scheduling-parameters"></a>Pārskatiet plānošanas parametrus

Lai nodrošinātu labu sniegumu, plānošanas rīks meklēs resursu tikai konkrētā laika daudzumā un konkrētam skaitam plānošanas konfliktu.

Lai pārskatītu plānošanas parametrus, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas pārvaldība \> Iestatījumi \> Plānošanas parametri**.
1. Izpildiet kādu no šīm darbībām:

    - Ja opcija **Plānošanas noilgums iespējots** ir iestatīta uz *Nē*, pārejiet uz 3. darbību.
    - Ja opcija **Plānošanas noilgums iespējots** ir iestatīta uz *Jā*, palieliniet lauka **Maksimālais plānošanas laiks katrai secībai** vērtību, lai dotu vairāk laika apstrādes pabeigšanai.

1. Izpildiet kādu no šīm darbībām:

    - Ja opcija **Plānošanas optimizācijas noilgums iespējots** ir iestatīta uz *Nē*, pārejiet uz 4. darbību.
    - Ja opcija **Plānošanas optimizācijas noilgums iespējots** ir iestatīta uz *Jā*, palieliniet lauka **Optimizācijas mēģinājumu noilgums** vērtību, lai dotu vairāk laika apstrādes pabeigšanai.

1. Ja lapā mainījāt kādu no iestatījumiem, pārplānojiet pasūtījumu, lai mēģinātu vēlreiz.

## <a name="review-capacity"></a>Pārskatiet noslodzi

Kļūda var rasties, veicot ierobežotu plānošanu, bet nav brīvas noslodzes.

Lai veiktu plānošanu ar bezgalīgu noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Ražošanas kontrole\> Ražošanas pasūtījumi\> Visi ražošanas pasūtījumi** un atveriet vai atlasiet to ražošanas pasūtījumu, kuru nevar ieplānot.
1. Darbību rūts cilnes **Grafiks** grupā **Ražošanas pasūtījums** atlasiet **Plānot darbības** vai **Plānot darbus**.
1. Dialoglodziņā **Darbību plānošana** vai **Darbu plānošana** iestatiet opciju **Galīga noslodze** uz vērtību *Nē*.
1. Lai plānotu pasūtījumu, atlasiet **Labi**.

Lai pārskatītu pieejamo resursa noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas pārvaldība \> Resursi \> Resursi** un atlasiet resursu, kas ir piemērojams pasūtījumam, kuru nevar ieplānot.
1. Darbību rūts **cilnē Resurss grupā** **Skats atlasiet Noslodzes grafiks vai** **·** **Noslodzes grafiks un pārliecinieties, vai ir pieejama noslodze.**

Lai pārskatītu pieejamo resursu grupas noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas pārvaldība \> Resursi \> Resursu grupas** un atlasiet resursu grupu, kas ir piemērojama pasūtījumam, kuru nevar ieplānot.
1. Darbību rūtī cilnē Resursu **grupa** **grupā** Skats atlasiet Noslodzes grafiks **vai** **Noslodzes** grafiks un pārliecinieties, ka ir pieejama noslodze.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Vispārējās plānošanas grāmatas resursam, kad resursu kalendārs ir slēgts

Izmantojot operāciju plānošanu, vispārējā plānošana plānos noslodzi saskaņā ar primārās resursu grupas kalendāru. Tā grāmatu par sekundāro operāciju vienlaicīgi ar primāro operāciju un neņemiet vērā sekundārās operācijas kalendārus vai noslodzi. Tā rezultātā ražošanas pasūtījums var tikt plānots slēgtā kalendārā vai laikā, kad sekundārā operācija nav pieejama (kalendārs slēgts, nav noslodzes).

Izmantojot darbu plānošanu, vispārējā plānošanā, plānojot pasūtījumu, tiek ņemta vērā gan primārās, gan sekundārās operācijas noslodze un kalendārs. Lai pasūtījumu ieplānotu, kalendārus abu operāciju resursiem ir jābūt atvērtiem un tiem ir pieejama noslodze.

## <a name="maximum-job-lead-time-is-too-short"></a>Maksimālais izpildes laiks ir par īsu

Plānošanas programma nevarēs **plānot** pasūtījumu, ja atrašanās vietai iestatītais maksimālais darba izpildes laiks ir mazāks par krājumam norādīto izpildes laiku tā noklusējuma pasūtījuma iestatījumos vai vajadzības iestatījumos.

Lai skatītu vai rediģētu **vietai iestatījumu** Maksimālais darba izpildes laiks, dodieties **\>\>** uz sadaļu Ražošanas kontroles iestatīšanas ražošanas kontroles parametri un atveriet **cilni** Vispārīgi.

Lai skatītu vai rediģētu krājuma pasūtījuma noklusējuma iestatījumus, rīkojieties šādi:

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Sarakstā atrodiet un atlasiet atbilstošo preci.
1. Darbību rūtī atveriet cilni Pārvaldīt krājumus **un** atlasiet Pasūtījuma noklusējuma **iestatījumus**.
1. Izvērsiet kopsavilkuma cilni **Krājumi** un pēc nepieciešamības skatiet **vai rediģējiet krājumu izpildes** laika iestatījumu.

Lai apskatītu vai rediģētu vajadzību iestatījumus krājumam, sekojiet šiem soļiem:

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Sarakstā atrodiet un atlasiet atbilstošo preci.
1. Darbību rūtī atveriet cilni Plāns **un** atlasiet Krājumu **vajadzība**.
1. Atveriet cilni **Izpildes laiks** un pēc nepieciešamības skatiet **vai rediģējiet** ražošanas laika vērtību.

## <a name="excessive-quantity-of-required-resources"></a>Nepieciešamo resursu pārmērīga daudzums

Plānošanas laikā programma mēģina saskaņot maršruta operācijai iestatīto resursu daudzumu ar piemērojamajiem resursiem saskaņā ar operācijas resursu prasībām. Pārāk liela resursu daudzuma iestatīšana var radīt to, ka maršruts nav realizējams, un tas radīs plānošanas kļūdu.

Lai pārbaudītu gan norādīto daudzumu, gan pie piemērotos resursus atlasītajai precei, maršrutam un maršruta operācijai, izmantojiet šādas procedūras:

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Režģī atrodiet un atlasiet atbilstošo preci.
1. Darbību rūtī atveriet cilni Inženiers **un** atlasiet **Maršrutu**.
1. Režģī atrodiet un atlasiet atbilstošo maršrutu.
1. Atveriet cilni **Pārskats** lapas apakšā.
1. Atlasiet operāciju no izvēlēto maršruta operāciju saraksta.
1. Atlasiet **Piederīgs** resursi, lai atvērtu dialogu, kur varat skatīt piederīgs resursus atlasītajai maršruta operācijai.
1. Atveriet cilni **Resursu** noslodze. **Šeit** laukā Daudzums tiek rādīts resursu daudzums, kas vajadzīgs atlasītajai maršruta operācijai. Nepieciešamības gadījumā skatiet un/vai rediģējiet to.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
