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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719555"
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
