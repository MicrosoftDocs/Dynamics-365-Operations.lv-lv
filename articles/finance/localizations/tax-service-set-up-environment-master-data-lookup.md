---
title: Iespējot pamatdatu uzmeklēšanu nodokļu aprēķina konfigurācijai
description: Šajā rakstā skaidrots, kā iestatīt un iespējot nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d9c234781e55fbf7f29eec14666c939d5d60e2fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879414"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Iespējot pamatdatu uzmeklēšanu nodokļu aprēķina konfigurācijai 

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt un iespējot nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti. Nolaižamajā sarakstā ir iespējams atlasīt **vērtības** nodokļu aprēķina konfigurācijā tādiem laukiem kā Juridiska persona, **Kreditora** konts, **Krājuma kods** un **Piegādes termiņš**. Šīs vērtības ir no savienotās Microsoft Dynamics 365 Finanšu vides, izmantojot Microsoft Dataverse datu avotu.

> [!NOTE] 
> Nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāte ir izvēles funkcionalitāte. Ja atspējot nodokļu pakalpojuma datu avotu atbalsta līdzekli regulēšanas **konfigurācijas Dataverse pakalpojumā (RCS), varat** izlaist tālāk norādītās darbības. Tomēr šādā gadījumā nolaižamais saraksts nebūs pieejams nodokļu aprēķina konfigurācijā.

1. Iestatīt Microsoft Power Platform integrāciju pakalpojumos Microsoft Dynamics Lifecycle Services (LCS). Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kad būsiet pabeidzis šo soli, Microsoft Power Platform vides nosaukums parādīsies **Power Platform Integrācijas** sadaļā.
2. Dodieties uz [Microsoft Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/environments) un atlasiet vides nosaukumu. Vides URL nav norādīts.
3. Iestatiet Dynamics 365 Finanses un Dataverse. Papildinformāciju skatiet sadaļā [Virtuālās entītijas risinājuma iegūšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) un [Autentifikācija un autorizācija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
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
