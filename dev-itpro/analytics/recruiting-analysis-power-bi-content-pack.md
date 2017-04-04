---
title: "Pieņemot darbā Power BI saturu"
description: "Šajā tēmā ir aprakstīts, Dynamics 365 operācijām - Recruiting Power BI saturu. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Pieņemot darbā Power BI saturu

Šajā tēmā ir aprakstīts, Dynamics 365 operācijām - Recruiting Power BI saturu. Tas izskaidro, kā piekļūt atskaitēm, kas ir iekļautas satura pakotne un sniedz informāciju par datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne.

<a name="accessing-the-content-pack"></a>Piekļūstot satura pakotni
--------------------------

Jūs varat atrast Recruiting satura pakotne bibliotēkā Shared aktīvu programmā Microsoft Dynamics Lifecycle Services (LCS). Lai iegūtu papildinformāciju par satura pakotnes lejupielāde un izveidojiet savienojumu ar savu Microsoft Dynamics 365 darbības datiem, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Atskaitēm, kas ir iekļautas satura pakotni
Pēc satura pakotne savienojuma izveidošanas ar savu dinamiku 365 darbības datiem, ziņojumi liecina uzņēmuma dati. Ja jūs nekad neesmu lietojis Microsoft Power BI pirms, jūs varat uzzināt vairāk par to uz [vadīto mācību lapas Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Atskaitēm, kas ir iekļautas satura pakotne ir gan diagrammām un tabulām, kas satur papildu informāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats                       | Saturs                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Iesniedzēja analīze           | Darbu, prasītāja avotiem, prasītāji pēc atrašanās vietas, un kopējais pretendentu skaitu pieteikumu iesniedzējiem           |
| Kandidāta statuss             | Pretendenti pēc tipa un statusu un Kandidāta statuss                                                    |
| Iesniedzēja demogrāfija       | Pēc vecuma un dzimuma kandidātiem un pretendentiem pēc izglītības līmeņa un statusa                             |
| Pieņemot darbā analīze          | Neto nomas attiecību, vidējais dienas nolīgt procentus slikti izīrē un rekrutēšanas izmaksas                    |
| Personāla atlases projekta analīze | Personāla atlases projekti, atveres, personāla atlases projektu un personāla atlases projekta pieteikuma numurs |

Varat filtrēt diagrammas un mozaīkas uz šiem ziņojumiem, un pin diagrammām un flīžu panelis. Papildinformāciju par to, kā filtrēt un pin barošanas BI sk [Create and Configure A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
365. dinamika attiecībā uz darbības datiem tiek lietota, lai aizpildītu Recruiting satura pakotnes ziņojumi. Tabulā ir norādīti satura pakotne tika balstīta uz juridiskajām personām.

| Elements                          | Saturs                                                         | Relācijas ar citām entītijām                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbā\_iesniedzējs           | Prasītāji, nolīgtais kandidātiem, neto nomas attiecību un izmaksas          | Darbā\_ApplicantName darbā\_uzņēmuma darbā\_CalendarOffset Recuriting\_dienas darbā\_GeographicLocation darbā\_demogrāfijas darbā\_darbu, pieņemt darbā\_mediju darbā\_RecruitmentProject                                |
| Darbā\_ApplicantName       | Iesniedzēja vārdu, uzvārdu un vārdu un uzvārdu                   | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_CalendarOffset      | Kalendārs, kas nobīda slāņa ziņojumus                                | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_uzņēmums             | Uzņēmumiem, lai filtrētu pārskatus                                   | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_datums                | Dienas, nedēļas, mēneši un gadi                                   | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_demogrāfija        | Dienas, dzimšanas, dzimuma, etniskās piederības un ģimenes stāvoklis         | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_EmployedApplicant   | Iesniedzējs, veiktspēju, sākuma datumu un pieteikuma iesniedzējs ierakstiet           | Darbā\_uzņēmuma darbā\_CalendarOffset darbā\_dienas darbā\_darbā GeographicLocation\_ApplicantName darbā\_nodarbinātības darbā\_sniegumu darbā\_darbu, pieņemt darbā\_mediju darbā\_RecruitmentProject          |
| Darbā\_nodarbinātības          | Sākuma datums, beigu datums un pārejas datumu                        | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_GeographicLocation  | Pilsētas, pagasta, pasta indeksu un rajons                 | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_darba                 | Funkciju, tipu un nosaukumu                                        | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_Media               | Pretendentiem avots                                             | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_Performance         | Novērtējums, apraksts un novērtējuma modelis                            | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_RecruitmentProject  | Projekta apraksts, projekta statusu un atveres                | Darbā\_iesniedzējs darbā\_darbā EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Darbā\_TerminatedApplicant | Pārtraukta, pretendenti, iemesls, sniegumu un izbeigšanas datumu | Darbā\_uzņēmuma darbā\_CalendarOffset darbā\_dienas darbā\_GeographicLocation darbā\_sniegumu darbā\_demogrāfijas darbā\_nodarbinātības darbā\_mediju darbā\_darbā RecruitmentProject\_ApplicantName |

Šīm vienībām tika izmantoti, lai izveidotu aprēķinātās mērvienības. Tās aprēķina, pasākumus, kas pēc tam tiek izmantoti, lai aprēķinātu galveno veiktspējas rādītāju (KPI) un atskaites, kas tiek izmantotas satura pakotne. Ja jūs vēlaties iekļaut jūsu atskaites un informācijas paneļa papildu aprēķinus, var lejupielādēt un modificēt LCS Recruiting.pbix failu. Šis fails ir noklusēto datu modelis, kas tika izmantots, lai izveidotu satura pakotne. Pēc tam, kad esat veicis izmaiņas, var izveidot organizācijas satura pakotne un vadības paneli, kas satur informāciju, ko esat pievienojis.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



