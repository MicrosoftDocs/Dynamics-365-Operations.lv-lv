---
title: Power BI satura pakotne Atvieglojumi
description: Šajā tēmā ir aprakstīta Power BI satura pakotne Atvieglojumi.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0e7cadc16c5ed6c6eab8c90090cac017221f63f466115b04a6a3b843db44b1c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733175"
---
# <a name="benefits-power-bi-content"></a>Power BI satura pakotne Atvieglojumi

[!include [banner](../includes/banner.md)]

Šajā aprakstīts Microsoft Power BI saturs **Atvieglojumi**. Tajā ir paskaidrots, kā piekļūt ietvertajiem pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Atvieglojumi** tiek rādīta darbvietā **Atvieglojumu pārvaldība**, ja izmantojat kādu no tālāk norādītajiem produktiem.

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Power BI satura pakotnes **Atvieglojumi** pārskatos ir ietvertas gan diagrammas, gan tabulas, kurās ir sniegta papildinformācija. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                      | Saturs                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Pārskats par reģistrēšanos atvieglojumiem | Vispopulārākie un vismazāk populārie plāni pēc reģistrāciju skaita, reģistrāciju skaits pēc darbinieku grupas un atlasītā atvieglojumu plāna opcijas |
| Darbinieka atvieglojumi           | Darbinieka reģistrācija pēc atlasītā atvieglojuma                                                        |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Power BI satura pakotnes **Atvieglojumi** pārskatu aizpildīšanai tiek izmantoti tālāk norādītie dati. Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti satura izveidei.

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