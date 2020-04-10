---
title: Pārdošanas cenu atlases kritēriju izveide
description: Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8c60b188b7c7090546e8367455e0f58ce9359b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147691"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="e1a22-103">Pārdošanas cenu atlases kritēriju izveide</span><span class="sxs-lookup"><span data-stu-id="e1a22-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1a22-104">Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="e1a22-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="e1a22-105">Šīs procedūras veikšanai ir nepieciešams, lai vismaz viens pārdošanas cenu modelis būtu pieejams.</span><span class="sxs-lookup"><span data-stu-id="e1a22-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="e1a22-106">Šajā piemērā tiek izmantots cenu modelis Skaļruņa risinājuma pārdošanas cenas modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="e1a22-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="e1a22-107">Parasti produktu menedžeris izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="e1a22-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="e1a22-108">Jauna kritērija pievienošana esošajam pārdošanas cenas modelim</span><span class="sxs-lookup"><span data-stu-id="e1a22-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="e1a22-109">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="e1a22-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e1a22-110">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="e1a22-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="e1a22-111">Sarakstā atlasiet rindu Skaļruņa risinājuma preces modelim, bet nenoklikšķiniet uz modeļa nosaukuma saites.</span><span class="sxs-lookup"><span data-stu-id="e1a22-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="e1a22-112">Darbību rūtī noklikšķiniet uz Modelis.</span><span class="sxs-lookup"><span data-stu-id="e1a22-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="e1a22-113">Noklikšķiniet uz Cenas modeļa kritēriji.</span><span class="sxs-lookup"><span data-stu-id="e1a22-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="e1a22-114">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="e1a22-114">Click New.</span></span>
7. <span data-ttu-id="e1a22-115">Laukā Nosaukums ierakstiet 'Debitoru grupa 10'.</span><span class="sxs-lookup"><span data-stu-id="e1a22-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="e1a22-116">Cenas modeļa kritērija nosaukums tiek izmantots, lai palīdzētu identificēt pamata atlases kritērijus.</span><span class="sxs-lookup"><span data-stu-id="e1a22-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="e1a22-117">Laukā Cenas modelis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e1a22-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="e1a22-118">Laukā Pasūtījuma tips atlasiet Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e1a22-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="e1a22-119">Pasūtījuma tips nosaka datu bāzes laukus, kas būs pieejami atlases vaicājumā.</span><span class="sxs-lookup"><span data-stu-id="e1a22-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="e1a22-120">Laukā Spēkā no ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="e1a22-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="e1a22-121">Laukā Beidzas pēc ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="e1a22-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="e1a22-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e1a22-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="e1a22-123">Izveidot vaicājumu atlases kritērijiem</span><span class="sxs-lookup"><span data-stu-id="e1a22-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="e1a22-124">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="e1a22-124">Click Edit.</span></span>
2. <span data-ttu-id="e1a22-125">Laukā Tabula atlasiet Debitorus.</span><span class="sxs-lookup"><span data-stu-id="e1a22-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="e1a22-126">Laukā Lauks atlasiet Debitoru grupu.</span><span class="sxs-lookup"><span data-stu-id="e1a22-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="e1a22-127">Šajā piemērā atlases kritērijiem tiks izmantota noteikta debitoru grupa.</span><span class="sxs-lookup"><span data-stu-id="e1a22-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="e1a22-128">Laukā Kritēriji atlasiet debitoru grupu 10.</span><span class="sxs-lookup"><span data-stu-id="e1a22-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="e1a22-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e1a22-129">Click OK.</span></span>

