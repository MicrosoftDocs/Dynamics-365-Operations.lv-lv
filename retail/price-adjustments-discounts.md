---
title: Cenu korekcijas un atlaides
description: "Šajā raksta ir sniegta informāciju par cenu korekcijām un atlaidēm programmatūras Microsoft Dynamics 365 for Operations modulī Mazumtirdzniecība un komercija."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: cb4f189b1f51788dea84702e4410cfaf8f570865
ms.contentlocale: lv-lv
ms.lasthandoff: 04/26/2017


---

# <a name="price-adjustments-and-discounts"></a>Cenu korekcijas un atlaides

[!include[banner](includes/banner.md)]


Šajā raksta ir sniegta informāciju par cenu korekcijām un atlaidēm programmatūras Microsoft Dynamics 365 for Operations modulī Mazumtirdzniecība un komercija.

Programmatūrā Microsoft Dynamics 365 for Operations — Retai varat veikt preču cenu korekcijas, kā arī iestatīt atlaides, kas tiek lietotas rindas precei vai transakcijai pārdošanas punktā (POS), zvanu centra pārdošanas pasūtījumā vai tiešsaistes pasūtījumā. Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām. Gan cenu korekcijām, gan atlaidēm var norādīt vienu sākuma datumu un beigu datumu vai atkārtošanās periodu, atlaides kodu un dažus papildu atribūtus. Cenu korekcijas un atlaides var lietot precēm, variantiem vai kategorijām. Ja precei tiek lietotas vairākas atlaides, debitors var saņemt vienu no atlaidēm vai kombinētu atlaidi atkarībā no konta konfigurācijas. Programmatūrā Dynamics 365 for Operations tiek automātiski lietota tā atlaide vai atlaižu kombinācija, kas nodrošina debitoram izdevīgāko cenu. Iestatot cenas korekciju vai atlaidi, pārliecinieties, lai akceptētu, ka cenu grupas ir piešķirtas pareizo kanālus, katalogus, piederības vai lojalitātes programmas, kuras vēlaties piemērot atlaidi. Turklāt, ja vēlaties automātiski ģenerēt atlaides ID, pirms jaunas cenas korekcijas vai atlaides definēšanas iestatiet numuru sērijas lapā **Mazumtirdzniecības rekvizīti**. **Piezīme.** Cenas korekciju vai atlaidi var dzēst. Taču tādējādi tiek zaudēta statistiskā informācija.

### <a name="types-of-discounts"></a>Atlaižu vedi

Ir pieejami četri mazumtirdzniecības atlaižu veidi.

-   **Vienkārša atlaide** — viena procentuālā vērtība vai summa.
-   **Daudzuma atlaide** — atlaide, kas tiek lietota, ja tiek pirktas divas preces vai vairāk.
-   **Komplekta piedāvājuma atlaide** — atlaide, kas tiek lietota, ja tiek nopirkta noteikta preču kombinācija.
-   **Sliekšņa atlaide** — atlaide, kas tiek lietota, ja transakcijas kopsumma pārsniedz noteiktu summu.

Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām. Pēc tam cenu grupas var saistīt ar kanāliem, kategorijām, piederībām un lojalitātes programmām.




