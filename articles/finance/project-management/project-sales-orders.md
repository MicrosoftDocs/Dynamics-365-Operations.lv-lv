---
title: Projekta pārdošanas pasūtījumi laika un materiāla projektiem
description: Šajā tēmā ir sniegta informācija par to, kā izveidot no projekta atkarīgus pārdošanas pasūtījumus laika un materiāla projektiem.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551206"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="19387-103">Projekta pārdošanas pasūtījumi laika un materiāla projektiem</span><span class="sxs-lookup"><span data-stu-id="19387-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="19387-104">Šajā tēmā ir sniegta informācija par to, kā izveidot projekta pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="19387-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="19387-105">Pārdošanas pasūtījumus var izmantot tikai tipa **Laiks un materiāls** projektiem.</span><span class="sxs-lookup"><span data-stu-id="19387-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="19387-106">Ja laika un materiāla projektam projekta līgumā ir vairāki finansējuma avoti, parametru lapā **Projektu pārvaldības un uzskaites parametri** ir jāiespējo parametrs **Atļaut pārdošanas pasūtījumus projektiem ar vairākiem finansējuma avotiem**.</span><span class="sxs-lookup"><span data-stu-id="19387-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="19387-107">Projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem atbalsts ir pieejams, sākot ar programmas laidiena 10.0.2 un jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="19387-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="19387-108">Parametrs projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem atbalsta iespējošanai tiks noņemts 2020. gada aprīļa laidiena kopumā, pēc kura funkcionalitāte vienmēr būs iespējota.</span><span class="sxs-lookup"><span data-stu-id="19387-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="19387-109">No projekta atkarīgus pārdošanas pasūtījumus var izveidot divējādi.</span><span class="sxs-lookup"><span data-stu-id="19387-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="19387-110">Atveriet konkrēto projektu.</span><span class="sxs-lookup"><span data-stu-id="19387-110">Go to the project itself.</span></span> <span data-ttu-id="19387-111">Darbību rūtī atlasiet **Pārvaldīt > Krājumu uzdevumi > Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="19387-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="19387-112">Informācijā par projektu pēc noklusējuma tiek iekļauts projekta pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="19387-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="19387-113">Ja projekta līgumā ir iekļauts vairāk nekā viens finansējuma avots, vispirms ir jāatlasa finansējuma avots, lai varētu iestatīt pārdošanas pasūtījuma debitoru.</span><span class="sxs-lookup"><span data-stu-id="19387-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="19387-114">Ja ir iekļauts tikai viens projekta finansējuma avots, debitors tiek iestatīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="19387-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="19387-115">Atveriet saraksta lapu **Visi pārdošanas pasūtījumi** un izveidojiet jaunu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="19387-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="19387-116">Ir jāatlasa projekta pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="19387-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="19387-117">Kad projekts ir atlasīts, debitors tiek iestatīts pēc finansējuma avota vai arī ir jāatlasa finansējuma avots, ja projekta līgumā ir ietverti vairāki finansējuma avoti.</span><span class="sxs-lookup"><span data-stu-id="19387-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

