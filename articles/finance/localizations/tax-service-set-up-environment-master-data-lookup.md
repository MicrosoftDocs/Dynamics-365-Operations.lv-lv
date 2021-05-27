---
title: Pamatdatu uzmeklēšanas vides iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021348"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Pamatdatu uzmeklēšanas vides iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.

1. Iestatīt Power Platform integrāciju pakalpojumos Lifecycle Services (LCS). Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Iestatīt Dynamics 365 Finance un Microsoft Dataverse. Papildinformāciju skatiet sadaļā [Risinājuma iegūšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) un [Autentifikācija un autorizācija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Iestatiet šādus elementus. Plašāku informāciju skatiet sadaļā [Virtuālo elementu iespējošana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressCityEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. Iestatiet Dynamics 365 Regulatory Configuration Service (RCS). 
5. Izveidojiet pakalpojuma pieprasījumu korporācijai Microsoft, lai nodrošinātu šādu līdzekļu testējamā varianta sniegšanu:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. Atvēriet darbvietu **Līdzekļu pārvaldība** un iespējojiet tālāk norādītos līdzekļus.

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
