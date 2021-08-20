---
title: Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu
description: Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3e27ed41ff1fa44d5e8779cb5e81e45d02110eb3b37be3a3b9938cabfc395bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777292"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Galvenie rēķinu dati kreditoru sistēmā, izmantojot kreditora rēķinu

[!include [banner](../../includes/banner.md)]

Šis uzdevuma ceļvedis palīdzēs izveidot kreditora rēķinu no pirkšanas pasūtījuma un apskatīt pirkšanas pasūtījuma, kvīts un rēķina saskaņošanas rezultātus (3 virzienu atbilstība).


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Navigācijas rūtī dodieties uz **Moduļi > Kreditori > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Kreditora konts** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Atrodiet kreditoru, kuru atlasīt. Piemēram, ritiniet uz leju līdz US-104.
5. Atlasiet kreditoru US-104.
6. Noklikšķiniet uz **Labi**.
7. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Atlasiet krājuma vienību. Piemēram, atlasiet krājuma kodu 1000.
9. Izvērsiet kopsavilkuma cilni **Detalizēta informācija par rindu**.
10. Noklikšķiniet uz cilnes **Iestatīšana**. Varat ignorēt atbilstības ierobežojumus, lai izmantotu ierobežojumu bez atbilstības, 2 virzienu atbilstību vai 3 virzienu atbilstību.  
11. Darbību rūtī noklikšķ. uz **Pirkšana**.
12. Noklikšķiniet uz **Apstiprināt**.

## <a name="receive-the-products"></a>Preču saņemšana
1. Darbību rūtī noklikšķ. uz **Saņemt**.
2. Nokl. **Pr. ieejas pl**.
3. Laukā **Produktu ieejas plūsma** ievadiet produktu ieejas plūsmas numuru. Piemēram, ievadiet PR123.
4. Lai iegrāmatotu produktu ieejas plūsmu, noklikšķiniet uz **Labi**.
5. Aizvērt lapu.

## <a name="create-a-vendor-invoice"></a>Kreditora rēķina izveidošana
1. Navigācijas rūtī dodieties uz **Moduļi > Kreditori > Pirkšanas pasūtījumi > Pirkšanas pasūtījumi, kas ir saņemti, bet kam nav izveidots rēķins**.
2. Atlasiet pirkšanas pasūtījumu, kuru izveidojāt.
3. Darbību rūtī noklikšķiniet uz **Rēķins**.
4. Noklikšķiniet uz **Rēķins**.
5. Ievadiet rēķina numuru laukā **Numurs**.
6. Laukā **Rēķina apraksts** ierakstiet vērtību.
7. Ievadiet datumu laukā **Rēķina datums**.
8. Laukā **Vienības cena** ievadiet 1200.
9. Nokl. **Piev. r.**
10. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet instalācijas maksas krājuma kodu. Piemēram, S0001
12. Atlasiet instalācijas maksas krājuma kodu. Ņemiet vērā, ka kopš izmaiņu veikšanas salīdzināšana nav veikta.  
13. Noklikšķiniet uz **Atjaunināt atbilstības statusu**.
14. Darbību rūtī nokl. uz **Pārskatīt**.
15. Nokl. **Atb. det. inf**. Nav nepieciešams noteikt atbilstību jaunai pakalpojumu rindai, tāpēc tās statuss paliek "Nav veikta".  
16. Atlasiet produktu ieejas plūsmu krājuma vienībai, kuru esat saņēmis. Rindai ar produktu ieejas plūsmu atbilstība tika noteikta, bet ir daudzuma vai cenas neatbilstība, tāpēc tā nav izdevusies.  
17. Laukā **Vienības cena** ievadiet kādu skaitli. Tagad vienības cena atbilst, statuss tiek atjaunināts uz Nokārtots. Ja jūsu politika atļauj neatbilstības vai salīdzināšana ir tikai brīdinājums, rēķinu joprojām varat iegrāmatot.  
18. Aizvērt lapu.
19. Noklikšķiniet uz **Grāmatot**.
20. Aizveriet formu. Ņemiet vērā, ka pirkšanas pasūtījuma norāde vairs neatbilst statusam, ka tas ir saņemts, bet rēķins nav izrakstīts.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]