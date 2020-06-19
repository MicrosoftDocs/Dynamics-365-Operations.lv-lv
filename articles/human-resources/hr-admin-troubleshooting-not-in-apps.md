---
title: Human Resources neparādās Microsoft Dynamics 365 programmās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf47b4673e1c97965bba7728e5669b7639c4d56
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431088"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources neparādās Microsoft Dynamics 365 programmās

**Izejas plūsma**

Debitors neredz Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.

**Novēršana**

Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft Power Apps videi.

1. Lietotājam ar administratora tiesībām, kam ir Power Apps 2. plāna licence, jāatver [Power Apps administrēšanas portāls](https://preview.admin.powerapps.com/).

2. Atlasiet **Vides** un atlasiet pareizo vidi Human Resources.

3. Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.

    ![Cilne Vides lomas](media/environment-roles.png)

4. Cilnē **Lietotāji** pievienojiet lietot. vai savu org.

    ![Cilne Lietotāji](media/environment-maker.png)

5. Atlasiet **Saglabāt**.

6. Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Atl. **Sinhr.**, lai atjaun. liet. pr.

    ![Poga Sinhr.](media/get-more.png)

    Kad sinhronizācija ir pabeigta, Human Resources tiks parādīta sākumlapā.
