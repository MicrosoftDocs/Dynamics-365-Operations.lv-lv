---
title: Drošības diagnostika uzdevumu ierakstiem
description: Šajā rakstā ir sniegta informācija, kā analizēt un pārvaldīt drošības atļauju prasības, balstoties uz uzdevumu ierakstīšanu.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272526"
---
# <a name="security-diagnostics-for-task-recordings"></a>Drošības diagnostika uzdevumu ierakstiem

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Pirms sākšanas

Šajā rakstā ir sniegta informācija, kā analizēt un pārvaldīt drošības atļauju prasības, balstoties uz uzdevumu ierakstīšanu. Pirms izpildīsiet šajā rakstā aprakstītās darbības, jums nepieciešams veikt biznesa procesa uzdevumu ierakstīšanu, ko vēlaties analizēt. Lai reģistrētu biznesa procesu, skatiet [Uzdevumu reģistrētāja resursi](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Pārvaldīt uzdevuma reģistrēšanas drošību

1. Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Drošības diagnostikas uzdevumu reģistrēšanai**.
2. Atveriet uzdevumu reģistrēšanu no tā atrašanās vietas. Atlasiet **Atvērt no šī datora** vai **Atvērt no Lifecycle Services** un pēc tam atlasiet **Aizvērt**.
3. Tādējādi tiks atvērta **Drošības izvēlnes krājuma detalizētas informācijas** lapa, kas uzskaita šim procesam vajadzīgos drošības objektus.

 > [!NOTE]
 > Izvēlnes elementi **Darbība** un **Izvade** nav iekļauti sarakstā.

4. Laukā **Lietotāja ID** atlasiet lietotāju. Ja lietotājam nav atļauju atsevišķiem izvēlnes elementiem, lauks **Trūkstošās atļaujas** tiks atjaunināts uz **Jā**.
  
  ![Drošības izvēlnes krājuma detalizētas informācijas lapa.](../media/Security-Menu-Item-Details.png)

5. Atlasiet **Pievienot atsauci**, lai skatītu drošības objektu sarakstu, iekļaujot lomas, pienākumus un privilēģijas, kas piešķir trūkstošo atļauju.
6. Izvēlieties drošības objektu no saraksta:

    - Ja ir izvēlēta **Loma**, atlasiet **Pievienot lomu lietotājam**. Tas atvērs lapu **Piešķirt lietotājus lomām**. Papildinformāciju skatiet lapu [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).
    - Ja ir izvēlēts **Pienākums**, atlasiet **Pievienot pienākumu lomai**, atlasiet lomas, kurām jāpievieno pienākums, un pēc tam atlasiet **Labi**.
    - Ja ir izvēlēts **Privilēģija**, atlasiet **Pievienot privilēģiju pienākumiem**, atlasiet lomas, kurām jāpievieno pienākums, un pēc tam atlasiet **Labi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
