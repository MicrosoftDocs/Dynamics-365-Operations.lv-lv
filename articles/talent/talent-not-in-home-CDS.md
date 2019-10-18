---
title: Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitors neredz programmu Microsoft Dynamics 365 Talent starp Microsoft Dynamics 365 programmām.
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
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009380"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="0436b-103">Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="0436b-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0436b-104">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="0436b-104">**Issue**</span></span>

<span data-ttu-id="0436b-105">Debitors neredz programmu Microsoft Dynamics 365 Talent starp Microsoft Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="0436b-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="0436b-106">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="0436b-106">**Resolution**</span></span>

<span data-ttu-id="0436b-107">Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft PowerApps videi.</span><span class="sxs-lookup"><span data-stu-id="0436b-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="0436b-108">Lietotājam ar administratora tiesībām, kam ir PowerApps 2. plāna licence, jāatver [PowerApps administrēšanas portāls](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="0436b-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="0436b-109">Atlasiet **Vides** un atlasiet pareizo vidi programmai Talent.</span><span class="sxs-lookup"><span data-stu-id="0436b-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="0436b-110">Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="0436b-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Cilne Vides lomas](media/environment-roles.png)

4. <span data-ttu-id="0436b-112">Cilnē **Lietotāji** pievienojiet lietot. vai savu org.</span><span class="sxs-lookup"><span data-stu-id="0436b-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Cilne Lietotāji](media/environment-maker.png)

5. <span data-ttu-id="0436b-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0436b-114">Select **Save**.</span></span>
6. <span data-ttu-id="0436b-115">Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="0436b-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="0436b-116">Atl. **Sinhr.**, lai atjaun. liet. pr.</span><span class="sxs-lookup"><span data-stu-id="0436b-116">Select **Sync** to update the user apps.</span></span>

    ![Poga Sinhr.](media/get-more.png)

    <span data-ttu-id="0436b-118">Kad sinhronizācija ir pabeigta, progr. Talent tiks parādīta sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="0436b-118">After synchronization is completed, Talent will appear on the home page.</span></span>
