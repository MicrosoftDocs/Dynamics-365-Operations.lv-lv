---
title: Patēriņa reģistrēšana
description: Šajā tēmā ir aprakstīts, kā reģistrēt patēriņu Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c59664346c07f5e74825de41870f6635ced24ebd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216325"
---
# <a name="register-consumption"></a><span data-ttu-id="f5aa9-103">Patēriņa reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="f5aa9-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f5aa9-104">Kad uzturēšanas darbs ir pabeigts darba pasūtījumā, nākamā darbība ir izveidot patēriņa reģistrācijas un grāmatot žurnālus.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="f5aa9-105">Varat izveidot reģistrācijas tālāk norādītajos patēriņa veidos: stundas, krājumi un izdevumi.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="f5aa9-106">Dažādie patēriņa veidi tiek reģistrēti un grāmatoti lapā **Darba pasūtījuma žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="f5aa9-107">Žurnāla iestatījumi **Līdzekļu pārvaldībā** tiek izmantoti, lai izveidotu un grāmatotu atsevišķus žurnālus stundām, krājumiem un izdevumiem modulī **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="f5aa9-108">Dažos gadījumos, iespējams, jūs varat pievienot vai dzēst prognozes rindas darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f5aa9-109">Darba pasūtījuma dzīves cikla stāvokļa iestatījums, saistītais projekta tips un stadijas noteikumi, kas saistīti ar projekta tipu, nosaka, vai varat pievienot vai rediģēt žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="f5aa9-110">Lasiet vairāk informācijas par darba pasūtījumu dzīves cikla stāvokļiem un saistītiem projekta posmiem [Prognozes, darba pasūtījumi un projekti](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="f5aa9-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="f5aa9-111">Var iestatīt automātisku žurnālu grāmatošanu darba pasūtījuma dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="f5aa9-112">Vairāk informācijas skatiet sadaļā [Darba pasūtījuma dzīves cikla stāvokļi](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="f5aa9-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="f5aa9-113">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f5aa9-114">Atlasiet darba pasūtījumu un noklikšķiniet uz **Žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="f5aa9-115">Noklikšķiniet uz **Kopēt no prognozes**, lai pārsūtītu jebkuras prognozes rindas, kas var būt saistītas ar darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="f5aa9-116">Varat atlasīt, kurus patēriņa veidus vēlaties pārsūtīt.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="f5aa9-117">Ja nepieciešams, varat pievienot papildu patēriņa rindas attiecīgajā kopsavilkuma cilnē, noklikšķinot uz **Pievienot rindu** un aizpildot rindas datus.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="f5aa9-118">Noklikšķiniet uz **Validēt žurnālus**, lai validētu žurnāla rindas pirms grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="f5aa9-119">Noklikšķiniet uz **Grāmatot žurnālus**, lai grāmatotu žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="f5aa9-120">Pēc patēriņa žurnālu grāmatošanas varat atjaunināt darba pasūtījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="f5aa9-121">Piemēram, lai norādītu, ka darba pasūtījums ir pabeigts, varat atjaunināt dzīves cikla stāvokli uz "Pabeigts".</span><span class="sxs-lookup"><span data-stu-id="f5aa9-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="f5aa9-122">Laukā **Rādīt**, kas atrodas lapas **Darba pasūtījuma žurnāli** augšdaļā, atlasiet, kuras žurnāla rindas vēlaties skatīt: **Visas**, **Negrāmatotās** vai **Grāmatotās**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="f5aa9-123">Grāmatotajiem žurnāliem ir atzīme izvēles rūtī **Grāmatotas**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="f5aa9-124">Kad krājumu rindas ir veidotas darba pasūtījumu žurnālā, preču dimensijas un izsekošanas dimensijas, kas saistītas ar krājumu, tiek automātiski pārsūtītas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="f5aa9-125">Tālāk redzamajā ekrānuzņēmumā ir parādīts stundas vai krājuma reģistrācijas piemērs darba pasūtījumā **Darba pasūtījuma žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![1. attēls](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="f5aa9-127">Stundu sadalīšana darba pasūtījumos ar vairākiem darbu pasūtījuma uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="f5aa9-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="f5aa9-128">Ja darba pasūtījumā ir vairāki darba pasūtījuma uzdevumi, varat reģistrēt darba stundas, izmantojot funkciju **Sadalīt stundas**, t. i., vienas stundas reģistrācijas rinda var tikt vienmērīgi sadalīta katrā darba pasūtījuma uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="f5aa9-129">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f5aa9-130">Atlasiet darba pasūtījumu un noklikšķiniet uz **Žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f5aa9-131">Atlasiet stundu reģistrācijas rindu, kuru vēlaties sadalīt, un noklikšķiniet uz **Sadalīt stundas**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="f5aa9-132">Dialoglodziņā **Sadalīt stundas darba pasūtījuma uzturēšanas darbiem** laukā **Nodarbinātais** automātiski tiek parādīt tā darbinieka vārds, kas ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="f5aa9-133">Ja nepieciešams, varat atlasīt citu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="f5aa9-134">Atlasiet kategoriju stundu reģistrācijai laukā **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="f5aa9-135">Ievadiet darba stundu skaitu, kas jāsadala, laukā **Stundas**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![2. attēls](media/02-consumption.png)

7. <span data-ttu-id="f5aa9-137">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-137">Click **OK**.</span></span>

<span data-ttu-id="f5aa9-138">*Piemērs:* tālāk redzamajā ekrānuzņēmumā ir parādītas žurnāla rindas darba pasūtījumam, kas ietver trīs darba pasūtījuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="f5aa9-139">Pirmā rinda, kas ietver trīs darba stundas, ir sadalīta, un viena darba stunda tiek reģistrēta katram darba pasūtījuma uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="f5aa9-140">Pēc tam, kad ir izveidotas trīs stundu reģistrācijas rindas, varat izlemt, ko darīt ar sākotnējo stundu reģistrācijas rindu (piemērā norādīta kā pirmā rinda).</span><span class="sxs-lookup"><span data-stu-id="f5aa9-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="f5aa9-141">Varat to atstāt tādu, kāda tā ir, vai dzēst.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-141">You can keep it as is or delete it.</span></span> 

![3. attēls](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="f5aa9-143">Finanšu dimensijas patēriņa reģistrācijās</span><span class="sxs-lookup"><span data-stu-id="f5aa9-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="f5aa9-144">Veicot patēriņa reģistrācijas, noteiktā secībā reģistrācijām tiek pievienotas ar dažādiem reģistrācijas tipiem saistītās finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="f5aa9-145">*Stundu un izdevumu reģistrācijas:* vispirms tiek pievienotas finanšu dimensijas no žurnāla virsraksta, ja tādas ir.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f5aa9-146">Pēc tam tiek pievienotas finanšu dimensijas no saistītā darba pasūtījuma projekta.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f5aa9-147">Visbeidzot, tiek pievienotas finanšu dimensijas no resursa (nodarbinātā).</span><span class="sxs-lookup"><span data-stu-id="f5aa9-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="f5aa9-148">*Krājumu reģistrācijas:* vispirms tiek pievienotas finanšu dimensijas no žurnāla virsraksta, ja tādas ir.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f5aa9-149">Pēc tam tiek pievienotas finanšu dimensijas no saistītā darba pasūtījuma projekta.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f5aa9-150">Pēc tam tiek pievienotas finanšu dimensijas no vietas.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="f5aa9-151">Visbeidzot, tiek pievienotas finanšu dimensijas no krājuma.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="f5aa9-152">Visiem trim reģistrācijas tipiem tiek validēta finanšu dimensiju kombinācija, un nederīgas kombinācijas tiek atstatas tukšas.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="f5aa9-153">Šis ir standarta iestatījums ar citām Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="f5aa9-153">This is standard setup with other Finance and Operations apps.</span></span>

