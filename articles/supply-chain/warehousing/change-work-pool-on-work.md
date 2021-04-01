---
title: Mainīt darba pūlu darbam
description: Šajā tēmā ir paskaidrots, kā darba vienumiem var izmantot pogu Mainīt darba pūlu, lai mainītu esošā darba pūlu.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 61b988cf2501812e940f726e02d8fc1bcee2c035
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233059"
---
# <a name="change-work-pool-on-work"></a>Mainīt darba pūlu darbam

[!include [banner](../includes/banner.md)]

Darba pūlus var izmantot, lai organizētu darbu grupās. Piemēram, varat izveidot darba pūlu, lai klasificētu noteiktas noliktavas atrašanās vietā notiekošos darbus.

Līdzeklis *Mainīt darba pūlu darbam* pievieno pogu **Mainīt darba pūlu**, kas atrodas darba vienumu darbību rūtī. Tāpēc noliktavu pārvaldnieki var viegli mainīt esošā darba pūlu. Šis līdzeklis ļauj pārvaldniekiem ātri reaģēt uz izmaiņām noliktavas ražotnē, palīdzot uzlabot spēju pielāgoties mainīgajām situācijām un nepieciešamībai pārsūtīt darbu uz citu darba pūlu.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Ieslēgt līdzekli Mainīt darba pūlu darbam

Pirms sākat iestatīt vai izmantot šo līdzekli, ir jāpārliecinās, vai tas ir pieejams jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Mainīt darba pūlu darbam*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Iestatīt līdzekli Mainīt darba pūlu darbam

Lai izmantotu šo līdzekli, ir jābūt iestatītiem darba pūliem. Varat arī iestatīt darba veidnes, lai tās automātiski piešķirtu pūlu. Ja vēlaties strādāt ar piemēra scenāriju, kas ir sniegts tālāk šajā tēmā, iestatiet sistēmu, kā aprakstīts šajā sadaļā.

### <a name="set-up-work-pools"></a>Darba pūlu iestatīšana

Darba pūli ļauj kārtot darba vienumus pēc veida. Lai strādātu ar līdzekli *Mainīt darba pūlu darbam*, ir jābūt pieejamiem vismaz diviem darba pūliem. Veiciet tālāk norādītās darbības, lai skatītu un pievienotu darba pūlus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba pūli**.
1. Ja strādājat ar uzņēmuma **USMF** demonstrācijas datiem un šajā tēmā strādāsiet ar piemēra scenāriju, pievienojiet divus darba pūlus, ar šādiem iestatījumiem:

    - 1. darba pūls:

        - **Darba pūla ID:** *Webshop*
        - **Apraksts:** *Tīmekļa veikals*

    - 2. darba pūls:

        - **Darba pūla ID:** *CallCenter*
        - **Apraksts:** *Zvanu centrs*

1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="set-up-work-templates"></a>Iestatīt darba veidnes

Katrai darba veidnei varat iestatīt noklusējuma darba pūlu, pēc nepieciešamības. Katrai atbilstošajai veidnei ir jāpiešķir darba pūls kolonnā **Darba pūla ID**. Šādā gadījumā visi darba vienumi, kas tiek ģenerēti, izmantojot doto veidni, automātiski pārmanto piešķirto darba pūlu. Ja strādājat ar uzņēmuma **USMF** demonstrācijas datiem un šajā tēmā strādāsiet ar piemēra scenāriju,veiciet tālāk norādītās darbības.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Darbību rūtī atlasiet **Rediģēt**, lai lapu padarītu rediģējamu.
1. Rediģējiet veidni, iestatot šādas vērtības:

    - **Darba veidne:** *62 izdot iepakošanai*
    - **Darba pūla ID:** *Webshop*

1. Atlasiet **Saglabāt**.

## <a name="example-scenario"></a>Piemēra situācija

Šajā scenārijā ir parādīts, kā mainīt pašreizējo darba vienumu apstrādes straumi, mainot to darba pūlu. Tas izmanto uzņēmuma **USMF** demonstrācijas datus un iestatījumus, kas tika ieteikti iepriekš šajā tēmā.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Izveidot pārdošanas pasūtījumu un nodot to noliktavai

1. Apstipriniet, ka rīcībā esošajos krājumos ir pietiekami daudz *A0001* un *A0002* krājumu, noliktavā *62*. Dodieties uz **Krājumu vadība \> Pieprasījumi un pārskati \> Rīcībā esošs** un rediģējiet filtrus, kā norādīts šeit:

    - Vērtība **Noliktava** sākas ar *62*.
    - Vērtība **Krājuma kods** ir vai nu *A001* vai *A002*.

    Katram demonstrācijas datu daudzumam jābūt 10.

    Pēc tam jāizveido pārdošanas pasūtījums.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-007*
    - **Noliktava:** *62*

1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.
1. Jaunais pārdošanas pasūtījums ir atvērts. Tam ir jāietver jauna, tukša rinda režģī kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *2*

1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
1. Aizvērt lapu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Pievienot rindu**, lai pievienotu vēl vienu pārdošanas pasūtījuma rindu. Iestatiet šādas vērtības šai rindai:

    - **Krājuma numurs:** *A0002*
    - **Daudzums:** *2*

1. Izvēlnē **Krājumi** virs režģa atlasiet **Rezervācija**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
1. Aizvērt lapu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.
1. Tiks saņemti informatīvi ziņojumi, kuros būs norādīts no izlaides izveidotais kopuma ID un sūtījuma ID. Pierakstiet kopuma ID.

### <a name="review-the-outbound-wave"></a>Pārskatiet izejošo kopumu

1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
1. Režģī meklējiet kopuma ID, kas tika izveidots no pārdošanas pasūtījuma izlaides.
1. Atlasiet kopuma ID, lai skatītu detalizētu informāciju.
1. Kopsavilkuma cilnē **Kopuma rindas** pārliecinieties, ka pārdošanas pasūtījumam ir norādīts sūtījuma ID.

    > [!TIP]
    > Ja sūtījuma kopuma veidnes iestatījumos opcija **Apstrādāt kopumu, to pārvietojot uz noliktavu** ir iestatīta uz *Nē*, kopums ir jāapstrādā manuāli, darbību rūtī atlasot **Apstrādāt** no cilnes **Kopums**, lai izveidotu darbu.

1. Pārliecinieties, vai kopums ir apstrādāts. Šī apstrāde izveido nepieciešamo darbu.

### <a name="view-work-details-and-change-the-work-pool"></a>Skatīt detalizētu informāciju par darbu un mainīt darba pūlu

Varat izmantot lapu **Detalizēta informācija par darbu**, lai skatītu izveidoto darbu un pārvaldītu darba pūlu.

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Atlasiet tikko izveidotā darba rindu. Kolonnā **Pasūtījuma numurs** tiks parādīts pārdošanas pasūtījuma numurs.

    Lauks **Darba pūla ID** tiks iestatīts uz darba veidnē iestatīto darba pūla ID.

    > [!TIP]
    > Ja nav redzams lauks **Darba pūla ID**, pievienojiet kolonnu režģim un pēc tam atsvaidziniet lapu.

1. Lai mainītu darba pūlu, kas ir saistīta ar darba ID, darbību rūts cilnē **Darbs** atlasiet **Mainīt darba pūla ID**.
1. Dialoglodziņā **Mainīt darba pūlu**, kopsavilkuma cilnes **Parametri** laukā **Darba pūla ID** atlasiet *CallCenter*.
1. Atlasiet **Labi**, lai piemērotu izmaiņas.
1. Ievērojiet, ka lauka **Darba pūla ID** vērtība tagad ir nomainīta uz *CallCenter*.

> [!IMPORTANT]
> Kad tiek parādīts dialoglodziņš **Mainīt darba pūlu**, lauks **Darba pūla ID** var būt tukšs pēc noklusējuma. Ja lauks ir tukšs, kad atlasāt **Labi**, lai piemērotu izmaiņas, darba pūls tiks pilnībā noņemts no darba.
>
> Papildus darba pūlu pārslēgšanai šo procedūru var izmantot, lai pievienotu darba pūlu jebkuram darba vienumam, kuram nav darba pūla, vai noņemtu darba pūlu no jebkura darba vienuma, kuram tāds ir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]