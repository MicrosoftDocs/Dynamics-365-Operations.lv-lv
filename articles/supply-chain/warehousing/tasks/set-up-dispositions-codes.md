---
title: Izvietojuma kodu iestatīšana
description: Šī procedūra fokusējas uz atgriešanas metodes koda iestatīšanu, ko var izmantot mobilā ierīcē atgriezto pasūtījumu saņemšanas procesam.
author: Mirzaab
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb83108c934e864da0df39ec4ee36a0bc7ba7588
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574069"
---
# <a name="set-up-dispositions-codes"></a>Izvietojuma kodu iestatīšana

[!include [banner](../../includes/banner.md)]

Šī procedūra fokusējas uz atgriešanas metodes koda iestatīšanu, ko var izmantot mobilā ierīcē atgriezto pasūtījumu saņemšanas procesam. Atgriešanas metodes kodi ir noteikumu kopums, kas tiek izmantots, kad tiek saņemti krājumi. Piemēram, kad darba lietotājs izmanto mobilo ierīci, lai saņemtu krājumus, kas tika bojāti, lietotājam jānoskenē bojāto krājumu atgriešanas metodes kods. Saņemto preču krājumu statusu, darba veidni un novietojuma direktīvu var noteikt pēc skenēta atgriešanas metodes koda. Pirkšanas pasūtījuma saņemšanas procesam un ražošanas pasūtījuma pārskatam kā pabeigtam procesam atgriešanas metodes koda izmantošana nav obligāta. Pārdošanas pasūtījuma atgriešanas saņemšanas procesam, ja krājumi ir reģistrēti, izmantojot mobilo ierīci, atgriešanas metodes koda izmantošana ir obligāta.  Šajā ceļvedī tiek izmantoti demonstrācijas uzņēmuma USMF dati. Šī procedūra ir paredzēta noliktavas pārvaldniekam. 

1. Pārejiet uz sadaļu Noliktavas pārvaldība > Iestatījumi > Mobilā ierīce > Izvietojuma kodi.
2. Noklikšķiniet uz Jauns.
    * Izveidojiet jaunu atgriešanas metodes kodu, lai izmantotu debitora atgrieztajiem krājumiem.  
3. Laukā Atgriešanas metodes kods ierakstiet vērtību.
4. Laukā Krājumu statuss atlasiet krājumu statusu, kur pastāv krājuma bloķēšana.
    * Ja jūs izmantojat USMF, atlasiet "Bloķēšana". Jūs varat pievienot krājumu statusu atgriešanas metodes kodam, lai ignorētu noklusējuma statusu, kas ir pasūtījuma rindās.  
5. Laukā Darba veidne ierakstiet kādu vērtību.
    * Nav obligāti: atlasiet darba veidnes kodu, kas ir saistīts ar atgriešanas pasūtījumu. Ja vērtības nav, darba veidne tiks atrisināta, izmantojot standarta noteikumus, kas konfigurēti jūsu sistēmā. Darba veidnes izvēle ierobežos procesus, ar kuriem var izmantot šo atgriešanas metodes kodu. Piemēram, ja atgriešanas metodes kodam ir darba veidne ar darba pasūtījumu ar tipu pirkšanas pasūtījums, to nevar izmantot, lai reģistrētu krājumus, ko atgriež debitori.  
6. Laukā Atgriešanas metodes kods ierakstiet vērtību.
    * Atgriešanas metodes kods nosaka atlikušo atgriešanas pasūtījuma procesu reģistrētiem krājumiem. Šajā piemērā klientam jāsaņem kredīta notu. Pievienojiet atgriešanas metodes kodu, kuras satur darbību Kredīts.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]