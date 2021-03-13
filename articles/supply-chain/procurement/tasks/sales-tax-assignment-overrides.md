---
title: PVN piešķire un pārrakstīšana
description: Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt komercijas kanāliem.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c6e1de5046a3ce5d896ba3686a28d6d474d4268
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020732"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="f39ec-103">PVN piešķire un pārrakstīšana</span><span class="sxs-lookup"><span data-stu-id="f39ec-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f39ec-104">Šajā procedūrā ir parādīts, kā pārdošanas nodokļu grupu piešķirt komercijas kanāliem.</span><span class="sxs-lookup"><span data-stu-id="f39ec-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="f39ec-105">Tajā ir arī izklāstīta jaunas pārdošanas nodokļu ignorēšanas izveidošana un tās piešķiršana jau pastāvošai pārdošanas nodokļu ignorēšanas grupai.</span><span class="sxs-lookup"><span data-stu-id="f39ec-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="f39ec-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="f39ec-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f39ec-107">Parejiet uz Retail un Commerce > Kanāli > Veikali > Visi veikali.</span><span class="sxs-lookup"><span data-stu-id="f39ec-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="f39ec-108">Sarakstā noklikšķiniet uz saites Kanāla ID grupai “Hjūstona”.</span><span class="sxs-lookup"><span data-stu-id="f39ec-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="f39ec-109">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f39ec-109">Click Edit.</span></span>
    * <span data-ttu-id="f39ec-110">Laukā “Pārdošanas nodokļu grupa” ir saraksts ar pārdošanas nodokļu grupām pašreizējam uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="f39ec-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="f39ec-111">Pašlaik piešķirtā grupa ir vispārīga pārdošanas nodokļu grupa “Teksasa”.</span><span class="sxs-lookup"><span data-stu-id="f39ec-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="f39ec-112">Ir pieejamas arī PVN grupas "Washington" un "Washington, King County".</span><span class="sxs-lookup"><span data-stu-id="f39ec-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="f39ec-113">PVN grupas var ietvert vairāku pašvaldību piemērojamos nodokļus.</span><span class="sxs-lookup"><span data-stu-id="f39ec-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="f39ec-114">Lauks “Pārdošanas nodokļu ignorēšana” ir vieta, kur pārdošanas nodokļu ignorēšanas grupas var kartēt uz kanālu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="f39ec-115">Pārdošanas nodokļu ignorēšanas grupas var izmantot, lai sagrupētu pārdošanas nodokļu ignorēšanu, kas darbojas vairākiem veikaliem.</span><span class="sxs-lookup"><span data-stu-id="f39ec-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="f39ec-116">Tā vietā, lai pārdošanas nodokļu ignorēšanu manuāli piešķirtu pa vienai, šādu grupu varat izveidot un piešķirt tieši kanāliem, lai ietaupītu laiku.</span><span class="sxs-lookup"><span data-stu-id="f39ec-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="f39ec-117">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f39ec-117">Click Save.</span></span>
5. <span data-ttu-id="f39ec-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-118">Close the page.</span></span>
6. <span data-ttu-id="f39ec-119">Doties uz Retail un Commerce > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšana.</span><span class="sxs-lookup"><span data-stu-id="f39ec-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="f39ec-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f39ec-120">Click New.</span></span>
8. <span data-ttu-id="f39ec-121">Laukā Pārdošanas nodokļu ignorēšana norādiet savas jaunās ignorēšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="f39ec-122">Laukā Apraksts norādiet ignorēšanas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="f39ec-123">Statusu iestatiet uz “Iespējot”.</span><span class="sxs-lookup"><span data-stu-id="f39ec-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="f39ec-124">Izvērsiet vai sakļaujiet sadaļu Ignorēt.</span><span class="sxs-lookup"><span data-stu-id="f39ec-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="f39ec-125">Atlasiet opciju laukā Tips.</span><span class="sxs-lookup"><span data-stu-id="f39ec-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="f39ec-126">Krājumu pārdošanas nodokļu grupas var izmantot, lai ignorētu nodokļus noteiktiem krājumiem, kas pieder šai grupai.</span><span class="sxs-lookup"><span data-stu-id="f39ec-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="f39ec-127">Piemēram, pārtikas precēm nodokļi parasti tiek piemēroti atšķirīgi no ilglietojamām precēm, un tām, visticamāk, būs pašām sava pārdošanas nodokļu grupa.</span><span class="sxs-lookup"><span data-stu-id="f39ec-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="f39ec-128">Pārdošanas nodokļu grupas ir nodokļu grupas, kas ir attiecināmas uz konkrētu kanālu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="f39ec-129">Piemēram, ja kanālā notiek gan mazumtirdzniecība, gan pārdošana no viena uzņēmuma citam, var izmantot dažādas pārdošanas nodokļu grupas.</span><span class="sxs-lookup"><span data-stu-id="f39ec-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="f39ec-130">Visi piemērojamie nodokļi būtu kartēti uz pārdošanas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="f39ec-131">Lai izveidotu savu pārdošanas nodokļu ignorēšanu, tagad varat atlasīt nodokļus “No” un “Uz” vai “No nodokļu grupas” un “Uz nodokļu grupu”.</span><span class="sxs-lookup"><span data-stu-id="f39ec-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="f39ec-132">Laukā “No” ir norādīti nodokļi vai nodokļu grupa, kas ir jāignorē.</span><span class="sxs-lookup"><span data-stu-id="f39ec-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="f39ec-133">Ignorēšana ar krājuma pārdošanas nodokļu grupu sniedz citādas opcijas nekā ignorēšana ar pārdošanas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="f39ec-134">Pārdošanas nodokļu ignorēšanu var iestatīt tā, lai ignorētu nodokļus visās transakcijās vai konkrētās transakcijas rindās.</span><span class="sxs-lookup"><span data-stu-id="f39ec-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="f39ec-135">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f39ec-135">Click Save.</span></span>
14. <span data-ttu-id="f39ec-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-136">Close the page.</span></span>
15. <span data-ttu-id="f39ec-137">Doties uz Retail un Commerce > Kanāla iestatīšana > Pārdošanas nodokļi > Pārdošanas nodokļu ignorēšanas grupas.</span><span class="sxs-lookup"><span data-stu-id="f39ec-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="f39ec-138">Šajā darbībā jūs tikko izveidotā pārdošanas nodokļa ignorēšanu piešķirsiet pārdošanas nodokļu ignorēšanas grupai, kas ir piešķirta kanālam Hjūstona.</span><span class="sxs-lookup"><span data-stu-id="f39ec-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="f39ec-139">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f39ec-139">Click Edit.</span></span>
17. <span data-ttu-id="f39ec-140">Izvērsiet vai sakļaujiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="f39ec-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="f39ec-141">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="f39ec-141">Click Add.</span></span>
19. <span data-ttu-id="f39ec-142">Laukā Pārdošanas nodokļu ignorēšana noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="f39ec-143">Sarakstā atlasiet iepriekš izveidoto pārdošanas nodokļa ignorēšanu.</span><span class="sxs-lookup"><span data-stu-id="f39ec-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="f39ec-144">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f39ec-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="f39ec-145">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f39ec-145">Click Save.</span></span>

