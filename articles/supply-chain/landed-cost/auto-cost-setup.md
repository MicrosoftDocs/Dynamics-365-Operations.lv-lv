---
title: Automātiska izmaksu iestatīšana
description: Šajā rakstā ir aprakstīts, kā iestatīt izmaksu noteikumus dažādiem ienākošo reisu līmeņiem. Pamatojoties uz šiem noteikumiem, sistēma aprēķina izmaksas un automātiski pievieno tās. Tādēļ lietotājiem nav manuāli jāpievieno izmaksas.
author: Weijiesa
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 02c78789fc7531c267cee936fa30a395e6d0b62f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852394"
---
# <a name="auto-costs-setup"></a>Automātiska izmaksu iestatīšana

[!include [banner](../../includes/banner.md)]

Var izmantot lapu **Automātiskās izmaksas**, lai iestatītu izmaksu noteikumus dažādām izmaksu zonām (piemēram, reisiem, nosūtīšanas konteineriem, konteineriem, pirkšanas pasūtījumiem, krājumiem vai pārsūtīšanas pasūtījuma rindām). Pamatojoties uz noteikumiem un laukiem, kurus lietotāji atlasa, kad tie izveido ierakstus vienai no izmaksu jomām, sistēma aprēķina izmaksas un automātiski pievieno tās. Tādēļ lietotājiem nav manuāli jāpievieno izmaksas.

Lai strādātu ar automātiskām izmaksām, dodieties uz sadaļu **Kopējās izmaksas \> Izmaksu aprēķināšanas iestatījumi  \>Automātiskās izmaksas**. Pēc tam iestatiet automātiskās izmaksu kārtulas atbilstoši aprakstam pārējā rakstā.

## <a name="work-with-cost-areas"></a>Darbs ar izmaksu apgabaliem

Automātiskās izmaksas darbojas kā tirdzniecības līgumi vai papildmaksas. Katrs automātiskais izmaksu ieraksts attiecas uz noteiktu izmaksu līmeni. Izmantojiet lauku **Izmaksu apgabals** saraksta rūts lapā **Automātiskās izmaksas** , lai atlasītu izmaksu apgabalu, ar kuru vēlaties strādāt. Saraksta rūtī ir redzamas tikai automātiskās izmaksas, kas pieder pašlaik atlasītajam izmaksu apgabalam. Visas jūsu veidotās automātiskās izmaksas piederēs pašlaik atlasītajai izmaksu jomai.

Izmaksu apgabali iespējo sistēmu izmaksu iejaukšanai izmaksu apgabalā pirkšanas pasūtījuma rindās. Piemēram, viena pārvadāšanas konteinera izmaksas saņems vērtību visām precēm šajā pārvadāšanas konteinerā. Ja ir divi vai vairāki pārvadāšanas konteineri, katram pārvadāšanas konteineram var norādīt vienu un to pašu izmaksu tipu. Tāpēc konteinera veidu var izmantot, lai atrastu pareizās automātiskās izmaksas.

## <a name="buttons-on-the-action-pane"></a>Pogas darbību rūtī

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas **Automātisko izmaksu** lapas darbību rūtī.

| Poga | Apraksts |
|---|---|
| Labot | Labot esošās automātiskās izmaksas. |
| Jauna | Automātisko izmaksu izveide. |
| Delete | Automātisko izmaksu dzēšana. |
| Kopēt no | Izveidot jaunu darba pasūtījumu, kas ir pamatots uz esošu ierakstu. Tad varat brīvi rediģēt jauno ierakstu. Šī poga palīdz ātri izveidot jaunas automātiskās izmaksas. |
| Parādīt dimensijas | Atveriet dialoglodziņu, kur var atlasīt krājumu dimensijas, kas parādītas izmaksu darbībām, kuras skatāt. Ja notīrīsiet izvēles rūtiņas, izmaksu darbībām tiks rādīts mazāk krājumu dimensiju. Tāpēc darbībai tiks rādīta mazāk detaļu. Ja krājuma dimensija ir norādīta automātiskām izmaksām, automātiskās izmaksas tiks lietotas tikai tad, kad norādītā krājumu dimensija tiks izmantota krājumam reisā. |

## <a name="settings-on-the-header"></a>Galvenes iestatījumi

Iestatījumu kombinācija virsraksta sadaļā nosaka, kad un kā reisam tiek pievienotas noteiktas automātiskās izmaksas. Automātiskās izmaksas tiks piemērotas reisam, pārvadāšanas konteineram vai folio tikai tad, kad informācija par automātiskām izmaksām atbilst detalizētai informācijai šīs izmaksu zonas galvenē. Visu atbilstošo automātisko izmaksu summa nosaka reisa novērtētās kopējās kopējās zemes izmaksas. Šīs izmaksas tiek izmaksātas visām vienībām kuģim vai reisam.

Tālāk esošajā tabulā ir aprakstīti galvenē pieejamie lauki. Tomēr konkrētie lauki, kas ir pieejami, mainās atkarībā no izmaksu zonas un pašlaik atlasītajām parādāmajām dimensijām.

| Lauks | Apraksts |
|---|---|
| **Konta kods** | <p>Atlasiet vienu no šīm vērtībām:</p><ul><li>**Tabula** - izmaksu kārtula attiecas uz noteiktu kreditoru.</li><li>**Grupa** - izmaksu kārtula attiecas uz noteiktu kreditoru grupu. Sistēma meklēs [kreditora izmaksu tipu grupu](costing-parameters-setup.md), kas ir saistīta ar kreditora ierakstu.</li><li>**Visi** – izmaksu kārtula attiecas uz visiem kreditoriem. |
| **Nosūtīšanas uzņēmums** | Atlasiet kreditoru vai kreditoru grupu, kurai tiek piemērota izmaksu kārtula. Šis lauks ir pieejams tikai tad, ja laukā **Uzņēmuma kods** atlasāt *Tabula* vai *Grupa*. |
| **Muitas aģents** | Atlasiet kreditoru vai kreditoru grupu, kurai tiek piemērota izmaksu kārtula. Šis lauks ir pieejams tikai tad, ja laukā **Uzņēmuma kods** atlasāt *Tabula* vai *Grupa*. |
| **Krājuma kods** | <p>Atlasiet vienu no šīm vērtībām:</p><ul><li>**Tabula** - izmaksu kārtula attiecas uz noteiktu krājumu.</li><li>**Grupa** - izmaksu kārtula attiecas uz noteiktu krājumu grupu. Sistēma meklēs [krājumu izmaksu tipu grupu](costing-parameters-setup.md), kas ir saistīta ar krājuma ierakstu.</li><li>**Visi** – izmaksu kārtula attiecas uz visiem krājumiem.|
| **Krājumu saistība** | Atlasiet krājumu vai krājumu grupu, kurai tiek piemērota izmaksu kārtula. Šis lauks ir pieejams tikai tad, ja laukā **Krājuma kods** atlasāt *Tabula* vai *Grupa*. |
| **Piegādes veids** | Atlasiet piegādes veidu (piemēram, gaiss vai jūra), uz kuru attiecas izmaksu noteikums. |
| **Konteinera veids** | Sūtījuma konteinera tips, kurā tiks nosūtītas preces. Automātiskas izmaksas var piemērot reisam tikai tad, ja konteinera veids, kura automātiskās izmaksu iestatījums atbilst reisa konteinera veidam. |
| **No porta** un **Uz portu** | Reisa avota ("no") ports un galamērķa ("uz") ports. (Dažiem sūtījumu konteineriem var būt atšķirīgi "uz" porti, jo reiss var apturēties vairākos portos.) Automātiskas izmaksas var piemērot reisam tikai tad, ja "no" un "uz" porti automātiskajā izmaksu iestatījumā sakrīt ar "no" un "uz" reisa portiem. |
| **Automātisko izmaksu numurs** | Unikālais automātisko izmaksu kārtulu identifikators. Šī lauka vērtība tiek automātiski ģenerēta, pamatojoties uz numuru sēriju, kas ir iestatīta lapā **Zemes izmaksu parametri**. |
| **Krājumu dimensijas** | Dažas izmaksu zonas ļauj virsrakstā iekļaut vienu vai vairākas krājumu dimensijas (piemēram, izmēru, krāsu, noliktavu un partijas numuru). Atlasiet Darbību rūtī **Parādīt dimensijas**, lai atlasītu dimensijas, kuras jāietver. |

## <a name="settings-on-the-lines-fasttab"></a>Kopsavilkuma cilnes Rindas iestatījumi

Kopsavilkuma cilnē **Rindas** pievienojiet rindu katrai valūtai, ko var izmantot, kad izmaksas tiek piemērotas pirkšanas pasūtījuma rindai reisā. 

Krājumiem un pirkšanas pasūtījumiem sistēma sakrīt ar katras pirkšanas pasūtījuma rindas valūtu attiecībā pret valūtām, kas norādītas kopsavilkuma cilnē **Rindas**. Tā izmantos tikai izmaksu vērtību, kas iestatīta atbilstības rindai vai krājumam. Ja rindas vai krājuma valūtai nav iestatīta neviena rinda, automātiskās izmaksas netiks attiecinātas uz šo rindu vai krājumu.

Citiem izmaksu apgabalu tipiem visas kopsavilkuma cilnes **Rindas** rindas tiks lietotas katram reisam, nosūtīšanas konteineram, folio vai pārsūtīšanas pasūtījuma rindai, kas atbilst virsrakstā izveidotajām vērtībām.

Tālāk esošajā tabulā ir aprakstīti katrā rindā pieejamie lauki. Tomēr konkrētie pieejamie lauki mainās atkarībā no pašlaik atlasītās izmaksu zonas.

| Lauks | Apraksts |
|---|---|
| **Valūta** | Atlasiet valūtu, uz kuru attiecas rinda. Šī valūta ir saistīta ar pirkšanas pasūtījumu. Kad sistēma mēģina atrast automātiskās izmaksas, kas jāpiemēro reisam un tā reisa rindām, tā atlasīs rindu, kurai ir tāda pati valūta kā pirkšanas pasūtījumam. Šis lauks ir pieejams tikai tad, ja lauks **Izmaksu apgabals** ir iestatīts uz *Pirkšanas pasūtījums* vai *Krājums*. |
| **Izmaksu veida kods** | Izmaksu tips. |
| **Norīkojuma metode** | <p>Metode, kas tiek izmantota izmaksu sadales rindām. Pieejamas šādas opcijas:</p><ul><li><p>**Procenti** – lauka **Izmaksu vērtība** vērtība ir procenti, kas attiecas uz preču kopējo vērtību.</p><p>Piemēram, ja lauks **Izmaksu vērtība** ir iestatīts uz *10* un preču kopējā vērtība $800, izmaksu vērtība ir $80 (= $800 × 10 procenti).</p></li><li>**Daudzums** – izmaksas tiks aprēķinātas, balstoties uz preču daudzumu.</li><li>**Daudzums** – izmaksas tiks aprēķinātas, balstoties uz preču vērtību.</li><li>**Daudzums** – izmaksas tiks aprēķinātas, balstoties uz preču tilpumu. Krājuma šablonā ir norādīts tilpums.</li><li>**Daudzums** – izmaksas tiks aprēķinātas, balstoties uz preču svaru. Krājuma šablonā ir norādīts svars.</li><li>**Daudzums** – izmaksas tiks aprēķinātas, balstoties uz preču tilpuma mērījumiem.</li><li><p>**Mērījums** – šī opcija aktivizē mērījumu norādīšanu modulī **Kopējās izmaksas**. Bieži vien to lieto organizācijas, kuras nepazīst atsevišķu preču tilpumu vai svaru, bet kurām ir nepieciešamas precīzākas iešana rezervēs, nekā atļautas opcijas **Summa** un **Daudzums**. Kravas ekspediators vai aģents nodrošina organizāciju ar svara vai kubikmetru krājumu līmenī vai pirkšanas pasūtījuma līmenī.</p><p>Piemēram, kravas pārvadāšana ir vienāda ar $900. Krājuma A svars ir 800 kilogrami (kg) un tilpums 2 kubikmetri (m³). Krājuma B svars ir 100 kilogrami (kg) un tilpums 1 kubikmetrs (m³). Šeit tiek iegūti rezultāti, kad izmaksas tiek aprēķinātas pēc svara:</p><ul><li>Krājums A = $800</li><li>Krājums B = $100</li></ul><p>Šeit tiek iegūti rezultāti, kad izmaksas tiek aprēķinātas pēc tilpuma:</p><ul><li>Krājums A = $600</li><li>Krājums B = $300</li></ul><p>**Piezīme:** Ja lauks **Aprēķināšanas metode** ir iestatīts uz *Mērījums*, sistēma izmanto mērījumus, kas ievadīti gan izmaksu apgabalam (nosūtīšanas konteineram), gan rindām. Šiem mērījumiem nav obligāti jāpievieno paredzētā kopsumma. Tomēr, ja nepieciešams, lai tie pievienotu līdz prognozētajam kopsummai, varat veikt pārbaudi, izmantojot statistiku, lai pārskatītu kopējos mērījumus. Mērījuma uzvednes iestatījums un automātiska mērījuma atjaunināšana sūtījuma vai konteinera līmenī tiek iestatīta reisa galvenē.</p></li></ul> |
| **No datuma** | Norādiet izmaksu diapazona sākumu izmaksu grāmatošanai, ja ir datumu diapazons. Šis datums ir pirmais datums, kad tiks lietotas automātiskās izmaksas. |
| **Līdz datumam** | Norādiet izmaksu diapazona beigas izmaksu grāmatošanai, ja ir datumu diapazons. Šis datums ir pēdējais datums, kad tiks lietotas automātiskās izmaksas. |
| **Kategorija** | <p>Atlasiet metodi, kas tiek izmantota izmaksu aprēķināšanai. Pieejamas šādas opcijas:</p><ul><li>**Fiksēts** – izmaksas tiks aprēķinātas, balstoties uz aprēķināšanas metodi.</li><li>**Gabali** – izmaksas tiks sadalītas pa gabaliem. Tāpēc netiks izmantota aprēķināšanas metode.</li><li>**Procenti** – tiks pievienota preču vērtības procentuālā vērtība. Tāpēc netiks izmantota aprēķināšanas metode.</li><li>**Likme** - izvēlieties šo opciju, ja ir daudzuma sadalījums. Rindas **Aprēķināšans metodes** laukam Ir jābūt iestatītam uz *Mērījums*.</li><ul> |
| **Sadalīts pēc daudzuma** | <p>Atzīmējiet šo izvēles rūtiņu, lai kopsavilkuma cilnē **Rindas** būtu pieejama poga **Daudzuma pārtraukumi**. Daudzuma pārtraukumi ļauj sadalīt izmaksas un dažādās izmaksas mainās atkarībā no daudzuma reisa pirkšanas pasūtījuma rindā. Šī funkcionalitāte bieži tiek lietota, kad piegādes režīms ir gaiss. Rindas **Kategorija** laukam ir jābūt iestatītam uz *Mērogs*.</p><p>Ieejas plūsmas daudzums, pamatojoties uz opciju, kas atlasīta laukā **Aprēķināšanas metodes**. Izmaksu vērtība tiks līdz daudzumam, kas ir ievadīts laukā **Izmaksu vērtība**.<p>Piemēram, 45–100 kg daudzums rada maksu $6,00 katram mērījumam (piemēram, kg/m³). Piemēram, daudzumi, kas pārsniedz 100 kg, veido $5,50 maksu mērījumam (piemēram, kg/m³).</p> |
| **Izmaksu vērtība** | Ievadiet izmaksu vērtību. |
| **Izmaksu valūtas kods** | Atlasiet izmaksu valūtu. |
| **Krājumu PVN grupa** | Atlasiet izmaksu nodokļu kodu. |
| **Minimālās izmaksas** | <p>Šis lauks tiek lietots tikai tad, ja ir atzīmēta izvēles rūtiņa **Sadalīts pēc daudzuma**. Ja mērījums nesasniedz šo vērtību, tiek atlasīta minimālā vērtība neatkarīgi no lapā **Daudzuma pārtraukumi** norādītajām izmaksām.<p>Piemēram, 0–45 kg daudzumi rada $6 maksu mērījumam (piemēram, kg/m³). Piemēram, 46–100 kg daudzumi rada $5,50 maksu mērījumam (piemēram, kg/m³). Ja tiek nosūtīti 2 kg, daudzuma pārtraukums izveidos vienības izmaksu $12. Tomēr, ja lauks **Minimālās izmaksas** ir iestatīts uz *USD 100*, galīgās izmaksas būs $100.</p> |
| **Uzkrātā** | Atzīmējiet šo izvēles rūtiņu, lai ļautu lietotājiem pārvietot šīs izmaksas no nosūtīšanas konteinera līmeņa uz reisa līmeni. Šajā gadījumā izmaksas var automātiski aprēķināt nosūtīšanas konteinera līmenī. Tomēr tos var arī kombinēt un visus krājumus visos reisa konteineros šo krājumu vietā izmantot arī atsevišķos pārvadāšanas konteineros. |
| **Saistīto izmaksu veids** | <p>Saistiet pašreizējo rindu ar citu rindu tajā pašā automātiskajā izmaksu ierakstā, norādot tās rindas **Izmaksu tipa koda** vērtību, ar kuru vēlaties izveidot saiti. Šī funkcionalitāte ir pieejama tikai tad, ja lauks **Kategorija** pašreizējai rindai ir iestatīts kā *Procenti*. Ja šī rinda ir saistīta ar citu rindu, pašreizējās rindas izmaksas tiks pamatotas uz citas rindas izmaksām.</p><p>Piemēram, kravas vērtība ir $1,000, un jūs vēlaties, lai piemaksa par degvielu būtu 10 procenti no kravas pārvadāšanas izmaksām. Šajā gadījumā rindai jābūt **Kategorijas** vērtībai *Procents*, **Izmaksu vērtībai** jābūt *10%* un **Saistīto izmaksu tipa** vērtībai jābūt *Kravai*.</p> |
| **Vērtības korekcija** un **Korekcijas summa** | <p>Izmantojiet šos laukus, lai pielāgotu vērtību un summu dažādām procentu vērtībām. Tās ir pieejamas tikai tad, ja **Izmaksu apgabala** lauks ir iestatīts kā *Krājums*.</p><p>Dažādiem krājuma komponentiem var iestatīt dažādas izmaksu aprēķināšanas. Vienam krājuma komponentam var būt izmaksu procentuālā likme, kas atšķiras no citiem šī krājuma komponentiem. Dažreiz šī pieeja ir nepieciešama, lai noteiktu preču daļu vērtēšanu ar dažādām likmēm.</p><p>Piemēram, nodoklis šim uzrāms tiek aprēķināts ar divām likmēm: vienam no uzr elementa komponentiem ir 10 procentu nodokļa likme, un otrajam komponentam ir 2 procentu nodokļa likme. Šajā gadījumā izmaksu aprēķināšana tiks sadalīta starp divām sastāvdaļām.</p><p>Izmaksas tiek aprēķinātas krājumam, bet izmaksu vērtība tiek pielāgota ar sastāvdaļu vērtību, kam ir atšķirīga izmaksu kategorija. Atlikušo sastāvdaļu izmaksas pēc tam var aprēķināt, izmantojot summu, par kādu tika koriģēts iepriekšējais aprēķins.</p><p>Piemēram, komandējuma komponenta A izmaksas ir $9,50 un 10 procentu nodoklis, un komponenta B izmaksas $0,50 ir un 2 procentu nodoklis. Tādējādi kopējās izmaksas ir $10,00. Pirmais ieraksts ir 10 procentu rindai. Tiek izmantotas šādas vērtības:</p><ul><li>**Kategorija:** *Procenti*</li><li>**Izmaksu vērtība:** *10*</li><li>**Koriģēta vērtība:** *Koriģēt pēc*</li><li>**Koriģētā vērtība:** *-0,50*</li></ul><p>Šie iestatījumi norāda, ka krājuma izmaksas (USD 10) jāsamazina par $0,50 (B komponenta cena) pirms 10 procentu nodokļa maksas aprēķināšanas. Tāpēc 10 procenti tiks piemēroti $9,50.</p><p>Otrais ieraksts ir 2 procentu rindai ($0,50 rinda, ar kuru tika koriģēta iepriekšējā ievadne). Tiek izmantotas šādas vērtības:</p><ul><li>**Kategorija:** *Procenti*</li><li>**Izmaksu vērtība:** *2*</li><li>**Koriģētā vērtība:** *Izmantot*</li><li>**Pielāgojums:** *0,50*</li></ul><p>Šis iestatījums aprēķina atlikušo nodokli, kas maksājams B komponentam.</p> |
