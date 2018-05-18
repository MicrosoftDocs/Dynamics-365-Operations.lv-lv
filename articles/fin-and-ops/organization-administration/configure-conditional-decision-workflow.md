---
title: "Konfigurēt nosacījuma lēmumu darbplūsmā"
description: "Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurēt nosacījuma lēmumu darbplūsmā

[!include [banner](../includes/banner.md)]

Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus.

Nosacījuma lēmums ir punkts, kurā darbplūsma sadalās divos atzaros. Lai konfigurētu nosacījuma lēmumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz nosacījuma lēmuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.

## <a name="name-a-decision"></a>Piešķiriet lēmumam nosaukumu
Lai ievadītu nosacījuma lēmuma nosaukumu, izpildiet tālāk aprakstītās darbības.
1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Laukā **Nosaukums** ievadiet unikālu nosacījuma lēmuma nosaukumu.

## <a name="set-conditions"></a>Iestatiet nosacījumus
Sistēma nosaka, kurš zars tiek izmantots, novērtējot iesniegto dokumentu, lai noteiktu, vai tas atbilst konkrētajiem nosacījumiem.
1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Noklikšķiniet uz **Pievienot nosacījumu**.
3.  Ievadiet nosacījumu.
4.  Nepieciešamības gadījumā ievadiet papildu nosacījumus.
5.  Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:
    1.  Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.
    2.  Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3.  Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.
    4.  Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos formā **Rekvizīti**.






