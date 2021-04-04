---
title: Lietotāju importēšana no Azure Active Directory
description: Sistēmas administratori var izmantot šo procedūru, lai manuāli importētu konkrētus lietotājus vai lielu skaitu lietotāju no Azure Active Directory.
author: peakerbl
manager: AnnBe
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
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571009"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="74027-103">Lietotāju importēšana no Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="74027-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="74027-104">Konkrētu lietotāju importēšana</span><span class="sxs-lookup"><span data-stu-id="74027-104">Import select users</span></span>

<span data-ttu-id="74027-105">Sistēmas administratori var izmantot šo procedūru, lai importētu konkrētus lietotājus no Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="74027-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="74027-106">Lietotājs tiks importēts kopā ar pašreizējo sesijas uzņēmumu kā noklusējuma uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="74027-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="74027-107">Pirms lietotāju importēšanas mainiet pašreizējo uzņēmumu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="74027-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="74027-108">Pārejiet uz sadaļu **Sistēmas administrēšana > Lietotāji > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="74027-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="74027-109">Noklikšķiniet uz **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="74027-109">Click **Import users**.</span></span>
4. <span data-ttu-id="74027-110">Atlasiet lietotājus, kas jāimportē, un atlasiet **Importēt lietotājus**.</span><span class="sxs-lookup"><span data-stu-id="74027-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="74027-111">Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="74027-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="74027-112">Lietotāju lielapjoma importēšana</span><span class="sxs-lookup"><span data-stu-id="74027-112">Import users in bulk</span></span>

<span data-ttu-id="74027-113">Sistēmas administratori var izmantot šo procedūru, lai importētu lielu skaitu lietotāju no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74027-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="74027-114">Ņemiet vērā, ka, izmantojot partijas importēšanas opciju, nav iespējams atlasīt lietotājus.</span><span class="sxs-lookup"><span data-stu-id="74027-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="74027-115">Palaidiet importēšanu kā pakešuzdevumu</span><span class="sxs-lookup"><span data-stu-id="74027-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="74027-116">Lietotājs tiks importēts kopā ar pašreizējo sesijas uzņēmumu kā noklusējuma uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="74027-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="74027-117">Pirms lietotāju importēšanas mainiet pašreizējo uzņēmumu, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="74027-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="74027-118">Pārejiet uz sadaļu **Sistēmas administrēšana > Lietotāji > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="74027-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="74027-119">Noklikšķiniet uz **Partijas importēšana**.</span><span class="sxs-lookup"><span data-stu-id="74027-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="74027-120">Izvērsiet sadaļu **Palaist fonā**.</span><span class="sxs-lookup"><span data-stu-id="74027-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="74027-121">Laukā **Partijas apstrāde** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="74027-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="74027-122">Laukā **Partijas grupa** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="74027-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="74027-123">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="74027-123">This is an optional step.</span></span>  
7. <span data-ttu-id="74027-124">Laukā **Privāts** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="74027-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="74027-125">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="74027-125">This is an optional step.</span></span>  
8. <span data-ttu-id="74027-126">Laukā **Kritisks darbs** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="74027-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="74027-127">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="74027-127">This is an optional step.</span></span>  
9. <span data-ttu-id="74027-128">Laukā **Pārraudzības kategorija** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="74027-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="74027-129">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="74027-129">Click **OK**.</span></span>

<span data-ttu-id="74027-130">Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="74027-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="74027-131">Izpilde smilškastes vidē</span><span class="sxs-lookup"><span data-stu-id="74027-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="74027-132">Atlasiet **Partijas importēšana**.</span><span class="sxs-lookup"><span data-stu-id="74027-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="74027-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="74027-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]