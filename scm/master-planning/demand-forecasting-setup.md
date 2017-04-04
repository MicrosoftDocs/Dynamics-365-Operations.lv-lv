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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Pieprasījuma prognozēšanas iestatīšana

Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei.  

Iestatīšanas uzdevumi ietver tālāk minēto datu un parametru iestatīšanu.

## <a name="item-allocation-key"></a>Krājumu sadalījuma princips
Pieprasījuma apjoma prognoze tiek aprēķināta krājumam un tā dimensijām tikai tad, ja uz krājumu attiecas krājumu sadalījuma princips. Šo noteikumu tiek ieviesta uz grupas lielu skaitu elementu, tāpēc, ka pieprasījuma prognozes var izveidot ātrāk. Krājumu sadalījuma atslēgas procenti tiek ignorēta, ģenerējot pieprasījuma prognozes. Prognozes tiek veidotas, pamatojoties tikai uz vēsturiskajiem datiem. 

Krājumam un tā dimensijām jābūt iekļautiem tikai vienā krājumu sadalījuma principā, ja krājumu sadalījuma princips tiek izmantots prognozes sagatavošanas laikā. 

Lai pievienotu noliktavas vienība (NV) krājumu sadalījuma atslēgu, dodieties uz **vispārējā plānošana**&gt;**Setup**&gt;**pieprasījuma prognozēšanas**&gt;**krājumu sadalījuma principus**. Lai piešķirtu krājumu sadalījuma principam, izmantojiet lapu **Krājumu piešķiršana**.

## <a name="intercompany-planning-groups"></a>Starpuzņēmumu plānošanas grupas
Pieprasījuma prognozēšanas laikā tiek izveidotas starpuzņēmumu prognozes. Microsoft Dynamics 365 operācijām, uzņēmumi, kas tiek plānoti kopā ir sagrupētas vienu starpuzņēmumu plānošanas grupu. Norādīt katram uzņēmumam, kura krājumu sadalījuma principus, jāņem vērā pieprasījumu prognozēšanu, saistīt krājumu sadalījuma atslēgu ar starpuzņēmumu plānošanas grupas dalībniekam, dodoties uz **vispārējā plānošana**&gt;**Setup**&gt;**starpuzņēmumu plānošanas grupas**. 

Pēc noklusējuma, ja neviens krājumu sadalījuma principi tiek piešķirti starpuzņēmumu plānošanas grupas dalībnieki, pieprasījuma prognozi aprēķina visiem krājumiem, kas piešķirti visu krājumu sadalījuma principus no visiem Dynamics 365 darbības uzņēmumiem. Lapā **Statistiskās bāzlīnijas prognozes ģenerēšana** ir pieejamas papildu uzņēmumu un krājumu sadalījuma principu filtrēšanas opcijas. 

Pārskatiet prognozēto krājumu skaitu. Nevajadzīgie krājumi var radīt izmaksu palielināšanos, ja tiek izmantots pakalpojums Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Pieprasījuma prognozēšanas parametri
Lai iestatītu pieprasījuma prognozēšanas parametrus, dodieties uz **vispārējā plānošana**&gt;**Setup**&gt;**pieprasījuma prognozēšanas parametrus**. Tā kā pieprasījuma prognozēšana ietver starpuzņēmumus, iestatījumiem ir globāla nozīme. Tas nozīmē, ka iestatījumi attiecas uz visiem uzņēmumiem. 

Pieprasījuma prognozēšanas laikā tiek ģenerēta daudzumu prognoze. Tāpēc laukā **Pieprasījuma apjoma prognozes vienība** ir jānorāda mērvienība, ar kādu ir jāizsaka daudzums. Mērvienībai ir jābūt unikālai, lai varētu nodrošināt, ka ir skaidri saprotams apkopojums un procentuālais sadalījums. Lai iegūtu sīkāku informāciju par apkopojumu un procentuālo iedalījumu, skatiet sadaļu [Bāzlīnijas prognozes manuālu korekciju veikšana](manual-adjustments-baseline-forecast.md). Pārliecinieties, vai uz visām pieprasījuma prognozēšanā iekļautajām noliktavas vienībām izmantotajām mērvienībām attiecas mērvienības un vispārējās prognozēšanas mērvienības konvertēšanas kārtula. Kad tiek palaista prognozes ģenerēšana, tiek reģistrēts to krājumu saraksts, kam nav veikta mērvienības konvertēšana, kas ļauj ērti labot iestatījumus. 

Pieprasījuma prognozēšanu var izmantot, lai prognozētu gan atkarīgu, gan neatkarīgu pieprasījumu. Piemēram, ja atzīmēta ir tikai izvēles rūtiņa **Pārdošanas pasūtījums** un ja visi pieprasījuma prognozēšanā iekļautie krājumi ir pārdoti, sistēmā tiek aprēķināts neatkarīgais pieprasījums. Tomēr krājumu sadalījuma principiem var pievienot kritiskos apakškomponentus, iekļaujot tos pieprasījuma prognozēšanā. Šajā gadījumā, ja ir atzīmēta izvēles rūtiņa **Ražošanas rinda**, tiek aprēķināta atkarīgā prognoze. 

Pastāv divas metodes, kā izveidot bāzes budžeta dinamika 365 operācijām. Lai ģenerētu prognozi, var izmantot prognozēšanas modeļus virs vēsturiskajiem datiem vai var vienkārši kopēt uz vēsturiskajiem datiem. Laukā **Prognozes ģenerēšanas stratēģija** var izvēlēties vienu no šīm divām metodēm. Lai izmantotu prognozes modeļus, atlasiet vienumu **Azure Machine Learning**. 

Noklikšķinot uz **Prognozes dimensijas** lapas **Pieprasījuma prognozēšanas parametri** kreisajā rūtī, var atlasīt arī pieprasījuma apjoma prognozes ģenerēšanā izmantojamās prognozes dimensijas. Prognozes dimensija norāda to detalizēto datu līmeni, kam prognoze ir definēta. Obligātās prognozes dimensijas ir uzņēmums, vieta un krājumu sadalījuma princips, bet var ģenerēt arī prognozes noliktavas, krājumu statusa, debitoru grupas, debitora konta, valsts/reģiona, pavalsts un krājuma, kā arī visu krājuma dimensiju līmenī. 

Jebkurā brīdī dimensiju sarakstam var pievienot pieprasījuma prognozēšanā izmantotās prognozes dimensijas. Prognozes dimensijas var arī sarakstā dzēst. Tomēr, ja prognozes dimensija tiek pievienota vai noņemta, tiek zaudētas manuāli veiktās korekcijas. 

No pieprasījuma prognozēšanas perspektīvas uz visiem krājumi neattiecas vienādi principi. Līdzīgus krājumus var grupēt pēc viena krājumu sadalījuma principa, un parametrus, piemēram, transakcijas tipus un prognozes metodes iestatījumus, var iestatīt katram krājumu sadalījuma principam. Noklikšķiniet uz **Krājumu sadalījuma princips** lapas **Pieprasījuma prognozēšanas parametri** kreisajā rūtī. 

Lai ģenerētu budžeta, Dynamics 365 operācijām izmanto Machine Learning web pakalpojumu. Lai izveidotu savienojumu ar pakalpojumu, ir jānorāda Dynamics 365 operācijām šādu informāciju, ja jūs piesakieties Microsoft Azure Machine Learning Studio:

-   Tīmekļa pakalpojuma lietojumprogrammas interfeisa (API) atslēga
-   Tīmekļa pakalpojuma galapunkta URL
-   Azure krātuves konta nosaukums
-   Azure krātuves konta atslēga

**Piezīme.** Azure krātuves konta nosaukums un atslēga ir jānorāda tikai tad, ja tiek izmantots pielāgots krātuves konts. Ja lokālā versija, jābūt pielāgotu krātuves kontam par debeszils, mašīnu apmācības pakalpojums varētu piekļūt vēsturiskus datus. 

Lai izveidotu pieprasījuma prognozes, var izvietot savu pakalpojumu, izmantojot mašīnu apmācības studija vai Dynamics 365 operācijas pieprasījuma prognozēšanai eksperimentu. Instrukcijas izvietošanas Dynamics 365 operācijas pieprasījuma prognozēšanas eksperimentus, kā interneta pakalpojumu ir pieejama Dynamics 365 operācijām. Lapā **Pieprasījuma prognozēšanas parametri** noklikšķiniet uz cilnes **Azure Machine Learning**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Iestatījumi Dynamics 365 operācijām pieprasījuma prognozēšanas mašīnu apmācības pakalpojumu
Lai apskatītu parametrus, kurus var konfigurēt Dynamics 365 par operācijas pieprasījuma prognozēšanas dienests, dodieties uz **vispārējā plānošana**&gt;**Setup**&gt;**pieprasījuma prognozēšanas**&gt;**prognozēšanas algoritma parametru**. **Prognozēšanas algoritma parametru** lapa rāda noklusējuma parametru vērtības. Šie parametri var pārrakstīt uz **pieprasījuma prognozēšanas parametrus** lapā. Lai vispārēji pārrakstītu parametrus, izmantojiet cilni **Vispārīgi** vai izmantojiet cilni **Krājumu sadalījuma principi**, lai pārrakstītu katra krājumu sadalījuma principa parametrus. Krājumu sadalījuma principa pārrakstītos parametrus ietekmē tikai krājumu prognoze, kas ir saistīta ar šo krājumu sadalījuma principu.

<a name="see-also"></a>Skatiet arī
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


