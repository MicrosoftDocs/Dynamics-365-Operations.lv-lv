---
title: Datu integrācijas problēmu novēršanas rokasgrāmata
description: Šajā rakstā ir sniegta informācija par problēmu novēršanu datu integrācijai starp Finance and Operations programmām un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019901"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="8ef47-103">Datu integrācijas problēmu novēršanas rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="8ef47-103">Troubleshooting guide for data integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="8ef47-104">Iespējojiet spraudņu izsekošanas žurnālus programmā Common Data Service un pārbaudiet informāciju par duālās rakstīšanas spraudņu kļūdām.</span><span class="sxs-lookup"><span data-stu-id="8ef47-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

<span data-ttu-id="8ef47-105">Ja duālās rakstīšanas sinhronizācijas laikā radīsies problēma vai kļūda, veiciet šīs darbības kļūdu pārbaudei izsekošanas žurnālā.</span><span class="sxs-lookup"><span data-stu-id="8ef47-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="8ef47-106">Lai varētu pārbaudīt kļūdas, vispirms ir jāiespējo spraudņu izsekošanas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="8ef47-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="8ef47-107">Lai iegūtu norādījumus, atveriet “Skatīt izsekošanas žurnālus” [Pamācība: uzrakstiet un reģistrējiet spraudni](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="8ef47-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="8ef47-108">Tagad varat pārbaudīt kļūdas.</span><span class="sxs-lookup"><span data-stu-id="8ef47-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="8ef47-109">Pierakstieties programmā Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="8ef47-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="8ef47-110">Atlasiet pogu **Iestatījumi** (zobrata simbols), pēc tam atlasiet **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="8ef47-111">Izvēlnē **Iestatījumi** atlasiet **Pielāgošana \> Spraudņu izsekošanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="8ef47-112">Atlasiet tipa nosaukumu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, lai parādītu informāciju par kļūdu.</span><span class="sxs-lookup"><span data-stu-id="8ef47-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="8ef47-113">Pārbaudīt duālās rakstīšanas sinhronizācijas kļūdas</span><span class="sxs-lookup"><span data-stu-id="8ef47-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="8ef47-114">Veiciet šīs darbības, lai pārbaudītu kļūdas testēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="8ef47-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="8ef47-115">Pierakstieties portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8ef47-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="8ef47-116">Atveriet LCS projektu, kuram ir jāveic testēšana.</span><span class="sxs-lookup"><span data-stu-id="8ef47-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="8ef47-117">Atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="8ef47-118">Izveidojiet Attālās darbvirsmas savienojumu ar programmas virtuālo mašīnu (VM), izmantojot vietējo kontu, kas parādīts portālā LCS.</span><span class="sxs-lookup"><span data-stu-id="8ef47-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="8ef47-119">Atveriet komponentu Notikumu skatītājs.</span><span class="sxs-lookup"><span data-stu-id="8ef47-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="8ef47-120">Pārejiet uz sadaļu **Lietojumprogrammu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> AX-DualWriteSync \> Darbību**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="8ef47-121">Tiek parādītas kļūdas un detalizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="8ef47-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="8ef47-122">Atsaistiet vienu Common Data Service vidi no programmas un saistiet ar citu vidi</span><span class="sxs-lookup"><span data-stu-id="8ef47-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="8ef47-123">Veiciet šīs darbības, lai atjauninātu saites.</span><span class="sxs-lookup"><span data-stu-id="8ef47-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="8ef47-124">Dodieties uz programmas vidi.</span><span class="sxs-lookup"><span data-stu-id="8ef47-124">Go to the application environment.</span></span>
2. <span data-ttu-id="8ef47-125">Atveriet Datu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="8ef47-125">Open Data Management.</span></span>
3. <span data-ttu-id="8ef47-126">Atlasiet **Saistiet ar CDS lietojumprogrammām**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="8ef47-127">Atlasiet visus darbojošos kartējumus un pēc tam atlasiet **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="8ef47-128">Atlasiet visus kartējumus un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8ef47-129">Opcija **Dzēst** nav pieejama, ja ir atlasīta veidne **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="8ef47-130">Notīriet šīs veidnes atlasi, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="8ef47-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="8ef47-131">**CustomerV3-Account** ir vecāka nodrošināta veidne un darbojas ar risinājumu No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="8ef47-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="8ef47-132">Tā parādās zem visām veidnēm, jo ir izlaista visā pasaulē.</span><span class="sxs-lookup"><span data-stu-id="8ef47-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="8ef47-133">Atlasiet **Atsaistīt vidi**.</span><span class="sxs-lookup"><span data-stu-id="8ef47-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="8ef47-134">Atlasiet **Jā**, lai apstiprinātu darbību.</span><span class="sxs-lookup"><span data-stu-id="8ef47-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="8ef47-135">Lai piesaistītu jauno vidi, izpildiet [instalēšanas rokasgrāmatā](https://aka.ms/dualwrite-docs) aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8ef47-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
