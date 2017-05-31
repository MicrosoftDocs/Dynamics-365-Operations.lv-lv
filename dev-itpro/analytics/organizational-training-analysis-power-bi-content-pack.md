---
title: "Power BI satura pakotne Organizācijas apmācība"
description: "Šajā tēmā ir aprakstīta Dynamics 365 for Operations Power BI satura pakotne Organizācijas apmācība. Tajā ir paskaidrots, kā piekļūt satura pakotnei, un ir izskaidrots satura pakotnes izstrādei izmantotais datu modelis un elementi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e1bfe405e2e4bf6445567d966ab20bd8645f8dbf
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="organizational-training-power-bi-content"></a>Power BI satura pakotne Organizācijas apmācība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīta Dynamics 365 for Operations Power BI satura pakotne Organizācijas apmācība. Tajā ir paskaidrots, kā piekļūt satura pakotnei, un ir izskaidrots satura pakotnes izstrādei izmantotais datu modelis un elementi.

<a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
--------------------------

Satura pakotne Organizācijas apmācība ir pieejama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un to savienot ar saviem Microsoft Dynamics 365 for Operations datiem, skatiet rakstā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Pēc tam, kad ir izveidots satura pakotnes savienojums ar jūsu Dynamics 365 for Operations datiem, pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats          | Saturs                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursa analīze | Reģistrācija pēc atrašanās vietas, kursa dalībnieki pēc statusa un reģistrācijas saraksts |
| Kursu veidi    | Kursu tipi pēc prasmēm                                                       |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Satura pakotnes Organizācijas apmācība pārskatu aizpildīšanai tiek izmantoti Dynamics 365 for Operations dati. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

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

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti satura pakotnē. Ja vēlaties pārskatos vai informācijas panelī ietvert papildu aprēķinus, varat no LCS lejupielādēt un modificēt failu Training.pbix. Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidošanai. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





