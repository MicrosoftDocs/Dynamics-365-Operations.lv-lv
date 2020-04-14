---
title: Krājumu saņemšanas pārskata profila iestatīšana
description: Šī tēma koncentrējas uz ierašanās pārskata profila iestatīšanu.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55512c75445a5f3b9c1521376a20d48dd60e22c6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145529"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Krājumu saņemšanas pārskata profila iestatīšana

[!include [banner](../../includes/banner.md)]]

Šī tēma koncentrējas uz ierašanās pārskata profila iestatīšanu. Saņemšanas pārskata profils ir noteikumu kopums, kas tiks izmantots, kad lietotājs atver saņemšanas pārskata lapu. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Šo procedūru parasti veic saņemšanas darbinieks.

1. Navigācijas rūtī ejiet uz **Moduļi > Krājumu pārvaldība > Iestatīšana> Izplatīšana > Ierašanās pārskata profili**.
2. Atlasiet **Jauns**. Tā kā būs gandrīz vienmēr jāstrādā vienā noliktavā, izkraujot kravas no pilnām kravas automašīnām, jums vajadzētu izveidot saņemšanas pārskata profilu, lai vienkāršotu saņemto krājumu reģistrācijas procesu.  
3. Laukā **Ierašanās pārskata profili** ievadiet vērtību.
4. Laukā **Rādīt rindas** atlasiet opciju. Atlasiet, kuras rindas parādīt kvītīs.  

    - **Visas** — rādīt visas rindas neatkarīgi no statusa.   
    - **Apstrādē** — rādīt kvītīs tās rindas, kuru progress ir Pabeigts vai Daļēji pabeigts. Tas nozīmē, ka saņemšanas žurnālā katrai rindai tika reģistrēts pilns daudzums vai daļējais daudzums.   
    - **Nepabeigts** — rādīt kvītīs tās rindas, kuru progress ir Nav vai Daļēji pabeigts. Tas nozīmē, ka saņemšanas žurnālā katrai rindai daudzums netiek reģistrēts vispār vai tikai daļēji.  

5. Izvērsiet vai sakļaujiet sadaļu **Ierašanās opcijas**.
6. Laukā **Dienas uz priekšu** ierakstiet vērtību. Ar šo tiek iestatīts filtrs, lai parādītu saņemšanas rindas, ko paredzams saņemt tuvāko dienu laikā (atkarībā no iestatītā numura).  
7. Laukā **Dienas atpakaļ** ierakstiet vērtību. Ar šo tiek iestatīts filtrs, lai parādītu saņemšanas rindas, ko bija paredzēts saņemt vairākas dienas pirms šodienas datuma.  
8. Laukā **Noliktavas** atlasiet vērtību. Filtrējiet pēc vienas vai vairākām noliktavām.  
9. Atlasiet vērtību laukā **Piegādes režīms**. Šādi filtrs tiek iestatīts tā, lai parādītu tikai ieejas plūsmas rindas ar šo piegādes veidu.  
10. Laukā **Nosaukums** atlasiet WHS.
11. Laukā **Noliktava** atkasiet 24. noliktavu. Tā ir noklusētā noliktava, kas tiks izmantota reģistrētām ieejas plūsmas rindām, kas lieto šo profilu.  
12. Laukā **Atrašanās vieta** atlasiet **Aizmugurējās durvis**. Tas ir noklusētais novietojums, kas tiks izmantots reģistrētām ieejas plūsmas rindām, kas lieto šo profilu.  
13. Izvērsiet vai sakļaujiet sadaļu **Ierašanās vaicājuma informācija**.
14. Laukā **Ierobežot vietā** atkasiet 2. vietu. Šādi filtrs tiek iestatīts tā, lai parādītu tikai ieejas plūsmas rindas ar šo novietojumu.  
15. Opciju **Pirkuma pasūtījumi** iestatiet uz **Jā**. Atlasiet ieejas plūsmas rindas no pirkšanas pasūtījumiem.  
16. Opciju **Pārsūtīšanas pasūtījumi** iestatiet uz **Jā**. Atlasiet ieejas plūsmas rindas no pārsūtīšanas pasūtījumiem.  
17. Atlasiet **Saglabāt**.
18. Aizvērt lapu.

