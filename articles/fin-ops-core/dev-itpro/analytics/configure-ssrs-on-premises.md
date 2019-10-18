---
title: SQL Server pārskatu izveides pakalpojumu konfigurēšana lokāliem izvietojumiem
description: Šajā tēmā ir sniegta informācija par SQL Server pārskatu izveides pakalpojumu (SSRS) konfigurēšanu lokālam izvietojumam.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: bb6e8a55c9bee4e60c3a627409d2fbe3b8915196
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174240"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="cffdb-103">SQL Server pārskatu izveides pakalpojumu konfigurēšana lokāliem izvietojumiem</span><span class="sxs-lookup"><span data-stu-id="cffdb-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cffdb-104">Izmantojiet šajā tēmā aprakstītās darbības, lai konfigurētu SQL Server Reporting Services (SSRS) savā Microsoft Dynamics 365 Finance + Operations (lokālajā) izvietojumā.</span><span class="sxs-lookup"><span data-stu-id="cffdb-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="cffdb-105">Atveriet programmu Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="cffdb-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="cffdb-106">Atstājiet noklusējuma vērtības laukā **Servera nosaukums**, kam ir jābūt pašreizējās mašīnas nosaukumam, un laukā **Pārskatu servera instance** — **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="cffdb-107">Noklikšķiniet uz **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-107">Click **Connect**.</span></span>

    <span data-ttu-id="cffdb-108">[![Pārskatu izveides pakalpojumu konfigurācijas savienojums](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="cffdb-109">Noklikšķiniet uz cilnes **Pakalpojuma konts** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="cffdb-110">[![Cilne Pakalpojuma konts](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="cffdb-111">Noklikšķiniet uz cilnes **Tīmekļa pakalpojuma URL** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="cffdb-112">[![Cilne Tīmekļa pakalpojuma URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="cffdb-113">Noklikšķiniet uz cilnes **Datu bāze** un pārliecinieties, vai **Datu bāzes nosaukums** un **Akreditācijas datu iestatījumi** atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cffdb-114">Jums būs jāizveido jauna datu bāze.</span><span class="sxs-lookup"><span data-stu-id="cffdb-114">You will need to create a new database.</span></span> <span data-ttu-id="cffdb-115">Lai to izdarītu, noklikšķiniet uz **Mainīt datu bāzi** un pēc tam pārbaudiet, vai jaunās datu bāzes nosaukums ir **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="cffdb-116">[![Cilne Datu bāze](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="cffdb-117">Noklikšķiniet uz cilnes **Tīmekļa portāla URL** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cffdb-118">Jums ir jānoklikšķina uz **Lietot**, lai izveidotu un pareizi konfigurētu portālu.</span><span class="sxs-lookup"><span data-stu-id="cffdb-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="cffdb-119">[![Cilne Tīmekļa portāla URL](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="cffdb-120">Pēc portāla konfigurēšanas cilne **Tīmekļa portāls** atbildīs tālāk esošajā attēlā redzamajai.</span><span class="sxs-lookup"><span data-stu-id="cffdb-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="cffdb-121">[![Cilne Tīmekļa portāls](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="cffdb-122">Noklikšķiniet uz pārskatu URL, lai skatītu SQL Server pārskatu izveides pakalpojumu tīmekļa portālu.</span><span class="sxs-lookup"><span data-stu-id="cffdb-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="cffdb-123">Kad esat portālā, izveidojiet jaunu mapi ar nosaukumu **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="cffdb-124">[![Mape Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="cffdb-125">Programmā **Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieks** noklikšķiniet uz cilnes **E-pasta iestatījumi** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="cffdb-126">[![Cilne E-pasta iestatījumi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="cffdb-127">Noklikšķiniet uz cilnes **Izpildes konts** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="cffdb-128">[![Cilne Izpildes konts](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="cffdb-129">Nemainiet cilnes **Šifrēšanas atslēgas** noklusējuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="cffdb-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="cffdb-130">[![Cilne Šifrēšanas atslēgas](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="cffdb-131">Noklikšķiniet uz cilnes **Abonēšanas iestatījumi** un pārbaudiet, vai iestatījumi atbilst tālāk esošajā attēlā redzamajiem.</span><span class="sxs-lookup"><span data-stu-id="cffdb-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="cffdb-132">[![Cilne Abonēšanas iestatījumi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="cffdb-133">Nemainiet cilnes **Paplašināma izvietošana** noklusējuma iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="cffdb-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="cffdb-134">[![Cilne Paplašināma izvietošana](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="cffdb-135">Nemainiet noklusējuma iestatījumus cilnē **Power BI integrācija**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="cffdb-136">[![Cilne Power BI integrācija](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="cffdb-137">Noklikšķiniet uz **Iziet**, lai aizvērtu programmu **Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieks**.</span><span class="sxs-lookup"><span data-stu-id="cffdb-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="cffdb-138">[![Pārskatu izveides pakalpojumu konfigurācijas pārvaldnieka aizvēršana](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="cffdb-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
