---
title: Power BI satura pakotne Kompensācija
description: Šajā rakstā ir aprakstīts Kompensācijas Power BI saturs. Tajā skaidrots, kā piekļūt pārskatiem un sniedz informāciju par izmantoto datu modeli.
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
ms.search.form: HcmCompensationWorkspace
ms.openlocfilehash: 58d78dede753d8ed81a0e815b9ea02c69b70121f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291834"
---
# <a name="compensation-power-bi-content"></a>Power BI satura pakotne Kompensācija

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts **Kompensācijas** Microsoft Power BI saturs. Tajā ir paskaidrots, kā piekļūt pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
**Kompensācija** Power BI saturs tiek rādīts darbvietā **Kompensāciju pārvaldība**, ja izmantojat kādu no tālāk norādītajiem produktiem.

- Finanšu un operāciju programmas
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Power BI satura pakotnes **Kompensācija** pārskatos ir ietvertas gan diagrammas, gan tabulas, kurās ir sniegta papildinformācija. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                     | Saturs |
|----------------------------|----------|
| Pārskats par atlīdzību      | Citu pārskatu kopsavilkums |
| Atlīdzības analīze      | Stundu darba un algoto darbinieku skaits pēc uzņēmuma, kopējais darbinieku skaits pēc atlīdzības plāna, vīriešu un sieviešu skaits pēc atlīdzības plāna un atlīdzība darbiniekiem pēc nodaļas |
| Pozīciju apmaksas analīze      | Lielākā un mazākā stundu darba un algas apmaksa, vislabāk un vissliktāk apmaksātās pozīcijas un pilnas slodzes un pusslodzes pozīcijas |
| Atlīdzības plāna analīze | Darbinieka reģistrācija pēc atlasītā atvieglojuma |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Power BI satura pakotnes **Kompensācija** pārskatu aizpildīšanai tiek izmantoti tālāk norādītie dati. Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti satura izveidei.

| Elements                   | Saturs                                                                                                   | Attiecības ar citiem elementiem |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendāra nobīde          | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          | Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieka tendence, Darbinieks, ar ko patrauktas darba attiecības |
| Uzņēmums                  | Uzņēmumi, pēc kuriem pārskatus filtrēt                                                                             | Pašreizējā atlīdzība, Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Atlīdzība             | Apmaksas likme un frekvence laika gaitā                                                                           | Pašreizējā atlīdzība, Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Pašreizējā atlīdzība     | Apmaksas likme un frekvence pašreizējā datumā                                                              | Uzņēmums, Atlīdzība, Demogrāfiskie dati, Darbs, Pozīcija |
| Pašreizējā pozīcija         | Amati ir pašreizējā datuma, pilna laika ekvivalenta (full-time equivalent — FTE) atvērti amati/vakances, un amati, kas ir atvērti līdz aizpildīšanai | Darbs, Pozīcija |
| Pašreizējais darbinieks         | Nodarbinātie pašreizējā datumā, vecums un skaits                                                         | Uzņēmums, Atlīdzība, Ģeogrāfiskā vieta, Darbinieka vārds, Pārskati par, Darbinieka amats, Demogrāfiskie dati, Darbs, Nodarbinātība, Pozīcija, Atvieglojumi |
| Datums                     | Dienas, nedēļas, mēneši un gadi                                                                             | Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieks, ar ko patrauktas darba attiecības, Darbinieka tendence |
| Demogrāfiskie dati             | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis                                                   | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Nodarbinātība               | Sākuma datums, beigu datums un pārejas datums                                                                  | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Ģeogrāfiskā atrašanās vieta      | Pilsēta, novads, pasta indekss un štats vai reģions                                                           | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Amats                      | Funkcija, tips un nosaukums                                                                                  | Pašreizējā pozīcija, Pašreizējais darbinieks |
| Iepriekšējā amata piešķire | Piešķiršanas iemesls, sākuma datums, beigu datums un darbs                                                           | Kalendāra nobīde, Datums, Darbs, Pozīcija |
| Pozīcija                 | Nodaļa, FTE, amats, amata tips un nosaukums                                                        | Pašreizējā pozīcija, Pašreizējais darbinieks |
| Amata tendence           | Amati laika gaitā, FTE un darbs                                                                          | Kalendāra nobīde, Datums, Darbs, Pozīcija |
| Pārskati par               | Vārds, uzvārds un pilnais vārds                                                                       | Pašreizējais nodarbinātais, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieks, ar kuru ir pārtrauktas darba attiecības      | Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības, pārtraukšanas datums, amats, pozīcija un darbs                                           | Uzņēmums, Atlīdzība, Ģeogrāfiskā vieta, Darbinieka vārds, Pārskati par, Kalendāra nobīde, Datums, Darbinieka amats, Demogrāfiskie dati, Nodarbinātība, Darbs, Pozīcija, Atvieglojumi |
| Atvieglojumi                 | Spēkā stāšanās datums, atvieglojumu opcija, atvieglojumu plāns un atvieglojumu tips                                             | Pašreizējais nosaukums, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieka vārds            | Vārds, uzvārds un pilnais vārds                                                                       | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieka amats           | Nosaukums un darba stāža datums                                                                                   | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieka tendence           | Nodarbinātie laika gaitā, skaits, uzņēmums un amats                                                        | Uzņēmums, Atlīdzība, Ģeogrāfiskā vieta, Darbinieka vārds, Pārskati par, Kalendāra nobīde, Datums, Darbinieka amats, Demogrāfiskie dati, Nodarbinātība, Darbs, Atvieglojumi |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
