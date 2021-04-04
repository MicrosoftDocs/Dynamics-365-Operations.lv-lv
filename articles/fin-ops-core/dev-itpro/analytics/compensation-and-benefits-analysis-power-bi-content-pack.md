---
title: Power BI satura pakotne Kompensācija un atvieglojumi
description: Šajā tēmā ir aprakstīta Power BI satura pakotne Kompensācija un atvieglojumi.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07a8be0a4c333e9d465341d9384e4b9a706f9e75
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559825"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Power BI satura pakotne Kompensācija un atvieglojumi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Power BI satura pakotne Kompensācija un atvieglojumi. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Kad ir izveidots satura pakotnes savienojums ar jūsu datiem, pārskatos tiek rādīti jūsu organizācijas dati. Ja nekad neesat lietojis Microsoft Power BI, varat par to vairāk uzzināt rakstā [Power BI vadītās mācīšanās lapa](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                     | Saturs                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Atlīdzību un atvieglojumu analīze | Stundu darba un algotie darbinieki pēc uzņēmuma, vidējā stundas samaksa, vidējā algotā samaksa, darbinieki pēc nodarbinātības tipa un plāna reģistrācija |
| Darbinieka atvieglojumi          | Darbinieka reģistrācija pēc atlasītā atvieglojuma                                                                                               |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Satura pakotnes Atlīdzība un atvieglojumi pārskatu aizpildīšanai tiek izmantoti programmas dati. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

| Elements                            | Saturs                                                                                                   | Attiecības ar citiem elementiem |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          | Darbaspēks\_PastPositionAssignment, Workforce\_PositionTrend, Workorce\_WorkerTrend, Workforce\_TerminatedWorker |
| Workforce\_Company                | Uzņēmumi, pēc kuriem pārskatus filtrēt                                                                             | Darbaspēks\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_Compensation           | Apmaksas likme un frekvence laika gaitā                                                                           | Darbaspēks\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_CurrentCompensation    | Apmaksas likme un frekvence pašreizējā datumā                                                              | Darbaspēks\_Uzņēmums, Darbaspēks\_Atlīdzība, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_CurrentPosition        | Amati ir pašreizējā datuma, pilna laika ekvivalenta (full-time equivalent — FTE) atvērti amati/vakances, un amati, kas ir atvērti līdz aizpildīšanai | Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentWorker          | Nodarbinātie pašreizējā datumā, vecums un skaits                                                         | Darbaspēks\_Uzņēmums, Darbaspēks\_Atlīdzība, Darbaspēks\_GeographicLocation, Darbaspēks\_Veiktspēja, Darbaspēks\_WorkerName, Darbaspēks\_ReportsToWorkerName, Darbaspēks\_WorkerTitle, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Darbs, Darbaspēks\_Nodarbinātība, Darbaspēks\_Amats, Darbaspēks\_WorkerBenefit |
| Workforce\_Date                   | Dienas, nedēļas, mēneši un gadi                                                                             | Darbaspēks\_PastPositionAssignment, Workforce\_PositionTrend, Workorce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_Employment             | Sākuma datums, beigu datums un pārejas datums                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_GeographicLocation     | Pilsēta, novads, pasta indekss un štats vai reģions                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_Job                    | Funkcija, tips un nosaukums                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | Piešķiršanas iemesls, sākuma datums, beigu datums un darbs                                                           | Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_Performance            | Vērtējums, apraksts un vērtēšanas modelis                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_Position               | Nodaļa, FTE, amats, amata tips un nosaukums                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Amati laika gaitā, FTE un darbs                                                                          | Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_Darbs, Darbaspēks\_Amats |
| Workforce\_ReportsToWorkerName    | Vārds, uzvārds un pilnais vārds                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_Skill                  | Prasme, prasmes tips un vērtējums                                                                              | |
| Darbaspēks\_TerminatedWorker       | Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības, pārtraukšanas datums, nosaukums, amats un darbs                                             | Darbaspēks\_Uzņēmums, Darbaspēks\_Atlīdzība, Darbaspēks\_GeographicLocation, Darbaspēks\_Veiktspēja, Darbaspēks\_WorkerName, Darbaspēks\_ReportsToWorkerName, Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_WorkerTitle, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Nodarbinātība, Darbaspēks\_Darbs, Darbaspēks\_Amats, Darbaspēks\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Spēkā stāšanās datums, atvieglojumu opcija, atvieglojumu plāns un atvieglojumu tips                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_WorkerName             | Vārds, uzvārds un pilnais vārds                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workforce\_WorkerTitle            | Nosaukums un darba stāža datums                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workorce\_WorkerTrend |
| Workorce\_WorkerTrend            | Nodarbinātie laika gaitā, skaits, uzņēmums un amats                                                        | Darbaspēks\_Uzņēmums, Darbaspēks\_Atlīdzība, Darbaspēks\_GeographicLocation, Darbaspēks\_Veiktspēja, Darbaspēks\_WorkerName, Darbaspēks\_ReportsToWorkerName, Darbaspēks\_CalendarOffset, Darbaspēks\_Datums, Darbaspēks\_WorkerTitle, Darbaspēks\_Demogrāfiskie dati, Darbaspēks\_Nodarbinātība, Darbaspēks\_Darbs, Darbaspēks\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]