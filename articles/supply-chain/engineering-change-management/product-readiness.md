---
title: Preces gatavība
description: Šajā tēmā izskaidrots, kā var izmantot gatavības pārbaudes, lai nodrošinātu, ka preces pamatdati ir pabeigti, pirms tā tiek izmantota darbībās.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 12707774c780a0f805deed532af27c3705ea1f55
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500602"
---
# <a name="product-readiness"></a>Preces gatavība

[!include [banner](../includes/banner.md)]

Varat izmantot gatavības pārbaudes, lai nodrošinātu, ka visi nepieciešamie preces pamatdati ir norādīti, pirms tā tiek izmantota darbībās. Kad tiek izmantotas gatavības pārbaudes, lietotājs vai grupa ir atbildīgs par noteiktu iepriekš definētu ar precēm saistītu datu apstiprināšanu.

Varat atzīmēt izvēles rūtiņu **Aktīva**, kas paredzēta tehniskajai precei, variantam vai versijai, tikai pēc tam, kad visi vajadzīgie dati ir ievadīti un pārbaudīti, un pēc tam, kad visas gatavības pārbaudes ir apstrādātas. Ja vismaz viena produkta, versijas vai varianta pārbaude nav apstrādāta, tad, mēģinot atzīmēt lodziņu **Aktīva**, saņemsit vedni, kas brīdina, ka ne visas pārbaudes ir izpildītas.

Varat izveidot gatavības pārbaudes jaunajām inženiertehniskām precēm, jauniem variantiem un jaunām tehniskām versijām. Jūs varat iespējot preču gatavības pārbaudes standarta (ne inženiertehniskajām) precēm, (skatiet arī sadaļu [Preču gatavības pārbaudes](#standard-products)). 

Standarta preces transakcijās varat lietot, pat, ja visas gatavības pārbaudes nav izpildītas. Ja jābloķē preces lietošana transakcijās, izmantojiet dzīvescikla stāvokli. Varat piešķirt dzīvescikla stāvokli, kas bloķē preces izmantošanu transakcijās un pēc tam, kad ir izpildītas visas gatavības pārbaudes, piešķirt jaunu dzīvescikla stāvokli, kas ļauj veikt vajadzīgās transakcijas.

## <a name="types-of-readiness-checks"></a>Gatavības pārbaužu veidi

Ir pieejami trīs gatavības pārbaužu veidi:

- **Sistēmas pārbaude** – sistēma pārbauda, vai ir derīgs ieraksts. Piemēram, ieraksts varētu būt aktīvs materiālu komplekts (MK).
- **Manuāla pārbaude** - lietotājs pārbauda, vai ieraksts ir derīgs. Piemēram, gatavības pārbaudei var būt nepieciešama noklusējuma pasūtījumu iestatījumu validācija. Dažos gadījumos, piemēram, kad prece joprojām tiek izstrādāta un tāpēc netiks iekļauta krājumos, nav nepieciešami nekādi noklusējuma pasūtījuma iestatījumi. Tomēr noklusējuma pasūtījuma iestatījumi var būt nepieciešami citai tāda paša veida precei, jo preci var glabāt krājumos. Lietotājs ir atbildīgs par to, kā pareizi pieņemt lēmumu, vai ir nepieciešama gatavības pārbaude.
- **Kontrolsaraksts** - lietotājs atbild uz jautājumu sēriju no kontrolsaraksta, un sistēma nosaka, vai atbildes atbilst cerībām. Kontrolsarakstam var būt jebkāda tēma. Piemēram, to var izmantot, lai noteiktu, vai mārketinga materiāli vai preču dokumentācija ir pabeigta.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Kā izveidot gatavības pārbaudes jaunai inženiertehniskai precei, variantam vai versijai

Gatavības pārbaudes ierobežojumus var piemērot izlaistajā preces līmenī, izlaisto variantu līmenī un inženiertehniskās versijas līmenī.

Veidojot jaunu *inženiertehnisko preci*, sistēma nosaka, vai uz to [attiecas gatavības pārbaudes politika](#assign-policy). Ja tiek lietota gatavības pārbaudes politika, rodas šādi gadījumi:

- Gatavības pārbaudes tiek veidotas precei saskaņā ar piemērojamo politiku.
- Tehniskā versija ir iestatīta uz neaktīvu, lai bloķētu preces izmantošanu. Visas preču inženiertehniskās versijas ir iestatītas uz neaktīvām.

Ja precei tiek izveidots jauns *variants*, sistēma pārbauda, vai uz to attiecas gatavības pārbaudes politika. (Gatavības pārbaudes var piemērot izlaistajā preces līmenī un inženiertehniskās versijas līmenī.) Ja uz to attiecas politika, tiek veiktas šādas darbības:

- Gatavības pārbaudes tiek veidotas precei saskaņā ar piemērojamo politiku.
- Inženiertehniskā versija un variants ir iestatīts uz neaktīvu, lai bloķētu preces izmantošanu.

Ja precei tiek izveidots jauna inženiertehniskā *versija*, sistēma pārbauda, vai uz to attiecas gatavības pārbaudes politika. (Gatavības pārbaudes var piemērot inženiertehniskās versijas līmenī.) Ja uz to attiecas politika, tiek veiktas šādas darbības:

- Gatavības pārbaudes tiek veidotas precei saskaņā ar piemērojamo politiku.
- Tehniskā versija ir iestatīta uz neaktīvu, lai bloķētu preces izmantošanu.

> [!NOTE]
> Gatavības pārbaudes politikas varat iestatīt arī standarta (ne inženiertehniskām) precēm. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Standarta preču gatavības pārbaudes](#standard-products).

## <a name="view-readiness-checks"></a>Skatīt gatavības pārbaudes

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Skatīt atvērtās preces vai preces versijas gatavības pārbaudes

Lai atrastu preces atvērtās gatavības pārbaudes, atveriet lapu **Izlaistās preces detaļas**. Pēc tam darbību rūts grupas **Gatavības pārbaudes** cilnē **Prece** atlasiet **Gatavības pārbaudes**.

Lai atrastu preces versijas atvērtās gatavības pārbaudes, atveriet lapu **Tehniskās versijas** izlaistajai precei un izvēlieties versiju. Pēc tam darbību rūts grupas **Kontrolsaraksts** cilnē **Prece** atlasiet **Gatavības pārbaudes**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Skatīt atvērtās gatavības pārbaudes, kas jums piešķirtas

Lai skatītu jums piešķirtās atvērtās gatavības pārbaudes, veiciet vienu no šīm darbībām.

- Doties uz **Tehnisko izmaiņu pārvaldība \> Kopīgie \> Preces gatavība \> Manas atvērtās gatavības pārbaudes**.
- Doties uz **Preces informācijas pārvaldība \> Darbvietas \> Preces gatavība diskrētai ražošanai**.

Iestatījumi, kas norāda, kam ir piešķirta gatavības pārbaude, tiek veikta gatavības politikai. Gatavības pārbaudes var piešķirt personai vai komandai. Ja gatavības pārbaude ir piešķirta komandai, komandā ir viena persona, kurai ir jāapstrādā gatavības pārbaude.

## <a name="process-open-readiness-checks"></a>Apstrādāt atvērtās gatavības pārbaudes

### <a name="process-system-and-manual-readiness-checks"></a>Procesu sistēma un manuālās gatavības pārbaudes

Pēc tam, kad atverat lapu **Gatavības pārbaudes**, varat skatīt sistēmas un manuālās gatavības pārbaudes tematu, darbības rūtī atlasot **Skatīt saistīto informāciju**. Pēc tam varat pabeigt un/vai validēt datus gatavības pārbaudei. Atvērtajām gatavības pārbaudēm ir **Statusa** vērtība *Gaida*. Šis statuss norāda, ka gatavības pārbaude joprojām ir jāapstrādā. Lai apstrādātu gatavības pārbaudi, izpildiet tālāk aprakstītās darbības.

- Darbības rūtī atlasiet **Pārbaudīt/pabeigt**, lai pārskatītu un pabeigtu gatavības pārbaudi. Kad esat pabeidzis, **Statusa** lauks tiek atjaunināts uz *Nokārtots*.
- Darbības rūtī atlasiet **Izlaist**, ja vēlaties izlaist gatavības pārbaudi, kas nav obligāta. Piemēram, jūs iestatāt gatavības pārbaudi cenu aprēķiniem. Tomēr jūs izlemjat izlaist šo pārbaudi, kamēr prece joprojām ir izstrādes fāzē. Šādā gadījumā **Statusa** lauks tiek atjaunināts uz *Izlaists*.

Atkarībā no gatavības politikas konfigurācijas, kad **Statusa** lauks gatavības pārbaudei tiek atjaunināts uz statusu *Nokārtots*, var būt nepieciešams papildu solis, lai apstiprinātu gatavības pārbaudi. Šādā gadījumā atlasiet opciju **Apstiprinājums**, lai pabeigtu gatavības pārbaudi. Ja gatavības pārbaude ir izlaista, šis apstiprinājuma solis vienmēr ir obligāts.

Kad visas atvērtās gatavības pārbaudes jaunai precei, variantam vai versijai ir apstrādātas un apstiprinātas pēc nepieciešams, krājums automātiski kļūst aktīvs un gatavs lietošanai.

### <a name="process-checklist-readiness-checks"></a>Apstrādāt kontrolsaraksta gatavības pārbaudes

Lai atvērtu kontrolsarakstu, atveriet lapu **Gatavības pārbaudes** un pēc tam darbību rūtī atlasiet **Sākt kontrolsarakstu**. Kad kontrolsaraksts pabeigts, sistēma pārbauda, vai ir gatavības pārbaude ir nokārtota, pamatojoties uz anketas iestatījumiem. Ja pārbaude ir nokārtota, **Statusa** lauks tiek atjaunināts uz *Nokārtots*. Ja gatavības pārbaude nav obligāta, varat to izlaist. Šādā gadījumā **Statusa** lauks tiek atjaunināts uz *Izlaists*.

Atkarībā no gatavības politikas konfigurācijas, kad **Statusa** lauks gatavības pārbaudei tiek atjaunināts uz statusu *Nokārtots*, var būt nepieciešams papildu solis, lai apstiprinātu gatavības pārbaudi. Šādā gadījumā atlasiet opciju **Apstiprinājums**, lai pabeigtu gatavības pārbaudi. Ja gatavības pārbaude ir izlaista, šis apstiprinājuma solis vienmēr ir obligāts.

Kad visas atvērtās gatavības pārbaudes jaunai precei, variantam vai versijai ir apstrādātas un apstiprinātas pēc nepieciešams, krājums automātiski kļūst aktīvs un gatavs lietošanai.

## <a name="create-and-manage-product-readiness-policies"></a>Izveidot un pārvaldīt preču gatavības politikas

Izmantojiet preču gatavības politikas, lai pārvaldītu gatavības pārbaudes, kas attiecas uz preci. Katra gatavības politika ietver gatavības pārbaužu kopu. Kad inženiertehniskajai preču kategorijai vai kopīgotajai precei ir piešķirta gatavības politika, visām precēm, kas ir saistītas ar šo kategoriju vai kopīgoto preci, būs gatavības pārbaudes, kas iekļautas gatavības politikā.

Lai strādātu ar preces gatavības politikām, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Preces gatavības politikas**. Pēc tam izpildiet kādu no norādītajām darbībām.

- Lai izveidotu jaunu politiku, darbības rūtī atlasiet **Jauns** un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai rediģētu esošu politiku, atlasiet to saraksta rūtī, atlasiet **Jauns** darbību rūtī un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai dzēstu esošu politiku, atlasiet to saraksta rūtī, darbību rūtī atlasiet **Rediģēt** un tad kopsavilkuma cilnē **Vispārīgi** pārliecinieties, ka opcija **Aktīvs** ir iestatīta uz *Nē*. Pēc tam darbību rūtī atlasiet **Dzēst**.

### <a name="header"></a>Galvene

Iestatiet tālāk norādītos laukus preces gatavības politikas virsrakstā.

| Lauks | Apraksts |
|---|---|
| Vārds, uzvārds | Ievadiet politikas nosaukumu. |
| Apraksts | Ievadiet politikas aprakstu. |

### <a name="general-fasttab"></a>Cilne Vispārīgi

Iestatiet tālāk norādītos laukus preces gatavības politikas kopsavilkuma cilnē **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Preces veids | Atlasiet, vai politika attiecas uz *Krājuma* vai *Pakalpojuma* veida precēm. Pēc ieraksta saglabāšanas šo iestatījumu nevar mainīt. |
| Aktīvie | Lietojiet šo opciju, lai palīdzētu uzturēt gatavības politikas. Iestatiet to uz *Jā* visām jūsu izmantotajām gatavības politikām. Iestatiet to uz *Nē*, lai, to neizmantojot, atzīmētu gatavības politiku kā neaktīvu. Ņemiet vērā, ka nav iespējams deaktivizēt gatavības politiku, kas piešķirta inženiertehnisko preču kategorijai vai kopīgotajai precei, un var dzēst tikai neaktīvu laidienu politikas. |

### <a name="readiness-control-fasttab"></a>Gatavības kontroles kopsavilkuma cilne

Katram gatavības pārbaudes veidam, ko vēlaties iekļaut politikā, pievienojiet rindu **Gatavības kontroles** kopsavilkuma cilnē. Izmantojiet tālāk norādītās pogas kopsavilkuma cilnes rīkjoslā, lai pievienotu un noņemtu rindas pēc nepieciešamības:

- **Pievienot pārbaudi** - pievienojiet politikai standarta gatavības pārbaudi. Atlasot šo pogu, parādās dialoglodziņš **Pievienot pārbaudi**. Tur varat atlasīt no pieejamo pārbaužu saraksta.
- **Pievienot esošu anketu** - pievienojiet režģim tukšu rindu. Pēc tam varat piešķirt esošu anketu, iestatot laukus nākamajā tabulā.
- **Kopēt** – pievienojiet režģim atlasītās rindas kopiju.
- **Dzēst** - dzēsiet atlasīto rindu no režģa.

Katrai rindai, kuru pievienojat, iestatiet tālāk norādītos laukus.

| Lauks | Apraksts |
| --- | --- |
| Apstrādāt apgabalu | Atlasiet apgabalu, ar kuru ir saistīta pārbaude. |
| tips | Atlasiet, vai pārbaude ir sistēmas pārbaude, manuāla pārbaude vai kontrolsaraksts (anketa). |
| Vārds, uzvārds | Ja pārbaude ir kontrolsaraksts, ievadiet nosaukumu. Sistēmas un manuālo pārbaužu laikā šis lauks tiek iestatīts automātiski. |
| Apraksts | Ja pārbaude ir kontrolsaraksts, ievadiet aprakstu. Sistēmas un manuālo pārbaužu laikā šis lauks tiek iestatīts automātiski, un apraksts izskaidro pārbaudes fokusu. |
| Piemērot pārbaudes | Atlasiet, vai rindai ir jāģenerē gatavības pārbaudes, reaģējot uz jaunu izlaisto preci, izlaisto variantu vai izlaisto versiju. |
| Izpildīt vienumā | Atlasiet, vai gatavības pārbaudes, ko ģenerē rinda, attiecas uz visiem uzņēmumiem vai uz vienu uzņēmumu. |
| Uzņēmums | Ja **Izpildes** lauks tiek iestatīts uz *Viens uzņēmums*, atlasiet uzņēmumu. |
| Īpašnieka tips | Atlasiet, vai personai vai komandai ir jāpiešķir gatavības pārbaudes. |
| Īpašnieks | Atlasiet personu vai komandu, kam ir jāpiešķir gatavības pārbaude, ko ģenerē rinda. |
| Anketa | Atlasiet anketu, kas jāizmanto kontrolsarakstam. Kontrolsaraksts ir vietējais kontrolsaraksts uzņēmumā, kur pabeigta gatavības pārbaude. Sistēmai ir jāvar novērtēt, vai kontrolsaraksts ir pareizi atbildēts. Tāpēc kontrolsaraksts ir jāiestata tā, lai novērtējums tiktu veikts, pamatojoties uz pareizām atbildēm. Papildinformāciju par to, kā izveidot anketas, skatiet [Anketu lietošana](/dynamicsax-2012/appuser-itpro/using-questionnaires) un ar to saistītās tēmas. |
| Automātisks apstiprinājums | Gatavības pārbaudes ieraksti ietver izvēles rūtiņu **Apstiprināts**, kas norāda apstiprinājuma statusu. Atzīmējiet izvēles rūtiņu **Automātisks apstiprinājums** pārbaudēm, kas jāiestata uz apstiprināts uzreiz pēc tam, kad piešķirtais lietotājs tos pabeidz. Nodzēsiet šo izvēles rūtiņu, lai pieprasītu tiešu apstiprinājumu kā papildu darbību. |
| Obligāts | Atzīmējiet šo izvēles rūtiņu pārbaudēm, kas jāaizpilda piešķirtajam lietotājam. Obligātās pārbaudes nevar izlaist. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Gatavības politiku piešķiršana standarta un inženiertehniskajām precēm

Kad jūs izveidojat jaunu preci, kas pamatota uz inženiertehnisko kategoriju, jūs izveidojat gan *izlaisto preci*, gan saistīto *kopīgoto preci* . Veids, kādā izpildei nodotai precei tiek atrisinātas gatavības politikas, ir atkarīgs no tā, vai ir ieslēgta funkcija *Preču gatavības pārbaudes*. (Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Standarta preču gatavības pārbaudes](#standard-products).)

- Kad *Preču gatavības pārbaužu* funkcija jūsu sistēmā ir *izslēgta*, gatavības politika tiek iestatīta un rādīta tikai [inženiertehniskās kategorijas](engineering-versions-product-category.md) ierakstos. Lai uzzinātu, kura politika attiecas uz izlaistu preci, sistēma pārbauda **Preces gatavības politikas** lauku saistītajai inženiertehniskajai kategorijai. Var mainīt esošas preces gatavības politiku, rediģējot saistīto inženiertehnisko kategoriju (nevis kopīgoto preci).
- Ja *Preces gatavības pārbaudes* funkcija ir *ieslēgta*, tā pievieno **Preču gatavības politikas** lauku lapai **Prece** (kur ir iestatītas koplietotas preces) un lapai **Izlaistā prece** (kur vērtība ir tikai lasāma un tiek ņemta no saistītās koplietojamās preces). Sistēma atrod izlaistās preces gatavības politiku, pārbaudot saistīto koplietoto preci. Kad jūs izmantojat inženiertehnisko kategoriju jaunas inženiertehniskās preces izveidošanai, sistēma izveido gan kopīgu preci, gan izlaisto preci un kopē jebkuru **Preces gatavības politikas** iestatījumu inženiertehniskajai kategorijai jaunajā kopīgotajā precē. Tad varat mainīt esošas preces gatavības politiku, rediģējot saistīto kopīgoto preci (nevis izlaisto inženiertehnisko kategoriju).

Lai koplietojamai precei piešķirtu gatavības politiku, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Preču informācija \> Preces \> Preces**.
1. Atveriet vai izveidojiet preci, kurai vēlaties piešķirt gatavības politiku.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Preču gatavības politika** uz politikas nosaukumu, kas jālieto precei.

Lai inženiertehniskajai kategorijai piešķirtu gatavības politiku, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Inženiertehnisko izmaiņu pārvaldība \> Iestatījumi \> Inženiertehnisko produktu kategoriju detalizēta informācija**.
1. Atveriet vai izveidojiet inženiertehnisko kategoriju, kurai vēlaties piešķirt gatavības politiku.
1. Kopsavilkuma cilnē **Preču gatavības politika** iestatiet lauku **Preču gatavības politika** uz politikas nosaukumu, kas jālieto inženiertehniskajai kategorijai.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Standarta preču gatavības pārbaudes

Jūs varat iespējot preču gatavības pārbaudes standarta (ne inženiertehniskajām) precēm, ieslēdzot *Preču gatavības pārbaudes* funkciju Līdzekļu pārvaldībā. Šī funkcija veic dažas nelielas izmaiņas gatavības pārbaudes sistēmā, lai tā atbalsta standarta preces.

### <a name="enable-readiness-checks-on-standard-products"></a>Iespējot standarta preču gatavības pārbaudes

Lai iespējotu sistēmu veikt standarta preču gatavības pārbaudes, sekojiet šiem soļiem.

- Iespējojiet Inženiertehnisko izmaiņu pārvaldību jūsu sistēmā, kā aprakstīts [Inženiertehniskajā izmaiņu pārvaldības pārskatā](product-engineering-overview.md).
- Izmantojiet [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu līdzekli ar nosaukumu *Preču gatavības pārbaudes*.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Izveidot standarta preču gatavības politikas

Tiek izveidota gatavības politika standarta precēm tāpat kā inženiertehniskajām precēm. Informāciju skatiet iepriekš šajā tēmā.

### <a name="assign-readiness-policies-to-standard-products"></a>Piešķirt gatavības politikas standarta precēm

Lai piešķirtu standarta precei gatavības politiku, atveriet saistīto koplietoto preci un iestatiet lauku **Preču gatavības politika** uz tās politikas nosaukumu, kuru jālieto. Plašāku informāciju skatiet iepriekš šajā tēmā sadaļā [Gatavības politiku piešķiršana standarta un inženiertehniskajām precēm](#assign-policy).

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Skatīt un pārstrādāt standarta preču gatavības pārbaudes

Kad šī funkcija ir ieslēgta, jūs skatāt un apstrādājam gatavības pārbaudes standarta precēm tāpat, kā jūs to darām inženiertehniskajai precei. Informāciju skatiet iepriekš šajā tēmā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
