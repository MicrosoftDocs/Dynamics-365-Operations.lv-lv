---
title: Līdzekļu pārvaldības parametri
description: Līdzekļu pārvaldībā ir jāiestata vispārējie parametri, kas attiecas uz līdzekļiem, darba pasūtījumiem un darba pasūtījumu plānošanu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3ccbb7eed643abf613f8b75ae78854246d20f6d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569881"
---
# <a name="asset-management-parameters"></a>Līdzekļu pārvaldības parametri

[!include [banner](../../includes/banner.md)]

 

Līdzekļu pārvaldībā ir jāiestata vispārējie parametri, kas attiecas uz līdzekļiem, darba pasūtījumiem un darba pasūtījumu plānošanu. Šajā tēmā ir paskaidrots, kā tos iestatīt. Lai atvērtu veidlapu, atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu pārvaldības parametri**.

Pogu **Izveidot datu vedni** var izmantot, lai automātiski izveidotu iestatīšanas datus uzņēmuma pārbaudes vai demonstrācijas datu nolūkos programmā Dynamics 365 Supply Chain Management. Informāciju par to, kā izmantot vedni, skatiet Baltajā grāmatā "Testa datu iestatīšana Līdzekļu pārvaldībā".

Saite **Līdzekļi**

- **Noklusējuma funkcionālais novietojums** ir standarta funkcionālais novietojums, kas tiek automātiski atlasīts līdzekļiem, kad veidojat jaunus līdzekļus.  
- Laukā **Standarta kalendārs** atlasiet kalendāru, kas jāizmanto līdzekļu KPI aprēķināšanai, ja līdzeklim nav atlasīts neviens resurss.  
- Laukā **Skats** atlasiet standarta skatu, kas tiek parādīts, atverot veidlapu **Līdzekļu skats** (**Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Līdzekļu skats**).
- **Noklusējuma pieprasījuma veids** ir standarta uzturēšanas pieprasījuma veids, kas tiek automātiski atlasīts, veidojot jaunu pieprasījumu.  
- Ja vēlaties izveidot projektus, kas saistīti ar līdzekļiem, projektu attiecības saistībā ar **Galvenā projekta** atlasi, **Projektu hierarhiju** un iespēju **Automātiski izveidot projektus** ir iestatītas **Līdzekļu pārvaldības parametros**.  
- Laukā **Darba pasūtījumu projekta maska** definējiet darba pasūtījumiem un pakārtotajiem apakšlīdzekļiem atļauto apakšprojektu skaitu. Darba pasūtījuma maska tiek izmantota, lai definētu, cik darba pasūtījumu var izveidot līdzeklim un lietot saistītajā darba pasūtījumu darba projektā. Darba pasūtījumu maska ir iestatīta laukā **Saistītā darba pasūtījuma maska** **Līdzekļu pārvaldības parametros** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu pārvaldības parametri** > **Darba pasūtījumi**).  
>[!NOTE]
>Saistītā darba pasūtījuma maskas formāts ir restītes zīmju skaits (#) atkarībā no maksimālā darba pasūtījumu skaita, ko paredzēts izveidot līdzeklim. Piemērs: ## ļauj izveidot līdz 99 apakšprojektus.  
- Darbu veidu prognozes tiek glabātas par atlasīto projektu laukā **Prognozēt projektu**. Katram darba veidam automātiski tiek izveidota jauna aktivitāte attiecībā uz prognozēto projektu. Pēc tam prognozes par darba veidu tiek saglabātas prognozētajā projektā.  
- Laukā **Modelis** atlasiet prognozēto modeli, kas tiek izmantots darba veida un darba pasūtījumu prognozēm.  


Saite **Darba pasūtījumi**

- **Noklusējuma darba pasūtījuma veids** definē standarta iestatījumus, veidojot darba pasūtījumu.  
- **Preventīvā darba pasūtījuma veids** definē darba pasūtījuma veidu, kas tiek izmantots, veidojot darba pasūtījumus no uzturēšanas plāniem. Ja šis lauks ir atstāts tukšs, tiek izmantots darba pasūtījuma veids laukā **Noklusējuma darba pasūtījuma veids**.  
- Laukā **Saistītā darba pasūtījuma maska** varat definēt maksimālo darba pasūtījumu skaitu, kas var būt saistīts ar darba pasūtījumu. Piemērs: ## ļauj būt līdz 99 saistītajiem darba pasūtījumiem. Ja definējat masku, kā aprakstīts šeit, saistītie darba pasūtījumi tiks numurēti [darba pasūtījuma ID darba pasūtījumam, ar kuru ir saistīts darba pasūtījums]-01,-02,-03 un tā tālāk. Ja maska netiek definēta šajā laukā, saistītais darba pasūtījums saņems nākamā secīgā darba pasūtījuma ID.  
- Atlasiet "Jā" uz **Kopēt kļūmes** pārslēgšanas pogas, ja vēlaties saistītajos uzturēšanas pieprasījumos automātiski kopēt kļūmes, kas reģistrētas par darba pasūtījumiem.  
- Laukā **Līmenis** definējiet funkcionālā novietojuma līmeni, kas tiek automātiski ievietots darba pasūtījumā, ja visi saistītie darba pasūtījuma darbi attiecas uz to pašu funkcionālo novietojumu. Ja visi darba pasūtījuma darbi nav saistīti ar to pašu funkcionālo novietojumu definētajā līmenī, lauks **Funkcionālais novietojums** darba pasūtījumā tiek atstāts tukšs. Piemērs: ievietojot šajā laukā skaitli "1", tas ir augšējais līmenis funkcionālā novietojuma struktūrā. Ievietojot šajā laukā skaitli "0", netiek definēts konkrēts funkcionālā novietojuma līmenis, bet tikai tas, ka visiem darba pasūtījuma darbiem darba pasūtījumā jābūt saistītiem ar to pašu funkcionālo novietojumu, kas jāpievieno darba pasūtījumam.  
- Žurnālus, ko izmanto, iegrāmatojot patēriņu darba pasūtījumā, var atlasīt kopsavilkuma cilnes **Vispārīgi** laukos **Stunda**, **Vienība** un **Izdevumi**.  
- Laukā **Preces valodas avots** atlasiet valodu, ko izmantot preču nosaukumiem Līdzekļu pārvaldības pārskatos. Varat atlasīt valodu, kas iestatīta uzņēmuma kontā, vai valodu, kas iestatīta lietotājam, kurš pašlaik ir pieteicies.  
- Atlasiet "Jā" uz **Reāllaika atjaunināšanas** pārslēgšanas pogas, ja vēlaties automātiski atjaunināt izmaiņas darba veida noklusējumos, uzturēšanas plānos un uzturēšanas ciklos.
> - Ja atlasīsit "Nē", izmaiņas darba veidu noklusējumos, uzturēšanas plānos un uzturēšanas ciklos netiks automātiski atjauninātas Līdzekļu pārvaldībā  
> - Pārslēgšanas pogā atlasiet "Nē", ja tiek sinhronizēti lieli datu apjomi, piemēram, daudzi līdzekļi vai funkcionālie novietojumi, kas iestatīti uzturēšanas plānos vai uzturēšanas ciklos, vai liels skaits uzturēšanas plānu vai ciklu.  
> - Veicot izmaiņas darba veidu noklusējumos vai uzturēšanas plānos vai uzturēšanas ciklos un esat atlasījis "Nē" reāllaika atjaunināšanai, brīdinājums var netikt parādīts, ja izmaiņas ietekmē:
>   - funkcionālos novietojumus, kas iestatīti apkopes plānos vai ciklos  
>   - objektus, kas iestatīti apkopes plānos vai ciklos  
>   - uzturēšanas plānu iestatīšanu  
>   - uzturēšanas ciklu iestatīšanu  
- Kopsavilkuma cilnē **Kategorija** var definēt noklusējuma kategorijas, kas attiecas uz patēriņu darba pasūtījumos.  


Saite **Darba pasūtījuma plānošana**

- **Grafika plānošanas periods** nosaka periodu dienās, kas aprēķināts no darba pasūtījuma paredzamā sākuma datuma, kura laikā darba pasūtījuma darbi tiek plānoti.  
- **Vispārējais plāns** attiecas uz resursiem modulī **Organizācijas administrēšana**. Atlasot vispārējo plānu šajā laukā, var redzēt noslodzes rezervācijas, kas saistītas ar darba pasūtījumiem **Noslodzes rezervācijās** (**Organizācijas administrēšana** > **Resursi** > **Resursi** > atlasiet resursu > cilni **Resurss** > pogu **Noslodzes rezervācijas**). Atatājot šo lauku tukšu, var redzēt noslodzi, kas saistīta ar darba pasūtījumiem **Noslodzē** (**Organizācijas administrēšana** \> **Resursi** \> **Resursi** \> atlasiet resursu \> cilni **Resurss** \> pogu **Noslodze**).  

>[!NOTE]
>Atlase attiecībā uz vispārējā plāna izmantošanu vai neizmantošanu modulī **Līdzekļu pārvaldība** un saistītā veidlapa, kas tiek izmantota, lai iegūtu pārskatu par noslodzes rezervācijām vai noslodzi, ir standarta iestatīšana. Atkarībā no iestatījuma laukā **Vispārējais plāns**, jūs varat piekļūt noslodzes informācijai **Noslodzes rezervācijās** vai **Noslodzē** modulī **Organizācijas administrēšana**. Nav iespējams izveidot iestatījumu, kurā noslodzes rezervācijas tiek rādītas abos skatos.  

Zemāk redzamajā aizzīmju sarakstā aprakstītie lauki attiecas uz aprēķinātiem vērtējuma rezultātiem, kurus izmanto darba pasūtījuma prioritātes aprēķināšanai darba pasūtījumu plānošanas laikā.

- **Prioritāte** — vērtējuma rādītājs, kas aprēķināts kopā ar vērtējuma rezultātu laukos  **Kritiskums** un **Sākuma datums**. Skaitlis šajā laukā tiek dalīts ar skaitli darba pasūtījuma laukā **Prioritāte**. Piemērs: ja šajā laukā tiek ievietota vērtība "5,00" un darba pasūtījuma prioritāte ir "20", tad prioritātes vērtējuma rādītājs ir 0,25.  
- **Kritiskums** — vērtējuma rādītājs, kas aprēķināts kopā ar vērtējuma rezultātu laukos **Prioritāte** un **Sākuma datums**. Skaitlis šajā laukā tiek reizināts ar skaitli darba pasūtījuma laukā **Kritiskums**. Piemērs: ja šajā laukā tiek ievietota vērtība "10,00" un darba pasūtījuma prioritāte ir "5", tad kritiskuma vērtējuma rādītājs ir 50.  
- **Sākuma datums** — vērtējuma rādītājs, kas aprēķināts kopā ar vērtējuma rezultātu laukos **Prioritāte** un **Kritiskums**. Šis lauks norāda dienas rezultātu kā negatīvu vērtību un tiek salīdzināts ar darba pasūtījuma lauku **Paredzamais sākums**. Piemērs: ja šajā laukā tiek ievietota vērtība "10,00" un darba pasūtījuma paredzamais sākuma datums ir trīs dienas no šī brīža, vērtējuma rezultāts ir mīnus 30,00. Pievienojot rezultātus 0,25 un 50 no piemēriem iepriekš aprakstītos laukos **Prioritāte** un **Kritiskums**  kopumā ir plus 20,25. Šis skaitlis tiek salīdzināts ar visiem pārējiem darba pasūtījumu vērtējuma rezultātiem darba pasūtījumu plānošanas laikā, un pēc tam vispirms tiek plānoti augstākā vērtējuma rādītāji.  
- **Atbildīgais darbinieks** — vērtējuma rādītājs, kas aprēķināts kopā ar **Atbildīgās darbinieku grupas**, **Vēlamā darbinieka**, **Vēlamo darbinieku grupas**, **Līdzekļa atrašanās vietas** un **Sākuma datuma** vērtējuma rādītāju vērtībām. Ja šajā laukā tiek ievietota vērtība "50,00" un darba pasūtījumam ir atlasīts atbildīgais darbinieks, šis darbinieks kopējā darbinieku aprēķinā darba pasūtījuma plānošanas laikā saņem 50 punktus.  
- **Atbildīgā darbinieku grupa** — vērtējuma rādītājs, kas aprēķināts kopā ar **Atbildīgās darbinieku grupas**, **Vēlamā darbinieka**, **Vēlamo darbinieku grupas**, **Līdzekļa atrašanās vietas** un **Sākuma datuma** vērtējuma rādītāju vērtībām. Ja šajā laukā tiek ievietota vērtība "50,00" un darba pasūtījumam ir atlasīts atbildīgais darbinieks, šis darbinieks kopējā darbinieku aprēķinā darba pasūtījuma plānošanas laikā saņem 50 punktus.  
- **Ierobežot līdz atbildīgajam** Jā/Nē pārslēgšanas poga ierobežo darba pasūtījuma plānošanai pieejamo darbinieku skaitu. Atlasiet "Nē", ja vēlaties aprēķināt rezultātu visiem darbiniekiem neatkarīgi no tā, vai tie ir iestatīti kā atbildīgie darbinieki vai kā daļa no atbildīgās darbinieku grupas. Atlasiet "Jā", ja vēlaties aprēķināt rezultātu darbiniekiem, kuri darba pasūtījumā ir iestatīti kā atbildīgi darbinieki un/vai iekļauti darba pasūtījumam atlasītajā atbildīgajā darbinieku grupā.  
- **Vēlamais darbinieks** — vērtējuma rādītājs, kas aprēķināts kopā ar **Atbildīgās darbinieku grupas**, **Vēlamā darbinieka**, **Vēlamo darbinieku grupas**, **Līdzekļa atrašanās vietas** un **Sākuma datuma** vērtējuma rādītāju vērtībām. Tiek aprēķināti un summēti kopā četri vērtējuma rādītāji, lai nodrošinātu punktu skaitu, kas tiek izmantots, atlasot to, kurš darbinieks ir jāpiešķir kuram darba pasūtījumam darba pasūtījumu plānošanas laikā. Ja šajā laukā tiek ievietota vērtība "10,00" un darba pasūtījumam darbinieks ir atlasīts kā vēlamais darbinieks, šis darbinieks kopējā darbinieku aprēķinā darba pasūtījuma plānošanas laikā saņem 10 punktus.  
- **Vēlamā darbinieku grupa** — vērtējuma rādītājs, kas aprēķināts kopā ar **Atbildīgās darbinieku grupas**, **Vēlamā darbinieka**, **Vēlamo darbinieku grupas**, **Līdzekļa atrašanās vietas** un **Sākuma datuma** vērtējuma rādītāju vērtībām. Ja šajā laukā tiek ievietota vērtība "10,00" un darbinieks ir piešķirts vēlamajai darbinieku grupai, kas atlasīta darba pasūtījumam, šis darbinieks kopējā darbinieku aprēķinā darba pasūtījuma plānošanas laikā saņem 10 punktus.  
- **Ierobežot līdz vēlamajam** Jā/Nē pārslēgšanas poga ierobežo darba pasūtījuma plānošanai pieejamo darbinieku skaitu. Atlasiet "Nē", ja vēlaties aprēķināt rezultātu visiem darbiniekiem neatkarīgi no tā, vai tie ir iestatīti kā vēlamie darbinieki vai kā daļa no vēlamās darbinieku grupas. Atlasiet "Jā", ja vēlaties aprēķināt rezultātu tikai tiem darbiniekiem, kuri ir iestatīti kā vēlamie darbinieki un/vai iekļauti vēlamajā darbinieku grupā.  
- **Atrašanās vieta** — vērtējuma rādītājs, kas aprēķināts kopā ar **Atbildīgās darbinieku grupas**, **Vēlamā darbinieka**, **Vēlamo darbinieku grupas**, **Līdzekļa atrašanās vietas** un **Sākuma datuma** vērtējuma rādītāju vērtībām. Ja šajā laukā ir ievietota vērtība "3000,00", darbinieks iegūst 3000 punktus aprēķinā, ja darbinieks atrodas tajā pašā rūpnīcā vai objektā, kur atrodas līdzeklis, kuram darbs ir jāieplāno.  

  - Ja jūsu uzņēmums izmanto funkcionālos novietojumus, darbinieki saņem pilnu punktu skaitu, ja tie atrodas funkcionālajā novietojumā, kas saistīts ar līdzekli. Ja līdzekļa funkcionālajam novietojumam ir primārais līdzeklis, darbinieki šajā funkcionālajā novietojumā saņem 1/2 punktu skaita. Ja arī šai atrašanās vietai ir vecākelements, darbinieki šajā vietā saņem 1/3 punktu skaita. Ja arī šai atrašanās vietai ir vecākelements, darbinieki šajā vietā saņem 1/4 punktu skaita un tā tālāk.  
  - Ja jūsu uzņēmums izmanto līdzekļu atrašanās vietu, kuru mēs neiesakām, lai aprēķinātu atrašanās vietas rezultātus, tiek izmantota atrašanās vieta, apgabals un zona. Darbinieki saņem pilnu punktu skaitu, ja tie atrodas atrašanās vietā un zonā, kas saistīta ar līdzekli. Ja darbinieka atrašanās vieta atbilst tikai atrašanās vietai un apgabalam, darbinieka vērtējuma rādītājs ir 2/3 no pilna punktu skaita. Ja darbinieka atrašanās vieta atbilst tikai atrašanās vietai, darbinieka vērtējuma rādītājs ir 1/3 no pilna punktu skaita.  

- **Ierobežot līdz atrašanās vietai** Jā/Nē pārslēgšanas poga ierobežo darba pasūtījuma plānošanai pieejamo darbinieku skaitu. Atlasiet "Nē", ja vēlaties aprēķināt rezultātu visiem darbiniekiem visos funkcionālajos novietojumos. Atlasiet "Jā", ja vēlaties aprēķināt rezultātu tikai tiem darbiniekiem, kuri ir saistīti ar darba pasūtījuma funkcionālo novietojumu.

>[!NOTE]
>Trīs "Ierobežot līdz..." pārslēgšanas pogas ir ieviestas, lai palielinātu darba pasūtījuma plānošanas ātrumu, ierobežojot darbiniekiem aprēķināto punktu skaitu.

**Darbinieka sākuma datums** — vērtējuma rādītājs, kas aprēķināts kopā ar **Atbildīgās darbinieku grupas**, **Vēlamā darbinieka**, **Vēlamo darbinieku grupas**, **Līdzekļa atrašanās vietas** un **Sākuma datuma** vērtējuma rādītāju vērtībām. Šis lauks norāda dienas rezultātu kā negatīvu vērtību un tiek salīdzināts ar darba pasūtījuma lauku **Paredzamais sākums**. Piemērs: ja šajā laukā tiek ievietota vērtība "10,00" un darba pasūtījuma paredzamais sākuma datums ir rīt, vērtējuma rezultāts ir mīnus 10,00.

  - Pieņemot, ka plānojamajam darba pasūtījumam nav atlasīta atbildīgais darbinieks un atbildīgā darbinieku grupa, pievienojot un atņemot vērtējuma rādītāju vērtības piemēros iepriekš minētajos laukos **Vēlamais darbinieks**, **Vēlamā darbinieku grupa**, **Līdzekļa atrašanās vieta** un **Sākuma datums**, jūs iegūstat kopsummu 3010,00. Tas nozīmē augstu rezultātu darbiniekam, kurš jau ir atlasīts kā vēlamais darbinieks, kā arī iekļauts darba pasūtījuma vēlamajā darbinieku grupā, un darbinieks atrodas arī tajā pašā objektā, kur līdzeklis, kam nepieciešams ieplānot darbu. Kopumā tas nozīmē, ka ir labas izredzes, ka darba pasūtījuma plānošanas laikā attiecīgais darbinieks tiks atlasīts darba izpildei.  
  - Ja vienā no iepriekš minētajiem astoņiem laukiem ir ievietota vērtība "0,00", šis vērtējuma rezultāts netiks izmantots darba pasūtījuma plānošanas laikā.  


Saite **Dokumentu veidi**

Atlasiet dokumentu veidus, kuriem jābūt pieejamiem, drukājot pielikumus, kas saistīti ar darba pasūtījuma pārskatu. Tas tiek darīts, noklikšķinot uz dokumenta veida sadaļā **Pieejams** un noklikšķinot uz pogas ![bultiņa uz priekšu](media/15-setup-for-objects.png). Ja vēlaties noņemt atlasīto dokumenta veidu, atlasiet dokumenta veidu sadaļā **Atlasīts** un noklikšķiniet uz pogas ar ![bultiņa atpakaļ](media/16-setup-for-objects.png).



Saite**Numuru sērijas**

Atlasiet šajā sadaļā nepieciešamās numuru sērijas. Līdzekļiem ir divas numuru sērijas: viena manuāli izveidotiem līdzekļiem, bet otra —līdzekļiem, kas izveidoti, izmantojot gaidošos līdzekļus.
