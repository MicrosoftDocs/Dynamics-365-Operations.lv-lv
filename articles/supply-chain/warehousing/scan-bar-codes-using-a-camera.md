---
title: Svītrkodu skenēšana Warehouse Management mobile programmā, izmantojot kameru
description: Šajā tēmā ir paskaidrots, kā iestatīt Warehouse Management mobile programmu svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831222"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="74943-103">Svītrkodu skenēšana Warehouse Management mobile programmā, izmantojot kameru</span><span class="sxs-lookup"><span data-stu-id="74943-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74943-104">Šajā tēmā ir paskaidrots, kā iestatīt Warehouse Management mobile programmu svītrkodu skenēšanai, izmantojot mobilās ierīces kameru.</span><span class="sxs-lookup"><span data-stu-id="74943-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="74943-105">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="74943-105">Setup</span></span>

<span data-ttu-id="74943-106">Programmas Warehouse Management mobile displeja iestatījumos varat norādīt, vai svītrkodu skenēšanai izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="74943-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="74943-107">Ja izmantosiet opciju **Izmantot kameru kā skeneri**, varēsiet izmantot kameru katrā ievades laukā, kura vēlamais ievades režīms ir iestatīts uz **Skenēšana**.</span><span class="sxs-lookup"><span data-stu-id="74943-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="74943-108">Lai noteiktu to, vai ievades laukam ir jābūt skenējamam, lapā **Noliktavas programmu lauku nosaukumi** iestatiet opcijas **Vēlamais ievades režīms** uz **Skenēšana**.</span><span class="sxs-lookup"><span data-stu-id="74943-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="74943-109">Ja tiks atlasīta šī opcija, Warehouse Management mobile programmā skenēšanai varēs izmantot kameru.</span><span class="sxs-lookup"><span data-stu-id="74943-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="74943-110">Lai iegūtu vairāk informācijas, skatiet [Konfigurēt laukus programmai Warehouse Management mobile](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="74943-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="74943-111">Atbalstītie svītrkoda formāti</span><span class="sxs-lookup"><span data-stu-id="74943-111">Supported bar code formats</span></span>

<span data-ttu-id="74943-112">Tiek atbalstīti visizplatītākie svītrkoda formāti, tostarp Kods 128, Kods 39, Kods 93, EAN-8, EAN-13, UPC-E, UPC A un QR kodi.</span><span class="sxs-lookup"><span data-stu-id="74943-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="74943-113">Navigācija</span><span class="sxs-lookup"><span data-stu-id="74943-113">Navigation</span></span>

<span data-ttu-id="74943-114">Kameras lapa tiks iniciēta katrā lapā, kurā ievades laukam **Vēlamais ievades režīms** ir iestatīts uz *Skenēšana*, kad esat atvēris kameru lapu, navigēšanai izmantojiet tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="74943-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="74943-115">Atlasiet pogu Atpakaļ, lai atgrieztos lapā **Uzdevumi un informācija**.</span><span class="sxs-lookup"><span data-stu-id="74943-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="74943-116">Atlasiet zīmuli lapā **Uzdevumi un informācija**, lai pārietu uz lapu, kurā varat manuāli ievadīt datus.</span><span class="sxs-lookup"><span data-stu-id="74943-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="74943-117">**Uzdevumu un informācijas** lapā noklikšķiniet uz kameras ikonas, lai atgrieztos kameras lapā.</span><span class="sxs-lookup"><span data-stu-id="74943-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="74943-118">Kameras lapā, noklikšķinot uz pogas Kamera, tā būs pelēkota tik ilgi, līdz tiks identificēts svītrkods.</span><span class="sxs-lookup"><span data-stu-id="74943-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="74943-119">Ja svītrkods netiks identificēts 5 sekunžu laikā, procesam iestāsies taimauts un poga Kamera atkal kļūst pieejama.</span><span class="sxs-lookup"><span data-stu-id="74943-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="74943-120">Pēc tam vēlreiz varēsiet mēģināt skenēt svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="74943-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="74943-121">Pavēršot kameru uz svītrkodu, labākam rezultātam gādājiet, lai svītrkods atrastos vienā līmenī ar iekavām.</span><span class="sxs-lookup"><span data-stu-id="74943-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="74943-122">Kad svītrkods būs veiksmīgi noskenēts, rezultāts tiks apstrādāts un jūs varēsiet pāriet uz nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="74943-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="74943-123">Ja nākamajā darbībā būs vēl viens ievades lauks, kura vēlamais ievades režīms būs iestatīts uz Skenēšana, vēlreiz tiks atvērta kamera lapa.</span><span class="sxs-lookup"><span data-stu-id="74943-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="74943-124">Ja nākamā darbība nebūs skenēšanas lauks, kameras lapa netiks iniciēta.</span><span class="sxs-lookup"><span data-stu-id="74943-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]