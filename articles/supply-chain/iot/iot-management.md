---
title: IoT informācijas pārraudzība un pārvaldība
description: Šajā tēmā ir paskaidrots, kā pārraudzīt un pārvaldīt IoT informāciju.
author: robinarh
ms.date: 08/16/2019
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
ms.openlocfilehash: 86e20b9e60e890833c0eb8573e92c0fbb27f8c9a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908423"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="68dd9-103">IoT informācijas pārraudzība un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="68dd9-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68dd9-104">Šajā tēmā ir paskaidrots, kā pārraudzīt un pārvaldīt IoT informāciju.</span><span class="sxs-lookup"><span data-stu-id="68dd9-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="68dd9-105">Pārraudzīt scenārijus programmā Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="68dd9-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="68dd9-106">IoT informācijas apstrādi var pārraudzīt no vairākām vietām:</span><span class="sxs-lookup"><span data-stu-id="68dd9-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="68dd9-107">**Moduļi \> Ražošanas kontrole \> Pieprasījumi un pārskati \> IoT informācija \> Paziņojumi** – skatīt neatrisināto paziņojumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="68dd9-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="68dd9-108">**Moduļi \> Ražošanas kontrole \> Pieprasījumi un pārskati \> IoT informācija \> Slēgti paziņojumi** – skatīt to paziņojumu sarakstu, kas ir atrisināti vai noraidīti.</span><span class="sxs-lookup"><span data-stu-id="68dd9-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="68dd9-109">**Moduļi \> Ražošanas kontrole \> Pieprasījumi un pārskati \> IoT informācija \> Metrikas atslēgas** – skatīt **Resursa statusa** laika sēriju diagrammu metrikas atslēgas.</span><span class="sxs-lookup"><span data-stu-id="68dd9-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="68dd9-110">**Moduļi \> Ražošanas kontrole \> Ražošanas izpilde \> Resursa statuss** – izsekot konkrētu metriku, izmantojot dialoglodziņu **Konfigurēt**.</span><span class="sxs-lookup"><span data-stu-id="68dd9-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="68dd9-111">Ja scenārijs nosaka izņēmumu, paziņojumā tiek parādīta informācija par izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="68dd9-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="68dd9-112">**Darbvietas \> Ražošanas stāva pārvaldība \> Paziņojumi** – skatīt neatrisināto paziņojumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="68dd9-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="68dd9-113">IoT informācijas scenārija darbības modificēšana</span><span class="sxs-lookup"><span data-stu-id="68dd9-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="68dd9-114">Kad scenārijs darbojas, var veikt šādas izmaiņas:</span><span class="sxs-lookup"><span data-stu-id="68dd9-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="68dd9-115">Pievienot jaunas sensora shēmas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="68dd9-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="68dd9-116">Atlasīt jaunas signāla datu vērtības.</span><span class="sxs-lookup"><span data-stu-id="68dd9-116">Select new signal data values.</span></span>
+ <span data-ttu-id="68dd9-117">Atcelt esošo signāla datu vērtību atlasi.</span><span class="sxs-lookup"><span data-stu-id="68dd9-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="68dd9-118">Pievienot un kartēt jaunas signāla datu vērtības.</span><span class="sxs-lookup"><span data-stu-id="68dd9-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="68dd9-119">Atjaunināt sliekšņa vērtības.</span><span class="sxs-lookup"><span data-stu-id="68dd9-119">Update threshold values.</span></span>

<span data-ttu-id="68dd9-120">Kad scenārijs darbojas, šādas izmaiņas ir aizliegtas:</span><span class="sxs-lookup"><span data-stu-id="68dd9-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="68dd9-121">Dzēst vai modificēt shēmas definīcijas, kuras pašlaik izmanto iespējots scenārijs.</span><span class="sxs-lookup"><span data-stu-id="68dd9-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="68dd9-122">Mainīt iespējota scenārija atlasītos shēmu ceļus.</span><span class="sxs-lookup"><span data-stu-id="68dd9-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="68dd9-123">Simulācijas opcijas</span><span class="sxs-lookup"><span data-stu-id="68dd9-123">Simulation options</span></span>

<span data-ttu-id="68dd9-124">Var simulēt rūpnīcas mašīnas signālus.</span><span class="sxs-lookup"><span data-stu-id="68dd9-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="68dd9-125">Papildinformāciju skatiet šādās tēmās:</span><span class="sxs-lookup"><span data-stu-id="68dd9-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="68dd9-126">IoT DevKit AZ3166 savienošana ar Azure IoT centrmezglu</span><span class="sxs-lookup"><span data-stu-id="68dd9-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="68dd9-127">Raspberry Pi tiešsaistes simulatora savienošana ar Azure IoT centrmezglu (Node.js)</span><span class="sxs-lookup"><span data-stu-id="68dd9-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="68dd9-128">Ierīces simulācijas risinājuma paātrinātāja pārskats</span><span class="sxs-lookup"><span data-stu-id="68dd9-128">Device Simulation solution accelerator overview</span></span>](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]