---
title: "Power BI saturs Izmaksu pārvaldība"
description: "Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI saturā Izmaksu pārvaldība. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f509852f15b9518d0a01be1f89d4f07c76caf341
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="cost-management-power-bi-content"></a>Power BI saturs Izmaksu pārvaldība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kas ir iekļauts Power BI saturā Izmaksu pārvaldība. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

# <a name="overview"></a>Pārskats

Microsoft Power BI saturs **Izmaksu pārvaldība** ir paredzēts krājumu grāmatvežiem vai organizācijas darbiniekiem, kuri atbild par krājumiem. Power BI saturā **Izmaksu pārvaldība** ir sniegti pārvaldības ieskati par krājumiem un nepabeigto darbu (NP) krājumiem, kā arī par izmaksu plūsmu caur tiem pēc kategorijas laika gaitā. Šo informāciju var arī izmantot kā finanšu pārskata detalizētu papildinājumu.

## <a name="key-measures"></a>Galvenie mēri

+ Sākuma bilance
+ Beigu bilance
+ Neto apgrozījums
+ Neto izmaiņas %
+ Vecumstruktūras

## <a name="key-performance-indicators"></a>Izpildes pamatrādītājs
+ Krājumu apgrozījums
+ Krājumu precizitāte

Vienumam CostAggregatedCostStatementEntryEntity primārais datu avots ir tabula CostStatementCache. Šo tabulu pārvalda datu kopas kešatmiņas struktūra. Pēc noklusējuma šī tabula tiek atjaunināta ik pēc 24 stundām, bet datu kešatmiņas konfigurācijā varat iespējot manuālu atjaunināšanu. Pēc tam manuālu atjaunināšanu varat veikt darbvietā **Izmaksu pārvaldība** vai **Izmaksu analīze**. Pēc CostStatementCache atjaunināšanas jums ir jāatjaunina OData savienojums ar Power BI.com, lai šajā vietnē būtu redzami atjauninātie dati. Novirzes (pirkšanas, ražošanas) mēri šajā Power BI saturā attiecas tikai uz vienumiem, kuru vērtība ir noteikta ar standarta izmaksu krājumu metodi. Ražošanas novirze tiek aprēķināta kā aktīvo izmaksu un realizēto izmaksu starpība. Ražošanas novirze tiek aprēķināta, kad ražošanas pasūtījuma statuss ir **Pabeigts**. Papildinformāciju par ražošanas novirzes tipiem un katra tipa aprēķināšanu skatiet rakstā [Par noviržu analizēšanu pabeigtam ražošanas pasūtījumam](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Power BI saturs **Izmaksu pārvaldība** ir pieejams vietnē PowerBI.com. Papildinformāciju par to, kā pievienot un lejupielādēt jūsu Microsoft Dynamics 365 for Finance and Operations datus, skatiet rakstā [Piekļuve Power BI saturam vietnē PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI saturā iekļautā metrika
Saturā ietilpst pārskatu lapu komplekts. Katra lapa sastāv no rādītāju kopas, kuri ir vizualizēti kā diagrammas, elementi un tabulas. Nākamajā tabulā ir sniegts apskats par vizualizācijām Power BI saturā **Izmaksu pārvaldība**.

| Pārskata lapa | Diagrammas | Virsraksti |
|---|---|---|
|Krājumi vispār (noklusējums pēc pašreizējā perioda) |Precizitāte |Krājumu mēri:<br>Krājumu beigu bilance<br>Krājumu neto izmaiņas<br>Krājumu neto izmaiņas %<br>|
| |Krājumu apgrozījums | |
| |Krājumu beigu bilance pēc resursu grupas | |
| |Krājumu neto izmaiņas pēc kategorijas nosaukuma 1. līmeņa un kategorijas nosaukuma 2. līmeņa| |
| |Pirkšanas novirzes pēc resursu grupas un kategorijas nosaukuma 3. līmeņa | |
|Krājumi pēc vietas (noklusējums pēc pašreizējā perioda) |Krājumu beigu bilance pēc vietas nosaukuma un resursu grupas | |
| |Krājumu apgrozījums pēc vietas nosaukuma un resursu grupas | |
| |Krājumu beigu bilance pēc pilsētas un resursu grupas | |
|Krājumi pēc resursu grupas (noklusējums pēc pašreizējā perioda) |Krājumu mēri | |
| |Krājumu precizitāte pēc summas pēc resursu grupas | |
| |Krājumu apgrozījums pēc summas pēc resursu grupas | |
|Krājumu YOY (pēc noklusējuma pašreizējais gads pret iepriekšējo gadu) |Krājumu mēri | |
| |Krājumu KPI:<br>Krājumu apgrozījums<br>Krājumu precizitāte | |
| |Krājumu beigu bilance pēc gada un resursu grupas | |
| |Pirkšanas novirzes pēc gada un kategorijas nosaukuma 3. līmeņa | |
|Krājumi vecumstruktūras (noklusējums pēc pašreizējā gada) |Krājumu vecumstruktūras pēc ceturkšņa un resursu grupas | |
| |Krājumu vecumstruktūras pēc ceturkšņa un vietas nosaukuma | |
|NP vispār (noklusējums pēc pašreizējā perioda) |NP neto izmaiņas pēc kategorijas nosaukuma 1. līmeņa un kategorijas nosaukuma 2. līmeņa |Nepabeigto darbu NP mēri:<br>NP beigu bilance<br>NP neto izmaiņas<br>NP neto izmaiņas %<br> |
| |Ražošanas novirzes pēc resursu grupas un kategorijas nosaukuma 3. līmeņa | |
| |NP neto izmaiņas pēc resursu grupas | |
|NP pēc vietas (noklusējums pēc pašreizējā perioda) |Nepabeigto darbu NP mēri | |
| |NP neto izmaiņas pēc vietas nosaukuma un kategorijas nosaukuma 2. līmeņa | |
| |Ražošanas novirzes pēc vietas nosaukuma un kategorijas nosaukuma 3. līmeņa | |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Power BI satura pakotnes **Izmaksu pārvaldība** pārskatu lapu aizpildīšanai tiek izmantoti Dynamics 365 for Finance and Operations dati. Šie dati tiek attēloti kā apkopoti mērījumi, kuri pa posmiem tiek izveidoti elementu krātuvē, kas ir analīzes veikšanai optimizēta Microsoft SQL datu bāze. Papildinformāciju skatiet tēmā [Apskats par Power BI integrāciju elementu krātuvē](power-bi-integration-entity-store.md). Kā satura pamats tiek izmantoti tālāk norādītie galvenie apkopošanas mērījumi.

| Elements            | Galvenais apkopošanas mērījums | Dynamics 365 for Finance and Operations datu avots | Lauks             | Apraksts                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Pārskatu ieraksti | Neto apgrozījums                | CostAggregatedCostStatementEntryEntity      | sum(\[Summa\])   | Summa uzskaites valūtā |
| Pārskatu ieraksti | Neto izmaiņu daudzums       | CostAggregatedCostStatementEntryEntity      | sum(\[Daudzums\]) |                                   |

Nākamajā tabulā ir parādīts, kā galvenie apkopošanas mērījumi tiek izmantoti, lai satura datu kopā izveidotu vairākus aprēķinātos mērus.

| Mērs                                 | Kā šis mērs tiek aprēķināts                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sākuma bilance                       | \[Beigu bilance\]-\[Neto izmaiņas\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Sākuma bilances daudzums              | \[Beigu bilances daudzums\]-\[Neto izmaiņu daudzums\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Beigu bilance                          | CALCULATE(SUM(\[Summa\]), FILTER(ALLEXCEPT(“Finanšu kalendāri”, “Finanšu kalendāri”\[LedgerRecId\], “elementi”\[ID\], “elementi”\[Nosaukums\], “Virsgrāmatas”\[Valūta\], “Virsgrāmatas”\[Apraksts\], “Virsgrāmatas”\[Nosaukums\]), “Finanšu kalendāri”\[Datums\] &lt;= MAX(“Finanšu kalendāri”\[Datums\])))                                                                                                                                                                                           |
| Beigu bilances daudzums                 | CALCULATE(SUM(\[Daudzums\]), FILTER(ALLEXCEPT(“Finanšu kalendāri”, “Finanšu kalendāri”\[LedgerRecId\], “elementi”\[ID\], “elementi”\[Nosaukums\], “Virsgrāmatas”\[Valūta\], “Virsgrāmatas”\[Apraksts\], “Virsgrāmatas”\[Nosaukums\]), “Finanšu kalendāri”\[Datums\] &lt;= MAX(“Finanšu kalendāri”\[Date\])))                                                                                                                                                                                         |
| Krājumu sākuma bilance             | CALCULATE(\[Sākuma bilance\], “Pārskata ieraksti”\[Pārskata tips\] = “Krājumi”)                                                                                                                                                                                                                                                                                                                                                                                      |
| Krājumu beigu bilance                | CALCULATE(\[Beigu bilance\], “Pārskata ieraksti”\[Pārskata tips\] = “Krājumi”)                                                                                                                                                                                                                                                                                                                                                                                         |
| Krājumu neto izmaiņas                    | CALCULATE(\[Neto izmaiņas\], “Pārskata ieraksti”\[Pārskata tips\] = “Krājumi”)                                                                                                                                                                                                                                                                                                                                                                                             |
| Krājumu neto izmaiņu daudzums           | CALCULATE(\[Neto izmaiņu daudzums\], “Pārskata ieraksti”\[Pārskata tips\] = “Krājumi”)                                                                                                                                                                                                                                                                                                                                                                                    |
| Krājumu neto izmaiņas %                  | IF(\[Krājumu beigu bilance\] = 0, 0, \[Krājumu neto izmaiņas\] / \[Krājumu beigu bilance\])                                                                                                                                                                                                                                                                                                                                                                           |
| Krājumu apgrozījums pēc summas                | if(OR(\[Krājumu vidējā bilance\] &lt;= 0, \[Pārdoto vai patērēto krājumu izejošās plūsmas\] &gt;= 0), 0, ABS(\[Pārdoto vai patērēto krājumu izejošās plūsmas\])/\[Krājumu vidējā bilance\])                                                                                                                                                                                                                                                                                                  |
| Krājumu vidējā bilance               | (\[Krājumu beigu bilance\] + \[Krājumu sākuma bilance\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Pārdoto vai patērēto krājumu izejošās plūsmas       | \[Pārdotie krājumi\] + \[Patērēto materiālu krājumu izmaksas\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Patērēto materiālu krājumu izmaksas        | CALCULATE(\[Krājumu neto izmaiņas\], “Pārskata ieraksti”\[Kategorijas nosaukums - 2. līmenis\_\] = “ConsumedMaterialsCost”)                                                                                                                                                                                                                                                                                                                                                            |
| Pārdotie krājumi                          | CALCULATE(\[Krājumu neto izmaiņas\], “Pārskata ieraksti”\[Kategorijas nosaukums - 2. līmenis\_\] = “Pārdots”)                                                                                                                                                                                                                                                                                                                                                                             |
| Krājumu precizitāte pēc summas            | IF(\[Krājumu beigu bilance\] &lt;= 0, IF(OR(\[Krājumu aprēķinātā summa\] &lt;&gt; 0, \[Krājumu beigu bilance\] &lt; 0), 0, 1), MAX(0, (\[Krājumu beigu bilance\] - ABS(\[Krājumu aprēķinātā summa\]))/\[Krājumu beigu bilance\]))                                                                                                                                                                                                                              |
| Krājumu aprēķinātā summa                | CALCULATE(\[Krājumu neto izmaiņas\], “Pārskata ieraksti”\[Kategorijas nosaukums - 3. līmenis\_\] = “Uzskaite”)                                                                                                                                                                                                                                                                                                                                                                         |
| Krājumu vecumstruktūras                         | if(ISBLANK(max(“Finanšu kalendāri”\[Datums\])), blank(), MAX(0, MIN(\[Krājumu vecumstruktūru ienākošo plūsmu daudzums\], \[Krājumu vecumstruktūru beigu bilances daudzums\] - \[Krājumu vecumstruktūru ienākošo plūsmu daudzums nākotnē\]))) \* \[Krājumu vidējās vienības izmaksas\]                                                                                                                                                                                                                                |
| Krājumu vecumstruktūru ienākošo plūsmu daudzums       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Krājumu neto izmaiņu daudzums\], “Pārskata ieraksti”\[Daudzums\] &gt; 0, FILTER(ALLEXCEPT(“Finanšu kalendāri”, “Finanšu kalendāri”\[LedgerRecId\], “elementi”\[ID\], “elementi”\[Nosaukums\], “Virsgrāmatas”\[Valūta\], “Virsgrāmatas”\[Apraksts\], “Virsgrāmatas”\[Nosaukums\]), “Finanšu kalendāri”\[Datums\] &lt;= MAX(“Finanšu kalendāri”\[Datums\]))), CALCULATE(\[Krājumu neto izmaiņu daudzums\], “Pārskata ieraksti”\[Daudzums\] &gt; 0)) |
| Krājumu vecumstruktūru beigu bilances daudzums | \[Krājumu beigu bilances daudzums\] + CALCULATE(\[Krājumu neto izmaiņu daudzums\], FILTER(ALLEXCEPT(“Finanšu kalendāri”, “Finanšu kalendāri”\[LedgerRecId\], “elementi”\[ID\], “elementi”\[Nosaukums\], “Virsgrāmatas”\[Valūta\], “Virsgrāmatas”\[Apraksts\], “Virsgrāmatas”\[Nosaukums\]), “Finanšu kalendāri”\[Datums\] &gt; max(“Finanšu kalendāri”\[Datums\]) ))                                                                                                                                 |
| Krājumu vecumstruktūru ienākošās plūsmas nākotnē  | CALCULATE(\[Krājumu neto izmaiņas\], “Pārskata ieraksti”\[Summa\] &gt; 0, FILTER(ALLEXCEPT(“Finanšu kalendāri”, “Finanšu kalendāri”\[LedgerRecId\], “elementi”\[ID\], “elementi”\[Nosaukums\], “Virsgrāmatas”\[Valūta\], “Virsgrāmatas”\[Apraksts\], “Virsgrāmatas”\[Nosaukums\]), “Finanšu kalendāri”\[Datums\] &gt; MAX(“Finanšu kalendāri”\[Datums\])))                                                                                                                                             |
| Krājumu vidējās vienības izmaksas                 | CALCULATE(\[Krājumu beigu bilance\] / \[Krājumu beigu bilances daudzums\],ALLEXCEPT(“Finanšu kalendāri”, “Finanšu kalendāri”\[LedgerRecId\], “elementi”\[ID\], “elementi”\[Nosaukums\], “Virsgrāmatas”\[Valūta\], “Virsgrāmatas”\[Apraksts\], “Virsgrāmatas”\[Nosaukums\]))                                                                                                                                                                                                                 |
| Pirkšanas novirzes                      | CALCULATE(SUM(\[Summa\]), “Pārskata ieraksti”\[Kategorijas nosaukums - 2. līmenis\_\] = “Ražots”, “Pārskata ieraksti”\[Pārskata tips\] = “Novirze”)                                                                                                                                                                                                                                                                                                                              |
| NP sākuma bilance                   | CALCULATE(\[Sākuma bilance\], “Pārskata ieraksti”\[Pārskata tips\] = “NP”)                                                                                                                                                                                                                                                                                                                                                                                            |
| NP beigu bilance                      | CALCULATE(\[Beigu bilance\], “Pārskata ieraksti”\[Pārskata tips\] = “NP”)                                                                                                                                                                                                                                                                                                                                                                                               |
| NP neto izmaiņas                          | CALCULATE(\[Neto izmaiņas\], “Pārskata ieraksti”\[Pārskata tips\] = “NP”)                                                                                                                                                                                                                                                                                                                                                                                                   |
| NP neto izmaiņas %                        | IF(\[NP beigu bilance\] = 0, 0, \[NP neto izmaiņas\] / \[NP beigu bilance\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Ražošanas novirzes                    | CALCULATE(SUM(\[Summa\]), “Pārskata ieraksti”\[Kategorijas nosaukums - 2. līmenis\_\] = “ManufacturedCost”, “Pārskata ieraksti”\[Pārskata tips\] = “Novirze”)                                                                                                                                                                                                                                                                                                                      |
| Kategorijas nosaukums - 1. līmenis                 | switch(\[Kategorijas nosaukums - 1. līmenis\_\], “None”, “Nav”, "NetSourcing", “Neto avoti”, "NetUsage", “Neto lietojums”, "NetConversionCost", “Neto konvertēšanas izmaksas”, "NetCostOfGoodsManufactured", “Ražoto preču neto izmaksas”, "BeginningBalance", “Sākuma bilance”)                                                                                                                                                                                                         |
| Kategorijas nosaukums - 2. līmenis                 | switch(\[Kategorijas nosaukums - 2. līmenis\_\], “Nav”, “Nav”, “Ražots”, “Ražots”, “Norakstīts”, “Norakstīts”, “Pārsūtīts”, “Pārsūtīts”, “Pārdots”, “Pārdots”, “ConsumedMaterialsCost”, “Patērēto materiālu izmaksas”, “ConsumedManufacturingCost”, “Patērētās ražošanas izmaksas", “ConsumedOutsourcingCost”, “Patērētās ārpakalpojumu izmaksas”, “ConsumedIndirectCost”, “Patērētās netiešās izmaksas", “ManufacturedCost”, “Ražošanas izmaksas”, “Novirzes”, “Novirzes”)                            |
| Kategorijas nosaukums - 3. līmenis                 | switch(\[Kategorijas nosaukums - 3. līmenis\_\], “Nav”, "“Nav”, “Uzskaite”, “Nav”, “ProductionPriceVariance”, “Ražošanas cena, “QuantityVariance”, “Daudzums”, “SubstitutionVariance”, “Aizstāšana”, “ScrapVariance”, “Brāķis”, “LotSizeVariance”, “Laidiena lielums”, “RevaluationVariance”, “Pārvērtēšana”, “PurchasePriceVariance”, “Pirkšanas cena”, “CostChangeVariance”, “Izmaksu izmaiņas”, “RoundingVariance”, “Noapaļošanas novirze”)                                                   |

Tālāk norādītās galvenās dimensijas tiek lietotas kā filtri, lai apkopošanas mērījumus sadalītu, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements           | Atribūtu piemēri                       |
|------------------|----------------------------------------------|
| Elementi         | ID, Nosaukums                                     |
| Finanšu kalendāri | Kalendārs, Mēnesis, Periods, Ceturksnis, Gads       |
| KPI mērķi        | Krājumu precizitātes mērķis, Krājumu apgrozījuma mērķis |
| Virsgrāmatas          | Valūta, Nosaukums, Apraksts                  |
| Atrašanās vietas            | ID, nosaukums, Valsts, Pilsēta                      |

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)





