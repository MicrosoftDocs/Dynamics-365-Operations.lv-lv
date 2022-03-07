---
title: Nevar izrakstīt rēķinu uz klientu vērstam pārdošanas pasūtījumam
description: Pēc opcijas Grāmatot rēķinu automātiski iespējošanas vairs nevar izrakstīt rēķinu sākotnējam pārdošanas pasūtījumam un sākotnējam tiešās piegādes pirkšanas pasūtījumam.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026707"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Nevar izrakstīt rēķinu uz klientu vērstam pārdošanas pasūtījumam

KB numurs: 4611793

## <a name="symptoms"></a>Simptomi

Pēc opcijas **Grāmatot rēķinu automātiski** iespējošanas kreditora lapā **Starpuzņēmums** vairs nevar izrakstīt rēķinu sākotnējam pārdošanas pasūtījumam un sākotnējam tiešās piegādes pirkšanas pasūtījumam.

## <a name="resolution"></a>Novēršana

Starpuzņēmumu un tiešās piegādes pasūtījumu rēķinu sinhronizācijas darbību kontrolē un izpilda parametri, kas aprakstīti sadaļā [Parametru iestatīšana starpuzņēmumu pasūtījuma grāmatošanai](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Pēc šo parametru iestatīšanas vispirms jāizraksta rēķins par starpuzņēmumu pārdošanas pasūtījumu. Tad tiks sinhronizēti sākotnējie pārdošanas pasūtījumi un pirkšanas pasūtījumi.
