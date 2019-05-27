---
title: Lietotāju lielapjoma importēšana
description: Sistēmas administratori var izmantot šo procedūru, lai importētu lielu skaitu lietotāju no Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548096"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="08306-103">Lietotāju lielapjoma importēšana</span><span class="sxs-lookup"><span data-stu-id="08306-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08306-104">Sistēmas administratori var izmantot šo procedūru, lai importētu lielu skaitu lietotāju no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="08306-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="08306-105">Izpildīt kā pakešuzdevumu</span><span class="sxs-lookup"><span data-stu-id="08306-105">Run as a batch job</span></span>
1. <span data-ttu-id="08306-106">Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.</span><span class="sxs-lookup"><span data-stu-id="08306-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="08306-107">Noklikšķiniet uz Partijas importēšana.</span><span class="sxs-lookup"><span data-stu-id="08306-107">Click Batch import.</span></span>
3. <span data-ttu-id="08306-108">Izvērsiet sadaļu Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="08306-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="08306-109">Laukā Pakešapstrāde atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="08306-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="08306-110">Laukā Uzdevuma apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="08306-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="08306-111">Laukā Partijas grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="08306-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="08306-112">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="08306-112">This is an optional step.</span></span>  
7. <span data-ttu-id="08306-113">Laukā Privāts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="08306-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="08306-114">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="08306-114">This is an optional step.</span></span>  
8. <span data-ttu-id="08306-115">Laukā Kritisks darbs atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="08306-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="08306-116">Šis solis nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="08306-116">This is an optional step.</span></span>  
9. <span data-ttu-id="08306-117">Laukā Pārraudzības kategorija atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="08306-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="08306-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="08306-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="08306-119">Izpilde smilškastes vidē</span><span class="sxs-lookup"><span data-stu-id="08306-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="08306-120">Noklikšķiniet uz Partijas importēšana.</span><span class="sxs-lookup"><span data-stu-id="08306-120">Click Batch import.</span></span>
2. <span data-ttu-id="08306-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="08306-121">Click OK.</span></span>

