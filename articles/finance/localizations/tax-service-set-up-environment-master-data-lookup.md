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
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="cd24a-103">Pamatdatu uzmeklēšanas vides iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cd24a-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cd24a-104">Šajā tēmā skaidrots, kā iestatīt vidi, lai lietotu nodokļu aprēķina pamatdatu uzmeklēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="cd24a-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="cd24a-105">Iestatīt Power Platform integrāciju pakalpojumos Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cd24a-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="cd24a-106">Papildinformāciju skatiet sadaļā [Microsoft Power Platform integrācija - Pievienojumprogrammas pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cd24a-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="cd24a-107">Iestatīt Dynamics 365 Finance un Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cd24a-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="cd24a-108">Papildinformāciju skatiet sadaļā [Risinājuma iegūšana](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) un [Autentifikācija un autorizācija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="cd24a-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="cd24a-109">Importēt *Priekšnosacījumu nodokļu pakalpojuma virtuālā elementa risinājumu* no [Nodokļu pakalpojuma virtuālā elementa](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="cd24a-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="cd24a-110">Iestatiet Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="cd24a-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="cd24a-111">Izveidojiet pakalpojuma pieprasījumu korporācijai Microsoft, lai nodrošinātu šādu līdzekļu testējamā varianta sniegšanu:</span><span class="sxs-lookup"><span data-stu-id="cd24a-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="cd24a-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="cd24a-112">ERCdsFeature</span></span>
      - <span data-ttu-id="cd24a-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="cd24a-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="cd24a-114">Pakalpojumā Finance atvēriet darbvietu **Līdzekļu pārvaldība** un iespējojiet tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="cd24a-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="cd24a-115">(Priekšskatījums) Elektronisko pārskatu izrakstīšanas Dataverse datu avotu atbalsts</span><span class="sxs-lookup"><span data-stu-id="cd24a-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="cd24a-116">(Priekšskatījums) nodokļu pakalpojuma Dataverse datu avotu atbalsts</span><span class="sxs-lookup"><span data-stu-id="cd24a-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="cd24a-117">(Priekšskatījums) Globalizācijas līdzekļi</span><span class="sxs-lookup"><span data-stu-id="cd24a-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="cd24a-118">Piesakieties RCS, izmantojot nomnieka administratora kontu.</span><span class="sxs-lookup"><span data-stu-id="cd24a-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="cd24a-119">Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Savienotie pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="cd24a-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="cd24a-120">Atlasiet **Jauns**, lai pievienotu ierakstu, un ievadiet tālāk norādīto lauka informāciju.</span><span class="sxs-lookup"><span data-stu-id="cd24a-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="cd24a-121">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="cd24a-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="cd24a-122">Laukā **Veids** atlasiet **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="cd24a-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="cd24a-123">Laukā **Pieteikums** ievadiet jūsu Dataverse URL.</span><span class="sxs-lookup"><span data-stu-id="cd24a-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="cd24a-124">Laukā **Nomnieks** ievadiet savu nomnieku.</span><span class="sxs-lookup"><span data-stu-id="cd24a-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="cd24a-125">Laukā **Pielāgotais URL** ievadiet savu Dataverse URL un pievienojiet to ar "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="cd24a-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="cd24a-126">Atlasiet **Pārbaudīt savienojumu** un pabeidziet savienojuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="cd24a-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="cd24a-127">[![Pārbaudīt savienojuma pogu](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="cd24a-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="cd24a-128">Dodieties uz **Elektronisko pārskatu izrakstīšana** > **Nodokļa konfigurācijas** un importējiet nodokļu konfigurācijas no [Nodokļu konfigurācijām](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="cd24a-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="cd24a-129">[![Nodokļu konfigurācijas lapa, nodokļu datu modeļa koks](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="cd24a-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="cd24a-130">Ja izmantojat Microsoft konfigurāciju, dodieties uz **Ar nodokli apliekamo dokumentu modeļu kartēšanu** vai **Dataverse modeļu kartēšanu**, un laukā **Saistītais pieteikums** atlasiet ierakstu, ko izveidojāt 7. darbībā.</span><span class="sxs-lookup"><span data-stu-id="cd24a-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="cd24a-131">Iestatiet **Noklusējums modeļu kartēšanai** kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="cd24a-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="cd24a-132">[![Modeļu kartēšanas lapa](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="cd24a-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
