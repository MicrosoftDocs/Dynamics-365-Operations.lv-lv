--- 
title: "Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana"
description: "Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 593b4ddb1442d77fd8a29e9d9b161936505f1fb3
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="b2ae3-103">Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b2ae3-103">Set up short picking item reallocation</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2ae3-104">Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="b2ae3-105">Ir iespējams izmantot automātisku atkārtota sadalījuma procesu, kurā tiek izmantotas atrašanās vietas direktīvas, lai izgūtu preces, ja tās ir pieejamas citā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="b2ae3-106">Vai arī, izmantojot manuālu atkārtotu sadalījumu, mobilajā ierīcē tiek parādīts atrašanās vietu saraksts ar pieejamo daudzumu, ļaujot noliktavas darbiniekam izvēlieties atrašanās vietu krājumu izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="b2ae3-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="b2ae3-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="b2ae3-109">Iestatīt darba izņēmumus</span><span class="sxs-lookup"><span data-stu-id="b2ae3-109">Set up work exceptions</span></span>
1. <span data-ttu-id="b2ae3-110">Dodieties uz Noliktavas vadība > Iestatīšana > Darbs > Darba izņēmumi.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="b2ae3-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-111">Click New.</span></span>
    * <span data-ttu-id="b2ae3-112">Ir iespējams definēt vairākus darba izņēmumus ar dažādām krājumu pārdales politikām, kas ļauj noliktavas darbiniekam izvēlieties vienu, pamatojoties uz kravas apstrādes vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="b2ae3-113">Laukā Darba izņēmuma kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="b2ae3-114">Piešķiriet darba izņēmumam nosaukumu, lai norādītu, kādam nolūkam tas tiek izmantots.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="b2ae3-115">Piemēram, Saīsinātas izdošanas rokasgrāmata.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="b2ae3-116">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2ae3-117">Laukā Izņēmuma tips atlasiet 'Saīsinātā izdošana'.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="b2ae3-118">Atlasiet izvēles rūtiņu Krājumu koriģēšana.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="b2ae3-119">Šī opcija norāda, ka krājumi tiks automātiski noregulēti uz vērtību 0 saīsinātas izdošanas atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="b2ae3-120">Laukā Noklusējuma korekcijas veida kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="b2ae3-121">Piemēram, izmantojot USMF, jūs varat atlasīt 'Noņemt Res Adj Out'.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="b2ae3-122">Laukā Krājuma atkārtots sadalījums atlasiet 'Manuāls'.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="b2ae3-123">Ja atlasāt Manuāls vai Automātisks un manuāls, noliktavas darbiniekam jāļauj izmantot manuālu atkārtotu sadali.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="b2ae3-124">Iestatīt darbinieku manuālas krājuma atkārtotas sadales izmantošanai</span><span class="sxs-lookup"><span data-stu-id="b2ae3-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="b2ae3-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-125">Close the page.</span></span>
2. <span data-ttu-id="b2ae3-126">Dodieties uz Noliktavas vadība > Iestatīšana > Nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="b2ae3-127">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-127">Click Edit.</span></span>
4. <span data-ttu-id="b2ae3-128">Sarakstā atlasiet darbinieks 24.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="b2ae3-129">Izvērsiet sadaļu Darbs.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-129">Expand the Work section.</span></span>
6. <span data-ttu-id="b2ae3-130">Atlasiet Jā laukā Atļaut manuālu krājuma atkārtotu sadali.</span><span class="sxs-lookup"><span data-stu-id="b2ae3-130">Select Yes in the Allow manual item reallocation field.</span></span>


