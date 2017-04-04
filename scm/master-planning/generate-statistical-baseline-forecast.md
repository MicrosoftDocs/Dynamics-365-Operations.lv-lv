---
title: "Ģenerēt statistikas bāzes prognoze"
description: "Šis raksts sniedz informāciju par parametriem un filtriem, kas tiek izmantoti pieprasījuma prognozēšanas aprēķinos."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Ģenerēt statistikas bāzes prognoze

Šis raksts sniedz informāciju par parametriem un filtriem, kas tiek izmantoti pieprasījuma prognozēšanas aprēķinos. 

Veidojot bāzlīnijas prognozi, vispirms ir jānorāda aprēķinā izmantotie parametri un filtri. Piemēram, varat izveidot bāzlīnijas prognozi, kas sniedz vērtējumu par pieprasījumu, ņemot vērā pagājušajā gada darījumu datus noteiktam uzņēmumam, nākamajam mēnesim un atlasītai krājumu grupai. 

Lai ģenerētu budžeta pieprasījumu, dodieties uz **vispārējā plānošana &gt;prognozēšanas &gt;pieprasījuma prognozēšanas &gt;ģenerēt statistikas bāzes prognoze**. 

Prognozes intervālu var atlasīt prognozes ģenerēšanas brīdī. Pieejamās vērtības ir šādas: diena, nedēļa un mēnesis. 

Prognozes ģenerēšanā izmantojamo intervālu skaits ir iestatīts laukā** Prognozes periods**. 

Ja prognozes stratēģija ir iestatīta ar opciju **Kopēt vēsturiskā pieprasījuma vietā**, vēsturiskā perioda beigas tiek ignorētas. Sistēma kopē numuru norādīta spaiņos **laiks horizon** lauku prognozētais pieprasījums, sākot no datuma, kas noteikts **dienas** laukā zem **vēsturisko horizontu**. Kopējot vēsturisko pieprasījumu no noteikta datuma uz priekšu, ražošanas plānotāji var sagatavot nākamā ceturkšņa plānu divējādi:

-   kopējot pieprasījumu no tā paša pagājušajā gada ceturkšņa;
-   kopējot pieprasījumu no iepriekšējā ceturkšņa.

Lai nepieļautu ražošanas plānos pārpratumus, noteiktu prognožu intervālu skaitu var sasaldēt. Šis skaits tiek iestatīts laukā **Sasaldēt periodu**. Laukā **Koriģēta pieprasījuma apjoma prognoze **tiek atspējotas iesaldēto intervālu šūnas, vizuāli norādot, ka šīs vērtības nedrīkst mainīt. 

Bāzlīnijas pieprasījuma apjoma prognozes sākuma datumam nav jābūt pašreizējam datumam vai datumam nākotnē. Lai iestatītu citu sākuma datumu, izmantojiet lauku **Bāzlīnijas prognozes sākuma datums - Sākuma datums**. Piemēram, jūnijā lietotāji var ģenerēt nākamā gada prognozi. Ja trūkst prognožu intervālu starp vēsturiskā pieprasījuma beigām un bāzlīnijas sākumu, prognozes var būt neprecīzas. Ja izmantojat Microsoft Dynamics 365 operācijas pieprasījuma prognozēšanas dienests, ir četri veidi, kā kurā var aizpildīt trūkstošos nepilnības. Var izvēlēties metodi, kādu vēlaties, nosakot MISSING\_vērtību\_aizstāšanas parametru par **pieprasījuma prognozēšanas parametrus** lapā. 

**Bāzlīnijas budžeta sākuma datumu** - **no dienas** lauks ir noteikts budžeta spaini, piemēram, sākumā Amerikas Savienotajās valstīs, ja prognozēšanas kausa nedēļas svētdienā. Sistēma automātiski pielāgo **bāzlīnijas budžeta sākuma datumu** - **no dienas** lauku atbilstoši budžeta kausu sākumam. 

**Bāzlīnijas budžeta sākuma datumu** - **no dienas** lauku var iestatīt datumu pagātnē. Tas nozīme, ka var ģenerēt pagājuša perioda pieprasījuma apjoma prognozi. Tas ir noderīgi, jo ļauj lietotājiem nomainīt prognozes pakalpojuma parametrus tā, lai par pagājušu periodu ģenerēta statistikas prognoze atbilstu faktiskajam vēsturiskajam pieprasījumam. Lietotāji var pēc tam turpināt izmantot šos parametru iestatījumus, lai ģenerētu turpmākā perioda statistiskās bāzlīnijas prognozi. 

Ja ir atlasīta izvēles rūtiņa **Pārsūtīt manuālās korekcijas uz pieprasījumu apjoma prognozi**, manuāli veiktās iepriekšējā pieprasījuma prognozēšanas iterāciju korekcijas var automātiski piemērot jaunajai bāzlīnijas prognozei. Ja izvēles rūtiņas atlase ir noņemta, manuālās korekcijas netiek pievienotas bāzlīnijas prognozei, bet tās netiek dzēstas. Manuāli veiktās prognozes korekcijas var dzēst tikai prognozes datu importēšanas laikā, noņemot izvēles rūtiņas **Saglabāt manuāli veiktās bāzlīnijas pieprasījuma apjoma prognozes korekcijas** atlasi. Manuāli veiktās korekcijas tiek saglabātas autorizācijas laikā. Tādējādi, ja lietotājs veic manuālas korekcijas budžetā, bet nav atļauj budžeta atpakaļ uz dinamiku 365 operācijām, izmaiņas tiek zaudētas. Plašāku informāciju par manuālo korekciju un kā viņi strādā, sk [atļauj koriģētā prognoze](authorize-adjusted-forecast.md). 

Izveidotajai pieprasījuma apjoma prognozei var piešķirt nosaukumu un pievienot komentārus, lai lietotāji varētu vieglāk atrast ģenerēto prognozi. Šīs vērtības ir redzamas prognozes ģenerēšanas vēstures lapā **Statistiskās bāzlīnijas prognozes ģenerēšanas vēsture**. 

Prognozes ģenerēšanas laikā var izmantot starpuzņēmumu plānošanas grupas, krājumu sadalījuma principu un citus filtrus. Tos var izmantot, lai uzlabotu veiktspēju vai sadalītu datus pārvaldāmās vienībās. Tomēr ņemiet vērā, ka pieprasījuma apjoma prognoze netiek ģenerēta krājumu sadalījuma principa dalībniekam, kas nav saistīts ar starpuzņēmumu plānošanas grupu, arī tad, ja krājumu sadalījuma princips ir atlasīts vaicājumā. 

**Padoms**. Dažreiz, ģenerējot pieprasījuma apjoma prognozi, lietotāji var saņemt kļūdas ziņojumus vai prognozes ģenerēšana tiek izpildīta, nepievienojot sesijas žurnālu. Tas var notikt, ja vaicājumā ir palikuši dati, kas iepriekš ir izmantoti prognozes ģenerēšanai. Lai novērstu šo problēmu, noklikšķiniet uz **Atlasīt** un atveriet lapu **Vaicājums** lapu, noklikšķiniet uz **Atiestatīt** un pēc tam atkārtojiet bāzlīnijas prognozes ģenerēšanu. 

Ja budžets netiek ģenerēta lielu vienumu kopa, bet, piemēram, vienam vienumam vai vienu krājumu sadalījuma atslēgu vienā reizē, tad lai iegūtu labākus rezultātus, jūs varat atlasīt **izmantot pieprasījuma atbildes režīmu** izvēles rūtiņu **Master plānošanas - Setup - pieprasījuma prognozēšanas** - **pieprasījuma prognožu parametri - Azure Machine Learning** tab.

<a name="see-also"></a>Skatiet arī
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


