---
title: "Talent neparādās starp Microsoft Dynamics 365 programmām (CDS1.0)"
description: "Šajā tēmā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 for Talent starp Microsoft Dynamics 365 programmām."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="c5aa6-103">Talent neparādās starp Microsoft Dynamics 365 programmām (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="c5aa6-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5aa6-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="c5aa6-104">**Issue**</span></span>

<span data-ttu-id="c5aa6-105">Debitors neredz programmu Microsoft Dynamics 365 for Talent starp Microsoft Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="c5aa6-106">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="c5aa6-106">**Resolution**</span></span>

<span data-ttu-id="c5aa6-107">Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft PowerApps videi.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="c5aa6-108">Lietotājam ar adm. ties., kam ir PowerApps 2. plāna lic., jāatver [PowerApps adm. port](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="c5aa6-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="c5aa6-109">Atlasiet **Vides** un atlasiet pareizo vidi programmai Talent.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="c5aa6-110">Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Cilne Vides lomas](media/environment-roles.png)

4. <span data-ttu-id="c5aa6-112">Cilnē **Lietotāji** pievienojiet lietot. vai savu org.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Cilne Lietotāji](media/environment-maker.png)

5. <span data-ttu-id="c5aa6-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-114">Select **Save**.</span></span>
6. <span data-ttu-id="c5aa6-115">Lietotājam ir jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="c5aa6-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="c5aa6-116">Atl. **Sinhr.**, lai atjaun. liet. pr.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-116">Select **Sync** to update the user apps.</span></span>

    ![Poga Sinhr.](media/get-more.png)

    <span data-ttu-id="c5aa6-118">Kad sinhronizācija ir pabeigta, progr. Talent tiks parādīta sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="c5aa6-118">After synchronization is completed, Talent will appear on the home page.</span></span>
