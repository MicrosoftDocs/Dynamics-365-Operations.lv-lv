---
title: Pamatdatu uzmeklēšanas vides iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869082"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Pamatdatu uzmeklēšanas vides iestatīšana

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.

1. Iestatīt Power Platform integrāciju pakalpojumos Lifecycle Services (LCS). Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Iestatīt Dynamics 365 Finance un Microsoft Dataverse. Papildinformāciju skatiet sadaļā [Risinājuma iegūšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) un [Autentifikācija un autorizācija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Importēt *Priekšnosacījumu nodokļu pakalpojuma virtuālā elementa risinājumu* no [Nodokļu pakalpojuma virtuālā elementa](https://go.microsoft.com/fwlink/?linkid=2158160).
4. Iestatiet Dynamics 365 Regulatory Configuration Service (RCS). 
5. Izveidojiet pakalpojuma pieprasījumu korporācijai Microsoft, lai nodrošinātu šādu līdzekļu testējamā varianta sniegšanu:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Pakalpojumā Finance atvēriet darbvietu **Līdzekļu pārvaldība** un iespējojiet tālāk norādītos līdzekļus.

      - (Priekšskatījums) Elektronisko pārskatu izrakstīšanas Dataverse datu avotu atbalsts
      - (Priekšskatījums) nodokļu pakalpojuma Dataverse datu avotu atbalsts
      - (Priekšskatījums) Globalizācijas līdzekļi

5. Piesakieties RCS, izmantojot nomnieka administratora kontu.
6. Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Savienotie pieteikumi**. 
7. Atlasiet **Jauns**, lai pievienotu ierakstu, un ievadiet tālāk norādīto lauka informāciju. 

   - Laukā **Nosaukums** ievadiet nosaukumu.
   - Laukā **Veids** atlasiet **Dataverse**.
   - Laukā **Pieteikums** ievadiet jūsu Dataverse URL.
   - Laukā **Nomnieks** ievadiet savu nomnieku.
   - Laukā **Pielāgotais URL** ievadiet savu Dataverse URL un pievienojiet to ar "/api/data/v9.1".

8. Atlasiet **Pārbaudīt savienojumu** un pabeidziet savienojuma izveidi. 

   [![Pārbaudīt savienojuma pogu](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Nodokļa konfigurācijas** un importējiet nodokļu konfigurācijas no [Nodokļu konfigurācijām](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Nodokļu konfigurācijas lapa, nodokļu datu modeļa koks](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Ja izmantojat Microsoft konfigurāciju, dodieties uz **Ar nodokli apliekamo dokumentu modeļu kartēšanu** vai **Dataverse modeļu kartēšanu**, un laukā **Saistītais pieteikums** atlasiet ierakstu, ko izveidojāt 7. darbībā.
11. Iestatiet **Noklusējums modeļu kartēšanai** kā **Jā**.

   [![Modeļu kartēšanas lapa](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
