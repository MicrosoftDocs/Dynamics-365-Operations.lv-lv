---
title: Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu
description: Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778550"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu

[!include [banner](../../includes/banner.md)]

Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai. Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana. 

**Lapā Kreditoru parādu parametri** pārliecinieties, vai ir atlasīta **opcija Iespējot rēķinu salīdzināšanas validāciju**, **lauks Rēķinu grāmatošana ar neatbilstībām** ir iestatīts uz Pieprasīt apstiprinājumu **un lauks Rindu salīdzināšanas politika** ir iestatīts **uz** **Trīspusēja** atbilstība.

Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Atv. **Visi pirkš. pasūt**.
2. Klikšķiniet **Jauns**.
3. Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Laukā **Kreditora konts** ierakstiet vērtību.
5. Noklikšķiniet uz **Labi**.
6. Nokl. **Piev. r.**
7. Laukā **Krājuma kods** ierakstiet vērtību.
8. Darbību rūtī noklikšķ. uz **Pirkšana**.
9. Noklikšķiniet uz **Apstiprināt**.

## <a name="post-a-product-receipt"></a>Grāmatot produktu ieejas plūsmu
1. Darbību rūtī noklikšķ. uz **Saņemt**.
2. Nokl. **Pr. ieejas pl**.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā **Prod. ieejas pl.** ierakstiet vērtību.
5. Noklikšķiniet uz **Labi**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Ierakstīt kreditora rēķinu un saskaņot to ar produktu ieejas plūsmu
1. Darbību rūtī noklikšķiniet uz **Rēķins**.
2. Noklikšķiniet uz **Rēķins**.
3. Laukā **Numurs** ierakstiet vērtību.
4. Nokl. uz **Noklusējums no: Pasūt. daudz.**, lai atv. dialogl.
5. Laukā **Noklusējuma daudzums rindām** atlasiet kādu opciju.
6. Noklikšķiniet uz **Labi**.
7. Noklikšķiniet uz pogas **Jā**.
8. Nokl. **Sask. prod. ieejas pl.**.
9. Noklikšķiniet uz **Labi**.
10. Darbību rūtī nokl. uz **Pārskatīt**.
11. Nokl. **Atb. det. inf**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
