---
title: No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm
description: Šajā tēmā ir izskaidrots, kā iestatīt uz atribūtiem balstītu cenu noteikšanu.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a75f3afcf4761ac6a9575eae9a620a1e9f01c8e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981042"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="85bba-103">No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm</span><span class="sxs-lookup"><span data-stu-id="85bba-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85bba-104">Šajā tēmā ir izskaidrots, kā iestatīt uz atribūtiem balstītu cenu noteikšanu.</span><span class="sxs-lookup"><span data-stu-id="85bba-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="85bba-105">Kā priekšnosacījumam, jums jābūt preces konfigurācijas modelim, kam ir viens vai vairāki komponenti un atribūti.</span><span class="sxs-lookup"><span data-stu-id="85bba-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="85bba-106">Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa preces modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="85bba-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="85bba-107">Parasti produktu menedžeris izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="85bba-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="85bba-108">Izveidot jaunu cenas modeli</span><span class="sxs-lookup"><span data-stu-id="85bba-108">Create a new price model</span></span>
1. <span data-ttu-id="85bba-109">Sākumlapā atlasiet **Produkta varianta modeļa definīcija**.</span><span class="sxs-lookup"><span data-stu-id="85bba-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="85bba-110">Atlasiet krājumu **produkta konfigurācijas modeļi** sadaļā **saites**.</span><span class="sxs-lookup"><span data-stu-id="85bba-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="85bba-111">Sarakstā atlasiet rindu **Augstākās klases runātājs**, bet neatlasiet saiti nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="85bba-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="85bba-112">Darbību rūtī atlasiet **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="85bba-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="85bba-113">Atlasiet **Cenu modeļi**.</span><span class="sxs-lookup"><span data-stu-id="85bba-113">Select **Price models**.</span></span>
6. <span data-ttu-id="85bba-114">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="85bba-114">Select **New**.</span></span>
7. <span data-ttu-id="85bba-115">Laukā **Cenu modeļa nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="85bba-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="85bba-116">Izmantojiet nosaukumu, kas ļauj viegli identificēt modeli.</span><span class="sxs-lookup"><span data-stu-id="85bba-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="85bba-117">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="85bba-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="85bba-118">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="85bba-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="85bba-119">Pievienot cenas elementus</span><span class="sxs-lookup"><span data-stu-id="85bba-119">Add price elements</span></span>
1. <span data-ttu-id="85bba-120">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="85bba-120">Select **Edit**.</span></span> <span data-ttu-id="85bba-121">Katrs komponents preces modelī var saturēt pamatcenas elementu un jebkādu cenas izteiksmes kārtulu skaitu.</span><span class="sxs-lookup"><span data-stu-id="85bba-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="85bba-122">Jūs varat arī pievienot cenas dažādās valūtās.</span><span class="sxs-lookup"><span data-stu-id="85bba-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="85bba-123">Laukā **Bāzes cenas izteiksme** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="85bba-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="85bba-124">Piemēram, ievadiet 100.</span><span class="sxs-lookup"><span data-stu-id="85bba-124">For example, type 100.</span></span> <span data-ttu-id="85bba-125">Pamatcenas izteiksme var būt skaitliska vērtība, vai tā var sastāvēt no aritmētiska aprēķina, kas ietver vienu vai vairākus atribūtus.</span><span class="sxs-lookup"><span data-stu-id="85bba-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="85bba-126">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="85bba-126">Select **Add**.</span></span>
4. <span data-ttu-id="85bba-127">Laukā **Nosaukums** ievadiet `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="85bba-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="85bba-128">Cenas izteiksmes nosaukums palīdz noteikt, ko atspoguļo cenas elements.</span><span class="sxs-lookup"><span data-stu-id="85bba-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="85bba-129">Šajā piemērā tiek izveidots cenas elements Rosewood skaļruņa korpusa apdares opcijai.</span><span class="sxs-lookup"><span data-stu-id="85bba-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="85bba-130">Atlasīt **Rediģēt nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="85bba-130">Select **Edit condition**.</span></span> <span data-ttu-id="85bba-131">Cenas nosacījumu palīdz nodrošināt to, ka cenas izteiksmes elements tiek iekļauts pārdošanas cenā tikai tad, ja ir noteiktu atribūtu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="85bba-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="85bba-132">Laukā **ConstraintBody** ievadiet `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="85bba-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="85bba-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="85bba-133">Select **OK**.</span></span>
8. <span data-ttu-id="85bba-134">Laukā **Izteiksme** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="85bba-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="85bba-135">Piemēram, ievadiet `50`.</span><span class="sxs-lookup"><span data-stu-id="85bba-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="85bba-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="85bba-136">Close the page.</span></span>

