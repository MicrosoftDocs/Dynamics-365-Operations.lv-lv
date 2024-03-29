---
title: Power BI satura pakotne Pārdošanas un ienesīguma veiktspēja
description: Šajā rakstā ir aprakstīts, kas ir iekļauts pārdošanas un ienesīguma veiktspējas saturā Power BI.
author: Henrikan
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.form: SalesProfitabilityPerformancePowerBI
ms.openlocfilehash: 77271ad9f5a1d7c131e1d7750de280f0c70daaa4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274665"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI satura pakotne Pārdošanas un ienesīguma veiktspēja

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kas ir iekļauts **pārdošanas un ienesīguma veiktspējas saturā** Microsoft Power BI. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Pārdošanas un ienesīguma veiktspēja** ir izveidota, lai pārdošanas vadītāji varētu uzraudzīt galvenos ieņēmumu, bruto peļņas un peļņas normas pārdošanas rādītājus. Tas izmanto pārdošanas transakciju datus un nodrošina gan uzņēmuma līmeņa pārdošanas rādītāju apkopošanas skatu, gan pārdošanas veiktspējas datu sadalījumu pēc debitora un preces.

Pārskati izceļ ieņēmumus un peļņas palielinājumu laika gaitā. Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tendencēm saistībā ar atsevišķiem kreditoriem un precēm. Turklāt diagrammas salīdzina dažādu preču kategoriju un debitoru grupu ieņēmumus un peļņu. Tāpēc kategorijas un reģionālie vadītāji var noteikt labākos un sliktākos rezultātus. Visbeidzot, visaptverošs pārskats atzīmē atsevišķus debitora ieņēmumus salīdzinājumā ar peļņas normu. Tāpēc kontu pārvaldniekiem ir uz datiem balstīts pamatojums tam, ko tie var izmantot, lai pielāgotu pārdošanas un mārketinga pasākumus katra debitora profilam.

**Pārdošanas un ienesīguma veiktspējas** saturs sniedz pārdošanas daļas vadītājiem iespēju analizēt pārdošanas veiktspēju pēc tālāk minētajiem rādītājiem.

- Līdzšinējā gada ieņēmumi (pēc debitoru grupas, atsevišķa debitora, pārdošanas kategorijas, atsevišķas preces un atrašanās vietas)
- Ieņēmumu izmaiņas pa gadiem (pēc debitora reģiona un pārdošanas kategorijas)

Ienesīgumu var analizēt tālāk minētajos veidos.

- Bruto peļņa un peļņas norma (pēc debitoru grupas un preču pārdošanas kategorijas)
- Bruto peļņas izmaiņas gadu no gada
- Debitora ienesīgums (pēc ieņēmumu un peļņas normas attiecības)

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Pārdošanas un ienesīguma veiktspēja** tiek rādīta lapā **Pārdošanas un ienesīguma veiktspēja** (**Pārdošana un mārketings** \> **Pieprasījumi un pārskati** \> **Pārdošanas apjoma analīze** \> **Pārdošanas un ienesīguma veiktspēja**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie rādītāji
Power BI satura pakotnē **Pārdošanas un ienesīguma veiktspēja** ir iekļauts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts apskats par satura rādītāju vizualizēšanu.

| Pārskata lapa            | Diagrammas                                     | Elementi                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Ieņēmumi pēc debitora    | Pirmie 10 debitori pēc ieņēmumiem                | Kopējie ieņēmumi                                           |
|                        | Ieņēmumu kopsumma pēc debitoru grupas            | Ieņēmumu palielinājums pa gadiem                                      |
|                        | Vidējie debitora ieņēmumi pēc debitoru grupas | Bruto peļņa                                            |
|                        | Ieņēmumi un bruto peļņa pēc debitoru grupas   |                                                         |
| Ieņēmumi pēc preces     | Ieņēmumi un bruto peļņa pēc pārdošanas kategorijas   | \# preču kopskaits                                    |
|                        | Pirmās 10 preces pēc ieņēmumiem                 | Aktīvo preču kopskaits un procenti no visu preču kopskaita |
|                        | Ieņēmumu kopsumma pēc pārdošanas kategorijas            | To preču skaits, kas veido 80% ieņēmumu           |
| Ieņēmumi pēc perioda\*    | Ieņēmumi pēc mēneša                           | Ieņēmumu palielinājums pa gadiem                                      |
|                        | Iepriekšējā perioda ieņēmumu novirze pa gadiem             | Ieņēmumu palielinājums pa gadiem (%)                                    |
|                        | Pārdošanas kopsummas novirze pēc debitora reģiona    |                                                         |
| Ieņēmumi pēc atrašanās vietas    | Pārdošanas ieņēmumi pēc pilsētas                      |                                                         |
|                        | Ieņēmumu palielinājums pa gadiem (%)                       |                                                         |
|                        | Pārdošanas ieņēmumi pēc reģiona                    |                                                         |
| Debitora ienesīgums | Bruto peļņas un ieņēmumu attiecība pēc debitora   | Bruto peļņa, peļņas norma, ieņēmumu palielinājums pa gadiem          |
| Ienesīguma analīze | Ieņēmumi un bruto peļņa pēc mēneša          |                                                         |
|                        | Pirmie 15 debitori pēc peļņas normas           |                                                         |
|                        | Mēneša bruto peļņa pa gadiem                 |                                                         |

\* Šī gada un pagājušā gada ieņēmumi un palielinājums pēc pārdošanas kategorijas.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Power BI satura pakotnes **Pārdošanas un ienesīguma veiktspēja** pārskata aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet rakstā [Power BI integrācija elementu krātuvē](power-bi-integration-entity-store.md).

Šā satura apkopotie mērījumi ir Microsoft Dynamics AX to kopējo mērījumu apakškopa, kas bija pieejami pārdošanas kubā 2012. un Microsoft Dynamics AX 2012 R3. Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami. Papildinformāciju skatiet emuāra ziņas [Power BI integrācija elementu krātuvē programmā Dynamics](/archive/blogs/dynamicsaxbi/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update) sadaļā par procedūru apkopošanas mērījumu sagatavošanai elementu krātuvē.

Tālāk ir norādīti elementa Rēķina rindas galvenie apkopošanas mērījumi, kas tiek izmantoti kā satura pamatdati.

| Elements        | Galvenie apkopošanas mērījumi                   | Dynamics 365 datu avots | Lauks                                        | Apraksts                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Rēķina rindas | Ieņēmumi                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Summa uzskaites valūtā.            |
|               | Pārdoto preču pašizmaksa                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | Izmaksu summas un korekcijas vērtības summa.    |
|               | Komisijas rindas summa — uzskaites valūta | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Komisijas summa uzskaites valūtā. |

Tālāk esošajā tabulā ir norādīti rēķina rindas galvenie apkopošanas mērījumi, kas tiek izmantoti vairāku aprēķināto mērījumu izveidei satura datu kopā.

| Mērs           | Aprēķins                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruto peļņa      | SUM(Ieņēmumi – PPPI – Komisija –PVN (iekļauts debitora rēķina rindas summā))          |
| Bruto peļņa      | SUM(Bruto peļņa / (Ieņēmumi – PVN (iekļauts debitora rēķina rindas summā)))             |
| Pagājušā gada ieņēmumi | Pagājušā gada ieņēmumi = CALCULATE(SUM('Rēķina rindas'\[Ieņēmumi\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]) |

Tālāk minētās galvenās dimensijas pārdošanas kubā tiek izmantotas kā filtri, lai sadalītu apkopotos mērījumus, tādējādi var sasniegt lielāku granularitāti un iegūt plašākus analītiskos priekšstatus.

| Elements           | Atribūtu piemēri                               |
|------------------|------------------------------------------------------|
| Debitori        | Debitoru grupas, Debitoru reģioni, Adrese, Nozare |
| Preces         | Preces numurs, Preces nosaukums, Krājumu grupas nosaukums       |
| Pārdošanas kategorijas | Pārdošanas kategoriju nosaukumi                                 |
| Juridiskas personas   | Juridisko personu nosaukumi                                   |
| Datumi            | Datumi                                                |

Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu. Taču varat mainīt datumu filtru pārskata filtru sadaļā. Varat mainīt arī uzņēmuma filtru.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
