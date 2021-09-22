---
title: Jaukti krājuma veidi, izmantojot sadales centra pārvaldības profilu
description: Lai sadales centra pārvaldības profils efektīvi pārvaldītu krājuma jaukšanu, vispirms ir jāiestata darba galvenes pārtraukums. Šajā lapā paskaidrots, kā to izdarīt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476968"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Krājumu veidi tiek jaukti, izmantojot sadales centra pārvaldības profilu.

## <a name="symptoms"></a>Simptomi

Jūs lietojat *sūtījumu apvienošanas politiku*. Esat iestatījuši *sadales centra pārvaldības profilu* *atrašanās vietas profilam*, taču, kad darbs tiek izveidots, krājumu veidi gala vietā tiek jaukti.

## <a name="resolution"></a>Novēršana

Doka pārvaldības profiliem nepieciešams, lai darbs tiktu sadalīts iepriekš. Citiem vārdiem sakot, doka pārvaldības profils sagaida, ka darba galvenei nebūs vairāku izvietošanas vietu.

Lai doka pārvaldības profils efektīvi pārvaldītu krājumu jaukšanu, ir jāiestata darba galvenes pārtraukums.

Šajā piemērā mūsu sadales centra pārvaldības profils tiek konfigurēts tā, lai **Krājumu veidus nevajadzētu jaukt** ir iestatīta uz *Sūtījuma ID* un mēs tam iestatīsim darba galvenes pārtraukumu:

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Atlasiet rediģējamā **Darba pasūtījuma veidu** (piemēram, *Pirkšanas pasūtījumi*).
1. Atlasiet darba veidni rediģēšanai.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Atveriet cilni **Kārtošana** un pievienojiet rindu ar šādiem iestatījumiem:
    - **Tabula** - *Pagaidu darba darbības*
    - **Atveidotā tabula** - *Pagaidu darba darbības*
    - **Lauks** - *Sūtījuma ID*
1. Atlasiet **Labi**.
1. Jūs atgriežaties lapā **Darbu veidnes**. Darbību rūtī atlasiet **Darba galvenes pārtraukumi**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Atzīmējiet izvēles rūtiņu, kas saistīta ar **lauka nosaukuma** *sūtījuma ID*.
1. Darbību rūtī atlasiet **Saglabāt**.
