---
title: "Tiešās piegādes"
description: "Šajā rakstā ir sniegta informācija par tiešajām piegādēm. Tiešās piegādes ir tādas piegādes, kas no kreditora tiek nosūtītas tieši debitoram."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1f2cdae674dc88a4d533258e24b1ecf7ec4cf55b
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="direct-deliveries"></a>Tiešās piegādes

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par tiešajām piegādēm. Tiešās piegādes ir tādas piegādes, kas no kreditora tiek nosūtītas tieši debitoram.

Tiešās piegādes ietaupa piegādes laiku un samazina izmaksas, kas ir saistītas ar krājuma pārvadāšanu, jo pirms preču nosūtīšanas debitoram tās nav jāuzglabā noliktavā.  

Tiešās piegādes var izveidot lapā **Pārdošanas pasūtījums**. Vispirms izveidojiet pārdošanas pasūtījumu un pasūtījuma rindas. Pēc tam darbību rūtī noklikšķiniet uz cilnes **Pārdošanas pasūtījums** un atlasiet **Tiešā piegāde**. Norādiet rindas, kas jāapstrādā kā tiešā piegāde. Tagad tiek izveidota saite starp tiešās piegādes pārdošanas pasūtījuma rindām un atbilstošām pirkšanas pasūtījuma rindām.  

**Piezīme.** Ja daļa pasūtītā daudzuma jau ir piegādāta, atlikušais daudzums ir jāsadala. Izveidojiet jaunu rindu daudzumam, kas ir jāpiegādā tieši, un atņemiet šo daudzumu no sākotnējā rindā norādītā daudzuma. Ja sākotnējais daudzums bija, piemēram, 15, un piecas vienības jau ir piegādātas, jāizveido jauna rinda atlikušajam daudzumam 10 un pēc tam sākotnējais daudzums ir jāsamazina par šo skaitu.  

Kad esat izveidojis tiešās piegādes saiti starp pārdošanas pasūtījuma rindām un pirkšanas pasūtījuma rindām, varat atjaunināt pārdošanas pasūtījumu, izmantojot pavadzīmi. No pirkšanas pasūtījuma palaidiet pavadzīmes atjaunināšanu vai rēķina atjaunināšanu. Rēķins ir jāatjaunina no pārdošanas pasūtījuma lapā **Pārdošanas pasūtījums**. Atjauninot rēķinu, pārdošanas pasūtījumā norādītais daudzums nedrīkst būt lielāks par daudzumu, kas ir reģistrēts kā saņemts. Piemēram, pārdošanas pasūtījuma rindai ir 10 vienības, bet tikai piecas vienības no pārdošanas pasūtījuma rindas ir atjauninātas, izmantojot pavadzīmi. Ja, atjauninot rēķinu no pārdošanas pasūtījuma, sarakstā **Daudzums** atlasījāt **Viss**, tiek rēķinā tiek atjaunināti tikai tie krājumi, kas tika fiziski saņemti vai atjaunināti, izmantojot pavadzīmi. Visa pārdošanas pasūtījuma rinda netiek atjaunināta.

## <a name="delivery-date"></a>Piegādes datums
Ja atjaunināt lauku **Pieprasītais saņemšanas datums** pārdošanas pasūtījuma rindā, lauks **Piegādes datums** atbilstošajā pirkšanas līgumā arī tiek atjaunināts. Tāpat arī, ja atjaunināt lauku **Apstiprināts** pirkšanas pasūtījuma rindā, tiek atjaunināts arī atbilstošās pārdošanas pasūtījuma rindas lauks **Apstiprinātais saņemšanas datums** un **Apstiprinātais nosūtīšanas datums**.

## <a name="delivery-address"></a>Piegādes adrese
Parasti pirkšanas pasūtījuma piegādes adrese ir uzņēmuma adrese. Tomēr, kad veidojat tiešo piegādi, kā piegādes adrese tiek ievadīta debitora adrese. Ja maināt piegādes adresi pirkšanas pasūtījuma rindā ar piegādes veidu **Tiešā piegāde**, tiek atjaunināta arī piegādes adrese atbilstošajai pārdošanas pasūtījuma rindai. Tāpat, ja maināt piegādes adresi pārdošanas pasūtījuma rindā, tiek atjaunināta arī piegādes adrese pirkšanas pasūtījuma rindā.

## <a name="deleting-order-lines"></a>Pasūtījuma rindu dzēšana
Ja mēģināt dzēst pārdošanas pasūtījuma rindu, kuras piegādes veids ir **Tiešā piegāde**, tiek parādīts ziņojums, kur ir norādīts, ka šai rindai ir piesaistītas pirkšanas pasūtījuma rindas. Ja pārdošanas pasūtījuma rinda ir piegādāta daļēji, nevarat dzēst šo pārdošanas pasūtījuma rindu vai tai piesaistītās pirkšanas pasūtījuma rindas.

## <a name="warehouse"></a>Noliktava
Kad veidojat tiešo piegādi, jūsu pārdotie krājumi nekad fiziski netiek ievesti noliktavā. Tomēr pārdošanas pasūtījuma rindā tik un tā ir jānorāda noliktava. Tāpat arī attiecīgajam krājumam krājumu modeļu grupā var būt norādītas izsniegšanas prasībās. Tā kā krājumi nekad fiziski netiek ievesti noliktavā, šīs prasības tiek ignorētas, ja pārdošanas pasūtījumam izmantojat tiešo piegādi.




