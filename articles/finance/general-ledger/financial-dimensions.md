---
title: Finanšu dimensijas
description: Šajā tēmā ir aprakstīti dažādie finanšu dimensiju tipi un izskaidrots, kā tie tiek iestatīti.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0715d3e4e4cb167c55d9c7d98cdf599187bf3b43
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178804"
---
# <a name="financial-dimensions"></a>Finanšu dimensijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidroti dažādie finanšu dimensiju tipi un izskaidrots, kā tie tiek iestatīti.

Izmantojiet lapu **Finanšu dimensijas**, lai izveidotu finanšu dimensijas, ko varat izmantot kā kontu segmentus kontu plānos. Ir divu veidu finanšu dimensijas: pielāgotas dimensijas un uz elementu balstītas dimensijas. Pielāgotās dimensijas tiek kopīgi izmantotas dažādās juridiskajās personās, un to vērtības ievada un uztur lietotāji. Attiecībā uz elementu balstītajām dimensijām to vērtības sistēmā tiek definētas kaut kur citur, piemēram, elementā Klienti vai Veikali. Dažas uz elementu balstītas dimensijas tiek kopīgi izmantotas dažādās juridiskajās personās, bet citas uz elementu balstītas dimensijas ir paredzētas tikai noteiktam uzņēmumam.

Kad esat izveidojis finanšu dimensijas, izmantojiet lapu **Finanšu dimensiju vērtības**, lai katrai finanšu dimensijai piešķirtu papildu rekvizītus.

Finanšu dimensijas varat izmantot, lai attēlotu juridiskās personas. Programmā Dynamics 365 Finance nav jāveido juridiskās personas. Taču finanšu dimensijas nav paredzēts izmantot, lai risinātu juridisko personu operāciju vai biznesa prasības. Starpvienību uzskaites funkcionalitāte programmā Finance ir paredzēta darbam tikai ar katras transakcijas ietvaros izveidotajiem uzskaites ierakstiem.

Pirms finanšu dimensijas iestatāt kā juridiskas personas, nosakiet, vai šie iestatījumi ir piemēroti jūsu organizācijai, novērtējot savas uzņēmējdarbības procesus tālāk norādītajās jomās.

- Krājums
- Pārdošanas un pirkšanas darījumi starp finanšu dimensijām un juridiskām personām
- PVN aprēķins un pārskatu izveide
- Operāciju pārskatu izveide

Lūk, daži no ierobežojumiem.

- PVN funkcijas var lietot tikai juridiskām personām, nevis finanšu dimensijām.
- Dažos pārskatos finanšu dimensijas nav ietvertas. Tādēļ, lai ziņotu pēc finanšu dimensijas, jums, iespējams, ir jāmodificē pārskati.

## <a name="custom-dimensions"></a>Pielāgotas dimensijas

Lai izveidotu lietotāja definētu finanšu dimensiju, laukā **Izmantot vērtības no** atlasiet opciju **Pielāgota dimensija**.

Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku. Varat ievadīt rakstzīmes, kas paliek tādas pašas katrai dimensijas vērtībai, piemēram, burtus vai defisi (-). Numura zīmes (\#) un zīmes (&) var ievadīt arī kā to rakstzīmju vietturus, kuras mainīsies ikreiz, izveidojot dimensijas vērtību. Numura zīmi (\#) izmantojiet kā vietturi cipariem un zīmi & izmantojiet kā vietturi burtiem. Formāta maskas lauks ir pieejams tikai tad, ja laukā **Izmantot vērtības no** ir atlasīta opcija **Pielāgota dimensija**.

**Piemērs**

Lai dimensijas vērtību noteiktu kā burtus “CC” un trīs ciparus, kā formāta maska ir jāieraksta **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Uz elementu balstītas dimensijas

Lai izveidotu uz elementu balstītu finanšu dimensiju, laukā **Izmantot vērtības no** atlasiet sistēmas definētu elementu, uz kuru balstīt šo finanšu dimensiju. Pēc tam finanšu dimensijas vērtības tiek veidotas no šī elementa. Piemēram, lai izveidotu dimensiju vērtības projektiem, atlasiet vienumu **Projekti**. Pēc tam dimensijas vērtība tiek izveidota katram projekta nosaukumam. Lapā **Finanšu dimensiju vērtības** tiek rādītas vērtības šim elementam. Ja šīs vērtības ir atkarīgas no uzņēmuma, tad lapā tiek rādīts arī uzņēmums.

## <a name="activating-dimensions"></a>Dimensiju aktivizēšana

Kad aktivizējat kādu finanšu dimensiju, tabula tiek atjaunināta tā, lai tajā būtu ietverts finanšu dimensijas nosaukums. Dzēstās dimensijas tiek noņemtas. Dimensiju vērtības varat ievadīt, pirms aktivizējat kādu finanšu dimensiju. Taču finanšu dimensiju nekur nevar patērēt, kamēr tā nav aktivizēta. Jūs nevarat finanšu dimensiju, piemēram, pievienot konta struktūrai, kamēr šī finanšu dimensija nav aktivizēta. Atlasot opciju **Aktivizēt**, visas dimensijas tiek atjauninātas un tiek parādītas statusa izmaiņas.

## <a name="translations"></a>Tulkojumi

Lapā **Teksta tulkojums** atlasītajai finanšu dimensijai varat ievadīt tekstu dažādās valodās. Lapā **Galvenā konta tulkojums** attiecīgajam galvenajam kontam varat ievadīt tekstu dažādās valodās. 

## <a name="legal-entity-overrides"></a>Juridiskas personas prioritātes

Ne visas dimensijas ir derīgas visām juridiskajām personām. Turklāt dažas dimensijas var attiekties tikai uz noteiktu periodu. Tādos gadījumos varat izmantot sadaļu **Juridiskas personas prioritātes**, lai norādītu uzņēmumus, attiecībā uz kuriem šī dimensija ir jāaiztur, kā arī īpašnieku un periodu, kad šī dimensija ir aktīva.

## <a name="deleting-financial-dimensions"></a>Finanšu dimensiju dzēšana

Lai palīdzētu uzturēt atsauču datu integritāti, finanšu dimensijas dzēst ir iespējams reti. Ja mēģināt dzēst kādu finanšu dimensiju, tiek izvērtēti tālāk norādītie kritēriji.

- Vai šī finanšu dimensija ir izmantota kādā iegrāmatotā un neiegrāmatotā transakcijā vai kādā dimensiju vērtību kombinācijā?
- Vai šī finanšu dimensija ir izmantota kādā aktīvā konta struktūrā, papildu kārtulas struktūrā vai finanšu dimensiju kopā?
- Vai šī finanšu dimensija veido daļu no noklusējuma finanšu dimensiju integrācijas formāta?
- Vai šī finanšu dimensija ir iestatīta kā noklusējuma dimensija?

Ja finanšu dimensija atbilst kādam no šiem kritērijiem, tad šo finanšu dimensiju nevar izdzēst.

## <a name="default-dimension-values"></a>Noklusējuma dimensijas vērtības

Šablona ierakstu vērtības, piemēram, debitoru un kreditoru, var izmantot kā noklusējuma vērtības jaunās dimensijās. Ja tiek izveidotas jaunas dimensijas, šablona ieraksta ID tiek ievadīts šo šablona ierakstu dimensijas vērtībās. Piemēram, izveidojot jaunu debitoru, debitora ID tiek ievadīts debitora dimensijā. Izveidojot pārdošanas pasūtījumus, rēķinus vai citus dokumentus, kuros ir jānorāda debitora ID, tiek izmantotas esošās noklusējuma kārtulas un dokumentos tiek pievienots debitora ID.

Šo līdzekli kontrolē dimensijas iestatījums. Šī iestatījuma nosaukums ir **Kopēt vērtības uz šo dimensiju katrā no jauna izveidotājā vienumā DimensionName**, kur **DimensionName** ir dimensijas nosaukums. Pēc noklusējuma līdzeklis ir izslēgts. Tomēr to var ieslēgt jebkurā laikā.

Ja ieraksti dimensijai jau pastāv, šablona ieraksti tiek atjaunināti, aktivizējot līdzekli. Tomēr esošie dokumenti un transakcijas netiek atjauninātas.

Ja izmantojat veidni, lai izveidotu šablona ierakstu, raugieties, lai šablona dimensijas veidnes vērtība būtu tukša. Piemēram, ja veidojat debitoru, izmantojot veidni, raugieties, lai debitora dimensijas vertība veidnē būtu tukša. Veidojot jauno debitoru, debitora dimensijas noklusējuma vērtība tiks ņemta no jaunā debitora numura.  

## <a name="derived-dimensions"></a>Atvasinātās dimensijas

Dimensiju var konfigurēt tā, lai, ievadot šo dimensiju dokumentā, tiek automātiski ievadīta informācija par citām dimensijām. Piemēram, ja tiek ievadīts izmaksu centrs 10, vērtību **20** var automātiski ievadīt nodaļas dimensijā.

Dimensiju lapā var iestatīt atvasinātās vērtības.

1. Atlasiet dimensiju un pēc tam atlasiet **Atvasinātās dimensijas**.

    Lapā **Atvasinātas dimensijas** ir ietverts režģi. Atlasītās dimensijas segments ir šī režģa pirmā kolonna.

2. Pievienojiet atvasināmos segmentus. Katrs segments tiek parādīts kā kolonna.

Ievadiet dimensiju kombinācijas, kas ir jāatvasina no dimensijas pirmajā kolonnā. Piemēram, lai varētu izmantot izmaksu centru kā dimensiju, no kuras ir atvasināta nodaļa un vieta, ievadiet izmaksas centra vērtību 10, nodaļas vērtību 20 un vietas vērtību 30. Pēc tam, ievadot izmaksu centru 10 šablona ierakstā vai transakciju lapā, nodaļa 20 un vieta 30 tiek ievadīta pēc noklusējuma.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Esošu vērtību pārrakstīšana ar atvasinātām dimensijām
 
Pēc noklusējuma atvasinātās dimensijas process nepārraksta atvasināto dimensiju esošās vērtības. Piemēram, ja ievada izmaksu centru 10 un citas dimensijas netiek ievadītas, pēc noklusējuma tiek ievadīta nodaļas 20 un vieta 30. Tomēr, ja izmaksu centrs tiek mainīts, jau izveidotās vērtības netiek mainītas. Tāpēc šablona ierakstos var izveidot noklusējuma dimensijas, un atvasinātās dimensijas šīs dimensijas neizmaina.

Varat mainīt atvasināto dimensiju uzvedību, lai tās pārrakstītu esošās vērtības, atzīmējot izvēles rūtiņu **Aizstāt esošās dimensiju vērtības ar atvasinātajām vērtībām** lapā **Atvasinātās dimensijas**. Ja šis lauks ir atlasīts, varat ievadīt dimensiju ar atvasinātām dimensiju vērtībām, un šīs atvasinātās dimensiju vērtības pārrakstīs visas jau pastāvošās vērtības. Izmantojot iepriekšējo piemēru — ja ievadāt izmaksu centru 10 un netiek ievadīta neviena cita dimensija, pēc noklusējuma tiek ievadīta nodaļa 20 un novietojums 30. Taču, ja vērtības jau bija nodaļa 50 un novietojums 60, šīs vērtības tagad tiek mainītas uz nodaļu 20 un novietojumu 30.
 
Atvasinātās dimensijas ar šo iestatījumu automātiski neaizstāj esošās noklusējuma dimensiju vērtības, kad dimensiju vērtības tiek iestatītas uz noklusējuma vērtībām. Dimensiju vērtības tiek pārrakstītas tikai tad, kad ievadāt jaunu dimensijas vērtību tādā lapā, kur šai dimensijai lapā jau pastāv atvasinātās vērtības.

### <a name="preventing-changes-with-derived-dimensions"></a>Izmaiņu novēršana ar atvasinātām dimensijām
 
Kad izmantojat komandu **Pievienot segmentu** lapā **Atvasinātās dimensijas**, lai kādu segmentu pievienotu kā atvasinātu dimensiju, lapas **Pievienot segmentu** apakšā tiek piedāvāta opcija, kas ļauj jums nepieļaut izmaiņas šai dimensijai, kad tā tik atvasināta kādā lapā. Pēc noklusējuma šī opcija ir izslēgta, tāpēc netiek novērsta atvasināto dimensiju vērtību mainīšana. Mainiet šo iestatījumu uz **Jā**, ja vēlaties novērst šīs dimensijas mainīšanu pēc tās atvasināšanas. Piemēram, ja dimensijas Nodaļa vērtība tiek atvasināta no dimensijas Izmaksu centrs vērtības, vērtību Nodaļa nevar mainīt, ja iestatījums **Novērst izmaiņas** ir **Jā**. 
 
Šis iestatījums nenovērš izmaiņu veikšanu, ja dimensijas vērtība ir derīga, bet nav uzskaitīta atvasināto dimensiju sarakstā. Piemēram, ja Nodaļa 20 tiek atvasināta no Izmaksu centrs 10 un ievadāt Izmaksu centrs 10, vairs nevar rediģēt Nodaļa 20. Taču, ja ievadāt Izmaksu centrs 20 un šī vērtība nav atvasināto dimensiju sarakstā vienumam Izmaksu centrs, vērtību Nodaļa varat rediģēt. 
 
Visos gadījumos konta vērtība un visas dimensiju vērtības joprojām tiks validētas attiecībā pret kontu struktūrām pēc tam, kad ir lietotas atvasināto dimensiju vērtības. Ja izmantojat atvasinātās dimensijas un to validēšana ir nesekmīga, kad šīs dimensijas tiek lietas lapā, ir jāmaina atvasināto dimensiju vērtības atvasināto dimensijas lapā, lai tās varētu izmantot transakcijās. 
 
Kad maināt dimensijas kopsavilkuma cilnē **Finanšu dimensijas**, nevar rediģēt dimensiju, kas ir atzīmēta izmaiņu novēršanai. Ja kontu un dimensijas ievadāt lapas segmentētā ieraksta vadīklā, šīs dimensijas var rediģēt. Taču, kad izcēlumu pārvietojat prom no segmentētā ieraksta vadīklas un to pārvietojat uz citu lauku vai veicat kādu darbību, šis konts un dimensijas tiek validētas attiecībā pret atvasināto dimensiju sarakstu un kontu struktūrām, lai pārliecinātos, ka ievadāt atbilstošās vērtības. 

### <a name="derived-dimensions-and-entities"></a>Atvasinātās dimensijas un elementi

Atvasināto dimensiju segmentus un vērtības var iestatīt, izmantojot elementus.

- Atvasināts dimensijas elements iestata vadošo dimensiju un segmentus, kurus izmanto šīm dimensijām.
- Elements Atvasināto dimensiju vērtība ļauj importēt vērtības, kuras ir jāatvasina katrai vadošajai dimensijai.

Ja elementu tiek izmantots datu importēšanai un šis elements importē dimensijas, importēšanas laikā stājas spēkā atvasinātās dimensijas kārtulas, ja vien elements īpaši neignorē šīs dimensijas.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Finanšu dimensiju definēšana](tasks/define-financial-dimensions.md)
- [Finanšu dimensijas noklusējuma veidņu uzturēšana](tasks/maintain-financial-dimension-default-templates.md)
