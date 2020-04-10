---
title: PVN aprēķināšana un koriģēšana kreditora rēķinā
description: Šajā tēmā paskaidrots, kā pielāgot PVN kreditora rēķinam Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139971"
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

