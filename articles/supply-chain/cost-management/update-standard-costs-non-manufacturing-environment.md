---
title: Standarta izmaksu atjaunināšana vidē, kas nav saistīta ar ražošanu
description: Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas vidē, kas nav saistīta ar ražošanu.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 548955f544842ea5f60fd2d800c8c11cb459ee4c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679084"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Standarta izmaksu atjaunināšana vidē, kas nav saistīta ar ražošanu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti norādījumi par to, kā atjaunināt standarta izmaksas vidē, kas nav saistīta ar ražošanu.

Norādījumi tālāk tiek sniegti, pieņemot, ka standarta izmaksu atjaunināšanai tiek izmantota divu versiju pieeja. Izmantojot šo pieeju, viena izmaksu aprēķināšanas versija ietver standarta izmaksas, kas sākotnēji ir noteiktas uz fiksētu periodu, un otra izmaksu aprēķināšanas versija ietver inkrementālos atjauninājumus. Visi atjauninājumi tiek ievadīti kā izmaksu ieraksti, kas ir ietverti otrā izmaksu aprēķināšanas versijā, un galu galā tiek iespējoti. Papildu vienas versijas pieeja izmanto sākotnēji definētu standarta izmaksu kopu. Lai varētu izmantot divu versiju pieeju, jādefinē otra izmaksu aprēķināšanas versija. Tālāk ir sniegtas norādes, ka definēt šo izmaksu aprēķināšanas versiju.

-   Piešķiriet izmaksu aprēķināšanas veidu **Standartizmaksas**.
-   Piešķiriet jēgpilnu identifikatoru, kas norāda izmaksu aprēķināšanas versijas komponentus, piemēram, **2016-ATJAUNINĀJUMI**.
-   Pārliecināties, ka saturā ir ietverti izmaksu ieraksti.
-   Atļaujiet visām vietām ievadīt izmaksu ierakstus. Ja tiek norādīta vietu, izmaksu ierakstus var ievadīt tikai šai vietai.
-   Norādiet regresa principu **Nav**. Regresa princips attiecas tikai uz ražoto krājumu izmaksu aprēķiniem.

Lai labotu, pielāgotu vai atjauninātu jauno krājumu standarta izmaksas, veiciet tālāk aprakstītās darbības.

1.  Izmantojiet lapu **Izmaksu aprēķināšanas versijas** **iestatījumi**, lai iespējotu otrajā izmaksu aprēķināšanas versijā ievadāmos izmaksu datus. Papildus var nepieļaut neapstiprinātu izmaksu aktivizāciju, lai aktivizācija tādējādi ir atļauta tikai tad, kad neapstiprinātās izmaksas ir pilnībā un precīzi definētas. Var arī papildus ievadīt datumu laukā **No datuma**. Kā vispārīgu norādi izmantojiet datumu, kad tiek plānots iespējot inkrementālos atjauninājumus. Ar izmaksu aprēķināšanu saistīto lauku **No datuma** var atstāt arī tukšu, bet pēc tam katram izmaksu ierakstam ievadiet datumu laukā **No datuma**.
2.  Izmantojiet lapu **Krājuma cena**, lai ievadītu atjauninājumus kā krājumu izmaksu ierakstus, kas ir ietverti otrajā izmaksu aprēķināšanas versijā.
3.  Izmantojiet pārskatu **Krājuma cenas**, lai pārbaudītu otrajā izmaksu aprēķināšanas versijā iekļauto krājuma izmaksu ierakstu aizpildīšanu un precizitāti.
4.  Izmantojiet lapu **Izmaksu aprēķināšanas versijas uzturēšana**, lai mainītu bloķējošo karodziņu un tādējādi atļautu otrajā izmaksu aprēķināšanas versijā iekļauto neapstiprināto izmaksu ierakstu aktivizēšanu.
5.  Izmantojiet lapu **Aktivizēt cenas** (ko var atvērt, izmantojot lapu **Izmaksu aprēķināšanas versijas uzturēšana**), lai atļautu visu otrajā izmaksu aprēķināšanas versijā iekļauto neapstiprināto krājumu izmaksu ierakstu aktivizēšanu. Var aktivizēt arī atsevišķu krājumu neapstiprināto izmaksu ierakstus, lapā **Krājuma cena** noklikšķinot uz pogas **Aktivizēt neapstiprinātās cenas**.
6.  Lai nepieļautu papildu datu uzturēšanu, izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatīšana**, lai mainītu bloķējošos karodziņus, kas ir iekļauti otrajā izmaksu aprēķināšanas versijā. Bloķēšana novērsīs jaunu nenokārtotu izmaksu ievadi un nenokārtoto izmaksu aktivizāciju.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]