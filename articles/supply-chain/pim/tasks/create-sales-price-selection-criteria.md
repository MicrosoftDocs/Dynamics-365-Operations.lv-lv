---
title: Pārdošanas cenu atlases kritēriju izveide
description: Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920535"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="0c73b-103">Pārdošanas cenu atlases kritēriju izveide</span><span class="sxs-lookup"><span data-stu-id="0c73b-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c73b-104">Šajā procedūrā parādīts kā izveidot pārdošanas cenas atlases kritēriju atribūtam atbilstošu pārdošanas cenu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="0c73b-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="0c73b-105">Šīs procedūras veikšanai ir nepieciešams, lai vismaz viens pārdošanas cenu modelis būtu pieejams.</span><span class="sxs-lookup"><span data-stu-id="0c73b-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="0c73b-106">Šajā piemērā tiek izmantots cenu modelis Skaļruņa risinājuma pārdošanas cenas modelis paraugdatu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="0c73b-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="0c73b-107">Parasti produktu menedžeris izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="0c73b-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="0c73b-108">Jauna kritērija pievienošana esošajam pārdošanas cenas modelim</span><span class="sxs-lookup"><span data-stu-id="0c73b-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="0c73b-109">Dodieties uz **Preču informācijas pārvaldība \> Preces \> Preču konfigurācijas modeļi**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="0c73b-110">Sarakstā atlasiet rindu Skaļruņa risinājuma preces modelim, bet atlasiet modeļa nosaukuma saiti.</span><span class="sxs-lookup"><span data-stu-id="0c73b-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="0c73b-111">Darbību rūtī atlasiet **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="0c73b-112">Atlasiet **Cenas modeļa kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="0c73b-113">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-113">Select **New**.</span></span>
1. <span data-ttu-id="0c73b-114">Laukā **Nosaukums** ierakstiet 'Debitoru grupa 10'.</span><span class="sxs-lookup"><span data-stu-id="0c73b-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="0c73b-115">Cenas modeļa kritērija nosaukums tiek izmantots, lai palīdzētu identificēt pamata atlases kritērijus.</span><span class="sxs-lookup"><span data-stu-id="0c73b-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="0c73b-116">Laukā **Cenas modelis** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0c73b-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="0c73b-117">Laukā **Pasūtījuma tips** atlasiet *Pārdošanas pasūtījums*.</span><span class="sxs-lookup"><span data-stu-id="0c73b-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="0c73b-118">Pasūtījuma tips nosaka datu bāzes laukus, kas būs pieejami atlases vaicājumā.</span><span class="sxs-lookup"><span data-stu-id="0c73b-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="0c73b-119">Laukā **Spēkā no** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="0c73b-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="0c73b-120">Laukā **Beidzas pēc** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="0c73b-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="0c73b-121">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="0c73b-122">Izveidot vaicājumu atlases kritērijiem</span><span class="sxs-lookup"><span data-stu-id="0c73b-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="0c73b-123">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-123">Select **Edit**.</span></span>
2. <span data-ttu-id="0c73b-124">Laukā **Tabula** atlasiet *Debitorus*.</span><span class="sxs-lookup"><span data-stu-id="0c73b-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="0c73b-125">Laukā **Lauks** atlasiet *Debitoru grupu*.</span><span class="sxs-lookup"><span data-stu-id="0c73b-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="0c73b-126">Šajā piemērā atlases kritērijiem tiks izmantota noteikta debitoru grupa.</span><span class="sxs-lookup"><span data-stu-id="0c73b-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="0c73b-127">Laukā **Kritēriji** atlasiet *Debitoru grupu 10*.</span><span class="sxs-lookup"><span data-stu-id="0c73b-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="0c73b-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0c73b-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]