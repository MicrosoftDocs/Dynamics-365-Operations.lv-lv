---
title: Kā darbinieki izmanto ražotnes izpildes interfeisu
description: Šajā tēmā aprakstīts, kā izmantot ražotnes izpildes interfeisu no darbinieka skata punkta.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e84df8aa4f3e4079cf97d35b0d67a75d68dbb4b2
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860537"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Kā darbinieki izmanto ražotnes izpildes interfeisu

[!include [banner](../includes/banner.md)]

Ražotnes izpildes interfeiss ir optimizēts skārienvadībai. Tā dizains nodrošina vizuālo kontrastu, kas atbilst pieejamības prasībām ražotnes vidēm. Tas piedāvā visas tās pašas funkcionālās iespējas kā darba kartes ierīce. Tomēr tas arī rada iespēju daudzus darbus sākt paralēli no darbu saraksta. (Šī iespēja ir pazīstama arī kā *darbu apvienošana*.) Turklāt no darbu saraksta darbinieki var atvērt ceļvedi, kas izveidots Microsoft Dynamics 365 rokasgrāmatā. Tādējādi tie var iegūt vizuālus norādījumus HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Pierakstīšanās ražošanas izpildes interfeisā kā darbiniekam

Pirms darbinieki var sākt izmantot ierīci, uzraudzītājam vai tehniskajam personālam ir jāsagatavo un jāatver pareizā lapa programmā Dynamics 365 Supply Chain Management. Papildinformāciju par to, kā iestatīt ierīci, skatiet tēmā [Ierīces iestatīšana darbināšanai ražotnes izpildes interfeisā](production-floor-execution-setup.md).

Kad ierīce ir sagatavota, tajā tiek parādīta pierakstīšanās lapa. Šī lapa tiek rādīta informāciju par vietējās darba šūnas darbu statusu. Šī informācija tiek periodiski atjaunināta. Lapā darbinieki izmanto savu žetonu ID, lai pierakstītos. Lai gan darbiniekiem nav jābūt lietotāja kontam programmā Supply Chain Management, viņiem ir jābūt *laikā reģistrēta darbinieka* kontam, ko viņi var izmantot pierakstoties.

![Ražotnes izpildes interfeisa pierakstīšanās lapa.](media/pfei-sign-in-page.png "Ražotnes izpildes interfeisa pierakstīšanās lapa")

Šīs tēmas pārējās sadaļās ir aprakstīts, kā darbinieki mijiedarbojas ar interfeisu.

## <a name="all-jobs-tab"></a>Cilne Visi darbi

Cilnē **Visi darbi** ir pieejams darbu saraksts, kurā redzami visi ražošanas darbi, kuru statuss ir *Nesākts*, *Apturēts* vai *Sākts*. (Šis cilnes nosaukums ir pielāgojams un var atšķirties jūsu sistēmai.)

![Cilne Visi darbi.](media/pfei-all-jobs-tab.png "Cilne Visi darbi")

Darbu sarakstā ir tālāk minētās kolonnas. Numuri atbilst iepriekšējā attēlā redzamajiem numuriem.

1. **Atlases kolonna** — kolonna, kas atrodas vistālāk pa kreisi, izmanto atzīmes, lai norādītu darbinieka atlasītos darbus. Darbinieki sarakstā var vienlaicīgi atlasīt vairākus darbus. Lai sarakstā atlasītu visus darbus, atzīmējiet izvēles rūtiņu kolonnas galvenē. Kad ir atlasīts viens darbs, detalizēta informācija par šo darbu tiek rādīta lapas apakšējā daļā.
1. **Darba statusa kolonna** — šajā kolonnā tiek izmantoti simboli, lai norādītu katra darba statusu. Darbu, kuriem nav simbola šajā kolonnā, statuss ir *Nav sākts*. Zaļš trijstūris norāda darbus, kuru statuss ir *Sākts*. Divas dzeltenas vertikālas līnijas norāda darbus, kuru statuss ir *Apturēts*.
1. **Augstas prioritātes kolonna** – šajā kolonnā ir izmantotas izsaukuma atzīmes, lai norādītu darbus, kuriem ir augsta prioritāte.
1. **Pasūtījums** – šajā kolonnā tiek rādīts darba ražošanas pasūtījuma numurs.
1. **Apraksts** — šajā kolonnā ir parādīts tās operācijas apraksts, kurā darbs ietilpst.
1. **Pieprasīts** — šajā kolonnā tiek rādīts daudzums, ko darbā paredzēts saražot.
1. **Sākts** — šajā kolonnā tiek rādīts daudzums, kas darbam jau ir sākts.
1. **Pabeigts** — šajā kolonnā tiek rādīts daudzums, kas darbam jau ir pabeigts.
1. **Brāķēts** — šajā kolonnā tiek rādīts daudzums, kas darbam ir brāķēts.
1. **Atlikušais** — šajā kolonnā tiek rādīts daudzums, kas darbam vēl jāpabeidz.

## <a name="active-jobs-tab"></a>Cilne Aktīvie darbi

Cilnēs **Aktīvie darbi** ir parādīts visu to darbu saraksts, ko jau pierakstījies darbinieks ir sācis. (Šis cilnes nosaukums ir pielāgojams un var atšķirties jūsu sistēmai.)

![Cilne Aktīvie darbi.](media/pfei-active-jobs-tab.png "Cilne Aktīvie darbi")

Darbu sarakstā ir tālāk minētās kolonnas:

- **Atlases kolonna** — kolonna, kas atrodas vistālāk pa kreisi, izmanto atzīmes, lai norādītu darbinieka atlasītos darbus. Darbinieki sarakstā var vienlaicīgi atlasīt vairākus darbus. Lai sarakstā atlasītu visus darbus, atzīmējiet izvēles rūtiņu kolonnas galvenē. Kad ir atlasīts viens darbs, detalizēta informācija par šo darbu tiek rādīta lapas apakšējā daļā.
- **Pasūtījums** – šajā kolonnā tiek rādīts darba ražošanas pasūtījuma numurs.
- **Apraksts** — šajā kolonnā ir parādīts tās operācijas apraksts, kurā darbs ietilpst.
- **Pieprasīts** — šajā kolonnā tiek rādīts daudzums, ko darbā paredzēts saražot.
- **Sākts** — šajā kolonnā tiek rādīts daudzums, kas darbam jau ir sākts.
- **Pabeigts** — šajā kolonnā tiek rādīts daudzums, kas darbam jau ir pabeigts.
- **Brāķēts** — šajā kolonnā tiek rādīts daudzums, kas darbam ir brāķēts.
- **Atlikušais** — šajā kolonnā tiek rādīts daudzums, kas darbam vēl jāpabeidz.

## <a name="my-machine-tab"></a>Cilne Mana iekārta

Cilne **Mana iekārta** ļauj darbiniekiem atlasīt līdzekli, kas ir saistīts ar iekārtas resursu filtra iestatījuma cilnē **Visi darbi**. Darbinieks pēc tam var skatīt atlasītā pamatlīdzekļa stāvokli un veselības stāvokli, nolasot vērtības līdz četriem atlasītajiem skaitītājiem un neseno uzturēšanas pieprasījumu un reģistrēto dīkstāves pieprasījumu sarakstu. Darbinieks var arī pieprasīt atlasītā pamatlīdzekļa uzturēšanu un reģistrēt un rediģēt iekārtas dīkstāves laiku. (Šis cilnes nosaukums ir pielāgojams un var atšķirties jūsu sistēmai.)
 
![Cilne Mana iekārta.](media/pfei-my-machine-tab.png "Cilne Mana iekārta")

Cilnei **Mana iekārta** ir šādas kolonnas. Numuri atbilst iepriekšējā attēlā redzamajiem numuriem.

1. **Iekārtas līdzeklis** - izvēlieties iekārtas līdzekli, ko vēlaties izsekot. Sāciet ierakstīt nosaukumu, lai to atlasītu no atbilstošu pamatlīdzekļu saraksta, vai atlasiet palielināmo-saskaņošanas ikonu, lai atlasītu no visu līdzekļu saraksta, kas saistīts ar resursiem, kas atrodas darbu saraksta filtrā.

    > [!NOTE]
    > Supply Chain Management lietotāji var piešķirt resursu katram pamatlīdzeklim pēc nepieciešamības, izmantojot lapu **Visi līdzekļi** (cilnē **Fiksētie pamatlīdzekļi**, izmantojot nolaižamo sarakstu **Resursi** ). Papildinformāciju skatiet nodaļā [Līdzekļa izveide](../asset-management/objects/create-an-object.md).

1. **Iestatījumi** – izvēlieties ātrumkārbas ikonu, lai atvērtu dialoglodziņu, kur var izvēlēties, kuru skaitītāju skatīt atlasītajam iekārtas pamatlīdzeklim. Šo skaitītāju vērtības ir parādītas **Pamatlīdzekļu pārvaldības** cilnes augšpusē. **Iestatījumu** izvēlne (parādīta ekrānuzņēmumā) ļauj aktivizēt līdz pat četriem skaitītājiem. Katram skaitītājam, kuru vēlaties iespējot, izmantojiet uzmeklēšanas lauku elementa augšā, lai atlasītu skaitītāju. Uzmeklēšanas laukā ir uzskaitīti visi skaitītāji, kas saistīti ar līdzekli, kas atlasīts **Pamatlīdzekļu pārvaldības lapas** augšpusē. Iestatiet katru skaitītāju, lai pārraudzītu skaitītāja **Apkopoto** vērtību vai pēdējo **Faktisko** vērtību. Piemēram, ja iestatāt skaitītāju, kas izseko, cik stundu dators darbojas, tad to vajadzētu iestatīt uz **Uzkrāts**. Ja iestatāt skaitītāju, lai izmērītu jaunāko atjaunināto temperatūras vai spiediens, jums tas jāiestata uz **Faktiskais**. Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.

    ![Cilne Manas iekārtas iestatījumi.](media/pfei-my-machine-tab-settings.png "Cilne Manas iekārtas iestatījumi")

1. **Pieprasījuma uzturēšana** – atlasiet šo pogu, lai atvērtu dialoglodziņu, kur varat izveidot uzturēšanas pieprasījumu. Varat sniegt aprakstu un piezīmi. Pieprasījums tiks nosūtīts Supply Chain Management lietotājam, kurš tad varēs pārveidot uzturēšanas pieprasījumu uz uzturēšanas darba pasūtījumu.
1. **Reģistrēt dīkstāves laiku** – atlasiet šo pogu, lai atvērtu dialoglodziņu, kur reģistrēt iekārtas dīkstāves laiku. Varat atlasīt pamatojuma kodu un ievadīt dīkstāves laika posmu. Iekārtas dīkstāves reģistrācija tiek izmantota iekārtas līdzekļa efektivitātes aprēķināšanai.
1. **Apskatīt vai rediģēt** – atlasiet šo pogu, lai atvērtu dialoglodziņu, kur var labot vai apskatīt esošos dīkstāves ierakstus.

## <a name="starting-and-completing-production-jobs"></a>Ražošanas darbu sākšana un pabeigšana

Darbinieki sāk ražošanas darbu, atlasot darbu cilnē **Visi darbi** un pēc tam atlasot **Sākt darbu**, lai atvērtu dialoglodziņu **Sākt darbu**.

![Dialoglodziņš Sākt darbu.](media/pfei-start-job-dialog.png "Dialoglodziņš Sākt darbu")

Darbinieki izmanto dialoglodziņu **Sākt darbu**, lai apstiprinātu ražošanas daudzumu un pēc tam sāktu darbu. Darbinieki var pielāgot daudzumu, atlasot lauku **Daudzums** un pēc tam izmantojot parādīto ciparu tastatūru. Darbinieki pēc tam atlasa **Sākt**, lai sāktu darbu. Dialoglodziņš **Sākt darbu** tiek aizvērts un darbs tiek pievienots cilnē **Aktīvie darbi**.

Darbinieki var sākt darbu, kam ir jebkurš statuss. Kad darbinieks sāk darbu, kura statuss ir *Nav sākts*, lauks **Daudzums** dialoglodziņā **Sākt darbu** sākotnēji rāda pilnu daudzumu. Kad darbinieks sāk darbu, kura statuss ir *Sākts* vai *Apturēts*, lauks **Daudzums** sākotnēji rāda atlikušo daudzumu.

## <a name="reporting-good-quantities"></a>Ziņošana par preču daudzumiem

Kad darbinieks pabeidz vai daļēji pabeidz darbu, viņš var ziņot par preču daudzumiem, kas tika saražoti, atlasot darbu cilnē **Aktīvie darbi** un pēc tam atlasot **Pārskata norise**. Pēc tam dialoglodziņā **Pārskata norise** darbinieks ievada preču daudzumu, izmantojot ciparu tastatūru. Pēc noklusējuma daudzums ir tukšs. Kad daudzums ir ievadīts, darbinieks var atjaunināt darba statusu uz *Norit*, *Apturēts* vai *Pabeigts*.

![Dialoglodziņš Ziņot par norisi.](media/pfei-report-progress-dialog.png "Dialoglodziņš Ziņot par norisi")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Pārskats par preču daudzumiem partijas pasūtījumos, kuros ir līdzprodukti un blakusprodukti

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)] 
<!--KFM: Preview until GA with 10.0.23 -->

Darbinieki var izmantot ražošanas izpildes interfeisu, lai ziņotu par partijas pasūtījumu progresu. Šis pārskats iekļauj pārskatus par līdzproduktiem un blakusproduktiem.

Daži ražotāji, īpaši procesa nozarēs, izmanto pakešveida pasūtījumus, lai pārvaldītu savus ražošanas procesus. Partijas pasūtījumi tiek izveidoti no formulām, un šīs formulas var definēt tā, lai tām līdzprodukti un blakusprodukti būtu izvade. Ziņojot par šo partijas pasūtījumu datiem, formulas krājumam, kā arī līdzproduktiem un blakusproduktiem ir jāreģistrē ražošanas apjoms.

Kad darbinieks pabeidz vai daļēji pabeidz darbu partijas pasūtījumā, viņš var ziņot par preču vai brāķa daudzumu katrai precei, kas ir definēta kā pasūtījuma izvade. Preces, kas definētas kā partijas pasūtījuma izvade, var būt *Formulas*, *Līdzprodukta*, vai *Blakusprodukta* tipa preces.

Lai ziņotu par preču labajiem daudzumiem, darbinieks atlasa darbu cilnē **Aktīvie darbi** un pēc tam atlasa **Pārskata progress**.

Pēc tam dialoglodziņā **Pārskata progress** darbinieks var atlasīt starp precēm, kas definētas kā izvade pakešveida pasūtījumam, par kuru ir pārskats. Darbinieks sarakstā var atlasīt vienu vai vairākas preces un pēc tam atlasīt **Pārskata progress**. Katra produkta daudzums pēc noklusējuma ir tukšs, un darbinieks var izmantot skaitlisko tastatūru, lai ievadītu daudzumu. Lai pārvietotos starp atlasītajām precēm, darbinieks var izmantot pogas **Iepriekšējais** un **Nākamais**. Kad daudzums ir ievadīts katrai precei, darbinieks var atjaunināt darba statusu uz *Norit*, *Apturēts* vai *Pabeigts*.

![Ziņot par līdzproduktiem un blakusproduktiem.](media/report-co-by-products.png "Ziņot par līdzproduktiem un blakusproduktiem")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Pārskats par partijas pasūtījumiem plānošanas krājumiem

Kad darbinieks pabeidz darbu ar pakešuzdevumu plānotai precei, viņi ziņos daudzumu tikai par līdzproduktiem un blakusproduktiem, jo plānošanas krājumiem nav *Formulas* tipa krājuma.

### <a name="reporting-co-product-variation"></a>Ziņot par līdzprodukta variāciju

Ja partijas pasūtījums ir izveidots no formulas versijas, kur **Līdzproduktu variāciju** opcija ir iestatīta uz *Jā*, darbinieks var ziņot par līdzproduktiem, kas nav daļa no partijas pasūtījumu definīcijas. Šī funkcionalitāte tiek izmantota scenārijos, kuros ražošanas procesā var rasties neparedzēta produkta izvade.

Šajā gadījumā darbinieks var norādīt līdzproduktu un daudzumu pārskatam, pārskata norises dialoglodziņā atlasot **Līdzproduktu variācijas**. Pēc tam darbinieks var atlasīt no visām izlaistajām precēm, kas definētas kā līdzprodukti.

## <a name="reporting-scrap"></a>Ziņošana par brāķi

Kad darbinieks pabeidz vai daļēji pabeidz darbu, viņš var ziņot par preču brāķi, kas tika saražots, atlasot darbu cilnē **Aktīvie darbi** un pēc tam atlasot **Ziņot par brāķi**. Pēc tam dialoglodziņā **Ziņot par brāķi** darbinieks ievada brāķa daudzumu, izmantojot ciparu tastatūru. Darbinieks atlasa arī pamatojumu (*Neviens*, *Mašīna*, *Operators* vai *Materiāls*).

![Dialoglodziņš Ziņot par brāķi.](media/pfei-report-scrap-dialog.png "Dialoglodziņš Ziņot par brāķi")

## <a name="completing-a-job-and-starting-a-new-job"></a>Darba pabeigšana un jauna darba sākšana

Parasti darbinieki pabeidz darbu, atlasot vienu vai vairākus pašreizējos darbus cilnē **Aktīvie darbi** un pēc tam atlasot **Ziņot par norisi**. Pēc tam tie ievada saražoto daudzumu (derīgo daudzumu) un iestata statusu uz *Pabeigts*. Ja atlasīts vairāk par vienu darbu, darbinieks pēc tam izmanto pogas **Iepriekšējais** un **Nākamais**, lai pārvietotos starp tām. Lai sāktu jaunu darbu, darbinieks to atlasa cilnē **Visi darbi** un pēc tam atlasa **Sākt darbu**.

Darbinieks var arī sākt jaunu darbu, kamēr iepriekšējais darbs joprojām ir atvērts. No jauna, darbinieks atlasa jaunu darbu cilnē **Visi darbi** un pēc tam atlasa **Sākt darbu**. Tomēr šajā gadījumā dialoglodziņš **Sākt darbu** informē darbinieku, ka tas pašlaik strādā pie darba, un ka viņam ir jāpārtrauc vai jāpabeidz šis darbs, pirms sākt jaunu darbu.

## <a name="working-on-multiple-jobs-in-parallel"></a>Darbs ar vairākiem darbiem paralēli

Viens darbinieks vienlaicīgi var strādāt ar vairākiem darbiem (tas ir, paralēli). Šajā gadījumā darbu apkopojums, ar kuriem darbinieks strādā, tiek saukts par *darbu komplektu*. Darbinieks var pievienot jaunus darbus komplektam vai pabeigt vienu vai vairākus darbus komplektā. Sekojošajos divos scenārijos ir parādīts, kā darbinieks var strādāt ar darbiem paralēli.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>1. scenārijs: darbinieks, kuram nav aktīvu darbu, vēlas sākt divus darbus un strādāt ar tiem paralēli

Darbinieks atlasa divus darbus cilnē **Visi darbi** un pēc tam atlasa **Sākt darbu**. Dialoglodziņā **Sākt darbu** ir redzami abi atlasītie darbi, un darbinieks var pielāgot daudzumu, lai sāktu katru darbu. Darbinieks pēc tam apstiprina dialoglodziņu un var sākt abus darbus.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>2. scenārijs: darbinieks, kuram ir divi aktīvie darbi, kas ir procesā, vēlas sākt trešo darbu un strādāt ar to paralēli diviem pārējiem

Darbinieks atlasa trešo darbu cilnē **Visi darbi** un pēc tam atlasa **Komplekts**. Dialoglodziņā **Komplekts** darbinieks var pielāgot daudzumu sākšanai. Darbinieks pēc tam apstiprina dialoglodziņu, atlasot **Komplekts**.

## <a name="working-on-indirect-activities"></a>Darbs netiešajās aktivitātēs

Netiešās aktivitātes ir aktivitātes, kas nav tieši saistītas ar ražošanas pasūtījumu. Netiešās aktivitātes var definēt elastīgi, kā aprakstīts sadaļā [Netiešo aktivitāšu iestatīšana laikam un apmeklējumam](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Piemēram, Šenona, ražotnes darbiniece Contoso, vēlas apmeklēt uzņēmuma sanāksmi, un sapulces tiek uzskatītas par netiešo aktivitāti. Ir spēkā viens no tālāk minētajiem diviem scenārijiem.

- **Šenona strādā pie viena vai vairākiem aktīviem darbiem.** Šenona atlasa **Aktivitāte**, identificē darbību (sapulce) un apstiprina savu izvēli. Tiek parādīts ziņojums, ka viņai ir pašlaik notiekošie darbi. No ziņojuma Šenona var izvēlēties pabeigt vai pārtraukt darbus, ar kuriem viņa strādā, pirms dodas uz sapulci.
- **Šenonai nav aktīvu darbu.** Šenona atlasa **Aktivitāte**, identificē darbību (sapulce) un apstiprina savu izvēli. Tagad viņa ir reģistrēta kā sapulcē klātesoša.

Abos scenārijos pēc tam, kad Šenona apstiprina savu izvēli, viņa dodas vai nu uz pierakstīšanās lapu, vai uz lapu, kas gaidīs, lai viņa apstiprinātu, ka viņa ir atgriezusies no netiešās aktivitātes. Lapa, kas tiek parādīta, ir atkarīga no ražotnes izpildes interfeisa konfigurācijas. (Papildinformāciju skatiet sadaļā [Ražotnes izpildes interfeisa konfigurēšana](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Pārtraukumu reģistrēšana

Darbinieki var reģistrēt pārtraukumus. Pārtraukumus var elastīgi definēt, kā aprakstīts sadaļā [Apmaksa, pamatojoties uz reģistrācijām](pay-based-on-registrations.md).

Darbinieks reģistrē pārtraukumu, atlasot **Pārtraukums** un pēc tam atlasot karti, kas apzīmē pārtraukuma veidu (piemēram, pusdienas). Kad darbinieks ir apstiprinājis atlasi, ierīce rāda vai nu pierakstīšanās lapu, vai arī lapu, kas gaidīs, lai darbinieks apstiprinātu, ka ir atgriezies no pārtraukuma. Lapa, kas tiek parādīta, ir atkarīga no ražotnes izpildes interfeisa konfigurācijas. (Papildinformāciju skatiet sadaļā [Ražotnes izpildes interfeisa konfigurēšana](production-floor-execution-configure.md).)

## <a name="opening-instructions"></a>Atvēršanas instrukcijas

Darbinieki var atvērt dokumentu, kas ir piesaistīts darbam, atlasot **Instrukcijas**. Poga **Instrukcijas** ir pieejama tikai tad, ja dokuments ir saistīts ar darbu pamatdatos. Piemēram, dokuments, kas ir piesaistīts precei, kura atrodas lapā **Izlaistie produkti** programmā Supply Chain Management, būs pieejams darbiniekiem, lai to atvērtu ražotnes izpildes interfeisā.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Jauktās realitātes ceļvežu atvēršana HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) var palīdzēt darbiniekiem, sniedzot iespēju iegūt praktisku apmācību, kā izmantot jaukto realitāti. Jūs varat definēt standartizētus procesus, izmantojot detalizētus norādījumus, kas iepazīstinās darbiniekus ar nepieciešamajiem rīkiem un daļām un parādīs tiem, kā izmantot šos rīkus reālās darba situācijās. Tālāk ir sniegts šā procesa apskats.

1. Katru reizi, kad nodarbinātais atver darbu sarakstu ražotnes izpildes interfeisā, interfeiss atrod atbilstošos ceļvežus parādītajiem darbiem.
1. Darbinieks atlasa **Ceļveži**, lai skatītu ceļvežu sarakstu.
1. Darbinieks sarakstā atlasa atbilstošo ceļvedi.
1. Ražotnes izpildes interfeiss atlasītajam ceļvedim parāda QR kodu.
1. Darbinieks uzliek HoloLens un paskatās uz QR kodu, lai startētu ceļvedi.
1. Darbinieks strādā ar ceļvedi, lai apgūtu uzdevumu.

Papildinformācijas par to, kā izveidot, piešķirt un lietot ceļvežus HoloLens, skatiet sadaļā [Jauktās realitātes ceļvežu nodrošināšana darbiniekiem ražošanā](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
