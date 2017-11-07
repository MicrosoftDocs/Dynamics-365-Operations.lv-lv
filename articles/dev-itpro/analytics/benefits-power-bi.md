---
title: "Power BI satura pakotne Atvieglojumi"
description: "Šajā tēmā ir aprakstīta Power BI satura pakotne Atvieglojumi. Tajā ir paskaidrots, kā piekļūt ietvertajiem pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e650047473136d1aaf455e96f9d7c63a426563f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="benefits-power-bi-content"></a>Power BI satura pakotne Atvieglojumi

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Microsoft Power BI satura pakotne **Atvieglojumi**. Tajā ir paskaidrots, kā piekļūt ietvertajiem pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Power BI satura pakotne **Atvieglojumi** tiek rādīta darbvietā **Atvieglojumu pārvaldība**, ja izmantojat kādu no tālāk norādītajiem produktiem.

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs)
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Power BI satura pakotnē **Atvieglojumi** iekļautajos pārskatos ir ietvertas gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                       | Saturs                                                                                       |
|------------------------------|------------------------------------------------------------------------------------------------|
| Pārskats par reģistrēšanos atvieglojumiem  | Vispopulārākie un vismazāk populārie plāni pēc reģistrāciju skaita, reģistrāciju skaits pēc darbinieku grupas un atlasītā atvieglojumu plāna opcijas |
| Darbinieka atvieglojumi            | Darbinieka reģistrācija pēc atlasītā atvieglojuma                                                        |
                                                                                             
Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Power BI satura paplašināšana
Izmantojot pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) pieejamās satura pakotnes, varat nodrošināt lielisku analīzes funkcionalitāti personām, kuras nepierakstās programmatūrā Dynamics 365 for Finance and Operations. Varat izmainīt šīs satura pakotnes, tajās ietverot citus pārskatus vai vizualizācijas, un pēc tam publicēt tās savā Power BI.com nomniekā analīzes veikšanai.

Power BI satura pakotne **Atvieglojumi** ir pieejama LCS koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt satura pakotni un ieviest to savā organizācijā, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md). Power BI satura pakotnes implementēšanas demonstrāciju skatiet tēmā [Power BI saturs pakalpojumā Dynamics Lifecycle Services no Microsoft un jūsu partneriem](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

>[!NOTE]
>Pakalpojumā Lifecycle Services pieejamie .pbix formāta faili ir paredzēti tikai programmatūrai Dynamics 365 for Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Power BI satura pakotnē **Atvieglojumi** ietverto pārskatu aizpildīšanai tiek izmantoti tālāk norādītie dati. Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti satura izveidei.

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

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un satura pakotnē ietverto pārskatu datus. Ja vēlaties pārskatos vai informācijas panelī ietvert papildu aprēķinus, varat lejupielādēt .pbix formāta failu no pakalpojuma LCS un izmainīt to. Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidei. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

