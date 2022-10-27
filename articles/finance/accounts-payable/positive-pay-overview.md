---
title: Pozitīvā maksājuma pārskats
description: Šajā rakstā ir sniegta informācija par pozitīvo maksājumu, kas tiek izmantots, lai izveidotu elektronisku čeku sarakstu, ko var iesniegt bankā.
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: thweeloc
ms.custom:
- "88463"
- intro-internal
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: f25dfaaa2e52b58c7b6971b4d277ef315de431a0
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715771"
---
# <a name="positive-pay-overview"></a>Pozitīvā maksājuma pārskats

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par pozitīvo maksājumu, kas tiek izmantots, lai izveidotu elektronisku čeku sarakstu, ko var iesniegt bankā. 

Pozitīvais maksājums tiek izmantots, lai izveidotu elektronisku čeku sarakstu, ko var iesniegt bankā. Pozitīvā maksājuma faili var bankām palīdzēt novērst krāpšanos ar čekiem. Katru reizi, izdrukājot čekus, tiek iestatīts pozitīvais maksājums, lai izveidotu elektronisko čeku sarakstu. Pēc tam, iesniedzot čeku bankā, tas tiek salīdzināts ar iepriekš iesniegto čeku sarakstu. Ja čeks atbilst čekam sarakstā, banka to dzēš. Ja čeks neatbilst čekam sarakstā, banka to aiztur uz pārskatīšanu.

Pozitīvo maksājumu sauc arī par SafePay. 

Pozitīvo maksājumu faili var saturēt konfidenciālu informāciju par maksājumu saņēmējiem un čeku summām. Šī iemesla dēļ nodrošiniet, lai no failu ģenerēšanas, līdz to saņemšanai bankā, tiek veikti atbilstoši drošības pasākumi. Pozitīvā maksājuma faili tiek lejupielādēti saskaņā ar tīmekļa pārlūkprogrammas lejupielādes instrukcijām. 

Pozitīvā maksājuma faili tiek izveidoti, izmantojot datu elementus. Lai varētu izveidot pozitīvā maksājuma failu, vispirms ir jāiestata XML transformācijas formāti, kas pārveido datus bankai izmantojamā formātā. 

Katram bankas kontam, kuram vēlaties ģenerēt pozitīvā maksājuma datus, jāpiešķir pozitīvā maksājuma formāts. Kad maksājumi ir izveidoti, var izveidot pozitīvā maksājuma failu vienai juridiskajai personai un vienam bankas kontam. Papildus var izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un bankas kontiem vienlaicīgi. 

Kad čeki ir ievietoti sarakstā un pozitīvā maksājuma fails ir apmaksāts, banka jums nosūta apstiprinājuma numuru. Pēc tam varat konfigurēt pozitīvā maksājuma failu sistēmā. 

Ja pozitīvā maksājuma fails ir jāmaina, to var atsaukt. Pēc tam katra pozitīvā maksājuma failā tiek atiestatīts lauks, kas norāda, vai šis čeks ir iekļauts pozitīvā maksājuma failā.

Papildinformāciju skatiet tēmā [Pozitīvā maksājuma failu iestatīšana un ģenerēšana](set-up-generate-positive-pay-files.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
