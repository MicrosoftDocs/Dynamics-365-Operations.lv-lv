---
title: Pieprasījuma prognozēšanas iestatīšana
description: Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei.
author: ChristianRytt
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f71d7a1ef2e8b6a113124d3fb17f1681d62aed9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575756"
---
# <a name="demand-forecasting-setup"></a>Pieprasījuma prognozēšanas iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti iestatīšanas uzdevumi, kas jāizpilda, sagatavotos pieprasījuma prognozēšanas izpildei.  

Iestatīšanas uzdevumi ietver tālāk minēto datu un parametru iestatīšanu.

## <a name="item-allocation-keys"></a>Krājumu sadalījuma principi

Pieprasījuma apjoma prognoze tiek aprēķināta krājumam un tā dimensijām tikai tad, ja uz krājumu attiecas krājumu sadalījuma princips. Šī kārtula tiek izmantota, lai grupētu lielu krājumu skaitu, kas ļauj paātrināt pieprasījuma apjoma prognožu izveidošanu. Ģenerējot pieprasījuma apjoma prognozes, krājumu sadalījuma principa procentuālais īpatsvars tiek ignorēts. Prognozes tiek veidotas, pamatojoties tikai uz vēsturiskajiem datiem.

Krājumam un tā dimensijām jābūt iekļautiem tikai vienā krājumu sadalījuma principā, ja krājumu sadalījuma princips tiek izmantots prognozes sagatavošanas laikā.

Lai pievienotu noliktavas vienību (SKU) krājuma sadalījuma principam, dodieties uz **Galvenā plānošana \>Iestatījumi \>Pieprasīt prognozi\> krājuma sadalījuma principi**. Lai piešķirtu krājumu sadalījuma principam, izmantojiet lapu **Krājumu piešķiršana**.

## <a name="intercompany-planning-groups"></a>Starpuzņēmumu plānošanas grupas

Pieprasījuma prognozēšanas laikā tiek izveidotas starpuzņēmumu prognozes. Programmā Dynamics 365 Supply Chain Management uzņēmumi, kuriem plānošana tiek veikta kopā, tiek grupēti vienā starpuzņēmumu plānošanas grupā. Lai konkretizētu, kurus krājuma sadalījuma principus vajadzētu ņemt vērā katra uzņēmuma pieprasījuma prognozēšanai, saistiet krājuma sadalījuma principu ar starpuzņēmumu plānošanas grupas dalībnieku, dodoties uz **Galvenā plānošana \> Iestatījumi \> Starpuzņēmumu plānošanas grupas**.

Ja starpuzņēmumu plānošanas grupas dalībniekiem nav piešķirts neviens krājumu sadalījuma princips, pēc noklusējuma pieprasījuma apjoma prognoze tiek aprēķināta visiem krājumiem, kas ir piešķirti visiem krājumu sadalījuma principiem visiem uzņēmumiem. Lapā **Statistiskās bāzlīnijas prognozes ģenerēšana** ir pieejamas papildu uzņēmumu un krājumu sadalījuma principu filtrēšanas opcijas.

Pārskatiet prognozēto krājumu skaitu. Nevajadzīgie krājumi var izraisīt izmaksu palielināšanos, ja izmantojat Microsoft Azure algoritmisko mācīšanos.

## <a name="demand-forecasting-parameters"></a>Pieprasījuma prognozēšanas parametri

Lai iestatītu pieprasījuma prognozēšanas parametrus, dodieties uz **Galvenā plānošana \> Iestatījumi  \> \> Prognozes pieprasīšana \> Prognozes parametru pieprasīšana**. Tā kā pieprasījuma prognozēšana ietver starpuzņēmumus, iestatījumiem ir globāla nozīme. Tas nozīmē, ka iestatījumi attiecas uz visiem uzņēmumiem.

Pieprasījuma prognozēšanas laikā tiek ģenerēta daudzumu prognoze. Tāpēc laukā **Pieprasījuma apjoma prognozes vienība** ir jānorāda mērvienība, ar kādu ir jāizsaka daudzums. Mērvienībai jābūt unikālai, nodrošinātu, ka apkopošanas un īpatsvara izkliede ir loǵiska. Lai iegūtu sīkāku informāciju par apkopojumu un procentuālo iedalījumu, skatiet sadaļu [Bāzlīnijas prognozes manuālu korekciju veikšana](manual-adjustments-baseline-forecast.md). Pārliecinieties, vai uz visām pieprasījuma prognozēšanā iekļautajām noliktavas vienībām izmantotajām mērvienībām attiecas mērvienības un vispārējās prognozēšanas mērvienības konvertēšanas kārtula. Kad tiek palaista prognozes ģenerēšana, tiek reģistrēts to krājumu saraksts, kam nav veikta mērvienības konvertēšana, kas ļauj ērti labot iestatījumus.

Pieprasījuma prognozēšanu var izmantot, lai prognozētu gan atkarīgu, gan neatkarīgu pieprasījumu. Piemēram, ja atzīmēta ir tikai izvēles rūtiņa **Pārdošanas pasūtījums** un ja visi pieprasījuma prognozēšanā iekļautie krājumi ir pārdoti, sistēmā tiek aprēķināts neatkarīgais pieprasījums. Tomēr krājumu sadalījuma principiem var pievienot kritiskos apakškomponentus, iekļaujot tos pieprasījuma prognozēšanā. Šajā gadījumā, ja ir atzīmēta izvēles rūtiņa **Ražošanas rinda**, tiek aprēķināta atkarīgā prognoze.

Bāzlīnijas prognozes izveidošanai ir pieejamas divas metodes. Lai ģenerētu prognozi, var izmantot prognozēšanas modeļus virs vēsturiskajiem datiem vai var vienkārši kopēt uz vēsturiskajiem datiem. Laukā **Prognozes ģenerēšanas stratēģija** var izvēlēties vienu no šīm divām metodēm. Lai izmantotu prognozes modeļus, atlasiet vienumu **Azure Machine Learning**.

Lapas **Pieprasījuma prognozes parametri** kreisajā rūtī atlasot **Prognozes izmēri** varat arī atlasīt prognozes izmēru kopu, kuru izmantot, kad tiek ǵenerēta pieprasījuma prognoze. Prognozes dimensija norāda to detalizēto datu līmeni, kam prognoze ir definēta. Prognozes izmēriem ir nepieciešams uzņēmums, vieta un krājuma sadalījuma princips, taču prognozes varat ǵenerēt arī noliktavas, krājuma statusa, klientu grupas, klientu konta, valsts/reǵiona, statusa un krājuma, kā arī visu krājuma izmēru līmenī.

Jebkurā brīdī dimensiju sarakstam var pievienot pieprasījuma prognozēšanā izmantotās prognozes dimensijas. Prognozes dimensijas var arī sarakstā dzēst. Tomēr, ja prognozes dimensija tiek pievienota vai noņemta, tiek zaudētas manuāli veiktās korekcijas.

Ne visi krājumi no pieprasījuma prognozes skatupunkta ir ar vienādu veiktspēju. Līdzīgus krājumus var grupēt pēc viena krājumu sadalījuma principa, un parametrus, piemēram, transakcijas tipus un prognozes metodes iestatījumus, var iestatīt katram krājumu sadalījuma principam. Lapas **Pieprasījuma prognozes parametri** kreisajā rūtī atlasiet **Krājuma sadalījuma principi**.

Lai ǵenerētu prognozi, Supply Chain Management izmanto algoritmiskās mācīšanās tīmekļa pakalpojumu. Ja pierakstāties pakalpojumā Microsoft Azure Machine Learning Studio (klasikā), tad, lai izveidotu savienojumu ar pakalpojumu, ir jāievada tālāk norādītā informācija.

- Tīmekļa pakalpojuma lietojumprogrammas interfeisa (API) atslēga
- Tīmekļa pakalpojuma galapunkta URL
- Azure krātuves konta nosaukums
- Azure krātuves konta atslēga

> [!NOTE]
> Azure krātuves konta nosaukums un atslēga ir jānorāda tikai tad, ja tiek izmantots pielāgots krātuves konts. Ja tiek izmantota lokālā versija, ir nepieciešams pielāgots krātuves konts pakalpojumā Azure, lai pakalpojums Algoritmiskā mācīšanās varētu piekļūt vēsturiskajiem datiem.

Lai izveidotu pieprasījuma apjoma prognozes, varat izvietot savu pakalpojumu, izmantojot Machine Learning Studio vai Supply Chain Management pieprasījuma prognozēšanas eksperimentus. Norādījumi par to, kā izvietot pieprasījuma prognozēšanas eksperimentus kā tīmekļa pakalpojumu, ir pieejami programmā Supply Chain Management. Lapā **Pieprasījuma prognozes parametri** atveriet cilni **Azure algoritmiskā mācīšanās**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Pieprasījuma prognozēšanas pakalpojuma agoritmiskās mācīšanās iestatījumi

Lai skatītu parametrus, kurus var konfigurēt pieprasījuma prognozēšanas pakalpojumam, dodieties uz **Galvenā plānošana \> Iestatīšana \> Pieprasījuma prognoze \> Prognozes algoritmiskie parametri**. Lapā **Prognozes algoritmiskie noklusējuma parametri** parādītas parametru noklusējuma vērtības. Šos parametrus varat pārrakstīt, dodoties uz **Galvenā plānošana \> Iestatījumi \> Pieprasījuma prognoze \> Pieprasījuma prognozes parametri**, kur varat veikt tālāk norādītās darbības:

- Lietojiet cilni **Vispārīgi**, lai pārrakstītu parametrus vispārīgi.
- Lietojiet cilni **Krājuma sadalījuma principi**, lai pārrakstītu parametrus katram krājuma sadalījuma principam. Krājumu sadalījuma principa pārrakstītos parametrus ietekmē tikai krājumu prognoze, kas ir saistīta ar šo krājumu sadalījuma principu.

### <a name="forecast-algorithm-parameters"></a>Budžeta algoritma parametri

Lapas **Pieprasījuma prognozes parametri** cilnē **Krājuma sadalījuma principi** varat lietot kopsavilkuma cilni **Prognozes algoritmiskie parametri**, lai piešķirtu prognozes algoritmiskos parametrus krājuma sadalījuma principam, kas pašlaik atlasīts režģī pa kreisi. Izmantojiet rīkjoslas pogas **Pievienot** un **Noņemt**, lai izveidotu vajadzīgo parametru kolekciju. Katram saraksta parametram atlasiet vienu no šīm vērtībām laukā **Nosaukums** un laukā **Vērtība** ievadiet atbilstošo vērtību:

- **Ticamības līmeņa procenti** — Ticamības intervāls sastāv no vērtību diapazona, kuras darbojas kā labi pieprasījuma prognozes aptuvenie rezultāti. Ticamības līmenis 95% norāda, ka pastāv 5% risks, ka nākamais pieprasījums nebūs ticamības intervāla diapazonā.
- **Uzspiest sezonalitāti** — Konkretizē, vai uzspiest modelim noteikta veida sezonalitātes lietošanu. Attiecas tikai uz objektiem ARIMA un ETS. Opcijas: AUTOMĀTISKS (noklusējuma), NAV, ADITĪVS, MULTIPLIKATĪVS.
- **Prognozēšanas modelis** — Opcijas: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALL.  Lai atlasītu atbilstošāko modeli, izmantojiet **VISI**.
- **Maksimālās prognozētās vērtības** — Konkretizē maksimālo vērtību, kuru izmantot prognozēs. Formāts: +1E[n] vai skaitliska konstante.
- **Minimālās prognozētās vērtības** — Konkretizē minimālo vērtību, kuru izmantot prognozēs. Formāts: -1E[n] vai skaitliska konstante.
- **Trūkst vērtības aizstājēja** — Konkretizē, kā tiek aizpildītas trūkstošās vietas vēsturiskajos datos. Opcijas: skaitliska vērtība, VIDĒJAIS, IEPRIEKŠĒJAIS, INTERPOLĒTS LINEĀRS, INTERPOLĒTS POLINOMA.
- **Trūkstošais vērtības aizstājēja tvērums** — Konkretizē, vai vērtības aizstājējs attiecas tikai uz katras atsevišķās granularitātes atribūta datu diapazonu vai uz visu datu kopu. Datumu diapazona, kuru sistēma izmanto, aizpildot trūkstošās vietas vēsturiskajos datos, izveidošanai ir pieejamas tālāk norādītās opcijas:

  - VISPĀRĪGI — Sistēma izmanto pilno visu granularitātes atribūtu datumu diapazonu.
  - HISTORY_DATE_RANGE – Sistēma izmanto konkrētu datumu diapazonu, kas dialoglodziņa **Ģenerēt statistisko bāzlīnijas prgonozi** lauka grupā **Vēsturiskais horizonts** definēts laukos **Datums no** un **Datums līdz**.
  - GRANULARITY_ATTRIBUTE — Sistēma izmanto pašlaik apstrādātā granularitātes atribūta datumu diapazonu.

  > [!NOTE]
  > Granularitātes atribūts ir prognozes izmēru kombinācija, attiecībā pret kuru tiek veikta prognoze. Prognozes izmērus varat definēt lapā **Pieprasījuma prognozes parametri**.

- **Sezonalitātes norāde** — Nodrošina sezonalitātes datu norādi prognozēšanas modelim, lai uzlabotu prognozes precizitāti. Formāts: vesels skaitlis, kas norāda intervālu skaitu, kur tiek atkārtots pieprasījuma modelis. Piemēram, ievadiet "6" datiem, kas atkārtojas ik pēc sešiem mēnešiem.
- **Testa kopas izmēra procentuālais daudzums** — Vēsturisko datu īpatsvars, kurus jāizmanto kā prognozes precizitātes aprēķina testa kopa.

## <a name="additional-resources"></a>Papildu resursi

- [Pārskats par pieprasījuma prognozēšanu](introduction-demand-forecasting.md)
- [Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)
- [Manuāla bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
