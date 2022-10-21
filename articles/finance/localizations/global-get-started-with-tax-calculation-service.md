---
title: Darba sākšana ar nodokļu aprēķinu
description: Šajā rakstā skaidrots, kā iestatīt nodokļu aprēķinu.
author: EricWangChen
ms.date: 10/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.custom: intro-internal
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 42898823ffc366351c6f58f1fe9b924678ab4b49
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690388"
---
# <a name="get-started-with-tax-calculation"></a>Darba sākšana ar nodokļu aprēķinu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kā sākt darbu ar nodokļu aprēķinu. Šī raksta sadaļās Microsoft Dynamics ir vadītas augsta līmeņa dizaina un konfigurācijas darbības pakalpojumā Lifecycle Services (LCS), regulēšanas konfigurācijas pakalpojums (RCS), Dynamics 365 Finanses un Dynamics 365 Supply Chain Management. 

Uzstādīšana sastāv no trim galvenajiem soļiem.

1. Sistēmā LCS instalējiet nodokļu aprēķina pievienojumprogrammu.
2. Sistēmā RCS iestatiet Nodokļu aprēķina līdzekli. Šis iestatījums nav specifisks juridiskajai personai. To var koplietot visas Finance un Supply Chain Management juridiskās personas.
3. Finance un Supply Chain Management iestatiet Nodokļu aprēķina parametrus pēc juridiskās personas.

## <a name="high-level-design"></a>Augsta līmeņa dizains

### <a name="runtime-design"></a><a name="runtime"></a> Izpildlaika dizains

Šajā ilustrācijā parādīts augsta līmeņa nodokļu aprēķina izpildlaika dizains. Tā kā nodokļu aprēķinu var integrēt vairākās Dynamics 365 programmās, ilustrācija kā piemēru izmanto integrāciju ar Finansēm.

1. Darbība, piemēram, pārdošanas pasūtījums vai pirkšanas pasūtījums, ir izveidota finansēs.
2. Finanses automātiski izmanto PVN grupas un krājumu PVN grupas noklusējuma vērtības.
3. Ja darbībai **ir** atlasīta PVN poga, tiek parādīts nodokļu aprēķins. Finanses pēc tam nosūta lietderīgo slodzi uz nodokļu aprēķina pakalpojumu.
4. Nodokļu aprēķina pakalpojums saskaņo lietderīgo slodzi ar iepriekš definētiem noteikumiem nodokļu funkcijai, lai atrastu precīzāku PVN grupu un krājumu PVN grupu vienlaicīgi.

    - Ja lietderīgo slodzi var saskaņot **ar** matricu Nodokļu grupas piemērojamība, tā ignorē PVN grupas vērtību ar piemēroto nodokļu grupas vērtību piemērojamības noteikumā. Pretējā gadījumā tas turpinās izmantot Finanšu PVN grupas vērtību.
    - Ja lietderīgo slodzi var **saskaņot** ar matricu Krājumu nodokļu grupa piemērojamība, piemērojamības kārtulā tiek ignorēta krājumu PVN grupas vērtība ar atbilstošo krājumu nodokļu grupas vērtību. Pretējā gadījumā tas turpinās izmantot krājumu PVN grupas vērtību no Finanšu.

5. Nodokļu aprēķinu pakalpojums nosaka gala nodokļu kodus, izmantojot PVN grupas un krājumu PVN grupas krustpunktu.
6. Nodokļu aprēķināšanas pakalpojums aprēķina nodokli, balstoties uz nodokļu beigu kodiem, ko tas noteicis.
7. Nodokļu aprēķināšanas pakalpojums atgriež nodokļu aprēķina rezultātu finansēm.

![Nodokļu aprēķina izpildlaika dizains.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Augsta līmeņa konfigurācija

Šajās darbībās sniegts augsta līmeņa pārskats par konfigurācijas procesu nodokļu aprēķināšanas pakalpojumam.

1. LCS instalē nodokļu **aprēķina** pievienojumprogrammu savā LCS projektā.
2. RCS izveidojiet nodokļu **aprēķina līdzekli**.
3. RCS iestatiet Nodokļu aprēķina **līdzekli**:

    1. Atlasiet nodokļu konfigurācijas versiju.
    2. Veidojiet nodokļu kodus.
    3. Izveidojiet PVN grupu.
    4. Izveidojiet krājumu PVN grupu.
    5. Nav obligāti: izveidot nodokļu grupas piemērojamību, ja vēlaties ignorēt noklusēto PVN grupu, kas tiek ievadīta no debitora vai kreditora pamatdatiem.
    6. Nav obligāti: izveidot krājumu grupas piemērojamību, ja vēlaties ignorēt noklusēto krājumu PVN grupu, kas ievadīta no krājumu pamatdatiem.

4. RCS izpildiet un publicējiet nodokļu **aprēķina** līdzekli.
5. Finanšu sadaļā atlasiet publicēto nodokļu **aprēķina** līdzekli.

Kad šīs darbības pabeigtas, šie iestatījumi no RCS tiek automātiski sinhronizēti finansēs.

- PVN kodi
- PVN grupas
- Krājumu PVN grupas

Pārējās šī raksta sadaļas sniedz detalizētāku konfigurācijas darbību aprakstu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms varat izpildīt atlikušās šajā rakstā norādītās procedūras, ir jāizpilda šādi priekšnosacījumi:<!--TO HERE-->

- Jums jābūt piekļuvei LCS kontam un jābūt izvietotam LCS projektam ar 2. vai augstākas pakāpes vidi, kurā darbojas Dynamics 365 versija 10.0.21 vai jaunāka.
- Jums ir jāizveido RCS vide jūsu organizācijai, un jums ir jābūt piekļuvei savam kontam. Papildinformāciju par to, kā izveidot RCS vidi, skatiet šeit: [Regulatory Configuration Service pārskats](rcs-overview.md).
- Ņemot vērā jūsu uzņēmējdarbības vajadzības, jūsu izvietotās vides Finance vai Supply Chain Management darbvietā **Līdzekļu pārvaldība** jābūt ieslēgtiem tālāk minētajiem līdzekļiem.

    - Nodokļu aprēķināšanas pakalpojums
    - Vairāku PVN reģistrācijas numuru atbalsts
    - Nodokļi pārsūtīšanas pasūtījumā

- Izvietotās RCS vides darbvietā **Līdzekļu pārvaldība** jābūt ieslēgtiem tālāk minētajiem līdzekļiem.

    - Globalizācijas līdzekļi

- Šīs lomas ir jāpiešķir atbilstoši lietotājiem jūsu RCS vidē:

    - Elektroniskā pārskata izstrādātājs
    - Globalizācijas līdzekļu izstrādātājs
    - Nodokļu programmas izstrādātājs
    - Konsultants saistībā ar nodokļu programmas darbību
    - Nodokļu pakalpojuma izstrādātājs

## <a name="set-up-tax-calculation-in-lcs"></a>Iestatīt Nodokļu aprēķinu sistēmā LCS

1. Pierakstīšanās programmā [LCS](https://lcs.dynamics.com)
2. Pabeidziet Microsoft Power Platform integrācijas iestatīšanu. Papildinformāciju skatiet sadaļā [Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Atlasiet vienu no izvietotām vidēm, un pēc tam atlasiet **Instalēt jaunu pievienojumprogrammu**.
4. Atlasiet **Nodokļu aprēķins**.
5. Izlasiet un piekrītiet noteikumiem un nosacījumiem un pēc tam atlasiet **Instalēt**.

## <a name="set-up-tax-calculation-in-rcs"></a>Iestatīt Nodokļu aprēķinu sistēmā RCS

Šīs sadaļas darbības nav saistītas ar noteiktu juridisko personu. Jums ir jāveic šī procedūra tikai vienu reizi, un jūs variet pabeigt to jebkurā juridiskajā persona programmā RCS.

1. Pierakstieties [RCS](https://marketing.configure.global.dynamics.com/).
2. Darbvietā **Elektronisko pārskatu veidošana** pievienojiet jaunu konfigurācijas nodrošinātāju. Kā nodrošinātāja nosaukumu izmantojiet uzņēmuma nosaukumu. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Atlasiet tikko izveidoto konfigurācijas nodrošinātāju un pēc tam atlasiet **Iestatīt aktīvu**.
4. Atlasiet **Microsoft** konfigurācijas nodrošinātāju, un tad atlasiet **Repozitoriji**.
5. Laukā **Tips** atlasiet **Globāls**.
6. Atlasiet **Atvērt**.
7. Dodieties uz **Nodokļu datu modelis**, izvērsiet failu koku un pēc tam atlasiet **Nodokļu konfigurācija**.
8. Atlasiet pareizu nodokļu [konfigurācijas versiju, pamatojoties](global-tax-calcuation-service-overview.md#versions) uz finanšu versiju, un pēc tam atlasiet **Importēt**.
9. Darbvietā **Globalizācijas līdzekļi**, atlasiet **Līdzekļi**, atlasiet elementu **Nodokļu aprēķins** un pēc tam atlasiet **Pievienot**.

    > [!NOTE]
    > Versijā 10.0.26 **vai jaunākā versijā varat importēt demonstrācijas funkciju JURIDISKĀm personām PARA**! Plašāku informāciju skatiet līdzekļa [demonstrācijas datu importēšana](tax-calculation-import-export-feature.md).

10. Atlasiet vienu no šiem līdzekļu tipiem:

    - **Jauns līdzeklis** – izveidojiet līdzekļa iestatījumu, kam ir tukšs saturs.
    - **Balstīts uz esošo līdzekli** – izveidojiet līdzekli no esoša līdzekļa un kopējiet saturu no esoša līdzekļa iestatījuma.

11. Ievadiet jaunā līdzekļa nosaukumu un aprakstu un pēc tam atlasiet **Izveidot līdzekli**.

    Pēc līdzekļa izveides automātiski tiek izveidota tā melnraksta versija. Varat atlasīt **Iegūt šo versiju**, lai atkārtoti bāzētu melnraksta versiju jebkurā pabeigtā versijā.

12. Atlasiet līdzekļa melnraksta versiju un pēc tam atlasiet **Rediģēt**. Ir aizpildīta lapa **Nodokļu aprēķina iestatījums**.
13. Atlasiet **Konfigurācijas versija**. 8. darbībā jums vajadzētu redzēt importēto konfigurācijas versiju.

    Microsoft nodrošina nodokļu aprēķina noklusējuma nodokļu konfigurāciju. Šī konfigurācija sedz lielāko daļu nodokļu aprēķina darbību prasību. Tas tiks atjaunināts, balstoties uz tirgus atsauksmēm. Ja konfigurācija jāpaplašina, lai tā atbilstu noteiktām prasībām, skatiet sadaļu [Kā veidot nodokļu pakalpojumu paplašinājumu](./tax-service-add-data-fields-tax-integration-by-extension.md), lai saņemtu informāciju par to, kā ģenerēt un atlasīt savu nodokļu konfigurāciju.

14. Pēc **Konfigurācijas versija** izvēles, tiek parādītas vairākas papildu cilnes. Lai pabeigtu obligāto cilnes iestatīšanu, izpildiet šeit norādīto rīkojumu.

    **Obligātā iestatīšana**

    - **Nodokļu kodi** — uztur pamatdatus nodokļu kodiem. Visi šajā cilnē izveidotie nodokļu kodi automātiski tiek sinhronizēti ar Finance, ja iespējojat pašreizējo versiju.
    - **Nodokļu grupa** — definē nodokļu grupas pamatdatus un nodokļu kodus grupā.
    - **Krājuma nodokļu grupa** — definē krājuma nodokļu grupas pamatdatus un nodokļu kodus grupā.

    **Izvēles iestatīšana**

    - **Nodokļu grupas piemērojamība** — definē matricu, kas nosaka nodokļu grupu. Ja šajā matricā piemērojamības noteikumi neatbilst Dynamics 365 ar nodokli apliekamajam dokumentam, nodokļu aprēķins izmanto ar nodokli apliekamā dokumenta rindas noklusējuma vērtību.
    - **Krājuma nodokļu grupas piemērojamība** — definē matricu, kas nosaka krājuma nodokļu grupu. Ja šajā matricā piemērojamības noteikumi neatbilst Dynamics 365 ar nodokli apliekamajam dokumentam, nodokļu aprēķins izmanto ar nodokli apliekamā dokumenta rindas noklusējuma vērtību.
    - **Debitora nodokļu reģistrācijas numura piemērojamība** — ja vienam debitoram ir vairāki nodokļa reģistrācijas numuri, nodokļu aprēķins var automātiski noteikt pareizo nodokļa reģistrācijas numuru. Šīs cilnes matricā definējiet nosacījumus, kurus jāizmanto, lai veiktu noteikšanu. Pretējā gadījumā Finance un Supply Chain Management turpinās izmantot ar nodokli apliekamo dokumentu noklusējuma nodokļa reģistrācijas numuru pārdošanas darbībām.
    - **Kreditora nodokļu reģistrācijas numura piemērojamība** — ja vienam kreditoram ir vairāki nodokļa reģistrācijas numuri, nodokļu aprēķins var automātiski noteikt pareizo nodokļa reģistrācijas numuru. Šīs cilnes matricā definējiet nosacījumus, kurus jāizmanto, lai veiktu noteikšanu. Pretējā gadījumā Finance un Supply Chain Management turpinās izmantot ar nodokli apliekamo dokumentu noklusējuma nodokļa reģistrācijas numuru pirkšanas darbībām.
    - **Saraksta koda piemērojamība** — automātiski nosaka lauka **Saraksta kods** vērtību, izmantojot elastīgākus un konfigurējamus noteikumus. Šīs cilnes matricā definējiet nosacījumus, kurus jāizmanto, lai veiktu noteikšanu. Pretējā gadījumā Finance un Supply Chain Management turpinās izmantot ar nodokli apliekamo dokumentu noklusējuma kodu.

15. Cilnē **Nodokļu kodi** atlasiet **Pievienot** un ievadiet nodokļa kodu un aprakstu.
16. Atlasiet **Nodokļa komponents**. Nodokļa komponents ir metožu grupa, kas definēta atlasītās nodokļu konfigurācijas iepriekšējā versijā. Pieejami tālāk norādītie nodokļu komponenti.

    - Pēc neto summas
    - Pēc bruto summas
    - Pēc daudzuma
    - Pēc rezerves
    - Nodoklis no nodokļa

17. Atlasiet **Saglabāt**. Vairāk lauku kļūst pieejami, balstoties uz atlasīto nodokļu sastāvdaļu.
18. Lai identificētu nodokļa koda būtību, lietojiet šādas opcijas:

    - Ir atbrīvots
    - Ir Importa nodoklis
    - Ir apgrieztā maksa
    - Neiekļaut pamatsummas aprēķinā

    Importa nodokļu scenārijam iestatiet vienu nodokļa kodu, kam ir pozitīva nodokļu likme, un atzīmējiet to kā **Ir Importa nodoklis**.

    Apgrieztās maksas scenārijam iestatiet divus nodokļu kodus, no kuriem vienam ir pozitīva nodokļu likme, bet otram ir negatīva nodokļu likme, bet tāda pati likmes vērtība. Atzīmējiet negatīvo nodokļa kodu kā **Ir Apgrieztā maksa**. Papildinformāciju par atgrieztās maksas risinājumu programmā Finance skatiet [Apgrieztās maksas mehānisms PVN/GST shēmai](emea-reverse-charge.md).

    Dažiem nodokļu tipiem, kas nav jāiekļauj nodokļu pamatsummas aprēķinā cenu ietverošām transakcijām (piemēram, muitas nodoklim dažās valstīs vai reģionos), atlasiet izvēles rūtiņu **Neiekļaut pamatsummas aprēķinā**. Papildinformāciju par šo parametru skatiet sadaļā [Nodokļu aprēķināšana virs cenas, ja ir iespējots parametrs Cenas ietver nodokļus](global-exclude-from-tax-base-amount-calculation.md).

    Uzturējiet nodokļu likmes un nodokļu summas ierobežojumus šim nodokļu kodam.

19. Atkārtojiet 15.-18. darbību, lai pievienotu visus citus nepieciešamos nodokļu kodus.
20. Cilnē **Nodokļu grupa** atlasiet kolonnu **Nodokļu grupa**, pievienojiet to matricai kā ievades nosacījumu un pēc tam pievienojiet rindas, lai uzturētu nodokļu grupas pamatdatus.

    Tālāk ir minēts piemērs.

    | Nodokļu grupa    | Nodokļu kodi           |
    | ------------ | ------------------- |
    | DEU_Dom | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Dom | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

21. Cilnē **Krājumu nodokļu grupa** atlasiet kolonnu **Krājumu nodokļu grupa**, pievienojiet to matricai kā ievades nosacījumu un pēc tam pievienojiet rindas, lai uzturētu nodokļu grupas pamatdatus.

    Tālāk ir minēts piemērs.

    | Krājumu nodokļu grupa | Nodokļu kodi                                    |
    | -------------- | -------------------------------------------- |
    | Pilns           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Samazināts        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

22. Cilnē **Nodokļu grupas piemērojamība** atlasiet kolonnas, kas ir nepieciešamas pareizās nodokļu grupas noteikšanai, un pēc tam atlasiet **Pievienot**. Ievadiet vai atlasiet vērtības katrai kolonnai. Lauks **Nodokļu grupa** būs šīs matricas rezultāts. Ja šī cilne netiek konfigurēta, tiks izmantota PVN grupa transakciju rindā.

    Tālāk ir minēts piemērs.

    | Biznesa process | Nosūtītājs | Saņēmējs | Nodokļu grupa    |
    | ---------------- | --------- | ------- | ------------ |
    | Pārdošana            | DEU       | DEU     | DEU_Dom |
    | Pārdošana            | DEU       | FRA     | DEU_EU       |
    | Pārdošana            | BEL       | BEL     | BEL_Dom |
    | Pārdošana            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Ja nodokļu dokumenta rindās noklusētā PVN grupa ir pareiza, atstājiet šo matricu tukšu. Papildinformāciju skatiet šī raksta [izpildlaika](#runtime) dizaina sadaļā.

23. Cilnē **Krājumu nodokļu grupas piemērojamība** atlasiet kolonnas, kas ir nepieciešamas pareizā nodokļu koda noteikšanai, un pēc tam atlasiet **Pievienot**. Ievadiet vai atlasiet vērtības katrai kolonnai. Lauks **Krājumu nodokļu grupa** būs šīs matricas rezultāts. Ja šī cilne netiek konfigurēta, tiks izmantota krājumu PVN grupa transakciju rindā.

    Tālāk ir minēts piemērs.

    | Krājuma kods | Krājumu nodokļu grupa |
    | --------- | -------------- |
    | D0001     | Pilns           |
    | D0003     | Samazināts        |

    > [!NOTE]
    > Ja noklusētā krājumu PVN grupa apliekamā dokumenta rindās ir pareiza, atstājiet šo matricu tukšu. Papildinformāciju skatiet šī raksta [izpildlaika](#runtime) dizaina sadaļā.

    Papildinformāciju par to, kā nodokļu aprēķinā tiek noteikti nodokļu kodi, skatiet sadaļā [PVN grupas un krājuma PVN grupas noteikšanas loģika](global-sales-tax-group-determination.md).

24. Iestatiet debitora nodokļu reģistrācijas numuru, kreditora nodokļa reģistrācijas numuru un sarakstu kodu piemērojamību, pamatojoties uz uzņēmējdarbības vajadzībām.
25. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
26. Atlasiet **Mainīt statusu** \> **Pabeigts**. Kad statuss ir mainīts uz **Pabeigts**, versiju vairs nevar rediģēt.
27. Atlasiet **Mainīt statusu** \> **Publicēt**. Šī nodokļu līdzekļa iestatīšanas versija tiks novirzīta uz globālo repozitoriju un būs redzama katrai Finance juridiskajai personai.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Nodokļu aprēķina iestatīšana Dynamics 365

Pēc iestatīšanas pabeigšanas RCS, būs nodrošināta nodokļu līdzekļa publicētā versija. Veiciet šīs darbības, lai Finance sistēmā iestatītu Nodokļu aprēķinu.

Iestatījumus šajā sadaļā veic juridiska persona. Jums tas jākonfigurē katrai juridiskajai personai, kurai programmā Finance vēlaties iespējot Nodokļu aprēķinu.

1. Programmā Finance dodieties uz **Nodoklis** \> **Uzstādīšana** \> **Nodokļu konfigurācija** \> **Nodokļu aprēķina parametri**.
2. Cilnē **Vispārīgi** iestatiet šādus laukus:

    - **Iespējot nodokļu aprēķina pakalpojumu** — atzīmējiet šo izvēles rūtiņu, lai iespējotu nodokļu aprēķinu juridiskajai personai. Ja tas nav iespējots pašreizējai juridiskajai personai, juridiskā persona turpinās izmantot esošo nodokļu programmu, lai noteiktu un aprēķinātu nodokli.
    - **Līdzekļa iestatījumi** — atlasiet publicētu nodokļu līdzekļu iestatījumus un juridiskās personas versiju. Plašāku informāciju par to, kā iestatīt un izpildīt publicētā nodokļa funkciju, skatiet šī raksta iepriekšējā sadaļā.
    - **Biznesa process** – atlasiet iespējošanai biznesa procesus.

3. Cilnē **Aprēķins** definējiet juridiskās personas paredzamo noapaļošanas kārtulu. Papildinformāciju par noapaļošanas loģiku skatiet sadaļā [Nodokļu aprēķina noapaļošanas noteikumi](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Cilnē **Kļūdu apstrāde** definējiet juridiskās personas paredzamo kļūdu apstrādes metodi. Ir pieejamas trīs opcijas:

    - Nē
    - Brīdinājums
    - Kļūda

    Katram rezultāta kodam sadaļā **Detalizēta informācija** var iestatīt kļūdu apstrādes metodi. Alternatīvi, ja daži rezultātu kodi netiek sinhronizēti no nodokļu aprēķina pakalpojuma, noklusējuma metodi varat iestatīt sadaļā **Vispārīgi**.

5. Cilnē **Vairākas PVN reģistrācijas** varat atsevišķi ieslēgt PVN deklarāciju, ES pārdošanas sarakstu un Intrastat, lai strādātu vairāku PVN reģistrāciju scenārijā. Plašāku informāciju par nodokļu pārskatu veidošanu vairākām PVN reģistrācijām skatiet sadaļā [Pārskatu sniegšana vairākām PVN reģistrācijām](emea-reporting-for-multiple-vat-registrations.md).
6. Saglabājiet iestatījumus un atkārtojiet iepriekšējās darbības katrai papildu juridiskajai personai. Kad tiek publicēta jauna versija un vēlaties to lietot, iestatiet lauku **Līdzekļu iestatīšana** lapas **Nodokļu aprēķina parametri** cilnē **Vispārīgi** (skat. 2. darbību).
