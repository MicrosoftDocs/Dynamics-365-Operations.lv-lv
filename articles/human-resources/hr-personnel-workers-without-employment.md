---
title: Nodarbinātie bez nodarbinātības
description: Darbinieki, kuriem nav turpmākas, aktīvas vai vēsturiskas nodarbinātības jūsu organizācijā, parādās veidlapā Darbinieki bez nodarbinātības.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924575"
---
# <a name="workers-without-employment"></a>Nodarbinātie bez nodarbinātības

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbinieki, kuriem nav turpmākas, aktīvas vai vēsturiskas nodarbinātības jūsu organizācijā, parādās veidlapā **Darbinieki bez nodarbinātības**. Darbinieki ar šādu statusu var parādīties, ja importējat darbiniekus bez nodarbinātības ieraksta vai ja dzēšat darbinieka nodarbinātību, izmantojot **Darbinieki > Nodarbinātības vēsture**.

Pēc noklusējuma veidlapa **Darbinieki bez nodarbinātības** ir pieejama ar šādām lomām:

- Personāla vadības asistents
- Personāla vadības vadītājs
- Personāla atlases darbinieks
- Atlīdzību un atvieglojumu vadītājs
- Algu administrators
- Algu vadītājs
- Apmācības vadītājs

Sarakstā **Darbinieki bez nodarbinātības** varat dzēst uzskaitītās personas. Pēc noklusējuma šī privilēģija tiek piešķirta Human Resources asistenta lomai. Varat piešķirt šo privilēģiju citām lomām, izmantojot šādas darbības:

1. Atlasiet **Sistēmas administrēšana** un pēc tam atlasiet **Drošības konfigurēšana**.

2. Cilnē **Privilēģijas** filtrējiet sarakstu **Privilēģijas** **Uzturēt darbiniekus**.

   [![Filtrēt privilēģiju sarakstu](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Kolonnā **Atsauces** atlasiet **Displeja izvēlnes elementi**.

4. Kolonnā **Displeja izvēlnes vienumi** atlasiet **HcmWorkersWithoutEmployment**.

   [![Atlasīt formu](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Iestatiet **Dzēšanas** atļauju uz **Piešķirt**.

6. Atlasiet cilni **Nepublicētie objekti**.

7. Atlasiet **Publicēt visus**.

   [![Publicēt izmaiņas](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]