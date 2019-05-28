---
title: Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu
description: Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569636"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a>Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Atrodiet kreditoru, kuru atlasīt. Piemēram, ritiniet uz leju līdz US-104.
5. Atlasiet kreditoru US-104.
6. Noklikšķiniet uz Labi.
7. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Atlasiet krājuma vienību. Piemēram, atlasiet krājuma kodu 1000.
9. Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.
10. Noklikšķiniet uz cilnes Iestatījumi.
    * Varat ignorēt atbilstības ierobežojumus, lai izmantotu ierobežojumu bez atbilstības, 2 virzienu atbilstību vai 3 virzienu atbilstību.  
11. Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.
12. Darbību rūtī noklikšķiniet uz Pirkt.
13. Noklikšķiniet uz Apstiprināt.

## <a name="receive-the-products"></a>Preču saņemšana
1. Darbību rūtī noklikšķiniet uz Saņemt.
2. Noklikšķiniet uz Produktu ieejas plūsma.
3. Laukā Produktu ieejas plūsma ievadiet produktu ieejas plūsmas numuru. Piemēram, ievadiet PR123.
4. Lai iegrāmatotu produktu ieejas plūsmu, noklikšķiniet uz OK.
5. Aizvērt lapu.

## <a name="create-a-vendor-invoice"></a>Kreditora rēķina izveidošana
1. Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Pirkšanas pasūtījumi, kas saņemti, bet nav ierakstīti rēķinā.
2. Atlasiet pirkšanas pasūtījumu, kuru izveidojāt.
3. Darbību rūtī noklikšķiniet uz Rēķins.
4. Noklikšķiniet uz Rēķins.
5. Ievadiet rēķina numuru laukā Numurs.
6. Laukā Rēķina apraksts ierakstiet vērtību.
7. Laukā Rēķina datums ievadiet datumu.
8. Laukā Vienības cena ievadiet 1200.
9. Noklikšķiniet uz Pievienot rindu.
10. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet instalācijas maksas krājuma kodu. Piemēram, S0001
12. Atlasiet instalācijas maksas krājuma kodu.
    * Ņemiet vērā, ka kopš izmaiņu veikšanas salīdzināšana nav veikta.  
13. Noklikšķiniet uz Atjaunināt atbilstības statusu.
14. Darbību rūtī noklikšķiniet uz Pārskatīt.
15. Noklikšķiniet uz Detalizēta informācija par atbilstību.
    * Nav nepieciešams noteikt atbilstību jaunai pakalpojumu rindai, tāpēc tās statuss paliek "Nav veikta".  
16. Atlasiet produktu ieejas plūsmu krājuma vienībai, kuru esat saņēmis.
    * Rindai ar produktu ieejas plūsmu atbilstība tika noteikta, bet ir daudzuma vai cenas neatbilstība, tāpēc tā nav izdevusies.  
17. Laukā Vienības cena ievadiet kādu skaitli.
    * Tagad vienības cena atbilst, statuss tiek atjaunināts uz Nokārtots. Ja jūsu politika atļauj neatbilstības vai salīdzināšana ir tikai brīdinājums, rēķinu joprojām varat iegrāmatot.  
18. Aizvērt lapu.
19. Noklikšķiniet uz Grāmatot.
20. Aizveriet formu.
    * Ņemiet vērā, ka pirkšanas pasūtījuma norāde vairs neatbilst statusam, ka tas ir saņemts, bet rēķins nav izrakstīts.  

