---
title: Regulatory Configuration Service (RCS) - dzēst RCS vidi
description: Šajā tēmā skaidrots, kā Regulatory Configuration Service (RCS) sistēmas administrators var dzēst RCS vidi un saistītos datus.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295822"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="5523c-103">Regulatory Configuration Service (RCS) - dzēst RCS vidi</span><span class="sxs-lookup"><span data-stu-id="5523c-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5523c-104">Šajā tēmā skaidrots, kā Regulatory Configuration Service (RCS) sistēmas administrators var dzēst RCS vidi un saistītos datus.</span><span class="sxs-lookup"><span data-stu-id="5523c-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="5523c-105">Pirms varat pabeigt šajā tēmā norādīta procedūra, jāizpilda šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="5523c-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="5523c-106">RCS videi ir jābūt piešķirtai lomai **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="5523c-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="5523c-107">Lomai **Sistēmas administrators** ir jābūt piešķirtai lomai **RCSDeleteEnvironmentDuty**.</span><span class="sxs-lookup"><span data-stu-id="5523c-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="5523c-108">RCS vides dzēšana</span><span class="sxs-lookup"><span data-stu-id="5523c-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="5523c-109">Atvēriet RCS un atlasiet darbvietas elementu **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="5523c-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="5523c-110">Sadaļā **Saistītās saites** atlasiet **Dzēst RCS vidi**.</span><span class="sxs-lookup"><span data-stu-id="5523c-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Dzēst RCS vides saiti sadaļā Saistītās saites](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="5523c-112">Dialoglodziņā, kas tiek parādīts, pārskatiet ziņojumus par vides dzēšanas tvērumu.</span><span class="sxs-lookup"><span data-stu-id="5523c-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Ziņojumi RCS vides dzēšanas dialoglodziņā](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="5523c-114">RCS vides dzēšanu nevar atcelt.</span><span class="sxs-lookup"><span data-stu-id="5523c-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="5523c-115">Ar šo darbību tiek dzēsta atlasītā RCS vide un jebkuri saistītie dati, tostarp līdzekļi un konfigurācijas, kas tiek glabātas Globālajā repozitorijā.</span><span class="sxs-lookup"><span data-stu-id="5523c-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="5523c-116">Līdzekļi un konfigurācijas, kas tiek koplietotas ar citām organizācijām, netiks kopīgotas un tiks dzēstas, ja tām nav atkarību.</span><span class="sxs-lookup"><span data-stu-id="5523c-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="5523c-117">Līdzekļi un konfigurācijas, kurām ir atkarības, tiks atzīmētas kā pārtrauktas.</span><span class="sxs-lookup"><span data-stu-id="5523c-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="5523c-118">Sniegtajā laukā ievadiet RCS vides vispārēji unikālo identifikatoru (GUID), lai apstiprinātu, ka vēlaties to dzēst.</span><span class="sxs-lookup"><span data-stu-id="5523c-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="5523c-119">Vides GUID ir ietverts dzēšanas ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="5523c-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="5523c-120">Atlasiet **Dzēst vidi**.</span><span class="sxs-lookup"><span data-stu-id="5523c-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="5523c-121">Jūsu RCS vide un jebkuri saistītie dati tagad tiek dzēsti.</span><span class="sxs-lookup"><span data-stu-id="5523c-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5523c-122">Pēc RCS vides dzēšanas datus nevar atkopt.</span><span class="sxs-lookup"><span data-stu-id="5523c-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="5523c-123">Jaunu RCS vidi var izveidot jebkurā pieejamā RCS reģionā.</span><span class="sxs-lookup"><span data-stu-id="5523c-123">A new RCS environment can be created in any available RCS region.</span></span>
