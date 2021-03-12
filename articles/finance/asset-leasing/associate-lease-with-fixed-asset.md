---
title: Pamatlīdzekļu saistīšana ar nomu
description: Tēmā ir paskaidrots, kā esošu pamatlīdzekli saistīt ar jaunu nomu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 274fcc73b48282a8025a210dd488105500609d5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971432"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="d044b-103">Pamatlīdzekļu saistīšana ar nomu</span><span class="sxs-lookup"><span data-stu-id="d044b-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d044b-104">Tēmā ir paskaidrots, kā esošu pamatlīdzekli saistīt ar jaunu nomu.</span><span class="sxs-lookup"><span data-stu-id="d044b-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="d044b-105">Saistot pamatlīdzekli ar nomu, līdzekļa lietošanas tiesību (LLT) vērtība sākotnējā atzīšanā būs pamatlīdzekļa iegādes izmaksas.</span><span class="sxs-lookup"><span data-stu-id="d044b-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="d044b-106">Pirms varat pamatlīdzekli saistīt ar nomu, pamatlīdzeklim ir jāizveido ieraksts pie Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="d044b-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="d044b-107">Pēc tam lapā **Nomas kopsavilkums** ir jāizveido noma un pamatlīdzeklis jāsaista ar šo nomu.</span><span class="sxs-lookup"><span data-stu-id="d044b-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="d044b-108">Nomas pievienošana, izpildot darbības [Nomas pievienošana vai kopēšana](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="d044b-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="d044b-109">Lapas **Pievienot nomu** laukā **Pamatlīdzekļa numurs** atlasiet līdzekli, kas vēl nav iegūts.</span><span class="sxs-lookup"><span data-stu-id="d044b-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="d044b-110">Atlasiet **Grāmatas** un apstipriniet maksājuma grafiku.</span><span class="sxs-lookup"><span data-stu-id="d044b-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="d044b-111">Atlasiet **Sākotnējā atzīšana**.</span><span class="sxs-lookup"><span data-stu-id="d044b-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="d044b-112">Atlasiet **Līdzekļu nomas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="d044b-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="d044b-113">Nomas sākotnējās atzīšanas žurnāla ieraksts ieraksta debetā pamatlīdzekli par summu, kas parasti tiek ierakstīts debetā LLT kontā.</span><span class="sxs-lookup"><span data-stu-id="d044b-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="d044b-114">Tagad varat skatīt pamatlīdzekļa darījuma veidu un grāmatu.</span><span class="sxs-lookup"><span data-stu-id="d044b-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="d044b-115">Atlasiet **Žurnāla detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="d044b-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="d044b-116">Atlasiet **Rindas**, lai skatītu atsevišķas žurnāla ieraksta rindas.</span><span class="sxs-lookup"><span data-stu-id="d044b-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="d044b-117">Atlasiet žurnāla rindu, kas satur līdzekli, un pēc tam atlasiet cilni **Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="d044b-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="d044b-118">Cilnē **Pamatlīdzekļi** tiek parādīts darījuma veids un grāmata.</span><span class="sxs-lookup"><span data-stu-id="d044b-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="d044b-119">Pēc noklusējuma lauks **Darījuma veids** ir iestatīts uz **Iegāde**, un lauks **Grāmata** ir iestatīts uz pašreizējo pamatlīdzekļu grāmatu.</span><span class="sxs-lookup"><span data-stu-id="d044b-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="d044b-120">Pēc sākotnējās atzīšanas žurnāla ieraksta grāmatošanas darījums tiek parādīts kā pamatlīdzekļa iegādes darījums.</span><span class="sxs-lookup"><span data-stu-id="d044b-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="d044b-121">Lai skatītu darījuma tabulu, dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**, atlasiet atbilstošo līdzekli un pēc tam atlasiet **Novērtējumi**.</span><span class="sxs-lookup"><span data-stu-id="d044b-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="d044b-122">Jums vajadzētu redzēt, ka sākotnējās atzīšanas žurnāla ieraksts ir izveidojis attiecīgā pamatlīdzekļa iegūšanas darījumu.</span><span class="sxs-lookup"><span data-stu-id="d044b-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="d044b-123">Tagad pamatlīdzeklim var aprēķināt nolietojumu, izmantojot standarta nolietojuma funkcionalitāti Pamatlīdzekļos.</span><span class="sxs-lookup"><span data-stu-id="d044b-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="d044b-124">Papildinformāciju par nolietojum skatiet [Nolietojuma metodes un konvencijas](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="d044b-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d044b-125">Ja saistāt pamatlīdzekli ar nomu, Līdzekļa nomā pogas **Līdzekļa nolietojums** un **Nomas vērtības samazinājums** ir atspējotas.</span><span class="sxs-lookup"><span data-stu-id="d044b-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="d044b-126">Varat skatīt līdzekļa nolietojumu un nomas vērtības samazinājuma darījumus no Pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="d044b-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="d044b-127">Poga **Līdzekļu darījumi**, kas atver pieprasījuma formu, arī ir atspējota.</span><span class="sxs-lookup"><span data-stu-id="d044b-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="d044b-128">Arī pieprasījumu **Līdzekļa darījumi** varat atvērt Pamatlīdzekļos.</span><span class="sxs-lookup"><span data-stu-id="d044b-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  
