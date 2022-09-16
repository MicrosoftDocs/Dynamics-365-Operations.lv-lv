---
title: Sūtījumu konsolidācijas politiku konfigurēšana
description: Šajā rakstā ir izskaidrots, kā iestatīt noklusējuma un pielāgotas piegādes konsolidācijas politikas.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427987"
---
# <a name="configure-shipment-consolidation-policies"></a>Sūtījumu konsolidācijas politiku konfigurēšana

[!include [banner](../includes/banner.md)]

Sūtījumu konsolidācijas process, kas izmanto sūtījuma konsolidācijas politikas, atļauj sūtījuma konsolidāciju automātiskās un manuālās nodošanas noliktavā laikā. Pēc šī līdzekļa ieslēgšanas jums ir jākonfigurē sākotnējās politikas. Ja neviena politika netiek konfigurēta, katra pārdošanas rinda ģenerēs atsevišķu sūtījumu, kurai ir viena noslodzes rinda.

Šajā rakstā rādītie scenāriji parāda, kā iestatīt noklusējuma un pielāgotas piegādes konsolidācijas politikas.

> [!WARNING]
> Ja jaunināt Microsoft Dynamics 365 Supply Chain Management sistēmu, kurā izmantojāt mantojuma sūtījuma konsolidācijas līdzekli, konsolidācija var pārtraukt darboties tik ilgi, cik gaidīts, izņemot gadījumu, ja izpildāt šeit norādīto izziņu.
>
> Piegādes ķēdes pārvaldības *instalācijās*, kur piegādes konsolidācijas politikas līdzeklis ir izslēgts, jūs iespējojat piegādes konsolidāciju, **izmantojot "Konsolidēt** sūtījumu, kad tiek izlaists uz noliktavu" iestatījumu katrai atsevišķai noliktavai. Šī funkcija ir obligāta versijā 10.0.29. Ja ir ieslēgta, iestatījums Konsolidēt sūtījumu, kad tiek izlaists uz noliktavu, **tiek** paslēpts iestatījums, *un* funkcionalitāte tiek aizstāta ar šajā rakstā aprakstītajām piegādes konsolidācijas politikām. Katra politika izveido konsolidācijas noteikumus un iekļauj vaicājumu, lai kontrolētu, uz kurieni attiecas šī politika. Kad pirmo reizi ieslēdzat šo līdzekli, piegādes konsolidācijas politiku lapā netiks definētas **piegādes konsolidācijas** politikas. Ja politikas nav definētas, sistēma izmanto mantojuma uzvedību. Tāpēc katra esošā noliktava turpina ievērot savus **Konsolidēt sūtījumus, kad tiek izlaista noliktava**, pat ja šis iestatījums tagad ir slēpts. Tomēr pēc tam, kad ir izveidota vismaz viena piegādes konsolidācijas politika, **Konsolidēt** sūtījumu, kad tiek veikta nosūtīšana uz noliktavu, iestatījumiem vairs nav nekādas ietekmes, un konsolidācijas funkcionalitāti pilnībā kontrolē politika.
>
> Pēc tam, kad būsiet nosakiet vismaz vienu nosūtīšanas piegādes konsolidācijas politiku, sistēma pārbauda konsolidācijas politikas katru reizi, kad pasūtījums tiek izdots noliktavai. Sistēma apstrādā politikas, izmantojot rangu, kas tiek definēts katras politikas politikas secības **vērtībā**. Tas attiecas uz pirmo ierobežojumu, kur vaicājums atbilst jaunajam pasūtījumam. Ja pasūtījumā nav neviena vaicājuma, katra pasūtījuma rinda ģenerē atsevišķu sūtījumu, kam ir viena noslodzes rinda. Tāpēc regresa gadījumā ieteicams izveidot noklusējuma politiku, kas attiecas uz visām noliktavām un grupām pēc pasūtījuma numura. Piešķiriet šai regresa politikai augstāko **politikas secības** vērtību tā, lai tā tiktu apstrādāta pēdējā.
>
> Lai pavairotu mantojuma uzvedību, ir jāizveido politika, kas negrupē pēc pasūtījuma numura un kam ir vaicājuma kritēriji, kas ietver visas attiecīgās noliktavas.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Ieslēgt Sūtījumu konsolidācijas politiku līdzekli

Lai izmantotu piegādes *konsolidācijas* politikas līdzekli, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja jūs palaižat versiju, kas vecāka par 10.0.29, tad administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot nosūtīšanas *konsolidācijas*[politikas līdzekli līdzekļu pārvaldības darbvietā.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a> Iestatiet sākotnējās konsolidācijas politikas

Ja strādājat *ar* jaunu sistēmu vai sistēmu, kur pirmo reizi esat tikko ieslēdzis piegādes konsolidācijas politiku līdzekli, veiciet šos soļus, lai iestatītu sākotnējās piegādes konsolidācijas politikas.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Pārvietot uz noliktavu \> Sūtījuma konsolidācijas politikas**.
1. Darbību rūtī atlasiet **Izveidot noklusēto iestatījumus**, lai izveidotu šādas politikas:

    - Politika, kuras nosaukums ir *Noklusējums* pārdošanas *pasūtījumu politikas* tipam.
    - Politika, kuras nosaukums ir *Noklusējums*.*·*
    - Politika, kuras nosaukums ir *CrossOrder pārsūtīšanas* izejas *plūsmas* politikas tipam. (Šis politika tiek izveidots tikai tad, ja jums ir vismaz viena noliktava, kur mantojuma **Konsolidēt sūtījumu, kad tika aktivizēts pārsūtīšanas uz** noliktavu iestatījums.)
    - Politika, kuras nosaukums ir *CrossOrder* pārdošanas *pasūtījumu politikas* tipam. (Šis politika tiek izveidots tikai tad, ja jums ir vismaz viena noliktava, kur mantojuma **Konsolidēt sūtījumu, kad tika aktivizēts pārsūtīšanas uz** noliktavu iestatījums.)

    > [!NOTE]
    > - Abas *CrossOrder politikas* apsver tādu pašu lauku kopu kā agrākā loģika. Tomēr tās ņem vērā arī pasūtījuma numura lauku. (Šis lauks tiek izmantots, lai konsolidētu rindas sūtījumos, pamatojoties uz tādiem faktoriem kā noliktava, piegādes transportēšanas veidu un adrese.)
    > - Abas *noklusējuma* politikas apsver vienu lauku kopu kā agrāko loģiku. Tomēr tās ņem vērā arī pasūtījuma numura lauku. (Šis lauks tiek izmantots, lai nkonsolidētu rindas sūtījumos, pamatojoties uz tādiem faktoriem kā pasūtījuma numurs, noliktava, piegādes transportēšanas veids un adrese.)

1. Ja sistēma pārdošanas pasūtījumu politikas *tipam ģenerēja* *Starpuzņēmumu* politiku, atlasiet to un pēc tam darbību rūtī atlasiet Vaicājumu **Rediģēt**. Vaicājumu redaktorā var skatīt, kurām noliktavām iepriekš iespējots iestatījums **Konsolidēt** sūtījumu, kad tiek veikta pārsūtīšana uz noliktavu. Tāpēc šī politika atjauno iepriekšējos iestatījumus šīm noliktavām.
1. Pielāgojiet jaunās noklusējuma politikas, kā nepieciešams, pievienojot vai noņemot laukus un/vai rediģējot vaicājumus. Varat arī pievienot tik daudz jaunu politiku, cik nepieciešams. Piemērus, kas parāda, kā pielāgot un konfigurēt savas politikas, skatiet tālāk šī raksta piemēra scenārijā.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Scenārijs: konfigurēt pielāgotas piegādes konsolidācijas politikas

Šajā scenārijā sniegts piemērs, kas parāda, kā iestatīt pielāgotas piegādes konsolidācijas politikas un pēc tam pārbaudīt tās, izmantojot demonstrācijas datus. Pielāgotās politikas var atbalstīt kompleksas biznesa prasības, kur sūtījumu konsolidācija ir atkarīga no vairākiem nosacījumiem. Katrai šīs jomas politikai vēlāk šajā scenārijā ir ietverts īss biznesa scenārija apraksts. Šīs piemēru politikas ir jāiestata secībā, kas nodrošina vaicājumu piramīdveida novērtējumu. (Citiem vārdiem, politikas, kurām ir visvairāk nosacījumu, ir jānovērtē kā augstākā prioritāte.)

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šis scenārijs atsaucas uz vērtībām un ierakstiem, kas iekļauti standarta [demonstrācijas](../../fin-ops-core/fin-ops/get-started/demo-data.md) datos, kas tiek nodrošināti Piegādes ķēžu pārvaldībai. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu *USMF*, pirms sākat darbu.

### <a name="prepare-master-data-for-this-scenario"></a>Sagatavot pamatdatus šim scenārijam

Pirms varat iziet cauri šajā scenārijā izmantotajiem nosacījumiem, jāsagatavo pamatdati, kas nepieciešami filtrēšanas darbībām, kā aprakstīts tālāk aprakstītajā apakšsadaļās. (Šie priekšnosacījumi attiecas arī uz scenārijiem, kas ir uzskaitīti [Piemērs scenārijiem par to, kā izmantot piegādes konsolidācijas politiku](#example-scenarios) sadaļu.)

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
1. Aizveriet lapu un pēc tam atkārtojiet 4. un 5. darbību debitoram ar konta numuru *US-004*.

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

Parasti šo biznesa gadījumu var aplūkot, izmantojot noklusējuma politiku, ko izveidojāt Sākotnējās [konsolidācijas politikas iestatīšana](#initial-policies). Tomēr varat arī manuāli izveidot līdzīgas politikas, veicot šādas darbības.

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

Turpmākie scenāriji parāda, kā var izmantot piegādes konsolidācijas politikas, ko izveidojāt, lasot šo rakstu. Katrs scenārijs jums izskaidros sūtījumu konsolidācijas procesu, kas izmanto sūtījuma konsolidācijas politikas automātiskās vai manuālās nodošanas noliktavā laikā:

- 1. scenārijs: [Konsolidēt sūtījumus, kad tie tiek izlaisti noliktavā, izmantojot automātisko pārdošanas pasūtījumu izlaišanu](../warehousing/consolidate-shipments-automatic.md)
- 2. scenārijs: [konsolidēt sūtījumus, ja sūtījuma konsolidācijas politika tiek ignorēta lapā “Pārvietot uz noliktavu”](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- 3. scenārijs: [Konsolidēt sūtījumus, kravu plānošanas rīkā izmantojot pārvietošanu uz noliktavu](../warehousing/consolidate-shipments-load-planning-workbench.md)
- 4. scenārijs: [Konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas rīku](../warehousing/consolidate-shipments-manual-workbench.md)
- 5. scenārijs: [Manuāli konsolidēt sūtījumus, izmantojot sūtījumu konsolidācijas lapu](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Papildu resursi

- [Kravu konsolidācijas politikas pārskats](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
