---
title: "Power BI satura pakotne Pirkumu tēriņu analīze"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē Pirkumu tēriņu analīze. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par satura pakotnes izveidei izmantoto datu modeli un elementiem."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI satura pakotne Pirkumu tēriņu analīze

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura pakotnē Pirkumu tēriņu analīze. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par satura pakotnes izveidei izmantoto datu modeli un elementiem.

<a name="overview"></a>Pārskats
--------

Microsoft Power BI satura pakotne Pirkumu tēriņu analīze ir izveidota iepirkumu nodaļas vadītāju un par budžetu atbildīgo vadītāju vajadzībām. Tā ir izstrādāta tā, lai palīdzētu viņiem sekot līdzi pirkumu tēriņiem. Tā izmanto pirkumu transakciju datus no programmatūras Microsoft Dynamics 365 for Operations un nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces. Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā. Tāpēc tos var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm. Diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām. Kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas. Satura pakotne sniedz iepirkumu daļas vadītājiem un par budžetu atbildīgajiem vadītājiem analizēt pirkumu tēriņus tālāk norādītajos veidos.

-   Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)
-   Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)

## <a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
Satura pakotne Pirkumu tēriņu analīze ir publicēta kā ieviešanas līdzeklis pakalpojumā Microsoft Dynamics Lifecycle Services (LCS), un tai var piekļūt programmatūrā Microsoft Dynamics 365 for Operations. Papildinformāciju par to, kā piekļūt Power BI pārskatiem, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie rādītāji
Satura pakotnē Pirkumu tēriņu analīze ir iekļauts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts apskats par satura pakotnes rādītāju vizualizēšanu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Pārskata lapa</th>
<th>Diagrammas</th>
<th>Elementi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pirkumi pēc kreditora</td>
<td><ul>
<li>Pirmie 10 kreditori pēc pirkšanas (joslu grēdu diagramma)</li>
<li>Pirkumu kopsumma pēc kreditoru grupas/valsts/nosaukuma (sektoru diagramma)</li>
<li>Pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</li>
<li>Vidējie pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)</li>
</ul></td>
<td><ul>
<li>Kopējā pirkšana</li>
<li>Pirkumu palielinājums pa gadiem</li>
<li>Kreditoru kopskaits</li>
<li>Aktīvo kreditoru kopskaits</li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkumi pēc preces</td>
<td><ul>
<li>Pirkumi pēc sagādes kategorijas/preces nosaukuma (stabiņu diagramma)</li>
<li>Pirkumu kopsumma pēc sagādes kategorijas/preces nosaukuma (sektoru diagramma)</li>
<li>Pirmās 10 preces pēc pirkšanas (joslu grēdu diagramma)</li>
</ul></td>
<td><ul>
<li>Preču kopskaits</li>
<li>Aktīvo preču kopskaits procentos no preču kopskaita</li>
<li>To preču skaits, kas veido 80% pirkumu</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pirkumi pēc perioda*</td>
<td><ul>
<li>Pirkumi pēc mēneša/dienas (stabiņu diagramma)</li>
<li>Apkopotā pirkumu novirze pa gadiem (ūdenskrituma diagramma)</li>
<li>Pirkumu kopsummas palielinājums pa gadiem (stabiņu diagramma)</li>
<li>Sagādes izraksts (matrica)</li>
</ul></td>
<td><ul>
<li>Pirkumu palielinājums pa gadiem</li>
<li>Pirkumu palielinājums (%)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkumi pēc kreditora atrašanās vietas</td>
<td><ul>
<li>Pirkumi pēc pilsētas</li>
<li>Pirkumu palielinājums pa gadiem (%)</li>
<li>Pirkumi pēc valsts</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Pirkumu tēriņu analīze pēc laika</td>
<td><ul>
<li>Pašreizējā gada pirkumi pēc mēneša/dienas (līniju diagramma)</li>
<li>Pašreizējā un pagājušā gada pirkumi (līniju un stabiņu diagramma)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Pirkumu tēriņu analīze pēc kreditora</td>
<td><ul>
<li>Pirmo 10 kreditoru pirkumi procentos (%) no pirkumiem (piltuves diagramma)</li>
<li>Pirmie 10 kreditori ar palielinātiem tēriņiem pa gadiem</li>
<li>Pirmie 10 kreditori ar samazinātiem tēriņiem pa gadiem</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas

## <a name="data-model-and-entities"></a>Datu modelis un elementi
Satura pakotnes Pirkumu tēriņu analīze pārskata izveidei tiek izmantoti Dynamics 365 for Operations dati. Šie dati tiek attēloti kā apkopoti mērījumi, kuri pa posmiem tiek izveidoti elementu krātuvē, kas ir analīzes veikšanai optimizēta Microsoft SQL datu bāze. Papildinformāciju par elementu krātuvi skatiet emuāra ierakstā [Power BI integrācija elementu krātuvē programmatūrā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Šajā satura pakotnē ietvertie apkopošanas mērījumi ir to apkopošanas mērījumu apakškopa, kas ir pieejami pirkšanas kubā programmatūrā Microsoft Dynamics AX 2012 un Microsoft Dynamics 365 for Operations 2012 R3. Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami. Papildinformāciju skatiet emuāra ieraksta [Power BI integrācija elementu krātuvē programmatūrā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) sadaļā par apkopošanas mērījumu izvietošanas elementu krātuvē procedūru. Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pakotnes pamatdati.

| Elements        | Galvenie apkopošanas mērījumi | Datu avots programmai Dynamics 365 for Operations | Lauks              | apraksts                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Rēķina rindas | Pirkšana                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa uzskaites valūtā |

Tālāk esošajā tabulā ir norādīti galvenie mērījumi, kas tiek aprēķināti satura pakotnē no elementa Rēķina rindas.

| Mērs               | Aprēķins                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Pašreizējā gada pirkumi | Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])                                            |
| Pagājušā gada pirkumi    | Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\])) |
| Pirkumu palielinājums pa gadiem   | Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]                            |

Tālāk norādītās galvenās dimensijas satura pakotnē tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements                 | Atribūtu piemēri                                |
|------------------------|-------------------------------------------------------|
| Kreditori                | Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums |
| Preces               | Preces numurs, Preces nosaukums, Krājumu grupas nosaukums        |
| Sagādes kategorijas | Sagādes kategorija, Sagādes kategoriju nosaukumi      |
| Juridiskas personas         | Juridiskās personas nosaukums                                     |
| Datumi                  | Datumi, Gada nobīde                                    |

Pēc noklusējuma satura pakotne nodrošina pašreizējā kalendārā gada datu rādīšanu. Taču varat mainīt datumu filtru pārskata filtru sadaļā. Varat mainīt arī uzņēmuma filtru.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)



