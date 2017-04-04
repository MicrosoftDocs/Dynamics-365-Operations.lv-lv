---
title: "Pārdošanas un rentabilitātes veiktspēja enerģijas BI saturu"
description: "Šajā tēmā ir aprakstīts, kādas programmas ir iekļautas komplektā Dynamics 365 operācijām - pārdošanas un rentabilitātes veiktspējas satura pakotne Microsoft Power BI. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tiek izmantoti, lai izveidotu satura pakotne."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Pārdošanas un rentabilitātes veiktspēja enerģijas BI saturu

Šajā tēmā ir aprakstīts, kādas programmas ir iekļautas komplektā Dynamics 365 operācijām - pārdošanas un rentabilitātes veiktspējas satura pakotne Microsoft Power BI. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tiek izmantoti, lai izveidotu satura pakotne.

<a name="overview"></a>Pārskats
--------

Šī satura pakotne tika izveidots pārdošanas menedžeriem, lai uzraudzītu galvenajiem pārdošanas rādītājiem ieņēmumi, bruto peļņa un peļņa. Tas izmanto pārdošanas transakciju datus no Dynamics 365 operācijām un nodrošina gan apkopojuma skatu uzņēmuma mēroga pārdošanas apjomu un pārdošanas veiktspēju sadalījumu, par klientiem un produktiem. Iezīmējot izmaiņas ieņēmumu un peļņas pieaugumu laika gaitā, atskaites var izmantot, lai brīdinājuma vadītājiem par pozitīvās un negatīvās tendences attiecībā uz atsevišķiem klientiem un produktiem. Kategoriju un reģionālos vadītājus to uzskatīs par noderīgu ir diagrammas, lai salīdzinātu ieņēmumus un rentabilitāti, dažādu produktu kategoriju un klientu grupas viens otram izcelt atpalicējiem un līderiem. Visaptverošu ziņojumu, kurā skicēta individuālu klientu ieņēmumi pret peļņas piedāvājumus kontu pārvaldnieki datu dublējumkopija attune savas pārdošanas un mārketinga centienus katra klienta attiecīgā profila pamats. Pārdošanas un rentabilitātes veiktspējas satura pakotne ļauj analizēt pārdošanas veiktspēju, pārdošanas vadītāji:

-   Ieņēmumu gada sākuma līdz konkrētajam datumam (pēc klientu grupai un atsevišķiem klientiem, tirdzniecības kategorijām, un atsevišķu produktu un ģeogrāfisko teritoriju)
-   Ieņēmumu izmaiņas, gada vairāk nekā gadu (pēc klientu reģionos un pārdošanas kategorijām)

Rentabilitāti var analizēt ar:

-   Bruto peļņa un peļņa (pēc klientu grupām un produktu pārdošanas kategorijām)
-   Bruto peļņa pārmaiņu gads vairāk nekā gadu
-   (Pret bruto peļņa | Online ieņēmumiem), klientu ienesīgumam

## <a name="accessing-the-content-pack"></a>Piekļūstot satura pakotni
Pārdošanas un rentabilitātes veiktspēja enerģijas BI satura pakotne ir publicēts kā aktīvu īstenošanu Lifecycle Services (LCS) un tai var piekļūt no Dynamics 365 operācijām. Plašāku informāciju par to, kā piekļūt un palaišanas strāvas BI ziņojumus, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Metriku, kas iekļauti satura pakotni
Satura pakotne ietver pārskatu, kas sastāv no metriku iztēlojās kā diagrammas, flīzes un tabulām. Nākamajā tabulā sniegts pārskats par vizualizāciju saturu iepakojumā.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Atskaites lapu**        | **Charts**                                 | **Flīzes**                                               |
| Ieņēmumi pēc klienta    | 10 labākos klientus pēc ieņēmumiem                | Kopējie ieņēmumi                                           |
|                        | Kopējieieņēmumi, debitoru grupai            | Ieņēmumu pieaugums YOY                                      |
|                        | Vidējā debitora ieņēmumiem pēc klientu grupas | Bruto peļņa                                            |
|                        | Ieņēmumi & bruto peļņa klientu grupa   |                                                         |
| Ieņēmumi pa produktiem     | Ieņēmumi & bruto peļņa, pārdošanas Kategorija   | Kopējais \#produktu                                    |
|                        | 10 labākos produktus pēc ieņēmumiem                 | Aktīvās un procentos no kopējā kopskaits |
|                        | Kopējie ieņēmumi pēc pārdošanas kategorijas            | Ražojumus, kas veido 80 % ieņēmumu numuru           |
| Ieņēmumi par periodu\*    | Ieņēmumi pēc mēneša                           | Ieņēmumu pieaugums YOY                                      |
|                        | Noslēdzošo ienākumu dispersija, YOY             | YOY ieņēmumu pieaugums %                                    |
|                        | Kopējā pārdošanas dispersiju pēc klientu reģiona    |                                                         |
| Ieņēmumi pēc atrašanās vietas    | Pārdošanas ieņēmumus pa pilsētu                      |                                                         |
|                        | YOY ieņēmumu pieaugums %                       |                                                         |
|                        | Pārdošanas ieņēmumi pēc reģiona                    |                                                         |
| Klientu ienesīgumam | Bruto peļņa, salīdzinot ieņēmumus ar klientu   | Bruto peļņa, bruto peļņa, YOY ieņēmumu pieaugumu          |
| Ienesīguma analīze | Ieņēmumu un bruto peļņa par mēnesi          |                                                         |
|                        | Top 15 klienti, bruto peļņas           |                                                         |
|                        | Bruto peļņa pēc mēneša, YOY                 |                                                         |

\*Ieņēmumi šī un pagājušā gadā un izaugsmi pēc tirdzniecības kategorijām.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Dinamika 365 darbības datiem tiek lietota, lai aizpildītu pārdošanas apjomu un rentabilitāti veiktspējas satura pakotnes pārskats. Tas tiek attēlots kā apkopojuma mērījumus, kas ir iestudētas entītiju krātuvē, kas ir optimizēta Analytics Microsoft SQL datu bāzi. Lasīt vairāk par to blog [Power BI integrācija ar entītiju veikalā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Apkopojuma mērījumus šo saturu iepakojumā ir apkopojuma mērījumi, kas bija pieejami programmā Dynamics AX 2012 un AX 2012 R3 pārdošanas kuba apakškopu. Posms kuba apkopojuma mērījumu vienība krātuvē ir jāpadara tās izvietojamas. Lai iegūtu papildinformāciju, skatiet procedūras aprakstu par to, kā posms apkopošanas mērījumu vienība veikalu blog [Power BI integrācija ar entītiju veikalā Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Šādus galvenos apkopojuma mērījumus rēķina rindas vienība izmanto par pamatu satura pakotnes.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Apkopojuma galvenajiem mērījumiem**               | **Datu avotu dinamiku 365 operācijām** | **Field**                                    | **Description**                          |
| Rēķina rindas | Ieņēmumi                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa uzskaites valūtā            |
|               | Pārdoto preču pašizmaksa                           | InventTrans                                     | SUMMA (CostAmountPosted + CostAmountAdjustment) | Izmaksu summa + korekcija                 |
|               | Komisijas rindas summu – norēķinu valūtu | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisijas summa norēķinu valūtu |

Tabulā ir norādīti galveno apkopoto mērījumus rēķina rindas vienība, kas tiek izmantoti, lai izveidotu vairākas aprēķinātās mērvienības iepakojuma satura dataset.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Aprēķināts kā**                                                                                |
| Bruto peļņa      | SUM (ieņēmumi-COGS-Komisija – PVN (iekļauta debitora rēķina rindas summa))          |
| Bruto peļņa      | SUMMA (bruto peļņa / (ieņēmumi - PVN (iekļauta debitora rēķina rindas summa)))             |
| Pagājušajā gadā ieņēmumi | Ieņēmumi pērn = aprēķināt (SUM ('Rēķina rindas'\[ieņēmumi\]), SAMEPERIODLASTYEAR (datumi\[datumu\]) |

Šādi galvenie izmēri norādīti **pārdošanas kuba** tiek izmantoti kā filtrus šķēle apkopojuma mērījumus, lai panāktu lielāku detalizācijas un dziļāku analītisku ieskatu.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Atribūtu piemēri**                           |
| Debitori        | Debitoru grupas, debitoru reģionu, adresi, rūpniecības |
| Preces         | Produkta numuru, preces nosaukums, preču grupas nosaukums       |
| Pārdošanas kategorijas | Pārdošanas kategoriju nosaukumus                                 |
| Juridiskas personas   | Juridisku personu vārdus                                   |
| Datumi            | Datumi                                                |

Pēc noklusējuma satura pakotne rāda datus par esošo kalendāro gadu, bet jūs varat atvērt sadaļu atskaites filtrus un mainīt datuma filtrs. Jūs varat arī mainīt uzņēmuma filtrs.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)



