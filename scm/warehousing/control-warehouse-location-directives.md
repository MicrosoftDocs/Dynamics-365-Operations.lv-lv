---
title: "Vadības noliktavas darbu, izmantojot darba veidnes un vieta direktīvām"
description: "Šajā rakstā aprakstīts, kā izmantot darba veidnes un novietojuma direktīvas, lai noteiktu, kā un kur darbs tiek veikts noliktavā."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 64bcea1f305d67c01967184596a58a48a002cf48
ms.lasthandoff: 03/31/2017


---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Vadības noliktavas darbu, izmantojot darba veidnes un vieta direktīvām

Šajā rakstā aprakstīts, kā izmantot darba veidnes un novietojuma direktīvas, lai noteiktu, kā un kur darbs tiek veikts noliktavā.

Instrukcijas, ko noliktavas darbinieki saņem mobilajā ierīcē, nosaka darba veidnes, kuras iestatāt programmā Microsoft Dynamics 365 for Operations, lai definētu dažādus noliktavas procesus un uzdevumus. Darba veidnes nosaka, kā darbs tiek veikts katram noliktavas procesam. Saistot novietojuma direktīvu ar darba veidnēm, var palīdzēt garantēt, ka darbs notiek noteiktās noliktavu fiziskās daļās.

## <a name="work-templates"></a>Darbu veidnes
Lapa **Darbu veidnes** ļauj definēt darba operācijas, kas jāveic noliktavā. Parasti, noliktavas darba operācijas sastāv no darbību pāra: noliktavas darbinieks paņem rīcībā esošos krājumus vienā novietojumā un pēc tam liek paņemtos krājumus citā novietojumā. 

Darba veidnes sastāv no virsraksta un saistītām rindām. Katra darba veidne ir paredzēta īpašam *darba pasūtījuma veidam*. Daudzi darba pasūtījuma tipi ir saistīti ar avota dokumentiem, piemēram, pirkšanas vai pārdošanas pasūtījumiem. Tomēr, citi darba pasūtījumu tipi veido atsevišķus noliktavas procesus, piemēram, cikla inventarizāciju. *Darbu kopu ID *ļauj organizēt darbu grupās. 

Iestatījumus darba virsraksta definīcijā var izmantot, lai noteiktu, kad jāizveido jauns darba gabals. Piemēram, var iestatīt maksimālo izdošanas rindu skaitu un maksimālo plānoto izdošanas laiku. Pēc tam, ja darbs pārdošanas pasūtījuma izdošanas procesam pārsniedz kādu no šīm vērtībām, šis darbs tiek sadalīts divos darba gabalos. 

Darba rindas attēlo fiziskos uzdevumus, kas ir nepieciešami, lai varētu apstrādāt darbu. Piemēram, izejošajam noliktavas procesam var būt darba rinda krājumu paņemšanai noliktavā un cita rinda šo krājumu novietošanai sagatavošanas zonā. Pēc tam var būt papildu rinda krājumu izdošanai no sagatavošanas posmiem un cita rinda krājumu ievietošanai kravas automašīnā iekraušanas procesa ietvaros. Varat iestatīt *direktīvas kodu *darba veidnes rindās. Direktīvas kods ir saistīts ar novietojuma direktīvu un tāpēc palīdz nodrošināt, ka noliktavas darbs tiek apstrādāts pareizā novietojumā noliktavā. 

Vaicājumu var iestatīt, lai kontrolētu, kad tiek izmantota konkrētā darba veidne. Piemēram, var iestatīt ierobežojumu, lai noteiktu veidni varētu izmantot darbam tikai noteiktā noliktavā. Vai arī var būt vairākas veidnes, kas tiek izmantotas, lai izveidotu darbu izejošā pārdošanas pasūtījuma apstrādei atkarībā no pārdošanas izcelsmes. Sistēma izmanto **kārtas numurs** lauku, lai noteiktu kārtību, kādā tiek novērtētas veidnes pieejamos darba. Tādēļ, ja jums ir ļoti konkrētu vaicājumu par konkrētu darbu veidni, jums ir jāsniedz tas zemas kārtas numurs. Pēc tam šis vaicājums tiks novērtēts pirms citiem, vispārīgākiem vaicājumiem. 

Lai apturētu vai pauzētu darba procesu, var izmantot iestatījumu **Pārtraukt darbu** darba rindā. Tādā gadījumā, darbiniekam, kurš veic darbu, netiks lūgts veikt nākamās darba rindas darbību. Lai pārietu uz nākamo darbību, šim darbiniekam vai citam darbiniekam jāatlasa darbs vēlreiz. Varat arī atdalīt uzdevumus darba gabalā, izmantojot citu *darba klases ID *darba veidnes rindās.

## <a name="location-directives"></a>Novietojuma direktīvas
Novietojuma direktīvas ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Piemēram, pārdošanas pasūtījuma transakcijā novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti. Novietojuma direktīvas sastāv no virsraksta un saistītām rindām un tās izveido lapā **Novietojuma direktīvas**. 

Virsrakstā katrai novietojuma direktīvai jābūt saistītai ar *darba pasūtījuma tipu*, kas norāda krājumu transakcijas tipu, kas tiks izmantots direktīvai, piemēram, pārdošanas pasūtījumus, papildināšanu vai izejmateriālu izdošanu. *Darba tips *norāda, vai novietojuma direktīva tiks izmantota izdošanas vai nodošanas darbam vai citam noliktavas procesam, piemēram, inventarizācijai vai krājumu statusa izmaiņām. Jānorāda arī *vietne *un *noliktava*. *Direktīvas kodu*, ko norādāt virsrakstā, var izmantot, lai saistītu novietojuma direktīvu ar vienu vai vairākām darba veidnēm. 

Attiecībā uz darba veidnēm, varat iestatīt vaicājumu, lai noteiktu, kad tiek izmantota konkrēta novietojuma direktīva. Piemēram, varat norādīt ka tad, kad pārdošanas pasūtījuma izcelsme ir e-komercija, krājums ir jāizdod no atvēlētās zonas noliktavā. Sistēma izmanto lauku **Secības numurs**, lai noteiktu secību, kādā tiek novērtētas pieejamas novietojuma direktīvas. 

Novietojuma direktīvas rindas iestata papildu ierobežojumus attiecībā uz novietojuma meklēšanas noteikumu lietošanu. Varat norādīt minimālo daudzumu un maksimālo daudzumu, kuram direktīva jāpiemēro, kā arī varat norādīt, ka direktīvai jābūt paredzētai noteiktai krājuma vienībai. Piemēram, ja mērvienība ir paletes, krājumus paletēs var izvietot konkrētā novietojumā. Var arī norādīt, vai daudzumu var sadalīt starp vairākiem novietojumiem. Tāpat kā novietojuma direktīvas virsraksts katrai novietojuma direktīvas rindai ir sērijas numurs, kas nosaka secību, kādā rindas tiek novērtētas. 

Novietojuma direktīvām ir viens papildu detalizācijas līmenis: *novietojuma direktīvas darbības*. Var definēt vairākas novietojuma direktīvas darbības katrai rindai. Vēlreiz, kārtas numurs tiek izmantota, lai noteiktu kārtību, kādā darbības tiek novērtētas. Šajā līmenī, lai noteiktu, kā atrast vislabāko vietu noliktavā var iestatīt vaicājumu. Varat arī izmantot iepriekš definētus **Stratēģijas **iestatījumus, lai atrastu optimālu novietojumu.

### <a name="example-of-the-use-of-location-directives"></a>Novietojuma direktīvas izmantošanas piemērs

Šajā piemērā mēs apsvērsim pirkšanas pasūtījuma procesu, kur novietojuma direktīvai ir jāatrod brīva vieta noliktavā krājumiem, kas tikko reģistrēti saņemšanas dokā. Pirmkārt, mēs vēlamies mēģināt atrast brīvu vietu noliktavā, apvienojot rīcībā esošos krājumus. Ja konsolidācija nav iespējama, tad vēlamies atrast tukšu novietojumu. 

Lai izmantotu šo scenāriju, mums jādefinē divas novietojuma direktīvas darbības. Pirmajai darbībai secībā ir jāizmanto stratēģija **Konsolidēt** un otrajai vajadzētu izmantot stratēģiju **Tukšs novietojums bez ienākoša darba**. Ja mēs noteiksim trešo darbību pārpildes scenārija apstrādei, ir iespējami divi rezultāti, kad noliktavā vairs nav vietas: darbu var izveidot pat tad, ja nav definēti novietojumi, vai darba izveides process var neizdoties. Rezultātu nosaka iestatījumi lapā **Novietojuma direktīvas kļūmes**, kur varat izlemt, vai atlasīt opciju **Pārtraukt darbu, ja rodas ar novietojuma direktīvu saistīta kļūme** katram darba pasūtījuma tipam.


