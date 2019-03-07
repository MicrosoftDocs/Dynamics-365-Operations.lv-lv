---
title: Kontrolēt noliktavas darbu, izmantojot darbu veidnes un novietojuma direktīvas
description: Šajā tēmā ir sniegta informācija par to kā izmantot darba veidnes un vietas direktīvas, lai noteiktu, kā un kur darbs tiek veikts noliktavā.
author: perlynne
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e7c36fb912f35252d6e40d17477ac2962cbc23
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "325415"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Kontrolēt noliktavas darbu, izmantojot darbu veidnes un novietojuma direktīvas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par to kā izmantot darba veidnes un vietas direktīvas, lai noteiktu, kā un kur darbs tiek veikts noliktavā.

Tas, kādas instrukcijas noliktavas darbinieki saņem mobilajā ierīcē, ir atkarīgs no darba veidnēm, kuras iestatāt programmā Microsoft Dynamics 365 for Finance and Operations, lai definētu dažādos noliktavas procesus un uzdevumus. Darba veidnes nosaka, kā darbs tiek veikts katram noliktavas procesam. Saistot novietojuma direktīvu ar darba veidnēm, var palīdzēt garantēt, ka darbs notiek noteiktās noliktavu fiziskās daļās.

## <a name="work-templates"></a>Darbu veidnes
Lapa **Darbu veidnes** ļauj definēt darba operācijas, kas jāveic noliktavā. Parasti, noliktavas darba operācijas sastāv no darbību pāra: noliktavas darbinieks paņem rīcībā esošos krājumus vienā novietojumā un pēc tam liek paņemtos krājumus citā novietojumā. 

Darba veidnes sastāv no virsraksta un saistītām rindām. Katra darba veidne ir paredzēta īpašam *darba pasūtījuma veidam*. Daudzi darba pasūtījuma tipi ir saistīti ar avota dokumentiem, piemēram, pirkšanas vai pārdošanas pasūtījumiem. Tomēr, citi darba pasūtījumu tipi veido atsevišķus noliktavas procesus, piemēram, cikla inventarizāciju. *Darbu kopu ID* ļauj organizēt darbu grupās. 

Iestatījumus darba virsraksta definīcijā var izmantot, lai noteiktu, kad jāizveido jauns darba gabals. Piemēram, var iestatīt maksimālo izdošanas rindu skaitu un maksimālo plānoto izdošanas laiku. Pēc tam, ja darbs pārdošanas pasūtījuma izdošanas procesam pārsniedz kādu no šīm vērtībām, šis darbs tiek sadalīts divos darba gabalos. 

Darba rindas attēlo fiziskos uzdevumus, kas ir nepieciešami, lai varētu apstrādāt darbu. Piemēram, izejošajam noliktavas procesam var būt darba rinda krājumu paņemšanai noliktavā un cita rinda šo krājumu novietošanai sagatavošanas zonā. Pēc tam var būt papildu rinda krājumu izdošanai no sagatavošanas posmiem un cita rinda krājumu ievietošanai kravas automašīnā iekraušanas procesa ietvaros. Varat iestatīt *direktīvas kodu* darba veidnes rindās. Direktīvas kods ir saistīts ar novietojuma direktīvu un tāpēc palīdz nodrošināt, ka noliktavas darbs tiek apstrādāts pareizā novietojumā noliktavā. 

Vaicājumu var iestatīt, lai kontrolētu, kad tiek izmantota konkrētā darba veidne. Piemēram, var iestatīt ierobežojumu, lai noteiktu veidni varētu izmantot darbam tikai noteiktā noliktavā. Vai arī var būt vairākas veidnes, kas tiek izmantotas, lai izveidotu darbu izejošā pārdošanas pasūtījuma apstrādei atkarībā no pārdošanas izcelsmes. Lai noteiktu secību, kādā tiek novērtētas pieejamās darbu veidnes, sistēma izmanto lauku **Kārtas numurs**. Tādēļ, ja jums ir ļoti konkrēts vaicājums konkrētai darba veidnei, tam ir jāpiešķir zems kārtas numurs. Pēc tam šis vaicājums tiks novērtēts pirms citiem, vispārīgākiem vaicājumiem. 

Lai apturētu vai pauzētu darba procesu, var izmantot iestatījumu **Pārtraukt darbu** darba rindā. Tādā gadījumā, darbiniekam, kurš veic darbu, netiks lūgts veikt nākamās darba rindas darbību. Lai pārietu uz nākamo darbību, šim darbiniekam vai citam darbiniekam jāatlasa darbs vēlreiz. Varat arī atdalīt uzdevumus darba gabalā, izmantojot citu *darba klases ID* darba veidnes rindās.

## <a name="location-directives"></a>Novietojuma direktīvas
Novietojuma direktīvas ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Piemēram, pārdošanas pasūtījuma transakcijā novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti. Novietojuma direktīvas sastāv no virsraksta un saistītām rindām un tās izveido lapā **Novietojuma direktīvas**. 

Virsrakstā katrai novietojuma direktīvai jābūt saistītai ar *darba pasūtījuma tipu*, kas norāda krājumu transakcijas tipu, kas tiks izmantots direktīvai, piemēram, pārdošanas pasūtījumus, papildināšanu vai izejmateriālu izdošanu. *Darba tips* norāda, vai novietojuma direktīva tiks izmantota izdošanas vai nodošanas darbam vai citam noliktavas procesam, piemēram, inventarizācijai vai krājumu statusa izmaiņām. Jānorāda arī *vietne* un *noliktava*. *Direktīvas kodu*, ko norādāt virsrakstā, var izmantot, lai saistītu novietojuma direktīvu ar vienu vai vairākām darba veidnēm. 

Attiecībā uz darba veidnēm, varat iestatīt vaicājumu, lai noteiktu, kad tiek izmantota konkrēta novietojuma direktīva. Piemēram, varat norādīt ka tad, kad pārdošanas pasūtījuma izcelsme ir e-komercija, krājums ir jāizdod no atvēlētās zonas noliktavā. Sistēma izmanto lauku **Secības numurs**, lai noteiktu secību, kādā tiek novērtētas pieejamas novietojuma direktīvas. 

Novietojuma direktīvas rindas iestata papildu ierobežojumus attiecībā uz novietojuma meklēšanas noteikumu lietošanu. Varat norādīt minimālo daudzumu un maksimālo daudzumu, kuram direktīva jāpiemēro, kā arī varat norādīt, ka direktīvai jābūt paredzētai noteiktai krājuma vienībai. Piemēram, ja mērvienība ir paletes, krājumus paletēs var izvietot konkrētā novietojumā. Var arī norādīt, vai daudzumu var sadalīt starp vairākiem novietojumiem. Tāpat kā novietojuma direktīvas virsraksts katrai novietojuma direktīvas rindai ir sērijas numurs, kas nosaka secību, kādā rindas tiek novērtētas. 

Novietojuma direktīvām ir viens papildu detalizācijas līmenis: *novietojuma direktīvas darbības*. Var definēt vairākas novietojuma direktīvas darbības katrai rindai. Un atkal — kārtas numurs tiek izmantots, lai noteiktu secību, kādā darbības tiek novērtētas. Šajā līmenī varat iestatīt vaicājumu, lai definētu, kā atrast vislabāko novietojumu noliktavā. Varat arī izmantot iepriekš definētus **Stratēģijas** iestatījumus, lai atrastu optimālu novietojumu.

## <a name="location-directives-configuration-details"></a>Detalizēta informācija par vietas direktīvu konfigurāciju 

 ### <a name="sequence-number"></a>Sērijas numurs
 
Šis skaitlis norāda, kādā secībā tiek apstrādāta atlasītā pasūtījuma tipa vietas direktīva. To var mainīt, izmantojot izvēlnes vienumu **Pārvietot uz augšu** un **Pārvietot uz leju**.
 
 ### <a name="work-type"></a>Darba veids
 
Šis ir veicamā darba veids. Pieejamā darba veids ir atkarīgs no laukā **Darba pasūtījuma veids** atlasītā krājumu transakcijas veida.
-   **Izvietošana** - darba veids, kas ir vienāda ar **Izvietošana** nozīmē, ka vietas direktīva atrod vispiemērotāko vietu tādu krājumu novietošanai vai atrašanai, kas tiek pievienoti sistēmā saņemšanas, ražošanas vai krājumu korekciju gadījumā. To var izmantot, lai definētu izvietošanu sagatavošanas vietā vai pie galīgās nosūtīšanas vietas angāra durvīm.
-   **Izdošana** - darba veids, kas ir vienāda ar **Izdošana** nozīmē, ka noliktavā tiek atrasta vispiemērotākā vieta, no kuras notiek fiziska krājumu rezervēšana (darba izveidošana). Izdošanu var pabeigt (izdošanas darba rindu var slēgt) arī tad, ja darbs nav pabeigts. Lietotājs var pabeigt fizisko izdošanu, kas ir izdošanas darbība. Lietotājs pēc tam var atcelt darbību, izmantojot mobilo ierīci, un pabeigt darbu vēlāk. Tomēr, pabeidzot galīgo izdošanu, darba virsraksts tiek slēgts. 
-   **Inventarizācija, Korekcijas, Muita, Krājumu statusa maiņa, Unikāla noliktavas vienības identifikatora izveide, drukāšana, Statusa maiņa, Iepakot ligzdotos unikālos noliktavas vienības identifikatoros** — šie vienumi nav piemēroti izmantošanai kādas vietas direktīvas iestatīšanai. Tas ir uzskaitījums, tāpēc darba pasūtījuma veidam nav pievienota filtrēšana. 

### <a name="directive-code"></a>Direktīvas kods

Atlasiet direktīvas kodu, ko saistīt ar darba veidni vai papildināšanas veidni. Veidlapā **Direktīvas kods** var izveidot jaunus kodus, kurus var izmantot darba veidnes papildināšanas veidnes un vietas direktīvas savienojumiem. To var izmantot arī saites starp jebkuras darba veidnes rindas un vietas direktīvas (piemēram, angāra durvis vai sagatavošanas vietas) izveidošanai.

Ņemiet vērā, ka, ja kods ir iestatīts, ģenerējot darbu, sistēma nemeklē vietas direktīvu pēc secības, bet meklēšana tiek veikta pēc direktīvas koda. Tas nozīmē, ka var veikt precīzāk norādīt, kāda vietas veidne darba veidnē tiek izmantota konkrētai darbībai, piemēram, materiālu sagatavošana. 

### <a name="site"></a>Atrašanās vieta

Vieta ir obligāti aizpildāms lauks, jo vietas direktīvai ir jānorāda derīga vieta un noliktava. 

### <a name="warehouse"></a>Noliktava

Noliktava ir obligāti aizpildāms lauks, jo vietas direktīvai ir jānorāda derīga vieta un noliktava.

### <a name="multiple-sku"></a>Vairākas NV

Tas pieļauj vairākas noliktavas vienības (NV) vietā, piemēram, angāra durvis. Ja tiek atlasīts vienums **Vairākas NV**, darbā (paredzamajā) tiek norādīta izvietošanas vieta, bet tas var apstrādāt tikai vairāku preču izvietošanu (ja darbs ietver dažādu, nevis vienas NV izdošanu un izvietošanu). Ja vienums **Vairākas NV** netiek atlasīts, izvietošanas vieta tiek norādīta tikai tad, ja izvietošana ietver tikai viena veida NV. Lai varētu izmantot abas darbības, ir jānorāda divas rindas — viena ar ieslēgtu vairāku NV opciju un viena ar izslēgtu vairāku NV opciju. Tām ir jābūt vienādai struktūrai un iestatījumiem. Izvietošanas operāciju gadījumā ir nepieciešamas vietas direktīvas, kas ir identiskas arī tad, ja darba ID nav norādīta viena un vairākas NV. Ja ir pasūtījums, kas ietver vairāk nekā vienu krājumu, ir jāiestata arī izdošana.

### <a name="sequence-number"></a>Sērijas numurs

Ievadiet secību, kādā atlasītajam darba tipam tiek apstrādāta novietojuma direktīvas rinda. Ja nepieciešams, secību var arī mainīt, izmantojot vienumu **Pārvietot uz augšu** un **Pārvietot uz leju**.

### <a name="fromto-quantity"></a>Daudzums no/uz

Šī opcija nodrošina iespēju norādīt daudzuma diapazonu, ja ir jāatlasa vidēja līmeņa režģa secību. Vienuma Diapazons no/uz vērtību laukā Daudzums var norādīt attiecīgajās vienībās.

### <a name="unit"></a>Vienība

Varat norādīt minimālo daudzumu un maksimālo daudzumu, kuram direktīva jāpiemēro, kā arī varat norādīt, ka direktīvai jābūt paredzētai noteiktai krājuma vienībai. Mērvienības lauks rindā tiek izmantots tikai daudzuma novērtēšanai.

Pārbaudot, vai vietas direktīvas rindas nosacījums ir spēkā, vērtība ir atkarīga no attiecīgās vienības daudzuma, kas ir norādīts vietas direktīvas rindā. Katru reizi sasniedzot vietas direktīvas rindu, sistēma mēģina pārvērst pieprasījuma vienību uz rindā norādīto vienību. Ja mērvienības pārvēršana neeksistē, tā turpinās nākamajā rindā. 

### <a name="locate-quantity"></a>Novietot daudzumu

Šī opcija tiek izmantota tikai daudzuma izvietošanai/noteikšanai noliktavā. Tā ir paredzēta tikai izvietošanas darba veidam. Derīgās vērtības ir norādītas tālāk.

-   **Noliktavas vienības daudzums** — novērtējot, vai daudzums atbilst daudzuma diapazonam laukā “No” un “Uz", izmantojiet daudzumu, kas norādīts saņemtajai noliktavas vienībai.
-   **Izmantotais daudzums** — novērtējot, vai daudzums atbilst daudzuma diapazonam laukā “No” un “Uz", izmantojiet daudzumu, kas ir klasificētās konkrētās transakcijas laikā.
-   **Atlikušais daudzums** — novērtējot, vai daudzums atbilst daudzumam diapazonam laukā “No” un “Uz”, izmantojiet atlikušo daudzumu pašlaik pārbaudītajā pirkšanas pasūtījuma rindā.
-   **Paredzamais daudzums** — novērtējot, vai daudzums atbilst daudzumam diapazonam laukā “No” un “Uz”, izmantojiet kopējo daudzumu pirkšanas pasūtījuma rindā neatkarīgi no tā, kas jau ir saņemts.

### <a name="restrict-by-unit"></a>Ierobežot atbilstoši vienībai

Tas ļauj saistīt vietas direktīvas rindu ar vienu vai vairākām mērvienībām. Ja, rezervējot daudzumu, vēlaties rezervēt tikai paletes no konkrēta vietu kopuma, tad vidējā līmeņa režģa secība ierobežo šo īpašo secību ar “PL”, līdz ar to jebkurš daudzums, kas ir mazāks nekā viena palete, netiek atlasīts secībai. Lai iestatītu vienības, atlasiet **Ierobežot pēc vienības**. Rindai var noteikt vairāk nekā vienas vienības ierobežojumu. Tas darbojas tikai ar veida izdošanas vietas direktīvām. 

### <a name="round-up-to-unit"></a>Noapaļot uz augšu līdz vienībai

Šis lauks darbojas kopā ar lauku **Ierobežot pēc vienības**. Ja ir iestatīta vietas direktīvas rinda **Ierobežot pēc vienības** opcija “kaste”, atlasot opciju **Noapaļot līdz vienībai**, tiek norādīts, ka ārpus izejmateriālu izdošanas direktīvas ģenerēts darbs ir jānoapaļo ar precizitāti līdz vienai apstrādes vienībai (norādīta laukā **Ierobežot pēc vienības**). Ņemiet vērā, ka tas ir spēkā tikai izejmateriālu izdošanai un tikai ar veida izdošanas vietas direktīvām.

### <a name="locate-packing-qty"></a>Iepakojuma daudzuma meklēšana

Ja pārdošanas, pārsūtīšanas vai ražošanas pasūtījumā ir norādīts iepakojumu daudzums, sistēma var atlasīt tikai tas vietas, kur konkrētajā vietā ir iepakojuma daudzums. Tas darbojas tikai ar veida izdošanas vietas direktīvām.

### <a name="allow-split"></a>Atļaut sadalījumu

Tas norāda, vai vietas direktīva var sadalīt saņemto daudzumu vai daudzumu, kas ir rezervēts vairāku noliktavu vietās, vai arī visam daudzumam jāatrodas vienā vietā vai tas ir jārezervē no vienas vietas, lai varētu izveidot darbu. 

### <a name="sequence-number"></a>Sērijas numurs

Šis skaitlis norāda secību, kādā tiek apstrādāta atlasītā darba tipa novietojuma direktīva. Ja nepieciešams, šo secību varat mainīt. Tomēr, izmantojot secības numurus, ievērojiet piesardzību, jo apstrāde vienmēr tiek veikta noteiktā secībā. 

### <a name="name"></a>Vārds, uzvārds

Ievadiet vietas direktīvas darbības nosaukumu. Norādot nosaukumu, ievērojiet konkrētību.

### <a name="fixed-location-usage"></a>Fiksētā novietojuma lietojums 

-   **Fiksētas un nefiksētas vietas** — vietas direktīva ņem vēra visas vietas.
-   **Tikai fiksētas vietas precei** — vietas direktīva ņem vērā precēm tikai fiksētas vietas.
-   **Tikai fiksētas vietas preces variantam** — vietas direktīva ņem vērā preces variantiem tikai fiksētas vietas.

### <a name="allow-negative-inventory"></a>Atļaut negatīvu krājumu daudzumu

Atlasiet šo opciju, lai vietas direktīvās atļautu negatīvus krājumus norādītajā noliktavas vietā. 

### <a name="batch-enabled"></a>Partija iespējota. 

Atzīmējiet šo opciju, lai lietotu partijas stratēģijas krājumiem, kam ir iespējotas partijas. Ja ir sasniegta rinda, kurā opcijai **Partija iespējota** nav iestatīts neviens partija krājums, process pāriet uz nākamo darbības rindu. 

### <a name="strategy"></a>Stratēģija

-   **Konsolidēt** — šī stratēģija tiek izmantota, lai konsolidētu krājumus noteiktā vietā, ja jau ir pieejami līdzīgi krājumi. Tas darbojas tikai ar izvietošanas veida vietas direktīvu. Biežāk izvietošanas iestatīšanai izmanto konsolidēšanu pirmajā darbības rindā un pēc tam otrajā mēģinājumā izmanto izvietošanu bez konsolidācijas. Preču konsolidēšana padara efektīvāku vēlāku izdošanu.
-   **Saskaņo iepakojuma daudzumu** — šī stratēģija tiek izmantota, lai pārbaudītu, vai izdošanas vietā ir norādītais iepakojuma daudzums. Tas darbojas tikai ar veida izdošanas vietas direktīvu. 
-   **FEFO partijas rezervēšana** — šī stratēģija tiek izmantota, ja krājumi tiek novietoti, izmantojot partijas beigu datumu, un tiek piešķirti partijas rezervācijai. Šo stratēģiju var izmantot tikai krājumiem, kuriem iespējotas partijas. Tas darbojas tikai ar izdošanas darba veida vietas direktīvu. 
-   **Noapaļot uz augšu līdz pilnai NV** — šo stratēģiju izmanto krājumu daudzuma noapaļošanai, lai tas atbilstu noliktavas vienību (NV) daudzumam, kas ir piešķirts izdodamajiem krājumiem. Šo stratēģiju var izmantot tikai veida izdošanas vietas direktīvas papildināšanas veidam. 
-   **Tukša vieta bez ienākoša darba** — šo stratēģiju izmanto, lai atrastu tukšas vietas. Novietojums tiek uzskatīts par tukšu, ja tam nav fizisku krājumu un nav gaidāms ienākošais darbs. Šo stratēģiju izmanto tikai vietas direktīvas izvietošanas veidam. 

### <a name="example-of-the-use-of-location-directives"></a>Novietojuma direktīvas izmantošanas piemērs

Šajā piemērā ir aprakstīts pirkšanas pasūtījuma process, kur vietas direktīvai ir jāatrod brīva vieta noliktavā krājuma vienībām, kas ir tikko reģistrētas saņemšanas dokā. Vispirms ir jāatrod brīva vieta noliktavā, konsolidējot rīcībā esošos krājumus. Ja konsolidācija nav iespējama, tad ir jāatrod tukša vieta. 

Šādā gadījumā ir jādefinē divas vietas direktīvas darbības. Pirmajai darbībai secībā ir jāizmanto stratēģija **Konsolidēt** un otrajai vajadzētu izmantot stratēģiju **Tukšs novietojums bez ienākoša darba**. Ja tiek definēta trešā darbība pārpildes scenārija apstrādei, iespējami divi galarezultāti, kurā noliktavā vairs nav vietas: darbu var izveidot arī tad, ja nav definētas vietas, vai darba izveides process var neizdoties. Rezultātu nosaka iestatījumi lapā **Novietojuma direktīvas kļūmes**, kur varat izlemt, vai atlasīt opciju **Pārtraukt darbu, ja rodas ar novietojuma direktīvu saistīta kļūme** katram darba pasūtījuma tipam.
