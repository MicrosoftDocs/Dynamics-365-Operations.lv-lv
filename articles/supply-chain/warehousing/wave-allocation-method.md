---
title: Kopumu sadalījums
description: Šajā tēmā ir aprakstīts, kā iestatīt kopuma sadalījuma darbību, tostarp to, kā tam iespējot paralēlo apstrādi.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fd874f3c6c1f4d25b3257d6465686dcb8e95b933
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576020"
---
# <a name="wave-allocation"></a>Kopumu sadalījums

[!include [banner](../includes/banner.md)]

Kopuma apstrāde var būt laikietilpīga, un lielākā daļa apstrādes laika tiek pavadīta sadalījuma solī un darba izveides solī.

Tagad ir iespējams darbināt katru no šiem soļiem paralēli, kas var uzlabot kopuma apstrādes veiktspēju un ļaut lielāku kopumu caurlaidi tajā pašā noliktavā. Šajā tēmā skaidrots, kā iestatīt kopuma sadalījuma metodi paralēlai palaišanai. Papildinformāciju par to, kā iestatīt darba izveidi paralēlai palaišanai, skatiet sadaļā [Darba izveides plānošana kopuma laikā](configure-wave-schedule-work-creation.md).

Iepriekš bija iespējams piešķirt tikai vienu kopumu noliktavā vienlaicīgi. Šis ierobežojums ir noņemts un aizstāts ar jaunu ierobežojumu, kas bloķē tikai krājumu un dimensijas, kas atrodas virs novietojuma rezervāciju hierarhijā. Dimensijas virs novietojuma vienmēr ietver preču dimensijas. Piemēram, ja krājums ir konfigurēts, izmantojot *Krāsu*, tad varianti *Sarkans*, *Zils* un *Dzeltens* var tikt apstrādāti paralēli.

Tas nozīmē, ja vienu un to pašu krājumu, kam ir tādas pašas dimensijas virs novietojuma, piešķir viens kopums, citiem kopumiem jāgaida, lai iegūtu slēgu tam pašam krājumam un dimensijām. Ja bloķēšanu nevar iegūt laicīgi, radīsies kļūda un kopuma apstrāde neizdosies.

Lai izmantotu paralēlo apstrādi, kopumam ir jādarbojas partijā.

## <a name="performance-improvements"></a>Veiktspējas uzlabojumi

Paralēlās apstrādes veiktspējas priekšrocības ietilpst divās kategorijās:

- **Uzlabota caurlaide** - kopumu caurlaide parasti uzlabosies, pat ja paralēlā apstrāde nav konfigurēta, it īpaši scenārijos, kuros kopumos pārklājas krājumi.
- **Atsevišķa kopuma sadalījuma uzlabojums** — debitora datu pārbaude ir paralēlā 50% veiktspējas uzlabojums pēc pārslēgšanās uz paralēlo sadalījumu. Paralēlā apstrāde tiek veikta krājumiem un dimensijām virs novietojuma, tādējādi uzlabojumi ir atkarīgi no tā, cik dažādu krājumu ir kopums, pieejamā infrastruktūra un sadalījuma ilgums attiecībā pret darba izveides ilgumu.

## <a name="configure-parallel-allocation"></a>Konfigurēt paralēlu sadalījumu

### <a name="warehouse-management-parameters"></a>Noliktavas pārvaldības parametri

Lai izmantotu paralēlu sadalījuma apstrādi, dodieties uz **Noliktavas pārvaldība > Iestatījumi > Noliktavas pārvaldības parametri**, atveriet cilni **Kopuma apstrāde** un veiciet šādus iestatījumus:

- **Kopuma apstrādes partijas grupa** — atlasiet partijas grupu, kas jāizmanto sākotnējās laišanas darbību apstrādei. Tālāko sadalījuma apstrādi var veikt, izmantojot dažādas pakešuzdevumu grupas.
- **Veikt kopumiem pakešveida apstrādi** — iestatiet to kā *Jā*, lai izmantotu paralēlo apstrādi.
- **Gaidīt slēgu (ms)** - Ievadiet milisekundēs izteiktu laiku, cik ilgi sadalījuma darbībai ir jāgaida sistēmas resurss, kuru ir bloķējusi cita sadalījuma darbība. Kad šis laiks ir pagājis, kopums netiek apstrādāts un tiek parādīts kļūdas ziņojums. Ir ieteicams atļaut vismaz dažas sekundes, lai ļautu pabeigt vienas loģiskās vienības sadalījumu.

Papildinformāciju par šīm un citām kopuma apstrādes opcijām lapā **Noliktavas pārvaldības parametri** skatiet [Kopuma apstrādes noliktavas parametros](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Kopuma apstrādes metodes

Lai iestatītu paralēlo apstrādi:

1. Dodieties uz **Noliktavas pārvaldība > Iestatījumi > Kopumi > Kopuma procesa metodes**.
1. Atlasiet režģī `allocateWave` metodi.
1. Darbību rūtī atlasiet **Uzdevuma konfigurāciju**.
1. Tiek atvērta **Kopuma grāmatošanas metodes uzdevuma konfigurācijas** lapa. Šajā režģī ir uzskaitītas visas noliktavas, kurās metode ir `allocateWave` konfigurēta. Paralēlā apstrāde tiks izmantota tikai uzskaitītajām noliktavām. Izmantojiet darbību rūts pogas, lai pievienotu vai aizvācu noliktavas no režģa pēc nepieciešamības. 
1. Katrai noliktavai veiciet šādus iestatījumus:
    - **Maksimālais pakešuzdevumu skaits** - norādiet pakešuzdevumu skaitu, kas ir jāizmanto sadalījumam atlasītajā noliktavā. Optimālais pakešuzdevumu skaits ir atkarīgs no pieejamās infrastruktūras un citu pakešuzdevumu apstrādes serverī. Pārbaudes, kas veiktas četrās pamata vidēs, kas bija atvēlētas kopuma apstrādei, rādīja, ka astoņu uzdevumu izmantošana rada labākus rezultātus.
    - **Kopuma apstrādes partijas grupa** - noteiktas partijas grupas var izmantot atšķirīgām noliktavām, lai atļautu sadalījuma apstrādei samazināt pa noliktavām.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Iespējot vai atspējot paralēlošanu visām juridiskajām personām

Ieteicams iestatīt `allocateWave` metodi paralēlai palaišanai visām juridiskajām personām, jo tas palīdz uzlabot kopuma apstrādes veiktspēju. Tiek sākta Supply Chain Management versija 10.0.17, visām jaunajām un atjauninātām instalācijām pēc noklusējuma tiek aktivizēta *Kopuma paralēlās izmantošanas kopuma sadalīšanas metode*, un to nevar atkal izslēgt. Pēc šīs funkcijas iespējošanas ir šādas darbības:

- `allocateWave` metode tiek atjaunināta, lai ietvertu uzdevuma konfigurācijas iestatījumu, kas ļauj izmantot lapu **Kopuma apstrādes metodes**, lai definētu vienlaicīgi veicamo uzdevumu skaitu, kas ir vienāds ar paralēlo procesu skaitu. Tā rezultātā laiks, kas tiek izmantots iedalītā kopuma darbībā (kas parasti ir 30% līdz 60% no kopējā apstrādes laika) tiek samazināts par faktoru, kas aptuveni ir vienāds ar uzdevumu skaitu. Ir iespējams atlasīt arī to, kura pakete tiks piešķirta šo uzdevumu izpildei. Ir svarīgi atzīmēt, ka visas juridiskās personas tiks konfigurētas, lai paketes ietvaros apstrādātu kopumus. Noliktavām, kas jau ir konfigurētas, lai apstrādātu kopumus paketē, un noliktavām, kas jau ir konfigurētas `allocateWave` metodes izmantošanai paralēli, esošā konfigurācija tiks saglabāta.
- Pēc noklusējuma visas jaunās juridiskās personas ir konfigurētas, lai apstrādātu kopumus partijā. Visām jaunajām noliktavām, kurām ir iespējota **Noliktavas pārvaldības procesu** opcija, būs konfigurēta `allocateWave` metode paralēlai palaišanai pēc noklusējuma.
- Lapā **Noliktavas pārvaldības parametri** iestatījuma **Procesa saglabāšana partijā** ir iestatīta uz *Jā* un **Gaidīt slēgu (ms)** uz noklusējuma iestatījumu 15 sekundes. Tas nozīmē, ka visi kopumi tiks izpildīti partijā. Kad kopums darbojas, piešķiršanas posmā tas iegūst vienuma un izmēru slēdzeni virs atrašanās vietas. Kad nākamā laidiena apstrādes uzdevums mēģina iegūt vienu un to pašu slēdzeni identiskam ierakstam, tas tiek bloķēts līdz nākamās apstrādes beigām. Iestatījumi **Gaidīt slēgu (ms)** izveido maksimālo laiku, ko sistēma gaidīs, pirms slēgs tiks atbrīvots.

Lai izmantotu paralēlo apstrādi, kopumam ir jādarbojas partijā. Tāpēc jūs samazināsiet kopuma apstrādes veiktspēju, izslēdzot iestatījumu **Procesa saglabāšana partijā**, it īpaši, ja kopuma apstrāde izmanto paralēlu procesu, kā to nosaka uzdevumu konfigurācija attiecīgajām kopuma metodēm.

Ja nepieciešams, varat atsaukt katru iestatījumu, kas tika veikts pēc noklusējuma, kad instancei automātiski aktivizēta funkcionalitāte *Kopuma paralēlošana kopuma dalīšanas metodei*. Lai izpildītu šo darbību:

- Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**. Cilnē **Kopuma apstrāde** lietojiet vēlamās vērtības **Kopuma apstrādei partijā** un **Gaidīt bloķēšanu (ms)**.
- Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**. Atlasiet `allocateWave` metodi. Darbību rūtī atlasiet **Uzdevuma konfigurāciju**, lai atvērtu lapu ar katras noliktavas sarakstu, kur metode iestatīta paralēlai palaišanai. Ja nepieciešams, modificējiet vai dzēsiet pakešuzdevumu skaitu un katrai uzskaitītai noliktavai piešķirto kopuma grupu.

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="troubleshoot-using-the-infolog"></a>Problēmu novēršana, izmantojot informācijas žurnālu

Tā kā tiek izmantota partijas struktūra, kopuma apstrādes laikā radušās kļūdas tiks uztvertas kā daļa no pakešuzdevumiem Infologs. Lai lasītu ar lai kopumu saistītos pakešuzdevumus:

1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
1. Atlasiet kopumu, kuru vēlaties pārbaudīt.
1. Darbības rūtī atveriet cilni **Kopums** un grupā **Kopums** atlasiet **Pakešuzdevumi**.

Kopuma apstrāde ir pašlabošana, tādēļ par jebkādu apstrādes laikā konstatēto kļūdu ir jāziņo, izmantojot informācijas žurnālu.

Ar paralēlo apstrādi saistīta kļūda var būt tāda, ka divi kopumi mēģina piešķirt vienu krājumu vienlaicīgi, bet viens nav pabeigts, tādējādi cits kopums noteiktā laikā nevar iegūt bloķēšanu. Ja tāda ir, pakešuzdevumu žurnālā tiks ietverta informācija, kas norāda, ka krājuma bloķēšanu nav iespējams iegūt. Šādā gadījumā neveiksmīgais kopums ir jāapstrādā vēlreiz.

Tā kā apstrāde notiek paralēli, dati jāsaglabā dažādās tabulās, lai atsekotu apstrādes stāvokli. Tas nozīmē, ka pakešuzdevumu žurnālos var būt kļūdas, piemēram, atslēgas dublikātu kļūdas.

Pakešuzdevumu kļūdas ir arī daļa no pakešuzdevumu žurnāla. Svarīgākā informācija parasti ir apakšpusē.

Retos gadījumos, piemēram, ja SQL savienojums ir pabeigts, kopuma apstrādei ir iespējams beigties neatbilstīgā stāvoklī, kurā pakešuzdevums tiek palaists, bet apstrāde ir apturēta. Kopums nevar apstrādāt kļūdas šādi, tādēļ mēģinājums iztīrīt neizdevušos kopumus tiek veikts, kad tiek palaists nākamais kopums. Vai arī, ja pašreizējais kopums ir neatbilstīgā stāvoklī, veiciet šādas darbības:

1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
1. Atlasiet kopumu, kas jānotīra.
1. Darbības rūtī atveriet cilni **Kopums** un grupā **Kopums** atlasiet **Attīrīšanas kopuma dati**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Problēmu novēršana, izmantojot kopuma norises žurnālu

Ja **Noliktavas pārvaldības parametru** lapā ir iespējota opcija **Izveidot kopuma norises žurnālu**, tad žurnāla ieraksts tiek izveidots katru reizi, kad krājumam tiek sākta un beigta dimensija. Šis žurnāls jāiespējo tikai tad, kad tas ir nepieciešams, piemēram, sākotnējās testēšanas vai problēmu novēršanas laikā. Kad šī opcija ir aktivizēta, jūs variet skatīt žurnālu, veicot šādas darbības:

1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
1. Atlasiet kopumu, kuru vēlaties pārbaudīt.
1. Darbību rūts cilnē **Kopums**, grupā **Kopums** atlasiet **Progress**.
