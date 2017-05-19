---
title: "Power BI satura pakotne Darbinieku zināšanas un attīstība"
description: "Šajā tēmā ir aprakstīts Power BI saturs Dynamics 365 for Operations – Darbinieku zināšanas un attīstība. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai izveidotu šo satura pakotni."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 48a12a32fd6a0d95f50b98e6533173265b9867ab
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI satura pakotne Darbinieku zināšanas un attīstība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts Power BI saturs Dynamics 365 for Operations – Darbinieku zināšanas un attīstība. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai izveidotu šo satura pakotni.

<a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
--------------------------

Satura pakotne Darbinieku zināšanas un attīstība ir atrodama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un to savienot ar saviem Microsoft Dynamics 365 for Operations datiem, skatiet rakstā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Pēc satura pakotnes savienošanas ar jūsu Dynamics 365 for Operations datiem pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                            | Saturs                                               |
|-----------------------------------|--------------------------------------------------------|
| Zināšanu un attīstības analīze | Grupas dalībnieka prasmju tipi un grupas dalībnieka prasmes pēc tipa |
| Prasmju profils                     | Prasmju profils atlasītajam darbiniekam                |
| Prasmju analīze                    | Prasmes pēc tipa un vērtējuma                              |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Satura pakotnes Darbinieku zināšanas un attīstība pārskatu aizpildīšanai tiek izmantoti Dynamics 365 for Operations dati. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

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

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti satura pakotnē. Ja pārskatos un informācijas panelī vēlaties ietvert papildu aprēķinus, varat no LCS lejupielādēt un modificēt failu CompetenciesandDevelopment.pbix. Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidošanai. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





