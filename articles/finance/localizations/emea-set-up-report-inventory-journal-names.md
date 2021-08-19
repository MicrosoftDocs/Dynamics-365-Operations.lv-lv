---
title: Krājumu žurnāla pārskati
description: Kad lietojat konfigurējamus krājumu pārskatus, kuru pamatā ir elektronisko pārskatu veidošana, ir nepieciešams iestatīt attiecības starp konkrētu pārskatu un žurnāla tipu.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalName
audience: Application User
ms.reviewer: kfend
ms.custom: 265144
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 21db23a111f746f6b1e3228b27f836fe57d7b01d4cd0e3d6233356ee446bd5e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750295"
---
# <a name="inventory-journal-reports"></a>Krājumu žurnāla pārskati

[!include [banner](../includes/banner.md)]

Kad lietojat konfigurējamus krājumu pārskatus, kuru pamatā ir elektronisko pārskatu veidošana, ir nepieciešams iestatīt attiecības starp konkrētu pārskatu un žurnāla tipu.

Lai iestatītu attiecības starp konkrētu pārskatu un kādu žurnāla tipu, lapā **Krājumu žurnālu nosaukumi** (**Krājumu vadība** &gt; **Iestatīšana** &gt; **Žurnālu nosaukumi** &gt; **Krājumi**) ievadiet šī pārskata nosaukumu. **Piezīme.** Lai iestatītu atbalstītās konfigurācijas, lejupielādējiet nepieciešamās elektronisko pārskatu konfigurācijas. Papildinformāciju skatiet rakstā [Lejupielādēt elektronisko pārskatu konfigurācijas no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md). Nākamajā tabulā ir uzskaitīti krājumu pārskatu piemēri ar Eiropā atbalstītām konfigurācijām.

| Valsts/reģions            |    Pārskata apraksts               | Žurnāla tips     |    Formāta kartēšanas nosaukums                  |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| Lietuva, Ungārija | Inventarizācijas akta pārskats          | Inventarizācija         | Inventarizācijas akts (HU, LT)            |
| Latvija, Polija     | Krājumu pārklasificēšanas dokuments | Pārsūtījums         | InventoryReclassificationDocument\_PLLV |
| Igaunija            | Krājumu pārklasificēšanas dokuments | Pārsūtījums         | InventoryReclassificationDocument\_EE   |
| Polija             | Iekšējais PW/RW                      | Kustība         | InventJournalLinesDocPL                 |
| Latvija             | Krājumu kustības dokuments         | Kustība         | Kustība\_LV                            |
| Latvija             | Krājumu norakstīšanas dokuments       | Pielāgojums       | InventJournalLines\_LV                  |
| Latvija             | Pārvietojuma pavadzīme              | Pārsūtījums         | InternalTransferDeliveryNote\_LV        |
| Latvija             | Uzskaitīšanas dokumenta pārskats            | Inventarizācija         | CountedDocument\_LV                     |
| Latvija             | Inventarizācijas saraksta pārskats                | Inventarizācija         | Inventarizācijas saraksts                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]