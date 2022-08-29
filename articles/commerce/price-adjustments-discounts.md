---
title: Cenu korekcijas un atlaides
description: Šajā rakstā ir sniegta informācija par cenu korekcijām un atlaidēm programmā Dynamics 365 Commerce.
author: josaw1
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.industry: Retail
ms.search.form: RetailParameters, RetailPeriodicDiscount
ms.openlocfilehash: ff90df814d6930b5cf92772e430625943e0ae983
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279094"
---
# <a name="price-adjustments-and-discounts"></a>Cenu korekcijas un atlaides

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegta informācija par cenu korekcijām un atlaidēm programmā Dynamics 365 Commerce.

Programmā Commerce varat veikt preču cenu korekcijas, kā arī iestatīt atlaides, kas tiek lietotas rindas krājumam vai transakcijai pārdošanas punktā (POS), zvanu centra pārdošanas pasūtījumā vai tiešsaistes pasūtījumā. Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām. Gan cenu korekcijām, gan atlaidēm var norādīt vienu sākuma datumu un beigu datumu vai atkārtošanās periodu, atlaides kodu un dažus papildu atribūtus. 

Cenu korekcijas un atlaides var lietot precēm, variantiem vai kategorijām. Ja precei tiek lietotas vairākas atlaides, debitors var saņemt vienu no atlaidēm vai kombinētu atlaidi atkarībā no konta konfigurācijas. Commerce automātiski lieto to atlaidi vai atlaižu kombināciju, kas nodrošina debitoram izdevīgāko cenu. Iestatot cenas korekciju vai atlaidi, pārliecinieties, lai akceptētu, ka cenu grupas ir piešķirtas pareizo kanālus, katalogus, piederības vai lojalitātes programmas, kuras vēlaties piemērot atlaidi. Turklāt, ja vēlaties automātiski ģenerēt atlaides ID, pirms jaunas cenas korekcijas vai atlaides definēšanas iestatiet numuru sērijas lapā **Commerce rekvizīti**.

> [!NOTE]
> Varat dzēst cenas korekciju vai atlaidi. Taču tādējādi tiek zaudēta statistiskā informācija.

## <a name="types-of-discounts"></a>Atlaižu vedi

Ir pieejami daudz atlaižu veidi:

- **Vienkārša atlaide** — viena procentuālā vērtība vai summa.
- **Daudzuma atlaide** — atlaide, kas tiek lietota, ja tiek pirktas divas preces vai vairāk.
- **Komplekta piedāvājuma atlaide** — atlaide, kas tiek lietota, ja tiek nopirkta noteikta preču kombinācija.
- **Sliekšņa atlaide** — atlaide, kas tiek lietota, ja transakcijas kopsumma pārsniedz noteiktu summu.
- **Uz piedāvājumu balstīta atlaide** – atlaide, kas tiek piemērota, kad darbības kopsumma ir lielāka par norādīto summu un apmaksai tiek izmantots noteikts maksājuma tips (piemēram, skaidra nauda, kredītkarte vai debetkarte).
- **Nosūtīšanas atlaide** – atlaide, kas tiek piemērota, kad darbības kopsumma ir lielāka par norādīto summu un pasūtījumā tiek izmantots noteikts piegādes veids (piemēram, divu dienu piegāde vai nakts piegāde).

Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām. Pēc tam cenu grupas var saistīt ar kanāliem, kategorijām, piederībām un lojalitātes programmām.

> [!NOTE]
> Komplekta atlaidei un sliekšņa atlaidei ir rekvizīti ar nosaukumu “Saskaitīt preces, kam nevar piemērot atlaidi” un “Saskaitīt preces, kam nevar piemērot atlaidi, sasniedzot sliekšņa atlaidi”. Ja šie rekvizīti ir iespējoti, krājums, kas nav piemērots nevienai atlaidei, joprojām var palīdzēt kvalificēt transakciju atlaides saņemšanai, tomēr neatbilstošais krājums atlaidi nesaņems. 
> 
> Piemēram, ja tiek izveidota komplekta atlaide ar divām rindām, A un B, kur debitoram vajadzētu iegūt 10% atlaidi abiem krājumiem, bet krājumam A ir atzīmēta konfigurācija “Liegt visas atlaides”, tad krājums A šajā gadījumā netiktu iekļauts atlaidē. Tomēr, ja ir iespējots rekvizīts “Saskaitīt preces, kam nevar piemērot atlaidi”, tad A krājumu var izmantot, lai kvalificētos komplekta atlaidei, bet 10% atlaide tiks piemērota tikai krājumam B. Līdzīga loģika attiecas uz sliekšņa atlaidi. 
>
> Tomēr rekvizītam “Saskaitīt preces, kam nevar piemērot atlaidi, sasniedzot sliekšņa atlaidi” ir vairāk iespēju, salīdzinot ar komplekta atlaižu rekvizītu “Saskaitīt preces, kam nevar piemērot atlaidi”. Ja ir iespējota sliekšņa atlaide un ja ir krājums ar jau esošu atlaidi, kas liegtu krājumam iegūt citas atlaides, tad par šo krājumu samaksātā cena kvalificēsies sliekšņa atlaidei, bet šim krājumam netiks piemērota papildu atlaide.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
