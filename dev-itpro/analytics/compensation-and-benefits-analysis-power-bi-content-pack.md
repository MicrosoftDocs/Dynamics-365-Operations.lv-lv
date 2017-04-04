---
title: "Kompensāciju un pabalstu Power BI saturu"
description: "Šajā tēmā ir aprakstīts, Dynamics 365 operācijām - kompensāciju un pabalstu Power BI satura. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne."
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

# <a name="compensation-and-benefits-power-bi-content"></a>Kompensāciju un pabalstu Power BI saturu

Šajā tēmā ir aprakstīts, Dynamics 365 operācijām - kompensāciju un pabalstu Power BI satura. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne.

<a name="accessing-the-content-pack"></a>Piekļūstot satura pakotni
--------------------------

Jūs varat atrast kompensāciju un pabalstu satura pakotne bibliotēkā Shared aktīvu programmā Microsoft Dynamics Lifecycle Services (LCS). Lai iegūtu papildinformāciju par satura pakotnes lejupielāde un izveidojiet savienojumu ar savu Microsoft Dynamics 365 darbības datiem, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Atskaitēm, kas ir iekļautas satura pakotni
Pēc satura pakotne savienojuma izveidošanas ar savu dinamiku 365 darbības datiem, ziņojumi liecina uzņēmuma dati. Ja jūs nekad neesmu lietojis Microsoft Power BI pirms, jūs varat uzzināt vairāk par to uz [vadīto mācību lapas Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Atskaitēm, kas ir iekļautas satura pakotne ir gan diagrammām un tabulām, kas satur papildu informāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                     | Saturs                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| COMP un labumu analīze | Stundas un algoti darbinieki, uzņēmumu, vidējais stundu apmaksu, algoti vidējās algas, darbinieku pēc nodarbinātības veida un plānot iesaistīšanās |
| Darbinieka pabalsti          | Darbinieku iesaistīšanās ar atlasītajiem labuma                                                                                               |

Varat filtrēt diagrammas un mozaīkas uz šiem ziņojumiem, un pin diagrammām un flīžu panelis. Papildinformāciju par to, kā filtrēt un pin barošanas BI sk [Create and Configure A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
365. dinamika attiecībā uz darbības datiem tiek lietota, lai aizpildītu kompensāciju un pabalstu satura pakotnes ziņojumi. Tabulā ir norādīti satura pakotne tika balstīta uz juridiskajām personām.

| Elements                            | Saturs                                                                                                   | Relācijas ar citām entītijām                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbaspēks\_CalendarOffset         | Kalendārs, kas nobīda slāņa ziņojumus                                                                          | Darbaspēks\_PastPositionAssignment darbaspēka\_PositionTrend Workorce\_WorkerTrend darbaspēka\_TerminatedWorker                                                                                                                                                                                                                     |
| Darbaspēks\_uzņēmums                | Uzņēmumiem, lai filtrētu pārskatus                                                                             | Darbaspēks\_CurrentCompensation darbaspēka\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Darbaspēks\_kompensācijas           | Apmaksas likmes un frekvenču, laika gaitā                                                                           | Darbaspēks\_CurrentCompensation darbaspēka\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Darbaspēks\_CurrentCompensation    | Apmaksas likmes un frekvenču pašreizējā datumā                                                              | Darbaspēks\_uzņēmuma darbaspēka\_kompensāciju darbaspēka\_demogrāfijas darbaspēka\_darbu darbaspēka\_pozīciju                                                                                                                                                                                                                            |
| Darbaspēks\_CurrentPosition        | Pozīcijas pašreizējā datumā pilna darba laika ekvivalentu (FTE), atveriet pozīcijām un pozīcijām atvērt piepildīta | Darbaspēks\_darbu darbaspēka\_stāvoklis                                                                                                                                                                                                                                                                                               |
| Darbaspēks\_CurrentWorker          | Darba ņēmēju, sākot ar pašreizējo datumu, vecumu un darbinieku skaits                                                         | Darbaspēks\_uzņēmuma darbaspēka\_kompensāciju darbaspēka\_GeographicLocation darbaspēka\_veiktspējas darbaspēka\_WorkerName darbaspēka\_ReportsToWorkerName darbaspēka\_WorkerTitle darbaspēka\_demogrāfijas darbaspēka\_darbu darbaspēka\_darbaspēka nodarbinātības\_pozīciju darbaspēka\_WorkerBenefit                                            |
| Darbaspēks\_datums                   | Dienas, nedēļas, mēneši un gadi                                                                             | Darbaspēks\_PastPositionAssignment darbaspēka\_PositionTrend darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Darbaspēks\_demogrāfija           | Dienas, dzimšanas, dzimuma, etniskās piederības un ģimenes stāvoklis                                                   | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_nodarbinātības             | Sākuma datums, beigu datums un pārejas datumu                                                                  | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_GeographicLocation     | Pilsētas, pagasta, pasta indeksu un rajons                                                           | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_darba                    | Funkciju, tipu un nosaukumu                                                                                  | Darbaspēks\_CurrentPosition darbaspēka\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Darbaspēks\_PastPositionAssignment | Piešķiršanas iemesls, sākuma datums, beigu datums un darba                                                           | Darbaspēks\_CalendarOffset darbaspēka\_datums darbaspēka\_darbu darbaspēka\_pozīciju                                                                                                                                                                                                                                                     |
| Darbaspēks\_Performance            | Novērtējums, apraksts un novērtējuma modelis                                                                      | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_stāvoklis               | Departaments, FTE, pozīciju, novietojuma tipu un nosaukumu                                                        | Darbaspēks\_CurrentPosition darbaspēka\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Darbaspēks\_PositionTrend          | Nostājas, laika gaitā, FTE, un darbs                                                                          | Darbaspēks\_CalendarOffset darbaspēka\_datums darbaspēka\_darbu darbaspēka\_pozīciju                                                                                                                                                                                                                                                     |
| Darbaspēks\_ReportsToWorkerName    | Vārdu, uzvārdu un vārdu un uzvārdu                                                                       | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_prasmju                  | Iemaņu, prasmju tipu un vērtējums                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Darbaspēks\_TerminatedWorker       | Pārtraukta, strādnieku, izbeigšanas datumu, virsrakstu, nostāju un darbu                                             | Darbaspēku\_uzņēmuma darbaspēka\_kompensāciju darbaspēka\_GeographicLocation darbaspēka\_sniegumu darbaspēka\_WorkerName darbaspēka\_ReportsToWorkerName darbaspēka\_CalendarOffset darbaspēks\_datums darbaspēka\_WorkerTitle darbaspēka\_demogrāfijas darbaspēka\_darbaspēka nodarbinātības\_darbu darbaspēka\_pozīciju darbaspēka\_WorkerBenefit |
| Darbaspēks\_WorkerBenefit          | Spēkā stāšanās dienas, labu iespēju, pabalstu plāna un atvieglojumu tipa                                             | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_WorkerName             | Vārdu, uzvārdu un vārdu un uzvārdu                                                                       | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Darbaspēks\_WorkerTitle            | Virsraksts un darba stāža datums                                                                                   | Darbaspēks\_CurrentWorker darbaspēka\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Darbinieku laika gaitā, darbinieku, sabiedrības, un pozīcija                                                        | Darbaspēku\_uzņēmuma darbaspēka\_kompensāciju darbaspēka\_GeographicLocation darbaspēka\_sniegumu darbaspēka\_WorkerName darbaspēka\_ReportsToWorkerName darbaspēka\_CalendarOffset darbaspēks\_datums darbaspēka\_WorkerTitle darbaspēka\_demogrāfijas darbaspēka\_darbaspēka nodarbinātības\_darbu darbaspēka\_WorkerBenefit                     |

Šīm vienībām tika izmantoti, lai izveidotu aprēķinātās mērvienības datu modelī. Tās aprēķina, pasākumus, kas pēc tam tiek izmantoti, lai aprēķinātu galveno veiktspējas rādītāju (KPI) un atskaites, kas tiek izmantotas satura pakotne. Ja jūs vēlaties iekļaut jūsu atskaites un informācijas paneļa papildu aprēķinus, var lejupielādēt un modificēt LCS CompensationandBenefits.pbix failu. Šis fails ir noklusēto datu modelis, kas tika izmantots, lai izveidotu satura pakotne. Pēc tam, kad esat veicis izmaiņas, var izveidot organizācijas satura pakotne un vadības paneli, kas satur informāciju, ko esat pievienojis.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



