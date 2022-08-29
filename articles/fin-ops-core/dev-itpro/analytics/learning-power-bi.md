---
title: Power BI satura pakotne Mācības
description: Šis raksts apraksta apmācību Power BI saturu.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a7aca9e47ed26dcb4ef7f4b9aee72987e2d8fdd2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273965"
---
# <a name="learning-power-bi-content"></a>Power BI satura pakotne Mācības

[!include [banner](../includes/banner.md)]

Šis raksts apraksta **apmācību** Microsoft Power BI saturu.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati

Power BI satura pakotnes **Mācības** pārskatos ir ietvertas gan diagrammas, gan tabulas, kurās ir sniegta papildinformācija. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                | Saturs |
|-----------------------|----------|
| Apmācības apskats     | Citu pārskatu kopsavilkums |
| Kursa analīze       | Reģistrācija pēc atrašanās vietas, dalībnieks pēc statusa, kursi pēc tipa katram uzņēmumam un kursu apmeklētība pēc darba |
| Reģistrācijas analīze | Reģistrācijas saraksts |
| Kursu veidi          | Kursu tipi pēc prasmēm |
| Instruktoru analīze   | Kursu un instruktoru koeficients, instruktoru skaits, kursi pēc instruktora, kursi katram instruktoram un kursu darba kārtība pēc instruktora |
| Piedāvātie kursi       | Kursu saraksts |
| Kursu veidošana        | Kursu darba kārtība |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

Power BI satura pakotnes **Mācības** pārskatu aizpildīšanai tiek izmantoti tālāk norādītie dati. Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti satura izveidei.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
