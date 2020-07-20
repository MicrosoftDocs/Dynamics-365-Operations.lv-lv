---
title: Apstiprināt un pārsūtīt
description: Šajā tēmā ir paskaidrots, kā izmantot līdzekli apstiprināt un pārsūtīt, kas ļauj lietotājiem nosūtīt kravas no noliktavas, pirms tiek aizpildīts viss ar šīm kravām saistītais darbs.
author: mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 488eed23972022f9437e62a462ae5f70d6833a67
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530562"
---
# <a name="confirm-and-transfer"></a>Apstiprināt un pārsūtīt

[!include [banner](../includes/banner.md)]

Līdzeklis *Apstiprināt un pārsūtīt* ļauj lietotājiem nosūtīt kravas no noliktavas, pirms tiek aizpildīts viss ar šīm kravām saistītais darbs. Saņemot sūtījumu, kas ietver kravas rindas, kas netika pilnībā izdotas, apstiprinājuma lietotājam tiek pieprasīts sadalīt atlikušos daudzumus jaunā kravā vai atcelt nepabeigtos daudzumus.

Sistēmas, kas iestatītas atļaut kravas sadalīšanas atbalsta scenārijus, kur plānotās un daļēji ielādētās kravas ir jāpielāgo, sakarā ar jauniem vai mainīgiem apstākļiem.

Klients ietver loģiku, kas ļauj slēgt daļēji ielādētu kravu un apstiprināt to kā nosūtītu. Visi atlikušie sūtījumi un kravas rindas (ieskaitot pilnīgus vai daļējus rindu daudzumus) tiek nodotas jaunajai kravai un sūtījumiem, ja tas ir nepieciešams un to atļauj iestatījumi. Jauni sūtījumi un kravas tiek automātiski izveidoti, pamatojoties uz sākotnējiem piegādes un kravas izveides kritērijiem, un to galvenie atribūti paliek nemainīgi. Pastāv arī opcija automātiski atcelt atlikušos daudzumus, ja darba pasūtījums vēl nav izveidots un lietotājs uzskata šo atcelšanu par nepieciešamu.

Šī funkcionalitāte atbalsta scenārijus, kuros pilnā krava neietilpst vienā kravas automašīnā vai kad daļai kravas ir jāiziet no noliktavas, pirms pārējā krava ir gatava nosūtīšanai. Šajos scenārijos atlikušās preces var pārsūtīt uz jaunu kravu un līdz ar to uz jaunu kravas automašīnu. Tā kā šo funkciju var izmantot ar kravām, kas citādi ir paredzētas pilna kravas sūtījuma piegādei, tas nodrošina papildu elastību, lai pārvadājumu vadītājs varētu risināt nestandarta vai neparedzētus scenārijus.

Kad krava ir sadalīta, līdzeklis *Apstiprināt un pārsūtīt* veic šādas darbības:

- Jaunas kravas un sūtījumi tiek veidoti, kad ir nepieciešams. Katrai kravai vai sūtījumam būs vairums tādu pašu atribūtu kā oriģinālajai kravai vai sūtījumam. Izņēmums ir kravas statuss, kas tiks pārrēķināts, pamatojoties uz darba statusu.
- Lietotājs tiek informēts par jaunas kravas izveidi. Lietotājam tiek paziņots arī jaunās kravas ID.
- Kravas rindas, darba virsraksti un darba rindas, kas tika sadalītas, tiek atjauninātas ar jauno kravas un sūtījuma informāciju.
- Ja tiek sadalīts viss sūtījums, tas tiek uzturēts un tiek atjauninātas tikai kravas atsauces. Ja sūtījums ir jāsadala, tiek izveidots jauns sūtījums.

Atceļot atlikušos daudzumus, visi kravas rindas daudzumi, kas nav izdoti un kam nav ar tām saistīts neatcelts darbs, tiek noņemti no kravas. Ja kāds darbs ir procesā, lietotājs var kravu tikai sadalīt. Atlikušos daudzumus nevar atcelt.

Ir iespējams sadalīt tikai tās kravas, kas atbilst šādiem kritērijiem:

- Vienai vai vairākām kravas rindām ir izdotais daudzums.
- Kravas statuss ir mazāks nekā tika ielādēts.
- Nav kravas rindas datu. (Šie dati tiek veidoti, izmantojot noliktavas vienības konsolidāciju sagatavošanas posma atrašanās vietai, un līdzeklis *Apstiprināt un pārsūtīt* neatbalsta noliktavas vienības konsolidēšanu.)
- Pašlaik iepakošanas vietā nav paredzēts iepakot nevienu krājumu. (Līdzeklis *Apstiprināt un pārsūtīt* neatbalsta krājumus, kas ir izdoti iepakošanas stacijā, bet vēl nav iepakoti.)

> [!NOTE]
> Šī funkcionalitāte atšķiras no transportēšanas kravas funkcionalitātes, kas jāizmanto noliktavās, kurās pirms izdošanas nekad nevar plānot un izveidot kravas, bet tā vietā tiek ielādētas pieejamās transportēšanas vietas pēc izdošanas pabeigšanas.
>
> Lietojiet līdzekli *Apstiprināt un pārsūtīt* gadījumos, kad kravas parasti tiek plānotas un izveidotas pirms laika, radot izņēmumus, kad krava neietilps pieejamajā transportā (piemēram, kravas automašīnā).

## <a name="turn-on-confirm-and-transfer"></a>Ieslēgt apstiprināšanu un pārsūtīšanu

Lai varētu izmantot līdzekli *Apstiprināt un pārsūtīt*, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas vadība*
- **Līdzekļa nosaukums:** *Apstiprināt un pārsūtīt*

## <a name="set-up-confirm-and-transfer"></a>Iestatīt apstiprināšanu un pārsūtīšanu

Lai izmantotu līdzekli *Apstiprināt un pārsūtīt*, tas ir jāaktivizē katrā atbilstošajā kravas veidnē. Turklāt atkarībā no jūsu prasībām, iespējams, vēlēsities sagatavot darba veidnes, lai atbalstītu šo līdzekli. Ja vēlaties strādāt ar piemēra scenāriju, kas ir sniegts tālāk šajā tēmā, iestatiet sistēmu, kā aprakstīts šajā sadaļā. (Scenārija pamatā ir **USMF** demonstrācijas dati.)

### <a name="prepare-your-load-templates"></a>Kravas veidņu sagatavošana

1. Doties uz **Noliktavas pārvaldība \> Iestatīšana \> Krava \> Kravas veidnes**.
1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Atzīmējiet izvēles rūtiņu **Atļaut kravas sadalījumu nosūtīšanas apstiprinājuma laikā**, katrai esošajai veidnei, kurā vēlaties ieslēgt līdzekli. Varat arī atlasīt **Jauns**, lai izveidotu jaunu veidni, un konfigurētu to, kā nepieciešams. Katra krava, ko izveidojat, izmantojot šo veidni, pārmantos šo funkcionalitāti. (Ja strādājat ar **USMF** demonstrācijas datiem, ieslēdziet līdzekli kravas veidnei **20-pēdu konteiners**.)

### <a name="prepare-your-work-templates"></a>Darba veidņu sagatavošana

Šis iestatījums ne vienmēr ir nepieciešams. Šeit parādītajā piemērā tiek nodrošināts, ka darbs var tikt sadalīts pēc sūtījuma, atbalstot piemēra scenāriju, kas sniegts tālāk šajā tēmā. Ir arī citi veidi, kā sasniegt šo rezultātu.

1. Doties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba veidnes**.
1. Režģa lapas augšdaļā atlasiet esošu darba veidni, kurā vēlaties iestatīt līdzekli *Apstiprināt un pārsūtīt*. (Ja strādājat ar **USMF** demonstrācijas datiem, atlasiet darba veidni **51 izdot posmam**.) Varat arī izveidot jaunu darba veidni.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu dialoglodziņu **Pārdošana**.
1. Dialoglodziņa **Pārdošana** cilnē **Kārtošana**, atlasiet **Pievienot**, lai režģim pievienotu rindu.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **Tabula:** *Pagaidu darba darbības*
    - **Atveidotā tabula:** *Pagaidu darba darbības*
    - **Lauks:** *Sūtījuma ID*
    - **Meklēšanas virziens:** *Augošā secībā*

1. Atlasiet **Labi**, lai saglabātu iestatījumus un aizvērtu dialoglodziņu **Pārdošana**.
1. Ja saņemat ziņojumu, ka grupēšana tiks atiestatīta, atlasiet **Jā**, lai turpinātu.
1. Režģī lapas **Darbu veidnes** augšdaļā, atlasiet tikko rediģēto veidni, un tad darbību rūtī atlasiet **Darba galvenes pārtraukumi**.
1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Režģī iestatiet šādas vērtības:

    - **Tabulas nosaukums:** *Pagaidu darba darbības*
    - **Lauka nosaukums:** *Sūtījuma ID*
    - **Grupēt pēc šī lauka:** atzīmējiet šo izvēles rūtiņu.

1. Darbību rūtī atlasiet **Saglabāt**.
1. Aizvērt lapu.

## <a name="scenario"></a>Scenārijs

Scenārija piemērā izdošanas process vēl nav pabeigts, bet krājumi, kas ir izdoti līdz šim, ir jāielādē kravas automašīnā un jānosūta. Tāpēc lietotājs var sadalīt neizdotās kravas rindas jaunā kravā. Visas datu relācijas tiks automātiski atjauninātas.

> [!NOTE]
> Scenārijā aprakstītās noteiktās vērtības ir balstītas uz **USMF** demonstrācijas datiem. Ieteicams izmantot šos demonstrācijas datus, kamēr demonstrējat vai apgūstat, kā izmantot šo līdzekli. Ja neizmantojat **USMF** demonstrācijas datus, aizstājiet savas vērtības kā nepieciešams.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>1. darbība: izveidot kravu ar vairākām kravas rindām

Lai varētu lietot šo funkcionalitāti, ir jābūt kravai, kas ietver vairākas kravas rindas. Ir jāpārliecinās, vai izdošanas vietās ir pietiekami daudz krājumu visiem krājumiem pārdošanas pasūtījumos, ko izveidosit. Pārskatiet vietas direktīvas iestatījumus (**Noliktavas pārvaldība \> Iestatīšana \> Vietas direktīvas**) un atzīmējiet izdošanas vietas, kas tiek izmantotas pārdošanas pasūtījuma izdošanai. Pielāgojiet krājumus, izveidojiet manuālās kustības, izmantojiet papildināšanu vai jebkuru citu plūsmu, kā nepieciešams.

Lai izveidotu atbilstošu kravu, vispirms izveidojiet trīs pārdošanas pasūtījumus, veicot šādas darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**, lai atvērtu dialoglodziņu **Izveidot pārdošanas pasūtījumu**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet šādas vērtības (kā minimums):

    - Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz *US-004* (*Cave Wholesales*).
    - Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Noliktava** uz *51*.

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu, un aizveriet dialoglodziņu **Pārdošanas pasūtījuma izveide**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Režģī **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādas vērtības:

    - **Krājuma numurs:** *M9200*
    - **Daudzums:** *40*
    - **Vienība:** *ea*

1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lai atvērtu lapu **Rezervācija**, darbību rūtī atlasiet **Rezervēt vietu**.
1. Rezervējiet krājumus pārdošanas rindā un pēc tam aizveriet lapu **Rezervācija**.
1. Atkārtojiet 1. līdz 4. soli, lai pievienotu otru pārdošanas pasūtījumu tam pašam klientam un noliktavai.
1. Pievienojiet divas pārdošanas rindas ar šādām vērtībām. Pēc katras rindas pievienošanas rezervējiet tām krājumus, kā aprakstīts 6. līdz 8. solī.

    - **1. rinda:** iestatiet lauku **Kravas numurs** uz *M9200*, lauku **Daudzums** uz *30* un lauku **Vienība** uz *Katrs*.
    - **2. rinda:** iestatiet lauku **Kravas numurs** uz *M9201*, lauku **Daudzums** uz *20* un lauku **Vienība** uz *Katrs*.

1. Atkārtojiet 1. līdz 4. soli, lai pievienotu trešo pārdošanas pasūtījumu tam pašam klientam un noliktavai.
1. Pievienojiet divas pārdošanas rindas ar šādām vērtībām. Pēc katras rindas pievienošanas rezervējiet tām krājumus, kā aprakstīts 6. līdz 8. solī.

    - **1. rinda:** iestatiet lauku **Kravas numurs** uz *M9201*, lauku **Daudzums** uz *20* un lauku **Vienība** uz *Katrs*.
    - **2. rinda:** iestatiet lauku **Kravas numurs** uz *M9202*, lauku **Daudzums** uz *60* un lauku **Vienība** uz *Katrs*.

#### <a name="load-planning-workbench"></a>Kravu plānošanas rīks

Kravu plānošanas rīks izmanto kravas veidnes ID, lai plānotu sūtījumus un izlaistu pārdošanas pasūtījuma rindas noliktavai.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Laukā **Noliktava** atlasiet *51*.

    Tagad varat izveidot kravu tikko izveidotajiem pārdošanas pasūtījumiem.

1. Cilnē **Pārdošanas rindas**, kas atrodas režģī, atlasiet pārdošanas rindas jaunajiem pārdošanas pasūtījumiem.
1. Darbību rūtī cilnē **Piedāvājums un pieprasījums** grupā **Pievienot**, atlasiet **Jaunai kravai**.
1. Dialoglodziņā **Kravas veidnes piešķire** laukā **Kravas veidnes ID** atlasiet *20-pēdu konteiners*.
1. Atlasiet **Labi**.
1. Lapas **Kravu plānošanas rīks** sadaļā **Kravas**, kas atrodas režģī, atrodiet tikko izveidoto kravas ID noliktavai *51*. Ritiniet pa labi, līdz redzat kolonnu **Atļaut kravas sadalījumu nosūtīšanas apstiprinājuma laikā**. Atlasiet izvēles rūtiņu, kas attiecas uz kravu.
1. Atlasiet kravu.
1. Izvēlnē **Izlaišana** virs režģa atlasiet **Pārvietot uz noliktavu**, lai izveidotu darbu.
1. Dialoglodziņā **Pārvietot kravu uz noliktavu** pārbaudiet, vai kopsavilkuma cilnē **Iekļaujamie ieraksti** tiek parādīts kravas ID.
1. Atlasiet **Labi**.

    Iespējams saņemsit ziņojumu “Operācijas apstrāde”, kamēr sistēma izveidos sūtījumus un darbu.

1. Lapas **Kravu plānošanas rīks** sadaļā **Kravas**, kravai vajadzētu būt ar kravas statusu *Nokomplektēts*. Atlasiet kravu un pēc tam izvēlnē **Saistītā informācija** virs režģa, atlasiet **Kopuma informācija**, lai skatītu izveidoto sūtījuma ID. Pēc pabeigšanas, aizveriet lapu **Kopumi**.
1. Lapas **Kravu plānošanas rīks** sadaļā **Kravas**, atlasiet kravu un tad izvēlnē **Saistītā informācija** virs režģa, atlasiet **Darba informācija**, lai skatītu darbu, kas tika izveidots pārdošanas pasūtījumiem.
1. Pierakstiet izveidotos darba ID. Var nākties ritināt pa labi, lai skatītu pārdošanas pasūtījuma numuru un sūtījuma ID, kas ir saistīts ar darba ID.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>2. darbība: iestatiet izpildes plūsmu mobilajām ierīcēm

Mobilās ierīces uzdevumiem būs nepieciešama lietotāja informācijas ievade, piemēram, darba ID vai noliktavas vienības ID. Laukos šī informācija parasti tiek nodrošināta noliktavas lietotājiem, kā svītrkodi, kas atrodami dokumentācijā, uz iepakojuma vai plauktiem. Lai pabeigtu mobilās ierīces scenāriju darbības, pārliecinieties, ka esat identificējis darba ID darbībām un noliktavas vienību ID krājuma un vietas darbībās.

1. Pierakstieties mobilajā ierīcē, izmantojot lietotāja ID un *51* noliktavas paroli.
1. Atlasiet **Izejošs**.
1. Atlasiet **Pārdošanas izdošana**.
1. Jums ir iespēja ievadīt darba ID vai noliktavas vienības ID. Ievadiet pirmā pārdošanas pasūtījuma darba ID un pēc tam atlasiet **Ievadīt**.
1. Laukā **Vieta** ievadiet atrašanās vietu, kas tiek rādīta, apstiprinot izdošanas vietu. Pēc tam atlasiet **Ievadīt**.
1. Laukā **LP** ievadiet noliktavas vienības ID. Noliktavas vienības ID jābūt saderīgam ar krājumu, noliktavu un krājuma atrašanās vietu, kurā notiek izdošana no atlasītās atrašanās vietas. Pēc pabeigšanas, atlasiet **Ievadīt**.
1. Laukā **Krājums** ievadiet krājuma numuru, lai apstiprinātu krājumu, kas tiek izdots, un pēc tam atlasiet **Ievadīt**.
1. Laukā **Daudz.** ievadiet krājuma daudzumu, kas tiek izdots, un pēc tam atlasiet **Ievadīt**.
1. Laukā **Mērķa LP** ievadiet mērķa noliktavas vienības ID. Mērķa noliktavas vienības definē lietotājs. Pārliecinieties, ka atcerēsities noliktavas vienības ID. Ieteicams izmantot pašreizējo datumu un divciparu secību, kā formātā (YYMMDD\#\#), piemēram, *19112301*. Pēc pabeigšanas, atlasiet **Ievadīt**.
1. Pārskatiet parādīto informāciju. Šī informācija ir *Izdošanas* informācija, kas tiks izmantota ievietošanas darbības datiem *Ievietošana*. Pēc pabeigšanas, atlasiet **Ievadīt**.

    - Tiek saņemts ziņojums **Darbība pabeigta**.

1. Atkārtojiet no 4. līdz 10. solim otrā pārdošanas pasūtījuma darba ID.

Nākamais solis ir abas izdotās noliktavas vienības ielādēt kravas automašīnā.

1. Pierakstieties mobilajā ierīcē, izmantojot lietotāja ID un *51* noliktavas paroli.
1. Atlasiet **Izejošs**.
1. Atlasiet **Pārdošanas ielāde**.
1. Ievadiet lietotāja definēto mērķa noliktavas vienības ID, ko izveidojāt pirmajam darba ID iepriekšējā procedūrā. Pēc tam atlasiet **Enter**, lai ievietotu mērķa noliktavas vienību vietā **STAGE**.
1. Vēlreiz ievadiet mērķa noliktavas vienības ID un pēc tam atlasiet **Ievadīt**, lai ievietotu noliktavas vienību vietā **AIZMUGURĒJĀS DURVIS**.
1. Atkārtojiet 4. līdz 5. soli mērķa noliktavas vienības ID, ko izveidojāt otrajam darba ID.

Abi darba ID tiks slēgti (ielādēti).

### <a name="step-3-confirm-the-outbound-shipment"></a>3. darbība: apstipriniet izejošu sūtījumu

Šajā darbībā, tiek apstiprināti divi pārdošanas pasūtījumi un darbi, kas ir apstiprināti ielādei, lai nosūtītu izdotos krājumus no kravas un izveidotu jaunu kravu neizdotajiem krājumiem. Izejoša sūtījuma apstiprinājums ir jāveic lapā **Kravas informācija**.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Kravu plānošanas rīks**.
1. Režģī sadaļā **Kravas** atlasiet jūsu izveidotās kravas ID rindu.
1. Izvēlieties kravas ID saiti, lai atvērtu lapu **Kravas informācija**.
1. Lapas **Kravas informācija** darbību rūts cilnē **Nosūtīt un saņemt** grupā **Apstiprināt**, atlasiet **Izejošs sūtījums**, lai sāktu apstiprināšanu.
1. Dialoglodziņā **Nosūtīšanas apstiprinājums**, kas atrodas laukā **Ielādēt sadalījuma metodi nosūtīšanas apstiprinājuma laikā**, atlasiet *Sadalīt daudzumu jaunai kravai*.
1. Atlasiet **Labi**.

    Iespējams saņemsit ziņojumu “Operācijas apstrāde”.

    Tiek saņemti informatīvi ziņojumi, kas norāda, ka krava ir apstiprināta nosūtīšanai un ka no sadalīšanas daudzuma ir izveidota jauna krava.

Atsvaidziniet lapu **Kravu plānošanas rīks**, lai skatītu tikko izveidoto kravu.

Varat arī apstiprināt, ka darbību relācijas ir atjauninātas šādos veidos:

- Atlikušie (neapstrādātie) sūtījumi un sūtījumu rindas tiek atjauninātas ar jaunu kravas ID.
- Pārdošanas pasūtījums ir saistīts ar jaunu kravas ID.
- Sākotnējā krava neietver atlikušās kravas rindas.
- Atlikušais darbs ir atjaunināts ar jaunu kravas ID.
- Kopums paliek nemainīts.
- Jaunās kravas statuss ir pareizi atjaunināts. (Ja darba statuss ir _Procesā_ kravas statuss arī ir _Procesā_.)

## <a name="notes-and-tips"></a>Piezīmes un padomi

- Varat ieslēgt parametru **Atļaut kravas sadalījumu nosūtīšanas apstiprinājuma laikā** pēc tam, kad krava ir izveidota ar izslēgtu **Kravas veidne** parametru, bet pirms ir sācies ielādes process. Dodieties uz vēlamo kravu un tad galvenes skatā ieslēdziet parametru.
- Opcija **Sadalīt daudzumu jaunai kravai** darbojas arī tad, ja dažiem atlikušā darba virsrakstiem ir statuss *Procesā*. Tāpēc joprojām varat izmantot funkcionalitāti, pat ja darbinieki jau izmanto izdošanas pasūtījumus.
- Atlasot **Atcelt neizpildīto daudzumu**, kamēr vēl ir atlikušais darbs ar statusu *Atvērts* vai *Notiek izpilde*, tiek parādīts šāds kļūdas ziņojums: “Nevar atcelt atlikušo kravas daudzumu. Darbam ir krava. "
- Atlasot **Atcelt neizpildīto daudzumu**, kad nav neviena atlikušā darba, bet kravā ir neatbrīvotas kravas rindas, tiek parādīts šāds kļūdas ziņojums: “Kravas nosūtīšanu nevarēja apstiprināt, jo krājuma daudzums pārsniedz procentuālo vērtību, kas definēta zem piegādes.” Lai izvairītos no kļūdas, varat iestatīt **Nepilns pasūtījums** procentuālo vērtību neatbrīvotai kravas rindai 100 procenti. Neizlaistās rindas netiks pārvietotas uz jaunu kravu, bet pašreizējā krava tiks apstiprināta ar nepietiekamu piegādi. Šādā gadījumā vairs nebūs iespējams atkārtoti nodot sākotnējo pasūtījumu. Tādēļ nāksies rīkoties citādi.
