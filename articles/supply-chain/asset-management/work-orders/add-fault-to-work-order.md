---
title: Kļūmes pievienošana darba pasūtījumam
description: Šajā tēmā ir paskaidrots, kā pievienot kļūmes reģistrācijas darba pasūtījumiem programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875782"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="3ed6b-103">Kļūmes pievienošana darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="3ed6b-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="3ed6b-104">Kļūmju noformētājā iestatītās kļūmes varat pievienot darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="3ed6b-105">Darba pasūtījumā atlasītajam līdzeklim jāsatur līdzekļu veidi, kam piesaistīts viens vai vairāki kļūdas ieraksti.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="3ed6b-106">Vairāk par iestatīšanu lasiet sadaļā [Kļūmju pārvaldība](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="3ed6b-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="3ed6b-107">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3ed6b-108">Sarakstā atlasiet darba pasūtījumu, kuram vēlaties veikt kļūmes reģistrāciju, un noklikšķiniet uz **Līdzekļa kļūme**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="3ed6b-109">Kopsavilkuma cilnē **Simptomi** noklikšķiniet uz **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="3ed6b-110">Laukā **Kļūme** automātiski tiek ievadīts kļūmes kārtas numurs.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="3ed6b-111">Laukā **Kļūmes simptoms** atlasiet attiecīgo kļūmes simptomu.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="3ed6b-112">Atlasiet **Kļūmes joma** un **Kļūmes veids**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="3ed6b-113">Laukā **Kļūmes datums** automātiski tiek ievadīts esošais datums.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="3ed6b-114">Var atlasīt arī citu datumu, ja vajadzīgs.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="3ed6b-115">Kopsavilkuma cilnē **Atlasītā simptoma iemesli** pievienojiet rindu, kura aprakstīts problēmas iemesls.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="3ed6b-116">Kopsavilkuma cilnē **Atlasītā simptoma labojumi** pievienojiet rindu, kurā aprakstīts iespējamais problēmas risinājums.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="3ed6b-117">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-117">Click **Save**.</span></span>

![1. attēls](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="3ed6b-119">Līdzekļa kļūmju skatīšana</span><span class="sxs-lookup"><span data-stu-id="3ed6b-119">View asset faults</span></span>

<span data-ttu-id="3ed6b-120">Sarakstā **Līdzekļu kļūmes** ir pārskats par visām līdzekļiem reģistrētajām kļūmēm.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="3ed6b-121">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**, lai atvērtu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="3ed6b-122">Līdzekļu kļūmju pārskata izdrukāšana</span><span class="sxs-lookup"><span data-stu-id="3ed6b-122">Print asset fault report</span></span>

<span data-ttu-id="3ed6b-123">Saraksta **Visi līdzekļi** lapā varat izdrukāt līdzekļu kļūmju pārskatu, kas parāda visas kļūmju reģistrācijas un kļūmju statistikas grafisko pārskatu.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="3ed6b-124">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="3ed6b-125">Sarakstā **Līdzekļi** atlasiet līdzekli, kuram vēlaties izdrukāt kļūmju pārskatu.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="3ed6b-126">Cilnē **Vispārīgi** > **Pārskatu sadaļā** klikšķiniet uz **Līdzekļa kļūme**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="3ed6b-127">Ievadiet konkrētu periodu vai izvēlieties kļūmes veidu.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="3ed6b-128">Noklikšķiniet **Labi**, lai izdrukātu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="3ed6b-129">Var izdrukāt arī kļūmju pārskatu vairākiem līdzekļiem vai līdzekļu- veidiem, klikšķinot uz **Līdzekļu pārvaldība** > **Pārskati** > **Līdzekļi** > **Līdzekļu kļūmes**.</span><span class="sxs-lookup"><span data-stu-id="3ed6b-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

