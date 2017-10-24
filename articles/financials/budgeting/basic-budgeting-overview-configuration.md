---
title: "Budžeta veidošanas apskats"
description: "Gandrīz ikvienam uzņēmumam, kas izmanto programmatūras Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise funkcionalitāti Finanšu dati, ir jāspēj izveidot budžeta un faktisko izmaksu salīdzinājuma pārskatus. Šajā rakstā ir paskaidrota minimālā konfigurācija, kas ir nepieciešama, lai programmatūras Dynamics 365 for Finance and Operations izdevumā Enterprise izveidotu budžetus vai tos ielādētu no kādas trešās puses programmas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b79206291264ddc053e401996398f6a4449ad52e
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="budgeting-overview"></a>Budžeta veidošanas apskats 

[!include[banner](../includes/banner.md)]


Gandrīz ikvienam uzņēmumam, kas izmanto programmatūras Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise funkcionalitāti Finanšu dati, ir jāspēj izveidot budžeta un faktisko izmaksu salīdzinājuma pārskatus. Šajā rakstā ir paskaidrota minimālā konfigurācija, kas ir nepieciešama, lai programmatūrā Dynamics 365 for Finance and Operations izveidotu budžetus vai tos ielādētu no kādas trešās puses programmas.

<a name="overview"></a>Pārskats
--------

Apstiprinātais budžets juridiskai personai tiek uzturēts dokumentā, kas ir pazīstams kā *budžeta reģistra ieraksts*. Rindas budžeta reģistra ieraksta dokumentā tiek sauktas par *budžeta konta* ierakstiem, un satur informāciju par apstiprinātā budžeta finanšu dimensiju, datumiem un summām. Budžeta reģistra ieraksta dokuments ietver pamata finanšu pārskatus un uzziņu lapas, kur virsgrāmatas faktiskās summas tiek salīdzinātas ar budžetā paredzētajām summām. 

Programmatūrā Dynamics 365 for Finance and Operations ir pieejamas vairākas budžeta reģistra ierakstu izveides metodes, kas ir norādītas tālāk.

-   Manuāli ievadiet dokumenta informāciju lapā **Budžeta reģistra ieraksti**.
-   Izmantojiet Microsoft Excel veidni, ko var atvērt, noklikšķinot uz pogas **Atvērt programmā Excel** lapā **Budžeta reģistra ieraksti**.
-   Izmantojiet datu elementu **Budžeta kontu ieraksti** sadaļā Datu pārvaldība, lai importētu budžeta reģistra ierakstus. Ja sistēmā ir jāimportē daudzi budžeta kontu ieraksti, ir jāapsver iespēja izmantot šo metodi un ieslēgt parametru **No kopas atkarīga** **apstrāde**.
-   Ja uzņēmums izmanto Budžeta plānošanas funkcionalitāti, lai sagatavotu budžeta datus, var izmantot periodisko procesu **Budžeta reģistra ieraksta ģenerēšana**.

Budžeta reģistra ieraksts tiek uzskatīts par pabeigtu, kad budžeta bilances ir atjauninātas. Lapā **Budžeta reģistra ieraksti** noklikšķiniet uz **Atjaunināt budžeta bilances** atlasītajam budžeta reģistra ierakstam vai vairākiem ierakstiem. Kad tiek atjauninātas budžeta bilances, budžeta reģistra ieraksta statuss mainās uz **Pabeigts**. Pabeigtu budžeta reģistra ierakstu nevar atkārtoti atvērt, lai veiktu labojumus. Tādēļ, ja jāpielāgo budžeta dati, ir jāizveido jauns budžeta reģistra ieraksts nevis jālabo pabeigtā budžeta reģistra ieraksta dati.

## <a name="configuration"></a>Konfigurācija
Konfigurējot budžeta plānošanu, sāciet no lapas **Budžeta veidošanas parametri**. Šajā lapā jādefinē budžeta žurnāls, numuru sērija budžeta reģistra ieraksti un darbalauku noklusējuma uzvedība.

Pēc tam, ja ir politikas, kas regulē budžeta reģistra ierakstu apstiprināšanu, pamatojoties uz budžeta tipu (piemēram, pārsūtīšanas vai pārskatīšanas), jāizveido budžeta reģistra ieraksta darbplūsmas lapā **Budžeta veidošanas darbplūsmas**. Ja ir scenāriji, kur pārsūtīšanas var būt atļautas bez darbplūsmas apstiprinājuma, varat definēt budžeta pārsūtīšanas nosacījumus, lai atbalstītu šo scenāriju. 

Lapā **Budžeta veidošanas dimensijas** ir jāatlasa finanšu dimensijas, ko izmantot budžeta plānošanai, pamatojoties uz dimensijām, kas tiek izmantotas kontu plānā. Budžeta plānošanai var atlasīt visas finanšu dimensijas vai to apakškopu.

Definējiet *budžeta modeli*, kas atbilst visiem vai dažiem budžetiem. Var izmantot vienu budžeta modeli visiem budžeta reģistra ierakstiem. Var arī izveidot atsevišķus modeļus, kam pamatā ir budžeta veids, ģeogrāfiskā atrašanās vieta vai kāds cits budžeta klasifikācijas tips. 

> [!NOTE] 
> Ja tiek izmantota budžeta kontrole, ar konkrētu budžeta cikla laika posmu varat saistīt tikai vienu budžeta modeli. 

Izveidojiet *budžeta kodus*, kas identificē ierakstāmo budžeta transakciju tipu un jebkuru saistīto darbplūsmu. Budžeta kodi var atbalstīt šādus budžeta tipus:

-   Sākotnējais budžets
-   Pārcelšana
-   Pārskatījums
-   Apgrūtinājums
-   Apgrūtinājums bez juridiskām saistībām
-   Pārnestais budžets

Budžeta kodi nodrošina auditācijas pierakstus par apstiprinātā budžeta modifikācijām budžeta cikla gaitā. Ja darbplūsma ir saistīta ar kādu budžeta kodu, tad darbplūsma būs iespējota visiem budžeta reģistra ierakstiem, kuri lieto šo budžeta kodu, un darbplūsmas darbības ir jāpabeidz, lai budžeta reģistra ieraksts varētu sasniegt stadiju **Pabeigts**.  

Ja vēlaties, varat arī iestatīt *budžeta pārsūtīšanas kārtulas*. Lai izmantotu budžeta pārsūtīšanas kārtulas, lapā **Budžeta parametri** atlasiet **Lietot budžeta pārsūtījumu kārtulas**. Kad tiek izmantotas budžeta pārsūtīšanas kārtulas, ja lietotājs veido dokumentu, izmantojot budžeta kodu ar tipu **Pārsūtīšana**, budžeta bilances netiks atjauninātas, ja ir pārkāptas budžeta pārsūtīšanas kārtulas. Piemēram, jūs varat atļaut budžeta pārsūtīšanas dokumentus, kur izdevumu budžets tiek pārsūtīts starp Pārdošanas un mārketinga nodaļas galvenajiem kontiem, un aizliegt budžeta pārsūtīšanu no vai uz šo nodaļu, ja šāda veida budžeta konta ierakstam piešķirts darbplūsmas apstiprinājums.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Darbvietu un uzziņu lapu izmantošana, lai izsekotu budžetu, salīdzinot ar faktiskām izmaksām
Budžeta pārvaldnieks var pārskatīt budžeta pašreizējo stāvokli darbvietā **Virsgrāmatas budžeti un prognozes**. Cilnes **Izdevumi pārsniedz budžetu** un **Ieņēmumi nesasniedz budžetu** nodrošina ātru finanšu dimensiju kombināciju apskatu, kur budžeta mērķi nav izpildīti vai tuvojas slieksnim. Jūs varat personalizēt budžeta sliekšņa procentuālo vērtību un finanšu dimensiju kopas, kas tiek izmantotas šajās cilnēs, noklikšķinot uz **Konfigurēt manu darbvietu**. Varat noklikšķināt uz **Vienību vadītāji**, lai apskatītu darbiniekus, kuri ir atbildīgi par noteiktām finanšu dimensiju kombinācijām, kas ir atlasītas šajās cilnēs. Piemēram, ja redzat, ka Operāciju nodaļas izdevumu budžets pārsniedz budžeta slieksni, jūs varat viegli atrast un sazināties ar Operāciju nodaļas vadītāju, lai apspriestu šo jautājumu. 

> [!NOTE] 
> Lapas **Organizācijas vienības** lauks **Nodaļas vadītājs** nosaka, kuri vadītāji atbalsta noteiktas finanšu dimensiju kombinācijas. Noklikšķiniet uz **Skatīt vairāk** cilnes apakšdaļā, lai atvērtu uzziņu lapu **Budžetā paredzētās pret faktiskajām**, lai iegūtu detalizētu informāciju par budžeta summām salīdzinājumā ar faktiskajām summām. 

Uzziņu lapa **Faktiski pret budžetu** ļauj iegūt detalizētu informāciju par budžetu, salīdzinot ar faktiskām summām. Atlasiet rindu uzziņu lapā un pēc tam noklikšķiniet uz **Perioda bilances**, lai apskatītu budžeta un faktisko summu sadalījumu pa finanšu periodiem. Lapa **Budžeta kontu ieraksti** sniedz detalizētu informāciju par budžeta summu budžeta reģistra ierakstos. Lapā **Virsgrāmatas žurnāla ieraksti** atveras Virsgrāmatas transakcijas, kas ir iekļautas aprēķinātā summā **Faktiskās vērtības**. 

Uzņēmums, kas izmanto Budžeta plānošanas funkcionalitāti, var izveidot un izmantot *budžeta prognozes* darbvietā **Virsgrāmatas budžeti un prognozes**.




