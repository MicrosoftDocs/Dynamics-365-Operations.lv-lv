---
title: IoT informācijas pievienojumprogrammas instalēšana LCS
description: Šajā tēmā ir paskaidrots, kā instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386537"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="d7166-103">IoT informācijas pievienojumprogrammas instalēšana LCS</span><span class="sxs-lookup"><span data-stu-id="d7166-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7166-104">Šajā tēmā ir paskaidrots, kā instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d7166-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d7166-105">Pirms varat instalēt pievienojumprogrammu, jums ir [jāizveido Azure resursi](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d7166-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="d7166-106">Iestatīt LCS vidi</span><span class="sxs-lookup"><span data-stu-id="d7166-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="d7166-107">Atveriet LCS un dodieties uz savu Microsoft Dynamics 365 Supply Chain Management vidi.</span><span class="sxs-lookup"><span data-stu-id="d7166-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="d7166-108">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="d7166-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="d7166-109">Atlasiet **Instalēt jaunu pievienojumprogrammu**, lai skatītu videi iespējoto pievienojumprogrammu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="d7166-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="d7166-110">Dialoglodziņā **Atlasīt instalējamo pievienojumprogrammu** atlasiet **IoT informācija**.</span><span class="sxs-lookup"><span data-stu-id="d7166-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="d7166-111">Dialoglodziņā **Iestatīt pievienojumprogrammu** norādiet detalizētu informāciju par savu IoT centrmezglu un Redis kešatmiņu.</span><span class="sxs-lookup"><span data-stu-id="d7166-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="d7166-112">Nepieciešamās vērtības varat atrast atslēgas akreditācijas datu komplektā, ko izveidojāt [Azure resursu izveidošana](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d7166-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="d7166-113">**Nomnieka ID** – Azure portālā dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **Direktorija ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7166-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="d7166-114">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="d7166-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d7166-115">**IoT Event Hub-saderīgs galapunkta atslēgas akreditācijas datu komplekta URI** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **DNS nosaukums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7166-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="d7166-116">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="d7166-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d7166-117">**IoT Event Hub-saderīgā galapunkta noslēpumu nosaukums** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Noslēpumi** un kopējiet noslēpuma nosaukumu, kur tiek glabāta notikuma centrmezgla savienojuma virkne IoT centrmezglam.</span><span class="sxs-lookup"><span data-stu-id="d7166-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="d7166-118">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="d7166-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d7166-119">**Redis kešatmiņas atslēgas akreditācijas datu komplekta URI** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **DNS nosaukums** vērtību.</span><span class="sxs-lookup"><span data-stu-id="d7166-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="d7166-120">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="d7166-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d7166-121">**Redis kešatmiņas galapunkta noslēpumu nosaukums** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Noslēpumi** un kopējiet noslēpuma nosaukumu, kur tiek glabāta savienojuma virkne Redis kešatmiņai.</span><span class="sxs-lookup"><span data-stu-id="d7166-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="d7166-122">Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="d7166-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="d7166-123">Atzīmējiet izvēles rūtiņu, lai piekristu noteikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="d7166-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="d7166-124">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="d7166-124">Select **Install**.</span></span>
8. <span data-ttu-id="d7166-125">Tiek parādīts ziņojuma lodziņš ar tekstu "Pievienojumprogramma ir sekmīgi aktivizēta instalēšanai."</span><span class="sxs-lookup"><span data-stu-id="d7166-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="d7166-126">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d7166-126">Select **OK**.</span></span>

<span data-ttu-id="d7166-127">LCS iestatīšana tagad ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="d7166-127">LCS setup is now completed.</span></span> <span data-ttu-id="d7166-128">Nākamā darbība ir [Scenāriju iestatīšana](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d7166-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="d7166-129">Pievienojumprogrammas atinstalēšana</span><span class="sxs-lookup"><span data-stu-id="d7166-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="d7166-130">Supply Chain Management [scenāriju atspējošana](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="d7166-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="d7166-131">LCS dodieties uz savas Supply Chain Management vides informāciju.</span><span class="sxs-lookup"><span data-stu-id="d7166-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="d7166-132">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="d7166-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="d7166-133">Atlasiet **Atinstalēt** IoT informācijas pievienojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="d7166-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
