---
title: Izveidot tiešsaistes kanālu un definēt kanāla atribūtus
description: Šajā procedūrā parādīts, kā izveidot jaunu tiešsaistes kanālu un pievienot to organizācijas hierarhijai.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140953"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="94e0d-103">Izveidot tiešsaistes kanālu un definēt kanāla atribūtus</span><span class="sxs-lookup"><span data-stu-id="94e0d-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94e0d-104">Šajā procedūrā parādīts, kā izveidot jaunu tiešsaistes kanālu un pievienot to organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="94e0d-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="94e0d-105">Lai izveidotu jaunu tiešsaistes kanālu, vispirms ir jāizveido organizācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="94e0d-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="94e0d-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="94e0d-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="94e0d-107">Izveidot jaunu tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="94e0d-107">Create a new online channel</span></span>
1. <span data-ttu-id="94e0d-108">Dodieties uz Mazumtirdzniecība un tirdzniecība > Kanāli > Tiešsaistes veikali.</span><span class="sxs-lookup"><span data-stu-id="94e0d-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="94e0d-109">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="94e0d-109">Click New.</span></span>
3. <span data-ttu-id="94e0d-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="94e0d-111">Laukā Noliktava ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="94e0d-112">Laukā Noliktavas laika josla atlasiet atbilstošo opciju.</span><span class="sxs-lookup"><span data-stu-id="94e0d-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="94e0d-113">Laukā Noklusējuma debitors ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="94e0d-114">Laukā Debitoru adrešu grāmata ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="94e0d-115">Laukā Apmaksas nosacījumi ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="94e0d-116">Laukā Maksājuma metode ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="94e0d-117">Laukā E-pasta paziņojumu profils ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="94e0d-118">Izvērsiet sadaļu Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="94e0d-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="94e0d-119">Laukā Biznesa vienība ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="94e0d-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="94e0d-120">Tādā pašā veidā iestatiet vērtību visām pārējām noklusējuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="94e0d-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="94e0d-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="94e0d-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="94e0d-122">Tiešsaistes kanāla pievienošana organizācijas hierarhijai</span><span class="sxs-lookup"><span data-stu-id="94e0d-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="94e0d-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="94e0d-123">Close the page.</span></span>
2. <span data-ttu-id="94e0d-124">Dodieties uz Organizācijas administrēšana > Organizācijas > Organizāciju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="94e0d-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="94e0d-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="94e0d-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="94e0d-126">Noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="94e0d-126">Click View.</span></span>
5. <span data-ttu-id="94e0d-127">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="94e0d-127">Click Edit.</span></span>
    * <span data-ttu-id="94e0d-128">Varat atlasīt jebkuru hierarhijas mezglu, kam vēlaties pievienot jaunu kanālu.</span><span class="sxs-lookup"><span data-stu-id="94e0d-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="94e0d-129">Klikšķiniet Ievietot.</span><span class="sxs-lookup"><span data-stu-id="94e0d-129">Click Insert.</span></span>
7. <span data-ttu-id="94e0d-130">Noklikšķiniet uz Tirdzniecības kanāls.</span><span class="sxs-lookup"><span data-stu-id="94e0d-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="94e0d-131">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="94e0d-131">Click OK.</span></span>
9. <span data-ttu-id="94e0d-132">Noklikšķiniet uz Publicēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="94e0d-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="94e0d-133">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="94e0d-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="94e0d-134">Noklikšķiniet uz Publicēt.</span><span class="sxs-lookup"><span data-stu-id="94e0d-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="94e0d-135">Pasūtījumu konfigurēšana gandrīz reāllaika paziņojumam</span><span class="sxs-lookup"><span data-stu-id="94e0d-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="94e0d-136">Pārejiet uz sadaļu Mazumtirdzniecība un tirdzniecība > Centrālā biroja iestatīšana > Parametri > Tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="94e0d-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="94e0d-137">Vienumam “Izmantot reāllaika pakalpojumu e-komercijas pasūtījuma izveidei” iestatiet uz “Jā”.</span><span class="sxs-lookup"><span data-stu-id="94e0d-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="94e0d-138">Palaidiet sadales grafiku 1070, lai sinhronizētu izmaiņas ar kanālu datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="94e0d-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


