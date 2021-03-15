---
title: Pārvaldīt tehnisko produktu izmaiņas
description: Šajā tēmā ir sniegta informācija par tehnisko izmaiņu pārvaldību. Tehnisko izmaiņu pārvaldība nodrošina strukturētus procesus, lai pārvaldītu tehnisko produktu izmaiņas, piedāvātu, pieprasītu un veiktu izmaiņas, pārskatītu un apstiprinātu izmaiņas, novērtētu to ietekmi uz esošajiem darījumiem un sekotu tiem.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8ae97d0e6aac1b0961427bd73a37612020231a9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983804"
---
# <a name="manage-changes-to-engineering-products"></a>Pārvaldīt tehnisko produktu izmaiņas

[!include [banner](../includes/banner.md)]

Tehnisko izmaiņu pārvaldība nodrošina strukturētus procesus tehnisko produktu izmaiņu pārvaldībai. Varat izmantot procesu *tehnisko izmaiņu pieprasījums*, lai piedāvātu un pieprasītu izmaiņas, un pēc tam izmantot procesu *tehnisko izmaiņu pasūtījums*, lai veiktu šīs izmaiņas. Lietotāji var izveidot tehnisko izmaiņu pieprasījumus vai tehnisko izmaiņu pasūtījumus, un tad notiek to pārskatīšana un apstiprināšana, to ietekmes uz esošajiem darījumiem novērtēšana un uzraudzība.

## <a name="engineering-change-requests"></a>Tehnisku izmaiņu pieprasījumi

Tehnisko izmaiņu pieprasījuma process ļauj iegūt pieprasījumus pēc izmaiņām no visiem uzņēmuma atbilstošajiem departamentiem. Nav svarīgi, vai strādājat kā inženieris vai ražošanas, piegādes, noliktavas vai pārdošanas nodaļā: jebkurš var izmantot tehnisko izmaiņu pieprasījumu, lai pieprasītu izmaiņas. Šīs izmaiņas var būt ideja jaunam produktam, problēma, ko atklājāt, strādājot ar esošu produktu, ieteikums par esoša produkta uzlabošanu vai kas cits.

Pēc tam, kad kāds iesniedz izmaiņu pieprasījumu, procesu *pārskatīšana un apstiprināšana* pārvalda darbplūsma, kas nosaka, kuram ir jāapstiprina izmaiņas (piemēram, produkta īpašnieks).

Lai iestatītu darbplūsmu tehnisko izmaiņu pasūtījumiem vai tehnisko izmaiņu pieprasījumiem, dodieties uz **Tehnisko izmaiņu pārvaldība \> Tehniskās darbplūsmas**. Atlasiet **Jauns**, izvēlieties, vai darbplūsma tiks izmantota, lai pārskatītu tehnisko izmaiņu pasūtījumus vai tehnisko izmaiņu pieprasījumus, un pēc tam konfigurējiet darbplūsmu.

Lai iegūtu vairāk informācijas par darbplūsmām, skatiet [Darbplūsmas sistēmas apskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Lai iegūtu vairāk informācijas par produktu īpašniekiem, skatiet [Produktu īpašnieki](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Izveidot jaunu tehnisko izmaiņu pieprasījumu

Lai izveidotu tehnisko izmaiņu pieprasījumu, veiciet vienu no šīm darbībām.

- Dodieties uz **Tehnisko izmaiņu pārvaldība \> Kopējais \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu pieprasījumi** un pēc tam darbību rūtī atlasiet **Jauns**.
- Atvēriet esošā tehniskā produkta lapu **Informācija par produktu**. Pēc tam darbību rūtī cilnē **Inženieris** grupā **Tehnisko izmaiņu pārvaldība** atlasiet **Tehnisko izmaiņu pieprasījums \> Jauns tehnisko izmaiņu pieprasījums**.

Tiek izveidots jauns izmaiņu pieprasījums. Tad var katrā kopsavilkuma cilnē iestatiet laukus, kā aprakstīts sekojošās apakšsadaļās.

#### <a name="general-fasttab"></a>Cilne Vispārīgi

Kopsavilkuma cilne **Vispārēji** ļauj norādīt izmaiņu pieprasījuma pamata aprakstu. Nākamajā tabulā ir aprakstīti lauki šajā kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Izmainīt pieprasījumu | Ievadiet tehnisko izmaiņu pieprasījumu. |
| Amats | Ievadiet tekstu, kas īsumā apraksta vai identificē izmaiņas pieprasījumā. |
| Prioritāte | Atlasiet vērtību, lai norādītu, cik augsta ir izmaiņu prioritāte. Pēc nepieciešamības varat pielāgot uzņēmuma pieejamās vērtības. (Papildu informāciju skatiet [Izveidot kopējas vērtības tehnisko izmaiņu pārvaldībai](engineering-change-management-setup.md).) |
| Kategorija | Atlasiet vērtību, lai aprakstītu pieprasīto izmaiņu veidu. Pēc nepieciešamības varat pielāgot uzņēmuma pieejamās vērtības. (Papildu informāciju skatiet [Izveidot kopējas vērtības tehnisko izmaiņu pārvaldībai](engineering-change-management-setup.md).) |
| Stingrība | Atlasiet vērtību, lai norādītu jautājuma nopietnību, kas jānosaka, implementējot pieprasījumu. Pēc nepieciešamības varat pielāgot uzņēmuma pieejamās vērtības. (Papildu informāciju skatiet [Izveidot kopējas vērtības tehnisko izmaiņu pārvaldībai](engineering-change-management-setup.md).) |
| Pieprasīja | Tā lietotāja vārds, kurš izveidoja pieprasījumu. |
| Atbilstoši | Pieprasījuma izveidošanas datums. |
| Statuss | Pieprasījuma statuss. Kad pieprasījums tiek izveidots pirmo reizi, tiek *Izveidots* statuss. Kad pieprasījums ir apstiprināts, statuss tiek mainīts uz *Apstiprināts*. Ja pieprasījumam ir izveidots saistīts izmaiņu pasūtījums, statuss mainās uz *Turpinājums*. |
| Izmaiņu pasūtījums | Izmaiņu pasūtījuma numurs, ja izmaiņu pieprasījums tika izsekots, izmantojot izmaiņu pasūtījumu. |

#### <a name="information-fasttab"></a>Informācijas kopsavilkuma cilne

Kopsavilkuma cilne **Informācija** ļauj pievienot papildu informāciju par pieprasījumu.

Lai pievienotu rindu režģim, rīkjoslā virs režģa atlasiet **Jauns** un pēc tam atlasiet vienu no šīm opcijām:

- **Fails** - faila augšupielāde.
- **Attēls** — attēla faila augšupielāde.
- **Piezīme** — Ievadiet piezīmi tieši režģī.
- **Vietrādis URL** — Ievadiet URL tieši režģī.

Nākamajā tabulā ir aprakstīti lauki katrā rindā.

| Lauks | Apraksts |
|---|---|
| Izveidošanas datums un laiks | Datums un laiks, kad tika izveidota rinda. |
| tips | Informācijas veids, kam tika izveidota rinda (fails, attēls, piezīme vai URL). |
| Apraksts | Ievadiet rindas aprakstu. |
| Ierobežojums | Vērtība, kas norāda, vai pievienotā informācija nāca no iekšēja vai ārēja avota. |
| Piesaistīts | Atzīmētā izvēles rūtiņa norāda, ka rinda ietver pielikumu (failu vai attēlu). Lai lejupielādētu pielikumu, atlasiet rindu un pēc tam rīkjoslā virs režģa atlasiet **Atvērt**. |

#### <a name="products-fasttab"></a>Produktu kopsavilkuma cilne

Kopsavilkuma cilne **Produkti** ļauj jums uzskaitīt katru produktu, ko ietekmē izmaiņu pieprasījums. Rīkjoslas pogas var izmantot, lai pievienotu produktus režģim vai noņemtu produktus.

Šis saraksts ir paredzēts tikai informatīviem nolūkiem. Tāpēc jūs varat pievienot tik daudz saistīto produktu, cik uzskatāt par atbilstošu. Ja esošajām produktam izveidojat izmaiņu pieprasījumu no lapas **Informācija par produktu**, šis produkts ir jāuzskaita kopsavilkuma cilnē **Produkti** pēc pieprasījuma ieraksta saglabāšanas.

#### <a name="source-fasttab"></a>Avota kopsavilkuma cilne

Kopsavilkuma cilne **Avots** ļauj izsekot izmaiņu pieprasījuma sākumpunktu. Tas noder, piemēram, ja vēlaties redzēt, vai izmaiņu pieprasījums tika izveidots no pārdošanas pasūtījuma, kurš to izveidoja un kurā uzņēmumā tas tika izveidots.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Novērtēt izmaiņu pieprasījuma biznesa ietekmi

Pārskatot izmaiņu pieprasījumu, var meklēt atkarības. Šādā veidā varat novērtēt pieprasīto izmaiņu ietekmi uz atvērtajām darījumiem, piemēram, pārdošanas pasūtījumiem, ražošanas pasūtījumiem un rīcībā esošajiem krājumiem.

1. Dodieties uz **Tehnisko izmaiņu pārvaldība \> Kopējais \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu pieprasījumi**.
1. Vai nu atveriet esošu izmaiņu pieprasījumu, vai arī darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu izmaiņu pieprasījumu.
1. Darbības rūtī cilnē **Izmaiņu pieprasījums**, kas atrodas grupā **Ietekme uz uzņēmējdarbību**, atlasiet vienu no šīm pogām:

    - **Meklēšana** — skenējiet visus atvērtos darījumus un pēc tam atveriet dialoglodziņu **Uzņēmējdarbības ietekme uz atvērtiem darījumiem**, ko ietekmēs izmaiņas.
    - **Skatīt iepriekšējo meklēšanu** – Atvēriet dialoglodziņu **Uzņēmējdarbības ietekme uz atvērtiem darījumiem**, kas uzskaita iepriekšējās meklēšanas rezultātus. (Jauna meklēšana nav veikta.)

1. Ja problēma, kurai nepieciešamas izmaiņas, ir kritiska, varat bloķēt atvērtos darījumus vai informēt atbildīgo lietotāju, izmantojot pogas rīkjoslā, kas atrodas dialoglodziņā **Uzņēmējdarbības ietekme uz atvērtiem darījumiem**.

### <a name="create-a-change-order-from-a-change-request"></a>Izmaiņu pasūtījuma izveide no izmaiņu pieprasījuma

Inženieris, kurš veic tehnisko izmaiņu pieprasījuma pārskatīšanu, var izveidot tehnisko izmaiņu pasūtījumu tieši no lapas **Tehnisko izmaiņu pieprasījums**. Darbības rūtī cilnē **Mainīt pieprasījumu**, kas atrodas grupā **Tehnisko izmaiņu pasūtījums**, atlasiet **Kopēt saiti un produktus**.

## <a name="engineering-change-orders"></a>Tehnisku izmaiņu pasūtījumi

Tehnisko izmaiņu pasūtījumi nodrošina strukturētu procesu izmaiņu veikšanai tehniskajos produktos. Izmaiņas var ierosināt, izmantojot ar inženieriju saistītu datu kopiju. Reālie pamatdati netiek ietekmēti. Papildinformāciju par ar inženieriju saistītiem datiem skatiet [Tehnisko versiju un tehnisko preču kategorijas](engineering-versions-product-category.md).

Varat izveidot tehnisko izmaiņu pasūtījumu, kas ir balstīts uz apstiprināto tehnisko izmaiņu pieprasījumu. Inženieri var izveidot arī tehniskās izmaiņas pasūtījumus no nulles. Varat iekļaut vairākus produktus vienā tehnisko izmaiņu pasūtījumā, veicot kādu no šīm darbībām:

- Manuāli atlasiet produtus.
- Lietojiet materiālu komplektu (MK), lai iekļautu produktus, kas ir zemāki produktu struktūrā (tas ir, bērnelementi).
- Izmantojiet meklēšanu ´kur lietots´, lai iekļautu produktus, kas ir augstāki par produkta struktūru (t.i., vecākelementi).

Pēc tam, kad priekšlikums par izmaiņām ir pabeigts, pārskatīšanas un apstiprināšanas process tiks apstrādāts darbplūsmā. Var iestatīt dažādas darbplūsmas, kas pamatotas uz prioritātēm un nopietnību.

Lai iestatītu darbplūsmu tehnisko izmaiņu pasūtījumiem vai tehnisko izmaiņu pieprasījumiem, dodieties uz **Tehnisko izmaiņu pārvaldība \> Tehniskās darbplūsmas**. Atlasiet **Jauns**, izvēlieties, vai darbplūsma tiks izmantota, lai pārskatītu tehnisko izmaiņu pasūtījumus vai tehnisko izmaiņu pieprasījumus, un pēc tam konfigurējiet darbplūsmu.

Lai iegūtu vairāk informācijas par darbplūsmām, skatiet [Darbplūsmas sistēmas apskats](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Lūk, dažas tipiskas ieinteresētās personas, kurām varētu būt jāapstiprina tehnisko izmaiņu secība:

- **Produktu īpašnieki** - Lai iegūtu vairāk informācijas par produktu īpašniekiem, skatiet [Produktu īpašnieki](product-owner.md).
- **Atbildīgās grupas vadītājs** – Lauks **Inženieris** tehnisko izmaiņu pasūtījuma skatā **Virsraksts** tiek parādīts inženieris, kas izveidoja tehnisko izmaiņu pasūtījumu. Ja inženieris pieder komandai, kas definēta sistēmā, lauks **Atbildīgais** parāda šīs grupas vadītāju.
- **Finanšu departaments** — finanšu departamentam varētu būt jāpārskata gadījumi, kad izmaiņas ietver lielas izmaksas.

Varat izvēlēties, vai tehnisko izmaiņu pasūtījums ir jāapstrādā uzreiz pēc tā apstiprināšanas, kā darbplūsmas daļa, vai arī apstrāde jāveic vēlāk, kā manuālu darbību. Tehnisko izmaiņu pasūtījuma apstrādes laikā tiek atjaunināti tehniskie dati faktiskajā produktā.

Apskatot izmaiņu pieprasījumu, darbības rūtī cilnē **Izmaiņu pieprasījums**, kas atrodas grupā **Ietekme uz uzņēmējdarbību**, atlasiet **Meklēšana**, lai novērtētu piedāvāto izmaiņu ietekmi uz atvērtajiem darījumiem, piemēram, pārdošanas pasūtījumiem, ražošanas pasūtījumiem un rīcībā esošajiem krājumiem. Rezultāti tiek parādīti dialoglodziņā **Ietekme uz uzņēmējdarbību**, kur varat atlasīt ietekmētos darījumus un pēc tam izmantot komandas rīkjoslā, lai skatītu papildu informāciju, paziņot atbildīgajam lietotājam vai bloķēt darījumu.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Tehnisko izmaiņu pasūtījumi inženiertehniskajos vai operacionālajos uzņēmumos

Kā aprakstīts sadaļā [Inženiertehniskie uzņēmumi un datu īpašumtiesību kārtulas](engineering-org-data-ownership-rules.md), produktu dati, kurus var rediģēt, ir atkarīgi no juridiskās personas veida, ar kuru strādājat (inženiertehniskais uzņēmums pret operacionālo uzņēmumu). Datu īpašumtiesību kārtulas tiek lietotas arī tehnisko izmaiņu pasūtījumiem. Tāpēc atkarībā no juridiskās personas, kurā veidojat tehnisko izmaiņu pasūtījumu, var veikt dažāda veida izmaiņas. Daži piemēri:

- Tehnisko izmaiņu pasūtījumiem **inženiertehniskajā uzņēmumā** var veikt pamata izmaiņas tehniskajiem datiem. Piemēram, var izveidot jaunas produkta versijas, mainīt produkta struktūru, izmantojot MK, un mainīt tehnisko atribūtu vērtības. Attiecībā uz katru attiecīgo produktu, atlasiet vienu no šīm vērtībām laukā **Ietekme**:

    - **Nav** — atjauniniet esošo produkta versiju (versijas atjaunināšana).
    - **Jauna versija** — izveidot jaunu versiju, kas pamatota uz atlasīto produkta versiju.
    - **Jauns produkts** — Izveidojiet pilnīgi jaunu produktu vai produkta variantu, kas ir balstīts uz atlasīto produkta versiju.

- Tehnisko izmaiņu pasūtījumiem **operacionālā uzņēmumā** varat mainīt produkta loģistikas datus. Piemēram, varat bagātināt esošo MK ar ielādes iestatījumiem, pievienot vietējos maršrutus vai vietējos MK un pat bagātināt MK, pievienojot jaunas MK rindas vietējiem iepakojuma materiāliem, eļļošanas šķidrumiem vai instrukcijām vietējā valodā. Bagātināšana, ko lietotāji veic operacionālajā uzņēmumā, tiks saglabāta, kad no inženiertehniskā uzņēmuma tiek nosūtīti jauni atjauninājumi. Papildinformāciju skatiet šeit: [Inženiertehniskie uzņēmumi un datu īpašumtiesību kārtulas](engineering-org-data-ownership-rules.md).

    Kad tehnisko izmaiņu pasūtījumi tiek apstrādāti inženiertehniskajā uzņēmumā, produkti tiek izveidoti un/vai atjaunināti tikai inženiertehniskajā uzņēmumā. Tāpēc, ja preču šablona dati ir jāatjaunina, ir arī jāatbrīvo produkti no operacionāliem uzņēmumiem.

- Produktus var tieši izlaist no tehnisko izmaiņu pasūtījumiem. Atveriet izmaiņu pasūtījumu un pēc tam darbības rūtī, cilnē **Mainīt pasūtījumu** grupā **Produktu laidieni** atlasiet **Izlaist produkta struktūru**. Process darbojas tieši tāpat, kā tas darbojas, izlaižot produktus no lapas **Izlaistie produkti**. Plašāku informāciju skatiet sadaļā [Izlaist produkta struktūras](release-product-structure.md).
- Varat produktus automātiski izlaist no tehnisko izmaiņu pasūtījumiem, pamatojoties uz šādiem faktoriem:

    - Atkārtota izlaišana uzņēmumiem, kuros produkti tika iepriekš izlaisti. Atlasiet **Meklēšana**, lai skenētu visus iepriekšējos laidienus, un pēc tam atlasiet **Skatīt**, lai apskatītu rezultātus. Lapā **Skatīt** ir redzami iepriekšējā produkta laidieni, un jūs varat atlasīt, kurus produktus vēlaties izlaist atkārtoti. Pēc tam aizveriet lapu **Skatīt** un atlasiet **Process**, lai atkārtoti izlaistu atlasītos produktus.
    - Automātiskās izlaišanas iestatījumi tehnisko produktu kategorijas izlaišanas kontrolē. Šo izlaišanu var veikt kā darbplūsmas daļu. Kad tiek izmantots bloks **savākt laidiena priekšlikumu**, laidiena priekšlikums tiks aizpildīts ar atkārtotas izlaišanas priekšlikumiem (skatiet iepriekšējo saraksta vienumu) un produkti tiks nodoti uzņēmumiem, ja tehnisko produktu kategorijas izlaišanas kontrolē ir atzīmēta izvēles rūtiņa **Izlaist automātiski**. Varat atlasīt **Skatīt**, lai skatītu rezultātus, kā aprakstīts iepriekšējā saraksta vienumā. Produkti tiks izlaisti arī tad, kad tiek izmantots bloks **procesa laidiena priekšlikums**. Ja izvēlaties tikai apkopot priekšlikumu kā darbplūsmas daļu, varat manuāli sākt izlaišanu, atlasot **Process**, kā aprakstīts iepriekšējā saraksta vienumā.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Sekošana tehnisko izmaiņu pieprasījumam, izmantojot tehnisko izmaiņu pasūtījumu

Tiklīdz tehnisko izmaiņu pieprasījums ir apstiprināts, varat tam sekot, izmantojot tehnisko izmaiņu pasūtījumu. Varat kombinēt vairākus tehnisko izmaiņu pieprasījumus vienā tehnisko izmaiņu pasūtījumā. Vienā tehnisko izmaiņu pasūtījumā var iekļaut pat vairākus produktus. (Parasti šo pieeju izmanto, kad vienas un tās pašas izmaiņas jālieto vairākiem produktiem.) Tomēr nevar izveidot vairākus tehnisko izmaiņu pasūtījumus no vienas tehnisko izmaiņu pieprasījuma.

Lai izsekotu izmaiņu pieprasījumam, izmantojot izmaiņu pasūtījumu, atveriet izmaiņu pieprasījumu un pēc tam darbību rūtī, cilnē **Mainīt pasūtījumu**, kas atrodas grupā **Tehnisko izmaiņu pasūtījuma**, atlasiet **Kopēt saiti un produktus**. Pēc tam varat atlasīt esošo tehnisko izmaiņu pasūtījumu, lai savienotu to ar izmaiņu pieprasījumu, vai arī varat izveidot jaunu tehnisko izmaiņu pasūtījumu šim konkrētajam pieprasījumam.

## <a name="engineering-change-order-report"></a>Tehnisku izmaiņu pasūtījuma pārskats

Tehnisko izmaiņu pasūtījumu pārskati apraksta izmaiņas, kas tika veiktas tehnisko izmaiņu pasūtījumā. Tās noder gan pārskatīšanas, gan apstiprināšanas procesa laikā un pēc tā.

Lai skatītu tehnisko izmaiņu pasūtījuma pārskatu, atveriet atbilstošo izmaiņu pasūtījumu un pēc tam darbības rūtī, cilnē **Mainīt pasūtījumu**, kas atrodas grupā **Skatīt**, atlasiet **Tehnisko izmaiņu pasūtījuma pārskats**.

## <a name="fields-on-an-engineering-change-order"></a>Tehnisko izmaiņu pasūtījuma lauki

Lielākā daļa tehnisko izmaiņu pasūtījumu lauku ir tādi paši kā izlaisto produktu, tehnisko versiju, dokumentu, MK (rindu) un maršrutu (operāciju) lauki. Tomēr lauki sekojošajā tabulā ir unikāli izmaiņu pasūtījumu veikšanai.

| Lauks | Apraksts |
|---|---|
| Tehnisku izmaiņu iemesli | Atlasiet ietekmētā produkta izmaiņas iemeslu. |
| Izmaiņu apraksts | Izmaiņas apraksta ievadīšana. |
| Nepieciešamie īpašie instrumenti | Norādiet, vai, lai piemērotu izmaiņas, ir nepieciešama īpaša rīku izveide. |
| Tehnisko materiālu izvietojums | Atlasiet materiāla izvietojuma kodu visiem atkritumiem, kas rodas, veicot izmaiņas. |
| Nepieciešams klienta apstiprinājums | Norādiet, vai ir nepieciešams debitora apstiprinājums, pirms var piemērot izmaiņas. |
| Saņemts klienta apstiprinājums | Norādiet debitora apstiprinājuma statusu. |
| Vides veselība un drošība | Norādiet, vai vides veselības un drošības noteikumi attiecas uz izmaiņām. Ja attiecas, tad varat atlasīt piemērojamās kārtulas. |

Varat izmantot pogu **Uzturēt/kopēt izmaiņu informāciju**, lai kopētu izmaiņu informāciju starp ietekmētajiem produktiem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]