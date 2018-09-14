--- 
title: 'Izmaksu elementu izveide  '
description: "Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: bbaf4f7533d51d554d838e8e9e2aa05ca451298a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="create-cost-elements"></a><span data-ttu-id="238e0-103">Izmaksu elementu izveide  </span><span class="sxs-lookup"><span data-stu-id="238e0-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="238e0-104">Izmaksu elementus izmaksu uzskaitē var izveidot vairākos veidos.</span><span class="sxs-lookup"><span data-stu-id="238e0-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="238e0-105">Šajā procedūrā ir izskaidrots, kā izveidot izmaksu elementu, importējot galvenos kontus un izmantojot datu savienojumu.</span><span class="sxs-lookup"><span data-stu-id="238e0-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="238e0-106">Lai izveidotu šo procedūru, tika izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="238e0-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="238e0-107">Šī procedūra ir paredzēta līdzeklim Izmaksu uzskaite, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="238e0-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="238e0-108">Izveidot jaunus izmaksu elementus</span><span class="sxs-lookup"><span data-stu-id="238e0-108">Create new cost elements</span></span>
1. <span data-ttu-id="238e0-109">Dodieties uz sadaļu Izmaksu uzskaite > Dimensijas > Izmaksu elementa dimensijas.</span><span class="sxs-lookup"><span data-stu-id="238e0-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="238e0-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="238e0-110">Click New.</span></span>
3. <span data-ttu-id="238e0-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="238e0-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="238e0-112">Ievadiet vai atlasiet vērtību laukā Dimensiju elementu datu savienotājs.</span><span class="sxs-lookup"><span data-stu-id="238e0-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="238e0-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="238e0-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="238e0-114">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="238e0-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="238e0-115">Konfigurēt datu savienotāju</span><span class="sxs-lookup"><span data-stu-id="238e0-115">Configure the data connector</span></span>
1. <span data-ttu-id="238e0-116">Noklikšķiniet uz Konfigurēt dimensiju elementa nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="238e0-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="238e0-117">Ievadiet vai atlasiet vērtību laukā Kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="238e0-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="238e0-118">Atlasiet Koplietots, lai izmantotu koplietojamo kontu plānu.</span><span class="sxs-lookup"><span data-stu-id="238e0-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="238e0-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="238e0-119">Click New.</span></span>
4. <span data-ttu-id="238e0-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="238e0-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="238e0-121">Varat izmantot filtrus, lai atlasītu kontus, kas atbilst jūsu kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="238e0-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="238e0-122">Ievadiet vai atlasiet vērtību laukā No galvenā konta.</span><span class="sxs-lookup"><span data-stu-id="238e0-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="238e0-123">Ievadiet vai atlasiet vērtību laukā Uz galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="238e0-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="238e0-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="238e0-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="238e0-125">Importēt galvenos kontus</span><span class="sxs-lookup"><span data-stu-id="238e0-125">Import main accounts</span></span>
1. <span data-ttu-id="238e0-126">Noklikšķiniet uz Importēt dimensiju elementus.</span><span class="sxs-lookup"><span data-stu-id="238e0-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="238e0-127">Galvenie konti tiks importēti izmaksu uzskaitē un izmantoti kā izmaksu elementi.</span><span class="sxs-lookup"><span data-stu-id="238e0-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="238e0-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="238e0-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="238e0-129">Skatīt importētos kontus kā izmaksu elementus</span><span class="sxs-lookup"><span data-stu-id="238e0-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="238e0-130">Noklikšķiniet uz Skatīt dimensijas elementus.</span><span class="sxs-lookup"><span data-stu-id="238e0-130">Click View dimension members.</span></span>
    * <span data-ttu-id="238e0-131">Skatiet importētos virsgrāmatas kontus kā izmaksu elementus, uz kuriem var aizplūst izmaksas jūsu uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="238e0-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


