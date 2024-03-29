---
title: Mobilās ierīces izvēlnes vienuma iestatīšana, lai reģistrētu saņemtos krājumus
description: Šis raksts fokusējas uz mobilās ierīces izvēlnes vienuma iestatīšanu.
author: Mirzaab
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b59a78ef98215bec7610fe17ed56e6fc287004c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882320"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Mobilās ierīces izvēlnes vienuma iestatīšana, lai reģistrētu saņemtos krājumus

[!include [banner](../../includes/banner.md)]

Šis raksts fokusējas uz mobilās ierīces izvēlnes vienuma iestatīšanu. Šis izvēlnes elements tiek izmantots, lai reģistrētu tādu krājumu ieejas plūsmu, kas pasūtīti, izmantojot pirkšanas pasūtījumus. 

Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF. Šī procedūra ir paredzēta noliktavas pārvaldniekam.


## <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes elementi**.
2. Atlasiet **Jauns**.
3. Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību. Tas ir unikāls identifikators šim mobilās ierīces izvēlnes elementam. Piemēram, jūs varat ierakstīt `My PO registration`.  
4. Laukā **Nosaukums** ievadiet vērtību. Tas ir nosaukums, kas tiks rādīts lietotājam mobilajā ierīcē. Piemēram, jūs varat ierakstīt `PO registration`.  
5. Laukā **Režīms** atlasiet **Darba**. Pirkšanas pasūtījuma rindai saņemto rīcībā esošo daudzumu reģistrēšanas rezultātā tiks izveidots darbs, kas pārvietos krājumus no saņemšanas zonas uz krājumiem. Darbs netiks izveidots, kamēr krājumi nav reģistrēti. Taču opciju **Izmantot esošo darbu** atstājiet iestatītu uz **Nē**.
6. Sadaļas **Vispārīgi** laukā **Darba izveides process** atlasiet **Pirkuma pasūtījuma krājuma saņemšana**.
    - Pirkšanas pasūtījuma rindai jābūt unikāli identificējamai pirms rīcībā esošo var reģistrēt noliktavā. Šajā scenārijā mobilā ierīce reģistrēs pirkšanas pasūtījuma numuru un krājuma kodu, un tas ļaus sistēmai identificēt PP rindu. Tiks izveidots izvietošanas darbs un to var saņemt cits darbinieks. Jūsu izvēlētā darba izveides metode nosaka, kuri lauki kļūst pieejami kopsavilkuma cilnē **Vispārīgi**.  
    - Ja jūs atlasāt opciju **Izmantot noklusējuma datus**, poga **Noklusējuma dati** tiek iespējota. Šeit var atlasīt laukus, lai parādītu datus, kuri darbiniekam parasti ir nepieciešami ikdienas darba veikšanai, lai šīs vērtības tiktu rādītas mobilā ierīcē.  
    - Parametrs **Numura zīmes grupēšana** darbojas kopā ar vienību secības grupu, kas tiek piešķirta saņemtajam krājumam. Varat norādīt, vai ieejas plūsmas, kas ir mazākas par vai lielākas par vienu paleti, ir jāgrupē vienā unikālajā noliktavas vienības identifikatorā vai ir jāsadala pa atsevišķām numura zīmēm katrai vienībai.  
    - Ja atlasāt opciju **Ģenerēt numura zīmi**, tiek ģenerēts unikāls numura zīmes numurs, pamatojoties uz numuru secības atlasi.  
    - Varat atlasīt veidni, kas tiks izmantota, veidojot darbu. Piemēram, ja reģistrējat krājumu pirkšanas pasūtījumam, izvietošanas darbs tiks ģenerēts, pamatojoties uz darba veidni. Ja neatlasāt darba veidni šeit, sistēma piešķirs veidni, pamatojoties uz vaicājuma kritērijiem, kas ir saistīti ar veidnēm.  
    - Ja atgriešanas kodi tiek parādīti mobilajā ierīcē, darbinieki var novērtēt krājumu statusu vai kvalitāti un atlasīt atbilstošu kodu. Atgriešanas koda noteikumi nosaka, vai krājumi būs pieejami citiem noliktavas procesiem. Noteikumi arī nosaka, kura novietojuma direktīva tiek izmantota izveidotajam darbam.   
    - Ja atlasāt opciju **Partijas izvietojuma kodi**, darbinieki var novērtēt partijas statusu vai kvalitāti un izvēlēties atbilstošo izvietojuma kodu. Partijas atgriešanas metodes kodam iestatītie noteikumi nosaka, vai partija būs pieejama citiem noliktavas procesiem.  
    - Ja atlasāt opciju **Drukāt etiķetes**, numura zīmes etiķete tiks automātiski izdrukāta, kad preces tiks saņemtas.  
7. Atlasiet **Saglabāt**.
8. Aizvērt lapu.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Izvēlnes elementa pievienošana mobilās ierīces izvēlnei
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.
2. Lietojiet **Ātro filtru**, lai filtrētu lauku **Nosaukums** ar vērtību `inbound`.
3. Atlasiet **Rediģēt**.
4. Kokā Pieejamās izvēlnes un krājumi atlasiet to izvēlnes krājumu, kuru izveidojāt iepriekš.
5. Atlasiet bultiņu, kas norāda pa labi.
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]