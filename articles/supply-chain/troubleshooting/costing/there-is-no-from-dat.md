---
title: Krājumu cenu lapas cilnē Aktīvās cenas nav vērtības Sākuma datuma
description: Krājumu cenu lapas cilnē Aktīvās cenas nav vērtības Sākuma datuma.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026726"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Krājumu cenu lapas cilnē Aktīvās cenas nav vērtības Sākuma datuma

KB numurs: 4613548

## <a name="symptoms"></a>Simptomi

**Krājumu cenu** lapas cilnē **Aktīvās cenas** nav vērtības **Sākuma datuma**.

## <a name="resolution"></a>Novēršana

**Sākuma datuma** vērtība (spēkā stāšanās datums), kas ir iestatīts uz gaidošo cenu, netiek pārvietots uz aktīvo cenu.

Kad krājuma izmaksu ieraksts tiek ievadīts pirmo reizi, tā statuss ir *Gaidošs* un tam ir plānotais spēkā stāšanās datums. Kad aktivizējat krājuma izmaksu ierakstu, šis statuss tiek atjaunināts uz *Aktīvs* un spēka stāšanās datums tiek atjaunināts uz aktivizēšanas datumu. Tāpēc aktīvās cenas aktivizēšanas datums vienmēr ir faktiskais aktivizēšanas datums.

Papildinformāciju skatiet tēmā [Izmaksu versiju pārskats](../../cost-management/costing-versions.md).
