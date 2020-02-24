---
title: Lietotāja interfeisa elementi
description: Šajā tēmā ir aprakstīti lietotāja interfeisa (UI) elementi programmā.
author: tlefor
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: ''
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8087090b16ddbcf9586ae289c6ec7c1d23087422
ms.sourcegitcommit: c0929ebda9dfb7affe2a187336abf980ce2009a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2020
ms.locfileid: "2994122"
---
# <a name="user-interface-elements"></a><span data-ttu-id="5db55-103">Lietotāja interfeisa elementi</span><span class="sxs-lookup"><span data-stu-id="5db55-103">User interface elements</span></span>

<span data-ttu-id="5db55-104">Šajā tēmā ir aprakstīti lietotāja interfeisa (UI) elementi, kas tiek izmantoti programmā.</span><span class="sxs-lookup"><span data-stu-id="5db55-104">This topic describes the user interface (UI) elements used in the app.</span></span> <span data-ttu-id="5db55-105">Pirms lietotāji var pārvietoties interfeisā, ir svarīgi zināt to elementu nosaukumus un funkcijas, kuri veido interfeisu.</span><span class="sxs-lookup"><span data-stu-id="5db55-105">Before users can navigate the interface, it's important to know the names and functions of the elements that make up the interface.</span></span>

## <a name="overview"></a><span data-ttu-id="5db55-106">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="5db55-106">Overview</span></span>

- <span data-ttu-id="5db55-107">**Darbību rūts** — josla zem navigācijas joslas.</span><span class="sxs-lookup"><span data-stu-id="5db55-107">**Action Pane** - The bar beneath the navigation bar.</span></span> <span data-ttu-id="5db55-108">Šeit var atlasīt cilnes, lai mainītu ierakstus, kas tiek parādīti lapā.</span><span class="sxs-lookup"><span data-stu-id="5db55-108">Here, you can select tabs to change records shown in the page.</span></span> <span data-ttu-id="5db55-109">Šeit var rediģēt un saglabāt ierakstus.</span><span class="sxs-lookup"><span data-stu-id="5db55-109">You can edit and save the records here.</span></span>  
- <span data-ttu-id="5db55-110">**Papildinformācija** — varat apskatīt informāciju un sekot noteiktu ierakstu darbībām šajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="5db55-110">**FactBox** - You can see information and follow the activities of certain records in this pane.</span></span>  
- <span data-ttu-id="5db55-111">**Papildinformācijas rūts** — varat ritināt dažādus ieraksta aspektus, lai tos skatītu sadaļā Papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="5db55-111">**FactBox pane** Here, you can scroll through different aspects of a record to view in the FactBox.</span></span>  
- <span data-ttu-id="5db55-112">**Filtra rūts** — dažās lapās varat atlasīt opciju **Rādīt filtrus**, lai atvērtu šo rūti.</span><span class="sxs-lookup"><span data-stu-id="5db55-112">**Filter pane** - On some pages, you can select **Show filters** to open this pane.</span></span> <span data-ttu-id="5db55-113">Tas ļauj jums sašaurināt rezultātus, kas redzami lapā.</span><span class="sxs-lookup"><span data-stu-id="5db55-113">It allows you to narrow the results visible to you on the page.</span></span>  
- <span data-ttu-id="5db55-114">**Navigācijas josla** — josla, kas atrodas interfeisa augšpusē.</span><span class="sxs-lookup"><span data-stu-id="5db55-114">**Navigation bar** - The bar at the top of the interface.</span></span> <span data-ttu-id="5db55-115">Tas ietver tādas sadaļas kā **Dynamics 365 portāls**, **Meklēšana**, **Uzņēmuma atlasītājs**, **Darbību centrs**, **Iestatījumi**, **Palīdzība un atbalsts** un lietotāja profilu.</span><span class="sxs-lookup"><span data-stu-id="5db55-115">It contains the **Dynamics 365 portal**, **Search**, **company picker**, **Action center**, **Settings**, **Help & Support**, and the user profile.</span></span>  
- <span data-ttu-id="5db55-116">**Navigācijas saraksts** — dažās lapās varat ritināt šo rūti, lai atrastu noteiktu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5db55-116">**Navigation list** - On some pages, you can scroll through this pane to find a specific record.</span></span> <span data-ttu-id="5db55-117">Ja šī opcija ir atlasīta, informācija par ierakstu tiks parādīta lapā.</span><span class="sxs-lookup"><span data-stu-id="5db55-117">When selected, the details of the record will appear in the page.</span></span>  
- <span data-ttu-id="5db55-118">**Navigācijas rūts** — kreisās puses tālākā rūts.</span><span class="sxs-lookup"><span data-stu-id="5db55-118">**Navigation pane** - The left-most pane.</span></span> <span data-ttu-id="5db55-119">No šejienes varat atrast jebkuru preces lapu.</span><span class="sxs-lookup"><span data-stu-id="5db55-119">From here, you can find any page in the product.</span></span>  
- <span data-ttu-id="5db55-120">**Lapa** — interfeisa centrālais fokuss.</span><span class="sxs-lookup"><span data-stu-id="5db55-120">**Page** - The central focus of the interface.</span></span> <span data-ttu-id="5db55-121">Atlases, kas veiktas citos lietotāja interfeisa komponentos, ietekmēs, kādi ieraksti tiek parādīti šeit.</span><span class="sxs-lookup"><span data-stu-id="5db55-121">Selections made on the other UI components will affect what records are shown here.</span></span>  
- <span data-ttu-id="5db55-122">**Rūts** — labās puses tālākā rūts.</span><span class="sxs-lookup"><span data-stu-id="5db55-122">**Pane** - The right-most pane.</span></span> <span data-ttu-id="5db55-123">Tā atvērsies dažos gadījumos, kad ir jāmaina un jāsaglabā ieraksta aspekti.</span><span class="sxs-lookup"><span data-stu-id="5db55-123">This will open in some cases when aspects of a record need to be changed and saved.</span></span>  
- <span data-ttu-id="5db55-124">**Cilne** — atsaucoties uz darbības rūti, tā ir opciju izvēlne, kas parādās, kad darbības rūtī atlasāt doto opciju.</span><span class="sxs-lookup"><span data-stu-id="5db55-124">**Tab** - When referring to the Action Pane, it's a menu of options that appears when you select a given option in the Action Pane.</span></span>  

![Šis attēls parāda šo elementu novietojumu interfeisā.](media/user-interface-01.png)

## <a name="tabs-fields-and-sections"></a><span data-ttu-id="5db55-126">Cilnes, lauki un sadaļas</span><span class="sxs-lookup"><span data-stu-id="5db55-126">Tabs, fields, and sections</span></span>

<span data-ttu-id="5db55-127">*Cilne* ir atlase, kas veikta lapā, kas atver citu ieraksta aspektu tajā pašā lapā.</span><span class="sxs-lookup"><span data-stu-id="5db55-127">A *tab* is a selection made on the page that opens a different aspect of a record on the same page.</span></span> <span data-ttu-id="5db55-128">Bieži tā ļauj mainīt noteiktus *laukus* vai lietotāja interfeisa elementus, kas ļauj ievadīt rakstisku ievadi.</span><span class="sxs-lookup"><span data-stu-id="5db55-128">Often, it will allow you to change certain *fields*, or UI elements that allow typed input.</span></span> 

<span data-ttu-id="5db55-129">*Kopsavilkuma cilne* ir cilne ar papildu priekšrocībām, kas ļauj skatīt vairākas cilnes.</span><span class="sxs-lookup"><span data-stu-id="5db55-129">A *FastTab* is a tab with the added benefit of allowing multiple tabs to be visible at the same.</span></span> <span data-ttu-id="5db55-130">Jūs varat izvērst kopsavilkuma cilni, atlasot lejupvērsto bultiņu tās labajā malā.</span><span class="sxs-lookup"><span data-stu-id="5db55-130">You can expand a FastTab by selecting the downward-pointing arrow on the right end of it.</span></span>

![Tālāk esošajā attēlā ir parādīts ciļņu un kopsavilkuma ciļņu piemērs.](media/user-interface-02.png)

<span data-ttu-id="5db55-132">*Sadaļa* ir līdzīga cilnei. Vārds “sadaļa” bieži tiek izmantots, lai aprakstītu jebkuru lapas apgabalu, kas kārto noteiktu informācijas kategoriju.</span><span class="sxs-lookup"><span data-stu-id="5db55-132">A *section* is similar to a tab. The word "section" is often used to describe any area of a page that organizes a specific category of information.</span></span> <span data-ttu-id="5db55-133">Tālāk esošajā attēlā ir visu sadaļu piemēri — kopsavilkums, pasūtījumi un izlase.</span><span class="sxs-lookup"><span data-stu-id="5db55-133">In the following image, Summary, Orders and favorites, and Links are all examples of sections.</span></span>

![Tālāk esošajā attēlā ir parādīts cilnes un sadaļas piemērs.](media/user-interface-03.png)

## <a name="dialog-boxes-and-drop-down-menus"></a><span data-ttu-id="5db55-135">Dialoglodziņi un nolaižamās izvēlnes</span><span class="sxs-lookup"><span data-stu-id="5db55-135">Dialog boxes and drop-down menus</span></span>

<span data-ttu-id="5db55-136">*Dialoglodziņš* ir rūts, kas atveras, kad ir veiktas noteiktas atlases, lai mainītu vai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5db55-136">A *dialog box* is a pane that opens when certain selections are made to change or create a record.</span></span> <span data-ttu-id="5db55-137">Dialoglodziņos ir ietverti lauki, kas ļauj ievadīt rakstisku ievadi.</span><span class="sxs-lookup"><span data-stu-id="5db55-137">Dialog boxes contain fields that allow you to enter typed input.</span></span> <span data-ttu-id="5db55-138">Dažkārt norādītais lauks ļaus jums atlasīt lejupvērstu bultiņu, kas atver opciju sarakstu, no kura izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="5db55-138">Sometimes, a given field will allow you to select a downward facing arrow that opens a list of options to choose from.</span></span> <span data-ttu-id="5db55-139">To sauc par *nolaižamo izvēlni*.</span><span class="sxs-lookup"><span data-stu-id="5db55-139">This is called a *drop-down menu*.</span></span> <span data-ttu-id="5db55-140">Tālāk esošajā attēlā lauki **Veids** un **Klienta grupa** ietver opciju atvērt nolaižamo izvēlni.</span><span class="sxs-lookup"><span data-stu-id="5db55-140">In the following image, the **Type** and **Customer group** fields contain the option to open a drop-down menu.</span></span>

![Tālāk esošajā attēlā ir parādīts dialoglodziņa piemērs.](media/user-interface-04.png)

<span data-ttu-id="5db55-142">Dažos gadījumos, atlasot šo opciju, tiks atvērts dialoglodziņš pie dotās pogas.</span><span class="sxs-lookup"><span data-stu-id="5db55-142">In some cases, a dialog box will open near a given button when you select it.</span></span> <span data-ttu-id="5db55-143">To sauc par *nolaižamo dialoglodziņu*.</span><span class="sxs-lookup"><span data-stu-id="5db55-143">This is called a *drop-down dialog box*.</span></span> <span data-ttu-id="5db55-144">Tālāk esošajā attēlā tika atlasīta poga **Sākuma datums**, kas atvēra nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="5db55-144">In the following image, the **As of date** button was selected, which opened a drop-down dialog box.</span></span>

![Tālāk esošajā attēlā ir parādīts nolaižamā dialoglodziņa piemērs.](media/user-interface-05.png)

## <a name="notifications"></a><span data-ttu-id="5db55-146">Paziņojumi</span><span class="sxs-lookup"><span data-stu-id="5db55-146">Notifications</span></span>

<span data-ttu-id="5db55-147">Noteiktas izmaiņas objektos, ko pārraudzīsiet, parādīsies kā *paziņojumi*.</span><span class="sxs-lookup"><span data-stu-id="5db55-147">Certain changes to the objects you oversee will appear as *notifications*.</span></span> <span data-ttu-id="5db55-148">Paziņojumi var jūs informēt, kad tiek mainīta noteikta klienta informācija, vai arī tie var brīdināt, kad sistēma nevar pieņemt ievadītos datus, kas pievienoti noteiktos laukos.</span><span class="sxs-lookup"><span data-stu-id="5db55-148">Notifications may notify you when a specific customer's information has been changed, or it may alert you when the system can't accept inputs you've added in certain fields.</span></span> <span data-ttu-id="5db55-149">Varat uzzināt par to, kā pielāgot paziņojumus, kas tiek saņemti, sadaļā [Brīdinājumu pārskats](../get-started/alerts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5db55-149">You can learn how to customize what you receive notifications about in the [Alerts overview](../get-started/alerts-overview.md).</span></span>

<span data-ttu-id="5db55-150">Paziņojumi parādās dažādos veidos.</span><span class="sxs-lookup"><span data-stu-id="5db55-150">Notifications appear in a variety of ways.</span></span>
- <span data-ttu-id="5db55-151">**Līdzekļa remarka** — tā parādīsies blakus laukam, cilnei vai citai pogai, lai sniegtu paskaidrojumu par to, kam tiek izmantots šis līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="5db55-151">**Feature callout** - This will appear next to a field, tab, or other button to offer an explanation of what the feature is used for.</span></span> 
- <span data-ttu-id="5db55-152">**Darbību centrs** — navigācijas joslā blakus darbību centra pogai tiks parādīts lodziņš, kurā ir paziņojums.</span><span class="sxs-lookup"><span data-stu-id="5db55-152">**Action center** - A box that contains the notification will appear next to the Action center button on the navigation bar.</span></span> <span data-ttu-id="5db55-153">Varat skatīt detalizētu informāciju par paziņojumu, atlasot vienumu **Darbību centrs**.</span><span class="sxs-lookup"><span data-stu-id="5db55-153">You can see details about the notification by selecting **Action center**.</span></span>  
- <span data-ttu-id="5db55-154">**Ziņojumu josla** — tā parādīsies zem darbības rūts.</span><span class="sxs-lookup"><span data-stu-id="5db55-154">**Message bar** - This will appear beneath the Action Pane.</span></span>  

<span data-ttu-id="5db55-155">Tālāk esošajā attēlā ir parādīti šo paziņojumu veidu piemēri.</span><span class="sxs-lookup"><span data-stu-id="5db55-155">The following image shows examples of these types of notifications.</span></span>

![Tālāk esošajā attēlā ir parādīti šo paziņojumu piemēri.](media/user-interface-06.png)

- <span data-ttu-id="5db55-157">**Ziņojuma lodziņš** — tas parādīsies virs interfeisa un jums ar to ir jāmijiedarbojas, pirms varat turpināt izmantot preci.</span><span class="sxs-lookup"><span data-stu-id="5db55-157">**Message box** - This will appear over the interface and must be interacted with before you can continue to use the product.</span></span>  

![Tālāk esošajā attēlā ir parādīts ziņojuma piemērs.](media/user-interface-07.png)

## <a name="toolbars-grids-and-lists"></a><span data-ttu-id="5db55-159">Rīkjoslas, režģi un saraksti</span><span class="sxs-lookup"><span data-stu-id="5db55-159">Toolbars, grids, and lists</span></span>

<span data-ttu-id="5db55-160">*Rīkjosla* ietver rīkus, piemēram, iespēju pievienot laukus vai noņemt ierakstus.</span><span class="sxs-lookup"><span data-stu-id="5db55-160">A *toolbar* contains tools, such as the ability to add fields or remove records.</span></span> <span data-ttu-id="5db55-161">Dažreiz rīkjosla parādīsies lapā virs *režģa*.</span><span class="sxs-lookup"><span data-stu-id="5db55-161">Sometimes, a toolbar will appear on the page above a *grid*.</span></span> <span data-ttu-id="5db55-162">Šis apgabals, režģis, ir nosaukums, kas piešķirts ierakstu rindām ar dažādām datu kolonnām.</span><span class="sxs-lookup"><span data-stu-id="5db55-162">This area, grid, is a name given to rows of records with various columns of data.</span></span> <span data-ttu-id="5db55-163">Ne virs visiem režģiem ir rīkjoslas.</span><span class="sxs-lookup"><span data-stu-id="5db55-163">Not all grids have toolbars above them.</span></span>

<span data-ttu-id="5db55-164">*Saraksts* ir nosaukums, kas tiek piešķirts ierakstu kolekcijai, ko varat ritināt.</span><span class="sxs-lookup"><span data-stu-id="5db55-164">A *list* is the name given to a collection of records that you can scroll through.</span></span> <span data-ttu-id="5db55-165">Šos ierakstus varat pārnest lapā, atlasot tos.</span><span class="sxs-lookup"><span data-stu-id="5db55-165">You can bring these records into the page by selecting them.</span></span> <span data-ttu-id="5db55-166">Bieži vien tas atvērs režģi.</span><span class="sxs-lookup"><span data-stu-id="5db55-166">Often, this will open a grid.</span></span>

![Tālāk esošajā attēlā ir redzami rīkjoslu, režģu un sarakstu piemēri.](media/user-interface-08.png)
