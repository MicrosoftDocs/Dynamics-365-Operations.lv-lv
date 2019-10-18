---
title: Funkcionālie novietojumi un līdzekļi
description: Šajā tēmā aprakstīti funkcionālie novietojumi un līdzekļi Līdzekļu pārvaldībā. Līdzekļu pārvaldība ir uzlabots modulis līdzekļu un uzturēšanas darbu pārvaldībai programmā Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 5271b673d758608cae8e43d72b7e75b259d5f142
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024618"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="8ad91-104">Funkcionālie novietojumi un līdzekļi</span><span class="sxs-lookup"><span data-stu-id="8ad91-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8ad91-105">Šajā tēmā aprakstīti funkcionālie novietojumi un līdzekļi Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="8ad91-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="8ad91-106">Līdzekļu pārvaldība ir uzlabots modulis līdzekļu un uzturēšanas darbu pārvaldībai programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8ad91-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="8ad91-107">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="8ad91-107">Overview</span></span>

<span data-ttu-id="8ad91-108">Līdzekļu pārvaldība ir cieši integrēta ar vairākiem moduļiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8ad91-108">Asset Management is integrated seamlessly with several modules in Finance and Operations.</span></span> <span data-ttu-id="8ad91-109">Nākamajā attēlā ir parādīti interfeisi ar citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="8ad91-109">The following illustration shows the interfaces with other modules.</span></span>

![1. attēls](media/01-overview-image.png)

<span data-ttu-id="8ad91-111">Līdzekļu pārvaldība ļauj efektīvi pārvaldīt un izpildīt visus uzdevumus, kas saistīti ar dažāda veida iekārtu pārvaldīšanu un apkopi uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="8ad91-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="8ad91-112">Šajā aprīkojumā ietilpst mašīnas, ražošanas iekārtas un transportlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="8ad91-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="8ad91-113">Līdzekļu pārvaldība arī atbalsta risinājumus daudzās nozarēs.</span><span class="sxs-lookup"><span data-stu-id="8ad91-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="8ad91-114">Nākamajā attēlā ir parādīts pārskats par galveno funkcionalitāti, ko ietver Līdzekļu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="8ad91-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![2. attēls](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="8ad91-116">Funkcionālie novietojumi un līdzekļi</span><span class="sxs-lookup"><span data-stu-id="8ad91-116">Functional locations and assets</span></span>

<span data-ttu-id="8ad91-117">Funkcionālie novietojumi tiek izmantoti, lai pārvaldītu līdzekļus to atrašanās vietās.</span><span class="sxs-lookup"><span data-stu-id="8ad91-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="8ad91-118">Šī pārvaldība ietver līdzekļu izmaksu izsekošanu funkcionālajos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="8ad91-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="8ad91-119">Funkcionālie novietojumi tiek strukturēti hierarhiski, un atrašanās vietām var būt apakšvietas.</span><span class="sxs-lookup"><span data-stu-id="8ad91-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="8ad91-120">Funkcionālo novietojumu struktūra ir statiska.</span><span class="sxs-lookup"><span data-stu-id="8ad91-120">The structure of functional locations is static.</span></span> <span data-ttu-id="8ad91-121">Citiem vārdiem sakot, atrašanās vietas nevar mainīt vietu.</span><span class="sxs-lookup"><span data-stu-id="8ad91-121">In other words, locations can't change place.</span></span> <span data-ttu-id="8ad91-122">Līdzekļus var uzstādīt funkcionālajos novietojumos un pēc vajadzības vēlāk tos var uzstādīt citos funkcionālajos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="8ad91-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="8ad91-123">Līdzekļa izmaksās vienmēr tiek ievērota līdzekļa atrašanās vieta.</span><span class="sxs-lookup"><span data-stu-id="8ad91-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="8ad91-124">Citiem vārdiem sakot, ja uzstādāt līdzekli jaunā funkcionālajā novietojumā, līdzeklis automātiski izmanto finanšu dimensijas, kas ir saistītas ar jauno funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="8ad91-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="8ad91-125">Tāpēc līdzekļa izmaksas vienmēr ir saistītas ar funkcionālo novietojumu, kurā līdzeklis attiecīgajā brīdī ir uzstādīts.</span><span class="sxs-lookup"><span data-stu-id="8ad91-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="8ad91-126">Šī automātiskā finanšu dimensiju apstrāde palīdz garantēt izmaksu pilnīgu izsekošanu, ja jūsu uzņēmums veic projektu kontroli un ziņošanu par funkcionālajiem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="8ad91-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="8ad91-127">Tas, kā veidojat savu funkcionālo novietojumu hierarhiju, ir atkarīgs no uzņēmuma vajadzībām attiecībā uz iekšējo iekārtu vai klientu apkalpošanas aprīkojuma uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="8ad91-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="8ad91-128">Nākamajā attēlā ir parādīts tādu funkcionālo novietojumu piemērs, kuru pamatā ir ģeogrāfiskās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="8ad91-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![3. attēls](media/03-overview-image.png)

<span data-ttu-id="8ad91-130">Nākamajā attēlā ir parādīts tādu funkcionālo novietojumu piemērs, kuru pamatā ir debitori.</span><span class="sxs-lookup"><span data-stu-id="8ad91-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![4. attēls](media/04-overview-image.png)
