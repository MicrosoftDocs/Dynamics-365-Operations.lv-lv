---
title: "Power BI saturs Pārdošanas un ienesīguma veiktspēja"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts pārdošanas un ienesīguma veiktspējas Power BI saturā. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97c8f3d57ba1accb8d940c7edd3ddcac2146968b
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI saturs Pārdošanas un ienesīguma veiktspēja

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kas ir iekļauts **pārdošanas un ienesīguma veiktspējas** Microsoft Power BI saturā. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

**Pārdošanas un ienesīguma veiktspēja** Power BI saturs tika izveidots, lai pārdošanas vadītāji var uzraudzīt galvenos ieņēmumu, bruto peļņas un peļņas normas pārdošanas rādītājus. Tas izmanto pārdošanas transakciju datus un nodrošina gan uzņēmuma līmeņa pārdošanas rādītāju apkopošanas skatu, gan pārdošanas veiktspējas datu sadalījumu pēc debitora un preces.

Pārskati izceļ ieņēmumus un peļņas palielinājumu laika gaitā. Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tendencēm saistībā ar atsevišķiem kreditoriem un precēm. Turklāt diagrammas salīdzina dažādu preču kategoriju un debitoru grupu ieņēmumus un peļņu. Tāpēc kategorijas un reģionālie vadītāji var noteikt labākos un sliktākos rezultātus. Visbeidzot, visaptverošs pārskats atzīmē atsevišķu debitora ieņēmumus salīdzinājumā ar peļņas normu. Tāpēc kontu pārvaldniekiem ir uz datiem balstīts pamatojums tam, ko tie var izmantot, lai pielāgotu pārdošanas un mārketinga pasākumus katra debitora profilam. 

**Pārdošanas un ienesīguma veiktspējas** saturs sniedz pārdošanas daļas vadītājiem iespēju analizēt pārdošanas veiktspēju pēc tālāk minētajiem rādītājiem.

-   Līdzšinējā gada ieņēmumi (pēc debitoru grupas, atsevišķa debitora, pārdošanas kategorijas, atsevišķas preces un atrašanās vietas)
-   Ieņēmumu izmaiņas pa gadiem (pēc debitora reģiona un pārdošanas kategorijas)

Ienesīgumu var analizēt tālāk minētajos veidos.

-   Bruto peļņa un peļņas norma (pēc debitoru grupas un preču pārdošanas kategorijas)
-   Bruto peļņas izmaiņas gadu no gada
-   Debitora ienesīgums (pēc ieņēmumu un peļņas normas attiecības)

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Ja izmantojat programmatūru Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs), tad Power BI saturs **Pārdošanas un ienesīguma veiktspēja** tiek rādīts lapā **Pārdošanas un ienesīguma veiktspēja** (**Pārdošana un mārketings** > **Pieprasījumi un pārskati** > **Pārdošanas veiktspējas analīze** > **Pārdošanas un ienesīguma veiktspēja**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI saturā iekļautā metrika
**Pārdošanas un ienesīguma veiktspējas** Power BI satura pakotnē ir iekļauts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. Tālāk esošajā tabulā ir sniegts apskats par satura rādītāju vizualizēšanu.

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

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Microsoft Dynamics 365. Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai.

**Pārdošanas un ienesīguma veiktspējas** Power BI saturs ir pieejama LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Noteikti lejupielādējiet **pārdošanas un ienesīguma veiktspējas** saturu, kas attiecas uz izmantoto Dynamics 365 versiju.

> [!NOTE]
> Ja izmantojat Microsoft Dynamics 365 for Operations versiju 1611, šī Power BI satura izmantošanas priekšnosacījums ir KB 4011327. Ja esat pierakstījies LCS, tad KB varat piekļūt šeit: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
**Pārdošanas un ienesīguma veiktspējas** Power BI satura pārskata aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md). 

Šajā saturā ietvertie apkopošanas mērījumi ir apakškopa tiem apkopošanas mērījumiem, kas ir pieejami pārdošanas kubā programmatūrā Microsoft Dynamics AX 2012 un Microsoft Dynamics AX 2012 R3. Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami. Papildinformāciju skatiet emuāra ieraksta [Power BI integrācija elementu krātuvē programmatūrā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) sadaļā par apkopošanas mērījumu izvietošanas elementu krātuvē procedūru. 

Tālāk ir norādīti elementa Rēķina rindas galvenie apkopošanas mērījumi, kas tiek izmantoti kā satura pamatdati.

| Elements        | Galvenie apkopošanas mērījumi                   | Dynamics 365 datu avots                    | Lauks                                        | Apraksts                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Rēķina rindas | Ieņēmumi                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa uzskaites valūtā.            |
|               | Pārdoto preču pašizmaksa                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Izmaksu summas un korekcijas vērtības summa.    |
|               | Komisijas rindas summa — uzskaites valūta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisijas summa uzskaites valūtā. |

Tālāk esošajā tabulā ir norādīti rēķina rindas galvenie apkopošanas mērījumi, kas tiek izmantoti vairāku aprēķināto mērījumu izveidei satura datu kopā.

| Mērs           | Aprēķins                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruto peļņa      | SUM(Ieņēmumi – PPPI – Komisija –PVN (iekļauts debitora rēķina rindas summā))          |
| Bruto peļņa      | SUM(Bruto peļņa / (Ieņēmumi – PVN (iekļauts debitora rēķina rindas summā)))             |
| Pagājušā gada ieņēmumi | Pagājušā gada ieņēmumi = CALCULATE(SUM('Rēķina rindas'\[Ieņēmumi\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]) |

Tālāk minētās pārdošanas kuba galvenās dimensijas tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements           | Atribūtu piemēri                               |
|------------------|------------------------------------------------------|
| Debitori        | Debitoru grupas, Debitoru reģioni, Adrese, Nozare |
| Preces         | Preces numurs, Preces nosaukums, Krājumu grupas nosaukums       |
| Pārdošanas kategorijas | Pārdošanas kategoriju nosaukumi                                 |
| Juridiskas personas   | Juridisko personu nosaukumi                                   |
| Datumi            | Datumi                                                |

Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu. Taču varat mainīt datumu filtru pārskata filtru sadaļā. Varat mainīt arī uzņēmuma filtru.

