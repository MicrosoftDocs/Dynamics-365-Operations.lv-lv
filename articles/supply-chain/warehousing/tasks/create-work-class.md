--- 
title: Darba klases izveide
description: "Šajā procedūrā parādīts, kā iestatīt darba klasi."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9a775366bdaecb59a375f245f7a4d17a659cab11
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-work-class"></a><span data-ttu-id="c53ee-103">Darba klases izveide</span><span class="sxs-lookup"><span data-stu-id="c53ee-103">Create a work class</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c53ee-104">Šajā procedūrā parādīts, kā iestatīt darba klasi.</span><span class="sxs-lookup"><span data-stu-id="c53ee-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="c53ee-105">Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu tipu, ko noliktavas darbinieks var apstrādāt mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="c53ee-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="c53ee-106">Rindas, ko darbinieks var apstrādāt, nosaka darba klases pēc mobilās ierīces izvēlnes elementiem, kuriem noliktavas darbinieks var piekļūt, un darba klases, kas norādīta darba rindās.</span><span class="sxs-lookup"><span data-stu-id="c53ee-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="c53ee-107">Darba klases var arī izmantot, lai apstiprinātu izvietošanas novietojumu darba pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="c53ee-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="c53ee-108">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="c53ee-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c53ee-109">Šī procedūra ir paredzēta noliktavas pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="c53ee-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="c53ee-110">Dodieties uz Noliktavas vadība > Iestatīšana > Darbs > Darba klases.</span><span class="sxs-lookup"><span data-stu-id="c53ee-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="c53ee-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c53ee-111">Click New.</span></span>
3. <span data-ttu-id="c53ee-112">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c53ee-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="c53ee-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c53ee-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c53ee-114">Laukā Darba pasūtījuma tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="c53ee-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="c53ee-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c53ee-115">Click New.</span></span>
7. <span data-ttu-id="c53ee-116">Laukā Novietojuma tips ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c53ee-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="c53ee-117">Atlasot novietojuma veidu, tiek noteikts ierobežojums attiecībā uz to, kur krājumus varat ievietot, pēc tam, kad tie būs izdoti.</span><span class="sxs-lookup"><span data-stu-id="c53ee-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="c53ee-118">Šis iestatījums tiek izmantots, kad novietojuma direktīva mēģina atrisināt novietojumu vai noliktavas darbinieks manuāli nodrošina mobilās ierīces izvēlnes elementa novietojumu.</span><span class="sxs-lookup"><span data-stu-id="c53ee-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="c53ee-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c53ee-119">Close the page.</span></span>


