---
title: Dokumenta rindas darbplūsmu konfigurēšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt dokumenta rindas darbplūsmas elementu.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b85370a4c38bbe5511d501b1ab5afcfd8fd0838
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190193"
---
# <a name="configure-line-item-workflows"></a>Dokumenta rindas darbplūsmu konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā konfigurēt dokumenta rindas darbplūsmas elementu.

Lai konfigurētu dokumenta rindas darbplūsmas elementu, darbplūsmas redaktorā ar peles labo taustiņu noklikšķiniet uz elementa un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**. Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu dokumenta rindas darbplūsmas elementa rekvizītus.

## <a name="name-the-line-item-workflow-element"></a>Piešķiriet dokumenta rindas darbplūsmas elementa nosaukumu

Veiciet šādas darbības, lai ievadītu dokumenta rindas darbplūsmas elementa nosaukumu.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Nosaukums** ievadiet dokumenta rindas darbplūsmas elementa unikālo nosaukumu.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Norādiet, vai visu rindu apstrādei tiek izmantota tā pati darbplūsma

Veiciet šīs darbības, lai norādītu, vai visu dokumenta rindu apstrādei tiek izmantota tā pati darbplūsma.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Ja visu dokumenta rindu apstrādei jāizmanto tā pati darbplūsma, noklikšķiniet uz **Izsauciet vienu darbplūsmu visiem krājumiem rindā**. Pēc tam atlasiet darbplūsmu, ko izmantot rindu vienumu apstrādei.
3. Ja tādu rindu vienumu apstrādei, kas atbilst konkrētai nosacījumu kopai, jāizmanto noteikta darbplūsma, noklikšķiniet uz **Izsauciet darbplūsmu katram krājumam rindā**. Pēc tam veiciet šīs darbības, lai definētu nosacījumu kopu:

    1. Noklikšķiniet uz **Pievienot**.
    2. Atlasiet nosacījumu tabulā.
    3. Cilnē **Nosacījuma nosaukums** ievadiet nosaukumu nosacījumu kopai, kuru definējat.
    4. Lai ievadītu nosacījumu, noklikšķiniet uz **Pievienot nosacījumu**.
    5. Ievadiet visus nepieciešamos papildu nosacījumus.
    6. Lai pārbaudītu, vai ievadītā nosacījuma kopa ir pareizi konfigurēta, noklikšķiniet uz **Pārbaudīt**. Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu un pēc tam noklikšķiniet uz **Pārbaudīt**. Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem. Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.

    Cilnē **Darbplūsma** atlasiet darbplūsmu tādu rindu vienumu apstrādei, kuri atbilst definēto nosacījumu kopai.