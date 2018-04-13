---
title: "Power BI saturs Apmācība"
description: "Šajā tēmā ir aprakstīts Power BI saturs Apmācība."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: e5a78812aabaa5c835fe23787a9cbb57d1a7770e
ms.contentlocale: lv-lv
ms.lasthandoff: 12/19/2017

---

# <a name="learning-power-bi-content"></a>Power BI saturs Apmācība

[!INCLUDE [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts Microsoft Power BI saturs **Apmācība**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Power BI saturā **Apmācība** iekļautajos pārskatos ir ietvertas gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                | Saturs |
|-----------------------|----------|
| Apmācības apskats     | Citu pārskatu kopsavilkums |
| Kursa analīze       | Reģistrācija pēc atrašanās vietas, dalībnieks pēc statusa, kursi pēc tipa katram uzņēmumam un kursu apmeklētība pēc darba |
| Reģistrācijas analīze | Reģistrācijas saraksts |
| Kursu veidi          | Kursu tipi pēc prasmēm |
| Instruktoru analīze   | Kursu un instruktoru koeficients, instruktoru skaits, kursi pēc instruktora, kursi katram instruktoram un kursu darba kārtība pēc instruktora |
| Piedāvātie kursi       | Kursu saraksts |
| Kursu veidošana        | Kursu darba kārtība |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Power BI saturā **Apmācība** ietverto pārskatu aizpildīšanai tiek izmantoti tālāk norādītie dati. Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti satura izveidei.

| Elements           | Saturs                                                         | Attiecības ar citiem elementiem |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalendāra nobīde  | Kalendārs nobīdās, lai sadalītu pārskatus                                | Kursa darba kārtība, kursa dalībnieki |
| Uzņēmums          | Uzņēmumi, pēc kuriem pārskatus filtrēt                                   | Kursa darba kārtība, kursa dalībnieki |
| Kursi           | Kurss, apraksts, instruktora vārds, atrašanās vieta, telpa un statuss | Kursa darba kārtība, kursa dalībnieki, kursa prasme |
| Kursa darba kārtība    | Darba kārtība, kurss un sākuma un beigu laiks                          | Uzņēmums, kalendāra nobīde, datums, kurss |
| Kursa dalībnieki | Vārds, statuss, amats un reģistrācijas datums                         | Uzņēmums, kalendāra nobīde, datums, kurss, demogrāfiskie dati, nodarbinātība, kurss, darbinieka vārds, darbinieka amats, darbs, pozīcija |
| Kursa prasme     | Prasme, prasmes veids un līmenis                                     | Kursi |
| Datums             | Dienas, nedēļas, mēneši un gadi                                   | Kursa darba kārtība, kursa dalībnieki |
| Demogrāfiskie dati     | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis         | Kursa darba kārtība, kursa dalībnieki |
| Nodarbinātība       | Sākuma datums, beigu datums un pārejas datums                        | Kursa darba kārtība, kursa dalībnieki |
| Amats              | Funkcija, tips un nosaukums                                        | Kursa darba kārtība, kursa dalībnieki |
| Pozīcija         | Pozīcija, amats un pilnas slodzes ekvivalents (FTE)                  | Kursa darba kārtība, kursa dalībnieki |
| Darbinieka vārds    | Vārds, uzvārds un pilnais vārds                             | Kursa dalībnieki |
| Darbinieka amats   | Nosaukums un darba stāža datums                                         | Kursa dalībnieki |



