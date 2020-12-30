---
title: Konfigurēt Palīdzības pieredzi Finance and Operations programmām
description: Šajā tēmā ir sniegta informācija par palīdzības sistēmas komponentiem dažām Microsoft Dynamics 365 programmām. Tas arī izskaidro, kā savienot šīs programmas un sniedz kopsavilkumu par procesu pielāgotas palīdzības izveidei.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0495bbc008ed1760b98c2c1ace63fc4a8b1ab5cc
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694425"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="514a6-104">Konfigurēt Palīdzības pieredzi Finance and Operations programmām</span><span class="sxs-lookup"><span data-stu-id="514a6-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="514a6-105">Šajā tēmā atradīsit pārskatu par programmas palīdzības sistēmas komponentiem Finance and Operations, piemēram, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce un Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="514a6-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="514a6-106">Šī tēma arī izskaidro, kā savienot šos komponentus, un sniedz kopsavilkumu par procesu pielāgotas palīdzības izveidei.</span><span class="sxs-lookup"><span data-stu-id="514a6-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="514a6-107">Palīdzības arhitektūra</span><span class="sxs-lookup"><span data-stu-id="514a6-107">Help architecture</span></span>

<span data-ttu-id="514a6-108">Finance and Operations programmas ietver konceptuālus apskatus un citas tēmas, kas publicētas [https://docs.microsoft.com/dynamics365](/dynamics365/) vietnē.</span><span class="sxs-lookup"><span data-stu-id="514a6-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="514a6-109">Šim saturam var piekļūt no preces **Palīdzības** rūts.</span><span class="sxs-lookup"><span data-stu-id="514a6-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="514a6-110">Nākamajā attēlā ir parādītas daļas no palīdzības sistēmas.</span><span class="sxs-lookup"><span data-stu-id="514a6-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="514a6-111">[![Palīdzības sistēmas arhitektūra](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="514a6-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="514a6-112">Preces palīdzības sistēma izvelk rakstus no docs.microsoft.com un citām saistītām vietnēm.</span><span class="sxs-lookup"><span data-stu-id="514a6-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="514a6-113">Tas arī velk uzdevumu ceļvežus, kas tiek uzglabāti Biznesa procesu modelētājā (BPM) Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="514a6-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="514a6-114">Uzdevumu ceļvežu pievienošana</span><span class="sxs-lookup"><span data-stu-id="514a6-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="514a6-115">Cilne **Uzdevumu ceļveži** pašlaik nav pieejami Personāla vadībā vai Commerce.</span><span class="sxs-lookup"><span data-stu-id="514a6-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="514a6-116">Tomēr uzdevumu ceļveži Darba sākšanas pieredzē Personāla vadībā ir pieejami pamata funkcionalitātes segšanai.</span><span class="sxs-lookup"><span data-stu-id="514a6-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="514a6-117">Procesuālā palīdzība ir pieejama arī vietnē [https://docs.microsoft.com/dynamics365](/dynamics365/) gan Personāla vadības, gan Commerce programmām.</span><span class="sxs-lookup"><span data-stu-id="514a6-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="514a6-118">Lapā **Sistēmas parametri** sistēmas administratori var konfigurēt piekļuvi attiecīgajām uzdevumu ceļveža bibliotēkām ieviešanai.</span><span class="sxs-lookup"><span data-stu-id="514a6-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="514a6-119">Lai konfigurētu palīdzību, jums ir jāpierakstās ar kontu tajā pašā nomniekā, kurā ir izvietota programma.</span><span class="sxs-lookup"><span data-stu-id="514a6-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="514a6-120">Savienojumu ar LCS bibliotēku nav iespējams izveidot no programmas instances, kas darbojas lokālā virtuālajā cietajā diskā (VHD).</span><span class="sxs-lookup"><span data-stu-id="514a6-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="514a6-121">[![Veidlapa Sistēmas parametri, kurā ir atvērti palīdzības iestatījumi](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="514a6-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="514a6-122">Lai konfigurētu risinājuma uzdevumu ceļvežus, veiciet šīs darbības lapā **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="514a6-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="514a6-123">Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="514a6-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="514a6-124">Noteikti atlasiet saiti formas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam atlasiet **Labi**, lai piekļūtu lapai **Sistēmas parametri**.</span><span class="sxs-lookup"><span data-stu-id="514a6-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="514a6-125">[![Izveidot savienojumu ar LCS](./media/connect-to-lcs-crop-1024x365.png "Izveidot savienojumu ar LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="514a6-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="514a6-126">Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.</span><span class="sxs-lookup"><span data-stu-id="514a6-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="514a6-127">Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="514a6-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="514a6-128">Iestatiet BPM bibliotēku attēlošanas secību.</span><span class="sxs-lookup"><span data-stu-id="514a6-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="514a6-129">Displejs nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="514a6-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="514a6-130">Kad esat izpildījis šīs darbības, varat atvērt rūti **Palīdzība** un atlasiet cilni **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz  Finance and Operations programmās pašlaik atvērto lapu.</span><span class="sxs-lookup"><span data-stu-id="514a6-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="514a6-131">Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.</span><span class="sxs-lookup"><span data-stu-id="514a6-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="514a6-132">Tulkotu uzdevumu ceļvežu parādīšana</span><span class="sxs-lookup"><span data-stu-id="514a6-132">Showing translated task guides</span></span>

<span data-ttu-id="514a6-133">Tulkotie uzdevumu ceļveži pirmo reizi tika izlaisti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="514a6-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="514a6-134">Lai redzētu lokalizēto uzdevumu ceļvežu palīdzību, pārliecinieties, ka jūsu Dynamics 365 risinājums ir savienots ar 2016. gada maija bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="514a6-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="514a6-135">Lietotāji var mainīt uzdevuma ceļveža rādīšanas valodu, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**.</span><span class="sxs-lookup"><span data-stu-id="514a6-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="514a6-136">Lai gan daudzi uzdevumu ceļveži ir iztulkoti, klients šobrīd nerāda tulkoto uzdevumu ceļvežu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="514a6-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="514a6-137">Turklāt 2016. gada maija bibliotēkā tulkojumi ir pieejami tikai tiem uzdevumu ceļvežiem, kas tika izlaisti 2016. gada februārī.</span><span class="sxs-lookup"><span data-stu-id="514a6-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="514a6-138">Microsoft izdosim atjauninātu bibliotēku, kas iekļauj papildu tulkojumus.</span><span class="sxs-lookup"><span data-stu-id="514a6-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="514a6-139">Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.</span><span class="sxs-lookup"><span data-stu-id="514a6-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="514a6-140">Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).</span><span class="sxs-lookup"><span data-stu-id="514a6-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="514a6-141">Pielāgotās palīdzības pievienošana</span><span class="sxs-lookup"><span data-stu-id="514a6-141">Adding custom Help</span></span>

<span data-ttu-id="514a6-142">Var izmantot uzdevumu ceļvežus, lai izveidotu palīdzību, vai jūs varat savienot pielāgotās palīdzības vietni rūtī **Palīdzība**.</span><span class="sxs-lookup"><span data-stu-id="514a6-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="514a6-143">Pielāgotās palīdzības izveide, izmantojot uzdevumu ceļvežus</span><span class="sxs-lookup"><span data-stu-id="514a6-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="514a6-144">Atbalstītajām programmām varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tad tos saglabājot LCS biznesa procesu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="514a6-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="514a6-145">Personāla vadībai nav iespējams izveidot pielāgotus uzdevumu ceļvežus.</span><span class="sxs-lookup"><span data-stu-id="514a6-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="514a6-146">Ja esat partneris un pārveidojat bibliotēku par korporatīvo bibliotēku, un iekļaujat to kādā risinājumā, tā ir pieejama jūsu klientiem.</span><span class="sxs-lookup"><span data-stu-id="514a6-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="514a6-147">Varat arī izveidot APQC vienotās bibliotēkas kopiju, pēc tam atvērt uzdevumu reģistrēšanu kopijā, rediģēt un saglabāt tos ar savām veiktajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="514a6-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="514a6-148">Papildinformāciju skatiet tēmā [Uzdevuma reģistrētāja resursi](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="514a6-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="514a6-149">Savienojuma izveide ar pielāgotu palīdzības vietni</span><span class="sxs-lookup"><span data-stu-id="514a6-149">Connect a custom Help site</span></span>

<span data-ttu-id="514a6-150">Finance and Operations lietojumprogrammas reti tiek lietotas ārpus kastes veidlapā.</span><span class="sxs-lookup"><span data-stu-id="514a6-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="514a6-151">Tā vietā risinājums ir pielāgots un paplašināts, lai atbilstu organizācijas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="514a6-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="514a6-152">Varat arī pielāgot un paplašināt palīdzības pieredzi.</span><span class="sxs-lookup"><span data-stu-id="514a6-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="514a6-153">Piemēram, varat pievienot pielāgotu palīdzību preces **Palīdzības** rūtij.</span><span class="sxs-lookup"><span data-stu-id="514a6-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="514a6-154">Korporācija Microsoft ir nodrošinājusi rīku komplektu, lai palīdzētu jums izvietot un savienot pielāgotu palīdzību **Palīdzības** rūtī.</span><span class="sxs-lookup"><span data-stu-id="514a6-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="514a6-155">Lai iegūtu informāciju par to, kā varat iestatīt pielāgotu palīdzības risinājumu, kas ir saistīts ar **Palīdzības** rūti, skatiet [Pielāgotās palīdzības pārskatu](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="514a6-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="514a6-156">Ja vēlaties sadarboties ar Microsoft, strādājot ar rīkiem un procesiem palīdzības pielāgošanai, aizpildiet veidlapu [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="514a6-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="514a6-157">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="514a6-157">See also</span></span>

[<span data-ttu-id="514a6-158">Palīdzības sistēma</span><span class="sxs-lookup"><span data-stu-id="514a6-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="514a6-159">Pielāgotās palīdzības pārskats</span><span class="sxs-lookup"><span data-stu-id="514a6-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="514a6-160">Uzdevuma reģistrētāja resursi</span><span class="sxs-lookup"><span data-stu-id="514a6-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="514a6-161">Dokumentācijas vai apmācības izveide, izmantojot uzdevuma reģistrētāju</span><span class="sxs-lookup"><span data-stu-id="514a6-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="514a6-162">Pielāgotās palīdzības GitHub repozitorijs</span><span class="sxs-lookup"><span data-stu-id="514a6-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
