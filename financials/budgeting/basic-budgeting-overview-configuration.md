---
title: "Budžeta veidošanas apskats"
description: "Gandrīz katrs uzņēmums, kas izmanto Financials funkcionalitāti Microsoft Dynamics 365 operācijām būs iespēja izveidot atskaites budžeta vs reālos datus. Šajā rakstā ir paskaidrots, minimālā konfigurācija, kas ir nepieciešama, lai izveidotu budžeta dinamika 365 operācijām vai ielādēt tos no trešās puses programmu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Budžeta veidošanas apskats

Gandrīz katrs uzņēmums, kas izmanto Financials funkcionalitāti Microsoft Dynamics 365 operācijām būs iespēja izveidot atskaites budžeta vs reālos datus. Šajā rakstā ir paskaidrots, minimālā konfigurācija, kas ir nepieciešama, lai izveidotu budžeta dinamika 365 operācijām vai ielādēt tos no trešās puses programmu.

<a name="overview"></a>Pārskats
--------

Apstiprinātais budžets juridiskai personai tiek uzturēts dokumentā, kas ir pazīstams kā *budžeta reģistra ieraksts*. Budžeta reģistra ieraksta dokumenta rindām ir pazīstami kā *budžeta kontu* ierakstus, un ietver finanšu dimensiju informāciju, datumus un summas, kas no apstiprinātā budžeta. Budžeta reģistra ierakstu dokumentu ir integrēta ar pamata finanšu pārskati un izmeklēšanas lappusēm, kur grāmatas faktiskās summas tiek salīdzināti ar budžetu summas. 

Pastāv vairākas metodes, lai radītu budžeta reģistra ierakstiem programmā Dynamics 365 operācijām:

-   Manuāli ievadiet dokumenta informāciju lapā **Budžeta reģistra ieraksti**.
-   Izmantojiet Microsoft Excel veidni, ko var atvērt, noklikšķinot uz pogas **Atvērt programmā Excel** lapā **Budžeta reģistra ieraksti**.
-   Izmantojiet datu elementu **Budžeta kontu ieraksti** sadaļā Datu pārvaldība, lai importētu budžeta reģistra ierakstus. Jums vajadzētu apsvērt šo metodi un ieslēdzot **kopu, kuras pamatā** * * apstrādes * * parametrs, kad daudzi budžeta kontu ierakstu sistēmā ir jāimportē.
-   Ja uzņēmums izmanto Budžeta plānošanas funkcionalitāti, lai sagatavotu budžeta datus, var izmantot periodisko procesu **Budžeta reģistra ieraksta ģenerēšana**.

Budžeta reģistra ierakstā tiek uzskatīts pabeigts pēc budžeta bilances ir atjaunināti. Par **budžeta reģistra ieraksti** lapu, noklikšķiniet uz **atjauninātu budžeta bilances** atlasīto budžetu reģistra ierakstu vai vairākiem ierakstiem. Kad tiek atjauninātas budžeta bilances, budžeta reģistra ieraksta statuss mainās uz **Pabeigts**. Pabeigtu budžeta reģistra ierakstu nevar atkārtoti atvērt, lai veiktu labojumus. Tādēļ, ja jāpielāgo budžeta dati, ir jāizveido jauns budžeta reģistra ieraksts nevis jālabo pabeigtā budžeta reģistra ieraksta dati.

## <a name="configuration"></a>Konfigurācija
Konfigurējot budžeta plānošanu, sāciet no lapas **Budžeta veidošanas parametri**. Šajā lapā jādefinē budžeta žurnāls, numuru sērija budžeta reģistra ieraksti un darbalauku noklusējuma uzvedība.

Pēc tam, ja ir politikas, kas regulē budžeta reģistra ierakstu apstiprināšanu, pamatojoties uz budžeta tipu (piemēram, pārsūtīšanas vai pārskatīšanas), jāizveido budžeta reģistra ieraksta darbplūsmas lapā **Budžeta veidošanas darbplūsmas**. Ja ir scenāriji, kur pārsūtīšanas var būt atļautas bez darbplūsmas apstiprinājuma, varat definēt budžeta pārsūtīšanas nosacījumus, lai atbalstītu šo scenāriju. 

Lapā **Budžeta veidošanas dimensijas** ir jāatlasa finanšu dimensijas, ko izmantot budžeta plānošanai, pamatojoties uz dimensijām, kas tiek izmantotas kontu plānā. Budžeta plānošanai var atlasīt visas finanšu dimensijas vai to apakškopu.

Noteikt * budžeta modeli *, kas atbilst visām vai dažām no budžetiem. Var izmantot vienu budžeta modeli visiem budžeta reģistra ierakstiem. Var arī izveidot atsevišķus modeļus, kam pamatā ir budžeta veids, ģeogrāfiskā atrašanās vieta vai kāds cits budžeta klasifikācijas tips. 

> [!NOTE] 
> Ja izmanto budžeta kontroli, tikai vienu budžeta modeli var saistīt ar konkrētu budžeta ciklu laika posmu. 

Izveidojiet *budžeta kodus*, kas identificē ierakstāmo budžeta transakciju tipu un jebkuru saistīto darbplūsmu. Budžeta kodi var atbalstīt šādus budžeta tipus:

-   Sākotnējais budžets
-   Pārcelšana
-   Pārskatījums
-   Apgrūtinājums
-   Apgrūtinājums bez juridiskām saistībām
-   Pārnestais budžets

Budžeta kodi nodrošina auditācijas pierakstus par apstiprinātā budžeta modifikācijām budžeta cikla gaitā. Ja darbplūsma ir saistīta ar budžeta kods, darbplūsma tiks iespējoti visi budžeta reģistra ierakstus, kas izmanto šo budžeta kods un darbplūsmas soļus jāpabeidz pirms budžeta reģistra ierakstā var sasniegt **pabeigts** posmā.  

Varat arī pēc izvēles iestatīt *budžeta nodošanas noteikumiem*. Izmantot budžeta pārsūtīšanas kārtulas, atlasiet **izmantot noteikumus par budžeta nodošanu** par **budžeta parametri** lapā. Kad tiek izmantotas budžeta pārsūtīšanas kārtulas, ja lietotājs veido dokumentu, izmantojot budžeta kodu ar tipu **Pārsūtīšana**, budžeta bilances netiks atjauninātas, ja ir pārkāptas budžeta pārsūtīšanas kārtulas. Piemēram, jūs varat atļaut budžeta pārsūtīšanas dokumentus, kur izdevumu budžets tiek pārsūtīts starp Pārdošanas un mārketinga nodaļas galvenajiem kontiem, un aizliegt budžeta pārsūtīšanu no vai uz šo nodaļu, ja šāda veida budžeta konta ierakstam piešķirts darbplūsmas apstiprinājums.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Darbvietu un uzziņu lapu izmantošana, lai izsekotu budžetu, salīdzinot ar faktiskām izmaksām
Budžeta pārvaldnieks var pārskatīt budžeta pašreizējo stāvokli darbvietā **Virsgrāmatas budžeti un prognozes**. Cilnes **Izdevumi pārsniedz budžetu** un **Ieņēmumi nesasniedz budžetu** nodrošina ātru finanšu dimensiju kombināciju apskatu, kur budžeta mērķi nav izpildīti vai tuvojas slieksnim. Jūs varat personalizēt budžeta sliekšņa procentuālo vērtību un finanšu dimensiju kopas, kas tiek izmantotas šajās cilnēs, noklikšķinot uz **Konfigurēt manu darbvietu**. Varat noklikšķināt uz **Vienību vadītāji**, lai apskatītu darbiniekus, kuri ir atbildīgi par noteiktām finanšu dimensiju kombinācijām, kas ir atlasītas šajās cilnēs. Piemēram, ja redzat, ka Operāciju nodaļas izdevumu budžets pārsniedz budžeta slieksni, jūs varat viegli atrast un sazināties ar Operāciju nodaļas vadītāju, lai apspriestu šo jautājumu. 

> [!NOTE] 
> **Departamenta vadītājs** lauku **organizācijas vienībām** lapa nosaka, kura vadītāji atbalsta konkrētu finanšu dimensiju kombinācijas. Noklikšķiniet uz **Skatīt vairāk** cilnes apakšdaļā, lai atvērtu uzziņu lapu **Budžetā paredzētās pret faktiskajām**, lai iegūtu detalizētu informāciju par budžeta summām salīdzinājumā ar faktiskajām summām. 

Uzziņu lapa **Faktiski pret budžetu** ļauj iegūt detalizētu informāciju par budžetu, salīdzinot ar faktiskām summām. Atlasiet rindu uzziņu lapā un pēc tam noklikšķiniet uz **Perioda bilances**, lai apskatītu budžeta un faktisko summu sadalījumu pa finanšu periodiem. Lapa **Budžeta kontu ieraksti** sniedz detalizētu informāciju par budžeta summu budžeta reģistra ierakstos. Lapā **Virsgrāmatas žurnāla ieraksti **atveras Virsgrāmatas transakcijas, kas ir iekļautas aprēķinātā summā **Faktiskās vērtības**. 

Uzņēmums, kas izmanto Budžeta plānošanas funkcionalitāti, var izveidot un izmantot *budžeta prognozes *darbvietā **Virsgrāmatas budžeti un prognozes**.


