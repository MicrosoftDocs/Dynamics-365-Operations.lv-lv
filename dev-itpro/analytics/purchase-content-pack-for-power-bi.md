---
title: "Iepirkuma pavadīt Power BI satura analīze"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauta pirkšanas pavadīt analīzes satura pakotne Microsoft Power BI. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tiek izmantoti, lai izveidotu satura pakotne."
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

# <a name="purchase-spend-analysis-power-bi-content"></a>Iepirkuma pavadīt Power BI satura analīze

Šajā tēmā ir aprakstīts, kas ir iekļauta pirkšanas pavadīt analīzes satura pakotne Microsoft Power BI. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tiek izmantoti, lai izveidotu satura pakotne.

<a name="overview"></a>Pārskats
--------

Iegādei tērē satura pakotne Microsoft Power BI tika izveidots iepirkumu vadītāji un menedžeri, kuri ir atbildīgi par budžeta analīzi. Tā ir izstrādāta, lai palīdzētu viņiem saglabāt acu par iegādes izdevumus. To izmanto pirkšanas transakciju datus no Microsoft Dynamics 365 operācijām un nodrošina gan apkopojuma skatu figūriņa uzņēmuma pirkšanu un pirkšanas izdevumus par kreditoru un produktu iedalījums. Atskaites Marķēt izmaiņas pirkšanas izdevumi laika gaitā. Tāpēc tos var izmantot, lai brīdinājuma vadītājiem par pozitīvo un negatīvo izdevumu tendences atsevišķiem kreditoriem un produktiem. Diagrammās redzama iegādes izdevumus dažādu iepirkumu kategorijas un kreditoru grupām. Kategoriju un reģionālajiem vadītājiem noderīgi izmantot šīm kartēm, kas palīdzēs identificēt izmaiņas izdevumu darbību. Satura pakotne pieņemsim pirkšanas vadītāji un menedžeri, kuri ir atbildīgi par budžetu analizēt iegādes izdevumus šādos veidos:

-   Gada sākuma līdz konkrētajam datumam var iegādāties (kreditoru grupai un atsevišķiem kreditoriem, iepirkuma kategorija un atsevišķu produktu un piegādātāju atrašanās vietu)
-   Gadā-vairāk nekā gadu iepirkuma pārmaiņas (pēc kreditoru grupu un iepirkumu kategorijas)

## <a name="accessing-the-content-pack"></a>Piekļūstot satura pakotni
Pirkšanas pavadīt satura pakotne ir publicēts kā aktīvu īstenošanu programmā Microsoft Dynamics Lifecycle Services (LCS) un tai var piekļūt no Microsoft Dynamics 365 operāciju analīze. Lai iegūtu papildinformāciju par piekļuvi un varas BI atvērtās atskaites, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metriku, kas ir iekļautas satura pakotni
Iegādei tērē analīzes satura pakotne ietver atskaites, kas sastāv no metriku kopa. Šiem rādītājiem ir iztēlojās kā diagrammas, flīzes un tabulām. Nākamajā tabulā sniegts pārskats par vizualizācijas saturu iepakojumā.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atskaites lapu</th>
<th>Diagrammas</th>
<th>Flīzes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pēc kreditora pirkšanas</td>
<td><ul>
<li>Top 10 piegādātājiem, iepirkuma (joslu grēdu diagrammā)</li>
<li>Pirkšanas pasūtījumus pa piegādātājiem kopējā grupas / valsts / nosaukums (sektoru diagramma)</li>
<li>Pirkšanas pasūtījumus pa piegādātājiem grupas / valsts / nosaukums (stabiņu diagramma)</li>
<li>Vidējā pirkšanas pasūtījumus pa piegādātājiem grupas / valsts / nosaukums (stabiņu diagramma)</li>
</ul></td>
<td><ul>
<li>Kopējā pirkšana</li>
<li>YOY iepirkuma pieaugums</li>
<li>Kopējais # kreditoriem</li>
<li>Kopējo aktīvu pārdevējiem #</li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkuma, preču</td>
<td><ul>
<li>Iepirkuma kategorija var iegādāties / produkta nosaukums (stabiņu diagramma)</li>
<li>Pirkšanas kopsumma pēc iepirkuma kategorija / produkta nosaukums (sektoru diagramma)</li>
<li>10 labākos produktus pēc pirkuma (joslu grēdu diagrammā)</li>
</ul></td>
<td><ul>
<li>Kopējā produktu #</li>
<li>Kopējo aktīvu produktu procentuālā daļa kopējā produktu #</li>
<li>Ražojumus, kas veido 80 % pirkumu skaits</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pirkuma, periods *</td>
<td><ul>
<li>Pirkumu mēnesis / diena (stabiņu diagramma)</li>
<li>Kumulatīvais pirkšanas YOY dispersijas (ūdenskrituma diagramma)</li>
<li>Kopējos pirkšanas YOY pieaugumu (stabiņu diagramma)</li>
<li>Iepirkumu paziņojumu (matrica)</li>
</ul></td>
<td><ul>
<li>YOY iepirkuma pieaugums</li>
<li>YOY iepirkuma pieaugums %</li>
</ul></td>
</tr>
<tr class="even">
<td>Iegādāties pēc pārdevēja atrašanās vietas</td>
<td><ul>
<li>Pirkuma, pilsētas</li>
<li>Iepirkuma YOY pieaugumu %</li>
<li>Valsts iepirkuma</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Iepirkuma pavadīt analīze pēc laika</td>
<td><ul>
<li>Pirkuma kārtējā gadā pa mēnešiem / dienā (līniju diagramma)</li>
<li>Iepirkuma pašreizējā un pērn (rindu un kolonnu diagramma)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Iepirkuma pavadīt analīze pēc kreditora</td>
<td><ul>
<li>Top 10 kreditora pirkšanas % pirkuma (piltuve)</li>
<li>Top 10 kreditoriem ar lielāku tēriņu YOY</li>
<li>Top 10 kreditoriem ar mazāku izdevumu YOY</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Šogad un pērn pirkšanu un izaugsmi pēc iepirkumu kategorijas

## <a name="data-model-and-entities"></a>Datu modelis un subjekti
Dinamika 365 operācijām, kuras dati tiek izmantoti pirkšanas pārskatam pavadīt satura analīzes pakotnei. Šie dati tiek attēlots kā apkopojuma mērījumus, kas ir iestudētas entītiju krātuvē, kas ir Microsoft SQL datu bāzi, kas ir optimizēta analytics. Plašāku informāciju par entītiju veikalu, skatiet [Power BI integrācija ar entītiju veikalā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog post. Apkopojuma mērījumus šo saturu iepakojumā ir apkopojuma mērījumus, kas bija pieejami pirkšanas kubā Microsoft Dynamics AX 2012 un Microsoft Dynamics 365 operācijas 2012 R3 apakškopu. Posms kuba apkopojuma mērījumu vienība veikalā, ir jāpadara tās izvietojamas. Plašāku informāciju skatiet procedūru sagatavošanas kopējais mērījumu vienība veikalā [Power BI integrācija ar entītiju veikalā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog post. Šādus galvenos apkopojuma mērījumus ir pieejami tieši no rēķina rindas vienība un tiek izmantoti par pamatu satura pakotne.

| Elements        | Apkopojuma galvenajiem mērījumiem | Datu avotu dinamiku 365 operācijām | Lauks              | apraksts                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Rēķina rindas | Pirkšana                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa uzskaites valūtā |

Tabulā ir norādīts atslēgas mērījumiem aprēķinātās satura pakotni no rēķina rindas vienība.

| Mērs               | Aprēķins                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Iepirkuma pašreizējā gadā | Pirkuma kārtējā gada = SUM ('Rēķina rindas'\[pirkuma\])                                            |
| Pagājušajā gadā iepirkuma    | Pirkšanas pagājušajā gadā = aprēķināt (SUM ('Rēķina rindas'\[pirkšanas\]), SAMEPERIODLASTYEAR (datumi\[dienas\])) |
| YOY iepirkuma pieaugums   | YOY iepirkuma pieaugums = \[iegādāties kārtējam gadam\] - \[iegādāties pagājušajā gadā\]                            |

Šādas galvenās dimensijas saturu iepakojumā tiek izmantoti kā filtrus šķēle apkopojuma mērījumus, tāpēc, ka jūs varat sasniegt lielāku detalizācijas un analītisko dziļākai izpratnei.

| Elements                 | Atribūtu piemēri                                |
|------------------------|-------------------------------------------------------|
| Kreditori                | Kreditoru grupas, kreditoru valstī vai reģionos, kreditora nosaukums |
| Preces               | Produkta numuru, preces nosaukums, preču grupas nosaukums        |
| Sagādes kategorijas | Iepirkuma kategorija, Sagādes kategoriju nosaukumus      |
| Juridiskas personas         | Juridiskās personas nosaukums                                     |
| Datumi                  | Datumus, gada nobīde                                    |

Pēc noklusējuma satura pakotne rāda datus kārtējam kalendāra gadam. Tomēr jūs varat mainīt datuma filtrs sadaļā atskaites filtrus. Jūs varat arī mainīt uzņēmuma filtrs.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)



