---
title: "Neatbilstību novēršana rēķinu kopsummu salīdzināšanas laikā"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 8ccc1af0e1bd7909b7810d359a916849ecc1a709
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Neatbilstību novēršana rēķinu kopsummu salīdzināšanas laikā

[!include[banner](../includes/banner.md)]




Viens rēķinu salīdzināšanas validēšanas veids ir rēķinu kopsummu salīdzināšana. Lai norādītu, ka sistēmai būtu jāveic rēķinu kopsummu salīdzināšana, lapā **Kreditoru moduļa parametri** cilnē **Rēķinu validēšana** iestatiet opciju **Saskaņot rēķinu kopsummas** uz **Jā**. 

Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi. Sešas kopsummas tiek salīdzinātas lapā **Detalizēta informācija par rēķinu kopsummu atbilstību**. Ja kāda no kopsummām atšķiras no paredzamās atbilstošās pirkšanas pasūtījuma kopsummas, salīdzināšanas laikā atklātā neatbilstība tiek atzīmēta. 

Lai pārskatītu rēķinu, kurā ir kopsummu salīdzināšanas neatbilstības, darbvietā **Kreditora rēķina ieraksts** noklikšķiniet uz elementa **Neizlemtie rēķini**. Pēc tam darbību rūtī cilnē **Pārskatīt** noklikšķiniet uz **Detalizēta informācija par atbilstību**. Ja ir konstatētas salīdzināšanas neatbilstības, blakus rēķina summai parādās brīdinājuma ikonas. Sīkāk par kopsummām varat skatīt detalizētā informācijā par rēķinu kopsummu atbilstību. 

Kad neatbilstība ir identificēta, var būt nepieciešams sazināties ar kreditoru, ja uzskatāt, ka rēķinā minētā informācija nav pareiza. Atkarībā no rezultātā iegūtās vienošanās ar kreditoru, varat veikt kādu no šīm darbībām:

-   Pieņemt cenas atšķirību un grāmatot rēķinu, kurā ir salīdzināšanas neatbilstības. Sistēmu var iestatīt, lai pieprasītu apstiprinājumu, pirms var grāmatot, vai pastāv salīdzināšanas neatbilstības. Šajā gadījumā jums ir jāapstiprina salīdzināšanas neatbilstība un pēc izvēles var ievadīt apstiprinājuma komentāru. Pēc tam varat atlasīt rēķina grāmatošanu.
-   Labot rēķina summu uz prognozējamo summu un grāmatot šo rēķinu.
-   Pieprasīt no kreditora visu kredītu un jaunu, labotu rēķinu.

Plašāku informāciju skatiet šeit: [Izpēte/izņēmumu novēršana](tasks/research-resolve-exceptions.md).



