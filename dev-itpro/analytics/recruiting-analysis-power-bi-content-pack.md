---
title: "Power BI satura pakotne Personāla atlase"
description: "Šajā tēmā ir aprakstīta Power BI satura pakotne Personāla atlase. Tajā ir paskaidrots, kā piekļūt pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 49cfd0f1ed645f1980b21b6d4f453cb7a8957a1a
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="recruiting-power-bi-content"></a>Power BI satura pakotne Personāla atlase

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta Microsoft Power BI satura pakotne **Personāla atlase**. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="accessing-the-power-bi-content"></a>Piekļūšana Power BI saturam
Ja izmantojat Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise 2017. gada jūlija atjauninājumu, **Personāla atlase** Power BI saturs tiek rādīts darbvietā **Personāla atlases pārvaldība**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Pārskati un vizualizācijas personāla atlases pārvaldības darbvietā
**Personāla atlases pārvaldība** darbvieta satur cilni **Analītika**. Šajā cilnē ir iegults Power BI saturs par personāla atlasi. Saturs sastāv no pārskata cilnes un papildu cilnēm, kas satur detalizētu informāciju. Tabulā ir sniegts katras cilnes pārskatu apraksts.

| Pārskats               | Saturs |
|----------------------|----------|
| Pārskats par personāla atlasi | Citu pārskatu apkopojums |
| Kandidātu analīze   | Kandidātu kopskaits, kandidāti pēc amata, kandidātu avoti, kandidātu sieviešu skaits salīdzinājumā kandidātiem vīriešiem un kandidāti pēc atrašanās vietas |
| Kandidāta statuss     | Kandidāti pēc veida un statusa un kandidāta statuss |
| Personāla atlases analīze  | Neto pieņemšanas darbā attiecība, vidējais dienu skaits līdz pieņemšanai darbā, neveiksmīgie pieņemšanas darbā gadījumi procentos un personāla atlases izmaksas, personāla atlases projektu skaits, lietotā pieņemšana darbā un kandidāti salīdzinājumā ar vakancēm pēc personāla atlases projekta |

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Tālāk esošajā tabulā ir norādīti elementi, kas ir izmantoti **personāla atlases** Power BI satura izveidei.

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

Šie elementi tika izmantoti, lai izveidotu aprēķinātos mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un satura pakotnē ietverto pārskatu datus. Ja vēlaties pārskatos vai informācijas panelī ietvert papildu aprēķinus, varat lejupielādēt un modificēt failu Recruiting.pbix no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS). Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidei. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

