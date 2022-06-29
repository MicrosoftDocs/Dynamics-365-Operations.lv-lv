---
title: Pieprasījuma prognozēšanas iestatīšana
description: Šajā rakstā ir aprakstīti iestatīšanas uzdevumi, kas jāveic, lai sagatavotos pieprasījuma prognozēšanai.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fae2ac53dec8696075e7506d979c1cf9fb277af5
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960159"
---
# <a name="demand-forecasting-setup"></a>Pieprasījuma prognozēšanas iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt pieprasījuma prognozēšanu.  

## <a name="item-allocation-keys"></a>Krājumu sadalījuma principi

Krājumu sadalījuma principi izveido krājumu grupas. Pieprasījuma apjoma prognoze tiek aprēķināta krājumam un tā dimensijām tikai tad, ja uz krājumu attiecas krājumu sadalījuma princips. Šis noteikums tiek ieviests liela krājumu skaita grupēšanai, lai pieprasījuma apjoma prognozes varētu izveidot ātrāk. Prognozes tiek veidotas, pamatojoties tikai uz vēsturiskajiem datiem.

Krājumam un tā dimensijām jābūt iekļautiem tikai vienā krājumu sadalījuma principā, ja krājumu sadalījuma princips tiek izmantots prognozes sagatavošanas laikā.

Lai izveidotu krājumu sadalījuma principus un pievienotu tiem noliktavas vienību (NV), veiciet šos soļus.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Pieprasījuma prognozēšana \> Krājumu sadalījuma principi**.
1. Atlasiet krājumu sadalījuma principu saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu. Jaunā vai atlasītās atslēgas virsrakstā iestatiet šādus laukus:

    - **Krājumu sadalījuma princips** – ievadiet unikālu atslēgas nosaukumu.
    - **Nosaukums** – ievadiet atslēgas aprakstošo nosaukumu.

1. Lai pievienotu krājumus atlasītajam krājumu sadalījuma principam vai noņemtu krājumus, veiciet vienu no tālāk minētajām darbībām:

    - Kopsavilkuma cilnē **Krājumu sadalījums** izmantojiet rīkjoslas **pogas Jauns** **un Dzēst**, lai pievienotu vai noņemtu krājumus pēc vajadzības. Katrai rindai atlasiet krājuma kodu un pēc tam pēc tam piešķiriet dimensiju vērtības citās kolonnās pēc izvēles. Lai **mainītu** režģī rādīto dimensiju kolonnu kopu, rīkjoslā atlasiet Rādīt dimensijas. (Vērtība laukā **Ģenerējot** pieprasījuma apjoma prognozes, procentu kolonna tiek ignorēta.)
    - Ja vēlaties atslēgai pievienot lielu skaitu krājumu, darbību rūtī atlasiet Piešķirt krājumus, **lai** atvērtu lapu, kurā atlasītajai atslēgai varat atrast un piešķirt vairākus krājumus.

> [!IMPORTANT]
> Esiet uzmanīgi, lai iekļautu tikai atbilstošus krājumus katrā krājumu sadalījuma atslēgā. Nevajadzīgie krājumi var izraisīt izmaksu palielināšanos, ja izmantojat Microsoft Azure algoritmisko mācīšanos.

## <a name="intercompany-planning-groups"></a>Starpuzņēmumu plānošanas grupas

Pieprasījuma apjoma prognozēšana var ģenerēt starpuzņēmumu prognozes. Uzņēmumi Dynamics 365 Supply Chain Management, kas plānoti kopā, tiek grupēti vienā starpuzņēmumu plānošanas grupā. Lai norādītu, uz uzņēmumu, kuri krājumu sadalījuma principi ir jāņem vērā pieprasījuma prognozēšanai, saistiet krājumu sadalījuma principu ar starpuzņēmumu plānošanas grupas dalībnieku.

> [!IMPORTANT]
> Optimizācijas plānošana pašlaik neatbalsta starpuzņēmumu plānošanas grupas. Lai izdarītu starpuzņēmumu plānošanu, kas izmanto optimizācijas plānošanu, iestatiet vispārējās plānošanas pakešuzdevumus, kas ietver vispārējos plānus visiem atbilstošajiem uzņēmumiem.

Lai iestatītu starpuzņēmumu plānošanas grupas, veiciet šādus soļus.

1. Dodieties uz **vispārējās plānošanas \> iestatījumu \> starpuzņēmumu plānošanas grupām**.
1. Atlasiet plānošanas grupu saraksta rūtī vai atlasiet Jauns **darbību** rūtī, lai izveidotu jaunu. Jaunās vai atlasītās grupas virsrakstā iestatiet šādus laukus:

    - **Nosaukums** – ievadiet plānošanas grupas unikālu nosaukumu.
    - **Apraksts** – ievadiet īsu plānošanas grupas aprakstu.

1. Kopsavilkuma cilnē **Starpuzņēmumu plānošanas** grupas dalībnieki izmantojiet rīkjoslas pogas, lai pievienotu rindu katram uzņēmumam (juridiskajai personai), kam vajadzētu būt grupas daļai. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Juridiska persona** – atlasiet nosaukumu uzņēmumam (juridiskajai personai), kas ir atlasītās grupas dalībnieks.
    - **Plānošanas secība –** piešķiriet pasūtījumu, kādā uzņēmums jāapstrādā saistībā ar citiem uzņēmumiem. Vispirms tiek apstrādātas mazvērtības. Šis pasūtījums var būt svarīgs, kad viena uzņēmuma pieprasījums ietekmē citus uzņēmumus. Šādos gadījumos pēdējais ir jāapstrādā uzņēmums, kas nodrošina pieprasījumu.
    - **vispārējais** plāns – atlasiet vispārējo plānu, kas jāaktivizē pašreizējam uzņēmumam;
    - **Automātiska statiskā plāna kopēšana** – atzīmējiet šo izvēles rūtiņu, lai kopētu plāna rezultātu uz statisko plānu.
    - **Automātiska dinamiskā plāna kopēšana —** atzīmējiet šo izvēles rūtiņu, lai kopētu plāna rezultātus uz dinamisko plānu.

1. Ja starpuzņēmumu plānošanas grupas dalībniekiem nav piešķirts neviens krājumu sadalījuma princips, pēc noklusējuma pieprasījuma apjoma prognoze tiek aprēķināta visiem krājumiem, kas ir piešķirti visiem krājumu sadalījuma principiem visiem uzņēmumiem. Papildu filtrēšanas opcijas uzņēmumiem **un krājumu sadalījuma atslēgas ir pieejamas dialoglodziņā Statistiskās bāzlīnijas** prognozes ģenerēšana (**Vispārējās \>\>\> plānošanas pieprasījuma apjoma prognozēšanas ģenerēšana Ģenerēt statistiskās bāzlīnijas prognozi**). Lai piešķirtu krājumu sadalījuma principus uzņēmumam atlasītajā starpuzņēmumu plānošanas grupā, **·** **atlasiet** uzņēmumu un pēc tam kopsavilkuma cilnē Starpuzņēmumu plānošanas grupas dalībnieki atlasiet Krājumu sadalījuma principus rīkjoslā.

> [!IMPORTANT]
> Pārliecinieties, vai katrā starpuzņēmumu plānošanas grupā jāiekļauj tikai atbilstoši krājumu sadalījuma principi. Nevajadzīgi krājumi var radīt palielinātas izmaksas, ja lietojat Azure mašīnas apmācību.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a> Iestatīt pieprasījuma prognozēšanas parametrus

Izmantojiet lapu **Pieprasījuma prognozēšanas parametri**, lai iestatītu vairākas opcijas, kas kontrolēs to, kā pieprasījuma apjoma prognozēšana darbosies jūsu sistēmā.

### <a name="open-the-demand-forecasting-parameters-page"></a>Atvērt lapu Pieprasījuma prognozēšanas parametri

Lai iestatītu pieprasījuma prognozēšanas parametrus, dodieties uz vispārējās **plānošanas iestatījuma \>\> Pieprasījuma prognozēšanas pieprasījuma prognozēšanas \> parametriem**. Tā kā pieprasījuma prognozēšana ietver starpuzņēmumus, iestatījumiem ir globāla nozīme. Citiem vārdiem sakot, tas attiecas uz visām juridiskajām personām (uzņēmumiem).

### <a name="general-settings"></a>Vispārīgie iestatījumi

Lietojiet **lapas Pieprasījuma** prognozēšanas parametri **cilni** Vispārīgi, lai definētu vispārīgos iestatījumus pieprasījuma prognozēšanai.

#### <a name="demand-forecast-unit"></a>Pieprasījuma apjoma prognozes vienība

Pieprasījuma prognozēšanas laikā tiek ģenerēta daudzumu prognoze. Tāpēc laukā **Pieprasījuma apjoma prognozes vienība** ir jānorāda mērvienība, ar kādu ir jāizsaka daudzums. Šis lauks nosaka vienību, kas tiks izmantota visām pieprasījuma apjoma prognozēm neatkarīgi no parastajām krājumu vienībām katrai precei. Izmantojot konsekventu prognozes vienību, palīdziet nodrošināt, ka apkopojumam un procentuālajai sadalei ir nozīme. Lai iegūtu sīkāku informāciju par apkopojumu un procentuālo iedalījumu, skatiet sadaļu [Bāzlīnijas prognozes manuālu korekciju veikšana](manual-adjustments-baseline-forecast.md).

Visām NV mērvienībām, kas ir iekļautas pieprasījuma prognozē, pārliecinieties, vai pastāv mērvienībai un vispārīgai prognozēšanas mērvienībai paredzēts konvertēšanas noteikums, ko šeit atlasāt. Ģenerējot prognozi, tiek reģistrēts to krājumu saraksts, kuriem nav mērvienības pārvēršanas. Tādēļ iestatījumu var viegli labot. Papildinformāciju par mērvienībām un to, kā tās pārveidot, skatiet [sadaļā Mērvienību pārvaldība](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Darbību tipi

Izmantojiet laukus Darbību tipu **FastTab**, lai atlasītu darbību tipus, kas tiek izmantoti, kad tiek ģenerēta statistiskās bāzlīnijas prognoze.

Pieprasījuma apjoma prognozēšanu var izmantot, lai prognozētu gan pakārtoto pieprasījumu, gan neatkarīgu pieprasījumu. Piemēram, ja **tikai** *pārdošanas* pasūtījuma opcija ir iestatīta uz Jā un visi krājumi, kas tiek apsvērti pieprasījuma prognozēšanai, ir krājumi, kas tiek pārdoti, sistēma aprēķina neatkarīgu pieprasījumu. Tomēr krājumu sadalījuma principiem var pievienot kritiskos apakškomponentus, iekļaujot tos pieprasījuma prognozēšanā. Šajā gadījumā, ja opcija Ražošanas **rinda** ir iestatīta uz *Jā*, tiek aprēķināta pakārtotā prognoze.

Darbības tipus vienam vai vairākiem specifiskiem krājumu sadalījuma taustiņiem var ignorēt, izmantojot **cilni Krājumu sadalījuma** principi. Šī cilne nodrošina līdzīgus laukus.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Izvēlieties, kā izveidot bāzlīnijas prognozi

Prognozes **ģenerēšanas stratēģijas lauks** ļauj atlasīt metodi, kas tiek izmantota, lai izveidotu bāzlīnijas prognozi. Ir pieejamas trīs metodes:

- *Kopēt vēsturiskā pieprasījuma laikā* – izveidojiet prognozes, vienkārši kopējot vēsturiskos datus.
- *Azure mašīnas apmācības pakalpojums* – izmantojiet prognozes modeli, kas izmanto Azure mašīnas apmācības pakalpojumu. Azure datora apmācības pakalpojums ir pašreizējais mašīnas apmācības risinājums azure. Tāpēc ieteicams to lietot, ja vēlaties lietot budžeta modeli.
- *Azure mašīnas apmācība* – izmantojiet prognozes modeli, kurā tiek lietota Azure Machine Learning Studio (maks). Azure mašīnas mācību studija (azure Machine Learning Studio ) ir novecojusi un drīzumā tiks noņemta no Azure. Tādēļ ir ieteicams atlasīt *Azure datora apmācības pakalpojumu*, ja pirmo reizi iestatāt pieprasījuma prognozēšanu. Ja pašlaik izmantojat Azure Machine Learning Studio (azure Machine Learning Studio), jums pēc iespējas ātrāk jāplāno pārslēgties uz Azure datora apmācību pakalpojumu.

Izmantojot cilni Krājumu sadalījuma principi, varat ignorēt prognozes ģenerēšanas metodi vienai vai vairākām specifiskām krājumu **sadalījuma atslēgām** . Šī cilne nodrošina līdzīgus laukus.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Ignorēt noklusējuma prognozes algoritma parametrus globālā mērogā

Noklusējuma prognozes algoritma parametri un vērtības ir piešķirtas pieprasījuma **prognozēšanas parametru** lapā (**Vispārējās plānošanas iestatījuma \>\> pieprasījuma prognozēšanas pieprasījuma \> prognozēšanas parametri**). Tomēr jūs varat ignorēt tos **globāli**, izmantojot prognozes algoritma parametru **kopsavilkuma cilni,** **kas atrodas lapas Pieprasījuma prognozēšanas parametri cilnē** Vispārīgi. (Varat arī ignorēt tos noteiktiem sadalījuma principus, izmantojot **Krājumu sadalījuma atslēgu** cilne lapā Pieprasījuma **prognozēšanas parametri** .)

Izmantojiet rīkjoslas **pogas** **Pievienot** un noņemt, lai izveidotu nepieciešamo parametru ignorēšanas kolekciju. Katram parametram sarakstā atlasiet vērtību laukā Nosaukums **un** pēc tam laukā Vērtība ievadiet atbilstošu **vērtību**. Visi parametri, kas nav uzskaitīti šeit, izmantos to vērtības no pieprasījuma prognozēšanas **parametru lapas iestatījumiem**. Papildinformāciju par to, kā izmantot parametru standarta kopu un to vērtības atlasīt, [skatiet sadaļā Pieprasījuma prognozēšanas modeļu noklusētie parametri un](#model-parameters) vērtības.

### <a name="set-forecast-dimensions"></a>Iestatīt prognozes dimensijas

Prognozes dimensija norāda to detalizēto datu līmeni, kam prognoze ir definēta. Uzņēmums, vieta un krājumu sadalījuma princips ir nepieciešamas prognožu dimensijas. Var ģenerēt arī prognozes noliktavā, krājumu statusā, debitoru grupā, debitora kontā, valstī/reģionā, štatā un/vai krājuma līmenī un visos krājumu dimensiju līmeņos. Izmantojiet cilni **Prognozes dimensijas** lapā **Pieprasījuma** prognozēšanas parametri, lai atlasītu prognozes dimensiju kopu, ko izmanto, kad tiek ģenerēta pieprasījuma apjoma prognoze.

Jebkurā laikā varat pievienot prognozes dimensijas to dimensiju sarakstam, kas tiek izmantotas pieprasījuma prognozēšanai. Prognozes dimensijas var arī sarakstā dzēst. Tomēr, ja prognozes dimensija tiek pievienota vai noņemta, tiek zaudētas manuāli veiktās korekcijas.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Iestatīt ignorēšanu noteiktiem krājumu sadalījuma principus

Ne visi vienumi darbojas vienādi no pieprasījuma prognozēšanas perspektīvas. Tāpēc varat izveidot sadalījuma principu – specifiskus ignorējumus vairumam cilnē Vispārīgi definēto **iestatījumu**. Izņēmums ir pieprasījuma apjoma prognozes vienība. Lai iestatītu ignorēšanu specifiskam krājumu sadalījuma principam, sekojiet šiem soļiem.

1. Lapā Pieprasījuma **prognozēšanas** **parametri** cilnē Krājumu sadalījuma principi izmantojiet rīkjoslas pogas, lai pievienotu krājumu sadalījuma principus režģim kreisajā pusē, vai aizvāciet tos pēc pieprasījuma. Pēc tam atlasiet sadalījuma principu, kuram vēlaties iestatīt ignorēšanu.
1. Kopsavilkuma cilnē **Darbību tipi** iespējojiet darbību veidus, ko vēlaties izmantot, lai ģenerētu statistiskās bāzlīnijas prognozi precēm, kas pieder atlasītajam sadalījuma principam. Iestatījumi darbojas tieši tāpat, kā tie **darbojas** cilnē Vispārīgi, bet tie attiecas tikai uz atlasīto krājumu sadalījuma principu. Visiem iestatījumiem šeit (gan *vērtībām Jā*, gan *Vērtību Nav*) ir prioritāte visiem **darbību tipu** iestatījumiem **cilnē** Vispārīgi.
1. Kopsavilkuma cilnē **Prognozes algoritma parametri** atlasiet prognozes ģenerēšanas stratēģiju un prognozes algoritma parametru ignorēšanu precēm, kas pieder atlasītajai sadalījuma atslēgai. Šie iestatījumi darbojas tieši tāpat, kā tie **darbojas** cilnē Vispārīgi, bet tie attiecas tikai uz atlasīto krājumu sadalījuma principu. Izmantojiet rīkjoslas **pogas** **Pievienot** un noņemt, lai definētu nepieciešamo parametru ignorēšanas kolekciju. Katram parametram sarakstā atlasiet vērtību laukā Nosaukums **un** pēc tam laukā Vērtība ievadiet atbilstošu **vērtību**. Papildinformāciju par to, kā izmantot parametru standarta kopu un to vērtības atlasīt, [skatiet sadaļā Pieprasījuma prognozēšanas modeļu noklusētie parametri un](#model-parameters) vērtības.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Savienojuma iestatīšana ar Azure Machine Learning Service

Lai iestatītu **savienojumu ar Azure Machine Learning Service, izmantojiet cilni Azure Machine Learning** Service. Šis risinājums ir viena no bāzlīnijas prognozes izveides opcijām. Šie iestatījumi šajā cilnē ir spēkā tikai tad **, ja lauks Prognozes ģenerēšanas stratēģija** ir iestatīts uz *Azure Machine Learning Service*.

Papildinformāciju par to, kā iestatīt Azure datora apmācību pakalpojumu un pēc tam izmantot šeit iestatījumus, lai izveidotu savienojumu ar to, [skatiet sadaļā Azure Datora apmācību pakalpojums](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Savienojuma iestatīšana ar Azure Machine Learning Studio (iestata)

> [!IMPORTANT]
> Azure mašīnas mācību studija (maks. ) ir novecojusi. Tādēļ vairs nevarat izveidot tam Azure jaunas darbvietas. To ir aizstājis Azure mašīnas apmācības pakalpojums, kas nodrošina līdzīgu funkcionalitāti un citu informāciju. Ja vēl neizmantojat Azure mašīnas apmācību, jums jāsāk izmantot Azure mašīnas apmācības pakalpojumu. Ja jums jau ir darbvieta, kas izveidota Azure Datora apmācību studijai (azure Machine Learning Studio ) (azure), varat turpināt tās izmantošanu, līdz šī funkcija ir pilnībā noņemta no Azure. Tomēr ir ieteicams atjaunināt Azure mašīnas apmācības pakalpojumu pēc iespējas ātrāk. Lai arī programma turpinās jūs brīdināt, ka Azure Machine Learning Studio (amortizēta) ir novecojusi, prognozēšanas rezultāts netiks ietekmēts. Papildinformāciju par jauno Azure mašīnas apmācības pakalpojumu un to, kā to iestatīt, [skatiet sadaļā Azure Machine Learning Service](#setup-amls).
>
> Varat brīvi pārslēgties starp jauno un veco datora apmācību risinājumu izmantošana ar Piegādes ķēžu pārvaldību, kamēr ir pieejama vecā Azure Datora mācību studija (Azure Machine Learning Studio —azure) darbvieta.

Ja jums jau ir pieejama Azure Machine Learning Studio (azure) darbvieta, varat izmantot to, lai ģenerētu prognozes, savienojot to ar piegādes ķēžu pārvaldību. Šo savienojumu var izveidot, izmantojot lapu **Pieprasījuma prognozēšanas parametri** **cilnē Azure Machine Learning**. (Iestatījumiem šajā cilnē ir ietekme tikai tad, ja **Prognozes ģenerēšanas stratēģijas** lauks ir iestatīts uz *Azure Machine Learning*.) Ievadiet tālāk norādīto informāciju par Jūsu Azure Machine Learning Studio (azure) darbalauku:

- Tīmekļa pakalpojuma lietojumprogrammas interfeisa (API) atslēga
- Tīmekļa pakalpojuma galapunkta URL
- Azure krātuves konta nosaukums
- Azure krātuves konta atslēga

> [!NOTE]
> Azure krātuves konta nosaukums un atslēga ir jānorāda tikai tad, ja tiek izmantots pielāgots krātuves konts. Ja izvietojat lokālo versiju, jums ir jābūt pielāgotam glabāšanas kontam azure, lai datora apmācība varētu piekļūt vēsturiskajiem datiem.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a> Pieprasījuma prognozēšanas modeļu noklusējuma parametri un vērtības

Lietojot iekārtu apmācību, lai ģenerētu budžeta plānošanas modeļus, jūs kontrolējiet iekārtu apmācības opcijas, iestatot vērtības algoritma *parametru prognozēšanai*. Šīs vērtības tiek sūtītas no piegādes ķēžu pārvaldības uz Azure mašīnas apmācību. Izmantojiet lapu **Prognozēšanas algoritma parametri**, lai kontrolētu, kādi vērtību tipi ir jānorāda un kādas vērtības katrai no tām vajadzētu būt.

Lai iestatītu noklusējuma parametrus un vērtības, kas tiek izmantotas pieprasījuma prognozēšanas modeļiem, dodieties uz vispārējās **plānošanas iestatījuma \> Pieprasījuma prognozēšanas \> algoritma parametriem \>**. Ir nodrošināta parametru standarta kopa. Katram parametram ir šādi lauki:

- **Nosaukums** — azure izmantotā parametra nosaukums. Parasti šo nosaukumu nevajadzētu mainīt, ja vien neesat pielāgojis uzņēmuma Azure Machine Learning kalendāru.
- **Apraksts** — parametra kopējais nosaukums. Šis nosaukums tiek izmantots, lai identificētu parametru citās vietās sistēmā (piemēram, pieprasījuma prognozēšanas **parametru** lapā).
- **Vērtība** – parametra noklusētā vērtība; Ievadītā vērtība ir atkarīga no rediģējamā parametra. 
- **Skaidrojums** – īss parametra apraksts un tas, kā to lietot. Šis apraksts parasti ietver izziņu par derīgām vērtībām **laukā** Vērtība.

Šie parametri ir sniegti pēc noklusējuma. (Ja būs jāatgriezīs pie šī standarta saraksta, atlasiet **Atjaunot** darbību rūtī.)

- **Ticamības līmeņa procenti** — Ticamības intervāls sastāv no vērtību diapazona, kuras darbojas kā labi pieprasījuma prognozes aptuvenie rezultāti. Ticamības līmenis 95% norāda, ka pastāv 5% risks, ka nākamais pieprasījums nebūs ticamības intervāla diapazonā.
- **Uzspēciet** sezonālo būtību – norāda, vai piespiedīsiet modeli izmantot noteiktu sezonas tipu. Šis parametrs attiecas tikai uz ARIMA un ETS. Opcijas: *AUTO (noklusējuma)*, NAV *,* PIE *NUMERĀCIJA*, REIZINĀŠANAS *·*.
- **Budžeta modelis** – norāda, kuru budžeta modeli lietot. Opcijas: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALL*. Lai atlasītu labāko atbilstības modeli, lietojiet *ALL*.
- **Maksimālās prognozētās vērtības** — Konkretizē maksimālo vērtību, kuru izmantot prognozēs. Formāts: +1E[n] vai skaitliska konstante.
- **Minimālās prognozētās vērtības** — Konkretizē minimālo vērtību, kuru izmantot prognozēs. Formāts: -1E[n] vai skaitliska konstante.
- **Trūkst vērtības aizstājēja** — Konkretizē, kā tiek aizpildītas trūkstošās vietas vēsturiskajos datos. Opcijas: *(skaitliska vērtība)*, VIDĒJAIS *·*, *IEPRIEKŠĒJAIS*, *INTERPOLATE LINEĀRAIS*, *INTERPOLĀCIJAS POLIMIĀLI*.
- **Trūkstošais vērtības aizstājēja tvērums** — Konkretizē, vai vērtības aizstājējs attiecas tikai uz katras atsevišķās granularitātes atribūta datu diapazonu vai uz visu datu kopu. Datumu diapazona, kuru sistēma izmanto, aizpildot trūkstošās vietas vēsturiskajos datos, izveidošanai ir pieejamas tālāk norādītās opcijas:

    - *GLOBĀLA* – sistēma izmanto visu granularitātes atribūtu datumu pilnu diapazonu.
    - *HISTORY_DATE_RANGE* — sistēma **·** **·** **izmanto noteiktu datumu diapazonu, kas ir definēts, izmantojot laukus No datuma un Līdz datumam sadaļā Vēsturiskais periods** **, kas atrodas dialoglodziņā Statistiskās bāzlīnijas prognozes** ģenerēšana.
    - *GRANULARITY_ATTRIBUTE* — sistēma izmanto pašlaik apstrādātā granularitātes atribūta datumu diapazonu.

    > [!NOTE]
    > Granularitātes atribūts ir prognozes izmēru kombinācija, attiecībā pret kuru tiek veikta prognoze. Prognozes izmērus varat definēt lapā **Pieprasījuma prognozes parametri**.

- **Sezonalitātes norāde** — Nodrošina sezonalitātes datu norādi prognozēšanas modelim, lai uzlabotu prognozes precizitāti. Formāts: vesels skaitlis, kas norāda intervālu skaitu, kuriem pieprasījuma modelis atkārto pati sevi. Piemēram, ievadiet *6 datiem*, kas atkārtojas pati ik pēc sešiem mēnešiem.
- **Testa kopas izmēra procentuālais daudzums** — Vēsturisko datu īpatsvars, kurus jāizmanto kā prognozes precizitātes aprēķina testa kopa.

Šo parametru vērtības var ignorēt, dodoties uz vispārējās plānošanas **iestatījuma \> Pieprasījuma \> prognozēšanas pieprasījuma prognozēšanas \> parametriem**. Lapā Pieprasījuma **prognozēšanas** parametri varat ignorēt parametrus šādos veidos:

- Izmantojiet cilni **Vispārīgi,** lai globāli ignorētu parametrus.
- Izmantojiet cilni **Krājumu sadalījuma principi,** lai ignorētu parametrus specifiskiem krājumu sadalījuma principus. Parametri, kas tiek ignorēti noteiktam krājumu sadalījuma principam, ietekmē tikai to krājumu prognozi, kas ir saistīti ar šo krājumu sadalījuma principu.

> [!NOTE]
> Budžeta algoritma **parametru lapā** jūs varat izmantot pogas Darbību rūtī, lai pievienotu parametrus sarakstam, vai izņemt parametrus no saraksta. Taču parasti šo pieeju nevajadzētu izmantot, ja vien neesat pielāgojis eksperimentu Azure mašīnas izglītībā.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a> Iestatīt Azure mašīnas apmācības pakalpojumu

Piegādes ķēdes pārvaldība aprēķina pieprasījuma apjoma prognozes, izmantojot Azure datora apmācību pakalpojumu, kas ir jāiestata un jāpalaiž savam Azure abonementam. Šajā sadaļā ir aprakstīts, kā iestatīt Azure datora apmācību pakalpojumu Azure un pēc tam savienot to ar piegādes ķēžu pārvaldības vidi.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Iespējot Azure datora apmācības pakalpojumu līdzekļu pārvaldībā

Lai pieprasījuma prognozēšanai varētu lietot Azure datora apmācību pakalpojumu, ir jāaktivizē funkcionalitāte piegādes ķēžu pārvaldībā, lai iespējotu integrāciju. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Vispārējā plānošana*
- **Līdzekļa nosaukums:** *Azure mašīnas apmācības pakalpojums pieprasījuma prognozēšanai*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a> Datora apmācību iestatīšana Azure

Lai iespējotu Azure lietošanas iekārtu apmācību, lai apstrādātu prognozes, šim nolūkam ir jāiestata Azure iekārtu apmācības darbvieta. Ir divas opcijas:

- Lai iestatītu darbvietu, palaižot Microsoft nodrošinātu skriptu, [izpildiet 1. opcijas norādes:](#ml-workspace-script) Palaist skriptu, lai automātiski iestatītu datora apmācību darbvietu sadaļu, [un tad pārejiet uz sadaļu Iestatīt Azure datora apmācību pakalpojuma savienojuma parametrus Piegādes ķēžu](#demand-forecast-parameters) pārvaldība.
- Lai manuāli iestatītu darbvietu, [rīkojieties saskaņā ar 2. opcijas instrukcijām:](#ml-workspace-manual) manuāli iestatiet datora apmācības darbalauku un [tad izlaidiet uz priekšu iestatīt Azure datora](#demand-forecast-parameters) apmācību pakalpojuma savienojuma parametrus Piegādes ķēdes pārvaldības sadaļā. Šī opcija prasa vairāk laika, bet tā dod jums lielāku kontroli.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a> 1. opcija: skripta palaišana, lai automātiski iestatītu datora apmācības darbvietu

Šajā sadaļā ir aprakstīts, kā iestatīt jūsu datora apmācības darbvietu, izmantojot sistēmas Microsoft sniegto automatizētu skriptu. Ja vēlaties, visus [resursus var iestatīt manuāli, sekojot instrukcijām 2. opcijā: manuāli iestatīt datora apmācības darbvietu](#ml-workspace-manual) sadaļu. Nav jāpabeidz abas opcijas.

1. Cilnē GitHub atveriet pieprasījuma [Dynamics 365 Supply Chain Management prognozēšanas veidnes ar Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repository (repo) un lejupielādējiet šādus failus:

    - quick_setup.ps1
    - sampleInput.csv
    - Riks/parameters.py
    - rik/api_trigger.to
    - Riks/run.py
    - src/REntryScript/forecast.r

1. Atveriet PowerShell logu un palaidiet quick_setup.ps1 **skriptu**, kuru lejupielādējāt iepriekšējā darbībā. Izpildiet ekrānā redzamos norādījumus. Skripts iestatīs nepieciešamo darbalauku, glabāšanu, noklusējuma datu krātuvi un skaitļošanas resursus. Tomēr jums vēl ir jāizveido nepieciešamie konveijeri, sekojot šīs procedūras atlikušajiem soļiem. (Konveijers ir veids, kā no Piegādes ķēžu pārvaldības sākt prognozētos skriptus.)
1. Azure mašīnas mācību studijā augšupielādējiet sampleInput.csv **failu, ko lejupielādējāt 1**. solī, konteinerā, kura nosaukums ir azureml *.* (Skripts quick_setup.ps1 izveidoja šo konteineru.) Šis fails ir nepieciešams, lai publicētu konveijeru un ģenerētu testa prognozi. Norādījumus skatiet sadaļā " [Bloķēt BLOB" augšupielādi](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. Azure datora mācību studijā atlasiet **Toms, kas** atrodas Tomā.
1. Failu struktūrā atrodiet šādu atrašanās **vietu** : **Lietotāji/\[pašreizējais lietotājs\]/src**.
1. Augšupielādējiet atlikušos četrus failus, kas tika lejupielādēti 1. solī, atrašanās vietā, kuru tika atrasts iepriekšējā solī.
1. Atlasiet tikko **api_trigger.no** augšupielādēto failu un palaidiet to. Tas izveidos konveijeru, ko var izraisīt, izmantojot API.
1. Jūsu darbvieta tagad ir iestatīta. Pārejiet uz sadaļu [Iestatīt Azure mašīnas apmācības pakalpojuma savienojuma parametrus Piegādes ķēžu pārvaldība](#demand-forecast-parameters).

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a> 2. opcija: manuāla datora apmācības darbalauku iestatīšana

Šajā sadaļā aprakstīts, kā manuāli iestatīt jūsu datora apmācības darbvietu. Procedūras šajā sadaļā ir jāveic tikai tad, ja nolēmāt ne palaist automatizētā iestatīšanas skriptu, kā aprakstīts 1. opcijā: palaist skriptu, [lai iestatītu datora apmācības darbvietas](#ml-workspace-script) sadaļu.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a> 1. darbība: jauna darbvietas izveide

Izmantojiet šo procedūru, lai izveidotu jaunu iekārtu apmācības darbvietu.

1. Pieteikties Savā Azure portālā.
1. Atvērt mašīnas **apmācības** pakalpojumu.
1. Rīkjoslā **atlasiet** Izveidot, lai atvērtu ceļvedi **Izveidot**.
1. Pabeidziet ceļvedi, izpildot ekrānā redzamos norādījumus. Kamēr strādājat, atcerieties šādus punktus:

    - Izmantojiet noklusējuma iestatījumus, ja vien citi punkti šajā sarakstā neiesakām atšķirīgus iestatījumus.
    - Noteikti atlasiet ģeogrāfisko reģionu, kas atbilst reģionam, kurā ir izvietota jūsu Piegādes ķēžu pārvaldības instance. Pretējā gadījumā daži dati var iziet caur reģiona robežām. Papildinformāciju skatiet tālāk šī [raksta](#privacy) paziņojumā par konfidencialitāti.
    - Izmantojiet atvēlētos resursus, piemēram, resursu grupas, glabāšanas kontus, konteineru reģistrācijas, Azure atslēgu debes krājumus un resursus.
    - **Ceļveža lapā Iestatīt azure mašīnas apmācības pakalpojuma** savienojuma parametrus ir jānorāda glabāšanas konta nosaukums. Lietojiet kontu, kas ir atvēlēts pieprasījuma prognozēšanai. Pieprasījuma prognozēšanas ievades un izvades dati tiks saglabāti šajā glabāšanas kontā.

Papildinformāciju skatiet sadaļā [Darbalauku izveidošana](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a> 2. darbība: glabāšanas konfigurēšana

Lai iestatītu glabāšanu, izmantojiet tālāk norādītās darbības.

1. GitHub atveriet [pieprasījuma prognozēšanas Dynamics 365 Supply Chain Management veidnes, izmantojot Azure machine learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repo, un lejupielādējiet **sampleInput.csv** failu.
1. Atveriet glabāšanas kontu, ko izveidojāt [1. darbībā: izveidojiet jaunu darbvietas](#create-workspace) sadaļu.
1. Izpildiet sadaļā Izveidot [konteineru sniegtos norādījumus](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container), lai izveidotu konteineru, kura nosaukums ir *azureml*.
1. Augšupielādējiet **sampleInput.csv failu**, ko lejupielādējāt 1. darbībā, konteinerā, ko tikko izveidojāt. Šis fails ir nepieciešams, lai publicētu konveijeru un ģenerētu testa prognozi. Norādījumus skatiet sadaļā " [Bloķēt BLOB" augšupielādi](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>3. darbība: noklusējuma datu krātuves konfigurēšana

Izmantojiet tālāk norādītās darbības, lai iestatītu noklusējuma datu krātuvi.

1. Azure datora mācību studijā atlasiet **Datastores** sadaļā Azure Machine Learning Studio.
1. Izveidojiet jaunu *Azure BLOB* *glabāšanas veida datu krātuvi, kas norāda uz azureml* BLOB [glabāšanas konteineru, kuru izveidojāt 2. darbībā:](#config-storage) glabāšanas sadaļas konfigurēšana. (Ja jaunā datu krātuves autentifikācijas tips ir *Konta atslēga*, kas ir izveidota glabāšanas konta atslēga. Norādījumus skatiet noliktavas konta [piekļuves atslēgu pārvaldīšana](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).)
1. Padariet jauno datu krātuvi par noklusējuma datu krātuvi, atverot tās detalizētu informāciju un atlasot **Iestatīt kā noklusēto datu krātuvi**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a> 4. darbība: resursu konfigurēšana

Izmantojiet tālāk norādītās darbības, lai iestatītu skaitļošanas resursu Azure Machine Learning Studio, lai palaistu prognozēšanas ģenerēšanas skriptus.

1. Atvērt detalizētas informācijas lapu par mašīnu apmācības darbalauku, ko izveidojāt [1. darbībā: izveidojiet jaunu darbalauku](#create-workspace) sadaļu. Atrast Studio **tīmekļa URL vērtību** un atlasīt saiti, lai to atvērtu.
1. Navigācijas **rūtī** atlasiet Aprēķināt.
1. Cilnē Aprēķināt **instances atlasiet** Jauns, **lai atvērtu** vedni, kas palīdzēs izveidot jaunu aprēķināto instanci. Izpildiet ekrānā redzamos norādījumus. Skaitļošanas instance tiks lietota, lai izveidotu pieprasījuma prognozēšanas konveijeru (To var dzēst pēc konveijera publicēšanas.) Izmantojiet noklusētos iestatījumus.
1. Cilnē Aprēķināt **klasterus** atlasiet Jauns **, lai atvērtu** vedni, kas palīdzēs izveidot jaunu skaitļošanas klasteri. Izpildiet ekrānā redzamos norādījumus. Skaitļošanas klasteris tiks izmantots, lai ģenerētu pieprasījuma apjoma prognozes. Tā iestatījumi ietekmē veiktspēju un izpildes maksimālo paralēlo līmeni. Iestatiet sekojošos laukus, bet izmantojiet noklusētos iestatījumus visiem citiem laukiem:

    - **Nosaukums** – ievadiet *e2ecpucluster*.
    - **Virtuālās mašīnas** lielums – pielāgojiet šo iestatījumu atbilstoši datu apjomam, ko plānojat izmantot kā ievadi pieprasījuma prognozēšanai. Zaru skaits nedrīkst pārsniegt 11, jo ir nepieciešams viens zars, lai izraisītu pieprasījuma apjoma prognozes ģenerēšanu, un maksimālais zaru skaits, ko pēc tam var izmantot prognozes ģenerēšanai, ir 10. (Zaru skaits tiks iestatīts arī parameters.py failā [5. solis. Konveijera sadaļas](#create-pipelines) izveide.) Katrā mezglā būs vairāki darbinieka procesi, kas paralēli izpildīs prognozēšanas skriptus. Kopējais darbinieku procesu skaits jūsu darbā būs zaru *skaits*, kam zaram ir × *zaru skaits*. Piemēram, *\_ ja datora klasterim ir standarta D4* (astoņi kodoli) un maksimums ir 11 zari, `nodes_count`*un ja vērtība failā parameters.py iestatīta uz 10*, paralēlo darbu efektīvais līmenis ir 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a> 5. solis. Konveijera izveide

Konveijers ir veids, kā sākt prognozēšanas skriptus no Piegādes ķēžu pārvaldības. Izmantojiet šo procedūru, lai izveidotu nepieciešamos konveijerus.

1. Cilnē GitHub atveriet veidnes [pieprasījuma prognozēšanai Dynamics 365 Supply Chain Management ar Azure machine learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repo un lejupielādējiet šādus failus:

    - Riks/parameters.py
    - rik/api_trigger.to
    - Riks/run.py
    - src/REntryScript/forecast.r

1. Azure datora mācību studijā atlasiet **Toms, kas** atrodas Tomā.
1. Failu struktūrā atrodiet šādu atrašanās **vietu** : **Lietotāji/\[pašreizējais lietotājs\]/src**.
1. Augšupielādējiet četrus 1. solī lejupielādētos failus atrašanās vietā, kuru tika atrasts iepriekšējā solī.
1. Pakalpojumā Azure atveriet un pārskatiet **parameters.py** failu, ko tikko augšupielādējat. Pārliecinieties, vai vērtība `nodes_count` ir mazāka [nekā vērtība, ko esat konfigurējis skaitļošanas klasterim 4. darbībā: konfigurējiet skaitļošanas resursus](#config-compute-resources) sadaļā. Ja vērtība `nodes_count` ir lielāka vai vienāda ar zaru skaitu skaitļošanas klasterī, konveijera darbību var sākt. Tomēr tas pārstās reaģēt, kamēr gaidīs nepieciešamos resursus. Papildinformāciju par zaru skaitu skatiet [4. darbībā: resursu skaitļošanas konfigurācijas](#config-compute-resources) sadaļa.
1. Atlasiet tikko **api_trigger.no** augšupielādēto failu un palaidiet to. Tas izveidos konveijeru, ko var izraisīt, izmantojot API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a> Iestatīt jaunu Active Directory programmu

Active Directory programma ir nepieciešama, lai autentificētu resursus, kas ir paredzēti pieprasījuma prognozēšanai, izmantojot pakalpojuma sniedzēju. Tāpēc pieteikumam ir jābūt ar zemāko privilēģijas līmeni, kas nepieciešams prognozes ģenerēšanas laikā.

1. Pieteikties Savā Azure portālā.
1. Reģistrēt jaunu pieteikumu nomnieka Azure Active Directory (Azure AD). Norādījumus skatiet sadaļā Portāla [lietošana, lai izveidotu programmu un pakalpojumu Azure AD sniedzēju, kas var piekļūt resursiem](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Izpildiet ekrānā redzamos norādījumus, pabeidzot ceļvedi. Izmantojiet noklusētos iestatījumus.
1. Piešķiriet jaunajai Active Directory programmai piekļuvi tālāk norādītajiem resursiem, ko izveidojāt [sadaļā Mašīnas apmācības iestatīšana Azure](#ml-workspace). Norādījumus skatiet sadaļā Azure [lomu piešķiršana, izmantojot Azure portālu](/azure/role-based-access-control/role-assignments-portal?tabs=current). Šis solis iespējos sistēmu importēt un eksportēt prognozēšanas datus un izraisīt iekārtu apmācības konveijeru no Piegādes ķēžu pārvaldības.

    - Datora apmācības darbvietas veicināšanas loma
    - Izdalītā loma atvēlētajā glabāšanas kontā
    - Glabāšanas BLOB datu veicinātājs loma atvēlētajā glabāšanas kontā

1. **Izveidotā pieteikuma sadaļā Sertifikāti &** noslēpumi izveidojiet pieteikumam noslēpumu. Norādījumus skatiet sadaļā Klienta [noslēpuma pievienošana](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Atzīmējiet programmas ID un tā noslēpumu. Detalizēta informācija par šo programmu būs nepieciešama vēlāk, kad iestatīsiet **pieprasījuma prognozēšanas parametru** lapu Piegādes ķēžu pārvaldībā.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a> Iestatīt Azure datora apmācības pakalpojuma savienojuma parametrus piegādes ķēdes pārvaldībā

Izmantojiet tālāk norādītās darbības, lai savienotu jūsu Piegādes ķēžu pārvaldības vidi ar iekārtu apmācību pakalpojumiem, ko tikko iestatījāt Azure.

1. Pierakstieties Supply Chain Management.
1. Dodieties uz **vispārējās plānošanas iestatījumu \> pieprasījuma \> prognozēšanas pieprasījuma \> prognozēšanas parametriem**.
1. Cilnē Vispārīgie **iestatījumi** pārliecinieties, vai lauks **Prognozes ģenerēšanas stratēģija** ir iestatīts uz *Azure Machine Learning Service*.
1. Cilnē Krājumu **sadalījuma atslēgas** pārliecinieties, vai lauks Prognozes ģenerēšanas stratēģija ir iestatīts uz Azure Machine Learning Service **katrai sadalījuma atslēgai,** *kam* pieprasījuma prognozēšanai jāizmanto Azure datora apmācības pakalpojums.
1. **Cilnē Azure Mašīnas apmācības pakalpojums** iestatiet šādus laukus:

    - **Nomnieka ID** — ievadiet ID azure nomniekam. Piegādes ķēdes pārvaldība izmantos šo ID, lai autentificētu tās Azure mašīnas apmācības pakalpojumā. Nomnieka ID varat atrast **Azure** portāla pārskata Azure AD lapā.
    - **Galvenā pakalpojuma programmas ID** - ievadiet programmas ID lietojumprogrammai, kuru izveidojāt [active Directory lietojumprogrammas](#aad-app) sadaļā. Šī vērtība tiek izmantota, lai autorizētu API pieprasījumus Azure datora apmācības pakalpojumam.
    - **Pakalpojuma galvenā noslēpums** – ievadiet galvenā pieteikuma noslēpumu programmai, ko izveidojāt [Active Directory lietojumprogrammas](#aad-app) sadaļā. Šī vērtība tiek izmantota, lai iegādātos piekļuves marķieri drošības atslēgai, ko izveidojāt, lai veiktu autorizētas operācijas attiecībā uz Azure krātuvi un Azure datora valodas darbvietu.
    - **Glabāšanas konta nosaukums** — ievadiet Azure glabāšanas konta nosaukumu, ko norādījāt, palaižot iestatīšanas vedni savā Azure darbvietā. (Plašāku informāciju skatiet [Datora apmācību iestatīšana Azure](#ml-workspace) sadaļā.)
    - **Konveijera galapunkta** adrese — ievadiet vietrāžu URL konveijera vietrādī REST galapunktam jūsu Azure mašīnas apmācības pakalpojumam. Jūs izveidojāt šo konveijeru kā pēdējo soli, kad [iestatāt mašīnas apmācību Azure](#ml-workspace). Lai saņemtu konveijera vietrādi URL, piesakieties Azure portālā, navigācijas laikā **atlasiet** konveijerus. Cilnē Konveijers **atlasiet** konveijera galapunktu, kura nosaukums ir **TriggerDemandForecastGeneration**. Pēc tam kopējiet parādīto REST galapunktu.

    ![Parametri lapas Pieprasījuma prognozēšanas parametri cilnē Azure Machine Learning Service.](media/azure-ml-service-parameters.png "Lapas Pieprasījuma prognozēšanas parametri cilnē Azure Machine Learning Service")

## <a name="privacy-notice"></a><a name="privacy"></a>Paziņojums par konfidencialitāti

*Kad izvēlaties Azure Machine Learning Service* kā prognožu ģenerēšanas stratēģiju, Piegādes ķēžu pārvaldība automātiski sūta debitora datus pēc vēsturiskā pieprasījuma, piemēram, uzkrātajiem daudzumiem, preču nosaukumiem un to produktu dimensijām, nosūtīšanas un saņemšanas vietām, debitoru identifikatoriem, kā arī prognozējiet parametrus ģeogrāfiskā reģionā, kur atrodas jūsu datora apmācības darbvieta un ar to saistītais glabāšanas konts. nākotnes pieprasījumu prognozēšanas nolūkā. Azure mašīnas apmācības pakalpojums var būt citā ģeogrāfiskā reģionā, nevis ģeogrāfiskā reģionā, kur ir izvietota piegādes ķēžu pārvaldība. Daži lietotāji var kontrolēt, vai šī funkcionalitāte ir iespējota, atlasot prognozes ģenerēšanas stratēģiju lapā **Pieprasījuma prognozēšanas parametri**.

## <a name="additional-resources"></a>Papildu resursi

- [Pieprasījuma prognozes apskats](introduction-demand-forecasting.md)
- [Statistiskās bāzlīnijas prognozes ģenerēšana](generate-statistical-baseline-forecast.md)
- [Manuāla bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)
- [Webi plkst.: pieprasījuma apjoma prognozēšana ar Azure mašīnas apmācību sērijām](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
