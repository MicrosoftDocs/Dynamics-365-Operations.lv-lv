---
title: "Rezervēt krājumu daudzumus"
description: "Šajā tēmā ir aprakstītas dažādās opcijas, kas ir pieejamas krājumu rezervēšanai."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c351618f4d710062dd8f369c5319cdce79f7339
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-inventory-quantities"></a>Rezervēt krājumu daudzumus

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstītas dažādās opcijas, kas ir pieejamas krājumu rezervēšanai.

Krājumu daudzumus noteiktiem pārdošanas pasūtījumiem varat rezervēt automātiski. Tas nozīmē, ka rezervēto krājumu nevar izņemt no noliktavas citiem pasūtījumiem, ja vien netiek atcelta šī krājuma rezervācija vai daļa no krājuma rezervācijas.

Krājumu rezervēšanai pastāv vairāki tālāk aprakstītie iemesli.
-   Pirmais pasūtīts – pirmais piegādāts, kas nozīmē, ka debitori iegūst pieejamus krājumus tādā pašā secībā, kādā viņi iesniedz savus pasūtījumus.
-   Krājumu deficītu izraisa ilgs vai nezināms kreditora piegādes laiks. Iespējams, vēlaties nodrošināt, ka noteikti debitori vai pasūtījumi saņem pirmo pieejamo krājumu piegādi.
-   Noteiktiem debitoriem un noteiktiem pasūtījumu tipiem ir pirmā piegādes prioritāte.
-   krājumi ar sērijas vai partijas numuriem. Var iezīmēt noteiktus krājumus, kas ir vai tiks piegādāti noteiktiem pasūtījumiem;
-   Speciāli pasūtīti krājumi, kuri ir rezervēti noteiktiem pasūtījumiem.
-   Ražošanas pasūtījumi. Piemēram, varat atzīmēt krājumus, kuri tiek ražoti un pielāgoti noteiktiem pasūtījumiem.

Krājumus var rezervēt automātiski, kad tiek veidota jauna pasūtījuma rinda, vai arī krājumus var rezervēt manuāli atsevišķiem pasūtījumiem. Krājumus var rezervēt arī dažādos ražošanas procesa posmos. Rezervēt var tikai uzkrātas preces. Pakalpojumus nevar rezervēt, jo tajos nav rīcībā esošu krājumu. Var rezervēt gan fiziskus rīcībā esošus krājumus, gan pasūtītus, bet vēl nesaņemtus krājumus. Ja rezervētais daudzums ir lielāks nekā rīcībā esošais krājums, tiek parādīts ziņojums, ka tik lielu daudzumu nevarat rezervēt. Pēc tam varat vai nu rezervēt šo daudzumu tik un tā, vai mainīt pasūtīto daudzumu. Daudzumu var rezervēt vai mainīt. Ja ir rezervēts vairāk krājumu nekā pieejams, iztrūkums tiek segts nākamajā reizē, kad šie krājumi ir pieejami piegādei.

## <a name="inventory-reservation-policies"></a>Krājumu rezervēšanas politikas
Krājumu rezervēšana politikas tiek iestatītas lapā **Krājumu modeļu grupas**, lapā **Krājumu un noliktavas vadības parametri** un lapā **Ražošanas parametri**.
### <a name="policies-on-the-item-model-groups-page"></a>Politikas lapā Krājumu modeļu grupas

Sadaļā **Krājumu politikas** ir iekļautas tālāk norādītās rezervēšanas politikas.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Rezervēšanas politika**  | **Apraksts**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| No datuma atkarīgs FIFO    | Ja atlasāt opciju **No datuma atkarīgs FIFO**, tad krājumu rezervēšanu nosaka kārtošanas datums saskaņā ar principu FIFO. Partijas tiek rezervētas, pamatojoties uz agrāko krājumu saņemšanas datumu saskaņā ar principu “pirmais iekšā, pirmais ārā” (first in, first out — FIFO).                                                                                                                                                                                                                                                                       |
| Pirms nosūtīšanas datuma | Šī opcija kļūst pieejama tikai tad, ja ir atlasīta opcija **No datuma atkarīgs FIFO**. Ja atlasāt vienumu **Pirms nosūtīšanas datuma**, krājumi tiek rezervēti atpakaļ no vēlamā nosūtīšanas datuma atbilstoši principam “pēdējais iekšā, pirmais ārā” (last in, first out — LIFO). Ja ieejas plūsmas pirms nosūtīšanas datuma nav pieejamas, tiek lietota FIFO rezervēšana.                                                                                                                                                                                                           |
| Krājuma rezervācija pārdošanai  | Nosaka, vai krājumu rezervēšana notiek manuāli vai automātiski. Ja rezervēšana notiek automātiski, krājumi tiek rezervēti, kad tiek izveidotas pasūtījuma rindas. Ir iespējams rezervācijas veikt MK krājuma numura līmenī (opcija **Automātiski**) vai atsevišķiem MK elementiem (opcija **Izvēršana**). Vienuma **Krājuma rezervācija pārdošanai** noklusējuma vērtība var tikt pārmantota no lapas **Debitoru parādu parametri.** Šajā lapā vērtība tiek iestatīta cilnes **Vispārīgi** **sadaļas** **Pārdošanas noklusējuma vērtības** laukā Rezervācija. |
| Tās pašas partijas atlasīšana    | Tās pašas partijas rezervēšana ļauj rezervēt krājumus pārdošanas pasūtījuma rindai no vienas krājumu partijas. Ja vēlaties izmantot šo opciju, arī opcija **Konsolidēt vajadzību** ir jāiestata uz **Jā**. Pastāv papildu iestatījumi, kas ir nepieciešami izsekošanas dimensiju grupai un noliktavas dimensiju grupai. Papildinformāciju skatiet rakstā [Tās pašas partijas rezervēšana pārdošanas pasūtījumam](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Konsolidēt vajadzību | Šī opcija ir līdzīga opcijai **Tās pašas partijas atlasīšana**, un tā pārdošanas pasūtījuma rindās rezervētos krājumus apkopo vienā vajadzībā.                                                                                                                                                                                                                                                                                                                                                                                      |
| No datuma atkarīgs FEFO    | Šī opcija ļauj rezervēt partijas, kurām tuvojas to beigu datums vai derīguma termiņa datums. Arī laukam **Izdošanas kritēriji** ir jāiestata vērtība **Beigu datums** vai **Derīguma termiņa datums**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Opciju No datuma atkarīgs FIFO un Pirms nosūtīšanas datuma lietojuma piemērs

Šajā piemērā krājumam numur A rīcībā esošie krājumi pastāv trīs dažādiem partijas numuriem.
| Krājums | Paketes numurs | Daudzums | Datums             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5.        | 2016. gada 2. februāris |
| A           | 1001         | 3.        | 2016. gada 1. janvāris  |
| A           | 1002         | 7.        | 2016. gada 3. marts    |

Pārdošanas pasūtījums, kuram ir jābūt automātiski rezervētam un piegādātam 2016. gada 4. aprīlī, rezervē šādu partiju:
-   Ja ir noņemta atzīme gan izvēles rūtiņai **No datuma atkarīgs FIFO**, gan izvēles rūtiņai **Pirms nosūtīšanas datuma**, tad tiek rezervēta partija 1000, jo tā ir partija ar zemāko numuru.
-   Ja ir atzīmēta izvēles rūtiņa **No datuma atkarīgs FIFO**, bez izvēles rūtiņai **Pirms nosūtīšanas datuma** ir noņemta atzīme, tad tiek rezervēta partija 1001, jo tā ir partija ar pirmo saņemšanas datumu (FIFO).
-   Ja ir atzīmēta gan izvēles rūtiņa **No datuma atkarīgs FIFO**, gan izvēles rūtiņa **Pirms nosūtīšanas datuma**, tad tiek rezervēta partija 1002, jo tās partijas saņemšana ir vistuvāk pārdošanas pasūtījuma nosūtīšanas datumam.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Politikas lapā Krājumu un noliktavas vadības parametri

Saistībā ar rezervācijām lapā **Krājumu un noliktavas vadības parametri** pastāv divas tālāk aprakstītās opcijas.
-   Opcija **Rezervēt pasūtītos krājumus** cilnē **Vispārīgi** jums ļauj rezervēt krājumu ieejas plūsmas, kuras ir pasūtītas attiecībā pret krājumu izejas plūsmām moduļos Debitoru parādi, Projektu pārvaldība un uzskaite un Ražošanas kontrole. Šo šai opcijai noņemat atzīmi, varat rezervēt tikai tos krājumus, kas ir fiziski saņemti. Ja iestatīts noteikts krājums, lai pieņemtu negatīvus krājumus, šis lauks nav svarīgs.
-   Opcija **Rezervēt krājumus automātiski** cilnē **Transportēšana** nosaka noklusējuma iestatījumu, ja krājumi tiek automātiski rezervēti pārsūtīšanas pasūtījumiem. Atsevišķiem pārsūtīšanas pasūtījumiem var šo noklusējuma iestatījumu var ignorēt.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Krājumu rezervēšanas politikas lapā Ražošanas parametri

Lauka **Rezervācija** vērtību cilnē **Vispārīgi**, lapā **Ražošanas parametri** nosaka šī ražošanas procesa noklusējuma punkts, kurā ir nepieciešams rezervēt krājumus. Piemēram, krājumus var rezervēt, kad darbs tiek plānots vai darbs tiek uzsākts.

