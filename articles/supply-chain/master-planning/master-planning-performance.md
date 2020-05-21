---
title: Vispārējās plānošanas veiktspējas uzlabošana
description: Šajā tēmā ir paskaidrotas dažādas opcijas, kas var palīdzēt uzlabot vispārējās plānošanas veiktspēju vai novērst problēmas.
author: t-benebo
manager: tfehr
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: fa8426c3a1f19f8607f45e9ac4d57300abddb161
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323650"
---
# <a name="improve-master-planning-performance"></a>Vispārējās plānošanas veiktspējas uzlabošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrotas dažādas opcijas, kas var palīdzēt uzlabot vispārējās plānošanas veiktspēju vai novērst problēmas. Tajā ir ietverta informācija par parametriem un iestatījumiem, un par ieteicamajām konfigurācijām un darbībām. Tajā ietverts arī visu svarīgo parametru kopsavilkums, kuri jāņem vērā, kad ir ilgstoši vispārējās plānošanas darbi.

Šī tēma ir paredzēta sistēmas administratoriem vai IT lietotājiem, kuriem ir iespēja veikt problēmu novēršanu. Tā ir paredzēta arī ražošanas vai piegādes plānotājiem, jo tajā ir iekļauta informācija par parametriem, kas saistīti ar uzņēmējdarbības plānošanas prasībām. 

## <a name="parameters-related-to-master-planning-performance"></a>Parametri, kas saistīti ar vispārējās plānošanas veiktspēju

Vispārējās plānošanas izpildes laiku ietekmē dažādi parametri, un tie ir jāņem vērā.

### <a name="number-of-threads"></a>Pavedienu skaits

Parametrs **Pavedienu skaits** ļauj pielāgot vispārējās plānošanas procesu, lai palīdzētu uzlabot tā veiktspēju noteiktā datu kopā. Šis parametrs norāda kopējo pavedienu skaitu, kas tiks izmantoti vispārējās plānošanas izpildei. Tas izraisa vispārējās plānošanas izpildes paralelizēšanu, kas palīdz samazināt izpildes laiku. 

Varat iestatīt parametra **Pavedienu skaits** vērtību dialoglodziņā **Vispārējās plānošanas izpilde**. Lai atvērtu šo dialoglodziņu, pārejiet uz **Vispārējā plānošana \> Vispārējā plānošana \> Izpildīt \> Vispārējā plānošana** vai atlasiet vienumu **Izpildīt** darbvietā **Vispārējā plānošana**. Piemērotākā vērtība šim parametram ir jānosaka eksperimentāli. Tomēr, lai aprēķinātu sākotnējo vērtību, varat izmantot šādas formulas:

- **Ja strādājat ražošanas nozarē:** (Pavedienu skaits) = (Plānoto pasūtījumu skaits ÷ 1000)
- **Citos gadījumos:** (Pavedienu skaits) = (Krājumu skaits ÷ 1000)

Vispārējās plānošanas laikā izmantoto palīgu skaitam ir jābūt mazākam par vai vienādam ar maksimālo pakešapstrādes serverī atļauto pavedienu skaitu. Ja palīgu skaits pārsniedz pakešapstrādes servera pavedienu skaitu, papildu pavedieni neveic nekādas darbības.

> [!NOTE]
> Parametra **Pavedienu skaits** iestatīšana uz **0** (nulle) palielina vispārējās plānošanas izpildes laiku. Tādēļ ieteicams vienmēr iestatīt vērtību, kas ir lielāka par 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Uzdevumu skaits palīga uzdevumu komplektā

Mainot iestatījumu **Uzdevumu skaits uzdevumu komplektā** (t. i., komplekta lielumu), varat samazināt izpildes laiku. Šis iestatījums kontrolē krājumu skaitu, kuru kopīgu plānošanu veic viens palīgs.

Lapas **Vispārējās plānošanas parametri** (**Vispārējā plānošana \> Iestatījumi \> Vispārējās plānošanas parametri**) cilnes **Vispārīgi** sadaļā **Veiktspēja** var iestatīt parametru **Uzdevumu skaits uzdevumu komplektā**. Šī parametra piemērotākā vērtība ir atkarīga no jūsu datiem. Tādēļ ieteicams sākt ar vērtību **1**un pēc tam eksperimentālā ceļā noteikt piemērotāko vērtību jūsu iestatījumiem.

Parasti ir ieteicams palielināt uzdevumu skaitu, ja krājumu skaits ir ļoti liels (simtiem tūkstošu). Pretējā gadījumā ir jāsamazina uzdevumu skaits. Tālāk minētajām konkrētajām nozarēm ņemiet vērā šādus ieteikumus:

- Mazumtirdzniecības un izplatīšanas nozarēs, kur ir daudz neatkarīgu krājumu, izmantojiet daudzus palīgus, jo starp krājumiem nav atkarības. 
- Ražošanas nozarē, kur ir daudz materiālu komplektu (MK) un kopīgu apakškomponentu, izmantojiet mazāku palīgu skaitu, jo atkarības starp krājumiem var radīt gaidīšanas laikus.

> [!TIP]
> Ja radušās veiktspējas problēmas, ieteicams samazināt iestatījuma **Palīgu skaits uzdevumu komplektā** vērtību uz **1**. Pēc tam varat sākt eksperimentālā ceļā meklēt piemērotāko vērtību jūsu iestatījumiem. Parasti veiktspējas problēmas rodas, ja vienam krājumam apstrādei nepieciešams ilgāks nekā pārējiem krājumiem. Šādā gadījumā redzēsit, ka diviem secīgiem uzdevumi, kuriem ir statuss **Vajadzība** vispārējās plānošanas izpildē, ir nepieciešams ievērojami atšķirīgs laiks, lai tos izpildītu. Ārkārtējos gadījumos šī atšķirība var būt pat 30 minūtes. Uzdevumu izpildei nepieciešamo laiku var novērtēt, aplūkojot katra uzdevuma ilgumu.

### <a name="use-of-cache"></a>Kešatmiņas izmantošana

Parametrs **Kešatmiņas izmantošana** ļauj pielāgot vispārējās plānošanas procesu, lai palīdzētu uzlabot tā veiktspēju noteiktā datu kopā. Piemēram, varat pielāgot to, lai sasniegtu šādus rezultātus:

- Ja tiek izmantots lielāks kešatmiņas apjoms, atmiņā tiek apkopots vairāk datu. Paredzams, ka dati tiks izmantoti vēlāk vēlreiz. Ja dati ir atmiņā, jūs varat saglabāt dažus datu bāzu pieprasījumus. Tomēr, ja tiek izmantots lielāks kešatmiņas apjoms, pieaug atmiņas prasības.
- Ja tiek izmantots mazāks kešatmiņas apjoms, tos pašus datus var būt nepieciešams ienest no datu bāzes biežāk. Turklāt Application Object Server (AOS) visa procesa laikā saglabā atmiņā maz datu.

Ir grūti prognozēt, kura opcija būs labāka, jo katrs gadījums ir atkarīgs ne tikai no datiem, bet arī no aparatūras. Piemēram, tā kā mazāka kešatmiņas apjoma izmantošana izraisa papildu noslodzi datu bāzes serverī, nav vēlams izmantot šo opciju, ja datu bāzes serveris jau ir pārslogots.

Lapas **Vispārējās plānošanas parametri** (**Vispārējā plānošana \> Iestatījumi \> Vispārējās plānošanas parametri**) cilnes **Vispārīgi** sadaļā **Veiktspēja** var iestatīt parametru **Kešatmiņas izmantošana**. Kešdarbes efektivitāte lielā mērā ir atkarīga no klienta datiem. Piemēram, ja kešotie dati nekad nav vajadzīgi, jūs tikai nelietderīgi izmantojat atmiņu, glabājot datus līdz plānošanas procesa beigām. Šādā gadījumā, konfigurējot mazāku kešatmiņas izmantošanu, veiktspēja var palielināties, jo AOS ir nepieciešams mazāks atmiņas apjoms un servera resursi tiek atbrīvoti citiem uzdevumiem.

> [!TIP]
> Parasti ieteicams iestatīt parametram **Kešatmiņas izmantošana** opciju **Maksimāla**, jo šis parametrs ir paredzēts kā veiktspējas uzlabošanas līdzeklis. Ieteicams iestatīt parametram opciju **Minimāla**, ja lietojat to lokāli un ja ir ierobežota atmiņa (aptuveni 2 gigabaiti \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Pasūtījumu skaits apstiprināšanas komplektā

Parametrs **Pasūtījumu skaits apstiprināšanas komplektā** norāda kopējo pasūtījumu skaitu, ko vienlaicīgi apstrādās katrs pavediens/pakešuzdevums. Tas izraisa automātiskās apstiprināšanas procesa paralelizēšanu

Lapas **Vispārējās plānošanas parametri** (**Vispārējā plānošana \> Iestatījumi \> Vispārējās plānošanas parametri**) cilnes **Vispārīgi** sadaļā **Veiktspēja** var iestatīt parametru **Pasūtījumu skaits apstiprināšanas komplektā**. Automātiskās apstiprināšanas procesa paralelizēšana balstās uz pasūtījumiem, kuri jāapstrādā kopā. Piemēram, ja šim parametram ir iestatīta vērtība **50**, piemēram, katrs pavediens vai pakešuzdevums vienlaicīgi izvēlēsies 50 pasūtījumus un apstrādās tos kopā. Ieteicams noteikt piemērotāko vērtību eksperimentālā ceļā. Tomēr, lai aprēķinātu sākotnējo vērtību, varat izmantot šādu formulu:

(Pasūtījumu skaits komplektā) = (Pieprasījuma krājumu skaits ÷ Pavedienu skaits)

> [!NOTE]
> Iestatot parametram **Pasūtījumu skaits apstiprināšanas komplektā** vērtību **0** (nulle), nenotiks automātiskās apstiprināšanas procesa paralelizēšana. Viss process tiks izpildīts vienā pakešuzdevumā, un tam būs kopējs izpildes laiks. Tādēļ vispārējās plānošanas izpildes laiks palielināsies. Šī iemesla dēļ ieteicams iestatīt šim parametram vērtību, kas ir lielāka par **0** (nulli).

### <a name="time-fences"></a>Periodi

Periodi norāda, cik tālu nākotnē tiek veikti aprēķini un aprēķinātas dažādas prasības, izmantojot vispārējo plānošanu. Jo ilgāks ir periods, jo ilgāks laiks ir nepieciešams vispārējās plānošanas izpildei. Tādēļ iestatiet periodus atbilstoši jūsu uzņēmuma vajadzībām. Plašāku informāciju par periodiem skatiet tēmā [Vispārējās plānošanas iestatīšana](master-planning-setup.md).

### <a name="actions"></a>Darbības

Periodu vidū var arī atrast parametru **Darbības ziņojums**. Darbības ziņojumu aprēķins izraisa ilgāku izpildes laiku vispārējai plānošanai. Ja darbības ziņojumi netiek regulāri analizēti un pielietoti (katru dienu, katru nedēļu utt.), apsveriet iespēju izslēgt aprēķinu vispārējās plānošanas izpildes laikā. Lai izslēgtu aprēķinu, lapā **Vispārējie plāni** (**Vispārējie plāni \> Iestatīšana \> Plāni \> Vispārējie plāni**) iestatiet periodam **Darbības ziņojums** vērtību **0** (nulle). Arī pārliecinieties, ka iestatījums **Darbības ziņojuma** ir izslēgts visām vajadzību grupām.

### <a name="futures"></a>Aizkavēšanās

Aizkavēšanās aprēķins izraisa ilgāku izpildes laiku vispārējai plānošanai. Ja neplānojat MK vai ja aizkaves nav jāizplata no piedāvājuma uz pieprasījumu plānošanas laikā, apsveriet iespēju izslēgt aizkavēšanās aprēķinus vispārējās plānošanas laikā. Lai izslēgtu aprēķinus, iestatiet periodam **Aizkavēšanās** vienumu **0** (nulle) vispārējam plānam, kas tiek izpildīts. Arī pārliecinieties, ka iestatījums **Aizkavēšanās** ir izslēgts visām vajadzību grupām.

## <a name="one-heavy-routine-at-a-time"></a>Vienlaicīgi viena lielas noslodzes rutīna

Paredzot vispārējo plānošanu, neparedziet vienlaicīgi citus pakešuzdevumus. Esiet īpaši uzmanīgs, lai tajā pašā laikā neieplānotu citas lielas noslodzes rutīnas, piemēram, krājumu slēgšanu.

## <a name="review-the-session-log"></a>Pārskatīt sesijas žurnālu

Sistēma var apkopot papildu informāciju par uzdevumiem, kas tiek palaisti vispārējās plānošanas laikā. Lai sistēma apkopotu šo informāciju, dialoglodziņā **Vispārējās plānošanas izpilde** ieslēdziet iestatījumu **Izsekot apstrādes laiku**. Apkopotā informācija var palīdzēt atrast sastrēgumus izpildē. Piemēram, ja parametram **Uzdevumu skaits palīga uzdevumu komplektā** ir iestatīta vērtība **1**, varat identificēt krājumu, kuram ir visilgākais izpildes laiks. Varat arī salīdzināt dažādu tādu pavedienu izpildes laikus, kuriem ir statuss **Vajadzība**, un salīdzināt katra uzdevuma ilgumu.

Lai pārskatītu jūsu sistēmas vispārējās plānošanas izpildes, veiciet kādu no norādītajām darbībām.

- Darbvietā **Vispārējā plānošana** atlasiet vispārējo plānu nolaižamajā laukā un pēc tam uz elementa **Vispārējā plānošana** atlasiet **Vēsture**. Atlasiet darbu, atlasiet vienumu **Pieprasījumi** kopsavilkuma cilnē un pēc tam atlasiet **Apstrādes uzdevuma ilgums**.
- Lapā **Vispārējie plāni** atlasiet plānu kreisajā rūtī un pēc tam atlasiet vienumu **Vēsture** kopsavilkuma cilnē. Atlasiet darbu, atlasiet vienumu **Pieprasījumi** kopsavilkuma cilnē un pēc tam atlasiet **Apstrādes uzdevuma ilgums**.

Pārskatot sesijas žurnālu, ņemiet vērā šādus aspektus:

- Vienumam **Atjaunināšana** parasti nav nepieciešams ilgs laiks (parasti tas ilgst līdz 30 minūtēm), taču tas ir viena pavediena.
- Vienumam **Kopēt plānu** parasti nav nepieciešams ilgs laiks (tas ilgst līdz vienai minūtei).
- **Automātiskā apstiprināšana** parasti ilgst aptuveni 30 minūtes. Tomēr tai var būt nepieciešamas vairākas stundas atkarībā no pasūtījumu skaita un krājumu sarežģītības.
- Vienumam **Automātiska apstiprināšana** parasti ir nepieciešams mazāk laika nekā iestatījumam **Vajadzība**.
- Vienumam **Vajadzība** parasti ir nepieciešams visvairāk laika salīdzinājumā ar citiem iestatījumiem.
- Vienumiem **Darbība** un **Turpmākais ziņojums** var būt nepieciešams ilgs laiks atkarībā no datiem un MK skaita.

## <a name="filtering-of-items"></a>Krājumu filtrēšana

Filtri, kas tiek lietoti dialoglodziņā **Vispārējās plānošanas izpilde**, ietekmē vispārējās plānošanas izpildes ilgumu. Pārejiet uz **Vispārējā plānošana \> Vispārējā plānošana \> Izpildīt \> Vispārējā plānošana** vai atlasiet **Izpildīt** darbvietā **Vispārējā plānošana**. Lai izslēgtu krājumus no izpildes, ieteicams filtrēt pēc krājuma dzīves cikla stāvokļa (nevis pēc krājumu numuriem). Filtrējot pēc dzīves cikla stāvokļa, atjaunināšanas procesam būs nepieciešams mazāk laika nekā tad, ja tiek veikta filtrēšana pēc krājumu numuriem.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Automātiski filtrēt pēc krājumiem ar tiešu pieprasījumu

Lai uzlabotu vispārējās plānošanas izpildes laiku, varat izvēlēties iekļaut tikai krājumus, kuriem ir tiešais pieprasījums. Šo filtru var izmantot tikai pilnīgai vispārējās plānošanas palaišanai bez citiem filtriem, kas tiek lietoti laukā **Ieraksti, kurus iekļaut.** Vispārējā plānošana, kas tiek palaista ar filtriem, ignorē iestatījumu **Automātiski filtrēt pēc vienumiem ar tiešo pieprasījumu**.

Lauks **Automātiski filtrēt pēc vienumiem ar tiešo pieprasījumu** ir atrodams lapā **Vispārējās plānošanas parametri**, un to var izmantot gan priekšapstrādes, gan pēcapstrādes iestatījumiem.

### <a name="pre-processing"></a>Priekšapstrāde
**Iepriekšēja apstrāde: automātiski filtrēt pēc vienumiem ar tiešu pieprasījuma** parametrs nodrošina, ka vispārējās plānošanas pirmsapstrādes fāze ietver tikai tos krājumus, kas atbilst vismaz vienam no šiem nosacījumiem:
  - Krājumam ir paredzama saņemšana vai izdošana, piemēram, pirkšanas pasūtījums, pārdošanas pasūtījums, piedāvājums, pārvietošanas pasūtījums vai ražošanas pasūtījums. 
  - Krājumam ir krājuma segums ar drošības krājumu (minimālo rīcībā esošo krājumu daudzumu).
  - Krājumam pastāv prognozes pieprasījums pēc šodienas.
  - Krājumam pastāv prognozes piegāde pēc šodienas.
  - Krājums ietver visas nepārtrauktības rindas no zvanu centra moduļa, kas vēl jāizveido.

> [!NOTE]
> Krājums, kuram ir fiziski pieejami rīcībā esošie krājumi, neparāda prasības transakciju, jo krājumam nav pieprasījuma.

### <a name="post-processing"></a>Pēcapstrāde
Opcija **Pēcapstrāde: Automātiski filtrēt pēc vienumiem ar tiešu pieprasījumu** ir būtiska tikai tad, ja savās vajadzības grupās iestatāt **MK versijas prasību**. Pretējā gadījumā parametrs nav jāiespējo. 

Pirms vajadzības darbības sākšanas ir jāveic pirmsvajadzības solis, kura laikā krājumi ar iespējoto vajadzības iestatījumu **MK versijas pieprasījums** tiks pārstrādāti. Tas tiek darīts, lai nodrošinātu, ka krājumi no nepieciešamās MK versijas tiek plānoti. Krājumiem, kuriem varētu būt pieprasījums pirmsapstrādes laikā, vairs nav pieprasījuma, un tādēļ tie jāizslēdz no plānošanas palaišanas.

## <a name="performance-checklist-summary"></a>Veiktspējas kontrolsaraksta kopsavilkums

- **Pavedienu skaits** — iestatiet vērtību, kas ir lielāka par **0** (nulli).
- **Uzdevumu skaits palīga uzdevumu komplektā** — iestatiet vērtību, kas ir lielāka par **0** (nulli). (Izmantojiet formulas, kas sniegtas iepriekš šajā tēmā.)
- **Kešatmiņas izmantošana** — iestatiet vienumu **Maksimāla**, ja vien sistēmai netrūkst atmiņas.
- **Pasūtījumu skaits apstiprināšanas komplektā** — iestatiet vērtību, kas ir lielāka par **0** (nulli). (Izmantojiet formulu, kas sniegta iepriekš šajā tēmā.)
- **Periodi** — pielāgojiet sava uzņēmuma vajadzībām.
- **Darbības un aizkavēšanās** — atspējojiet darbības un aizkavēšanās, ja tās nelietojat.
- **Vienlaicīgi viena lielas noslodzes rutīna** — nepalaidiet vispārējo plānošanu kopā ar citām lielas noslodzes rutīnām.
- **Pārskatīt sesijas žurnālu.**
- **Krājumu filtrēšana** — izmantojiet dzīves cikla stāvokli, lai izslēgtu krājumus no vispārējās plānošanas izpildes. (Neizmantojiet krājuma numurus.)
