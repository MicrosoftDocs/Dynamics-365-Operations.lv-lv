---
title: Izlaist uz noliktavu
description: Šajā rakstā ir sniegta detalizēta informācija par pārsūtīšanas uz noliktavu procesu. Tajā aprakstītas tās entitījas, kuras tiek izveidotas, izlaižot pasūtījumu uz noliktavu, un opcijas, kuras varat lietot, lai iniciētu šo procesu.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c3280b2e39d7af5ca99cad703cad6ecc7b307bff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893183"
---
# <a name="release-to-warehouse"></a>Izlaist uz noliktavu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegta detalizēta informācija par pārsūtīšanas uz noliktavu procesu. Tajā aprakstītas tās entitījas, kuras tiek izveidotas, izlaižot pasūtījumu uz noliktavu, un opcijas, kuras varat lietot, lai iniciētu šo procesu.

## <a name="release-to-warehouse-overview"></a>Izlaišanas noliktavā pārskats

Izlaišana noliktavā ir process, kurā inventārs tiek sagatavots izsūtīšanas apstrādei. Izlaižot pasūtījumu uz noliktavu, sistēma izveidot kravu rindas un sūtījumus. Ja ir iestatīta automātiskā kopuma apstrāde, tiek izveidotas arī kravas un vajadzīgais darbs. Iesaistīto entitīju konfigurācija ir atkarīga no sistēmas iestatījumiem. Šajā sadaļas sadaļā ir pārskata entītijas, kas izveidotas, kad tiek nodotas izpildei noliktavas procesā, un sistēmas iestatījumus, kas tos definē.

*Sūtījums* ir pārdošanas pasūtījumu vai pārsūtīšanas pasūtījuma rindu grupa, kura attiecas uz vienu un to pašu klientu vai vienu un to pašu piegādes adresi.

*Krava* ir pārdošanas pasūtījumu vai pārsūtīšanas pasūtījumu rindu grupa, kura parasti tiek izsūtīta vienā kravas auto, vagonā vai citā transporta līdzeklī. Kravai var būt viens vai vairāki sūtījumi. Varat manuāli izveidot kravu, jaunai kravai pievienojot pasūtījuma rindas. Šādā gadījumā pasūtījuma rindas tiek piešķirtas kravai, pirms tiek iniciēts izlaišanas uz noliktavu process, un tās var izlaist vienīgi no lapas **Plānošanas rīka ielāde**.

Noliktavas *darbs* ir jebkura noliktavas darbība, kuru veic noliktavas darbinieks. Parasti noliktavas darba darbības sastāv no vismaz divām secīgām darbībām: noliktavas darbinieks saņem rīcībā esošos krājumus vienā vietā un pēc tam tos novieto citā.

Kad noliktavā tiek izlaisti pasūtījumi, sistēma rada *kravu rindas* un tās sagrupē sūtījumos. Sūtījumu apvienošanas process ļauj veikt automātisku sūtījumu apvienošanu izlaišanas uz noliktavu procesa laikā. Papildinformāciju skatiet sadaļā [Sūtījumu apvienošanas politika](about-shipment-consolidation-policies.md).

Sistēma izmanto *kopumus*, lai izveidotu atlases darbus un kravas sūtīšanai. *Kopuma veidnei* ir jābūt pieejamai kopumam, kuru vēlaties izveidot un pasūtījuma rindas noliktavai. *Sūtījuma* tipa kopuma veidnes tiek izmantotas, lai sūtītu vienumus pārdošanas pasūtījumiem un pārsūtīšanas pasūtījumiem.

Katra kopuma veide satur *kopuma metodes*. Kopuma metodes izpilda darbības, piemēram, darba izveidi kopumam vai kravu izveidi. Piemēram, kopuma veidne sūtīšanas kopumiem var ietvert metodes kravu izveidei, rindu piešķirei kopumiem papildināšanai un izdošanas darbu izveidi kopumam. Kopuma veidne nosaka iestatījumus, kuri definē to, kā kopums tiks ģenerēts un apstrādāts, kuras darbības veicamas manuāli, un kuras darbības tiks veiktas automātiski. Papildu informāciju skatiet [Kopuma veidnes](wave-templates.md). Tādējādi, atkarībā no jūsu kopuma veidnes konfigurācijas, kopums tiek vai nu automātiski izveidots, apstrādāts un izlaists, kad izlaižat uz noliktavu pasūtījumu, vai arī dažas vai visas no darbībām tiek veiktas manuāli pēc tam, kad tiek veikta izlaišana uz noliktavu.

Pēc kopuma apstrādes sistēma izveidot izveides darbu, pamatojoties piemērotā *darba veidnē* un *atrašanās vietas direktīvā* un padara šo darbu pieejamu mobilajās ierīcēs. Darba veidne nosaka to, kā darbs tiek veikts katram noliktavas procesam, bet atrašanās vietas direktīva konkretizē krājuma kustības izdošanas un nolikšanas vietas. Papildinformāciju skatiet šeit: [Noliktavas darba kontrolēšana, izmantojot darbu veidnes un novietojuma direktīvas](control-warehouse-location-directives.md).

> [!NOTE]
> Kopumi pēc noklusējuma tiek apstrādāti partijas režīmā.

Kopuma apstrādes laikā sistēma parasti izveido jaunu kravu katram sūtījumam, kam nav piešķirta krava. Ja vēlaties, lai sistēma esošām slodzēm piešķir nepiešķirtus sūtījumus, varat izmantot papildu kopuma kravas veidošanas funkciju. Papildinformāciju skatiet sadaļā [Papildu kravas veidošana kopuma laikā](advanced-load-building-during-wave.md).

Lapās **Pārdošanas pasūtījumi** un **Pārsūtīšanas pasūtījumi** varat pārskatīt entitījas, kuras izveidotas pasūtījumu rindām izlaišanas uz noliktavu laikā.

- Lapa **Pārdošanas pasūtījumi**:

    - Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktavas** un pēc tam izvēlnē atlasiet **Sūtīšanas informācija**, lai atvērtu saistītos sūtījumus, **Kravu informācija**, lai atvērtu saistītās kravas, vai **Darbu informācija**, lai atvērtu saistīto informāciju par darbu.
    - Kopsavilkuma cilnē **Rindu informācija** atlasiet cilni **Krava**, lai pārskatītu saistītās kravas.

- Lapa **Pārsūtīšanas pasūtījumi**:

    - Darbību rūts cilnē **Sūtīšana** atlasiet **Sūtīšanas informācija**, lai atvērtu saistītos sūtījumus, vai **Kravas informācija**, lai atvērtu saistītās kravas.
    - Kopsavilkuma cilnē **Pārsūtīšanas pasūtījuma rindas** atlasiet **Darba informācija**, lai atvērtu informāciju par saistīto darbu.

Beigās, kad pasūtījums tiek izdots noliktavai, automatizētākā plūsma darbojas šādi:

1. Sistēma izveido pasūtījuma un kopuma sūtījumu.
1. Kopums tiek apstrādāts.
1. Sistēma izveido kravas un darba ID.

Atkarībā no kopumu veidnēm, darba veidnēm un atrašanās vietas direktīvu iestatījumiem, daži šīs plūsmas darbi var kļūt par manuāliem. Taču vispārīgā plūsma paliek nemainīga.

Ir vairākas opcijas, kā varat izlaist pasūtījumu uz noliktavu. Varat darbību veikt manuāli vai varat iestatīt pakešdarbu. Pārējās šī raksta sadaļas detalizēti pārskata dažādus veidus, kā veikt darbības ar noliktavu.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Manuāla izlaišana uz noliktavu no lapām Pārdošanas pasūtījumi un Pārsūtīšanas pasūtījumi

Varat izlaist pasūtījumu uz noliktavu tieši no lapas **Pārdošanas pasūtījumi** vai **Pārsūtīšanas pasūtījumi**, atlasot opciju **Izlaist uz noliktavu**.

- Lapā **Pārdošanas pasūtījumi** poga atrodas Darbību rūts cilnē **Noliktava**.
- Lapā **Pārsūtīšanas pasūtījumi** poga atrodas Darbību rūts cilnē **Sūtīšana**.

No lapas **Pārdošanas pasūtījumi** varat vienlaikus izlaist vairākus pārdošanas pasūtījumus.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Manuāla izlaišana uz noliktavu no lapas Izlaišana uz noliktavu

Pašlaik sistēma nodrošina trīs lapas, kurās varat skatīt rindas vairākiem pasūtījumiem un tās izlaist uz noliktavu:

- **Izlaist uz noliktavu** (**Noliktavu pārvaldība \> Izlaist uz noliktavu \> Izlaist uz noliktavu**) — Šajā lapā varat strādāt gan ar pārdošanas, gan pārsūtīšanas pasūtījumiem. Taču tās veiktspēja ir lēnāka, nekā pārējām divām lapām. Šī lapa drīz būs novecojusi.
- **Izlaist pārdošanas pasūtījumus uz noliktavu** (**Noliktavu pārvaldība \> Izlaist uz noliktavu \> Izlaist pārdošanas pasūtījumus uz noliktavu**) — Šajā lapā varat strādāt tikai ar pārdošanas pasūtījumiem. Taču tās veiktspēja ir labāka, nekā lapai **Izlaist uz noliktavu**.
- **Izlaist pārsūtīšanas pasūtījumus uz noliktavu** (**Noliktavu pārvaldība \> Izlaist uz noliktavu \> Izlaist pārsūtīšanas pasūtījumus uz noliktavu**) — Šajā lapā varat strādāt tikai ar pārsūtīšanas pasūtījumiem. Taču tās veiktspēja ir labāka, nekā lapai **Izlaist uz noliktavu**.

Visām trim lapām ir līdzīgas funkcijas, kā aprakstīts pārējā sadaļā. Ar visām no tām varat atlasīt pasūtījumu rindas vai veselus pasūtījumus un tos izlaist uz noliktavu.

Katrai lapai ir augšdaļa, kurā varat atlasīt pasūtījuma rindas, un apakšdaļa, kurā varat iniciēt izlaišanu uz noliktavu. Varat izmantot filtrus no augšdaļas, lai meklētu tās pārdošanas pasūtījuma rindas, kuras vēlaties izlaist. Lapā **Izlaist uz noliktavu** ir sniegta atsevišķa cilne pārdošanas un pārsūtīšanas pasūtījumiem augšdaļā, bet pārējās divās lapās tiek rādīts tikai viena veida pasūtījums.

Rīkjosla augšdaļā ietver šādas pogas, kuras varat lietot, lai atlasītu pogas, kuras varat lietot, lai atlasītu pasūtījuma rindas, kuras izlaist uz noliktavu:

- **Pievienot** — Atlasiet vienu vai vairākas rindas augšdaļā, un pēc tam atlasiet šo pogu rindām apakšdaļā.
- **Pievienot visas** — Pievienojiet visas rindas no augšdaļas apakšdaļā.
- **Pievienot pasūtījumu** — Atlasiet pasūtījumu, un tad atlasiet šo pogu, lai pievienotu visas rindas no šī pasūtījuma apakšdaļā.

Pēc tam, kad ir pabeigta rindu pievienošana apakšdaļai, atzīmējiet katru rindu, kuru vēlaties izlaist. Pēc tam rīkjoslā atlasiet **Izlaist uz noliktavu**, lai šīs rindas izlaistu uz noliktavu.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Manuāla izlaišana uz noliktavu no lapas Kravas plānošanas rīks

Varat arī manuāli izlaist pasūtījumus uz noliktavu, lietojot lapu **Kravas plānošanas rīks**. Šī lapa ļauj organizēt pasūtījuma rindas kravās un pēc tam izlaist šīs kravas uz noliktavu.

Lai atvērtu lapu **Kravas plānošanas rīks**, dodieties uz **Noliktavas pārvaldība \> Kravas**. Varat to atvērt arī no lapām **Pārdošanas pasūtījumi** un **Pārsūtīšanas pasūtījumi**. Lapas augšdaļā varat atlasīt pārdošanas pasūtījuma rindas cilnē **Pārdošanas rindas** un pārsūtīt pasūtījuma rindas cilnē **Pārsūtīšanas rindas** un pēc tam pievienot šīs rindas jaunai vai esošai kravai.

Darbību rūts cilnē **Piegāde un pieprasījums** ir iekļautas šādas pogas, kuras varat lietot, lai augšdaļā kravai pievienotu pasūtījuma rindas:

- **Uz jaunu kravu** — Atlasiet vienu vai vairākas rindas augšdaļā, un pēc tam atlasiet šo pogu, lai izveidotu jaunu kravu un tai pievienotu rindas.
- **Uz esošu kravu** — Atlasiet vienu vai vairākas rindas augšdaļā, un pēc tam atlasiet šo pogu, lai pievienotu rindas esošai kravai.
- **Viss pasūtījums uz jaunu kravu** — Atlasiet pasūtījumus, un pēc tam atlasiet šo pogu, lai izveidotu jaunu kravu un tai pievienotu visas rindas no šiem pasūtījumiem.
- **Viss pasūtījums uz esošu kravu** — Atlasiet pasūtījumu, un pēc tam atlasiet šo pogu, lai pievienotu rindas no šī pasūtījuma esošai kravai.

Apakšdaļā varat pārskatīt izveidotās kravas. Lai izlaistu kravas uz noliktavu, atlasiet tās un pēc tam atlasiet rīkjoslā **Atlasīt \> Izlaist uz noliktavu**. Ja lietojat automātisko kopumu apstrādi, jo kravas jau ir piešķirtas pasūtījumu rindām, sistēma rada sūtījumus un darba ID, kad tiek veikta izlaišana uz noliktavu.

## <a name="automatic-release-to-the-warehouse"></a>Automātiska izlaišana uz noliktavu

Lai automātiski izlaistu pasūtījumus uz noliktavu, lietojiet uzdevumus **Automātiska pārdošanas pasūtījumu izlaišana** un **Automātiska pārsūtīšanas pasūtījumu izlaišana**.

Lai iestatītu pakešuzdevumu, ar kuru izlaiž pārdošanas pasūtījumus, izpildiet tālāk norādītās darbības.

1. Doties uz **Noliktavu pārvaldība \> Pārvietot uz noliktavu \> Automātiska pārdošanas pasūtījumu nodošana**.
1. Dialoglodziņā **Automātiska pārdošanas pasūtījumu izlaišana** kopsavilkuma cilnē **Parametri** iestatiet šādus laukus:

    - **Izlaižamais daudzums** — Atlasiet, vai uz noliktavu vajadzētu izlaist visu daudzumu vai tikai fiziski rezervēto daudzumu.
    - **Ļaut daļēji izlaistu pasūtījumu izlaišanu** — Norādiet, vai uz noliktavu vajadzētu izlaist atlikušos daļēji izlaisto pasūtījumu daudzumus.
    - **Paturēt rezervācijas izlaišanas kļūmes gadījumā** — Norādiet, vai daudzumus, kuri tika automātiski rezervēti pārdošanas pasūtījumam, ir jāturpina rezervēt, ja izlaišana uz noliktavu neizdodas.
    - **Grupas izpilde pēc debitora** – norādiet, vai sistēmai ir jāapstrādā atsevišķas pārsūtīšanas uz noliktavu operācijas katram debitoram vai jāizlaiž visi pārdošanas pasūtījumi vienlaicīgi. Kad ir iestatīta opcija *Jā*, sistēma apkopos visas pārdošanas pasūtījuma rindas atlasītajam debitoram, izlaiž šos pasūtījumus noliktavā un pēc tam apstrādās nākamo debitoru. Kad šī opcija ir iestatīta uz *Nē*, sistēma izlaiž visas pieejamās pārdošanas pasūtījuma rindas vienā darbības izpildei noliktavā. Iespējojot šo opciju, varat palīdzēt uzlabot izlaišanas uz noliktavas procesu veiktspēju un piederību tām. Tomēr, ja izmantojat šo opciju, kopā ar laidiena veidnēm, kas ir konfigurētas laidieniem, kuri tiek konfigurēti laidieniem, kuri tiek izlaisti nosūtīšanai uz noliktavu, ir jābūt piesardzīgiem, jo šī kombinācija var ģenerēt daudzus viena debitora kopumus, no kuriem katram ir darbs, kas ģenerēts tikai šim debitoram. Ja vēlaties ģenerēt darbu, kas apvieno kravas vairākiem debitoriem, *izslēdziet* opciju Grupas izlaide pēc debitora vai konfigurējiet laidiena veidnes, lai izmantotu atliktu apstrādi.
    - **Bloķēta pasūtījuma apstrāde** — Atlasiet, kā sistēmai vajadzētu apstrādāt pārdošanas pasūtījumus, kuri ir pašlaik ir bloķēti, jo tos rediģē citi lietotāji vai procesi:

        - *Gaidīt uz pasūtījumu atbloķēšanu* — Sistēmai vajadzētu pagaidīt, līdz pasūtījumi tiek atbloķēti, pirms tie tiek izlaisti uz noliktavu. Šajā gadījumā izlaišana uz noliktavu varētu aizņemt vairāk laika.
        - *Izlaist bloķētus pasūtījumus* — Sistēmai vajadzētu izlaist bloķētus pasūtījumus.

    - **Derīgi pasūtījumu veidi** — Atlasiet pārdošanas pasūtījumu veidus, kurus iekļaut paketē.
    - **Kredīta ierobežojuma veids** — Atlasiet, vai kredītlimitu pārbaudes vajadzētu veikt izlaišanas uz noliktavu laikā un, ja pārbaudes ir jāveic, kādu transakciju tajās iekļaut.

1. Lai pārvaldītu, kurus pasūtījumus vajadzētu apstrādāt, kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt**. Tiek atvērts standarta vaicājuma dialoglodziņš, kur varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā tie darbojās citiem Microsoft Dynamics 365 Supply Chain Management vaicājumiem.
1. Kopsavilkuma cilnē **Palaist fonā** atlasiet, vai darbu vajadzētu palaist pakešrežīmā un/vai iestatiet periodisko grafiku. Lauki darbojas tāpat, kā citi [fona darbu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Lai piemērotu iestatījumus un uzsāktu izlaišanu uz noliktavu, atlasiet **Labi**.

Lai iestatītu pakešuzdevumu, ar kuru izlaiž pārsūtīšanas pasūtījumus, izpildiet tālāk norādītās darbības.

1. Doties uz **Noliktavas pārvaldība \> Izdot noliktavai \> Automātiska pārsūtīšanas pasūtījumu izdošana**.
1. Dialoglodziņā **Automātiska pārsūtīšanas pasūtījumu izlaišana** kopsavilkuma cilnē **Parametri** iestatiet šādus laukus:

    - **Izlaižamais daudzums** — Atlasiet, vai uz noliktavu vajadzētu izlaist visu daudzumu vai tikai fiziski rezervēto daudzumu.
    - **Ļaut daļēji izlaistu pasūtījumu izlaišanu** — Norādiet, vai uz noliktavu vajadzētu izlaist atlikušos daļēji izlaisto pasūtījumu daudzumus.
    - **Grupēt izlaišanu pēc mērķa noliktavas** — Norādiet, vai sistēmai vajadzētu izlaist visus pārsūtīšanas pasūtījumus vienlaicīgi, vai tai vajadzētu grupēt pārsūtīšanas pasūtījuma rindas pēc mērķa noliktavas un pēc tam izlaist katru grupu uz noliktavu atsevišķi.

1. Lai pārvaldītu, kurus pasūtījumus vajadzētu apstrādāt, kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt**. Tiek atvērts standarta vaicājuma dialoglodziņš, kur varat definēt atlases kritērijus, kārtošanas kritērijus un savienojumus. Lauki darbojas tāpat, kā tie darbojās citiem Supply Chain Management vaicājumiem.
1. Kopsavilkuma cilnē **Palaist fonā** atlasiet, vai darbu vajadzētu palaist pakešrežīmā un/vai iestatiet periodisko grafiku. Lauki darbojas tāpat, kā citi [fona darbu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Lai piemērotu iestatījumus un uzsāktu izlaišanu uz noliktavu, atlasiet **Labi**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
