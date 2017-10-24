---
title: "Power BI saturs Darbinieku attīstība"
description: "Šajā tēmā ir aprakstīts Power BI saturs Darbinieku attīstība. Tajā ir paskaidrots, kā piekļūt pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 91f7071cc759686dd90b5893adaf58d1521e9185
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="employee-development-power-bi-content"></a>Power BI saturs Darbinieku attīstība

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts Microsoft Power BI saturs **Darbinieku attīstība**. Tajā ir paskaidrots, kā piekļūt pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam

Ja lietojat programmatūru Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs), tad satura pakotne **Darbinieku attīstība** ir atrodama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un saistīt to ar saviem datiem, skatiet tēmā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Power BI satura pakotnē **Darbinieku attīstība** ietvertajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                        | Saturs |
|-------------------------------|----------|
| Darbinieku attīstības apskats | Citu pārskatu kopsavilkums |
| Darbinieku prasmju analīze       | Darbinieku prasmju tipi un darbinieku prasmes pēc tipa |
| Darbinieku prasmju līmeņa analīze | Darbinieku prasmju līmeņi pēc nodaļas, darbinieki pēc prasmju līmeņa un prasmju tipa, un augstākie līmeņi katrai prasmei |
| Prasmju profils                 | Prasmju profils atlasītajam darbiniekam |
| Prasmju analīze                | Prasmes pēc tipa un vērtējuma |
| Veiktspējas vērtējuma analīze   | Darbinieki pēc zemākā un augstākā vērtējuma pēc darba, darbinieku vērtējumi pēc nodaļas, darbinieki pēc vērtējuma un pozīcijas tipa un augstākie un zemākie vērtējumi pēc pozīcijas  |
| Darbinieku veiktspējas analīze | Darbinieku vērtējumi atlasītajam vērtējumam pēc vadītāja |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
| Elements                   | Saturs                                                                                                   | Attiecības ar citiem elementiem |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendāra nobīde          | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          | Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieka tendence, Darbinieks, ar ko patrauktas darba attiecības 
| Uzņēmums                  | Uzņēmumi, pēc kuriem pārskatus filtrēt                                                                             | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Pašreizējā pozīcija         | Amati ir pašreizējā datuma, pilna laika ekvivalenta (full-time equivalent — FTE) atvērti amati/vakances, un amati, kas ir atvērti līdz aizpildīšanai | Darbs, Pozīcija |
| Pašreizējais darbinieks         | Nodarbinātie pašreizējā datumā, vecums un skaits                                                         | Uzņēmums, Ģeogrāfiskā vieta, Darbinieka vārds, Kam atskaitās, Darbinieka amats, Demogrāfiskie dati, Darbs, Nodarbinātība, Pozīcija |
| Datums                     | Dienas, nedēļas, mēneši un gadi                                                                             | Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieks, ar ko patrauktas darba attiecības, Darbinieka tendence |
| Demogrāfiskie dati             | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis                                                   | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Nodarbinātība               | Sākuma datums, beigu datums un pārejas datums                                                                  | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Ģeogrāfiskā atrašanās vieta      | Pilsēta, novads, pasta indekss un štats vai reģions                                                           | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Amats                      | Funkcija, tips un nosaukums                                                                                  | Pašreizējā pozīcija, Pašreizējais darbinieks |
| Iepriekšējā amata piešķire | Piešķiršanas iemesls, sākuma datums, beigu datums un darbs                                                           | Kalendāra nobīde, Datums, Darbs, Pozīcija |
| Pozīcija                 | Nodaļa, FTE, amats, amata tips un nosaukums                                                        | Pašreizējā pozīcija, Pašreizējais darbinieks |
| Amata tendence           | Amati laika gaitā, FTE un darbs                                                                          | Kalendāra nobīde, Datums, Darbs, Pozīcija |
| Kam atskaitās               | Vārds, uzvārds un pilnais vārds                                                                       | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieks, ar kuru ir pārtrauktas darba attiecības      | Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības, pārtraukšanas datums, nosaukums, amats un darbs                                             | Uzņēmums, Ģeogrāfiskā vieta, Darbinieka vārds, Kam atskaitās, Kalendāra nobīde, Datums, Darbinieka amats, Demogrāfiskie dati, Nodarbinātība, Darbs, Pozīcija |
| Darbinieka vārds            | Vārds, uzvārds un pilnais vārds                                                                       | Pašreizējais nodarbinātais, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieka amats           | Nosaukums un darba stāža datums                                                                                   | Pašreizējais darbinieks, Darbinieks, ar kuru ir pārtrauktas darba attiecības, Darbinieka tendence |
| Darbinieka tendence           | Nodarbinātie laika gaitā, skaits, uzņēmums un amats                                                        | Uzņēmums, Ģeogrāfiskā vieta, Darbinieka vārds, Kam atskaitās, Kalendāra nobīde, Datums, Darbinieka amats, Demogrāfiskie dati, Nodarbinātība, Darbs |
| Darbs                      | Funkcija, tips un nosaukums                                                                                      | Pašreizējais darbinieks, Pašreizējā pozīcija, Darbinieka tendence, Darbam vēlamās prasmes, Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieks, ar kuru ir pārtrauktas darba attiecības |
| Darbam vēlamās prasmes      | Svarīgums, vērtējums, prasme un prasmes līmenis                                                                 | Amats |
| Darbinieku prasmju analīze  | Sertificēts, līmenis, līmeņa datums un prasme                                                                    | Darbinieka vārds, Prasme |  
| Veiktspēja              | Vērtējums, apraksts un vērtēšanas modelis                                                                      | Pašreizējais darbinieks, Pašreizējā pozīcija, Darbinieka tendence, Darbam vēlamās prasmes, Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieks, ar kuru ir pārtrauktas darba attiecības |
|  Prasme                   | Prasme, prasmes tips un vērtējums                                                                              | Darbinieku prasmju analīze, Darbam vēlamās prasmes |                                                                                                                        

Šie elementi tika izmantoti, lai datu modelī izveidotu aprēķinātus mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti Power BI saturā. Ja vēlaties pārskatos vai informācijas panelī ietvert papildu aprēķinus, varat lejupielādēt .pbix formāta failu no pakalpojuma LCS un izmainīt to. Šis fails ir noklusējuma datu modelis, kas tika izmantots Power BI satura izveidošanai. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

