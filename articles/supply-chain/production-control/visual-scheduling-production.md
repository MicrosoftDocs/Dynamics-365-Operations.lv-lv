---
title: Ganta diagrammas izmantošana darba plānošanā
description: Ražošanas plānotāji var kontrolēt un optimizēt ražošanas plānus, izmantojot Ganta diagrammas.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage, GanttColorTable, GanttReqExplosionColor, GanttReqExplosionSetup, GanttTable, GanttTimescaleSetup, GanttWrkCtr, GanttWrkCtrColor, GanttWrkCtrJobInfo, GanttWrkCtrLoadResources, GanttWrkCtrMoveJob, GanttWrkCtrSetup, GanttWrkCtrView
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97fc3c6bd096854b5aa72980dd2bd6f3a8a1ef9e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353424"
---
# <a name="gantt-chart-for-job-scheduling"></a>Ganta diagrammas izmantošana darba plānošanā

[!include [banner](../includes/banner.md)]

Ganta diagramma ir izveidota ar mērķi ražošanas plānotājiem sniegt iespēju kontrolēt un optimizēt ražošanas plānu. Ganta diagramma padara operāciju plūsmu pārredzamu un ļauj viegli pielāgot ražošanas grafiku, vienlaikus ņemot vērā materiālu vai resursu iztrūkumu. Tas palīdz plānotājiem efektīvi izmantot pieejamos resursus, samazināt notiekošos darbus un optimizēt caurlaides laikus ražošanas pasūtījumiem.

Ganta diagramma ir vizuāls plānoto darbību attēlojums noteiktā laika intervālā. Darbības tiek plānotas resursiem, kuriem noslodzes kalendārā ir definēta noslodze. Ganta diagrammā var parādīt tālāk norādīto tipu darbības.

-   Darbi no ražošanas pasūtījumiem, kam ir ieplānoti darbi.
-   Darbi no plānotajiem ražošanas pasūtījumiem.
-   Darbam ieplānotās projekta darbības ar tipu Stundu prognozes.

Ganta diagrammu var atvērti divos dažādos skatos: **Pasūtījumu skats** un **Resursu skats**. Skatā **Pasūtījumu skats** darbības tiek grupētas atbilstoši ražošanas pasūtījumiem. Tas var noderēt, piemēram, ja vēlaties uzturēt pārskatu par visiem darbiem, kas pieder tiem pašiem pasūtījumiem. Skatā **Resursu skats** visi darbi tiek grupēti atsevišķos resursos. Šis skats var būt noderīgs, optimizējot plānu resursu līmenī, piemēram, iekārtu vai iekārtu grupas līmenī. Ganta diagrammās tālāk esošajos attēlos ir attēlots **Pasūtījumu skats** un **Resursu skats** ar tālāk uzskaitītajiem galvenajiem elementiem.

1.  Ganta diagrammas darbība
2.  Materiālu iztrūkuma ikona
3.  Materiālu pieejamības ikona
4.  Pasūtījuma piegādes datuma ikona
5.  Noslodzes josla

## <a name="order-view"></a>Pasūtījumu skats

[![Pasūtījumu skats.](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Resursu skats
[![Resursu skats.](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Aktivitātes
Darbības tiek parādītas kā joslas un ir izkārtotas laika skalas režģī ar plānotu sākuma un beigu laiku, padarot joslu garumu proporcionālu laikam, kas nepieciešams darbības izpildei. Darbības tiek rādītas atbilstoši laika skalai. Laika skalu varat pielāgot izvēlnē, kurā atlasāt sākuma un beigu datumu un laika vienību, piemēram, stundas vai dienas. Pielāgojot laika skalu, varat iestatīt laika intervālu, kurā vēlaties pārvaldīt darbības. 

Izmantojot dažādas opcijas darbību krāsu kontrolēšanai, varat iegūt labāku pārskatu. Varat konfigurēt atsevišķu krāsu darbībām, izmantot dizaina krāsu, kas ir vispārīgais programmā lietotais krāsu dizains, vai arī iestatīt krāsas kontrolēšanu ar krāsas kodu ražošanas pasūtījumiem. 

Darbību laika intervālam ir fona nokrāsa. Periodi ar baltu nokrāsu norāda laika intervālu ar definētu noslodzi darbības resursam, savukārt periodi ar pelēku nokrāsu norāda laika intervālus bez definētas noslodzes. 

Kreisajā diagrammas pusē ir pieejama papildinformācija par darbību, piemēram, resurss, kam ir ieplānota darbība, un ražošanas pasūtījuma numurs. Saistība starp darbiem, kas pieder vienam pasūtījumam, tiek parādīta ar bultiņu. 

Papildinformācija par darbību ir pieejama darbības dialoglodziņā. Lai atvērtu dialoglodziņu, veiciet dubultklikšķi uz darbības vai atlasiet izvēlni **Informācija**. Darbības dialogā var redzēt ieplānoto sākuma un beigu datumu, kā arī laika informācija par to, kurus materiālus ir plānots patērēt darbībā. 

Darbības var grupēt pa grupēšanas līmeņiem. Grupēšanas līmeņi ir hierarhiski, un tos var izmantot, lai loģiski grupētu darbības. Piemēram, ja jums ir izkārtojums, kurā ražošanas darbības ir grupētas pa parametriem Vieta, Ražošanas vienības, Resursu grupas un Resursi, grupēšanas līmeņus varat izmantot, lai darbības grupētu saskaņā ar šo izkārtojumu. Grupēšanas līmeņus var izvērst un sakļaut atsevišķā grupēšanas līmenī vai visos diagrammas līmeņos, izmantojot izvēlnes pogas **Izvērst visu** un **Sakļaut visu**. Varat arī konfigurēt grupēšanas līmeņus tā, lai tie, atverot diagrammu, tiktu izvērsti vai sakļauti.

### <a name="material-availability"></a>Materiālu pieejamība

Ganta diagrammu var iestatīt tā, lai plānotājam tiktu sniegta detalizēta informācija par atsevišķu darbību materiālu statusu. Piemēram, tas var būt noderīgi, ja materiāls ir aizkavēts un ietekmē ražošanas plānu. Šajā gadījumā problēmas saistībā ar materiāliem tiks iezīmētas Ganta diagrammā, lai palīdzētu plānotājam apzināt sekas un veikt nepieciešamās korekcijas. 

Ja plānotais darba sākuma datums ir vēlāks par darba patērēto materiālu pieejamības datumu, darbs tiek parādīts kopā ar materiālu iztrūkuma ikonu. Materiālu pieejamības datums tiek aprēķināts, balstoties uz piesaistes informāciju dinamiskajā vispārējā plānā. Materiālu iztrūkuma ikona tiek parādīta, piemēram, darbam, kurš patērē materiālu, kas ir piesaistīts pirkšanas pasūtījumam ar ieejas plūsmu, kas ir vēlāka par plānoto darba sākuma datumu.

### <a name="indicator-of-material-availability-date"></a>Materiālu pieejamības datuma indikators

Kad iestatāt darbu ar materiālu iztrūkumu rādīšanu diagrammā, var parādīt arī ikonu, kas norāda materiālu pieejamības datumu darbam. Ikona tiek rādīta tikai tad, ja materiālu pieejamības datums ir noteiktajā diagrammas laika intervālā. Ja materiālu pieejamības datums ir ārpus noteiktā laika intervālā, detalizētāku materiālu pieejamības informāciju var iegūt materiālu sarakstā, kas pieejams darba dialoglodziņā. Sarakstā ir arī ikona, kas norāda novēlotos materiālus darbam. Varat pārplānot darbu tā, lai materiālu pieejamības datums tiktu izmantots kā sākuma datums.

### <a name="indicator-of-order-delivery-date"></a>Pasūtījuma piegādes datuma indikators

Šī ikona norāda ražošanas pasūtījuma piegādes datumu. Ikona ir redzama tikai skatā Pasūtījumu skats.

### <a name="capacity-bar"></a>Noslodzes josla

Varat konfigurēt diagrammu tā, lai tajā tiktu rādīta resursa noslodzes josla. Šajā joslā sniegts pārskats par darbības resursa noslodzi noteiktajā diagrammas laika intervālā. Noslodzes josla netiek rādīta laika periodiem, kuros resurss nav rezervēts. Periodos, kuros resurss ir rezervēts noslodzei, noslodzes josla tiek rādīta kā aizpildīta josla. Periodos, kuros resursam ir pārsniegta rezervēšana, josla ir biezāka un sarkanā krāsā. Piemēram, ja divi darbi pārklājas, noslodzes joslā tiek norādīta rezervēšanas pārsniegšana laika intervālā, kurā ir pārklāšanās. Noslodzes josla tiek atjaunināta dinamiski, kad plānojat darbu. Noslodzes joslu var iespējot izvēlnē **Rādīt noslodzes joslu**. To var parādīt tikai skatā **Resursu skats**. Ja vēlaties iegūt detalizētāku skatu ar noslodzes grafiku resursā, izmantojiet diagrammu **Noslodzes grafiks**, kuru var atvērt izvēlnē vai atlasītās darbības kontekstizvēlnē.

## <a name="job-scheduling-in-the-gantt-chart"></a>Darbu plānošana Ganta diagrammā
Ganta diagrammā ir dažādas opcija korekciju veikšanai ražošanas plānā. Ganta diagrammā varat pārplānot darbības, izmantojot vilkšanas un nomešanas darbības vai grafika izvēlni. Plānošanas procesā varat ņemt vērā resursu noslodzi, resursu iespējas un materiālu ierobežojumus.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Darba plānošana ar vilkšanas un nomešanas darbībām

Varat pārplānot darbu noteiktajā laika intervālā, izmantojot vilkšanas un nomešanas darbības. Darbu var pārplānot tikai tam pašam resursam, un vienlaikus var plānot tikai vienu darbu.

### <a name="schedule-a-job-from-the-menu"></a>Darba plānošana, izmantojot izvēlni

Izvēlnē **Plānot darbus** var ieplānot vienu vai vairākus atlasītos darbus diagrammā atbilstoši plānošanas virzienam un plānošanas datumam un laikam. Ir pieejami trīs plānošanas virzieni.

-   No plānošanas datuma uz priekšu
-   No plānošanas datuma atpakaļ
-   Uz priekšu no materiālu pieejamības datuma

Nav iespējams plānot darbu ārpus noteiktā laika intervāla Ganta diagrammā. Mēģinot to darīt, darbs paliks neieplānots un jūs saņemsit kļūdas ziņojumu “Darbu nevarēja ieplānot ielādētajā laika periodā”.

### <a name="schedule-previous-jobs"></a>Plānot iepriekšējos darbus

Darbību tīklam, piemēram, darbiem, kas pieder vienam ražošanas pasūtījumam, varat izmantot funkciju **Plānot iepriekšējos darbus**, lai iepriekšējos darbus plānotu attiecībā pret atlasīto darbu tīklā. Tālāk esošajā piemērā iezīmētā darbība ir atlasītais darbs. Diagramma tiek parādīta pirms tam, kad ir ieplānots iepriekšējais darbs, un pēc tam, kad ir ieplānots iepriekšējais darbs. 

[![Plānot iepriekšējo darbu.](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Plānot nākamos darbus

Funkciju **Plānot nākamos darbus** varat izmantot, lai nākamos darbus plānotu attiecībā pret atlasīto darbu darbību tīklā. Tālāk esošajā piemērā iezīmētā darbība ir atlasītais darbs. Diagramma tiek parādīta pirms tam, kad ir ieplānots nākamais darbs, un pēc tam, kad ir ieplānots nākamais darbs. 

[![Plānot nākamo darbu.](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Plānot ap darbu

Funkciju **Plānot ap darbu** varat izmantot, lai nākamo darbu un iepriekšējo darbu plānotu attiecībā pret atlasīto darbu darbību tīklā. Tālāk esošajā piemērā iezīmētā darbība ir atlasītais darbs. Diagramma tiek parādīta pirms tam, kad ir ieplānots darbs, un pēc tam, kad ir ieplānots darbs. 

[![Plānot ap darbu.](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Sakārtot darbus

Funkciju **Sakārtot** varat izmantot, lai sakārtotu atlasītās darbības vienam resursam. Šīs darbības var būt gan vienā darbības tīklā, gan piederēt dažādiem tīkliem. Izmantojot sakārtošanas funkciju, tiks likvidēti laika pārtraukumi starp atlasītajām darbībām. Šo funkciju varat izmantot, lai optimizētu resursu noslodzes lietojumu. Diagramma tiek parādīta pirms tam, kad ir ieplānots darbs, un pēc tam, kad ir ieplānots darbs. 

[![Sakārtot darbu.](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Darbību atkārtota piešķiršana no viena resursa citam

Varat atkārtoti piešķirt darbu no viena resursa citam. Tas var būt noderīgi gadījumos, kad iekārta nedarbojas vai tai ir pārsniegta rezervēšana un jums ir jāatrod cits pieejams resurss, kas var veikt darbu.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Darbības atkārtota piešķiršana, izmantojot vilkšanas un nomešanas darbības

Skatā **Resurss** varat darbību atkārtoti piešķirt citam resursam Ganta diagrammā, veicot vilkšanas un nomešanas darbības. To var izdarīt, atlasot rindu, kurā ir ieplānota attiecīgā darbība. Kad rinda ir atlasīta, velciet rindu uz resursu diagrammā, kas ir grupēta citā resursu grupēšanas līmenī.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Darbības atkārtota piešķiršana, izmantojot izvēlni Plānot darbus

Darbu var atkārtoti piešķirt, izmantojot dialoglodziņu **Plānot darbu**, kuru var atvērt izvēlnē **Plānot darbu**. Šajā izvēlnē varat atkārtoti piešķirt darbu tikai resursam, kas jau ir ielādēts Ganta diagrammā. Atlasot tikai vienu darbu, resursa nolaižamā izvēlne tiks kārtota pa lietojamajiem resursiem. Atlasot vairāk darbu, resursu sarakstā nebūs nekādas informācijas par lietojamajiem resursiem.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Papildu resursu ielāde Ganta diagrammā
Skatā **Resursu skats** ir iespēja ielādēt papildu resursus Ganta diagrammā. Tas var būt noderīgi, ja vēlaties atrast alternatīvu resursu darbam, kas ir ieplānots iekārtai, kurai ir pārsniegta rezervēšana vai kas nedarbojas. Lapā **Ielādēt papildu resursus** ir pieejams saraksts ar resursiem, kas darbojas no saraksta atvēršanas datuma. Kā pirmie sarakstā būs norādīti lietojamie resursi attiecībā pret atlasīto darbu Ganta diagrammā. Ja pirms saraksta atvēršanas ir atlasīti vairāki darbi, netiks parādītas nekādas norādes par lietojamajiem resursiem. Lapā **Ielādēt papildu resursus** varat atlasīt vienu vai vairākus resursus, kas tiks ielādēti Ganta diagrammā pēc atlases apstiprināšanas. Ja Ganta diagrammas laika intervālā esošajam atlasītajam resursam nav ieplānots neviens darbs, resurss tiks novietots resursu grupēšanas līmenī Ganta diagrammas darbību saraksta apakšdaļā.

### <a name="access-the-gantt-chart"></a>Piekļuve Ganta diagrammai

Ganta diagrammu var atvērt no tālāk norādītajām lapām.


|                                                 <strong>Lapa</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Apraksts</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Ražošanas pasūtījumu saraksts un papildinformācija</strong>                                    | Lapā <strong>Ražošanas pasūtījumu saraksts un papildinformācija</strong> Ganta diagrammu var atvērt no viena vai vairākiem atlasītajiem pasūtījumiem. Atverot diagrammu no izvēlnes vienuma <strong>Ganta diagramma</strong>, tiks ielādēti visi ar atlasītajiem ražošanas pasūtījumiem saistītie darbi, kā arī darbi no cietiem ražošanas pasūtījumiem, kas ir ieplānoti tiem pašiem resursiem. Atverot diagrammu no izvēlnes vienuma <strong>Ganta diagramma — ātrais skats</strong>, tiks ielādēti tikai ar atlasītajiem ražošanas pasūtījumiem saistītie darbi. Šajā skatā nav iespējams plānot darbus. |
|                                               <strong>Resurss</strong>                                                |                                                                                                                                                        Lapā <strong>Resurss</strong> Ganta diagrammu varat atvērt no izvēlnes vienuma <strong>Ganta diagramma</strong>. Pēc atlasīšanas diagrammā tiks ielādēti visi atlasītajā laika intervālā resursam ieplānotie darbi.                                                                                                                                                         |
|                                            <strong>Resursu grupa</strong>                                             |                                                                                                                                                 Lapā <strong>Resursu grupa</strong> Ganta diagrammu varat atvērt no izvēlnes vienuma <strong>Ganta diagramma</strong>. Pēc atlasīšanas tiks parādīti visi resursu grupas resursiem ieplānotie darbi atlasītajā laika intervālā.                                                                                                                                                 |
|                                             <strong>Ganta diagrammas</strong>                                              |                                                                                 Lapā <strong>Ganta diagrammas</strong> varat konfigurēt Ganta diagrammas pa resursiem un resursu grupām. Piemēram, ja vēlaties kontrolēt ražošanas darbības noteiktām resursu vai resursu grupu kopām, lapā <strong>Ganta diagrammas</strong> varat izveidot atsevišķas to konfigurācijas. Pēc tam Ganta diagrammu var atvērt no katras konfigurācijas.                                                                                 |
|                                       <strong>Stundu prognozes</strong> (projekts)                                        |                                                                                                                              Resursiem var ieplānot tipa <strong>Stundu prognozes</strong> projekta darbības. Lapā <strong>Stundu prognoze</strong> esošajā izvēlnē <strong>Plānošana</strong> varat atvērt Gantt diagrammu par kādu pasūtījumu, lai skatītu darbam ieplānotās stundu prognozes tipa projekta darbības.                                                                                                                               |
|           <strong>Veicamais darbs</strong> (saraksts darbvietā <strong>Ražošanas pārvaldība</strong> )            |                                                                                               Darbvietā <strong>Veicamo darbu saraksts ražošanas vadībā</strong> tiek rādīti darbi no ražošanas un partijas pasūtījumiem, kas notiek atlasītajos darbvietas resursos. Izvēlnes vienumā <strong>Ganta diagramma</strong> varat atvērt Ganta diagrammu, un visi sarakstā atlasītie darbi tiks ielādēti diagrammā.                                                                                               |
| <strong>Izlaišanai paredzētie ražošanas pasūtījumi</strong> (pieejama darbvietā <strong>Ražošanas pārvaldība</strong> ) |                                                                                                                                         Lapa Izlaišanai paredzētie ražošanas pasūtījumi tiek atvērta no darbvietas <strong>Ražošanas pārvaldība</strong>. Šajā lapā tiek rādīti plānotie ražošanas un partijas pasūtījumi, kas gaida izlaišanu. Šajā lapā Ganta diagrammu varat atvērt atlasītajiem ražošanas pasūtījumiem.                                                                                                                                          |

## <a name="additional-resources"></a>Papildu resursi  
[Vizuāla plānošana ar Ganta diagrammu ražošanas un partijas pasūtījumiem (video)](https://youtu.be/BtbuShkGj4I)

[Ražošanas vizuālā plānošana (demonstrācijas skripts)](/dynamics/s-e/)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]