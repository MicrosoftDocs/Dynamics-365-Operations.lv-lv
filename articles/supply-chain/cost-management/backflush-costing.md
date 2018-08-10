---
title: "Atgriezeniska izmaksu aprēķināšana"
description: "Šajā tēmā tiek ieviests atgriezeniskas izmaksu aprēķināšanas jēdziens, kas tiek izmantots ražošanai Lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9fe717752da4c697cf0d896c0d40832330f0d118
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="backflush-costing"></a>Atgriezeniska izmaksu aprēķināšana

[!include [banner](../includes/banner.md)]

Šajā tēmā tiek ieviests atgriezeniskas izmaksu aprēķināšanas jēdziens, kas tiek izmantots ražošanai Lean manufacturing. 

Izmaksu aprēķināšana ražošanai Lean manufacturing ļauj ražošanas plūsmā izmantot izmaksu uzkrāšanas metodi, kas ir pazīstama kā atgriezeniska izmaksu aprēķināšana. Atgriezeniskas izmaksu aprēķināšanas metodes ietvaros izmantotie tiešie materiāli tiek uzkrāti ražošanas plūsmas nepabeigtā projekta (NP) izmaksu kontā. Tiek izmantota standarta izmaksu krājumu modeļu grupa. Preces, kas tiek saņemtas no ražošanas plūsmas, tiek atskaitītas no NP pēc standarta izmaksām. Galvenā atšķirība starp atgriezenisko izmaksu aprēķināšanu un standarta izmaksām ir tāda, ka atgriezeniskās izmaksu aprēķināšanas gadījumā novirzes netiek aprēķinātas atbilstoši Kanban vai pabeigtajām precēm. Tā vietā novirzes tiek aprēķinātas atbilstoši ražošanas plūsmām noteiktā periodā. Ar šo metodi tiek ieviesta patiesi racionāla koncepcija atskaišu veidošanai par materiālu patēriņu. Par specializēto izdoto materiālu daudzumu netiek ziņots Kanban vai ražošanas pasūtījumā. Tā vietā pilnas partijas vai materiālu apstrādes vienības tiek iekļautas ražošanas plūsmā. Pēc tam, kad partijas vai materiālu apstrādes vienības ir reģistrētas kā tukšas, tās tiek norādītas kā patērētas. Papildu patēriņu var izmantot atkarībā no [ražošanas plūsmas konfigurācijas](../production-control/lean-manufacturing-modeling-lean-organization.md). Pirms var izmantot papildu patēriņu, organizācijām jāsniedz iespēja izmantot materiālus ražošanas plūsmas NP ietvaros. Periodiskā atgriezeniskā izmaksu aprēķināšana nosaka NP faktisko vērtību līdz perioda beigām. Šī noteikšana pamatojas uz Kanban materiālu apstrādes vienībām un Kanban darba statusu. Atšķirības starp efektīvajām vērtībām un faktiskajām NP vērtībām pa izmaksu grupām un krājumiem tiek uzskaitītas un parādītas kā novirzes.

## <a name="configuring-backflush-costing"></a>Atgriezeniskas izmaksu aprēķināšanas konfigurēšana
Lai iespējotu izmaksu aprēķināšanu, ir jāizpilda šāda iestatīšana:

-   **Iestatiet NP kontus ražošanas uzdevumu grupai un ražošanas plūsmai.** NP konti ražošanas plūsmai ir norādīti ražošanas uzdevumu grupā. Atgriezeniskas izmaksu aprēķināšanas ražošanas plūsma aprēķina novirzes kā starpību starp NP vērtību pirms un pēc atgriezeniskās izmaksu aprēķināšanas veikšanas katrai ražošanas plūsmai. Tādēļ ieteicams izveidot NP kontu katrai ražošanas plūsmai.
-   **Piešķiriet izmaksu kategoriju resursu grupai.** Izmaksu kategorija ir jāpiešķir darba šūnas izpildes laika kategorijai. Lai noteiktu novirzes pēc aktivitātes, ir jāizveido izmaksu kategorija katrai darba šūnai. Izmaksu kategorijas iestatīšanai un daudzumam netiek ņemtas vērā izmaksu aprēķināšanā ražošanai lean manufacturing. Atgriezeniskajā izmaksu aprēķināšanā tiek ignorēti NP konti pa resursu grupām. Apakšuzņēmēju aktivitātēm nav nepieciešama izmaksu kategorija. Tā vietā tiek izmantota izmaksu grupa, kas ir piešķirta aktīvajam pakalpojumam.
-   **Piešķiriet izmaksu grupas.** Lai iespējotu izmaksu seguma segmentāciju ražošanas plūsmā, ir jāpiešķir izmaksu grupas pēc izmaksu grupas tipa:
    -   **Tiešo materiālu izmaksu grupa** — tiešajiem materiāliem ir nepieciešama izmaksu grupa, kas identificē materiālu kategoriju izmaksu aprēķināšanai. Šī izmaksu grupa sniedz iespēju iegūt apkopoto skatu par izmaksām, NP un novirzēm pēc tiešā materiāla.
    -   **Tiešo ražošanas izmaksu grupa** — tiešo ražošanas izmaksu grupa atspoguļo darba resursu tiešo izmaksu segumu ražošanas plūsmā. Šī izmaksu grupa sniedz iespēju iegūt apkopoto skatu par izmaksām, NP un novirzēm pēc tiešajām ražošanas izmaksām.
    -   **Netiešo izmaksu grupa** — netiešo izmaksu grupa ir vajadzīga, lai aprēķinātu netiešo izmaksu segumu ražošanas plūsmā. Šī izmaksu grupa sniedz iespēju iegūt apkopoto skatu par izmaksām, NP un novirzēm pēc netiešajām izmaksām.
    -   **Tiešo ārpakalpojumu izmaksu grupa** — izmaksu grupa pakalpojumiem sniedz iespēju iegūt apkopoto skatu par piešķirtajām izmaksām un NP un nosaka apakšuzņēmēju pakalpojumu izmaksu novirzes.
    -   **Izmaksu grupa pabeigtai precei** — pabeigtajai precei ir nepieciešama izmaksu grupa, kas identificē preču kategoriju izmaksu aprēķināšanai. Šī izmaksu grupa sniedz iespēju iegūt apkopoto skatu par izmaksām, NP un novirzēm pēc preču kategorijas. Preču standarta izmaksas tiek aprēķinātas, izmantojot izmaksu aprēķinu, kas ir balstīts uz materiālu komplektu (MK), kā arī uz ražošanas plūsmu un Kanban nosacījumiem vai maršrutu.

### <a name="costing-sheet"></a>Izmaksu aprēķina lapa

Izmaksu aprēķina lapa modelē uzņēmuma izmaksu struktūru un ir veidota pēc izmaksu grupām, lai klasificētu izmaksas. Izmaksu aprēķina lapai ir dažādas formas. Tā parāda izmaksu informāciju saskaņā ar struktūru, kura tajā izveidota. Izmaksu aprēķina lapā varat arī definēt formulu, kas tiek izmantota, lai aprēķinātu netiešās izmaksas. Aprēķina formulas pamatā var būt daudzums, svars, tilpums vai vērtība.

-   **Definējiet izmaksu novērtēšanas versiju.** Izmaksu novērtēšanas versijā uzņēmums definē, kā jāuztur izmaksas. Izmaksu novērtēšanas versijā var būt iekļauta standarta izmaksu ierakstu kopa vai plānoto izmaksu ierakstu kopa atkarībā no izmaksu novērtēšanas tipa, kas piešķirts cenu versijai. Izmaksu novērtēšanas versijai, kas tiek izmantota izmaksu aprēķināšanai ražošanai Lean manufacturing, jābūt balstītai uz standarta izmaksām.
-   **Piešķiriet izlaistajām precēm krājumu modeļu grupu.** Visas preces, kuras ir saistītas ar ražošanas plūsmu, ir jāpiešķir krājumu modeļu grupai, kas izmanto krājumu modeļu grupu **Standarta izmaksas**. Standarta izmaksas tiek uzturētas atbilstoši vietai un aktivizēšanas datumam. Preču šabloniem var atlasīt krājumu modeļu grupu, ja izmaksas tiek uzturētas atbilstoši variantam vai preces šablonam.
-   **Pēc definīcijas apakšuzņēmēju pakalpojumi ir neinventarizēti pakalpojumi.** Apakšuzņēmēju aktivitātēm nav krājumu modeļu grupas. Lai pareizi aprēķinātu izmaksas apakšuzņēmēja aktivitātei, jāpārliecinās, vai pakalpojuma aktivitāte pieder krājumu modeļu grupai, kurai krājuma ierobežojumi ir iestatīti kā **Uzkrātā prece = Aplams**.

Ražošanas produktu gadījumā izmaksu aprēķinam, kas balstās uz ražošanas plūsmu, ir nepieciešams, lai tiktu uzturētas standarta izmaksas pakalpojumiem, kas ir saistīti ar apakšuzņēmēju aktivitātēm. Izmaksu grupa, kas ir piešķirta pakalpojumiem, tiek izmantota, lai noteiktu apakšuzņēmēja aktivitātes izmaksu novirzes.

## <a name="cost-calculation-for-lean-manufacturing"></a>Izmaksu aprēķins ražošanai Lean manufacturing
Precēm, kas tiek piegādātas no ražošanas plūsmas, MK aprēķina pamatā jābūt maršruta versijai vai ražošanas plūsmai. MK aprēķins aprēķina preces izmaksas, kā arī saistīto sadalījumu pa resursiem un materiāliem, kas nepieciešami, lai izveidotu preci. Ieturējumi no NP konta ražošanas plūsmai tiek veikti, izmantojot preces sadalījumu pa krājumiem un izmaksu grupām.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Aprēķins, kas balstīts uz ražošanas plūsmu

Lean manufacturing programmatūrai Microsoft Dynamics 365 for Finance and Operations darbība ir neatkarīga no maršrutiem. Izmaksu aprēķinu precēm, kuras tiek piegādātas no ražošanas plūsmas, var balstīt uz attiecīgo ražošanas plūsmu. Pirms var veikt aprēķinu, jāizveido Kanban nosacījums, ar kuru tiek piegādāta prece no ražošanas plūsmas. Ja aprēķina datumā preci var piegādāt no vairākām ražošanas plūsmām tajā pašā vietā, varat atlasīt ražošanas plūsmu MK aprēķinam. Lapā **Noklusējuma ražošanas plūsma** varat konfigurēt noklusējuma ražošanas plūsmu katram krājumam. Ja vienam produktam tajā pašā ražošanas plūsmā, kas ir aktīva aprēķina datumā, pastāv vairāki Kanban nosacījumi, aprēķins atlasa pirmo Kanban nosacījumu, kas ir aktīvs attiecīgajam aprēķinam.

### <a name="calculation-that-is-based-on-the-route"></a>Aprēķins, kas balstīts uz maršrutu

Aprēķins, kas balstīts uz maršrutu, ir tikpat derīgs kā aprēķins, kas balstīts uz ražošanas plūsmu. Tomēr aprēķinā, kas balstīts uz maršrutu, nav izmantota izmaksu aprēķināšana Lean manufacturing funkcionalitātei. Maršrutam ir jāizmanto resursu pieprasījums resursu grupām. Lai izvairītos no sistemātiskām novirzēm, tam jāizmanto arī tās pašas darba šūnas vai vismaz tās pašas izmaksu kategorijas. Ir jāizvairās no izmaksu kategorijām iestatīšanai un daudzumam. Tās nepalīdz aprēķināt izmaksas detalizētākā sadalījumā nekā Lean manufacturing atgriezeniskā izmaksu aprēķināšana. Lai noteiktu, kura opcija (ražošanas plūsmas vai maršruta) ir jāizmanto izmaksu aprēķināšanai, ņemiet vērā izmaksu sadalījuma rezultātus. Versija, kas vairāk atbilst realitātei un rada mazāk noviržu kopumā, ir labākā izvēle. Lean manufacturing vidē, kur prece tiek piegādāta, izmantojot vienu ražošanas plūsmu un vienu Kanban nosacījumu, aprēķins, kas ir balstīts uz ražošanas plūsmu, iespējams, ir precīzāks. Precei, kuru var piegādāt, izmantojot ražošanu Lean manufacturing un ražošanas pasūtījumus tajā pašā vietā, vai kurai var būt vairākas ražošanas plūsmas vai vairāki Kanban nosacījumi tajā pašā plūsmā, aprēķins var būt precīzāks, ja tas balstīts uz maršruta versiju, kas ir īpaši veidota izmaksu aprēķinam, nevis ražošanai. Ražošanas plūsmas aprēķins jāizmanto, lai aprēķinātu preces, kas ietver apakšlīgumu slēgšanu. Programmatūrā Microsoft Dynamics 365 for Finance and Operations izmaksu modeļiem apakšlīgumu slēgšanai, izmantojot ražošanas pasūtījumus, un apakšlīgumu slēgšanai Lean manufacturing ietvaros tiek izmantotas divas dažādas pieejas. Lean manufacturing ievieš jaunu izmaksu grupas tipu **Tiešie ārpakalpojumi**, lai aprēķinātu apakšuzņēmēju pakalpojumus.

## <a name="material-consumption"></a>Materiālu patēriņš
Kad materiāli tiek patērēti no krājumiem uz NP, materiālu izmaksas tiek pievienotas NP atbilstoši faktiskajām standarta izmaksām attiecīgajai izmaksu grupai. Šī operācija notiek saskaņā ar šādiem nosacījumiem:

-   Kanban izejas plūsmas tiek grāmatotas Kanban izdošanas rindām, kuras atjaunina krājumus.
-   Ir pabeigti pārsūtīšanas darbi, kuri atjaunina krājumus izdodot, bet ne saņemot (materiālu pārsūtīšana no krājumiem uz NP).

## <a name="receiving-products-from-the-production-flow"></a>Preču saņemšana no ražošanas plūsmas
Preces tiek saņemtas no ražošanas plūsmas saskaņā ar šādiem nosacījumiem:

-   Ir pabeigti apstrādes darbi, kuriem vienumam **Atjaunināt krājumus saņemot** iestatīta opcija **Jā**.
-   Ir pabeigti pārsūtīšanas darbi, kuri atjaunina krājumus saņemot, bet kuriem vienumam **Atjaunināt krājumus izdodot** ir iestatīta opcija **Nē** (pārsūtīšana no NP uz krājumiem). Šī opcija ļauj saņemt jebkuras preces no ražošanas plūsmas neatkarīgi no MK un maršruta konfigurācijas. Process vienkārši seko fiziskajām plūsmām. Šī opcija ir īpaši piemērota blakusproduktu, līdzproduktu vai brāķa saņemšanai no ražošanas plūsmas un attiecīgi ražošanas plūsmas NP izmaksu bilances labošanai.

Preces, kas tiek saņemtas no ražošanas plūsmas, tiek atskaitītas no NP.

## <a name="products-in-wip"></a>Preces NP ietvaros
Programmatūrā Microsoft Dynamics 365 for Finance and Operations pieejamais Lean manufacturing NP modelis sniedz iespēju izmantot Kanban materiālu apstrādes vienības statusu, lai pārvaldītu materiālus, daļēji pabeigtās preces un pabeigtās preces, kas ir iekļauti NP.

-   **Piešķirts** — Kanban var būt patērēti materiāli, kuri ir uzskaitīti NP.
-   **Saņemts** — ja Kanban attiecas uz pēdējo aktivitāti, kurai vienumam **Atjaunināt krājumus saņemot** ir iestatīta opcija **Nē**, tas parāda tādas preces vai nepabeigtas preces pilnu materiālu apstrādes vienību, kas nav reģistrēta krājumos.

Ņemiet vērā, ka materiāli, kas iekļauti NP, nav redzami rīcībā esošo krājumu pārskatos. Tomēr tie ir redzami Kanban daudzuma pārskatos.

## <a name="consuming-products-in-wip"></a>Preču patēriņš NP ietvaros
Preces, kas iekļautas NP, tiek patērētas, kad tiek iztukšotas attiecīgās Kanban materiālu apstrādes vienības. Kanban iztukšošanas signāls neizveido aktīvu izmaksu aprēķināšanas darījumu, bet stāsies spēkā, palaižot nākamo atgriezenisko izmaksu aprēķināšanu. Iztukšotās Kanban materiālu apstrādes vienības vairs netiek uzskatītas par rīcībā esošām un tādēļ tiek aprēķinātas kā patērētas perioda ietvaros.

### <a name="automatic-empty-registration"></a>Automātiska iztukšošanas reģistrācija

Plānotiem vai notikumu Kanban signāliem var iestatīt automātisku iztukšošanas reģistrāciju Kanban nosacījumā:

-   **Pēc materiālu apstrādes vienību saņemšanas** — pēc noklusējuma plānotiem Kanban signāliem materiāli tiek deklarēti kā patērēti, kad ir pabeigts pēdējais Kanban darbs. Fiksēta daudzuma Kanban signāliem šo opciju ieteicams izmantot tikai attiecībā uz viena nodalījuma Kanban, jo tā atgriež karti uz pieprasījuma avotu ikreiz, kad Kanban tiek saņemts galamērķī.
-   **Pēc izcelsmes pieprasījuma reģistrēšanas** — šī opcija ir pieejama tikai notikumu Kanban un ir minēto Kanban signālu noklusējuma opcija. Saistībā ar NP šī opcija ir noderīga, lai nodrošinātu, ka NP ir attīrīti, jo Kanban signāli komponentiem NP ietvaros tiek automātiski iztukšoti un tādējādi patērēti no NP, kad ir sagatavots vecākelementa Kanban.

Visbeidzot, Kanban materiālu apstrādes vienības var piešķirt (= nepabeigts), saņemt (= pilns) vai iztukšot. Netiek veikta daļēja iztukšošana. Tādēļ, lai iespējotu precīzu patēriņa reģistrāciju, ir svarīgi ierobežot Kanban preces daudzumu, lai tas būtu mazākas nekā patēriņš perioda ietvaros. Preces, kas tiek pārvietotas uz ražotni lielās partijās, kas aptver vairāku dienu vai nedēļu pieprasījuma apjomu, nevar patērēt NP. Tā vietā šīs preces ir jāglabā krājumos.

## <a name="backflush-costing"></a>Atgriezeniska izmaksu aprēķināšana
Atgriezeniskā izmaksu aprēķināšana jāveic, lai periodiski novērtētu NP un izveidotu perioda beigu statusu, kas aprēķina materiālu, darbaspēka un netiešo izmaksu novirzes. Aprēķinātās novirzes tiek grāmatotas noviržu kontos. Atgriezeniskās izmaksu aprēķināšanas procesā visas juridisko personu ražošanas plūsmas tiek izmantotas vienā pakešuzdevumā. Palaižot atgriezenisko izmaksu aprēķināšanu kā pakešuzdevumu, ražošanas plūsma var veikt apstrādi, sadalot vairākos pavedienos. Atgriezenisko periodu nosaka pēc beigu datuma. Nevar grāmatot jaunus darījumus datumā, kad ir izpildīta atgriezeniskā izmaksu aprēķināšana. Nedrīkst izpildīt atgriezenisko izmaksu aprēķināšanu pašreizējam datumam, pirms diena ir beigusies. Atgriezeniskā izmaksu aprēķināšana veic tālāk norādītās darbības.

1.  Nosakiet neizmantoto daudzumu ražošanas plūsmā perioda beigu datumā. Pēc tam, kad tiek palaista atgriezeniskā izmaksu aprēķināšana, varat skatīt neizmantoto daudzumu izpildītās izmaksu aprēķināšanas datumā dialoglodziņā **Neizmantotais daudzums**.
2.  Aprēķiniet ražošanas plūsmas neto realizēto lietojumu perioda ietvaros.
3.  Attīriet NP no realizēto resursu patēriņa un precēm.
4.  Aprēķiniet ražošanas standarta izmaksu novirzes attiecīgajā periodā. **Perioda ietvaros patērētajiem komponentiem:**
    -   Finansiāli atjauniniet neto realizēto materiālu daudzumu, kas patērēts ražošanas plūsmā perioda ietvaros. Sistēma veic apstrādi, izmantojot secību “pirmais iekšā, pirmais ārā” (first in, first out — FIFO) atsevišķiem krājumu darījumiem, lai finansiāli atjauninātu fiziski atjauninātus darījumus attiecīgajai ražošanas plūsmai, līdz tiek sasniegts neto realizētais daudzums periodā.
    -   Darījumi ir finansiāli sadalīti, lai kartētu precīzu patērēto daudzumu.
    -   Neizmantotais daudzums ražošanas plūsmas NP paliek fiziski atjauninātā statusā.

    **Perioda ietvaros ražošanas pabeigtajam daudzumam:**
    -   Finansiāli atjauniniet krājumu darījumus pabeigtajam daudzumam perioda ietvaros.

    **Konvertēšanas izmaksām:**
    -   Lietotie konvertēšanas izmaksu darījumi (maršruta darījumi), kas reģistrēti attiecīgajā periodā, tiek finansiāli atjaunināti.
    -   Visas tiešās ražošanas izmaksas tiek finansiāli atjauninātas. Visi Kanban procesa darbi, kas pabeigti attiecīgajā periodā, tiek uzkrāti.
    -   Visas netiešās izmaksas, kas aprēķinātas par patērētajiem materiāliem perioda ietvaros, tiek aprēķinātas un atskaitītas no NP. Atlikušās netiešās izmaksas tiek grāmatotas kā novirze.

5.  Aprēķiniet ražošanas standarta izmaksu novirzes. Novirze tiek aprēķināta pa izmaksu grupām.






