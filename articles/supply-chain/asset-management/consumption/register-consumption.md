---
title: Patēriņa reģistrēšana
description: Šajā tēmā ir aprakstīts, kā reģistrēt patēriņu Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913097"
---
# <a name="register-consumption"></a><span data-ttu-id="f62ca-103">Patēriņa reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="f62ca-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f62ca-104">Kad uzturēšanas darbs ir pabeigts darba pasūtījumā, nākamā darbība ir izveidot patēriņa reģistrācijas un grāmatot žurnālus.</span><span class="sxs-lookup"><span data-stu-id="f62ca-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="f62ca-105">Varat izveidot reģistrācijas tālāk norādītajos patēriņa veidos: stundas, krājumi un izdevumi.</span><span class="sxs-lookup"><span data-stu-id="f62ca-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="f62ca-106">Dažādie patēriņa veidi tiek reģistrēti un grāmatoti lapā **Darba pasūtījuma žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="f62ca-107">Žurnāla iestatījumi **Līdzekļu pārvaldībā** tiek izmantoti, lai izveidotu un grāmatotu atsevišķus žurnālus stundām, krājumiem un izdevumiem modulī **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="f62ca-108">Iespējams, jūs varat pievienot vai dzēst prognozes rindas darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="f62ca-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f62ca-109">Darba pasūtījuma dzīves cikla stāvokļa iestatījums, saistītais projekta tips un stadijas noteikumi, kas saistīti ar projekta tipu, nosaka, vai varat pievienot vai rediģēt žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="f62ca-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="f62ca-110">Uzziniet vairāk par darba pasūtījumu dzīves cikla stāvokļiem un saistītām projekta stadijām sadaļā [Integrācija projektu vadībā un uzskaitē](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="f62ca-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="f62ca-111">Var iestatīt automātisku žurnālu grāmatošanu darba pasūtījuma dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="f62ca-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="f62ca-112">Vairāk informācijas skatiet sadaļā [Darba pasūtījuma dzīves cikla stāvokļi](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="f62ca-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="f62ca-113">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f62ca-114">Atlasiet darba pasūtījumu un noklikšķiniet uz **Žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f62ca-115">Noklikšķiniet uz **Kopēt no prognozes**, lai pārsūtītu jebkuras prognozes rindas, kas var būt saistītas ar darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="f62ca-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="f62ca-116">Varat atlasīt, kurus patēriņa veidus vēlaties pārsūtīt.</span><span class="sxs-lookup"><span data-stu-id="f62ca-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="f62ca-117">Ja nepieciešams, varat pievienot papildu patēriņa rindas attiecīgajā kopsavilkuma cilnē, noklikšķinot uz **Pievienot rindu** un aizpildot rindas datus.</span><span class="sxs-lookup"><span data-stu-id="f62ca-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="f62ca-118">Noklikšķiniet uz **Validēt žurnālus**, lai validētu žurnāla rindas pirms grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="f62ca-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="f62ca-119">Noklikšķiniet uz **Grāmatot žurnālus**, lai grāmatotu žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="f62ca-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="f62ca-120">Kad esat grāmatojis patēriņa žurnālus, varat atjaunināt darba pasūtījuma dzīves cikla stāvokli, piemēram, uz “Pabeigts”, lai norādītu, ka darba pasūtījums ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="f62ca-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="f62ca-121">Laukā **Rādīt**, kas atrodas lapas **Darba pasūtījuma žurnāli** augšdaļā, atlasiet, kuras žurnāla rindas vēlaties skatīt: visas, negrāmatotās vai grāmatotās.</span><span class="sxs-lookup"><span data-stu-id="f62ca-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="f62ca-122">Grāmatotajiem žurnāliem ir atzīme izvēles rūtī **Grāmatotas**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="f62ca-123">Kad krājumu rindas ir veidotas darba pasūtījumu žurnālā, preču dimensijas un izsekošanas dimensijas, kas saistītas ar krājumu, tiek automātiski pārsūtītas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="f62ca-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="f62ca-124">Tālāk redzamajā ekrānuzņēmumā ir parādīts stundas vai krājuma reģistrācijas piemērs darba pasūtījumā **Darba pasūtījuma žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![1. attēls](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="f62ca-126">Stundu sadalīšana darba pasūtījumos ar vairākiem darbu pasūtījuma uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="f62ca-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="f62ca-127">Ja darba pasūtījumā ir vairāki darba pasūtījuma uzdevumi, varat reģistrēt darba stundas, izmantojot funkciju **Sadalīt stundas**, t. i., vienas stundas reģistrācijas rinda var tikt vienmērīgi sadalīta katrā darba pasūtījuma uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="f62ca-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="f62ca-128">Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f62ca-129">Atlasiet darba pasūtījumu un noklikšķiniet uz **Žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f62ca-130">Atlasiet stundu reģistrācijas rindu, kuru vēlaties sadalīt, un noklikšķiniet uz **Sadalīt stundas**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="f62ca-131">Dialoglodziņā **Sadalīt stundas darba pasūtījuma uzturēšanas darbiem** laukā **Nodarbinātais** automātiski tiek parādīt tā darbinieka vārds, kas ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="f62ca-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="f62ca-132">Ja nepieciešams, varat atlasīt citu darbinieku.</span><span class="sxs-lookup"><span data-stu-id="f62ca-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="f62ca-133">Atlasiet kategoriju stundu reģistrācijai laukā **Kategorija**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="f62ca-134">Ievadiet darba stundu skaitu, kas jāsadala, laukā **Stundas**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![2. attēls](media/02-consumption.png)

7. <span data-ttu-id="f62ca-136">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f62ca-136">Click **OK**.</span></span>

<span data-ttu-id="f62ca-137">*Piemērs:* tālāk redzamajā ekrānuzņēmumā ir parādītas žurnāla rindas darba pasūtījumam, kas ietver trīs darba pasūtījuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="f62ca-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="f62ca-138">Pirmā rinda, kas ietver trīs darba stundas, ir sadalīta, un viena darba stunda tiek reģistrēta katram darba pasūtījuma uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="f62ca-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="f62ca-139">Pēc tam, kad ir izveidotas trīs stundu reģistrācijas rindas, varat izlemt, ko darīt ar sākotnējo stundu reģistrācijas rindu (piemērā norādīta kā pirmā rinda).</span><span class="sxs-lookup"><span data-stu-id="f62ca-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="f62ca-140">Varat to atstāt tādu, kāda tā ir, vai dzēst.</span><span class="sxs-lookup"><span data-stu-id="f62ca-140">You can keep it as is or delete it.</span></span> 

![3. attēls](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="f62ca-142">Finanšu dimensijas patēriņa reģistrācijās</span><span class="sxs-lookup"><span data-stu-id="f62ca-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="f62ca-143">Veicot patēriņa reģistrācijas, noteiktā secībā reģistrācijām tiek pievienotas ar dažādiem reģistrācijas tipiem saistītās finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="f62ca-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="f62ca-144">*Stundu un izdevumu reģistrācijas:* vispirms tiek pievienotas finanšu dimensijas no žurnāla virsraksta, ja tādas ir.</span><span class="sxs-lookup"><span data-stu-id="f62ca-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f62ca-145">Pēc tam tiek pievienotas finanšu dimensijas no saistītā darba pasūtījuma projekta.</span><span class="sxs-lookup"><span data-stu-id="f62ca-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f62ca-146">Visbeidzot, tiek pievienotas finanšu dimensijas no resursa (nodarbinātā).</span><span class="sxs-lookup"><span data-stu-id="f62ca-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="f62ca-147">*Krājumu reģistrācijas:* vispirms tiek pievienotas finanšu dimensijas no žurnāla virsraksta, ja tādas ir.</span><span class="sxs-lookup"><span data-stu-id="f62ca-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f62ca-148">Pēc tam tiek pievienotas finanšu dimensijas no saistītā darba pasūtījuma projekta.</span><span class="sxs-lookup"><span data-stu-id="f62ca-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f62ca-149">Pēc tam tiek pievienotas finanšu dimensijas no vietas.</span><span class="sxs-lookup"><span data-stu-id="f62ca-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="f62ca-150">Visbeidzot, tiek pievienotas finanšu dimensijas no krājuma.</span><span class="sxs-lookup"><span data-stu-id="f62ca-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="f62ca-151">Visiem trim reģistrācijas tipiem tiek validēta finanšu dimensiju kombinācija, un nederīgas kombinācijas tiek atstatas tukšas.</span><span class="sxs-lookup"><span data-stu-id="f62ca-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="f62ca-152">Tas ir standarta iestatījums sistēmā Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f62ca-152">This is standard setup in Dynamics 365 for Finance and Operations.</span></span>

