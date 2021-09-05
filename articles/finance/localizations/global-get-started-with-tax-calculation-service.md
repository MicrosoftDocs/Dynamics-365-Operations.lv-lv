---
title: Darba sākšana ar nodokļu aprēķinu
description: Šajā tēmā paskaidrots, kā iestatīt Nodokļu aprēķinu.
author: wangchen
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1ddbb22d4f7c6108ca93b415276c53794b5450dd
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394516"
---
# <a name="get-started-with-tax-calculation"></a>Darba sākšana ar nodokļu aprēķinu

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegta informācija par to, kā sākt darbu ar Nodokļu aprēķinu. Vispirms tas palīdz veikt konfigurācijas darbības programmās Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) un Dynamics 365 Finance, un Dynamics 365 Supply Chain Management. Pēc tam tā pārskata kopējo procesu, kas saistīts ar Nodokļu aprēķina iespēju izmantošanu Finance un Supply Chain Management transakcijās.

Iestatījums sastāv no četrām galvenām darbībam:

1. Sistēmā LCS instalējiet nodokļu aprēķina pievienojumprogrammu.
2. Sistēmā RCS iestatiet Nodokļu aprēķina līdzekli. Šis iestatījums nav specifisks juridiskajai personai. To var koplietot visas Finance un Supply Chain Management juridiskās personas.
3. Finance un Supply Chain Management iestatiet Nodokļu aprēķina parametrus pēc juridiskās personas.
4. Finance un Supply Chain Management izveidojiet tādus darījumus kā pārdošanas pasūtījumi un izmantojiet Nodokļu aprēķinu, lai noteiktu un aprēķinātu nodokļus.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms varat pabeigt šajā tēmā norādītās procedūras, katram vides veidam ir jāievieš priekšnosacījumi.

### <a name="for-a-production-environment"></a>Ražošanas videi

Ražošanas videi ir jābūt izpildītiem tālāk minētajiem priekšnosacījumiem.

- Jums jābūt piekļuvei LCS kontam un jābūt izvietotam LCS projektam ar 2. vai augstākas pakāpes vidi, kurā darbojas Dynamics 365 versija 10.0.21 vai jaunāka.
- Jums ir jāizveido RCS vide jūsu organizācijai, un jums ir jābūt piekļuvei savam kontam. Papildinformāciju par to, kā izveidot RCS vidi, skatiet šeit: [Regulatory Configuration Service pārskats](rcs-overview.md).
- Ņemot vērā jūsu uzņēmējdarbības vajadzības, jūsu izvietotās vides Finance vai Supply Chain Management darbvietā **Līdzekļu pārvaldība** jābūt ieslēgtiem tālāk minētajiem līdzekļiem.

    - Nodokļu aprēķins
    - Vairāku PVN reģistrācijas numuru atbalsts
    - Nodokļi pārsūtīšanas pasūtījumā
    - ES pārdošanas saraksta pārsūtīšana, pamatojoties tikai uz nodokļu darījumiem
    - Intrastat pārskatu veidošana pēc vairākiem nodokļu ID
    - ES pārdošanas sarakstu pārskatu veidošana pēc vairākiem nodokļu ID
    - PVN deklarācija pēc vairākiem nodokļu ID

- Izvietotās RCS vides darbvietā **Līdzekļu pārvaldība** jābūt ieslēgtiem tālāk minētajiem līdzekļiem.

    - Globalizācijas līdzekļi

### <a name="for-a-test-environment-public-preview"></a>Testa videi (publiskais priekšskatījums)

Testa videi ir jābūt izpildītiem tālāk minētajiem priekšnosacījumiem.

- Jums jābūt piekļuvei LCS kontam un jābūt izvietotam LCS projektam ar 2. vai augstākas pakāpes vidi, kurā darbojas Dynamics 365 versija 10.0.18 ar KB4616360 vai jaunāka versija.
- Jums ir jāizveido RCS vide jūsu organizācijai, un jums ir jābūt piekļuvei savam kontam. Papildinformāciju par to, kā izveidot RCS vidi, skatiet šeit: [Regulatory Configuration Service pārskats](rcs-overview.md).
- Lai iespējotu testējumu jūsu izvietotā Finance vai Supply Chain Management vidē, jums ir jāsazinās ar uzņēmumu Microsoft, rakstot uz epasta adresi <taxcalc@microsoft.com>.
- Ņemot vērā jūsu uzņēmējdarbības vajadzības, jūsu izvietotās vides Finance vai Supply Chain Management darbvietā **Līdzekļu pārvaldība** jābūt ieslēgtiem tālāk minētajiem līdzekļiem.

    - Nodokļu aprēķins
    - Vairāku PVN reģistrācijas numuru atbalsts
    - Nodokļi pārsūtīšanas pasūtījumā
    - ES pārdošanas saraksta pārsūtīšana, pamatojoties tikai uz nodokļu darījumiem
    - Intrastat pārskatu veidošana pēc vairākiem nodokļu ID
    - ES pārdošanas sarakstu pārskatu veidošana pēc vairākiem nodokļu ID
    - PVN deklarācija pēc vairākiem nodokļu ID

- Izvietotās RCS vides darbvietā **Līdzekļu pārvaldība** jābūt ieslēgtiem tālāk minētajiem līdzekļiem.

    - Globalizācijas līdzekļi

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
8. Atlasiet pareizo nodokļu konfigurācijas versiju, pamatojoties uz savu Finance versiju, un pēc tam atlasiet **Importēt**.

    | Partijas versija | Nodokļu konfigurācija                       | Modeļa kartēšana                   |
    | --------------- | --------------------------------------- | ------------------------------- |
    | 10.0.18         | Nodokļu konfigurācija — Eiropa 30.12.82     |                                 |
    | 10.0.19         | Nodokļu aprēķina konfigurācija 36.38.193 |                                 |
    | 10.0.20         | Nodokļu aprēķina konfigurācija 40.43.208 |                                 |
    | 10.0.21         | Nodokļu aprēķina konfigurācija 40.46.212 | Dataverse Modeļa kartēšana 40.46.9 |

9. Darbvietā **Globalizācijas līdzekļi**, atlasiet **Līdzekļi**, atlasiet elementu **Nodokļu aprēķins** un pēc tam atlasiet **Pievienot**.
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

14. Cilnē **Nodokļu kodi** atlasiet **Pievienot** un ievadiet nodokļa kodu un aprakstu.
15. Atlasiet **Nodokļa komponents**. Nodokļa komponents ir metožu grupa, kas definēta atlasītās nodokļu konfigurācijas iepriekšējā versijā. Pieejami tālāk norādītie nodokļu komponenti.

    - Pēc neto summas
    - Pēc bruto summas
    - Pēc daudzuma
    - Pēc rezerves
    - Nodoklis no nodokļa

16. Atlasiet **Saglabāt**. Vairāk lauku kļūst pieejami, balstoties uz atlasīto nodokļu sastāvdaļu.
17. Lai identificētu nodokļa koda būtību, lietojiet šādas opcijas:

    - Ir atbrīvots
    - Ir Importa nodoklis
    - Ir apgrieztā maksa
    - Neiekļaut pamatsummas aprēķinā

    Importa nodokļu scenārijam iestatiet vienu nodokļa kodu, kam ir pozitīva nodokļu likme, un atzīmējiet to kā **Ir Importa nodoklis**.

    Apgrieztās maksas scenārijam iestatiet divus nodokļu kodus, no kuriem vienam ir pozitīva nodokļu likme, bet otram ir negatīva nodokļu likme, bet tāda pati likmes vērtība. Atzīmējiet negatīvo nodokļa kodu kā **Ir Apgrieztā maksa**. Papildinformāciju par atgrieztās maksas risinājumu programmā Finance skatiet [Apgrieztās maksas mehānisms PVN/GST shēmai](emea-reverse-charge.md).

    Dažiem nodokļu tipiem, kas nav jāiekļauj nodokļu pamatsummas aprēķinā cenu ietverošām transakcijām (piemēram, muitas nodoklim dažās valstīs vai reģionos), atlasiet izvēles rūtiņu **Neiekļaut pamatsummas aprēķinā**. Papildinformāciju par šo parametru skatiet sadaļā [Nodokļu aprēķināšana virs cenas, ja ir iespējots parametrs Cenas ietver nodokļus](global-exclude-from-tax-base-amount-calculation.md).

    Uzturējiet nodokļu likmes un nodokļu summas ierobežojumus šim nodokļu kodam.

18. Atkārtojiet 14.-17. darbību, lai pievienotu visus citus nepieciešamos nodokļu kodus.
19. Cilnē **Nodokļu grupa** atlasiet kolonnu **Nodokļu grupa**, pievienojiet to matricai kā ievades nosacījumu un pēc tam pievienojiet rindas, lai uzturētu nodokļu grupas pamatdatus.

    Tālāk ir minēts piemērs.

    | Nodokļu grupa    | Nodokļu kodi           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. Cilnē **Krājumu nodokļu grupa** atlasiet kolonnu **Krājumu nodokļu grupa**, pievienojiet to matricai kā ievades nosacījumu un pēc tam pievienojiet rindas, lai uzturētu nodokļu grupas pamatdatus.

    Tālāk ir minēts piemērs.

    | Krājumu nodokļu grupa | Nodokļu kodi                                    |
    | -------------- | -------------------------------------------- |
    | Pilns           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Samazināts        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. Cilnē **Nodokļu grupas piemērojamība** atlasiet kolonnas, kas ir nepieciešamas pareizās nodokļu grupas noteikšanai, un pēc tam atlasiet **Pievienot**. Ievadiet vai atlasiet vērtības katrai kolonnai. Lauks **Nodokļu grupa** būs šīs matricas rezultāts. Ja šī cilne netiek konfigurēta, tiks izmantota PVN grupa transakciju rindā.

    Tālāk ir minēts piemērs.

    | Biznesa process | Nosūtītājs | Saņēmējs | Nodokļu grupa    |
    | ---------------- | --------- | ------- | ------------ |
    | Pārdošana            | DEU       | DEU     | DEU_Domestic |
    | Pārdošana            | DEU       | FRA     | DEU_EU       |
    | Pārdošana            | BEL       | BEL     | BEL_Domestic |
    | Pārdošana            | BEL       | FRA     | BEL_EU       |

22. Cilnē **Krājumu nodokļu grupas piemērojamība** atlasiet kolonnas, kas ir nepieciešamas pareizā nodokļu koda noteikšanai, un pēc tam atlasiet **Pievienot**. Ievadiet vai atlasiet vērtības katrai kolonnai. Lauks **Krājumu nodokļu grupa** būs šīs matricas rezultāts. Ja šī cilne netiek konfigurēta, tiks izmantota krājumu PVN grupa transakciju rindā.

    Tālāk ir minēts piemērs.

    | Krājuma kods | Krājumu nodokļu grupa |
    | --------- | -------------- |
    | D0001     | Pilns           |
    | D0003     | Samazināts        |

    Papildinformāciju par to, kā nodokļu aprēķinā tiek noteikti nodokļu kodi, skatiet sadaļā [PVN grupas un krājuma PVN grupas noteikšanas loģika](global-sales-tax-group-determination.md).

23. Iestatiet debitora nodokļu reģistrācijas numuru, kreditora nodokļa reģistrācijas numuru un sarakstu kodu piemērojamību, pamatojoties uz uzņēmējdarbības vajadzībām.
24. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
25. Atlasiet **Mainīt statusu** \> **Pabeigts**. Kad statuss ir mainīts uz **Pabeigts**, versiju vairs nevar rediģēt.
26. Atlasiet **Mainīt statusu** \> **Publicēt**. Šī nodokļu līdzekļa iestatīšanas versija tiks novirzīta uz globālo repozitoriju un būs redzama katrai Finance juridiskajai personai.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Nodokļu aprēķina iestatīšana Dynamics 365

Pēc iestatīšanas pabeigšanas RCS, būs nodrošināta nodokļu līdzekļa publicētā versija. Veiciet šīs darbības, lai Finance sistēmā iestatītu Nodokļu aprēķinu.

Iestatījumus šajā sadaļā veic juridiska persona. Jums tas jākonfigurē katrai juridiskajai personai, kurai programmā Finance vēlaties iespējot Nodokļu aprēķinu.

1. Programmā Finance dodieties uz **Nodoklis** \> **Uzstādīšana** \> **Nodokļu konfigurācija** \> **Nodokļu aprēķina parametri**.
2. Cilnē **Vispārīgi** iestatiet šādus laukus:

    - **Iespējot nodokļu aprēķina pakalpojumu** — atzīmējiet šo izvēles rūtiņu, lai iespējotu nodokļu aprēķinu juridiskajai personai. Ja tas nav iespējots pašreizējai juridiskajai personai, juridiskā persona turpinās izmantot esošo nodokļu programmu, lai noteiktu un aprēķinātu nodokli.
    - **Līdzekļa iestatījumi** — atlasiet publicētu nodokļu līdzekļu iestatījumus un juridiskās personas versiju. Papildinformāciju par publicēta nodokļu līdzekļa iestatīšanu un pabeigšanu skatiet šīs tēmas iepriekšējā sadaļā.
    - **Biznesa process** – atlasiet iespējošanai biznesa procesus.

3. Cilnē **Aprēķins** definējiet juridiskās personas paredzamo noapaļošanas kārtulu. Papildinformāciju par noapaļošanas loģiku skatiet sadaļā [Nodokļu aprēķina noapaļošanas noteikumi](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Cilnē **Kļūdu apstrāde** definējiet juridiskās personas paredzamo kļūdu apstrādes metodi. Ir pieejamas trīs opcijas:

    - Nr.
    - Brīdinājums
    - Kļūda

    Katram rezultāta kodam sadaļā **Detalizēta informācija** var iestatīt kļūdu apstrādes metodi. Alternatīvi, ja daži rezultātu kodi netiek sinhronizēti no nodokļu aprēķina pakalpojuma, noklusējuma metodi varat iestatīt sadaļā **Vispārīgi**.

5. Cilnē **Vairākas PVN reģistrācijas** varat atsevišķi ieslēgt PVN deklarāciju, ES pārdošanas sarakstu un Intrastat, lai strādātu vairāku PVN reģistrāciju scenārijā. Plašāku informāciju par nodokļu pārskatu veidošanu vairākām PVN reģistrācijām skatiet sadaļā [Pārskatu sniegšana vairākām PVN reģistrācijām](emea-reporting-for-multiple-vat-registrations.md).
6. Saglabājiet iestatījumus un atkārtojiet iepriekšējās darbības katrai papildu juridiskajai personai. Kad tiek publicēta jauna versija un vēlaties to lietot, iestatiet lauku **Līdzekļu iestatīšana** lapas **Nodokļu aprēķina parametri** cilnē **Vispārīgi** (skat. 2. darbību).

## <a name="transaction-processing"></a>Darbību apstrāde

Kad esat pabeidzis visas iestatīšanas procedūras, varat izmantot Nodokļu aprēķinu, lai noteiktu un aprēķinātu nodokli programmā Finance. Darījumu apstrādes darbības paliek tās pašas. Finance versijā 10.0.21 tiek atbalstītas šādi darījumi:

- Pārdošanas process

    - Pārdošanas piedāvājums
    - Pārdošanas pasūtījums
    - Apstiprināšana
    - Izdošanas saraksts
    - Pavadzīme
    - Pārdošanas rēķins
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Galvenā maksa
    - Rindas maksa

- Pirkšanas process

    - Pirkuma pasūtījums
    - Apstiprināšana
    - Saņemšanas saraksts
    - Produktu ieejas plūsma
    - Pirkšanas rēķins
    - Galvenā maksa
    - Rindas maksa
    - Kredīta piezīme
    - Atgriešanas pasūtījums
    - Pirkšanas pieprasījums
    - Pirkšanas pieprasījuma rindas maksa
    - Piedāvājuma pieprasījums
    - Piedāvājuma pieprasījuma virsraksta maksa
    - Piedāvājuma pieprasījuma rindas maksa

- Krājumu process

    - Pārvietošanas pasūtījums – nosūtīšana
    - Pārsūtīšanas pasūtījums - saņemšana
