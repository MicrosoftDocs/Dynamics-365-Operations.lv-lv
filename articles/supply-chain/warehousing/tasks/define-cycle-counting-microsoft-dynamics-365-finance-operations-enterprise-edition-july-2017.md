---
title: 'Cikla inventarizācijas definēšana '
description: Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e55ccab9205ffa8462d7d40f644e759a34e703d8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146012"
---
# <a name="define-cycle-counting"></a>Cikla inventarizācijas definēšana  

[!include [banner](../../includes/banner.md)]

Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības. Šajā uzdevuma ierakstā parādīts, kā iestatīt noklusēto inventarizācijas darba prioritāti, iespējot mobilās ierīces izvēlnes elementu, lai apstrādātu gan izdošanas un inventarizācijas operācijas, iespējot inventarizācijas robežvērtības trigeri, kad novietojums kļūs tukšs un iespējot cikla inventarizācijas plānu noteiktam krājumam noteiktā noliktavā. Parasti šos uzdevumus veic noliktavas pārvaldnieks. Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.


## <a name="set-the-priority-of-counting-work"></a>Inventarizācijas darba prioritātes iestatīšana
1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana> Noliktavas pārvaldības parametri**.
2. Noklikšķiniet uz cilnes **Cikla inventarizācija**.
3. Ievadiet skaitli laukā **Noklusējuma cikla inventarizācijas darba prioritāte**. Šis solis maina cikla inventarizācijas darba prioritāti salīdzinājumā ar citiem darba veidiem noliktavā. Ievadot skaitli, kas ir mazāks par citu darba veidu skaitu, jūs palielināsiet cikla inventarizācijas darba prioritāti.  
4. Noklikšķiniet uz **Saglabāt**.
5. Aizvērt lapu.

## <a name="enable-the-mobile-device"></a>Mobilās ierīces iespējošana
1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes elementi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību.
4. Laukā **Nosaukums** ievadiet vērtību. 
5. Laukā **Režīms** atlasiet “Darba”.
6. Iestatiet opciju **Izmantot esošo darbu** uz Jā. Iestatot šo opciju uz Jā, sistēma meklēs pašreizējo darbu, ja tiek izmantots mobilās ierīces izvēlnes elements.  
7. Laukā **Noteica:** atlasiet “Sistēmas noteikts”. Ja ir atlasīts "System directed", noliktavas darbinieks tiks novirzīts uz atvērto darbu, kas atrodas definētajās darba klasēs. (Mēs izveidosim šīs darba klases vēlāk.)  
8. Izvērtiet fastTab **Darba klases**. Tagad mēs izveidosim divas darba klases, kas tiks lietotas ar šo mobilās ierīces izvēlnes vienumu. Ja tiek izmantots izvēlnes vienums, šīm darba klasēm būs nepieciešams vaicājums, un lietotājam tiks parādīts darbs ar augstāko prioritāti.  
9. Klikšķiniet **Jauns**.
10. Laukā **Darba klases ID** atlasiet vērtību.
11. Klikšķiniet **Jauns**.
12. Laukā **Darba klases ID** atlasiet vērtību.
13. **Darbību rūtī** noklikšķiniet uz **Saglabāt**.
14. Aizvērt lapu.
15. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.
16. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
17. Kokā atlasiet "the menu item that you just created".
18. Noklikšķiniet uz **Rediģēt**.
19. Noklikšķiniet uz bultiņas, lai šo izvēlnes elementu pievienotu izvēlnei.
20. Noklikšķiniet uz **Saglabāt**.

## <a name="create-a-counting-threshold"></a>Inventarizācijas sliekšņa izveide
1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas sliekšņi**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vērtību laukā **Cikla inventarizācijas sliekšņa ID**.
4. Iestatiet opciju **Nekavējoties apstrādāt cikla inventarizāciju** uz Jā.
5. Laukā **Apraksts** ierakstiet kādu vērtību.
6. Noklikšķiniet uz **Saglabāt**.
7. Noklikšķiniet uz **Atlasīt atrašanās vietas**.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Atlasiet vērtību laukā **Kritēriji**.
10. Noklikšķiniet uz **Labi**.
11. Aizvērt lapu.

## <a name="create-a-cycle-count-plan"></a>Cikla inventarizācijas plāna izveide
1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Noliktavas pārvaldība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vērtību laukā **Cikla inventarizācijas plāna ID**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Ievadiet skaitli laukā **Maksimālais cikla inventarizāciju skaits**.
6. Noklikšķiniet uz **Saglabāt**.
7. Noklikšķiniet uz **Atlasīt atrašanās vietas**.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Atlasiet vērtību laukā **Kritēriji**.
10. Noklikšķiniet uz **Labi**.
11. Ievadiet skaitli laukā **Dienu skaits starp cikla inventarizācijām**. Piemēram, ja lauks **Dienu skaits starp cikla inventarizācijām** ir iestatīts uz 5, cikla inventarizācijas darbs tiks veidots ik pēc piecām dienām. Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts trešajā dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t.i., 8. dienā.  
12. Noklikšķiniet uz **Saglabāt**.
13. Klikšķiniet **Jauns**.
14. Ievadiet skaitli laukā **Secības numurs**. Kārtošana tiek veikta no mazākā skaitļa uz lielāko skaitli. Vērtībai jābūt lielākai par 0 (nulle).  
15. Sarakstā atzīmējiet atlasīto rindu.
16. Laukā **Apraksts** ierakstiet kādu vērtību.
17. Noklikšķiniet uz **Saglabāt**.
18. Noklikšķiniet uz vaicājuma **Definēt preces**.
19. Sarakstā atzīmējiet atlasīto rindu.
20. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.
21. Noklikšķiniet uz **Labi**.
22. Aizvērt lapu.

