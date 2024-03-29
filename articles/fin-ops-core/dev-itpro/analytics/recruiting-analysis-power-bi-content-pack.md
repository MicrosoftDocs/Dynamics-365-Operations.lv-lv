---
title: Power BI satura pakotne Personāla atlase
description: Šajā rakstā ir aprakstīts Personāla atlases Power BI saturs.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.form: HcmRecruitmentWorkspace
ms.openlocfilehash: 412a1225544bb73649c9f0e703ec7b9a0d2613e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276602"
---
# <a name="recruiting-power-bi-content"></a>Power BI satura pakotne Personāla atlase

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts **Personāla atlases** Microsoft Power BI saturs. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Personāla atlase** tiek rādīta darbvietā **Personāla atlases pārvaldība**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Pārskati un vizualizācijas personāla atlases pārvaldības darbvietā
Darbvietā **Personāla atlases pārvaldība** ir cilne **Analīze**. Šajā cilnē ir iegults personāla atlasei paredzētais Power BI saturs. Saturs sastāv no pārskata cilnes un papildu cilnēm, kas satur detalizētu informāciju. Tabulā ir sniegts katras cilnes pārskatu apraksts.

| Pārskats               | Saturs |
|----------------------|----------|
| Pārskats par personāla atlasi | Citu pārskatu apkopojums |
| Kandidātu analīze   | Kandidātu kopskaits, kandidāti pēc amata, kandidātu avoti, kandidātu sieviešu skaits salīdzinājumā kandidātiem vīriešiem un kandidāti pēc atrašanās vietas |
| Kandidāta statuss     | Kandidāti pēc veida un statusa un kandidāta statuss |
| Personāla atlases analīze  | Neto pieņemšanas darbā attiecība, vidējais dienu skaits līdz pieņemšanai darbā, neveiksmīgie pieņemšanas darbā gadījumi procentos un personāla atlases izmaksas, personāla atlases projektu skaits, lietotā pieņemšana darbā un kandidāti salīdzinājumā ar vakancēm pēc personāla atlases projekta |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Papildinformāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Informācijas paneļa izveide un konfigurēšana](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Tālāk esošajā tabulā ir norādīti Power BI satura pakotnes **Personāla atlase** izveidei izmantotie elementi.

| Elements               | Saturs                                                         | Attiecības ar citiem elementiem |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Kandidāts            | Kandidāti, pieņemtie kandidāti, neto pieņemšanas darbā attiecība un izmaksas          | Kandidāta vārds, uzņēmums, kalendāra nobīde, datums, ģeogrāfiskā atrašanās vieta, demogrāfiskie dati, amats, multivide, personāla atlases projekts |
| Kandidāta vārds       | Kandidāta vārds, uzvārds un pilns vārds                   | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Kalendāra nobīde      | Kalendārs nobīdās, lai sadalītu pārskatus                                | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Uzņēmums              | Uzņēmumi, pēc kuriem pārskatus filtrēt                                   | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Datums                 | Dienas, nedēļas, mēneši un gadi                                   | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Demogrāfiskie dati         | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis         | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Darbā pieņemtais kandidāts   | Kandidāts, veiktspēja, sākuma datums un kandidāta veids           | Uzņēmums, kalendāra nobīde, datums, ģeogrāfiskā atrašanās vieta, kandidāta vārds, nodarbinātība, veiktspēja, amats, multivide, personāla atlases projekts |
| Nodarbinātība           | Sākuma datums, beigu datums un pārejas datums                        | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Ģeogrāfiskā vieta  | Pilsēta, novads, pasta indekss un štats vai reģions                 | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Amats                  | Funkcija, tips un nosaukums                                        | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Plašsaziņas līdzekļi                | Kandidātu avots                                             | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Veiktspēja          | Vērtējums, apraksts un vērtēšanas modelis                            | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Personāla atlases projekts  | Projekta apraksts, projekta statuss un vakances                | Kandidāts, darbā pieņemtais kandidāts, atbrīvotais kandidāts |
| Atbrīvotais kandidāts | Atbrīvotie kandidāti, iemesls, veiktspēja un atbrīvošanas datums | Uzņēmums, kalendāra nobīde, datums, ģeogrāfiskā atrašanās vieta, veiktspēja, demogrāfiskie dati, nodarbinātība, multivide, personāla atlases projekts, kandidāta vārds |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
