---
title: Darbplūsmas vēstures skatīšana
description: Šajā tēmā ir aprakstītas darbības, lai apskatītu apstrādes un apstiprināšanas nolūkos darbplūsmas sistēmā iesniegta dokumenta statusu.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d7118e85ff56f8c935c24a91dc84c6cc09641e0
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694315"
---
# <a name="view-workflow-history"></a><span data-ttu-id="327be-103">Darbplūsmas vēstures skatīšana</span><span class="sxs-lookup"><span data-stu-id="327be-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="327be-104">Šajā tēmā ir aprakstītas darbības, lai apskatītu apstrādes un apstiprināšanas nolūkos darbplūsmas sistēmā iesniegta dokumenta statusu.</span><span class="sxs-lookup"><span data-stu-id="327be-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="327be-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="327be-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="327be-106">Dodieties uz **Navigācijas rūts > Moduļi > Kopīgi > Vaicājumi > Darbplūsma > Darbplūsmas vēsture**.</span><span class="sxs-lookup"><span data-stu-id="327be-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="327be-107">Lietojiet šo veidlapu, lai apskatītu apstrādes un apstiprināšanas nolūkos darbplūsmas sistēmā iesniegta dokumenta statusu.</span><span class="sxs-lookup"><span data-stu-id="327be-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="327be-108">**Instances ID** ir identifikācijas kods tādai darbplūsmas instancei, kura apstrādā vai ir apstrādājusi šo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="327be-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="327be-109">**Statuss** ir dokumenta darbplūsmas statuss.</span><span class="sxs-lookup"><span data-stu-id="327be-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="327be-110">**Darbplūsmas ID** ir identifikācijas kods tādai darbplūsmai, kas apstrādā vai ir apstrādājusi šo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="327be-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="327be-111">**Dokuments** ir dokumenta identifikācijas kods.</span><span class="sxs-lookup"><span data-stu-id="327be-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="327be-112">**Dokumenta veids** ir apstrādei iesniegtā dokumenta veids.</span><span class="sxs-lookup"><span data-stu-id="327be-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="327be-113">**Darbplūsma** ir nosaukums tādai darbplūsmai, kas apstrādā vai ir apstrādājusi šo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="327be-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="327be-114">**Versija** ir versijas numurs tādai darbplūsmai, kas apstrādā vai ir apstrādājusi šo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="327be-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="327be-115">**Izveides datums un laiks** ir dokumenta iesniegšanas datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="327be-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="327be-116">**Patērētais laiks** ir laiks, cik pagājis kopš dokumenta iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="327be-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="327be-117">Ar pogu **Atsākt** jūs atlasītajam dokumentam varat atsākt darbplūsmas procesu.</span><span class="sxs-lookup"><span data-stu-id="327be-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="327be-118">Ar pogu **Atsaukt** jūs varat atsaukt atlasīto dokumentu, lai tas netiktu apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="327be-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="327be-119">Sarakstā atlasiet saiti vēlamajā rindā.</span><span class="sxs-lookup"><span data-stu-id="327be-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="327be-120">Pārliecinieties, ka sadaļa **Darba vienumi** ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="327be-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="327be-121">Šajā sadaļā varat skatīt darba vienumus, kas ir saistīti ar atlasīto dokumentu.</span><span class="sxs-lookup"><span data-stu-id="327be-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="327be-122">Piemēram, ir jāpabeidz kāds uzdevums vai ir jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="327be-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="327be-123">Ar pogu **Mainīt piešķiri** tiek atvērts dialoglodziņš, kur darba vienumu varat piešķirt citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="327be-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="327be-124">Pārliecinieties, ka sadaļa **Izsekošanas detaļas** ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="327be-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="327be-125">Šajā sadaļā varat apskatīt atlasītā dokumenta darbplūsmas vēsturi.</span><span class="sxs-lookup"><span data-stu-id="327be-125">In this section you can view the workflow history of the selected document.</span></span>  

