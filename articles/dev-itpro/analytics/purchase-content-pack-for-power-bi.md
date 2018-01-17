---
title: "Power BI satura pakotne Pirkumu tēriņu analīze"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI satura pirkumu tēriņu analīzē. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti saturā, un ir sniegta informācija par satura izveidei izmantoto datu modeli un elementiem."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 07b6f433a8355d7f9ed6dce8e26f78d38a86a713
ms.contentlocale: lv-lv
ms.lasthandoff: 12/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI satura pakotne Pirkumu tēriņu analīze

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts Microsoft Power BI satura **pirkumu tēriņu analīzē**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

**Pirkumu tēriņu analīzes** Power BI saturs tika veidots, lai iepirkumu nodaļas vadītājiem un vadītājiem, kuri ir atbildīgi par budžetu, palīdzētu sekot pirkuma tēriņiem. Vadītāji var analizēt pirkumu tēriņus šādos veidos:

-   Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)
-   Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)

Saturam tiek izmantoti pirkumu transakciju dati, un tas nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces. Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā. Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm. Turklāt diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām. Tādēļ kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Power BI satura pakotne **Pirkšanas tēriņu analīze** tiek rādīta lapā **Pirkšanas un tēriņu rādītāju analīze** (**Sagāde un avoti** > **Pieprasījumi un pārskati** > **Pirkšanas rādītāju analīze** > **Pirkšanas un tēriņu rādītāju analīze**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI saturā iekļautā metrika
**Pirkumu tēriņu analīzes** Power BI satura pakotnē ir iekļauts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. Zemāk norādītajā tabulā ir sniegts pārskats par vizualizācijām.

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

\* Šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas

## <a name="data-model-and-entities"></a>Datu modelis un elementi
**Pirkumu tēriņu analīzes** Power BI satura pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md).

Šajā saturā ietvertie apkopošanas mērījumi ir apakškopa tiem apkopošanas mērījumiem, kas ir pieejami pirkšanas kubā programmatūrā Microsoft Dynamics AX 2012 un Microsoft Dynamics AX 2012 R3. Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami. Papildinformāciju skatiet emuāra ieraksta [Pārskats par Power BI integrāciju, izmantojot elementu krātuvi](power-bi-integration-entity-store.md) sadaļā par apkopošanas mērījumu izvietošanas elementu krātuvē procedūru. Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pamatdati.

| Elements        | Galvenie apkopošanas mērījumi | Datu avots                                 | Lauks              | Apraksts                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Rēķina rindas | Pirkšana                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa uzskaites valūtā. |

Tālāk esošajā tabulā ir norādīti galvenie satura mērījumi, kas tiek aprēķināti no elementa Rēķina rindas.

| Mērs               | Aprēķins                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Pašreizējā gada pirkumi | Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])                                            |
| Pagājušā gada pirkumi    | Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\])) |
| Pirkumu palielinājums pa gadiem   | Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]                            |

Tālāk norādītās galvenās dimensijas saturam tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements                 | Atribūtu piemēri                                |
|------------------------|-------------------------------------------------------|
| Kreditori                | Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums |
| Preces               | Preces numurs, Preces nosaukums, Krājumu grupas nosaukums        |
| Sagādes kategorijas | Sagādes kategorija, Sagādes kategoriju nosaukumi      |
| Juridiskas personas         | Juridiskās personas nosaukums                                     |
| Datumi                  | Datumi, Gada nobīde                                    |

Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu. Taču varat mainīt datumu filtru pārskata filtru sadaļā. Varat mainīt arī uzņēmuma filtru.

