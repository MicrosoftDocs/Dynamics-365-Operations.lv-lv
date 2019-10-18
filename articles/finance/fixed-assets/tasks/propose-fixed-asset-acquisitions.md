---
title: Pamatlīdzekļa iegādes priekšlikums
description: Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178818"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="c1d2b-103">Pamatlīdzekļa iegādes priekšlikums</span><span class="sxs-lookup"><span data-stu-id="c1d2b-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1d2b-104">Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="c1d2b-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="c1d2b-106">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="c1d2b-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-107">Select **New**.</span></span>
3. <span data-ttu-id="c1d2b-108">Ievadiet vai atlasiet vērtību laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="c1d2b-109">Darbību rūtī atlasiet **Rindiņas**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="c1d2b-110">Atlasiet **Priekšlikumi**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="c1d2b-111">Atlasiet **Iegādes priekšlikums**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="c1d2b-112">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-112">Select **Filter**.</span></span> <span data-ttu-id="c1d2b-113">Atlasiet **Atiestatīt**, lai notīrītu iepriekšējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="c1d2b-114">Atlasiet rindu **Pamatlīdzekļa numurs**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="c1d2b-115">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="c1d2b-116">Iestatiet atlikušos kritērijus pamatlīdzekļiem, kurus vēlaties iegūt, izmantojot šo priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="c1d2b-117">Atlasiet **Labi** divas reizes, lai izietu no rūts.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="c1d2b-118">Pārbaudiet izveidotās transakcijas rindas.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="c1d2b-119">Tikai pamatlīdzekļi ar iegādes datumu un iegādes cenu, kas ir iestatīta grāmatā, tiks iekļauti iegādes priekšlikumā.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="c1d2b-120">Lapā atlasiet cilni **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="c1d2b-121">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="c1d2b-121">Select **Post**.</span></span>

