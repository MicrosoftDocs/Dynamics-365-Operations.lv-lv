--- 
title: "Mobilās ierīces izvēlnes vienuma iestatīšana, lai reģistrētu saņemtos krājumus"
description: "Šis uzdevums koncentrējas uz mobilās ierīces izvēlnes elementa iestatīšanu."
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
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 642e2b05c9f9a59f6b47a22f3d92f2f6ae245039
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Mobilās ierīces izvēlnes vienuma iestatīšana, lai reģistrētu saņemtos krājumus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevums koncentrējas uz mobilās ierīces izvēlnes elementa iestatīšanu. Šis izvēlnes elements tiek izmantots, lai reģistrētu tādu krājumu ieejas plūsmu, kas pasūtīti, izmantojot pirkšanas pasūtījumus. 

Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF. Šī procedūra ir paredzēta noliktavas pārvaldniekam.


## <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide
1. Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.
    * Tas ir unikāls identifikators šim mobilās ierīces izvēlnes elementam. Piemēram, varat ierakstīt "Manu PP reģistrācija".  
4. Laukā Virsraksts ierakstiet kādu vērtību.
    * Tas ir nosaukums, kas tiks rādīts lietotājam mobilajā ierīcē. Piemēram, varat ierakstīt "PP reģistrācija".  
5. Laukā Režīms atlasiet "Darbs".
    * Pirkšanas pasūtījuma rindai saņemto rīcībā esošo daudzumu reģistrēšanas rezultātā tiks izveidots darbs, kas pārvietos krājumus no saņemšanas zonas uz krājumiem. Darbs netiks izveidots, kamēr krājumi nav reģistrēti.  Tāpēc atstājiet opcijai Izmantot esošo darbu vērtību Nē.  
6. Izvērsiet vai sakļaujiet sadaļu Vispārīgi.
7. Laukā Darba izveides process atlasiet "Pirkšanas pasūtījuma krājuma saņemšana".
    * Pirkšanas pasūtījuma rindai jābūt unikāli identificējamai pirms rīcībā esošo var reģistrēt noliktavā. Šajā scenārijā mobilā ierīce reģistrēs pirkšanas pasūtījuma numuru un krājuma kodu, un tas ļaus sistēmai identificēt PP rindu. Tiks izveidots izvietošanas darbs un to var saņemt cits darbinieks.    Atlasītā darba veidošanas metode nosaka, kuri lauki kļūst pieejami kopsavilkuma cilnē Vispārīgi.  
    * Ja atlasāt opciju Lietot noklusējuma datus, tiek aktivizēta poga Noklusējuma dati. Šeit var atlasīt laukus, lai parādītu datus, kuri darbiniekam parasti ir nepieciešami ikdienas darba veikšanai, lai šīs vērtības tiktu rādītas mobilā ierīcē.  
    * Numura zīmju grupēšanas parametrs darbojas kopā ar vienības secību grupu, kas ir piešķirta saņemtajam krājumam. Varat norādīt, vai ieejas plūsmas, kas ir mazākas par vai lielākas par vienu paleti, ir jāgrupē vienā unikālajā noliktavas vienības identifikatorā vai ir jāsadala pa atsevišķām numura zīmēm katrai vienībai.  
    * Atlasot opciju Ģenerēt numura zīmi, tiek ģenerēts unikāls numura zīmes numurs, pamatojoties uz numuru sērijas atlasi.   
    * Varat atlasīt veidni, kas tiks izmantota, veidojot darbu. Piemēram, ja reģistrējat krājumu pirkšanas pasūtījumam, izvietošanas darbs tiks ģenerēts, pamatojoties uz darba veidni. Ja neatlasāt darba veidni šeit, sistēma piešķirs veidni, pamatojoties uz vaicājuma kritērijiem, kas ir saistīti ar veidnēm.  
    * Ja atgriešanas kodi tiek parādīti mobilajā ierīcē, darbinieki var novērtēt krājumu statusu vai kvalitāti un atlasīt atbilstošu kodu. Atgriešanas koda noteikumi nosaka, vai krājumi būs pieejami citiem noliktavas procesiem. Noteikumi arī nosaka, kura novietojuma direktīva tiek izmantota izveidotajam darbam.   
    * Ja atlasāt opciju Partijas atgriešanas metodes kodi, darbinieki var novērtēt partijas statusu vai kvalitāti un atlasīt atbilstošu atgriešanas kodu.  Partijas atgriešanas metodes kodam iestatītie noteikumi nosaka, vai partija būs pieejama citiem noliktavas procesiem.  
    * Ja atlasāt opciju Drukāt etiķetes numura zīmes uzlīme tiks izdrukāta automātiski, kad krājumi tiks saņemti.  
8. Noklikšķiniet uz Saglabāt.
9. Aizvērt lapu.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Izvēlnes elementa pievienošana mobilās ierīces izvēlnei
1. Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka Nosaukums ar vērtību “ienākošais”.
3. Noklikšķiniet uz Rediģēt.
4. Kokā atlasiet “Pieejamo izvēļņu un krājumu kokā atlasiet iepriekš izveidoto izvēlnes elementu”.
    * Atlasiet iepriekš izveidoto izvēlnes elementu.  
5. Noklikšķiniet uz bultiņas, kas rāda pa labi.
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.

