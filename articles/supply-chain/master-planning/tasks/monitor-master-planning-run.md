---
title: Vispārējās plānošanas izpildes pārraudzība
description: Šajā tēmā izskaidrots, kā ražošanas plānotājs var redzēt, vai notiek vispārējās plānošanas izpilde.
author: ChristianRytt
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfd1906200038c27e63f9434bba27e7146f4c80c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575612"
---
# <a name="monitor-a-master-planning-run"></a>Vispārējās plānošanas izpildes pārraudzība

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Ganta diagrammas izmantošana, lai vizualizētu vispārējās plānošanas norisi

Lapā **Skatīt vispārējās plānošanas norisi** varat skatīt detalizētu informāciju par vēsturisko vispārējo plānošanu, kas tiek veikta kā Ganta diagramma. Šī funkcionalitāte var palīdzēt jums aprēķināt laiku, kas tiek pavadīts dažādos vispārējās plānošanas posmos. Pašreizējam aktīvajam plānošanas darbam lapu **Skatīt vispārējās plānošanas norisi** var izmantot, lai izsekotu norisei un skatītu prognozēto atlikušo laiku.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>Vispārējā plāna progresa vizualizācijas līdzekļa ieslēgšana un izmantošana

Lai izmantotu šo funkcionalitāti, izpildiet tālāk aprakstītās darbības.

1. Darbvietā **Līdzekļu pārvaldība** cilnē **Jauns** atlasiet sarakstā **Vispārējās plānošanas norises vizualizācija**. Ja šī funkcija netiek parādīta cilnē **Jauns**, skatiet cilnēs **Neiespējotās** un **Visas**.
1. Atlasiet **Iespējot tagad**. Pēc izvēles atlasiet **Grafiks** un pēc tam atlasiet laiku, kad vēlaties ieslēgt līdzekli.

Lapā **Skatīt vispārējās plānošanas norisi** var apskatīt gan vēsturiskos, gan aktīvos plānošanas darbus. 

Lai skatītu vēsturiskos plānošanas darbus, ir divas opcijas. 

1. Dodieties uz **Vispārējā plānošana \>Iestatīšana \>Plāni \>Vispārējie plāni** un pēc tam darbību rūtī atlasiet **Vēsture**. Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.
1. Dodieties uz **Vispārējā plānošana \>Darbvietas \>Vispārējā plānošana**, vispārējā plānošanā noklikšķiniet uz **Vēsture**. Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.

Lai skatītu aktīvos plānošanas darbus, ir divas opcijas. 
1. Dodieties uz **Vispārējā plānošana \>Darbvietas \>Vispārējā plānošana**, darbību rūtī atlasiet **Nepabeigtais plānošanas process**. Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.
1. Dodieties uz **Vispārējā plānošana \>Darbvietas \>Vispārējā plānošana**, vispārējā plānošanā noklikšķiniet uz **Skatīt norisi**. Kad vēlamais darbs ir izvēlēts, atlasiet **Pieprasījumi** un pēc tam atlasiet **Skatīt norisi**.

Piezīme: aktīvos darbus var skatīt tikai tad, kad plānošanas darbs tiek apstrādāts.

### <a name="analyze-a-master-planning-job"></a>Vispārējās plānošanas darbu analizēšana

Ganta diagrammā varat izvērst katru no sekojošajiem plānošanas procesiem, lai apskatītu papildu detaļas par patērēto laiku:

- Notiek inicializēšana
- Datu dzēšana un ievietošana
- Vajadzību plānošana
- Aizkaves
- Optimizācijas priekšlikumi
- Pabeigšana
- Automātiskā apstiprināšana

Ganta diagramma ir noderīgs rīks, ja vēlaties skatīt darbības ziņojumu izmantošanas ietekmi.

#### <a name="navigation-in-the-gantt-chart"></a>Navigācija Ganta diagrammā

- Lai izvērstu atlasīto grupu un parādītu detaļas, koka skatā atlasiet pluszīmi (**+**).
- Lai sakļautu atlasīto grupu, koka skatā atlasiet mīnusa zīmi (**–**).
- Navigācijai varat izmantot tastatūru. Izmantojiet **Augšupvērsto bultiņu** un **Lejupvērsto bultiņu**, lai pārvietotos starp rindām. Izmantojiet **Labo bultiņu** un **Kreiso bultiņu**, lai izvērstu un sakļautu grupas.
- Lai atvērtu vai aizvērtu visus Ganta diagrammas līmeņus, atlasiet **Izvērst visu** vai **Sakļaut visu**.
- Lai skatītu saistīto apstrādes laiku, novietojiet kursoru virs uzdevuma. (Uzdevumi ir viszemākais līmenis Ganta diagrammā.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Skatīt papildu vispārējās plānošanas izpildi, lai salīdzinātu darbus

Atlasot vispārējās plānošanas darbu laukā **Rādīt papildu vispārējās plānošanas izpildi**, Ganta diagrammā var apskatīt papildu vispārējo plānošanu un salīdzināt abus darbus.

#### <a name="bom-level-display"></a>MK līmeņa displejs

Materiālu komplekta (MK) līmeņi tiek parādīti dažādi segumi plānošanai, kavējumiem, darbībām un apstiprināšanai.

- **Vajadzību plānošana** – MK līmeņi tiek parādīti, kā paredzēts. Tie tiek aprēķināti no augšmalas.

    **Piemērs:** MK līmenis 0, 1, 2

- **Kavēšanās** – MK līmeņi tiek parādīti kā seguma plānošanas MK līmeņi, kas reizināti ar –1. (Citiem vārdiem, tiem ir negatīva zīme.)

    **Piemērs:** MK līmenis –2, –1, 0

- **Darbības ziņojums** – MK līmeņi tiek parādīti, kā paredzēts. Tie tiek aprēķināti no augšmalas.

    **Piemērs:** MK līmenis 0, 1, 2

- **Automātiskā apstiprināšana** — MK līmeņi tiek parādīti kā 999 mīnus seguma plānošanas MK līmenis.

    **Piemērs:** MK līmenis 999, 998, 997

Sekojošajā tabulā ir apkopotas darbības.

| Parādītais MK līmenis | Galaprodukts | Apakškomponents | Izejmateriāls |
|---|---|---|---|
| Vajadzību plānošana | 0 | 1. | 2. |
| Aizkaves | 0 | –1 | –2 |
| Optimizācijas priekšlikums | 0 | 1. | 2. |
| Automātiskā apstiprināšana | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Norises vizualizēšana

Ja skatāt vispārējās plānošanas darbu, kas pašlaik tiek palaists, Ganta diagrammā tiek rādīta norise ar krāsām. Sekojošās krāsas attiecas uz zilo krāsu dizainu. Citiem krāsu dizainiem krāsas atšķirsies.

- **Tumši zils** – pabeigti plānošanas uzdevumi.
- **Oranžs** — uzdevums pašlaik darbībā.
- **Gaiši zils** — atlikušo uzdevumu novērtējums.

Krāsa tiek rādīta tikai zemākajā Ganta diagrammas līmenī. Atlasiet **Izvērst visu**, lai skatītu visus uzdevumus vispārējā plānošanas darbā. Atlikušo uzdevumu novērtējums ir balstīts uz vēsturiskiem vispārējiem plānošanas darbiem.

## <a name="run-master-planning-and-track-processing-time"></a>Veikt vispārējo plānošanu un izsekot apstrādes laiku

1. Noklusējuma informācijas panelī atlasiet **Vispārējā plānošana**.
1. Laukā **Plāns** ievadiet vai atlasiet kādu vērtību.
1. Atlasiet **Izpildīt**.
1. Iestatiet **Izsekot apstrādes laiku** opciju uz **Jā**.
1. Laukā **Pavedienu skaits** ievadiet skaitli.
1. Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.
1. Režģī atlasiet rindu, kur **Lauks** ir iestatīts uz **Krājuma kods**.
1. Laukā **Kritērijs** ievadiet vērtību.
1. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]