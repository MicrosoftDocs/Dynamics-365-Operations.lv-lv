---
title: Svītrkodu skenēšana noliktavas programmā, izmantojot kameru
description: Šajā tēmā ir paskaidrots, kā iestatīt noliktavas programmu svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432571"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="8c891-103">Svītrkodu skenēšana noliktavas programmā, izmantojot kameru</span><span class="sxs-lookup"><span data-stu-id="8c891-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c891-104">Šajā tēmā ir paskaidrots, kā iestatīt noliktavas programmu svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.</span><span class="sxs-lookup"><span data-stu-id="8c891-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="8c891-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="8c891-105">Prerequisites</span></span>
<span data-ttu-id="8c891-106">Lai izmantotu šo līdzekli, jūsu ierīcē ir jābūt instalētai noliktavas programmas versijai 1.2.0.0, kā arī kamerai.</span><span class="sxs-lookup"><span data-stu-id="8c891-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="8c891-107">Kad atverat programmu pēc atjaunināšanas, tiek prasīts atļaut programmai Warehousing izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="8c891-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="8c891-108">Ja ierīcei nav kameras, uzvedne netiks rādīta un jūs nevarēsiet izmantot kameru ka skeneri.</span><span class="sxs-lookup"><span data-stu-id="8c891-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="8c891-109">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="8c891-109">Setup</span></span>
<span data-ttu-id="8c891-110">Noliktavas programmas displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="8c891-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="8c891-111">Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**.</span><span class="sxs-lookup"><span data-stu-id="8c891-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="8c891-112">Lai noteiktu to, vai ievades laukam ir jābūt skenējamam, lapā **Noliktavas programmu lauku nosaukumi** iestatiet opcijas **Vēlamais ievades režīms** uz **Skenēšana**.</span><span class="sxs-lookup"><span data-stu-id="8c891-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="8c891-113">Ja tiks atlasīta šī opcija, noliktavas programmā skenēšanai varēs izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="8c891-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="8c891-114">Plašāku informāciju par to, kā konfigurēt lauku nosaukumus noliktavas programmā, skatiet tēmā [programmas lauku nosaukumu konfigurēšana noliktavas programmā](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="8c891-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="8c891-115">Atbalstītie svītrkoda formāti</span><span class="sxs-lookup"><span data-stu-id="8c891-115">Supported bar code formats</span></span>
<span data-ttu-id="8c891-116">Tiek atbalstīti visizplatītākie svītrkoda formāti, tostarp Kods 128, Kods 39, Kods 93, EAN-8, EAN-13, UPC-E, UPC A un QR kodi.</span><span class="sxs-lookup"><span data-stu-id="8c891-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="8c891-117">Navigācija</span><span class="sxs-lookup"><span data-stu-id="8c891-117">Navigation</span></span>
<span data-ttu-id="8c891-118">Kameras lapa tiks iniciēta katrā lapā, kurā ievades laukam vēlamais ievades režīms ir iestatīts uz Skenēšana, kad esat atvēris kameru lapu, navigēšanai izmantojiet tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="8c891-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="8c891-119">Noklikšķiniet uz pogas Atpakaļ, lai atgrieztos uzdevumu un informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="8c891-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="8c891-120">Uzdevumu un informācijas lapā noklikšķiniet uz zīmuļa ikonas, lai pārietu uz lapu, kurā datus var ievadīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="8c891-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="8c891-121">Uzdevumu un informācijas lapā noklikšķiniet uz kameras ikonas, lai atgrieztos kameras lapā.</span><span class="sxs-lookup"><span data-stu-id="8c891-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="8c891-122">Uzdevumu un informācijas lapa</span><span class="sxs-lookup"><span data-stu-id="8c891-122">Task and details page</span></span> | <span data-ttu-id="8c891-123">Kameras lapa</span><span class="sxs-lookup"><span data-stu-id="8c891-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Kameras skenēšanas uzdevuma informācijas lapas piemērs](./media/camera-scanning-example-task-detail-page50.png)          | ![Kameras skenēšanas, piemēram, kameras lapa ir mazāka](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="8c891-126">Kameras lapā, noklikšķinot uz pogas Kamera, tā būs pelēkota tik ilgi, līdz tiks identificēts svītrkods.</span><span class="sxs-lookup"><span data-stu-id="8c891-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="8c891-127">Ja svītrkods netiks identificēts 5 sekunžu laikā, procesam iestāsies taimauts un poga Kamera atkal kļūst pieejama.</span><span class="sxs-lookup"><span data-stu-id="8c891-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="8c891-128">Pēc tam vēlreiz varēsiet mēģināt skenēt svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="8c891-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="8c891-129">Pavēršot kameru uz svītrkodu, labākam rezultātam gādājiet, lai svītrkods atrastos vienā līmenī ar iekavām.</span><span class="sxs-lookup"><span data-stu-id="8c891-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="8c891-130">Kad svītrkods būs veiksmīgi noskenēts, rezultāts tiks apstrādāts un jūs varēsiet pāriet uz nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="8c891-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="8c891-131">Ja nākamajā darbībā būs vēl viens ievades lauks, kura vēlamais ievades režīms būs iestatīts uz Skenēšana, vēlreiz tiks atvērta kamera lapa.</span><span class="sxs-lookup"><span data-stu-id="8c891-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="8c891-132">Ja nākamā darbība nebūs skenēšanas lauks, kameras lapa netiks iniciēta.</span><span class="sxs-lookup"><span data-stu-id="8c891-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

