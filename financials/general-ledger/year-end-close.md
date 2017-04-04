---
title: "Gada beigu slēgšana"
description: "Šajā tēmā ir aprakstīts, nepieciešama setup un darbības Virsgrāmatas beigu tuvu procesa braukšanai."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Gada beigu slēgšana

Šajā tēmā ir aprakstīts, nepieciešama setup un darbības Virsgrāmatas beigu tuvu procesa braukšanai. 

Finanšu gada beigās, ir jāpalaiž beigu tuvu procesa sākuma atlikumus pārcelt uz jauno gadu. Lielākā daļa organizāciju darbosies ciešā beigu procesa vairākas reizes. Pirmo reizi būtu iegūt bilances pārvietots uz jaunu finanšu gadu. Gada beigās tuvu var pēc tam palaist vēlreiz, kā daudzkārt tiek prasīts pārvietot atlikumus no pielāgošanas ieiešanu jaunajā finanšu gadā. 

Gada laikā slēgt procesā, pastāv divu veidu iespējamās darbības, kas izveidotas. Sākuma darbība vienmēr ir radīts un tiek lietots, lai izveidotu sākuma bilances jaunajā finanšu gadā. Atvēršanas darbības parāda bilances Virsgrāmatas kontu bilances jaunajā finanšu gadā, un no nesadalītās peļņas Virsgrāmatas kontu bilances peļņas un zaudējumu Virsgrāmatas kontu bilances jaunajā finanšu gadā. Slēgšanas darbība ir izveidota pēc izvēles, lai bilances, peļņas un zaudējumu pārskatu līdz nullei finanšu gads ir slēgts.

## <a name="prepare-to-run-the-year-end-close"></a>Sagatavot gada tuvu palaišanai
Pirms jūs darbināt beigu tuvu procesa, apstiprināt šādus iestatījumus: 

Lapā **Galvenais konts**:

-   Apstiprināt **galvenā konta tips** ir pareizi definēts katrā galvenajā kontā. Galvenā konta tips tiek izmantots, lai noteiktu, vai galvenā konta atlikums būs vērsta uz priekšu kā sākuma bilanci vai slēgtā uz nesadalītās peļņas sākuma darbības.
-   **Konta atvēršanu** lauku var izmantot, lai pārsūtītu galvenā konta atlikumu uz jaunu galveno kontu laikā aizvērt gada beigās. Jauns galvenais konts tiek ievadīts **konta atvēršanu** lauks. Parasti tas tiks izmantots galveno bilances kontiem, kad galvenais konts ir deaktivizēts un jauns galvenais konts tiek izmantots jaunajā finanšu gadā.

Par **Virsgrāmatas parametru** lapa zem **finanšu gada slēgšana**:

-   **Dzēst aizvērt gada darījumu** opciju lieto, lai norādītu, vai sistēmas ģenerēts sākuma darbība no tuvu iepriekšējā gada beigās būtu jāsvītro, vēlreiz palaižot tuvu gada beigās. Ja ir uzstādīta šī opcija **Jā**, iepriekšējās atvēršanas darbība tiek dzēsta un jaunās sākuma darbības ir izveidots, pamatojoties uz pašreizējo bilanci. Ja ir uzstādīta šī opcija **Nr**, paliek iepriekšējais sākuma darbība un papildu atvēršanu darbība tiek izveidota, lai pārvietotu bilances uz priekšu no pielāgošanas darbībām, kas grāmatotas pēc iepriekšējā gada beigās slēgt.
-   **Izveidot slēguma darbības pārsūtīšanas laikā** opcija tiek izmantota, lai veidotu slēguma darbības tiek slēgtas, lai panāktu nulles bilances, peļņas un zaudējumu pārskatu finanšu gadā. Ja ir uzstādīta šī opcija **Jā**, gan sākuma darbība un slēguma darbības tiek izveidots. Ja ir uzstādīta šī opcija **Nr**, nākamajā finanšu gadā, lai pārsūtītu bilances tiek veidota tikai sākuma darbība. Peļņas un zaudējumu kontu atlikumi paliek finanšu gada beigās.
-   **Fiskālajā gadā statuss jāiestata uz slēgts pastāvīgi** opciju lieto, lai iestatītu fiskālajā gadā neatgriezeniski slēgta statusu. Šo iestatījumu varat izmantot piesardzīgi, jo visi periodi ar neatgriezeniski slēgta statusu nevar atsākt, novērst labojumus no tiek grāmatota finanšu gada. Labākā prakse ir iestatīts tas **Nr**.
-   **Ir jāaizpilda dokumenta numurs** opcija tiek izmantota, lai definētu, vai dokumenta numurs ir nepieciešama, ja palaists beigu tuvu procesa. Ir labākā prakse prasīt dokumenta numuru, lai viegli identificētu darījumu atklāšana.

Par **finanšu Kalendārs** lapas:

-   Nākamajam finanšu gadam ir jābūt izveidotam, pirms palaišanas, gada beigās slēgt. Nākamajam finanšu gadam ir nepieciešama, lai izveidotu sākuma bilances sākuma periodu.

Par **Virsgrāmatas Kalendārs** lapas:

-   Pēc izvēles: Katram finanšu periodam finanšu gadam tiek slēgts var iestatīt **aizturēts** lai novērstu jaunu darbības tiek ievadītas. Korekcijas ierakstiem tiek identificēti, par aizturēšanas periodi var atbildēt regulēšanas ierakstu, pat tad, ja gada beigās ciešā process jau izpildīta.

## <a name="define-year-end-close-templates"></a>Noteiktu gada beigās aizveriet veidnes
Pēc tam, kad sistēma ir konfigurēta, tuvu beigu procesa var palaist. Par **gada beigās slēgt** lapas veidni var definēt par juridiskajām personām, par kuru gada beigās slēgt procesā grupa darbosies. Veidnē tiks atkārtoti lietota katru gada beigās tuvu, bet var mainīt, mainot jūsu organizācijā. 

Vispirms definējiet **grupas nosaukumu** veidni, un atlasiet finanšu kalendārs. Grupas nosaukums ir jāidentificē juridiskām vienībām, kas iekļautas grupas.  Piemēram, veidnes var izveidot, pamatojoties uz ģeogrāfiju, ar atsevišķas grupas, kas izveidotas Ziemeļamerikas juridiskām vienībām, EMEA juridiskajām personām un APAC juridiskajām personām. 

Pēc tam juridiskās personas var pievienot veidni. Juridiskās personas var pievienot, izvēloties organizatorisko hierarhiju vai atlasot juridiskām personām. Ja atlasīta organizācijas hierarhijai, tikai juridiskās personas ietvaros hierarhijas, kas izmanto atlasīto finanšu kalendārs tiks pievienota veidne. Ja izmantojat juridiskajām personām, lai pievienotu veidni, var pievienot tikai juridiskas personas ar vienu un to pašu finanšu kalendārs. Vienu un to pašu finanšu kalendārs ir nepieciešama, jo tuvāk gada beigām vadīja izvēloties finanšu gada, kas var atšķirties no kalendāra uz kalendāru. 

Pēc juridiskās vienības, kas tiek pievienoti, noteikt nesadalītās peļņas galvenā uzskaite par katru juridisku personu. **Pagājušā gada beigu datums tuvu** lauks tiek atjaunināts katru reizi, gada beigās tuvu palaist juridiskajai personai. 

**Finanšu dimensijai** cilni izmanto, lai definētu finanšu dimensijas, kuras tiks izmantotas sākuma darbība. Ņemiet vērā, ka definējat iestatījumi attiecas tikai juridiskajai personai, kas atlasīts laukā **juridiskajām personām** režģi. Iestatījumiem tiks atkārtots par katra juridiska persona režģī. 

**Pārsūtītu bilances dimensijas** tiek izmantota, lai definētu, vai par darbībām, kas grāmatotas bilances kontos finanšu dimensijām būtu jāuztur tāda pastāvīgi atjaunināta sākuma darbība. Labākā prakse ir iestatiet šo opciju kā **Jā**. **Pārsūtīšanas operāciju dimensijām** tiek izmantota, lai definētu, kuras finanšu dimensijas par darbībām, kas grāmatotas peļņas un zaudējumu kontā tiks nodota nesadalītās peļņas galvenais konts. Pirmkārt, noteikt attiecīgās atlasītā juridiskajai personai finanšu dimensijas. Tas ietver visas finanšu dimensijas iegrāmatots atbilstoši gada laikā pat tad, ja finanšu dimensijas nav daļa no aktīvā konta struktūra. Nākamajā, definēt katrai dimensijai vai nu kā **tuvu vienu** vai **aizvērt visas**.  Pēc noklusējuma ir **aizvērt visas**, kas uztur oriģinālo finanšu dimensiju vērtības no iegrāmatotās darbības un izmanto tos par radot sākuma atlikumus uz nesadalītās peļņas kontu. Katra unikālā kombinācija finanšu dimensijas vērtības tiks izveidota atsevišķa nesadalītās peļņas sākuma atlikumu. Ja **tuvu vienu** ir atlasīta, visas darbības, kas grāmatotas ar finanšu dimensijai tiek apkopoti uz nesadalītās peļņas sākuma atlikuma laukā pēc ievadīts dimensijas vērtības **tuvu vienu**. Piemēram, pieņemsim, ka visas darbības finanšu gadam tika nosūtīti ar kontu struktūru galvenā konta - departaments. Finanšu nodaļas dimensijā veidnē **tuvu vienu** ir atlasīts un 100 ievadīto vērtību. Ja visas darbības, kas grāmatotas departamenti, 200, 300 un 400 kopējie ieņēmumi ir $100,000, viena sākuma atlikums tiks izveidots Retained peļņa - 100. Ja atlasāt **tuvu vienu** un atstājiet tukšu finanšu dimensijas vērtību, visus darījumus grāmato nesadalītajā peļņā ar šo dimensijas vērtību, kas ir tukša. 

Gada beigās ciešā procesā neievēro kontu struktūras. Tas ir tāpēc, ka kontu struktūras var mainīt visu finanšu gadu un ne vienmēr ir iespējams identificēt attiecīgo kontu struktūru sakarā ar šīm izmaiņām.  Veidojot sākuma darbības bilances būs jāpārceļ ar finanšu dimensijas kā noteikts gada beigās ciešā veidni. Sākuma atlikumu ierakstus varētu iekļaut finanšu dimensijas vairs tekošā konta struktūra un segmentu kombinācijām, kas vairs nav derīgi tekošā konta struktūrā. Ja jūsu organizācija vēlas izslēgt finanšu dimensijai, nesadalītās peļņas sākuma atlikumu, kas finanšu dimensijai jābūt **tuvu vienu** un atstāt tukšas dimensijas vērtību.

## <a name="run-the-year-end-close-process"></a>Palaist beigu tuvu procesa
Pēc gada beigās aizveriet veidnes tiek veidotas, beigu tuvu procesa ir uzsākta, izvēloties **palaist fiskālajā gadā** darbību rūtī. Atlasiet visas vai juridiskās personas, no kuras darbināt gada beigās aizveriet veidni apakškopu. Aizverot darbojas gada beigās pirmo reizi finanšu gadā, būs iespējams izvēlēties visas juridiskās vienības, lai izveidotu sākuma atlikumiem visām juridiskajām personām. Ja izmantojat gada beigās aizveriet atkal, jūs varat izvēlēties, lai palaistu procesu tikai juridiskām personām, par kurām regulēšanas ieraksti tika grāmatoti. 

Atlasiet finanšu gads, kas jūs vēlētos vadīt gada beigās ciešā process pret. Ja pastāv vairāk nekā viena slēguma periodu finanšu gada pēdējā perioda **perioda nosaukums** lauks būs pieejami tā, lai var izvēlēties kuru slēgšanas periodu pēc slēguma darījumu, ja iestatījums ir noteikts, lai veidotu slēgšanas darbību. 

Ievadiet dokumenta numuru, kas vai var nebūt vajadzīgi, atkarībā no iestatījumiem kopumā Virsgrāmatas parametri. Visām juridiskajām personām, apstrādei atlasītie gada beigās ciešā izmantos to pašu dokumenta numuru. Dokumenta numurs netiek ģenerēta, izmantojot numuru sērijas. Tas ir labākās prakses, lai ievadītu dokumenta numuru, pat tad, ja tas ir nepieciešams. Ievadot dokumenta numurs ir vieglāk atrast sākuma darbība jaunajā finanšu gadā. Ja nav ievadīts dokumenta numurs, dokumenta būs tukša sākuma darbības. 

Ja jūs vēlaties apgriezt tuvu iepriekšējā gada beigām atlasītajam finanšu gadam, kas **atsaukt iepriekšējo tuvu** uz **Jā**. Gada beigās tuvu būs atgriezeniska, bet process var vēlreiz palaist jebkurā laikā. Gada beigās klāt, atgriežot **pagājušā gada beigu datums tuvu** nebūs pieejama. 

Tuvu beigu procesa noklusējumus lai palaistu pakešuzdevumu režīmā. Tas ir labākās prakses, lai palaistu procesu pakešuzdevumu režīmā ļauj lietotājam atgriezties uz citām darbībām. Pēc gada beigām ciešā process ir pabeigts, **pagājušā gada beigu datums tuvu** tiks papildināta ar sesijas datumu.

Lai iegūtu papildinformāciju, skatiet [tuvu Virsgrāmatas perioda beigās](close-general-ledger-at-period-end.md).


