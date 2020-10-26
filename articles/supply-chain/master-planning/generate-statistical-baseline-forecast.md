---
title: Statistiskās bāzlīnijas prognozes ģenerēšana
description: Šajā tēmā ir sniegta informācija par parametriem un filtriem, kas tiek izmantoti pieprasījuma prognozēšanas aprēķinos.
author: roxanadiaconu
manager: tfehr
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db0ac2d56db46f283716df6615e404a5354f8d3e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982849"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Statistiskās bāzlīnijas prognozes ģenerēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par parametriem un filtriem, kas tiek izmantoti pieprasījuma prognozēšanas aprēķinos. 

Veidojot bāzlīnijas prognozi, vispirms ir jānorāda aprēķinā izmantotie parametri un filtri. Piemēram, varat izveidot bāzlīnijas prognozi, kas sniedz vērtējumu par pieprasījumu, ņemot vērā pagājušajā gada darījumu datus noteiktam uzņēmumam, nākamajam mēnesim un atlasītai krājumu grupai. 

Lai ģenerētu pieprasījuma apjoma prognozi, pārejiet uz sadaļu **Vispārējā plānošana &gt; Prognozēšana &gt; Pieprasījuma prognozēšana &gt; Ģenerēt statistiskās bāzlīnijas prognozi**. 

Prognozes intervālu var atlasīt prognozes ģenerēšanas brīdī. Pieejamās vērtības ir šādas: diena, nedēļa un mēnesis. 

Prognozes ģenerēšanā izmantojamo intervālu skaits ir iestatīts laukā **Prognozes periods**. 

Ja prognozes stratēģija ir iestatīta ar opciju **Kopēt vēsturiskā pieprasījuma vietā**, vēsturiskā perioda beigas tiek ignorētas. Sistēma nodrošina laukā **Prognozes periods** norādītā intervālu skaita kopēšanu uz prognozēto pieprasījumu, sākot ar sadaļas **Vēsturiskais periods** laukā **Sākuma datuma** iestatīto datumu. Kopējot vēsturisko pieprasījumu no noteikta datuma uz priekšu, ražošanas plānotāji var sagatavot nākamā ceturkšņa plānu divējādi:

-   kopējot pieprasījumu no tā paša pagājušajā gada ceturkšņa;
-   kopējot pieprasījumu no iepriekšējā ceturkšņa.

Lai nepieļautu ražošanas plānos pārpratumus, noteiktu prognožu intervālu skaitu var sasaldēt. Šis skaits tiek iestatīts laukā **Sasaldēt periodu**. Laukā **Koriģēta pieprasījuma apjoma prognoze** tiek atspējotas iesaldēto intervālu šūnas, vizuāli norādot, ka šīs vērtības nedrīkst mainīt. 

Bāzlīnijas pieprasījuma apjoma prognozes sākuma datumam nav jābūt pašreizējam datumam vai datumam nākotnē. Lai iestatītu citu sākuma datumu, izmantojiet lauku **Bāzlīnijas prognozes sākuma datums - Sākuma datums**. Piemēram, jūnijā lietotāji var ģenerēt nākamā gada prognozi. Ja trūkst prognožu intervālu starp vēsturiskā pieprasījuma beigām un bāzlīnijas sākumu, prognozes var būt neprecīzas. Ja izmantojat pieprasījuma prognozēšanas pakalpojumu, trūkstošos intervālus varat aizpildīt četros veidos. Varat izvēlēties izmantojamo metodi, lapā **Pieprasījuma prognozēšanas parametri** iestatot parametru MISSING\_VALUE\_SUBSTITUTION . 

> [!NOTE]
> Trūkstošo vērtību aizvietošana darbojas tikai datu atšķirībām starp vēsturisko datu sākuma un beigu datumiem. Dati netiks aizpildīti pirms vai pēc pēdējā fiziskā datu punkta, un tā darbojas tikai kā ekstrapolācija starp faktiski pastāvošajiem datu punktiem. 

Laukā **Bāzlīnijas prognozes sākuma datums** - **Sākuma datums** ir jāiestata prognozes intervāla sākuma datums, piemēram, ASV ir jāiestata svētdiena, ja prognozēšanas intervāls ir nedēļa. Sistēma nodrošina lauka **Bāzlīnijas prognozes sākuma datums** - **Sākuma datums** vērtības automātisku pielāgošanu atbilstoši prognozes intervāla sākumam. 

Kā lauka **Bāzlīnijas prognozes sākuma datums** - **Sākuma datums** vērtību var iestatīt pagājušu datumu. Tas nozīme, ka var ģenerēt pagājuša perioda pieprasījuma apjoma prognozi. Tas ir noderīgi, jo ļauj lietotājiem pielāgot prognozes pakalpojuma parametrus tā, lai par pagājušu periodu ģenerēta statistikas prognoze atbilstu faktiskajam vēsturiskajam pieprasījumam. Lietotāji var pēc tam turpināt izmantot šos parametru iestatījumus, lai ģenerētu turpmākā perioda statistiskās bāzlīnijas prognozi. 

Ja ir atlasīta izvēles rūtiņa **Pārsūtīt manuālās korekcijas uz pieprasījumu apjoma prognozi**, manuāli veiktās iepriekšējā pieprasījuma prognozēšanas iterāciju korekcijas var automātiski piemērot jaunajai bāzlīnijas prognozei. Ja izvēles rūtiņas atlase ir noņemta, manuālās korekcijas netiek pievienotas bāzlīnijas prognozei, bet tās netiek dzēstas. Manuāli veiktās prognozes korekcijas var dzēst tikai prognozes datu importēšanas laikā, noņemot izvēles rūtiņas **Saglabāt manuāli veiktās bāzlīnijas pieprasījuma apjoma prognozes korekcijas** atlasi. Manuāli veiktās korekcijas tiek saglabātas autorizācijas laikā. Tādēļ, ja lietotājs prognozes korekcijas veic manuāli, bet prognozi neautorizē programmatūrā Supply Chain Management, šīs izmaiņas tiek zaudētas. Papildinformāciju par manuāli veiktajām korekcijām un to darbību skatiet tēmā [Koriģētās prognozes autorizēšana](authorize-adjusted-forecast.md). 

Izveidotajai pieprasījuma apjoma prognozei var piešķirt nosaukumu un pievienot komentārus, lai lietotāji varētu vieglāk atrast ģenerēto prognozi. Šīs vērtības ir redzamas prognozes ģenerēšanas vēstures lapā **Statistiskās bāzlīnijas prognozes ģenerēšanas vēsture**. 

Prognozes ģenerēšanas laikā var izmantot starpuzņēmumu plānošanas grupas, krājumu sadalījuma principu un citus filtrus. Tos var izmantot, lai uzlabotu veiktspēju vai sadalītu datus pārvaldāmās vienībās. Tomēr ņemiet vērā, ka pieprasījuma apjoma prognoze netiek ģenerēta krājumu sadalījuma principa dalībniekam, kas nav saistīts ar starpuzņēmumu plānošanas grupu, arī tad, ja krājumu sadalījuma princips ir atlasīts vaicājumā. 

> [!TIP]
> Dažreiz, ģenerējot pieprasījuma apjoma prognozi, lietotāji var saņemt kļūdas ziņojumus vai prognozes ģenerēšana tiek izpildīta, nepievienojot sesijas žurnālu. Tas var notikt, ja vaicājumā ir palikuši dati, kas iepriekš ir izmantoti prognozes ģenerēšanai. Lai atrisinātu šo problēmu, noklikšķiniet uz **Atlasīt** un atveriet lapu **Vaicājums** lapu, atlasiet **Atiestatīt** un pēc tam atkārtojiet bāzlīnijas prognozes ģenerēšanu. 

Ja prognoze tiek ģenerēta nevis par lielu krājumu kopu, bet, piemēram, tikai par vienu krājumu vai vienu krājumu sadalījuma principu, tad, lai iegūtu labāku rezultātu, varat atzīmēt izvēles rūtiņu **Izmantot pieprasījuma atbildes režīmu** cilnē **Vispārējā plānošana — Iestatījumi — Pieprasījuma prognozēšana** - **Pieprasījuma prognozēšanas parametri — Azure algoritmiskā mācīšanās**.

> [!NOTE]
> Potenciāli lēzenu prognozi var izraisīt vēsturiskie dati, kuriem jābūt ar ilgāku vēsturisko periodu (vismaz 3 laika periodi, lai varētu konstatēt tendences, piemēram, 3 gadi ar mēneša prognozi). Lai iegūtu labākus rezultātus, varat mēģināt mainīt laika diapazona granularitāti vai paplašināt laika diapazonu.

<a name="additional-resources"></a>Papildu resursi
--------

- [Pieprasījuma prognozēšanas iestatīšana](demand-forecasting-setup.md)

- [Manuāla bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)

- [Autorizēt koriģēto pieprasījuma apjoma prognozi](authorize-adjusted-forecast.md)
