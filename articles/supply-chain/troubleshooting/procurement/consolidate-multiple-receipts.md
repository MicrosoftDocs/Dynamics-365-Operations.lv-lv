---
title: Nav iespējams konsolidēt vairākas preču kvītis vienā pirkuma pasūtījumā
description: Nevar konsolidēt vairāku produktu ieejas plūsmas vienā pirkšanas pasūtījumā, ja dažādām produktu ieejas plūsmu rindām ir dažādi uzskaites datumi.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476953"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Nav iespējams konsolidēt vairākas preču kvītis vienā pirkuma pasūtījumā

## <a name="symptoms"></a>Simptomi

Nevar konsolidēt vairāku produktu ieejas plūsmas vienā pirkšanas pasūtījumā, ja dažādām produktu ieejas plūsmu rindām ir dažādi uzskaites datumi.

## <a name="resolution"></a>Novēršana

Agrākajās Dynamics 365 Supply Chain Management versijās konsolidēšana šādā situācijā bija atļauta. Tomēr praksē pastāv nosliece uz kļūdu. Izveidotais pirkšanas pasūtījuma rindu uzskaites datums nedrīkst atšķirties no uzskaites datuma produktu ieejas plūsmas rindās, no kurām tika izveidotas šīs pirkšanas pasūtījuma rindas. (Pirkšanas pasūtījuma rindu uzskaites datums atbilst uzskaites datumam pirkšanas pasūtījuma galvenē.) Tāpēc vairāku produktu ieejas plūsmu konsolidēšana vienā pirkšanas pasūtījumā vairs netiek atļauta.

Uzskaites datums tiek izmantots, piemēram, budžeta rezervācijām un apgrūtinājumam. Tāpēc tas jāsaglabā pārejas periodā no produktu ieejas plūsmas uz pirkšanas pasūtījumu.
