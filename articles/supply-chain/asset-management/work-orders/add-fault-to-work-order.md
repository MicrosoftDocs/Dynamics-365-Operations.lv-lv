---
title: Kļūmes pievienošana darba pasūtījumam
description: Šajā tēmā ir paskaidrots, kā pievienot kļūmes reģistrācijas darba pasūtījumiem programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875782"
---
# <a name="add-fault-to-work-order"></a>Kļūmes pievienošana darba pasūtījumam

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Kļūmju noformētājā iestatītās kļūmes varat pievienot darba pasūtījumam. Darba pasūtījumā atlasītajam līdzeklim jāsatur līdzekļu veidi, kam piesaistīts viens vai vairāki kļūdas ieraksti. Vairāk par iestatīšanu lasiet sadaļā [Kļūmju pārvaldība](../setup-for-work-orders/fault-management.md).

1. Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Sarakstā atlasiet darba pasūtījumu, kuram vēlaties veikt kļūmes reģistrāciju, un noklikšķiniet uz **Līdzekļa kļūme**.

3. Kopsavilkuma cilnē **Simptomi** noklikšķiniet uz **Pievienot rindu**. Laukā **Kļūme** automātiski tiek ievadīts kļūmes kārtas numurs.

4. Laukā **Kļūmes simptoms** atlasiet attiecīgo kļūmes simptomu.

5. Atlasiet **Kļūmes joma** un **Kļūmes veids**.

6. Laukā **Kļūmes datums** automātiski tiek ievadīts esošais datums. Var atlasīt arī citu datumu, ja vajadzīgs.

7. Kopsavilkuma cilnē **Atlasītā simptoma iemesli** pievienojiet rindu, kura aprakstīts problēmas iemesls.

8. Kopsavilkuma cilnē **Atlasītā simptoma labojumi** pievienojiet rindu, kurā aprakstīts iespējamais problēmas risinājums.

9. Noklikšķiniet uz **Saglabāt**.

![1. attēls](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Līdzekļa kļūmju skatīšana

Sarakstā **Līdzekļu kļūmes** ir pārskats par visām līdzekļiem reģistrētajām kļūmēm.

Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**, lai atvērtu sarakstu.


## <a name="print-asset-fault-report"></a>Līdzekļu kļūmju pārskata izdrukāšana

Saraksta **Visi līdzekļi** lapā varat izdrukāt līdzekļu kļūmju pārskatu, kas parāda visas kļūmju reģistrācijas un kļūmju statistikas grafisko pārskatu.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi**.

2. Sarakstā **Līdzekļi** atlasiet līdzekli, kuram vēlaties izdrukāt kļūmju pārskatu.

3. Cilnē **Vispārīgi** > **Pārskatu sadaļā** klikšķiniet uz **Līdzekļa kļūme**.

4. Ievadiet konkrētu periodu vai izvēlieties kļūmes veidu.

5. Noklikšķiniet **Labi**, lai izdrukātu atskaiti.

>[!NOTE]
>Var izdrukāt arī kļūmju pārskatu vairākiem līdzekļiem vai līdzekļu- veidiem, klikšķinot uz **Līdzekļu pārvaldība** > **Pārskati** > **Līdzekļi** > **Līdzekļu kļūmes**.

