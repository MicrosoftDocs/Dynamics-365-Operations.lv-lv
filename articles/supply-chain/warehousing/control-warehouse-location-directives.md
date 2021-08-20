---
title: Kontrolēt noliktavas darbu, izmantojot darbu veidnes un novietojuma direktīvas
description: Šajā tēmā ir sniegta informācija par to, kā izmantot darba veidnes un vietas direktīvas, lai noteiktu, kā un kur darbs tiek veikts noliktavā.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7e955fba12e963a443c0304f0a8a0e395c46909dd34de12cd51fa9788491786
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770148"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Kontrolēt noliktavas darbu, izmantojot darbu veidnes un novietojuma direktīvas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par to kā izmantot darba veidnes un vietas direktīvas, lai noteiktu, kā un kur darbs tiek veikts noliktavā.

Tas, kādas instrukcijas noliktavas darbinieki saņem mobilajā ierīcē, ir atkarīgs no darba veidnēm, kuras iestatāt programmā Dynamics 365 Supply Chain Management, lai definētu dažādos noliktavas procesus un uzdevumus. Darba veidnes nosaka, kā darbs tiek veikts katram noliktavas procesam. Saistot novietojuma direktīvu ar darba veidnēm, var palīdzēt garantēt, ka darbs notiek noteiktās noliktavu fiziskās daļās.

## <a name="work-templates"></a>Darbu veidnes

Lapa **Darbu veidnes** ļauj definēt darba operācijas, kas jāveic noliktavā. Parasti, noliktavas darba operācijas sastāv no darbību pāra: noliktavas darbinieks paņem rīcībā esošos krājumus vienā novietojumā un pēc tam liek paņemtos krājumus citā novietojumā. 

Darba veidnes sastāv no virsraksta un saistītām rindām. Katra darba veidne ir paredzēta īpašam *darba pasūtījuma veidam*. Daudzi darba pasūtījuma tipi ir saistīti ar avota dokumentiem, piemēram, pirkšanas vai pārdošanas pasūtījumiem. Tomēr, citi darba pasūtījumu tipi veido atsevišķus noliktavas procesus, piemēram, cikla inventarizāciju. *Darbu kopu ID* ļauj organizēt darbu grupās. 

Iestatījumu izmantošana darba virsraksta definīcijā, lai noteiktu, kad jāizveido jauns darba gabals. Piemēram, var iestatīt maksimālo izdošanas rindu skaitu un maksimālo plānoto izdošanas laiku. Pēc tam, ja darbs pārdošanas pasūtījuma izdošanas procesam pārsniedz kādu no šīm vērtībām, šis darbs tiek sadalīts divos darba gabalos.

Izmantojiet pogu **Darba virsraksta pārtraukumi**, lai definētu, kad sistēmai jāizveido jaunus darba virsrakstus. Piemēram, lai izveidotu darba virsrakstu katram _pasūtījuma numuram_, darbības rūtī atlasiet **Rediģēt vaicājumu** un pēc tam pievienojiet lauku **Pasūtījuma numurs** vaicājumu redaktora cilnei **Kārtošana**. Lauki, kas ir pievienoti cilnei **Kārtošana**, ir pieejami atlasei kā *grupēšanas lauki*. Lai iestatītu grupēšanas laukus, darbības rūtī atlasiet **Darba virsraksta pārtraukumi** un pēc tam katram laukam, kuru vēlaties izmantot kā grupēšanas lauku, atzīmējiet izvēles rūtiņu kolonnā **Grupēt pēc ša lauka**.

Darba rindas attēlo fiziskos uzdevumus, kas ir nepieciešami, lai apstrādātu darbu. Piemēram, izejošajam noliktavas procesam var būt viena darba rinda krājumu paņemšanai noliktavā un cita rinda šo krājumu novietošanai sagatavošanas zonā. Pēc tam var būt papildu rinda krājumu izdošanai no sagatavošanas posmiem un cita rinda krājumu ievietošanai kravas automašīnā iekraušanas procesa ietvaros. Varat iestatīt *direktīvas kodu* darba veidnes rindās. Direktīvas kods ir saistīts ar novietojuma direktīvu un tāpēc palīdz garantēt, ka noliktavas darbs tiek apstrādāts pareizā novietojumā noliktavā.

Vaicājumu var iestatīt, lai kontrolētu, kad tiek izmantota konkrētā darba veidne. Piemēram, var iestatīt ierobežojumu, lai noteiktu veidni varētu izmantot darbam tikai noteiktā noliktavā. Vai arī var būt vairākas veidnes, kas izveido darbu izejošā pārdošanas pasūtījuma apstrādei atkarībā no pārdošanas izcelsmes. Lai noteiktu secību, kādā tiek novērtētas pieejamās darbu veidnes, sistēma izmanto lauku **Kārtas numurs**. Tādēļ, ja jums ir ļoti konkrēts vaicājums konkrētai darba veidnei, tam ir jāpiešķir zems kārtas numurs. Pēc tam šis vaicājums tiks novērtēts pirms citiem, vispārīgākiem vaicājumiem.

> [!NOTE]
> Lai neļautu sistēmai automātiski pārrakstīt darba veidnes *secības numurus* pēc veidnes dzēšanas, ieslēdziet līdzekli *Dzēšot, saglabāt darba veidnes secības numurus* sadaļā [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Lai apturētu vai pauzētu darba procesu, var izmantot iestatījumu **Pārtraukt darbu** darba rindā. Tādā gadījumā, darbiniekam, kurš veic darbu, netiks lūgts veikt nākamās darba rindas darbību. Lai pārietu uz nākamo darbību, šim darbiniekam vai citam darbiniekam jāatlasa darbs vēlreiz. Varat arī atdalīt uzdevumus darba gabalā, izmantojot citu *darba klases ID* darba veidnes rindās.

## <a name="location-directives"></a>Novietojuma direktīvas

Novietojuma direktīvas ir nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Piemēram, pārdošanas pasūtījuma transakcijā novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti. Novietojuma direktīvas sastāv no virsraksta un saistītām rindām un tās izveido lapā **Novietojuma direktīvas**.

Virsrakstā katrai novietojuma direktīvai jābūt saistītai ar *darba pasūtījuma tipu*, kas norāda krājumu transakcijas tipu, kas tiks izmantots direktīvai, piemēram, pārdošanas pasūtījumus, papildināšanu vai izejmateriālu izdošanu. *Darba tips* norāda, vai novietojuma direktīva tiks izmantota izdošanas vai nodošanas darbam vai citam noliktavas procesam, piemēram, inventarizācijai vai krājumu statusa izmaiņām. Jānorāda arī *vietne* un *noliktava*. *Direktīvas kodu*, ko norādāt virsrakstā, var izmantot, lai saistītu novietojuma direktīvu ar vienu vai vairākām darba veidnēm. 

Attiecībā uz darba veidnēm, varat iestatīt vaicājumu, lai noteiktu, kad tiek izmantota konkrēta novietojuma direktīva. Piemēram, varat norādīt ka tad, kad pārdošanas pasūtījuma izcelsme ir e-komercija, krājums ir jāizdod no atvēlētās zonas noliktavā. Sistēma izmanto lauku **Secības numurs**, lai noteiktu secību, kādā tiek novērtētas pieejamas novietojuma direktīvas.

Novietojuma direktīvas rindas iestata papildu ierobežojumus attiecībā uz novietojuma meklēšanas noteikumu lietošanu. Varat norādīt minimālo daudzumu un maksimālo daudzumu, kuram direktīva jāpiemēro, kā arī varat norādīt, ka direktīvai jābūt paredzētai noteiktai krājuma vienībai. Piemēram, ja mērvienība ir paletes, krājumus paletēs var izvietot konkrētā novietojumā. Var arī norādīt, vai daudzumu var sadalīt starp vairākiem novietojumiem. Tāpat kā novietojuma direktīvas virsraksts katrai novietojuma direktīvas rindai ir sērijas numurs, kas nosaka secību, kādā rindas tiek novērtētas.

Novietojuma direktīvām ir viens papildu detalizācijas līmenis: *novietojuma direktīvas darbības*. Var definēt vairākas novietojuma direktīvas darbības katrai rindai. Un atkal — kārtas numurs tiek izmantots, lai noteiktu secību, kādā darbības tiek novērtētas. Šajā līmenī varat iestatīt vaicājumu, lai definētu, kā atrast vislabāko novietojumu noliktavā. Varat arī izmantot iepriekš definētus **Stratēģijas** iestatījumus, lai atrastu optimālu novietojumu.

Plašāku informāciju par atrašanās vietas direktīvu izveidošanu un konfigurēšanu skatiet šeit: [Novietojuma direktīvas izveide](create-location-directive.md).

### <a name="how-location-directives-work"></a>Kā darbojas atrašanās vietas direktīvas

Atrašanās vietas direktīvas nosaka, *kur* krājumi jāizdod un *kur* tie jāievieto. Sistēma izvērtē atrašanās vietas direktīvu attiecībā uz katru darba rindu un pēc tam atlasa atrašanās vietu, pamatojoties uz detalizētu informāciju par darba rindu. Sistēma vispirms atrod visas atrašanās vietas direktīvas, kas atbilst noteiktai darba rindai (piemēram, tās ir paredzētas pareizai noliktavai un atbilst vaicājumam). Pēc tam tā secīgi izvērtē atrastās direktīvas.

> [!NOTE]
> Ir īpaši gadījumi, kad izdošanas vieta vai izvietošanas vieta ir iepriekš atlasīta. Piemēram, _pirkšanas reģistrācijas_ laikā pirmā izdošana vienmēr ir no atrašanās vietas, kur notiek reģistrācija. Cits piemērs ir *krājumu kustība pēc veidnes*, kur noliktavas darbinieks atlasa izdošanas vietu, un tikai izvietošanas vietas tiek atrastas, izmantojot novietojumu direktīvas.

## <a name="additional-resources"></a>Papildu resursi

- Video: [Noliktavas pārvaldības konfigurācija Deep Dive](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Palīdzības tēma: [Darbs ar novietojuma direktīvām](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]