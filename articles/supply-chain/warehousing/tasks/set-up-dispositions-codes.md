--- 
title: "Izvietojuma kodu iestatīšana"
description: "Šī procedūra fokusējas uz atgriešanas metodes koda iestatīšanu, ko var izmantot mobilā ierīcē atgriezto pasūtījumu saņemšanas procesam."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c004543188656dfd53d7539717cd6e93d0b9f47a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-dispositions-codes"></a>Izvietojuma kodu iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


