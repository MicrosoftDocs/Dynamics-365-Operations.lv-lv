---
title: Darbs nav bloķēts
description: Darbs nav bloķēts
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924208"
---
# <a name="work-isnt-blocked"></a>Darbs nav bloķēts

Kļūdas kods: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Darbs ar ID %1 nav bloķēts.

## <a name="cause"></a>Iemesls

Opcija **Bloķēts kopums** kopumam ir iestatīta uz *Nē*. Darbu nevar atbloķēt, jo pašlaik tas nav bloķēts.

## <a name="resolution"></a>Novēršana

 Atbloķēt var tikai, ja opcija **Bloķēts kopums** ir iestatīta uz *Jā*.
