---
title: "Standarta izmaksu pārveidošanas apskats"
description: "Šajā rakstā ir sniegts procesa pārskats, kas palīdz iestatīt un palaist standarta izmaksu pārveidošanas procesu. Norādītās darbības ir jāveic pēc tam, kad ir pilnībā izpildīti standarta izmaksu pārveidošanas priekšnoteikumi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6e223c2d9a683d7b92b73d3fe3d3c8b22684d22c
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="standard-cost-conversion-overview"></a>Standarta izmaksu pārveidošanas apskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts procesa pārskats, kas palīdz iestatīt un palaist standarta izmaksu pārveidošanas procesu. Norādītās darbības ir jāveic pēc tam, kad ir pilnībā izpildīti standarta izmaksu pārveidošanas priekšnoteikumi. 

Izmantojiet lapu **Standarta izmaksu pārveidošanas**, lai pārvērstu atlasīto krājumu partijas krājumu modeli no faktiskās izmaksu pieejas uz standarta izmaksu pieeju. Pārvēršanas process ietver nepieciešamo krājumu slēgšanu, vairākas darbības pārejas periodā, ko nosaka pārejas sākuma datums un plānotais pārvēršanas datums, un pēc tam pārvēršanu un ar to saistīto krājumu slēgšanu.

-   Krājumu slēgšana pirms pārejas perioda — krājumu slēgšana attiecas nepieciešamu darbību, jo tā nosedz krājuma atvērtās transakcijas, izmantojot veco vērtēšanas metodi. Pārejas perioda laikā var ievadīt un iegrāmatot ar iepriekšēju datumu veiktas transakcijas, piemēram, rēķinus, lai var aizvērt iepriekšējo periodu. Krājumu slēgšanas datumam jābūt vienu dienu pirms pārejas sākuma datuma, lai nodrošinātu pilnīgu vecās novērtēšanas metodes izmantošanas pārtraukšanu.
-   Pārvēršanas darbības pārejas periodā — izmantojiet lapu **Standarta izmaksu pārveidošanas**, lai izveidotu pārvēršanas ierakstu, kas ietver arī lietotāja noteiktu jaunās izmaksu versijas identifikatoru. Identificējiet krājumus, kuriem nepieciešama pārvēršana, un pēc tam ievadiet krājumu neapstiprinātās standarta izmaksas jaunajā izmaksu aprēķināšanas versijā. Veiciet atlasīto krājumu pārbaudi, lai noteiktu problēmas, kas var kavēt pārvēršanu, novērsiet problēmas un pēc tam veiciet citas pārbaudes. Kad šie krājumi pārbaudīti un problēmas netiek konstatētas, mainiet pārvēršanas ieraksta statusu **Gatavs**. Plānotajā pārvēršanas datumā veiciet pārvēršanu un pēc izvēles iekļaujiet krājumu slēgšanu. Krājuma vienību kustības transakcijas pārejas perioda laikā tiek iegrāmatotas un novērtētas saskaņā ar veco krājumu modeli. Kad pārvēršana ir sekmīgi pabeigta, krājumu kustības transakcijas tiek vēlreiz novērtētas pret standarta izmaksām.
-   Krājuma slēgšana pirms pārvēršanas — krājuma slēgšanu var iekļaut pārvēršanā plānotajā pārvēršanas datumā veiktajā vai arī to var veikt pirms pārvēršanas kā atsevišķu darbību.

Kad pārvēršanas process ir sekmīgi pabeigts, katra krājuma modeļa pamatā ir standarta izmaksas un tiek iespējotas krājuma standarta izmaksas. Nākamās krājumu transakcijas tiek novērtētas pēc krājuma standarta izmaksām. Papildus sistēma pārvērš krājuma fiziskā krājuma saņemšanas un izsniegšanas transakcijas uz standarta izmaksām saskaņā ar pārvēršanas datumu. Sistēma pārvērš arī krājuma finansiālo rīcībā esošo krājumu uz standarta izmaksām un iegrāmato vērtības starpību kā krājuma pārvērtēšanu. Visas transakcijas, kas tiek veiktas pēc pārvēršanas, tiek vērtētas pēc krājuma standarta izmaksām. Jūs nevarat ievadīt ar iepriekšēju datumu veiktas darbības pirms pārvēršanas datuma, jo ir jāveic krājuma slēgšana vienu dienu pirms pārvēršanas datuma. Pārvēršanu var veikt tikai tad, ja ir veikta krājuma slēgšana vienu dienu iepriekš. Krājuma slēgšanu nevar atcelt.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Definējiet standarta izmaksu pārveidošanas ierakstu un saistīto cenu versiju
Lai izveidotu pārvēršanas ierakstu, izmantojiet lapu **Standarta izmaksu pārvēršanas**. Jaunu pārveidošanas ierakstu var izveidot tikai tad, kad esošie pārveidošanas ieraksti ir pabeigti. Plānotā pārejas perioda ilgumu nosaka ar pārejas sākuma datumu un plānoto pārveidošanas datumu. Plānotais pārejas periods var būt vienu dienu garš. Plānotais pārejas periods palīdz nodrošināt, ka pārveidošanas procesā ir pietiekami daudz laika, lai varētu pabeigt visas tā darbības. Krājumu slēgšana jāveic datumā, kas ir vienu dienu pirms pārejas perioda sākuma datuma, lai nodrošinātu, ka nosegtās transakcijas ir pabeigtas pirms tiek sākts pārveidošanas process. Lai pārbaudītu, vai transakcijas sākuma datums un krājuma slēgšanas datums ir pareizi saskaņots, var vai nu mainīt pārejas sākuma datumu vienu dienu pēc esošā krājuma slēgšanas, vai arī veikt krājuma slēgšanu. Ievadot pārveidošanas ierakstu, ir jāievada arī lietotāja noteiktais jaunās izmaksu aprēķināšanas versijas identifikators, kas ietver pārveidoto krājumu standarta izmaksas. Izmaksu aprēķināšanas versija tie izveidota automātiski, saglabājot pārvēršanas ierakstu.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Pārskatiet un mainiet jauno pārveidošanas ieraksta izmaksu aprēķināšanas versiju
Jaunā izmaksu aprēķināšanas versija tiek piešķirta pārveidošanas ierakstam, kā norāda izmaksu aprēķināšanas veids **Pārvēršana**. Piešķirtā izmaksu aprēķināšanas versija ir līdzīga standarta izmaksu aprēķināšanas versijai, un tā ietves krājuma izmaksu ierakstus krājumiem, kas ir saistīti ar pārveidošanas ierakstu. Piešķirtai pārveidošanas ieraksta izmaksu aprēķināšanas versijai ir pieejami tālāk norādītie iestatījumi, kas, ja nepieciešams, ir jāpārskata un jāmaina dažādās cilnēs.

-   **Izmaksu novērtēšanas veids:** šim laukam ir jāiestata opcija **Standarta izmaksas**.
-   **Versija:** identifikators norāda datus, kas ir ievadīti izmaksu aprēķināšanas versijas ID pārveidošanas ierakstā.
-   **Nosaukums:** nosaukuma lauks pēc noklusējuma ir tukšs. Ja nepieciešams, nosaukumu var ievadīt.
-   **Bloķēt:** šim laukam jāiestata opcija **Nē**. Izmaksu aprēķināšanas versijas laukā var ievadīt izmaksu ierakstus, līdz tiek mainīts pārveidošanas ieraksta statuss **Gatavs**. Statuss **Gatavs** norāda, ka atlasītie krājumi ir pārbaudīti, un ka nedrīkst atļaut mainīt izmaksu ierakstus.
-   **Bloķēt aktivizāciju:** šim laukam jāiestata opcija **Jā**. Piešķirtajā izmaksu aprēķināšanas versijā neapstiprinātos izmaksu ierakstus nevar manuāli aktivizēt. Aktivizācija notiek tad, kad tiek veikta pārveidošana.
-   **No datuma:** šis datums norāda plānoto pārveidošanas datumu, kas ir ievadīts pārveidošanas ierakstā.
-   **Vieta:** atstājiet lauku tukšu tā, lai izmaksu ierakstus var ievadīt visām vietām.
-   **Atļaut cenas veida lauku grupu:** iestatiet šī lauka opciju **Jā**, tādējādi ļaujot ievadīt tikai izmaksu cenu ierakstus.
-   **Regresa princips:** šim laukam jāiestata opcija **Nav**. Mainiet regresa principa statusu **Aktīvs**, ja nepieciešami izmaksu dati, kas ir aktivizēti citās izmaksu aprēķināšanas versijās. Piemēram, lai aprēķinātu saražoto krājumu izmaksas, iespējams, ka ir nepieciešama informācija par komponentiem, izmaksu kategorijām un netiešajām izmaksām.
-   **Regresa izmaksu aprēķināšanas versija:** atstājiet šo lauku tukšu.

Krājuma izmaksu datus piešķirtajā izmaksu aprēķināšanas versijā var uzturēt, tikai izmantojot lapu **Standarta izmaksu pārveidošanas**. Lapu **Izmaksu aprēķināšanas versijas iestatīšana** vai **Izmaksu aprēķināšanas versijas uzturēšana** nevarat izmantot, lai aprēķinātu izmaksu aprēķināšanas versijas izmaksas pārvēršanas laikā. Taču šīs lapas var izmantot, lai uzturētu piešķirto izmaksu aprēķināšanas versiju, kad ir pabeigts pārveidošanas process.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Norādiet uz standarta izmaksām pārveidojamos krājumus
Izmantojiet lapu**Standarta izmaksu pārvēršanas**, lai norādītu atsevišķus krājumus, kas jāpārvērš uz standarta izmaksām. Izmantojot lapu **Pievienot krājumus pārveidošanai uz standarta izmaksām**, var pievienot vairākus krājumus. Lai nodrošinātu pareizu izmaksu aprēķināšanu, visi ražotie krājumi jāiekļauj vienā pārveidošanas ierakstā.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Ievadiet vai aprēķiniet katra pārveidotā krājuma neapstiprinātās standarta izmaksas
Izmantojiet lapu **Krājuma cena**, lai ievadītu neapstiprinātās standarta izmaksas pirkšanas un pārsūtīšanas krājumu piešķirtajā izmaksu aprēķināšanas versijā. Izmaksu ieraksti ir raksturīgi vietai, un krājuma nenokārtotās izmaksas ir jāievada no katras vietas. Izmantojiet lapu **Krājuma cena**, lai aprēķinātu saražoto krājumu neapstiprinātās standarta izmaksas. Saražotā krājuma neapstiprinātās izmaksas ir jāaprēķina katrai ražošanas vietai, ja vien vieta nav arī pārsūtīšanas vieta. Šajā gadījumā neapstiprinātās izmaksas jāievada manuāli. Dažiem krājumiem var būt norādīta krāsas, izmēra vai konfigurācijas dimensija. Lapā **Standarta izmaksu pārvēršanas** izvēles rūtiņa **Izmantot izmaksu cenu pēc varianta** norāda katras preču dimensijas kombinācijas standarta izmaksas. Ja šīs izvēles rūtiņas atlase ir noņemta, ir jāievada tikai krājuma neapstiprinātās izmaksas.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Pārbaudiet un novērsiet jebkādas problēmas, kas saistītas ar pārveidojamiem krājumiem
Izmantojiet pārskatu**Standarta izmaksu pārveidošanas pārbaudes**, lai noskaidrotu problēmas, kas saistās ar pārveidojamiem krājumiem. Ja uz krājumu neattiecas nekādas problēmas, pārveidošanas ierakstā tiek nomainīts tā statuss **Pārbaudīts**. Ja uz krājumu attiecas problēmas, tās ir jānovērš un pēc tam vēlreiz jāpalaiž pārskata sagatavošana, līdz tiek mainīts krājuma statuss **Pārbaudīts**. Ja ar krājumu saistīto problēmu nevar savlaicīgi novērst, šo krājumu var dzēst pārveidošanas ierakstā un pēc tam pārveidot krājumu vēlāk.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Mainiet pārveidošanas ieraksta statusu uz Gatavs
Kad ir mainīts pārveidošanas ieraksta statuss **Gatavs**, pirms standarta izmaksu pārveidošanas palaišanas sistēma veic galīgo pārbaudi. Statuss **Gatavs** tiek mainīts tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.

-   Visu krājumu pārveidošanas ierakstā statuss ir **Pārbaudīts**.
-   Krājumu slēgšanai ir veikta vienu dienu pirms pārejas perioda sākuma datuma. Lai pārbaudītu, vai transakcijas sākuma datums un krājuma slēgšanas datums ir pareizi saskaņots, var vai nu mainīt pārejas sākuma datumu vienu dienu pēc esošā krājuma slēgšanas, vai arī veikt krājuma slēgšanu.

## <a name="7-back-up-the-database-before-conversion"></a>7. Dublējiet datu bāzi pirms pārveidošanas
Dublējums ļauj atjaunot datu bāzi, ja pārveidošanas procesa laikā rodas kļūdas.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Veiciet pārveidošanas procesu, kad pārveidošanas ieraksta statuss ir Gatavs
Pārveidošanas process pieprasa, lai vienu dienu pirms plānotā pārveidošanas datuma ir veikta krājumu slēgšana. Šī prasība nodrošina, ka pārejas periodā nevar ievadīt transakcijas ar atpakaļejošu datumu. Ja krājumu slēgšana nav veikta, sistēmā tiek parādīts ziņojums ar jautājumu, vai vēlaties to veikt pārveidošanas procesa laikā. Pārveidošanas procesā vienlaicīgi tiek apstrādāts viens krājums. Tas tiek sākts ar preču struktūras zemākā līmeņa krājumiem atbilstoši krājuma zema līmeņa kodam. Kad krājums ir sekmīgi pārveidots, pārveidošanas ierakstā tiek nomainīts tā statuss **Pārveidots**. Ja pārveidošanas process tiek pārtraukts, visu krājumu, kas nav sekmīgi pārveidoti, statuss joprojām ir **Pārbaudīts**. Sekmīgas pārveidošanas procesa pabeigšana rada tālāk aprakstītos rezultātus.

-   Pārveidošanas ieraksta statuss **Gatavs** tiek mainīts uz **Pabeigts**, un visu atlasīto krājumu statuss **Pārbaudīts** tiek mainīts uz **Pārveidots**.
-   Pārveidotā krājuma modeļa grupa tiek mainīta tā, ka tā norāda jaunu grupu, uz kuru attiecas standarta izmaksu krājumu modelis.
-   Pārveidoto krājumu standarta izmaksas tiek iespējotas piešķirtajā izmaksu aprēķināšanas versijā.
-   Izmaksu aprēķināšanas versijas izmaksu aprēķināšanas veids **Pārveidošana** tiek mainīts uz **Standarta izmaksas**, un izmaksu aprēķināšanas versija tagad ir tāda pati kā citas standarta izmaksām paredzētās izmaksu aprēķināšanas versijas.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Apstipriniet un saskaņojiet pārveidoto krājumu vērtības
Izmantojot pārskatu **Noviržu analīzes izraksts**, var analizēt pārvērtēšanas novirzes, bet, izmantojot pārskatu **Krājumu vērtība**, var skatīt krājumu vērtību noteiktā datumā.

-   Analizēt pārvērtēšanas novirzes. Izmantojiet pārskatu **Noviržu analīzes izraksts**, lai skatītu pārveidoto krājumu pārvērtēšanas novirzes. Lai skatītu pārveidoto krājumu, kam ir pieejami krājumi, pārvērtēšanas transakcijas, var izmantot lapu **Standarta izmaksu transakcijas**.
-   Analizējiet krājumu vērtību pirms pārejas perioda sākuma datuma. Izmantojiet pārskatu **Krājumu vērtība**, lai skatītu pārveidoto krājumu vērtības. Pārskata laukā Līdz datumam izmantojiet datumu, kas ir vienu dienu pirms pārejas perioda sākuma datuma.
-   Analizējiet krājumu vērtību pirms pārveidošanas datuma. Izmantojiet pārskatu **Krājumu vērtība**, lai skatītu pārveidoto krājumu vērtības. Pārskata laukā Līdz datumam izmantojiet datumu, kas norāda vienu dienu pirms pārveidošanas procesa datuma.
-   Analizējiet krājumu vērtību pārveidošanas datumā. Izmantojiet pārskatu **Krājumu vērtība**, lai skatītu krājumu vērtības no pārveidošanas datuma. Datumiem abos pārskata laukos No datuma un Līdz datumam jāatbilst pārveidošanas datumam. Pārskata atlases kritērijiem ir jāparāda pārveidotie krājumi.
-   Analizējiet krājumu kustību transakcijas ar atpakaļejošu datumu. Izmantojiet pārskatu **Krājumu vērtība**, lai skatītu krājuma kustību transakcijas, kas ievadītas pēc pārveidošanas ar atpakaļejošu datumu. Datumiem pārskata laukos No datuma un Līdz datumam jāatbilst pārejas perioda sākuma datumam un pārveidošanas datumam, atņemot vienu dienu. Pārskata atlases kritērijiem ir jāparāda pārveidotie krājumi. Pārskatā ir redzamas krājumu kustību transakcijas, kas ir veiktas ar standarta izmaksām pārejas perioda laikā.


<a name="see-also"></a>Skatiet arī
--------

[Standarta izmaksu konvertēšanas priekšnoteikumi](prerequisites-standard-cost-conversion.md)




