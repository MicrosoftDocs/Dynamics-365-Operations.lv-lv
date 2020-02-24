---
title: Savienojuma izveide ar palīdzības sistēmu
description: Šajā tēmā ir aprakstīti palīdzības sistēmas komponenti Finance and Operations programmām, kā arī sniegts apskats par savienojumu izveidi ar tiem un kopsavilkums par pielāgota palīdzības satura izveidi.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006176"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="efcf0-103">Savienojuma izveide ar palīdzības sistēmu</span><span class="sxs-lookup"><span data-stu-id="efcf0-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efcf0-104">Šajā tēmā ir aprakstīti palīdzības sistēmas komponenti Finance and Operations programmām, piemēram Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span><span class="sxs-lookup"><span data-stu-id="efcf0-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="efcf0-105">Tajā ir sniegts pārskats par to, kā izveidot savienojumu ar šiem komponentiem, kā arī kopsavilkums par to, kā izveidot pielāgotus palīdzības materiālus.</span><span class="sxs-lookup"><span data-stu-id="efcf0-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="efcf0-106">Palīdzības arhitektūra</span><span class="sxs-lookup"><span data-stu-id="efcf0-106">Help architecture</span></span>

<span data-ttu-id="efcf0-107">Nākamajā attēlā ir parādītas daļas no palīdzības sistēmas.</span><span class="sxs-lookup"><span data-stu-id="efcf0-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="efcf0-108">Produktā iebūvētā palīdzības sistēma izgūst rakstus no https://docs.microsoft.com, kā arī uzdevumu ceļvežus no Biznesa procesu modelētāja pakalpojumos Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="efcf0-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="efcf0-109">Līdzekļi, kas diagrammā ir atzīmēti ar zvaigznīti (\*), ir plānoti, taču vēl nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="efcf0-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="efcf0-110">[![Palīdzības sistēmas arhitektūra](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="efcf0-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="efcf0-111">Savienojuma izveide ar palīdzības sistēmu</span><span class="sxs-lookup"><span data-stu-id="efcf0-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="efcf0-112">Cilne **Uzdevumu ceļveži** pašlaik nav pieejama Dynamics 365 Human Resources vai Commerce.</span><span class="sxs-lookup"><span data-stu-id="efcf0-112">The **Task guides** tab is currently not available in Dynamics 365 Human Resources or Commerce.</span></span> <span data-ttu-id="efcf0-113">Mēs pašlaik strādājam pie tā, šo funkcionalitāti iespējotu nākamajos laidienos.</span><span class="sxs-lookup"><span data-stu-id="efcf0-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="efcf0-114">Uzdevumu ceļveži versijas  Human Resources funkcionalitātē Darba sākšana joprojām ir pieejami pamata funkcionalitātes segšanai.</span><span class="sxs-lookup"><span data-stu-id="efcf0-114">The Task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="efcf0-115">Procesuālā palīdzība ir pieejama arī vietnē docs.microsoft.com gan Human Resources, gan Commerce programmām.</span><span class="sxs-lookup"><span data-stu-id="efcf0-115">Procedural help is also available on the docs.microsoft.com site for both Human Resources and Commerce.</span></span>

<span data-ttu-id="efcf0-116">Izmantojot lapu **Sistēmas parametri**, sistēmas administratori izveido savienojumu ar palīdzības sistēmas daļām implementācijas nolūkā.</span><span class="sxs-lookup"><span data-stu-id="efcf0-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="efcf0-117">[![Veidlapa Sistēmas parametri, kurā ir atvērti palīdzības iestatījumi](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="efcf0-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="efcf0-118">Lapā **Sistēmas parametri** izpildiet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="efcf0-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efcf0-119">Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="efcf0-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="efcf0-120">Noteikti noklikšķiniet uz saites formas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz **Labi**, lai piekļūtu lapai **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="efcf0-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="efcf0-121">[![Izveidot savienojumu ar LCS](./media/connect-to-lcs-crop-1024x365.png "Izveidot savienojumu ar LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="efcf0-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="efcf0-122">Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.</span><span class="sxs-lookup"><span data-stu-id="efcf0-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="efcf0-123">Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="efcf0-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="efcf0-124">Iestatiet BPM bibliotēku attēlošanas secību.</span><span class="sxs-lookup"><span data-stu-id="efcf0-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="efcf0-125">Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="efcf0-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="efcf0-126">Kad esat izpildījis šīs darbības, varat atvērt rūti **Palīdzība** un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz  Finance and Operations programmās pašlaik atvērto lapu.</span><span class="sxs-lookup"><span data-stu-id="efcf0-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="efcf0-127">Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.</span><span class="sxs-lookup"><span data-stu-id="efcf0-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="efcf0-128">Tulkotu uzdevumu ceļvežu parādīšana</span><span class="sxs-lookup"><span data-stu-id="efcf0-128">Showing translated task guides</span></span>

<span data-ttu-id="efcf0-129">Tulkotie uzdevumu ceļveži pirmo reizi tika nodrošināti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="efcf0-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="efcf0-130">Lai redzētu lokalizēto uzdevumu ceļvežu palīdzību programmatūrā Finance and Operations, pārliecinieties, ka ir izveidots savienojums ar maija bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="efcf0-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="efcf0-131">Uzdevuma ceļveža rādīšanas valodu katram lietotājam var norādīt, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**.</span><span class="sxs-lookup"><span data-stu-id="efcf0-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="efcf0-132">Lai gan daudzi uzdevumu ceļveži ir iztulkoti, pašlaik klients nerāda tulkoto uzdevumu ceļvežu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="efcf0-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="efcf0-133">Turklāt maijā izlaistajā bibliotēkā tulkotā veidā ir pieejami tikai tie uzdevumu ceļveži, kas tika izlaisti 2016. gada februārī.</span><span class="sxs-lookup"><span data-stu-id="efcf0-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="efcf0-134">Mēs izdosim atjauninātu bibliotēku ar papildu tulkojumiem.</span><span class="sxs-lookup"><span data-stu-id="efcf0-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="efcf0-135">Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.</span><span class="sxs-lookup"><span data-stu-id="efcf0-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="efcf0-136">Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).</span><span class="sxs-lookup"><span data-stu-id="efcf0-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="efcf0-137">Pielāgotas palīdzības veidošana</span><span class="sxs-lookup"><span data-stu-id="efcf0-137">Creating custom help</span></span>

<span data-ttu-id="efcf0-138">Var lietot uzd. ceļv., lai izveidotu piel. palīdz. vai savienotu vietni ar rūti Pal.</span><span class="sxs-lookup"><span data-stu-id="efcf0-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="efcf0-139">Pielāg. pal. izveide ar uzd. ceļv.</span><span class="sxs-lookup"><span data-stu-id="efcf0-139">Create custom help with task guides</span></span>

<span data-ttu-id="efcf0-140">Savai programmatūrai Finance, Supply Chain Management un Commerce varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tos saglabājot LCS biznesa procesu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="efcf0-140">You can create custom help for Finance, Supply Chain Management, and Commerce by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="efcf0-141">Personāla vadībai nav iespējams izveidot pielāgotus uzdevumu ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="efcf0-141">You cannot create custom task guides for Human Resources.</span></span>

<span data-ttu-id="efcf0-142">Partneriem — ja bibliotēku paaugstināt uz korporatīvu bibliotēku, un iekļaut to kādā risinājumā, tā būs pieejama jūsu klientiem.</span><span class="sxs-lookup"><span data-stu-id="efcf0-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="efcf0-143">Varat arī izveidot APQC vienotās globālās bibliotēkas kopiju, pēc tam atvērt savu kopiju, no tās atvērt uzdevumu ierakstus, modificēt tos un saglabāt ierakstus ar savām veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="efcf0-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="efcf0-144">Papildinformāciju skatiet tēmā [Uzdevuma reģistrētāja resursi](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="efcf0-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="efcf0-145">Sav. ar piel. vietni</span><span class="sxs-lookup"><span data-stu-id="efcf0-145">Connect a custom site</span></span>

<span data-ttu-id="efcf0-146">Microsoft ir sniedzis tehn. dokum. un parauga kodu, kas apraksta, kā veidot un savienot pielāg. palīdz. vietni ar rūti Palīdzība.</span><span class="sxs-lookup"><span data-stu-id="efcf0-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="efcf0-147">Plašāku informāciju skatiet:</span><span class="sxs-lookup"><span data-stu-id="efcf0-147">For more information, see:</span></span>

- [<span data-ttu-id="efcf0-148">Izveidot Pielāgotu palīdzību programmatūrai Finance and Operations (tehniskais dokuments)</span><span class="sxs-lookup"><span data-stu-id="efcf0-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="efcf0-149">Pielāg. palīdz. GitHub repoz.</span><span class="sxs-lookup"><span data-stu-id="efcf0-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="efcf0-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="efcf0-150">Additional resources</span></span>

[<span data-ttu-id="efcf0-151">Palīdzības sistēma</span><span class="sxs-lookup"><span data-stu-id="efcf0-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="efcf0-152">Uzdevuma reģistrētāja resursi</span><span class="sxs-lookup"><span data-stu-id="efcf0-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="efcf0-153">Dokumentācijas vai apmācības izveide, izmantojot uzdevuma reģistrētāju</span><span class="sxs-lookup"><span data-stu-id="efcf0-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
