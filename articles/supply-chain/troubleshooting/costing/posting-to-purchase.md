---
title: Pirkumu uzkrājums, kam ir nulles summa, tiek grāmatots nulles vērtības produktu ieejas plūsmai
description: Kad tiek grāmatota produktu ieejas plūsma ar nulles vērtību, sistēma izveido pirkumu uzkrājumu grāmatošanu, kur summa ir 0 (nulle).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722179"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Pirkumu uzkrājums, kam ir nulles summa, tiek grāmatots nulles vērtības produktu ieejas plūsmai

KB numurs: 4612588

## <a name="symptoms"></a>Simptomi

Kad tiek grāmatota produktu ieejas plūsma ar nulles vērtību, sistēma izveido pirkumu uzkrājumu grāmatošanu, kur summa ir 0 (nulle).

## <a name="resolution"></a>Novēršana

Pēc noklusējuma *Purchase, accrual* tipa virsgrāmatas grāmatošanai lauks `IsTransferredIndetail` vienmēr tiek iestatīts uz *Kopsavilkums* apakšgrāmatu darījumos. Tāpēc sistēma izveido saistītu dokumenta ierakstu, pat ja summa ir 0 (nulle).

Lai izlaistu šo grāmatošanas tipu, ja summa ir 0 (nulle), paplašiniet `subledgerJournalizer.markDoNotTransferEntries` metodi tā, lai tā iekļauj `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, kā parādīts piemērā.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
