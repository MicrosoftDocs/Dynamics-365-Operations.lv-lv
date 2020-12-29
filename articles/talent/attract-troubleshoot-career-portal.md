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
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="cd069-103">Attract lietotāji nevar pieteikties darbiem karjeras portālā</span><span class="sxs-lookup"><span data-stu-id="cd069-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="cd069-104">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="cd069-104">Issue</span></span>

<span data-ttu-id="cd069-105">Attract lietotāji nevar pieteikties darbiem karjeras portālā.</span><span class="sxs-lookup"><span data-stu-id="cd069-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="cd069-106">Kad tie mēģina pieteikties darbam, kas tika izveidots programmā Dynamics 365 Talent: Attract, pārlūkprogramma ielādē lapu nepārtraukti, un darbība netiek pabeigta.</span><span class="sxs-lookup"><span data-stu-id="cd069-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="cd069-107">Iemesls</span><span class="sxs-lookup"><span data-stu-id="cd069-107">Cause</span></span>

<span data-ttu-id="cd069-108">Šī problēma rodas, kad Talent Relationship grupai nav Talent lietotāja lomas.</span><span class="sxs-lookup"><span data-stu-id="cd069-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="cd069-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="cd069-109">Resolution</span></span>

<span data-ttu-id="cd069-110">Piešķiriet Talent lietotāja lomu Talent Relationship grupai.</span><span class="sxs-lookup"><span data-stu-id="cd069-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="cd069-111">Piesakieties [Power Platform administrēšanas centrā](https://admin.powerplatform.microsoft.com), izmantojot jebkuru no šiem administratora akreditācijas datiem:</span><span class="sxs-lookup"><span data-stu-id="cd069-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="cd069-112">Dynamics 365 administrators</span><span class="sxs-lookup"><span data-stu-id="cd069-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="cd069-113">Globālais administrators</span><span class="sxs-lookup"><span data-stu-id="cd069-113">Global admin</span></span>
   - <span data-ttu-id="cd069-114">Power Platform administrators</span><span class="sxs-lookup"><span data-stu-id="cd069-114">Power Platform admin</span></span>

2. <span data-ttu-id="cd069-115">Navigācijas rūtī atlasiet **Vides** un pēc tam atlasiet vidi, kurā piešķirt Talent lietotāja lomu Talent Relationship grupai.</span><span class="sxs-lookup"><span data-stu-id="cd069-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Atlasīt vidi](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="cd069-117">Rūtī **Vides** atlasiet **Vides URL** un piesakieties vides administrēšanas portālā (piemēram, https:<orgname>. crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="cd069-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="cd069-118">Atlasiet **Iestatījumi**, atlasiet **Sistēma** un pēc tam atlasiet **Drošība**.</span><span class="sxs-lookup"><span data-stu-id="cd069-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Naviģēt uz Drošību](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="cd069-120">Atlasiet **Komandas**.</span><span class="sxs-lookup"><span data-stu-id="cd069-120">Select **Teams**.</span></span>

   ![Atlasiet Komandas](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="cd069-122">Meklēšanas lodziņā meklējiet **Talent Relationship grupa** un pēc tam atlasiet grupu no meklēšanas rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="cd069-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="cd069-123">Izvēlieties **PĀRVALDĪT LOMAS** no lentes.</span><span class="sxs-lookup"><span data-stu-id="cd069-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="cd069-124">Dialoglodziņā **Pārvaldīt grupas lomas** atlasiet **Talent lietotājs** no pieejamo lomu saraksta un pēc tam atlasiet **Labi**, lai pielietotu lomu.</span><span class="sxs-lookup"><span data-stu-id="cd069-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Lietot lomu](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="cd069-126">Pārbaudiet izmaiņas:</span><span class="sxs-lookup"><span data-stu-id="cd069-126">Test your changes:</span></span>

   1. <span data-ttu-id="cd069-127">Ieejiet karjeras portālā no jauna pārlūka loga.</span><span class="sxs-lookup"><span data-stu-id="cd069-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="cd069-128">Piesakieties darbam no karjeras portāla.</span><span class="sxs-lookup"><span data-stu-id="cd069-128">Apply for the job from the career portal.</span></span> 