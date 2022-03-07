---
title: Materiālu patēriņa reģistrēšana, izmantojot mobilo ierīci
description: Šajā tēmā ir aprakstītas darbplūsmas, kas ļauj reģistrēt izejmateriālu patēriņu ražošanas procesā, izmantojot rokas ierīci.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abc8607e5c3c6ab63a3878b92072bde2ebb0216c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814540"
---
# <a name="register-material-consumption-using-a-mobile-device"></a>Materiālu patēriņa reģistrēšana, izmantojot mobilo ierīci

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas darbplūsmas, kas ļauj reģistrēt izejmateriālu patēriņu ražošanas procesā, izmantojot rokas ierīci.

<a name="introduction"></a>Ievads
------------

Šī darbplūsma ir jāizmanto tad, ja ir obligāti nepieciešams nodrošināt materiālu izsekojamību. Šādos gadījumos, lai uzturētu materiālu izsekojamību, jāziņo par precīzu patēriņam paredzēto laiku un daudzumu. Šo procesu var redzēt pretēji sākotnējām vai atgriezeniskajām norakstīšanas operācijām, ja pastāv nobīde starp reģistrācijas laiku un laiku, kad notiek faktiskais patēriņš. Tas izskaidro, kāpēc automātiskā patēriņa stratēģiju nevar izmantot dažiem materiāliem ar izsekojamības prasībām. Tālāk ir sniegts vienkāršs scenārijs, kurā ir paskaidrots, kā iestatīt darbplūsmu, lai iespējotu izejmateriālu patēriņa reģistrāciju ražošanas vajadzībām, izmantojot rokas ierīci. [![Darbplūsmas iestatīšana, lai iespējotu izejmateriālu patēriņa reģistrēšanu, izmantojot rokas ierīci](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Detalizēta informācija par scenāriju

Nepārtrauktā ražošanas procesā (5) tiek patērēts no partijas atkarīgs izejmateriāls RM-100. Materiāls ir rīcībā esošos atrašanās vietā Bulk-001 (1) ar noliktavas vienību PL-1 un divām partijām B1 un B2, abās ar daudzumu 100 mārciņas. RM 100 noliktavas darbs (2) tiek izlaists un apstrādāts, un materiāli tiek izdoti no Bulk-001 ražošanas ievades atrašanās vietā PIL-01 (3), kas tiek definēta kā no noliktavas vienības neatkarīga. Mašīnu operators nosver materiālus no ražošanas ievades atrašanās vieta (3) un reģistrē svaru un partijas numuru kā patērētu (4). No ražošanas ievades vietas daļu materiālu manuāli pievieno ražošanas procesam noteiktajos laika intervālos. Kad mašīnas operators pievieno materiālu, tas tiek novērtēts uz svariem, un tiek reģistrēts partijas numurs.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Darbplūsmas iestatīšana, lai reģistrētu patēriņu, izmantojot rokas ierīci
Izveidojiet pabeigtu derīgu preci FG-100 ar materiālu komplektu, kurā ir ietverts no partijas atkarīgais izejmateriāls RM-100. Pievienojiet divas izejmateriāla RM-100 partijas B1 un B2 ar daudzumu 100 vietai Bulk-001 noliktavas vienīb­ā PL-1. Materiālu komplekta rindā esošais tīrīšanas princips attiecībā uz RM-100 tiek iestatīts uz **Manuāls**. Iestatiet ražošanas ievades vietu PIL-01. To var izdarīt, atlasot šo atrašanās vietu kā noklusējuma ražošanas ievades vietu noliktavā 51.

1.  Jaunas mobilās ierīces izvēlnes elementa izveide: 

-    **Izvēlnes vienuma nosaukums** — reģistrēt materiālu patēriņu. 
-    **Virsraksts** — reģistrē materiālu patēriņu. 
-    **Režīms** — netiešs. 
-    **Aktivitātes kods** — reģistrēt materiālu patēriņu.

2.  Pievienojiet izvēlnes elementu ierīces izvēlnei **Mobilā ražošana**.
3.  Izveidojiet ražošanas pasūtījumu galaproduktam: 

-    **Krājuma numurs** — FG-100 
-    **Vieta** — 5 
-    **Noliktava** — 51 
-    **Daudzums** — 150

Ražošanas pasūtījums ir **Novērtēts** un **Izlaists** un noliktavas darbs tiek izveidots.

4.  Pabeidziet darbu, izmantojot izejmateriālu izdošanas rokas ierīcei darbplūsmu.

Tas izdos materiālu no lielapjoma atrašanās vietas uz ražošanas ievades vietu PIL-01. Kad darbs ir pabeigts, materiāla statuss ir **Izdots ražošanas ievades vietā**. Statuss pēc darba apstrādes var būt vai nu **Izdots** vai **Rezervēts fiziski**. Tas ir konfigurēta ar parametru **Izejas plūsmas statuss pēc izvietošanas noliktavas veidlapas**.

5.  Sāciet ražošanas pasūtījumu no klienta vai no rokas ierīces, izmantojot izvēlnes elementu **Ražošanas sākums**.

Pēc tam, kad ražošanas pasūtījums ir sākts, materiālu patēriņu var reģistrēt ar rokas ierīces darbplūsmu. Vispirms reģistrējiet partijas B1 patēriņu 25 mārciņu apmērā.

6.  Rokas ierīces izvēlnē atlasiet izvēlnes elementu **Reģistrēt materiālu** **patēriņu** un ievadiet tālāk norādīto informāciju: 

-    Ražošanas pasūtījuma numurs. 
-    Atrašanās vieta, kurā materiāls tiks patērēts; šajā gadījumā PIL-01. 
-    Krājuma numurs: RM-100. 
-    Partijas numurs: B1. 
-    Daudzums: 25.

7.  Atlasiet **Labi**.

Ņemiet vērā, ka displejā tiek parādīts ziņojums “Žurnāla rinda ir izveidota”. Ražošanas pasūtījumā ir atvērts žurnāls ar veidu **Ražošanas izdošanas saraksts** krājumam ar numuru RM-100 un partijas numuru B1. 

Tagad varat izvēlēties turpināt savu reģistrāciju, piemēram, partijas numura B2, un ikreiz, kad atlasāt **Labi**, atvērtajam žurnālam tiek pievienota jauna žurnāla rinda. 

Kad esat pabeidzis reģistrāciju, atlasiet **Gatavs**, lai grāmatotu žurnālu un beigtu darbplūsmu.

### <a name="additional-comments"></a>Papildu piebilde 

-   Ja lietotājs atceļ darbplūsmu pēc žurnāla rindas izveides, žurnāla statuss ir Negrāmatots, bet, ja lietotājs vēlāk izmanto darbplūsmu tam pašam ražošanas pasūtījumam, tad rindas tiek pievienotas atvērtajam žurnālam, nevis jaunajam žurnālam.
-   Jaunā darbplūsma atbalsta arī sērijas numuru reģistrāciju.
-   Var reģistrēt tikai to krājuma numuru, kas ir definēta materiālu komplektā vai atlasītā ražošanas pasūtījuma vai partijas pasūtījuma formulā.
-   Materiālu var pārmērīgi patērēt. Piemēram, ja tika novērtēts materiāla patēriņš 100 mārciņas, tad tas var tikt pārmērīgi patērēts ar daudzumu, piemēram, 105 mārciņas.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]