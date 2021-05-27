---
title: Saskaņošanas iemeslu dēļ kā kredīta kontu var pievienot tikai galveno kontu
description: Kad transportēšanas pārvaldībā iestatāt saskaņošanas iemeslu, tikai galveno kontu var pievienot kā kredīta kontu.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026697"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Saskaņošanas iemeslu dēļ kā kredīta kontu var pievienot tikai galveno kontu

KB numurs: 4603538

## <a name="symptoms"></a>Simptomi

Kad transportēšanas pārvaldībā iestatāt saskaņošanas iemeslu, tikai galveno kontu var pievienot kā kredīta kontu. Kā kredīta kontu nevar pievienot izmaksu centru vai jebkādu citu dimensiju. Tomēr debeta konts ļauj atlasīt citas dimensijas.

## <a name="resolution"></a>Novēršana

Ja saskaņošana nav veikta, lai maksātu kreditoram, bet lai kreditētu noteiktu galveno kontu, sistēma neļauj jums atlasīt kredīta konta finanšu dimensiju, kad ir iestatīts saskaņošanas iemesls.

Ja konta struktūrai kredīta galvenajam kontam nepieciešama specifiska finanšu dimensijas vērtība, iegūto kreditoru žurnālu nevar grāmatot automātiski, jo trūkst finanšu dimensijas vērtības. Tāpēc jums vispirms ir manuāli jānorāda kredīta konts, izmantojot **Rēķinu žurnāla** lapu.

Tā kā kredīta kontam ir nepieciešama dimensijas vērtība, kreditoru rēķinu žurnālu nevar automātiski grāmatot. Pēc tam, kad manuāli pievienojat dimensijas vērtību galvenajam kontam kredīta rindai, tā ir jāgrāmato manuāli.
