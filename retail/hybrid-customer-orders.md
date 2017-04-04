---
title: "Hibrīda klientu pasūtījumus"
description: "Hibrīda klienta pasūtījums ir vienā pasūtījumā, ko satur produkti, kas var pārvadāt no veikala klientu, kā arī produkti, kas iekāpj vai piegādāti vēlāk."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hibrīda klientu pasūtījumus

Hibrīda klienta pasūtījums ir vienā pasūtījumā, ko satur produkti, kas var pārvadāt no veikala klientu, kā arī produkti, kas iekāpj vai piegādāti vēlāk.

Microsoft Dynamics 365 operācijām - mazumtirdzniecība, var izvēlēties vai nu veic visus produktus vai veikt izvēlēto produktu klienta pasūtījumu. Produktu līnijas, kas atzīmēti kā veikt tiek automātiski aprēķināti pēc pasūtījuma izveides, līdzīgi tas ir tas pats, par rīkojumu, kas tiks noplūktiem-up pēc pasūtījuma izveides. Maksājamo summu par hibrīdu pasūtījumiem nosaka, pievienojot depozīta procenti pēc savākšanas un kuģis produktu līnijas ar rindām veic pilnā apmērā. Hibrīda pasūtījumiem, sistēma pārslēdzas starp klientu pasūtījumu un naudas and carry režīmu šādi:

-   Ja visu produktu grozā ir iestatīts uz **veikt piegādes**, pasūtījums tiks apstrādāta kā Cash and Carry darbība.
-   Ja jebkurai vai visām līnijām grozā ir iestatītas, lai vai nu **Pick** vai **kuģa piegādes**, pasūtījums tiks apstrādāta kā klienta pasūtījumu.

Ja grozs rinda ir atzīmēta un **Pick atlasīti**, **kuģis izvēlēts**, vai **veikt atlasītā** ir atlasīta, tikai konkrētu grozs līnija ir iestatīts, ka piegādes metode. Tādā gadījumā pakārtots plūsmas darbība turpinās kā parasti. Tomēr ja **Pick atlasīti**, **kuģis izvēlēts**, vai **veikt atlasītā** atzīmēta bez ratiem līnijas tiek atlasīts, lapa atveras jauns uzskaita grozs rindas. Šajā ekrānā varat atlasīt vairākas rindas vienlaikus, nosakot piegādes metodi. Ja izmantojat šo metodi rindu atlasīšana, iepriekšējā piegādes metode, kas piešķirts rindā tiks ignorēts.

<a name="see-also"></a>Skatiet arī
--------

[Klientu pasūtījumu pārskats](customer-orders-overview.md)


