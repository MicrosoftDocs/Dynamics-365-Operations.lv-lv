---
title: Power BI satura pakotne Darbinieku attīstība
description: Šajā rakstā aprakstīts Darbinieku izstrādes Power BI saturs.
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
ms.openlocfilehash: 307a7ba2b885ba1437d5ef54c2f9d70ef00e2b14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284184"
---
# <a name="employee-development-power-bi-content"></a>Power BI satura pakotne Darbinieku attīstība

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstīts Darbinieku **izstrādes** Microsoft Power BI saturs.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie pārskati
Power BI satura pakotnes **Darbinieku attīstība** pārskatos ir ietvertas gan diagrammas, gan tabulas, kurās ir sniegta papildinformācija. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                        | Saturs |
|-------------------------------|----------|
| Darbinieku attīstības apskats | Citu pārskatu kopsavilkums |
| Darbinieku prasmju analīze       | Darbinieku prasmju tipi un darbinieku prasmes pēc tipa |
| Darbinieku prasmju līmeņa analīze | Darbinieku prasmju līmeņi pēc nodaļas, darbinieki pēc prasmju līmeņa un prasmju tipa, un augstākie līmeņi katrai prasmei |
| Prasmju profils                 | Prasmju profils atlasītajam darbiniekam |
| Prasmju analīze                | Prasmes pēc tipa un vērtējuma |
| Veiktspējas vērtējuma analīze   | Darbinieki pēc zemākā un augstākā vērtējuma pēc darba, darbinieku vērtējumi pēc nodaļas, darbinieki pēc vērtējuma un pozīcijas tipa un augstākie un zemākie vērtējumi pēc pozīcijas |
| Darbinieku veiktspējas analīze | Darbinieku vērtējumi atlasītajam vērtējumam pēc vadītāja |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana

| Elements                   | Saturs                                                                                                   | Attiecības ar citiem elementiem |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendāra nobīde          | Kalendārs nobīdās, lai sadalītu pārskatus                                                                          | Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieka tendence, Darbinieks, ar ko patrauktas darba attiecības |
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
| Darbs                      | Funkcija, tips un nosaukums                                                                                  | Pašreizējais darbinieks, Pašreizējā pozīcija, Darbinieka tendence, Darbam vēlamās prasmes, Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieks, ar kuru ir pārtrauktas darba attiecības |
| Darbam vēlamās prasmes      | Svarīgums, vērtējums, prasme un prasmes līmenis                                                                 | Amats |
| Darbinieku prasmju analīze  | Sertificēts, līmenis, līmeņa datums un prasme                                                                    | Darbinieka vārds, Prasme |
| Veiktspēja              | Vērtējums, apraksts un vērtēšanas modelis                                                                      | Pašreizējais darbinieks, Pašreizējā pozīcija, Darbinieka tendence, Darbam vēlamās prasmes, Iepriekšējās pozīcijas piešķire, Pozīcijas tendence, Darbinieks, ar kuru ir pārtrauktas darba attiecības |
| Prasme                    | Prasme, prasmes tips un vērtējums                                                                              | Darbinieku prasmju analīze, Darbam vēlamās prasmes |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
