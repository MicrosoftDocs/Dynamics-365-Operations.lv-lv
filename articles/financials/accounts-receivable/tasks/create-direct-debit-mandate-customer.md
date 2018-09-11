--- 
title: "Tiešā debeta pilnvarojuma izveide debitoram"
description: "Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Tiešā debeta pilnvarojuma izveide debitoram

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā.


## <a name="create-a-bank-account"></a>Banku konta izveide
1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Piemēram, atlasiet US-001
3. Darbību rūtī noklikšķiniet uz Debitors.
4. Noklikšķiniet uz Banku konti.
5. Noklikšķiniet uz Jauns.
6. Ierakstiet vērtību laukā Bankas konts.
7. Laukā Nosaukums ierakstiet kādu vērtību.
8. Ievadiet vērtību laukā IBAN.
9. Laukā Valūta ierakstiet kādu vērtību.
10. Noklikšķiniet uz Saglabāt.
11. Aizvērt lapu.
12. Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
15. Noklikšķiniet uz Rediģēt.
16. Izvērsiet sadaļu Papildu identifikācija.
17. Laukā Tiešā debeta ID ierakstiet kādu vērtību.
18. Ievadiet vērtību laukā IBAN.
19. Aizvērt lapu.
20. Aizvērt lapu.

## <a name="define-the-electronic-payment-method"></a>Elektroniskās maksāšanas metodes definēšana
1. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas metodes.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Maksāšanas metode.
4. Apraksta laukā ierakstiet vērtību.
5. Maksājuma tipam tiešā debeta pilnvarojuma maksāšanas metodē ir jābūt Elektroniskais maksājums.
6. Laukā Pieprasīt pilnvarojumu atlasiet Jā.
7. Aizvērt lapu.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Pievienojiet debitoram tiešā debeta pilnvarojumu.
1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Piemēram, atlasiet US-001
3. Noklikšķiniet uz Rediģēt.
4. Izvērsiet Maksāšanas noklusējuma sadaļu.
5. Laukā Maksājuma metode ievadiet vai atlasiet vērtību.
6. Izvērsiet Maksāšanas noklusējuma sadaļu.
7. Izvērsiet sadaļu Tiešā debeta pilnvarojumi.
8. Noklikšķiniet uz Pievienot.
9. Ievadiet vai atlasiet vērtību laukā Bankas konts.
10. Laukā Kreditora bankas konts, ievadiet vai atlasiet kādu vērtību.
11. Ievadiet maksājumu skaitu, kuru paredzat apstrādāt šim pilnvarojumam.
12. Noklikšķiniet uz OK.
13. Klikšķiniet Drukāt.
14. Noklikšķiniet uz Pilnvarojuma pārskats.
15. Aizvērt lapu.
16. Noklikšķiniet uz Rediģēt.
17. Ievadiet datumu laukā Parakstīšanas datums.
18. Noklikšķiniet uz Jā.
19. Ievadiet pilnvarojuma parakstīšanas vietu.
20. Noklikšķiniet uz OK.
21. Aizvērt lapu.

## <a name="create-a-free-text-invoice-with-mandate"></a>Brīvā teksta rēķina izveide ar pilnvarojumu
1. Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.
2. Noklikšķiniet uz Jauns.
3. Atlasiet debitoru, kuram pievienojāt šo pilnvarojumu.
4. Laukā Tiešā debeta pilnvarojuma ID ievadiet vai atlasiet kādu vērtību.


