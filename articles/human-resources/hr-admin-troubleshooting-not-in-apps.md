---
title: Human Resources neparādās Microsoft Dynamics 365 programmās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f90af26483cf82de57cbe8dd4237b39b281786804557319d5f6a7fc407027523
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782124"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources neparādās Microsoft Dynamics 365 programmās

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izejas plūsma**

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