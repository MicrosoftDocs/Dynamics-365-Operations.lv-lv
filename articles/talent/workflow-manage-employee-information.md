---
title: "Darbplūsmu izmantošana darbinieku informācijas pārvaldībai"
description: "Šajā tēmā ir aprakstīts, kā varat izmanto personāla vadības darbplūsmu iespējas, lai pārvaldītu darbinieku informāciju. Piemēram, varat saistīt darbplūsmu ar pozīciju un konfigurēt apstiprināšanas darbplūsmu, kas tiek sākta, kad darbinieki maina savu ierakstu."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47c569f3531bf00795078b7b042bf899b51bad8d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="000ae-104">Darbplūsmu izmantošana darbinieku informācijas pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="000ae-104">Use workflows to manage employee information</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="000ae-105">Šajā tēmā ir aprakstīts, kā varat izmanto personāla vadības darbplūsmu iespējas, lai pārvaldītu darbinieku informāciju.</span><span class="sxs-lookup"><span data-stu-id="000ae-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="000ae-106">Piemēram, varat saistīt darbplūsmu ar pozīciju un konfigurēt apstiprināšanas darbplūsmu, kas tiek sākta, kad darbinieki maina savu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="000ae-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="000ae-107">Personāla vadības darbplūsmu iespējas nodrošina vairākas darbplūsmas personāla vadības darbību pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="000ae-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="000ae-108">Turklāt ir pieejamas vairākas opcijas, kas sniedz iespēju modificēt noteiktas darbplūsmas un saistīt tās ar padotības hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="000ae-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="000ae-109">Ir pieejamas darbplūsmas, kas palīdz pārvaldīt dažādu standarta darbinieku informācijas veidu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="000ae-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="000ae-110">Varat saistīt darbplūsmu ar pozīciju.</span><span class="sxs-lookup"><span data-stu-id="000ae-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="000ae-111">Šādā gadījumā, ja darbinieki maina savu darbinieka ierakstu, tiek sākta darbplūsma, kas pieprasa apstiprināšanu pirms jaunās informācijas saglabāšanas.</span><span class="sxs-lookup"><span data-stu-id="000ae-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="000ae-112">Ir pieejamas iepriekš definētas tālāk norādītās informācijas darbplūsmas, kas palīdz efektīvi pārvaldīt izmaiņas un uzturēt darbinieku datus pareizus.</span><span class="sxs-lookup"><span data-stu-id="000ae-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="000ae-113">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="000ae-113">Identification numbers</span></span>
-   <span data-ttu-id="000ae-114">Kursi</span><span class="sxs-lookup"><span data-stu-id="000ae-114">Courses</span></span>
-   <span data-ttu-id="000ae-115">Izglītība</span><span class="sxs-lookup"><span data-stu-id="000ae-115">Education</span></span>
-   <span data-ttu-id="000ae-116">Attēls</span><span class="sxs-lookup"><span data-stu-id="000ae-116">Image</span></span>
-   <span data-ttu-id="000ae-117">Patapinātie krājumi</span><span class="sxs-lookup"><span data-stu-id="000ae-117">Loaned items</span></span>
-   <span data-ttu-id="000ae-118">Profesionālā pieredze</span><span class="sxs-lookup"><span data-stu-id="000ae-118">Professional experience</span></span>
-   <span data-ttu-id="000ae-119">Projektu pieredze</span><span class="sxs-lookup"><span data-stu-id="000ae-119">Project experience</span></span>
-   <span data-ttu-id="000ae-120">Prasmes</span><span class="sxs-lookup"><span data-stu-id="000ae-120">Skills</span></span>
-   <span data-ttu-id="000ae-121">Atbildīgie amati</span><span class="sxs-lookup"><span data-stu-id="000ae-121">Positions of trust</span></span>
-   <span data-ttu-id="000ae-122">Personāla vadības darbības</span><span class="sxs-lookup"><span data-stu-id="000ae-122">Human resources actions</span></span>
-   <span data-ttu-id="000ae-123">Kursu reģistrācija</span><span class="sxs-lookup"><span data-stu-id="000ae-123">Course registration</span></span>

<span data-ttu-id="000ae-124">Kad darbinieki tiek pieņemti darbā, pārcelti citā amatā vai ar viņiem tiek pārtrauktas darba attiecības, darbplūsma var tikt ietverts pārskatīšanas process.</span><span class="sxs-lookup"><span data-stu-id="000ae-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="000ae-125">Tādējādi darbplūsmas ietvaros var tikt pārskatīts dokuments vai darbības nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="000ae-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="000ae-126">Kad pārskatīšanas process ir pabeigts, dokuments vai darbība tiek pabeigta un darbplūsma pāriet pie galīgās apstiprināšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="000ae-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="000ae-127">Darbplūsmas saistīšana ar padotības hierarhiju</span><span class="sxs-lookup"><span data-stu-id="000ae-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="000ae-128">Varat saistīt darbplūsmu ar jebkuru konfigurēto hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="000ae-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="000ae-129">Piemēram, ja pozīcija ir saistīta ar matricas padotības hierarhiju, varat konfigurēt darbplūsmu, kas nodrošina noteikta projekta izmaksu novirzīšanu projekta vadītajam, nevis tā darbinieka vadītājam, kurš ir saistīts ar šo pozīciju.</span><span class="sxs-lookup"><span data-stu-id="000ae-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="000ae-130">Lai izveidotu jaunu darbplūsmu vai modificētu esošu darbplūsmu, lapā **Personāla vadības darbplūsmas** noklikšķiniet uz **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="000ae-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="000ae-131">Sarakstā atlasiet darbplūsmu, lai palaistu darbplūsmu noformētāju.</span><span class="sxs-lookup"><span data-stu-id="000ae-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="000ae-132">Varat izmantot noformētāju, lai izveidotu jaunu darbplūsmu vai mainītu esošas darbplūsmas darbības.</span><span class="sxs-lookup"><span data-stu-id="000ae-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="000ae-133">Ja maināt esošu darbplūsmu, izmaiņas tiek saglabātas kā jauna versija.</span><span class="sxs-lookup"><span data-stu-id="000ae-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="000ae-134">Tāpēc vienmēr varat atgriezieties pie iepriekšējās versijas, ja tas ir nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="000ae-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="000ae-135">Personāla vadības darbības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="000ae-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="000ae-136">Lai konfigurētu pamata darbplūsmu, kas tiek sākta, kad darbinieks pieprasa savas personiskās informācijas izmaiņas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="000ae-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="000ae-137">Lapā **Personāla vadības darbplūsmas** noklikšķiniet uz **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="000ae-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="000ae-138">Pieejamo darbplūsmu sarakstā atlasiet vienumu **Identifikācijas numuri**.</span><span class="sxs-lookup"><span data-stu-id="000ae-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="000ae-139">Noklikšķiniet uz **Palaist**, lai palaistu darbplūsmu noformētāju, un pēc tam ievadiet savu lietotājvārdu un paroli, kad tiek parādīta attiecīga uzvedne.</span><span class="sxs-lookup"><span data-stu-id="000ae-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="000ae-140">Velciet elementu **Apstiprināt identifikācijas numuru** no darbplūsmas elementu saraksta uz noformētāja rāmi.</span><span class="sxs-lookup"><span data-stu-id="000ae-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="000ae-141">Savienojiet apstiprināšanas elementu ar elementiem **Sākt** un **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="000ae-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="000ae-142">Veiciet dubultklikšķi uz **Apstiprināt elementu**, noklikšķiniet ar peles labo pogu un atlasiet vienumu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="000ae-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="000ae-143">Veiciet tālāk norādītās darbības, lai pievienotu darbplūsmas elementa instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="000ae-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="000ae-144">Atlasiet vienumu **Piešķire** un pēc tam piešķires veida sadaļā atlasiet vienumu **Hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="000ae-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="000ae-145">Sadaļā **Hierarhija** atlasiet vienumu **Konfigurējama hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="000ae-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="000ae-146">Pievienojiet apturēšanas nosacījumu un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="000ae-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="000ae-147">Izpildiet visas papildu instrukcijas (nedrīkst būt neviens papildu brīdinājums).</span><span class="sxs-lookup"><span data-stu-id="000ae-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="000ae-148">Noklikšķiniet uz **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="000ae-148">Click **Save and close**.</span></span> <span data-ttu-id="000ae-149">Kad tiek atvērts dialoglodziņš, aktivizējiet jauno darbplūsmu un atlasiet vienumu **Padarīt aktīvu**.</span><span class="sxs-lookup"><span data-stu-id="000ae-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="000ae-150">Pārejiet uz sadaļu **Personāla vadība** &gt; **Pozīcijas** &gt; **Pozīciju hierarhijas tipi**.</span><span class="sxs-lookup"><span data-stu-id="000ae-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="000ae-151">Atlasiet vienumu **Matrica**.</span><span class="sxs-lookup"><span data-stu-id="000ae-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="000ae-152">Pievienojiet sarakstam darbplūsmu **Nodarbinātā identifikācijas numurs**.</span><span class="sxs-lookup"><span data-stu-id="000ae-152">Add the **Worker identification number** workflow to the list.</span></span>





