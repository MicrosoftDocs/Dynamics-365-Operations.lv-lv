---
title: "Savienojuma izveide ar palīdzības sistēmu"
description: "Šajā tēmā ir aprakstīti programmatūrai Microsoft Dynamics 365 for Finance and Operations paredzētās palīdzības sistēmas komponenti, sniegts apskats par to, kā tos savienot, un kopsavilkums par to, kā izveidot pielāgotu palīdzību."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: a27b21ffcde9bfbb7e6276ef35b2e48bd23af70d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="a9b47-103">Savienojuma izveide ar palīdzības sistēmu</span><span class="sxs-lookup"><span data-stu-id="a9b47-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a9b47-104">Šajā tēmā ir aprakstīti Microsoft Dynamics 365 for Finance and Operations palīdzības sistēmas komponenti.</span><span class="sxs-lookup"><span data-stu-id="a9b47-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a9b47-105">Tajā ir sniegts pārskats par to, kā izveidot savienojumu ar šiem komponentiem, kā arī kopsavilkums par to, kā izveidot pielāgotus palīdzības materiālus.</span><span class="sxs-lookup"><span data-stu-id="a9b47-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="a9b47-106">Palīdzības arhitektūra</span><span class="sxs-lookup"><span data-stu-id="a9b47-106">Help architecture</span></span>
<span data-ttu-id="a9b47-107">Nākamajā attēlā ir redzamas Finance and Operations palīdzības sistēmas daļas.</span><span class="sxs-lookup"><span data-stu-id="a9b47-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="a9b47-108">Produktā iebūvētā palīdzības sistēma izgūst rakstus no Finance and Operations vietnes (https://docs.microsoft.com), kā arī uzdevumu ceļvežus no biznesa procesu modelētāja pakalpojumos Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a9b47-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="a9b47-109">Līdzekļi, kas diagrammā ir atzīmēti ar zvaigznīti (\*), ir plānoti, taču vēl nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="a9b47-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="a9b47-110">[![Palīdzības sistēmas arhitektūra](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="a9b47-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="a9b47-111">Savienojuma izveide ar palīdzības sistēmu</span><span class="sxs-lookup"><span data-stu-id="a9b47-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="a9b47-112">Cilne **Uzdevumu ceļveži** pašlaik nav pieejama versijā Microsoft Dynamics 365 for Talent un Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a9b47-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="a9b47-113">Mēs pašlaik strādājam pie tā, šo funkcionalitāti iespējotu nākamajos laidienos.</span><span class="sxs-lookup"><span data-stu-id="a9b47-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="a9b47-114">Uzdevumu ceļveži versijas Talent funkcionalitātē Darba sākšana joprojām ir pieejami pamata funkcionalitātes segšanai.</span><span class="sxs-lookup"><span data-stu-id="a9b47-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="a9b47-115">Palīdzība saistībā ar procedūrām ir pieejama arī vietnē docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) gan versijai Retail, gan versijai Talent.</span><span class="sxs-lookup"><span data-stu-id="a9b47-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="a9b47-116">Izmantojot lapu **Sistēmas parametri**, sistēmas administratori izveido savienojumu ar palīdzības sistēmas daļām implementācijas nolūkā.</span><span class="sxs-lookup"><span data-stu-id="a9b47-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="a9b47-117">[![Veidlapa Sistēmas parametri ar palīdzības sistēmas iestatījumiem](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Lapā **Sistēmas parametri** veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a9b47-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9b47-118">Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="a9b47-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="a9b47-119">Noteikti noklikšķiniet uz saites veidlapas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz **Labi**, lai piekļūtu lapai **Sistēmas parametri**.[![Savienojuma izveide ar LCS](./media/connect-to-lcs-crop-1024x365.png "Savienojuma izveide ar LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="a9b47-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="a9b47-120">Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.</span><span class="sxs-lookup"><span data-stu-id="a9b47-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="a9b47-121">Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a9b47-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="a9b47-122">Saistībā ar programmatūru Finance and Operations un Microsoft saturu atlasiet visjaunāko APQC vienoto bibliotēku programmatūrai Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9b47-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="a9b47-123">Versijai Retail mēs bibliotēku izlaidīsim tuvākajā laikā.</span><span class="sxs-lookup"><span data-stu-id="a9b47-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="a9b47-124">Nav nepieciešams atlasīt bibliotēku versijai Talent — savienojums ar pareizo bibliotēku jums ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="a9b47-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="a9b47-125">Iestatiet BPM bibliotēku attēlošanas secību.</span><span class="sxs-lookup"><span data-stu-id="a9b47-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="a9b47-126">Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="a9b47-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="a9b47-127">Kad esat izpildījis šīs darbības, varat atvērt rūti **Palīdzība** un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz programmatūrā Finance and Operations pašlaik atvērto lapu.</span><span class="sxs-lookup"><span data-stu-id="a9b47-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="a9b47-128">Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.</span><span class="sxs-lookup"><span data-stu-id="a9b47-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="a9b47-129">Tulkotu uzdevumu ceļvežu parādīšana</span><span class="sxs-lookup"><span data-stu-id="a9b47-129">Showing translated task guides</span></span>

<span data-ttu-id="a9b47-130">Tulkotie uzdevumu ceļveži pirmo reizi tika nodrošināti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="a9b47-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="a9b47-131">Lai redzētu lokalizēto uzdevumu ceļvežu palīdzību programmatūrā Finance and Operations, pārliecinieties, ka ir izveidots savienojums ar maija bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="a9b47-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="a9b47-132">Uzdevuma ceļveža rādīšanas valodu katram lietotājam var norādīt, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**.</span><span class="sxs-lookup"><span data-stu-id="a9b47-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a9b47-133">Lai gan daudzi uzdevumu ceļveži ir iztulkoti, pašlaik Finance and Operations klients nerāda tulkoto uzdevumu ceļvežu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="a9b47-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="a9b47-134">Turklāt maijā izlaistajā bibliotēkā tulkotā veidā ir pieejami tikai tie uzdevumu ceļveži, kas tika izlaisti 2016. gada februārī.</span><span class="sxs-lookup"><span data-stu-id="a9b47-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="a9b47-135">Mēs izdosim atjauninātu bibliotēku ar papildu tulkojumiem.</span><span class="sxs-lookup"><span data-stu-id="a9b47-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="a9b47-136">Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.</span><span class="sxs-lookup"><span data-stu-id="a9b47-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="a9b47-137">Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).</span><span class="sxs-lookup"><span data-stu-id="a9b47-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="a9b47-138">Pielāgotas palīdzības veidošana</span><span class="sxs-lookup"><span data-stu-id="a9b47-138">Creating custom help</span></span>
<span data-ttu-id="a9b47-139">Savai programmatūrai Finance and Operations un Retail varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tos saglabājot LCS biznesa procesu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="a9b47-139">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="a9b47-140">Pielāgotus uzdevumu ceļvežus nevar izveidot programmatūrai Talent.</span><span class="sxs-lookup"><span data-stu-id="a9b47-140">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="a9b47-141">Partneriem — ja bibliotēku paaugstināt uz korporatīvu bibliotēku, un iekļaut to kādā risinājumā, tā būs pieejama jūsu klientiem.</span><span class="sxs-lookup"><span data-stu-id="a9b47-141">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="a9b47-142">Varat arī izveidot APQC vienotās globālās bibliotēkas kopiju, pēc tam atvērt savu kopiju, no tās atvērt uzdevumu ierakstus, modificēt tos un saglabāt ierakstus ar savām veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="a9b47-142">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="a9b47-143">Papildinformāciju skatiet tēmā [Kā izveidot uzdevuma ierakstu izmantošanai dokumentācijas vai apmācības nolūkā](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="a9b47-143">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="a9b47-144">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="a9b47-144">See also</span></span>
--------

[<span data-ttu-id="a9b47-145">Pārskats par palīdzības sistēmu</span><span class="sxs-lookup"><span data-stu-id="a9b47-145">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="a9b47-146">Pārskats par uzdevuma reģistrētāju</span><span class="sxs-lookup"><span data-stu-id="a9b47-146">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="a9b47-147">Kā izveidot uzdevuma ierakstu, ko lietot kā dokumentāciju vai apmācību</span><span class="sxs-lookup"><span data-stu-id="a9b47-147">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





