---
title: Automatizēt Virsgrāmatas nosegšanu
description: Šajā rakstā ir sniegta informācija par Automatizēt Virsgrāmatas segšanas procesu.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9707762"
---
# <a name="automate-ledger-settlements"></a>Automatizēt Virsgrāmatas nosegšanu

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finanšu versijā 10.0.31 automātiskā **Virsgrāmatas nosegšanas** procesa funkcija ir pieejama **Līdzekļu pārvaldības darbvietā** . Jūs variet iespējot **Automatizēt virsgrāmatas segšanas procesu** **tikai tad, ja ir aktivizēta funkcija Apzināšana starp Virsgrāmatas nosegšanu** un gada beigu aizvēršanu.

Virsgrāmatas nosegšana ir salīdzināšanas process debeta un kredīta darbībām Virsgrāmatā. Organizācijas, kas veic Virsgrāmatas nosegšanas darbības periodiskajā grafikā, tagad var automatizēt procesu. Automātiskās Virsgrāmatas segšanas procesa laikā debeta darbību un kredīta darbību var automātiski saskaņot tikai tad, ja to summas uzskaites valūtā ir vienādas.Piemēram, debeta summu ar $1.00 automātiski var saskaņot ar kredīta summu, kas $1.00. Tomēr debeta vērtību $1.00 automātiski nevar saskaņot ar diviem kredītiem, no kuriem katrs ir $0.50. Virsgrāmatas darbību summu daļēja saskaņošana netiek atbalstīta.

Virsgrāmatas nosegšanas automatizācija definē šādu informāciju:

- Izpildot Virsgrāmatas nosegšanu
- Kādus kritērijus izmanto, lai atbilstu debetiem un kredītiem, ko var automātiski nosegt
- Kādā pasūtījumā tiek apstrādāta Virsgrāmatas nosegšanas informācija

## <a name="define-the-occurrence-of-ledger-settlements"></a>Noteikt Virsgrāmatas nosegšanas gadījumu

Virsgrāmatas nosegšanas automatizācija izmanto procesa automatizācijas struktūru. Dažādi biznesa procesi izmanto šo struktūru, lai definētu atlasītā procesa atkārtošanos. Virsgrāmatas segšanai dodieties uz sadaļu Sistēmas  **administrēšanas \> iestatīšanas \> procesa automatizācija** vai **Virsgrāmatas \> iestatīšanas procesa \> automatizācija**.

Vispirms atlasiet opciju Izveidot jaunu **procesa automatizāciju** un atlasiet Virsgrāmatas segšanas ****. Pēc tam ceļvedis jūs vadīs cauri automatizācijas iestatīšanas procesam.

## <a name="general-page"></a>Vispārīgā lapa

 **Vedņa** vispārīgajā lapā ievadiet tā Virsgrāmatas nosegšanas gadījuma nosaukumu, kuru veidojat. Piemēram, ja jūsu atbilstošie debeti un kredīti pirmdien ir nosegti Virsgrāmatā, ievadiet aprakstošu nosaukumu, piemēram **, LedgerSettle\_ Nor**. Ievadītais nosaukums ir parādīts virsgrāmatas nosegšanas **lapas** kolonnā Automatizācijas **noteikums** .

Atlikušie lapas iestatījumi ir vispārēji un nosaka gadījumu modeli šai Virsgrāmatas nosegšanas versijai. Piemēram, ja gadījums ir pirmdienā, to var norādīt tā, lai tas darbotos katru nedēļu, un var izvēlēties pirmdienu kā nedēļas dienu, kad tā darbojas. Varat ievadīt arī sākotnējo grafika laiku, piemēram, 2:00 AM, tā, lai procesa automatizācija tiktu pabeigta pirms nākamās darba dienas sākuma. Iesakām plānot procesa automatizāciju, lai tā tiek veikta ārpus parastajām darba stundām. Šādā veidā darba dienas laikā jūs palīdziet samazināt grāmatvedību ietekmēšanu.

Papildinformāciju par citiem laukiem vispārīgajā **lapā** skatiet procesa automatizācijas dokumentācijā.

## <a name="ledger-settlements-match-criteria-page"></a>Virsgrāmatas nosegšanas darbību atbilstības kritēriju lapa

Nākamā vedņa lapa ir Virsgrāmatas nosegšanas **darbību atbilstības kritēriju** lapa. To izmanto, lai definētu galvenos kontus, kas ir iekļauti procesa automatizācijas notikumā, un kritērijus, kas tiek izmantoti, lai noteiktu atbilstošus debetus un kredītus.

### <a name="account-selection"></a>Konts

Tiek rādīti galvenie konti, kas iepriekš definēti kā juridiskās personas Virsgrāmatas nosegšanas konti. (Jūs definējat galvenos kontus kā Virsgrāmatas nosegšanas kontus pie **Virsgrāmatas iestatīšana \> Virsgrāmatā \> parametri Virsgrāmatas \> nosegšanai**.)

### <a name="main-account-and-posting-layer"></a>Galvenais konts un grāmatošanas līmenis

Pamatkonta  **un** grāmatošanas **līmeņa** vērtības ir nepieciešamas atbilstības kritērijiem. Virsgrāmatas **debeta** darbības **un kredīta** darbības galvenā konta un grāmatošanas līmeņa vērtībām jābūt vienādām ar vērtībām automātiskas Virsgrāmatas nosegšanas procesa laikā.

### <a name="posting-type"></a>Grāmatošanas tips

Atlasiet opciju **Grāmatošanas tips**, ja Virsgrāmatas debeta un kredīta darbībām jābūt vienādam grāmatošanas tipam, lai tās atbilstu automātiskas Virsgrāmatas nosegšanas procesa laikā.

### <a name="financial-dimensions"></a>Finanšu dimensijas

Atlasiet opciju **Finanšu dimensijas**, ja Virsgrāmatas debeta un kredīta darbībām jābūt vienādām finanšu dimensijām, lai tās atbilstu automātiskas Virsgrāmatas nosegšanas procesa laikā. Ja atlasīta šī opcija, sarakstā Pieejamās finanšu dimensijas ir jāatlasa finanšu dimensiju **vērtību** kritērijs. Sarakstā **Pieejamās finanšu** dimensijas nav galvenā konta dimensija, jo tā automātiski tiek pieprasīta kā daļa no atbilstības kritērijiem.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Skatīt Virsgrāmatas nosegšanas automatizācijas rezultātus

Kad ir izveidotas Virsgrāmatas segšanas automatizācijas sērijas, katras virsgrāmatas nosegšanas gadījumi tiek parādīti procesa automatizācijas nedēļas skatā. Turklāt tiek rādīts katra gadījuma statuss. Izmanto šādus statusus:

- **Ieplānots**  — automatizācija ir ieplānota, bet vēl nav palaista.
- **Notiek izpilde** – automatizācija pašlaik tiek palaista.
- **Kļūda**  – automatizācija ir palaista, bet radās kļūda. Kļūdas varat skatīt, atlasot pogu **Skatīt** rezultātus.
- **Pabeigts**  – automatizācija ir veiksmīgi palaista. Varat skatīt nosegšanas rezultātus Virsgrāmatas **nosegšanas lapā**.

Lai skatītu atbilstošos rezultātus, dodieties uz Virsgrāmatas periodiskajiem **\> uzdevumiem Virsgrāmatā \>**. Automatizācijas **nosacījuma** lauks Virsgrāmatas nosegšanas **lapā parāda automatizētā Virsgrāmatas nosegšanas** plānotā uzdevuma nosaukumu, kas tika izmantots darbības segšanai. Neveiksmīgi nosegšanas mēģinājumi neatjaunina automatizācijas **kārtulas** vērtību. Ja manuāli anulējat darbību, kas iepriekš tika veiksmīgi nokārtota automatizācijas procesā, automatizācijas **kārtulas** vērtība tiks noņemta.

Saskaņoto **ierakstu** nosegšanas datuma lauks rāda datumu, kad tika veikts automatizācijas process.

## <a name="editing-a-ledger-settlement-automation"></a>Virsgrāmatas nosegšanas automatizācijas rediģēšana

Procesa automatizācijas struktūra ļauj jums rediģēt sērijas un notikumus, kas izveidoti virsgrāmatas segšanai. Sērijas var labot ne no lapas Procesu automatizācija **** , vai no procesa automatizācijas nedēļas skata. Piemēram, ja vadītājs nolemj pirmdien veikt Virsgrāmatas nosegšanu nevis pirmdien, bet reizi nedēļā, **viņi var atrast gadījumu nedēļas skatā un atlasīt Skatīt/Rediģēt - Sērijas**.

Ja rediģējat sēriju, tiek piedāvāts norādīt, vai izmaiņas jāveic visiem esošajiem gadījumiem vai tikai jauniem gadījumiem. Vēsturisks gadījums, kura statuss jau **ir Pabeigts**, vai **** pabeigts ar statusu Kļūda, netiks mainīti.

Varat arī pievienot jaunu gadījumu vai mainīt esošu gadījumu. Piemēram, nākamais Virsgrāmatas nosegšanas gadījums ir ieplānots palaist trešdienu, 1. janvāri, bet šis datums ir svētku diena. Jūs varat mainīt gadījumu vai nu no lapas Procesa automatizācija **** , vai no procesa automatizācijas nedēļas skata. Tiek atvērta lapa, kurā parādīta detalizēta informācija par grafiku un atbilstības kritērijiem. Šeit varat labot ieplānoto laiku un datumu. Varat arī rediģēt atbilstības kritērijus, ja nepieciešamas izmaiņas. 

Varat arī deaktivizēt notikumu vai sēriju. Lai deaktivizētu gadījumu un aizturētu tā apstrādi, atlasiet to procesa automatizācijas nedēļas skatā un pēc tam atlasiet Deaktivizēt ****. Jūs varat atspējot sērijas lapā Procesa **automatizācija** .

## <a name="security-for-ledger-settlement-automation"></a>Virsgrāmatas nosegšanas automatizācijas drošība

**Virsgrāmatas segšanas** automatizācijas sēriju iestatījumu uzturēšana pienākums ir pievienots grāmatvedības pārvaldnieka un grāmatvedības supervizora lomām, **un Virsgrāmatas segšanas** automatizācijas sēriju iestatījumu skatīšanas pienākums ir pievienots grāmatveža, grāmatvedības pārvaldnieka un grāmatvedības supervizoru lomām Virsgrāmatas segšanas automatizāciju lomai. Šie pienākumi ir noklusējuma drošības iestatījumi, bet tos var mainīt, ņemot vērā jūsu organizācijas prasības.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Virsgrāmatas parametri Virsgrāmatas segšanas automatizācijai

Lauks **Nosegšana** - tipiskā bilance norāda pasūtījumu, kurā tiks apstrādāta automātiskā Virsgrāmatas nosegšana. Lai iestatītu vai skatītu nosegšanas **parastu** bilances vērtību, **\>\> dodieties uz sadaļu Virsgrāmatas iestatījumu virsgrāmatas** parametri un **atlasiet cilni Virsgrāmatas nosegšana**.

Ja **ir atlasīts** Debets, automatizētais Virsgrāmatas nosegšanas process sākas debeta pusē un meklē atbilstošus kredītus. Ja **ir** atlasīts Kredīts, automatizētais Virsgrāmatas nosegšanas process sākas kredīta pusē un meklē atbilstošos debetus. Šai opcijai ir jāatspoguļo galvenā konta tipiskā bilance.

## <a name="processing-a-ledger-settlement-automation"></a>Virsgrāmatas nosegšanas automatizācijas apstrāde

Kad automatizācija tiek palaista, sistēma atlasa Virsgrāmatas darbības galvenajiem kontiem, kas ir definēti procesa automatizācijas sērijām. Tas pasūta darbības pēc datuma, izmantojot datumu diapazonu no finanšu gada sākuma līdz procesa automatizācijas palaišanas datumam. Tā sakrīt, ņemot vērā norādītos atbilstības kritērijus. Jāsakrīt debeta un kredīta summu uzskaites valūtas absolūtajām vērtībām, lai tie būtu nosegti.

Lai gan galvenais konts tiek apstrādāts virsgrāmatas segšanas automatizācijas gadījumā, jūs to nevarat parādīt Virsgrāmatas **nosegšanas lapā**. Jums jāgaida, kamēr automatizācijas process tiks pabeigts. Ieteicams ieplānot procesa automatizāciju, lai tā darbotos ārpus darba stundām, lai palīdzētu novērst konfliktus.

Automatizācijas process ietvers visas darbības, kas atbilst kritērijiem, izņemot darbības, kas manuāli atzīmētas segšanai Virsgrāmatas **nosegšanas** lapā.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Darbību, kas tiek segtas ar automatizācijas procesu, atcelšana

Varat atsaukt segšanu, kas ir veikta, izmantojot automatizētu Virsgrāmatas segšanas procesu. Kad transakcija, kas tika segta ar automatizācijas procesu, ir anulēta, automatizācijas **kārtulas** vērtība tiks noņemta.
