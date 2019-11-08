---
title: Kļūmes pievienošana darba pasūtījumam
description: Šajā tēmā ir paskaidrots, kā pievienot kļūmes reģistrācijas darba pasūtījumiem programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2b58cc31578d7bb102c6b5aa8b4ce2d6cfe8c893
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626205"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="3a9a7-103">Pievienot kļūmi darba pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="3a9a7-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3a9a7-104">Kļūmes, kas iestatītas kļūmju noformētājā, varat pievienot darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="3a9a7-105">Vienam vai vairākiem kļūdas ierakstiem jābūt piesaistītiem tiem līdzekļu veidiem, kas tiek izmantoti darba pasūtījumā atlasītajam līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="3a9a7-106">Plašāku informāciju par iestatīšanu skatiet zem saites [KĻūmju pārvaldība](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="3a9a7-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="3a9a7-107">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3a9a7-108">Atlasiet darba pasūtījumu, kuram izveidot kļūmju reģistrāciju, un pēc tam darbības rūts cilnē **Darba pasūtījums**, kas atrodas grupā **Līdzekļi**, atlasiet **Līdzekļa kļūme**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="3a9a7-109">Kopsavilkuma cilnē **Simptomi** atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="3a9a7-110">Laukā **Kļūme** automātiski tiek ievadīts kļūmes kārtas numurs.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="3a9a7-111">Laukā **Kļūmes simptoms** atlasiet attiecīgo kļūmes simptomu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="3a9a7-112">Laukā **Kļūmes apgabals** un **Kļūmes veids** atlasiet atbilstīgās vērtības.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="3a9a7-113">Laukā **Kļūmes datums** automātiski tiek ievadīts esošais datums.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="3a9a7-114">Pēc vajadzības varat atlasīt citu datumu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="3a9a7-115">Kopsavilkuma cilnē **Atlasītā simptoma iemesli** pievienojiet rindu, kas apraksta problēmas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="3a9a7-116">Kopsavilkuma cilnē **Atlasītā simptoma labojumi** pievienojiet rindu, kas apraksta iespējamo problēmas risinājumu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="3a9a7-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-117">Select **Save**.</span></span>

<span data-ttu-id="3a9a7-118">Attēlā tālāk parādīts kļūmes reģistrācijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-118">The illustration below shows an example of a fault registration.</span></span>

![1. attēls](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="3a9a7-120">Līdzekļa kļūmju skatīšana</span><span class="sxs-lookup"><span data-stu-id="3a9a7-120">View asset faults</span></span>

<span data-ttu-id="3a9a7-121">Sarakstā **Līdzekļu kļūmes** ir pārskats par visām līdzekļiem reģistrētajām kļūmēm.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="3a9a7-122">Saraksta **Līdzekļu kļūmes** lapā ir pārskats par visām kļūmēm, kas reģistrētas līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="3a9a7-123">Lai atvērtu lapu, atlasiet **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="3a9a7-124">Līdzekļu kļūmju pārskata izdrukāšana</span><span class="sxs-lookup"><span data-stu-id="3a9a7-124">Print asset fault report</span></span>

<span data-ttu-id="3a9a7-125">Saraksta **Visi līdzekļi** lapā varat izdrukāt līdzekļu kļūmju pārskatu, kas parāda visas kļūmju reģistrācijas un kļūmju statistikas grafisko pārskatu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="3a9a7-126">Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi**</span><span class="sxs-lookup"><span data-stu-id="3a9a7-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="3a9a7-127">Atlasīt līdzekli, kuram jādrukā kļūmju pārskats.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="3a9a7-128">Darbību rūts cilnē **Vispārīgi**, grupā **ārskati** atlasiet **Līdzekļu kļūmes**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="3a9a7-129">Ievadiet konkrētu periodu vai izvēlieties kļūmes veidu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="3a9a7-130">Atlasiet **Labi**, lai izdrukātu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="3a9a7-131">Lai izdrukātu kļūmju pārskatu vairākiem līdzekļiem vai līdzekļu veidiem, atlasiet **Līdzekļu pārvaldība** > **Pārskati** > **Līdzekļi** > **Līdzekļu kļūmes**.</span><span class="sxs-lookup"><span data-stu-id="3a9a7-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

