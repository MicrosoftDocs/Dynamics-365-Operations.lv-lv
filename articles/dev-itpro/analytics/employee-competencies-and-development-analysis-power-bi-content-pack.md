---
title: "Power BI satura pakotne Darbinieku zināšanas un attīstība"
description: "Šajā tēmā ir aprakstīts Power BI saturs Finance and Operations – Darbinieku zināšanas un attīstība."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 99fa6e396989e6e204d84cc776f627c7c4baf1d1
ms.contentlocale: lv-lv
ms.lasthandoff: 12/19/2017

---

# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI satura pakotne Darbinieku zināšanas un attīstība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts Power BI saturs Finance and Operations – Darbinieku zināšanas un attīstība. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Pēc tam, kad ir izveidots satura pakotnes savienojums ar jūsu Dynamics 365 for Finance and Operations datiem, pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                            | Saturs                                               |
|-----------------------------------|--------------------------------------------------------|
| Zināšanu un attīstības analīze | Grupas dalībnieka prasmju tipi un grupas dalībnieka prasmes pēc tipa |
| Prasmju profils                     | Prasmju profils atlasītajam darbiniekam                |
| Prasmju analīze                    | Prasmes pēc tipa un vērtējuma                              |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Finance and Operations dati tiek izmantoti satura pakotnes Darbinieku zināšanas un attīstība pārskatu aizpildīšanai. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

| Elements                            | Saturs                                                                                                   | Attiecības ar citiem elementiem                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbaspēks\_CalendarOffset         | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_Uzņēmums                | Uzņēmumi, pēc kuriem pārskatus filtrēt                                                                             |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_Atlīdzība           | Apmaksas likme un frekvence laika gaitā                                                                           |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_CurrentCompensation    | Apmaksas likme un frekvence pašreizējā datumā                                                              | Darbaspēks\_Uzņēmums Darbaspēks\_CurrentCompensation Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Amati ir pašreizējā datuma, pilna laika ekvivalenta (full-time equivalent — FTE) atvērti amati/vakances, un amati, kas ir atvērti līdz aizpildīšanai | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Nodarbinātie pašreizējā datumā, vecums un skaits                                                         | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_GeographicLocation Darbaspēks\_Veiktspēja Darbaspēks\_PersonSkill Darbaspēks\_WorkerName Darbaspēks\_ReportsToWorkerName Darbaspēks\_WorkerTitle Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Darbs Darbaspēks\_Nodarbinātība Darbaspēks\_Amats                     |
| Darbaspēks\_Datums                   | Dienas, nedēļas, mēneši un gadi                                                                             |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_Demogrāfiskie dati           | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis                                                   |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_Nodarbinātība             | Sākuma datums, beigu datums un pārejas datums                                                                  |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_GeographicLocation     | Pilsēta, novads, pasta indekss un štats vai reģions                                                           |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_Darbs                    | Funkcija, tips un nosaukums                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_JobPreferredSkill      | Svarīgums, vērtējums, prasme un prasmes līmenis                                                                 | Darbaspēks\_Prasme Darbaspēks\_Darbs                                                                                                                                                                                                                                                                         |
| Darbaspēks\_PastPositionAssignment | Piešķiršanas iemesls, sākuma datums, beigu datums un darbs                                                           | Darbaspēks\_ClaendarOffset Darbaspēks\_Datums Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                                                            |
| Darbaspēks\_Veiktspēja            | Vērtējums, apraksts un vērtēšanas modelis                                                                      |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_PersonSkill            | Līmenis, līmeņa datums un prasme                                                                               | Darbaspēks\_Prasme                                                                                                                                                                                                                                                                                        |
| Darbaspēks\_PersonSkillAnalysis    | Sertificēts, līmenis, līmeņa datums un prasme                                                                    | Darbaspēks\_WorkerName Darbaspēks\_Prasme                                                                                                                                                                                                                                                                  |
| Darbaspēks\_Amats               | Nodaļa, FTE, amats, amata tips un nosaukums                                                        |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_PositionTrend          | Amati laika gaitā, FTE un darbs                                                                          | Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                                                            |
| Darbaspēks\_ReportsToWorkerName    | Vārds, uzvārds un pilnais vārds                                                                       |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_Prasme                  | Prasme, prasmes tips un vērtējums                                                                              |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_TerminatedWorker       | Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības, pārtraukšanas datums, nosaukums, amats un darbs                                             | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_GeographicLocation Darbaspēks\_Veiktspēja Darbaspēks\_WorkerName Darbaspēks\_ReportsToWorkerName Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_WorkerTitle Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Nodarbinātība Darbaspēks\_Darbs Darbaspēks\_Amats |
| Darbaspēks\_WorkerName             | Vārds, uzvārds un pilnais vārds                                                                       |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_WorkerTitle            | Nosaukums un darba stāža datums                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Darbaspēks\_WorkerTrend             | Nodarbinātie laika gaitā, skaits, uzņēmums un amats                                                        | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_GeographicLocation Darbaspēks\_Veiktspēja Darbaspēks\_WorkerName Darbaspēks\_ReportsToWorkerName Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_WorkerTitle Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Nodarbinātība Darbaspēks\_Darbs                     |






