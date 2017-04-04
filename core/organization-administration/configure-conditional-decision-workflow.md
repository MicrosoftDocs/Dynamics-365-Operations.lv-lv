---
title: "Konfigurēt nosacīts lēmums darbplūsmā"
description: "Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 3bba3d849d02cd84c2c0e0c5c15f7b649b3e125c
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurēt nosacīts lēmums darbplūsmā

Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus.

Nosacījuma lēmums ir punkts, kurā darbplūsma sadalās divos atzaros. Lai konfigurētu nosacījuma lēmumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz nosacījuma lēmuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.

## <a name="name-a-decision"></a>Piešķiriet lēmumam nosaukumu
Lai ievadītu nosacījuma lēmuma nosaukumu, izpildiet tālāk aprakstītās darbības.
1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Laukā **Nosaukums** ievadiet unikālu nosacījuma lēmuma nosaukumu.

## <a name="set-conditions"></a> Iestatiet nosacījumus
Sistēma nosaka, kurš zars tiek izmantots, novērtējot iesniegto dokumentu, lai noteiktu, vai tas atbilst konkrētajiem nosacījumiem.
1.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2.  Click **Add condition**.
3.  Ievadīt nosacījumu.
4.  Nepieciešamības gadījumā ievadiet papildu nosacījumus.
5.  Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:
    1.  Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.
    2.  Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.
    3.  Noklikšķiniet uz **Tests**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.
    4.  Noklikšķiniet uz **OK** vai **atcelt** atgriezties **Properties** formu.




