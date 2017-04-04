---
title: "Organizācijas apmācību jauda BI saturu"
description: "Šajā tēmā ir aprakstīts, Dynamics 365 operācijām - organizācijas apmācību jauda BI saturu. Tas izskaidro, kā piekļūt satura pakotne un apraksta datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organizācijas apmācību jauda BI saturu

Šajā tēmā ir aprakstīts, Dynamics 365 operācijām - organizācijas apmācību jauda BI saturu. Tas izskaidro, kā piekļūt satura pakotne un apraksta datu modelis un vienībām, kas tika izmantoti, lai izveidotu satura pakotne.

<a name="accessing-the-content-pack"></a>Piekļūstot satura pakotni
--------------------------

Jūs varat atrast organizācijas mācību satura pakotne bibliotēkā Shared aktīvu programmā Microsoft Dynamics Lifecycle Services (LCS). Lai iegūtu papildinformāciju par satura pakotnes lejupielāde un izveidojiet savienojumu ar savu Microsoft Dynamics 365 darbības datiem, skatiet [Power BI saturu no Microsoft un partneri LCS](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Atskaitēm, kas ir iekļautas satura pakotni
Pēc satura pakotne savienojuma izveidošanas ar savu dinamiku 365 darbības datiem, ziņojumi liecina uzņēmuma dati. Ja jūs nekad neesmu lietojis Microsoft Power BI pirms, jūs varat uzzināt vairāk par to uz [vadīto mācību lapas Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Atskaitēm, kas ir iekļautas satura pakotne ir gan diagrammām un tabulām, kas satur papildu informāciju. Tabulā ir sniegts pārskatu apraksts.

| Pārskats          | Saturs                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analīzes gaitā | Reģistrācija ar atrašanās vietu, kursu dalībniekus ar statusu un reģistrācijas saraksts |
| Kursu tipi    | Kursu tipi pēc prasmēm                                                       |

Varat filtrēt diagrammas un mozaīkas uz šiem ziņojumiem, un pin diagrammām un flīžu panelis. Papildinformāciju par to, kā filtrēt un pin barošanas BI sk [Create and Configure A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Datu modeļa un elementu izprašana
365 dinamika attiecībā uz darbības datiem lieto, lai papildinātu tās atskaites, kuras atrodas organizācijas mācību satura pakotne. Tabulā ir norādīti satura pakotne tika balstīta uz juridiskajām personām.

| Elements                    | Saturs                                                         | Relācijas ar citām entītijām                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mācības,\_CalendarOffset  | Kalendārs, kas nobīda slāņa ziņojumus                                | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Apmācības\_uzņēmums         | Uzņēmumiem, lai filtrētu pārskatus                                   | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Apmācības\_Course          | Kursu, apraksts, instruktoru nosaukums, atrašanās vieta, telpa un statuss | Mācības,\_CourseAgenda apmācību\_CourseAttendees apmācību\_CourseSkill                                                                                                                             |
| Mācības,\_CourseAgenda    | Programmu, kursu un sākuma un beigu laiku                          | Apmācības\_uzņēmuma apmācību\_CalendarOffset apmācību\_datums mācību\_Course                                                                                                                         |
| Mācības,\_CourseAttendees | Nosaukums, statuss, darbu un reģistrācijas datums                         | Apmācības\_uzņēmuma apmācību\_CalendarOffset apmācību\_datums mācību\_demogrāfijas apmācību\_nodarbinātības apmācības\_apmācības kursu\_WorkerName apmācību\_WorkerTitle apmācību\_darba apmācība\_pozīciju |
| Mācības,\_CourseSkill     | Prasme, prasme veidam un līmenim                                     | Apmācības\_Course                                                                                                                                                                                   |
| Apmācības\_datums            | Dienas, nedēļas, mēneši un gadi                                   | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Apmācības\_demogrāfija    | Dienas, dzimšanas, dzimuma, etniskās piederības un ģimenes stāvoklis         | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Apmācības\_nodarbinātības      | Sākuma datums, beigu datums un pārejas datumu                        | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Apmācības\_darba             | Funkciju, tipu un nosaukumu                                        | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Apmācības\_stāvoklis        | Pozīciju, nosaukums un pilna darba laika ekvivalentu (FTE)                  | Mācības,\_CourseAgenda apmācību\_CourseAttendees                                                                                                                                                   |
| Mācības,\_WorkerName      | Vārdu, uzvārdu un vārdu un uzvārdu                             | Mācības,\_CourseAttendees                                                                                                                                                                          |
| Mācības,\_WorkerTitle     | Virsraksts un darba stāža datums                                         | Mācības,\_CourseAttendees                                                                                                                                                                          |

Šīm vienībām tika izmantoti, lai izveidotu aprēķinātās mērvienības datu modelī. Tās aprēķina, pasākumus, kas pēc tam tiek izmantoti, lai aprēķinātu galveno veiktspējas rādītāju (KPI) un atskaites, kas tiek izmantotas satura pakotne. Ja jūs vēlaties iekļaut jūsu atskaites un informācijas paneļa papildu aprēķinus, var lejupielādēt un modificēt LCS Training.pbix failu. Šis fails ir noklusēto datu modelis, kas tika izmantots, lai izveidotu satura pakotne. Pēc tam, kad esat veicis izmaiņas, var izveidot organizācijas satura pakotne un vadības paneli, kas satur informāciju, ko esat pievienojis.

## <a name="additional-resources"></a>Papildu resursi
Šeit norādītas dažas noderīgas saites, kas ir saistītas ar elementiem un Power BI satura izveidi:

-   [Datu elementi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizācijas satura pakotnes izveide](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datu modelēšana, izmantojot Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI elementu pievienošana darbvietām](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



