---
title: Drošības diagnostika uzdevumu reģistrēšanai
description: Šajā tēmā sniegta informācija par to, kā analizēt un pārvaldīt drošības atļaujas prasības, pamatojoties uz uzdevuma reģistrāciju.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 4aecda7e0d604b70dec58a4f5bb2992fe7e0a5e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982434"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="6c086-103">Drošības diagnostika uzdevumu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="6c086-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="6c086-104">Pirms sākšanas</span><span class="sxs-lookup"><span data-stu-id="6c086-104">Before you begin</span></span>

<span data-ttu-id="6c086-105">Šajā tēmā sniegta informācija par to, kā analizēt un pārvaldīt drošības atļaujas prasības, pamatojoties uz uzdevuma reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="6c086-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="6c086-106">Pirms šajā tēmā aprakstīto darbību veikšanas jums ir jābūt uzdevuma reģistrēšanai biznesa procesiem, ko vēlaties analizēt.</span><span class="sxs-lookup"><span data-stu-id="6c086-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="6c086-107">Lai reģistrētu biznesa procesu, skatiet [Uzdevumu reģistrētāja resursi](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="6c086-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="6c086-108">Pārvaldīt uzdevuma reģistrēšanas drošību</span><span class="sxs-lookup"><span data-stu-id="6c086-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="6c086-109">Dodieties uz **Sistēmas administrēšana** > **Drošība** > **Drošības diagnostikas uzdevumu reģistrēšanai**.</span><span class="sxs-lookup"><span data-stu-id="6c086-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="6c086-110">Atveriet uzdevumu reģistrēšanu no tā atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="6c086-110">Open the task recording from its location.</span></span> <span data-ttu-id="6c086-111">Atlasiet **Atvērt no šī datora** vai **Atvērt no Lifecycle Services** un pēc tam atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="6c086-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="6c086-112">Tādējādi tiks atvērta **Drošības izvēlnes krājuma detalizētas informācijas** lapa, kas uzskaita šim procesam vajadzīgos drošības objektus.</span><span class="sxs-lookup"><span data-stu-id="6c086-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="6c086-113">Izvēlnes elementi **Darbība** un **Izvade** nav iekļauti sarakstā.</span><span class="sxs-lookup"><span data-stu-id="6c086-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="6c086-114">Laukā **Lietotāja ID** atlasiet lietotāju.</span><span class="sxs-lookup"><span data-stu-id="6c086-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="6c086-115">Ja lietotājam nav atļauju atsevišķiem izvēlnes elementiem, lauks **Trūkstošās atļaujas** tiks atjaunināts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6c086-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Drošības izvēlnes krājuma detalizētas informācijas lapa](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="6c086-117">Atlasiet **Pievienot atsauci**, lai skatītu drošības objektu sarakstu, iekļaujot lomas, pienākumus un privilēģijas, kas piešķir trūkstošo atļauju.</span><span class="sxs-lookup"><span data-stu-id="6c086-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="6c086-118">Izvēlieties drošības objektu no saraksta:</span><span class="sxs-lookup"><span data-stu-id="6c086-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="6c086-119">Ja ir izvēlēta **Loma**, atlasiet **Pievienot lomu lietotājam**.</span><span class="sxs-lookup"><span data-stu-id="6c086-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="6c086-120">Tas atvērs lapu **Piešķirt lietotājus lomām**.</span><span class="sxs-lookup"><span data-stu-id="6c086-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="6c086-121">Papildinformāciju skatiet lapu [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6c086-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="6c086-122">Ja ir izvēlēts **Pienākums**, atlasiet **Pievienot pienākumu lomai**, atlasiet lomas, kurām jāpievieno pienākums, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6c086-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="6c086-123">Ja ir izvēlēts **Privilēģija**, atlasiet **Pievienot privilēģiju pienākumiem**, atlasiet lomas, kurām jāpievieno pienākums, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6c086-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
