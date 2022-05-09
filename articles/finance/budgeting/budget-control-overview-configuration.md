---
title: Budžeta kontroles pārskats
description: Šajā tēmā ir ieviests budžeta kontroles līdzeklis un sniegta informācija, lai palīdzētu jums konfigurēt budžeta kontroli, lai optimizētu jūsu organizācijas finanšu resursu pārvaldību.
author: panolte
ms.date: 03/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7019b3546b83047e91fa129d8d92f209f131c993
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644854"
---
# <a name="budget-control-overview"></a>Budžeta kontroles pārskats

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir ieviests budžeta kontroles līdzeklis un sniegta informācija, lai palīdzētu jums konfigurēt budžeta kontroli, lai optimizētu jūsu organizācijas finanšu resursu pārvaldību.

Budžeta kontrole atbalsta organizācijas finanšu resursu pārvaldību, izmantojot kontu plānu, darbplūsmas, lietotāju grupas, pirmdokumentus un žurnālus, konfigurējamu pieejamo līdzekļu aprēķinu, budžeta ciklus un sliekšņus. Kad tiek izmantotas kontroles, organizācija var plānot, mērīt, pārvaldīt un prognozēt savus finanšu resursus visa finanšu gada garumā. 

Kad budžeti ir apstiprināti sistēmā, varat izmantot budžeta plānus, lai ģenerētu budžeta reģistra ierakstus un organizācijai reģistrētu izdevumu budžetu. Alternatīvi budžeta reģistra ierakstus varat izveidot trešās puses programmā vai importēt no trešās puses programmas, nevis izmantot budžeta plānošanas funkcionalitāti. 

Izdevumus var reģistrēt, izmantojot galvenos kontus un finanšu dimensijas. Kopējo izdevumu kontroli varat konfigurēt, lai tā atbilstu organizācijas politikām un prasībām, grupējot finanšu dimensiju un galveno kontu kombinācijas. 

Nākamajā diagrammā ir parādīta budžeta kontroles vieta tipiska budžeta cikla stadijās.

[![Parasts budžeta veidošanas cikls.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Budžeta kontroli varat konfigurēt atbilstoši vairākiem tālāk aprakstītajiem faktoriem.

- **Finanšu dimensijas** — kādas finanšu dimensijas jāizmanto budžeta un faktisko vērtību atskaitēm un kādas finanšu dimensijas ir nepieciešamas, lai kontrolētu budžetus? Vai pastāv specifiskas dimensiju vai galveno kontu kombinācijas, kurām ir jāpievērš īpaša uzmanība? Piemēram, vai ir prasība izsekot budžetu un faktiskās izmaksas atbilstoši izmaksu centram un programmai? Vai ceļojuma izdevumiem ir nepieciešama īpaša uzmanība?
- **Laiks** — kāds laika posms (finanšu periods, finanšu periods līdz datumam un citi posmi) tiks izmantots, lai novērtētu pieejamos budžeta līdzekļus?
- **Pirmdokumenti**— kādus pirmdokumentus ir nepieciešams novērtēt budžeta kontrolei? Vai dokumentos ir jānovērtē katra rinda atsevišķi vai jānovērtē dokuments kopumā?
- **Pieejamo līdzekļu aprēķins** — vai pieejamo līdzekļu aprēķinā ir jāņem vērā tādi dokumenti kā pirkšanas pieprasījumi (apgrūtinājumi bez juridiskām saistībām) un pirkšanas pasūtījumi (apgrūtinājumi)? Vai aprēķinā ir jāņem vērā dokumenti, kuru statuss ir melnraksts?
- **Ignorēt atļauju** — kam ir atļauja pārsniegt pieejamo budžetu?

Budžeta kontrole pilnībā tiek integrēta ar programmu. Tāpēc pieejamo budžetu varat novērtēt gan plānotajiem pirkumiem, gan faktiskajiem pirkumiem. Ir pieejamas budžeta uzziņas un atskaites. Tāpēc lietotāji var novērtēt budžetu visā budžeta cikla laikā un veikt visas nepieciešamās korekcijas, kas izpaužas kā budžeta pārskatījumi vai pārsūtījumi. Budžeta pārvaldnieks var arī eksportēt budžeta un faktiskās vērtības uz programmu Microsoft Excel, lai pēc nepieciešamības tās labāk analizētu un veiktu labāku prognozi.

## <a name="configuring-budget-control"></a>Budžeta kontroles konfigurēšana

### <a name="budget-cycle-time-span"></a>Budžeta cikla laika posms

Kad ir konfigurēts budžeta veidošanas pamats, lapā **Budžeta cikla laika posms** varat definēt budžeta vai budžeta kontroles laiku vai sākuma un beigu periodus. Budžeta cikli bieži atbilst finanšu kalendāriem, bet var ietvert vairākus finanšu gadus.

Nākamās konfigurēšanas darbības tiek veiktas cilnēs, kas tiek atvertas no lapas **Budžeta kontroles konfigurācija**.

### <a name="define-parameters"></a>Definēt parametrus

Pamatojoties uz budžetam iespējotajām finanšu dimensijām, budžeta kontrolei varat izmantot visas finanšu dimensijas vai to apakškopu. 

Turklāt varat norādīt noklusējuma laika intervālu (piemēram, **Finanšu gads**, **Finanšu gads līdz datumam**, **Finanšu periods** vai **Reizi ceturksnī**), ka budžeta kontrole tiks izpildīta saistītā budžeta laikā. Varat arī norādīt noklusējuma budžeta pārvaldnieku un slieksni, kas tiek izmantoti, lai lietotājiem ziņotu, ka ir sasniegts slieksnis. Vērtības šajos laukos tiks izmantotas kā noklusējuma vērtības visos jaunajos budžeta kontroles nosacījumos vai budžeta grupās, kas tiek veidoti. Taču atsevišķām noteikumu grupām noklusējuma vērtības var mainīt. 

Veidi, kādā budžeti tiek veidoti un reģistrēti budžeta reģistrā, palīdz noteikt laika posmu, kurš tiek atlasīts, kad tiek novērtēti pieejamie budžeta līdzekļi. Ja tiek izstrādāta un izmantota dimensiju vērtību kombinācijas ikgadējā summa, ieteicams izmantot finanšu gadu vai finanšu gadu līdz datumam. Taču, ja organizācija, kas budžetus veido finanšu periodam vai piešķir finanšu periodiem, vēlas iegūt detalizētāku kontroli, tā var apsvērt iespēju izmantot finanšu periodu līdz datumam vai ceturkšņa laika posmus. 

Turklāt konfigurāciju palīdz noteikt organizācijas kultūra, tā kā tā ir saistīta ar budžeta veidošanu un budžeta kontroli.

### <a name="over-budget-permissions"></a>Budžeta sliekšņa pārsniegšanas atļaujas

Pēc tam cilnē **Budžeta sliekšņa pārsniegšanas atļaujas** varat norādīt lietotāju grupas. Var arī norādīt, vai lietotājiem, kuri ir kādas grupas dalībnieki, ir atļauts pārsniegt budžetu. Varat nepieļaut, ka lietotāji budžetu pārsniedz par lielāku summu nekā slieksnis, kurš tika iestatīts lapā **Budžeta parametri**, vai varat nepieļaut, ka lietotāji budžetu pārsniedz par jebkādu summu, neatkarīgi no sliekšņa. Atkarībā no tā, cik proaktīvi organizācija pārvalda savus tēriņus, šīs atļaujas tai var palīdzēt pārvaldīt savus finanšu resursus. 

### <a name="budget-funds-available"></a>Pieejamie budžeta līdzekļi

Pēc tam cilnē **Pieejamie budžeta līdzekļi** varat definēt formulu, kas tiek izmantota, lai aprēķinātu pieejamos budžeta līdzekļus. Atkarībā no tā, cik konservatīvi organizācija pārvalda savus finanšu resursus, vai atkarībā no noteikumiem vai nozares prasībām, šis aprēķins var ietvert dokumentu melnrakstus vai neiegrāmatotus dokumentus. 

> [!NOTE]
> Ja budžeta cikla laikā tiek modificēts aprēķins, izmaiņas neietekmēs dokumentus, kas iepriekš tika izpildīti budžeta kontroles pārbaudes un tika grāmatoti vai pabeigti. Funkcija ar nosaukumu Tikai **atsekot summas pieejamos budžeta fondos ļauj** jums mainīt datus, kas tiek izsekoti tabulās BudgetSourceTracking. Ja ir ieslēgts šis līdzeklis, summas tiek glabātas tikai tad, ja tās ir atlasītas lietošanai pieejamo budžeta līdzekļu aprēķinā. Papildinformāciju skatiet sadaļā Pieejamie [budžeta līdzekļi](budget-funds-available.md).

### <a name="documents-and-journals"></a>Dokumenti un žurnāli

Cilnē Dokumenti **un** žurnāli varat atlasīt, uz kuriem pirmdokumentiem un žurnāliem attiecas budžeta kontroles pārbaudes un vai pārbaudes tiks veiktas rindas ieraksta vai visa dokumenta līmenī. Turklāt jaunā budžeta kontroles dokumentu filtrēšanas uzlabojumu līdzeklis, **·** Microsoft Dynamics kas ir pieejams no 365 finanšu versijas 10.0.27, sniedz uz vaicājumu balstītu filtra opciju katram dokumentam, kas ir iekļauts budžeta kontrolē. Tāpēc varat norādīt, kuri budžeta kontroles dokumenti ir pārbaudīti. Šādā veidā funkcija iespējo budžeta pārbaudi tikai dokumenta tipa apakškopai. Piemēram, var pārbaudīt tikai pirkšanas pasūtījumus, kur lauks **Kopa** ir iestatīts uz **01**. Jauna kolonna, kas tiek pievienota cilnei **Dokumenti un** žurnāli, norāda, vai atlasītajam dokumentu tipam ir definēts vaicājums. Turklāt divas jaunas pogas, kas ir pievienotas rīkjoslai virs dokumentu režģa, ļauj jums pievienot, rediģēt vai dzēst filtrēšanu. 

Ar izvēles rūtiņām atzīmētajiem pirmdokumentiem ir jāveic salīdzināšana attiecībā uz bilancēm, kuras ir iekļautas pieejamo budžeta līdzekļu aprēķinā. Piemēram, ja esat atlasījis **Budžeta rezervācijas apgrūtinājumiem**, jums jāatlasa opcija **Pirkšanas pasūtījumi**. Kad tiek veikta budžeta pārbaude, apskatot pirkšanas rindas summas un kontus, rezervēšanai piešķirtā budžeta kontroles kategorija ir **Apgrūtinājums**. Kad tiek veikta budžeta pārbaude pirkšanas pieprasījuma summām un kontiem, rezervēšanai piešķirtā budžeta kontroles kategorija ir **Apgrūtinājums bez juridiskām saistībām**. 

Ja pieejamo budžeta līdzekļu aprēķinā ir iekļautas pozīcijas **Budžeta rezervācijas apgrūtinājumam** un/vai **Budžeta rezervācijas apgrūtinājumam** bez juridiskām saistībām un tie ir jāatspoguļo ar grāmatojumiem virsgrāmatā, tad jums jāatzīmē šīs izvēles grupā **Saistību uzskaite** lapā **Virsgrāmatas parametri**.

### <a name="assign-budget-models"></a>Piešķirt budžeta modeļus

Pēc tam cilnē **Piešķirt budžeta modeļus** jūs piešķirat budžeta modeļus tiem budžeta cikla laika posmiem, kas ir jāiekļauj budžeta kontrolē.

### <a name="define-budget-control-rules"></a>Definēt budžeta kontroles nosacījumus

Pēc tam cilnē **Definēt budžeta kontroles nosacījumus** jums ir jāizveido specifiski nosacījumi, ņemot vērā budžeta kontrolei iespējotās finanšu dimensijas. Piemēram, ja koncentrējaties uz nodaļas izdevumiem vai izdevumu diapazonu, tad šīs cilnes iestatījumus varat izmantot, lai definētu un izvērtētu šos izdevumus. Katram budžeta kontroles nosacījumam varat definēt atšķirīgus sliekšņus. 

> [!Important]
> Budžeta kontrole būs iespējota visiem galvenajiem kontiem ar tipu **Peļņa un zaudējumi**, **Izdevumi**, **Ieņēmumi, Bilance, Saistības, Kapitāls** vai **Aktīvi**. Ja cilnē **Definēt budžeta kontroles noteikumus** ir kāds nosacījums, kuram ir tukši kritēriji, tad budžeta kontrole tiek iespējota **visām** finanšu dimensiju kombinācijām, kas ietver šo tipu galvenos kontus. Tāpēc nodrošiniet, lai tiktu izveidoti budžeta kontroles nosacījumi, kas definē vienīgi tos finanšu dimensiju kombināciju diapazonus, kur ir svarīgi ieslēgt budžeta kontroli.

### <a name="select-main-accounts"></a>Atlasīt galvenos kontus

Ja lapā **Definēt parametrus** kā budžeta kontroles dimensija nav atlasīts **Galvenais konts**, bet tiek pārvaldīti specifiski izdevumi, šos izdevumus varat atlasīt cilnē **Atlasīt galvenos kontus**. Ja kā budžeta kontroles dimensija ir atlasīts **Galvenais konts**, nav nepieciešami nekādi ieraksti.

### <a name="define-budget-groups"></a>Definēt budžeta grupas

Pēc tam cilnē **Definēt budžeta grupas** pēc izvēles varat definēt unikālas finanšu dimensiju kombinācijas, kurās budžeta resursi tiek apkopoti sekundāro budžeta pārbaužu veikšanai. Varat izveidot vienu ierakstu, kas ietver visu organizāciju, vai definēt vairākas grupas, kas pārstāv atsevišķas nodaļas vai izmaksu centrus.

### <a name="define-message-levels"></a>Definēt ziņojumu līmeņus

Ja budžeta kontroles brīdinājuma ziņojumi ir jāaiztur kādai no lietotāju grupām, šīs grupas varat norādīt lapā **Definēt ziņojumu līmeņus**. Lietotāju grupu dalībnieki turpina saņemt kļūdu ziņojumus, kad viņi pārsniedz pieejamos budžeta līdzekļus, pamatojoties uz savām budžeta pārsniegšanas atļaujām.

### <a name="activate-budget-control"></a>Aktivizēt budžeta kontroli

Kad budžeta kontrole ir konfigurēta, varat to ieslēgt un aktivizēt cilnē **Aktivizēt budžeta kontroli**. Pēc tam melnraksta versija stājas spēkā.

> [!Important]
> Kad budžeta kontrole ir ieslēgta un aktīva un kad transakcijas ir iegrāmatotas, to nevajadzētu izslēgt gada vidū. Ja budžeta kontrole tiek izslēgta, budžeta kontroles nolūkiem vairs netiek reģistrētas aktivitātes un budžeta pārbaudes vairs netiek veiktas. Tāpēc dokumenti, kas jau ir iegrāmatoti, ar budžeta kontroli saistītajās uzziņās un atskaitēs varētu nepareizi atspoguļot jebkādas atvieglošanas summas vai bilances. Tostarp ietilpst budžeta kontroles statistika par jebkādiem lejupstraumes vai koriģējošajiem dokumentiem un žurnāliem. 

Turklāt ņemiet vērā, ka transakcijas, tostarp budžeta reģistra ieraksti, kas iegrāmatotas pirms budžeta kontroles ieslēgšanas, budžeta kontrolei netiek ņemtas vērā. Tāpēc budžeta kontroli ieteicams ieslēgt tikai jauna budžeta cikla sākumā. Nodrošiniet, lai budžeta reģistra ierakstos, kas ietver budžeta kontrolei nepieciešamās sākuma budžeta bilances, būtu iekļautas budžeta bilances, kas atjauninātas tikai pēc budžeta kontroles ieslēgšanas. Kad lietotājs manuāli izsauc budžeta kontroles pārbaudi dokumentā, jebkurš atvērts dokuments (piemēram, pirkšanas pasūtījums) tiks pārbaudīts attiecībā uz pieejamajiem budžeta līdzekļiem un saņems budžeta rezervāciju budžeta kontrolei.

## <a name="using-budget-control"></a>Budžeta kontroles lietošana
Kad budžeta kontrole ir ieslēgta, saņemsit budžeta kontroles brīdinājumu un kļūdu ziņojumus dokumentos un žurnālos, kas ir konfigurēti budžeta kontrolei. Atcerieties — budžeta kontroli varat konfigurēt tā, lai lietotāji tiktu brīdināti, ja viņi pārsniedz budžeta līdzekļus, bet transakcijas joprojām varētu apstiprināt vai grāmatot. Detalizētu informāciju par nesekmīgajām budžeta pārbaudēm var skatīt lapā **Budžeta kontroles kļūdas un brīdinājumi**.

No šīs lapas lietotāji var atvērt lapu **Budžeta kontroles statistika pēc perioda**, lai skatītu detalizētu informāciju par budžeta pieejamību un rezervācijām atlasīto budžeta kontroles dimensiju kombinācijai. Lietotāji var arī atvērt lapu **Budžeta kontroles statistika**, lai skatītu visas budžeta pieejamību visām finanšu dimensiju kombinācijām, kas tiek lietotas budžeta kontrolē. 

Ja budžeta kontrole ir ieslēgta pirkšanas pasūtījumiem, tad budžeta pārvaldnieks var lietot darbvietu **Virsgrāmatas budžeti un prognozes**, lai pārskatītu visu neapstiprināto pirkšanas pasūtījumu rindu, kuriem ir budžeta pārbaudes brīdinājumi un kļūdas. Ja budžeta pārvaldniekam ir konfigurētas budžeta pārsniegšanas atļaujas, pirkšanas pasūtījumus var apstiprināt tieši darbvietā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
