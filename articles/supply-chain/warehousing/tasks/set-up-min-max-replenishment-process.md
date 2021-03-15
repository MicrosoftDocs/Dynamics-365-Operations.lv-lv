---
title: Min.-maks. papildināšanas procesa iestatīšana
description: Šī procedūra parāda, kā iestatīt papildināšanas procesu, kas izmanto minimuma/maksimuma papildināšanas stratēģiju.
author: perlynne
manager: tfehr
ms.date: 10/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, InventItemIdLookupSimple, WMSLocationIdLookup, WHSLocDirTable, InventLocationIdLookup, SysQueryForm, WHSWorkTemplateTable, WHSReplenishmentTemplates, UnitOfMeasureLookup, SysQueryTableLookUp, SysQueryFieldLookUp, SysRecurrence, WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e14614829f414bc9063b84ec848816e77dbd571a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976942"
---
# <a name="set-up-a-min-max-replenishment-process"></a>Min.-maks. papildināšanas procesa iestatīšana

[!include [banner](../../includes/banner.md)]

Šī procedūra parāda, kā iestatīt papildināšanas procesu, kas izmanto minimuma/maksimuma papildināšanas stratēģiju. Ja krājumu daudzums ir zem minimālā līmeņa, tiks izveidots uzdevums atrašanās vietas papildināšanai. Procedūra parāda arī kā lietot fiksētas izdošanas vietas, lai ļautu atjaunot krājumus pat tad, ja krājumu daudzums ir mazāks par minimālo līmeni, un to, kā iespējot papildināšanas procesa regulāru palaišanu, izmantojot pakešuzdevumu. Šos uzdevumus parasti veic noliktavas pārvaldnieks. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības zemāk, vai to var palaist, izmantojot savus datus. Ja jūs izmantojat savus datus, pārliecinieties, ka jums ir noliktava, kas ir iespējota noliktavas vadības procesiem.


## <a name="create-a-fixed-picking-location"></a>Izveidojiet fiksētu izdošanas vietu
1. Dodieties uz **Navigācijas rūti > Moduļi > Noliktavas pārvaldība > Iestatīšana > Noliktava > Fiksētās atrašanās vietas**. Tas ir papildu uzdevums min.-maks. papildināšanai, bet ja jūs izmantojat fiksētu izdošanas vietu, tas ļauj krājuma papildināšanu pat, ja tas sarūk zem minimālā līmeņa, jo sistēma var noteikt, kurus krājumus nepieciešams papildināt, pat tad, ja tie ir beigušies.
2. Klikšķiniet **Jauns**.
3. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt krājumu A0001.  
4. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt "Vieta 2".  
5. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību. Ja izmantojat krājumu USMF, varat atlasīt 24. noliktavu.  
6. Laukā **Atrašanās vieta** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt CP-003.  
7. Aizvērt lapu.

## <a name="create-a-replenishment-location-directive"></a>Izveidojiet papildināšanas vietas direktīvu
1. Dodieties uz **Noliktavas vadība > Iestatīšana > Novietojuma direktīvas**. Atrašanās vietas direktīvas tiek izmantotas, lai noteiktu, kur vienības jāizdod papildināšanas procesā.
2. Laukā **Darba pasūtījuma veids** atlasiet “Papildināšana“.
3. **Sadaļā Darbību rūts** noklikšķiniet uz **Jauns**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Darba veids** atlasiet vienumu “Izdošana”.
6. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt "Vieta 2".  
7. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību. Ja izmantojat krājumu USMF, varat atlasīt 24. noliktavu.  
8. Noklikšķiniet uz **Saglabāt**.
9. Sadaļā **Rindas** noklikšķiniet uz **Jauns**.
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā **Līdz daudzumam** ievadiet skaitu. Piemēram, jūs varat iestatīt to uz 9999.  
12. Atzīmējiet izvēles rūtiņu **Atļaut sadali**. Ja atlasāt šo opciju, darba izveides process ļaus darbu rindas daudzumiem tikt sadalītiem vairākās vietās.  
13. Noklikšķiniet uz **Saglabāt**.
14. Sadaļā **Atrašanās vietas direktīvas darbības** noklikšķiniet uz **Jauns**.
15. Sarakstā atzīmējiet atlasīto rindu.
16. Laukā **Nosaukums** ierakstiet kādu vērtību.
17. Noklikšķiniet uz **Saglabāt**.
18. **Darbību rūtī** noklikšķiniet uz **Rediģēt vaicājumu**. Jūs varat rediģēt šo vaicājumu, lai pievienotu ierobežojumus, kur krājumu var atlasīt papildināšanas procesā. Piemēram, var gadīties, ka krājumu var izmantot tikai no lielapjoma zonas noliktavā.
19. Noklikšķiniet uz **Labi**.
20. Aizvērt lapu.

## <a name="create-a-replenishment-work-template"></a>Izveidojiet papildināšanas darba veidni.
1. Doties uz **Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes**. Darba veidne tiek izmantota, lai norādītu sistēmai, kā ir jāveido min. /maks. papildināšanas darbs. Vismaz jābūt darba veidnes rindai izdošanai un izvietošanai. Darba veidne paziņos, ka tā ir nederīga līdz brīdim, kad ir ievadīta visa nepieciešamā informācija. 
2. Laukā **Darba pasūtījuma veids** atlasiet “Papildināšana“.
3. **Sadaļā Darbību rūts** noklikšķiniet uz **Jauns**.
4. Laukā **Darba veidne** ierakstiet kādu vērtību.
5. Noklikšķiniet uz **Saglabāt**.
6. Sadaļā **Darba veidnes detalizētas informācija** noklikšķiniet uz **Jauns**.
7. Laukā **Darba veids** atlasiet vienumu “Izdošana”.
8. Laukā **Darba klases ID** ievadiet vai atlasiet vērtību. Tā būtu darba klase, kas ir saistīta ar papildināšanu. Ja jūs izmantojat USMF, atlasiet Papildināt.  
9. Sadaļā **Darba veidnes detalizētas informācija** noklikšķiniet uz **Jauns**.
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā **Darba veids** atlasiet “Ievietot”.
12. Laukā **Darba klases ID** ievadiet vai atlasiet vērtību.
13. Noklikšķiniet uz **Saglabāt**.
14. Aizvērt lapu.

## <a name="create-a-new-replenishment-template"></a>Izveidojiet jaunu papildināšanas veidni
1. Dodieties uz **Noliktavas vadība > Iestatīšana > Iestatīšana > Papildināšanas veidnes**. Papildināšanas veidne tiek izmantota, lai definētu krājumus un daudzumus un atrašanās vietu papildināšanai.
2. **Sadaļā Darbību rūts** noklikšķiniet uz **Jauns**.
3. Laukā **Papildināšanas veidne** ierakstiet vērtību. Piešķiriet veidnei nosaukumu, lai norādītu, ka tā ir min. /maks. papildināšanai.  
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Atlasiet izvēles rūtiņu **Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus**. Ja atlasāt šo opciju, tā nodrošina kopuma pieprasījuma papildināšanu, lai patērētu daudzumus, kas ir saistīti ar min. /maks. papildināšanu. Piemēram, tas varētu būt noderīgi, ja min. /maks. papildināšanas darbs netiek uzreiz apstrādāts, lai izvairītos no nevajadzīgas pieprasījuma papildināšanas darba izveides.
6. Sadaļā **Papildināšanas veidnes detalizētas informācija** noklikšķiniet uz **Jauns**.
7. Ievadiet skaitli laukā **Secības numurs**.
8. Laukā **Apraksts** ierakstiet kādu vērtību.
9. Sarakstā atzīmējiet atlasīto rindu.
10. Laukā **Papildināšanas vienība** ievadiet vai atlasiet kādu vērtību. Piemēram, atlasiet gab. Šis iestatījums ir obligāts. Tas ļauj norādīt citu mērvienību papildināšanas darbam, salīdzinājumā ar vienību, kas ir norādīta minimālā un maksimālā krājumu līmeņiem šajā veidnē.
11. Laukā **Darba veidne** ievadiet vai atlasiet kādu vērtību. Atrodiet iepriekš izveidoto darba veidni.  
12. Laukā **Minimālais daudzums** ievadiet skaitli. Atlasiet minimālo daudzumu, kam vajadzētu aktivizēt papildināšanu. Piemēram, iestatiet to uz 50. Ir iespējams atstāt šo iestatījumu uz nulli, ja papildināt fiksētu atrašanās vietu, un opcija **Papildināt tukšas fiksētas atrašanās vietas** ir iestatīta uz 'Jā'. Ieteicams arī atlasīt opciju **Papildināt tikai fiksētas atrašanās vietas**, lai uzlabotu veiktspēju.
13. Laukā **Maksimālais daudzums** ievadiet skaitli. Piemēram, iestatiet to uz 100.  
14. Laukā **Vienība** ievadiet vai atlasiet kādu vērtību. Piešķiriet vienību minimālajam un maksimālajam daudzumam. Piemēram, iestatiet to uz gab.  
15. Atzīmējiet izvēles rūtiņu **Papildināt tukšas fiksētas atrašanās vietas**. Atzīmējiet šo izvēles rūtiņu, lai papildinātu fiksētas atrašanās vietas, kad tās ir tukšas. Pretējā gadījumā tiek papildināti tikai tie novietojumi, kur pastāv rīcībā esošs daudzums.
16. Atzīmējiet izvēles rūtiņu **Papildināt tikai tukšas fiksētas atrašanās vietas**.
17. Noklikšķiniet uz **Atlasīt preces**. Šī ir vieta, lai definētu, kuri produkti ir jāpapildina. Ja ir atlasīta opcija Fiksētas izdošanas vietas, jums nepieciešams arī noteikt atrašanās vietas šajā vaicājumā. Ir pieejami variantam specifiski, kā arī precei specifiski vaicājumi.
18. Atlasiet rindu **Krājumi**.
19. Laukā **Kritēriji** ierakstiet kādu vērtību. Atlasiet krājumus, kas ir jāpapildina fiksētās atrašanās vietās. Piemēram, ierakstiet A*, lai atlasītu visus krājuma numurus, kas sākas ar A.
20. Noklikšķiniet uz **Pievienot**. Pievienojiet atrašanās vietas entītiju (ja vien tā jau pastāv), lai varētu ierobežot papildināšanas darbu fiksētām izdošanas vietām noteiktā noliktavas apgabalā.
21. Sarakstā atzīmējiet atlasīto rindu.
22. Iestatiet lauku **Tabula** uz 'Atrašanās vietas'.
23. Laukā **Lauks** atlasiet 'Atrašanās vietas profila ID'.
24. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.
25. Noklikšķiniet uz **Labi**.
26. Aizvērt lapu.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Iestatiet papildināšanas procesu, lai to varētu palaist kā pakešuzdevumu.
1. Dodieties uz **Noliktavas vadība > Papildināšana > Papildināšanas**. Papildināšanas lapa ļauj jums iestatīt papildināšanas palaišanu kā pakešuzdevumu, vai pieprasīt tās palaišanu manuāli.
2. Noklikšķiniet uz **Filtrēt**.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.
5. Noklikšķiniet uz **Labi**.
6. Izvērsiet sadaļu **Darbināt fonā**.
7. Iestatiet opciju **Pakešapstrāde** uz 'Jā'.
8. Noklikšķiniet uz **Periodiskums**.
9. Atlasiet opciju **Bez beigu datuma**.
10. Iestatiet **Atkārtošanās shēmu**. Piemēram: atlasiet Dienas.  
11. Noklikšķiniet uz **Labi**.
12. Noklikšķiniet uz **Labi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]