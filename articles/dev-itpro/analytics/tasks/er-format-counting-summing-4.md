---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (4. daļa. Formāta palaišana)
description: Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "336202"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a>ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (4. daļa: Palaist formātu)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus. Šīs darbības var veikt uzņēmumā DEMF.

Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras “ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (3. daļa: Izmantot aprēķinus izvades sagatavošanai)” darbības.

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Pārbaudīt šo konfigurāciju attiecībā uz Intrastat pārskatu izveidošanu
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
3. Kokā struktūrā izvērsiet 'Intrastat model'.
4. Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.
5. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.
6. Darbību rūtī noklikšķiniet uz Konfigurācijas.
7. Noklikšķiniet uz Lietotāja parametri.
8. Laukā Palaist iestatījumus atlasiet Jā.
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz Rediģēt.
11. Laukā Palaist melnrakstu atlasiet Jā.
12. Noklikšķiniet uz Saglabāt.
13. Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.
14. Izvērsiet sadaļu Elektroniskie pārskati.
15. Atlasiet konfigurāciju “Intrastat (DE) with counting & summing”.
16. Atlasiet konfigurāciju “Intrastat (DE) with counting & summing”.
17. Noklikšķiniet uz Saglabāt.
18. Aizvērt lapu.
19. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.
20. Noklikšķiniet uz Izvade.
21. Noklikšķiniet uz Atskaite.
    * Izpildiet Intrastat pārskata ģenerēšanas procesu.  
22. Laukā No datuma iestatiet datumu 2000-01-01.
    * Definējiet tāda pārskata perioda sākuma un beigu datumus, kas ietver esošos datumus transakciju veidlapā.  
23. Laukā Līdz datumam iestatiet datumu uz 2022-12-31.
    * Definējiet tāda pārskata perioda sākuma un beigu datumus, kas ietver esošos datumus transakciju veidlapā.  
24. Laukā Virziens atlasiet opciju 'Arrivals'.
25. Laukā Ģenerēt failu atlasiet Jā.
26. Noklikšķiniet uz OK.
    * Pārskatiet izveidoto izvades dokumentu ar kopsavilkuma rindām beigās.  
27. Noklikšķiniet uz Jauns.
28. Sarakstā atzīmējiet atlasīto rindu.
29. Laukā Virziens atlasiet opciju 'Dispatches'.
30. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
31. Laukā Prece ievadiet vai atlasiet kādu vērtību.
32. Iestatiet svara vērtību 10.
33. Iestatiet vienuma Rēķina summa vērtību 10000.
34. Iestatiet vienuma Statistiskā summa vērtību 10000.
35. Noklikšķiniet uz Izvade.
36. Noklikšķiniet uz Atskaite.
37. Laukā Virziens atlasiet opciju 'Dispatches'.
38. Noklikšķiniet uz OK.
    * Pārskatiet izveidoto izvades dokumentu ar kopsavilkuma rindām beigās. Ņemiet vērā, ka tas ir izmainīts, salīdzinot ar pirmo izpildi.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Palaist šo konfigurāciju atkļūdošanas režīmā, lai pārskatītu apkopotos uzskaites & summēšanas datus
1. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
2. Kokā struktūrā izvērsiet 'Intrastat model'.
3. Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.
4. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.
5. Darbību rūtī noklikšķiniet uz Konfigurācijas.
6. Noklikšķiniet uz Lietotāja parametri.
7. Laukā Palaist atkļūdošanas režīmu atlasiet Jā.
8. Noklikšķiniet uz OK.
9. Aizvērt lapu.
10. Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.
11. Noklikšķiniet uz Izvade.
12. Noklikšķiniet uz Atskaite.
13. Noklikšķiniet uz OK.
14. Aizvērt lapu.
15. Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.
16. Kokā struktūrā izvērsiet 'Intrastat model'.
17. Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.
18. Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.
19. Noklikšķiniet uz Atkļūdošanas žurnāli.
    * Ņemiet vērā, ka atlasītās konfigurācijas izpildes procesam ir izveidots atkļūdošanas žurnāla ieraksts.  
20. Noklikšķiniet uz Pievienot.
21. Noklikšķiniet uz Atvērt.
    * Pārskatiet izveidoto XML failu, kas ietver uzskaites un summēšanas datus, kas tika apkopoti atlasītās konfigurācijas izpildes laikā.  

