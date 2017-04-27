---
title: "Power BI saturs Atlīdzība un atvieglojumi"
description: "Šajā tēmā ir aprakstīts Power BI saturs Dynamics 365 for Operations – Atlīdzība un atvieglojumi. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai izveidotu šo satura pakotni."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 557f9218032e2b1160b6ea0631ada951353d2afd
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-and-benefits-power-bi-content"></a>Power BI saturs Atlīdzība un atvieglojumi

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts Power BI saturs Dynamics 365 for Operations – Atlīdzība un atvieglojumi. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai izveidotu šo satura pakotni.

<a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
--------------------------

Satura pakotne Atlīdzība un atvieglojumi ir atrodama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un to savienot ar saviem Microsoft Dynamics 365 for Operations datiem, skatiet rakstā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Pēc satura pakotnes savienošanas ar jūsu Dynamics 365 for Operations datiem pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                     | Saturs                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Atlīdzību un atvieglojumu analīze | Stundu darba un algotie darbinieki pēc uzņēmuma, vidējā stundas samaksa, vidējā algotā samaksa, darbinieki pēc nodarbinātības tipa un plāna reģistrācija |
| Darbinieka atvieglojumi          | Darbinieka reģistrācija pēc atlasītā atvieglojuma                                                                                               |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Satura pakotnes Atlīdzība un atvieglojumi pārskatu aizpildīšanai tiek izmantoti Dynamics 365 for Operations dati. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

| Elements                            | Saturs                                                                                                   | Attiecības ar citiem elementiem                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbaspēks\_CalendarOffset         | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          | Darbaspēks\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Darbaspēks\_Uzņēmums                | Uzņēmumi, pēc kuriem pārskatus filtrēt                                                                             | Darbaspēks\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Darbaspēks\_Atlīdzība           | Apmaksas likme un frekvence laika gaitā                                                                           | Darbaspēks\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Darbaspēks\_CurrentCompensation    | Apmaksas likme un frekvence pašreizējā datumā                                                              | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                                                            |
| Darbaspēks\_CurrentPosition        | Amati ir pašreizējā datuma, pilna laika ekvivalenta (full-time equivalent — FTE) atvērti amati/vakances, un amati, kas ir atvērti līdz aizpildīšanai | Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                                                                                                                               |
| Darbaspēks\_CurrentWorker          | Nodarbinātie pašreizējā datumā, vecums un skaits                                                         | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_GeographicLocation Darbaspēks\_Veiktspēja Darbaspēks\_WorkerName Darbaspēks\_ReportsToWorkerName Darbaspēks\_WorkerTitle Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Darbs Darbaspēks\_Nodarbinātība Darbaspēks\_Amats Darbaspēks\_WorkerBenefit                                            |
| Darbaspēks\_Datums                   | Dienas, nedēļas, mēneši un gadi                                                                             | Darbaspēks\_PastPositionAssignment Darbaspēks\_PositionTrend Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                     |
| Darbaspēks\_Demogrāfiskie dati           | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis                                                   | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_Nodarbinātība             | Sākuma datums, beigu datums un pārejas datums                                                                  | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_GeographicLocation     | Pilsēta, novads, pasta indekss un štats vai reģions                                                           | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_Darbs                    | Funkcija, tips un nosaukums                                                                                  | Darbaspēks\_CurrentPosition Darbaspēks\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Darbaspēks\_PastPositionAssignment | Piešķiršanas iemesls, sākuma datums, beigu datums un darbs                                                           | Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                                                                                     |
| Darbaspēks\_Veiktspēja            | Vērtējums, apraksts un vērtēšanas modelis                                                                      | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_Amats               | Nodaļa, FTE, amats, amata tips un nosaukums                                                        | Darbaspēks\_CurrentPosition Darbaspēks\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Darbaspēks\_PositionTrend          | Amati laika gaitā, FTE un darbs                                                                          | Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_Darbs Darbaspēks\_Amats                                                                                                                                                                                                                                                     |
| Darbaspēks\_ReportsToWorkerName    | Vārds, uzvārds un pilnais vārds                                                                       | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_Prasme                  | Prasme, prasmes tips un vērtējums                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Darbaspēks\_TerminatedWorker       | Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības, pārtraukšanas datums, nosaukums, amats un darbs                                             | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_GeographicLocation Darbaspēks\_Veiktspēja Darbaspēks\_WorkerName Darbaspēks\_ReportsToWorkerName Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_WorkerTitle Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Nodarbinātība Darbaspēks\_Darbs Darbaspēks\_Amats Darbaspēks\_WorkerBenefit |
| Darbaspēks\_WorkerBenefit          | Spēkā stāšanās datums, atvieglojumu opcija, atvieglojumu plāns un atvieglojumu tips                                             | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_WorkerName             | Vārds, uzvārds un pilnais vārds                                                                       | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_WorkerTitle            | Nosaukums un darba stāža datums                                                                                   | Darbaspēks\_CurrentWorker Darbaspēks\_TerminatedWorker Darbaspēks\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_WorkerTrend             | Nodarbinātie laika gaitā, skaits, uzņēmums un amats                                                        | Darbaspēks\_Uzņēmums Darbaspēks\_Atlīdzība Darbaspēks\_GeographicLocation Darbaspēks\_Veiktspēja Darbaspēks\_WorkerName Darbaspēks\_ReportsToWorkerName Darbaspēks\_CalendarOffset Darbaspēks\_Datums Darbaspēks\_WorkerTitle Darbaspēks\_Demogrāfiskie dati Darbaspēks\_Nodarbinātība Darbaspēks\_Darbs Darbaspēks\_WorkerBenefit                     |

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti satura pakotnē. Ja pārskatos un informācijas panelī vēlaties ietvert papildu aprēķinus, varat no LCS lejupielādēt un modificēt failu CompensationandBenefits.pbix. Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidošanai. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





