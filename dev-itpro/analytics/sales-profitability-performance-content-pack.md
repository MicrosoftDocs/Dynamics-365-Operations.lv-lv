---
title: "Power BI satura pakotne Pārdošanas un ienesīguma veiktspēja"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Dynamics 365 for Operations Microsoft Power BI satura pakotnē Pārdošanas un ienesīguma veiktspēja. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par satura pakotnes izveidei izmantoto datu modeli un elementiem."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 357f7071d801b13518c83170f8d0e7946dd9dede
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI satura pakotne Pārdošanas un ienesīguma veiktspēja

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kas ir iekļauts Dynamics 365 for Operations Microsoft Power BI satura pakotnē Pārdošanas un ienesīguma veiktspēja. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par satura pakotnes izveidei izmantoto datu modeli un elementiem.

<a name="overview"></a>Pārskats
--------

Šī satura pakotne ir izveidota pārdošanas daļas vadītājiem, lai viņi varētu pārraudzīt galvenos pārdošanas rādītājus, tostarp, ieņēmumu, bruto peļņas un peļņas normas rādītājus. Tā izmanto pārdošanas transakciju datus no programmatūras Dynamics 365 for Operations un nodrošina gan uzņēmuma līmeņa pārdošanas rādītāju apkopošanas skatu, gan pārdošanas veiktspējas datu sadalījumu pēc debitora un preces. Pārskatos izceļot ieņēmumus un peļņas palielinājumu laika gaitā, tos var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tendencēm attiecībā uz atsevišķiem debitoriem un precēm. Kategoriju un reģionālajiem vadītājiem ir noderīgas diagrammas, kurās ir salīdzināti dažādu preču kategoriju un debitoru grupu ieņēmumi un ienesīgums, lai noteiktu kategorijas un grupas, kas sniedz labākos un sliktākos rezultātus. Visaptverošs pārskats, kurā ir sniegts atsevišķa debitora ieņēmumu un peļņas normas attiecība, sniedz kontu pārvaldniekiem iespēju pielāgot pārdošanas un mārketinga pasākumus katra debitora attiecīgajam profilam, pamatojoties uz datiem. Satura pakotne Pārdošanas un ienesīguma veiktspēja sniedz pārdošanas daļas vadītājiem iespēju analizēt pārdošanas veiktspēju pēc tālāk minētajiem rādītājiem.

-   Līdzšinējā gada ieņēmumi (pēc debitoru grupas, atsevišķa debitora, pārdošanas kategorijas, atsevišķas preces un atrašanās vietas)
-   Ieņēmumu izmaiņas pa gadiem (pēc debitora reģiona un pārdošanas kategorijas)

Ienesīgumu var analizēt pēc tālāk minētajiem rādītājiem.

-   Bruto peļņa un peļņas norma (pēc debitoru grupas un preču pārdošanas kategorijas)
-   Bruto peļņas izmaiņas gadu no gada
-   Debitora ienesīgums (pēc ieņēmumu un peļņas normas attiecības)

## <a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
Power BI satura pakotne Pārdošanas un ienesīguma veiktspēja ir publicēta kā ieviešanas līdzeklis pakalpojumā Lifecycle Services (LCS), un tai var piekļūt programmatūrā Dynamics 365 for Operations. Papildinformāciju par to, kā palaist Power BI pārskatus, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).
**Piezīme.** Rakstā KB 4011327 ir priekšnosacījumi tā Power BI saturam. Kad esat pierakstījies pakalpojumos Lifecycle Services, tad KB varat piekļūt šeit: <a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>.

## <a name="metrics-included-in-the-content-pack"></a>Satura pakotnē iekļautie rādītāji
Satura pakotnē ir iekļauts pārskats, kas sastāv no rādītāju kopas, kurā rādītāji ir vizualizēti diagrammu, elementu un tabulu veidā. Tālāk esošajā tabulā ir sniegts apskats par satura pakotnes rādītāju vizualizēšanu.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Pārskata lapa**        | **Diagrammas**                                 | **Elementi**                                               |
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
Satura pakotnes Pārdošanas un ienesīguma veiktspēja pārskata aizpildīšanai tiek izmantoti Dynamics 365 for Operations dati. Šie dati tiek attēloti kā apkopoti mērījumi, kuri ir pieejami elementu krātuvē, kas ir analīzes veikšanai optimizēta Microsoft SQL datu bāze. Papildinformāciju par to lasiet emuārā [Power BI integrācija elementu krātuvē programmatūrā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Šajā satura pakotnē ietvertie apkopošanas mērījumi ir to apkopošanas mērījumu apakškopa, kas ir pieejami pārdošanas kubā programmatūrā Dynamics AX 2012 un AX 2012 R3. Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami. Papildinformāciju skatiet emuāra [Power BI integrācija elementu krātuvē programmatūrā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) sadaļā par to, kā padarīt apkopošanas mērījumus pieejamus elementu krātuvē. Tālāk ir norādīti elementa Rēķina rindas galvenie apkopošanas mērījumi, kas tiek izmantoti kā satura pakotnes pamatdati.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Elements**    | **Galvenie apkopošanas mērījumi**               | **Dynamics 365 for Operations datu avots** | **Lauks**                                    | **Apraksts**                          |
| Rēķina rindas | Ieņēmumi                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa uzskaites valūtā            |
|               | Pārdoto preču pašizmaksa                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Izmaksu summa + korekcija                 |
|               | Komisijas rindas summa — uzskaites valūta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisijas rindas summa uzskaites valūtā |

Tālāk esošajā tabulā ir norādīti elementa Rēķina rindas galvenie apkopošanas mērījumi, kas tiek izmantoti vairāku aprēķināto mērījumu izveidei satura pakotnes datu kopā.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Mērījums**       | **Aprēķins**                                                                                |
| Bruto peļņa      | SUM(Ieņēmumi – PPPI – Komisija –PVN (iekļauts debitora rēķina rindas summā))          |
| Bruto peļņa      | SUM(Bruto peļņa / (Ieņēmumi – PVN (iekļauts debitora rēķina rindas summā)))             |
| Pagājušā gada ieņēmumi | Pagājušā gada ieņēmumi = CALCULATE(SUM('Rēķina rindas'\[Ieņēmumi\]), SAMEPERIODLASTYEAR(Datumi\[Datums\]) |

Tālāk norādītās **pārdošanas kuba** galvenās dimensijas tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Elements**       | **Atribūtu piemēri**                           |
| Debitori        | Debitoru grupas, Debitoru reģioni, Adrese, Nozare |
| Preces         | Preces numurs, Preces nosaukums, Krājumu grupas nosaukums       |
| Pārdošanas kategorijas | Pārdošanas kategoriju nosaukumi                                 |
| Juridiskas personas   | Juridisko personu nosaukumi                                   |
| Datumi            | Datumi                                                |

Pēc noklusējuma satura pakotnē tiek radīti dati par pašreizējo kalendāro gadu, taču varat atvērt pārskata filtru sadaļu un mainīt datumu filtru. Varat mainīt arī uzņēmuma filtru.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)





