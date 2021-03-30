---
title: Pamatlīdzekļa iegādes priekšlikums
description: Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205032"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="949e5-103">Pamatlīdzekļa iegādes priekšlikums</span><span class="sxs-lookup"><span data-stu-id="949e5-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="949e5-104">Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="949e5-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="949e5-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="949e5-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="949e5-106">Lai iegūtu pamatlīdzekli, izmantojot pamatlīdzekļu priekšlikumu žurnālu, vispirms ir jāizveido pamatlīdzekļa ieraksts un pēc tam jādefinē iegādes cena pamatlīdzekļu grāmatā.</span><span class="sxs-lookup"><span data-stu-id="949e5-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="949e5-107">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="949e5-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="949e5-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="949e5-108">Select **New**.</span></span>
3. <span data-ttu-id="949e5-109">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="949e5-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="949e5-110">Darbību rūtī atlasiet **Rindiņas**.</span><span class="sxs-lookup"><span data-stu-id="949e5-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="949e5-111">Atlasiet **Priekšlikumi**.</span><span class="sxs-lookup"><span data-stu-id="949e5-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="949e5-112">Atlasiet **Iegādes priekšlikums**.</span><span class="sxs-lookup"><span data-stu-id="949e5-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="949e5-113">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="949e5-113">Select **Filter**.</span></span> <span data-ttu-id="949e5-114">Atlasiet **Atiestatīt**, lai notīrītu iepriekšējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="949e5-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="949e5-115">Atlasiet rindu **Pamatlīdzekļa numurs**.</span><span class="sxs-lookup"><span data-stu-id="949e5-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="949e5-116">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="949e5-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="949e5-117">Iestatiet atlikušos kritērijus pamatlīdzekļiem, kurus vēlaties iegūt, izmantojot šo priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="949e5-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="949e5-118">Atlasiet **Labi** divas reizes, lai izietu no rūts.</span><span class="sxs-lookup"><span data-stu-id="949e5-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="949e5-119">Pārbaudiet izveidotās transakcijas rindas.</span><span class="sxs-lookup"><span data-stu-id="949e5-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="949e5-120">Tikai pamatlīdzekļi ar iegādes datumu un iegādes cenu, kas ir iestatīta grāmatā, tiks iekļauti iegādes priekšlikumā.</span><span class="sxs-lookup"><span data-stu-id="949e5-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="949e5-121">Lapā atlasiet cilni **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="949e5-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="949e5-122">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="949e5-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]