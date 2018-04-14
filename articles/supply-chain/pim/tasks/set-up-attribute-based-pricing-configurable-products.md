--- 
title: "No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm"
description: "Šajā procedūrā parādīts kā iestatīt atribūtam atbilstošu cenu noteikšanu."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6562e4776e8d15258921f174fdc3cd30f4ac18e0
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="a1fd1-103">No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm</span><span class="sxs-lookup"><span data-stu-id="a1fd1-103">Set up attribute-based pricing for configurable products</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1fd1-104">Šajā procedūrā parādīts kā iestatīt atribūtam atbilstošu cenu noteikšanu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="a1fd1-105">Kā priekšnosacījumam, jums jābūt preces konfigurācijas modelim, kam ir viens vai vairāki komponenti un atribūti.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="a1fd1-106">Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa preces modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="a1fd1-107">Parasti produktu menedžeris izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="a1fd1-108">Izveidot jaunu cenas modeli</span><span class="sxs-lookup"><span data-stu-id="a1fd1-108">Create a new price model</span></span>
1. <span data-ttu-id="a1fd1-109">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a1fd1-110">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="a1fd1-111">Sarakstā atlasiet augstas kvalitātes skaļruņa rindu, bet nenoklikšķiniet uz nosaukuma saites.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="a1fd1-112">Darbību rūtī noklikšķiniet uz Modelis.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="a1fd1-113">Noklikšķiniet uz Cenu modeļi.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-113">Click Price models.</span></span>
6. <span data-ttu-id="a1fd1-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-114">Click New.</span></span>
7. <span data-ttu-id="a1fd1-115">Laukā Cenas modeļa nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="a1fd1-116">Izmantojiet nosaukumu, kas ļauj viegli identificēt modeli.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="a1fd1-117">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a1fd1-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="a1fd1-119">Pievienot cenas elementus</span><span class="sxs-lookup"><span data-stu-id="a1fd1-119">Add price elements</span></span>
1. <span data-ttu-id="a1fd1-120">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-120">Click Edit.</span></span>
    * <span data-ttu-id="a1fd1-121">Katrs komponents preces modelī var saturēt pamatcenas elementu un jebkādu cenas izteiksmes kārtulu skaitu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="a1fd1-122">Jūs varat arī pievienot cenas dažādās valūtās.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="a1fd1-123">Laukā Pamatcenas izteiksme ievadiet laukā vērtību.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="a1fd1-124">Piemēram, ievadiet 100.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-124">For example, type 100.</span></span>   <span data-ttu-id="a1fd1-125">Pamatcenas izteiksme var būt skaitliska vērtība, vai tā var sastāvēt no aritmētiska aprēķina, kas ietver vienu vai vairākus atribūtus.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="a1fd1-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-126">Click Add.</span></span>
4. <span data-ttu-id="a1fd1-127">Laukā Nosaukums ierakstiet 'Rosewood'.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="a1fd1-128">Cenas izteiksmes nosaukums palīdz noteikt, ko atspoguļo cenas elements.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="a1fd1-129">Šajā piemērā tiek izveidots cenas elements Rosewood skaļruņa korpusa apdares opcijai.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="a1fd1-130">Noklikšķiniet uz Rediģēt nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-130">Click Edit condition.</span></span>
    * <span data-ttu-id="a1fd1-131">Cenas nosacījumu palīdz nodrošināt to, ka cenas izteiksmes elements tiek iekļauts pārdošanas cenā tikai tad, ja ir noteiktu atribūtu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="a1fd1-132">Laukā ConstraintBody ievadiet 'CabinetFinish=="Rosewood"'.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="a1fd1-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-133">Click OK.</span></span>
8. <span data-ttu-id="a1fd1-134">Laukā Izteiksme ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="a1fd1-135">Piemēram, ievadiet 50.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-135">For example, type 50.</span></span>  
9. <span data-ttu-id="a1fd1-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-136">Close the page.</span></span>
10. <span data-ttu-id="a1fd1-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a1fd1-137">Close the page.</span></span>


