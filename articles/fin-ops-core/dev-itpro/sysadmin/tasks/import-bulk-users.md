---
title: Lietotāju importēšana no Azure Active Directory
description: Sistēmas administratori var izmantot šo procedūru, lai manuāli importētu konkrētus lietotājus vai lielu skaitu lietotāju no Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745793"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="3ecd6-103">Lietotāju importēšana no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3ecd6-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="3ecd6-104">Konkrētu lietotāju importēšana</span><span class="sxs-lookup"><span data-stu-id="3ecd6-104">Import select users</span></span>

<span data-ttu-id="3ecd6-105">Sistēmas administratori var izmantot šo procedūru, lai importētu konkrētus lietotājus no Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3ecd6-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="3ecd6-106">Lietotājs tiks importēts kopā ar pašreizējo sesijas uzņēmumu kā noklusējuma uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3ecd6-107">Pirms lietotāju importēšanas mainiet pašreizējo uzņēmumu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3ecd6-108">Pārejiet uz sadaļu **Sistēmas administrēšana > Lietotāji > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="3ecd6-109">Noklikšķiniet uz **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-109">Click **Import users**.</span></span>
4. <span data-ttu-id="3ecd6-110">Atlasiet lietotājus, kas jāimportē, un atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="3ecd6-111">Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="3ecd6-112">Lietotāju lielapjoma importēšana</span><span class="sxs-lookup"><span data-stu-id="3ecd6-112">Import users in bulk</span></span>

<span data-ttu-id="3ecd6-113">Sistēmas administratori var izmantot šo procedūru, lai importētu lielu skaitu lietotāju no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="3ecd6-114">Ņemiet vērā, ka, izmantojot partijas importēšanas opciju, nav iespējams atlasīt lietotājus.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="3ecd6-115">Palaidiet importēšanu kā pakešuzdevumu</span><span class="sxs-lookup"><span data-stu-id="3ecd6-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="3ecd6-116">Lietotājs tiks importēts kopā ar pašreizējo sesijas uzņēmumu kā noklusējuma uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3ecd6-117">Pirms lietotāju importēšanas mainiet pašreizējo uzņēmumu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3ecd6-118">Pārejiet uz sadaļu **Sistēmas administrēšana > Lietotāji > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="3ecd6-119">Noklikšķiniet uz **Partijas importēšana**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="3ecd6-120">Izvērsiet sadaļu **Palaist fonā**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="3ecd6-121">Laukā **Partijas apstrāde** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="3ecd6-122">Laukā **Partijas grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="3ecd6-123">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-123">This is an optional step.</span></span>  
7. <span data-ttu-id="3ecd6-124">Laukā **Privāts** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="3ecd6-125">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-125">This is an optional step.</span></span>  
8. <span data-ttu-id="3ecd6-126">Laukā **Kritisks darbs** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="3ecd6-127">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-127">This is an optional step.</span></span>  
9. <span data-ttu-id="3ecd6-128">Laukā **Pārraudzības kategorija** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="3ecd6-129">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-129">Click **OK**.</span></span>

<span data-ttu-id="3ecd6-130">Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="3ecd6-131">Izpilde smilškastes vidē</span><span class="sxs-lookup"><span data-stu-id="3ecd6-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="3ecd6-132">Atlasiet **Partijas importēšana**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="3ecd6-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3ecd6-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]