---
title: Rēķinu un pamatdatu auditēšana kreditoru modulī
description: Šajā rakstā ir paskaidrots, kā pārbaudīt rēķinus un galvenos datus kreditoru parādos.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4525534f906322c7fe4c232f0f6da5b308829087
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775220"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Rēķinu un pamatdatu auditēšana kreditoru modulī

[!include [banner](../../includes/banner.md)]

Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai. Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana. 

**Lapā Kreditoru parādu parametri** pārliecinieties, vai ir atlasīta **opcija Iespējot rēķinu salīdzināšanas validāciju**, **lauks Rēķinu grāmatošana ar neatbilstībām** ir iestatīts uz Pieprasīt apstiprinājumu **un lauks Rindu salīdzināšanas politika** ir iestatīts **uz** **Trīspusēja** atbilstība.

Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Atv. **Visi pirkš. pasūt**.
2. Klikšķiniet **Jauns**.
3. Laukā **Kreditora konts** ierakstiet vērtību.
4. Noklikšķiniet uz **Labi**.
5. Nokl. **Piev. r.**
6. Laukā **Krājuma kods** ierakstiet vērtību.
7. Darbību rūtī noklikšķ. uz **Pirkšana**.
8. Noklikšķiniet uz **Apstiprināt**.

## <a name="post-a-product-receipt"></a>Grāmatot produktu ieejas plūsmu
1. Darbību rūtī noklikšķ. uz **Saņemt**.
2. Nokl. **Pr. ieejas pl**.
3. Laukā **Prod. ieejas pl.** ierakstiet vērtību.
4. Noklikšķiniet uz **Labi**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Ierakstīt kreditora rēķinu un saskaņot to ar produktu ieejas plūsmu
1. Darbību rūtī noklikšķ. uz **Rēķins > Rēķins**.
2. Laukā **Numurs** ierakstiet vērtību.
3. Nokl. uz **Noklusējums no: Pasūt. daudz.**, lai atv. dialogl.
4. Laukā **Noklusējuma daudzums rindām** atlasiet kādu opciju.
5. Noklikšķiniet uz **Labi**.
6. Noklikšķiniet uz pogas **Jā**.
7. Nokl. **Sask. prod. ieejas pl.**.
8. Noklikšķiniet uz **Labi**.
9. Darbību rūtī nokl. uz **Pārskatīt**.
10. Nokl. **Atb. det. inf**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
