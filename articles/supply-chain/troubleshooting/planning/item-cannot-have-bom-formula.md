---
title: Krājumam nevar būt MK vai formula
description: Mēģinot apstiprināt pasūtījumu, krājuma validācijas laikā tiek parādīts kļūdas ziņojums. Tas norāda, ka krājumam nevar būt materiālu komplekts (MK) vai formula.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294128"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Krājumam nevar būt MK vai formula

Kļūdas kods: PRO2614

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt pasūtījumu, krājuma validācijas laikā tiek parādīts šis kļūdas ziņojums:

> Krājums nedrīkst saturēt MK formulu

## <a name="resolution"></a>Novēršana

Krājumiem, kuriem ir materiālu komplekts (MK) vai formula, jābūt tipam *Plānošanas krājums*, *MK* vai *formula*. Lai mainītu krājuma tipu, veiciet šādas darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet attiecīgo preci.
1. Kopsavilkuma cilnē **Inženieris** iestatiet lauku **Ražošanas veids** uz *Plānošanas krājums*, *MK* vai *formula*.
