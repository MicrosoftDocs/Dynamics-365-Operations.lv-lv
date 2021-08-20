---
title: Sūtījumu konsolidācijas politiku konfigurēšana
description: Šajā tēmā skaidrots, kā iestatīt noklusētās un pielāgotas sūtījumu konsolidācijas politikas.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 51e66cf025db06d9864ce78ba4118dc95f401acb2d1654fcf785a5649629b7f9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735924"
---
# <a name="configure-shipment-consolidation-policies"></a>Sūtījumu konsolidācijas politiku konfigurēšana

[!include [banner](../includes/banner.md)]

Sūtījumu konsolidācijas process, kas izmanto sūtījuma konsolidācijas politikas, atļauj sūtījuma konsolidāciju automātiskās un manuālās nodošanas noliktavā laikā. Pēc šī līdzekļa ieslēgšanas jums ir jākonfigurē sākotnējās politikas. Ja neviena politika netiek konfigurēta, katra pārdošanas rinda ģenerēs atsevišķu sūtījumu, kurai ir viena noslodzes rinda.

Šajā tēmā norādītie scenāriji rāda, kā iestatīt noklusējuma un pielāgotas sūtījumu konsolidācijas politikas.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Ieslēgt Sūtījumu konsolidācijas politiku līdzekli

> [!IMPORTANT]
> [Pirmajā scenārijā](#scenario-1), kas aprakstīts šajā tēmā, vispirms ir jāiestata noliktava, lai tiktu izmantota agrākā sūtījumu konsolidācijas funkcija. Tad būs pieejamas sūtījuma konsolidācijas politikas. Šādā veidā varat izbaudīt jaunināšanas scenārija darbību. Ja plānojat izmantot demonstrācijas datu vidi, lai ietu cauri pirmajam scenārijam, neieslēdziet līdzekli pirms scenārija izmantošanas.

Lai varētu izmantot *Sūtījumu konsolidācijas politikas* līdzekli, tas ir jāieslēdz sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Konsolidēt sūtījumu*

## <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Katrs scenārijs šajā tēmā atsaucas uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu **USMF**, pirms sākat darbu.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>1. scenārijs: Noklusējuma sūtījumu konsolidācijas politiku konfigurēšana

Ir divi gadījumi, kad ir jākonfigurē noklusējuma politiku minimālais skaits pēc tam, kad ieslēdzat *Sūtījuma konsolidācijas politiku* līdzekli:

- Tiek jaunināta vide, kurā jau ir dati.
- Jūs iestatāt pavisam jaunu vidi.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Jaunināt vidi, kur noliktavas jau ir konfigurētas starppasūtījuma konsolidācijai

Kad sākat šo procedūru, ir jāizslēdz *Sūtījuma konsolidācijas politiku* līdzeklis, lai simulētu vidi, kur pamata starppasūtījumu konsolidācijas līdzeklis jau ticis izmantots. Pēc tam varat izmantot līdzekļu pārvaldību, lai ieslēgtu šo līdzekli, lai varētu uzzināt par to, kā iestatīt sūtījuma konsolidācijas politikas pēc jaunināšanas.

Sekojiet šiem soļiem, lai iestatītu noklusējuma sūtījuma konsolidācijas politikas vidē, kur noliktavas jau ir konfigurētas starppasūtījumu konsolidācijai.

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Noliktava \> Noliktavas**.
1. Sarakstā atrodiet un atveriet vēlamo noliktavas ierakstu (piemēram, noliktava *24* **USMF** demonstrācijas datos).
1. Darbību rūtī atlasiet **Rediģēt**.
1. Kopsavilkuma cilnē **Noliktava** iestatiet opciju **Konsolidēt sūtījumu, pārvietojot uz noliktavu** uz *Jā*.
1. Atkārtojiet 2.-4. soli pārējām noliktavām, kurās nepieciešama konsolidācija.
1. Aizvērt lapu.
1. Izmantojiet [līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu *Sūtījuma konsolidācijas politiku* līdzekli. **Līdzekļu pārvaldības** darbvietā līdzekļa nosaukums ir *Konsolidēt sūtījumu*.
1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**. Iespējams, būs jāatsvaidzina pārlūkprogramma, lai skatītu jauno **Sūtījuma konsolidācijas politiku** izvēlnes krājumu pēc līdzekļa ieslēgšanas.
1. Darbību rūtī atlasiet **Izveidot noklusēto iestatījumus**, lai izveidotu šādas politikas:

    - **Starppasūtījuma** politika *Pārdošanas pasūtījumu* politikas veidam (ar nosacījumu, ka jums ir vismaz viena noliktava, kas iestatīta agrākas konsolidācijas funkcijas izmantošanai)
    - **Noklusējuma** politika *Pārdošanas pasūtījumu* politikas veidam
    - **Noklusējuma** politika *Pārvietošanas jautājuma* politikas veidam
    - **Starppasūtījuma** politika *Pārvietošanas jautājuma* politikas veidam (ar nosacījumu, ka jums ir vismaz viena noliktava, kas iestatīta agrākas konsolidācijas funkcijas izmantošanai)

    > [!NOTE]
    > - Abām **CrossOrder** politikām ir tāda pati lauku kopa kā iepriekšējā loģikā, izņemot laukam Pasūtījuma numurs. (Šis lauks tiek izmantots, lai konsolidētu rindas sūtījumos, pamatojoties uz tādiem faktoriem kā noliktava, piegādes transportēšanas veidu un adrese.)
    > - Abām **Noklusējuma** politikām ir tāda pati lauku kopa kā iepriekšējā loģikā, ieskaitot lauku Pasūtījuma numurs. (Šis lauks tiek izmantots, lai nkonsolidētu rindas sūtījumos, pamatojoties uz tādiem faktoriem kā pasūtījuma numurs, noliktava, piegādes transportēšanas veids un adrese.)

1. Atlasiet **CrossOrder** politiku *Pārdošanas pasūtījumu* politikas veidam un pēc tam darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā ņemiet vērā, ka noliktavas, kurās opcija **Konsolidēt sūtījumu, pārvietot uz noliktavu** ir iestatīta uz *Jā*. Tāpēc tās ir iekļautas vaicājumā.

### <a name="create-default-policies-for-a-new-environment"></a>Izveidot noklusējuma politikas jaunajai videi

Sekojiet šiem soļiem, lai iestatītu noklusējuma sūtījuma konsolidācijas politikas pavisam jaunā vidē.

1. Izmantojiet [līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu *Sūtījuma konsolidācijas politiku* līdzekli, ja tas jau nav ieslēgts. **Līdzekļu pārvaldības** darbvietā līdzekļa nosaukums ir *Konsolidēt sūtījumu*.
1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Darbību rūtī atlasiet **Izveidot noklusēto iestatījumus**, lai izveidotu šādas politikas:

    - **Noklusējuma** politika *Pārdošanas pasūtījumu* politikas veidam
    - **Noklusējuma** politika *Pārvietošanas jautājuma* politikas veidam

    > [!NOTE]
    > Abām **Noklusējuma** politikām ir tāda pati lauku kopa kā iepriekšējā loģikā, ieskaitot lauku Pasūtījuma numurs. (Šis lauks tiek izmantots, lai nkonsolidētu rindas sūtījumos, pamatojoties uz tādiem faktoriem kā pasūtījuma numurs, noliktava, piegādes transportēšanas veids un adrese.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>2. scenārijs: Pielāgoto sūtījumu konsolidācijas politiku konfigurēšana

Šajā scenārijā parādīts, kā iestatīt pielāgotas sūtījuma konsolidācijas politikas. Pielāgotās politikas var atbalstīt kompleksas biznesa prasības, kur sūtījumu konsolidācija ir atkarīga no vairākiem nosacījumiem. Katrai šīs jomas politikai vēlāk šajā scenārijā ir ietverts īss biznesa scenārija apraksts. Šīs piemēru politikas ir jāiestata secībā, kas nodrošina vaicājumu piramīdveida novērtējumu. (Citiem vārdiem, politikas, kurām ir visvairāk nosacījumu, ir jānovērtē kā augstākā prioritāte.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Ieslēdziet līdzekli un sagatavojiet pamatdatus šim scenārijam

Pirms jūs varat iziet cauri vingrinājumiem šajā scenārijā, jums jāieslēdz līdzeklis un jāsagatavo pamatdati, kas nepieciešami, lai veiktu filtrēšanu, kā aprakstīts turpmākajās apakšsadaļās. (Šie priekšnosacījumi attiecas arī uz scenārijiem, kas uzskaitīti sadaļā [Piemēru scenāriji, kā izmantot sūtījuma konsolidācijas politikas](#example-scenarios).)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Ieslēgt šo līdzekli un izveidot noklusējuma politikas

Izmantojiet līdzekļu pārvaldību, lai ieslēgtu šo līdzekli, ja to vēl neesat ieslēdzis, un izveidojiet noklusējuma konsolidācijas politikas, kas ir aprakstītas [1. scenārijā](#scenario-1).

#### <a name="create-two-new-product-filter-codes"></a>Izveidot divus jaunus preces filtra kodus

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Preces filtri \> Preces filtri** un pievienojiet divus preču filtrus:

    - Preču filtrs 1:

        - **Filtra kods:** *Uzliesmojošs*
        - **Filtra nosaukums:** *4. kods*

    - Preču filtrs 2:

        - **Filtra kods:** *Sprādzienbīstams*
        - **Filtra nosaukums:** *4. kods*

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet preci, kuras krājuma kods ir *M9200*. (Jūsu atlasītajai precei ir jābūt iespējotai papildu noliktavas \[WMS\] procesiem, un šis produkts ir iepriekš iespējots WMS procesiem **USMF** demonstrācijas datos.)
1. Kopsavilkuma cilnē **Noliktava** iestatiet lauku **4. kods** uz *Uzliesmojošs*.
1. Aizvērt lapu.
1. Atveriet preci, kuras krājuma kods ir *M9201*. (Šī prece ir arī iepriekš iespējota WMS procesiem **USMF** demonstrācijas datos.)
1. Kopsavilkuma cilnē **Noliktava** iestatiet lauku **4. kods** uz *Sprādzienbīstams*.
1. Aizvērt lapu.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Izveidojiet jaunu piegādes transportēšanas veidu

1. Pārejiet uz sadaļu **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Režīms**.
1. Izveidojiet transportēšanas veidu, kas tiks izmantots konsolidācijas vaicājumos, un nosauciet to par *Gaisa*.
1. Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Sūtījumu pārvadātāji**.
1. Izveidojiet pārvadātāju, kam ir turpmāk aprakstītie iestatījumi:

    - **Sūtījuma pārvadātājs:** *Gaisa*
    - **Nosaukums:** *Gaisa*
    - **Režīms:** *Gaisa*

1. Jaunā pārvadātāja kopsavilkuma cilnē **Pakalpojumi** pievienojiet rindu, kurai ir šādi iestatījumi:

    - **Pārvadātāja pakalpojums:** *Gaisa*
    - **Transportēšanas metode:** *Gaisa*

1. Darbību rūtī atlasiet **Saglabāt**.

    > [!NOTE]
    > Kad saglabāsit jauno pārvadātāju, **Piegādes veida** lauks jaunajai rindai **Pakalpojumu** režģī automātiski tiek iestatīts uz *Airwa-Air*. Kad izmantojat *Airwa-Air* piegādes veidu pārdošanas pasūtījumam, *Gaisa* transportēšanas režīms tiks izmantots saistītajiem sūtījumiem.

#### <a name="create-an-order-pool"></a>Izveidojiet pasūtījumu kopu

1. Dodieties uz **Pārdošana un mārketings \> Iestatījumi \> Pārdošanas pasūtījumi \> Pasūtījumu kopas**.
1. Izveidojiet pasūtījuma kopu, kas tiks izmantota konsolidācijas vaicājumam. Šai pasūtījumu kopai ir jābūt šādiem iestatījumiem:

    - **Kopa:** ievadiet veselu skaitli, kas vēl nav izmantots citā kopā.
    - **Nosaukums:** *ShipCons*

1. Dodieties uz **Pārdošana un mārketings \> Debitori \> Visi debitori**.
1. Atveriet debitoru, kam ir konta numurs *US-003*.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma noklusējumu** iestatiet **Pārdošanas pasūtījumu kopas** lauku jūsu tikko izveidotajai pasūtījuma kopai.
1. Aizveriet lapu un pēc tam atkārtojiet 4. un 5. soli debitoram, kam ir konta numurs *ASV-004*.

### <a name="create-example-policy-1"></a>Izveidot piemēru politiku 1

Šajā piemērā tiks izveidota *Debitors + režīms* politika, ko var izmantot šādiem biznesa gadījumiem:

- Politika veiks vaicājumu noteiktam debitora kontam (*US-001*) un noteiktam piegādes veidam (*Airwa-Air*).
- Konsolidācija ar atvērtiem sūtījumiem ir izslēgta.
- Konsolidācija tiek veikta pēc pasūtījuma ID. (Citiem vārdiem, katrā pasūtījumā, noliktavā, un tā tālāk būs atsevišķi sūtījumi.)

Sekojiet šiem soļiem, lai izveidotu sūtījuma konsolidācijas politiku šim biznesa gadījumam.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu politiku, kurai ir šādi iestatījumi:

    - **Politikas nosaukums:** *CustomerMode*
    - **Politikas apraksts:** *Debitora konts un piegādes veids*

1. Atstājiet opciju **Konsolidēt ar atvērtu sūtījumu** uz *Nē*.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Konsolidācijas lauki** sarakstā **Atlikušie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Piegādes veids*.
1. Atlasiet **Pievienot** pogu ![Labā bultiņa.](media/forward-button.png) lai pārvietotu lauku uz **Atlasītie lauki** sarakstu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Dialoglodziņa vaicājumu redaktorā cilnē **Diapazons**, kas atrodas režģī, atrodiet rindu, kur **Lauka** lauks ir iestatīts uz *Debitora konts*, un iestatiet lauku **Kritēriji** uz *US-001*.
1. Atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:

    - **Tabula:** *Pasūtījuma rindas*
    - **Atveidotā tabula:** *Pasūtījuma rindas*
    - **Lauks:** *Piegādes veids*
    - **Kritēriji:** *Airwa-Air*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

> [!NOTE]
> Šim biznesa gadījumam pasūtījuma rindas debitoram *US-001*, kas izmanto *Airwa-Air* piegādes veidu, netiks konsolidētas starp pasūtījumiem. Šo politiku ir paredzēts izmantot secībā vispirms gadījumos, kad visi pārējie piegādes veidi tiek konsolidēti šim debitoram.

### <a name="create-example-policy-2"></a>Izveidot piemēru politiku 2

Šajā piemērā tiks izveidota *Bīstamas preces* politika, ko var izmantot šādiem biznesa gadījumiem:

- Politika veiks vaicājumu noteiktam filtra kodam (*bīstams*) un noteiktam piegādes veidam (*Airwa-Air*).
- Konsolidācija ar atvērtiem sūtījumiem ir ieslēgta.
- Konsolidācija tiek veikta starp pasūtījumiem. (Citiem vārdiem sakot, katrā kontā, noliktavā un tā tālāk būs atsevišķi sūtījumi, bet tikai krājumu grupas ietvaros, kas norādīti vaicājumā.)

Sekojiet šiem soļiem, lai izveidotu sūtījuma konsolidācijas politiku šim biznesa gadījumam.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu politiku, kurai ir šādi iestatījumi:

    - **Politikas nosaukums:** *Krājuma veids*
    - **Politikas apraksts:** *Konsolidējiet viena krājuma veidu starp pasūtījumiem*

1. Iestatiet opciju **Konsolidēt ar atvērtu sūtījumu** uz *Jā*.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Konsolidācijas lauki** sarakstā **Atlikušie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Piegādes veids*.
1. Atlasiet **Pievienot** pogu ![Labā bultiņa.](media/forward-button.png) lai pārvietotu lauku uz **Atlasītie lauki** sarakstu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā cilnē **Savienojumi** izvērsiet un atlasiet **Tabulas \> Noslodzes detaļas** kokā.
1. Atlasiet **Pievienot tabulu savienojumu**.
1. Parādītajā relāciju režģī meklējiet un atlasiet rindu, kur **Relāciju** lauks ir iestatīts uz *Noliktavas krājuma numurs (preces numurs)*, un pēc tam atlasiet **Atlasīt**. 
1. Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:

    - **Tabula:** *Noliktavas krājuma numurs*
    - **Atveidotā tabula:** *Noliktavas krājuma numurs*
    - **Lauks:** *4. kods*
    - **Kritēriji:** *Uzliesmojošs*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

> [!NOTE]
> Šim biznesa gadījumam visām pasūtījuma rindām, kur krājumiem ir noteikts filtra kods (tas ir, filtra kods, kura **4. koda** lauks ir iestatīts uz *Uzliesmojošs*) tiks konsolidēts ar citiem tā paša veida krājumiem pasūtījumos. Ja ir atvērts sūtījums tam pašam kontam, noliktavai un krājumu grupai, jaunas rindas tai tiks pievienotas.

### <a name="create-example-policy-3"></a>Izveidot piemēru politiku 3

Šajā piemērā tiks izveidota *Debitoru prasību* politika, ko var izmantot šādiem biznesa gadījumiem:

- Politika veiks vaicājumu noteiktam debitora kontam.
- Konsolidācija ar atvērtiem sūtījumiem ir ieslēgta.
- Konsolidācija tiek veikta pāri pasūtījumiem, bet balstās uz debitora pieprasījumiem. (Citiem vārdiem, vairāki pasūtījumi tiks grupēti sūtījumos, pamatojoties uz to pašu debitora pieprasījuma numuru un noliktavu.)

Sekojiet šiem soļiem, lai izveidotu sūtījuma konsolidācijas politiku šim biznesa gadījumam.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu politiku, kurai ir šādi iestatījumi:

    - **Politikas nosaukums:** *CustomerOrderNo*
    - **Politikas apraksts:** *Konsolidēt rindas, pamatojoties uz debitoru PO*

1. Iestatiet opciju **Konsolidēt ar atvērtu sūtījumu** uz *Jā*.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Konsolidācijas lauki** sarakstā **Atlikušie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Debitora pieprasījums*.
1. Atlasiet **Pievienot** pogu ![Labā bultiņa.](media/forward-button.png) lai pārvietotu lauku uz **Atlasītie lauki** sarakstu.
1. Sarakstā **Atlikušie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Piegādes veids*.
1. Atlasiet **Pievienot** pogu ![Labā bultiņa.](media/forward-button.png) lai pārvietotu lauku uz **Atlasītie lauki** sarakstu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Dialoglodziņa vaicājumu redaktorā cilnē **Diapazons** atrodiet rindu, kur **Lauka** lauks ir iestatīts uz *Debitora konts*, un iestatiet lauku **Kritēriji** uz *US-001*.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

> [!NOTE]
> Šim biznesa gadījumam visas pasūtījuma rindas, kur pārdošanas pasūtījumiem ir viens un tas pats debitora pieprasījuma numurs, tiks konsolidētas vienā sūtījumā neatkarīgi no pārdošanas pasūtījuma numura. (Debitora pieprasījuma numurs tiek izmantots kā debitora pirkšanas pasūtījuma \[PP\] numurs.) Ja ir atvērti sūtījumi vienam un tam pašam kontam, noliktavai un debitora pieprasījumam, jaunas rindas tai tiks pievienotas. Šo politiku var izmantot, ja debitors nosūta papildu pasūtījuma rindas, kurām dienas laikā ir vairāki PP numuri, un vēlas, lai visas rindas tiktu grupētas vienā sūtījumā. (Citiem vārdiem sakot, būs viena preču transporta pavadzīme un viena pavadzīme.)

### <a name="create-example-policy-4"></a>Izveidot piemēru politiku 4

Šajā piemērā tiks izveidota *Debitori, kas atļauj konsolidāciju* politika, ko var izmantot šādiem biznesa gadījumiem:

- Politika veiks vaicājumu noteiktai pasūtījumu kopai, lai identificētu debitorus, kuri pieņem konsolidētos sūtījumus.
- Konsolidācija ar atvērtiem sūtījumiem ir izslēgta.
- Konsolidācija tiek veikta pāri pasūtījumiem, izmantojot laukus, kas atlasīti pēc noklusējuma CrossOrder politikas (lai replicētu iepriekšējo izvēles rūtiņu **Konsolidēt sūtījumu, izlaižot to uz noliktavu** ).

- Jūs varat ignorēt kārtulu pārdošanas pasūtījumā, atlasot citu pasūtījuma kopu.

Sekojiet šiem soļiem, lai izveidotu sūtījuma konsolidācijas politiku šim biznesa gadījumam.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu politiku, kurai ir šādi iestatījumi:

    - **Politikas nosaukums:** *Pasūtījuma kopa*
    - **Politikas apraksts:** *Konsolidēt starp pasūtījumiem, kas balstīti uz pasūtījumu kopu*

1. Atstājiet opciju **Konsolidēt ar atvērtu sūtījumu** uz *Nē*.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Konsolidācijas lauki** sarakstā **Atlikušie lauki**, atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Piegādes veids*.
1. Atlasiet **Pievienot** pogu ![Labā bultiņa.](media/forward-button.png) lai pārvietotu lauku uz **Atlasītie lauki** sarakstu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājuma redaktora dialoglodziņā cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu, kurai režģī ir šādi iestatījumi:

    - **Tabula:** *Pārdošanas pasūtījumi*
    - **Atveidotā tabula:** *Pārdošanas pasūtījumi*
    - **Lauks:** *Kopa*
    - **Kritēriji:** *ShipCons*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

> [!NOTE]
> Šim biznesa gadījumam visas pasūtījuma rindas, kurās pārdošanas pasūtījumi pieder vienai pasūtījumu kopai, tiks konsolidētas vienā sūtījumā pāri pārdošanas pasūtījumiem vienam kontam, noliktavai un piegādes transportēšanas veidam. Pasūtījuma kopas vietā var izmantot jebkuru citu lauku, lai atšķirtu debitoru grupu un pēc noklusējuma izmantotu pārdošanas pasūtījuma virsrakstu. Šo pieeju jūs varat izmantot, ja debitors, nevis noliktava, virza vajadzību pēc konsolidācijas. (Iepriekšējā konsolidācijas loģikā noliktava noveda pie konsolidācijas nepieciešamības.)

### <a name="create-example-policy-5"></a>Izveidot piemēru politiku 5

Šajā piemērā tiks izveidota *Noliktavas, kas atļauj konsolidāciju* politika, ko var izmantot šādiem biznesa gadījumiem:

- Politika veiks vaicājumu noteiktai pasūtījumu kopai, lai identificētu noliktavas, kuras var konsolidēt sūtījumus.
- Konsolidācija ar atvērtiem sūtījumiem ir izslēgta.
- Konsolidācija tiek veikta pāri pasūtījumiem, izmantojot laukus, kas atlasīti pēc noklusējuma CrossOrder politikas (lai replicētu iepriekšējo izvēles rūtiņu **Konsolidēt sūtījumu, izlaižot to uz noliktavu** ).

Parasti šo biznesa gadījumu var risināt, izmantojot noklusējuma politikas, ko izveidojāt [1. scenārijā](#scenario-1). Tomēr varat arī manuāli izveidot līdzīgas politikas, veicot šādas darbības.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Darbību rūtī atlasiet **Jauns**, lai izveidotu politiku, kurai ir šādi iestatījumi:

    - **Politikas nosaukums:** *Starppasūtījums*
    - **Politikas apraksts:** *Starppasūtījumu konsolidācija noteiktām noliktavām*

1. Atstājiet opciju **Konsolidēt ar atvērtu sūtījumu** uz *Nē*.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Konsolidācijas lauki** laukā **Atlikušie lauki** atlasiet rindu, kur lauks **Lauka nosaukums** ir iestatīts uz *Piegādes veids*.
1. Atlasiet **Pievienot** pogu ![Labā bultiņa.](media/forward-button.png) lai pārvietotu lauku uz **Atlasītie lauki** sarakstu.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Dialoglodziņa vaicājumu redaktorā cilnē **Diapazons** atrodiet rindu, kur **Lauka** lauks ir iestatīts uz *Noliktava*, un iestatiet lauku **Kritēriji** uz *61, 63*.
1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu.

### <a name="set-the-order"></a>Iestatīt pasūtījumu

Tagad, kad esat izveidojis visas savas politikas, jums ir jāizveido pasūtījums, kurā tie tiks lietoti. Lai izmantotu piramīdveida pieeju, kur politikas, kam ir visvairāk nosacījumu, tiek novērtētas kā augstākās prioritātes, veiciet šādas darbības.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Iestatiet lauku **Politikas veids** uz *Pārdošanas pasūtījumi*.
1. Atlasiet katru politiku, kas ir uzskaitīta kreisajā kolonnā, un pēc tam izmantojiet Darbību rūts pogas **Pārvietot uz augšu** un **Pārvietot uz leju**, lai sakārtotu politikas šādā secībā:

    1. CustomerMode
    1. Krājuma tips
    1. CustomerOrderNo
    1. Pasūtījuma kopa
    1. Starppasūtījums
    1. Noklusētā vērtība

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Piemēru scenāriji, kā izmantot sūtījumu konsolidācijas politikas

Šie scenāriji parāda, kā varat izmantot jūsu izveidotās sūtījuma konsolidācijas politikas, lasot šo tēmu. Katrs scenārijs jums izskaidros sūtījumu konsolidācijas procesu, kas izmanto sūtījuma konsolidācijas politikas automātiskās vai manuālās nodošanas noliktavā laikā:

- 1. scenārijs: [Konsolidēt sūtījumus, kad tie tiek izlaisti noliktavā, izmantojot automātisko pārdošanas pasūtījumu izlaišanu](../warehousing/consolidate-shipments-automatic.md)
- 2. scenārijs: [konsolidēt sūtījumus, ja sūtījuma konsolidācijas politika tiek ignorēta lapā “Pārvietot uz noliktavu”](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- 3. scenārijs: [Konsolidēt sūtījumus, kravu plānošanas rīkā izmantojot pārvietošanu uz noliktavu](../warehousing/consolidate-shipments-load-planning-workbench.md)
- 4. scenārijs: [Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku](../warehousing/consolidate-shipments-manual-workbench.md)
- 5. scenārijs: [Manuāli konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas lapu](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Papildu resursi

- [Sūtījumu konsolidācijas politikas](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]