---
title: Produktu ieejas plūsmas dokumenta numurs tiek patērēts pat tad, ja dokuments netiek ģenerēts
description: Produktu ieejas plūsmas dokumenta numurs tiek patērēts pat tad, ja nav izveidots finanšu dokuments produktu ieejas plūsmas laikā
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
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476978"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Produktu ieejas plūsmas dokumenta numurs tiek patērēts pat tad, ja dokuments netiek ģenerēts

## <a name="symptoms"></a>Simptomi

Produktu ieejas plūsmas dokumenta numurs tiek patērēts pat tad, ja nav izveidots finanšu dokuments produktu ieejas plūsmas laikā.

## <a name="resolution"></a>Novēršana

Ja krājumu modeļu grupu opcija **Uzkrāt saistības produktu ieejas plūsmā** ir iestatīta uz *Nē*, grāmatošana Virsgrāmatā netiks veikta. Tomēr fizisks notikums tiks ierakstīts, lai veiktu uzskaiti apakšgrāmatā, un šim notikumam nepieciešams dokumenta numurs. Šis dokumenta numurs ir dokumenta numurs, uz kuru ir atsauce krājumu darījumā.

Ieteicams iestatīt opciju **Uzkrāt saistības produktu ieejas plūsmā** uz *Jā*, kā aprakstīts šajā emuāra ierakstā: [Papildmaksu grāmatošana produktu ieejas plūsmas laikā](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
