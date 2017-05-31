---
title: "Piegādes grafiki"
description: "Piegādes grafiki ļauj izsekot pasūtījuma rindu daudzumam, ja vienam pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pirkšanas pasūtījumam tiek izmantotas vairākas piegādes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 701a8b2b94fecedcddada46ad6438448254c8e77
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="delivery-schedules"></a>Piegādes grafiki

[!include[banner](../includes/banner.md)]


Piegādes grafiki ļauj izsekot pasūtījuma rindu daudzumam, ja vienam pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pirkšanas pasūtījumam tiek izmantotas vairākas piegādes.

Izmantojiet piegādes grafikus, kad kopējais daudzums pasūtījuma vai piedāvājuma rindā ir jāpiegādā vairākos sūtījumos. Atsevišķi sūtījumi tiek norādīti ar piegādes rindām. Divas vai vairākas piegādes rindas veido vienu piegādes grafiku. Piegādes rindām var būt atšķirīgi piegādes datumi, daudzumi, piegādes režīmi un noliktavas dimensijas, piemēram, vieta un noliktava.  

**Piegādes grafika piemērs**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Kopējais pasūtījums (sākotnējā pasūtījuma rinda) | 600 krēsli                               |
| Pieprasītais piegādes grafiks       | 100 krēslu mēnesī                     |
| Pieprasītais piegādes laiks | 6 mēneši, katra mēneša pirmajā dienā |

Šādā gadījumā klients pieprasa piegādāt 600 krēslus paketēs pa 100 krēsliem sešu mēnešu laikā. Lai izsekotu piegādes prasības, izveidojiet piegādes grafiku. Piegādes grafika lapā izveidojiet sešas atsevišķas piegādes rindas. Katrā piegādes rindā ir 100 krēsli; tā norāda šo 100 krēslu piegādes datumu. Šajā gadījumā katra rinda ir korespondējoša pirmajā mēneša dienā sešus mēnešus pēc kārtas.  

Izveidojot piegādes grafiku, sākotnējās pasūtījuma rindas tips automātiski mainās uz **Pasūtījuma rinda ar vairākām piegādēm**. Šī tipa rindu dēvē par tirdzniecības rindu, un tā tiek apzīmēta ar ikonu. Piegādes rinda tiek atzīmēta ar citu ikonu. Ja piegādes rindā maināt daudzumu, tad tirdzniecības rinda tiek atjaunināta uz piegādes grafika kopējo daudzumu. Ja tirdzniecības līgums ir definējis pasūtījuma kopējo atlaidi, tad piegādes grafiks nodrošina, ka jūsu pasūtījumam piešķir kopējo pasūtījuma atlaidi pat tad, ja pasūtījums ir sadalīts atsevišķās piegādēs.  

Pasūtījumi, kuriem ir piegādes grafiks, tiek apstrādāti pret piegādes rindām. Apstrāde ietver pavadzīmju grāmatošanu, produktu ieejas plūsmas un rēķina izrakstīšanu.  

Dokumenta izdrukas pasūtījumiem un piedāvājumiem, kam ir piegādes grafiks, uzrāda tikai piegādes rindas. Tajās nebūs redzamas sākotnējas rindas (tirdzniecības rindas). **Piezīme.** Turklāt ir redzamas tikai piegādes rindas, kad veicat tālāk minētās darbības.

-   Amats
-   Kopēt lapas
-   Pārlūkot saraksta lapas un pārskatus

Apstiprinot pārdošanas piedāvājumu, iegūtie pārdošanas pasūtījumi uzradīs visu piegādes grafiku pat tad, ja pasūtījuma rindās ir vairākas piegādes. Turklāt viss piegādes grafiks būs redzams visās galvenajās lapās, piemēram, pārdošanas pasūtījumos, pārdošanas piedāvājumos un pirkšanas pasūtījumos.




