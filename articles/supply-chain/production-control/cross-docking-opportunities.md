---
title: Pārkraušana sadales centrā no ražošanas pasūtījumiem uz izejošajiem sadales centriem
description: Šajā tēmā ir aprakstīts, kā pārvaldīt materiāla pārkraušanu sadales centrā, kad ražošanas līnijā tiek reģistrēta materiāla pabeigšana un tas tiek pārvietots uz izejošās plūsmas transportēšanas sadales centru.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockOpportunityPolicy, WHSReservationHierarchy, WHSInventTableReservationHierarchy, WHSItemGroupLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d2f264564f627889d89444a7423179de0c6d4d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246289"
---
# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Pārkraušana sadales centrā no ražošanas pasūtījumiem uz izejošajiem sadales centriem

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pārvaldīt materiāla pārkraušanu sadales centrā, kad ražošanas līnijā tiek reģistrēta materiāla pabeigšana un tas tiek pārvietots uz izejošās plūsmas transportēšanas sadales centru.

<a name="introduction"></a>Ievads
------------

Pārkraušana sadales centrā no ražošanas novietojuma uz izejošās plūsmas novietojumu ir noderīga ražotājiem, kuri saražo lielu preču daudzumu un vēlas nosūtīt preces, tiklīdz ražošanas līnijās tiek reģistrēta to pabeigšana. Mērķis ir nosūtīt preces uz sadales centriem, kas atrodas fiziski tuvu debitoru pieprasījuma vietai, nevis veidot krājumus ražošanas vietā.

Ja nav tūlītēja preces pieprasījuma, tā ir jānovieto noliktavas novietojumos ražošanas vietā. Šis process tiek dēvēts arī par *iespējām atbilstošu pārkraušanu sadales centrā*, kas nozīmē, ka gadījumā, ja ir saņemts preces nosūtīšanas pieprasījums, ir jāizmanto šī iespēja, nevis jāpārvieto prece uz iekšējo noliktavu.

Tālāk sniegtajā piemērā ir aprakstītas trīs ražošanas līnijas galā (2) sāktas plūsmas versijas.

Tiek reģistrēta preces pabeigšana, tā tiek pārvietota uz ražošanas izejas plūsmas vietu (3), un autoiekrāvēja vadītājs paņem paleti šajā vietā (3).

-   Ja pastāv plānota aktivitāte (6) preces pārvietošanai no ražošanas vietas (1) uz sadales centru (7), sistēma sniedz kravas automašīnas vadītājam norādījumus novietot paleti vietā pie angāra durvīm (4).
-   Ja angāra durvīm jau ir piešķirta piekabe, kravas automašīnas vadītājs saņem norādījumus uzreiz iekraut preci piekabē.
-   Ja nepastāv plānota aktivitāte preces pārvietošanai, autoiekrāvēja vadītājs saņem norādījumus novietot preci kādā vietā iekšējā noliktavā (5).

[![opportunistic cross-docking](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Pārkraušanas sadales centrā konfigurēšana
Pārkraušanu sadales centrā var konfigurēt, izmantojot **darba politikas**. Darba politikā ir ietverts darba pasūtījuma veids, novietojums un prece. Tālāk esošajā piemērā ir konfigurēta preces X pārkraušana sadales centrā uz novietojumu Y.

#### <a name="work-order-types"></a>Darba pasūtījumu veidi

-   Darba pasūtījuma veids: Pabeigto preču izvietošana
-   Darba izveidošanas metode: Pārkraušana sadales centrā
-   Pārkraušanas sadales centrā politikas nosaukums: Pārsūtīšanas pasūtījumi

#### <a name="inventory-locations"></a>Krājumu vietas

-   Noliktava: 51
-   Novietojums: Y

#### <a name="products"></a>Preces

-   Krājuma numurs: X

Pašlaik pārkraušanu sadales centrā var konfigurēt tikai darba pasūtījumu veidiem, kas ir norādīti tālāk.

-   Pabeigto preču izvietošana
-   Līdzproduktu un blakusproduktu izvietošana

**Politikas pārkraušanai sadales centrā** ietvaros varat definēt dokumentu veidus, kas attiecas uz pārkraušanu sadales centrā. Pašlaik vienīgais atbalstītais dokumenta veids ir **pārsūtīšanas pasūtījumi**. Tālāk esošajā piemērā ir parādīta politikas pārkraušanai sadales centrā konfigurācija.

### <a name="cross-docking-policy-name-transfer-order"></a>Politikas pārkraušanai sadales centrā nosaukums: Pārsūtīšanas pasūtījums

- Sērijas numurs: 10
  -   Darba pasūtījuma veids: Pārsūtīt izejas plūsmu
- Pārkraušanas sadales centrā pieprasījumam ir nepieciešama vieta: Aplams
- Stratēģija pārkraušanai sadales centrā: Datums un laiks

### <a name="sequence-number"></a>Sērijas numurs

**Sērijas numurs** norāda dokumenta veida prioritāti. Pašlaik tiek atbalstīts tikai veids **Pārsūtīt izejas plūsmu**. Tāpēc sērijas numurs kļūs noderīgs tikai tad, kad tiks atbalstīts vairāk darba pasūtījumu veidu.

### <a name="cross-docking-policy"></a>Politika pārkraušanai sadales centrā

Politika pārkraušanai sadales centrā nodrošina arī prioritātes noteikšanas un pārsūtīšanas pasūtījumu pieprasījuma politikas iestatīšanu. Piemēram, ja pastāv vairāki vienas preces pārsūtīšanas pasūtījumi, pasūtījumu prioritāte tiek noteikta, pamatojoties uz kravai iestatīto un ar pārsūtīšanas pasūtījumu saistīto plānoto datumu un laiku. Plānoto datumu un laiku var tieši iestatīt kravai, vai arī tos iestatīt ar kravu saistītajam **norīkojumu grafikam**. Prioritātes noteikšana ir atkarīga no stratēģijas pārkraušanai sadales centrā. Pašlaik ir pieejama tikai viena stratēģija: **Datums un laiks**.

### <a name="cross-docking-demand-requires-location"></a>Pieprasījumam par pārkraušanu sadales centrā ir nepieciešams novietojums

Politikas pārkraušanai sadales centrā ietvaros varat iestatīt kritēriju, lai noteiktu, ka pārkraušanai sadales centrā ir piemēroti tikai tie pārsūtīšanas pasūtījumi, kuriem ir piesaistīts novietojums. Šo kritēriju var iestatīt, izmantojot lauku **Pieprasījumam par pārkraušanu sadales centrā ir nepieciešams novietojums**. Kā sadales centrā pārkrauto preču beigu novietojums tiek izmantots ar kravu saistītajā norīkojumu grafikā norādītais novietojums. Sadales centrā pārkrauto preču beigu novietojums ir atkarīgs no darba pasūtījuma veida **Izvietot** novietojuma direktīvas **Pārsūtīt izejas plūsmu**. Lauka **Pieprasījumam par pārkraušanu sadales centrā ir nepieciešams novietojums** iestatīšana var būt noderīga gadījumā, ja pabeigtās preces ir jāpārkrauj sadales centrā tikai tad, ja angāra durvīm ir piešķirta piekabe. Šādā gadījumā preces tiek tieši pārvietotas no ražošanas līnijas uz piekabi. Ja angāra durvīm ir piešķirta piekabe, lietotājs piešķir novietojumu norīkojumu grafikam un tādējādi padara novietojumu pieejamu pārkraušanai sadales centrā. Tālāk esošajās sadaļās ir detalizēti aprakstīti divi piemēri.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>1. gadījums — pārkraušana sadales centrā no ražošanas uz pārsūtīšanas pasūtījumiem

Pēc preces pabeigšanas reģistrēšanas ražošanas līnijā prece tiek pārvietota uz angāra durvju novietojumu, kur tā tiek iekrauta kravas automašīnā, un pēc tam prece tiek pārvietota uz sadales centru. Izmantot uzņēmuma USMF.

1.  Iespējojiet jaunu numuru sēriju pārkraušanai sadales centrā. Pārejiet uz labu **Numuru sērijas** un atlasiet pogu **Ģenerēt**. Vednis palīdzēs jums veikt vajadzīgo procesu.
2.  Izveidojiet politiku pārkraušanai sadales centrā. Pārejiet uz lapu **Politika pārkraušanai sadales centrā** un izveidojiet jaunu politiku ar nosaukumu **Pārkraušana sadales centrā uz pārsūtīšanas pasūtījumu**. Ņemiet vērā, ka vienīgais darba veids, ko varat atlasīt, ir **Pārsūtīt izejas plūsmu** un vienīgā pieejamā stratēģija pārkraušanai sadales centrā ir **Datums un laiks**.
3.  Izveidojiet darba politiku. Pārejiet uz lapu **Darba politikas** un izveidojiet jaunu darba politiku ar nosaukumu **Pārkraušana sadales centrā L0101**.
4.  Iestatiet kravas tā, lai tās tiktu automātiski izveidotas pārsūtīšanas pasūtījumiem. Izmantojot noliktavas parametrus, iestatiet kravas tā, lai tās tiktu automātiski aprēķinātas, kad tiek izveidoti pārsūtīšanas pasūtījumi. Krava ir viens no priekšnoteikumiem, kas ir nepieciešams, lai pārsūtīšanas pasūtījumam varētu veikt pārkraušanu sadales centrā.
5.  iestatiet krājumu kravas kartēšanu. Pārejiet uz lapu **Krājumu kravas kartēšana** un iestatiet krājumu grupas **CarAudio** standarta kravas veidni. Šī kartēšana nodrošina kravas veidnes automātisku izmantošanu kravai, kad tiek izveidots pārsūtīšanas pasūtījums.
6.  Izveidojiet pārsūtīšanas pasūtījumu. Izveidojiet krājuma Nr. L0101 pārsūtīšanas pasūtījumu. Daudzums = 20.
7.  Nododiet pārsūtīšanas pasūtījumu izpildei, izmantojot kravu plānošanas rīku. Cilnē **Nosūtīt** atlasiet kravu plānošanas rīka izvēlnes vienumu un kravas rindas izvēlne **Nodot izpildei** atlasiet opciju **Pārvietot uz noliktavu**. Tagad pārsūtīšanas pasūtījumam ir atvērta veida **Pārsūtīt izejas plūsmu** kopuma rinda.
8.  Izveidojiet ražošanas pasūtījumu. Pārejiet uz saraksta lapu **Ražošanas pasūtījums** un izveidojiet preces L0101 ražošanas pasūtījumu. Daudzums = 20. Novērtējiet ražošanas pasūtījumu un sāciet tā izpildi. Ņemiet vērā, ka lauka **Grāmatot izdošanas sarakstu tagad** vērtība ir **Nē**.
9.  Reģistrējiet pabeigšanu, izmantojot mobilo ierīci. Pārejiet uz mobilo ierīču portālu un atlasiet izvēlnes vienumu **Reģistrēt pabeigšanu un izvietot**. Tagad reģistrējiet preces L0101 pabeigšanu, izmantojot rokas ierīci. Daudzums = 10. Ņemiet vērā, ka izvietošanas novietojums ir **BAYDOOR**. Šis novietojums ir iegūts no darba pasūtījuma veida **Izvietot** novietojuma direktīvas **Pārsūtīt izejas plūsmu**. Pievērsiet uzmanību arī tam, ka ir izveidots un pabeigts veida **Pārsūtīt izejas plūsmu** darbs. Pārejiet uz detalizētu informāciju par pārsūtīšanas pasūtījuma darbu, lai pārbaudītu darba izpildi.
10. Tagad ziņojiet par papildu 10 gabaliem no mobilās ierīces. Ņemiet vērā, ka izvietošanas novietojums atkal ir **BAYDOOR**. Pievērsiet uzmanību arī tam, ka šiem 10 gabaliem ir izveidots jauns darbs ar veidu **Pārsūtīt izejas plūsmu**.
11. Tagad mēģiniet sākt vēl 20 gabalu ražošanu ražošanas pasūtījumā un pēc tam mēģiniet reģistrēt 20 gabalu pabeigšanu, izmantojot rokas ierīci. Šoreiz kā izvietošanas novietojums tiek piedāvāts novietojums **LP-001**. Šis novietojums ir iegūts no novietojuma direktīvas **Pabeigto preču izvietošana**. Šī novietojuma direktīva tiek izmantota, jo nepastāv neviena iespēja pārkraušanai sadales centrā. Preces LP-001 pārsūtīšanas pasūtījums tika pilnībā izpildīts, veicot divas pārkraušanas sadales centrā aktivitātes 9. un 10. darbībā. Ņemiet vērā, ka tika izveidots un apstrādāts darbs ar veidu **Pabeigto preču izvietošana**.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>2. gadījums — pārkraušana sadales centrā no ražošanas uz pārsūtīšanas pasūtījumiem, izmantojot norīkojumu grafiku

Pēc preces pabeigšanas reģistrēšanas ražošanas līnijā prece tiek pārvietota uz vietu pie angāra durvīm, kas ir norādīta vietu pie angāra durvīm norīkojumu grafikā. Izmantot uzņēmuma USMF.

1.  Mainiet politiku pārkraušanai sadales centrā. Mainiet 1. gadījuma ietvaros izveidoto politiku pārkraušanai sadales centrā, atzīmējot izvēles rūtiņu **Pieprasījumam par pārkraušanu sadales centrā ir nepieciešams novietojums**.
2.  Izveidojiet jaunu pārsūtīšanas pasūtījumu.
3.  Atveriet **kravu plānošanas rīku**.
4.  Kravu plānošanas rīkā pārejiet uz sadaļu **Kravas** un izvēlnē **Transportēšana** atlasiet opciju **Norīkojumu grafiks**, lai izveidotu jaunu norīkojumu grafiku. Ņemiet vērā, ka norīkojumu grafikā ir ietverta atsauce uz pārsūtīšanas pasūtījumu laukā **Pasūtījuma numurs**. Laukā **Plānotais sākuma datums/laiks novietojumā** varat iestatīt norīkojuma datumu un laiku. Šis datums un laiks tiek izmantots, nosakot pieprasījuma par pārkraušanu sadales centrā prioritāti pārkraušanas procesa laikā. Šajā laukā iestatītais datums un laiks tiek izmantoti, lai atjauninātu atbilstošās kravas lauka **Plānotās kravas nosūtīšanas datums un laiks** vērtību. Kopsavilkuma cilnē **Detalizēta nosūtīšanas informācija** norādītais novietojums ir novietojums, uz kuru tiek nosūtīts pārsūtīšanas pasūtījums.
5.  **Kravu plānošanas rīkā** nododiet kravu pārvietošanai uz noliktavu.
6.  Izveidojiet krājuma Nr. **L0101** ražošanas pasūtījumu un iestatiet tā statusu **Sākts**, norādot daudzumu 20.
7.  Reģistrējiet pabeigšanu, izmantojot mobilo ierīci.
8.  Pārejiet uz mobilo ierīču portālu un atlasiet izvēlnes vienumu **Reģistrēt pabeigšanu un izvietot**.
9.  Reģistrējiet krājuma Nr. **L0101** pabeigšanu, izmantojot rokas ierīci. Ņemiet vērā, ka izvietošanas novietojums tagad ir **BAYDOOR 2**. Šis novietojums ir iegūts no norīkojumu grafika, nevis novietojuma direktīvas **Pārsūtīšanas saņemšana**.

### <a name="additional-information"></a>Papildinformācija

-   Pārkraušana sadales centrā tiek atbalstīta gan ar partijas, gan ar sērijas numuru kontrolētiem krājumiem, kam partijas un sērijas numura dimensijas ir definētas virs un zem novietojuma rezervācijas hierarhijā. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]