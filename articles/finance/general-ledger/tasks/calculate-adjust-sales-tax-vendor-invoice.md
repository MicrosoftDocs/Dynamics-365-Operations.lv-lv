---
title: PVN aprēķināšana un koriģēšana kreditora rēķinā
description: Šajā rakstā ir izskaidrots, kā koriģēt PVN kreditora rēķinā dynamics 365 finansēs.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868378"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>PVN aprēķināšana un koriģēšana kreditora rēķinā

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā koriģēt PVN kreditora rēķinā. Ja sākotnējā pirmdokumentā ir parādīta atšķirīga nodokļu summa, nekā aprēķināts, pirms grāmatošanas šīs summas varat pielāgot. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums DEMF.

1. Pārejiet **uz sadaļu > kreditoriem, > rēķinu žurnālā**.
2. Atlasiet **Jauna**.
3. Jaunās rindas laukā **Nosaukums** atlasiet opciju nolaižamajā izvēlnē.
4. Darbību rūtī atlasiet **Rindiņas**.
5. Laukā **Konts** norādiet vēlamās vērtības.
6. Laukā **Rēķins** ierakstiet kādu vērtību.
7. Laukā **Kredīts** ievadiet kādu skaitli.
8. Laukā **Korespondējošais konts** norādiet vēlamās vērtības.
9. Atlasiet **PVN**.
10. Ievadiet skaitli laukā **Reālā PVN kopsumma**.
11. PVN summas katram PVN kodam iespējams koriģēt cilnē **Korekcija**.
12. Atlasiet **Atiestatīt faktiskās izmaksas no aprēķinātās summas**.
13. Atlasiet **Labi**.
14. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
