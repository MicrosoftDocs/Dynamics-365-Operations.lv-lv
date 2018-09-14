--- 
title: "Min.-maks. papildināšanas procesa iestatīšana"
description: "Šī procedūra parāda, kā iestatīt papildināšanas procesu, kas izmanto minimuma/maksimuma papildināšanas stratēģiju."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>Min.-maks. papildināšanas procesa iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra parāda, kā iestatīt papildināšanas procesu, kas izmanto minimuma/maksimuma papildināšanas stratēģiju. Ja krājumu daudzums ir zem minimālā līmeņa, tiks izveidots uzdevums atrašanās vietas papildināšanai. Procedūra parāda arī kā lietot fiksētas izdošanas vietas, lai ļautu atjaunot krājumus pat tad, ja krājumu daudzums ir mazāks par minimālo līmeni, un to, kā iespējot papildināšanas procesa regulāru palaišanu, izmantojot pakešuzdevumu. Šos uzdevumus parasti veic noliktavas pārvaldnieks. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības piezīmēs, vai to var palaist, izmantojot savus datus. Ja jūs izmantojat savus datus, pārliecinieties, ka jums ir noliktava, kas ir iespējota noliktavas vadības procesiem.


## <a name="create-a-fixed-picking-location"></a>Izveidojiet fiksētu izdošanas vietu
1. Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Fiksētie novietojumi.
    * Tas ir papildu uzdevums min.-maks. papildināšanai, bet ja jūs izmantojat fiksētu izdošanas vietu, tas ļauj krājuma papildināšanu pat, ja tas sarūk zem minimālā līmeņa, jo sistēma var noteikt, kurus krājumus nepieciešams papildināt, pat tad, ja tie ir beigušies.  
2. Noklikšķiniet uz Jauns.
3. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat atlasīt krājumu A0001.  
4. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat atlasīt "Vieta 2".  
5. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat krājumu USMF, varat atlasīt 24. noliktavu.  
6. Laukā Atrašanās vieta, ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat atlasīt CP-003.  
7. Aizvērt lapu.

## <a name="create-a-replenishment-location-directive"></a>Izveidojiet papildināšanas vietas direktīvu
1. Dodieties uz Noliktavas vadība > Iestatīšana > Novietojuma direktīvas.
    * Atrašanās vietas direktīvas tiek izmantotas, lai noteiktu, kur vienības jāizdod papildināšanas procesā.  
2. Laukā Darba pasūtījuma tips atlasiet 'Papildināšana'.
3. Noklikšķiniet uz Jauns.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Darba tips atlasiet vienumu “Izdošana”.
6. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat atlasīt "Vieta 2".  
7. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat krājumu USMF, varat atlasīt 24. noliktavu.  
8. Noklikšķiniet uz Saglabāt.
9. Noklikšķiniet uz Jauns.
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā Līdz daudzumam ierakstiet kādu skaitli.
    * Piemēram, jūs varat iestatīt to uz 9999.  
12. Atzīmējiet izvēles rūtiņu Atļaut sadali.
    * Ja atlasāt šo opciju, darba izveides process ļaus darbu rindas daudzumiem tikt sadalītiem vairākās vietās.  
13. Noklikšķiniet uz Saglabāt.
14. Noklikšķiniet uz Jauns.
15. Sarakstā atzīmējiet atlasīto rindu.
16. Laukā Nosaukums ierakstiet kādu vērtību.
17. Noklikšķiniet uz Saglabāt.
18. Noklikšķiniet uz Rediģēt vaicājumu.
    * Jūs varat rediģēt šo vaicājumu, lai pievienotu ierobežojumus, kur krājumu var atlasīt papildināšanas procesā. Piemēram, var gadīties, ka krājumu var izmantot tikai no lielapjoma zonas noliktavā.  
19. Noklikšķiniet uz OK.
20. Aizvērt lapu.

## <a name="create-a-replenishment-work-template"></a>Izveidojiet papildināšanas darba veidni.
1. Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.
    * Darba veidne tiek izmantota, lai norādītu sistēmai, kā ir jāveido min. /maks. papildināšanas darbs. Vismaz jābūt darba veidnes rindai izdošanai un izvietošanai. Darba veidne paziņos, ka tā ir nederīga līdz brīdim, kad ir ievadīta visa nepieciešamā informācija.  
2. Laukā Darba pasūtījuma tips atlasiet 'Papildināšana'.
3. Noklikšķiniet uz Jauns.
4. Laukā Darba veidne ierakstiet kādu vērtību.
5. Noklikšķiniet uz Saglabāt.
6. Noklikšķiniet uz Jauns.
7. Laukā Darba tips atlasiet vienumu “Izdošana”.
8. Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.
    * Tā būtu darba klase, kas ir saistīta ar papildināšanu. Ja jūs izmantojat USMF, atlasiet Papildināt.  
9. Noklikšķiniet uz Jauns.
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā Darba tips atlasiet vienumu “Izvietošana”.
12. Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.
13. Noklikšķiniet uz Saglabāt.
14. Aizvērt lapu.

## <a name="create-a-new-replenishment-template"></a>Izveidojiet jaunu papildināšanas veidni
1. Dodieties uz Noliktavas vadība > Iestatīšana > Papildināšana > Papildināšanas veidnes.
    * Papildināšanas veidne tiek izmantota, lai definētu krājumus un daudzumus un atrašanās vietu papildināšanai.  
2. Noklikšķiniet uz Jauns.
3. Laukā Papildināšanas veidne, ierakstiet vērtību.
    * Piešķiriet veidnei nosaukumu, lai norādītu, ka tā ir min. /maks. papildināšanai.  
4. Apraksta laukā ierakstiet vērtību.
5. Atlasiet izvēles rūtiņu Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus.
    * Ja atlasāt šo opciju, tā nodrošina kopuma pieprasījuma papildināšanu, lai patērētu daudzumus, kas ir saistīti ar min. /maks. papildināšanu. Piemēram, tas varētu būt noderīgi, ja min. /maks. papildināšanas darbs netiek uzreiz apstrādāts, lai izvairītos no nevajadzīgas pieprasījuma papildināšanas darba izveides.  
6. Noklikšķiniet uz Jauns.
7. Ievadiet skaitli laukā Secības numurs.
8. Apraksta laukā ierakstiet vērtību.
9. Sarakstā atzīmējiet atlasīto rindu.
10. Laukā Papildināšanas vienība, ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet gab. Šis iestatījums ir obligāts. Tas ļauj norādīt citu mērvienību papildināšanas darbam, salīdzinājumā ar vienību, kas ir norādīta minimālā un maksimālā krājumu līmeņiem šajā veidnē.  
11. Laukā Darba veidne, ievadiet vai atlasiet kādu vērtību.
    * Atrodiet iepriekš izveidoto darba veidni.  
12. Laukā Minimālais daudzums, ievadiet skaitli.
    * Atlasiet minimālo daudzumu, kam vajadzētu aktivizēt papildināšanu. Piemēram, iestatiet to uz 50. Ir iespējams atstāt šo iestatījumu uz nulli, ja papildināt fiksētu atrašanās vietu, un opcija Papildināt tukšas fiksētas atrašanās vietas ir iestatīta uz Jā. Ieteicams arī atlasīt opciju Papildināt tikai fiksētas atrašanās vietas, lai uzlabotu veiktspēju.  
13. Laukā Maksimālais daudzums, ievadiet skaitli.
    * Piemēram, iestatiet to uz 100.  
14. Laukā Vienība ievadiet vai atlasiet kādu vērtību.
    * Piešķiriet vienību minimālajam un maksimālajam daudzumam. Piemēram, iestatiet to uz gab.  
15. Atzīmējiet izvēles rūtiņu Papildināt tukšas fiksētas atrašanās vietas.
    * Atzīmējiet šo izvēles rūtiņu, lai papildinātu fiksētas atrašanās vietas, kad tās ir tukšas. Pretējā gadījumā tiek papildināti tikai tie novietojumi, kur pastāv rīcībā esošs daudzums.  
16. Atzīmējiet izvēles rūtiņu Papildināt tikai tukšas fiksētas atrašanās vietas.
17. Noklikšķiniet uz Atlasīt preces.
    * Šī ir vieta, lai definētu, kuri produkti ir jāpapildina. Ja ir atlasīta opcija Fiksētas izdošanas vietas, jums nepieciešams arī noteikt atrašanās vietas šajā vaicājumā. Ir pieejami variantam specifiski, kā arī precei specifiski vaicājumi.  
18. Atlasiet Krājumu rindu.
19. Laukā Kritēriji ierakstiet kādu vērtību.
    * Atlasiet krājumus, kas ir jāpapildina fiksētās atrašanās vietās. Piemēram, ierakstiet A*, lai atlasītu visus krājuma numurus, kas sākas ar A.  
20. Noklikšķiniet uz Pievienot.
    * Pievienojiet atrašanās vietas entītiju (ja vien tā jau pastāv), lai varētu ierobežot papildināšanas darbu fiksētām izdošanas vietām noteiktā noliktavas apgabalā.  
21. Sarakstā atzīmējiet atlasīto rindu.
22. Iestatiet lauku Tabula uz Atrašanās vietas.
23. Laukā Lauks, atlasiet Atrašanās vietas profila ID.
24. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
25. Noklikšķiniet uz OK.
26. Aizvērt lapu.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Iestatiet papildināšanas procesu, lai to varētu palaist kā pakešuzdevumu.
1. Dodieties uz Noliktavas vadība > Papildināšana > Papildināšanas.
    * Papildināšanas lapa ļauj jums iestatīt papildināšanas palaišanu kā pakešuzdevumu, vai pieprasīt tās palaišanu manuāli.  
2. Noklikšķiniet uz Filtrēt.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
5. Noklikšķiniet uz Labi.
6. Izvērsiet sadaļu Palaist fonā.
7. Iestatiet Pakešapstrādes opciju uz Jā.
8. Noklikšķiniet uz Periodiskums.
9. Atlasiet opciju Bez beigu datuma.
10. Iestatiet Atkārtošanās shēmu.
    * Piemēram: atlasiet Dienas.  
11. Noklikšķiniet uz OK.
12. Noklikšķiniet uz OK.


