---
title: Iestatīt darba sadalījuma struktūras veidņu lomas
description: Šajā tēmā sniegta informācija par lomas informācijas iestatīšanu darba sadalījuma struktūras veidnēs.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760606"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Iestatīt darba sadalījuma struktūras veidņu lomas

[!include [banner](../includes/banner.md)]

Projektu vadītāji var iestatīt darba sadalījuma struktūras (Work breakdown structure - WBS) veidnes, kuras var lietot, izveidojot WBS jauniem projektiem. Projektu vadītāji var pievienot lomas veidnes izveides laikā. Izmantojiet šādu procedūru, lai piešķirtu lomu WBS veidnei.

1. Atlasiet **Projektu vadība un uzskaite** > **Iestatījumi** > **Projekti** > **Darba sadalījuma struktūras veidnes**.
2. Atlasītajai WBS veidnei atlasiet **Detalizēta informācija**.
3. Atlasiet sarakstā uzdevumu un pēc tam laukā **Loma** atlasiet lomu, kura tiks piešķirta uzdevumam.

## <a name="work-with-a-wbs"></a>Darbs ar WBS

Jūs varat izveidot jaunu WBS vai kopēt WBS no esošas WBS veidnes. Projektu vadītājs var ērti pārvaldīt resursus, piešķirot lomas jauniem uzdevumiem WBS struktūrā. Lomas var aizstāt vai nu pēc tam, kad resurss ir iegūts, vai arī pēc tam, kad ir identificēts apstiprināts resurss darbam pie attiecīgā uzdevuma. Šis elastīgums ļauj projektu vadītājiem veikt šādus uzdevumus:

- Identificēt resursu skaitu, kas nepieciešami WBS darba pakotnēm.
- Novērtēt projekta izmaksas.
- Noteikt sākotnējo budžetu.
- Novērtēt darbību ilgumu, pamatojoties uz lomām un resursiem.
- Izstrādāt dažus projekta vadības plānus, pamatojoties uz pieejamo projekta informāciju.

WBS struktūrā ir pievienotas papildu opcijas, lai labāk izmantotu resursu sadalījuma funkcionalitāti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resursu piešķires</td>
<td>Skatīt piešķirtos resursus, datumus, stundu skaitu un rezervācijas tipu uzdevumiem WBS struktūrā.</td>
</tr>
<tr class="even">
<td>Automātiski ģenerēt grupu</td>
<td>Automātiski pievienot plānotos resursus, izmantojot lomas, kas ir saistītas ar uzdevumu. Programma Finance automātiski iesaka plānotos resursus, izmantojot vairāku kritēriju lēmumu analīzi, kuras pamatā ir lomas. Pēc lomu un darba (stundas) iestatīšanas uzdevumiem WBS struktūrā un pēc struktūras nodošanas atlasiet <strong>Automātiski ģenerēt grupu</strong>. Nepieciešamais plānoto resursu skaits tiek pievienots WBS struktūrai un cilnē <strong>Projekta un grupas plānošana</strong>.</td>
</tr>
<tr class="odd">
<td>Resurss (nolaižamais saraksts)</td>
<td>Lapā <strong>Palaist resursu piešķiri</strong> varat atlasīt resursus stingrai vai vieglai rezervācijai, pamatojoties uz noteiktu ilgumu. Jūs varat pielāgot skata iestatījumus, lai skatītu un iestatītu resursu darbību ilgumu. Jūs varat atlasīt un piešķirt resursus darba pakotņu līmenī, izmantojot šādas opcijas:
<ul>
<li><strong>Pieņemt</strong> — apstiprināt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Atcelt</strong> — atcelt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Piešķirt automātiski</strong> – atlasītajam uzdevumam tiek automātiski atlasīts un piešķirts pieejams personāla resurss ar atbilstošu lomu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Lapā **Visi projekti** atlasiet projektu **XYZ jaunināšanas fāze 2**.
2. Atlasiet **Plāns** > **Aktivitātes** > **Darba sadalījuma struktūra**.
3. Atlasiet **Jauns**, lai WBS struktūrā pievienotu šādas pirmā līmeņa aktivitātes:

    - Uzsākšana
    - Plānošana
    - Izpilda
    - Pārraudzīšana un kontrole
    - Slēgt

4. Iestatiet datumus un darbu (stundas), kā parādīts nākamajā attēlā.

    [![Datumu un darba iestatīšana](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Atlasiet uzdevuma rindu **Uzsākšana** un pēc tam laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
6. Atlasiet **Publicēt**.
7. Tajā pašā rindā, laukā **Resurss** atlasiet **Rihards Taurenis** un pēc tam atlasiet **Pieņemt**.
8. Atlasiet uzdevuma rindu **Plānošana** un pēc tam laukā **Loma** atlasiet **Biznesa analītiķis**.
9. Atlasiet **Publicēt** un pēc tam atlasiet **Automātiski ģenerēt grupu**.
10. Tiek parādīts ziņojuma lodziņš, un atlasiet tajā **Jā**.
11. Laukā **Resurss** pārbaudiet, vai vērtība ir **Biznesa analītiķis 1**.
12. Resursam **Biznesa analītiķis 1** atveriet uzmeklēšanu un atlasiet **Palaist resursu piešķires**. Pēc tam atlasiet nodarbināto attiecīgajam uzdevumam.
13. Atlasiet **Nestingrā piešķiršana** &gt; **Visa noslodze**.

    > [!NOTE] 
    > Netiek parādīts brīdinājums par to, ka norādītais resurss tagad ir 2, jo resursu skaits joprojām ir 1.

14. Lapā **Darba sadalījuma struktūra** pārbaudiet resursa piešķiri WBS struktūrā un pēc tam atlasiet **Saglabāt**.
