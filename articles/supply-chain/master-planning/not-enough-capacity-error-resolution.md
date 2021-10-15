---
title: Plānošanas rīka kļūdas "Nav atrasts pietiekami daudz kapacitātes" novēršana
description: Šajā tēmā sniegta informācija par iemesliem un risinājumiem tam, kāpēc Ražošanas pasūtījumu %1 nav iespējams plānot. Plānošanas rīka kļūda "Nav atrasts pietiekami daudz kapacitātes".
author: ChristianRytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 16626a7ee74e89bd129d8435a17d16b41a5e0387
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565763"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Plānošanas rīka kļūdas "Nav atrasts pietiekami daudz kapacitātes" novēršana

[!include [banner](../includes/banner.md)]

Palaižot plānošanu, iespējams, saņemsit šādu kļūdas ziņojumu:

> Ražošanas pasūtījumu %1 nevarēja plānot. Nav atrasts pietiekami daudz kapacitātes.

Ir vairāki iemesli, kāpēc plānošanas rīkam radās problēma un tiek radīts šis ziņojums. Šajā tēmā sniegti norādījumi, kuri palīdzēs atrast galveno kļūdas cēloni un to mazināt.

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

Šī kļūda var rasties, ja veicat plānošanu ar galīgu vērtību, taču nav pieejama noslodze.

Lai veiktu plānošanu ar bezgalīgu noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Ražošanas kontrole\> Ražošanas pasūtījumi\> Visi ražošanas pasūtījumi** un atveriet vai atlasiet to ražošanas pasūtījumu, kuru nevar ieplānot.
1. Darbību rūts cilnes **Grafiks** grupā **Ražošanas pasūtījums** atlasiet **Plānot darbības** vai **Plānot darbus**.
1. Dialoglodziņā **Darbību plānošana** vai **Darbu plānošana** iestatiet opciju **Galīga noslodze** uz vērtību *Nē*.
1. Lai plānotu pasūtījumu, atlasiet **Labi**.

Lai pārskatītu pieejamo resursa noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas pārvaldība \> Resursi \> Resursi** un atlasiet resursu, kas ir piemērojams pasūtījumam, kuru nevar ieplānot.
1. Darbību rūts cilnes **Resursi** grupā **Skatīt** atlasiet opciju **Noslodze** vai **Noslodze grafiski** un pārliecinieties, ka ir pieejama noslodze.

Lai pārskatītu pieejamo resursu grupas noslodzi, izpildiet šīs darbības.

1. Dodieties uz **Organizācijas pārvaldība \> Resursi \> Resursu grupas** un atlasiet resursu grupu, kas ir piemērojama pasūtījumam, kuru nevar ieplānot.
1. Darbību rūts cilnes **Resursu grupa** grupā **Skatīt** atlasiet opciju **Noslodze** vai **Noslodze grafiski** un pārliecinieties, ka ir pieejama noslodze.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
