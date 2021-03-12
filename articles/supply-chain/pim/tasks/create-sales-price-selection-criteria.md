---
title: Pārdošanas cenu atlases kritēriju izveide
description: Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60a7c7230d4eb57d840121f6ee490bf829e0dc8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999660"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="77f11-103">Pārdošanas cenu atlases kritēriju izveide</span><span class="sxs-lookup"><span data-stu-id="77f11-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77f11-104">Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="77f11-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="77f11-105">Šīs procedūras veikšanai ir nepieciešams, lai vismaz viens pārdošanas cenu modelis būtu pieejams.</span><span class="sxs-lookup"><span data-stu-id="77f11-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="77f11-106">Šajā piemērā tiek izmantots cenu modelis Skaļruņa risinājuma pārdošanas cenas modelis paraugdatu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="77f11-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="77f11-107">Parasti produktu menedžeris izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="77f11-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="77f11-108">Jauna kritērija pievienošana esošajam pārdošanas cenas modelim</span><span class="sxs-lookup"><span data-stu-id="77f11-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="77f11-109">Noklikšķiniet uz Preces varianta modeļa definīcija.</span><span class="sxs-lookup"><span data-stu-id="77f11-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="77f11-110">Noklikšķiniet uz Preču konfigurācijas modeļi.</span><span class="sxs-lookup"><span data-stu-id="77f11-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="77f11-111">Sarakstā atlasiet rindu Skaļruņa risinājuma preces modelim, bet nenoklikšķiniet uz modeļa nosaukuma saites.</span><span class="sxs-lookup"><span data-stu-id="77f11-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="77f11-112">Darbību rūtī noklikšķiniet uz Modelis.</span><span class="sxs-lookup"><span data-stu-id="77f11-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="77f11-113">Noklikšķiniet uz Cenas modeļa kritēriji.</span><span class="sxs-lookup"><span data-stu-id="77f11-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="77f11-114">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="77f11-114">Click New.</span></span>
7. <span data-ttu-id="77f11-115">Laukā Nosaukums ierakstiet 'Debitoru grupa 10'.</span><span class="sxs-lookup"><span data-stu-id="77f11-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="77f11-116">Cenas modeļa kritērija nosaukums tiek izmantots, lai palīdzētu identificēt pamata atlases kritērijus.</span><span class="sxs-lookup"><span data-stu-id="77f11-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="77f11-117">Laukā Cenas modelis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="77f11-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="77f11-118">Laukā Pasūtījuma tips atlasiet Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="77f11-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="77f11-119">Pasūtījuma tips nosaka datu bāzes laukus, kas būs pieejami atlases vaicājumā.</span><span class="sxs-lookup"><span data-stu-id="77f11-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="77f11-120">Laukā Spēkā no ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="77f11-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="77f11-121">Laukā Beidzas pēc ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="77f11-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="77f11-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="77f11-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="77f11-123">Izveidot vaicājumu atlases kritērijiem</span><span class="sxs-lookup"><span data-stu-id="77f11-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="77f11-124">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="77f11-124">Click Edit.</span></span>
2. <span data-ttu-id="77f11-125">Laukā Tabula atlasiet Debitorus.</span><span class="sxs-lookup"><span data-stu-id="77f11-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="77f11-126">Laukā Lauks atlasiet Debitoru grupu.</span><span class="sxs-lookup"><span data-stu-id="77f11-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="77f11-127">Šajā piemērā atlases kritērijiem tiks izmantota noteikta debitoru grupa.</span><span class="sxs-lookup"><span data-stu-id="77f11-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="77f11-128">Laukā Kritēriji atlasiet debitoru grupu 10.</span><span class="sxs-lookup"><span data-stu-id="77f11-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="77f11-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="77f11-129">Click OK.</span></span>

