---
title: "BOM veidotāja funkcionalitāte"
description: "Šajā rakstā ir aprakstīts, kā jūs varat izmantot MK veidotāja lapu, lai materiālu komplektiem (MK) projektētu koka struktūras un strādātu ar tām. Varat noklikšķināt uz Iestatīšana, lai atlasītu dažādas konfigurācijas, un norādīt, kāda informācija tiek rādīta koka rindās."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c871cf4e5ee7f359010aac1fa0fef81e0e0df564
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="bom-designer-functionality"></a>BOM veidotāja funkcionalitāte

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā jūs varat izmantot MK veidotāja lapu, lai materiālu komplektiem (MK) projektētu koka struktūras un strādātu ar tām. Varat noklikšķināt uz Iestatīšana, lai atlasītu dažādas konfigurācijas, un norādīt, kāda informācija tiek rādīta koka rindās.

Ja atverat lapu **BOM veidotājs** no lapas **Izlaistās preces**, tā parāda materiālu komplektu hierarhiju, kas ir aktīva un apstiprināta atlasītajam krājumam, krājuma noklusējuma pasūtījuma vietu un faktisko datumu.  

Noklikšķiniet uz **Filtrs**, lai mainītu sākotnējo atlasi skatījumā. Iestatot rādīšanas principu uz **Atlasītie/Aktīvie vai atlasītie**, jūs varat atlasīt atsevišķus MK vai maršrutu versijas izmantošanai skatījumā. Jūs varat atlasīt neapstiprinātā un neaktīvā MK versijas, lai parādītu vai uzturētu materiālu komplekta veidotājā.  

**Piezīme:** ja MK veidotājs tiek atvērts no saraksta lapas **Materiālu komplekts**, tas neparāda maršruta informāciju. Pašlaik MK vai maršrutu versijas atlase ir MK un maršruta versijas rekvizīts, un attiecas uz visām MK veidotāja instancēm.  

Turpmākajās sadaļās aprakstīta funkcionalitāte, kas ir pieejama dažādās MK veidotāja cilnēs.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>MK struktūras analīze, izmantojot MK veidotāju
MK veidotājam ir divas sadaļas:

-   MK struktūras koka skatījums
-   Detalizētas informācijas sadaļa, kurā sniegta detalizēta informācija par atlasītajiem datiem. Atlasot zaru koka skatā, FastTabs tiek atjauninātas detalizētas informācijas sadaļā, pamatojoties uz šo mezglu:
    -   **Detalizēta informācija par MK rindu** – sniedz detalizētu informācija par MK rindu, kas ir atlasīta koka skatā.
    -   **Krājuma dati** – sniedz detalizētu informāciju par galveno krājumu vai krājumiem, kas tiek izmantoti atlasītajā zarā. Varat noklikšķināt uz **Labot izlaisto preci**, lai uzturētu atlasīto krājumu.
    -   **MK** – rāda MK virsrakstu, kas attiecas uz atlasīto zaru.
    -   **Maršruts** – rāda maršruta virsrakstu, kas attiecas uz atlasīto zaru.
    -   **Maršruta operācijas** – rāda maršruta operāciju priekšskatījumu. Kad ir atlasīta MK rinda, kas ir piešķirta konkrētai operācijai, operācija tiek atzīmēta kā **Operācijās nepieciešamie komponenti**.

## <a name="selecting-a-bom-and-route"></a>MK un maršruta atlasīšana
Filtrs, kas tiek lietots MK un maršrutam, tiek parādīts MK veidotāja virsrakstā. Jūs varat nomainīt filtru, izmantojot dialoglodziņu **Filtrs**. Tabulā ir aprakstīti šī dialoglodziņa lauki.

<table>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Preces dimensijas</td>
<td>Ja atlasītais galaprodukts ir preces šablons, jūs varat definēt aktīvas preces dimensijas galvenajai atlasei.<strong>Piezīme:</strong> atverot MK veidotāju precēm, kas nav preces šablons, preču dimensijas var atlasīt dialoglodziņā <strong>Filtrs</strong>.</td>
</tr>
<tr class="even">
<td>Vieta</td>
<td>Mainīt vietu, kur tiek rādīts MK koks. Noklusējuma atrašanās vieta ir pabeigtā krājuma noklusētā krājuma vieta.</td>
</tr>
<tr class="odd">
<td>Princips</td>
<td>Izvēlieties versijas parādīšanas principu, kas attiecas uz pašreizējo MK struktūru un pašreizējo maršrutu:
<ul>
<li>Kad princips iestatīts kā <strong>Aktīvs vai Atlasītie/Aktīvie</strong>, tiek atrasta šajā datumā derīga MK vai maršruta versija.</li>
<li>Kad princips ir iestatīts uz <strong>Atlasītie/Aktīvie vai Atlasītie</strong>, varat atlasīt MK versiju vai maršruta versiju, noklikšķinot uz <strong>MK</strong> &gt; <strong>MK versijas</strong> vai uz <strong>Maršruts</strong> &gt; <strong>Maršrutu versijas</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versijas datums</td>
<td>Ievadiet MK un maršruta versijas datumu. Versija tiek izmantota, lai identificētu, kuru MK versiju izmantot noteiktā datumā, kā to MK versijas iestatījumā nosaka versiju datumi.</td>
</tr>
<tr class="odd">
<td>No daudzuma</td>
<td>Filtrēt versijas, atlasot noteiktas no daudzuma. Ja iestatāt vērtību, var būt atlasītas dažādas MK un maršrutu versijas.</td>
</tr>
<tr class="even">
<td>Rādīt tikai derīgās</td>
<td>Ja šī izvēles rūtiņa ir atzīmēta, koka struktūrā tiek parādītas tikai MK rindas ar derīgiem datumiem. Varat noklikšķināt peles labo taustiņu vai veikt dubultklikšķi uz rindas, lai atvērtu lapu <strong>Labot MK rindu</strong> un skatītu MK rindas derīguma datumus.</td>
</tr>
</tbody>
</table>

Lietojot MK struktūras veidotāju, lai pārskatītu vai rediģētu MK, kas sastāv no viena vai vairākiem veidošanas līmeņiem, maršruts, kas ir saistīts ar augstākā līmeņa krājumu, parasti aptver pilnu MK hierarhiju. Lai vienkāršotu apskatu, displejā varat bloķēt augstākā līmeņa maršrutu, noklikšķinot uz **Skatīt** &gt; **Bloķēt maršrutu**. Lai atbloķētu šo maršrutu, noklikšķiniet uz **Skatīt** &gt; **Atbloķēt maršrutu**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>MK un MK rindu pievienošana un rediģēšana
Izmantojiet funkcijas **MK rindas**vai **MK**, lai modificētu MK rindas vai MK. Atlasot zaru kokā, zara tips nosaka, funkcijas, kas ir pieejamas.

| Funkcija                            | Apraksts                                                                                               | Zara tips un nosacījumi                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MK rindas &gt; Rediģēt                 | Atveriet dialoglodziņu, kur var rediģēt MK rindas atribūtus.                                             | Šī funkcija ir pieejama, ja ir atlasīts MK rindas zars.                                                                                                                                                                                                                                   |
| MK rindas &gt; Dzēst               | Dzēst MK rindu no atlasītā MK.                                                                  | Šī funkcija ir pieejama, kad MK rindas zars ir atlasīts, un MK nav slēgta rediģēšanai.                                                                                                                                                                                             |
| MK rindas &gt; Pievienot pirms rindas      | Atveriet dialoglodziņu, kurā var atlasīt preces variantu, ko iekļaut pirms atlasītās MK rindas.         | Šī funkcija ir pieejama, ja ir atlasīts MK rindas zars.                                                                                                                                                                                                                                   |
| MK rindas &gt; Pievienot komponenta MK | Atveriet dialoglodziņu, kurā var atlasīt preces variantu, ko iekļaut atlasītās MK rindas beigās.       | Šī funkcija ir pieejama, ja atlasītajam zaram ir atlasīts MK. Ja šī funkcija nav pieejama, atlasītajam krājuma variantam, iespējams, nav norādīta MK versija. Šajā gadījumā varat noklikšķināt uz **MK** &gt; **Izveidot versiju**, lai atlasītajam zaram izveidotu trūkstošo versiju. |
| MK rindas &gt; Pievienot pēc rindas       | Atveriet dialoglodziņu, kurā var atlasīt preces variantu, ko iekļaut pēc atlasītās MK rindas.          | Šī funkcija ir pieejama, ja ir atlasīts MK rindas zars.                                                                                                                                                                                                                                   |
| MK &gt; Izveidot versiju             | Izveidojiet jaunu MK versiju vai MK atlasītā zara preces variantam.                             | Šī funkcija ir pieejama, ja atlasītais MK rindas zars ir saistīts ar krājumu, kura ražošanas veids ir **MK** vai **Formula**.                                                                                                                                                  |
| BOM &gt; Aprēķins                | Atveriet dialoglodziņu, kur var palaist izmaksu vai pārdošanas cenas aprēķinu atlasītās preces variantam. | Šī funkcija ir pieejama, ja atlasītais zars ir saistīts ar MK versiju.                                                                                                                                                                                                         |
| MK &gt; Pārbaudīt                      | Apstiprināt un pārbaudīt atlasīto MK.                                                                      | Šī funkcija ir pieejama, ja atlasītais zars ir saistīts ar MK versiju.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Koka skata konfigurēšana
Noklikšķiniet uz **Iestatījumi**, lai pielāgotu informāciju, kas tiek parādīta MK veidotāja koka skatā.

| Lauku grupa | Apraksts                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MK         | Izmantojiet izvēles rūtiņas, lai atlasītu kritērijus, kas tiek parādīti koka struktūrā. MK veidotājs parāda atlasītos kritērijus abu ciļņu apakšdaļā. |
| Maršruts       | Izmantojiet izvēles rūtiņas, lai atlasītu kritērijus, kas tiek parādīti maršrutiem.                                                                                    |






