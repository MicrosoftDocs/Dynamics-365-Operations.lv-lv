--- 
title: "Pirkšanas pasūtījuma izveide vienreizējam piegādātājam"
description: "Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Pirkšanas pasūtījuma izveide vienreizējam piegādātājam

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam. Piegādātājs tiek automātiski izveidots ar pirkšanas pasūtījumu, nevis kreditora konts ir jāizveido manuāli. Pirkuma pasūtījumu parasti veic iepirkuma aģenti. Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF. Pastāv priekšnosacījums, kas vienreizējā kreditora kontam ir jābūt iestatītam lapā Kreditoru parametri.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Pirkšanas pasūtījuma izveide vienreizējam piegādātājam
1. Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Atlasiet Jā laukā Vienreizējs piegādātājs.
    * Kreditora konts tiek automātiski izveidots un piešķirts pirkšanas pasūtījumam. Kreditora konts tiek izveidots, pamatojoties uz veidni, kas ir norādīta kreditoru parametru lapas cilnē Vispārīgi.  
4. Laukā Nosaukums ierakstiet nosaukumu šim piegādātājam.
5. Noklikšķiniet uz OK.
    * Pirkšanas pasūtījumu tagad var pabeigt un apstrādāt tāpat kā jebkuru citu pasūtījumu. Ar veidu, kā tas tiek darīts, nav saistīta neviena izteikta īpašība. Rēķins ņems vērā veicamu transakciju uz kreditora kontu, kas tika izveidota ar šo pasūtījumu, un pēc tam tiks apstrādāts maksājums. Kad tas ir pabeigts, kreditora kontu var dzēst. Parasti to dara kreditoru departaments.  


