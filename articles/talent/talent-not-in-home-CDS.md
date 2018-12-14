---
title: "Talent neparādās starp Microsoft Dynamics 365 programmām (CDS1.0)"
description: "Šajā tēmā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 for Talent starp Microsoft Dynamics 365 programmām."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent neparādās starp Microsoft Dynamics 365 programmām (CDS1.0)

[!include [banner](includes/banner.md)]

**Izsniegt**

Debitors neredz programmu Microsoft Dynamics 365 for Talent starp Microsoft Dynamics 365 programmām.

**Izšķirtspēja**

Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft PowerApps videi.

1. Lietotājam ar adm. ties., kam ir PowerApps 2. plāna lic., jāatver [PowerApps adm. port](https://preview.admin.powerapps.com/).
2. Atlasiet **Vides** un atlasiet pareizo vidi programmai Talent.
3. Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.

    ![Cilne Vides lomas](media/environment-roles.png)

4. Cilnē **Lietotāji** pievienojiet lietot. vai savu org.

    ![Cilne Lietotāji](media/environment-maker.png)

5. Atlasiet **Saglabāt**.
6. Lietotājam ir jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Atl. **Sinhr.**, lai atjaun. liet. pr.

    ![Poga Sinhr.](media/get-more.png)

    Kad sinhronizācija ir pabeigta, progr. Talent tiks parādīta sākumlapā.

