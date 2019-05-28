---
title: 'Cikla inventarizācijas definēšana '
description: Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
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
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571691"
---
# <a name="define-cycle-counting"></a>Cikla inventarizācijas definēšana  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības. Šajā uzdevuma ierakstā parādīts, kā iestatīt noklusēto inventarizācijas darba prioritāti, iespējot mobilās ierīces izvēlnes elementu, lai apstrādātu gan izdošanas un inventarizācijas operācijas, iespējot inventarizācijas robežvērtības trigeri, kad novietojums kļūs tukšs un iespējot cikla inventarizācijas plānu noteiktam krājumam noteiktā noliktavā. Parasti šos uzdevumus veic noliktavas pārvaldnieks. Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.


## <a name="set-the-priority-of-counting-work"></a>Inventarizācijas darba prioritātes iestatīšana
1. Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Cikla inventarizācija.
3. Laukā Cikla inventarizācijas noklusējuma darba prioritāte ievadiet skaitli.
    * Šis solis maina cikla inventarizācijas darba prioritāti salīdzinājumā ar citiem darba veidiem noliktavā. Ievadot skaitli, kas ir mazāks par citu darba veidu skaitu, jūs palielināsiet cikla inventarizācijas darba prioritāti.  
4. Noklikšķiniet uz Saglabāt.
5. Aizvērt lapu.

## <a name="enable-the-mobile-device"></a>Mobilās ierīces iespējošana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.
4. Laukā Virsraksts ierakstiet kādu vērtību.
5. Laukā Režīms atlasiet "Darbs".
6. Iestatiet opciju Izmantot esošo darbu uz Jā.
    * Iestatot šo opciju uz Jā, sistēma meklēs pašreizējo darbu, ja tiek izmantots mobilās ierīces izvēlnes elements.  
7. Laukā Novirzītājs atlasiet vienumu "Sistēmas noteikts".
    * Ja ir atlasīts "System directed", noliktavas darbinieks tiks novirzīts uz atvērto darbu, kas atrodas definētajās darba klasēs. (Mēs izveidosim šīs darba klases vēlāk.)  
8. Izvērsiet vai sakļaujiet sadaļu Darba klases.
    * Tagad mēs izveidosim divas darba klases, kas tiks lietotas ar šo mobilās ierīces izvēlnes vienumu. Ja tiek izmantots izvēlnes vienums, šīm darba klasēm būs nepieciešams vaicājums, un lietotājam tiks parādīts darbs ar augstāko prioritāti.  
9. Noklikšķiniet uz Jauns.
10. Laukā Darba klases ID ierakstiet kādu vērtību.
11. Noklikšķiniet uz Jauns.
12. Laukā Darba klases ID ierakstiet kādu vērtību.
13. Noklikšķiniet uz Saglabāt.
14. Aizvērt lapu.
15. Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.
16. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
17. Kokā atlasiet "the menu item that you just created".
18. Noklikšķiniet uz Rediģēt.
19. Noklikšķiniet uz bultiņas, lai šo izvēlnes elementu pievienotu izvēlnei.
20. Noklikšķiniet uz Saglabāt.

## <a name="create-a-counting-threshold"></a>Inventarizācijas sliekšņa izveide
1. Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas robežvērtības.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Cikla inventarizācijas sliekšņa ID.
4. Iestatiet opciju Nekavējoties apstrādāt cikla inventarizāciju uz Jā.
5. Apraksta laukā ierakstiet vērtību.
6. Klikšķiniet Saglabāt.
7. Noklikšķiniet uz Atlasīt novietojumus.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Laukā Kritēriji atlasiet vērtību.
10. Noklikšķiniet uz OK.
11. Aizvērt lapu.

## <a name="create-a-cycle-count-plan"></a>Cikla inventarizācijas plāna izveide
1. Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Cikla inventarizācijas plāna ID.
4. Laukā Apraksts ierakstiet kādu vērtību.
5. Laukā Maksimālais cikla inventarizāciju skaits ievadiet skaitli.
6. Klikšķiniet Saglabāt.
7. Noklikšķiniet uz Atlasīt novietojumus.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Laukā Kritēriji atlasiet vērtību.
10. Noklikšķiniet uz OK.
11. Laukā Dienu skaits starp cikla inventarizācijām ievadiet skaitli.
    * Piemēram, ja laukā Dienu skaits starp cikla inventarizācijām iestatītā vērtība ir 5, cikla inventarizācijas darbs tiks izveidots ik pēc piecām dienām. Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts trešajā dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t.i., 8. dienā.  
12. Noklikšķiniet uz Saglabāt.
13. Noklikšķiniet uz Jauns.
14. Ievadiet skaitli laukā Secības numurs.
    * Kārtošana tiek veikta no mazākā skaitļa uz lielāko skaitli. Vērtībai jābūt lielākai par 0 (nulle).  
15. Sarakstā atzīmējiet atlasīto rindu.
16. Apraksta laukā ierakstiet vērtību.
17. Klikšķiniet Saglabāt.
18. Noklikšķiniet uz Definēt preces vaicājumu.
19. Sarakstā atzīmējiet atlasīto rindu.
20. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
21. Noklikšķiniet uz OK.
22. Aizvērt lapu.

