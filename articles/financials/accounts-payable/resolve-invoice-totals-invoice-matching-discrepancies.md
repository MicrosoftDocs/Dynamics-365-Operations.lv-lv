---
title: Atrisināt neatbilstību rēķinu kopsummu saskaņošanas laikā
description: Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi.
author: abruer
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f4747c13d70d45404069a200124336d6f54947
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/25/2019
ms.locfileid: "896354"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Atrisināt neatbilstību rēķinu kopsummu saskaņošanas laikā

[!include [banner](../includes/banner.md)]

Viens rēķinu salīdzināšanas validēšanas veids ir rēķinu kopsummu salīdzināšana. Lai norādītu, ka sistēmai būtu jāveic rēķinu kopsummu salīdzināšana, lapā **Kreditoru moduļa parametri** cilnē **Rēķinu validēšana** iestatiet opciju **Saskaņot rēķinu kopsummas** uz **Jā**. 

Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi. Sešas kopsummas tiek salīdzinātas lapā **Detalizēta informācija par rēķinu kopsummu atbilstību**. Ja kāda no kopsummām atšķiras no paredzamās atbilstošās pirkšanas pasūtījuma kopsummas, salīdzināšanas laikā atklātā neatbilstība tiek atzīmēta. 

Lai pārskatītu rēķinu, kurā ir kopsummu salīdzināšanas neatbilstības, darbvietā **Kreditora rēķina ieraksts** noklikšķiniet uz elementa **Neizlemtie rēķini**. Pēc tam darbību rūtī cilnē **Pārskatīt** noklikšķiniet uz **Detalizēta informācija par atbilstību**. Ja ir konstatētas salīdzināšanas neatbilstības, blakus rēķina summai parādās brīdinājuma ikonas. Sīkāk par kopsummām varat skatīt detalizētā informācijā par rēķinu kopsummu atbilstību. 

Kad neatbilstība ir identificēta, var būt nepieciešams sazināties ar kreditoru, ja uzskatāt, ka rēķinā minētā informācija nav pareiza. Atkarībā no rezultātā iegūtās vienošanās ar kreditoru, varat veikt kādu no šīm darbībām:

-   Pieņemt cenas atšķirību un grāmatot rēķinu, kurā ir salīdzināšanas neatbilstības. Sistēmu var iestatīt, lai pieprasītu apstiprinājumu, pirms var grāmatot, vai pastāv salīdzināšanas neatbilstības. Šajā gadījumā jums ir jāapstiprina salīdzināšanas neatbilstība un pēc izvēles var ievadīt apstiprinājuma komentāru. Pēc tam varat atlasīt rēķina grāmatošanu.
-   Labot rēķina summu uz prognozējamo summu un grāmatot šo rēķinu.
-   Pieprasīt no kreditora visu kredītu un jaunu, labotu rēķinu.

Plašāku informāciju skatiet šeit: [Izpēte/izņēmumu novēršana](tasks/research-resolve-exceptions.md).


