---
title: Kravas veidnes
description: Šajā tēmā ir aprakstīts, kā iestatīt kravas veidnes un kā kravas veidni saistīt ar jaunu kravu.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d33e4c71680947316b540d2aef7a7220305f2054
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674650"
---
# <a name="load-templates"></a>Kravas veidnes

[!include [banner](../../includes/banner.md)]

Kad izveidojat jaunu kravu, varat piešķirt kravas veidni. Kravas veidnē ir ietverta informācija par aprīkojumu un par tādiem mērījumiem kā, piemēram, kravas augstums, platums, dziļums un tilpums.

Šajā tēmā ir aprakstīts, kā iestatīt kravas veidnes un kā kravas veidni saistīt ar jaunu kravu.

## <a name="set-up-a-load-template"></a>Kravas veidnes iestatīšana

1. Doties uz **Transportēšanas pārvaldība \> Uzstādīšana \> Kravas plānošana \> Kravas veidne**.
1. Darbības rūtī atlasiet **Jauns**, lai pievienotu jaunu veidni vai **Rediģēt**, lai rediģētu esošo veidni.
1. Jaunās vai esošās veidnes rindā iestatiet šādus laukus:

    - **Kravas veidnes ID** - ievadiet unikālu kravas veidnes identifikatoru (ID).
    - **Aprīkojums** - atlasiet aprīkojumu, kas jāizmanto kravas nosūtīšanai.
    - **Kravas augstums**, **Kravas platums** un **Kravas dziļums** - ievadiet kravas dimensijas.
    - **Maks. atļautais kravas tilpums** un **Maks. atļautais kravas svars** - ievadiet maksimālo atļauto kravas apjomu un svaru.
    - **Maksimālais atļautais bruto svars** - ievadiet maksimālo atļauto kravas bruto svaru. Kravas bruto svars ietver gan kravas taras svaru, gan kravas noslodzes svaru.
    - **Maksimālais atļautais kravas vienību skaits** - ievadiet maksimālo kravas vienību skaitu, ko var saturēt krava.
    - **Kravas noslodze uz grīdas** — atzīmējiet šo izvēles rūtiņu, lai lietotu grīdas noslodzi. Grīdas nestspējas gadījumā kastes konteinerā tiek sakrautas no grīdas līdz griestiem un no vienas sienas līdz otrai, maksimizējot iekšējo ietilpību.

1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="associate-a-load-template-with-a-new-load"></a>Kravas veidnes saistīšana ar jaunu kravu

1. Dodieties uz **Transportēšanas pārvaldība \> Plānošana \> Kravu plānošanas rīks**.
1. Lapas augšdaļā atlasiet vienu no šīm cilnēm atkarībā no pirmdokumenta tipa, kuram tiek veidota krava: **Sūtījumi**, **Pārdošanas rindas**, **Pārsūtīšanas rindas** vai **Pirkšanas pasūtījuma rindas**. 
1. Atlasiet konkrētu dokumentu, kam plānot kravu.
1. Darbību rūtī cilnē **Piedāvājums un pieprasījums** grupā **Pievienot**, atlasiet **Jaunai kravai**.
1. Dialoglodziņā **Kravas veidne** laukā **Kravas veidnes ID** atlasiet veidni, ko piemērot.
1. Atlasiet **Labi**, lai pielietotu veidni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]