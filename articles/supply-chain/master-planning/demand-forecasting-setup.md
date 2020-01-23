---
title: Pieprasījuma prognozēšanas iestatīšana
description: Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f56157be8cc61486801fc4c01bb191432dd9a541
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935495"
---
# <a name="demand-forecasting-setup"></a>Pieprasījuma prognozēšanas iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei.  

Iestatīšanas uzdevumi ietver tālāk minēto datu un parametru iestatīšanu.

## <a name="item-allocation-key"></a>Krājumu sadalījuma princips
Pieprasījuma apjoma prognoze tiek aprēķināta krājumam un tā dimensijām tikai tad, ja uz krājumu attiecas krājumu sadalījuma princips. Šī kārtula tiek izmantota, lai grupētu lielu krājumu skaitu, kas ļauj paātrināt pieprasījuma apjoma prognožu izveidošanu. Ģenerējot pieprasījuma apjoma prognozes, krājumu sadalījuma principa procentuālais īpatsvars tiek ignorēts. Prognozes tiek veidotas, pamatojoties tikai uz vēsturiskajiem datiem. 

Krājumam un tā dimensijām jābūt iekļautiem tikai vienā krājumu sadalījuma principā, ja krājumu sadalījuma princips tiek izmantots prognozes sagatavošanas laikā. 

Lai krājumu sadalījuma principam pievienotu noliktavas vienību (stock keeping unit — SKU), dodieties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Pieprasījuma prognozēšana** &gt; **Krājumu sadalījuma principi**. Lai piešķirtu krājumu sadalījuma principam, izmantojiet lapu **Krājumu piešķiršana**.

## <a name="intercompany-planning-groups"></a>Starpuzņēmumu plānošanas grupas
Pieprasījuma prognozēšanas laikā tiek izveidotas starpuzņēmumu prognozes. Programmā Dynamics 365 Supply Chain Management uzņēmumi, kuriem plānošana tiek veikta kopā, tiek grupēti vienā starpuzņēmumu plānošanas grupā. Lai katram uzņēmumam norādītu, kuri krājumu sadalījuma principi jāņem vērā, veicot pieprasījuma prognozēšanu, krājumu sadalījuma princips ir jāsaista ar starpuzņēmumu plānošanas grupas dalībnieku, dodoties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Starpuzņēmumu plānošanas grupas**. 

Ja starpuzņēmumu plānošanas grupas dalībniekiem nav piešķirts neviens krājumu sadalījuma princips, pēc noklusējuma pieprasījuma apjoma prognoze tiek aprēķināta visiem krājumiem, kas ir piešķirti visiem krājumu sadalījuma principiem visiem uzņēmumiem. Lapā **Statistiskās bāzlīnijas prognozes ģenerēšana** ir pieejamas papildu uzņēmumu un krājumu sadalījuma principu filtrēšanas opcijas. 

Pārskatiet prognozēto krājumu skaitu. Nevajadzīgie krājumi var izraisīt izmaksu palielināšanos, ja izmantojat Microsoft Azure algoritmisko mācīšanos.

## <a name="demand-forecasting-parameters"></a>Pieprasījuma prognozēšanas parametri
Lai iestatītu pieprasījuma prognozēšanas parametrus, dodieties uz **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Pieprasījuma prognozēšanas parametri**. Tā kā pieprasījuma prognozēšana ietver starpuzņēmumus, iestatījumiem ir globāla nozīme. Tas nozīmē, ka iestatījumi attiecas uz visiem uzņēmumiem. 

Pieprasījuma prognozēšanas laikā tiek ģenerēta daudzumu prognoze. Tāpēc laukā **Pieprasījuma apjoma prognozes vienība** ir jānorāda mērvienība, ar kādu ir jāizsaka daudzums. Mērvienībai ir jābūt unikālai, lai varētu nodrošināt, ka ir skaidri saprotams apkopojums un procentuālais sadalījums. Lai iegūtu sīkāku informāciju par apkopojumu un procentuālo iedalījumu, skatiet sadaļu [Bāzlīnijas prognozes manuālu korekciju veikšana](manual-adjustments-baseline-forecast.md). Pārliecinieties, vai uz visām pieprasījuma prognozēšanā iekļautajām noliktavas vienībām izmantotajām mērvienībām attiecas mērvienības un vispārējās prognozēšanas mērvienības konvertēšanas kārtula. Kad tiek palaista prognozes ģenerēšana, tiek reģistrēts to krājumu saraksts, kam nav veikta mērvienības konvertēšana, kas ļauj ērti labot iestatījumus. 

Pieprasījuma prognozēšanu var izmantot, lai prognozētu gan atkarīgu, gan neatkarīgu pieprasījumu. Piemēram, ja atzīmēta ir tikai izvēles rūtiņa **Pārdošanas pasūtījums** un ja visi pieprasījuma prognozēšanā iekļautie krājumi ir pārdoti, sistēmā tiek aprēķināts neatkarīgais pieprasījums. Tomēr krājumu sadalījuma principiem var pievienot kritiskos apakškomponentus, iekļaujot tos pieprasījuma prognozēšanā. Šajā gadījumā, ja ir atzīmēta izvēles rūtiņa **Ražošanas rinda**, tiek aprēķināta atkarīgā prognoze. 

Bāzlīnijas prognozes izveidošanai ir pieejamas divas metodes. Lai ģenerētu prognozi, var izmantot prognozēšanas modeļus virs vēsturiskajiem datiem vai var vienkārši kopēt uz vēsturiskajiem datiem. Laukā **Prognozes ģenerēšanas stratēģija** var izvēlēties vienu no šīm divām metodēm. Lai izmantotu prognozes modeļus, atlasiet vienumu **Azure Machine Learning**. 

Noklikšķinot uz **Prognozes dimensijas** lapas **Pieprasījuma prognozēšanas parametri** kreisajā rūtī, var atlasīt arī pieprasījuma apjoma prognozes ģenerēšanā izmantojamās prognozes dimensijas. Prognozes dimensija norāda to detalizēto datu līmeni, kam prognoze ir definēta. Obligātās prognozes dimensijas ir uzņēmums, vieta un krājumu sadalījuma princips, bet var ģenerēt arī prognozes noliktavas, krājumu statusa, debitoru grupas, debitora konta, valsts/reģiona, pavalsts un krājuma, kā arī visu krājuma dimensiju līmenī. 

Jebkurā brīdī dimensiju sarakstam var pievienot pieprasījuma prognozēšanā izmantotās prognozes dimensijas. Prognozes dimensijas var arī sarakstā dzēst. Tomēr, ja prognozes dimensija tiek pievienota vai noņemta, tiek zaudētas manuāli veiktās korekcijas. 

No pieprasījuma prognozēšanas perspektīvas uz visiem krājumi neattiecas vienādi principi. Līdzīgus krājumus var grupēt pēc viena krājumu sadalījuma principa, un parametrus, piemēram, transakcijas tipus un prognozes metodes iestatījumus, var iestatīt katram krājumu sadalījuma principam. Noklikšķiniet uz **Krājumu sadalījuma princips** lapas **Pieprasījuma prognozēšanas parametri** kreisajā rūtī. 

Lai ģenerētu prognozi, programmā Supply Chain Management tiek izmantots algoritmiskās mācīšanās tīmekļa pakalpojums. Ja pierakstāties pakalpojumā Microsoft Azure Machine Learning Studio (klasikā), tad, lai izveidotu savienojumu ar pakalpojumu, ir jāievada tālāk norādītā informācija.

-   Tīmekļa pakalpojuma lietojumprogrammas interfeisa (API) atslēga
-   Tīmekļa pakalpojuma galapunkta URL
-   Azure krātuves konta nosaukums
-   Azure krātuves konta atslēga

> [!NOTE]
> Azure krātuves konta nosaukums un atslēga ir jānorāda tikai tad, ja tiek izmantots pielāgots krātuves konts. Ja tiek izmantota lokālā versija, ir nepieciešams pielāgots krātuves konts pakalpojumā Azure, lai pakalpojums Algoritmiskā mācīšanās varētu piekļūt vēsturiskajiem datiem. 

Lai izveidotu pieprasījuma apjoma prognozes, varat izvietot savu pakalpojumu, izmantojot Machine Learning Studio vai Supply Chain Management pieprasījuma prognozēšanas eksperimentus. Norādījumi par to, kā izvietot pieprasījuma prognozēšanas eksperimentus kā tīmekļa pakalpojumu, ir pieejami programmā Supply Chain Management. Lapā **Pieprasījuma prognozēšanas parametri** noklikšķiniet uz cilnes **Azure Machine Learning**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Pieprasījuma prognozēšanas pakalpojuma agoritmiskās mācīšanās iestatījumi
Lai skatītu pieprasījuma prognozēšanas pakalpojuma konfigurējamos parametrus, pārejiet uz sadaļu **Vispārējā plānošana** &gt; **Iestatīšana** &gt; **Pieprasījuma prognozēšana** &gt; **Prognozēšanas algoritma parametri**. Lapā **Prognozēšanas algoritma parametri** ir redzamas parametru noklusējuma vērtības. Šos parametrus var pārlabot lapā **Pieprasījuma prognozēšanas parametri**. Lai vispārēji pārrakstītu parametrus, izmantojiet cilni **Vispārīgi** vai izmantojiet cilni **Krājumu sadalījuma principi**, lai pārrakstītu katra krājumu sadalījuma principa parametrus. Krājumu sadalījuma principa pārrakstītos parametrus ietekmē tikai krājumu prognoze, kas ir saistīta ar šo krājumu sadalījuma principu.

### <a name="forecast-algorithm-parameters"></a>Budžeta algoritma parametri

Cilnē **Sadalījuma principi** jūs varat iestatīt **Prognozēšanas algoritma parametri** katram krājumu sadalījuma principam. Ir pieejamas tālāk minētās opcijas.
- **Ticamības līmeņa procenti**: ticamības intervālu veido vairākas vērtības, kas darbojas kā labs pieprasījuma apjoma prognozes aprēķins. Ticamības līmenis 95% norāda, ka pastāv 5% risks, ka nākamais pieprasījums nebūs ticamības intervāla diapazonā.
- **Spēka sezonalitāte**: norāda, vai piespiest modeli izmantot noteikta veida sezonalitāti. Attiecas tikai uz objektiem ARIMA un ETS. Opcijas: AUTOMĀTISKS (noklusējuma), NAV, ADITĪVS, MULTIPLIKATĪVS.
- **Prognozēšanas modelis**: opcijas: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, VISI. Lai atlasītu atbilstošāko modeli, izmantojiet **VISI**.
- **Maksimālā prognozētā vērtība**: norāda maksimālo vērtību, ko izmantot prognozēm. Formāts: +1E[n] vai skaitliska konstante.
- **Minimālā prognozētā vērtība**: norāda minimālo vērtību, ko izmantot prognozēm. Formāts: -1E[n] vai skaitliska konstante.
- **Trūkstošās vērtības aizvietošana**: norāda, kā tiek aizpildītas atstarpes vēsturiskajos datos. Opcijas: skaitliska vērtība, VIDĒJAIS, IEPRIEKŠĒJAIS, INTERPOLĒTS LINEĀRS, INTERPOLĒTS POLINOMA.
- **Trūkstošās vērtības aizstāšanas tvērums**: norāda, vai vērtības aizvietošana attiecas tikai uz katra atsevišķa granularitātes atribūta datu diapazonu, vai uz visu datu kopu. Opcijas: GRANULARITĀTES_ATRIBŪTS (noklusējuma), GLOBĀLS.
- **Sezonalitātes norādījums**: sezonas datiem norādiet prognozēšanas modeļa atgādinājumu, lai uzlabotu prognozes precizitāti. Formāts: vesels skaitlis, kas norāda intervālu skaitu, kur tiek atkārtots pieprasījuma modelis. Piemēram, ievadiet "6" datiem, kas atkārtojas ik pēc sešiem mēnešiem.
- **Testa kopas lielums procentos**: vēsturisko datu procentuālais daudzums, kas tiks izmantots kā testa kopa, lai aprēķinātu prognozes precizitāti. 

<a name="additional-resources"></a>Papildu resursi
--------

[Pārskats par pieprasījuma prognozēšanu](introduction-demand-forecasting.md)

[Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)

[Manuāla bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)



