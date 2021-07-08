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
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294124"
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
