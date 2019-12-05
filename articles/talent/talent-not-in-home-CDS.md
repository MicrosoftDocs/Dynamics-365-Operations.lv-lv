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
ms.openlocfilehash: 7f0cc1c7ec1234b7eedaade0ffadb66965ed2121
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772992"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="dba62-103">Programma Talent nav redzama starp Microsoft Dynamics 365 programmām (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="dba62-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dba62-104">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="dba62-104">**Issue**</span></span>

<span data-ttu-id="dba62-105">Debitors neredz programmu Microsoft Dynamics 365 Talent starp Microsoft Dynamics 365 programmām.</span><span class="sxs-lookup"><span data-stu-id="dba62-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="dba62-106">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="dba62-106">**Resolution**</span></span>

<span data-ttu-id="dba62-107">Lietotājs ir jāpievieno lomai Vides veidotājs programmas Microsoft Power Apps videi.</span><span class="sxs-lookup"><span data-stu-id="dba62-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="dba62-108">Lietotājam ar administratora tiesībām, kam ir Power Apps 2. plāna licence, jāatver [Power Apps administrēšanas portāls](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="dba62-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="dba62-109">Atlasiet **Vides** un atlasiet pareizo vidi programmai Talent.</span><span class="sxs-lookup"><span data-stu-id="dba62-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="dba62-110">Cilnē **Drošība**, cilnē **Vides lomas** atlasiet **Vides veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="dba62-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Cilne Vides lomas](media/environment-roles.png)

4. <span data-ttu-id="dba62-112">Cilnē **Lietotāji** pievienojiet lietot. vai savu org.</span><span class="sxs-lookup"><span data-stu-id="dba62-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Cilne Lietotāji](media/environment-maker.png)

5. <span data-ttu-id="dba62-114">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="dba62-114">Select **Save**.</span></span>
6. <span data-ttu-id="dba62-115">Lietotājam jāpierakstās [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="dba62-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="dba62-116">Atl. **Sinhr.**, lai atjaun. liet. pr.</span><span class="sxs-lookup"><span data-stu-id="dba62-116">Select **Sync** to update the user apps.</span></span>

    ![Poga Sinhr.](media/get-more.png)

    <span data-ttu-id="dba62-118">Kad sinhronizācija ir pabeigta, progr. Talent tiks parādīta sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="dba62-118">After synchronization is completed, Talent will appear on the home page.</span></span>
