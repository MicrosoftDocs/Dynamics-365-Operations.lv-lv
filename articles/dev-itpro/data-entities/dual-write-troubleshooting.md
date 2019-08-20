---
title: Datu integrācijas problēmu novēršanas rokasgrāmata
description: Šajā tēmā ir sniegta problēmu novēršanas informācija par datu integrāciju starp programmām Microsoft Dynamics 365 for Finance and Operations un Common Data Service.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797279"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="aea0a-103">Datu integrācijas problēmu novēršanas rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="aea0a-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="aea0a-104">Iespējojiet spraudņa izsekošanu Common Data Service un pārbaudiet duālā ieraksta spraudņa kļūdas detaļas</span><span class="sxs-lookup"><span data-stu-id="aea0a-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="aea0a-105">Ja radusies problēma vai kļūda ar duālā ieraksta sinhronizāciju, varat pārbaudīt kļūdas trasēšanas žurnālā:</span><span class="sxs-lookup"><span data-stu-id="aea0a-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="aea0a-106">Pirms varat pārbaudīt kļūdas, ir jāiespējo spraudņa izsekošana, izmantojot norādījumus rakstā [Reģistrēt spraudni](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs), lai iespējotu spraudņa izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="aea0a-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="aea0a-107">Tagad varat pārbaudīt kļūdas.</span><span class="sxs-lookup"><span data-stu-id="aea0a-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="aea0a-108">Piesakieties pakalpojumā Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="aea0a-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="aea0a-109">Noklikšķiniet uz ikonas Iestatījumi (zobrats) un atlasiet **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="aea0a-110">Izvēlnē **Iestatījumi** izvēlieties **Pielāgošana > Spraudņa izsekošanas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="aea0a-111">Lai parādītu detalizētu kļūdas informāciju, noklikšķiniet uz tipa nosaukuma **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="aea0a-112">Duālā ieraksta sinhronizācijas kļūdu pārbaude programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aea0a-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="aea0a-113">Varat pārbaudīt kļūdas testēšanas laikā, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="aea0a-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="aea0a-114">Piesakieties Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="aea0a-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="aea0a-115">Atveriet LCS projektu, kuru izvēlējāties, lai veiktu duālā ieraksta testēšanu.</span><span class="sxs-lookup"><span data-stu-id="aea0a-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="aea0a-116">Pārejiet uz Cloud Hosted Environments.</span><span class="sxs-lookup"><span data-stu-id="aea0a-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="aea0a-117">Attālā darbvirsma uz Finance and Operations virtuālās mašīnas, izmantojot lokālo kontu, kas tiek parādīts LCS.</span><span class="sxs-lookup"><span data-stu-id="aea0a-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="aea0a-118">Atvērt notikumu skatītāju.</span><span class="sxs-lookup"><span data-stu-id="aea0a-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="aea0a-119">Dodieties uz **Programmas un Pakalpojumu žurnāli > Microsoft > Dynamics > AX-DualWriteSync > Darbības**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="aea0a-120">Tiek parādītas kļūdas un detaļlizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="aea0a-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="aea0a-121">Kā noņemt saiti un saistīt citu Common Data Service vidi no programmas Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aea0a-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="aea0a-122">Varat atjaunināt saites, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="aea0a-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="aea0a-123">Dodieties uz Finance and Operations vidi.</span><span class="sxs-lookup"><span data-stu-id="aea0a-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="aea0a-124">Atveriet Datu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="aea0a-124">Open Data Management.</span></span>
+ <span data-ttu-id="aea0a-125">Noklikšķiniet uz **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="aea0a-126">Atlasiet visus darbojošos kartējumus un noklikšķiniet uz **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="aea0a-127">Atlasiet visus kartējumus un noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aea0a-128">Opcija **Dzēst** netiks parādīta, ja ir atlasīta veidne**CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="aea0a-129">Ja nepieciešams, atceliet tās atlasi.</span><span class="sxs-lookup"><span data-stu-id="aea0a-129">Unselect it if needed.</span></span> <span data-ttu-id="aea0a-130">**CustomerV3-Account** ir vecāka nodrošināta veidne un darbojas ar risinājumu No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="aea0a-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="aea0a-131">Tā kā tā ir izlaista globāli, tā tiek parādīta zem visām veidnēm.</span><span class="sxs-lookup"><span data-stu-id="aea0a-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="aea0a-132">Noklikšķiniet uz **Atsaistīt vidi**.</span><span class="sxs-lookup"><span data-stu-id="aea0a-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="aea0a-133">Noklikšķiniet uz **Jā**, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="aea0a-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="aea0a-134">Lai piesaistītu jauno vidi, izpildiet [instalēšanas rokasgrāmatā](https://aka.ms/dualwrite-docs) aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="aea0a-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

