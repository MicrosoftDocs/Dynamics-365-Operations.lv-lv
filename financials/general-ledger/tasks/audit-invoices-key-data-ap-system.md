--- 
title: "Rēķinu un pamatdatu auditēšana kreditoru modulī"
description: "Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 38cc5587d970d05492638ed349484e6c002d5363
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Rēķinu un pamatdatu auditēšana kreditoru modulī

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


