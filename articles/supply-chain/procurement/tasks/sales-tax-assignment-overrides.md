---
title: PVN piešķire un pārrakstīšana
description: Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt mazumtirdzniecības kanāliem.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f08829bccbaea6fb70563e553f9042300b4d5ea9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838002"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="b7b2a-103">PVN piešķire un pārrakstīšana</span><span class="sxs-lookup"><span data-stu-id="b7b2a-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7b2a-104">Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt mazumtirdzniecības kanāliem.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="b7b2a-105">Tajā ir arī izklāstīta jaunas pārdošanas nodokļu ignorēšanas izveidošana un tās piešķiršana jau pastāvošai pārdošanas nodokļu ignorēšanas grupai.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="b7b2a-106">Šajā procedūrā</span><span class="sxs-lookup"><span data-stu-id="b7b2a-106">This procedure</span></span>

<span data-ttu-id="b7b2a-107">tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b7b2a-108">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="b7b2a-109">Sarakstā noklikšķiniet uz saites Mazumtirdzniecības kanāla ID grupai “Hjūstona”.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="b7b2a-110">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-110">Click Edit.</span></span>
    * <span data-ttu-id="b7b2a-111">Laukā “Pārdošanas nodokļu grupa” ir saraksts ar pārdošanas nodokļu grupām pašreizējam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="b7b2a-112">Pašlaik piešķirtā grupa ir vispārīga pārdošanas nodokļu grupa “Teksasa”.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="b7b2a-113">Ir pieejamas arī PVN grupas "Washington" un "Washington, King County".</span><span class="sxs-lookup"><span data-stu-id="b7b2a-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="b7b2a-114">PVN grupas var ietvert vairāku pašvaldību piemērojamos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="b7b2a-115">Lauks “Pārdošanas nodokļu ignorēšana” ir vieta, kur pārdošanas nodokļu ignorēšanas grupas var kartēt uz kanālu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="b7b2a-116">Pārdošanas nodokļu ignorēšanas grupas var izmantot, lai sagrupētu pārdošanas nodokļu ignorēšanu, kas darbojas vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="b7b2a-117">Tā vietā, lai pārdošanas nodokļu ignorēšanu manuāli piešķirtu pa vienai, šādu grupu varat izveidot un piešķirt tieši kanāliem, lai ietaupītu laiku.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="b7b2a-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-118">Click Save.</span></span>
5. <span data-ttu-id="b7b2a-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-119">Close the page.</span></span>
6. <span data-ttu-id="b7b2a-120">Doties uz Mazumtirdzniecība un komercija > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšana.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="b7b2a-121">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-121">Click New.</span></span>
8. <span data-ttu-id="b7b2a-122">Laukā Pārdošanas nodokļu ignorēšana norādiet savas jaunās ignorēšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="b7b2a-123">Laukā Apraksts norādiet ignorēšanas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="b7b2a-124">Statusu iestatiet uz “Iespējot”.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="b7b2a-125">Izvērsiet vai sakļaujiet sadaļu Ignorēt.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="b7b2a-126">Atlasiet opciju laukā Tips.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="b7b2a-127">Krājumu pārdošanas nodokļu grupas var izmantot, lai ignorētu nodokļus noteiktiem krājumiem, kas pieder šai grupai.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="b7b2a-128">Piemēram, pārtikas precēm nodokļi parasti tiek piemēroti atšķirīgi no ilglietojamām precēm, un tām, visticamāk, būs pašām sava pārdošanas nodokļu grupa.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="b7b2a-129">Pārdošanas nodokļu grupas ir nodokļu grupas, kas ir attiecināmas uz konkrētu kanālu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="b7b2a-130">Piemēram, ja kanālā notiek gan mazumtirdzniecība, gan pārdošana no viena uzņēmuma citam, var izmantot dažādas pārdošanas nodokļu grupas.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="b7b2a-131">Visi piemērojamie nodokļi būtu kartēti uz pārdošanas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="b7b2a-132">Lai izveidotu savu pārdošanas nodokļu ignorēšanu, tagad varat atlasīt nodokļus “No” un “Uz” vai “No nodokļu grupas” un “Uz nodokļu grupu”.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="b7b2a-133">Laukā “No” ir norādīti nodokļi vai nodokļu grupa, kas ir jāignorē.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="b7b2a-134">Ignorēšana ar krājuma pārdošanas nodokļu grupu sniedz citādas opcijas nekā ignorēšana ar pārdošanas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="b7b2a-135">Pārdošanas nodokļu ignorēšanu var iestatīt tā, lai ignorētu nodokļus visās transakcijās vai konkrētās transakcijas rindās.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="b7b2a-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-136">Click Save.</span></span>
14. <span data-ttu-id="b7b2a-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-137">Close the page.</span></span>
15. <span data-ttu-id="b7b2a-138">Doties uz Mazumtirdzniecība un komercija > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšanas grupas.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="b7b2a-139">Šajā darbībā jūs tikko izveidotā pārdošanas nodokļa ignorēšanu piešķirsiet pārdošanas nodokļu ignorēšanas grupai, kas ir piešķirta kanālam Hjūstona.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="b7b2a-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-140">Click Edit.</span></span>
17. <span data-ttu-id="b7b2a-141">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="b7b2a-142">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-142">Click Add.</span></span>
19. <span data-ttu-id="b7b2a-143">Laukā Pārdošanas nodokļu ignorēšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="b7b2a-144">Sarakstā atlasiet iepriekš izveidoto pārdošanas nodokļa ignorēšanu.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="b7b2a-145">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="b7b2a-146">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-146">Click Save.</span></span>

