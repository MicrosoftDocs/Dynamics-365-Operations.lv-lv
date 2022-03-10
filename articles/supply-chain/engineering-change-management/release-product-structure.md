---
title: Izlaist preču struktūras
description: Šajā tēmā skaidrots, kā var izlaist pilnīgas preču struktūras papildus izlaistajām precēm kopā ar to tehniskajām versijām. Šādā veidā var nodrošināt, ka tehnisko preču datus var viegli izmantot atkārtoti atšķirīgās juridiskās personās.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4dc1b073350044ef8afb765470ed14da88a70fdd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567491"
---
# <a name="release-product-structures"></a>Izlaist preču struktūras

[!include [banner](../includes/banner.md)]

Lai nodrošinātu, ka tehniski svarīgus preču datus var viegli atkārtoti izmantot dažādās juridiskās personās, varat izlaist pilnīgas preču struktūras papildus preču izlaišanai kopā ar to tehniskajām versijām. Tāpēc ir iespējams nodot materiālu komplekta (MK) struktūras kopā ar pamatvienību vienā laidiena darbībā. Šādā gadījumā tiek izlaistas arī MK un zemākā līmeņa preces.

Tehniskās preces izveido un uztur to inženierijas uzņēmums tādā veidā, ka tie izstrādes brīdī atbilst kvalitātes prasībām. Katram uzņēmumam, kas ražo preces, ir nepieciešama tā pati prece un pamatā esošais MK. Atkarībā no ražošanas iestādes maršruts var tikt izveidots lokāli. Šādā gadījumā maršrutu nedrīkst izlaist kopā ar preci. Juridiskām personām, kas pārdos preces, bet tās neražos, MK var nebūt nepieciešami.

Lai procesu padarītu efektīvāku, visus ar tehniku saistītos datus var izlaist vienlaicīgi citiem darbojošajiem uzņēmumiem. Šie dati ietver preču struktūru. Izlaišanas procesa laikā varat izvēlēties, kuru preces datu daļu izlaist.

Plašāku informāciju par tehniskajiem uzņēmumiem un darbojošajiem uzņēmumiem skatiet [Tehnisko uzņēmumu un datu īpašumtiesību kārtulas](engineering-org-data-ownership-rules.md).

Ievērojiet, ka jūs varat izlaist standarta preces un tehniskās preces kopā ar izlaisto preču struktūru. Šī procesa laikā visa preču struktūra tiks izlaista, pat MK un maršruts no uzņēmuma, kurā preces tiek izlaistas.

Piemēram, kā izlaist preci, skatiet sadaļu [Tehniskās preces izlaišana vietējā uzņēmumā](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Izlaistie preces dati, kad tiek izmantota izlaistās preces struktūra

Tehniskajās precēs ir iekļauti šādi dati:

- **Preces dati** - tiek izveidota jauna izlaistā prece.
- **Tehniskās versijas dati** - tehniskā versija un tās dati tiek izveidoti vai atjaunināti. Ņemiet vērā, ka tad, ja atkārtoti tiek nodota tāda pati tehniskā versija darbojošajam uzņēmumam, tehniskie dati tiks pārrakstīti.
- **Tehniskie atribūti** - tehniskie atribūti un to vērtības tiek veidotas vai atjauninātas.
- **Tehnikas materiālu komplekts** - var izveidot vai atjaunināt tehnikas MK un tā rindas. Lai iegūtu vairāk informācijas par datu īpašumtiesībām, skatiet [Preču īpašnieki](product-owner.md).
- **Tehniskie maršruti** - tehniskie maršruti un to darbības car tikt veidotas vai atjauninātas. Lai iegūtu vairāk informācijas par datu īpašumtiesībām, skatiet [Preču īpašnieki](product-owner.md).
- **Tehniskie dokumenti** - tiek veidoti vai atjaunināti tehniskie dokumenti, kas ir saistīti ar tehnisko versiju.

Kad sistēmā tiek ieslēgta tehnisko izmaiņu pārvaldība, ir pieejama izlaistās preces struktūra. Turklāt standarta preces tiek iekļautas to MK un maršrutos, kad tās tiek izlaistas.

## <a name="product-acceptance"></a>Preču pieņemšana

**Preces pieņemšana** ir galvenais parametrs, kas ietekmē nodošanas procesu. Varat iestatīt šo parametru katram uzņēmumam, pārejot uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldības parametri**. Plašāku informāciju skatiet [Tehnisko izmaiņu pārvaldības parametri](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automātiska preces pieņemšana

Katra tehniskās preces izlaišana sākas, kad kāds no tehniskā uzņēmuma izvēlas izlaižamo preci. Kad **Preces pieņemšanas** parametrs ir iestatīts uz *Automātisks*, lietotājam tehniskajā uzņēmumā ir jāizlemj, kuri preces dati ir automātiski jānodod darbības uzņēmumiem. Prece tiks automātiski nodota uzņēmumiem, kas atlasīti atbrīvošanas vednī.

### <a name="manual-product-acceptance"></a>Manuāla preču pieņemšana

Katra tehniskās preces izlaišana sākas, kad kāds no tehniskā uzņēmuma izvēlas izlaižamo preci. Kad **Preces pieņemšanas** parametrs ir iestatīts uz *Manuāls*, lietotājam tehniskajā uzņēmumā ir jāizlemj, kuri preces dati ir jānodod darbības uzņēmumiem. Lietotājs no katra darbības uzņēmuma pārskata preču datus un lemj par to, vai pieņemt izlaišanu. Kad dati tiek saņemti, lietotājs darbības uzņēmumā var iestatīt šādas opcijas:

- Ja preces (atjauninājumi) nav būtiskas darbības uzņēmumam, lietotājs var izvēlēties nepieņemt izlaišanu.
- Lietotājs var mainīt krājuma veidni jaunām precēm.
- Lietotājs var izvēlēties, vai preci izlaist kopā ar MK un/vai maršrutiem un vai tās ir jāatbrīvo kā apstiprinātas un aktīvas.
- Lietotājs var mainīt preču spēkā stāšanās datumu.

Piemēram, kā pieņemt preci, skatiet [Preču pārskatīšana un apstiprināšana pirms to nodošanas vietējā uzņēmumā](engineering-scenarios.md#accept).

> [!NOTE]
> Standarta precēm varat izlaist no jebkuras juridiskas personas uz citu juridisku personu. Tehniskajām precēm vienīgā juridiskā persona, no kuras varat izlaist, ir tehniskais uzņēmums.

## <a name="release-policies"></a>Laidiena politikas

Ne visiem darbību uzņēmumiem ir vajadzīgi tie paši preces dati. Parasti darbības uzņēmumiem, kas ražo tehnikas preces, ir nepieciešama MK, turpretī darbības uzņēmumam, kas pārdod tikai tehnikas preces, nav nepieciešams MK. Varat izmantot laidiena politikas, lai izveidotu parametrus, kas tiek izmantoti preču izlaišanai.

Papildinformāciju par produktu kategorijām skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

Laidiena procesa laikā varat ietekmēt iestatījumus.

## <a name="create-and-manage-product-release-policies"></a>Izveidot un pārvaldīt preču laidiena politikas

Lai strādātu ar preces laidiena politikām, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Preces laidiena politikas**. Pēc tam izpildiet kādu no norādītajām darbībām.

- Lai izveidotu jaunu politiku, darbības rūtī atlasiet **Jauns** un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai rediģētu esošu politiku, atlasiet to saraksta rūtī, atlasiet **Jauns** darbību rūtī un pēc tam iestatiet laukus, kā aprakstīts turpmākajās apakšsadaļās.
- Lai dzēstu esošu politiku, atlasiet to saraksta rūtī, darbību rūtī atlasiet **Rediģēt** un tad kopsavilkuma cilnē **Vispārīgi** pārliecinieties, ka opcija **Aktīvs** ir iestatīta uz *Nē*. Pēc tam darbību rūtī atlasiet **Dzēst**.

### <a name="header"></a>Galvene

Iestatiet tālāk norādītos laukus preces laidiena politikas virsrakstā.

| Lauks | Apraksts |
|---|---|
| Vārds, uzvārds | Ievadiet politikas nosaukumu. |
| Apraksts | Ievadiet politikas aprakstu. |

### <a name="general-fasttab"></a>Cilne Vispārīgi

Iestatiet tālāk norādītos laukus preces laidiena politikas kopsavilkuma cilnē **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Preces veids | Atlasiet, vai politika attiecas uz *Krājuma* vai *Pakalpojuma* veida precēm. Pēc ieraksta saglabāšanas šo iestatījumu nevar mainīt. |
| Ražošanas veids | Šis lauks parādās tikai tad, ja esat iespējojis [formulu izmaiņu pārvaldību](manage-formula-changes.md) jūsu sistēmā. Atlasiet ražošanas tipu, uz kuru attiecas šī izlaišanas politika:<ul><li>**Līdzprodukts** – izmantojiet šo izlaišanas politiku, lai pārvaldītu līdzproduktus. Līdzprodukti tiek ražoti procesa ražošanas laikā, un tie nav versijas vai inženiertehniskās preces. Līdzproduktu izlaišanas politikas var palīdzēt nodrošināt, ka svarīgi iestatījumi, piemēram, **Noliktavas dimensiju grupa** un **Izsekošanas dimensiju grupa**, tiek iestatīti, izmantojot Izlaistās preces veidni, pirms tie tiek nodoti izpildei uzņēmumam.</li><li>**Blakusprodukts** – izmantojiet šo izlaišanas politiku, lai pārvaldītu blakusproduktus. Blakusprodukti tiek ražoti procesa ražošanas laikā, un tie nav versijas vai inženiertehniskās preces. Blakusproduktu izlaišanas politikas var palīdzēt nodrošināt, ka svarīgi iestatījumi, piemēram, **Noliktavas dimensiju grupa** un **Izsekošanas dimensiju grupa**, tiek iestatīti, izmantojot Izlaistās preces veidni, pirms tie tiek nodoti izpildei uzņēmumam.</li><li>**Neviens** - lietojiet šo politiku, lai pārvaldītu standarta preces, kas nav versijas vai inženiertehniskās preces, līdzprodukti vai blakusprodukti.</li><li>**Plānošanas krājums** – izmantojiet šo izlaišanas politiku, lai pārvaldītu plānošanas krājumus, kas ražoti, izmantojot procesa ražošanu. Plānošanas krājumiem tiek lietotas formulas. Tie ir līdzīgi formulas krājumiem, taču tos izmanto, lai ražotu tikai līdzproduktus un blakusproduktus, bet ne pabeigtās preces.</li><li>**MK** – izmantojiet šo izlaišanas politiku, lai pārvaldītu inženiertehniskās preces, kuras neizmanto formulas, un parasti (bet ne vienmēr) ietver MK.</li><li>**Formula** – izmantojiet šo izlaišanas politiku, lai pārvaldītu pabeigtos krājumus, kas ražoti, izmantojot procesa ražošanu. Šiem krājumiem būs formula, bet ne MK.</li></ul> |
| Lietot veidnes | Atlasiet vienu no šīm opcijām, lai norādītu, vai un kā preces laidiena veidnes jālieto, kad tiek lietota politika.<ul><li>**Vienmēr** – izlaistās preces veidne vienmēr ir jāizmanto laidieniem. Ja atlasāt šo opciju, izmantojiet kopsavilkuma cilni **Visas preces**, lai norādītu veidni, kas tiek izmantota katram uzņēmumam, kas tiek izlaists. Ja nenorādāt veidni katram uzņēmumam, kas ir uzskaitīts kopsavilkuma cilnē **Visas preces**, jūs saņemsiet kļūdu, mēģinot saglabāt politiku.</li><li>**Nav obligāti** – ja izlaistā prece ir norādīta uzņēmumam, kas ir norādīts kopsavilkuma cilnē **Visas preces**, šī veidne tiks izmantota, izlaižot preci uz šo uzņēmumu. Pretējā gadījumā veidne netiks izmantota. Ja atlasāt šo opciju, varat saglabāt politiku, nepiešķirot veidnes visiem uzņēmumiem. (Brīdinājums netiks rādīts.)</li><li>**Nekad** – netiks izmantota neviena izlaistās preces veidne, pat ja veidne ir norādīta uzņēmuma, kas norādīti kopsavilkuma cilnē **Visas preces**. Veidnes kolonnas nebūs pieejamas.</li></ul> |
| Aktīvie | Lietojiet šo opciju, lai palīdzētu uzturēt laidiena politikas. Iestatiet to uz *Jā* visām jūsu izmantotajām laidiena politikām. Iestatiet to uz *Nē*, lai, to neizmantojot, atzīmētu laidiena politiku kā neaktīvu. Ņemiet vērā, ka nav iespējams deaktivizēt laidiena politiku, kas piešķirta tehnisko preču kategorijai, un var dzēst tikai neaktīvu laidienu politikas. |

### <a name="all-products-fasttab"></a>Visas preces kopsavilkuma cilne

Kopsavilkuma cilnē **Visas preces** pievienojiet rindu katram darbības uzņēmumam, kuram vēlaties izmantot šo politiku, lai to nodotu izpildei. Izmantojiet pogas kopsavilkuma cilnē **Visas preces**, lai pievienotu un noņemtu rindas pēc nepieciešamības. Katrai rindai, kuru pievienojat, iestatiet tālāk norādītos laukus.

> [!NOTE]
> Iestatījumi kopsavilkuma cilnē **Visas preces** attiecas gan uz tehniskajām precēm, gan uz standarta precēm.

| Lauks | Apraksts |
|---|---|
| Uzņēmuma kontu ID | Atlasiet uzņēmumu, uz kuru attiecas rinda. Rindas parametri tiks piemēroti, kad preces tiks nodotas šim uzņēmumam. |
| Veidnes izlaistā prece | Pievienojiet veidni precei. |
| Kopēt MK apstiprinājumu | Atzīmējiet šo izvēles rūtiņu, lai kopētu MK apstiprināšanas statusu uz saņemšanas uzņēmumu. |
| Kopēt MK aktivizāciju | Atzīmējiet šo izvēles rūtiņu, lai kopētu MK aktivizācijas statusu uz saņemšanas uzņēmumu. |
| Kopēt maršruta apstiprinājumu | Atzīmējiet šo izvēles rūtiņu, lai kopētu maršruta apstiprināšanas statusu uz saņemšanas uzņēmumu.|
| Kopēt maršruta aktivizēšanu | Atzīmējiet šo izvēles rūtiņu, lai kopētu maršruta aktivizācijas statusu uz saņemšanas uzņēmumu. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Opcijas parametri tehniskajām precēm kopsavilkuma cilne

Katru reizi, kad jūs pievienojiet rindu kopsavilkuma cilnē **Visas preces**, rinda, kurai ir atbilstoša **Uzņēmuma kontu ID** vērtība, tiek izveidota arī kopsavilkuma cilnē **Opcijas parametri tehniskajām precēm**. Tad, ja jūs noņemat rindu no kopsavilkuma cilnes **Visas preces**, rinda, kurai ir atbilstoša **Uzņēmuma kontu ID** vērtība, tiek noņemta no kopsavilkuma cilnes **Opcijas parametri tehniskajām precēm**.

Katrai rindai, kas tiek rādīta kopsavilkuma cilnē **Opciju parametri tehniskajām precēm**, iestatiet sekojošos laukus.

> [!NOTE]
> Iestatījumi kopsavilkuma cilnē **Opciju parametri tehniskajām precēm** attiecas tikai uz tehniskajiem izstrādājumiem.

| Lauks | Apraksts |
|---|---|
| Veidnes MK | Kad prece, kam ir MK, tiek izlaista, tiks pievienotas norādītā veidnes MK rindas. Šis lauks noder vietējo komponentu, piemēram, iepakojuma vai instrukciju pievienošanai vietējā valodā. |
| Veidnes maršruts | Kad prece, kam ir maršruts, tiek izlaista, tiks pievienotas norādītā veidnes rindas. |
| Kopēšanas spēkā būšana | Atlasiet, vai, izlaižot preces no tehniskā uzņēmuma uz darbības uzņēmumu, ir jākopē darba izpildes datumi. |
| Automātiski pievienot izlaides priekšlikumam | Atzīmējiet šo izvēles rūtiņu precēm, kuras ir automātiski jānodod tehnisko izmaiņu pasūtījumā. Šādā veidā preces, kas pieder tehnisko preču kategorijām, kas izmanto šo izlaišanas politiku, var tikt automātiski nodoti darbību uzņēmumiem, kur šī opcija ir iestatīta. (Plašāku informāciju skatiet rakstā [Pārvaldīt izmaiņas tehniskajām precēm](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Pārskatiet katru preci, to izlaižot

Kad tiek izlaistas tehniskās preces, kurām ir MK vai maršruti, parametri tiks iestatīti uz noklusētajām vērtībām, kā norādīts laidiena politikā. Kā lietotājs, jūs varat ietekmēt šo uzvedību izlaišanas pusē, kad izmantojat laidiena preces struktūru.

Lai izlaistu tehniskās preces, lapā **Izlaistās preces** atlasiet preces, ko nodot laidienam, un pēc tam atlasiet opciju **Izlaist preces struktūru**, lai atvērtu laidiena ceļvedi. Lapā **Atlasīt tehniskās preces** tiek parādītas preces. Atlasiet vienu preci un pēc tam atlasiet **Laidiena detaļas**, lai pārskatītu preces laidiena detaļas.

Lapā **laidiena detaļas** varat mainīt **Saņemt MK**, **Kopēt MK apstiprinājumu**, **Kopēt MK aktivizāciju**, **Saņemt MK**, **Kopēt maršruta apstiprinājumu** un **Kopēt maršruta aktivizācijas** lauku vērtības. Push-pull scenārijā varat mainīt to pašu lauku vērtību, kas atrodas saņemšanas pusē, ar nosacījumu, ka MK un maršruts tiek izlaists.

## <a name="product-owners-and-product-releases"></a>Preču īpašnieki un preces laidieni

Preces īpašnieki zina, kurām juridiskām personām ir nepieciešamas savas preces, preces var izlaist tikai šīs preces preču īpašnieka grupas dalībnieki. Citi lietotāji nevar izlaist preces, kas tām nepieder.

Šo darbību var veikt tikai tad, ja prece ir tieši atlasīta izlaišanai. Preces, kas ir daļa no citas preces struktūras, izmantojot MK, *var* izlaist neīpašnieka lietotāji, izlaižot pamatproduktu, ar nosacījumu, ka tiem pieder pamatprodukts.

Piemēram, prece X ir piešķirta *Dizaina skapju* preces īpašnieku grupai. Prece X arī ir daļa no preces Y MK, kas ir piešķirts *Dizaina skaļruņu* preces īpašnieku grupai. Ja lietotājs no *Dizaina skaļruņu* preces īpašnieku grupas atbrīvo produktu Y un tā MK, prece X tiks izlaista kopā ar preci Y.

Papildinformāciju skatiet sadaļā [Preču īpašnieki](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
