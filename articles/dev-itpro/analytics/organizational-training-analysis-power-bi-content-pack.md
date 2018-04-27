---
title: "Power BI saturs Organizācijas apmācības"
description: "Šajā tēmā ir aprakstīta Finance and Operations Power BI satura pakotne Organizācijas apmācība."
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
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 18567a3241fce02e17df368f544e545fad93e1d9
ms.contentlocale: lv-lv
ms.lasthandoff: 03/23/2018

---

# <a name="organizational-training-power-bi-content"></a>Power BI saturs Organizācijas apmācības

[!INCLUDE [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Finance and Operations Power BI satura pakotne Organizācijas apmācība. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Kad ir izveidots satura pakotnes savienojums ar jūsu Finance and Operations datiem, pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats          | Saturs                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursa analīze | Reģistrācija pēc atrašanās vietas, kursa dalībnieki pēc statusa un reģistrācijas saraksts |
| Kursu veidi    | Kursu tipi pēc prasmēm                                                       |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Satura pakotnes Organizācijas apmācība pārskatu aizpildīšanai tiek izmantoti Finance and Operations dati. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

| Elements                    | Saturs                                                         | Attiecības ar citiem elementiem                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalendārs nobīdās, lai sadalītu pārskatus                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Uzņēmumi, pēc kuriem pārskatus filtrēt                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Kurss, apraksts, instruktora vārds, atrašanās vieta, telpa un statuss | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Darba kārtība, kurss un sākuma un beigu laiks                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Vārds, statuss, amats un reģistrācijas datums                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Prasme, prasmes veids un līmenis                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Dienas, nedēļas, mēneši un gadi                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Sākuma datums, beigu datums un pārejas datums                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Funkcija, tips un nosaukums                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Pozīcija, amats un pilnas slodzes ekvivalents (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Vārds, uzvārds un pilnais vārds                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Nosaukums un darba stāža datums                                         | Training\_CourseAttendees                                                                                                                                                                          |





