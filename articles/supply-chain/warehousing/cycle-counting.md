---
title: "Cikla inventarizācija"
description: "Šajā rakstā aprakstīts, kā var izmantot cikla inventarizāciju ar noliktavas risinājumu, kas ir pieejams modulī Noliktavas pārvaldība. Šis raksts neattiecas uz noliktavas risinājumu, kas ir pieejams modulī Krājumu vadība."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2437d3efe7841021ff4bd35f307fddddc76eb4c6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="cycle-counting"></a>Cikla inventarizācija

[!include[banner](../includes/banner.md)]


Šajā rakstā aprakstīts, kā var izmantot cikla inventarizāciju ar noliktavas risinājumu, kas ir pieejams modulī Noliktavas pārvaldība. Šis raksts neattiecas uz noliktavas risinājumu, kas ir pieejams modulī Krājumu vadība.

Cikla inventarizācija ir noliktavas process, ko var izmantot, lai auditētu rīcībā esošu krājumu vienības. Cikla inventarizācijas procesu var aprakstīt trīs soļos:

1.  **Cikla inventarizācijas darba izveide** — cikla inventarizācijas darbu var izveidot automātiski, pamatojoties uz krājumu sliekšņa parametriem vai izmantojot cikla inventarizācijas plānu. Vai arī varat manuāli izveidot cikla inventarizācijas darbu, izmantojot krājuma vai noliktavas parametrus lapā **Cikla inventarizācijas darbs pēc krājuma** vai lapā **Cikla inventarizācijas darbs pēc novietojuma**.
2.  **Cikla inventarizācijas apstrāde** — pēc cikla inventarizācijas darba izveides tas tiek veikts, saskaitot noliktavas novietojumā esošos krājumus un pēc tam izmantojot mobilo ierīci, lai ievadītu rezultātu programmatūrā Microsoft Dynamics 365 for Finance and Operations. Noliktavas novietojumā esošos krājumus var arī saskaitīt, neizveidojot cikla inventarizācijas darbu. Šo procesu sauc par *cikla inventarizāciju uz vietas*.
3.  **Aprēķinātās vērtības starpību atrisināšana** — pēc cikla inventarizācijas visiem krājumiem ar uzskaitītās vērtības starpību lapā **Viss darbs** tiek piešķirts statuss **Neapstiprināts pārskats**. Šīs starpības var atrisināt lapā **Izskatīšanu gaidošais cikla inventarizācijas darbs**.

Šajā ilustrācijā ir parādīts cikla inventarizācijas process. ![Cikla inventarizācijas procesa plūsma](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Cikla inventarizācijas priekšnoteikumi
Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda, pirms varat izmantot cikla inventarizāciju.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Priekšnosacījums</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Krājums</td>
<td>Krājumam jābūt iespējotam noliktavas pārvaldības procesiem.</td>
</tr>
<tr class="even">
<td>Noliktava</td>
<td>Noliktavai jābūt iespējotai noliktavas pārvaldības procesiem. Lai noliktavu aktivizētu noliktavas pārvaldības procesiem, lapā <strong>Noliktavas</strong> atlasiet noliktavu un pēc tam atzīmējiet opciju <strong>Izmantot noliktavas pārvaldības procesus</strong>. Lai cikla inventarizācijas laikā darbinieki varētu pārvietot paletes, kopsavilkuma cilnē <strong>Noliktavas pārvaldība</strong> atlasiet opciju <strong>Atļaut palešu pārvietošanu cikla inventarizācijas laikā</strong>.</td>
</tr>
<tr class="odd">
<td>Darbu pūli</td>
<td>Nav obligāti: izveidojiet darba kopu, lai nošķirtu noliktavas darbu, pamatojoties uz darba veidu (šajā gadījumā cikla inventarizācijas darbs).</td>
</tr>
<tr class="even">
<td>Vietas</td>
<td>Iespējojiet cikla inventarizāciju novietojumiem. Lai iespējotu cikla inventarizāciju noliktavas novietojumā, lapā <strong>Novietojuma profili</strong> atlasiet opciju <strong>Atļaut cikla inventarizāciju</strong>.</td>
</tr>
<tr class="odd">
<td>Noliktavas vadības parametri</td>
<td>Iestatiet cikla inventarizācijas parametrus. Lapā <strong>Noliktavas pārvaldības parametri</strong> norādiet noklusējuma korekcijas veida kodu, darba klases ID un cikla inventarizācijas darba prioritāti.</td>
</tr>
<tr class="even">
<td>Mobilā ierīce</td>
<td><ul>
<li>Izveidojiet vienas tālāk lapā <strong>Mobilās ierīces izvēlnes vienumi</strong> minētās metodes izvēlnes vienumu:
<ul>
<li>Lietotāja noteikta cikla inventarizācija</li>
<li>Sistēmas noteikta cikla inventarizācija</li>
<li>Cikla inventarizācijas grupēšana</li>
<li>Cikla inventarizācija uz vietas</li>
</ul>
</li>
<li>Iestatiet izvēlni mobilajai ierīcei.</li>
<li>Izveidojiet darba lietotāja kontu un piešķiriet mobilās ierīces izvēlni, ko izmantot darba lietotāja ID.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Saistītais iestatīšanas uzdevums</td>
<td>Iestatiet cikla inventarizācijas plānu noliktavas novietojumam.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Automātiska cikla inventarizācijas darba izveide
Ir divi veidi, kā plānot cikla inventarizācijas darba periodisku izveidi: iestatīt cikla inventarizācijas sliekšņa vērtības vai iestatīt cikla inventarizācijas plānus.

-   Cikla inventarizācijas slieksnis norāda krājumu vienību daudzumu vai procentuālo ierobežojumu. Cikla inventarizācijas darbs tiek izveidots automātiski, kad tiek sasniegts sliekšņa ierobežojums.
-   Cikla inventarizācijas plāns izveido cikla inventarizācijas darbu uzreiz vai periodiski, izmantojot pakešuzdevumu. Kad tiek izveidots cikla inventarizācijas darbs, inventarizācijas darba rinda satur informāciju par to, kurā novietojumā veikt inventarizāciju. Ar šo novietojumu saistītie rīcībā esošie krājumi netiek bloķēti, un tāpēc tie ir pieejami rezervēšanai un izejošajai apstrādei pat tad, ja pastāv atvērts inventarizācijas darbs.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Cikla inventarizācijas darba izveide, pamatojoties uz krājumu sliekšņa parametriem

Cikla inventarizācijas darbu var izveidot, ja krājumu skaits ir mazāks par noteikto sliekšņa vērtību attiecīgajā novietojumā. Piemēram, novietojumā, kura cikla inventarizācijas sliekšņa vērtība ir 40, ir 60 krājumi. Pārdošanas pasūtījuma transakcijas laikā 25 krājumi tiek izdoti no novietojuma un izvietoti sagatavošanas posma novietojumā. Jaunais krājumu skaits ir 35, un tas ir mazāks par sliekšņa vērtību, tādēļ cikla inventarizācijas darbs novietojumam tiek izveidots automātiski.

### <a name="schedule-cycle-counting-work"></a>Cikla inventarizācijas darba plānošana

Cikla inventarizācijas plānu var ieplānot, lai cikla inventarizācijas darbu izveidotu uzreiz vai periodiski. Iestatot cikla inventarizācijas plānus, jūs varat kontrolēt darba kopu, kurai tiek izveidots cikla inventarizācijas darbs, maksimālo cikla inventarizāciju skaitu, kas tiek izveidotas krājumiem dažādos novietojumos, un dienu skaitu, pirms noliktavas novietojumā atkal tiek veikta inventarizācija. Piemēram, krājums ir pieejams trīs novietojumos noliktavā, un maksimālajam cikla inventarizāciju skaitam ir iestatīta vērtība **2**. Šādā gadījumā, palaižot cikla inventarizācijas plānu, tiks izveidotas divas cikla inventarizācijas diviem novietojumiem, kuros atrodas krājumi. Vēl viens piemērs — jūs iestatāt dienu skaitam starp cikla inventarizācijām vērtību **5**. Šādā gadījumā cikla inventarizācijas darbs tiek izveidots ik pēc piecām dienām. Tomēr, ja cikla inventarizācijas darbs tiek apstrādāts 3. dienā, nākamais cikla inventarizācijas darbs tiks izveidots piecas dienas pēc tam, kad tika apstrādāta pēdējā cikla inventarizācija, t. i., 8. dienā.

## <a name="create-cycle-counting-work-manually"></a>Manuāla cikla inventarizācijas darba izveide
Lai izveidotu cikla inventarizācijas darbu manuāli, var izmantot lapu **Cikla inventarizācijas darbs pēc krājuma** vai **Cikla inventarizācijas darbs pēc novietojuma**. Jūs varat norādīt maksimālo izveidojamo cikla inventarizāciju skaitu. Piemēram, ja noliktavas vadītājs norāda vērtību **5**, cikla inventarizācijas darbs tiek izveidots piecos novietojumos pat tad, ja šis krājums ir iekļauts 10 novietojumos. Jūs arī varat atlasīt darba kopas ID, kam jāpiešķir izveidotie cikla inventarizācijas darba ID. Kad darba kopas ID tiek apstrādāts cikla inventarizācijai, šai darba kopai piešķirtie cikla inventarizācijas darba ID tiek apstrādāti kā grupa.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Cikla inventarizācijas izpilde, izmantojot mobilo ierīci
Ir pieejamas vairākas metodes, kā var apstrādāt cikla inventarizācijas darbu, izmantojot programmatūru Microsoft Dynamics 365 for Finance and Operations mobilajā ierīcē.

-   **Lietotāja vadība** — darbinieks var norādīt cikla inventarizācijas darba ID ar statusu **Atvērts**.
-   **Sistēmas noteikts** — programmatūrā Dynamics 365 for Finance and Operations darbiniekam tiek piešķirts cikla inventarizācijas darba ID.
-   **Cikla inventarizācijas grupēšana** — darbinieks var grupēt cikla inventarizācijas darba ID, kas noteikti konkrētam novietojumam, zonai vai darbu kopai.
-   **Vietas cikla inventarizācija** — darbinieks jebkurā laikā var saskaitīt noliktavas novietojumā esošos krājumus, neveidojot cikla inventarizācijas darbu. Lai veiktu vietas cikla inventarizāciju kādā novietojumā, darbinieks ievada novietojuma ID.

Tālāk ir sniegts piemērs, kā veikt vietas cikla inventarizāciju, izmantojot mobilo ierīci. Norādījumi, kurus darbinieks redz ierīcē, mainās atkarībā no cikla inventarizācijas izvēlnes vienuma iestatījumiem.

1.  Mobilajā ierīcē atlasiet izvēlnes vienumu, lai apstrādātu vietas cikla inventarizācijas darbu.
2.  Reģistrējiet novietojumu, kur veikt vietas cikla inventarizāciju.
3.  Reģistrējiet un apstipriniet krājuma kodu un saskaitīto krājumu daudzumu. **Piezīme.** Atkarībā no lapā **Nodarbinātais** iestatītajiem parametriem lapā **Viss darbs** tiek atjaunināts cikla inventarizācijas darba statuss **Gaida pārskatu** vai **Slēgts**.
4.  Nav obligāti: novietojumā atlikušajiem krājumiem atkārtojiet 3. darbību un pārbaudiet, vai inventarizācija nav jāveic papildu krājumiem.

## <a name="resolve-cycle-counting-differences"></a>Cikla inventarizācijas starpību atrisināšana
Ja ar darba lietotāja ID saistītajai opcijai **Ir cikla inventarizācijas vadītājs** ir atzīmēts iestatījums **Nē**, tālāk minētajos scenārijos rodas cikla inventarizācijas starpība.

-   Inventarizācijas laikā aprēķinātā vērtība neatbilst novirzes ierobežojumiem, kas noteikti lapas **Darba lietotāji** laukā **Maksimālais procentuālais ierobežojums** vai **Maksimālais daudzuma ierobežojums**. Piemēram, novietojumā rīcībā esošo krājumu skaits ir 50, un darba lietotājam noteiktā novirzes robežas vērtība ir 10. Ja darba lietotājs ievada vērtību, kas nav starp 40 un 60, rodas starpība.
-   Inventarizācijas laikā aprēķinātā vērtība atšķiras no rīcībā esošo krājumu daudzuma, un nav iestatīti novirzes ierobežojumi.

Jūs varat pielāgot inventarizācijas laikā aprēķinātās vērtības starpības un pēc tam akceptēt inventarizācijas laikā aprēķināto vērtību lapā **Izskatīšanu gaidošā cikla inventarizācija**. Jūs varat pārbaudīt koriģēto krājuma daudzuma skaitu lapā **Rīcībā esošie krājumi pēc novietojuma**. Inventarizācijas laikā aprēķinātā vērtība tiek noraidīta, ja starpību nevar apstiprināt.

# <a name="see-also"></a>Skatiet arī
[Konfigurēt mobilās ierīces darbam noliktavā](configure-mobile-devices-warehouse.md)




