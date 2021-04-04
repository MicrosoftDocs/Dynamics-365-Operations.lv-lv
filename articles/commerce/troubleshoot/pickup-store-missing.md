---
title: Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, no kuriem saņemt
description: Šajā tēmā ir sniegti problēmu novēršanas norādes, kas var palīdzēt, kad mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, kuros var saņemt preces.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585436"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="1f50a-103">Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, no kuriem saņemt</span><span class="sxs-lookup"><span data-stu-id="1f50a-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f50a-104">Šajā tēmā ir sniegti problēmu novēršanas norādes, kas var palīdzēt, kad mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, kuros var saņemt preces.</span><span class="sxs-lookup"><span data-stu-id="1f50a-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="1f50a-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1f50a-105">Description</span></span>

<span data-ttu-id="1f50a-106">Mazumtirdzniecības veikals netiek parādīts to veikalu sarakstā, kuros var saņemt preces.</span><span class="sxs-lookup"><span data-stu-id="1f50a-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="1f50a-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="1f50a-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="1f50a-108">Veikala adreses garuma un platuma konfigurēšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1f50a-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="1f50a-109">Lai konfigurētu veikala adreses garumu un platumu programmā Commerce Headquarters, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="1f50a-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1f50a-110">Parejiet uz **Mazumtirdzniecība un komercija \> Kanāli \> Veikali \> Visi veikali**.</span><span class="sxs-lookup"><span data-stu-id="1f50a-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="1f50a-111">Atrodiet veikalu, kuru vēlaties redzēt saņemšanas opcijās e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="1f50a-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="1f50a-112">Atzīmējiet tās vērtību **Pārvaldības struktūrvienības numurs**.</span><span class="sxs-lookup"><span data-stu-id="1f50a-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="1f50a-113">Pārejiet uz sadaļu **Organizācijas administrēšana \> Organizācijas \> Pārvaldības struktūrvienības**.</span><span class="sxs-lookup"><span data-stu-id="1f50a-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="1f50a-114">Meklējiet pārvaldības struktūrvienības numuru, ko iepriekš atzīmējāt, un pēc tam meklēšanas rezultātos atlasiet pārvaldības struktūrvienību.</span><span class="sxs-lookup"><span data-stu-id="1f50a-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="1f50a-115">Kopsavilkuma cilnē **Adreses** atlasiet **Papildu opcijas** un pēc tam atlasiet **Papildu**.</span><span class="sxs-lookup"><span data-stu-id="1f50a-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="1f50a-116">Kopsavilkuma cilnē **Vispārīgi** pārliecinieties, vai lauki **Garums** un **Platums** ir pareizi iestatīti.</span><span class="sxs-lookup"><span data-stu-id="1f50a-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="1f50a-117">Šīs darbības ietvaros pārliecinieties, vai vērtības ir pareizi norādītas kā pozitīvi vai negatīvi skaitļi.</span><span class="sxs-lookup"><span data-stu-id="1f50a-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="1f50a-118">Izpildes grupu konfigurēšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1f50a-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="1f50a-119">Lai konfigurētu izpildes grupas Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1f50a-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1f50a-120">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāli \> Tiešsaistes veikali**.</span><span class="sxs-lookup"><span data-stu-id="1f50a-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="1f50a-121">Atlasiet konfigurējamo tiešsaistes veikalu.</span><span class="sxs-lookup"><span data-stu-id="1f50a-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="1f50a-122">Darbību rūtī atlasiet cilni **Iestatīšana** un pēc tam atlasiet **Izpilde/grupas piešķire**.</span><span class="sxs-lookup"><span data-stu-id="1f50a-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="1f50a-123">Lapā **Izpilde/s grupas piešķire** atlasiet tiešsaistes veikala izpildes grupu.</span><span class="sxs-lookup"><span data-stu-id="1f50a-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="1f50a-124">Sadaļā **Iestatījumi** pārliecinieties, vai mazumtirdzniecības veikals ir pareizi konfigurēts izpildes grupai.</span><span class="sxs-lookup"><span data-stu-id="1f50a-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f50a-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1f50a-125">Additional resources</span></span> 

[<span data-ttu-id="1f50a-126">Pārvaldības struktūrvienības izveide</span><span class="sxs-lookup"><span data-stu-id="1f50a-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="1f50a-127">Tiešsaistes kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1f50a-127">Set up an online channel</span></span>](../channel-setup-online.md)