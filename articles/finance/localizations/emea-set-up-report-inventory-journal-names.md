---
title: Krājumu žurnāla pārskati
description: Kad lietojat konfigurējamus krājumu pārskatus, kuru pamatā ir elektronisko pārskatu veidošana, ir nepieciešams iestatīt attiecības starp konkrētu pārskatu un žurnāla tipu.
author: AdamTrukawka
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265144
ms.search.form: InventJournalName
ms.openlocfilehash: 786cb792ad7f2acb10b451ebee3dfb247b287e8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283431"
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
