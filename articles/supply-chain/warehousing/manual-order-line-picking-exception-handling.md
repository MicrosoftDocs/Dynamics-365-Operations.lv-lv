---
title: Manuāli apstrādāt pārdošanas un pārsūtīšanas rindu izdošanas izņēmumus
description: Šajā rakstā aprakstīts, kā administratori var manuāli izdot (vai anulēt) krājumu darbības, lai novērstu problēmas, kas rodas bojātu pārdošanas un pārsūtīšanas pasūtījumu datus.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404429"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Manuāli apstrādāt pārdošanas un pārsūtīšanas rindu izdošanas izņēmumus

[!include [banner](../includes/banner.md)]

Manuāla pārdošanas un pārsūtīšanas rindu izdošanas izņēmumu apstrāde ļauj administratoriem labot problēmas, ko radījuši bojāti pārdošanas un pārsūtīšanas pasūtījumu dati. Tas ļauj uzticamiem lietotājiem manuāli izdot (vai anulēt izdošanu) krājumu darbības, kas ir saistītas ar pārdošanas un pārsūtīšanas pasūtījumu rindām, kamēr noliktavas procesi jau notiek.

Šeit aprakstīto funkcionalitāti vajadzētu izmantot tikai gadījumos, kad sistēma nevar pabeigt noliktavas procesu steka apstrādi parastā veidā. Pēc noklusējuma to var lietot tikai lietotāji ar sistēmas administratora lomu. Tomēr varat tai piešķirt piekļuvi, piešķirot manuāli pārdošanas *rindu privilēģiju Izdot pārdošanas rindas* citām lomām pēc pieprasījuma.

## <a name="turn-on-this-feature-for-your-system"></a>Līdzekļa ieslēgšana sistēmā

Pirms varat izmantot šajā rakstā aprakstītos līdzekļus, tiem ir jābūt ieslēgtiem jūsu sistēmā. Administratori var izmantot līdzekļu [pārvaldības iestatījumus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai pārbaudītu līdzekļu statusu un ieslēgtu tos. Līdzekļu pārvaldības **darbvietā** līdzekļi ir uzskaitīti, izmantojot šādus nosaukumus:

- *Manuālās pārdošanas rindas izdošanas pakalpojums administratoram vai līdzīgiem uzticamiem lietotājiem*<br>(No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir obligāta un to nevar izslēgt.)
- *Manuālās pārsūtīšanas rindas izdošanas pakalpojums administratoram vai līdzīgiem uzticamiem lietotājiem*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Labot darbības, kas saistītas ar pārdošanas vai pārsūtīšanas pasūtījuma rindām

Izmantojiet šo procedūru, lai labotu darbības, kas saistītas ar pārdošanas vai pārsūtīšanas pasūtījuma rindām.

1. Veiciet vienu no tālāk minētajām darbībām atkarībā no labojamā pasūtījuma tipa:

    - Lai labotu ar pārdošanas pasūtījumu saistīto darbību, pārejiet uz sadaļu **\>\>\> Noliktavas pārvaldības periodiskie uzdevumi Manuāla pārdošanas rindas izvēle.**
    - Lai labotu ar pārsūtīšanas pasūtījumu saistīto darbību, pārejiet uz sadaļu **\>\> Noliktavas pārvaldības periodiskie uzdevumi Manuāla izdošanas \> pārsūtīšanas rindu tīrīšana.**

1. **Lapā Izdot pārdošanas rindas** **manuāli** vai Manuāli izvēlēties pārsūtīšanas rindas izmantojiet filtrus režģa augšpusē, lai atrastu meklēto rindu, un pēc tam augšējā režģī atlasiet mērķa pasūtījuma rindu.
1. Lai skatītu **papildinformāciju** par atlasīto rindu **,** **·** **izmantojiet apakšējā sadaļā lietojiet cilnes Krājumu darbības,** Noslodzes rindas, Darba rindas un Konteinera rindas. Informācija šajās cilnēs sniedz pamata apskatu par saistītajiem noliktavas procesiem un to statusiem.
1. Darbību rūtī atlasiet **Izdot**, lai atvērtu atlasīto pasūtījuma rindu lapā **Izdot** krājumu darbībām. Šo soli var veikt pat pasūtījuma rindām, kas jau ir nodotas izpildei noliktavā. (Parasti pasūtījuma rindas, kas ir izlaistas nosūtīšanai uz noliktavu, nevar atvērt **Izdošanas** lapa.)

    > [!NOTE]
    > Atverot lapu Izdot, varat saņemt dažādus **brīdinājumus**. Rīkojieties saskaņā ar šiem brīdinājumiem. Piemēram, varat saņemt brīdinājumu par pasūtījuma rindām, kas saistītas ar noliktavas darbu. Šādā gadījumā ir nozīme mēģināt atcelt [darbu](cancel-warehouse-work.md), pirms manuālas labošanas ir ieteicams atcelt darbu, izmantojot standarta atcelšanas darba funkcionalitāti.

1. Atlasiet rindu režģī **Darbības** un pēc tam darbību rīkjoslā **atlasiet** Pievienot **izdošanas** rindu.
1. Atlasītā rinda tiek pārvietota uz izdošanas **rindu režģi**. Iestatiet atbilstošās vērtības visām kolonnām, kurām trūkst nepieciešamās informācijas. (Piemēram, norādiet novietojumu un noliktavas vienību, no kuras krājums jāizņem/jāizņem.)
1. Izdošanas **rindu rīkjoslā** atlasiet **Apstiprināt izdošanu**.

## <a name="correct-load-line-quantities"></a>Labot noslodzes rindas daudzumus

Lai labotu noslodzes rindas daudzumu, izmantojiet tālāk norādītās darbības.

1. Veiciet vienu no tālāk minētajām darbībām atkarībā no labojamā pasūtījuma tipa:

    - Lai labotu ar pārdošanas pasūtījumu saistīto darbību, pārejiet uz sadaļu **\>\>\> Noliktavas pārvaldības periodiskie uzdevumi Manuāla pārdošanas rindas izvēle.**
    - Lai labotu ar pārsūtīšanas pasūtījumu saistīto darbību, pārejiet uz sadaļu **\>\> Noliktavas pārvaldības periodiskie uzdevumi Manuāla izdošanas \> pārsūtīšanas rindu tīrīšana.**

1. **Lapā Izdot pārdošanas rindas** **manuāli** vai Manuāli izvēlēties pārsūtīšanas rindas izmantojiet filtrus režģa augšpusē, lai atrastu meklēto rindu, un pēc tam augšējā režģī atlasiet mērķa pasūtījuma rindu.
1. **Apakšējās sadaļas** cilnē Kravas rindas manuāli **atlasiet Labošanas kravas rindas** rīkjoslā.
1. Lapā Pareizās **noslodzes rindas manuāli** **režģī** Krājumu transakcijas pārskatiet krājumu darbības, kas ir saistītas ar atlasīto noslodzes rindu.
1. Ja nepieciešams, labojiet noslodzes rindas daudzumus šādās kolonnās:

    - **Darba izveidotais daudzums**
    - **Izdotais daudzums**
    - **Plānotais daudzums pārkraušanai sadales centrā**

    Sistēma validēs jebkuras izmaiņas, ko veicāt šajās kolonnās.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
