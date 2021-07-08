---
title: Atceltas produktu ieejas plūsmas neatjaunina darbības statusu uz Reģistrētas
description: Pēc produktu ieejas plūsmu atcelšanas saņemšanas kravā, sistēma automātiski atjaunina krājumu transakcijas statusu no Saņemts uz Pasūtīts.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294126"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Atceltas produktu ieejas plūsmas neatjaunina darbības statusu uz Reģistrētas

## <a name="symptoms"></a>Simptomi

Pēc darbības **Atcelt produktu ieejas plūsmas** palaišanas ienākošā kravā, sistēma automātiski atjaunina krājumu transakciju statusu no *Saņemts* uz *Pasūtīts*.

## <a name="resolution"></a>Novēršana

Kad pavadzīmes ir atceltas izejošām kravām, krājumu darbību statuss paliek *Izdots*. Tomēr, kad produktu ieejas plūsmas no ienākošās krāvas tiek atceltas, krājumu transakciju statuss netiek atjaunots uz *Reģistrēts*. Tādēļ pēc tam, kad produktu ieejas plūsma no ienākošās kravas ir atcelta, noliktavas darbiniekam ir atkārtoti jāreģistrē kravu krājumu daudzumi.

Papildinformāciju skatiet sadaļā [Reģistrēt krājumu daudzumus, kas tiek saņemti ar ienākošo kravu](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
