---
title: Rādīt atlikušo atvaļinājuma dienu skaitu ražošanas izpildes interfeisā
description: Šajā rakstā ir sniegts piemēra scenārijs, kurā parādīts, kā iestatīt Microsoft Dynamics 365 Supply Chain Management, lai tā varētu izmantot algu statistiku, lai sniegtu darbiniekiem viņu atvaļinājuma bilances apskatu par pašreizējo gadu.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852278"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Rādīt atlikušo atvaļinājuma dienu skaitu ražošanas izpildes interfeisā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts piemēra scenārijs, kurā parādīts, kā iestatīt Microsoft Dynamics 365 Supply Chain Management, lai tā varētu izmantot algu statistiku, lai sniegtu katram darbiniekam pārskatu par viņu atvaļinājuma bilanci šajā gadā. Darbinieki varēs redzēt savu atvaļinājuma bilanci **ražošanas izpildes** interfeisa dialoglodziņā Mana diena.

Šajā scenārijā tiek lietots Dānijas svētku dienu likums, kur atvaļinājuma gads ir no 1. septembra līdz 31. augustam. Šajā scenārijā jūsu uzņēmums ir nolīgis jaunu darbinieku un šim darbiniekam tiks piešķirta bilance 10 atvaļinājuma dienu laikā par atlikušo atvaļinājuma gadu.

## <a name="turn-on-the-required-features"></a>Ieslēgt nepieciešamos līdzekļus

Lai palaistu šo scenāriju, ražošanas izpildes *interfeisa līdzeklim funkciju pārvaldībā jāiespējo skats*["Mana diena"](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Papildinformāciju par to, kā aktivizēt šo un citas funkcijas ražošanas izpildes interfeisam, skatiet sadaļā [Ražošanas izpildes interfeisa konfigurēšana](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Padarīt pieejamus datu paraugus

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.

## <a name="create-a-new-pay-type"></a>Izveidot jaunu apmaksas tipu

Sāciet ar jauna apmaksas *tipa izveidi,* kas atsecēs darbinieku nopelnītās atvaļinājuma dienas (tiek sauktas arī par viņu atvaļinājuma *bilanci*). Parasti apmaksas tipus izmanto, lai aprēķinātu darbinieku apmaksu. Tomēr šeit izveidotais apmaksas tips tiks izmantots bilances jāaprēķina.

1. Pārejiet uz **sadaļu Laika un apmeklētības \> iestatīšanas \> algu \> apmaksas tipi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunā rindā iestatiet šādas vērtības:

    - **Apmaksas tips:** *5151-1*
    - **Apraksts: skaitītājs** *darbinieka atvaļinājuma dienām*
    - **Iekļaut eksportā:** *Nē*

## <a name="update-the-pay-agreement"></a>Atjaunināt apmaksas līgumu

Šajā sadaļā labosiet esošu apmaksas līgumu, pievienojot jaunu apmaksas tipu un iestatot noteikumus, *kas* definēs, kā katra darbinieka atvaļinājuma bilance tiek koriģēta, kad tiek reģistrētas atvaļinājuma dienas.

1. Dodieties uz **Laika un apmeklētības \> iestatīšanas \> algu \> algu līgumus**.
1. Atlasiet apmaksas līgumu, kam vēlaties iestatīt atvaļinājuma politiku. (Ja strādājat ar standarta USMF parauga datiem, ir tikai viens apmaksas līgums, *Man*.)
1. Pārliecinieties, vai atlasītais apmaksas līgums ir derīgs pašreizējam datumam. Ja strādājat ar standarta USMF parauga datiem, **·** *man* apmaksas līguma lauka Līdz datumam vērtība var būt iestatīta uz pagājušu datumu. Pēc vajadzības mainiet vērtību tā, lai tas būtu gads vai divi nākotnē.
1. Darbību rūtī atlasiet līguma **rindas**.
1. **Lapas Apmaksas līguma** rindas kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības rīkjoslā:

    - Pirmajā nolaižamajā sarakstā atlasiet **pirmdienu**.
    - Otrajā nolaižamajā sarakstā atlasiet **Kavējums**.

1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet apmaksas tipa lauku **uz** apmaksas tipu, ko izveidojāt šim scenārijam (*5151-1*). Atstājiet visus pārējos laukus iestatītus uz to noklusētajām vērtībām.
1. Kamēr jaunā rinda joprojām ir atlasīta, Kopsavilkuma cilnē **Vispārīgi** iestatiet šādas vērtības:

    - **Kavējuma kods: atvaļinājums** *·*
    - **Izmantot fiksētu daudzumu:** *Jā*
    - **Konstante:** *-1*

1. Darbību rūtī atlasiet Kopēt **dienu**.
1. **Dialoglodziņā Dienas kopēšana** iestatiet šādas vērtības:

    - **Otrdiena**, **trešdiena**, **ceturtdiena** un piektdiena **:** *Jā*
    - **Pārrakstīt:** *Jā*
    - **Kavējums:** *Jā*

1. Atlasiet **Labi**.

## <a name="create-a-payroll-statistic-group"></a>Algas statistikas grupas izveide

*Algu statistikas grupas tiek lietotas*, lai perioda laikā iestatītu darbinieku reģistrācijas statistiku. Šajā scenārijā izmantosiet algu statistikas grupu, lai aprēķinātu atvaļinājuma dienu skaitu, ko darbinieki nopelna atvaļinājuma periodā. Dānijā atvaļinājuma periods ir no 1. septembra līdz 31. augustam.

1. Dodieties **uz laika un apmeklētības \>\> iestatīšanas algu \> algu statistikas grupām**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunā rindā iestatiet šādas vērtības:

    - **Algu statistikas grupa:** *APMAKSĀJAMS*
    - **Apraksts: atvaļinājuma** *bilance*
    - **Pārskaitījums:** *Nr.*

1. Kamēr jaunā rinda joprojām ir atlasīta, **atlasiet** Iestatījumi darbību rūtī.
1. Lai režģim **pievienotu** rindu, **Darbību** rūtī iestatīšanas lapā atlasiet Jauns.
1. Jaunajā rindā iestatiet apmaksas tipa **lauku uz** *5151-1*.
1. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) perioda **koda lauku** un pēc tam atlasiet Skatīt **detalizētu informāciju**. Tagad varat iestatīt perioda kodu, kuru vēlāk piešķirsiet šim laukam.
1. Lai režģim **pievienotu** rindu, Perioda **tipu** lapā Darbību rūtī atlasiet Jauns.
1. Jaunā rindā iestatiet šādas vērtības:

    - **Perioda tipi:** *Year*
    - **Apraksts: atvaļinājuma** *gads*
    - **Biežums:** *gadi*

1. Kamēr ir atlasīta jaunā rinda, darbību rūtī **atlasiet Ģenerēt** periodus.
1. Dialoglodziņā Periodu **ģenerēšanas** iestatiet šādas vērtības:

    - **Norādīt perioda sākuma datumu:** *2021. gada 1. septembris*
    - **Perioda ilgums:** *5*

1. Atlasiet **Labi**.
1. Aizveriet lapu **Perioda tipi**, lai atgrieztos **algu statistikas grupu** lapā.
1. Iestatiet tikko **izveidotā** perioda koda lauku Perioda tips (*YearYear*).

## <a name="create-a-statistical-balance-setup"></a>Statistikas bilances iestatījumu izveide

Šajā sadaļā jums tiks izveidots statistikas *bilances iestatījums*, kas ir saistīts ar algas statistikas grupu, kuru izveidojāt iepriekšējā sadaļā. Vēlāk ražošanas izpildes interfeisā šo statistiskās **bilances** iestatījumu saistīsiet ar skatu Mana diena. Tad **mans dienas** skats varēs parādīt atvaļinājuma bilances apmaksas tipam, kas ir piešķirts saistītai algu statistikas grupai.

1. Pārejiet uz **sadaļu Laika un apmeklētības \> iestatīšanas \> algu \> statistiskās bilances iestatījumi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Jaunā rindā iestatiet šādas vērtības:

    - **Algu statistikas grupa:** *APMAKSĀJAMS*
    - **Ārējais nosaukums:** *atvaļinājuma bilance*
    - **Brīvā režīma:** *Nē*

## <a name="create-a-manual-premium"></a>Manuālas prēmijas izveide

*Manuālās prēmijas* parasti tiek izmantotas, lai piešķirtu darbiniekiem papildu apmaksu par papildu darbu. Šajā scenārijā izveidosiet manuālu prēmiju, ko varat izmantot, lai iestatītu sākotnējo atvaļinājuma bilanci katram darbiniekam.

1. Dodieties uz **Laika un apmeklētības \> iestatīšanas \> algu manuālās \> prēmijas**.
1. Darbību rūtī atlasiet Jauns **, lai** pievienotu ierakstu.
1. Jaunajā ierakstā iestatiet šādas vērtības:

    - **Prēmijas:** *SASKAŅĀ ARV*
    - **Apraksts:** *Darbinieku atvaļinājuma bilances korekcijas*
    - **Apmaksas tips:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Iestatīt darbinieka sākotnējo atvaļinājuma bilanci un koriģēt to par vienu dienu

Algu administratori izmanto lapu **Apstiprināt**, lai pārskatītu un apstiprinātu darbinieku ikdienas reģistrācijas. Šajā scenārijā jūs veiksiet administratora lomu, lai varētu iestatīt sākotnējo darbinieka atvaļinājuma bilanci un reģistrēt darbinieka atvaļinājuma dienas.

1. Dodieties uz **laiku un apmeklētības pārskatīšanu \> un apstipriniet \> apstiprināšanu**.
1. **Dialoglodziņā Apstiprināt** iestatiet šādus laukus:

    - **Apstiprinājumu grupa** – atlasiet apstiprinājumu grupu, kurai piederat. (Ja strādājat ar standarta USMF parauga datiem, ir tikai viena apstiprinājumu grupa, *AdmMan*.)
    - **Skatīt visu grupu, 1 dienu** – atlasīt opciju un pēc tam iestatīt lauku uz pašreizējo datumu.

1. Atlasiet **Labi**.
1. Lapa **Apstiprināt** parāda sarakstu ar ierakstiem, kas atbilst jūsu kritērijiem. Atlasiet darbinieku, kuru vēlaties apstiprināt. Ja strādājat ar standarta USMF parauga datiem, atlasiet darbinieka *000496* (Šī uzrādāmā *portra*).
1. Piešķirt atlasītajam darbiniekam 10 atvaļinājuma dienas:

    1. Kamēr darbinieks joprojām ir atlasīts **, atlasiet Prēmijas** rindas darbību rūtī.
    1. Lai režģim **pievienotu** rindu, prēmijas rindu **lapā** Darbību rūtī atlasiet Jauns.
    1. Jaunā rindā iestatiet šādas vērtības:

        - **Prēmijas:** *SASKAŅĀ ARV*
        - **Daudzums:** *10*

    1. Aizveriet lapu **Prēmijas** rindas.

1. Apstiprināšanas lapā **reģistrējiet** faktu, ka darbinieks ir izmantojis vienu no viņu atvaļinājuma dienām pašreizējā datumā:

    1. Kamēr darbinieks joprojām ir atlasīts, **lapas apakšējā daļā cilnē Pārskats** rīkjoslā atlasiet Jauns, **lai** režģim pievienotu rindu.
    1. Jaunā rindā iestatiet šādas vērtības:

        - **Žurnāla reģistrācijas tips: Kavējums** *·*
        - **Atsauce: Atvaļinājums** *·*

    1. Lapas augšējā daļā rīkjoslā atlasiet Pārsūtīt, lai **lietotu** atvaļinājuma bilanci un aprēķinātu ieturējumus.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfigurējiet ražošanas izpildes interfeisu, lai tajā būtu ietverts dialoglodziņš Mana diena

Šajā sadaļā ražošanas izpildes interfeisam **pievienosiet** pogu Mana diena. Tad darbinieki var izmantot šo pogu, lai atvērtu **dialoglodziņu** Mana diena.

1. Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.
1. Atlasiet konfigurāciju, piemēram, Noklusējums *·*.
1. Darbību rūtī atlasiet cilnes **Dizains**.
1. **Saraksta rūts lapā** Dizains atlasiet Visi darbi, *lai* skatītu šīs cilnes iestatījumus. Galvenā **skata laukam** tagad ir jārāda visu *darbu vērtība*.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnes **Sekundāra rīku** josla kolonnā Pieejamās **darbības** atlasiet **Mana diena**. Pēc tam atlasiet labās bultiņas pogu, lai pārvietotu to uz kolonnu **Atlasītās** darbības.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Pārbaudīt bilanci ražošanas izpildes interfeisā

Šajā sadaļā pieteiksieties ražošanas izpildes interfeisā kā darbiniekam, kura iepriekš iestatītais atvaļinājuma laiks. Tad atvērsiet dialoglodziņu **Mana diena**, lai skatītu atvaļinājuma bilanci.

1. Dodieties uz Ražošanas kontroles **iestatījums \> Ražošanas izpilde \> Ražošanas izpilde \>.**
1. Ja tiek piedāvāts atlasīt konfigurāciju, atlasiet konfigurāciju, kuru iepriekš iestatījāt šajā scenārijā (Noklusējums *·*).
1. Pieteikties kā lietotājs, kuru iepriekš iestatījāt šajā scenārijā. Ja strādājat ar standarta USMF parauga datiem, jums ir jāpiesakās, *ievadot 123* **žetona ID** laukā. Šis žetona ID atbilst Siana Portra.
1. Izvēlieties **Mana diena** kreisajā rīkjoslā.
1. Pārbaudiet dialoglodziņa **sadaļu** Bilances. Šajā sadaļā tagad jāparāda, ka jums ir deviņas atvaļinājuma dienas bilance.
