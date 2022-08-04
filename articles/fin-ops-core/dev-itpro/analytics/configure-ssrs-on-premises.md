---
title: SQL Server pārskatu izveides pakalpojumu konfigurēšana lokāliem izvietojumiem
description: Šajā rakstā ir sniegta informācija par SQL servera pārskata pakalpojumu (SSRS) konfigurēšanu lokālai izvietošanai.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.custom:
- "55651"
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 5608d3cca15f7d6dbc8feb672ec8cec5227c0c47
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205634"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>SQL Server pārskatu izveides pakalpojumu konfigurēšana lokāliem izvietojumiem

[!include [banner](../includes/banner.md)]

Izmantojiet šajā rakstā norādītās darbības, lai konfigurētu SQL Server pārskatu izveides pakalpojumus (SSRS) jūsu izvietošanai Microsoft Dynamics 365 Finance + Operations (on-premises).

1. Atveriet programmu Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieks.
2. Atstājiet noklusējuma vērtības laukā **Servera nosaukums**, kam ir jābūt pašreizējās mašīnas nosaukumam, un laukā **Pārskatu servera instance** — **MSSQLSERVER**.
3. Noklikšķiniet uz **Savienot**.

    [![Pārskatu izveides pakalpojumu konfigurācijas savienojums.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Noklikšķiniet uz cilnes **Pakalpojuma konts** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.

    [![Cilne Pakalpojuma konts.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Noklikšķiniet uz cilnes **Tīmekļa pakalpojuma URL** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.

    [![Cilne Tīmekļa pakalpojuma URL.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Noklikšķiniet uz cilnes **Datu bāze** un pārliecinieties, vai **Datu bāzes nosaukums** un **Akreditācijas datu iestatījumi** atbilst tālāk esošajā attēlā redzamajiem.

    > [!NOTE]
    > Jums būs jāizveido jauna datu bāze. Lai to izdarītu, noklikšķiniet uz **Mainīt datu bāzi** un pēc tam pārbaudiet, vai jaunās datu bāzes nosaukums ir **DynamicsAxReportServer**.

    [![Cilne Datu bāze.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Noklikšķiniet uz cilnes **Tīmekļa portāla URL** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.

    > [!NOTE]
    > Jums ir jānoklikšķina uz **Lietot**, lai izveidotu un pareizi konfigurētu portālu.

    [![Cilne Tīmekļa portāla URL.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Pēc portāla konfigurēšanas cilne **Tīmekļa portāls** atbildīs tālāk esošajā attēlā redzamajai.

    [![Cilne Tīmekļa portāls.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Noklikšķiniet uz pārskatu URL, lai skatītu SQL Server pārskatu izveides pakalpojumu tīmekļa portālu.
9. Kad esat portālā, izveidojiet jaunu mapi ar nosaukumu **Dynamics**.

    [![Mape Dynamics.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Programmā **Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieks** noklikšķiniet uz cilnes **E-pasta iestatījumi** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.

    [![Cilne E-pasta iestatījumi.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Noklikšķiniet uz cilnes **Izpildes konts** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.

    [![Cilne Izpildes konts.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Nemainiet cilnes **Šifrēšanas atslēgas** noklusējuma iestatījumus.

    [![Cilne Šifrēšanas atslēgas.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Noklikšķiniet uz cilnes **Abonēšanas iestatījumi** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.

    [![Cilne Abonēšanas iestatījumi.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Nemainiet cilnes **Paplašināma izvietošana** noklusējuma iestatījumus.

    [![Cilne Paplašināma izvietošana.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Nemainiet noklusējuma iestatījumus cilnē **Power BI integrācija**.

    [![Cilne Power BI integrācija.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Noklikšķiniet uz **Iziet**, lai aizvērtu programmu **Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieks**.

    [![Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieka aizvēršana.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
