---
title: Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 Talent starp Microsoft Dynamics 365 programmām.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009380"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Problēma**

Debitors neredz programmu Microsoft Dynamics 365 Talent starp Microsoft Dynamics 365 programmām.

**Izšķirtspēja**

Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft PowerApps videi.

1. Lietotājam ar administratora tiesībām, kam ir PowerApps 2. plāna licence, jāatver [PowerApps administrēšanas portāls](https://preview.admin.powerapps.com/).
2. Atlasiet **Vides** un atlasiet pareizo vidi programmai Talent.
3. Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.

    ![Cilne Vides lomas](media/environment-roles.png)

4. Cilnē **Lietotāji** pievienojiet lietot. vai savu org.

    ![Cilne Lietotāji](media/environment-maker.png)

5. Atlasiet **Saglabāt**.
6. Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Atl. **Sinhr.**, lai atjaun. liet. pr.

    ![Poga Sinhr.](media/get-more.png)

    Kad sinhronizācija ir pabeigta, progr. Talent tiks parādīta sākumlapā.
