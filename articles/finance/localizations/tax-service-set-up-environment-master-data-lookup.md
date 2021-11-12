---
title: Pamatdatu uzmeklēšanas vides iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 10/26/2021
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
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700408"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Pamatdatu uzmeklēšanas vides iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.

1. Iestatīt Microsoft Power Platform integrāciju pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kad būsiet pabeidzis šo soli, Microsoft Power Platform vides nosaukums parādīsies **Power Platform Integrācijas** sadaļā.
2. Dodieties uz [Microsoft Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/environments) un atlasiet vides nosaukumu. Vides URL nav norādīts.
3. Iestatīt Dynamics 365 Finance un Dataverse. Papildinformāciju skatiet sadaļā [Virtuālās entītijas risinājuma iegūšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) un [Autentifikācija un autorizācija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Iestatiet šādus elementus. Plašāku informāciju skatiet sadaļā [Virtuālo Microsoft Dataverse elementu iespējošana](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

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

5. Regulatory configuration service (RCS) iestatīšana. Atvēriet darbvietu **Līdzekļu pārvaldība** un iespējojiet tālāk norādītos līdzekļus:

    - Elektronisko pārskatu izrakstīšanas Dataverse datu avotu atbalsts
    - Nodokļu pakalpojuma Dataverse datu avotu atbalsts
    - Globalizācijas līdzekļi

6. Piesakieties RCS, izmantojot nomnieka administratora kontu.
7. Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Savienotie pieteikumi**. 
8. Atlasiet **Jauns**, lai pievienotu ierakstu, un ievadiet tālāk norādīto lauka informāciju. 

    - Laukā **Nosaukums** ievadiet nosaukumu.
    - Laukā **Veids** atlasiet **Dataverse**.
    - Laukā **Pieteikums** ievadiet jūsu Dataverse URL.
    - Laukā **Nomnieks** ievadiet savu nomnieku.
    - Laukā **Pielāgotais URL** ievadiet savu Dataverse URL un pievienojiet to ar "/api/data/v9.1".

9. Atlasiet **Pārbaudīt savienojumu** un pabeidziet savienojuma izveidi. 

    [![Pārbaudīt savienojuma pogu.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Nodokļa konfigurācijas** un importējiet nodokļu konfigurācijas no [Nodokļu konfigurācijām](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Nodokļu konfigurācijas lapa, nodokļu datu modeļa koks.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Ja izmantojat Microsoft konfigurāciju, dodieties uz **Ar nodokli apliekamo dokumentu modeļu kartēšanu** vai **Dataverse modeļu kartēšanu**, un laukā **Saistītais pieteikums** atlasiet ierakstu, ko izveidojāt 7. darbībā.
12. Iestatiet **Noklusējums modeļu kartēšanai** kā **Jā**.

    [![Modeļu kartēšanas lapa.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
