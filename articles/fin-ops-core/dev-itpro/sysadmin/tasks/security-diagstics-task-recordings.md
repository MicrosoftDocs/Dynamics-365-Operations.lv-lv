---
title: Drošības diagnostika uzdevumu reģistrēšanai
description: Šajā tēmā sniegta informācija par to, kā analizēt un pārvaldīt drošības atļaujas prasības, pamatojoties uz uzdevuma reģistrāciju.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 4aecda7e0d604b70dec58a4f5bb2992fe7e0a5e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982434"
---
# <a name="security-diagnostics-for-task-recordings"></a>Drošības diagnostika uzdevumu reģistrēšanai

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Pirms sākšanas

Šajā tēmā sniegta informācija par to, kā analizēt un pārvaldīt drošības atļaujas prasības, pamatojoties uz uzdevuma reģistrāciju. Pirms šajā tēmā aprakstīto darbību veikšanas jums ir jābūt uzdevuma reģistrēšanai biznesa procesiem, ko vēlaties analizēt. Lai reģistrētu biznesa procesu, skatiet [Uzdevumu reģistrētāja resursi](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Pārvaldīt uzdevuma reģistrēšanas drošību

1. Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Drošības diagnostikas uzdevumu reģistrēšanai**.
2. Atveriet uzdevumu reģistrēšanu no tā atrašanās vietas. Atlasiet **Atvērt no šī datora** vai **Atvērt no Lifecycle Services** un pēc tam atlasiet **Aizvērt**.
3. Tādējādi tiks atvērta **Drošības izvēlnes krājuma detalizētas informācijas** lapa, kas uzskaita šim procesam vajadzīgos drošības objektus.

 > [!NOTE]
 > Izvēlnes elementi **Darbība** un **Izvade** nav iekļauti sarakstā.

4. Laukā **Lietotāja ID** atlasiet lietotāju. Ja lietotājam nav atļauju atsevišķiem izvēlnes elementiem, lauks **Trūkstošās atļaujas** tiks atjaunināts uz **Jā**.
  
  ![Drošības izvēlnes krājuma detalizētas informācijas lapa](../media/Security-Menu-Item-Details.png)

5. Atlasiet **Pievienot atsauci**, lai skatītu drošības objektu sarakstu, iekļaujot lomas, pienākumus un privilēģijas, kas piešķir trūkstošo atļauju.
6. Izvēlieties drošības objektu no saraksta:

    - Ja ir izvēlēta **Loma**, atlasiet **Pievienot lomu lietotājam**. Tas atvērs lapu **Piešķirt lietotājus lomām**. Papildinformāciju skatiet lapu [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).
    - Ja ir izvēlēts **Pienākums**, atlasiet **Pievienot pienākumu lomai**, atlasiet lomas, kurām jāpievieno pienākums, un pēc tam atlasiet **Labi**.
    - Ja ir izvēlēts **Privilēģija**, atlasiet **Pievienot privilēģiju pienākumiem**, atlasiet lomas, kurām jāpievieno pienākums, un pēc tam atlasiet **Labi**.
