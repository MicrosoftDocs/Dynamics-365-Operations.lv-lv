---
title: Tiešā debeta pilnvarojuma izveide debitoram
description: Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bbf3703941255dfd82b8fb501ba8a9d1f3a2ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835080"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Tiešā debeta pilnvarojuma izveide debitoram

[!include [banner](../../includes/banner.md)]

Šajā uzdevumu ceļvedī parādīts, kā izveidot tiešā debeta pilnvarojumu un izmantot to rēķinā.


## <a name="create-a-bank-account"></a>Banku konta izveide
1. **Navigācijas rūtī** ejiet uz sadaļu **Moduļi > Debitori > Klienti > Visi klienti**.
2. Sarakstā atlasiet ierakstu. Piemēram, atlasiet US-001
3. Darbību rūtī noklikšķiniet uz **Klients**.
4. Noklikšķiniet uz **Bankas konti**.
5. Klikšķiniet **Jauns**.
6. Laukā **Bankas konts** ierakstiet vērtību.
7. Laukā **Nosaukums** ierakstiet kādu vērtību.
8. Laukā **IBAN** ievadiet vērtību.
9. Laukā **Valūta** ierakstiet vērtību.
10. Noklikšķiniet uz **Saglabāt**.
11. Aizvērt lapu.
12. **Navigācijas rūtī** pārejiet uz **Moduļi > Naudas un bankas pārvaldība > Bankas konti > Bankas konti**.
13. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
14. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
15. Noklikšķiniet uz **Rediģēt**.
16. Izvērsiet kopsavilkuma cilni **Papildu identifikācija**.
17. Laukā **Tiešā debeta ID** ierakstiet vērtību.
18. Laukā **IBAN** ievadiet vērtību.
19. Aizvērt lapu.
20. Aizvērt lapu.

## <a name="define-the-electronic-payment-method"></a>Elektroniskās maksāšanas metodes definēšana
1. **Navigācijas rūtī** pārejiet uz **Moduļi > Debitori > Maksājumu iestatīšana > Maksāšanas veidi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Maksāšanas veids** ievadiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Maksājuma veids** ievadiet „Elektroniskais maksājums”. Maksājuma tipam tiešā debeta pilnvarojuma maksāšanas metodē ir jābūt Elektroniskais maksājums.
6. Atlasiet „Jā” laukā **Prasīt pilnvarojumu**.
7. Aizvērt lapu.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Pievienojiet debitoram tiešā debeta pilnvarojumu.
1. **Navigācijas rūtī** ejiet uz sadaļu **Moduļi > Debitori > Klienti > Visi klienti**.
2. Sarakstā atlasiet ierakstu. Piemēram, atlasiet US-001
3. Noklikšķiniet uz **Rediģēt**.
4. Izvērsiet kopsavilkuma cilni **Maksājumu kavējumi**.
5. Ievadiet vai atlasiet vērtību laukā **Maksājuma metode**.
6. Izvērsiet kopsavilkuma cilni **Maksājumu kavējumi**.
7. Izvērsiet kopsavilkuma cilni **Tiešā debeta pilnvarojumi**.
8. Noklikšķiniet uz **Pievienot**.
9. Ievadiet vai atlasiet vērtību laukā **Bankas konts**.
10. Ievadiet vai atlasiet vērtību laukā **Kreditora bankas konts**.
11. Laukā **Maksājumu biežums** ievadiet maksājumu skaitu, ko paredzat apstrādāt šim pilnvarojumam.
12. Noklikšķiniet uz **Labi**.
13. Noklikšķiniet uz **Drukāt**.
14. Noklikšķiniet uz **Pilnvarojuma atskaite**.
15. Aizvērt lapu.
16. Noklikšķiniet uz **Rediģēt**.
17. Laukā **Paraksta datums** ievadiet datumu.
18. Noklikšķiniet uz pogas **Jā**.
19. Ievadiet pilnvarojuma parakstīšanas vietu.
20. Noklikšķiniet uz **Labi**.
21. Aizvērt lapu.

## <a name="create-a-free-text-invoice-with-mandate"></a>Brīvā teksta rēķina izveide ar pilnvarojumu
1. **Navigācijas rūtī** ejiet uz **Moduļi > Debitori > Rēķini > Visi brīva teksta rēķini**.
2. Klikšķiniet **Jauns**.
3. Atlasiet debitoru, kuram pievienojāt šo pilnvarojumu.
4. Ievadiet vai atlasiet vērtību laukā **Tiešā debeta pilnvarojuma ID**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]