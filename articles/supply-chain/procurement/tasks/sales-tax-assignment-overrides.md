--- 
title: "PVN piešķire un pārrakstīšana"
description: "Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt mazumtirdzniecības kanāliem."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8b3dc0beec17d80f7bbbcf234656a537a445789f
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="704da-103">PVN piešķire un pārrakstīšana</span><span class="sxs-lookup"><span data-stu-id="704da-103">Sales tax assignment and overrides</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="704da-104">Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="704da-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="704da-105">Tajā ir arī izklāstīta jaunas pārdošanas nodokļu ignorēšanas izveidošana un tās piešķiršana jau pastāvošai pārdošanas nodokļu ignorēšanas grupai.</span><span class="sxs-lookup"><span data-stu-id="704da-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="704da-106">Šajā procedūrā</span><span class="sxs-lookup"><span data-stu-id="704da-106">This procedure</span></span>

<span data-ttu-id="704da-107">tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="704da-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="704da-108">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="704da-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="704da-109">Sarakstā noklikšķiniet uz saites Mazumtirdzniecības kanāla ID grupai “Hjūstona”.</span><span class="sxs-lookup"><span data-stu-id="704da-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="704da-110">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="704da-110">Click Edit.</span></span>
    * <span data-ttu-id="704da-111">Laukā “Pārdošanas nodokļu grupa” ir saraksts ar pārdošanas nodokļu grupām pašreizējam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="704da-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="704da-112">Pašlaik piešķirtā grupa ir vispārīga pārdošanas nodokļu grupa “Teksasa”.</span><span class="sxs-lookup"><span data-stu-id="704da-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="704da-113">Ir pieejamas arī PVN grupas "Washington" un "Washington, King County".</span><span class="sxs-lookup"><span data-stu-id="704da-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="704da-114">PVN grupas var ietvert vairāku pašvaldību piemērojamos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="704da-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="704da-115">Lauks “Pārdošanas nodokļu ignorēšana” ir vieta, kur pārdošanas nodokļu ignorēšanas grupas var kartēt uz kanālu.</span><span class="sxs-lookup"><span data-stu-id="704da-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="704da-116">Pārdošanas nodokļu ignorēšanas grupas var izmantot, lai sagrupētu pārdošanas nodokļu ignorēšanu, kas darbojas vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="704da-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="704da-117">Tā vietā, lai pārdošanas nodokļu ignorēšanu manuāli piešķirtu pa vienai, šādu grupu varat izveidot un piešķirt tieši kanāliem, lai ietaupītu laiku.</span><span class="sxs-lookup"><span data-stu-id="704da-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="704da-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="704da-118">Click Save.</span></span>
5. <span data-ttu-id="704da-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="704da-119">Close the page.</span></span>
6. <span data-ttu-id="704da-120">Doties uz Mazumtirdzniecība un komercija > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšana.</span><span class="sxs-lookup"><span data-stu-id="704da-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="704da-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="704da-121">Click New.</span></span>
8. <span data-ttu-id="704da-122">Laukā Pārdošanas nodokļu ignorēšana norādiet savas jaunās ignorēšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="704da-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="704da-123">Laukā Apraksts norādiet ignorēšanas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="704da-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="704da-124">Statusu iestatiet uz “Iespējot”.</span><span class="sxs-lookup"><span data-stu-id="704da-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="704da-125">Izvērsiet vai sakļaujiet sadaļu Ignorēt.</span><span class="sxs-lookup"><span data-stu-id="704da-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="704da-126">Atlasiet opciju laukā Tips.</span><span class="sxs-lookup"><span data-stu-id="704da-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="704da-127">Krājumu pārdošanas nodokļu grupas var izmantot, lai ignorētu nodokļus noteiktiem krājumiem, kas pieder šai grupai.</span><span class="sxs-lookup"><span data-stu-id="704da-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="704da-128">Piemēram, pārtikas precēm nodokļi parasti tiek piemēroti atšķirīgi no ilglietojamām precēm, un tām, visticamāk, būs pašām sava pārdošanas nodokļu grupa.</span><span class="sxs-lookup"><span data-stu-id="704da-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="704da-129">Pārdošanas nodokļu grupas ir nodokļu grupas, kas ir attiecināmas uz konkrētu kanālu.</span><span class="sxs-lookup"><span data-stu-id="704da-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="704da-130">Piemēram, ja kanālā notiek gan mazumtirdzniecība, gan pārdošana no viena uzņēmuma citam, var izmantot dažādas pārdošanas nodokļu grupas.</span><span class="sxs-lookup"><span data-stu-id="704da-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="704da-131">Visi piemērojamie nodokļi būtu kartēti uz pārdošanas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="704da-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="704da-132">Lai izveidotu savu pārdošanas nodokļu ignorēšanu, tagad varat atlasīt nodokļus “No” un “Uz” vai “No nodokļu grupas” un “Uz nodokļu grupu”.</span><span class="sxs-lookup"><span data-stu-id="704da-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="704da-133">Laukā “No” ir norādīti nodokļi vai nodokļu grupa, kas ir jāignorē.</span><span class="sxs-lookup"><span data-stu-id="704da-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="704da-134">Ignorēšana ar krājuma pārdošanas nodokļu grupu sniedz citādas opcijas nekā ignorēšana ar pārdošanas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="704da-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="704da-135">Pārdošanas nodokļu ignorēšanu var iestatīt tā, lai ignorētu nodokļus visās transakcijās vai konkrētās transakcijas rindās.</span><span class="sxs-lookup"><span data-stu-id="704da-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="704da-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="704da-136">Click Save.</span></span>
14. <span data-ttu-id="704da-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="704da-137">Close the page.</span></span>
15. <span data-ttu-id="704da-138">Doties uz Mazumtirdzniecība un komercija > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšanas grupas.</span><span class="sxs-lookup"><span data-stu-id="704da-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="704da-139">Šajā darbībā jūs tikko izveidotā pārdošanas nodokļa ignorēšanu piešķirsiet pārdošanas nodokļu ignorēšanas grupai, kas ir piešķirta kanālam Hjūstona.</span><span class="sxs-lookup"><span data-stu-id="704da-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="704da-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="704da-140">Click Edit.</span></span>
17. <span data-ttu-id="704da-141">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="704da-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="704da-142">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="704da-142">Click Add.</span></span>
19. <span data-ttu-id="704da-143">Laukā Pārdošanas nodokļu ignorēšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="704da-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="704da-144">Sarakstā atlasiet iepriekš izveidoto pārdošanas nodokļa ignorēšanu.</span><span class="sxs-lookup"><span data-stu-id="704da-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="704da-145">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="704da-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="704da-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="704da-146">Click Save.</span></span>


