---
title: "Pieprasījuma prognozēšanas iestatīšana"
description: "Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5074f3ded26f55c6244feba9fcf0199c81cad468
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="demand-forecasting-setup"></a>Pieprasījuma prognozēšanas iestatīšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei.  

Iestatīšanas uzdevumi ietver tālāk minēto datu un parametru iestatīšanu.

## <a name="item-allocation-key"></a>Krājumu sadalījuma princips
Pieprasījuma apjoma prognoze tiek aprēķināta krājumam un tā dimensijām tikai tad, ja uz krājumu attiecas krājumu sadalījuma princips. Šī kārtula tiek izmantota, lai grupētu lielu krājumu skaitu, kas ļauj paātrināt pieprasījuma apjoma prognožu izveidošanu. Ģenerējot pieprasījuma apjoma prognozes, krājumu sadalījuma principa procentuālais īpatsvars tiek ignorēts. Prognozes tiek veidotas, pamatojoties tikai uz vēsturiskajiem datiem. 

Krājumam un tā dimensijām jābūt iekļautiem tikai vienā krājumu sadalījuma principā, ja krājumu sadalījuma princips tiek izmantots prognozes sagatavošanas laikā. 

Lai krājumu sadalījuma principam pievienotu noliktavas vienību (stock keeping unit — SKU), dodieties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Pieprasījuma prognozēšana** &gt; **Krājumu sadalījuma principi**. Lai piešķirtu krājumu sadalījuma principam, izmantojiet lapu **Krājumu piešķiršana**.

## <a name="intercompany-planning-groups"></a>Starpuzņēmumu plānošanas grupas
Pieprasījuma prognozēšanas laikā tiek izveidotas starpuzņēmumu prognozes. Izmantojot programmatūru Microsoft Dynamics 365 for Operations, uzņēmumi, kuriem plānošana tiek veikta kopā, tiek grupēti vienā starpuzņēmumu plānošanas grupā. Lai katram uzņēmumam norādītu, kuri krājumu sadalījuma principi jāņem vērā, veicot pieprasījuma prognozēšanu, krājumu sadalījuma princips ir jāsaista ar starpuzņēmumu plānošanas grupas dalībnieku, dodoties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Starpuzņēmumu plānošanas grupas**. 

Ja starpuzņēmumu plānošanas grupas dalībniekiem nav piešķirts neviens krājumu sadalījuma princips, pieprasījuma apjoma prognoze pēc noklusējuma tiek aprēķināta visiem krājumiem, kas ir piešķirti visiem krājumu sadalījuma principiem visos Dynamics 365 for Operations uzņēmumos. Lapā **Statistiskās bāzlīnijas prognozes ģenerēšana** ir pieejamas papildu uzņēmumu un krājumu sadalījuma principu filtrēšanas opcijas. 

Pārskatiet prognozēto krājumu skaitu. Nevajadzīgie krājumi var radīt izmaksu palielināšanos, ja tiek izmantots pakalpojums Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Pieprasījuma prognozēšanas parametri
Lai iestatītu pieprasījuma prognozēšanas parametrus, dodieties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Pieprasījuma prognozēšanas parametri**. Tā kā pieprasījuma prognozēšana ietver starpuzņēmumus, iestatījumiem ir globāla nozīme. Tas nozīmē, ka iestatījumi attiecas uz visiem uzņēmumiem. 

Pieprasījuma prognozēšanas laikā tiek ģenerēta daudzumu prognoze. Tāpēc laukā **Pieprasījuma apjoma prognozes vienība** ir jānorāda mērvienība, ar kādu ir jāizsaka daudzums. Mērvienībai ir jābūt unikālai, lai varētu nodrošināt, ka ir skaidri saprotams apkopojums un procentuālais sadalījums. Lai iegūtu sīkāku informāciju par apkopojumu un procentuālo iedalījumu, skatiet sadaļu [Bāzlīnijas prognozes manuālu korekciju veikšana](manual-adjustments-baseline-forecast.md). Pārliecinieties, vai uz visām pieprasījuma prognozēšanā iekļautajām noliktavas vienībām izmantotajām mērvienībām attiecas mērvienības un vispārējās prognozēšanas mērvienības konvertēšanas kārtula. Kad tiek palaista prognozes ģenerēšana, tiek reģistrēts to krājumu saraksts, kam nav veikta mērvienības konvertēšana, kas ļauj ērti labot iestatījumus. 

Pieprasījuma prognozēšanu var izmantot, lai prognozētu gan atkarīgu, gan neatkarīgu pieprasījumu. Piemēram, ja atzīmēta ir tikai izvēles rūtiņa **Pārdošanas pasūtījums** un ja visi pieprasījuma prognozēšanā iekļautie krājumi ir pārdoti, sistēmā tiek aprēķināts neatkarīgais pieprasījums. Tomēr krājumu sadalījuma principiem var pievienot kritiskos apakškomponentus, iekļaujot tos pieprasījuma prognozēšanā. Šajā gadījumā, ja ir atzīmēta izvēles rūtiņa **Ražošanas rinda**, tiek aprēķināta atkarīgā prognoze. 

Bāzlīnijas prognozes izveidošanai programmatūrā Dynamics 365 for Operations ir pieejamas divas metodes. Lai ģenerētu prognozi, var izmantot prognozēšanas modeļus virs vēsturiskajiem datiem vai var vienkārši kopēt uz vēsturiskajiem datiem. Laukā **Prognozes ģenerēšanas stratēģija** var izvēlēties vienu no šīm divām metodēm. Lai izmantotu prognozes modeļus, atlasiet vienumu **Azure Machine Learning**. 

Noklikšķinot uz **Prognozes dimensijas** lapas **Pieprasījuma prognozēšanas parametri** kreisajā rūtī, var atlasīt arī pieprasījuma apjoma prognozes ģenerēšanā izmantojamās prognozes dimensijas. Prognozes dimensija norāda to detalizēto datu līmeni, kam prognoze ir definēta. Obligātās prognozes dimensijas ir uzņēmums, vieta un krājumu sadalījuma princips, bet var ģenerēt arī prognozes noliktavas, krājumu statusa, debitoru grupas, debitora konta, valsts/reģiona, pavalsts un krājuma, kā arī visu krājuma dimensiju līmenī. 

Jebkurā brīdī dimensiju sarakstam var pievienot pieprasījuma prognozēšanā izmantotās prognozes dimensijas. Prognozes dimensijas var arī sarakstā dzēst. Tomēr, ja prognozes dimensija tiek pievienota vai noņemta, tiek zaudētas manuāli veiktās korekcijas. 

No pieprasījuma prognozēšanas perspektīvas uz visiem krājumi neattiecas vienādi principi. Līdzīgus krājumus var grupēt pēc viena krājumu sadalījuma principa, un parametrus, piemēram, transakcijas tipus un prognozes metodes iestatījumus, var iestatīt katram krājumu sadalījuma principam. Noklikšķiniet uz **Krājumu sadalījuma princips** lapas **Pieprasījuma prognozēšanas parametri** kreisajā rūtī. 

Lai ģenerētu prognozi, Dynamics 365 for Operations izmanto tīmekļa pakalpojumu Algoritmiskā mācīšanās. Lai izveidotu savienojumu ar pakalpojumu, piesakoties pakalpojumā Microsoft Azure Machine Learning Studio, programmatūrā Dynamics 365 for Operations ir jānorāda tālāk minētā informācija.

-   Tīmekļa pakalpojuma lietojumprogrammas interfeisa (API) atslēga
-   Tīmekļa pakalpojuma galapunkta URL
-   Azure krātuves konta nosaukums
-   Azure krātuves konta atslēga

**Piezīme.** Azure krātuves konta nosaukums un atslēga ir jānorāda tikai tad, ja tiek izmantots pielāgots krātuves konts. Ja tiek izmantota lokālā versija, ir nepieciešams pielāgots krātuves konts pakalpojumā Azure, lai pakalpojums Algoritmiskā mācīšanās varētu piekļūt vēsturiskajiem datiem. 

Lai izveidotu pieprasījuma apjoma prognozes, varat izvietot savu pakalpojumu, izmantojot Machine Learning Studio vai Dynamics 365 for Operations pieprasījuma prognozēšanas eksperimentus. Norādījumi par to, kā izvietot Dynamics 365 for Operations pieprasījuma prognozēšanas eksperimentus kā tīmekļa pakalpojumu, ir pieejami programmatūrā Dynamics 365 for Operations. Lapā **Pieprasījuma prognozēšanas parametri** noklikšķiniet uz cilnes **Azure Machine Learning**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Iestatījumi Dynamics 365 for Operations pieprasījuma prognozēšanas algoritmiskās mācīšanās pakalpojumam
Lai apskatītu parametrus, kurus var konfigurēt izmantošanai ar Dynamics 365 for Operations pieprasījuma prognozēšanas pakalpojumu, dodieties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Pieprasījuma prognozēšana** &gt; **Prognozēšanas algoritma parametri**. Lapā **Prognozēšanas algoritma parametri** ir redzamas parametru noklusējuma vērtības. Šos parametrus var pārlabot lapā **Pieprasījuma prognozēšanas parametri**. Lai vispārēji pārrakstītu parametrus, izmantojiet cilni **Vispārīgi** vai izmantojiet cilni **Krājumu sadalījuma principi**, lai pārrakstītu katra krājumu sadalījuma principa parametrus. Krājumu sadalījuma principa pārrakstītos parametrus ietekmē tikai krājumu prognoze, kas ir saistīta ar šo krājumu sadalījuma principu.

<a name="see-also"></a>Skatiet arī
--------

[Ievads par pieprasījuma prognozēšanu](introduction-demand-forecasting.md)

[Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)

[Manuālu bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)



