---
title: Lai plānoto ražošanas pasūtījumu varētu apstiprināt, tas ir jāplāno
description: Mēģinot apstiprināt plānoto pasūtījumu, tiek parādīts kļūdas ziņojums, ka pasūtījums ir jāplāno pirms tā apstiprināšanas.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777747"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Lai plānoto ražošanas pasūtījumu varētu apstiprināt, tas ir jāplāno

Kļūdas kods: SYS309802

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt plānoto pasūtījumu saņemsit šādu kļūdas ziņojumu:

> Plānotajam ražošanas pasūtījumam ir jābūt plānotam, pirms to var apstiprināt.

## <a name="cause"></a>Iemesls

Plānotie sākuma un beigu datumi nedrīkst būt tukši.

## <a name="resolution"></a>Novēršana

Lai norādītu plānotā pasūtījuma sākuma un beigu datumus, izpildiet šīs darbības.

1. Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**.
1. Atveriet attiecīgo plānoto pasūtījumu.
1. Kopsavilkuma cilnes **Vispārīgi** sadaļā **Plānots** norādiet datumus laukos **Sākuma datums** un **Beigu datums**.
