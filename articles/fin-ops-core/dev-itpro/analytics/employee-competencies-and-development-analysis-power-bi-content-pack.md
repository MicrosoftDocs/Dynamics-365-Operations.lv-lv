---
title: Power BI satura pakotne Darbinieka zināšanas un attīstība
description: Šajā tēmā ir aprakstīta Power BI satura pakotne Darbinieku kompetences un attīstība.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bed461677cbdfa57b0a198b7179eccb9828dc944
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687130"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI satura pakotne Darbinieka zināšanas un attīstība

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Power BI satura pakotne Darbinieku kompetences un attīstība. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Kad ir izveidots satura pakotnes savienojums ar jūsu datiem, pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat saņemt lapā [Power BI vadītā apmācība](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                            | Saturs                                               |
|-----------------------------------|--------------------------------------------------------|
| Zināšanu un attīstības analīze | Grupas dalībnieka prasmju tipi un grupas dalībnieka prasmes pēc tipa |
| Prasmju profils                     | Prasmju profils atlasītajam darbiniekam                |
| Prasmju analīze                    | Prasmes pēc tipa un vērtējuma                              |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Programmas dati tiek izmantoti satura pakotnes Darbinieku zināšanas un attīstība pārskatu aizpildīšanai. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

| Elements                            | Saturs                                                                                                   | Attiecības ar citiem elementiem |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Darbaspēks\_CalendarOffset         | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          | |
| Darbaspēks\_Uzņēmums                | Uzņēmumi, pēc kuriem pārskatus filtrēt                                                                             | |
| Darbaspēks\_Atlīdzība           | Apmaksas likme un frekvence laika gaitā                                                                           | |
| Darbaspēks\_CurrentCompensation    | Apmaksas likme un frekvence pašreizējā datumā                                                              | Darbaspēks\_Uzņēmums, Darbaspēks\_CurrentCompensation, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_CurrentPosition        | Amati ir pašreizējā datuma, pilna laika ekvivalenta (full-time equivalent — FTE) atvērti amati/vakances, un amati, kas ir atvērti līdz aizpildīšanai | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Nodarbinātie pašreizējā datumā, vecums un skaits                                                         | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība. Darbaspēks\_GeographicLocation, Darbaspēks\_Veiktspēja, Darbaspēks\_PersonSkill, Darbaspēks\_WorkerName, Darbaspēks\_ReportsToWorkerName, Darbaspēks\_WorkerTitle, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Darbs, Darbaspēks\_Nodarbinātība, Darbaspēks\_Amats |
| Workforce\_Date                   | Dienas, nedēļas, mēneši un gadi                                                                             | |
| Darbaspēks\_Demogrāfiskie dati           | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis                                                   | |
| Darbaspēks\_Nodarbinātība             | Sākuma datums, beigu datums un pārejas datums                                                                  | |
| Darbaspēks\_GeographicLocation     | Pilsēta, novads, pasta indekss un štats vai reģions                                                           | |
| Darbaspēks\_Darbs                    | Funkcija, tips un nosaukums                                                                                  | |
| Darbaspēks\_JobPreferredSkill      | Svarīgums, vērtējums, prasme un prasmes līmenis                                                                 | Darbaspēks\_Prasme, Darbaspēks\_Darbs |
| Workforce\_PastPositionAssignment | Piešķiršanas iemesls, sākuma datums, beigu datums un darbs                                                           | Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_Performance            | Vērtējums, apraksts un vērtēšanas modelis                                                                      | |
| Darbaspēks\_PersonSkill            | Līmenis, līmeņa datums un prasme                                                                               | Darbaspēks\_Prasme |
| Darbaspēks\_PersonSkillAnalysis    | Sertificēts, līmenis, līmeņa datums un prasme                                                                    | Darbaspēks\_WorkerName, Darbaspēks\_Prasme |
| Workforce\_Position               | Nodaļa, FTE, amats, amata tips un nosaukums                                                        | |
| Darbaspēks\_PositionTrend          | Amati laika gaitā, FTE un darbs                                                                          | Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_ReportsToWorkerName    | Vārds, uzvārds un pilnais vārds                                                                       | |
| Darbaspēks\_Prasme                  | Prasme, prasmes tips un vērtējums                                                                              | |
| Darbaspēks\_TerminatedWorker       | Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības, pārtraukšanas datums, nosaukums, amats un darbs                                             | Darbaspēks\_Uzņēmums, Darbaspēks\_Atlīdzība, Darbaspēks\_GeographicLocation, Darbaspēks\_Veiktspēja, Darbaspēks\_WorkerName, Darbaspēks\_ReportsToWorkerName, Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_WorkerTitle, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Nodarbinātība, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_WorkerName             | Vārds, uzvārds un pilnais vārds                                                                       | |
| Darbaspēks\_WorkerTitle            | Nosaukums un darba stāža datums                                                                                   | |
| Darbaspēks\_WorkerTrend             | Nodarbinātie laika gaitā, skaits, uzņēmums un amats                                                        | Darbaspēks\_Uzņēmums, Darbaspēks\_Atlīdzība, Darbaspēks\_GeographicLocation, Darbaspēks\_Veiktspēja, Darbaspēks\_WorkerName, Darbaspēks\_ReportsToWorkerName, Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_WorkerTitle, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Nodarbinātība, Darbaspēks\_Darbs |
