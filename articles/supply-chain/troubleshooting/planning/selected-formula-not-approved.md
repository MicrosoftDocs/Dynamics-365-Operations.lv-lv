---
title: Atlasītais formulas numurs nav apstiprināts partijas pasūtījumam
description: Mēģinot apstiprināt plānoto pasūtījumu, tiek saņemts kļūdas ziņojums, kurā norādīts, ka atlasītais formulas numurs nav apstiprināts partijas pasūtījumam.
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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712914"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Atlasītais formulas numurs nav apstiprināts partijas pasūtījumam

Kļūdas kods: PRO2614

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt plānoto pasūtījumu saņemsit šādu kļūdas ziņojumu:

> Atlasītais formulas cipars nav apstiprināts lietošanai partijas pasūtījumā.

## <a name="cause"></a>Iemesls

Sistēma validē apstiprināšanas darbību, lai pārliecinātos, ka aktīvajam krājumam ir pieejama apstiprināta formula. Iespējams, formula ir jāapstiprina.

## <a name="resolution"></a>Novēršana

Lai apstiprinātu formulu, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Materiālu komplekti un formulas \> Formulas**.
1. Atlasiet atbilstošo formulu.
1. Darbību rūts cilnē **Formula**, grupā **Uzturēt** atlasiet **Apstiprināt formulu**.
1. Dialoglodziņā **Apstiprināt MK vai formulu** atlasiet apstiprinātāju un pēc tam atlasiet **Labi**.
