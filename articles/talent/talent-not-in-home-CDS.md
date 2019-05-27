---
title: Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 for Talent starp Microsoft Dynamics 365 programmām.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518601"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="774bc-103">Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="774bc-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="774bc-104">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="774bc-104">**Issue**</span></span>

<span data-ttu-id="774bc-105">Debitors neredz programmu Microsoft Dynamics 365 for Talent starp Microsoft Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="774bc-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="774bc-106">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="774bc-106">**Resolution**</span></span>

<span data-ttu-id="774bc-107">Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft PowerApps videi.</span><span class="sxs-lookup"><span data-stu-id="774bc-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="774bc-108">Lietotājam ar adm. ties., kam ir PowerApps 2. plāna lic., jāatver [PowerApps adm. port](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="774bc-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="774bc-109">Atlasiet **Vides** un atlasiet pareizo vidi programmai Talent.</span><span class="sxs-lookup"><span data-stu-id="774bc-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="774bc-110">Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="774bc-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Cilne Vides lomas](media/environment-roles.png)

4. <span data-ttu-id="774bc-112">Cilnē **Lietotāji** pievienojiet lietot. vai savu org.</span><span class="sxs-lookup"><span data-stu-id="774bc-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Cilne Lietotāji](media/environment-maker.png)

5. <span data-ttu-id="774bc-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="774bc-114">Select **Save**.</span></span>
6. <span data-ttu-id="774bc-115">Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="774bc-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="774bc-116">Atl. **Sinhr.**, lai atjaun. liet. pr.</span><span class="sxs-lookup"><span data-stu-id="774bc-116">Select **Sync** to update the user apps.</span></span>

    ![Poga Sinhr.](media/get-more.png)

    <span data-ttu-id="774bc-118">Kad sinhronizācija ir pabeigta, progr. Talent tiks parādīta sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="774bc-118">After synchronization is completed, Talent will appear on the home page.</span></span>
