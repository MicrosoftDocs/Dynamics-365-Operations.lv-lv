---
title: Darbplūsmas elementi
description: Šajā tēmā ir aprakstīti dažādie elementi, kas veido darbplūsmu.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fa9613b37fceeda1ea73c5fd5d4f7a7edc74cf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "333810"
---
# <a name="workflow-elements"></a><span data-ttu-id="234f9-103">Darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="234f9-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="234f9-104">Šajā tēmā ir aprakstīti dažādie elementi, kas veido darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="234f9-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="234f9-105">Darbplūsma sastāv no elementiem.</span><span class="sxs-lookup"><span data-stu-id="234f9-105">A workflow consists of elements.</span></span> <span data-ttu-id="234f9-106">Turpmākajās sadaļās ir aprakstīts katrs elementa veids.</span><span class="sxs-lookup"><span data-stu-id="234f9-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="234f9-107">Uzdevumi</span><span class="sxs-lookup"><span data-stu-id="234f9-107">Tasks</span></span>

<span data-ttu-id="234f9-108">*Uzdevums* ir darba vienība, kas ir jāveic.</span><span class="sxs-lookup"><span data-stu-id="234f9-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="234f9-109">Darbplūsmai var pievienot divu viedu uzdevumus: manuālos uzdevumus un automatizētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="234f9-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="234f9-110">Manuāls uzdevums</span><span class="sxs-lookup"><span data-stu-id="234f9-110">Manual task</span></span>

<span data-ttu-id="234f9-111">*Manuāls uzdevums* ir darba vienība, kas ir jāveic lietotājam.</span><span class="sxs-lookup"><span data-stu-id="234f9-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="234f9-112">Piemēram, izdevumu pārskata darbplūsma var būt manuāls uzdevums, kura ietvaros norīkotajam lietotājam ir jāveic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="234f9-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="234f9-113">Jāpārskata kopā ar izdevumu pārskatu iesniegtie čeki.</span><span class="sxs-lookup"><span data-stu-id="234f9-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="234f9-114">Jāzvana darbinieka vadītājam.</span><span class="sxs-lookup"><span data-stu-id="234f9-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="234f9-115">Automatizēts uzdevums</span><span class="sxs-lookup"><span data-stu-id="234f9-115">Automated task</span></span>

<span data-ttu-id="234f9-116">*Automatizēts uzdevums* ir darba vienība, kas ir jāveic sistēmai.</span><span class="sxs-lookup"><span data-stu-id="234f9-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="234f9-117">Darbiniekam nekas nav jādara.</span><span class="sxs-lookup"><span data-stu-id="234f9-117">No human interaction is required.</span></span> <span data-ttu-id="234f9-118">Piemēram,pārdošanas pasūtījuma darbplūsma var būt automatizēts uzdevums, kura ietvaros sistēmai ir jāveic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="234f9-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="234f9-119">Jāveic kredīta pārbaude.</span><span class="sxs-lookup"><span data-stu-id="234f9-119">Perform a credit check.</span></span>
- <span data-ttu-id="234f9-120">Jāizveido debitora ieraksts, ja tāda vēl nav.</span><span class="sxs-lookup"><span data-stu-id="234f9-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="234f9-121">Apstiprināšanas procesi</span><span class="sxs-lookup"><span data-stu-id="234f9-121">Approval processes</span></span>

<span data-ttu-id="234f9-122">*Apstiprināšanas process* ir process, kas sastāv no atsevišķiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="234f9-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="234f9-123">Katrā apstiprināšanas solī lietotājs var veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="234f9-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="234f9-124">Apstiprināt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="234f9-124">Approve the document.</span></span>
- <span data-ttu-id="234f9-125">Noraidīt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="234f9-125">Reject the document.</span></span>
- <span data-ttu-id="234f9-126">Pieprasīt dokumenta izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="234f9-126">Request a change to the document.</span></span>
- <span data-ttu-id="234f9-127">Piešķirt dokumentu apstiprināšanai citam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="234f9-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="234f9-128">Dokumenta rindas darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="234f9-128">Line-item workflow elements</span></span>

<span data-ttu-id="234f9-129">Var izveidot darbplūsmu dokumentu vai dokumenta rindu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="234f9-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="234f9-130">Pieņemsim, ka esat izveidojis darba laika uzskaites tabulas apstiprinājuma darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="234f9-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="234f9-131">(Šī darbplūsma tiks saukta par *dokumenta darbplūsmu*.) Varat pievienot šai dokumenta darbplūsmai *rindas vienuma darbplūsmas* elementu.</span><span class="sxs-lookup"><span data-stu-id="234f9-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="234f9-132">Izpildot rindas vienuma elementu, apstrādei tiek nodots katras dokumenta rindas vienums.</span><span class="sxs-lookup"><span data-stu-id="234f9-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="234f9-133">Iespējams, vēlaties, lai visu rindu vienumu apstrādei tiktu izmantota viena dokumenta rindu darbplūsma, vai arī, iespējams, vēlaties, lai katra rindas vienuma apstrādei tiktu izmantota atšķirīga dokumenta rindas darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="234f9-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="234f9-134">Iedomājieties, ka darbinieks ir iesniedzis darba laika uzskaites tabulu, kas līdzinās tālāk esošajā attēlā redzamajai.</span><span class="sxs-lookup"><span data-stu-id="234f9-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Darbplūsma ar rindas elementiem](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="234f9-136">Šādā scenārijā, iespējams, vēlaties izveidot tālāk norādītās dokumenta rindas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="234f9-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="234f9-137">**1. dokumenta rindas darbplūsma** — šī darbplūsma tiek izmantota to rindas vienumu apstrādei, kuru projekta ID ir 1111.</span><span class="sxs-lookup"><span data-stu-id="234f9-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="234f9-138">**2. dokumenta rindas darbplūsma** — šī darbplūsma tiek izmantota to rindas vienumu apstrādei, kuru projekta ID ir 2222.</span><span class="sxs-lookup"><span data-stu-id="234f9-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="234f9-139">**3. dokumenta rindas darbplūsma** — šī darbplūsma tiek izmantota to rindas vienumu apstrādei, kuru projekta ID ir 3333.</span><span class="sxs-lookup"><span data-stu-id="234f9-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="234f9-140">Plūsmas kontroles elementi</span><span class="sxs-lookup"><span data-stu-id="234f9-140">Flow-control elements</span></span>

<span data-ttu-id="234f9-141">Tālāk norādītie elementi ļauj izveidot darbplūsmas ar alternatīviem atzariem vai atzariem, kas tiek izpildītie vienlaikus.</span><span class="sxs-lookup"><span data-stu-id="234f9-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="234f9-142">Manuāls lēmums</span><span class="sxs-lookup"><span data-stu-id="234f9-142">Manual decision</span></span>

<span data-ttu-id="234f9-143">*Manuāls lēmums* ir punkts, kur darbplūsma sadalās divos atzaros.</span><span class="sxs-lookup"><span data-stu-id="234f9-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="234f9-144">Lietotājam ir jāpieņem lēmums, un šis lēmums nosaka, kurš atzars tiek izmantots iesniegtā dokumenta apstrādei.</span><span class="sxs-lookup"><span data-stu-id="234f9-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="234f9-145">Nosacījuma lēmums</span><span class="sxs-lookup"><span data-stu-id="234f9-145">Conditional decision</span></span>

<span data-ttu-id="234f9-146">*Nosacījuma lēmums* arī ir punkts, kur darbplūsma sadalās divos atzaros.</span><span class="sxs-lookup"><span data-stu-id="234f9-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="234f9-147">Taču to, kurš atzars ir jāizmanto iesniegtā dokumenta apstrādei, izvēlas sistēma.</span><span class="sxs-lookup"><span data-stu-id="234f9-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="234f9-148">Lai pieņemtu šo lēmumu, sistēma novērtē dokumentu un nosaka, vai tas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="234f9-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="234f9-149">Paralēla aktivitāte</span><span class="sxs-lookup"><span data-stu-id="234f9-149">Parallel activity</span></span>

<span data-ttu-id="234f9-150">*Paralēla aktivitāte* ir darbplūsmas elements, kas satur divus vai vairāk darbplūsmas atzaru, kas tiek izpildīti vienlaikus.</span><span class="sxs-lookup"><span data-stu-id="234f9-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="234f9-151">Pakārtotā darbplūsma</span><span class="sxs-lookup"><span data-stu-id="234f9-151">Subworkflow</span></span>

<span data-ttu-id="234f9-152">*Pakārtotā darbplūsma* ir darbplūsma, kas darbojas citas darbplūsmas kontekstā.</span><span class="sxs-lookup"><span data-stu-id="234f9-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
