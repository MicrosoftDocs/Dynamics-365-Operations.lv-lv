---
title: IoT informācijas pievienojumprogrammas instalēšana LCS
description: Šajā tēmā ir paskaidrots, kā instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826447"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="9f64e-103">IoT informācijas pievienojumprogrammas instalēšana LCS</span><span class="sxs-lookup"><span data-stu-id="9f64e-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f64e-104">Šajā tēmā ir paskaidrots, kā instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9f64e-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9f64e-105">Ņemiet vērā, ka pievienojumprogrammas nevar instalēt demonstrācijas/izmēģinājuma vidē.</span><span class="sxs-lookup"><span data-stu-id="9f64e-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="9f64e-106">Pirms varat instalēt pievienojumprogrammu, jums ir [jāizveido Azure resursi](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9f64e-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="9f64e-107">Iestatīt LCS vidi</span><span class="sxs-lookup"><span data-stu-id="9f64e-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="9f64e-108">Atveriet LCS un dodieties uz savu Microsoft Dynamics 365 Supply Chain Management vidi.</span><span class="sxs-lookup"><span data-stu-id="9f64e-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="9f64e-109">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="9f64e-110">Atlasiet **Instalēt jaunu pievienojumprogrammu**, lai skatītu videi iespējoto pievienojumprogrammu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="9f64e-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="9f64e-111">Dialoglodziņā **Atlasīt instalējamo pievienojumprogrammu** atlasiet **IoT informācija**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="9f64e-112">Dialoglodziņā **Iestatīt pievienojumprogrammu** norādiet detalizētu informāciju par savu IoT centrmezglu un Redis kešatmiņu.</span><span class="sxs-lookup"><span data-stu-id="9f64e-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="9f64e-113">Nepieciešamās vērtības varat atrast atslēgas akreditācijas datu komplektā, ko izveidojāt [Azure resursu izveidošana](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9f64e-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="9f64e-114">**Nomnieka ID** – Azure portālā dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **Direktorija ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f64e-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="9f64e-115">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="9f64e-116">**IoT Event Hub-saderīgs galapunkta atslēgas akreditācijas datu komplekta URI** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **DNS nosaukums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f64e-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="9f64e-117">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="9f64e-118">**IoT Event Hub-saderīgā galapunkta noslēpumu nosaukums** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Noslēpumi** un kopējiet noslēpuma nosaukumu, kur tiek glabāta notikuma centrmezgla savienojuma virkne IoT centrmezglam.</span><span class="sxs-lookup"><span data-stu-id="9f64e-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="9f64e-119">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="9f64e-120">**Redis kešatmiņas atslēgas akreditācijas datu komplekta URI** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **DNS nosaukums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f64e-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="9f64e-121">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="9f64e-122">**Redis kešatmiņas galapunkta noslēpumu nosaukums** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Noslēpumi** un kopējiet noslēpuma nosaukumu, kur tiek glabāta savienojuma virkne Redis kešatmiņai.</span><span class="sxs-lookup"><span data-stu-id="9f64e-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="9f64e-123">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="9f64e-124">Atzīmējiet izvēles rūtiņu, lai piekristu noteikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="9f64e-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="9f64e-125">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-125">Select **Install**.</span></span>
8. <span data-ttu-id="9f64e-126">Tiek parādīts ziņojuma lodziņš ar tekstu "Pievienojumprogramma ir sekmīgi aktivizēta instalēšanai."</span><span class="sxs-lookup"><span data-stu-id="9f64e-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="9f64e-127">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-127">Select **OK**.</span></span>

<span data-ttu-id="9f64e-128">LCS iestatīšana tagad ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="9f64e-128">LCS setup is now completed.</span></span> <span data-ttu-id="9f64e-129">Nākamā darbība ir [Scenāriju iestatīšana](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9f64e-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="9f64e-130">Pievienojumprogrammas atinstalēšana</span><span class="sxs-lookup"><span data-stu-id="9f64e-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="9f64e-131">Supply Chain Management [scenāriju atspējošana](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="9f64e-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="9f64e-132">LCS dodieties uz savas Supply Chain Management vides informāciju.</span><span class="sxs-lookup"><span data-stu-id="9f64e-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="9f64e-133">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="9f64e-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="9f64e-134">Atlasiet **Atinstalēt** IoT informācijas pievienojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="9f64e-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]