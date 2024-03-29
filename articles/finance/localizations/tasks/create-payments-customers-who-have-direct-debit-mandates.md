---
title: Maksājumu izveide debitoram ar tiešā debeta mandātiem
description: Šajā procedūrā parādīts, kā izveidot ISO20022 tiešā debeta maksājuma failu debitoram, kuram ir konfigurēts tiešais debets un ir apmaksājams rēķins.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ecc28cb11b8c34a438bb47b1cfa9a37e17297e421020b32030261af95b86a49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757938"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Maksājumu izveide debitoram ar tiešā debeta mandātiem

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā izveidot ISO20022 tiešā debeta maksājuma failu debitoram, kuram ir konfigurēts tiešais debets un ir apmaksājams rēķins. Rēķina izveide un grāmatošana nav obligāta. Apmaksājama rēķina vietā, jūs, pirms maksājuma faila ģenerēšanas, varat atlasīt pilnvarojumu žurnālā, lai atbalstītu debitoru priekšapmaksas gadījumā.



Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.



Šis ir piektā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas. Lai varētu pabeigt šo uzdevumu, jums ir jāpabeidz iepriekšējie uzdevumi. Vispirms jāimportē debitora maksājumu elektronisko pārskatu veidošanas konfigurācijas, jākonfigurē maksājumu metode un jāiestata uzņēmuma un debitora informācija. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Brīva teksta rēķina ar tiešā debeta informāciju grāmatošana
1. Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet DE-010.  
4. Laukā Maksājuma metode ievadiet vai atlasiet vērtību.
    * Piemēram, atlasiet elektronisks.  
5. Laukā Tiešā debeta pilnvarojuma ID ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Pievienot rindu.
7. Laukā Apraksts ierakstiet kādu vērtību.
8. Laukā Galvenais konts norādiet vēlamās vērtības.
9. Laukā Vienības cena ievadiet kādu skaitli.
10. Noklikšķiniet uz Grāmatot.
11. Noklikšķiniet uz OK.

## <a name="create-a-payment"></a>Maksājuma izveidošana
1. Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz Rindas.
5. Noklikšķiniet uz Maksājuma priekšlikums.
6. Noklikšķiniet uz Izveidot maksājuma priekšlikumu.
7. Izvērsiet sadaļu Iekļaujamie ieraksti.
8. Noklikšķiniet uz Filtrēt.
9. Sarakstā atlasiet rindu, kas attiecas uz klienta darījumu tabulu, un lauku Maksājuma metode.
    * Jūs varat lietot visus kritērijus, atlasot debitoru transakcijas, kas jāapmaksā. Šajā piemērā izmantojiet Elektronisks kā maksājuma metodi, lai filtrētu darījumus.  
10. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
11. Noklikšķiniet uz Labi.
12. Noklikšķiniet uz Labi.
13. Noklikšķiniet uz Izveidot maksājumus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]