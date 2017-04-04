---
title: "Izmaksu vadības strāvas BI saturu"
description: "Šajā tēmā ir aprakstīts, kādas programmas ir iekļautas izmaksu pārvaldības jauda BI saturu. To skaidro kā piekļūt varas BI atskaites un sniedz informāciju par datu modelis un vienībām, kas tiek izmantoti, lai veidotu saturu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Izmaksu vadības strāvas BI saturu

Šajā tēmā ir aprakstīts, kādas programmas ir iekļautas izmaksu pārvaldības jauda BI saturu. To skaidro kā piekļūt varas BI atskaites un sniedz informāciju par datu modelis un vienībām, kas tiek izmantoti, lai veidotu saturu.

# <a name="overview"></a>Pārskats

**Izmaksu pārvaldība** Microsoft Power BI saturs ir paredzēts krājumu grāmatveži vai organizācijas personām, kuras ir atbildīgas par krājumu. **Izmaksu pārvaldība** Power BI saturs nodrošina vadības ieskatu krājumi un Nepabeigtie (projekti NP) krājumu un kā izmaksu plūsmu caur tiem pēc kategorijas laika gaitā. Informāciju var izmantot kā papildinājumu detalizētu finanšu pārskatu.

## <a name="key-measures"></a>Galvenie pasākumi

+ Sākuma bilance
+ Beigu bilance
+ Neto apgrozījums
+ Neto apgrozījumu %
+ Vecumstruktūras

## <a name="key-performance-indicators"></a>Izpildes pamatrādītājs
+ Krājumu apgrozījums
+ Krājumu precizitāte

Primārais datu avots CostAggregatedCostStatementEntryEntity ir CostStatementCache galda. Šī tabula pārvalda kešatmiņas datu kopas ietvaros. Pēc noklusējuma tabula tiek atjaunināta ik pēc 24 stundām, bet to var iespējot manuālus atjauninājumus konfigurācijas datu kešatmiņā. Pēc tam tu vari manuālā atjaunināšana **izmaksu pārvaldība** vai **izmaksu analīze** darbvietu. Pēc izpildes CostStatementCache atjauninājumu, jums ir jāatjaunina OData savienojums ar jaudu BI.com, lai skatītu atjauninātos datus vietnē. Dispersija (pirkšana, ražošana) pasākumi šīs varas BI saturs attiecas tikai uz krājumiem, kas tiek novērtēti pēc krājuma standarta izmaksu metode. Ražošanas dispersiju aprēķina kā starpību starp aktīva un faktiskās izmaksas. Ražošanas dispersiju aprēķina, ja ražošanas pasūtījumam ir statuss **pabeigts**. Plašāku informāciju par ražošanas dispersijas veidi un kā tiek aprēķināts katram tipam, skatiet [par analizējot dispersijas pabeigto ražošanas pasūtījumu](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Piekļuvi saturam Power BI
**Izmaksu pārvaldība** BI enerģijas saturs ir pieejams no PowerBI.com. Plašāku informāciju par savienojumu un ielādē Microsoft Dynamics 365, attiecībā uz darbības datiem, skatiet [Access Power BI saturu no PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriku, kas iekļauti barošanas BI saturu
Saturs ietver virkni atskaišu lappusēm. Katras lappuses sastāv no metriku, kas iztēlojās kā diagrammas, flīzes un tabulas. Tālāk redzamajā tabulā sniegts pārskats par vizualizāciju, **izmaksu pārvaldība** BI enerģijas saturu.

| Atskaites lapu | Diagrammas | Virsraksti |
|---|---|---|
|Krājumu kopējais (noklusējums, pašreizējā periodā) |Precizitāte |Krājumu pasākumi:<br>Krājumu beigu atlikums<br>Krājumu neto apgrozījums<br>Krājumu neto apgrozījums %<br>|
| |Krājumu apgrozījums | |
| |Krājumu beigu atlikums pēc resursu grupas | |
| |Krājumu neto apgrozījumu ar kategorijas nosaukumu 1. līmeņa un kategorijas nosaukums 2. līmeņa| |
| |Resursu grupas un kategorijas nosaukums līmenis 3 iepirkuma dispersijas | |
|Krājumu pēc vietas (noklusējums, pašreizējā periodā) |Krājumu bilances beigšanas ar vietnes nosaukumu un resursu grupu | |
| |Krājumu, kas savukārt ar vietnes nosaukumu un resursu grupu | |
| |Krājumu beigu atlikums pa pilsētu un resursu grupām | |
|Krājumu pēc resursu grupas (noklusējums, pašreizējā periodā) |Krājumu pasākumi | |
| |Krājumu precizitāti, summa ar resursu grupu | |
| |Krājumu, kas savukārt summu ar resursu grupu | |
|YOY (noklusējuma kārtējā gadā vai iepriekšējā gadā) krājumi |Krājumu pasākumi | |
| |Krājumu KPI:<br>Krājumu apgrozījums<br>Krājumu precizitāte | |
| |Krājumu bilances beigšanas gads un resursu grupa | |
| |Gadā un kategorijas nosaukums līmenis 3 iepirkuma dispersijas | |
|Krājumu novecošanos (noklusējums pēc kārtējā gadā) |Krājumu novecošanos, ceturksnis un resursu grupa | |
| |Krājumu novecošanos, ceturksnis un vietnes nosaukumu | |
|NP kopumā (noklusējums, pašreizējā periodā) |Neto NP mainīt kategorijas nosaukums 1. līmeņa un kategorijas nosaukums līmenis 2 |Darba gaitā NP pasākumi:<br>NP beigu atlikums<br>NP neto apgrozījums<br>Neto apgrozījums NP %<br> |
| |Dispersijas ražošanas resursu grupu un kategoriju nosaukums 3. līmenis | |
| |Neto apgrozījums RNR, resursu grupas | |
|NP vietā (noklusējums, pašreizējā periodā) |Darba gaitā NP pasākumu | |
| |Neto NP mainīt vietnes nosaukumu un kategorijas nosaukums līmenis 2 | |
| |Dispersijas ražošanas vietas nosaukums un kategorijas nosaukums 3. līmenis | |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
365 dinamika attiecībā uz darbības datiem tiek lietota, lai aizpildītu ziņojumu lapas **izmaksu pārvaldība** BI enerģijas saturu. Šie dati tiek attēlots kā apkopojuma mērījumus, kas ir iestudētas entītiju krātuvē, kas ir Microsoft SQL datu bāzi, kas ir optimizēta analytics. Lai iegūtu papildinformāciju, skatiet [pārskats par strāvas BI integrācija ar entītiju veikalā](power-bi-integration-entity-store.md). Šādus galvenos apkopojuma mērījumus izmanto par saturu pamatu.

| Elements            | Kopējais mērījumu | Datu avotu dinamiku 365 operācijām | Lauks             | apraksts                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Paziņojums ieraksti | Neto apgrozījums                | CostAggregatedCostStatementEntryEntity      | SUM (\[summu\])   | Summa pārskata valūtā |
| Paziņojums ieraksti | Neto apgrozījuma daudzums       | CostAggregatedCostStatementEntryEntity      | SUM (\[daudzuma\]) |                                   |

Tabulā ir parādīts, kā galveno apkopoto mērījumus izmanto, lai izveidotu vairākas aprēķinātie līdzekļi satura dataset.

| Mērs                                 | Kā pasākums tiek aprēķināta                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sākuma bilance                       | \[Beigu atlikums\]-\[neto pārmaiņas\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Sākuma bilances daudzums              | \[Beigu atlikums daudzums\]-\[neto apgrozījuma daudzums\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Beigu bilance                          | APRĒĶINĀT (SUM (\[summa\]), filtrs (ALLEXCEPT ("Fiskālo kalendāri", "Fiskālā kalendāri"\[LedgerRecId\], "vienības"\[ID\], "vienības"\[nosaukums\], 'Grāmatas'\[valūtas\], 'Grāmatas'\[apraksts\], 'Grāmatas'\[nosaukums\]), "Fiskālā kalendāri"\[datumu\]&lt;= MAX ("Fiskālo kalendāri"\[datumu\])))                                                                                                                                                                                           |
| Beigu bilances daudzums                 | APRĒĶINĀT (SUM (\[daudzums\]), filtrs (ALLEXCEPT ("Fiskālo kalendāri", "Fiskālā kalendāri"\[LedgerRecId\], "vienības"\[ID\], "vienības"\[nosaukums\], 'Grāmatas'\[valūtas\], 'Grāmatas'\[apraksts\], 'Grāmatas'\[nosaukums\]), "Fiskālā kalendāri"\[datumu\]&lt;= MAX ("Fiskālo kalendāri"\[datumu\])))                                                                                                                                                                                         |
| Sākuma atlikums krājumu             | APRĒĶINĀT (\[sākuma atlikums\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "Krājumi")                                                                                                                                                                                                                                                                                                                                                                                      |
| Krājumu beigu atlikums                | APRĒĶINĀT (\[beigu atlikums\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "Krājumi")                                                                                                                                                                                                                                                                                                                                                                                         |
| Krājumu neto apgrozījums                    | APRĒĶINĀT (\[neto pārmaiņas\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "Krājumi")                                                                                                                                                                                                                                                                                                                                                                                             |
| Krājumu neto apgrozījuma daudzums           | APRĒĶINĀT (\[neto apgrozījuma daudzums\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "Krājumi")                                                                                                                                                                                                                                                                                                                                                                                    |
| Krājumu neto apgrozījums %                  | IF (\[krājumu beigu atlikums\] = 0, 0, \[krājuma neto apgrozījums\] / \[krājumu beigu atlikums\])                                                                                                                                                                                                                                                                                                                                                                           |
| Summu, savukārt krājuma                | Ja (OR (\[krājumu vidējais atlikums\]&lt;= 0, \[krājumu pārdot vai patērē jautājumiem\]&gt;= 0), 0, ABS (\[krājumu pārdot vai patērē jautājumiem\]) /\[krājumu vidējais atlikums\])                                                                                                                                                                                                                                                                                                  |
| Krājumu vidējais atlikums               | (\[Krājumu beigu atlikums\] + \[sākuma bilances krājumu\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Krājumu pārdot vai patērē jautājumiem       | \[Pārdoto krājumu\] + \[krājumu patērēts materiālu izmaksas\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Krājumu patērēts materiālu izmaksas        | APRĒĶINĀT (\[krājuma neto apgrozījums\], 'Paziņojumu ieraksti'\[kategorijas nosaukums - 2. līmeņa\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Pārdoto krājumu                          | APRĒĶINĀT (\[krājuma neto apgrozījums\], 'Paziņojumu ieraksti'\[kategorijas nosaukums - 2. līmeņa\_\] = "Pārdots")                                                                                                                                                                                                                                                                                                                                                                             |
| Precizitāte krājumu summu            | IF (\[krājumu beigu atlikums\]&lt;= 0, ja (vai (\[krājumu skaita summu\]&lt;&gt; 0, \[krājumu beigu atlikums\]&lt; 0), 0, 1), MAX (0, (\[krājumu beigu atlikums\] -ABS (\[krājumu skaita summu\])) /\[krājumu beigu atlikums\]))                                                                                                                                                                                                                              |
| Saskaitītais daudzums krājumu                | APRĒĶINĀT (\[krājuma neto apgrozījums\], 'Paziņojumu ieraksti'\[kategorijas nosaukums - līmenis 3\_\] = "Inventarizācija")                                                                                                                                                                                                                                                                                                                                                                         |
| Krājumu vecumstruktūras                         | Ja (ISBLANK (Maks ("Fiskālā kalendāri"\[datumu\])), blank(), MAX (0, MIN (\[krājumu novecošanos ieejas plūsmas daudzumu\], \[krājumu novecošanos beigu atlikumu daudzums\] - \[krājumu novecošanos ieejas plūsmas daudzumu nākotnē\]))) \*\[krājumu avg vienības pašizmaksa\]                                                                                                                                                                                                                                |
| Krājumu ieejas plūsmas daudzumu novecošanās       | IF (\[minDate\] = \[minDateAllSelected\], aprēķināt (\[krājumu izmaiņu neto daudzums\], 'Paziņojumu ieraksti'\[daudzums\]&gt; 0, filtru (ALLEXCEPT ("Fiskālo kalendāri", "Fiskālā kalendāri"\[LedgerRecId\], "vienības"\[ID\], "vienības"\[nosaukums\], 'Grāmatas'\[valūtas\], 'Grāmatas'\[apraksts\], 'Grāmatas'\[nosaukums\]), "Fiskālo kalendāri"\[datumu\]&lt;= MAX ("Fiskālo kalendāri"\[datumu\]))), aprēķināt (\[krājumu izmaiņu neto daudzums\], 'Paziņojumu ieraksti'\[daudzums\]&gt; 0)) |
| Beigu atlikums daudzums krājumu novecošanos | \[Krājumu beigu atlikums daudzums\] + aprēķināt (\[krājumu izmaiņu neto daudzums\], filtrs (ALLEXCEPT ("Fiskālo kalendāri", "Fiskālā kalendāri"\[LedgerRecId\], "vienības"\[ID\], "vienības"\[nosaukums\], 'Grāmatas'\[valūtas\], 'Grāmatas'\[apraksts\], 'Grāmatas'\[nosaukums\]), "Fiskālā kalendāri"\[datumu\]&gt; Maks ("Fiskālo kalendāri"\[datumu\])))                                                                                                                                 |
| Krājumu novecošanos saņemšanu nākotnē  | APRĒĶINĀT (\[krājuma neto apgrozījums\], "Paziņojumu ieraksti"\[summa\]&gt; 0, filtru (ALLEXCEPT ("Fiskālo kalendāri", "Fiskālā kalendāri"\[LedgerRecId\], "vienības"\[ID\], "vienības"\[nosaukums\], 'Grāmatas'\[valūtas\], 'Grāmatas'\[apraksts\], 'Grāmatas'\[nosaukums\]), "Fiskālā kalendāri"\[datumu\]&gt; MAX ("Fiskālo kalendāri"\[datumu\])))                                                                                                                                             |
| Krājumu avg vienības pašizmaksa                 | APRĒĶINĀT (\[krājumu beigu atlikums\] / \[krājumu beigu atlikums daudzums\], ALLEXCEPT ("Fiskālo kalendāri", 'Fiskālā kalendārus'\[LedgerRecId\], "vienības"\[ID\], "vienības"\[nosaukums\], 'Grāmatas'\[valūtas\], 'Grāmatas'\[apraksts\], 'Grāmatas'\[nosaukums\]))                                                                                                                                                                                                                 |
| Iepirkuma dispersijas                      | APRĒĶINĀT (SUM (\[summu\]), 'Paziņojumu ieraksti'\[kategorijas nosaukums - 2. līmeņa\_\] = "Procured", 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "Starpība")                                                                                                                                                                                                                                                                                                                              |
| NP sākuma bilance                   | APRĒĶINĀT (\[sākuma atlikums\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "NP")                                                                                                                                                                                                                                                                                                                                                                                            |
| NP beigu atlikums                      | APRĒĶINĀT (\[beigu atlikums\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "NP")                                                                                                                                                                                                                                                                                                                                                                                               |
| NP neto apgrozījums                          | APRĒĶINĀT (\[neto pārmaiņas\], 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "NP")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Neto apgrozījums NP %                        | IF (\[NP beigu atlikums\] = 0, 0, \[NP neto apgrozījums\] / \[NP beigu atlikums\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Ražošanas dispersijas                    | APRĒĶINĀT (SUM (\[summu\]), 'Paziņojumu ieraksti'\[kategorijas nosaukums - 2. līmeņa\_\] = "ManufacturedCost", 'Paziņojumu ieraksti'\[priekšraksta tipu\] = "Starpība")                                                                                                                                                                                                                                                                                                                      |
| Kategorijas nosaukums - 1. līmeņa                 | Slēdzi (\[kategorijas nosaukums - 1. līmeņa\_\], "None", "None", "NetSourcing", "Tīrā plānošanas", "NetUsage", "Interneta lietošanas", "NetConversionCost", "Neto konversijas izmaksas", "NetCostOfGoodsManufactured", "Neto izmaksas par precēm, kas ražotas", "BeginningBalance", "Sākuma atlikums")                                                                                                                                                                                                         |
| Kategorijas nosaukums - 2 līmenis                 | Slēdzi (\[kategorijas nosaukums - 2. līmeņa\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Pārvietot", "Pārvietot", "Pārdots", "Pārdots", "ConsumedMaterialsCost", "Patērēts materiālu izmaksas", "ConsumedManufacturingCost", "Patērē ražošanas izmaksu", "ConsumedOutsourcingCost", "Patērē ārpakalpojumu izmaksas", "ConsumedIndirectCost", "Consumed netiešās izmaksas", "ManufacturedCost", "Ražo izmaksas", "Neatbilstības", "Dispersijas")                            |
| Kategorijas nosaukums - līmenis 3                 | Slēdzi (\[kategorijas nosaukums - līmenis 3\_\], "None", "None", "Inventarizācija", "None", "ProductionPriceVariance", "Ražošanas cena", "QuantityVariance", "Daudzums", "SubstitutionVariance", "Aizstāšana", "ScrapVariance", "Brāķi", "LotSizeVariance", "Partijas lielumu", "RevaluationVariance", "Pārvērtēšanas", "PurchasePriceVariance", "Iepirkuma cena", "CostChangeVariance", "Izmaksu pārmaiņas", "RoundingVariance", "Noapaļošanas starpības")                                                   |

Šādi galvenie izmēri tiek izmantoti kā filtri, šķēle apkopojuma mērījumus, lai panāktu lielāku detalizācijas un nodrošinātu dziļāku analītisku ieskatu.

| Elements           | Atribūtu piemēri                       |
|------------------|----------------------------------------------|
| Elementi         | KODS, nosaukums                                     |
| Finanšu kalendāri | Kalendāra mēnesī, periodā, ceturksnis, gads       |
| KPI mērķi        | Krājuma mērķis precizitāti, krājumu savukārt mērķis |
| Virsgrāmatas          | Valūtas nosaukums, apraksts                  |
| Atrašanās vietas            | ID, vārdu, valsts, pilsēta                      |

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](..\data-entities\data-entities.md)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](configure-power-bi-integration.md)



