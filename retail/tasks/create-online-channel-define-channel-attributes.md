--- 
title: " Tiešsaistes kanālu izveide un kanāla atribūtu definēšana"
description: "Šajā procedūrā parādīts, kā izveidot jaunu tiešsaistes kanālu un pievienot to organizācijas hierarhijai."
author: jashanno
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 748c536692043a4cfe7d8b087066e12b3e7ddadc
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-online-channels-and-define-channel-attributes"></a><span data-ttu-id="cc8dd-103"> Tiešsaistes kanālu izveide un kanāla atribūtu definēšana</span><span class="sxs-lookup"><span data-stu-id="cc8dd-103">Create online channels and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cc8dd-104">Šajā procedūrā parādīts, kā izveidot jaunu tiešsaistes kanālu un pievienot to organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="cc8dd-105">Lai izveidotu jaunu tiešsaistes kanālu, vispirms ir jāizveido organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="cc8dd-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="cc8dd-107">Izveidot jaunu tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="cc8dd-107">Create a new online channel</span></span>
1. <span data-ttu-id="cc8dd-108">Dodieties uz Mazumtirdzniecība un komercija > Kanāli > Tiešsaistes veikali.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="cc8dd-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-109">Click New.</span></span>
3. <span data-ttu-id="cc8dd-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cc8dd-111">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="cc8dd-112">Laukā Noliktavas laika josla atlasiet atbilstošo opciju.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="cc8dd-113">Laukā Noklusējuma debitors ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="cc8dd-114">Laukā Debitoru adrešu grāmata ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="cc8dd-115">Laukā Apmaksas nosacījumi ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="cc8dd-116">Laukā Maksājuma metode ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="cc8dd-117">Laukā E-pasta paziņojumu profils ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="cc8dd-118">Izvērsiet sadaļu Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="cc8dd-119">Laukā Biznesa vienība ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="cc8dd-120">Tādā pašā veidā iestatiet vērtību visām pārējām noklusējuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="cc8dd-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="cc8dd-122">Tiešsaistes kanāla pievienošana organizācijas hierarhijai</span><span class="sxs-lookup"><span data-stu-id="cc8dd-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="cc8dd-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-123">Close the page.</span></span>
2. <span data-ttu-id="cc8dd-124">Dodieties uz Organizācijas administrēšana > Organizācijas > Organizāciju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="cc8dd-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cc8dd-126">Noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-126">Click View.</span></span>
5. <span data-ttu-id="cc8dd-127">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-127">Click Edit.</span></span>
    * <span data-ttu-id="cc8dd-128">Varat atlasīt jebkuru hierarhijas mezglu, kam vēlaties pievienot jaunu kanālu.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="cc8dd-129">Klikšķiniet Ievietot.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-129">Click Insert.</span></span>
7. <span data-ttu-id="cc8dd-130">Noklikšķiniet uz Mazumtirdzniecības kanāls.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-130">Click Retail channel.</span></span>
8. <span data-ttu-id="cc8dd-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-131">Click OK.</span></span>
9. <span data-ttu-id="cc8dd-132">Noklikšķiniet uz Publicēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="cc8dd-133">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="cc8dd-134">Noklikšķiniet uz Publicēt.</span><span class="sxs-lookup"><span data-stu-id="cc8dd-134">Click Publish.</span></span>


