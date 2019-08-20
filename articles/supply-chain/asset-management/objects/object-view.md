---
title: Līdzekļa skats
description: Šajā tēmā ir aprakstīts līdzekļa skats Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63e5ec5b2a47706763df8105932d722986535a9b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783431"
---
# <a name="asset-view"></a><span data-ttu-id="bebc0-103">Līdzekļa skats</span><span class="sxs-lookup"><span data-stu-id="bebc0-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bebc0-104">Šajā tēmā ir aprakstīts līdzekļa skats Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="bebc0-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="bebc0-105">Lapā **Līdzekļa skats** tiek rādīti aktīvie līdzekļi un funkcionālie novietojumi koka skatā.</span><span class="sxs-lookup"><span data-stu-id="bebc0-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="bebc0-106">Tāpēc varat viegli iegūt pārskatu par līdzekļa relācijām funkcionālajiem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="bebc0-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="bebc0-107">Turklāt varat skatīt detalizētu informāciju par funkcionālajiem novietojumiem, līdzekļiem un saistītiem materiālu komplektiem (MK).</span><span class="sxs-lookup"><span data-stu-id="bebc0-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="bebc0-108">Varat arī ātri iegūt pārskatu par aktīvajiem uzturēšanas pieprasījumiem un darba pasūtījumiem, kas saistīti ar līdzekli.</span><span class="sxs-lookup"><span data-stu-id="bebc0-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="bebc0-109">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Līdzekļa skats**.</span><span class="sxs-lookup"><span data-stu-id="bebc0-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="bebc0-110">Lai mainītu skatu, kas tiek parādīts lapā, atlasiet jaunu vērtību laukā **Skats**.</span><span class="sxs-lookup"><span data-stu-id="bebc0-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bebc0-111">Noklusējuma skats, kas tiek parādīts, atverot lapu **Līdzekļa skats**, ir atkarīgs no vērtības, kura ir atlasīta lapas **Līdzekļu pārvaldības parametri** cilnes **Līdzekļi** laukā **Skats** (**Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļu pārvaldības parametri**).</span><span class="sxs-lookup"><span data-stu-id="bebc0-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="bebc0-112">Lapas labajā malā kopsavilkuma cilnes parāda atlasītā skata detalizēto informāciju.</span><span class="sxs-lookup"><span data-stu-id="bebc0-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="bebc0-113">Atpakaļceļa taka, kas tiek parādīta virs koka skata, parāda pašreizējo atlasi koka skatā.</span><span class="sxs-lookup"><span data-stu-id="bebc0-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="bebc0-114">Šī atpakaļceļa taka izmanto šādu formātu:</span><span class="sxs-lookup"><span data-stu-id="bebc0-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="bebc0-115">Funkcionālā novietojuma ID / Funkcionālā novietojuma ID (ja ir vairāk nekā viens funkcionālais novietojums) \> Līdzekļa ID / Līdzekļa ID (ja ir vairāk nekā viens līdzeklis) – krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="bebc0-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="bebc0-116">Ja esat atlasījis līdzekli koka skatā, varat atlasīt **Aktīvos pieprasījumus** vai **Aktīvos darba pasūtījumus**, lai skatītu ar līdzekli saistītos uzturēšanas pieprasījumus vai darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bebc0-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="bebc0-117">Varat arī atlasīt **Atvērt** \> **Funkcionālais novietojums**, **Līdzeklis** vai **Līdzekļa MK**, lai atvērtu saistīto skatu.</span><span class="sxs-lookup"><span data-stu-id="bebc0-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="bebc0-118">Opcija **Līdzekļu funkcionālie novietojumi**, kuru var atlasīt laukā **Skats**, ir pieejama arī jebkurā līdzekļa uzmeklēšanas sarakstā, kur varat atlasīt līdzekli.</span><span class="sxs-lookup"><span data-stu-id="bebc0-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="bebc0-119">Koka skats tiek rādīts cilnē **Līdzekļa skats**, piemēram, kur [izveidot līdzekli](../objects/create-an-object.md) izveidojat uzturēšanas pieprasījumu vai izveidojat darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="bebc0-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
