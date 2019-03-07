---
title: 'Daļēja novietojuma cikla inventarizācijas procesa definēšana '
description: Ja izmantojat cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat nosūtīt faktiskās inventarizācijas operācijas, pieprasot, lai tiktu uzskaitītas tikai noteiktas preces un preču varianti, nevis visi rīcībā esošie krājumi atrašanās vietā.
author: ShylaThompson
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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2019
ms.locfileid: "373410"
---
# <a name="define-partial-location-cycle-counting-process"></a>Daļēja novietojuma cikla inventarizācijas procesa definēšana  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ja izmantojat cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat nosūtīt faktiskās inventarizācijas operācijas, pieprasot, lai tiktu uzskaitītas tikai noteiktas preces un preču varianti, nevis visi rīcībā esošie krājumi atrašanās vietā. Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, palīdzēt izvairīties no konsolidācijas kļūdām un ietaupīt laiku. Parasti noliktavas pārvaldnieks veic iestatījuma uzdevumus. Šo procedūru varat izmēģināt, izmantojot USMF demonstrācijas datu uzņēmumu vai izmantojot savus datus.


## <a name="create-a-cycle-counting-work-template"></a>Cikla inventarizācijas darba veidnes izveide
1. Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.
2. Laukā Darba pasūtījuma veids atlasiet "Cycle counting".
3. Noklikšķiniet uz Jauns.
4. Ievadiet skaitli laukā Secības numurs.
    * Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli. Vērtībai jābūt lielākai par 0 (nulle).  
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā Darba veidne ierakstiet kādu vērtību.
7. Laukā Darba veidnes apraksts ierakstiet kādu vērtību.
8. Laukā Darba kopas ID ievadiet vai atlasiet kādu vērtību.
9. Laukā Darba prioritāte ievadiet numuru.
10. Noklikšķiniet uz Saglabāt.
11. Noklikšķiniet uz Jauns.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Laukā Darba veids atlasiet "Counting".
14. Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.
15. Noklikšķiniet uz Saglabāt.
16. Noklikšķiniet uz Darba rindas pārtraukumi.
17. Noklikšķiniet uz Jauns.
18. Ievadiet skaitli laukā Secības numurs.
    * Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli. Vērtībai jābūt lielākai par 0 (nulle).  
19. Noklikšķiniet uz Saglabāt.
20. Aizvērt lapu.
21. Aizvērt lapu.

## <a name="create-a-cycle-counting-plan"></a>Cikla inventarizācijas plāna izveide
1. Dodieties uz Noliktavas vadība > Iestatīšana > Cikla inventarizācija > Cikla inventarizācijas plāni.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Cikla inventarizācijas plāna ID.
4. Laukā Apraksts ierakstiet kādu vērtību.
5. Laukā Maksimālais cikla inventarizāciju skaits ievadiet skaitli.
6. Laukā Darba veidne, ievadiet vai atlasiet kādu vērtību.
7. Noklikšķiniet uz Jauns.
8. Ievadiet skaitli laukā Secības numurs.
    * Kārtošanas secība ir no mazākā skaitļa uz lielāko skaitli. Vērtībai jābūt lielākai par 0 (nulle).  
9. Apraksta laukā ierakstiet vērtību.
10. Noklikšķiniet uz Saglabāt.
11. Noklikšķiniet uz Definēt preces vaicājumu.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
14. Noklikšķiniet uz OK.
15. Aizvērt lapu.
