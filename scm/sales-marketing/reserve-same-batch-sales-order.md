---
title: "Rezerves pašu partijas pārdošanas pasūtījumam"
description: "Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e9f48e6e057517bb7632e8c855f4439c446f3d30
ms.lasthandoff: 03/31/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Rezerves pašu partijas pārdošanas pasūtījumam

Šajā rakstā ir skaidrots, kā iestatīts preces, lai atļautu krājumus rezervēt pret atsevišķu krājumu partiju.

Tās pašas partijas rezervēšana ļauj rezervēt krājumus pārdošanas pasūtījuma rindai no vienas krājumu partijas. Piemēram, debitors, kurš pasūta tapetes, var pieprasīt, lai viss pasūtījums tiktu izpildīts, izmantojot vienu partiju vai laidienu, lai izvairītos no neatbilstībām tapešu ruļļos. Lai iestatītu to, ka precei tiks izmantota tās pašas partijas rezervēšana, precei piešķirtajai krājumu modeļu grupai, izsekošanas dimensiju grupai un noliktavas dimensiju grupai jābūt aktīviem šādiem iestatījumiem:

-   **Krājumu modeļu grupas** — krājumu modeļu grupai ir jābūt atlasītiem laukiem **Tās pašas partijas atlasīšana** un **Konsolidēt vajadzību** krājumu politiku lauku grupā **Rezervācija**.
-   **Izsekošanas dimensiju grupas** — izsekošanas dimensiju grupai ir jāatlasa lauks **Vajadzības plāns pa dimensijām** partijas numuram.
-   **Noliktavas dimensiju grupas** — noliktavas dimensiju grupai vienumam **Vieta** un **Noliktava** jābūt atlasītam laukam **Vajadzības plāns pa dimensijām**.

Rezervējot krājumus precei pārdošanas pasūtījuma rindā, kurai ir iestatīta tās pašas partijas atlasīšana, programma Microsoft Dynamics 365 for Operations mēģina rezervēt pasūtīto daudzumu no vienas krājumu partijas. Tiek ņemtas vērā arī konkrētas partijas atribūta prasības. Ja daudzumu nevar aizpildīt no vienas partijas, tiek parādīta lapa **Tās pašas partijas rezervēšanas konflikts**. Šajā lapā ir aprakstītas problēmas, kā arī darbības, ko varat veikt, lai turpinātu rezervēšanu. Partijas rezervēšanu var liegt šādi nosacījumi:

-   Partijas atgriešanas metodes kodam vienums **Bloķēt rezervāciju** pārdošanai ir atzīmēts kā **Bloķēts**.
-   Partijai ir beidzies derīguma termiņš, uz beigu datumu un attiecīgajām pārdošanas debitoriem dienām. Krājums joprojām var būt derīgs rezervēšanai, ja attiecīgā krājuma gadījumā uz krājumu modeļu grupu attiecas datuma kontroles princips “pirmais beidzies, pirmais ārā” un ja kā izdošanas kritērijs ir atlasīts derīguma termiņa datums.
-   Partijas atlikušais glabāšanas laika dienu skaits nav pietiekams, pamatojoties uz beigu datumu un derīguma termiņa datumu, pie kura pieskaita pārdošanas debitoriem dienas.



