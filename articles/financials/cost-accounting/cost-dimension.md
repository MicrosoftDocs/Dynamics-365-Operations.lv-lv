---
title: Dimensiju izveide un dimensijas elementu importēšana
description: Izmaksu uzskaite ir neatkarīgs modulis, kura darbības nolūkos ir nepieciešami pamatdati no citiem moduļiem.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d48ba0a0b80d251e107baa0ceeb66d8e328f13dc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "342320"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="9dbba-103">Dimensiju izveide un dimensijas elementu importēšana</span><span class="sxs-lookup"><span data-stu-id="9dbba-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dbba-104">Izmaksu uzskaite ir neatkarīgs modulis, kura darbības nolūkos ir nepieciešami dati no citiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="9dbba-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="9dbba-105">Šie dati ir iedalīti tālāk norādītajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="9dbba-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="9dbba-106">Izmaksu elementi</span><span class="sxs-lookup"><span data-stu-id="9dbba-106">Cost elements</span></span>
-  <span data-ttu-id="9dbba-107">Izmaksu objekti</span><span class="sxs-lookup"><span data-stu-id="9dbba-107">Cost objects</span></span>
-  <span data-ttu-id="9dbba-108">Statiskās dimensijas</span><span class="sxs-lookup"><span data-stu-id="9dbba-108">Statistical dimensions</span></span>

<span data-ttu-id="9dbba-109">**Izmaksu elements** atbilst ar izmaksām saistītam krājumam kontu plānā.</span><span class="sxs-lookup"><span data-stu-id="9dbba-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="9dbba-110">**Izmaksu objekts** atbilst jebkura tipa finanšu dimensijai, piemēram, precēm, izmaksu centriem un projektiem, kurus vēlaties novērtēt, kuriem vēlaties iedalīt izmaksas vai kurus vēlaties izmērīt tieši.</span><span class="sxs-lookup"><span data-stu-id="9dbba-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="9dbba-111">**Statistiskā dimensija** un tās elementi tiek izmantoti, lai reģistrētu beznaudas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="9dbba-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="9dbba-112">Statistisko dimensiju elementus var izmantot kā sadalījuma pamatu izmaksu sadalē un sadalījumā</span><span class="sxs-lookup"><span data-stu-id="9dbba-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="9dbba-113">Nākamajā diagrammā ir redzamas izmaksu uzskaitē lietotās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="9dbba-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="9dbba-114">[![Izmaksu uzskaites dimensijas](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="9dbba-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="9dbba-115">Kad dati ir importēti modulī Izmaksu uzskaite, varat tos izmantot, lai veidotu dažādas perspektīvas, kuras sniedz ieskatu vadītājiem visos organizācijas līmeņos.</span><span class="sxs-lookup"><span data-stu-id="9dbba-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="9dbba-116">Informācija par dimensiju izveidošanu un dimensiju elementu importēšanu ir sniegta tālāk uzskaitītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="9dbba-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="9dbba-117">Izmaksu elementu dimensijas</span><span class="sxs-lookup"><span data-stu-id="9dbba-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="9dbba-118">Izmaksu elementu izveide (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="9dbba-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="9dbba-119">Izmaksu objekta dimensijas</span><span class="sxs-lookup"><span data-stu-id="9dbba-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="9dbba-120">Izmaksu elementu izveide (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="9dbba-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="9dbba-121">Izmaksu elementu dimensiju elementu kartēšana uz kopīgu dimensiju elementu kopu</span><span class="sxs-lookup"><span data-stu-id="9dbba-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="9dbba-122">Izmaksu elementa dimensijas kartēšana (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="9dbba-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="9dbba-123">Statisko dimensiju elementu un statistisko mēru nodrošinātāju veidnes</span><span class="sxs-lookup"><span data-stu-id="9dbba-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






