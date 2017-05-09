---
title: Operations resursi
description: "Operācijas resursi izpilda projekta vai ražošanas procesa aktivitātes. Tie var būt dažādu veidu, ar dažādām iespējām."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f77fe37933854d66c35a4a14e6dfb6db398eb034
ms.lasthandoff: 03/31/2017


---

# <a name="operations-resources"></a>Operations resursi

[!include[banner](../includes/banner.md)]


Operācijas resursi izpilda projekta vai ražošanas procesa aktivitātes. Tie var būt dažādu veidu, ar dažādām iespējām. 

<a name="operations-resources"></a>Operations resursi
--------------------

Operācijas resursi ir iekārtas, rīki, darbinieki, iekārtas, fiziski apgabali vai kreditori, kas veic projekta darbības vai ražošanas procesa darbības. Tie var būt dažādu veidu, ar dažādām iespējām.

-   **Kreditors** — ārējais resurss, kas izpilda projekta vai ražošanas procesa darbības. Piemērs ir apakšuzņēmējs. Piesaistot kreditoru resursus kreditora kontam, varat ģenerēt apakšuzņēmējiem pirkumus, pamatojoties uz materiālu komplekta (MK) rindām vai ražošanas rindām.
-   **Personāla vadība** — projektu vai ražošanas darbinieks, kas veic darbību individuāli vai kā instrumenta vai mašīnas operators. Ja izmantojat personāla vadības funkcionalitāti, varat saistīt darbaspēku ar darbinieku. Pēc tam plānošanas programma var piešķirt resursus, pamatojoties uz zināšanām, kas definētas attiecīgajam darbiniekam.
-   **Iekārta** — iekārta vai cits ražošanas aprīkojums, kas nepieciešams ražošanai.
-   **Rīks** — instruments vai ierīce, ko parasti lieto kopā ar citu resursu, lai veiktu darbību projektā vai ražošanā.
-   **Atrašanās vieta** — tā specifiskā izmēra fiziskā atrašanās vieta, kas nepieciešams, lai veiktu darbību. Piemērs ir komplektēšanas zona.
-   **Iestāde** — ēka vai fiksēta struktūra, kas nepieciešams, lai veiktu darbību.

## <a name="calendars"></a>Kalendāri
Kalendāru var piešķirt operācijas resursiem; tas apraksta šī resursa ražīgumu (stundās). Operācijas resursu darba laiku nosaka pēc kalendāra, kas piešķirts tai resursu grupai, kuras daļa ir operācijas jeb darbības resursi. Varat iestatīt piešķirta kalendāra spēkā stāšanās datumu un beigu datumu. Pēc tam operācijas resursiem varat pievienot vismaz vairākus kalendārus. Tomēr piešķirto kalendāru datumi nedrīkst pārklāties, un operācijas resursus vienlaikus var piešķirt tikai vienam kalendāram. **Piezīme.** Ja nepastāv spēkā esošu darba kalendāru resursu grupai, piemēram, ja pēdējā piešķirtā kalendāra vai vienīgā piešķirtā kalendāra derīgums beidzies, jūs vairs nevarat piekļūt resursiem, kas piešķirti resursu grupai ražošanas plānošanas un operāciju plānošanas nolūkos. Varat arī piešķirt kalendāru resursu grupai, lai norādītu darba laikus resursu grupai un visiem darbības veikšanas resursiem, kas piešķirti resursu grupai. Resursu grupas noslodze tiek aprēķināta kā katras darbības veikšanas resursu noslodzes summa. Resursu grupai piešķirtais kalendārs ar laiku var mainīties.

## <a name="resource-capabilities"></a>Resursu iespējas
Iespēja ir operācijas resursa pieejamība konkrētas aktivitātes izpildīšanai. Pēc tam operācijas resursiem varat pievienot vismaz vairākas iespējas. Plānošanas programma tad piešķirs resursus, saskaņojot katras darbības resursu pieprasījumus ar pieejamo darbību veikšanas resursu iespējām. Iespējas var piešķirt visu veidu resursiem (**rīkam**, **kreditoram**, **iekārtai**, **cilvēkresursiem**, **novietojumam**, vai **iestādei**). Lai piešķirtu iespējas operācijas resursiem uz noteiktu laiku, definējiet iespēju piešķiršanas sākuma un beigu datumu. Plašāku informāciju skatiet sadaļā [Resursu iespējas](resource-capabilities.md).

## <a name="resource-groups"></a>Resursu grupas
Resursu grupa ir darbību veikšanas resursu kopa, kas pārstāv granularitāti, kādā vēlaties plānot resursus, ja izmantojat darbību veikšanas plānošanas metodi. Tādēļ resursu grupas parasti atbilst darba šūnu fiziskajai organizācijai, kuras ražotnē ir norādītas ar dzeltenām līnijām. Resursu grupa nosaka vietu, ražošanas vienību un noliktavas kontekstu grupai piešķirtajiem darbību veikšanas resursiem. Piešķirot darbības veikšanas resursus resursu grupai, resursus var plānot tikai tajā vietā, kur šī resursu grupa atrodas. Izveidotie darbību veikšanas resursi jums nav jāpiešķir resursu grupai. Tomēr pirms resursu grupas plānošanas darba veikšanai darbību veikšanas resursi ir jāpiešķir resursu grupai. Operācijas resursus uz ierobežotu laiku var piešķirt resursu grupai. Varat piešķirt operācijas resursus arī vairākām resursu grupām, lai varētu koplietot resursus vietnēs. Tomēr spēkā stāšanās datumi un beigu datumi nedrīkst pārklāties. Citiem vārdiem sakot, nevar vienlaikus piešķirt operācijas resursus divām resursu grupām. Resursu grupas piešķires izmaiņas stājas spēkā tikai jauniem resursu sadalījumiem. Noslodzes rezervācijas darbiem, darbībām un projekta stundu prognozēm, kas jau ir ieplānotas, netiks ietekmētas. **Piezīme.** Piešķirot **kreditora** operācijas grupas resursu grupai, visiem operācijas resursiem, kas piešķirti resursu grupai, jāatbilst **kreditora** grupai un jāpiesaista tam pašam kreditora kontam.

## <a name="production-units"></a>Ražošanas vienības
Ražošanas vienība ir administratīva vienība, kas ir resursu grupu kolekcija. Ražošanas vienība var saturēt vairākas resursu grupas, bet resursu grupu var piešķirt tikai vienai ražošanas vienībai. Ražošanas vienība parāda ražošanas resursu fizisko izkārtojumu, un tā neietekmē darbības vai to, kā tās tiek apstrādātas. Ražošanas vienība ir jāsaista ar vietu. Ražošanas vienībai varat piešķirt arī izdošanas noliktavu un glabāšanas noliktavu. Varat izmantot ražošanas vienību, lai konsolidētu un filtrētu ar ražošanu saistītos datus. Piemēram, ražotnes pārvaldnieks var skatīt pārskatu par konkrētas ražošanas vienības neizpildīto darba noslodzi un pieejamo noslodzi. Varat mainīt ražošanas vienību, kas piešķirta resursu grupai. Varat arī izdzēst ražošanas vienību. Tomēr šīs ražošanas vienības izmaiņas ir efektīvas tikai jaunajiem pasūtījumiem, kas ir izveidoti pēc vispārējās plānošanas izpildes. Ja vēlaties lietot ražošanas vienības izmaiņas esošajiem pasūtījumiem, tas jādara manuāli.

## <a name="resource-scheduling"></a>Resursu plānošana
Operācijas resursi tiek piešķirti darbībām, ieplānojot projektu vai ražošanu. Ir pieejamas divas plānošanas metodes: operāciju plānošana un darbu plānošana. Izmantojot darbību veikšanas plānošanu, katra darbības veikšana vai projekta darbība tiek ieplānota resursu grupā, kurā ir darbības veikšanas resursi atbilstoši darbības veikšanai norādītajām resursu prasībām. Ja darbībai nepieciešami noteikti operācijas resursi, plānošana rezervē noslodzi tikai noteiktām resursu grupas operācijām. Darbu plānošana ir daudz detalizētāka plānošanas forma par operāciju plānošanu. Tā sadala katru darbību tās atsevišķajos uzdevumos un darbos. Šie darbi pēc tam tiek piešķirti operācijas resursiem, kas tos veiks. Plānošana rezervē noslodzi resursu grupās, pamatojoties uz darbības laikiem, kas definēti ražošanas maršrutā vai projekta darbībās. Ja strādājat ar ierobežotu noslodzi, grafiks būs atkarīgs no tiem pieejamajiem operācijas resursiem, kas nepieciešami darbības veikšanai. Darbību veikšanas plānošanai resursu grupas noslodze ir pieejamās darbības veikšanas resursu summa, kas ir daļa no šīs grupas. Noslodzes rezervācijas, kas jau pastāv darbību veikšanas resursiem, tiek uzskatītas par nepieejamu noslodzi. Ja nav pietiekami daudz pieejamās noslodzes ražošanai, ražošanas pasūtījumus var aizkavēt vai pat apturēt. Lapā **Resursi **var definēt vairākus rekvizītus, kas kontrolē, kā tiek veiktas noslodzes rezervācijas:

-   **Noslodze** — norādiet operācijas resursu noslodzi stundā attiecībā uz noslodzes mērvienību.
-   **Paketes noslodze** — norādiet maksimālo gabalu daudzumu, ko operācijas resursi var vienlaikus apstrādāt.
-   **Efektivitātes procenti** — norādiet efektivitāti, kādu sagaidāt no šiem operācijas resursiem. Efektivitātes procenti pielāgo darbību veikšanas resursu caurlaidi un ietekmē resursiem rezervēto laiku. Tiek atbilstoši pielāgoti arī darbību veikšanas, kurās izmantoti darbību veikšanas resursi, izpildes laiki. Aprēķināšanai tiek izmantota šāda formula: plānošanas laiks = laiks × 100 ÷ efektivitātes procenti. Šajā formulā *Laiks* ietver gan izpildes laiku, gan iestatīšanas laiku.
-   **Operāciju plānošanas procenti** — norādiet maksimālo noslodzes procentuālo daudzumu tam operācijas resursam, kuru vēlaties izmantot operāciju plānošanā. Lai, plānojot darbu, ļautu pielāgot noslodzi, šī procentuālā vērtība jāiestata mazāk par 100 procentiem.
-   **Ierobežota noslodze** — iestatiet šo opciju kā **Jā**, ja operācijas resurss ir jāplāno, pamatojoties uz faktiski pieejamo noslodzi, un ja ir jāņem vērā esošās noslodzes rezervācijas. Ja šī opcija ir iestatīta uz **Nē**, tad tiek pieņemts, ka operācijas resursam ir neierobežotā noslodze un resursam var tikt pārsniegta rezervācija.
-   **Ierobežoti rekvizīti** — iestatiet šo opciju kā **Jā**, ja operācijas resurss jāplāno, pamatojoties uz faktisko noslodzi, kas ir pieejama, ņemot vērā nepieciešamos darba laika plānošanas rekvizītus.
-   **Ekskluzīvi** — iestatiet šo opciju kā **Jā**, ja nenevēlaties, lai operācijas resurss būs pieejams citam darbam vai operācijai, līdz pašreizējā produkcija ir pabeigta. Šādā gadījumā tas nozīmē, ka darbību veikšanas resursu nevar izmantot, pat ja resursa darbības laikā ir pārtraukumi.
-   **Deficīta resurss** —definējiet operāciju resursu kā deficīta resursu. Deficīta resurss tiek plānots, izmantojot ierobežotu noslodzi, atlasot opciju **Ierobežota noslodze** un **Deficīta plānošana** lapā **Vispārējie plāni**.

Lai plānotu vairākus darbību veikšanas resursus vienlaikus, piemēram, darbību veikšanai ražošanā, ir jānorāda prasības attiecībā uz dažādiem resursiem, izmantojot primārās un sekundārās darbības. Pēc tam var arī rezervēt vairākus operācijas resursus, kuriem ir dažāda noslodze. Darbību veikšanas resursi, kas paredzēti primārai darbības izpildei, nosaka darbības ilgumu.

## <a name="lean-work-cells"></a>Racionālās darba šūnas
Varat norādīt, ka resursu grupa ir racionālā darba šūna. Pēc tam resursu grupu var iekļaut ražošanas plūsmā. Norādot resursu grupu kā racionālu darba šūnu, netiek arī pieļauta resursu grupas un piešķirto darbību veikšanas resursu iedalīšana ražošanas pasūtījuma darbībām vai projekta stundu budžeta darbībām. Katrai resursu grupai, kas darbojas kā racionāla darba šūna, jānorāda šāda informācija.

-   **Kalendārs** — darba šūnas darba kalendārs, kurā jābūt standarta darba dienas rekvizītam.
-   **Ievades noliktava un novietojums** — noklusējuma atrašanās vieta, ko izmanto materiālu paņemšanai, lai veiktu darbību.
-   **Izstrādes noliktava un novietojums** — noklusējuma atrašanās vieta, kur ievieto visu darba šūnas izstrādi.
-   **Izpildlaika izmaksu kategorija** — šī kategorija jādefinē darba šūnai, ja tiek izsekotas tiešās darbaspēka izmaksas.

Ja resursu grupa tiek lietota kā racionāla darba šūna, darba šūnas noslodze tiek norādīta tieši resursu grupā. Tādēļ resursu grupai nav jāpiešķir operācijas resursi. **Piegādātāja** darbību veikšanas resursu veids darba šūnai jāpiešķir tikai tad, ja darba šūnu pārvalda apakšuzņēmējs. Ja darbību veikšanas resursu piešķir resursu grupai, kas ir atzīmēta kā darba šūna, darba šūnas noslodze netiek ietekmēta.

## <a name="costing-resources"></a>Izmaksu aprēķināšanas resursi
Definējot aktivitāti, piemēram, maršruta operāciju vai projekta stundu budžetu, varat norādīt prasību pēc noteikta darbības veikšanas resursa vai resursu grupas. Tomēr ir iespējams norādīt arī prasību pēc noteikta darbību veikšanas resursa veida vai darbību veikšanas resursa, kam ir konkrētas prasmes vai kompetence. Šī iemesla dēļ faktiska resursu piešķire netiek veikta līdz brīdim, kad ieplānota aktivitāte un ir rezervēta noslodze. Tāpēc maršruta operācijā var norādīt, ka novērtēšana un MK aprēķini jāveic, izmantojot konkrētu darbību veikšanas resursu. Šo darbību veikšanas resursu dēvē par izmaksu aprēķināšanas resursu. Varat arī pārsūtīt izmaksu kategorijas un darbības veikšanas laikus no izmaksu aprēķināšanas resursiem uz aktivitāti. Kad darbības veikšana ieplānota, novērtēšana un MK aprēķins tiek veikts, izmantojot faktiski ieplānotos darbību veikšanas resursus.




