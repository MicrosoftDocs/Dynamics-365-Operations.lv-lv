---
title: Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana
description: Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eae86b307ac8d8539c3897293c2fc21ea57d2d60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148243"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="b0287-103">Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b0287-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0287-104">Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.</span><span class="sxs-lookup"><span data-stu-id="b0287-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn't sufficient inventory at the location they've been directed to.</span></span> <span data-ttu-id="b0287-105">Ir iespējams izmantot automātisku atkārtota sadalījuma procesu, kurā tiek izmantotas atrašanās vietas direktīvas, lai izgūtu preces, ja tās ir pieejamas citā atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="b0287-105">It's possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they're available at another location.</span></span> <span data-ttu-id="b0287-106">Vai arī, izmantojot manuālu atkārtotu sadalījumu, mobilajā ierīcē tiek parādīts atrašanās vietu saraksts ar pieejamo daudzumu, ļaujot noliktavas darbiniekam izvēlieties atrašanās vietu krājumu izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="b0287-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="b0287-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="b0287-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="b0287-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="b0287-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="b0287-109">Iestatīt darba izņēmumus</span><span class="sxs-lookup"><span data-stu-id="b0287-109">Set up work exceptions</span></span>
1. <span data-ttu-id="b0287-110">Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Darba > Darba izņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="b0287-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="b0287-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b0287-111">Click **New**.</span></span> <span data-ttu-id="b0287-112">Ir iespējams definēt vairākus darba izņēmumus ar dažādām krājumu pārdales politikām, kas ļauj noliktavas darbiniekam izvēlieties vienu, pamatojoties uz kravas apstrādes vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b0287-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="b0287-113">Laukā **Darba izņēmuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b0287-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="b0287-114">Piešķiriet darba izņēmumam nosaukumu, lai norādītu, kādam nolūkam tas tiek izmantots.</span><span class="sxs-lookup"><span data-stu-id="b0287-114">Give the work exception a title to indicate what it's used for.</span></span> <span data-ttu-id="b0287-115">Piemēram, Saīsinātas izdošanas rokasgrāmata.</span><span class="sxs-lookup"><span data-stu-id="b0287-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="b0287-116">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b0287-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b0287-117">Laukā **Izņēmuma veids** atlasiet 'Saīsinātā izdošana'.</span><span class="sxs-lookup"><span data-stu-id="b0287-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="b0287-118">Atlasiet izvēles rūtiņu **Krājumu koriģēšana**.</span><span class="sxs-lookup"><span data-stu-id="b0287-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="b0287-119">Šī opcija norāda, ka krājumi tiks automātiski noregulēti uz vērtību 0 saīsinātas izdošanas atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="b0287-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="b0287-120">Laukā **Noklusējuma korekcijas veida kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b0287-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="b0287-121">Piemēram, izmantojot USMF, jūs varat atlasīt 'Noņemt Res Adj Out'.</span><span class="sxs-lookup"><span data-stu-id="b0287-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="b0287-122">Laukā **Krājuma atkārtots sadalījums** atlasiet 'Manuāls'.</span><span class="sxs-lookup"><span data-stu-id="b0287-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="b0287-123">Ja atlasāt Manuāls vai Automātisks un manuāls, noliktavas darbiniekam jāļauj izmantot manuālu atkārtotu sadali.</span><span class="sxs-lookup"><span data-stu-id="b0287-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="b0287-124">Iestatīt darbinieku manuālas krājuma atkārtotas sadales izmantošanai</span><span class="sxs-lookup"><span data-stu-id="b0287-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="b0287-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b0287-125">Close the page.</span></span>
2. <span data-ttu-id="b0287-126">Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Nodarbinātais**.</span><span class="sxs-lookup"><span data-stu-id="b0287-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="b0287-127">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="b0287-127">Click **Edit**.</span></span>
4. <span data-ttu-id="b0287-128">Sarakstā atlasiet darbinieks 24.</span><span class="sxs-lookup"><span data-stu-id="b0287-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="b0287-129">Izvērsiet kopsavilkuma cilni **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="b0287-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="b0287-130">Atlasiet 'Jā' laukā **Atļaut manuālu krājuma atkārtotu sadali**.</span><span class="sxs-lookup"><span data-stu-id="b0287-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

