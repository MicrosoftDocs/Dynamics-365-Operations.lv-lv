---
title: PVN aprēķināšana un koriģēšana kreditora rēķinā
description: Šajā tēmā paskaidrots, kā pielāgot PVN kreditora rēķinam Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 648d94e895a4941f5f3148134130b3ffa693a9d57e0bb4e236f5d5fb33aca48f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779816"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>PVN aprēķināšana un koriģēšana kreditora rēķinā

[!include [banner](../../includes/banner.md)]

Šajā tēmā paskaidrots, kā pielāgot PVN kreditora rēķinam . Ja sākotnējā pirmdokumentā ir parādīta atšķirīga nodokļu summa, nekā aprēķināts, pirms grāmatošanas šīs summas varat pielāgot. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums DEMF.

1. Navigācijas rūtī atveriet **Moduļi > Kreditori > Rēķini > Rēķinu žurnāls**.
2. Atlasiet **Jauns**.
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