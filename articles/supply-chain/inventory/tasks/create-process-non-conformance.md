---
title: Atbilstības izveide un apstrāde
description: Šajā tēmā ir paskaidrots, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383623"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="42394-103">Atbilstības izveide un apstrāde</span><span class="sxs-lookup"><span data-stu-id="42394-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42394-104">Šajā tēmā ir paskaidrots, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="42394-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="42394-105">Šo ierakstu var palaist USMF demonstrācijas uzņēmumā un var izmantot ieteiktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="42394-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="42394-106">Parasti šo procedūru veic kvalitātes darbinieks.</span><span class="sxs-lookup"><span data-stu-id="42394-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="42394-107">Vispirms jums jāizpilda prasības tēmā [Preču kvalitātes inspekcija](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md)</span><span class="sxs-lookup"><span data-stu-id="42394-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="42394-108">Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš palaiž uzdevumu ierakstu, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="42394-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="42394-109">Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="42394-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="42394-110">Atlasiet kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="42394-110">Select a quality order</span></span>
1. <span data-ttu-id="42394-111">Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Periodiskie uzdevumi > Kvalitātes vadība > Kvalitātes pārbaudes pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="42394-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="42394-112">Sarakstā atlasiet kvalitātes pasūtījumu, kas tika izveidots tēmā [Preču kvalitātes inspekcija](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="42394-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="42394-113">Neatbilstības izveide</span><span class="sxs-lookup"><span data-stu-id="42394-113">Create a nonconformance</span></span>
1. <span data-ttu-id="42394-114">Darbību rūtī atlasiet **Pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="42394-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="42394-115">Atlasiet **Neatbilstības**.</span><span class="sxs-lookup"><span data-stu-id="42394-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="42394-116">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="42394-116">Select **New**.</span></span>
4. <span data-ttu-id="42394-117">Lauka **Problēmas veids** nolaižamajā izvēlnē atlasiet problēmu, kas tika atrasta inspekcijā.</span><span class="sxs-lookup"><span data-stu-id="42394-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="42394-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="42394-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="42394-119">Neatbilstības apstiprināšana/noraidīšana</span><span class="sxs-lookup"><span data-stu-id="42394-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="42394-120">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="42394-120">Select **Functions**.</span></span>
2. <span data-ttu-id="42394-121">Atlasiet **Apstiprināt neatbilstību**.</span><span class="sxs-lookup"><span data-stu-id="42394-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="42394-122">Šim piemēram apstipriniet neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="42394-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="42394-123">Apstiprinātas neatbilstības var saistīt ar saistītām darbībām, lai reģistrētu darbu, kas veikts kā daļa no neatbilstības apstrādes un, kā šajā tēmā aprakstīts, labojošo darbību apstrādi.</span><span class="sxs-lookup"><span data-stu-id="42394-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="42394-124">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="42394-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="42394-125">Labojuma darbības izveide</span><span class="sxs-lookup"><span data-stu-id="42394-125">Create a correction action</span></span>
1. <span data-ttu-id="42394-126">Atlasiet **Labojumi**.</span><span class="sxs-lookup"><span data-stu-id="42394-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="42394-127">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="42394-127">Select **New**.</span></span>
3. <span data-ttu-id="42394-128">Jaunās rindas laukā **Personāla numura** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="42394-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="42394-129">Noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="42394-129">Click **Select**.</span></span>
5. <span data-ttu-id="42394-130">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="42394-130">Select **Attach**.</span></span> <span data-ttu-id="42394-131">Izveidojiet piezīmi par šo labojumu.</span><span class="sxs-lookup"><span data-stu-id="42394-131">Create a note about the correction.</span></span> <span data-ttu-id="42394-132">Šajā piemērā darbība ir sazināties ar kreditoru, lai apspriestu neatbilstības gadījumu.</span><span class="sxs-lookup"><span data-stu-id="42394-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="42394-133">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="42394-133">Select **New**.</span></span>
7. <span data-ttu-id="42394-134">Atlasiet **Piezīme**.</span><span class="sxs-lookup"><span data-stu-id="42394-134">Select **Note**.</span></span> <span data-ttu-id="42394-135">Atkarībā no pārskata iestatījumiem iestatījumiem, kas saistīti ar neatbilstību pārvaldību, var izdrukāt dažādus dokumentu veidus.</span><span class="sxs-lookup"><span data-stu-id="42394-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="42394-136">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="42394-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="42394-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="42394-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="42394-138">Labojuma uzturēšana</span><span class="sxs-lookup"><span data-stu-id="42394-138">Maintain a correction</span></span>
1. <span data-ttu-id="42394-139">Atlasiet **Atzīmēt kā pabeigtu**.</span><span class="sxs-lookup"><span data-stu-id="42394-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="42394-140">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="42394-140">Select **OK**.</span></span>
3. <span data-ttu-id="42394-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="42394-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="42394-142">Neatbilstības aizvēršana</span><span class="sxs-lookup"><span data-stu-id="42394-142">Close a nonconformance</span></span>
1. <span data-ttu-id="42394-143">Atlasiet **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="42394-143">Select **Functions**.</span></span>
2. <span data-ttu-id="42394-144">Atlasiet **Aizvērt neatbilstību**.</span><span class="sxs-lookup"><span data-stu-id="42394-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="42394-145">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="42394-145">Select **Yes**.</span></span>
4. <span data-ttu-id="42394-146">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="42394-146">Close the pages.</span></span>
