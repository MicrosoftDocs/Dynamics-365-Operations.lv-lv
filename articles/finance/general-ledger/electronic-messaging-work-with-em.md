---
title: Darbs ar elektronisko ziņojumu funkcionalitāti
description: Šajā tēmā ir sniegta informācija, kā strādāt ar elektronisko ziņojumu (EM) funkcionalitāti.
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8fd2301808f7eaec2ea9c01a66f030f527f461a36b3cb8aabddcfbf414f06d2a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779912"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Darbs ar elektronisko ziņojumu funkcionalitāti

[!include [banner](../includes/banner.md)]

Strādājot ziņojuma līmenī, noderīgāka ir lapa **Elektroniskie ziņojumi** (**Nodoklis** \> **Pieprasījumi un pārskati** \> **Elektroniskie ziņojumi** \> **Elektroniskie ziņojumi**). Strādājot datu vākšanas vai ziņojuma vienuma līmenī, noderīgāka ir lapa **Elektroniskā ziņojuma vienumi** (**Nodoklis** \> **Pieprasījumi un pārskati** \> **Elektroniskie ziņojumi** \> **Elektr. ziņojuma vienumi**).

## <a name="electronic-messages"></a>Elektroniskie ziņojumi

Lapa **Elektroniskie ziņojumi** norāda apstrādi, kas ir pieejama jums, pamatojoties uz jūsu lomu. Drošības lomas tiek saistītas ar apstrādi, iestatot attiecīgo apstrādi. Katrai apstrādei, kas jums ir pieejama, lapā ir redzami elektroniskie ziņojumi un ar tiem saistītā informācija.

Kopsav. cilnē **Ziņojumi** tiek rādīti atlasītās apstrādes elektron. ziņojumi. Atkarībā no atlasītā ziņojuma un iepriekš definētas apstrādes statusa dažas darbības var palaist, izmantojot pogas virs režģa:

- **Jauns** — šī poga ir saistīta ar darbībām, kuru tips ir **Izveidot ziņojumu**.
- **Dzēst** — šī poga ir pieejama, ja atlasītā ziņojuma pašreizējam statusam ir atzīmēta izvēles rūtiņa **Atļaut dzēšanu**.
- **Apkopot datus** — šī poga ir saistīta ar darbībām, kuru tips ir **Aizpildīt ierakstus**.
- **Ģenerēt pārskatu** — šī poga ir saistīta ar darbību tipu **Elektr. pārsk. veidoš. eksporta ziņojums**.
- **Sūtīt pārskatu** — šī poga ir saistīta ar darbību tipu **Tīmekļa pakalpojums**.
- **Importēt atbildi** — šī poga ir saistīta ar darbībām, kuru tips ir **Elektroniskā pārskata veidošanas imports**.
- **Atjaunināt statusu** — šī poga ir saistīta ar darbību tipu **Ziņojuma līmeņa lietotāja apstrāde**.
- **Ziņojuma vienumi** — atv. lapu **Elektr. ziņoj. vienumi**.

Kopsav. cilnē **Darbību žurnāls** ir redzama inform. par visām darbībām, kas izpildītas atlasītajam ziņojumam. Ja darbība izraisīja kļūdu, informācija par kļūdu ir pievienota saistītajai rindai režģī. Lai pārskatītu informāciju par kļūdu, atlasiet rindu režģī un pēc tam atlasiet pogu **Pielikums** (papīra saspraudes simbols) lapas augšējā labajā stūrī.

Kopsavilkuma cilnē **Ziņojuma papildu lauki** ir redzami visi papildu lauki, kas definēti ziņojumiem apstrādes iestatījumos. Kopsavilkuma cilnē arī ietilpst šo papildu lauku vērtības.

Kopsav. cilnē **Ziņojuma vienumi** ir redzami visi ziņ. vienumi, kas saistīti ar atlasīto ziņojumu. Atkarībā no atlasītā ziņojuma vienuma statusa dažas darbības var palaist, izmantojot pogas virs režģa:

- **Dzēst** — šī poga ir pieejama, ja atlasītā ziņojuma vienuma pašreizējam statusam ir atzīmēta izvēles rūtiņa **Atļaut dzēšanu**.
- **Atjaunināt statusu** — šī poga ir saistīta ar darbību tipu **Lietotāja apstrāde**.
- **Oriģinālais dokuments** — atveriet lapu, kurā redzams sākotnējais dokuments atlasītajam ziņojuma vienumam.

Pārskati, kas jau ir ģenerēti un saņemti attiecībā uz ziņojumu, ir pievienoti attiecīgajam ziņojumam. Lai skatītu ar ziņojumu saistītos pielikumus, atlasiet ziņojumu un pēc tam atlasiet pogu **Pielikums** (papīra saspraudes simbols) lapas augšējā labajā stūrī.

![Poga Pielikums](media/attachment-icon.png)

Poga **Pielikumi** norāda pielikumus, kas ir saistīti ar atlasīto ziņojumu. Lai skatītu failu, atlasiet to sarakstā pa kreisi un pēc tam darbību rūtī atlasiet **Atvērt**.

![Poga Atvērt](media/open-button.png)

Varat skatīt pielikumus, kas ir saistīti ar noteiktu darbību, kura iepriekš izpildīta ziņojumam. Lapā **Elektroniskie ziņojumi** kopsavilkuma cilnē **Ziņojumi** atlasiet ziņojumu. Kopsavilkuma cilnē **Darbību žurnāls** atlasiet darbību un pēc tam lapas augšējā labajā stūrī atlasiet pogu **Pielikums** (papīra sakliķa simbols).

Varat palaist visu apstrādi vai tikai konkrētu darbību, atlasot darbību rūtī **Palaist apstrādi**.

## <a name="electronic-message-items"></a>Elektroniskie ziņojumu krājumi

Lapa **Elektr. ziņoj. vienumi** tiek radīti visi ziņojuma vienumi un tādu darbību žurnāls, kas izpildītas katram ziņojuma vienumam. Lapā arī ir norādīti papildu lauki, kas ir definēti ziņojuma vienumiem, un šo papildu lauku vērtības.

Nākamajā tabulā ir aprakstīti lauki cilnē **Ziņojuma vienumi**.

<table>
<thead>
<tr>
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr>
<td>Apstrādā</td>
<td>Apstrādes nosaukums, kas izmantota, lai izveidotu ziņojuma vienumu.</td>
</tr>
<tr>
<td>Ziņojuma krājums</td>
<td>Ziņojuma vienuma ID. Šis ID tiek automātiski piešķirts, pamatojoties uz <b>Ziņojuma vienuma</b> numura sēriju, kas definēta lapā <b>Virsgrāmatas parametri</b>.</td>
</tr>
<tr>
<td>Ziņojuma krājuma datums</td>
<td>Ziņojuma vienuma izveidošanas datums.</td>
</tr>
<tr>
<td>Ziņojuma krājuma veids</td>
<td>Ziņojuma vienuma tips. Tai pašai apstrādei var iestatīt vairāku tipu ziņojuma vienumus (piemēram, <b>Ienākošie rēķini</b> un <b>Izejošie rēķini</b>). Šo lauku var iestatīt automātiski tikai tad, kad rēķins tiek pievienots ziņojumu vienumu tabulā.</td>
</tr>
<tr>
<td>Ziņojuma krājuma statuss</td>
<td><p>Ziņojuma vienuma faktiskais statuss. Pieejamie statusi mainās atkarībā no ziņojuma vienumu tipa. Daži piemēri:</p>
<ul>
<li><b>Aizpildīts</b> — ieraksts tika pievienots ziņ. vienumu tabulā.</li>
<li><b>Novērtēts</b> — ziņojuma vienumam tika aprēķināti papildu atribūti.</li>
<li><b>Iekļauts pārskatā</b> — ziņ. vienums veiksmīgi pievienots pārskatā.</li>
<li><b>Nav iekļauts</b> — šis statuss ir noderīgs, ja daži ziņ. vienumi jāizslēdz no pārskata pirms tā eksportēšanas.</li>
</ul>
</td>
</tr>
<tr>
<td>Pārsūtīšanas datums</td>
<td>Apstrādei, kas automātiski pārsūta ģenerēto pārskatu ārpus sistēmas, datums, kad tika pārsūtīts ziņojuma vienums.</td>
</tr>
<tr>
<td>Dokumenta numurs</td>
<td>Šis lauks tiek iestatīts automāt., balstoties uz ierakstu aizpildīš. darb. iestatījumu. Šo lauku var iestatīt automātiski tikai tad, kad rēķins tiek pievienots ziņojumu vienumu tabulā.</td>
</tr>
<tr>
<td>Konta numurs</td>
<td>Debitora vai kreditora konta numurs vai cita lauka vērtība atkarībā no lauka, kas definēts ierakstu aizpildīšanas darbībai. Šo lauku var iestatīt automātiski tikai tad, kad rēķins tiek pievienots ziņojumu vienumu tabulā.</td>
</tr>
<tr>
<td>Zņojums</td>
<td>Ziņojuma numurs. Šis numurs tiek automātiski piešķirts, pamatojoties uz <b>Ziņojuma</b> numura sēriju, kas definēta lapā <b>Virsgrāmatas parametri</b>.</td>
</tr>
<tr>
<td>Ziņojuma statuss</td>
<td>Elektroniskā ziņojuma faktiskais statuss.</td>
</tr>
<tr>
<td>Nākamā darbība</td>
<td>Nākamās darbības, kuras var sākt ziņojuma vienuma pašreizējam statusam.</td>
</tr>
</tbody>
</table>

Cilnē **Papildu lauki** tiek rādīti papildu lauki atlasītajam ziņojuma vienumam un to vērtības.

### <a name="run-processing"></a>Apstrādes palaišana

Darbību rūtī atlasiet **Palaist apstrādi**, lai palaistu apstrādi ziņojuma vienumiem. Lai palaistu noteiktu darbību, dialoglodziņā **Palaist apstrādi** opcijai **Izvēlēties darbību** iestatiet **Jā** un tad atlasiet darbību. Lai palaistu visu apstrādi, opcijai **Izvēlēties darbību** iestatiet **Nē**.

### <a name="generate-report"></a>Ģenerēt pārskatu

Darbību rūtī atlasiet **Ģenerēt pārskatu**. Šī poga ir saistīta ar darbību tipu **Elektroniskā pārskata veidošanas eksports**.

### <a name="update-status"></a>Labot statusu

Darbību rūtī atlasiet **Atjaun. statusu**, lai atjaun. viena vai vairāku ziņ. vien. statusu. Dialoglodziņā **Atjaunināt statusu** lietojiet cilni **Iekļaujamie ieraksti**, lai atlasītu atjaunināšanai ziņojuma vienumus. Pārliecinieties, vai ir pareizi definēti atlases kritēriji, jo ziņojuma vienumu statusi tiks atjaunināti saskaņā ar šiem kritērijiem, atlasītās darbības sākotnējo statusu un jūsu norādīto vērtību laukā **Jauns statuss**. Pēc statusa atjaunināšanas pabeigšanas būs grūti noteikt, kuri vienumi tika atjaunināti. Tādēļ būs grūti atritināt statusa atjauninājumu.

### <a name="electronic-messages"></a>Elektroniskie ziņojumi

Darbību rūtī atlasiet **Elektroniskie ziņojumi**, lai apskatītu elektronisko ziņojumu, kas saistīts ar atlasīto ziņojuma vienumu.

Var arī apskatīt failus, kas saistīti ar noteiktu ziņojuma vienumu. Atlasiet ziņojuma vienuma lauku **Ziņojums** vai darbību rūtī atlasiet **Elektroniskie ziņojumi**. Lapā **Elektroniskais ziņojums** atlasiet ziņojumu, kuram skatīt failus, un pēc tam atlasiet pogu **Pielikums** (papīra saspraudes simbols) lapas augšējā labajā stūrī.

Poga **Pielikums** norāda pielikumus, kas ir saistīti ar ziņojumu. Lai skatītu failu, atlasiet to sarakstā pa kreisi un pēc tam atlasiet **Atvērt** darbību rūtī.

### <a name="original-document"></a>Oriģinālais dokuments

Darbību rūtī atlasiet **Oriģinālais dokuments**, lai atvērtu sākotnējo dok. atlasītajam ziņojuma vienumam.
