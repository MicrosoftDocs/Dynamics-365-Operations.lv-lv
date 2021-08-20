---
title: Kopuma izpildes paziņojumi
description: Šajā tēmā ir aprakstīti kopuma izpildes paziņojumi un paskaidrots, kā tos iestatīt.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 26810f6e21f9c8ba6e92621a8e1ddee17837b6048107b961afb0e428059051af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752588"
---
# <a name="wave-execution-notifications"></a>Kopuma izpildes paziņojumi

[!include [banner](../includes/banner.md)]

*Kopuma izpildes paziņojumu* līdzeklis izmanto biznesa notikumus un darbību centru, lai piegādātu paziņojumus, kas saistīti ar kopuma izpildi. Tas ļauj norādīt notikumu tipus, kas ģenerē paziņojumus, noliktavas, kas tos ģenerē, un lietotājus, kuri tos saņem.

Navigācijas joslas labajā pusē esošā poga **Rādīt ziņojumus** (zvana simbolu) norāda, kad pašreizējam lietotājam ir pieejams darbību centra ziņojums. Lietotājs var atlasīt pogu **Rādīt ziņojumus**, lai atvērtu darbību centru un pārskatītu ziņojumus.

Biznesa notikumi rodas, kad tiek darbināti biznesa procesi. Biznesa procesus veido uzdevumi. Biznesa procesa laikā lietotāji, kas piedalās tajā, veic biznesa darbības, lai veiktu šos uzdevumus. Biznesa notikumi nodrošina mehānismu, kas ļauj ārējām sistēmām saņemt paziņojumus no Finance and Operations programmām. Šādā veidā sistēma var veikt biznesa darbības, atbildot uz biznesa notikumiem. Plašāku informāciju skatiet [Brīdinājumi kā biznesa notikumi](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-on-the-wave-execution-notifications-feature"></a>Līdzekļa Kopuma izpildes paziņojumu ieslēgšana

Lai varētu izmantot līdzekli *Kopuma izpildes paziņojumi*, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Kopuma izpildes paziņojumi*

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Scenārijs: sūtīt kopuma partijas izpildes paziņojumus darbību centram

Šajā scenārijā ir parādīta beigu plūsma paziņojumu par kopuma partijas izpildes kļūdu nosūtīšanai uz noteiktu lomu, izmantojot darbību centru.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Pārliecinieties, vai kopumi ir palaisti partijas režīmā

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.
1. Kopsavilkuma cilnē **Kopuma apstrāde** iestatiet opciju **Kopuma apstrādi partijās** uz *Jā*.

> [!NOTE]
> Ja vēlaties atspējot kopuma partijas izpildes paziņojumus, iestatiet opciju **Atspējot kopuma apstrādes partijas paziņojumus** uz *Jā*.

### <a name="configure-a-wave-notification-policy"></a>Konfigurēt kopuma paziņojuma politiku

Kopuma paziņojumu politikas definē sūtīto paziņojumu veidus un lietotājus, kuriem tiek sūtīts paziņojums.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma paziņojumu politikas**.
1. Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Kopuma paziņojumu politika:** *24BatchError*
    - **Apraksts:** *Noliktavas 24 kopuma partijas kļūda*
    - **Sūtīt paziņojumu par:** *Tikai kļūda*
    - **Lomai:** *Sistēmas administrators*

        > [!NOTE]
        > Tā kā šajā scenārijā tiek izmantoti demonstrācijas dati, tiek atlasīta loma *Sistēmas administrators*, kas ir gadījumam. Tādēļ, tā kā esat pieteicies kā sistēmas administrators, saņemsit paziņojumus. Tomēr praksē parasti ir jāatlasa precīzāka loma, lai paziņotu par kopuma paketes izpildes kļūdām, piemēram, *Noliktavas pārvaldnieks*.

1. Darbību rūtī atlasiet **Saglabāt**.

### <a name="configure-a-wave-template"></a>Konfigurēt kopuma veidni

Kopuma veidnes ļauj saistīt noteiktas kopuma metodes ar atbilstošo kopuma etiķešu veidni.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma veidnes**.
1. Saraksta rūtī iestatiet **Kopuma veidnes tipa** lauku uz *Nosūtīšana* un pēc tam atlasiet *24 nosūtīšanas noklusējuma* kopuma veidni noliktavai 24.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Kopuma paziņojumu politika** uz *24BatchError*.

### <a name="configure-a-work-template"></a>Konfigurēt darba veidni

Darba veidnes tiek izmantotas kopuma izpildes laikā, lai ģenerētu darbu. Šajā scenārijā kopuma izpildei ir jāaktivizē kļūda. Iestatot darba veidnes vaicājumu izmantot neesošu noliktavu, jūs nodrošināt, ka kopuma izpilde neizdodas un tādēļ nosūta paziņojumu.

1. Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.
1. Saraksta rūtī iestatiet **Kopuma veidnes tipa** lauku uz *Pārdošanas pasūtījumi* un pēc tam atlasiet *24 SO Stage* darba veidni noliktavai 24.
1. Darbību rūtī atlasiet **Rediģēt vaicājumu**.
1. Vaicājumu redaktora dialoglodziņā cilnē **Diapazons** rediģējiet tālāk norādīto rindu (vai pievienojiet to, ja tāda nav):

    - **Tabula:** *Pagaidu darba darbības*
    - **Atveidotā tabula:** *Pagaidu darba darbības*
    - **Lauks:** *Noliktava*
    - **Kritēriji:** Mainīt vērtību no *24* uz *Kļūda*.

1. Atlasiet **Labi** un apstipriniet izmaiņas.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Izveidot pārdošanas pasūtījumu un nodot to noliktavai

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.
1. Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *24*

1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet otru rindu, kurai ir šādi iestatījumi:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *10*

    > [!NOTE]
    > Šie krājumi un daudzumi ir tikai piemēri. Krājumiem ir jābūt pietiekamiem norādītajā noliktavā.

1. Kamēr jaunā pasūtījuma rinda joprojām ir atlasīta, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**, atlasiet rīkjoslā **Krājumi \> Rezervācija**.
1. Lapā **Rezervācija** darbību rūtī atlasiet **Rezervēt vietu**. Tad aizveriet lapu.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

### <a name="notifications-from-wave-batch-job-execution"></a>Paziņojumi no kopuma pakešuzdevuma izpildes

Atkarībā no biznesa notikumu iestatījuma, jūs visbeidzot saņemsiet paziņojumu par kopuma izpildes kļūmi. Darbību centra ziņojums līdzīgs šim piemēram un ietvers saiti uz kopumu, kas neizdevās.

> **Kopuma izpildes laikā radās kļūda**  
> Radās kļūda, izpildot kopumu USMF-000000001.  
> Pēdējie ziņojumi: kopumam USMF-000000001 netika izveidoti -000000001.
>
> **Statuss**  
> Aktīvie
>
> Atvērt kopuma detalizēto informāciju

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
