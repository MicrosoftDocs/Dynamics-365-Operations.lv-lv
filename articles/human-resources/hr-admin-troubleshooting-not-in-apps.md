---
title: Human Resources neparādās Microsoft Dynamics 365 programmās
description: Šajā tēmā ir izskaidrots, ko darīt, ja programma Microsoft Dynamics 365 Human Resources nav uzskaitīta starp Microsoft Dynamics 365 programmām.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfed82463eece882bed66c7b2dac1dd30e04720e
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413405"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Programma Human Resources netiek parādīta Microsoft Dynamics 365 programmās

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Problēma**

Debitors neredz Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.

**Novēršana**

Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft Power Apps videi.

1. Lietotājam ar administratora tiesībām, kam ir Power Apps 2. plāna licence, jāatver [Power Apps administrēšanas portāls](https://preview.admin.powerapps.com/).

2. Atlasiet **Vides** un atlasiet pareizo vidi Human Resources.

3. Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.

    ![Cilne Vides lomas.](media/environment-roles.png)

4. Cilnē **Lietotāji** pievienojiet lietot. vai savu org.

    ![Cilne Lietotāji.](media/environment-maker.png)

5. Atlasiet **Saglabāt**.

6. Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Atl. **Sinhr.**, lai atjaun. liet. pr.

    ![Poga Sinhr.](media/get-more.png)

    Kad sinhronizācija ir pabeigta, Human Resources tiks parādīta sākumlapā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
