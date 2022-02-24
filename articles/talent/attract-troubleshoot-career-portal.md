---
title: Attract lietotāji nevar pieteikties darbiem karjeras portālā
description: Šajā tēmā ir paskaidrots, kā novērst problēmu, ja Attract lietotāji nevar pieteikties darbiem no karjeras portāla.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461842"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract lietotāji nevar pieteikties darbiem karjeras portālā

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Izsniegt

Attract lietotāji nevar pieteikties darbiem karjeras portālā. Kad tie mēģina pieteikties darbam, kas tika izveidots programmā Dynamics 365 Talent: Attract, pārlūkprogramma ielādē lapu nepārtraukti, un darbība netiek pabeigta.

## <a name="cause"></a>Iemesls

Šī problēma rodas, kad Talent Relationship grupai nav Talent lietotāja lomas.

## <a name="resolution"></a>Novēršana

Piešķiriet Talent lietotāja lomu Talent Relationship grupai.

1. Piesakieties [Power Platform administrēšanas centrā](https://admin.powerplatform.microsoft.com), izmantojot jebkuru no šiem administratora akreditācijas datiem:

   - Dynamics 365 administrators
   - Globālais administrators
   - Power Platform administrators

2. Navigācijas rūtī atlasiet **Vides** un pēc tam atlasiet vidi, kurā piešķirt Talent lietotāja lomu Talent Relationship grupai.

   ![Atlasīt vidi](./media/attract-troubleshoot-career-portal-select-environment.png)

3. Rūtī **Vides** atlasiet **Vides URL** un piesakieties vides administrēšanas portālā (piemēram, https:<orgname>. crm.dynamics.com).

4. Atlasiet **Iestatījumi**, atlasiet **Sistēma** un pēc tam atlasiet **Drošība**.

   ![Naviģēt uz Drošību](./media/attract-troubleshoot-career-portal-security.png)

5. Atlasiet **Komandas**.

   ![Atlasiet Komandas](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Meklēšanas lodziņā meklējiet **Talent Relationship grupa** un pēc tam atlasiet grupu no meklēšanas rezultātiem.

7. Izvēlieties **PĀRVALDĪT LOMAS** no lentes.

8. Dialoglodziņā **Pārvaldīt grupas lomas** atlasiet **Talent lietotājs** no pieejamo lomu saraksta un pēc tam atlasiet **Labi**, lai pielietotu lomu.

   ![Lietot lomu](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Pārbaudiet izmaiņas:

   1. Ieejiet karjeras portālā no jauna pārlūka loga.
   2. Piesakieties darbam no karjeras portāla. 