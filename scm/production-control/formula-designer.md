---
title: "Formulas veidotājs"
description: "Šajā tēmā ir paskaidrots, kā izmantot formulas veidotāju, lai analizētu un uzturētu formulas koka skatā."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 84322bb3f02d236843bebc24c4c5eccdd4d9f2bf
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="formula-designer"></a>Formulas veidotājs

[!include[banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā izmantot formulas veidotāju, lai analizētu un uzturētu formulas koka skatā.

Kad lapu **Formulas veidotājs** atverat no lapas **Izlaistās preces**, tad kreisajā rūtī koka struktūrā tiek rādīts izlaistās preces līdzproduktu saraksts un komponentu hierarhija. Šī struktūra tiek atvasināta no atlasītajam krājumam un tā komponentiem aktīvās un apstiprinātas formulu hierarhijas, krājuma noklusējuma pasūtījuma vietai un faktiskajam datumam.

Noklikšķiniet uz **Iestatīšana**, lai atlasītu dažādas konfigurācijas un norādītu, kādai informācijai ir jābūt redzamai koka rindās.

Noklikšķiniet uz **Filtrs**, lai mainītu sākotnējo atlasi skatījumā. Ja rādīšanas principu iestatāt uz **Atlasītie/Aktīvie** vai **Atlasītie**, tad varat atlasīt atsevišķas formulu vai maršrutu versijas, ko izmantot šajā skatā. Varat atlasīt neapstiprinātas un neaktīvas formulu versijas, ko rādīt vai uzturēt formulu veidotājā.  

> [!NOTE]
> Ja lapu **Formulu veidotājs** atverat no saraksta lapas **Materiālu komplekts**, tajā netiek rādīta informācija par maršrutu. Pašlaik formulas vai maršruta versijas atlase attiecas uz visām formulu veidotāja instancēm.  

Nākamajās sadaļās ir aprakstīta funkcionalitāte, kas ir pieejama MK veidotājā.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Analizēt formulas struktūru, izmantojot formulu veidotāju
Formulu veidotājam ir divas tālāk norādītās sadaļas.

-   Formulas struktūras koka struktūras skats.
-   Detalizētas informācijas sadaļa, kurā sniegta detalizēta informācija par atlasītajiem datiem. Atlasot zaru koka skatā, FastTabs tiek atjauninātas detalizētas informācijas sadaļā, pamatojoties uz šo mezglu:
    -   **Detalizēta informācija par formulas rindu** — skatiet detalizētu informāciju par koka skatā atlasīto formulas rindu.
    -   **Krājuma dati** — skatiet detalizētu informāciju par galveno krājumu vai krājumiem, kas tiek izmantoti atlasītajā zarā. Varat noklikšķināt uz **Labot izlaisto preci**, lai uzturētu atlasīto krājumu.
    -   **Formula** — skatiet ar atlasīto zaru saistītās formulas virsrakstu.
    -   **Maršruts** — skatiet ar atlasīto zaru saistītā maršruta virsrakstu.
    -   **Maršruta operācijas** — skatiet maršruta operāciju priekšskatījumu. Kad tiek atlasīta materiālu komplekta (MK) rinda, kas ir piešķirta konkrētai operācijai, šī operācija tiek atzīmēta kā **Operācijās nepieciešamie komponenti**.

## <a name="select-a-formula-and-route"></a>Atlasīt formulu un maršrutu
Formulai un maršrutam lietotais filtrs tiek rādīts formulu veidotāja virsrakstā. Jūs varat nomainīt filtru, izmantojot dialoglodziņu **Filtrs**. Tabulā ir aprakstīti šī dialoglodziņa lauki.

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
<td>Ja atlasītā pabeigtā prece ir preces šablons, tad aktīvās preces dimensijas varat definēt galvenajai atlasei. Ņemiet vērā — ja formulu veidotāju atverat precei, kas nav preces šablons, tad dialoglodziņā <strong>Filtrs</strong> nevar atlasīt nekādas preču dimensijas.</p></td>
</tr>
<tr class="even">
<td>Atrašanās vieta</td>
<td>Mainiet vietu, kam tiek rādīts komponentu koks. Noklusējuma atrašanās vieta ir pabeigtā krājuma noklusētā krājuma vieta.</td>
</tr>
<tr class="odd">
<td>Princips</td>
<td><p>Atlasiet versijas parādīšanas principu, kas attiecas uz pašreizējo formulu struktūru un pašreizējo maršrutu.</p>
<ul>
<li>Kad princips tiek iestatīts kā <strong>Aktīvie</strong> vai <strong>Atlasītie/Aktīvie</strong>, tiek atrasta šim datumam derīgā formulas vai maršruta versija.</li>
<li>Kad princips tiek iestatīts kā <strong>Atlasītie/Aktīvie</strong> vai <strong>Atlasītie</strong>, varat atlasīt formulas versiju vai maršruta versiju, noklikšķinot uz <strong>Formula</strong> &gt; <strong>Formulas versijas</strong> vai uz <strong>Maršruts</strong> &gt; <strong>Maršrutu versijas</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versijas datums</td>
<td>Ievadiet formulas un maršruta versijas datumu. Versija norāda, kura formulas versija tiek izmantota noteiktā datumā, ņemot vērā versiju datumus formulas versijas iestatīšanā.</td>
</tr>
<tr class="odd">
<td>No daudzuma</td>
<td>Filtrējiet versijas, atlasot noteiktu daudzumu “no”. Ja iestatāt kādu vērtību, var tikt atlasītas citādas formulu un maršrutu versijas.</td>
</tr>
<tr class="even">
<td>Rādīt tikai derīgās</td>
<td>Ja atzīmējat šo izvēles rūtiņu, tad koka struktūrā tiek rādītas tikai tādas formulu rindas, kurām ir derīgi datumi. Ar peles labo pogu noklikšķiniet uz formulas rindas, lai atvērtu lapu <strong>Rediģēt formulas rindu</strong>, kur varat redzēt formulas rindas derīguma datumus.</td>
</tr>
</tbody>
</table>

Kad formulu veidotāju lietojat, lai pārskatītu vai rediģētu formulas, kas sastāv no viena vai vairākiem fantomu līmeņiem, tad maršruts, kas ir saistīts ar augstākā līmeņa krājumu, parasti aptver visu formulu hierarhiju. Lai vienkāršotu apskatu, displejā varat bloķēt augstākā līmeņa maršrutu, noklikšķinot uz **Skatīt** &gt; **Bloķēt maršrutu**. Lai atbloķētu šo maršrutu, noklikšķiniet uz **Skatīt** &gt; **Atbloķēt maršrutu**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Pievienot un rediģēt formulas un formulu rindas
Lai modificētu formulu rindas vai formulas, izmantojiet funkcijas **MK rindas** vai **Formula**. Kad kokā atlasāt kādu zaru, šī zara tips nosaka, kādas funkcijas ir pieejamas.

| Funkcija                            | Apraksts                                                                                               | Zara tips un nosacījumi |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| MK rindas &gt; Rediģēt                 | Atveriet dialoglodziņu, kur varat rediģēt formulas rindas atribūtus.                                         | Šī funkcija ir pieejama, ja ir atlasīts formulas rindas zars. |
| MK rindas &gt; Dzēst               | Dzēst formulas rindu no atlasītās formulas.                                                          | Šī funkcija ir pieejama, kad ir atlasīts kāds formulas rindas zars un šī formula nav slēgta rediģēšanai. |
| MK rindas &gt; Pievienot pirms rindas      | Atveriet dialoglodziņu, kur varat atlasīt preces variantu, kuru iekļaut pirms atlasītās formulas rindas.     | Šī funkcija ir pieejama, ja ir atlasīts formulas rindas zars. |
| MK rindas &gt; Pievienot komponenta MK | Atveriet dialoglodziņu, kur varat atlasīt preces variantu, kuru iekļaut atlasītās formulas rindas beigās.   | Šī funkcija ir pieejama, ja atlasītajam zaram ir atlasīta formula. Ja šī funkcija nav pieejama, tad atlasītajam krājuma variantam, iespējams, trūkst formulas versijas. Šajā gadījumā varat noklikšķināt uz **Formula** &gt; **Izveidot versiju**, lai atlasītajam zaram izveidotu trūkstošo versiju. |
| MK rindas &gt; Pievienot pēc rindas       | Atveriet dialoglodziņu, kur varat atlasīt preces variantu, kuru iekļaut pēc atlasītās formulas rindas.      | Šī funkcija ir pieejama, ja ir atlasīts formulas rindas zars. |
| Formula &gt; Izveidot versiju         | Izveidojiet jaunu formulas versiju vai formulu atlasītā zara preces variantam.                     | Šī funkcija ir pieejama, ja atlasītais formulas rindas zars ir saistīts ar krājumu, kura ražošanas tips ir **MK** vai **Formula**. |
| Formula &gt; Aprēķins            | Atveriet dialoglodziņu, kur var palaist izmaksu vai pārdošanas cenas aprēķinu atlasītās preces variantam. | Šī funkcija ir pieejama, ja atlasītais zars ir saistīts ar kādu formulas versiju. |
| Formula &gt; Pārbaudīt                  | Validējiet un pārbaudiet atlasīto formulu.                                                                  | Šī funkcija ir pieejama, ja atlasītais zars ir saistīts ar kādu formulas versiju. |

## <a name="configuring-the-tree-view"></a>Koka skata konfigurēšana
Noklikšķiniet uz **Iestatīšana**, lai pielāgotu formulu veidotāja koka skatā rādīto informāciju.

| Lauku grupa | Apraksts |
|-------------|-------------|
| MK         | Izmantojiet izvēles rūtiņas, lai atlasītu kritērijus, kas tiek parādīti koka struktūrā. Formulu veidotājs abu ciļņu apakšdaļā rāda atlasītos kritērijus. |
| Maršruts       | Izmantojiet izvēles rūtiņas, lai atlasītu kritērijus, kas tiek parādīti maršrutiem. |

