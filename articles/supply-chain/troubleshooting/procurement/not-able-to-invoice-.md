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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756755"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Nevar izrakstīt rēķinu uz klientu vērstam pārdošanas pasūtījumam

KB numurs: 4611793

## <a name="symptoms"></a>Simptomi

Pēc opcijas **Grāmatot rēķinu automātiski** iespējošanas kreditora lapā **Starpuzņēmums** vairs nevar izrakstīt rēķinu sākotnējam pārdošanas pasūtījumam un sākotnējam tiešās piegādes pirkšanas pasūtījumam.

## <a name="resolution"></a>Novēršana

Starpuzņēmumu un tiešās piegādes pasūtījumu rēķinu sinhronizācijas darbību kontrolē un izpilda parametri, kas aprakstīti sadaļā [Parametru iestatīšana starpuzņēmumu pasūtījuma grāmatošanai](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Pēc šo parametru iestatīšanas vispirms jāizraksta rēķins par starpuzņēmumu pārdošanas pasūtījumu. Tad tiks sinhronizēti sākotnējie pārdošanas pasūtījumi un pirkšanas pasūtījumi.
