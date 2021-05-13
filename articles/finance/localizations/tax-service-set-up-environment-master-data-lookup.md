---
title: Pamatdatu uzmeklēšanas vides iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.
author: kai-cloud
ms.date: 04/21/2021
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
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924158"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="a22ab-103">Pamatdatu uzmeklēšanas vides iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a22ab-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a22ab-104">Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="a22ab-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="a22ab-105">Iestatīt Power Platform integrāciju pakalpojumos Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a22ab-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="a22ab-106">Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a22ab-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="a22ab-107">Iestatīt Dynamics 365 Finance un Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a22ab-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="a22ab-108">Papildinformāciju skatiet sadaļā [Risinājuma iegūšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) un [Autentifikācija un autorizācija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="a22ab-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="a22ab-109">Iestatiet šādus elementus.</span><span class="sxs-lookup"><span data-stu-id="a22ab-109">Set up the following entities.</span></span> <span data-ttu-id="a22ab-110">Plašāku informāciju skatiet sadaļā [Virtuālo elementu iespējošana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="a22ab-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="a22ab-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="a22ab-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-112">CurrencyEntity</span></span>
      - <span data-ttu-id="a22ab-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="a22ab-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="a22ab-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="a22ab-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="a22ab-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="a22ab-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="a22ab-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="a22ab-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="a22ab-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="a22ab-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="a22ab-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="a22ab-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="a22ab-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="a22ab-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="a22ab-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="a22ab-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="a22ab-125">Iestatiet Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="a22ab-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="a22ab-126">Izveidojiet pakalpojuma pieprasījumu korporācijai Microsoft, lai nodrošinātu šādu līdzekļu testējamā varianta sniegšanu:</span><span class="sxs-lookup"><span data-stu-id="a22ab-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="a22ab-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="a22ab-127">ERCdsFeature</span></span>
      - <span data-ttu-id="a22ab-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="a22ab-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="a22ab-129">Atvēriet darbvietu **Līdzekļu pārvaldība** un iespējojiet tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="a22ab-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="a22ab-130">(Priekšskatījums) Elektronisko pārskatu izrakstīšanas Dataverse datu avotu atbalsts</span><span class="sxs-lookup"><span data-stu-id="a22ab-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="a22ab-131">(Priekšskatījums) nodokļu pakalpojuma Dataverse datu avotu atbalsts</span><span class="sxs-lookup"><span data-stu-id="a22ab-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="a22ab-132">(Priekšskatījums) Globalizācijas līdzekļi</span><span class="sxs-lookup"><span data-stu-id="a22ab-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="a22ab-133">Piesakieties RCS, izmantojot nomnieka administratora kontu.</span><span class="sxs-lookup"><span data-stu-id="a22ab-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="a22ab-134">Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Savienotie pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="a22ab-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="a22ab-135">Atlasiet **Jauns**, lai pievienotu ierakstu, un ievadiet tālāk norādīto lauka informāciju.</span><span class="sxs-lookup"><span data-stu-id="a22ab-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="a22ab-136">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a22ab-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="a22ab-137">Laukā **Veids** atlasiet **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="a22ab-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="a22ab-138">Laukā **Pieteikums** ievadiet jūsu Dataverse URL.</span><span class="sxs-lookup"><span data-stu-id="a22ab-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="a22ab-139">Laukā **Nomnieks** ievadiet savu nomnieku.</span><span class="sxs-lookup"><span data-stu-id="a22ab-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="a22ab-140">Laukā **Pielāgotais URL** ievadiet savu Dataverse URL un pievienojiet to ar "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="a22ab-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="a22ab-141">Atlasiet **Pārbaudīt savienojumu** un pabeidziet savienojuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="a22ab-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="a22ab-142">[![Pārbaudīt savienojuma pogu](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="a22ab-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="a22ab-143">Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Nodokļa konfigurācijas** un importējiet nodokļu konfigurācijas no [Nodokļu konfigurācijām](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="a22ab-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="a22ab-144">[![Nodokļu konfigurācijas lapa, nodokļu datu modeļa koks](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="a22ab-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="a22ab-145">Ja izmantojat Microsoft konfigurāciju, dodieties uz **Ar nodokli apliekamo dokumentu modeļu kartēšanu** vai **Dataverse modeļu kartēšanu**, un laukā **Saistītais pieteikums** atlasiet ierakstu, ko izveidojāt 7. darbībā.</span><span class="sxs-lookup"><span data-stu-id="a22ab-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="a22ab-146">Iestatiet **Noklusējums modeļu kartēšanai** kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a22ab-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="a22ab-147">[![Modeļu kartēšanas lapa](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="a22ab-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
