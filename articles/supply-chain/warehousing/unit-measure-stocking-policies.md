---
title: "Mērvienību un uzkrājumu politikas"
description: "Šajā raksta ir aprakstīts, kā noliktavas procesos izmantot noklusējuma vienības, kā arī vienību secību un pārveidošanu."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0a22e07f5a0e5bc30c8ad9dc87c5a506d62847d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="unit-of-measure-and-stocking-policies"></a>Mērvienību un uzkrājumu politikas

[!INCLUDE [banner](../includes/banner.md)]

Šajā raksta ir aprakstīts, kā noliktavas procesos izmantot noklusējuma vienības, kā arī vienību secību un pārveidošanu.

Vienību secību grupas nosaka to vienību secību, ko var izmantot noliktavas operācijās. Tās tiek izveidotas lapā **Vienību secību grupas**. Šī secība rāda dažādo vienību attiecības. Pieņemsim, ka jūs uzglabājat paletes, uz kurām ir kastes, kurās ir atsevišķas krājumu vienības. Šādā gadījumā ir jānodrošina trīs dažādas vienības un slāņu loģiskā secība. Vienību sēriju grupas ļauj definēt noliktavas vienību grupēšanas ierobežojumus un noklusējuma vienības, kas ir jāizmanto dažādos noliktavas procesos. Šis raksts attiecas gan uz papildu noliktavas risinājumiem, kas ir pieejamai modulī Noliktavas pārvaldība, gan uz vienkāršākiem noliktavas risinājumu, kas ir pieejami modulī Krājumu vadība.

## <a name="unit-sequence-groups-for-released-products"></a>Izlaisto preču vienību secību grupas
Ja vēlaties izmantot izlaistās preces noliktavas darba procesos, tām ir jāpiešķir vienību secību grupa. Ja apstiprināt preci, kas ir saistīta ar noliktavas dimensiju grupu, un šai noliktavas dimensiju grupai ir norādīts opcijas **Izmantot noliktavas vadības procesus** iestatījums **Jā**, jūs saņemat kļūdas ziņojumu, ja precei nav definēts vienību secību grupas ID. Ja izmantotajā vienību secību grupā ir vairākas rindas (un tāpēc vairākas vienības), ir jāiestata vienību konvertēšana starp šīm vienībām. Šos iestatījumus varat veikt lapā **Mērvienību pārveidošana**. Mazākajai vienībai ar izlaisto preci saistītajā secību grupā ir jāatbilst krājumu vienībai, kas ir definēta atbilstošajai precei. Krājumu vienība ir vienība, kas tiek izmantota rīcībā esošo krājumu pamata aprēķiniem. Varat arī iestatīt preces šablonu preču variantu mērvienību konvertēšanu, izmantojot opciju **Iespējot mērvienību konvertēšanu**.

## <a name="license-plate-grouping"></a>Numura zīmju grupēšana
Varat norādīt, vai ieejas plūsmas, kas ir mazākas vai lielākas par noteiktu vienību, ir jāgrupē vienā noliktavas vienībā vai ir jāsadala pa atsevišķām noliktavas vienībām. Lai iestatītu šo darbību, izmantojiet opciju **Numura zīmju grupēšana** lapas **Vienību secību grupas** cilnē **Rindas informācija**. Ja vēlaties izmantot noliktavas vienību grupēšanu, apstrādājot darbu mobilajā ierīcē, ir izvēlnes vienumā **Mobilā ierīce** ir jāatlasa opcija **Numura zīmju grupēšana**. Pieņemsim, ka jūs izmantojat mobilo ierīci, lai reģistrētu krājumu, kas ir saistīts ar vienību sēriju grupu ar divām rindām. Pirmā rinda atbilst gabaliem, un tai ir norādīta opcijas **Numura zīmju grupēšana** vērtība **Jā**. Otrā rinda atbilst paletes vienībai, un tai ir norādīta opcijas **Numura zīmju grupēšana** vērtība **Nē**. Šādā gadījumā sistēma var automātiski vadīt sadalīšanu pa 100 gabaliem un attiecīgu noliktavas vienību izveidi.

## <a name="units-for-cycle-counting"></a>Cikla inventarizācijas vienības
Lai definētu, kuras vienības ir jāizmanto cikla inventarizācijas procesā, atlasiet opciju **Izmantot vienību cikla inventarizācijai** lapā **Vienību secību grupas**. Šādā secību grupā varat atlasīt maksimāli četras vienības. Ja atlasāt vairāk par četrām vienībām, papildu vienības netiek rādītas mobilajā ierīcē.

## <a name="default-units-for-mobile-device-receiving-processes"></a>Mobilās ierīces saņemšanas procesa noklusējuma vienības
Lai iestatītu noklusējuma vienības, kas ir jāizmanto saņemšanas procesiem mobilajās ierīcēs, iespējojiet opcijas **Noklusējuma vienība pirkšanai un pārsūtīšanai** un **Noklusējuma vienība ražošanai** lapā **Vienību secību grupas**. Piemēram, varat norādīt, ka sistēmā pēc noklusējuma ir jāizmanto palešu daudzums, ja pirkšanas pasūtījuma rīcībā esošie krājumi tiek saņemti, izmantojot mobilo ierīci, taču kā noliktavas vienība ir jāizmanto gabali. Lai nodrošinātu katras paletes gabalu skaita konvertāciju, ir jādefinē vienību konvertācija, piemēram, 100 gab. = 1 pal.

## <a name="default-order-settings"></a>Pasūtījuma noklusējuma iestatījumi
Izlaisto preču izveides procesa ietvaros ir jāatlasa pirkšanas, pārdošanas un krājumu noklusējuma vienības, lai varētu apstrādāt dažādos pasūtījumus. Varat iestatīt noklusējuma vienības un daudzumus dažādajiem pirmdokumentiem, izmantojot lapas **Pasūtījuma noklusējuma iestatījumi** un **Atrašanās vietai raksturīgie pasūtījuma iestatījumi**. Šīm lapām varat piekļūt lapā **Izlaistās preces**.




