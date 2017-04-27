---
title: "Hibrīdie debitoru pasūtījumi"
description: "Hibrīds debitora pasūtījums ir atsevišķs pasūtījums, kurā ir ietvertas gan tādas preces, ko debitors var iznest no veikala, gan tādas, kas tiks izdots vai nosūtītas vēlāk."
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

# <a name="hybrid-customer-orders"></a>Hibrīdie debitoru pasūtījumi

[!include[banner](includes/banner.md)]


Hibrīds debitora pasūtījums ir atsevišķs pasūtījums, kurā ir ietvertas gan tādas preces, ko debitors var iznest no veikala, gan tādas, kas tiks izdots vai nosūtītas vēlāk.

Programmatūrā Microsoft Dynamics 365 for Operations — Retail varat izvēlēties debitora pasūtījuma opciju Iznest visas preces vai Iznest atlasītās preces. Par preču grupām, kas ir atzīmētas kā iznesamas, tiek automātiski izrakstīts rēķins uzreiz pēc pasūtījuma izveides. Tas pats pēc pasūtījuma izveides tiek darīts arī ar izdodamām precēm. Hibrīdo pasūtījumu apmaksas summa tiek aprēķināta, saskaitot izdodamo un nosūtāmo preču rindu depozīta procentu summu un iznesamo preču rindu pilnu summu. Apstrādājot hibrīdos pasūtījumus, sistēma pārslēdz debitora pasūtījumu režīmu un pārdošanas skaidrā naudā bez piegādes režīmiem tālāk norādītajā veidā.

-   Ja visām grozā esošajām precēm ir iestatīta opcija **Piegāde iznesot**, pasūtījums tiek apstrādāts kā pārdošanas skaidrā naudā bez piegādes transakcija.
-   Ja vienai vai visām groza rindām ir iestatīta opcija **Piegāde izdodot** vai **Piegāde nosūtot**, pasūtījums tiek apstrādāts kā debitora pasūtījuma transakcija.

Ja tiek atlasīta kāda groza rinda un tiek atlasīta opcija **Izdot atlasīto**, **Nosūtīt atlasīto** vai **Iznest atlasīto**, attiecīgā piegādes metode tiek iestatīta tikai atlasītajai groza rindai. Šādā gadījumā operācijas lejupstraumes plūsma turpinās kā parasti. Taču, ja opcija **Izdot atlasīto**, **Nosūtīt atlasīto** vai **Iznest atlasīto** tiek atlasīta, neatlasot nevienu groza rindu, tiek atvērta jauna lapa, kurā ir norādītas visas groza rindas. Šajā ekrānā varat vienlaikus atlasīt vairākas rindas, kam ir jāiestata attiecīgā piegādes metode. Ja izmantojat rindu atlases metodi, tiek pārrakstīta jebkura rindai iepriekš piešķirtā piegādes metode.

<a name="see-also"></a>Skatiet arī
--------

[Pārskats par debitoru pasūtījumiem](customer-orders-overview.md)




