---
title: Human Resources neparādās Microsoft Dynamics 365 programmās
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: d78199cf0e76ffd0676a26961a8e646938dc7333
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113453"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="d25a7-103">Human Resources neparādās Microsoft Dynamics 365 programmās</span><span class="sxs-lookup"><span data-stu-id="d25a7-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="d25a7-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="d25a7-104">**Issue**</span></span>

<span data-ttu-id="d25a7-105">Debitors neredz Dynamics 365 Human Resources starp Microsoft Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="d25a7-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="d25a7-106">**Novēršana**</span><span class="sxs-lookup"><span data-stu-id="d25a7-106">**Resolution**</span></span>

<span data-ttu-id="d25a7-107">Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft Power Apps videi.</span><span class="sxs-lookup"><span data-stu-id="d25a7-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="d25a7-108">Lietotājam ar administratora tiesībām, kam ir Power Apps 2. plāna licence, jāatver [Power Apps administrēšanas portāls](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="d25a7-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="d25a7-109">Atlasiet **Vides** un atlasiet pareizo vidi Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d25a7-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="d25a7-110">Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="d25a7-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Cilne Vides lomas](media/environment-roles.png)

4. <span data-ttu-id="d25a7-112">Cilnē **Lietotāji** pievienojiet lietot. vai savu org.</span><span class="sxs-lookup"><span data-stu-id="d25a7-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Cilne Lietotāji](media/environment-maker.png)

5. <span data-ttu-id="d25a7-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d25a7-114">Select **Save**.</span></span>

6. <span data-ttu-id="d25a7-115">Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="d25a7-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="d25a7-116">Atl. **Sinhr.**, lai atjaun. liet. pr.</span><span class="sxs-lookup"><span data-stu-id="d25a7-116">Select **Sync** to update the user apps.</span></span>

    ![Poga Sinhr.](media/get-more.png)

    <span data-ttu-id="d25a7-118">Kad sinhronizācija ir pabeigta, Human Resources tiks parādīta sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="d25a7-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
