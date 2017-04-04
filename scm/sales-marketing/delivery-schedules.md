---
title: "Piegādes grafiki"
description: "Piegādes grafiki ļauj izsekot pasūtījuma rindu daudzumam, ja vienam pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pirkšanas pasūtījumam tiek izmantotas vairākas piegādes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: fbada697060c823b0afdb72d1c0cfd8703f4d527
ms.lasthandoff: 03/31/2017


---

# <a name="delivery-schedules"></a>Piegādes grafiki

Piegādes grafiki ļauj izsekot pasūtījuma rindu daudzumam, ja vienam pārdošanas pasūtījumam, pārdošanas piedāvājumam vai pirkšanas pasūtījumam tiek izmantotas vairākas piegādes.

Izmantot piegādes grafiku, kad kopējo daudzumu pasūtījuma vai piedāvājuma rindā jānogādā vairākās partijās. Atsevišķām kravām tiek apzīmētas ar piegādes līniju. Divas vai vairākas piegādes rindas veido vienu piegādes grafiku. Piegādes rindām var būt atšķirīgi piegādes datumi, daudzumi, piegādes režīmi un noliktavas dimensijas, piemēram, vieta un noliktava.  

**Piegādes grafika piemērs**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Kopējais pasūtījums (sākotnējā pasūtījuma rinda) | 600 krēsli                               |
| Pieprasītais piegādes grafiks       | 100 krēslu mēnesī                     |
| Pieprasītais piegādes laiks | 6 mēneši, katra mēneša pirmajā dienā |

Šādā gadījumā klients pieprasa piegādāt 600 krēslus paketēs pa 100 krēsliem sešu mēnešu laikā. Lai izsekotu piegādes prasības, izveidojiet piegādes grafiku. Piegādes grafika lapā izveidojiet sešas atsevišķas piegādes rindas. Katrā piegādes rindā ir 100 krēsli; tā norāda šo 100 krēslu piegādes datumu. Šajā gadījumā katra rinda ir korespondējoša pirmajā mēneša dienā sešus mēnešus pēc kārtas.  

Izveidojot piegādes grafiku, sākotnējās pasūtījuma rindas tips automātiski mainās uz **Pasūtījuma rinda ar vairākām piegādēm**. Šī tipa rindu dēvē par tirdzniecības rindu, un tā tiek apzīmēta ar ikonu. Piegādes rinda tiek atzīmēta ar citu ikonu. Mainot daudzumu piegādi rindā, komerciālo rinda tiek atjaunināta ar kopējo daudzumu piegādes grafiku. Ja tirdzniecības līgums ir definēts pasūtījuma kopējo atlaidi, piegādes grafiks nodrošina, ka jūsu pasūtījumu pretendēt uz pasūtījuma kopējo atlaidi, pat tad, ja pasūtījums ir sadalīts atsevišķas piegādes.  

Pasūtījumi, kuriem ir piegādes grafiks, tiek apstrādāti pret piegādes rindām. Apstrāde ietver pavadzīmju grāmatošanu, produktu ieejas plūsmas un rēķina izrakstīšanu.  

Dokumenta izdrukas pasūtījumiem un piedāvājumiem, kam ir piegādes grafiks, uzrāda tikai piegādes rindas. Tajās nebūs redzamas sākotnējas rindas (tirdzniecības rindas). **Piezīme.** Turklāt ir redzamas tikai piegādes rindas, kad veicat tālāk minētās darbības.

-   Amats
-   Kopēt lapas
-   Pārlūkot saraksta lapas un pārskatus

Apstiprinot pārdošanas piedāvājumu, iegūtie pārdošanas pasūtījumi uzradīs visu piegādes grafiku pat tad, ja pasūtījuma rindās ir vairākas piegādes. Turklāt viss piegādes grafiks būs redzams visās galvenajās lapās, piemēram, pārdošanas pasūtījumos, pārdošanas piedāvājumos un pirkšanas pasūtījumos.


