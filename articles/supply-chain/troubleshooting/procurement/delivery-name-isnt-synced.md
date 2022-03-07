---
title: Piegādes saņēmēja nosaukums netiek sinhronizēts pēc pirkuma pasūtījuma piegādes adreses maiņas
description: Pēc piegādes saņēmēja adreses maiņas pirkuma pasūtījuma galvenē, piegādes saņēmēja nosaukums netiek sinhronizēts
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
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476952"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Piegādes saņēmēja nosaukums netiek sinhronizēts pēc pirkuma pasūtījuma piegādes adreses maiņas

## <a name="symptoms"></a>Simptomi

Pirkšanas pasūtījuma galvenē norādītā adrese tiek atjaunināta uz adresi, kas nav piegādes adrese. Lai gan adrese tiek atjaunināta pirkšanas pasūtījumā, piegādes nosaukums netiek atjaunināts, pamatojoties uz atjaunināto adresi.

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. Atlasītā adrese ir jāklasificē kā piegādes adrese. Pretējā gadījumā piegādes nosaukums netiek atjaunināts, pamatojoties uz atlasīto adresi.
