---
title: Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu
description: Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9d3fab4be1de90783d5885cf46b9e0cf6ee74b5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820621"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu

[!include [banner](../../includes/banner.md)]

Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai. Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana. 

Lapā Kreditoru moduļa parametri pārliecinieties, ka ir atlasīta opcija Iespējot rēķinu salīdzināšanas pārbaudes, lauks Grāmatot rēķinu ar neatbilstībām ir iestatīts uz Pieprasīt apstiprinājumu un lauks Rindu atbilstības ierobežojumi ir iestatīts uz Trīsvirzienu atbilstība.

Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Dodieties uz Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Laukā Kreditora konts ierakstiet kādu vērtību.
5. Noklikšķiniet uz OK.
6. Noklikšķiniet uz Pievienot rindu.
7. Laukā Krājuma kods ierakstiet kādu vērtību.
8. Darbību rūtī noklikšķiniet uz Pirkt.
9. Noklikšķiniet uz Apstiprināt.

## <a name="post-a-product-receipt"></a>Grāmatot produktu ieejas plūsmu
1. Darbību rūtī noklikšķiniet uz Saņemt.
2. Noklikšķiniet uz Produktu ieejas plūsma.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Produktu ieejas plūsma ierakstiet kādu vērtību.
5. Noklikšķiniet uz OK.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Ierakstīt kreditora rēķinu un saskaņot to ar produktu ieejas plūsmu
1. Darbību rūtī noklikšķiniet uz Rēķins.
2. Noklikšķiniet uz Rēķins.
3. Laukā Numurs ierakstiet kādu vērtību.
4. Noklikšķiniet uz Noklusējums no: Pasūtītais daudzums, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Noklusējuma daudzums rindām atlasiet kādu opciju.
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz Jā.
8. Noklikšķiniet uz Saskaņot produktu ieejas plūsmu.
9. Noklikšķiniet uz OK.
10. Darbību rūtī noklikšķiniet uz Pārskatīt.
11. Noklikšķiniet uz Detalizēta informācija par atbilstību.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]