---
title: Neatbilstību atrisināšanas rēķinu kopsummu salīdzināšanas laikā pārskats
description: Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0635f388dba16a1e4374f0915fbab5b88c3b76ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227454"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Neatbilstību atrisināšanas rēķinu kopsummu salīdzināšanas laikā pārskats

[!include [banner](../includes/banner.md)]

Viens rēķinu salīdzināšanas validēšanas veids ir rēķinu kopsummu salīdzināšana. Lai norādītu, ka sistēmai būtu jāveic rēķinu kopsummu salīdzināšana, lapā **Kreditoru moduļa parametri** cilnē **Rēķinu validēšana** iestatiet opciju **Saskaņot rēķinu kopsummas** uz **Jā**. 

Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi. Sešas kopsummas tiek salīdzinātas lapā **Detalizēta informācija par rēķinu kopsummu atbilstību**. Ja kāda no kopsummām atšķiras no paredzamās atbilstošās pirkšanas pasūtījuma kopsummas, salīdzināšanas laikā atklātā neatbilstība tiek atzīmēta. 

Lai pārskatītu rēķinu, kurā ir kopsummu salīdzināšanas neatbilstības, darbvietā **Kreditora rēķina ieraksts** noklikšķiniet uz elementa **Neizlemtie rēķini**. Pēc tam darbību rūtī cilnē **Pārskatīt** noklikšķiniet uz **Detalizēta informācija par atbilstību**. Ja ir konstatētas salīdzināšanas neatbilstības, blakus rēķina summai parādās brīdinājuma ikonas. Sīkāk par kopsummām varat skatīt detalizētā informācijā par rēķinu kopsummu atbilstību. 

Kad neatbilstība ir identificēta, var būt nepieciešams sazināties ar kreditoru, ja uzskatāt, ka rēķinā minētā informācija nav pareiza. Atkarībā no rezultātā iegūtās vienošanās ar kreditoru, varat veikt kādu no šīm darbībām:

-   Pieņemt cenas atšķirību un grāmatot rēķinu, kurā ir salīdzināšanas neatbilstības. Sistēmu var iestatīt, lai pieprasītu apstiprinājumu, pirms var grāmatot, vai pastāv salīdzināšanas neatbilstības. Šajā gadījumā jums ir jāapstiprina salīdzināšanas neatbilstība un pēc izvēles var ievadīt apstiprinājuma komentāru. Pēc tam varat atlasīt rēķina grāmatošanu.
-   Labot rēķina summu uz prognozējamo summu un grāmatot šo rēķinu.
-   Pieprasīt no kreditora visu kredītu un jaunu, labotu rēķinu.

Plašāku informāciju skatiet [Izpēte/izņēmumu novēršana](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]