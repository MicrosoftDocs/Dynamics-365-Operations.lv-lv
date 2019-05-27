---
title: Svītrkodu skenēšana, izmantojot kameru, programmā Dynamics 365 for Finance and Operations — Warehousing
description: Šajā tēmā ir paskaidrots, kā iestatīt programmu Dynamics 365 for Finance and Operations — Warehousing svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e78d0a82d3ca66a6912ea1a9517296ca241edf1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559047"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="46bde-103">Svītrkodu skenēšana, izmantojot kameru, programmā Dynamics 365 for Finance and Operations — Warehousing</span><span class="sxs-lookup"><span data-stu-id="46bde-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46bde-104">Šajā tēmā ir paskaidrots, kā iestatīt programmu Dynamics 365 for Finance and Operations — Warehousing svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.</span><span class="sxs-lookup"><span data-stu-id="46bde-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="46bde-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="46bde-105">Prerequisites</span></span>
<span data-ttu-id="46bde-106">Lai izmantotu šo līdzekli, jūsu ierīcē ir jābūt instalētai programmas Warehousing versijai 1.2.0.0, kā arī kamerai.</span><span class="sxs-lookup"><span data-stu-id="46bde-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="46bde-107">Kad atverat programmu pēc atjaunināšanas, tiek prasīts atļaut programmai Dynamics 365 for Finance and Operations — Warehousing izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="46bde-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="46bde-108">Ja ierīcei nav kameras, uzvedne netiks rādīta un jūs nevarēsiet izmantot kameru ka skeneri.</span><span class="sxs-lookup"><span data-stu-id="46bde-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="46bde-109">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="46bde-109">Setup</span></span>
<span data-ttu-id="46bde-110">Programmas Warehousing displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="46bde-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="46bde-111">Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**.</span><span class="sxs-lookup"><span data-stu-id="46bde-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="46bde-112">Lai noteiktu to, vai ievades laukam ir jābūt skenējamam, programmas Dynamics 365 for Finance and Operations lapā **Noliktavas programmu lauku nosaukumi** iestatiet opcijas **Vēlamais ievades režīms** vērtību **Skenēšana**.</span><span class="sxs-lookup"><span data-stu-id="46bde-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="46bde-113">Ja tiks atlasīta šī opcija, programmā Warehousing skenēšanai varēš izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="46bde-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="46bde-114">Plašāku informāciju par to, kā konfigurēt lauku nosaukumus programmā Warehousing, skatiet tēmā [Lauku nosaukumu konfigurēšana programmā Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="46bde-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="46bde-115">Atbalstītie svītrkoda formāti</span><span class="sxs-lookup"><span data-stu-id="46bde-115">Supported bar code formats</span></span>
<span data-ttu-id="46bde-116">Tiek atbalstīti visizplatītākie svītrkoda formāti, tostarp Kods 128, Kods 39, Kods 93, EAN-8, EAN-13, UPC-E, UPC A un QR kodi.</span><span class="sxs-lookup"><span data-stu-id="46bde-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="46bde-117">Navigācija</span><span class="sxs-lookup"><span data-stu-id="46bde-117">Navigation</span></span>
<span data-ttu-id="46bde-118">Kameras lapa tiks iniciēta katrā lapā, kurā ievades laukam vēlamais ievades režīms ir iestatīts uz Skenēšana, kad esat atvēris kameru lapu, navigēšanai izmantojiet tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="46bde-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="46bde-119">Noklikšķiniet uz pogas Atpakaļ, lai atgrieztos uzdevumu un informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="46bde-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="46bde-120">Uzdevumu un informācijas lapā noklikšķiniet uz zīmuļa ikonas, lai pārietu uz lapu, kurā datus var ievadīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="46bde-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="46bde-121">Uzdevumu un informācijas lapā noklikšķiniet uz kameras ikonas, lai atgrieztos kameras lapā.</span><span class="sxs-lookup"><span data-stu-id="46bde-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="46bde-122">Uzdevumu un informācijas lapa</span><span class="sxs-lookup"><span data-stu-id="46bde-122">Task and details page</span></span> | <span data-ttu-id="46bde-123">Kameras lapa</span><span class="sxs-lookup"><span data-stu-id="46bde-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="46bde-126">Kameras lapā, noklikšķinot uz pogas Kamera, tā būs pelēkota tik ilgi, līdz tiks identificēts svītrkods.</span><span class="sxs-lookup"><span data-stu-id="46bde-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="46bde-127">Ja svītrkods netiks identificēts 5 sekunžu laikā, procesam iestāsies taimauts un poga Kamera atkal kļūst pieejama.</span><span class="sxs-lookup"><span data-stu-id="46bde-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="46bde-128">Pēc tam vēlreiz varēsiet mēģināt skenēt svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="46bde-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="46bde-129">Pavēršot kameru uz svītrkodu, labākam rezultātam gādājiet, lai svītrkods atrastos vienā līmenī ar iekavām.</span><span class="sxs-lookup"><span data-stu-id="46bde-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="46bde-130">Kad svītrkods būs veiksmīgi noskenēts, rezultāts tiks apstrādāts un jūs varēsiet pāriet uz nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="46bde-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="46bde-131">Ja nākamajā darbībā būs vēl viens ievades lauks, kura vēlamais ievades režīms būs iestatīts uz Skenēšana, vēlreiz tiks atvērta kamera lapa.</span><span class="sxs-lookup"><span data-stu-id="46bde-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="46bde-132">Ja nākamā darbība nebūs skenēšanas lauks, kameras lapa netiks iniciēta.</span><span class="sxs-lookup"><span data-stu-id="46bde-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

