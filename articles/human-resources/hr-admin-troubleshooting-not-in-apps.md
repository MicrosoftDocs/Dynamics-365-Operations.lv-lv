---
title: Human Resources neparādās Microsoft Dynamics 365 programmās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009880"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="eeaa0-103">Human Resources neparādās Microsoft Dynamics 365 programmās</span><span class="sxs-lookup"><span data-stu-id="eeaa0-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="eeaa0-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="eeaa0-104">**Issue**</span></span>

<span data-ttu-id="eeaa0-105">Debitors neredz Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="eeaa0-106">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="eeaa0-106">**Resolution**</span></span>

<span data-ttu-id="eeaa0-107">Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft Power Apps videi.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="eeaa0-108">Lietotājam ar administratora tiesībām, kam ir Power Apps 2. plāna licence, jāatver [Power Apps administrēšanas portāls](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="eeaa0-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="eeaa0-109">Atlasiet **Vides** un atlasiet pareizo vidi Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="eeaa0-110">Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Cilne Vides lomas](media/environment-roles.png)

4. <span data-ttu-id="eeaa0-112">Cilnē **Lietotāji** pievienojiet lietot. vai savu org.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Cilne Lietotāji](media/environment-maker.png)

5. <span data-ttu-id="eeaa0-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-114">Select **Save**.</span></span>

6. <span data-ttu-id="eeaa0-115">Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="eeaa0-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="eeaa0-116">Atl. **Sinhr.**, lai atjaun. liet. pr.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-116">Select **Sync** to update the user apps.</span></span>

    ![Poga Sinhr.](media/get-more.png)

    <span data-ttu-id="eeaa0-118">Kad sinhronizācija ir pabeigta, Human Resources tiks parādīta sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="eeaa0-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
