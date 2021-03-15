---
title: Preces gatavība
description: Šajās tēmās izskaidrots, kā var izmantot gatavības pārbaudes, lai nodrošinātu, ka preces pamatdati ir pabeigti, pirms tā tiek izmantota darbībās.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8321a0d8516a6c2c085ce9c1236f70af1cca98da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967262"
---
# <a name="product-readiness"></a>Preces gatavība

[!include [banner](../includes/banner.md)]

Varat izmantot gatavības pārbaudes, lai nodrošinātu, ka visi nepieciešamie preces pamatdati ir norādīti, pirms tā tiek izmantota darbībās. Kad tiek izmantotas gatavības pārbaudes, lietotājs vai grupa ir atbildīgs par noteiktu iepriekš definētu ar precēm saistītu datu apstiprināšanu. Ja precei ir atvērta gatavības pārbaude, preci nevar izlaist vai izmantot darījumos.

**Aktīva** izvēles rūtiņa, kas paredzēta tehniskajai precei, variantam vai versijai, ir pieejama tikai pēc tam, kad visi vajadzīgie dati ir ievadīti un pārbaudīti, un pēc tam, kad visas gatavības pārbaudes ir apstrādātas. Šajā punktā preci, versiju vai variantu var izlaist citiem uzņēmumiem un izmantot darījumos. Varat izveidot gatavības pārbaudes jaunajām precēm, jauniem variantiem un jaunām tehniskām versijām.

## <a name="types-of-readiness-checks"></a>Gatavības pārbaužu veidi

Ir pieejami trīs gatavības pārbaužu veidi:

- **Sistēmas pārbaude** – sistēma pārbauda, vai ir derīgs ieraksts. Piemēram, ieraksts varētu būt aktīvs materiālu komplekts (MK).
- **Manuāla pārbaude** - lietotājs pārbauda, vai ieraksts ir derīgs. Piemēram, gatavības pārbaudei var būt nepieciešama noklusējuma pasūtījumu iestatījumu validācija. Dažos gadījumos, piemēram, kad prece joprojām tiek izstrādāta un tāpēc netiks iekļauta krājumos, nav nepieciešami nekādi noklusējuma pasūtījuma iestatījumi. Tomēr noklusējuma pasūtījuma iestatījumi var būt nepieciešami citai tāda paša veida precei, jo preci var glabāt krājumos. Lietotājs ir atbildīgs par to, kā pareizi pieņemt lēmumu, vai ir nepieciešama gatavības pārbaude.
- **Kontrolsaraksts** - lietotājs atbild uz jautājumu sēriju no kontrolsaraksta, un sistēma nosaka, vai atbildes atbilst cerībām. Kontrolsarakstam var būt jebkāda tēma. Piemēram, to var izmantot, lai noteiktu, vai mārketinga materiāli vai preču dokumentācija ir pabeigta.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Kā izveidot gatavības pārbaudes jaunai precei, variantam vai versijai

Kad izveidojat jaunu tehnisko **preci**, sistēma nosaka, vai gatavības pārbaudes politika ir iestatīta tehnisko preču kategorijai. (Gatavības pārbaudes ierobežojumus var piemērot izlaistajā preces līmenī, izlaisto variantu līmenī un tehniskās versijas līmenī.) Ja ir iestatīta politika, tiek veiktas šādas darbības:

- Gatavības pārbaudes tiek veidotas precei saskaņā ar piemērojamo politiku.
- Tehniskā versija ir iestatīta uz neaktīvu, lai bloķētu preces izmantošanu. Visas specifiskās preces versijas ir iestatītas kā neaktīvas.

Ja precei ir izveidots jauns **variants**, sistēma pārbauda, vai ir iestatītas izstrādes preču kategorijas gatavības pārbaudes. (Gatavības pārbaudes var piemērot izlaistajā preces līmenī un tehniskās versijas līmenī.) Ja ir iestatīta gatavības pārbaude, tiek veiktas šādas darbības:

- Šai precei tiek izveidotas gatavības pārbaudes.
- Tehniskā versija ir iestatīta uz neaktīvu, lai bloķētu preces izmantošanu.

Ja precei ir izveidots jauna tehniskā **versija**, sistēma pārbauda, vai ir iestatītas izstrādes preču kategorijas gatavības pārbaudes. (Gatavības pārbaudes var piemērot tehniskās versijas līmenī.) Ja ir iestatīta gatavības pārbaude, tiek veiktas šādas darbības:

- Šai precei tiek izveidotas gatavības pārbaudes.
- Tehniskā versija ir iestatīta uz neaktīvu, lai bloķētu preces izmantošanu.

## <a name="view-readiness-checks"></a>Skatīt gatavības pārbaudes

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Skatīt atvērtās preces vai preces versijas gatavības pārbaudes

Lai atrastu preces atvērtās gatavības pārbaudes, atveriet lapu **Izlaistās preces detaļas**. Pēc tam darbību rūts grupas **Gatavības pārbaudes** cilnē **Prece** atlasiet **Gatavības pārbaudes**.

Lai atrastu preces versijas atvērtās gatavības pārbaudes, atveriet lapu **Tehniskās versijas** izlaistajai precei un izvēlieties versiju. Pēc tam darbību rūts grupas **Kontrolsaraksts** cilnē **Prece** atlasiet **Gatavības pārbaudes**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Skatīt atvērtās gatavības pārbaudes, kas jums piešķirtas

Lai skatītu jums piešķirtās atvērtās gatavības pārbaudes, veiciet vienu no šīm darbībām.

- Doties uz **Tehnisko izmaiņu pārvaldība \> Kopīgie \> Preces gatavība \> Manas atvērtās gatavības pārbaudes**.
- Doties uz **Preces informācijas pārvaldība \> Darbvietas \> Preces gatavība diskrētai ražošanai**.

Iestatījumi, kas norāda, kam ir piešķirta gatavības pārbaude, tiek veikta tehnisko preču kategorijai. Gatavības pārbaudes var piešķirt personai vai komandai. Ja gatavības pārbaude ir piešķirta komandai, komandā ir viena persona, kurai ir jāapstrādā gatavības pārbaude. Papildinformāciju skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

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

Izmantojiet preču gatavības politikas, lai pārvaldītu gatavības pārbaudes, kas attiecas uz preci. Tā kā gatavības politika ir piešķirta tehniskajai kategorijai, visas pārbaudes gatavības politikā attiecas uz visām tehniskām precēm, kas ir balstītas uz tehnisko kategoriju. Papildinformāciju skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

Katra gatavības politika ietver gatavības pārbaužu kopu. Kad izstrādes preču kategorijai ir piešķirta gatavības politika, visām precēm, kas tiek veidotas no šīs tehnisko preču kategorijas, būs gatavības pārbaudes, kas norādītas gatavības politikā.

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
| Aktīvie | Lietojiet šo opciju, lai palīdzētu uzturēt gatavības politikas. Iestatiet to uz *Jā* visām jūsu izmantotajām gatavības politikām. Iestatiet to uz *Nē*, lai, to neizmantojot, atzīmētu gatavības politiku kā neaktīvu. Ņemiet vērā, ka nav iespējams deaktivizēt gatavības politiku, kas piešķirta tehnisko preču kategorijai, un var dzēst tikai neaktīvu laidienu politikas. |

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
| Anketa | Atlasiet anketu, kas jāizmanto kontrolsarakstam. Kontrolsaraksts ir vietējais kontrolsaraksts uzņēmumā, kur pabeigta gatavības pārbaude. Sistēmai ir jāvar novērtēt, vai kontrolsaraksts ir pareizi atbildēts. Tāpēc kontrolsaraksts ir jāiestata tā, lai novērtējums tiktu veikts, pamatojoties uz pareizām atbildēm. Papildinformāciju par to, kā izveidot anketas, skatiet [Anketu lietošana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) un ar to saistītās tēmas. |
| Automātisks apstiprinājums | Gatavības pārbaudes ieraksti ietver izvēles rūtiņu **Apstiprināts**, kas norāda apstiprinājuma statusu. Atzīmējiet izvēles rūtiņu **Automātisks apstiprinājums** pārbaudēm, kas jāiestata uz apstiprināts uzreiz pēc tam, kad piešķirtais lietotājs tos pabeidz. Nodzēsiet šo izvēles rūtiņu, lai pieprasītu tiešu apstiprinājumu kā papildu darbību. |
| Obligāts | Atzīmējiet šo izvēles rūtiņu pārbaudēm, kas jāaizpilda piešķirtajam lietotājam. Obligātās pārbaudes nevar izlaist. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]