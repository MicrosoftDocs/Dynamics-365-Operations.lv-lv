---
title: "Power BI satura pakotne Personāla atlase"
description: "Šajā tēmā ir aprakstīta Dynamics 365 for Operations Power BI satura pakotne Personāla atlase. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai izveidotu šo satura pakotni."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>Power BI satura pakotne Personāla atlase

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīta Dynamics 365 for Operations Power BI satura pakotne Personāla atlase. Tajā ir paskaidrots, kā piekļūt pārskatiem, kas ir iekļauti satura pakotnē, un ir sniegta informācija par datu modeli un elementiem, kas tika izmantoti, lai izveidotu šo satura pakotni.

<a name="accessing-the-content-pack"></a>Piekļuve satura pakotnei
--------------------------

Satura pakotne Personāla atlase ir pieejama Microsoft Dynamics Lifecycle Services (LCS) koplietojamo līdzekļu bibliotēkā. Papildinformāciju par to, kā lejupielādēt šo satura pakotni un to savienot ar saviem Microsoft Dynamics 365 for Operations datiem, skatiet rakstā [Power BI saturs pakalpojumā LCS no Microsoft un jūsu partneriem](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Satura pakotnē iekļautie pārskati
Pēc satura pakotnes savienošanas ar jūsu Dynamics 365 for Operations datiem pārskatos tiek rādīti jūsu organizācijas dati. Ja iepriekš neesat lietojis Microsoft Power BI, papildinformāciju par to varat uzzināt lapā [Vadītā apmācība par Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Satura pakotnē iekļautajos pārskatos ir gan diagrammas, gan tabulas, kas satur papildinformāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                       | Saturs                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Kandidātu analīze           | Kandidāti pēc amata, kandidātu avoti, kandidāti pēc atrašanās vieta un kandidātu kopskaits           |
| Kandidāta statuss             | Kandidāti pēc veida un statusa un kandidāta statuss                                                    |
| Kandidātu demogrāfiskie dati       | Kandidāti pēc vecuma un dzimuma un kandidāti pēc izglītības līmeņa un statusa                             |
| Personāla atlases analīze          | Neto pieņemšanas darbā attiecība, vidējais dienu skaits līdz pieņemšanai darbā, neveiksmīgie pieņemšanas darbā gadījumi procentos un personāla atlases izmaksas                    |
| Personāla atlases projektu analīze | Personāla atlases projektu skaits, vakances pēc personāla atlases projekta un kandidāti pēc personāla atlases projekta |

Šajos pārskatos esošās diagrammas un elementus varat filtrēt, un diagrammas un elementus varat piespraust informācijas panelim. Plašāku informāciju par filtrēšanu un piespraušanu pakalpojumā Power BI skatiet rakstā [Izveidot un konfigurēt informācijas paneli](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
Satura pakotnes Personāla atlase pārskatu aizpildīšanai tiek izmantoti Dynamics 365 for Operations dati. Nākamajā tabulā ir redzami elementi, uz kuriem šī satura pakotne bija balstīta.

| Elements                          | Saturs                                                         | Attiecības ar citiem elementiem                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | Kandidāti, pieņemtie kandidāti, neto pieņemšanas darbā attiecība un izmaksas          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Kandidāta vārds, uzvārds un pilns vārds                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalendārs nobīdās, lai sadalītu pārskatus                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Uzņēmumi, pēc kuriem pārskatus filtrēt                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Dienas, nedēļas, mēneši un gadi                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Dzimšanas datums, dzimums, etniskā izcelsme un ģimenes stāvoklis         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Kandidāts, veiktspēja, sākuma datums un kandidāta veids           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Sākuma datums, beigu datums un pārejas datums                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Pilsēta, novads, pasta indekss un štats vai reģions                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Funkcija, tips un nosaukums                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Kandidātu avots                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Vērtējums, apraksts un vērtēšanas modelis                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Projekta apraksts, projekta statuss un vakances                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Atbrīvotie kandidāti, iemesls, veiktspēja un atbrīvošanas datums | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Šie elementi tika izmantoti, lai izveidotu aprēķinātos mērus. Pēc tam šie aprēķinātie mēri tiek lietoti, lai aprēķinātu galvenos veiktspējas rādītājus (key performance indicators — KPI) un pārskatus, kas tiek izmantoti satura pakotnē. Ja vēlaties pārskatos vai informācijas panelī ietvert papildu aprēķinus, varat lejupielādēt un modificēt failu Recruiting.pbix no pakalpojuma LCS. Šis fails ir noklusējuma datu modelis, kas tika izmantots satura pakotnes izveidošanai. Kad esat pabeidzis izmaiņu veikšanu, varat izveidot organizācijas satura pakotni un informācijas paneli, kas satur jūsu pievienoto informāciju.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





