---
title: Tās pašas partijas rezervēšana pārdošanas pasūtījumam
description: Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju.
author: omulvad
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0937be76aa687ed986ff83e67f2db3e2dadd0f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807660"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Tās pašas partijas rezervēšana pārdošanas pasūtījumam

[!include [banner](../includes/banner.md)]

Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju.

Tās pašas partijas rezervēšana ļauj rezervēt krājumus pārdošanas pasūtījuma rindai no vienas krājumu partijas. Piemēram, debitors, kurš pasūta tapetes, var pieprasīt, lai viss pasūtījums tiktu izpildīts, izmantojot vienu partiju vai laidienu, lai izvairītos no neatbilstībām tapešu ruļļos. Lai iestatītu to, ka precei tiks izmantota tās pašas partijas rezervēšana, precei piešķirtajai krājumu modeļu grupai, izsekošanas dimensiju grupai un noliktavas dimensiju grupai jābūt aktīviem šādiem iestatījumiem:

- **Krājumu modeļu grupas** — krājumu modeļu grupai ir jābūt atlasītiem laukiem **Tās pašas partijas atlasīšana** un **Konsolidēt vajadzību** krājumu politiku lauku grupā **Rezervācija**.
- **Izsekošanas dimensiju grupas** — izsekošanas dimensiju grupai ir jāatlasa lauks **Vajadzības plāns pa dimensijām** partijas numuram.
- **Noliktavas dimensiju grupas** — noliktavas dimensiju grupai vienumam **Vieta** un **Noliktava** jābūt atlasītam laukam **Vajadzības plāns pa dimensijām**.

Ja rezervējat krājumus precei pārdošanas pasūtījuma rindā, kas ir iestatīta tās pašas partijas atlasei, sistēma mēģina rezervēt pasūtīto daudzumu no vienas krājumu partijas. Tiek ņemtas vērā arī konkrētas partijas atribūta prasības. Ja daudzumu nevar aizpildīt no vienas partijas, tiek parādīta lapa **Tās pašas partijas rezervēšanas konflikts**. Šajā lapā ir aprakstītas problēmas, kā arī darbības, ko varat veikt, lai turpinātu rezervēšanu. Partijas rezervēšanu var liegt šādi nosacījumi:

- Partijas atgriešanas metodes kodam vienums **Bloķēt rezervāciju** pārdošanai ir atzīmēts kā **Bloķēts**.
- Partijai ir beidzies derīguma termiņš, uz beigu datumu un attiecīgajām pārdošanas debitoriem dienām. Krājums joprojām var būt derīgs rezervēšanai, ja attiecīgā krājuma gadījumā uz krājumu modeļu grupu attiecas datuma kontroles princips “pirmais beidzies, pirmais ārā” un ja kā izdošanas kritērijs ir atlasīts derīguma termiņa datums.
- Partijas atlikušais glabāšanas laika dienu skaits nav pietiekams, pamatojoties uz beigu datumu un derīguma termiņa datumu, pie kura pieskaita pārdošanas debitoriem dienas.

Krājumiem, kas saistīti ar noliktavas dimensiju grupu, kurai ir iespējota opcija **Izmantot noliktavas vadības procesus**, varat rezervēt konkrētus partijas numurus, izmantojot rezervāciju hierarhiju ar partijas numura krājuma dimensiju, kas noteikta virs novietojuma dimensijas. Šis rezervēšanas hierarhijas tips ir pazīstams arī kā *Partija virs \[novietojuma\]* rezervēšanas hierarhijas. Lapa **Partijas rezervācija** pārsūtīšanas pasūtījuma rindām ļauj izvēlēties un rezervēt vairākas rindas, pamatojoties uz pieejamiem partijas numuriem. Papildinformāciju par to, kā rīkoties, ja izmantojat rezervāciju hierarhiju, kurai ir partijas numura dimensija zem vietas (*Partija zem \[novietojuma\]*), skatiet [Elastīga noliktavas līmeņa dimensiju rezervācijas politika](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
